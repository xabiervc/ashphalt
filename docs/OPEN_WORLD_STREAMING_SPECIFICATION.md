# Open-world streaming specification

## Initial approach

Use Unreal World Partition or an equivalent cell-based setup appropriate to the selected engine version. The first prototype can use a small map, but must preserve the same ownership and persistence boundaries intended for larger cities.

## Cell responsibilities

Each cell may own roads, props, landmarks, traffic spawn volumes, pedestrian volumes, activity anchors, audio zones, and streaming metadata. Persistent state belongs to city/world services, not transient actors.

## Persistence

When a cell unloads, preserve city state, discovered shortcuts, event status, rival state, damage consequences, route closures, weather seed, and spawned activity cooldowns. Do not serialize every transient traffic vehicle unless required by a future design decision.

## Streaming tests

- Drive across every cell boundary at top speed.
- Repeat while weather and Authority pursuit are active.
- Trigger an activity, leave its cell, return, and verify state.
- Save/load near a boundary.
- Profile hitches and memory after repeated crossings.
