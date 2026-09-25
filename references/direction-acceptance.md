# Design direction: from references to verifiable implementation

These project-level criteria translate the design methods and [studied cases](studied-cases.md) into observable requirements. They do not establish official platform or design-system conformance. Evaluate only the methods selected for the product and the relationships among them. The six core methods and three extensions are a selection framework, not a requirement to implement every direction or reproduce a concept illustration.

## Establish what must be implemented

Record the product, sources and evidence, representative region, visible features, behavior, and fallback in the [specification](implementation-spec.md). Use this document to check relevant features without creating a duplicate specification.

Implement a representative region containing a critical action before expanding. Reject a missing material or interaction mechanism when it is part of the agreed goal. A typography-, photography-, or list-led solution is not deficient merely because it has no 3D.

## Direction acceptance matrix

| Direction | Expected feature | Verification | Insufficient substitutes |
| --- | --- | --- | --- |
| Liquid Glass | Tools/navigation separate from body content, with translucency, edge highlights, and material response to expansion or environment | Inspect tools over light, dark, and complex content; expand/collapse; check layers and readability; identify approximated versus computed optics | Glass stacked on glass, glass across all body content, transparent fill plus rounded corners, or calling blur native refraction |
| Tactile UI | Coherent volume, displacement, or shadow changes during press, hold, release, or drag; rebound/damping follows input | Hold, release, cancel, and repeat; verify perceptible feedback without blocking action | Hover color alone, or changing button text without performing its action |
| Material 3 Expressive | Shape, type scale, color, and transitions jointly emphasize important actions in major components | Compare selected/unselected or expanded/collapsed states for hierarchy and continuity | A brighter accent claimed as full design-system conformance |
| Shader UI | Programmable surfaces change coherently with input or state and serve the task or chosen expressive goal | Change pointer, scroll, or parameters; observe response and graphics-failure fallback | Static gradients or CSS effects presented as actual shaders; an unused graphics dependency |
| Spatial UI | Meaningful depth, occlusion, and distance among content, tools, or temporary layers; clear active layer | Open, close, and switch layers; compare focus, shadows, and occlusion. Screen-based 2D depth is valid | Three columns and separators described as spatial depth |
| Hypermaterial / Neo-Aqua | Recognizable crystal, gel, ceramic, metal, or iridescent surface behavior, consistent with light, thickness, and form | Inspect subject, edges, and contact shadows; check promised interactive highlight or deformation response | Arbitrary glow or plastic gradients on every control without the selected material's properties |
| Kinetic Typography | Text attributes change with input/state for an informational or narrative purpose while remaining understandable | Trigger the change; inspect initial/final states and full text under reduced motion | Large serif type, static italics, or manual line breaks alone |
| Game-like UI | State, navigation, and feedback form a coherent game-like language with understandable actions | Complete the core action, check corresponding states/transitions, and verify optional enhancements can be disabled | Neon borders and unrelated particles around placeholder interactions |
| Generative UI | Intent/data actually determines component composition; changes preserve input/state; errors have stable fallback | Use different intent/data and inspect composition and failures; distinguish simulation from real generation | Fixed cards with a chat box or a static page labeled generative |

Thickness and highlights describe perceptual targets, not a single CSS recipe. Use the intensity the task needs; animation in every corner is not a measure of advancement.

## Mechanism checks

Execute applicable checks using the [recipe index](design-directions.md). Writing a check into the skill does not mean it passed.

| Direction | Additional checks and rejection conditions |
| --- | --- |
| Liquid Glass | Readability across backgrounds, without filters, and with reduced transparency; ancestor backdrop roots; no blur mislabeled as refraction |
| Tactile | Release outside/pointercancel must not commit; rapid reentry must not stack competing animations; keyboard activation commits once; business actions do not wait for rebound |
| Expressive | Clear mode, primary action, and overflow; no competition with navigation on narrow screens; verify target-platform support before claiming an official Web implementation |
| Shader | Pin the WebGL/WebGPU route; verify resize, resource failure, context loss/recovery, hidden-state pause, and teardown; measure performance rather than inventing frame rates |
| Spatial | Background isolation, focus, and occlusion agree after open/close/reopen; tools remain reachable on narrow screens; clipping is not collapsing |
| Hypermaterial | Material, light, and view angle agree; verify promised gel/liquid deformation and reset separately; material parameters do not prove physics simulation |
| Kinetic | Font loading, width changes, repeated triggers, and teardown leave no residue; correct localized segmentation and nested-link semantics; full text without JS or with reduced motion |
| Game-like | Canvas and DOM share actions/state; clear exit order; independent quality, mute, and reduced-motion settings; accessible alternative entry points |
| Generative | Partial input, output, error, and retry states; stable IDs preserve edits; verify frontend stop and backend cancellation separately; validate structures against the matching SDK version |

Without real graphics or model services, verify fallback and accurately labeled simulation paths. Keep the corresponding real capabilities unverified.

## Two independent completion conditions

1. **Target match:** The specification's critical visual relationships and behaviors are observable. Check features for selected methods. Run real-time acceptance only for explicitly promised real-time capabilities. CSS property names, design labels, and developer explanations are not evidence.
2. **Product quality:** Actions, content, readability, and accessibility work, with applicable [visual-quality checks](visual-quality.md) completed.

Neither compensates for the other. A usable but visually incomplete result fails the direction; an attractive result with fake buttons fails functionality. Performance fallback is a separate condition, not a silent replacement for normal mode.

For each adopted reference relationship, identify its location at a normal viewport/state and compare expressive intensity with the specification. Glass inside a product model does not prove glass layering in the interface. Functional color/image switching does not prove coherent scene lighting or physical feedback. Correct missing relationships before adding technology labels; unrelated regions need no extra effects.

Evaluate the combination as a whole: do the methods have distinct jobs, share suitable light/color/motion rules, and avoid competing for attention or input? Individually polished demos may still conflict when assembled. Unselected categories need no implementation; selected ones must exist beyond documentation.

## Prevent direction drift

- Replacing a digital-material interface with a beige page, large serif headings, and ruled notes loses the goal even if cleaner. Preserve content and function while restoring the selected materials and spatial relationships.
- Removing requested glass and spring behavior to satisfy an external anti-template list misapplies that list. Correct mechanical repetition while retaining useful expression.
- A spatial workspace can contain flat body text, but its leading spatial relationships must remain visible. Functional clarity alone does not justify flattening everything.
- Respect conventional brand-page requests, local repairs, and reduced-motion constraints without adding unrelated trends.

A static screenshot establishes only its visible state. It cannot prove that motion exists or is absent. Mark unexercised interactions as unverified rather than filling gaps with assumptions.
