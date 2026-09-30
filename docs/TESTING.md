# Testing protocol

## Driver comparison

Compare:
1. R9v2
2. T19
3. RP5-Turnip V1
4. Later RP5-Turnip revisions

Do not change Eden settings between driver tests unless the test explicitly targets an Eden setting.

## Fixed Eden baseline

### System
- Limit speed: Default
- Docked Mode: ON

### CPU
- CPU Overclock: ON
- Synchronise core speed: ON
- Everything else: Default

### Graphics
- Resolution: 1x
- VSync: FIFO
- Window adapting filter: Bilinear
- Anti-aliasing: None

### Advanced
- GPU Mode: Fast
- DMA Accuracy: Default
- VRAM Usage: Conservative
- Sync Memory Operations: OFF
- Disk Shader Cache: ON
- Force Clocks: OFF
- Reactive Flushing: OFF
- Buffer History: ON
- Optimised Vertex Buffers: ON

### Hacks
- Fast GPU Time: Medium
- Legacy Rescale Pass: ON
- Everything else: Default

## Suggested test

Use the same workload, save/state and location where practical. Run for approximately 5–10 minutes.

| Metric | Result |
|---|---|
| FPS | |
| Smoothness / frame pacing | |
| Shader stutter | |
| Visual quality/detail | |
| Graphical errors | |
| Crash/freeze/reboot | |
| Temperature | |
| Battery/thermal behaviour | |

If desired, rate each build separately from 1–10 for Performance, Smoothness, Visual quality and Stability. Do not combine them into one overall score.
