# Actions and rewards

## Action categories

| Category | Examples | Primary outputs |
|---|---|---|
| Driving skill | drift, jump, near miss, shortcut | score, time, reputation-neutral credits |
| Vehicle combat | ram, side-hit, disable, destroy | score, time, credits, heat |
| Emergency interaction | evade, assist, obstruct, destroy hostile unit | score, faction effects, route effects |
| Race objective | finish, hunt, protect, escape, deliver | credits, parts, unlocks |
| Faction action | accept, betray, protect, raid, expose | reputation, access, story flags |
| Preparation | repair, tune, salvage, inspect | vehicle state, costs, information |

## Faction standing changes

| Action | Authority | Underworld | Settlements | Circuit |
|---|---:|---:|---:|---:|
| Finish a sanctioned race | +2 | 0 | +1 | +5 |
| Destroy a hostile patrol | -3 | +1 | 0 | +2 |
| Escape a pursuit without collateral damage | +3 | 0 | +2 | +1 |
| Accept an illegal tuning job | -2 | +6 | -1 | +2 |
| Protect a settlement convoy | -1 | -2 | +8 | +1 |
| Betray a faction contract | -5 | -5 | -5 | -5 |
| Win an elite Circuit event | 0 | +1 | 0 | +10 |
| Sabotage an Authority checkpoint | -8 | +3 | -2 | +4 |
| Rescue an emergency crew | +4 | -1 | +5 | 0 |

All changes must include an event ID and visible reason.

## Reward composition

Every event preview shows expected credits, parts, reputation deltas, heat risk, vehicle wear, and unlock progress. Rewards are calculated from objective completion, optional objectives, event difficulty, and condition bonuses.

## Anti-exploit rules

- Targets have cooldowns for score and rewards.
- Repeated retries cannot duplicate unique unlocks.
- Score and credits use separate caps.
- Faction gains from the same action type diminish within one event.
- Save data records event completion and reward claims atomically.
