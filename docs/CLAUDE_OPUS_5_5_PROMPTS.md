# Ashphalt — Claude Opus 5.5 implementation prompts

Use one block at a time. Before modifying files, provide a five-line plan, files, acceptance criteria, risks, and wait for confirmation. Work single-player only. Update `PROGRESS.md` after approval.

## Block 0 — Repository audit

Read the documentation and inspect the Unreal project. Report conflicts, missing decisions, build risks, and the smallest viable implementation slice. Do not write code until approved.

## Block 1 — Project foundation

Create the Unreal 5.7+ project/module structure, domain folders, logging categories, stable IDs, configuration, test map conventions, and initial automation test target. Do not implement gameplay yet.

## Block 2 — First district

Build the fictional district test map with closed-loop track, shortcut, workshop area, AI test areas, NavMesh, placeholder post-apocalyptic dressing, and a repeatable benchmark configuration.

## Block 3 — Vehicle foundation

Implement the base Chaos vehicle, input, camera, reset, handling data, debug HUD, and controlled handling test. Profile physics and document tuning assumptions.

## Block 4 — Damage and repair

Implement component damage, collision impulse conversion, functional degradation, visual feedback, repair interface, workshop trigger, and automated collision/repair scenarios.

## Block 5 — Vehicle content

Create data-driven fictional archetypes, common vehicle interfaces, tuning slots, upgrades, compatibility, costs, and a debug garage. Verify AI/player data parity.

## Block 6 — Event framework

Implement event definitions, objectives, checkpoints, destruction scoring, timers, failure/recovery, rewards, aftermath state, and one complete race event.

## Block 7 — Rival and traffic AI

Implement traffic lanes, rival race states, attacks, recovery, repairs, shortcuts, deadlock recovery, debug spawning, and performance scenarios.

## Block 8 — Factions and reputation

Implement faction data, standing changes, tier thresholds, reason codes, save/load, debug commands, and deterministic event application.

## Block 9 — Consequences and economy

Wire reputation to workshop prices, parts, access, event availability, patrol disposition, rival behavior, and visible UI explanations. Add economic profile tests.

## Block 10 — Authority and emergency systems

Implement public-damage incidents, Authority state machine/Behavior Tree, pursuit, blocking, backup, fire response, ambulance response, and reputation-aware behavior.

## Block 11 — Weather and world events

Implement seeded weather, grip/visibility modifiers, route changes, event anticipation, resolution, aftermath, forced debug states, and replay metadata.

## Block 12 — Narrative and endings

Implement decision data, mega-decision UI flow, persistent consequences, mission context, ending evaluator, placeholder narrative content, save/load, and decision tests.

## Block 13 — Replay and determinism audit

Audit update order and random streams. Implement input/seed recording, checkpoints, tolerance comparison, divergence diagnostics, and regression replay fixtures.

## Block 14 — UI, accessibility, and polish

Implement HUD, damage readability, objectives, faction/reputation explanation, garage, workshop, event preview, accessibility options, pause/save flow, and error states.

## Block 15 — Vertical slice integration

Integrate one district, representative vehicles, event chain, rival, traffic, weather, workshop, faction choice, consequence, save/load, audio placeholders, and profiling. Run all acceptance tests and produce a gap report.

## Block 16 — QA hardening

Run unit, scenario, integration, performance, replay, save migration, and failure-path tests. Fix defects by priority and update traceability, changelog, and release status.

## Block 17 — Production handoff

Produce an implementation status report, known-risk register, content backlog, asset list, build instructions, test instructions, and next milestone recommendation. Do not begin multiplayer.
