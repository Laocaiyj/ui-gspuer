# Evidence-based acceptance and iteration

Use for redesign reviews, repeated shortfalls, or requested model comparisons. Continue with the current model. This document does not authorize automatic model switching, agents, or batch evaluation.

## Correct an explicit discrepancy

Hold the brief, content, viewport, and current state constant. Compare the reference/specification with the rendered page. Record each finding as:

`Region | Expected | Actual evidence | Change | Recheck result`

Fix action/readability blockers immediately, then missing composition or direction, then control consistency and spacing. Address a group of issues with a shared cause, preserve successful design, and recheck affected states. A button-spacing defect does not justify rebuilding the page.

For recurring defects, check whether references are visible, the specification is concrete, or assets/components are missing. Improve those inputs or use a working component rather than accumulating prohibitions and retry quotas. Report unresolved gaps honestly. If the user approves escalation, supply relevant decisions, screenshots, files, and reproduction steps.

| Cause | Next action |
| --- | --- |
| Missing visible reference or mechanism evidence | Open a concrete case and establish triggers and states instead of adding adjectives |
| Ambiguous or conflicting specification | Fix relevant decisions about composition, necessary mechanisms, parameters, and completion criteria |
| Coherent but aesthetically undistinguished result | Revisit the [visual idea and art-direction review](art-direction.md); compare composition and craft with the selected references before adding effects |
| Concept image drifts from a concrete brief | Check which decisions reached the actual generation prompt; revise the prompt or image without treating a static mockup as an implemented interface |
| Unrelated reference content or composition recurs | Trace it to the brief, loaded examples, or generation prompt using the [reuse review](visual-quality.md#before-delivery-inspect-the-rendered-page); replace unsupported carryover and preserve valid project content |
| Code or state defect | Reproduce and locate event, data, lifecycle, or resource errors |
| Valid code but mismatched rendering | Compare equivalent screenshots and real interactions; adjust proportions, surfaces, or timing and recheck |

Diagnose before choosing whether to revise the specification or implementation. Keep four evidence levels separate: **rules documented**, **component validated**, **generation validated across tasks**, and **controlled model comparison**. Earlier levels do not prove later ones.

## Acceptance threshold

Record **pass / needs revision / unverified** with evidence for each dimension. Report only material conclusions in ordinary delivery. An average score cannot compensate for broken functionality or a missing direction.

| Dimension | Basis |
| --- | --- |
| Direction match | Adopted relationships are visible in their intended regions/states at the specified intensity; inspect relevant composition, light/color, material, hierarchy, or motion. Technology names are not evidence |
| Overall design | Coherent hierarchy, density, letterforms, and spacing across the complete page at the same viewport |
| Product identity | Content and actions reflect the actual task, without unsupported metrics, generic slogans, or developer explanations filling space |
| Execution detail | Relevant checks for long/localized text, narrow layouts, page endings, control states, and focus |
| Functional usability | Critical actions produce accurate results; applicable empty, error, cancellation, and fallback paths are exercised |

Static screenshots verify static appearance. Motion requires trigger/process inspection, media requires real media-state inspection, and persistence requires reloading. Mark unavailable checks as unverified; source inference is not runtime evidence. Automation can check overflow, action results, and errors, but color or vocabulary scans cannot certify an absence of generic aesthetics.

When functionality passes but art direction does not, preserve verified behavior and return to the reference mapping. When assets are detailed but the page lacks identity, correct page relationships first. Do not remove explicit art-direction goals to eliminate an acceptance gap. Technical simplification must still meet the original target.

## When the user requests model comparison

Record both model and reasoning effort. Hold the task, starting code, skill revision, references, tools, context, and acceptance threshold constant. Compare configurations through repeated independent runs; one screenshot cannot establish a stable success rate.

Use different task types to avoid learning one workspace layout:

- Object-editing task: clear content/tool relationships and one real editing action.
- Dense data interface: shared baselines, stable density, and real filtering without forced giant decoration.
- Mobile page for a specified brand: retained brand/content, a critical action, and narrow-screen adaptation.

These are coverage examples, not an automatic execution checklist. Generate independently and hide model labels during review when practical. Record first-pass/final acceptance, revision rounds, elapsed time, and available usage/cost data. Cost per accepted result includes research, retries, and stronger-model corrections, not just the first generation.

No controlled comparison currently establishes equal acceptance rates between lightweight and stronger models. The workflow reduces unresolved design decisions; it does not guarantee elimination of model differences.

Sources: [OpenAI accuracy optimization](https://developers.openai.com/api/docs/guides/optimizing-llm-accuracy) for clear instructions, relevant context, examples, decomposition, and evaluation; [model selection](https://developers.openai.com/api/docs/guides/model-selection) and [deployment evaluation](https://developers.openai.com/api/docs/guides/deployment-checklist#choose-a-gpt-56-model) for task-level comparisons. Last reviewed 2026-09-23. Model names and documentation can change; use currently available configurations. The UI correction workflow is this skill's application of those principles, not an official outcome guarantee. Longer prompts are not necessarily better guidance.
