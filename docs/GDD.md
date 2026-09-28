# Ashphalt — Game Design Document

## 1. High concept

Ashphalt is a single-player-first post-apocalyptic arcade racing and vehicular-combat game. It combines reckless street racing, vehicle destruction, repair and tuning, faction politics, dynamic weather, and a consequence-driven original story.

The game is inspired by the energy of classic destruction racers but is not a remake. It uses a new title, fictional cities, fictional vehicle manufacturers, original characters, and an original setting.

## 2. Design goals

- Make reckless driving exciting without making the car uncontrollably fragile.
- Make destruction a useful strategy, not only visual spectacle.
- Make repairs and tuning meaningful while keeping them fast and enjoyable.
- Make player choices visible through prices, access, enemy behavior, missions, and endings.
- Build systems that are reproducible and testable wherever practical.
- Prioritize handling responsiveness, performance, and fun over feature count.

## 3. Setting

Civilization has not completely ended, but the old urban order has collapsed. Several fictional cities and districts are isolated by infrastructure failure, environmental disasters, and competing factions. Racing is entertainment, transport, commerce, intimidation, and political power.

The locations are fictional and designed for gameplay. They may use broad urban archetypes — dense downtown, industrial docks, suburban sprawl, desert highway settlement, flooded lowlands — but they are not intended to represent a specific real city.

The visual language is post-apocalyptic: cracked asphalt, overgrowth, damaged infrastructure, improvised barricades, abandoned vehicles, ash, smoke, broken lights, and repurposed buildings. The world should clearly communicate that this is not an ordinary present-day city.

## 4. Core gameplay loop

1. Accept or discover a race, contract, challenge, or faction opportunity.
2. Choose a vehicle and inspect its damage, tuning, condition, and available power-ups.
3. Select a route and decide whether to race cleanly, exploit shortcuts, attack rivals, or create chaos.
4. Drive through a dense district with traffic, pedestrians, hazards, emergency units, weather, and faction activity.
5. Earn time, money, reputation, parts, vehicles, and story consequences.
6. Visit a repair shop, salvage parts, tune the vehicle, and prepare for the next event.
7. Respond to the changing world and make major decisions that shape the campaign.

## 5. Race objectives

Each event can combine several objectives:

- Finish first.
- Destroy or disable rival vehicles.
- Survive for a time limit.
- Reach a target destruction score.
- Protect or sabotage a convoy.
- Escape Authority pursuit.
- Deliver a vehicle or part while preserving its condition.
- Complete a faction contract.

Checkpoints may structure a route, but they must not be the primary source of time rewards. Destruction, skillful risks, shortcuts, and event-specific actions should drive the arcade fantasy.

## 6. Vehicles

All manufacturers and model names are fictional. Vehicle designs should blend cues from multiple broad archetypes rather than copying one real car's distinctive trade dress.

Initial archetypes:

- Muscle-style brawler: heavy, powerful, strong ramming potential.
- Hot-hatch-style agile car: quick acceleration, good turning, lower armor.
- Off-road pickup-style vehicle: durable, stable on debris, slower on clean asphalt.
- Supercar-style machine: very fast, expensive, fragile under sustained damage.
- Utility van-style vehicle: high mass and cargo utility, poor agility, strong support potential.
- Faction variants: Authority interceptor, Underworld scavenger build, Settlement utility vehicle, Circuit specialist racer.

Every vehicle should expose data-driven values for mass, acceleration, top speed, steering response, braking, tire grip, armor, engine durability, wheel durability, repair cost, and tuning compatibility.

## 7. Damage and repair

Damage is component-based:

- Chassis.
- Engine.
- Wheels and suspension.
- Bodywork and protective parts.
- Optional ramming attachments.

Damage must affect function gradually. A damaged engine can reduce acceleration and top speed; a damaged wheel can affect steering and stability; destroyed bodywork can increase vulnerability. The system should produce sparks, smoke, detached parts, deformation, and readable audio/visual feedback.

The tuning and damage systems must support reckless play. One collision should not make the vehicle useless, but repeated abuse should create visible and strategic consequences.

Repair shops are fast and visual. Parts should visibly reattach or be replaced over a short sequence. The same repair API must work for player and AI vehicles. Repair prices and part availability can be modified by faction reputation.

## 8. Tuning and power-ups

Tuning categories:

- Engine output and cooling.
- Armor and structural reinforcement.
- Tires and grip.
- Weight distribution.
- Brakes and suspension.
- Ramming attachments.
- Utility equipment.

Power-ups should be creative, readable, and balanced around short-term decisions. They may alter handling, damage, traffic, repairs, or pursuit, but should not replace driving skill.

Tuning must be data-driven through Unreal Data Assets or Data Tables and apply symmetrically to AI vehicles.

