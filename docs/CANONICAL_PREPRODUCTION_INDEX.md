# Canonical pre-production index

## Authority model

This document defines document hierarchy. It prevents multiple files with "final" wording from silently contradicting one another.

## Normative hierarchy

1. `GDD.md` — product brief, fixed canon, pillars, scope, and high-level promise.
2. Specialist design documents — system rules and content definitions.
3. Data contracts — serialization and implementation shape.
4. Quality/QA documents — measurable acceptance and evidence.
5. Prompts and handoff documents — execution instructions, never new design authority.

If two documents conflict, the higher-level document wins only after the conflict is logged and resolved. Claude must stop and report unresolved conflicts.

## Normative specialist documents

- Core: `CORE_GAMEPLAY_SPECIFICATION.md`, `DRIVING_CONTROL_MODEL.md`, `VEHICLE_FEEL_METRICS.md`.
- World: `OPEN_CITY_DESIGN.md`, `CITY_SIZE_AND_DENSITY.md`, `CITY_STATE_MACHINE.md`.
- Campaign: `THE_ASH_RACE_CAMPAIGN.md`, `CAMPAIGN_STAGE_SPECIFICATION.md`, `CAMPAIGN_TIMELINE.md`.
- Narrative: `NARRATIVE_STATE_MACHINE.md`, `CHARACTER_ARCS.md`, `CANON_RULES.md`, `NARRATIVE_DATA_CONTRACTS.md`.
- Content: `CONTENT_INVENTORY_MATRIX.md`, `VERTICAL_SLICE_OPERATIONAL_PLAN.md`.
- Technical: `TECHNICAL_ARCHITECTURE.md`, `DATA_CONTRACTS.md`, `DETERMINISM_SPECIFICATION.md`.
- Quality: `QUALITY_GATES.md`, `QA_AND_VALIDATION.md`, `VERTICAL_SLICE_READINESS_GATE.md`, `PRODUCTION_READINESS_GATE.md`.

## Status rule

Every document has a status: Normative, Supporting, Operational, Deferred, Superseded, or Experimental. Only Normative and Operational documents may define implementation requirements.
