# Requirement obligation matrix

| Obligation | Normative source | State/data | Scene/asset | Test | Gate | Scope |
|---|---|---|---|---|---|---|
| Responsive weighty driving | DRIVING_CONTROL_MODEL | vehicle input/handling | Track A vehicle | control metrics/blind test | Q1 | mandatory |
| Readable speed and threats | CAMERA_SPEED_AND_READABILITY | camera/HUD state | metric map/Crown | failure explanation | Q1/Q2 | mandatory |
| Meaningful collisions | COLLISION_AND_DAMAGE_FEEL | component damage | wall/rival | impulse/damage test | Q2 | mandatory |
| Open exploration | OPEN_CITY_DESIGN | city/cell state | Crown blockout | traversal/streaming | Q2/Q3 | mandatory |
| Route choice | RACE_FLOW_DIAGRAMS | route ID | official/shortcut | route decision test | Q2 | mandatory |
| Rival memory | RIVAL_DRIVER_SPECIFICATION | CharacterState | rival placeholder | save/reaction test | Q2/Q3 | mandatory |
| Authority escalation | POLICE_AND_EMERGENCY_CATALOG | heat tier | interceptor | pursuit test | Q2 | mandatory |
| Repair/tuning decision | PROGRESSION_DECISION_DESIGN | vehicle build | workshop | upgrade choice test | Q2 | mandatory |
| Faction consequence | NARRATIVE_TRACEABILITY_MATRIX | reputation/flags | aftermath/UI | decision persistence | Q2/Q3 | mandatory |
| City-state persistence | CITY_STATE_MACHINE | CityState | Crown return | save/load/return | Q3 | mandatory |
| Accessibility baseline | ACCESSIBILITY_REQUIREMENTS | profile settings | HUD/menus | option persistence/user test | Q2/Q3 | mandatory |
| Audio/VFX readability | AUDIO_PREPRODUCTION_SPECIFICATION | cue/effect IDs | placeholders | reduced-channel tests | Q3 | objective |
| Replay/determinism | DETERMINISM_SPECIFICATION | seed/input stream | replay fixture | tolerance comparison | Q4 | objective |
| Five-city campaign | CAMPAIGN_CONTENT_BUDGET | campaign state | production content | campaign QA | Q4/Q5 | objective |
| Multiplayer | scope rules | deferred | none | none | future | deferred |
