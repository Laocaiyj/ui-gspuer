# Liquid Glass: environmental response in tool surfaces

Last reviewed: 2026-09-23. Based on Apple's official transcript and MDN; native-system behavior was not directly tested.

## Research basis

- [Apple WWDC25](https://developer.apple.com/videos/play/wwdc2025/219/), Dynamics, Adaptivity, and Principles: the native material combines optics, deformation, and environmental response. Separate tools from content and avoid glass on glass. Regular and Clear have different conditions of use; greater transparency is not inherently better.
- [MDN backdrop-filter](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/backdrop-filter): the filter processes pixels behind an element. Ancestor opacity/filter and other backdrop-root conditions affect the sampling boundary and can explain an apparently ineffective blur.

## Web implementation recipe

1. Identify the content each tool operates on and its depth relationships when closed, expanded, or scrolling. Develop against complex imagery/text, not only an empty background.
2. Specify the capability: CSS approximation or actual background-sampling refraction. An approximation combines a translucent base, edge highlights, local blur, and shadow. Computed refraction needs a suitable rendering path; do not rename an approximation as the native system.
3. As content changes, keep tool labels readable through controlled tint/masking. Selection or expansion should coordinate shape and depth. Keep text/actions in DOM; avoid reducing group opacity so that text becomes transparent too.
4. Check light, dark, and complex backgrounds. State the backing conditions for a Clear-like high-transparency treatment. Avoid unnecessary whole-surface light/dark jumps on large surfaces.
5. Normal mode retains the selected translucent characteristics. A no-filter or solid mode uses an opaque readable base; reduced motion preserves state.

## Acceptance

- The rendered view shows a meaningful tool/content relationship. Scrolling content does not obscure labels or focus indicators.
- Opening, closing, and rapid reversal leave no stale masks or incorrect hit areas.
- Assess a CSS approximation against its stated capability. If refraction is required, verify geometry-related changes in background sampling; ordinary blur is insufficient.

Validate the approximation in the current project. Native automatic adaptation does not arrive with a CSS property.
