# Reference cases and evidence

Source review baseline: **2026-09-23**. The table records documentation review, source inspection, and direct interaction separately. Findings are limited to the evidence described; implementation acceptance remains specific to the target project. Each linked recipe contains its primary sources and Web adaptation guidance.

| Direction | Research subject | Recorded evidence | Mechanisms captured |
| --- | --- | --- | --- |
| [Liquid Glass](directions/liquid-glass.md) | Apple WWDC25 Meet Liquid Glass: Dynamics, Adaptivity, Principles; MDN backdrop-filter | Full official transcript and documentation; native system not exercised | Navigation materials, background adaptation, Regular/Clear boundaries, Web capability levels |
| [Spatial](directions/spatial.md) | Apple WWDC23 Principles of Spatial Design: Dimensional; W3C modal dialog | Official transcript and Web interaction specification; no headset testing | Depth responsibilities, planar text, modal background isolation, focus return |
| [Expressive](directions/expressive.md) | Google's Send-action research; M3 Toolbars Overview/Guidelines | Original research plus browser reading of both toolbar pages and illustrations; native email app not exercised | Primary-action placement/size/color, toolbar modes, overflow, narrow layouts |
| [Tactile](directions/tactile.md) | Motion gestures, press, transitions, and author gesture example | Official documentation and example code; remote example not exercised | Successful release, cancellation, repeated input, springs independent of commit |
| [Shader](directions/shader.md) | Three ShaderMaterial, lava example, WebGL lifecycle | Official documentation and example source; lava animation not directly tested | Uniform inputs, renderer choice, context recovery, resource disposal |
| [Hypermaterial](directions/hypermaterial.md) | Three physical-transmission example and material documentation | Source plus browser interaction: roughness 0 → 0.5, restored to 0; thickness 0.01 → 2 | Roughness affected transmitted clarity; thickness affected the internal image; deformation remains separate |
| [Kinetic](directions/kinetic-type.md) | GSAP AutoSplit/ScrollTrigger author example; MDN font axes | Official documentation and example code; remote example not exercised | Font readiness, resplitting cleanup, localized text/link semantics, no-JS fallback |
| [Game-like](directions/game-like.md) | Bruno Simon folio-2025 interaction points, closing manager, quality settings | Author site/repository; driving flow not completed | Input hints, interaction states, exit priority, independent quality settings |
| [Generative](directions/generative.md) | Vercel AI SDK UI weather component, tool streaming, persistence, stopping | Official documentation and code examples; no model service connected | Schemas, stable IDs, retained input, stream states, cancellation, version matching |

The skill distributes methods and case research, without fixed assets or component demos. Implement and verify selected mechanisms in the current project; acceptance does not transfer from a reference case.

## Earlier supplementary cases

Evidence recorded on **2026-09-21**. These entries retain their original verification scope:

- [Codrops glass xylophone](https://tympanus.net/codrops/2026/08/04/building-an-endless-interactive-glass-xylophone-with-three-js/): dragging was exercised and changes in glass-bar color and pose were observed; sound was not verified.
- [Codrops infinite liquid-glass grid](https://tympanus.net/codrops/2026/09/08/building-an-infinite-liquid-glass-grid-with-three-js-webgpu-and-tsl/): article and code excerpts were read; the demo was not exercised, and text rendering varies by version.
- [Pinterest long-press menu recording](https://designspells.com/spells/long-press-menu-in-pinterest): recorded states were viewed; the original application, haptics, and exact timing were not verified.

Extract mechanisms without inheriting unverified performance, accessibility, or platform claims. Reopen specific cases when versions change, mechanisms are missing, or results persistently drift.
