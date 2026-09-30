# Technical quality budgets

## Initial targets

These are targets to validate on selected hardware, not guarantees before profiling:

- Stable 60 FPS target on the primary development target.
- Frame-time spikes investigated rather than hidden.
- Physics, AI, rendering, and streaming budgets recorded separately.
- No blocking hitch during normal district driving after assets are cached.
- Save/load completes with visible feedback and no data loss.
- Crash and ensure reports have reproducible scenario IDs.
- Performance benchmark map includes traffic, weather, destruction debris, and Authority escalation.

## Stability requirements

- No known data-loss save defect.
- No progression blocker in the main route.
- Safe recovery after vehicle reset, failed event, interrupted save, and invalid asset data.
- Automated validation for required Data Asset fields and ranges.

## Technical excellence

Use Unreal Insights, automation tests, scenario commands, memory reports, and build validation from the first playable slice. Optimize measured bottlenecks, not assumptions.
