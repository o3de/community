# Open 3D Engine Release: 22.05

## SIG-Build 

### Build Systems 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Github Pipelines | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | <div>https://github.com/o3de/o3de/tree/development/.github</div> | https://www.o3de.org/docs/contributing/to-code/git-workflow/ | | |
| Jenkins Pipelines | 🟡 Active | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🔵 In Progress | All  | <div>https://github.com/o3de/o3de/tree/development/scripts/build/Jenkins</div> | <div><div>https://github.com/o3de/sig-build/blob/main/AutomatedReview/JenkinsPipelineGuide.md</div></div> | | |
| Installer Builds | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | Windows Linux  | <div>https://github.com/o3de/o3de/tree/development/cmake/Platform/Windows</div><div><br></div><div><div>https://github.com/o3de/o3de/tree/development/cmake/Platform/Linux</div></div> | || | |
| Build Failure Analysis | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | || <div><div>https://github.com/o3de/sig-build/blob/main/AutomatedReview/RootCauseRunbook.md</div></div> | | |
| Build Scripts | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | <div><div>https://github.com/o3de/o3de/tree/development/scripts/build/Platform</div></div> | || | |
| Build Environments | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | <div>https://github.com/o3de/o3de/tree/development/scripts/build/build_node/Platform</div> | || | |
| Build Metrics | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | <div>https://github.com/o3de/o3de/tree/development/scripts/build</div> | || | |
| 3rd Party System | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | <div>https://github.com/o3de/3p-package-source</div> | || | |
### Infrastructure 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Jenkins | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | <div>https://github.com/o3de/o3de/tree/development/scripts/build/Jenkins</div> | <div>https://www.o3de.org/docs/contributing/to-code/git-workflow/</div> | | |
| Github | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | <div>https://github.com/o3de/o3de/tree/development/.github</div> | || | |
| LFS | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | || || | |
| License Scanning | 🟡 Active | 🟢 Complete | 🟢 Complete | 🔵 In Progress | 🔵 In Progress | All  | <div>https://github.com/o3de/o3de/tree/development/scripts/license_scanner</div> | || | |
## SIG-Content 

