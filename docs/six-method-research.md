# Six design methods: evidence and remaining gaps

Reviewed: **2026-09-27**.

## Finding

The six methods remain a useful selection framework, but they describe different things: material, feedback, expressive hierarchy, rendering, depth, and experimental material appearance. They are not interchangeable skins or a requirement to use six effects. The current skill already makes these distinctions and permits suitable 2D implementations. The research supports more precise observation of selected mechanisms, not mandatory modeling or a longer list of prohibited styles.

Hypermaterial is used here as an exploratory design label, not a platform standard. Category illustrations describe intended appearance; they cannot establish working optics, motion, performance, or official conformance.

## Primary-source findings

### Liquid Glass: choose the backing conditions, not maximum transparency

Apple distinguishes adaptive Regular from nonadaptive Clear. Clear has three conditions: media-rich backing, acceptable dimming of that backing, and bold, bright foreground content. Compact controls over decorative media may meet them; tools over color-critical imagery that cannot be dimmed do not. These are conditions for Apple's named variant, not a universal prohibition on Web transparency. Apple also describes lensing and geometry-responsive highlights rather than blur alone. [Apple: Meet Liquid Glass](https://developer.apple.com/videos/play/wwdc2025/219/)

The current recipe distinguishes approximated from computed optics but leaves Clear's conditions implicit. A CSS approximation does not inherit native adaptation. A useful visual inference is to inspect whether edges, transmitted detail and highlights describe the same form; a uniform border cannot alone establish lensing. This inference is not a requirement to reproduce Apple's renderer. [Current recipe](../references/directions/liquid-glass.md)

### Tactile: motion follows force and state

Motion separates successful release from outside cancellation. Physics-based springs incorporate velocity, while duration-and-bounce springs do not; inertia can decelerate and interact with bounds. These mechanisms are independent of a glossy raised finish. [Motion gestures](https://motion.dev/docs/react-gestures#tap), [Motion transitions](https://motion.dev/docs/react-transitions#type)

The skill already covers activation, cancellation, interruption, keyboard use and rebound. For a promised continuous drag/rebound, position and velocity continuity deserve inspection. This does not justify adding springs or soft-body simulation to every control, and the PDF's lavender button is not a required skin. [Current recipe](../references/directions/tactile.md)

### Expressive: grouping and continuity matter alongside emphasis

Google identifies color, shape, size, motion and containment as expressive tactics for drawing attention and grouping related elements. Its research also describes reduced usability when an unfamiliar playlist arrangement or missing action labels obscured basic tasks. Its Androidify implementation demonstrates coordinated scale, shape and transitions beyond toolbar styling. These examples do not establish the same performance gains or official Web conformance in another product. [Google design research](https://design.google/library/expressive-material-design-google-research), [Google: Androidify implementation](https://android-developers.googleblog.com/2025/05/androidify-building-delightful-ui-with-compose.html)

The current recipe covers priority and state changes but emphasizes toolbars. Containment and continuity are useful research directions: which objects belong together, what changes between states, and what remains recognizable. No fixed palette, irregular container or obligatory morph follows from those questions. [Current recipe](../references/directions/expressive.md)

### Shader: verify the declared driver

Three.js documents custom GPU shading and changing uniforms, including time. `ShaderMaterial` targets `WebGLRenderer`; a renderer or rainbow appearance alone is not proof of a particular effect. [Three.js ShaderMaterial](https://threejs.org/docs/pages/ShaderMaterial.html)

The recipe allows purposeful time-driven decoration, whereas the acceptance matrix emphasizes input/state changes. That wording is narrower than the supported use case. A slow autonomous shader should be inspected at different times; absent pointer response is not a defect when it was never promised. Actual shader execution, visual fit and measured performance remain separate questions. [Recipe](../references/directions/shader.md), [Acceptance matrix](../references/direction-acceptance.md#direction-acceptance-matrix)

### Spatial: depth expresses responsibility

Apple's spatial-design guidance uses depth, relative scale, occlusion and shadow to relate content and controls, often with subtle depth and planar text. Headset distances are not direct Web dimensions. [Apple: Principles of spatial design](https://developer.apple.com/videos/play/wwdc2023/10072/)

The existing recipe already asks which layer owns input, what sits in front, and where focus returns. No new rule is supported by this audit. A screen-based implementation can establish these relationships without a perspective scene or 3D engine. [Current recipe](../references/directions/spatial.md)

### Hypermaterial: distinguish the visible material relationships

Three.js separates roughness and metalness from transmission, thickness, coating, dispersion and iridescence. These parameters describe different mechanisms; transmission does not supply deformation, and metalness does not make geometry flow. [MeshStandardMaterial](https://threejs.org/docs/pages/MeshStandardMaterial.html), [MeshPhysicalMaterial](https://threejs.org/docs/pages/MeshPhysicalMaterial.html)

The following are perceptual interpretations for project review, not universal physical-material presets:

| Intended material | Visible relationship to inspect |
| --- | --- |
| Metal | Reflected surroundings and light/dark bands that agree with form |
| Ceramic | An opaque body whose silhouette and surface highlights remain coherent |
| Crystal | Interior, transmission and edge/thickness cues that describe the same volume |
| Iridescent coating | Color variation related to the stated view/light behavior, distinguished from an arbitrary rainbow fill |

Fixed-view assets, CSS or SVG can express appropriate appearances. Real-time optics or deformation require separate implementation and evidence when promised. The current recipe already distinguishes these capabilities. [Current recipe](../references/directions/hypermaterial.md)

## Combining methods without creating a new template

The project-level synthesis is to assign complementary responsibilities and inspect their assembled result. Spatial can organize the layers, a material can distinguish a tool surface, and Tactile can explain its response. Shader is a possible implementation route rather than another compulsory visual layer. Expressive grouping can remain clear alongside a material accent. This is an interpretation, not an officially endorsed combination of design systems.

“Cheap plastic” is not a technical material category. The actionable discrepancy is a mismatched mechanism or an incoherent relationship: identical gloss on unrelated materials, highlights unrelated to form, every control competing for attention, or requested expression absent from the actual page. A blanket ban on gloss, shadows or gradients would also reject legitimate uses. Existing [compatibility checks](../references/design-directions.md#visual-compatibility) address these relationships.

## Evidence boundary

This source review identifies implementation distinctions and questions to verify in the target product. It does not establish an aesthetic success rate, independent task acceptance, or equivalence between model configurations. Consult [validation status](../references/research-coverage.md#validation-status) before making release claims.
