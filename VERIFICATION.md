# Verification — 1.0.0 release (version code 2)

- Seven core tests pass: catalog, filtering, empty favorites, persistence, wraparound navigation, invalid saved data, and separate counters.
- JavaScript syntax check passes.
- The UI was exercised in a DOM harness for navigation, favorites, empty state, counter persistence, auto-advance and screensaver isolation. This is not a visual or device test.
- Android resources and Java sources were compiled using Android SDK 35 tools, Eclipse ECJ 3.38.0 and D8, then packaged and signed using a dedicated RSA-3072 release key. The APK signature was verified with apksigner (v1, v2 and v3). APK package metadata and minimum/target SDK were verified with aapt2.
- The Gradle Wrapper is 8.11.1 with the official distribution SHA-256. The full Gradle/AGP build and Android lint were not completed in this environment; the GitHub workflow is provided for those checks after upload.
- Not tested on a physical BYD head unit or Android emulator. Installation restrictions, device WebView version, orientation, fullscreen behavior, Arabic rendering and DreamService support require testing on the target device.
- No release signing key or signing secrets are included in the project. Signing certificate SHA-256: 02db3c3a26f05a37515655ea1c9ad79e69044db79b66942f5ab29ae5dbb08b7a.