### Frameworks 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| AzToolsFramework | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All | || || | |
| Lua | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All | || https://www.o3de.org/docs/user-guide/scripting/lua/ | | |
| Prefabs | || || || || || || || || | |
| Qt for Python | || || || || || || || || | |
### Editor 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Asset Browser | 🟡 Active | 🔵 In-Design | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | Windows Linux MacOS  | || || | |
| Framework | || || || || || || || || | |
| Localization | || || || || || || || || | |
| Undo / Redo | || || || || || || || || | |
| Asset Editor | 🔵 Backlogged | 🟠 Minimal | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | Windows Linux MacOS  | || || | |
### Canvas Tools 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Graph Model | 🟡 Active | 🟠 Minimal | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || | |
| Graph Canvas | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || | |
| Landscape Canvas | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | Windows Linux MacOS  | || || | |
### Project Manager 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Remote Projects | 🟡 Active | 🔵 In-Design | ⭕ Not Required | 🔵 In Progress | 🔵 In Progress | Windows Linux  | || || Still in early design  |
| Project versioning | 🟡 Active | 🔵 In-Design | ⭕ Not Required | 🔵 In Progress | 🔵 In Progress | Windows Linux  | || || Still in early design  |
| Template Management | 🟠 Planned | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux  | || || | |
| Gem Creation Wizard | 🟠 Planned | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux  | || || | |
| Remote Gems Improvements (URI vs URL) | 🟠 Planned | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux  | || || | |
| Remote Gems (Initial) | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | Windows Linux  | || || | |
### Scripting 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Expression Evaluation | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All | || || | |
| Script Canvas | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | Windows Linux MacOS  | || https://www.o3de.org/docs/user-guide/scripting/script-canvas/ | | |
| Script Canvas Developer | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | Windows Linux MacOS  | || || | |
| Script Events | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All | || https://www.o3de.org/docs/user-guide/scripting/script-events/ | | |
| Script Canvas Testing | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🟢 Optimized | Windows Linux MacOS  | || || Unit Testing framework in Script Canvas  |
| Lua Editor | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || https://www.o3de.org/docs/user-guide/scripting/lua/ | | |
### User Interface 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| LyShine (2D Render) | 🟡 Active | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || | |
### Animation 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Animation Playback Control | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Pose Blending | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Animation Syncing | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Motion Events | 🔵 Backlogged | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Bone Masking | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Motion Extraction (Root Motion) | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Motion Matching | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟡 Experimental | 🔵 In Progress | All  | || || | |
| Debug Rendering | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Animation Sharing | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Animation Compression | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Multi-threading | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Retargeting | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || There is currently no IK retargeting  |
| Inverse Kinematics (IK) | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || There is currently no full-body IK  |
| LOD | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Blend Tree/State Machine | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Transition Conditions | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Wildcard Conditions | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Debugging Tools (Anim Graph) | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || This is complete, but the anim graph static analyzer is still planned and on the backlog  |
| Visual Tools | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Software Skinning (Linear, Dual-Quat) | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| GPU Skinning (Linear, Dual-Quat) | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Morph Target/Facial Animation | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| GPU Accelerated Morphing | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Simulated Objects/Dynamic Bones | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || To improve stability and simulation quality this could be ported to use PhysX  |
| Ragdoll Runtime | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟡 Experimental | 🔵 In Progress | All  | || || | |
| Cloth Authoring | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Collider Authoring Tools | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🔵 In Progress | 🔵 In Progress | All  | || || | |
| Attachments | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Skinned Attachments | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
### World Building 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Terrain | 🟡 Active | 🟠 Minimal | ❌ None | 🟡 Experimental | 🟡 Needs Optimization | Windows | || || | |
| Dynamic Vegetation | 🟢 Complete | 🟢 Complete | 🟠 Partial | 🟢 Stable | 🟡 Needs Optimization | All | || || | |
### Viewport 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Manipulators | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || Manipulators for interacting with entities and components in the viewport  |
| Component Mode | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🔵 In Progress | 🔴 Needs Testing | Windows Linux MacOS  | || || Editing mode for Components in the main viewport  |
| Viewport UI | 🟡 Active | 🟠 Minimal | ⭕ Not Required | 🔵 In Progress | 🔴 Needs Testing | Windows Linux MacOS  | || || Qt UI elements that can be dynamically added/removed from the viewport  |
| Interaction Model | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | Windows Linux MacOS  | || || Interaction Model for working with Entities and Prefabs in the viewport  |
| Camera | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || CameraInput and ModularViewportCameraController for adjusting and interacting with the camera in the Editor  |
| View Bookmarks | 🟡 Active | 🟠 Minimal | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows Linux MacOS  | || || Support for storing view transforms in the Editor  |
| Manipulator Test Framework | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || Provides ability to write integration tests for manipulator interactions (screen-space to world-space transformations)  |
| Visibility | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | Windows Linux MacOS  | || || Visibility system to determine entities that fall inside the editor view frustum  |
| Editor Mode Visual Feedback | 🟡 Active | 🟠 Minimal | ⭕ Not Required | 🟡 Experimental | 🔵 In Progress | Windows Linux MacOS  | || || Covers screen space effects to communicate viewport state (e.g. Selection, Focus Mode etc..)  |
### White Box Tool 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Atom Integration | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || Atom rendering support for the White Box Tool  |
| Viewport Editing | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || Interaction Model for White Box Tool viewport editing  |
| Triangulation | 🔵 Backlogged | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux MacOS  | || || | |
| Boolean Operations | 🔵 Backlogged | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux MacOS  | || || | |
| Custom UV Mapping | 🔵 Backlogged | ❌ None | ⭕ Not Required | ❌ Unproven | ❌ Unsupported | Windows Linux MacOS  | || || | |
## SIG-Core 

### Core features 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| AzCore | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| AzFramework | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Math libraries | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| SDK Build | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | Windows Linux MacOS  | || || | |
| Reflection frameworks | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | All  | || || | |
| Streaming system | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | All  | || || | |
| Input system | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || || | |
| Logging and tracing | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | All  | || || | |
| || || || || || || || || || | |
| Profiling | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔵 In Progress | Windows  | || || | |
| Opimised standard library | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | All  | || || | |
### Physics API (minimal, non-backend specific) 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Collision Filtering | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | || || || | |
| Collision Filtering - Programmable Reserved Bits | 🔵 Backlogged | ❌ None | || || || || || || | |
| Joints | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | || || || | |
| Rigid Bodies | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | || || || | |
| Multiple Scenes | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | || || || Need to figure out workflow.  |
| Character Controller | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | || || || Improvements in backlog/roadmap.  |
| Ragdoll | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | || || || Improvements in backlog/roadmap.  |
| Materials | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | || || || Major workflow improvements under way.  |
| Shapes | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | || || || | |
| Heightfields | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | || || || | |
| Wind | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | || || || | |
| Scene Queries | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | || || || | |
### Nvidia PhysX Integration 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Ticking | 🔵 Backlogged | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | All  | || || | |
| Rigid Body Simulation | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | All  | || || | |
| Continuous Collision Detection (CCD) | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Collision Asset Pipeline | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Convex Decomposition | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Primitive Fitting | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Primitive Colliders | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Asset Colliders | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Shape Colliders | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || Tube and Disc not yet supported.  |
| Heightfield Colliders | 🟡 Active | 🟠 Minimal | ⭕ Not Required | 🟠 Volatile | 🟡 Needs Optimization | All  | || || | |
| Triggers | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || Usability issue with moving static triggers.  |
| Force Regions | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Wind | 🔵 Backlogged | 🟡 Partial | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | All  | || || Global wind is currently broken with rigid bodies. Ragdolls aren't affected by wind.  |
| Materials | 🟡 Active | 🟢 Complete | 🟢 Complete | 🟠 Volatile | 🔴 Needs Testing | All  | || || Major workflow improvements under way.  |
| Collision Filtering | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Joints | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Articulations | 🟠 Planned | ❌ None | ⭕ Not Required | ❌ Unproven | 🔴 Needs Testing | All  | || || | |
| Character Controller | 🟢 Complete | 🟠 Minimal | ⭕ Not Required | 🟠 Volatile | 🔴 Needs Testing | All  | || || Multiple functional improvements planned.  |
| Ragdoll | 🟡 Active | 🟡 Partial | 🟢 Complete | 🟠 Volatile | 🔴 Needs Testing | All  | || || Improvements in backlog/roadmap.  |
| Scripting | 🟢 Complete | 🟠 Minimal | ❌ None | 🟠 Volatile | 🔴 Needs Testing | All  | || || Needs a lot of usability work.  |
| Scene Queries | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Multi-Scene | 🔵 Backlogged | ❌ None | ⭕ Not Required | ❌ Unproven | 🔴 Needs Testing | All  | || || Need to figure out UX to progress with this. Many components currently rely on default scene.  |
| PhysX Visual Debugger Integration | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows  | || || Remote debugging not heavily tested.  |
| Debug Visualization | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | Windows Linux MacOS  | || || Only heavily tested on Windows. Lots of issues with z-fighting etc.  |
| Mesh Simplification | ❌ Unscheduled | || || || || || || || | |
### Cloth - NvCloth Integration 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Generic API | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Support for Mesh Components | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | All  | || || One optimization pass performed.  |
| Support for Actor Components | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔵 In Progress | All  | || || Skinned meshes: linear and dual quaternion blending. One optimization pass performed.  |
| Mesh Simplification | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Simulation Constraints | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || Motion constraints, Backstop, Tether constraints, horizontal/vertical, shearing, bending  |
| Realtime Editing | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Wind | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Actor Colliders | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| CCD | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Self Collision | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Async Simulation | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Debug Visualization | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🔴 Needs Testing | All  | || || | |
| Environmental Collision | 🔵 Backlogged | ❌ None | || || || || || || | |
| Painting Tool | 🔵 Backlogged | ❌ None | || || || || || || | |
| LOD | 🔵 Backlogged | ❌ None | || || || || || || | |
| Mesh Collision | 🔵 Backlogged | ❌ None | || || || || || || | |
### Destruction - Nvidia Blast Integration 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Authoring/Pipeline | 🔵 Backlogged | 🔵 In-Design | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || | |
| Geometry Destruction Simulation | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || | |
| Materials | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || Major workflow improvements under way.  |
| Scripting | 🟢 Complete | 🟠 Minimal | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || | |
| Atom Integration | 🔵 Backlogged | 🟠 Minimal | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || | |
| PhysX Integration | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟡 Experimental | 🔴 Needs Testing | Windows  | || || Blast can technically be independent from the physics backend  |
### Vehicles 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Vehicles | ❌ Unscheduled | || || || || || || || | |
### Fluids 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Fluids | ❌ Unscheduled | || || || || || || || | |
### Soft Bodies 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Soft Bodies | ❌ Unscheduled | || || || || || || || | |
## SIG-Docs-Community 

