# Ashphalt — Claude Opus 5.5 phase prompts

These prompts are intended for Claude Code with Claude Opus 5.5. Use one phase at a time. Do not ask the model to build the entire game in one response.

## Common operating rules

- Use Unreal Engine 5.7+.
- Keep the current scope single-player only. Do not implement online or local multiplayer in these phases.
- Before changing files, provide a five-line implementation plan and wait for confirmation.
- Work only on the requested phase.
- Use C++ for stable core systems and performance-critical logic; use Blueprints/Data Assets/Data Tables where they improve iteration and content authoring.
- Include a minimal test map or scenario, acceptance criteria, debug instrumentation, and a performance sanity check.
- Preserve existing architecture and avoid unrelated refactors.
- Update `PROGRESS.md` after the phase is approved.
- Prefer deterministic behavior: fixed simulation/update order, explicit seeded random streams, no unseeded gameplay randomness, and replay-friendly inputs.
- Do not use real car brands, logos, or 1:1 copies of distinctive vehicle designs.

---

## Phase 1 — Fictional district

We are building Ashphalt, a single-player-first post-apocalyptic arcade racing and vehicular-combat game in Unreal Engine 5.7+.

Build one compact fictional urban district as a test level. It should contain a closed-loop race circuit through streets, a few intersections, a shortcut, a workshop location, and safe areas for future AI tests. Add NavMeshBoundsVolume covering relevant drivable/walkable areas. Apply a basic post-apocalyptic art pass: cracked roads, damaged buildings, debris, broken lights, abandoned vehicles, vegetation, and smoke/ash placeholders.

Do not implement vehicles, AI, factions, weather, story, or networking yet. Add a simple spectator/flythrough test and document the level's acceptance criteria. First provide a five-line plan and wait for my confirmation.

## Phase 2 — Player vehicle

Implement the player-controlled vehicle using Chaos Vehicles and `ChaosWheeledVehicleMovementComponent`. Use a fictional vehicle with placeholder meshes if necessary. Add throttle, brake, steering, handbrake, reset/recovery, and a chase camera.

Tune it to feel weighty but responsive: not floaty, not excessively grippy, and not frustrating after minor impacts. Test suspension, friction, braking, steering, and stability during frame-time spikes. Add a test route in the Phase 1 district and show key tuning parameters in a debug HUD.

Do not add AI, damage, tuning, story, weather, or networking. First provide a five-line plan and wait for confirmation.

## Phase 3 — Component damage

Implement a component-based damage system for chassis, engine, wheels/suspension, bodywork, and optional ramming attachments. Convert collision impulse and contact data into damage using data-driven thresholds.

Damage must degrade functions progressively: engine damage affects acceleration/top speed, wheel damage affects steering/stability, chassis damage affects survivability, and bodywork damage affects protection. Add readable visual/audio feedback, detachable placeholder parts, smoke, sparks, and a debug damage panel.

Tune the system to reward reckless driving. A single collision should not make the car useless, but repeated abuse must matter. Create a controlled ramming test scenario. First provide a five-line plan and wait for confirmation.

## Phase 4 — Vehicle roster

Create 4-5 fictional vehicle archetypes extending the common vehicle base: heavy muscle-style brawler, agile hot-hatch-style car, off-road pickup-style vehicle, fast fragile supercar-style vehicle, and utility van-style vehicle.

Do not use real brands, logos, names, or 1:1 body copies. Use fictional manufacturers and blend cues from multiple archetypes. Store mass, acceleration, speed, braking, steering, grip, armor, component durability, repair cost, and tuning compatibility in Data Assets/Data Tables.

Create a test garage or debug selector to spawn and drive each vehicle. First provide a five-line plan and wait for confirmation.

## Phase 5 — Tuning

Implement data-driven tuning for engine output, armor, ramming attachments, tires/grip, brakes, suspension, and weight distribution. Tuning configurations must apply to any player or AI vehicle through the same API.

Do not hardcode upgrades per vehicle. Support compatibility rules, costs, installed-part state, stat previews, and save/load-ready data. Add a minimal test UI or console commands and demonstrate that changes affect Chaos Vehicle behavior and damage response.

Do not implement the full garage UI or AI behavior yet. First provide a five-line plan and wait for confirmation.

## Phase 6 — Repair shop

Implement a fast, visual repair-shop system that restores or replaces damaged vehicle components. It must work for any vehicle instance, not only the player. Add a workshop trigger in the Phase 1 district.

