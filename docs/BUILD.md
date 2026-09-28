# Build notes

A complete Android Turnip build requires the Mesa source tree plus an Android/ARM64 build environment and appropriate AdrenoTools packaging configuration.

Recommended workflow:

1. Obtain Mesa 24.3.0 source.
2. Apply the patch in `patches/v1/` to the exact source revision it targets.
3. Configure an Android AArch64 Mesa/Turnip build.
4. Compile the Turnip Vulkan driver.
5. Package the resulting library using an Eden-compatible AdrenoTools driver package.
6. Test on an actual Snapdragon 865 / Adreno 650 using the fixed BOTW configuration.

Do not claim a build is V1-release quality until it has been tested on the target hardware.
