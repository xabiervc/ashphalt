# Data contracts

## VehicleDefinition

`Id`, `ManufacturerId`, `Archetype`, `Mass`, `EngineProfile`, `HandlingProfile`, `ArmorProfile`, `ComponentHealth`, `TuningSlots`, `RepairProfile`, `DamageParts`, `FactionTags`, `UnlockRule`.

## UpgradeDefinition

`Id`, `Slot`, `StatModifiers`, `TradeOffs`, `CompatibilityRules`, `Cost`, `PartCost`, `FactionAvailability`, `VisualChange`, `AIEligibility`.

## FactionDefinition

`Id`, `DisplayName`, `StandingBounds`, `TierThresholds`, `EconomyModifiers`, `AccessRules`, `DispositionRules`, `EndingTags`.

## RaceEventDefinition

`Id`, `DistrictId`, `Objective`, `Participants`, `Route`, `WeatherSeedPolicy`, `FailureRules`, `Rewards`, `ReputationEffects`, `UnlockEffects`, `AftermathState`.

## WeatherDefinition

`Id`, `GripModifier`, `VisibilityModifier`, `AIProfile`, `RouteEffects`, `AudioProfile`, `TransitionRules`, `SeedPolicy`.

## SaveGame

Version, campaign seed, current district, vehicle states, upgrades, credits, parts, faction standing, decisions, unlocks, world events, and migration metadata.

## Replay

Build ID, data revision, map ID, configuration hash, tick rate, seed manifest, input stream, external commands, checkpoints, tolerance profile, and validation result.
