# Material 3 Expressive: use expression to emphasize the task

Last reviewed: 2026-09-23. Google's research and the Toolbars Overview/Guidelines and illustrations were read, including browser inspection; native applications were not exercised.

## Research basis

- [Google research](https://design.google/library/expressive-material-design-google-research): the email example jointly changes Send placement, size, and color. Counterexamples involving disorganized playlists and removed action labels show that expression cannot replace familiar semantics. Reported research speed improvements are not a promise for this project.
- [Toolbar overview](https://m3.material.io/components/toolbars/overview): at review time, the resource table marked Web as Unavailable. That neither prevents a custom Web implementation nor establishes that an official one exists. Recheck current platform availability when it matters.
- [Toolbar guidelines](https://m3.material.io/components/toolbars/guidelines): distinguish global docked and contextual floating tools; put overflow in a menu and consolidate groups in compact layouts. Do not combine collapsing and moving offscreen for the same scroll behavior. Desktop/Web adaptations have exceptions; one mobile position or radius rule is not universal.

## Web implementation recipe

1. Identify the current primary action and secondary tools. Establish priority jointly through shape, typography, color, and position; not every button or surface should demand equal emphasis.
2. Specify concrete state relationships. For browsing → editing, for example, tool options change with context, the mode remains clear, and selection/focus stay coherent after exit.
3. Size floating toolbars to necessary content. Before overflow, move secondary actions into a reachable menu. Larger windows may support vertical tools; narrow layouts prioritize unobstructed content and actions.
4. Describe selective adoption as expressive hierarchy inspired by the system. Claim full conformance only after checking relevant components, color roles, states, dimensions, and target platform. Mobile dp values are not automatically Web CSS-pixel compliance rules.
5. Shape transitions must not obstruct input. Reduced motion can use direct state changes or gentle feedback.

## Acceptance

With the same task and content, verify that the primary action is apparent, labels are complete, and the current mode is identifiable. Long labels and narrow layouts must not push tools out of bounds; collapsed actions remain accessible. Bright colors or Google fonts alone do not establish these outcomes.
