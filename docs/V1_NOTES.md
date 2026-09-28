# RP5-Turnip V1 — Development Notes

## Objective

Create a Turnip build specifically targeted at the Retroid Pocket 5's Snapdragon 865 / Adreno 650 for Switch emulation in Eden Legacy v0.2.0-rc1.

Current user observations:
- R9v2 feels more stable.
- MrPurple T19 feels faster and appears to show more detail.

V1 therefore uses Mesa 24.3.x as the baseline and treats R9v2 as the stability reference and T19 as the performance/detail reference.

## Method

Do not combine many speculative changes in one revision. Apply one change, build, test, compare, and keep/revert based on evidence.

## V1 first experiment

The V1 source package contains an A650/GMEM-focused research experiment. It must be compiled and benchmarked before conclusions are drawn.

This repository contains source modifications only; it does not claim to contain a finished Android `.so` or Eden `.adpkg` driver.

## Results template

### R9v2
FPS:
Smoothness:
Detail:
Stutter:
Graphics:
Crashes:
Temperature:

### T19
FPS:
Smoothness:
Detail:
Stutter:
Graphics:
Crashes:
Temperature:

### RP5-Turnip V1
FPS:
Smoothness:
Detail:
Stutter:
Graphics:
Crashes:
Temperature:
