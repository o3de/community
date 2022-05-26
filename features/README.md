# O3DE SIG Features Editing tool

jump to [Feature State Form](https://o3de.github.io/community/features/form.html)

Please use this tool to create, update, and produce the release feature list.
## Each column has a tooltip to explain its usage, finer details are explained below.

#### To produce a release report, click on the "Create Release Markdown", then enter the Release version, and it will download a compiled markdown file ([sample here](Sample-FeatureMarkdown.md))

The SIG pulldown is loaded from here: https://github.com/o3de/community/tree/main/features/sigjson

You can select the SIG and it will populate the page. Alternatively, you can also choose a JSON file from your local drive, but it must match the proper format.

From there, you can create new subsystems and rows as well as download the JSON when you are done.

when you make changes and want to save it in github, you can create a pull request from the community repo against the files listed above.
Once accepted and merges, your changes should appear on the github.io page in about 5-10 minutes.

The results of these files will be used as formatted tabled that will serve as artifacts in the release builds so that developers that want to use the engine can easily see the maturity of the features and subsystems of the engine.

If you have suggestions or want to work on the code, let someone know or reach out to me OBWANDO (Royal OBrien) on github or Discord.

> Subsystems should be larger categories like "Multiplayer, Core Networking, Cloud Services" or "Lighting, Render Hardware Interface, Shaders"

> Rows should be more specific to the feature that fits under that subsystem. Like "DirectX 12, Vulkan, Metal under Lighting subsystem" 

# Table Columns:

### Module: this is the name of the feature module

### Feature: This is the production state of the feature 
	Unscheduled: The feature has not been scheduled, it is something that is wanted, but thats about it.
	Deprecated: Feature has been deprecated and slated to go away (accompanied with some indication of replacement)deprecated
	Backlogged: Feature has been moved to the backlog
	Planned: Feature is actively being planned and/or in design phase.
	Active: Feature is actively in development
	Complete: Feature is production complete
	
### Content: The state of the content necessary for feature usage
	Not required: Content is not required for this feature
	Incompatible: Content exists, but is incompatible with current feature.
	Minimal: Minimal content is available, but may hinder feature usability
	Partial: Partial content is available, but does not hinder feature usability
	Complete: All content is complete for full feature usability
	
### Functional: The state of the functionality of the feature as defined by documentation.
	None: There is no defined documentation for the functionality of this feature.
	Deprecated: The feature has been deprecated and slated to go away (accompanied with some indication of replacement)
	In-Design:  Feature functionality is actively being planned and/or in design phase.
	Minimal: Feature meets minimal functional requirements
	Partial: Feature has greater than minimal functionality
	Complete: Feature has complete as defined in documentation.
	
### Code/API: The state of the code operation and its API
	Unproven: Code/API working but has had insufficient use to really harden any corner cases or identify potential pathological issues
	Deprecated: Code or API is slated to go away (accompanied with some indication of what the system will be replaced by)
	Experimental: Code is unstable or API is likely to change
	Volatile: Code works, but may crash or API is fixed, but may possibly change
	Stable: Code/API is actively used without any serious impediments and has no immediate upgrades planned.

### Performance: The performance state of the feature
	Untested: Feature is untested and may be unstable.
	Needs Testing: Feature requires testing to determine stability
	Needs Optimization: Feature does not crash and is stable and but needs optimizations
	Optimized: Feature is stable, does not crash and is optimized for use

### Platform: The platforms that are supported by this feature. 
	You can select multiple platforms from the pulldown
	
### Link: Link to Github Issue or Discussion for the feature

### Doc Link: Link to the documentation of the feature

### Notes: Notes realted to this entry which may change from time to time.


 
