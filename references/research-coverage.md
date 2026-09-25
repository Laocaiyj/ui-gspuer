# Research coverage and validation status

This document records the basis and limits of the skill's design guidance. Use it when maintaining sources or assessing release claims. Source review baseline: **2026-09-23**. Editorial and packaging review: **2026-09-25**; this does not constitute a new technical source review.

## Method coverage

The skill focuses on six core methods, with three optional extensions. Each direction has a source-backed implementation recipe and observable acceptance criteria. Selection follows the product's requirements; coverage does not imply that every method belongs in every interface.

| Scope | Methods | Reference |
| --- | --- | --- |
| Core | Liquid Glass, Tactile UI, Material 3 Expressive, Shader UI, Spatial UI, Hypermaterial | [Selection and combination](design-directions.md) |
| Extensions | Kinetic Typography, Game-like UI, Generative UI | [Optional extensions](design-directions.md#optional-extensions) |
| Quality review | Direction match, product identity, execution detail, and functional usability | [Direction acceptance](direction-acceptance.md) and [visual review](visual-quality.md) |

The [case index](studied-cases.md) records primary sources, inspection methods, and observation limits. [Visual review](visual-quality.md#primary-references-and-adoption-boundaries) documents the adoption boundaries for external anti-template guidance. All operating instructions are included in the repository; no private reference document is required.

## Eight discovery entry points

These directories support case discovery. Open the relevant original project before drawing conclusions about its design or behavior. Catalog coverage, membership access, and awards are separate from implementation evidence.

| Entry point | Research use | Verification needed |
| --- | --- | --- |
| [HOVERSTAT.ES](https://www.hoverstat.es/) | Experimental websites and authors | Inspect the original site's performance, accessibility, and product fit |
| [One Page Love Experimental](https://onepagelove.com/genre/experimental) | Single-page composition | Inspect the page and its interactions beyond the thumbnail |
| [Awwwards](https://www.awwwards.com/) | Projects by category or technology | Evaluate the selected example against the current task |
| [Codrops](https://tympanus.net/codrops/) | Author tutorials, source, and demos | Distinguish an effect demonstration from a complete product |
| [Design Spells](https://designspells.com/) | Microinteraction recordings | Verify behavior separately when haptics, timing, or implementation matter |
| [Recent](https://recent.design/) | Typography, motion, 3D, and related work | Investigate the mechanism behind a category label |
| [21st.dev](https://21st.dev/) | React components and structural starting points | Review each component's license, dependencies, and behavior |
| [Mobbin](https://mobbin.com/) | Product screens, elements, and flows | Record which screens or flows were actually accessible and inspected |

## Validation status

| Evidence level | Status | Supported conclusion | Limit |
| --- | --- | --- | --- |
| Documentation coverage | Documented | Nine directions have sources, mechanisms, implementation guidance, and acceptance criteria; four external skills inform visual-review guidance | Written criteria do not establish implementation quality |
| Component observations | Limited, historical | Local CSS-surface, press-feedback, and native-overlay checks were recorded; external transmission observations cover specified parameter changes | The local sample is not distributed, and observations do not establish cross-device performance or accessibility conformance |
| Showcase illustrations | Available | Identity, component, and interface studies illustrate proposed visual relationships and method combinations | Images do not validate interaction, shader execution, or whole-page generation reliability |
| End-to-end generation | Not evaluated under controlled conditions | No general success-rate claim is made across product types | Requires independent task runs and rendered/behavioral acceptance evidence |
| Model comparison | Not evaluated under controlled conditions | No equivalence claim is made between model sizes or reasoning settings | Requires repeated runs with fixed inputs, tools, skill revision, and acceptance criteria |

For controlled evaluation, use [evaluation and iteration](evaluation-loop.md#when-the-user-requests-model-comparison). Keep documentation checks, visual observations, interaction tests, and service integration results separate.

## Maintenance requirements

- When a method changes, update its source date, implementation recipe, and acceptance criteria together.
- Resolve version-sensitive APIs against the target project's pinned dependencies and matching official documentation.
- Record whether evidence comes from documentation, source inspection, recorded media, or direct interaction. Include the tested environment when behavior or performance is assessed.
- Treat previous observations as scoped records. Recheck a case when a new version, requirement, or unresolved discrepancy makes the existing evidence insufficient.
- Update release claims only when the corresponding evaluation has been completed. Editorial revision and successful packaging checks do not upgrade behavioral validation status.
