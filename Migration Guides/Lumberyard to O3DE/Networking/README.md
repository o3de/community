# Lumberyard 1.X to O3DE Network Migration Guide

## Introduction

In Lumberyard 1.X, the networking and multiplayer layer was provided through the [GridMate](https://github.com/awsdocs/amazon-lumberyard-user-guide/blob/master/doc_source/network-intro.md) libraries. In O3DE, GridMate was entirely removed and replaced by a new modern multiplayer solution contained in [Multiplayer](https://www.o3de.org/docs/user-guide/gems/reference/multiplayer/) gem and [AzNetworking](https://www.o3de.org/docs/user-guide/networking/) library. This document outlines how developers should approach migrating  between the two systems and approximate translation of concepts involved. The audience for this documentation are game multiplayer developers who are using GridMate in LY 1.X and are familiar with general concepts in game multiplayer topics.

## Concepts

This document provides an initial guide for translating legacy Lumberyard Gridmate concepts to O3DE multiplayer concepts. Keep in mind that this is a rough comparison guide as the two networking system are different in their approaches and implementations and are incompatible.

O3DE relies heavily on autocomponents to define networked properties and RPCs. See the tutorial https://www.o3de.org/docs/learning-guide/tutorials/multiplayer/first-multiplayer-component/ for an example that works you through creating network autocomponents.

The table below is meant as a suggested starting point of where to look to achieve a similar legacy behavior.
| **Lumberyard Concept**  | **O3DE Equivalent**  |
| :------------: | :------------: |
| Network/Network Binding Component  | Multiplayer/Network Binding Component  |
| GridMate::Replica | Multiplayer::EntityReplicator |
| NetBindable and ReplicaChunk | AutoComponent |
| GridMate::DataSet | Network Property in AutoComponent.xml |
| GridMate::Rpc | RemoteProcedure in AutoComponent.xml |
| GridMate::ReplicaManager | INetworkEntityManager |
| Gridmate::Marshaler | Serialize(AzNetworking::ISerializer&) |
| GridMate::Channel | IConnectionListener + INetworkInterface |

## Network/Network Binding Component → Multiplayer/Network Binding Component

In order to mark an entity as a network entity, one has to attach a Network Binding component to the entity in the Editor. Both the legacy and O3DE components are similarly named except that in O3DE, this component has a different category - "Multiplayer" instead of "Network". Note, in practice in O3DE you will want to add both Network Binding and Network Transform components, for an entity to appear on multiplayer clients.

## GridMate::Replica → Multiplayer::EntityReplicator

In LY, a multiplayer entity had a one to one counterpart called GridMate::Replica. In O3DE, the closest type is a Multiplayer::EntityReplicator. It acts as a behind-the-scenes tool that turns a regular game entity into a network entity. Entity Replicators are created for you for any entity that is marked as a network entity.

## NetBindable and ReplicaChunk → AutoComponent

In the legacy system, in order to turn a component into a network component, one had to perform a certain amount of C++ work, such as inheriting from NetBindable interface and implementing a number of API calls. In O3DE, this approach is replaced with a code-generated system. It begins with an XML file.

    <Component
        Name="NetworkTransformComponent" 
        Namespace="Multiplayer" 
        OverrideComponent="true" 
        OverrideController="true" 
        OverrideInclude="Multiplayer/Components/NetworkTransformComponent.h"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    </Component>

During the build process, such an XML file will be turned into a multiplayer component.

See the following links on the documentation:
- https://www.o3de.org/docs/user-guide/gems/reference/multiplayer/multiplayer-gem/autocomponents/
- https://www.o3de.org/docs/learning-guide/tutorials/multiplayer/first-multiplayer-component/

## GridMate::DataSet → Network Property in AutoComponent.xml

A DataSet in the legacy system represented a single replicated property. https://github.com/awsdocs/amazon-lumberyard-user-guide/blob/master/doc_source/network-replicas-data-sets.md

In O3DE a single replicated property is defined in XML auto-component using Network Property element. Here is an example at https://github.com/o3de/o3de/blob/5abfb831da4be6da6792fc0f91be377973b5b3ea/Gems/Multiplayer/Code/Source/AutoGen/NetworkTransformComponent.AutoComponent.xml#L16

    <Component
    ...
        <NetworkProperty Type="AZ::Vector3" Name="translation" Init="AZ::Vector3::CreateZero()" ReplicateFrom="Authority" ReplicateTo="Client" IsRewindable="true" IsPredictable="true" IsPublic="true" Container="Object" ExposeToEditor="false" ExposeToScript="false" GenerateEventBindings="true" />
    ...
    </Component>

## GridMate::Rpc → RemoteProcedure in AutoComponent.xml

A remote procedure is the legacy system was created using C++ template GridMate::Rpc. In O3DE, a remote procedure is defined in XML component definitions.

Here is an example https://github.com/o3de/o3de/blob/5abfb831da4be6da6792fc0f91be377973b5b3ea/Gems/Multiplayer/Code/Source/AutoGen/NetworkRigidBodyComponent.AutoComponent.xml#L16

    <Component ...>
    ...
        <RemoteProcedure Name="SendApplyImpulse" InvokeFrom="Server" HandleOn="Authority" IsPublic="true" IsReliable="true" GenerateEventBindings="false" Description="Applies an impulse">
            <Param Type="AZ::Vector3" Name="impulse" />
            <Param Type="AZ::Vector3" Name="worldPoint" />
        </RemoteProcedure>
    </Component>

## GridMate::ReplicaManager → INetworkEntityManager

In the legacy system, a replica manager was a central place to access replica objects. In O3DE a similar object is called a Network Entity Manager, which can be access via the following global function Multiplayer::GetNetworkEntityManager()

    // an example of using O3DE's network entity manager
    Multiplayer::GetNetworkEntityManager()->GetEntity(NetEntityId);

## Gridmate::Marshaler → Serialize(AzNetworking::ISerializer&)

In the legacy system, one can define a custom way to serialize data over the network by specifying a custom Marshaler class. In O3DE, the same can be achieved by specifying a member function Serialize(AzNetworking::ISerializer&). Here is an example https://github.com/o3de/o3de/blob/5abfb831da4be6da6792fc0f91be377973b5b3ea/Gems/Multiplayer/Code/Include/Multiplayer/MultiplayerTypes.h#L126

        struct PrefabEntityId
        {
            AZ::Name m_prefabName;
    ...
            bool Serialize(AzNetworking::ISerializer& serializer);
        };
    
        inline bool PrefabEntityId::Serialize(AzNetworking::ISerializer& serializer)
        {
            serializer.Serialize(m_prefabName, "prefabName");
            return serializer.IsValid();
        }

## GridMate::Channel → INetworkInterface and IConnectionListener

GridMate's channel functionality offers multiple independent streams of communication. Channels were designed with the intention of compartmentalizing different types of communication. AzNetworking does not provide an explicit mechanism for this like Channels but can accomplish similar using IConnectionListener and INetworkInterface.

As previously discussed, AzNetworking defines packets through XML. For each group of definitions, a corresponding IConnectionListener is implemented to handle those packet types. An INetworkInterface implementation is then created using the IConnectionListener as a means to route traffic to those handlers. MultiplayerSystemComponent is an excellent example of this. Through this mechanism, different types of communication can be easily compartmentalized.

INetworkInterface provides the mean to have multiple connections of various types. As an example of this combined in practice consider MultiplayerSystemComponent and MultiplayerEditorConnection.

As described, MultiplayerSystemComponent implements an IConnectionListener to handle routine Multiplayer packet types.

**MultiplayerSystemComponent**

            bool IsHandshakeComplete(AzNetworking::IConnection* connection) const;
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::Connect& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::Accept& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::ReadyForEntityUpdates& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::SyncConsole& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::ConsoleCommand& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::EntityUpdates& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::EntityRpcs& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::RequestReplicatorReset& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerPackets::ClientMigration& packet);
        
            //! IConnectionListener interface
            //! @{
            AzNetworking::ConnectResult ValidateConnect(const AzNetworking::IpAddress& remoteAddress, const AzNetworking::IPacketHeader& packetHeader, AzNetworking::ISerializer& serializer) override;
            void OnConnect(AzNetworking::IConnection* connection) override;
            AzNetworking::PacketDispatchResult OnPacketReceived(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, AzNetworking::ISerializer& serializer) override;
            void OnPacketLost(AzNetworking::IConnection* connection, AzNetworking::PacketId packetId) override;
            void OnDisconnect(AzNetworking::IConnection* connection, AzNetworking::DisconnectReason reason, AzNetworking::TerminationEndpoint endpoint) override;
            //! @}

