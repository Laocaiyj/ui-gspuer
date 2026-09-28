# From design instructions to rendered quality

Reviewed: **2026-09-27**. This research supplements [six-method research](six-method-research.md) with primary-source support for early rendered studies and separate visual and functional review.

## Problem and evidence boundary

A written direction cannot establish how composition, imagery, materials and controls work together in an implemented interface. This review examines methods for inspecting those relationships before extending a design across pages. Source findings support the workflow; they do not establish a measured improvement in this skill's output.

## Primary-source findings

| Evidence | Implication to test in this project |
| --- | --- |
| Design Council separates exploring possible answers from selecting one, and recommends small-scale testing, rejection and improvement. [Framework for Innovation](https://www.designcouncil.org.uk/resources/framework-for-innovation/) | For a new art direction, compare small rendered studies before propagating a weak choice across pages. Their number and fidelity should follow the uncertainty, not a mandatory multi-proposal ceremony. |
| Anthropic's frontend experiment used live-page inspection and separate assessment of design, originality, craft and functionality. It reports generous self-assessment, convergence from evaluative wording, and cases where an intermediate version was preferable to the last. [Harness experiment](https://www.anthropic.com/engineering/harness-design-long-running-apps) | Use actual rendered evidence and retain a comparison checkpoint. A revised page must improve the identified discrepancy; additional effects or a longer rationale do not establish improvement. Do not import the experiment's expensive iteration count or claim its results generalize to other models. |
| Anthropic's current frontend skill grounds choices in subject matter and allows the opening to be an image, interaction, typography or another appropriate treatment. [Source skill](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md) | Select the composition from the subject's characteristic experience. Avoid converting this source's specific typography prohibitions into universal rules. |
| Sonos describes a shared illustration language that communicates different hardware/software experiences, alongside a flexible identity system. [Sonos design account](https://www.sonos.com/en-au/blog/sonos-brand-design-refresh) | Preserve common visual rules while letting different content require different representations. Consistency need not mean placing the same emblem in every section. This account supports a design approach, not an independently measured aesthetic outcome. |
| Google reports iterative screen testing against intended emotional qualities, alongside navigation and accessibility. [Expressive design research](https://design.google/library/expressive-material-design-google-research) | Check whether the intended character survives in actual screens and task states. Successful interaction alone does not establish expressive quality; expressive intensity must retain clear actions. |
| Apple describes geometry-responsive highlights and coordinated optics, motion and environment. Three.js recommends environment lighting for its standard PBR material. [Apple material principles](https://developer.apple.com/videos/play/wwdc2025/219/), [Three.js material documentation](https://threejs.org/docs/pages/MeshStandardMaterial.html) | Inspect material within its final surroundings: silhouette, light, shadow and backing should support the intended appearance. This does not require glass, realism, WebGL or 3D modeling. |
| Anthropic recommends evaluation before extensive instructions, minimal changes addressing observed gaps, and tests with the intended models. [Skill authoring guidance](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices#evaluation-and-iteration) | Test this candidate against actual output. A text-only probe can verify instruction uptake but cannot demonstrate improved visual quality or lightweight-model equivalence. |

## Workflow synthesis

These are project recommendations inferred from the evidence above, not requirements asserted by the sources:

1. **Establish a visual target.** Translate relevant reference observations into the current content, composition and material relationships. Record what must remain recognizable and what may vary. Keep this reasoning outside product copy.
2. **Render a representative slice early.** Include the defining visual, real text and an important control in their intended surroundings. Inspect both wide and narrow layouts. Where competing treatments remain uncertain, compare small alternatives before expansion.
3. **Expand through content.** Carry shared type, color, lighting and motion relationships into a materially different content region or task state. Change its visual representation when the content calls for it; ordinary repeated controls should remain consistent.
4. **Repair the largest observed gap.** Compare the rendered slice with the target and previous version. Identify a visible discrepancy, change its cause, and inspect again. Preserve the stronger checkpoint if the revision regresses.
5. **Verify appearance and behavior separately.** Inspect representative pages and interaction states; report unavailable evidence explicitly. Do not substitute build success, attractive assets or method names for page-level acceptance.

## Evaluation contract

Freeze a shared brief, model configuration, resources and viewport sizes before comparing no-skill, current-skill and candidate runs. Preserve screenshots and task-state evidence. Review composition, subject specificity, coherent material cues, content differentiation and narrow-screen hierarchy separately from functional correctness. Repeated runs assess stability; a second subject checks whether the improvement merely memorized the sound-exhibition example. Report preferences as judgments with concrete visual reasons, not a universal beauty score.

No claim of improved aesthetics, artist-level output or cross-model parity follows from this research alone. Such claims require rendered comparative results and user acceptance.
