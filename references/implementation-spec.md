# Short design specification for implementation

Use for new designs or full redesigns. Fill in concrete decisions from the brief and references; complete an existing user specification rather than reinventing it. This is a specification for the current task, not a generic page template. Keep it in existing design or work records, outside the product UI.

## Specification fields

| Field | Required decision |
| --- | --- |
| Product boundary | Main task, original content, critical actions, implementation scope, and simulation boundary; distinguish required invariants from existing presentation open to redesign |
| Usage context | Purpose of each surface, first-use versus repeat-use needs, delivery platform, input modes, and applicable host/navigation conventions |
| Content basis | Supplied identity/assets/data, task-specific sample content needed, and reference details explicitly adopted under the [reuse boundaries](../SKILL.md#content-and-reuse-boundaries) |
| Reference basis | Concrete sources and observations for similar tasks, themes, and expression; adoption/rejection reasons and unverified items |
| Art direction | User preferences or stated assumptions translated into concrete choices; [visual idea](art-direction.md#develop-the-visual-idea), focal composition, type/image treatment, and distinctive details beyond a hero asset |
| Method combination | Product-specific visual language; selected methods and roles; translated reference relationships; shared type/shape/light/motion rules and role-specific material intensity; relationship between interface and content |
| Visual target | Method/reference relationship → project region/state → suitable expressive intensity → evidence; whether any image is an explicit reproduction target |
| Invariants and parameters | Relationships and states that must remain observable; adjustable colors, sizes, and intensity that must not erase the mechanism |
| First-viewport structure | Location and priority of content, tools, and supporting material; viewport-appropriate tracks, minmax or maximum-width rules; scroll ownership |
| Page composition | For new pages/full redesigns: region sequence, content/state sizing, and matched visual comparison from the [composition contract](art-direction.md#compose-the-page); include decision groups, adjacent-region relationships, narrow-screen sequence, and a purposeful detail |
| Visual parameters | Actual values or project tokens for relevant surfaces, text, accents, typography, spacing, radii, shadows, and motion |
| Representative composition | Real content, defining visual, action and neighbors at intended scale; wide/narrow render and distinguishing material cues; on repeated direction rejection or unresolved focal alternatives, two structurally different renders and an evidence-based selection under the [render checkpoint](art-direction.md#render-before-expanding) |
| State contract | Trigger → visible change → commit/cancel → result; rapid reentry, keyboard path, and teardown |
| Visual continuity | Consequential workflow states, their composition and method expression, shared visual rules, and justified differences in density or emphasis |
| Implementation constraints | Relevant pinned dependencies, renderer, and data/state ownership; include SDK, font-axis, or graphics constraints only when involved |
| Implementation choice | A suitable route and its rationale; identify essential capabilities if using real-time 3D. Static assets and 2D solutions can be primary implementations |
| Adaptation and fallback | Rearrangement conditions and tool destinations; behavior without filters or with reduced motion; long-text handling |
| Acceptance evidence | Comparable viewport/state renders against adopted reference qualities; fixed-content before/after checkpoint; actual actions and results; separate improvement from target fit, with the largest remaining discrepancy and recheck outcome |

Remove irrelevant fields. Replace vague sophistication with visible relationships and generic interactivity with concrete actions.

## Visual target and reference mapping

Start with [method selection](design-directions.md), then distinguish visual goals from technical choices. If the user leaves categories open, select appropriate mechanisms and their locations. Restrained or 2D implementations must still express the selected methods; an open brief does not bypass the library.

Category illustrations explain methods rather than define a project's acceptance image. Real cases supply transferable mechanisms. Product, brand, and the combination determine final composition, colors, and material intensity. Image similarity is a requirement only when the user explicitly requests reproduction.

Write one sentence defining the project's visual direction, then map the relationships to adopt. Premium, modern, tactile, or a technology name alone is insufficient.

For each adopted relationship, record: **source observation → current-project region and state → observable result → acceptance method**. Name actual objects and actions from this task. Specify how the relationship changes to fit the current content instead of importing the source's page structure. Add screenshot or interaction evidence after implementation. Missing expression needs revision, not an explanatory design card.

Distinguish **asset quality** (detail in a product model/image), **page art direction** (composition, light, color, type, surfaces, and content relationships), and **interaction expression** (perceptible response to input). Evaluate each against the user goal. A detailed model may support a page without establishing interface materials, spatial hierarchy, or dynamics. Consistency does not require turning every control into glass.

Choosing simpler technology changes implementation, not the agreed expressive intensity. Use simpler routes that meet the target. Otherwise improve assets or implementation, or report the concrete limitation. Removing the target feature is not acceptance.

## Implementation choices

Distinguish a requested visual result, interaction, and mandated technology. Choose a sufficient approach with appropriate complexity; there is no need to try every route or write a long report on each.

| Required result | Approaches to evaluate |
| --- | --- |
| Reading, lists, forms, typography, overlays, pressing, ordinary transitions | Semantic DOM, project components, CSS; layering, shadows, and occlusion can establish depth |
| Photography, illustration, fixed-view volume or material hero | Supplied or appropriately licensed media, generated imagery, prerendered assets, or SVG combined with interactive DOM |
| 2D graphics, image distortion, particles, local programmable surfaces | SVG, Canvas, or suitable shaders; 2D shaders do not require a 3D model |
| Free viewpoint rotation, view-dependent occlusion, manipulable geometry, scene-space interaction | Evaluate real-time 3D; inspect existing assets and rendering facilities before creating new geometry |

Choose real-time 3D when explicitly requested or when the core experience depends on its capabilities. State its job and check asset provenance, mobile cost, and fallback. Sophistication, immersion, depth, or a glass appearance alone does not justify an engine or decorative modeling.

Preserve explicitly requested refraction, geometric deformation, or shader technology with an implementation that supplies it. A static substitute is not equivalent completion. When only appearance is requested, images, CSS, or 2D implementations may be primary solutions rather than fallbacks.

State modeling means describing inputs and product state, not producing 3D assets. When learning from a 3D website, assess content, typography, and interaction independently from its renderer.

## Production media

For a new page or full redesign, select the defining visual's production route before expanding the interface. Use the following conditions; convenience or a self-contained file is not evidence that a medium meets the target.

| Observable need | Required production action |
| --- | --- |
| Suitable supplied or licensed imagery already meets the brief | Inspect and integrate it; preserve factual product appearance |
| A fixed-view subject needs photography, illustration, texture, or material detail, and suitable imagery is absent | Invoke the available image-generation skill/tool, inspect the output, save it, and integrate the actual asset before visual acceptance |
| The subject is authored vector art, meaningful data, or geometry/effects that must respond to input | Implement the required visual relationships in code; inspect detail and behavior rather than substituting a still image |
| The surface is text-led, or the request is a local control/content repair | Complete that scope; do not invent a hero or an imagery requirement |
| The chosen media route is unavailable, fails, or conflicts with an explicit restriction | Use a suitable permitted source if available; otherwise mark the media and visual target incomplete and report the specific limitation |

For each defining visual, keep **required qualities → chosen source/tool → actual asset path or procedural implementation → in-page review status** in the existing work record. A planned image, written generation prompt, or empty path is pending production. Structural drafts may use temporary geometry, but replace it before accepting a target that depends on richer imagery. Rings, gradient hills, or a shaded disc cannot stand in for missing subject detail merely because they are easy to implement. Intentional geometric art remains valid when it meets the chosen direction.

Produce the smallest useful representative asset first and test it with the real composition before expanding a collection. Neither one hero for every page nor a generated image for every item is required. Generate media layers, not a flattened screenshot of the working interface: controls, copy, search, and editing remain semantic components. README concepts can inform explicitly requested quality comparisons, but their subjects and layouts are not starter templates or proof of implemented quality.

1. **Choose the media relationship.** State whether the image is the subject to inspect, a framed illustration, or part of the surrounding visual field, and why that role serves the content. Sketch its bounds with the real title, action, and beginning of the next region. Decide which existing decorative layers to keep, rework, or remove by their job; an inherited grid, glow, or fade is not a constraint that new media must obey. Choose a shared field, intentional frame, or deliberate section break from the content relationship. None is the default solution.
2. **Brief the asset in context.** Specify subject and distinguishing material cues, focal scale, text-safe space, intended edge/boundary treatment, lighting/palette, aspect ratio, display size, narrow-screen crop, and transparency if needed. When media and UI depict one scene, reconcile their perspective, light, occlusion, and contact. When imagery is framed or contrasts deliberately with functional controls, coordinate hierarchy and alignment without making every surface share its material. Keep interface text and controls in semantic components.
3. **Produce and retain.** Use the appropriate available media workflow. Inspect the result before selecting it. Save the accepted asset in the project's established media location; record its exact generation prompt, source or input references, and intended use in project records outside the UI. Retain originals separately from delivery derivatives. If generation is unavailable, choose a suitable available source or disclose the remaining visual gap.
4. **Integrate and inspect.** Connect real asset paths with suitable dimensions, alternative text, loading behavior and optimized delivery sizes. Capture the artwork with its actual text/actions and a view spanning its boundary with the next region, at wide and narrow sizes. Check crop, focal order, edge treatment, and the chosen relationship. A fade may be intentional; if it only hides mismatched backgrounds, correct the composition or use an explicit boundary. Judge asset quality, page integration and behavior separately. Approval of a standalone asset establishes only that scope; preserve factual product appearance and any explicit requirement to keep the asset, while revising its placement or reporting an unresolved fit.

Research basis, reviewed 2026-09-28: [JetBrains' graphics process](https://blog.jetbrains.com/blog/2023/10/16/ai-graphics-at-jetbrains-story/) describes designer references and composition control; [Kotlin's identity study](https://blog.jetbrains.com/kotlin/2021/07/adding-volume-to-the-kotlin-identity/) combines typography with dimensional forms; the [HTML image standard](https://html.spec.whatwg.org/multipage/images.html#art-direction) distinguishes responsive art direction from resolution switching. The role and boundary workflow above is a design synthesis, not a requirement imposed by these sources.

## Implementation chunks

Each chunk needs only the relevant specification, existing files, selected components/references, data and state ownership, output/events, and observable completion criteria. Establish layout and content, then representative materials and actions, then full-page adaptation and review. Chunks are bounded tasks with results, not requests to disclose hidden reasoning or lengthy plans.

Describe each chunk using the current product's objects and actions. Carry over its state contract and acceptance criteria without introducing a sample application's content or layout.
