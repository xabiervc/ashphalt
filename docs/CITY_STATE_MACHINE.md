# City state machine

## States

`STABLE → DISTURBED → VIOLENT → BURNING → COLLAPSING → ASH_STATE`.

States may also recover partially through Settlement actions, emergency assistance, or faction agreements. Recovery cannot erase all consequences; it changes future routes and relationships.

## Transition inputs

- Destruction score.
- Authority heat.
- Emergency assets destroyed or protected.
- Convoy success/failure.
- Major story decisions.
- Time spent in the city.
- Weather event severity.
- Faction control changes.

## State effects

| State | Traffic | Authority | Routes | Economy | Narrative |
|---|---|---|---|---|---|
| Stable | normal | routine | all open | normal | hopeful |
| Disturbed | evasive | patrols | minor detours | slight scarcity | concern |
| Violent | sparse/aggressive | interceptors | blocks/shortcuts | repair premium | fear |
| Burning | emergency-heavy | heavy units | fire/flood closures | parts shortage | crisis |
| Collapsing | unstable | command response | major changes | severe scarcity | evacuation |
| Ash State | minimal | special response | permanent damage | restricted | aftermath |

## Persistence

Store state, transition cause, timestamp/event ID, affected routes, faction ownership, emergency status, discovered shortcuts, and recovery flags in SaveGame data.
