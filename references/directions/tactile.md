# Tactile UI: separate input, action, and rebound

Last reviewed: 2026-09-23. Motion documentation and author gesture examples were inspected; remote examples were not directly exercised.

## Research basis

[Motion gestures](https://motion.dev/docs/react-gestures#tap) distinguish press, successful release, and cancellation by releasing outside. [press](https://motion.dev/docs/press#press-end) exposes success at the end and returns a cleanup function when registered. [Spring transitions](https://motion.dev/docs/react-transitions#type) distinguish physics parameters from duration/bounce configuration; mixing them does not mean every value applies. The [author example](https://motion.dev/examples/react-gestures) coordinates multiple properties with gestures but does not implement a product commit, so it is not a finished acceptance case.

## Implementation recipe

1. Define idle → pressed → committed/cancelled → idle. Loading and selected are product states, not consequences of animation completion.
2. Choose a coherent force interpretation: a depressed surface with a shorter contact shadow, or drag damping and snap. There is no universal scale(.98) or heavy-shadow requirement. Press deformation must not move the target away from the pointer.
3. Let native buttons handle activation and visual layers receive pressed/disabled/selected state. Normally commit once on successful release and never on cancellation. Other commit timing needs a task-specific reason and suitable undo design. See [W3C pointer cancellation](https://www.w3.org/WAI/WCAG22/Understanding/pointer-cancellation.html).
4. Clear force state on outside release, pointercancel, focus loss, and teardown. Rapid reentry takes over from the current visual position rather than stacking competing animations. Valid actions need not wait for rebound.
5. Verify Enter/Space and touch without hover dependence. Reduced motion retains pressed/selected contrast while removing exaggerated travel. Missing vibration must not affect product behavior. Respect the project's framework; Motion is optional.

## Acceptance

Check hold, successful release, outside cancellation, repeated input, and disabled states: one commit, no stuck state or false success, and feedback consistent with the action. For dragging, also check scroll takeover, bounds, and cancellation during snap.

CSS displacement/shadow feedback, physical springs, soft-body simulation, and device haptics are different capabilities. Verify only the capabilities actually promised, and do not conflate them.
