**SIG <Template> Charter**

This charter adheres to the Roles and Organization Management specified in <sig-governance>.
 Team information may be found in the <readme.md>

**Overview of SIG**

Two concise lines explaining what this SIG does with bullet points of the major responsibilities

- Responsibility 1

**Goals**

- Major goals that SIG seeks to generally achieve

**Scope**
Rendering:
Publish GPU/Video hardware driver compatibility, supported versions, and requirements per platform.

Design and manage Material authoring, workflow, and editor.

DCC scripting interface to renderer - Interaction with 3rd party tools (maya/houdini/substance/etc)

Publish pipeline API and specification for user generated script integration support to manipulate asset pipelines.

Audio
Design and maintain architecture of engine audio API subsystem for integration.
Publish audio hardware driver compatibility, supported versions, and requirements per platform.
Design, produce specification, and maintain client side authoring component into 3rd party audio subsystem.
*Need Eric Phister to clarify audio playback details

AR/VR
Design and maintain common AR & VR Architecture API for engine integration
Design and maintain head tracking, object anchoring, and user interaction API to normalize and scale engine world space to AR & VR coordinate space.
Design and maintain VR stereo scopic rendering support.
Publish and maintain AR/VR device, SDK, and driver support.
Design and implement interface driver support

**In scope**

Design and manage feature of shader language and toolchain (AZSL/HLSL - AZSL C compiler)
Design and matain Rendering Pipeline Interface (RPI) (Application interface) pass system 
Design and matain Rendering Hardware Interface (RHI) (low level interface) to add or support new platforms (Vulkan/RT, Metal, DirectX 12, DXR/Raytracing)

**Cross-cutting Processes**

Publish and maintain data specification of renderer mesh, material, shader and texture formats for external file format groups. (example gltf to array of vertex points for rendering)

Design and maintain code for Mesh, material, shader, and texture builders from file format parser output to renderer asset format.

Support rendering of blend shapes from animation system, but not responsible for authoring of blend shapes.

Provide support, design, and guidance for GPU related subsystem support for 3rd party features. 

**Out of Scope**

Not responsible for the ingestion or export system for assets.
Not responsible for the builder queue system in AP. 
Not responsible for maintaining audio driver and hardware subsystem compatibility.
Not responsible for 3rd party authoring tool support, but may advise and refer to 3rd party.


**SIG Links and lists:**

- Joining this SIG
- Slack/Discord
- Mailing list
- Issues/PRs
- Meeting agenda & Notes

**Roles and Organization Management**

SIG Docs adheres to the standards for roles and organization management as specified by <sig-governance>. This SIG opts in to updates and modifications to <sig-governance>

**Individual Contributors**

Additional information not found in the sig-governance related to contributors.

**Maintainers**

Additional information not found in the sig-governance related to contributors

**Additional responsibilities of Chairs**

Additional information not found in the sig-governance related to SIG Chairs

**Subproject Creation**

Additional information not found in the sig-governance related to subproject creation

**Deviations from sig-governance**

Explicit Deviations from the sig-governance