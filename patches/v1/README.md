# V1 source modifications

This directory is reserved for source-level experimental changes targeting the Retroid Pocket 5 / Snapdragon 865 / Adreno 650 and Eden.

Rules:
1. Keep each logical change separate where possible.
2. Record the exact Mesa base commit.
3. Explain the expected technical effect.
4. Compile and test before drawing conclusions.
5. Record regressions as carefully as improvements.
6. Revert changes that introduce unacceptable instability or corruption.

The initial work investigates A650 rendering behaviour, including GMEM/sysmem decisions, while preserving a controlled baseline.

A change is **not considered an optimisation merely because it compiles**. It becomes a candidate optimisation only after measured testing on the target device.
