# Performance and memory budget

## Initial budgets to validate

- Primary target: stable 60 FPS on the agreed recommended PC profile.
- Frame budget at 60 FPS: 16.67 ms total.
- Initial allocation hypothesis: game/logic 4 ms, physics 4 ms, AI 2.5 ms, rendering 5 ms, streaming/audio/UI 1.17 ms. Rebalance after profiling.
- Streaming hitch target: no visible hitch during normal traversal after warm-up; record all exceptions.
- Audio/VFX budgets tracked separately for CPU, GPU, memory, voices, particles, lights, and translucency.

## Memory

Set explicit budgets for executable, textures, meshes, audio, VFX, world cells, save data, and transient traffic. Final values depend on hardware and must be recorded in the project profile.

## Performance gate

Benchmark at maximum designed traffic, rival, Authority, weather, destruction, and streaming load. A feature that exceeds budget needs optimization, a scoped fallback, or an approved budget change.
