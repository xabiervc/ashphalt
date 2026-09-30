# Narrative state machine

## States

`UNENTERED → INVITED → COMPETING → ALIGNED_OR_INDEPENDENT → FIRE_KEY_REVEALED → GATE_REACHED → OUTCOME_LOCKED`.

## State inputs

Stage completion, rival relationship, faction standing, city state, Fire Key clues, major decisions, rescue/sabotage history, and Chaos Rating profile.

## Rules

Narrative state changes are event-driven, persisted in SaveGame, visible through dialogue/world/UI, and reversible only through an explicitly documented branch or new campaign. No hidden global morality score may override recorded state.

## Tests

Each transition requires success, failure, save/load, replay, missing-optional-flag, and accessibility tests.
