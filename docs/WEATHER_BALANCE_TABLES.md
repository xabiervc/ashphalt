# Weather balance tables

| State | Grip multiplier | Visibility | Traffic | AI aggression | Route effect |
|---|---:|---:|---|---|---|
| Clear haze | 1.00 | 100% | normal | normal | none |
| Rain | 0.86 | 82% | cautious | -5% | puddles, longer braking |
| Fog | 0.94 | 55% | cautious | -10% | hidden shortcut signage |
| Ash storm | 0.78 | 35% | unstable | +5% | debris route may close |
| Sandstorm | 0.72 | 25% | sparse | +0% | off-road route advantage |
| Flood | 0.80 | 75% | rerouted | +0% | low route closed |

Weather changes must be telegraphed and use a minimum transition time of 20 seconds in normal events. Story events may override this. Vehicle upgrades can reduce but not eliminate penalties.

Every state defines audio, particles, post-process, AI modifiers, physics modifiers, route changes, warning UI, and seed policy.
