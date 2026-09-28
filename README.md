# RP5-Turnip-Eden

Experimental Mesa Turnip Vulkan driver development for the Retroid Pocket 5 (Qualcomm Snapdragon 865 / Adreno 650), focused on Nintendo Switch emulation with Eden.

## Status

**Experimental / research**

Not affiliated with or endorsed by Mesa, Qualcomm, Retroid, or Eden.

## Hardware target

| Component | Target |
|---|---|
| Device | Retroid Pocket 5 |
| SoC | Qualcomm Snapdragon 865 (SM8250) |
| GPU | Adreno 650 |
| RAM | 8 GB |
| Android | 13 |
| Eden baseline | Legacy v0.2.0-rc1 |
| Primary workload | Nintendo Switch emulation |
| Initial test | The Legend of Zelda: Breath of the Wild |

## Reference drivers

- Mesa Turnip 24.3.0 Revision 9v2 — stability reference
- MrPurple T19-toasted / Mesa 25.1.0-devel — performance/detail reference

The project's goal is not simply to use the newest Mesa release. It is to investigate changes that are useful specifically on Snapdragon 865 / Adreno 650 and Switch-emulation workloads.

## V1

V1 is a **source-level research patch**, not a finished Android driver binary.

The first experiment is deliberately isolated so later performance or stability changes can be attributed to individual modifications.

## Fixed BOTW test configuration

- Limit speed: default
- Docked mode: ON
- CPU overclock: ON
- Synchronise core speed: ON
- Resolution: 1x
- VSync: FIFO
- Window adapting filter: bilinear
- Anti-aliasing: none
- GPU mode: Fast
- DMA accuracy: default
- VRAM usage: conservative
- Sync memory operations: OFF
- Disk shader cache: ON
- Force clocks: OFF
- Reactive flushing: OFF
- Buffer history: ON
- Optimised vertex buffers: ON
- Fast GPU time: Medium
- Legacy rescale pass: ON
- Other settings: default

## Benchmark notes

For each driver record FPS, frame-time smoothness, shader stutter, visual detail, graphical corruption, crashes/freezes/reboots, and temperature if available. Use the same scene and settings whenever possible.

## Safety

Experimental GPU drivers can cause emulator crashes and, in rare cases, device instability. Keep a known-good driver available and do not treat experimental builds as production software.

## Licensing

Mesa and its components retain their upstream licensing and copyright notices. See the upstream Mesa source and individual source files for applicable licenses.
