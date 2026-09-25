# Kinetic Typography: changing text with intact semantics

Last reviewed: 2026-09-23. Official documentation and GreenSock example source were inspected; the remote example was not directly exercised.

## Research basis

- [MDN font axes](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-variation-settings#description): supported axes and values come from the actual font; prefer higher-level CSS properties where applicable.
- [GSAP SplitText](https://gsap.com/docs/v3/Plugins/SplitText/), Responsive Line Splitting, onSplit, and Accessibility: font/width changes can invalidate lines, and resplitting requires old-animation cleanup. The default ARIA strategy does not preserve every nested-link semantic.
- [GreenSock AutoSplit + ScrollTrigger](https://codepen.io/GreenSock/pen/GggpRoB): splits after fonts are ready and drives masks with scroll progress. Initial opacity:0 depends on JS restoration and must not be copied unconditionally.

## Implementation recipe

1. Define the trigger—entry, scroll, focus, or state—and whether it repeats or reverses. Use selected words, short headings, or navigation; keep body text, prices, and form labels stable.
2. Specify the changing property and its meaning: weight, width, position, or mask. Static oversized text is not kinetic typography.
3. Keep default HTML readable and enable decoration only after successful initialization. Check glyph coverage, axes, and font license. CJK text cannot be split into words by spaces alone; preserve Unicode grapheme clusters.
4. Recalculate after delayed font loading, wrapping, or breakpoint changes. Dispose old timelines before rebuilding. Restore original DOM or equivalent semantics on teardown. Reserve space so changing weight/width does not displace nearby controls.
5. Preserve link/button semantics and focus; prevent decorative duplicates from being announced twice. Reduced motion, font failure, or script failure must show complete, stable text immediately.

## Acceptance

Inspect before/during/after the trigger, rapid reverse scrolling, narrow reflow, and completed font loading. Text must not clip, split incorrectly, or disappear, and keyboard links still work. Animation code alone cannot prove screen-reader behavior.

Check GSAP licensing separately from font/image licensing; free use is not synonymous with MIT. Do not copy unverified example assets. Simple effects can use CSS/SVG without a text-splitting library.
