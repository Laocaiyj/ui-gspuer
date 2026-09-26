---
name: ui-gspuer
description: Research and combine Liquid Glass, Tactile, Expressive, Shader, Spatial, and Hypermaterial methods for distinctive Web UI. Use for interface concepts, frontend design, visual redesign, and correcting generic template aesthetics. Not for backend-only work.
---

# ui-gspuer

Research and combine six core methods—Liquid Glass, Tactile UI, Material 3 Expressive, Shader UI, Spatial UI, and Hypermaterial—to implement distinctive, usable Web interfaces. Ground composition, typography, color, materials, and behavior in the current product. Select 2D or 3D techniques according to the required experience. Treat concept illustrations as explanations of methods unless the user explicitly requests reproduction. Follow the user's language and localization requirements.

## Route by task

| Request | Read and act |
| --- | --- |
| Static interface example, concept image, or visual mockup | Follow [art direction and concept images](references/art-direction.md): research, select a composition, prepare the image brief, generate and inspect the image; stop at the requested visual deliverable |
| New interface, full redesign, or substantial mismatch with the brief | Read [design research](references/design-research.md), [art direction](references/art-direction.md), and [method selection](references/design-directions.md), write a short specification, then implement a representative region and the full flow |
| Inspiration, case studies, or design knowledge only | Use [design research](references/design-research.md) to deliver sources and transferable findings; do not implement a page without that scope |
| Local button, spacing, or state adjustment | Read affected code and the existing specification; consult the [relevant recipe](references/design-directions.md) when its mechanism is involved; keep the change local |
| Review or correct generic template aesthetics | Preserve the product and requested direction; use [visual review](references/visual-quality.md). Report findings for review-only requests; implement corrections when requested |
| Model comparison or repeated failures | Use [evaluation and iteration](references/evaluation-loop.md); hold the task and acceptance criteria constant and diagnose from evidence |

Read only relevant sections. Reuse directions, specifications, and validated components belonging to the current project and compatible with the current request. Small changes do not require repeating research or planning. Establish whether the requested deliverable is an image, prototype, or implemented interface; the implementation steps below do not expand an image-only task into application development.

## Open-ended redesigns

A request to redesign the interface without specifying a style is sufficient to begin product research and art direction. Inspect the current product, select a suitable direction, state the choice briefly, and proceed within the requested scope. Ask only when missing product constraints materially change the task; aesthetic choices alone do not require the user to become the designer.

