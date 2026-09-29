# NPC catalog

## Traffic

| Type | Durability | Speed profile | Reaction |
|---|---:|---|---|
| Civilian compact | 100 | low/medium | brake, swerve, flee |
| Civilian utility | 180 | low | block, stop, recover |
| Delivery hauler | 350 | low | wide turns, valuable target |
| Faction transport | 500 | medium | convoy behavior |
| Rival vehicle | data-driven | event-specific | race/attack/repair |

## Pedestrians

Use stylized, non-photorealistic representations. Types include commuter, scavenger, settlement worker, protester, racer fan, mechanic, and emergency worker. Each has spawn zone, movement speed, flee radius, panic duration, safe zone, and event tags.

## Crowd rules

Pedestrians must have safe spawn/despawn volumes, density caps, avoidance behavior, and a non-contact variant. They should not respawn immediately in front of a player to farm score.

## Character roles

- Player driver.
- Workshop mechanic.
- Authority commander.
- Underworld broker.
- Settlement coordinator.
- Circuit champion.
- Rival drivers.
- Emergency coordinator.

Each authored character needs goals, faction, vehicle, voice/text style, relationship flags, introduction event, conflict event, and exit state.
