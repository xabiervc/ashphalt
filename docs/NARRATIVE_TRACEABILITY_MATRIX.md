# Narrative traceability matrix

| Decision/action | State variable | Scene/event | Immediate result | Delayed result | Ending influence | Test |
|---|---|---|---|---|---|---|
| Protect convoy | `SettlementAidScore` | `EV_VERGE_CONVOY_01` aftermath | Settlements +8 | safe route unlock | coalition weight | `NT-001` |
| Destroy checkpoint | `AuthorityHeat` | `EV_CROWN_AUTHORITY_01` | score/heat | elite response | Authority-control penalty | `NT-002` |
| Accept illegal upgrade | `UnderworldDebt` | Workshop Row broker scene | vehicle advantage | debt ambush | Underworld control weight | `NT-003` |
| Rescue rival | `RivalTrust_<id>` | rival aftermath scene | lost time/reward | alliance support | coalition/Circuit weight | `NT-004` |
| Push city to Ash State | `CityState_<id>` | city aftermath | maximum Chaos Rating | route/economy damage | collapse weight | `NT-005` |
| Destroy protected emergency unit | `EmergencyCollateral` | response aftermath | score/penalty | faction hostility | destructive ending weight | `NT-006` |
| Release Fire Key | `FireKeyControl` | The Gate finale | branch selection | network ownership | ending selection | `NT-007` |

Every new decision must add a row with variable, scene/event, immediate/delayed effect, ending influence, save behavior, and test.
