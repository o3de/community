# Keystone Slice Converter

A slice converter tool exists to convert Lumberyard slices and levels into O3DE prefabs. This tool is intended to be short-lived and will be discarded after slice code is removed from O3DE.

## Description

Given an input slice or level, this tool will produce an output prefab file with the same name and location (except ending in ".prefab") that can be used as a replacement for that slice or level.

## Usage

This tool is a part of SerializeContextTools.exe, which isn't built and distributed by default.  You'll need to build the project in Visual Studio, it's located at Code/Tools/SerializeContextTools/SerializeContextTools.

To use, open a command line and enter a line like the following:

    SerializeContextTools.exe convert-slice --specializations=editor --project-path=D:\github\o3de\AutomatedTesting --files=D:\github\o3de\AutomatedTesting\Levels\*.ly

Usage Notes:

- Slices convert the same way, just with ".slice" instead of ".ly"
- Wildcards are recursive, so it will match any nested subdirectory
- Wildcards are optional - you can convert a single file by specifying it directly.

Scary output:

The following warnings / errors are all expected, and don't mean that something has gone wrong.

 <table>
  <tr> <td>==================================================================
Trace::Warning
 D:\github\o3de\Code\Framework\AzCore\AzCore\Settings\SettingsRegistryMergeUtils.cpp(416): 'bool __cdecl AZ::SettingsRegistryMergeUtils::MergeSettingsToRegistry_ConfigFile(class AZ::SettingsRegistryInterface &,class AZStd::basic_string_view<char,struct AZStd::char_traits<char> >,const struct AZ::SettingsRegistryMergeUtils::ConfigParserSettings &)'
Unable to open file "D:\github\o3de\AutomatedTesting\Cache\pc\user.cfg"
==================================================================</td>
  </tr>
</table> 

GridMate Allocator has already started! Ignoring current allocator descriptor!

 <table>
  <tr> <td>==================================================================
Trace::Assert
 D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp(3363): (42484) '__cdecl AZ::LuaScriptCaller::LuaScriptCaller(class AZ::BehaviorContext *,class AZ::BehaviorMethod *)'
Argument const Render::OutputDeviceTransformType& for Method AcesParameterOverrides::preset::Setter doesn't have support to be converted to Lua!
------------------------------------------------
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (3365) : AZ::LuaScriptCaller::LuaScriptCaller
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (4563) : AZ::ScriptContextImpl::CreateLuaCaller
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (4588) : AZ::ScriptContextImpl::BindMethodOnStack
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (4875) : AZ::ScriptContextImpl::BindClassMethodAndProperties
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (5094) : AZ::ScriptContextImpl::BindClass
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (5429) : AZ::ScriptContextImpl::BindTo
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptContext.cpp (5764) : AZ::ScriptContext::BindTo
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptSystemComponent.cpp (193) : AZ::ScriptSystemComponent::AddContextWithId
D:\github\o3de\Code\Framework\AzCore\AzCore\Script\ScriptSystemComponent.cpp (87) : AZ::ScriptSystemComponent::Activate
D:\github\o3de\Code\Framework\AzCore\AzCore\Component\Entity.h (395) : AZ::Entity::ActivateComponent
D:\github\o3de\Code\Framework\AzCore\AzCore\Component\Entity.cpp (211) : AZ::Entity::Activate
D:\github\o3de\Code\Framework\AzFramework\AzFramework\Application\Application.cpp (261) : AzFramework::Application::StartCommon
D:\github\o3de\Code\Framework\AzToolsFramework\AzToolsFramework\Application\ToolsApplication.cpp (302) : AzToolsFramework::ToolsApplication::StartCommon
D:\github\o3de\Code\Framework\AzFramework\AzFramework\Application\Application.cpp (253) : AzFramework::Application::Start
D:\github\o3de\Code\Framework\AzToolsFramework\AzToolsFramework\Application\ToolsApplication.cpp (287) : AzToolsFramework::ToolsApplication::Start
D:\github\o3de\Code\Tools\SerializeContextTools\main.cpp (95) : main
D:\a01\_work\26\s\src\vctools\crt\vcstartup\src\startup\exe_common.inl (79) : invoke_main
D:\a01\_work\26\s\src\vctools\crt\vcstartup\src\startup\exe_common.inl (288) : __scrt_common_main_seh
D:\a01\_work\26\s\src\vctools\crt\vcstartup\src\startup\exe_common.inl (331) : __scrt_common_main
D:\a01\_work\26\s\src\vctools\crt\vcstartup\src\startup\exe_main.cpp (17) : mainCRTStartup
00007FF9A4047C24 (KERNEL32) : BaseThreadInitThunk
00007FF9A468D721 (ntdll) : RtlUserThreadStart
==================================================================</td>
  </tr>
</table> 

 <table>
  <tr> <td>==================================================================
Trace::Error
 D:\github\o3de\Code\Framework\AzCore\AzCore\Asset\AssetManager.cpp(718): 'void __cdecl AZ::Data::AssetManager::RegisterCatalog(class AZ::Data::AssetCatalog *,const struct AZ::Uuid &)'
