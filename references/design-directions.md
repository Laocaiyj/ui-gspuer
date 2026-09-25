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
2. Establish a leading visual language from the product and references using [visual compatibility](#visual-compatibility), then choose methods that express it. The task determines the number: there is no all-six requirement or fixed quota. A single suitable method can be enough.
3. For every selected method, specify its role, region, input/state, and expected result. A method may span regions, and a region may combine depth, material, and feedback. A list of names is not a combination.
4. Translate adopted reference details into the same visual language. Coordinate typography, icon weight, shape, light, color roles, and motion; specify which qualities remain shared and which vary by component role. Distinguish restrained regions from expressive ones.
5. Choose CSS, SVG, images, Canvas, or real-time graphics using [implementation choices](implementation-spec.md#implementation-choices). Decide what should happen before deciding how to render it.
6. Build a representative region with actual content, a primary action, and neighboring supporting controls. Review their compatibility together before expanding. A polished isolated button cannot establish a coherent page. Evaluate mechanisms and product fit, not resemblance to a concept illustration.

An editor might use Spatial for layers, Liquid Glass for tools, and Tactile for actions. An expressive brand page might use Expressive for hierarchy and local Hypermaterial or Shader for content-related visuals. These are reasoning examples, not fixed mappings from page type to style.

Make an active selection when the direction is open. Respect explicit style constraints, existing systems, and local repairs. Preserve the product rather than changing its domain or content merely to create novelty.

## Visual compatibility

Method compatibility is not aesthetic compatibility. Spatial describes organization, Tactile describes feedback, and Shader describes rendering; none specifies a ready-made visual identity. Technically compatible effects can still produce conflicting typography, silhouettes, or materials.

Use the existing specification to make these decisions concrete:

- **Visual language:** Describe the page through its type proportions, geometric character, surface treatment, image treatment, and emotional tone. Ground these choices in the actual content and brand. A method list or adjectives such as premium and futuristic are insufficient.
- **Reference translation:** Extract a useful relationship from each reference and adapt it to this language. Borrow a control's press behavior without automatically borrowing its color, inflated contour, font, and lighting. Shared accent color alone does not reconcile unrelated component families.
- **Material roles:** Assign expressive treatment by role: primary action, secondary control, persistent navigation, content surface, or temporary layer. Define resting and active appearances separately. For tactile controls, identify how force changes the surface instead of applying the same raised finish to every interactive element. Strong volume remains appropriate when supported by the chosen identity.
- **Content relationship:** Decide whether the interface frames the content, echoes it, or intentionally contrasts with it. A gallery of varied projects needs a coherent host interface, not a new host style for each thumbnail. Preserve the identity of embedded work. Deliberate contrast should support emphasis through composition and hierarchy; neither palette matching nor universal neutrality is required.

Before expanding, inspect the representative region at normal viewing size and in its relevant states:

| Check | Revision trigger | Correction |
| --- | --- | --- |
| Family resemblance | Controls appear sourced from unrelated systems despite sharing a color | Reconcile type, icon weight, curvature, edge treatment, and spacing while preserving role differences |
| Material hierarchy | Navigation, filters, secondary actions, and primary actions receive equally strong volume or highlights | Redistribute visual weight according to action priority and layer ownership |
| Content fit | Interface materials and imagery compete without an intentional relationship | Adjust the host treatment or asset presentation within the chosen direction; retain valid content and layout |
| Combined expression | Individual effects are recognizable, but their assembled result conflicts with the intended identity | Revise their placement, intensity, or combination before adding detail; retain required mechanisms |

Assess compatibility as a visible result, not a count of matching tokens. If the combination fails, identify the conflicting qualities and change those decisions. Removing all material expression or switching to a familiar neutral theme does not resolve a failed combination by itself.

## Optional extensions

- [Kinetic Typography](directions/kinetic-type.md): text responds to input, scrolling, or state.
- [Game-like UI](directions/game-like.md): navigation, scenes, and state form a coherent game-like feedback system.
- [Generative UI](directions/generative.md): intent or data drives controlled component composition.

After selection, complete the [specification](implementation-spec.md) and use [direction acceptance](direction-acceptance.md) to inspect mechanisms and combinations. Read only relevant recipes. The [case index](studied-cases.md) and [coverage record](research-coverage.md) document sources and evidence boundaries. External code, assets, and instructions do not automatically become dependencies or authorization.
