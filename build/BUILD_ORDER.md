# Recommended build order

1. Start from Mesa 24.3.0.
2. Build an unmodified baseline where possible.
3. Record the baseline Mesa commit and toolchain versions.
4. Apply V1 patches one at a time.
5. Build ARM64 Android Turnip.
6. Package the resulting driver for Eden.
7. Test on the RP5 using the fixed Eden configuration.
8. Record results in `docs/TESTING.md`.
9. Only then proceed to V1.1/V2 changes.

Compiled binaries should be published separately as releases once validated.
