# Spatial UI: depth and interaction responsibilities

Last reviewed: 2026-09-23. Apple's official transcript and W3C modal patterns were read; no headset testing was performed.

## Research basis

- [Apple WWDC23](https://developer.apple.com/videos/play/wwdc2023/10072/), Dimensional: nearby controls and distant subjects can use different scales; occlusion and light/shadow reinforce hierarchy. Subtle depth can suffice, while interface text should stay planar. Headset field of view and physical distance are not direct Web parameters.
- [W3C modal dialog pattern](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/): the visual and interactive foreground must agree. Background content is inert, and closing restores appropriate focus. Setting aria-modal alone does not implement background isolation.

## Web implementation recipe

1. List content, persistent tools, temporary layers, and their scroll containers in the specification. Give each layer a real responsibility. Three columns are not three depth layers.
2. Associate persistent tools with the object being manipulated without covering critical content. Use native dialog or an established project overlay when temporary work must block background interaction. Nonmodal tools should not arbitrarily steal focus.
3. Opening establishes foreground focus/emphasis and controlled background de-emphasis; action or cancellation closes the layer and returns focus to the trigger or logical next position. Use top-layer/component layering facilities rather than continually increasing z-index.
4. Decorative pseudo-elements are not interactive layers. Hit areas must match visual positions. Keep text readable without whole-page perspective.
5. Narrow layouts can use drawers or sequential organization while retaining entry points and task state. Reduced motion removes retreat/parallax while occlusion, surfaces, and boundaries preserve hierarchy.

## Acceptance

Open with a keyboard, navigate with Tab/Shift+Tab, close with Escape and the close control, and verify focus return. Modal background content has no interactive path. Reopening restores the intended product state. Compare occlusion on desktop and narrow screens; screenshots cannot prove focus handling or headset behavior.

2D depth and native dialogs are not a visionOS implementation. Ordinary control groups can retain individual Tab stops. If using role=toolbar, implement its focus and arrow-key contract, including slider key conflicts, rather than changing ARIA labels alone. See [W3C Toolbar](https://www.w3.org/WAI/ARIA/apg/patterns/toolbar/).