Asset type {82557326-4AE3-416C-95D6-C70635AB7588} already has a catalog registered! New registration ignored!
==================================================================</td>
  </tr>
</table> 

 <table>
  <tr> <td>==================================================================
Trace::Error
 D:\github\o3de\Code\Framework\AzCore\AzCore\Asset\AssetManager.cpp(718): 'void __cdecl AZ::Data::AssetManager::RegisterCatalog(class AZ::Data::AssetCatalog *,const struct AZ::Uuid &)'
Asset type {6A1A3B00-3DF2-4297-96BB-3BA067A978E6} already has a catalog registered! New registration ignored!
================================================================== </td>
  </tr>
</table> 

 <table>
  <tr> <td>==================================================================
Trace::Warning
 D:\github\o3de\Code\Framework\AzCore\AzCore\UserSettings\UserSettings.cpp(31): 'void __cdecl AZ::UserSettingsInternal::AddSettings(class AZ::UserSettings *,unsigned int,unsigned int)'
There is no UserSettings handler for group 0, settings 475670885 will not be tracked!
==================================================================</td>
  </tr>
</table>

 <table>
  <tr> <td>==================================================================
Trace::Warning
 D:\github\o3de\Code\Framework\AzFramework\AzFramework\Spawnable\SpawnableSystemComponent.cpp(249): 'void __cdecl AzFramework::SpawnableSystemComponent::LoadRootSpawnableFromSettingsRegistry(void)'
No root spawnable assigned. The root spawnable can be assigned in the Settings Registry under the key '/Amazon/AzCore/Bootstrap/RootSpawnable'.
==================================================================</td>
  </tr>
</table> 


No Manifest found - ```<file>``` is a legacy Pak
 <table>
  <tr> <td>==================================================================
Trace::Error
 D:\github\o3de\Gems\AtomLyIntegration\AtomBridge\Code\Source\PerViewportDynamicDrawManager.cpp(49): 'void __cdecl AZ::AtomBridge::PerViewportDynamicDrawManager::UnregisterDynamicDrawContext(class AZ::Name)'
Attempted to call UnregisterDynamicDrawContext for unregistered name: "ViewportIconDisplay"
==================================================================</td>
  </tr>
</table> 

## Limitations

This tool will currently not handle the following correctly:

- Not supported by design: 
 - Legacy components.  All unrecognized components will get removed as a part of the conversion.  This is no different than what will happen if you open and resave that slice. 
   - There is a separate converter somewhere that can convert legacy rendering components to Atom components, it would need to be run first.
 - Component sort order components (EditorEntitySortComponent / EntityInspectorComponent).  The method of storing component sort order completely changed between slices and prefabs, with the data being stored on different types of components.  The tool doesn't have any specialized logic for converting data from one type of component to another, so while the EntityInspectorComponent itself will be converted, the data won't affect component sort order.
 - Transforms with non-uniform scale in them.  As a part of the conversion, the transforms will be saved out with a single scale value. 
   - There is a separate converter somewhere that can convert transforms with non-uniform scale into a transform with uniform scale plus a Non Uniform Scale component, it would need to be run first.
 - Any components that can't currently be serialized with the JSON serializer due to use of AZStd::any, AZStd::variant, AZStd::optional, custom serializers, serialization callbacks, etc.
 - Any entity references in the slice file that refer to entities outside of the slice file.  These will get reset to invalid IDs.  This can happen from systems like TrackView that auto-create components on entities being animated that have "backwards references" to the controlling sequence.
- Current limitations: 
  - Layers?  (Unknown, this has not been tested)
  - Slice instance entities that have been reparented underneath entities in other slices.  This also includes level entities that have been parented underneath slice entities. 
   - At a minimum, this would need to get the correct entity ID reference linkages
   - Ideally, for long-term prefab support, any entities that have been reparented under another slice should have the ownership transferred as well in the prefab world.  (i.e. instead of one Instance having an entity with a reference to another Instance, the entity should be moved to the other Instance via add/remove patches)
 - Standalone slices that have entity references "outside" of the slice data.  These simply can't be turned into equivalent prefab references without additional context in the converter as to where those references are intended to reference. 
   - One known cause of this is by using Trackview, following steps similar to the following: 
     - Create an entity.  Add a camera component to it.
     - Save the entity as a slice/prefab.
     - Open TrackView
     - Create new sequence
     - In Entity Inspector, select the camera entity
     - In TrackView, right-click and add selected entity
     - Save slice/prefab
     - Save level
 - Slice instances that have entity references that point "forward" to other slice instances that haven't been converted yet.
 - The serialized information about the component order is incorrect. See this PR for what the correct serialized form should look like : https://github.com/o3de/o3de/pull/8146/files

 - Levels having entities using Script Canvases might be broken after being converted by the tool if the Script Canvases have nodes with assigned entity IDs(For example: GetWorldTranslation, GetWorldTransform...).

**Error rendering macro 'jira'**
null

##### Updated Sept. 2022