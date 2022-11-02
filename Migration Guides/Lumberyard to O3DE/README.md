# Transitioning a project from Lumberyard (LY) to Open 3D Engine (O3DE)

This document covers high level considerations when transitioning a document from Lumberyard to O3DE. This document is living and will grow over time as users add their own transition experiences and advice.

**Requirements:**
- This guide focuses on the latest Lumberyard version, which is 1.28. Any conversion tools are authored assuming 1.28. If the project is not on 1.28, please see **In Progress Page** on how to upgrade your project to Lumberyard 1.28. 
- Transitioning a Lumberyard project to O3DE is best performed utilizing a source code version of O3DE. This is available at https://github.com/o3de/o3de

**Suggested sites (Open 3D Engine documentation, tutorials, downloads):**
- Open 3D Engine Documentation https://www.o3de.org/docs/
- Open 3D Engine Website https://www.o3de.org/
- Open 3D Engine Discord https://discord.gg/o3de
- Open 3D Engine Download https://www.o3de.org/download/
- Open 3D Engine Tutorials and Samples https://www.o3de.org/docs/learning-guide/
- Open 3D Engine Video Tutorials https://www.youtube.com/c/Open3DEngine
- Open 3D Engine O3DCon 2021 videos https://www.youtube.com/playlist?list=PLCQwFpnHSZQgkw7MdNQwagKKKvywt6b80

## Tutorials and Documents

|                                                             **Table of Contents**                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------:|
|                                                                   **EMFX**                                                                    |
|                                     [Migration guideline for animation: From Lumberyard to O3DE](./EMFX)                                      |
|                                                                **Networking**                                                                 |
|                                        [Lumberyard 1.X to O3DE Network Migration Guide](./Networking)                                         |
|                                                              **Other Documents**                                                              |
|                                 [Fbx Motion Sampling Settings](./Misc-Documents/FBX-Motion-Sampling-Settings)                                 |
|                                              [Slice Converter](./Misc-Documents/Slice-Converter)                                              |
|                            [Lumberyard features with no equivalent in O3DE](./Misc-Documents/Lumberyard-Features)                             |
|                                                                  **Scripts**                                                                  |
|                               [convert_physxconfiguration](./Misc-Documents/Scripts/convert_physxconfiguration)                               |
|                                  [convert_editor_game_xml](./Misc-Documents/Scripts/convert_editor_game_xml)                                  |
|                                                                 **Tutorials**                                                                 |
| [Converting a Legacy Renderer Project to an Atom Project](./Misc-Documents/Tutorials/Converting-a-Legacy-Renderer-Project-to-an-Atom-Project) |
|                  [Legacy Asset Conversion Utility (StarterGame)](./Misc-Documents/Tutorials/Legacy-Asset-Conversion-Utility)                  |
|                                    [StarterGame on Atom](./Misc-Documents/Tutorials/Starter-Game-On-Atom)                                     |
|                                                                   **Other**                                                                   |
|                     [SerializeContextTools Conversion Scripts](./Misc-Documents/SerializeContextTools-Conversion-Scripts)                     |

## Considerations when transitioning a project from Lumberyard to O3DE

**Renderer:** The O3DE renderer is referred to as Atom. The entire geometry, shader, and rendering pipeline has been completely re-architected for O3DE. Lumberyard features a deferred renderer, whereas O3DE utilizes a forward renderer.

**Entities:** `<slices vs prefabs high level>`

**EMFX:** `<atom vs lumberyard high level>`

**Audio:** `<both use wwise, different versions>`

**Physics:** PhysX gem components are mostly compatible with LY 1.28. There are changes in Physics API which would require manual update of the code where AzFramework::Physics was used. Now there's a new namespace AzPhysics, but the conversion of the code should be straight forward.

**Viewport:** (May not be much of a conversion issue, unless team modified the editor)

**Gems:** Lumberyard gems are not compatible with O3DE. Conversion will require finding O3DE version of the gem, or recompiling the gem for O3DE. 

**Editor Plugins/tools:** `<need info here>`

**Platforms:** Lumberyard publicly supports Windows (editor + runtime), Linux Server (runtime), iOS (runtime), and Android (runtime). O3DE supports Windows (editor + runtime), Linux (editor + runtime), Linux Server (runtime). iOS and Android are currently in development.

**Terrain:**

