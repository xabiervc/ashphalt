# First playable slice

## Purpose

Prove that Ashphalt's central loop is fun and technically viable before expanding content.

## Required playable content

- One compact fictional district.
- One closed-loop race route with one shortcut.
- One player vehicle using Chaos Vehicles.
- One rival placeholder vehicle.
- Basic throttle, brake, steering, handbrake, camera, and recovery.
- Component damage for chassis, engine, wheels, and bodywork.
- A workshop that restores damage.
- One event objective: finish first or disable the rival.
- One faction reputation change.
- One visible consequence: workshop price, route access, or patrol disposition.
- Basic HUD showing speed, objective, damage, timer, and consequence feedback.

## Deliberately excluded

Traffic crowds, pedestrians, advanced emergency AI, dynamic weather, multiple districts, full narrative, multiplayer, final art, and online services.

## Acceptance tests

1. The player can start, drive, brake, turn, collide, recover, and finish.
2. Collision damage changes at least one vehicle function and is visible.
3. Entering the workshop restores the vehicle through the common repair interface.
4. The event can be won by finishing or disabling the rival.
5. The event produces a deterministic reputation event with a visible reason.
6. The consequence changes a subsequent interaction.
7. The build runs at the agreed target frame rate on the development machine.
8. A fresh run can be repeated with the same seed and input sequence within documented tolerances.

## Exit decision

Mark the slice `PASS`, `PASS WITH RISKS`, or `FAIL`. A `FAIL` must identify a blocking issue and a reproduction procedure.
