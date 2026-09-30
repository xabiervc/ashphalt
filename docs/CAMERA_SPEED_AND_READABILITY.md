# Camera, speed, and readability

## Camera modes

- Default chase camera: stable, slightly elevated, collision-aware.
- Impact camera: short, proportional impulse; never removes control unexpectedly.
- High-speed camera: subtle FOV increase and motion cues, with accessibility disable.
- Exploration camera: wider awareness and reduced shake.
- Replay camera: separate presentation layer, never required for play.

## Readability rules

At driving speed the player must distinguish road surface, route boundary, obstacle, rival, Authority threat, workshop, landmark, and shortcut entrance. Critical threats require visual and audio redundancy.

## Initial values to test

- Default FOV: 85-95 degrees depending on resolution and camera distance.
- High-speed FOV increase: 5-10 degrees.
- Minimum warning lead time: 1.5 seconds for standard hazards, 2.5 seconds for major route changes.
- Camera shake default: low/medium, with full disable option.

## Acceptance

Blind testers can identify why they crashed and where to go next in at least 80% of sampled failures.