Meanwhile, MultiplayerEditorConnection implements packet types to facilitate setting up Multiplayer debugging in the Editor.

**MultiplayerEditorConnection**

            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerEditorPackets::EditorServerReadyForLevelData& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerEditorPackets::EditorServerLevelData& packet);
            bool HandleRequest(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, MultiplayerEditorPackets::EditorServerReady& packet);
            
            //! IConnectionListener interface
            //! @{
            AzNetworking::ConnectResult ValidateConnect(const AzNetworking::IpAddress& remoteAddress, const AzNetworking::IPacketHeader& packetHeader, AzNetworking::ISerializer& serializer) override;
            void OnConnect(AzNetworking::IConnection* connection) override;
            AzNetworking::PacketDispatchResult OnPacketReceived(AzNetworking::IConnection* connection, const AzNetworking::IPacketHeader& packetHeader, AzNetworking::ISerializer& serializer) override;
            void OnPacketLost([[maybe_unused]]AzNetworking::IConnection* connection, [[maybe_unused]]AzNetworking::PacketId packetId) override {}
            void OnDisconnect([[maybe_unused]]AzNetworking::IConnection* connection, [[maybe_unused]]AzNetworking::DisconnectReason reason, [[maybe_unused]]AzNetworking::TerminationEndpoint endpoint) override {}
            //! @}

In this case, each IConnectionListener implementation run on their own INetworkInterfaces. Each INetworkInterface can be configured in terms of protocol usage, timeouts, etc. In this way, different groups of packets can be easily encapsulated in separate connections. Each INetworkInterface is a separate connection and will consequently require distinct ports.

## Console Commands

In O3DE many of the [console function commands](https://www.o3de.org/docs/user-guide/networking/settings/#networking-commands) have been renamed to reflect new behaviours.

- mphost → host
- mpjoin → connect
- mpdisconnect → disconnect
- map → loadlevel

## Resources

O3DE Multiplayer:
https://www.o3de.org/docs/user-guide/gems/reference/multiplayer/
https://github.com/o3de/o3de/tree/development/Gems/Multiplayer
https://github.com/o3de/o3de-multiplayersample

Legacy:
https://github.com/awsdocs/amazon-lumberyard-user-guide/blob/master/doc_source/network-intro.md

##### Updated Aug 2022