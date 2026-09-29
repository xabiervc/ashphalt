# Determinism specification

## Goal

Make gameplay decisions, event selection, AI choices, weather, and replay inputs reproducible wherever practical. Do not promise bit-exact Chaos physics across hardware.

## Rules

- Gameplay logic uses a fixed tick.
- Systems run in an explicit documented order.
- Every random stream has a name, seed, owner, and purpose.
- No global unseeded random calls in gameplay code.
- Event IDs and seeds are saved with replay/session metadata.
- Floating-point comparisons use documented tolerances.
- AI tie-breakers use stable IDs rather than container iteration order.

## Suggested order

Input capture → event seed update → traffic → pedestrians → rivals → Authority/emergency → vehicle physics integration → collision damage → reputation/economy events → race objectives → save/replay sampling.

## Replay scope

Record initial map/configuration IDs, seed manifest, tick rate, player inputs, and significant external commands. Compare transforms, damage, events, reputation, and weather within tolerance.

## Known limitation

Chaos physics may diverge across platforms. If divergence exceeds tolerance, record a state checkpoint and diagnose rather than hiding the discrepancy.