**Particles:** O3DE does not have a built-in particle system. Conversion will require integrating a 3rd party particle system, usually via a gem. [PopcornFX](https://www.popcornfx.com/plugin-o3de/) has an integration with O3DE.

**Networking:**

**Asset Processing:**

**PathFinding/AI:**
* [Kythera](https://www.kythera.ai/o3de-download) has an integration with O3DE. 

* O3DE also offers an open-source [navigation gem](https://www.o3de.org/docs/user-guide/gems/reference/ai/recast/recast-navigation/) based on Recast/Detour.

## Tools available to assist with Lumberyard to O3DE conversion

[SerializeContextTools Conversion Scripts](./Misc-Documents/SerializeContextTools-Conversion-Scripts/README.md)<br>
[Script - convert_physxconfiguration](./Misc-Documents/Scripts/convert_physxconfiguration/README.md)<br>
[Script - convert_editor_game_xml](./Misc-Documents/Scripts/convert_editor_game_xml/README.md)<br>
[Slice Converte](./Misc-Documents/Slice-Converter/README.md)<br>

## Lumberyard features with no equivalent in  O3DE

[Lumberyard features](./Misc Documents/Lumberyard-Features/README.md)

## Network systems LY to O3DE

There is no automated path to port network components and logic from Lumberyard's Gridmate → to O3DE's Networking 2.0. Networking in O3DE is based on new systems so migration will require how to port “concepts” and intent, rather than actual assets and code.

See [Networking migration guide](./Networking/README.md) for more details.

## Script Canvas

**In Progress**

## Material Conversions

Differences in the Engines (note we should pull the data into the doc)
[Lumberyard features with no equivalent in O3DE](./Misc-Documents/Lumberyard-Features)

Any Texture and Material will be required to be re-witten due to the change in the rendering system. The best way to do this would to use the source files and import them into O3DE and build new materials. See below for guides on this topic
<u>Materials:</u> https://www.o3de.org/docs/atom-guide/look-dev/materials/
<u>Textures:</u> https://www.o3de.org/docs/atom-guide/look-dev/textures/


## EMFX

[EMFX](./EMFX/)

**Actor Asset**
The most significant change to the actor asset from Lumberyard 1.28 to O3DE is that `EMotionFX::Mesh` has been deprecated and replaced with the Atom mesh format (`Atom::Model`). Previously in Lumberyard 1.28, all export settings related to actor (skinned mesh) can be found under the actor tab in fbx settings. In O3DE, due to the usage of the atom mesh format, export settings related to the mesh have moved under the mesh tab. This step currently has to be performed manually following the steps below.

**Motion Asset**
The most noticeable improvement from Lumberyard 1.28 to O3DE around motion is that the system behind sampling motion has been re-written from scratch. This change has significantly improved the efficiency and quality of motion sampling. It offers both uniform and non-uniform sampling method options. If you want to learn more about the in-depth technical aspect of motion sampling improvement, see this article.  (Link to Misc-Documents/FBX-Motion-Sampling-Settings/)

**Animation Editor**
Since Lumberyard 1.28 we have removed all OpenGL rendering inside of the animation editor and replaced it with the Atom renderer. The new Atom render window has replaced the OpenGL render viewport. As a result, any user custom layout that still references the OpenGL render window will report a warning when opening and will not load any viewport window. We also made many more UX/UI improvements throughout the animation editor.

## Project Conversion (WAF to CMake)

Considerations for building when moving from Lumberyard to O3DE
Lumberyard uses WAF, O3DE uses Cmake therefor does not map 1:1

To learn more about the new CMake and how to best utilize it, checkout this dev series;
| **CMake Essentials** |
| :------------: |
| [CMake Essentials - Part 1](https://www.o3de.org/blog/posts/cmake-essentials-series-part-1/ ) |
| [CMake Essentials - Part 2](https://www.o3de.org/blog/posts/cmake-essentials-series-part-2/ ) |
| [CMake Essentials - Part 3](https://www.o3de.org/blog/posts/cmake-essentials-series-part-3/ ) |
| [CMake Essentials - Part 4](https://www.o3de.org/blog/posts/cmake-essentials-series-part-4/ ) |

## Particle Systems

Particle system does not exist in O3DE, therefor you will need to use a 3rd party solution such as PopcornFX.

**PopcornFX - Gem**

 Real-time FX solution for particle effects Multi-platform & cross engine for games, films & AR/VR/MR Source code of the gem is available for everyone, can be freely used, modified and shared under the Community License terms.

<u>Website:</u> https://www.popcornfx.com/
<u>Asset Repo:</u> https://github.com/PopcornFX/O3DEPopcornFXPlugin
<u>Example Project:</u> https://github.com/PopcornFX/O3DEPopcornFXExamples
<u>Installation:</u> https://www.popcornfx.com/docs/plugins/o3de-gem/gem-installation/
<u>Discord:</u> https://discord.gg/4ka27cVrsf
Version and Specs O3DE Version: 21.11, 21.11.2 or greater

## Prefabs

**In Progress**

## Lumberyard Documentation. 

#### Amazon Lumberyard User Guide

https://github.com/awsdocs/amazon-lumberyard-user-guide

#### Amazon Lumberyard Getting Started Guide

https://github.com/awsdocs/amazon-lumberyard-getting-started-guide

#### Lumberyard Release Notes

https://github.com/awsdocs/amazon-lumberyard-release-notes



##### Updated Sept 2022