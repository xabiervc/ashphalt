# Phase 0 — Unreal project setup

## Goal

Create a clean Unreal Engine 5.7+ project suitable for Ashphalt's first playable slice.

## Project choices

- Project type: Games.
- Primary target: desktop development build.
- Scripting: C++ with Blueprint support.
- Starter content: optional; use only for temporary placeholders.
- Ray tracing and high-cost rendering features: disabled initially unless the hardware benchmark justifies them.
- Version control: Git with large-file handling configured before adding binary assets.

## Initial modules

- `AshphaltCore`: IDs, logging, simulation clock, seeded random streams, configuration.
- `AshphaltVehicles`: Chaos vehicle base, input, damage, repair, tuning.
- `AshphaltWorld`: district, routes, workshop, weather, events.
- `AshphaltAI`: traffic, rivals, Authority, emergency, pedestrians.
- `AshphaltNarrative`: factions, reputation, decisions, save data.
- `AshphaltQA`: debug commands, scenario spawning, metrics, replay validation.

## Initial content folders

```text
Content/Ashphalt/Maps
Content/Ashphalt/Vehicles
Content/Ashphalt/Damage
Content/Ashphalt/Tuning
Content/Ashphalt/AI
Content/Ashphalt/Factions
Content/Ashphalt/Events
Content/Ashphalt/Weather
Content/Ashphalt/UI
Content/Ashphalt/Audio
Content/Ashphalt/Debug
```

## Completion criteria

- Project opens without errors.
- Development build compiles.
- Modules load in the editor.
- Test map can be opened and played.
- Git ignores generated Unreal folders and tracks required source/config/content files.
- A baseline profiling capture is recorded.
