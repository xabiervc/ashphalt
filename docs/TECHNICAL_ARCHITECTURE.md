# Technical architecture

For the open-city prototype, add a city/world state service, cell ownership/persistence, landmark registry, route/activity registry, traffic density service, and benchmark instrumentation to the previously defined Unreal layers.

Transient traffic and pedestrian actors may be pooled or unloaded; persistent city state, events, routes, rival relationships, reputation, weather seed, and consequences belong to world/campaign services.
