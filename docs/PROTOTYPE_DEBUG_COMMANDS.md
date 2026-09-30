# Prototype debug commands

## World

- `ash.world.reset_state`
- `ash.world.set_city_state <state>`
- `ash.world.reveal_landmarks`
- `ash.world.teleport <landmark_id>`
- `ash.world.stream_report`

## Vehicle

- `ash.vehicle.spawn <vehicle_id>`
- `ash.vehicle.damage <component> <amount>`
- `ash.vehicle.repair`
- `ash.vehicle.set_weather_grip <value>`
- `ash.vehicle.reset`

## AI and events

- `ash.ai.spawn_rival <rival_id>`
- `ash.ai.spawn_authority <unit_id>`
- `ash.ai.set_heat <tier>`
- `ash.event.start <event_id>`
- `ash.event.complete <event_id> <outcome>`
- `ash.activity.start <activity_id>`

## QA

- `ash.qa.seed <value>`
- `ash.qa.start_replay_record`
- `ash.qa.start_replay_playback`
- `ash.qa.performance_capture`
- `ash.qa.accessibility_report`
