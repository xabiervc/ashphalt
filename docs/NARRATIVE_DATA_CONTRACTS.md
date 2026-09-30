# Narrative data contracts

## StoryDecision

`DecisionId`, `StageId`, `ContextEventId`, `Options`, `SelectedOption`, `ImmediateEffects`, `DelayedEffects`, `FactionDeltas`, `CityStateEffects`, `Unlocks`, `Locks`, `RequiredFlags`, `FallbackText`, `LocalizationKeys`.

## CharacterState

`CharacterId`, `Trust`, `Debt`, `Fear`, `Respect`, `FactionStandingSnapshot`, `RelationshipTier`, `AvailableScenes`, `AvailableContracts`, `ExitState`.

## CityState

`CityId`, `State`, `TransitionCause`, `TransitionEventId`, `RouteOverrides`, `FactionControl`, `EmergencyStatus`, `WeatherSeed`, `RecoveryFlags`, `NarrativeFlags`.

## AshRaceStage

`StageId`, `CityId`, `RequiredEvents`, `OptionalEvents`, `RivalAppearances`, `RouteChoices`, `WeatherPolicies`, `ChaosThresholds`, `DecisionIds`, `Rewards`, `FailureStates`, `DepartureRules`.

## Validation

All IDs are stable and unique. All options have fallback text. All effects are serializable. All decisions have at least one test for immediate effect, delayed effect, save/load, and ending influence.
