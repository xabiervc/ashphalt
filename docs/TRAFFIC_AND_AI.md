# Traffic and AI

## Agent types

- Civilian traffic.
- Rival racers.
- Authority patrols.
- Underworld ambushers.
- Settlement escorts.
- Emergency responders.
- Pedestrians.

## AI architecture

Use Behavior Trees, Blackboard, NavMesh, and EQS for individual reasoning. Use data-driven state machines for traffic. Evaluate Mass Entity only after profiling proves that ordinary actors cannot meet the target.

## Rival states

Race, overtake, defend, attack, recover, seek repair, use shortcut, flee, exploit weather, and react to faction disposition.

## Traffic states

Follow lane, obey signal, avoid obstacle, stop after collision, recover from deadlock, yield to emergency unit, and flee/avoid major incidents.

## Authority states

Observe, warn, pursue, block route, request backup, recover, and disengage. State selection depends on public damage, faction reputation, event type, and available units.

## Test scenarios

Every agent type needs a deterministic spawn scenario, blocked-road scenario, collision scenario, weather scenario, and reputation scenario.
