# QA and validation

## Test layers

- Unit tests: formulas, tiers, costs, event rules, save migration.
- Scenario tests: vehicle collision, repair, pursuit, weather, route changes, faction reactions.
- Integration tests: event → reward → reputation → consequence → save/load.
- Replay tests: identical seed/input stream within tolerances.
- Performance tests: fixed benchmark map with traffic and AI load.
- Playtests: handling feel, readability, pacing, frustration, and economic recovery.

## Acceptance principles

A feature is not complete because it compiles. It must be observable, testable, documented, profiled, and playable in its intended context.

## Regression policy

Every approved phase adds a test scenario. Breaking an existing acceptance test blocks the phase until fixed or explicitly re-approved.

## Required metrics

Frame time, physics time, AI time, active actors, collision events per second, memory, loading time, save/load time, replay divergence, and crash rate.
