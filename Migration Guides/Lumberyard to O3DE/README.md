# Transitioning a project from LY to O3DE

This document covers high level considerations when transitioning a document from Lumberyard to O3DE. This document is living and will grow over time as users add their own transition experiences and advice.

**Requirements:**
- The project is currently utilizing Lumberyard 1.28. Any conversion tools are authored assuming 1.28. If the project is not on 1.28, please see https://wiki.agscollab.com/display/lmbr/Migration+Guide+-+Ly1.x+to+O3DE on how to upgrade your project to Lumberyard 1.28. 
- Transitioning a Lumberyard project to O3DE is best performed utilizing a source code version of O3DE. This is available at https://github.com/o3de/o3de

**Suggested sites (Open 3D Engine documentation, tutorials, downloads):**
- Open 3D Engine Documentation https://www.o3de.org/docs/
- Open 3D Engine Website https://www.o3de.org/
- Open 3D Engine Discord https://discord.gg/o3de
- Open 3D Engine Download https://www.o3de.org/download/
- Open 3D Engine Tutorials and Samples https://www.o3de.org/docs/learning-guide/
- Open 3D Engine Video Tutorials https://www.youtube.com/c/Open3DEngine
- Open 3D Engine O3DCon 2021 videos https://www.youtube.com/playlist?list=PLCQwFpnHSZQgkw7MdNQwagKKKvywt6b80

## Considerations when transitioning a project from Lumberyard to O3DE

**Renderer:** The O3DE renderer is referred to as Atom. The entire geometry, shader, and rendering pipeline has been completely re-architected for O3DE. Lumberyard features a deferred renderer, whereas O3DE utilizes a forward renderer.

**Entities:** `<slices vs prefabs high level>`

**EMFX:** `<atom vs lumberyard high level>`

**Audio:** `<both use wwise, different versions>`

**Physics: **PhysX gem components are mostly compatible with LY 1.28. There are changes in Physics API which would require manual update of the code where AzFramework::Physics was used. Now there's a new namespace AzPhysics, but the conversion of the code should be straight forward.

**Viewport:** (May not be much of a conversion issue, unless team modified the editor)

**Gems:** Lumberyard gems are not compatible with O3DE. Conversion will require finding O3DE version of the gem, or recompiling the gem for O3DE. 

**Editor Plugins/tools:** `<need info here>`

**Platforms:** Lumberyard publicly supports Windows (editor + runtime), Linux Server (runtime), iOS (runtime), and Android (runtime). O3DE supports Windows (editor + runtime), Linux (editor + runtime), Linux Server (runtime). iOS and Android are currently in development.

**Terrain: **

**Particles:** O3DE does not have a built in particle system. Conversion will require integrating a 3rd party particle system, usually via a gem. Currently PopcornFX has a 

**Networking:**

**Asset Processing:**

**PathFinding/AI:**
`<Other areas I am missing>`

## Tools available to assist with Lumberyard to O3DE conversion

**insert tools here**

##Lumberyard features with no equivalent in  O3DE

(Link to /Misc Documents/Lumberyard-Features.md)

##### Updated Aug 2022