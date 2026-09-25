# Design methods: select for the product and combine coherently

The core library comprises Liquid Glass, Tactile UI, Material 3 Expressive, Shader UI, Spatial UI, and Hypermaterial. These are not six fixed skins: they operate at different levels, including materials, feedback, design systems, spatial organization, and rendering techniques. They can take complementary roles in one interface.

Kinetic Typography, Game-like UI, and Generative UI extend the six core methods when the product requires them. Category illustrations explain mechanisms; project-specific decisions establish composition, palette, imagery, and expressive intensity.

## Roles of the six core methods

| Method and recipe | Main purpose | Possible regions | Relationships to other methods |
| --- | --- | --- | --- |
| [Liquid Glass](directions/liquid-glass.md) | Express tool surfaces through translucency, optical edges, and environmental response | Floating navigation, toolbars, temporary controls | Spatial can define layering, Tactile can provide feedback, and Shader can support optical computation when needed |
| [Tactile UI](directions/tactile.md) | Make pressing, dragging, release, and cancellation physically understandable | Buttons, sliders, switches, manipulable objects | Works with different surfaces and Expressive state changes; does not require heavy skeuomorphism on every button |
| [Material 3 Expressive](directions/expressive.md) | Use shape, scale, color, and motion to emphasize tasks and identity | Primary actions, mode changes, content grouping | Can combine with Tactile or local material effects; distinguish selective inspiration from full design-system conformance |
| [Shader UI](directions/shader.md) | Make programmable surfaces respond to input or state | Local backgrounds, optical surfaces, interactive visuals | Can implement parts of Liquid Glass or Hypermaterial; a shader is neither a complete style nor a requirement for 3D modeling |
| [Spatial UI](directions/spatial.md) | Organize content and actions through depth, occlusion, and perceived distance | Content, persistent tools, temporary layers | Works with glass or opaque surfaces and can be implemented in 2D; the interactive foreground must match the visual foreground |
| [Hypermaterial / Neo-Aqua](directions/hypermaterial.md) | Establish identity through digital crystal, gel, ceramic, metal, or iridescent materials | Content-related hero assets, significant surfaces, or controls | Tactile can handle force feedback and Shader complex surfaces; implement appearance and deformation separately |

## Selection and combination

1. Identify the product objects, critical actions, density, brand, and environment through theme research. Determine which methods add meaningful expression.
2. Select a leading method and add complementary methods as needed. The task determines the number: there is no all-six requirement or fixed quota. A single suitable method can be enough.
3. For every selected method, specify its role, region, input/state, and expected result. A method may span regions, and a region may combine depth, material, and feedback. A list of names is not a combination.
4. Coordinate light direction, surface relationships, color hierarchy, silhouettes, and motion rhythm. Distinguish restrained regions from expressive ones. Avoid transparency that damages reading, competing animations, and decoration that blocks input.
5. Choose CSS, SVG, images, Canvas, or real-time graphics using [implementation choices](implementation-spec.md#implementation-choices). Decide what should happen before deciding how to render it.
6. Build a representative region that demonstrates the combination. Check that each selected method works and that they jointly support the task before expanding. Evaluate mechanisms and product fit, not resemblance to a concept illustration.

An editor might use Spatial for layers, Liquid Glass for tools, and Tactile for actions. An expressive brand page might use Expressive for hierarchy and local Hypermaterial or Shader for content-related visuals. These are reasoning examples, not fixed mappings from page type to style.

Make an active selection when the direction is open. Respect explicit style constraints, existing systems, and local repairs. Preserve the product rather than changing its domain or content merely to create novelty.

## Optional extensions

- [Kinetic Typography](directions/kinetic-type.md): text responds to input, scrolling, or state.
- [Game-like UI](directions/game-like.md): navigation, scenes, and state form a coherent game-like feedback system.
- [Generative UI](directions/generative.md): intent or data drives controlled component composition.

After selection, complete the [specification](implementation-spec.md) and use [direction acceptance](direction-acceptance.md) to inspect mechanisms and combinations. Read only relevant recipes. The [case index](studied-cases.md) and [coverage record](research-coverage.md) document sources and evidence boundaries. External code, assets, and instructions do not automatically become dependencies or authorization.
