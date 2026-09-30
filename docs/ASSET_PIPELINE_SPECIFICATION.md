# Asset pipeline specification

## Asset lifecycle

Brief → concept → blockout → functional prototype → review → optimization → integration → QA → approved → maintained/deprecated.

## Required metadata

Stable ID, owner, source/license, domain, dependencies, memory budget, LOD policy, collision policy, audio/VFX hooks, localization keys, accessibility review, platform status, and approval state.

## Unreal rules

Use source control for text/source/config and Git LFS or approved storage for binaries. Generated folders remain ignored. Data Assets and Data Tables are validated for IDs, ranges, references, and version migration.

## Acceptance

A new asset can be traced from design requirement to file, owner, test, performance result, and release approval.
