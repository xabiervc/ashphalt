# Metrics test map specification

## Layout

- 500 m straight for acceleration and top speed.
- 300 m braking lanes from three speeds.
- Slalom with 12 m, 18 m, and 25 m spacing.
- 90-degree and hairpin turns.
- Ramp and uneven landing.
- Debris field with readable and unreadable variants.
- Wet, ash, and dry surfaces.
- Collision wall with impulse logging.
- Recovery lane and workshop trigger.

## Instrumentation

Display speed, steering input, throttle, brake, slip angle, tire contact, surface type, damage per component, impulse, recovery timer, camera FOV, frame time, physics time, and AI time.

## Reproducibility

The map uses stable IDs and fixed test seeds. Each run exports a compact result record for comparison.
