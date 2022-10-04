## Lumberyard features with no equivalent in  O3DE

- GeomCache Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-geom-cache.html
- River Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-river.html
- Road Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-road.html
- Lens Flare Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-lens-flare.html
- High Quality Shadow Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-high-quality-shadow.html
- Infinite Ocean Componenthttps://docs.aws.amazon.com/lumberyard/latest/userguide/component-infinite-ocean.html
- Water Volume Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-water-volume.html
- Rain Component  https://docs.aws.amazon.com/lumberyard/latest/userguide/component-rain.html
- Snow Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-snow.html
- Legacy Terrain Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-legacy-terrain.html
 - PhysX Terrain should still function, and can be rendered using a static mesh
- Lightning Component com/lumberyard/latest/userguide/component-lightning.html
- Lightning Arc Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-lightning-arc.html
- Sky Highlight https://docs.aws.amazon.com/lumberyard/latest/userguide/component-sky-highlight.html
- Occluder Area Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-occluder-area.html
- Vis Area Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-vis-area.html
- Particle Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-particle.html
- Legacy particles and their settings are not supported. Atom is working on PopcornFX support as a replacement.
- Portal Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-portal.html
- Render to Texture Component https://docs.aws.amazon.com/lumberyard/latest/userguide/component-render-to-texture.html
- Atom does support a flexible pass system that can be used to create a pass that renders to a render target (which can be used as input to another shader/material), or an alternate scene that renders with the main pipeline, so the equivalent can be achieved, but not without significant effort.
- Sky Cloud https://docs.aws.amazon.com/lumberyard/latest/userguide/component-sky-cloud.html

*We should make very clear sections for each major area of O3DE/Lumberyard that matches the above.*