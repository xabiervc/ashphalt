# Rival driver specification

## Rival data

Every rival has vehicle definition, tuning profile, driving archetype, risk tolerance, target preference, faction standing, repair behavior, shortcut knowledge, heat tolerance, relationship state, and event availability.

## Driving archetypes

- **The Racer:** prioritizes line, speed, and clean overtakes.
- **The Wrecker:** attacks the leader and accepts damage.
- **The Showman:** seeks score, crowds, stunts, and visible chaos.
- **The Survivor:** avoids unnecessary conflict and protects condition.
- **The Hunter:** targets the player or a named rival.
- **The Opportunist:** changes target based on current leader and city state.

## Rival evolution

A rival remembers major defeats, rescues, betrayals, and player behavior. These facts alter dialogue, tuning, event tactics, ambush probability, and alliance availability.

## Acceptance tests

- Rival can finish an event without scripting assistance.
- Rival can recover from collision and choose repair.
- Rival can use at least one shortcut.
- Rival behavior changes under two faction standings.
- Rival relationship state persists after save/load.
