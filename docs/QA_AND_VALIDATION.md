# QA and validation

## Test layers

- Unit: formulas, tiers, costs, event rules, save migration.
- Scenario: vehicle collision, repair, pursuit, weather, route changes, faction reactions.
- Integration: event → reward → reputation → consequence → save/load.
- Replay: identical seed/input stream within documented tolerances.
- Performance: benchmark map with traffic, weather, destruction, and Authority escalation.
- Accessibility: every option enabled, persisted, and behaviorally verified.
- Playtest: handling, readability, pacing, narrative causality, frustration, and voluntary replay.

## Quality gate evidence

A feature is not complete because it compiles. It must be observable, testable, documented, profiled, playtested, and reviewed against the quality gates in `QUALITY_GATES.md`.

## Regression policy

Every approved phase adds a test scenario. Breaking an acceptance test blocks the phase unless the change is explicitly re-approved with updated documentation and traceability.
