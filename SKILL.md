---
name: ui-gspuer
description: Use when designing or redesigning Web interfaces, browser or desktop app frontends, or static UI concepts, including generic-looking results, mismatched styles, and requests without design terminology. Not for backend-only work.
---

# ui-gspuer

Select Liquid Glass, Tactile, Expressive, Shader, Spatial, and Hypermaterial methods for the product. No fixed combination or 3D requirement. Follow the user's language.

## Route by task

Read relevant references.

| Request | Route |
| --- | --- |
| New interface or full redesign | [Research](references/design-research.md) → [art direction](references/art-direction.md) → [specification](references/implementation-spec.md) → implementation |
| Static concept image | [Concept workflow](references/art-direction.md#concept-image-workflow); deliver the image, not an application |
| Local adjustment | Inspect affected code and the relevant [method recipe](references/design-directions.md); keep scope local |
| Review or template correction | [Visual review](references/visual-quality.md); change files only when requested |
| Research or specification only | Deliver the requested findings or specification; stop before implementation |
| Repeated failures or model comparison | [Evaluation](references/evaluation-loop.md); separate documented rules from observed behavior |

## Open-ended redesigns

Infer [usage context](references/art-direction.md#identify-the-usage-context) from tasks, screens, and project configuration. Browser applications need workflow design; public presentation and reading have different priorities.

Translate [ordinary preferences](references/art-direction.md#interpret-ordinary-language) into concrete visual choices. Research, choose a direction, state it briefly, and proceed. Ask only about consequential missing constraints, not style vocabulary.

An unnamed style is not a request for a neutral editorial skin. Choose a content-specific visual idea and observable method cues; paper colors, serif type, decorative rings, or subtle shadows alone do not establish the selected direction.

Preserve data, capabilities, workflow semantics, stack, and explicit brand requirements. Existing layout, typography, decoration, and component styling may change during a redesign. Reuse logic without freezing presentation.

## Content and reuse boundaries

Keep current-project identity and valid content. Create necessary sample data for this task and distinguish it from real records. Each piece of [interface copy](references/visual-quality.md#purposeful-interface-copy) needs a user-facing purpose.

References supply relationships, not default brands, slogans, layouts, or palettes. Treat attachments according to their stated purpose. Match an image when reproduction is requested. Read README showcases and archived prompts for documentation work or explicit reference requests, not as unrelated starter prompts.

## Execute and verify

For new pages and full redesigns, put three explicit records in the working specification. For brief-only tasks, include them in the delivered brief:

- **Page sequence:** Region jobs, decision groups, dominant content, and neighboring relationships.
- **Region sizing:** Content that sets height, reserved space for changing states, and result placement.
- **Visual proof plan:** Adopted reference qualities, comparable rendered views, detail states, and matched before/after conditions; distinguish improvement from meeting the target.

Use task-specific decisions, not headings alone. Existing records can satisfy this contract without duplication; use the [composition procedure](references/art-direction.md#compose-the-page).

For every new page or full redesign, settle the **defining visual and its production route** before styling the whole page. Record required visual qualities, source/tool, and the resulting asset path or procedural implementation. If a fixed-view subject needs photographic, illustrative, textural, or material detail and no suitable supplied/licensed asset exists, use the available image-generation workflow and integrate its output before visual acceptance. A promise to add artwork later, or code-drawn placeholder shapes, does not complete that step. Keep semantic controls, data graphics, and genuinely procedural visuals in code; a text-led page or local repair need not acquire imagery.

Use the [production-media procedure](references/implementation-spec.md#production-media) for asset briefs, production evidence, decoration choices, and neighboring boundaries. Review the actual composition wide and narrow; existing decoration is open to revision.

When feedback rejects a media-led draft's generic artwork or lack of visual richness, name the replacement subject, select its production source/tool, and make one integrated replacement the next visual deliverable. Settle that choice now instead of handing off "generate if needed." Keep the artifact pending until produced and inspected; layout alternatives may share it.

**Repeated direction rejection or unresolved focal alternatives:** For implementation tasks, follow the [render checkpoint](references/art-direction.md#render-before-expanding): produce two structurally different renderable compositions, their wide/narrow evidence, and a selection tied to reference qualities. Use its recheck and expansion decision before propagating the direction. Local repairs and requested reproductions follow their own routes above.

1. **Ground the direction.** Inspect the project and existing constraints. For new designs, study relevant original sites using the research guide. Reuse sufficient current-project research; disclose unavailable evidence. Record adopted relationships.
2. **Make decisions executable.** [Compose the page](references/art-direction.md#compose-the-page) around content relationships before styling components. Use [method selection](references/design-directions.md) and selected recipes for material roles, actions, and adaptation. Select and deliver [production media](references/implementation-spec.md#production-media) when the defining visual needs it. For input-driven methods, include trigger → visible response → commit/cancel → fallback. State which visible cues distinguish each chosen material from a generic shaded shape.
3. **Render before expanding.** Build a [representative composition](references/art-direction.md#render-before-expanding) with real content, defining visual, and a working action. Complete that checkpoint before expanding through content-specific forms and consequential states. Preserve semantic controls and state continuity.
4. **Compare and correct.** Check [direction acceptance](references/direction-acceptance.md) against actual output. Compare the revision with its saved predecessor; retain the stronger result. Exercise actions, keyboard paths, narrow layouts, and reduced motion separately. Static images establish only visible states. Report unresolved visual gaps even when functionality passes.

Deliver links, changes, evidence, and gaps. Keep process notes outside the product. Mark unperformed checks unverified and respect validation restrictions. No automatic model switching, delegation, or indefinite retries.
