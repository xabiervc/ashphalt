# Driving control model

## Control goals

The vehicle should feel heavy enough for impacts to matter, but responsive enough for a player to correct a mistake without wrestling the physics.

## Inputs

- Throttle: analog where available; keyboard uses a configurable curve.
- Brake/reverse: separate input with progressive braking.
- Steering: speed-sensitive response with adjustable sensitivity and dead zone.
- Handbrake: deliberate rotation tool, not default turning input.
- Recovery: controlled reset with cost/state feedback.
- Camera/look: independent camera rotation and optional aim assist for threats.

## Initial tuning hypotheses

- Usable steering response: first meaningful heading change within 120 ms of input at low speed.
- High-speed steering smoothing: 80-160 ms response window, adjustable after playtest.
- Full braking from 100 km/h: target 35-50 m depending on vehicle archetype.
- Recovery from a moderate slide: 0.8-1.8 s for a trained player.
- Input-to-visible-response target: under 100 ms excluding display latency.

These are prototype targets, not production promises.

## Failure clarity

When control is lost, show whether cause was input, grip, damage, weather, collision, or route geometry. Do not hide systemic causes behind random physics.