### NewSubsystem 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| New Module | || || || || || || || || | |
## SIG-Graphics-Audio 

### Features 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Deferred Fog | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | All  | || https://docs.o3de.org/docs/user-guide/components/reference/atom/deferred-fog/ | | |
| Tonemapping | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/atom-sample-viewer/graphics-feature-samples/#tonemapping | | |
| Direct Lighting / Area Lights | 🟢 Complete | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/user-guide/components/reference/atom/light/ | | |
| Meshes | 🟡 Active | 🟡 Partial | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#meshes | | |
| Skinned Meshes | 🟡 Active | 🟡 Partial | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#meshes | | |
| Eye Adaptation | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#lighting | | |
| Culling | 🟡 Active | 🟡 Partial | 🟢 Complete | 🔵 In Progress | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/user-guide/components/reference/atom/occlusion-culling-plane/ | | |
| HDR Pipeline | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/ | | |
| Shadows | 🟡 Active | 🟡 Partial | 🟢 Complete | 🔵 In Progress | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/user-guide/components/reference/atom/light/ | | |
| Skybox and Physical Sky | 🟢 Complete | 🟡 Partial | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#lighting | | |
| SSAO | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Color Grading | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Depth of Field | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| PBR Materials | 🟡 Active | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/look-dev/materials/pbr/ | | |
| Post Processing Volumes | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Decals | 🟡 Active | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#lighting | | |
| Screen Space Reflections | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Subsurface Scattering | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Motion Vectors | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
| Temporal Anti-aliasing (TAA) | 🟡 Active | 🟡 Partial | 🟢 Complete | 🔵 In Progress | 🟡 Needs Optimization | All  | || https://www.o3de.org/docs/atom-guide/features/#post-processing-effects-postfx | | |
### Render Hardware Interface 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| DirectX 12 | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | || || https://www.o3de.org/docs/atom-guide/dev-guide/rhi/ | | |
| Vulkan | 🟡 Active | 🟢 Complete | ⭕ Not Required | 🟢 Stable | 🟡 Needs Optimization | || || https://www.o3de.org/docs/atom-guide/dev-guide/rhi/ | | |
| Metal | 🟡 Active | 🟡 Partial | ⭕ Not Required | 🟠 Volatile | 🟡 Needs Optimization | || || https://www.o3de.org/docs/atom-guide/dev-guide/rhi/ | | |
### Audio 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Wwyse Integration | 🟢 Complete | 🟡 Partial | ⭕ Not Required | 🟢 Stable | 🟢 Optimized | || || https://www.o3de.org/docs/atom-guide/dev-guide/rhi/ | | |
## SIG-Network 

