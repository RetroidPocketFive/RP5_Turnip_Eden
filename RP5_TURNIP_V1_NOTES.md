# RP5 Turnip V1 source modification

Target: Mesa 24.3.0 / Turnip, Snapdragon 865 / Adreno 650, Eden Legacy RC1.

## V1 change

`src/freedreno/vulkan/tu_cmd_buffer.cc` now prefers GMEM rendering on GPU ID 650 whenever the render pass is otherwise eligible for GMEM.

The existing `TU_DEBUG=sysmem` escape hatch remains available, so the build can still be tested against the original sysmem path.

### Why this is V1

This is deliberately a single, isolated driver behaviour change. It is intended to provide a clean A/B test against R9v2 and T19 instead of combining many speculative changes at once.

The A650 is known to have a history of Turnip/sysmem-related stability issues, and community A650-patched Turnip builds exist specifically to address crashes. See:
- https://github.com/Tranquility6789/Turnip-A650-Patched-Drivers
- https://github.com/nckstwrt/NetherSX2-Turnip

Mesa's Turnip documentation describes GMEM/sysmem as the two rendering paths on Adreno. The V1 change therefore targets the rendering-path selection rather than changing shader math or image formats.

## Important

This is source code only. It is **not yet a compiled Android driver**. It must be built with an Android AArch64 NDK/Mesa build environment before it can be installed in Eden.

## Test plan

Keep the user's existing Eden BOTW settings unchanged.

Compare:
1. R9v2
2. T19
3. RP5-Turnip V1

Record FPS, frame pacing, perceived detail, shader stutter, graphical corruption, crashes/reboots and temperature.

If V1 is less stable or slower, revert this single change and test a second profile rather than stacking changes.
