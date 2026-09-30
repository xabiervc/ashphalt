# Pre-production requirements traceability

| Critical question | Specification | Evidence required | Status |
|---|---|---|---|
| What happens in first five minutes? | FIRST_FIVE_MINUTES | first-session test | documented |
| What is learned in first hour? | FIRST_HOUR_LEARNING_CURVE | learning assessment | documented |
| What decision differentiates the game? | PLAYER_FANTASY_AND_GENRE, CORE_GAMEPLAY_SPECIFICATION | playtest explanation | documented |
| What changes between runs? | REPLAYABILITY_AND_CONTINUATION | repeat-session comparison | documented |
| Why continue after failure? | REPLAYABILITY_AND_CONTINUATION | recovery/replay data | documented |
| How long is the game? | CAMPAIGN_CONTENT_BUDGET, REPLAYABILITY_AND_CONTINUATION | completion telemetry/playtest | documented |
| Are narrative states coherent? | CAMPAIGN_TIMELINE, NARRATIVE_STATE_MACHINE, CANON_RULES | state-transition tests | documented |
| Is accessibility testable? | ACCESSIBILITY_REQUIREMENTS | user tests and persistence tests | documented |
| Are platforms/performance defined? | PLATFORM_MATRIX, PERFORMANCE_AND_MEMORY_BUDGET | benchmark reports | documented |
| Are saves safe and migratable? | SAVE_MIGRATION_SPECIFICATION | migration/corruption tests | documented |
| Is telemetry respectful? | PRIVACY_AND_TELEMETRY | network/log audit | documented |
| Is production readiness objective? | VERTICAL_SLICE_READINESS_GATE, PRODUCTION_READINESS_GATE | signed gate evidence | documented |
