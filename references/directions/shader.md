# Shader UI: verify the path from input to pixels

Last reviewed: 2026-09-23. Three.js documentation, example source, and the WebGL specification were read. Performance still requires measurement on target devices.

## Research basis

The GLSL route in [ShaderMaterial](https://threejs.org/docs/pages/ShaderMaterial.html) targets WebGLRenderer and takes changing values through uniforms; it is not a universal WebGPURenderer material.

The [official lava source](https://github.com/mrdoob/three.js/blob/dev/examples/webgl_shader_lava.html) uses time, noise, and two textures to change a surface. It is a rendering example, not a product interface.

[WebGL context recovery](https://registry.khronos.org/webgl/specs/latest/1.0/#5.15.2) and [Three resource disposal](https://github.com/mrdoob/three.js/blob/dev/manual/pages/how-to-dispose-of-objects.html) establish context and geometry/material/texture/render-target lifecycle concerns.

## Implementation recipe

1. Specify WebGL/GLSL or WebGPU/TSL/WGSL and verify the project's pinned versions. CSS/SVG may satisfy an appearance-only goal; when shader behavior is explicitly required, a static substitute is fallback only.
2. Define input range, coordinate system, reset conditions, and whether input changes UVs, normals, vertices, colors, or refraction sampling. Time-driven decoration is valid when appropriate, but is not pointer response.
3. Normalize pointer coordinates against actual canvas bounds. On resize, synchronize camera, drawing buffer, resolution uniforms, and render targets. Keep text/actions in DOM and avoid intercepting unrelated clicks with the canvas.
4. Provide readable fallback for initialization, resource, or compilation failure. Stop drawing on context loss and resume after renderer-appropriate resource recovery; avoid unbounded instance recreation.
5. Pause owned loops/listeners when hidden or unmounted. Dispose GPU objects according to ownership; unmounting one component must not delete shared textures. Render on demand for stable scenes.

## Acceptance

Two different inputs should produce explainable visual differences. Check resize, resource failure, context loss/recovery, repeated mounting, and reduced motion. Define the device, viewport, duration, and frame-time budget before measuring. If over budget, reduce resolution, postprocessing, samples, or transparent layers while preserving the main mechanism. A DPR cap or GPU usage is not evidence of smooth performance.

renderer.info caches need not reach zero. Inspect stability and ownership instead of classifying every retained object as a leak.
