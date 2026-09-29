# Ashphalt test scaffolding

The implementation repository is not yet a compiled Unreal project. This directory records the intended validation surface until the first project is created.

## Planned suites

- Core: IDs, seeds, clocks, configuration.
- Vehicles: handling configuration, damage, repair, tuning.
- Events: objectives, timers, rewards, failure, aftermath.
- Factions: standing changes, tiers, consequences, save/load.
- Weather: state transitions, modifiers, route effects.
- Replay: seed/input reproduction and tolerance checks.
- Performance: benchmark map, actor count, physics time, AI time, memory.

Each suite must become executable or manually reproducible when its corresponding Unreal module is implemented.