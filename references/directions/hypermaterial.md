# Hypermaterial / Neo-Aqua: distinguish material mechanisms

Last reviewed: 2026-09-23. Hypermaterial and Neo-Aqua are descriptive labels for digital-material expression, not an official design standard.

## Research basis

[MeshPhysicalMaterial](https://threejs.org/docs/pages/MeshPhysicalMaterial.html) distinguishes transmission, thickness, index of refraction, iridescence, and coating. [MeshStandardMaterial](https://threejs.org/docs/pages/MeshStandardMaterial.html) distinguishes roughness and metalness.

The [official transmission example source](https://github.com/mrdoob/three.js/blob/dev/examples/webgl_materials_physical_transmission.html) exposes environment, view, and independent material parameters in a GUI. Its values are not universal defaults.

Direct observation of the [live example](https://threejs.org/examples/webgl_materials_physical_transmission.html) on 2026-09-23: increasing roughness from 0 to 0.5 blurred the transmitted region. After restoring roughness to 0, increasing thickness from 0.01 to 2 changed the internal background image and edges. The observation covers those parameter changes only; cross-device performance and soft-body interaction were not evaluated.

## Material selection

Use [implementation choices](../implementation-spec.md#implementation-choices) to decide between static appearance, 2D feedback, and real-time optics/geometry. Parameters below explain selected real-time physical materials; they do not mandate Three.js or modeling. Fixed-view heroes can use images/prerendered assets, and controls can use CSS/SVG.

| Material | Relationship to implement | Important distinction |
| --- | --- | --- |
| Crystal/glass | Coordinate transmission, thickness, IOR, and environment reflection | Lower opacity alone is insufficient; physical transmission generally keeps opacity at 1 |
| Gel | Volumetric transmission, with separately implemented deformation/rebound if promised | Transmission parameters do not generate soft-body motion |
| Ceramic | Opaque silhouette, roughness, and highlights, optionally a glaze | Transparency is not the default |
| Liquid metal | Environment reflections change continuously with normals/deformation | Metalness does not make geometry flow |
| Iridescence | Thin-film color shifts with viewing/lighting angle | Static rainbow gradients, transmission dispersion, and iridescence are distinct mechanisms |
| Neo-Aqua | Highlights, thickness, translucent controls, and contemporary content hierarchy | Not a Three.js material class and not a requirement for full-page 3D |

## Implementation and acceptance

Choose the material appearance, product object, and light environment first. Check silhouette, highlights, and content clarity for the actual implementation. Materials may concentrate in the hero while body content and controls retain clear relationships.

For real-time materials, define which parameters or normals input changes. Vary angle, thickness, and roughness independently and inspect silhouette, interior, and reflection. If deformation is promised, verify input, force response, release, and reset separately. Static implementations do not require unrequested rotation/deformation. Brightness cannot substitute for material identity.

Complex shader features increase per-pixel cost. Lower transmission resolution or remove nonessential layers when necessary; manage resources/state using the [Shader recipe](shader.md). Fallback preserves the object's silhouette, meaning, and hit target. Explainable parameters are not evidence of cross-device visual or performance acceptance.
