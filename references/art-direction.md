# Art direction and interface concepts

Use for new visual concepts, full interface design, or feedback that a coherent result still lacks artistic distinction. For local repairs, preserve the established direction. This guide supports deliberate design decisions; it does not certify professional stature or guarantee a particular aesthetic outcome.

## Identify the usage context

Determine what users come to do, how often they return, and where the interface runs. Use existing routes, screens, workflows, and project configuration before asking. Classify individual surfaces when one product serves several purposes.

| Usage context | Design priorities |
| --- | --- |
| Public discovery, presentation, or decision-making | Explain the offering with credible content, support exploration and an appropriate next action; narrative and display typography can carry identity |
| Reading, reference, or publishing | Prioritize legibility, orientation, navigation, and content rhythm; neither a sales funnel nor a dashboard is assumed |
| Repeated creation, editing, or management | Keep current objects, tools, state, and frequent actions accessible; preserve work and continuity instead of repeatedly presenting an introduction |

These contexts do not mandate layouts or styles. Separately account for browser navigation and URLs, desktop window behavior and keyboard use, or mobile touch and constrained space as applicable. A responsive website and an installed app can share visual language while needing different navigation and interaction patterns. Reuse existing host chrome; avoid drawing imitation window controls inside the content. Do not change frameworks or delivery platforms merely to match a reference.

## Interpret ordinary language

Treat the user's mood words, dislikes, task descriptions, and screenshots as design inputs. Translate them into choices about hierarchy, density, typography, shape, material, color roles, and motion. Check those choices against the usage context and reference evidence before assigning method names. There is no fixed mapping from an adjective to a palette or one of the six methods.

When preferences are absent, derive a direction from the product, audience, content, and researched examples. When a preference is ambiguous but low risk, state a concrete interpretation and proceed. If plausible interpretations would materially change the experience, ask a short question in ordinary language about the desired experience or a reference; do not require a taxonomy choice. Select methods after the visual intention is clear, and evaluate the visible result rather than whether a style label appears in the brief.

## Develop the visual idea

Start with the user's content and task. Use [design research](design-research.md) for both workflow references and specific art-direction references. Inspect actual imagery and composition, not only project descriptions. If only text is available, label that evidence and do not claim a visual comparison.

Define what should distinguish this particular experience. Connect that idea to the user's activity, then express it through composition, typography, imagery, and selected methods. A genre label, palette, or mood is only one input. Derive the dominant object, content sequence, and control relationships from the task before choosing regions and proportions. Preserve familiar controls where they help the task.

For an open brief, compare plausible directions in a short working note before committing. Compare focal structure, content rhythm, and the relationship between imagery and controls, rather than color variants. Select the direction with the strongest product fit and visible distinction. This does not require generating multiple paid images, creating an approval stage, or redesigning a user-specified layout.

Resolve these decisions in the existing specification or image brief:

| Decision | Concrete description |
| --- | --- |
| Visual idea | What makes this experience recognizable, why it belongs to this product, and where it appears outside a hero asset |
| Composition | Dominant visual mass, supporting regions, relative proportions, alignment, crop, and the purpose of open space |
| Typography | Display versus functional roles, scale contrast, line breaks, tracking appropriate to the language, and alignment with controls |
| Imagery | Subject, framing, light, texture, and its relationship with surrounding surfaces; respect supplied assets and their purpose |
| Materials and color | Distinct base, accent, and state roles; where depth, reflections, roughness, or opacity change and why |
| Signature detail | A content-related treatment that survives beyond a logo or large image, such as a useful indexing rhythm, selection geometry, or control treatment |

Apply [visual compatibility](design-directions.md#visual-compatibility) to integrate the decisions. Sophistication can be quiet or expressive. Darkness, gold, serif type, distortion, asymmetry, or complexity is not a quality threshold. Use them when the product and composition justify them; retain required material expression.

## Carry the direction through the task

For a full redesign, select consequential states from the actual workflow, including content absence and the primary action's destination when applicable. Define how the visual idea carries into their grouping, proportions, controls, and feedback. Shared colors alone do not establish continuity. Dense editing can be quieter than browsing while retaining the same type, shape, and state language; do not decorate every field equally.

Use actual data where available. Review an empty state and a populated state with clearly identified fixtures when needed, without adding fixtures to the user's saved data. Size empty-state illustration and guidance around starting the task; reassess controls that have no useful purpose until content exists. For a static concept, state which view is shown and leave unseen states unverified rather than expanding the requested deliverable.

## Concept-image workflow

For a requested static interface image, use the host's available image-generation workflow. Perform research and art direction first; carry the resulting decisions into the actual generation prompt rather than relying on the generator to infer them from the skill name.

Write the generation prompt from the current specification, following the [content and reuse boundaries](../SKILL.md#content-and-reuse-boundaries). Specify the output format and view, product task and shown state, selected visual idea, concrete composition, type and image treatment, material placement, exact essential labels in the requested language, and details that must remain unchanged. Identify any input image as a reproduction target, a reference, or an edit target. Keep critical content readable; reduce incidental copy when it would become illegible. State positive visual relationships before concise exclusions specific to observed failures.

Inspect the generated image at overall and detail scales. Compare it against the chosen visual idea and the [review criteria](#review-the-art-direction). Check label accuracy, selected states, units, and numeric controls for internal consistency even in fictional examples. Revise the identified discrepancy while preserving successful decisions. A direction error requires revising the composition or brief; a local edge or label error calls for a local edit.

Deliver the requested image and identify it as a concept. An illustrated control or optical effect is not evidence of working interaction or rendering. Save project-bound final images and their production prompts in the project's established location when appropriate; keep process notes out of the depicted product. If generation is unavailable, report the limitation instead of presenting a written brief as a generated image.

## Review the art direction

Review functionality and basic consistency separately from artistic distinction. Use concrete comparisons and mark unresolved differences; self-awarded scores or adjectives do not establish acceptance.

| Dimension | Evidence to inspect | If it falls short |
| --- | --- | --- |
| Composition | Focal hierarchy, deliberate size contrast, crop, spacing rhythm, and supporting regions at the full viewport | Revise proportions and relationships before polishing small controls |
| Distinction | The product-specific visual idea appears in interface relationships beyond the cover image or brand name | Develop the idea further or select a stronger direction; more decoration is not sufficient |
| Craft | Letterforms, localized type, icon weight, edge thickness, material differentiation, and contact shadows at normal size | Correct the specific weak treatment without amplifying every surface |
| Reference translation | Adopted qualities are visible at comparable viewing size and expressive intensity | Restore the missing quality without copying unrelated content or changing the task |
| Integration | Content, controls, and materials form a coherent whole while maintaining their different roles | Use the compatibility checks rather than treating isolated component polish as completion |

A familiar layout can succeed through exceptional proportions and execution; novelty alone is not the objective. Conversely, a clean, usable result does not satisfy an explicit ambitious art-direction brief if its intended visual relationships remain absent.

Separate a manually directed showcase from an independent skill run. Record material human interventions and revision stages when comparing their outcomes. Do not infer reliable first-pass performance, model equivalence, or artist-level results from a curated image. If repeated corrections do not close the visual gap, report the remaining discrepancy rather than continually appending generic prohibitions to the skill.

For previously studied references and their evidence boundaries, consult the [case index](studied-cases.md) when relevant to the current research.
