# Campaign QA matrix

| Area | Required test | Pass evidence |
|---|---|---|
| Stage progression | Complete required events in intended order | correct unlocks and no dead end |
| Optional events | Complete, skip, and fail each optional event | campaign remains coherent |
| City states | Trigger every transition and recovery path | routes/UI/story update correctly |
| Rivals | Defeat, rescue, betray, and ignore rivals | relationship state persists |
| Fire Key | Acquire clues/components in different orders | finale resolves correctly |
| Factions | Test all reputation threshold crossings | economy/access/AI changes |
| Save/load | Save during travel, event, aftermath, and decision | no lost flags or rewards |
| Failure | Lose each stage type | fail-forward state is fair |
| Accessibility | Complete stages with key options enabled | no inaccessible blocker |
| Replay | Re-run deterministic scenarios | outputs remain within tolerance |
| Performance | Full stage at maximum designed load | target budgets maintained |

## Narrative regression

Every bug involving a wrong line, missing consequence, inconsistent faction reaction, or impossible decision state receives a stable scenario ID and automated or scripted regression coverage.
