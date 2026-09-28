# Ashphalt

A post-apocalyptic vehicular combat and racing game built with Unreal Engine 5.7+.

> **Status:** Pre-production / Phase 0
>
> This repository currently contains the Game Design Document and the phased prompts used to develop the project with Claude Code and Claude Opus 5.5.

## Vision

Ashphalt is a single-player-first arcade racing and vehicular-combat game inspired by the spirit of classic destruction racers, while establishing its own setting, mechanics, factions, vehicles, and story.

The player drives through fictional post-apocalyptic districts, where reckless driving, vehicle destruction, faction choices, weather, tuning, and story decisions shape the campaign and its consequences.

The project deliberately uses fictional cities, vehicle manufacturers, and models. Real-world cities and car brands are not required for the core experience.

## Core pillars

- Weighty but responsive arcade vehicle handling.
- Component-based vehicle damage that rewards reckless driving.
- Fast, visual repair-shop gameplay.
- Multiple fictional vehicle archetypes with tuning and asymmetric strengths.
- Post-apocalyptic districts designed for racing, destruction, shortcuts, and ambushes.
- Dynamic weather affecting grip, visibility, and route availability.
- Faction reputation with visible consequences for economy, access, combat, and story.
- Deterministic systems wherever practical: fixed simulation order, seeded randomness, and input-based replays.
- Single-player first. Local and online multiplayer are explicitly deferred until the core game is stable and fun.

## Factions

- **The Authority:** remnants of law enforcement and centralized order.
- **The Underworld:** scavenger gangs and black-market mechanics.
- **The Settlements:** civilian communities trying to rebuild.
- **The Circuit:** rival racer crews treating the wasteland as their arena.

## Technology

- Unreal Engine 5.7+.
- Chaos Vehicles for vehicle physics.
- Blueprints and C++ where appropriate.
- Behavior Trees, NavMesh, and EQS for AI.
- Data Assets/Data Tables for vehicles, upgrades, factions, consequences, weather, and story decisions.
- Git/GitHub for version control.

## Development phases

1. Base fictional district and race circuit.
2. Player vehicle and Chaos Vehicles handling.
3. Component-based damage.
4. Fictional vehicle roster.
5. Tuning/customization.
6. Repair-shop loop.
7. Factions and reputation.
8. Reputation consequences.
9. Traffic and pedestrians.
10. Authority and emergency AI.
11. Dynamic weather.
12. Story decisions and multiple endings.
13. Input-based replay validation.

Detailed implementation prompts are in [`docs/CLAUDE_OPUS_5_5_PROMPTS.md`](docs/CLAUDE_OPUS_5_5_PROMPTS.md). The full design is in [`docs/GDD.md`](docs/GDD.md).

## Current scope

The first development stage is single-player only. Multiplayer is intentionally excluded from the current implementation prompts and will be treated as a separate future project once the single-player foundations have been tested.

## Legal and licensing notes

This is a working title. Before any public commercial release, perform a professional trademark review of the name "Ashphalt" and all visual assets.

Vehicle designs should use fictional manufacturers and models. Do not use real logos, brand names, or 1:1 copies of distinctive vehicle designs without appropriate permission.

Unreal Engine licensing should be checked against Epic's current terms before release; commercial terms can change.

## Repository structure

```text
.
├── README.md
└── docs/
    ├── GDD.md
    └── CLAUDE_OPUS_5_5_PROMPTS.md
```

## Working method

Implement one phase at a time. For every phase:

1. Ask Claude Code for a five-line implementation plan.
2. Review the plan before allowing code changes.
3. Require a minimal test scene and acceptance criteria.
4. Run the project and verify the result manually.
5. Commit the phase separately.
6. Update `PROGRESS.md` with decisions, known issues, and next steps.

## License

No project license has been selected yet. Do not reuse or redistribute project assets until a license is explicitly added.
