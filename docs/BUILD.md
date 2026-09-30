# Build

The project targets an Android ARM64 Turnip build for the Adreno 650.

Required components include:
- Mesa source tree at the selected baseline
- Android NDK/toolchain
- Meson/Ninja build environment
- Appropriate Mesa/Turnip Android configuration
- Eden-compatible driver packaging configuration

The complete Mesa source tree is intentionally not committed to this repository.

Every build should record:
- Mesa tag/commit
- patch list
- Android NDK version
- compiler/toolchain version
- build date
- resulting driver hash

Do not label a binary as a tested RP5 release until it has been tested on an actual Snapdragon 865 / Adreno 650 device.
