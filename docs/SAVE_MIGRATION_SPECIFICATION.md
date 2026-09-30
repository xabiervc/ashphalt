# Save and migration specification

## Save layers

- Profile: settings, accessibility, input, audio, display.
- Campaign: stage, city states, faction standing, decisions, relationships, unlocks.
- Vehicle: condition, tuning, inventory, ownership.
- Replay metadata: build ID, data revision, seeds, inputs, checkpoints.

## Reliability

Use atomic writes, rotating backups, checksum/version header, corruption detection, recovery slot, explicit save status, and no destructive migration without confirmation.

## Migration

Every schema change increments a version. Provide migration code or a documented reset path. Test upgrades across at least the previous two versions in development.

## Failure handling

If a save is invalid, preserve the original, offer backup restore, explain the problem, and allow a safe new profile without crashing or silently losing progress.