### Core Networking 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Transport API | 🟢 Complete | || || || || || || || | |
| Multiple network interface support | 🟢 Complete | || || || || || || || | |
| Compression (TCP/UDP) | 🟢 Complete | || || || || || || || | |
| Metrics support | 🟢 Complete | || || || || || || || | |
| UDP Core | 🟢 Complete | || || || || || || || | |
| UDP: DTLS support | 🟢 Complete | || || || || || || || | |
| UDP: Reliable queue support | 🟢 Complete | || || || || || || || | |
| UDP: Fragmentated packet support | 🟢 Complete | || || || || || || || | |
| TCP | 🟢 Complete | || || || || || || || | |
| TCP: TLS Support | 🟢 Complete | || || || || || || || | |
| TCP: Ringbuffer support Pkg Xmit | 🟢 Complete | || || || || || || || | |
### Multiplayer 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Multiplayer component API | 🟢 Complete | || || || || || || || | |
| Local Prediction | 🟢 Complete | || || || || || || || | |
| Server Side Rollback | 🟢 Complete | || || || || || || || | |
| Play in Editor Mode | 🟡 Active | || || || || || || || | |
| Hosting/Joining a Game | 🟢 Complete | || || || || || || || | |
| Network property support | 🟢 Complete | || || || || || || || | |
| RPC support | 🟢 Complete | || || || || || || || | |
| Network Input support | 🟡 Active | || || || || || || || | |
| ScriptBind support | 🟡 Active | || || || || || || || | |
| Netbound entity support [NetBindComponent] | 🟢 Complete | || || || || || || || | |
| Entity replication support | 🟢 Complete | || || || || || || || | |
| Network Prefab Spawning | 🟡 Active | || || || || || || || | |
| Networked Animation | ❌ Unscheduled | || || || || || || || | |
| Network Audio Support | ❌ Unscheduled | || || || || || || || | |
| Network Simulation (Physics) | 🟢 Complete | || || || || || || || | |
| Quality of Service | 🟡 Active | || || || || || || || | |
| Debugging Tools | 🟡 Active | || || || || || || || | |
| Metrics | 🟡 Active | || || || || || || || | |
### AWS Cloud Services 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| HTTPS Support | 🟢 Complete | || || || || || || || | |
| Restful API Support | 🟡 Active | || || || || || || || | |
| AWS C++ SDK Support | 🟢 Complete | || || || || || || || | |
| Client Side Ident & Auth | 🟡 Active | || || || || || || || | |
| Runtime Metrics | 🟡 Active | || || || || || || || | |
| Amazon GameLift Support | 🟡 Active | || || || || || || || | |
### Microsoft Azure Cloud Services 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Core services | ❌ Unscheduled | || || || || || || || | |
## SIG-Operations 

### NewSubsystem 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| New Module | || || || || || || || || | |
## SIG-Platform 

### Platform Abstraction Layer 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| PAL CMake | 🟡 Active | 🟡 Partial | || || || || || || | |
| PAL Tools/Editor/AP | 🟡 Active | 🟡 Partial | || || || || || || | |
| || || || || || || || || || | |
### Platform Configure (Engine Centric) 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Windows | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Mac | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Android | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Linux | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Jasper | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Paris | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Salem | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Provo | 🟢 Complete | 🟢 Complete | || || || || || || | |
| || || || || || || || || || | |
### Platform Build (Engine Centric) 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Windows | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Mac | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Android | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Linux | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Jasper | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Paris | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Salem | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Provo | 🟢 Complete | 🟢 Complete | || || || || || || | |
| || || || || || || || || || | |
### Platform Configure (Project Centric) 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Windows | 🟡 Active | 🟡 Partial | || || || || || || | |
| Mac | 🟡 Active | 🟡 Partial | || || || || || || | |
| Android | 🟡 Active | 🟡 Partial | || || || || || || | |
| Linux | 🟡 Active | 🟡 Partial | || || || || || || | |
| Jasper | 🟡 Active | 🟡 Partial | || || || || || || | |
| Paris | 🟡 Active | 🟡 Partial | || || || || || || | |
| Salem | 🟡 Active | 🟡 Partial | || || || || || || | |
| Provo | 🟡 Active | 🟡 Partial | || || || || || || | |
### Platform Build (Project Centric) 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Windows | 🟡 Active | 🟡 Partial | || || || || || || | |
| Mac | 🟡 Active | 🟡 Partial | || || || || || || | |
| Android | 🟡 Active | 🟡 Partial | || || || || || || | |
| Linux | 🟡 Active | 🟡 Partial | || || || || || || | |
| Jasper | 🟡 Active | 🟡 Partial | || || || || || || | |
| Paris | 🟡 Active | 🟡 Partial | || || || || || || | |
| Salem | 🟡 Active | 🟡 Partial | || || || || || || | |
| Provo | 🟡 Active | 🟡 Partial | || || || || || || | |
### O3DE Object Externalization 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Project | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Gem | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Template | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Restricted | 🟡 Active | 🟡 Partial | || || || || || || | |
| Repo | 🟡 Active | 🔵 In-Design | || || || || || || | |
| || || || || || || || || || | |
### Language/Localization 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Editor | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Runtime | 🟡 Active | 🟡 Partial | || || || || || || | |
| || || || || || || || || || | |
### Packaging 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Windows | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Mac | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Android | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Linux | 🟢 Complete | 🟢 Complete | || || || || || || | |
| Jasper | 🟡 Active | 🟡 Partial | || || || || || || | |
| Paris | 🟡 Active | 🟠 Minimal | || || || || || || | |
| Salem | 🟡 Active | 🟠 Minimal | || || || || || || | |
| Provo | 🟡 Active | 🟠 Minimal | || || || || || || | |
## SIG-Release 

