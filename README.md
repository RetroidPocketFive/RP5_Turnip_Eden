# RP5-Turnip-Eden

Experimental Mesa Turnip Vulkan driver development for the **Retroid Pocket 5 (Qualcomm Snapdragon 865 / Adreno 650)**, focused on performance, stability and compatibility with the **Eden emulator**.

> **Status: Experimental / research**
>
> This project is independent and is not affiliated with or endorsed by Mesa, Qualcomm, Retroid, or Eden.

## Project goal

Investigate and develop hardware-focused Turnip changes for the Snapdragon 865 / Adreno 650, with the primary objective of optimising the Retroid Pocket 5 experience in Eden.

Focus areas:
- GPU performance
- frame pacing
- shader compilation behaviour
- rendering efficiency
- memory behaviour
- Vulkan compatibility
- stability
- thermal/power efficiency
- Eden compatibility
- RP5-specific optimisation

The project is **not tied to any particular application or game**. Individual workloads are used only as repeatable test cases.

## Hardware baseline

| Component | Target |
|---|---|
| Device | Retroid Pocket 5 |
| SoC | Qualcomm Snapdragon 865 / SM8250 |
| GPU | Adreno 650 |
| RAM | 8 GB |
| Android | 13 |
| Eden | Legacy v0.2.0-rc1 |

## Reference drivers

- **Mesa Turnip 24.3.0 Revision 9v2** — current stability reference
- **MrPurple T19-toasted / Mesa 25.1.0-devel** — current performance/detail reference

These are practical reference points from testing on the target device, not universal benchmark claims.

## Development baseline

- Mesa source baseline: **24.3.0**
- Target: Android ARM64 / Adreno 650
- Emulator baseline: Eden Legacy v0.2.0-rc1

## V1 philosophy

V1 is deliberately conservative. Changes should be isolated wherever practical so a performance or stability change can be attributed to a specific modification.

**baseline → one change → build → test → compare → keep/revert**

The first source experiment remains an experiment until compiled and tested on the actual RP5.

## Testing

Keep the same Eden configuration between driver comparisons whenever possible.

Record:
- FPS
- frame-time smoothness
- shader stutter
- visual quality/detail
- graphical corruption
- crashes/freezes/reboots
- temperature, if available
- battery/thermal behaviour where practical

## Safety

Experimental GPU drivers can cause emulator crashes and device instability. Keep a known-good driver available and do not use experimental builds as your only driver.

## Repository structure

```text
RP5_Turnip_Eden/
├── README.md
├── CHANGELOG.md
├── LICENSE-NOTICE.md
├── docs/
│   ├── HARDWARE.md
│   ├── TESTING.md
│   ├── BUILD.md
│   └── PROJECT_STATUS.md
├── patches/
│   └── v1/
│       ├── README.md
│       └── mesa/
└── build/
    └── BUILD_ORDER.md
```

Mesa source is intentionally not vendored into this repository. Upstream Mesa licensing and copyright notices must be retained for any source distributed here.
