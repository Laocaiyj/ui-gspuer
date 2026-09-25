# Game-like UI: state and navigation support immersion

Last reviewed: 2026-09-23. Author pages and source were read; driving, sound, gamepad, and device testing were not completed.

## Research basis

[Bruno Simon's portfolio](https://bruno-simon.com/) includes exploration, input hints, options, and return paths. Its [game loop](https://github.com/brunosimon/folio-2025#game-loop) separates input, physics, view, and rendering.

[InteractivePoints.js](https://github.com/brunosimon/folio-2025/blob/main/sources/Game/InteractivePoints.js) organizes reveal/conceal/hide/interact and updates hints by input mode. [ClosingManager.js](https://github.com/brunosimon/folio-2025/blob/main/sources/Game/ClosingManager.js) controls exit priority. [Quality.js](https://github.com/brunosimon/folio-2025/blob/main/sources/Game/Quality.js) defines quality tiers; these are not measured frame rates or a reduced-motion policy.

## Implementation recipe

1. Define user goals and states, such as available → focused → activated → completed/failed, with distinct menu/modal/scene state.
2. Drive DOM actions, HUD, and scene feedback from shared actions/state. Map input methods to equivalent behavior and update hints accordingly. Do not force driving, points, or neon into an ordinary workspace.
3. Allow newer state to take over during transitions; old callbacks must not restore stale scenes. Define which layer Escape/Back closes first, then restore operation and appropriate focus.
4. Provide accessible DOM routes to core content and navigation. Canvas text is not automatically semantic text. Sound is not the only feedback, and particle completion is not business completion.
5. Treat quality, mute, and reduced motion independently. Preserve the core content path after graphics failure and let nonessential motion be disabled. Bright, cartoon-like, or soft materials can also support game-like experiences.

## Acceptance

Complete discovery → action → feedback → return. Check consecutive transitions, input switching, and exit priority. Test mute, low quality, and reduced motion separately rather than bundling them into one low-performance mode.

The relevant [W3C animation-from-interactions criterion](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html) is Level AAA with an essential-animation exception. Following this design recommendation does not establish whole-site WCAG conformance. Borrow state mechanisms without automatically copying the car, map, or 3D engine.
