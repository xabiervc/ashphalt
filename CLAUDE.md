# Ashphalt — Claude Code project instructions

## Mission

Build Ashphalt as a single-player-first post-apocalyptic arcade racing and vehicular-combat game in Unreal Engine 5.7+.

## Non-negotiables

- Implement only the requested phase; do not invent unrelated features.
- Preserve the design documents and update them when an approved decision changes.
- Use fictional cities, manufacturers, models, logos, characters, and factions.
- Keep the current scope single-player. Multiplayer is deferred.
- Prefer C++ for stable core systems and performance-sensitive code; use Blueprints for iteration and content authoring.
- Use Data Assets/Data Tables for content and tuning.
- Use fixed-step gameplay logic, explicit update order, and named seeded random streams.
- Include a minimal test map, acceptance criteria, debug instrumentation, and a performance check in each implementation phase.
- Never claim cross-platform bit-exact Chaos determinism without evidence; use tolerances and document limitations.
- Update `PROGRESS.md` after approved implementation work.

## Required response before changes

Before editing files, provide exactly:

1. A five-line implementation plan.
2. Files to create or modify.
3. Acceptance criteria.
4. Risks or assumptions.
5. A request for confirmation.

Do not make code changes until confirmation is given.

## Documentation authority

`docs/GDD.md` is the product-level source of truth. The specialist documents refine it. If documents conflict, stop and report the conflict instead of silently choosing.
