# Scoring and combos

## Design goal

Scoring must make destruction and reckless driving central without requiring the player to harm one specific group. The game supports fictional, stylized civilians and emergency scenarios; presentation and rating boundaries must be reviewed before release.

## Base score table

| Action | Base score | Time reward | Credits | Notes |
|---|---:|---:|---:|---|
| Near miss | 50 | 0.1 s | 0 | Once per target every 8 s |
| Dangerous drift | 75 | 0.1 s | 0 | Requires speed and angle thresholds |
| Traffic vehicle hit | 100 | 0.2 s | 10 | Repeated same-target penalty |
| Traffic vehicle disabled | 350 | 0.5 s | 35 | Component damage required |
| Rival hit | 250 | 0.3 s | 20 | Scales with impact severity |
| Rival disabled | 1,000 | 2.0 s | 125 | Objective progress if applicable |
| Rival destroyed | 1,500 | 3.0 s | 175 | Once per rival per event |
| Authority patrol disabled | 1,500 | 2.0 s | 150 | Raises Authority hostility |
| Authority interceptor destroyed | 3,500 | 4.0 s | 400 | High-risk target |
| Authority heavy unit destroyed | 7,500 | 7.0 s | 900 | Requires coordinated damage |
| Elite pursuit unit defeated | 15,000 | 12.0 s | 2,000 | Boss-level event target |
| Stylized pedestrian hit | 125 | 0.25 s | 5 | Optional mode/rating toggle; never mandatory in story missions |
| Pedestrian near miss/escape | 150 | 0.3 s | 0 | Rewards danger without requiring contact |
| Route shortcut discovered | 500 | 0 | 75 | Once per event route |
| Emergency response avoided | 300 | 0.5 s | 25 | Rewards evasion |

## Combo rules

- Combo starts at 2 qualifying actions within 4 seconds.
- Each qualifying action increases the multiplier by 0.25.
- Normal cap: 5.0x.
- High-risk target cap: 7.5x, unlocked by event modifiers.
- Combo decays after 4 seconds without a qualifying action.
- The same target cannot advance a combo more than once every 2 seconds.
- Repeating one action category applies a 30% diminishing return after the third repetition.
- Destruction of an Authority unit increases public-damage heat even when it produces score.

## Multipliers

Final score = base action score × combo multiplier × event multiplier × difficulty modifier.

Time and credits use separate caps so score farming cannot create unlimited resources. A race has a maximum destruction-credit budget unless the event explicitly enables unlimited mayhem.

## Negative scoring

- Civilian convoy sabotage: -1,000 and Settlement reputation loss.
- Abandoning a protection contract: -750 and contract faction loss.
- Destroying a protected emergency vehicle: -2,500 unless the event marks it hostile.
- Repeatedly farming the same respawn point: score resets and no resource reward.

## Accessibility and content variants

The design must support an optional non-contact pedestrian mode. That mode replaces contact score with near-miss, stunt, and vehicle-destruction objectives without changing the core race progression.
