# Short design specification for implementation

Use for new designs or full redesigns. Fill in concrete decisions from the brief and references; complete an existing user specification rather than reinventing it. This is a specification for the current task, not a generic page template. Keep it in existing design or work records, outside the product UI.

## Specification fields

| Field | Required decision |
| --- | --- |
| Product boundary | Main task, original content, critical actions, implementation scope, and simulation boundary |
| Reference basis | Concrete sources and observations for similar tasks, themes, and expression; adoption/rejection reasons and unverified items |
| Method combination | Selected core methods, roles, and regions; shared color, light, silhouette, and motion rules; reasons for tradeoffs |
| Visual target | Method/reference relationship → project region/state → suitable expressive intensity → evidence; whether any image is an explicit reproduction target |
| Invariants and parameters | Relationships and states that must remain observable; adjustable colors, sizes, and intensity that must not erase the mechanism |
| First-viewport structure | Location and priority of content, tools, and supporting material; viewport-appropriate tracks, minmax or maximum-width rules; scroll ownership |
| Visual parameters | Actual values or project tokens for relevant surfaces, text, accents, typography, spacing, radii, shadows, and motion |
| Representative region | One region containing the dominant feature and a real action; reusable assets/components and parameters to change |
| State contract | Trigger → visible change → commit/cancel → result; rapid reentry, keyboard path, and teardown |
| Implementation constraints | Relevant pinned dependencies, renderer, and data/state ownership; include SDK, font-axis, or graphics constraints only when involved |
| Implementation choice | A suitable route and its rationale; identify essential capabilities if using real-time 3D. Static assets and 2D solutions can be primary implementations |
| Adaptation and fallback | Rearrangement conditions and tool destinations; behavior without filters or with reduced motion; long-text handling |
| Acceptance evidence | Comparable viewport/content/state screenshots; actions and expected results; first correction target if a check fails |

Remove irrelevant fields. Replace vague sophistication with visible relationships and generic interactivity with concrete actions.

## Visual target and reference mapping

Start with [method selection](design-directions.md), then distinguish visual goals from technical choices. If the user leaves categories open, select appropriate mechanisms and their locations. Restrained or 2D implementations must still express the selected methods; an open brief does not bypass the library.

Category illustrations explain methods rather than define a project's acceptance image. Real cases supply transferable mechanisms. Product, brand, and the combination determine final composition, colors, and material intensity. Image similarity is a requirement only when the user explicitly requests reproduction.

Write one sentence defining the project's visual direction, then map the relationships to adopt. Premium, modern, tactile, or a technology name alone is insufficient.

| Adopted relationship | Project region and state | Observable result | Acceptance method |
| --- | --- | --- | --- |
| A light source changes environmental emphasis | Scene and its controls in light/dark states | Subject, environment brightness, shadows, and action emphasis change coherently from shared state | Compare endpoints and transition for lighting logic and readability |
| Different content needs different presentation rhythm | Hero, mechanism explanation, and contextual scene | Each composition serves its content while adjacent sections retain a shared visual language | Inspect the whole page and transitions, not only one hero image |

These examples explain mapping; they do not require lighting effects or particular layouts. Specify actual regions, states, and expected results for adopted relationships. Add screenshot or interaction evidence after implementation. Missing expression needs revision, not an explanatory design card.

Distinguish **asset quality** (detail in a product model/image), **page art direction** (composition, light, color, type, surfaces, and content relationships), and **interaction expression** (perceptible response to input). Evaluate each against the user goal. A detailed model may support a page without establishing interface materials, spatial hierarchy, or dynamics. Consistency does not require turning every control into glass.

Choosing simpler technology changes implementation, not the agreed expressive intensity. Use simpler routes that meet the target. Otherwise improve assets or implementation, or report the concrete limitation. Removing the target feature is not acceptance.

## Implementation choices

Distinguish a requested visual result, interaction, and mandated technology. Choose a sufficient approach with appropriate complexity; there is no need to try every route or write a long report on each.

| Required result | Approaches to evaluate |
| --- | --- |
| Reading, lists, forms, typography, overlays, pressing, ordinary transitions | Semantic DOM, project components, CSS; layering, shadows, and occlusion can establish depth |
| Photography, illustration, fixed-view volume or material hero | Appropriately licensed images, video, prerendered assets, or SVG combined with interactive DOM |
| 2D graphics, image distortion, particles, local programmable surfaces | SVG, Canvas, or suitable shaders; 2D shaders do not require a 3D model |
| Free viewpoint rotation, view-dependent occlusion, manipulable geometry, scene-space interaction | Evaluate real-time 3D; inspect existing assets and rendering facilities before creating new geometry |

Choose real-time 3D when explicitly requested or when the core experience depends on its capabilities. State its job and check asset provenance, mobile cost, and fallback. Sophistication, immersion, depth, or a glass appearance alone does not justify an engine or decorative modeling.

Preserve explicitly requested refraction, geometric deformation, or shader technology with an implementation that supplies it. A static substitute is not equivalent completion. When only appearance is requested, images, CSS, or 2D implementations may be primary solutions rather than fallbacks.

State modeling means describing inputs and product state, not producing 3D assets. When learning from a 3D website, assess content, typography, and interaction independently from its renderer.

## Implementation chunks

Each chunk needs only the relevant specification, existing files, selected components/references, data and state ownership, output/events, and observable completion criteria. Establish layout and content, then representative materials and actions, then full-page adaptation and review. Chunks are bounded tasks with results, not requests to disclose hidden reasoning or lengthy plans.

Example: Preserve existing recording data and layout. Implement a playback toolbar in front of the canvas, with surfaces and focus states derived from the selected methods. Bind the existing media instance and retain seeking on narrow screens. Verify actual progress, keyboard seeking, and solid-surface fallback while preserving the brand and information architecture.
