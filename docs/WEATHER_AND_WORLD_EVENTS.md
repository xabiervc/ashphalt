# Weather and world events

## Weather states

- Clear ash haze: baseline visibility reduction.
- Rain: lower grip, reflections, reduced braking.
- Fog: shorter visibility and more cautious AI.
- Ash storm: severe visibility loss, route hazards, engine stress.
- Sandstorm: grip loss, drifting debris, off-road advantage.
- Flood: route closure and water hazards.

## Transition rules

Weather transitions use named seeds and a deterministic schedule in tests. Production can use a campaign seed while preserving replay metadata.

## World events

Convoy ambush, checkpoint lockdown, bridge failure, workshop emergency, gang roadblock, evacuation, salvage opportunity, and temporary shortcut.

## Presentation

Every event needs anticipation, readable warning, gameplay effect, resolution, and aftermath. Avoid invisible route changes that feel unfair.