The process should take seconds rather than becoming a menu-heavy minigame. Show parts reattaching, repairs progressing, cost, and the final condition. Preserve tuning and allow future faction-based price modifiers. Include damage-before/after tests and AI-callable repair functions, even though AI vehicles are not yet active.

First provide a five-line plan and wait for confirmation.

## Phase 7 — Factions and reputation

Implement four factions: The Authority, The Underworld, The Settlements, and The Circuit. Each has a standing value from -100 to +100 with Hostile, Unfriendly, Neutral, Friendly, and Allied tiers.

Create a SaveGame-compatible reputation component and data-driven standing changes. Add debug commands/UI to modify values and inspect tiers. Add event identifiers so future actions can apply reputation changes without hardcoding narrative logic into vehicles.

Do not implement consequences yet. First provide a five-line plan and wait for confirmation.

## Phase 8 — Consequences

Connect faction reputation to three concrete channels. Economy: workshop prices, repair costs, salvage, and tuning-part availability. Access: lock or unlock a route, district, race, workshop, or contract. Disposition: provide data-driven reaction rules for Authority, Underworld, and Circuit agents.

Make every consequence legible to the player. Show why something is locked, discounted, unavailable, hostile, or helpful. Add debug scenarios for each reputation tier and test save/load persistence.

Do not implement full AI behavior yet; expose clean query functions and rule data for later phases. First provide a five-line plan and wait for confirmation.

## Phase 9 — Traffic and pedestrians

Implement background traffic and pedestrians in the Phase 1 district. Traffic vehicles should follow lanes, stop for obstacles/collisions, recover from deadlocks, and react to the player's presence. Pedestrians should use stylized non-photorealistic visuals and flee from dangerous high-speed approaches.

Use NavMesh and Behavior Trees for individual agents initially. Evaluate Mass Entity only if measured agent counts require it. Use explicit seeded random streams for spawns and behavior variation. Add debug spawning, AI state display, and performance counters.

First provide a five-line plan and wait for confirmation.

## Phase 10 — Authority and emergency AI

Implement Authority pursuit AI with Behavior Trees, Blackboard, NavMesh, and EQS where helpful. Trigger pursuit through a public-damage/incident system and query Phase 8 reputation disposition rules to determine ignore, warn, pursue, or aggressive behavior.

Implement fire and ambulance equivalents responding to accident events generated by the damage system. They should navigate to incidents, perform a simple response, and leave or remain according to a data-driven rule. Add controlled tests for pursuit, blocked roads, accidents, and reputation tiers.

Use explicit seeded randomness. First provide a five-line plan and wait for confirmation.

## Phase 11 — Dynamic weather

Implement rain, fog, ash storm, and sandstorm states. Weather must affect Chaos Vehicle grip, visibility/post-process, AI decisions, audio, lighting, and optionally route availability.

Use an explicit seed and deterministic transition rules. Add debug commands to force each state, advance transitions, and reset the seed. Create one route event such as flooding or ash debris blocking a street, with clear player feedback and a reversible state for testing.

First provide a five-line plan and wait for confirmation.

## Phase 12 — Story decisions and endings

Implement 2-3 major, clearly signposted story decisions. Each decision should record an identifier, selected option, timestamp/mission context, reputation changes, unlocked/locked content, and follow-up consequences.

Implement a data-driven ending evaluator based on the accumulated reputation pattern across all four factions and recorded decisions. Start with placeholder text and debug commands. Avoid dozens of micro-branches; focus on meaningful choices with persistent effects.

Create automated tests for every decision option, save/load, and ending evaluation. First provide a five-line plan and wait for confirmation.

## Phase 13 — Input-based replay validation

Audit all previous phases for frame-rate-dependent gameplay logic, hidden global randomness, unstable update order, and unseeded random streams. Fix issues that prevent reproducible testing.

Implement an input-based replay system that records initial world seed, relevant configuration, tick rate, and player inputs rather than full state. Replay a short controlled session and compare vehicle transform, component damage, race events, reputation changes, and weather transitions within explicit tolerances.

Document what is and is not deterministic. Do not claim bit-exact cross-platform Chaos physics if it cannot be guaranteed. First provide a five-line plan and wait for confirmation.

---

## Future work — not part of this prompt set

Do not implement local or online multiplayer yet. Once the single-player game is stable and fun, create a separate multiplayer design covering authority model, replication, prediction, interpolation, lobbies, dedicated servers, anti-cheat, and testing.
