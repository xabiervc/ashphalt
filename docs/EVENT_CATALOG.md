# Event catalog

## Event ID convention

`EV_<DISTRICT>_<TYPE>_<NUMBER>`.

## Initial events

| ID | District | Type | Objective | Main risk | Reward profile |
|---|---|---|---|---|---|
| EV_CROWN_CIRCUIT_01 | The Crown | circuit | finish first | checkpoints and tunnels | medium credits, Circuit rep |
| EV_CROWN_WRECK_01 | The Crown | wreck run | 4,000 destruction score | Authority heat | parts and credits |
| EV_WORKS_HUNT_01 | The Works | rival hunt | disable named rival | containers and heavy traffic | vehicle unlock progress |
| EV_VERGE_CONVOY_01 | The Verge | protection | keep 2 of 3 vehicles alive | ambushes | Settlement rep and credits |
| EV_SALT_ESCAPE_01 | The Salt Run | escape | break pursuit | sandstorm | Circuit rep and shortcut |
| EV_LOWLANDS_DELIVERY_01 | The Lowlands | delivery | deliver part under 40% damage | flood route changes | rare part |
| EV_WORKS_AUTHORITY_01 | The Works | faction contract | defeat heavy unit | high repair cost | Underworld rep |
| EV_CROWN_SHOWDOWN_01 | The Crown | championship | win or destroy champion | elite pursuit | major story flag |

## Required event data

Each event must define participants, route, objective, secondary objectives, timer, weather seed, heat policy, allowed vehicle classes, damage rules, reward budget, reputation changes, unlocks, failure state, aftermath, and replay ID.

## Completion requirement

Before vertical slice, each event must have a blockout route, objective logic, success/failure tests, reward tests, save/load behavior, and a short playtest report.