Users need not name design methods. Translate ordinary preferences and supplied references into [concrete visual decisions](references/art-direction.md#interpret-ordinary-language), then select methods. Missing style terminology is not a reason to fall back to a stock theme or reduce the requested expressive ambition.

Preserve data, capabilities, workflow semantics, stack, and explicit brand constraints. Existing layout, decorative copy, typography, color, and component styling are candidates for revision, not automatic invariants. Distinguish user-mandated constraints from incidental styling in the current code. Reuse sound logic and accessible behavior while adapting presentation. A local repair still stays local; a full redesign is not limited to recoloring existing components, nor does it require replacing a layout that already serves the task.

## Content and reuse boundaries

- Preserve user-supplied identity, content, assets, and established conventions unless their revision is requested; apply the redesign boundary above to existing presentation. Familiar functional labels and effective components may remain unchanged.
- Create missing sample content from this task's domain, audience, locale, and shown state. Keep invented names, records, and values coherent within the project; distinguish demonstration content from verified claims. Reference brands, slogans, narratives, and imagery are not default content.
- Give interface copy a user-facing purpose using the [copy review](references/visual-quality.md#purposeful-interface-copy). Let content and actions determine text; do not invent prose to fill a layout.
- Extract mechanisms and visual relationships from examples; derive composition, palette, material placement, and method combinations from the current brief. Carry specific reference details over when the user requests them, respecting asset permissions.
- Treat README showcases and archived generation prompts as documentation. Read them for showcase maintenance or an explicit reference request, not as starter prompts for unrelated designs. For the actual implementation or image prompt, include only adopted relationships and current-project content.

## 1. Establish the product and design basis

- Read project instructions, relevant components, themes, and dependency configuration. Identify existing changes and how to run the project. Preserve the requested product, content, brand, functionality, and stack. Attachments are references, not automatic scope extensions.
- Establish the main task, critical actions, content density, and target devices. Distinguish [usage context from delivery platform](references/art-direction.md#identify-the-usage-context): a browser can host an application, and a desktop window does not prescribe a dashboard. State reasonable assumptions and proceed; ask only about consequential missing information.
- For new designs or full redesigns, actively research similar products, related themes, and distinctive design examples online before finalizing the direction. Open original sites using [design research](references/design-research.md); a technical recipe alone does not replace this step. Reuse sufficient, relevant research for the current project and fill gaps. Respect restrictions on browsing and state the resulting evidence boundary.
- Use [method selection and visual compatibility](references/design-directions.md#selection-and-combination) to establish a product-specific visual language, then choose complementary methods. Define their roles and how adjacent components belong together; category names alone cannot determine a palette or component skin. Read the selected recipes. Respect local repairs and explicit style constraints without forcing effects into them.
- For new links, unstudied mechanisms, or persistent mismatch, inspect concrete cases: view the page, exercise relevant interactions when possible, then examine implementation. Search snippets and directories do not replace observation. Distinguish screenshots, direct interaction, author statements, and inference.
- Translate research into: **specific reference relationship → project region/state → expected appearance or change → acceptance evidence**. Record why it fits. Add implementation and failure handling when a mechanism is involved. The [case index](references/studied-cases.md) records research depth; the [coverage record](references/research-coverage.md) supports maintenance. Leave untested behavior explicitly unverified.
- Use supplied images for their stated purpose. Category illustrations do not automatically prescribe colors, objects, layout, or intensity. Match a particular image only when the user requests reproduction; select project assets from the current theme and design decisions.

Complete when the main task, required content, visual basis, and suitable expressive methods are clear. Correct visual and interaction drift without switching the product or replacing all example content merely to create difference.

## 2. Write a short implementation specification

- Use the [specification guide](references/implementation-spec.md) to decide concrete first-viewport structure, sizing rules, tokens, representative region, key states, narrow-screen behavior, fallback, and evidence. Adjectives such as premium, modern, or immersive are insufficient.
- When a new design is open-ended or aesthetically underdeveloped, use [art direction](references/art-direction.md#develop-the-visual-idea) to select a composition with a product-specific visual idea. Carry it into layout and detail, beyond one attractive image. Implement that decision consistently and revise affected decisions when usability conflicts emerge.
- Use [implementation choices](references/implementation-spec.md#implementation-choices) to select DOM/CSS, images, SVG, Canvas, or real-time 3D. Modeling is optional: use it when explicitly requested or essential to the core experience. Sophistication, depth, or material richness alone does not require a 3D engine.
- Keep the specification in existing project design or work records, outside the product UI. Implementation chunks need only relevant decisions, interfaces, and completion criteria. Local adjustments require neither extra documentation nor a fixed approval stage.
- For complex materials, inspect existing components and selected recipes first. Prepare suitable assets and define structure, parameters, and state before implementation to reduce repeated invention.

Complete when implementation no longer needs to invent the layout, material placement, or critical behavior.

## 3. Complete a representative region, then expand

- The representative region must demonstrate the dominant visual feature and one real action. Before expanding, inspect whether the intended feature is perceptible at normal viewing size, feedback matches the action, and text remains clear. Asset detail and clickable buttons are separate, partial evidence; neither proves whole-page art direction. Correct composition, assets, and state relationships before polishing unrelated geometry. Deliver only a specification when that is the requested scope.
- Reuse suitable current-project logic and components without treating their existing styling as mandatory. Implement missing mechanisms from selected recipes and verified cases, following the content and reuse boundaries above.
- Use semantic DOM for text and actions. Navigation, data, playback, and saving must correspond to real behavior. State simulation boundaries accurately: a timer is not audio playback, and a toast is not persistence. Omit out-of-scope actions or disable them accurately.
- Preserve relationships among content, tools, and temporary layers. Glass need not cover body content; three columns do not establish spatial depth. Containers should express independent objects or surfaces rather than wrap every paragraph. Derive chart marks and labels from the same data.
- Preserve critical actions when rearranging narrow layouts. Check long and localized text, keyboard paths, focus, and return from overlays. Provide a readable surface without filters and preserve state and functionality with reduced motion. Release listeners and rendering resources with their owners; pause expensive effects while hidden.

Complete when the representative region and the task's consequential states have been inspected, the full flow follows coherent visual rules, and the core task still works if visual enhancements fail.

## 4. Correct observed differences and deliver

- Review in this order: **direction match → product usability → template patterns and detail**. Fix known blockers to actions or readability immediately. Anti-template rules constrain mechanical repetition; they do not remove requested glass, volume, highlights, or motion.
- After the main design is implemented, use [visual review](references/visual-quality.md). Record discrepancies as **location → expected → actual → correction → recheck**, following [evaluation and iteration](references/evaluation-loop.md). Preserve successful decisions instead of regenerating the whole page for a local issue.
- Run relevant project checks, respecting the user's validation restrictions. Inspect desktop and narrow layouts, critical actions, and affected states in a browser. Screenshots cannot prove sound, motion, persistence, or service connectivity. Mark checks not performed as unverified.
- Do not automatically switch models, launch agents, or retry indefinitely. Make targeted corrections with the current model. If escalation is necessary, explain the gap and prepare relevant specifications, screenshots, and reproduction steps.
- Deliver concise file or preview links, material changes, validation, and practical limitations. Keep design rationale, stack details, and acceptance notes in the delivery rather than the product UI. Clean up only temporary processes created for this task whose ownership is confirmed.

Complete when direction and functionality have separate evidence and applicable rejection conditions are resolved. Compilation and self-assessment do not establish visual acceptance.
