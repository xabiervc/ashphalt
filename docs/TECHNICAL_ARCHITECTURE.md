# Technical architecture

## Unreal layers

- Core module: IDs, clocks, seeds, logging, configuration, stable interfaces.
- Vehicle module: Chaos Vehicles integration, input, damage, repair, tuning.
- World module: districts, routes, workshops, hazards, weather.
- AI module: traffic, rivals, factions, Authority, emergency, pedestrians.
- Narrative module: decisions, reputation, contracts, endings.
- UI module: HUD, garage, workshop, event preview, faction status.
- QA module: debug commands, scenario spawning, metrics, replay validation.

## C++ and Blueprint boundary

C++ owns stable data structures, simulation services, save migration, physics-facing calculations, and automated tests. Blueprints own level composition, presentation, simple orchestration, and designer iteration. Data Assets own content values.

## Subsystems

Use GameInstance subsystems for campaign/save services, World subsystems for weather/event state, and local components for vehicle damage, tuning, reputation observation, and AI state.

## Naming

Use prefixes by asset type, stable IDs separate from display names, and folders by domain. Never use display text as a save identifier.

## Profiling

Use Unreal Insights, stat commands, and repeatable benchmark maps from the first vehicle build. Track frame time, physics time, actor count, AI time, draw calls, memory, and streaming.
