# Traffic density and performance

## Prototype density targets

- 6-10 civilian traffic vehicles active near the player.
- 12-20 traffic vehicles represented through pooled or low-cost simulation farther away.
- 4-8 pedestrians near the player, with capped background representation.
- 1 rival outside the event when relevant.
- 0-3 Authority units depending on heat.
- 0-2 emergency units during an event.

## Vertical-slice target

- 12-18 nearby traffic vehicles.
- 24-40 background traffic representations.
- 8-16 nearby pedestrians where enabled.
- 4-8 Authority/emergency units at peak escalation.
- 2-4 rivals in free roam or event context.

## Budgets

Record frame, physics, AI, streaming, draw-call, memory, and collision-event metrics. No density increase is approved without a benchmark capture on target hardware.

## Optimization rules

Use pooling, distance-based behavior tiers, HLOD/LOD, deterministic spawn volumes, and capped incident propagation. Do not optimize away readable reactions near the player.