### NewSubsystem 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| New Module | || || || || || || || || | |
## SIG-Security 

### NewSubsystem 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| New Module | || || || || || || || || | |
## SIG-Security-Reports 

### NewSubsystem 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| New Module | || || || || || || || || | |
## SIG-Testing 

### AutomatedReview 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Early Warning | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| CTest | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| GoogleTest | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| GoogleBenchmark | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| PyTest | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| O3DE EditorTest | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
| Test Metrics | 🟢 Complete | 🟢 Complete | 🟢 Complete | 🟢 Stable | 🟢 Optimized | || https://github.com/o3de/sig-testing | https://www.o3de.org/docs/user-guide/testing/ | | |
## SIG-UI-UX 

### UI Components 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Breadcrumb navigation | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-breadcrumbs-component/</div> | | |
| Browse Edit | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-browse-edit-component/</div> | | |
| Button | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-button-component/</div> | | |
| Card | 🟠 Planned | 🟡 Partial | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-card-widget/</div> | | |
| Checkbox | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-checkbox-component/</div> | | |
| Combobox | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-combobox-component/</div> | | |
| Context menu | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-context-menu-component/</div> | | |
| Filtered search | 🟠 Planned | 🟡 Partial | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-filtered-search-component/</div> | | |
| Line edit | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-line-edit-component/</div> | | |
| Progress indicators | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-progress-indicators-component/</div> | | |
| Radio button | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-radio-button-component/</div> | | |
| Reflected property editor | 🟠 Planned | 🟡 Partial | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-reflected-property-editor-component/</div> | | |
| Scrollbar | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-scrollbar-component/</div> | | |
| Slider | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-sliders-component/</div> | | |
| Spinbox | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-spinbox-component/</div> | | |
| Styled dock | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-styled-dock-component/</div> | | |
| Tab | 🟠 Planned | 🟡 Partial | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-tab-component/</div> | | |
| Toggle switch | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-toggle-switch-component/</div> | | |
| Tree view | 🟢 Complete | 🟢 Complete | || || || || || <div><span style="font-size: 0.875rem; letter-spacing: 0.2px; color: var(--jexcel_content_color);">https://www.o3de.org/docs/tools-ui/component-library/uidev-tree-view-component/</span></div> | | |
| Array | ❌ Unscheduled | ❌ None | || || || || || <br> | | |
| Table view | 🟢 Complete | 🟢 Complete | || || || || || <div>https://www.o3de.org/docs/tools-ui/component-library/uidev-table-view-component/</div> | | |
### UX Patterns 
| Module | Feature | Functional | Content | Code/API | Performance | Platform | Github Link | Doc Link | Notes |
| :-- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Component Card | 🟡 Active | 🟡 Partial | || || || || || <div>https://www.o3de.org/docs/tools-ui/ux-patterns/component-card/overview/</div> | | |
| Error handling | 🟠 Planned | 🟠 Minimal | || || || || || <div>https://www.o3de.org/docs/tools-ui/ux-patterns/error/overview/</div> | | |
| Hotkey management | 🔵 Backlogged | 🟠 Minimal | || || || || || || | |
| UI/UX Responsiveness standard | 🔵 Backlogged | ❌ None | || || || || || || | |
| Viewport interaction | 🔵 Backlogged | 🔵 In-Design | || || || || || || | |
| || || || || || || || || || | |
