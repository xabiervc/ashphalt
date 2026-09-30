# Open risks and ownership

| Risk | Owner role | Signal | Mitigation | Review gate | Status |
|---|---|---|---|---|---|
| Vehicle feel is not satisfying | Design/engineering | low replay or poor control results | tune control model; reduce scope if needed | Track A | open |
| Scope exceeds production capacity | Producer/design | tranche misses budget or schedule | apply cut rules; prioritize core loop | every gate | open |
| Camera/road readability fails at speed | Design/UX | wrong turns, late corrections | adjust camera, landmarks, route complexity | Track A/B | open |
| Performance budget is unrealistic | Engineering | frame-time or memory breach | profile early; reduce density/streaming scope | Track A/B | open |
| Accessibility options are ineffective | UX/QA | critical barrier in testing | revise controls, UI, audio redundancy | accessibility gate | open |
| Narrative consequences are not perceived | Narrative/design | low consequence recall | improve feedback and state presentation | Crown slice | open |
| Pipeline cannot repeat | Production/engineering | second event needs new architecture | simplify contracts and tooling | repeatability gate | open |

Open risks are owned hypotheses, not hidden blockers. Their status changes only through evidence.
