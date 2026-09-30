# Recoverable error specification

## Error classes

- Missing/invalid asset.
- Corrupt save.
- Failed stream/cell load.
- AI navigation deadlock.
- Physics vehicle invalid state.
- Audio/VFX budget overflow.
- Localization missing key.
- Replay divergence.

## Response

Log stable error ID, preserve player state, show a readable fallback, offer retry/reset/restore where safe, and collect opt-in diagnostics only. Never trap the player behind an unrecoverable objective or silently erase progress.

## Acceptance

Each error class has an intentional test injection, recovery action, user-facing message, and regression scenario.