## 9. Factions and reputation

Each faction has an independent standing value from -100 to +100:

- **The Authority:** law enforcement remnants and centralized order.
- **The Underworld:** scavenger gangs and black-market repair networks.
- **The Settlements:** civilians attempting to rebuild.
- **The Circuit:** rival racer crews and their underground league.

Standing tiers:

- Hostile.
- Unfriendly.
- Neutral.
- Friendly.
- Allied.

Actions that affect standing should be understandable: destroying a faction convoy, protecting a settlement, accepting a black-market job, betraying a crew, helping emergency responders, or sabotaging a rival event.

Consequences must be visible through at least three channels:

- **Economy:** workshop prices, repairs, tuning parts, salvage and rewards.
- **Access:** districts, shortcuts, races, safehouses, and contracts.
- **Behavior:** patrol aggression, gang ambushes, escorts, rival targeting, and emergency response.
- **Story:** major decisions and different campaign endings.

Avoid dozens of tiny branches. Use a small number of clearly signposted mega-decisions whose consequences persist.

## 10. AI

Use Unreal Behavior Trees, Blackboard, NavMesh, and EQS where appropriate. Evaluate Mass Entity later if traffic or crowd counts demand it.

AI groups:

- Traffic follows lanes, reacts to collisions, stops at obstacles, and behaves differently under weather conditions.
- Pedestrians use stylized, non-photorealistic designs and flee dangerous situations.
- Authority units pursue according to public damage and reputation.
- Fire and ambulance equivalents respond to accident events.
- Rival racers use vehicle tuning, faction disposition, route choices, attacks, repairs, and opportunistic shortcuts.

AI should be testable independently through debug spawners and controlled scenarios.

## 11. Weather and world events

Weather states include rain, fog, ash storms, and sandstorms. They can alter grip, visibility, AI decisions, audio, lighting, and route availability.

World events may include:

- Flooded streets.
- Collapsing structures.
- Convoy ambushes.
- Authority checkpoints.
- Gang roadblocks.
- Emergency response scenes.
- Temporary shortcuts through debris.

The system should be seeded and reproducible for tests and replays.

## 12. Determinism and testing

Determinism is a priority wherever practical:

- Use a fixed simulation tick for gameplay logic.
- Define an explicit system update order.
- Use explicit seeded random streams for weather, spawns, AI variance, and event selection.
- Avoid gameplay-affecting unseeded randomness.
- Record inputs and seeds for replay and regression testing.
- Do not assume Unreal Chaos physics is bit-exact across all hardware and platforms. Use authoritative state and tolerances if multiplayer is added in the future.

Every phase must include:

- A minimal test map or scenario.
- Acceptance criteria.
- Debug commands or instrumentation where useful.
- A performance check.
- A short entry in `PROGRESS.md`.

## 13. Narrative structure

The campaign follows a rising driver who becomes involved in the conflict between the four factions. The Circuit offers fame and access, the Underworld offers illegal performance, the Settlements offer legitimacy and protection, and the Authority offers order at a price.

The story should allow alliances, betrayals, opportunism, and partial cooperation. The player should not be forced into a simple good/evil path.

Start with 2-3 major decision points and several possible endings based on the accumulated reputation pattern and selected decisions. Prototype the logic before producing expensive cinematics.

## 14. Scope priorities

Priority 1: vehicle handling, collision feel, damage readability, and a fun test district.

Priority 2: vehicle variety, tuning, repair, race objectives, traffic, and faction consequences.

Priority 3: story content, weather variety, larger districts, additional vehicles, polish, and replay features.

Deferred: local multiplayer, online multiplayer, matchmaking, dedicated servers, and live-service features.

## 15. Unreal Engine architecture

- Chaos Vehicles for vehicle physics.
- C++ for stable core systems and performance-sensitive code where appropriate.
- Blueprints for iteration, content setup, UI, and designer-facing logic.
- Data Assets/Data Tables for vehicles, tuning, factions, weather, events, and story decisions.
- Behavior Trees, Blackboard, NavMesh, and EQS for AI.
- SaveGame for campaign state, reputation, decisions, unlocked vehicles, and upgrades.
- Unreal Insights and profiling tools from the first playable build.

## 16. Initial phase plan

1. Build a fictional district and closed-loop race circuit.
2. Add the player vehicle with Chaos Vehicles.
3. Add component-based damage.
4. Add the initial fictional vehicle roster.
5. Add tuning.
6. Add the repair-shop loop.
7. Add factions and reputation.
8. Connect reputation to economy, access, and AI disposition.
9. Add traffic and pedestrians.
10. Add Authority and emergency AI.
11. Add weather and route events.
12. Add story decisions and endings.
13. Add input-based replay validation.

Multiplayer remains outside the current scope.
