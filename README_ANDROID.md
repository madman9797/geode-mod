# Flappy Maker Bird — Android Geode build

This project is prepared specifically for building the Geode mod for Android.

## Easiest method with only an Android phone

You do not need to compile the C++ project locally on the phone. GitHub Actions can build the Android `.geode` package in the cloud.

1. Create a GitHub repository from this folder, or upload the files to an existing repository.
2. Open the repository's **Actions** tab.
3. Select **Build Flappy Maker Bird for Android**.
4. Run the workflow with **Run workflow**.
5. Wait for the build to finish.
6. Open the completed workflow run and download either:
   - `flappy-maker-bird-Android64` for 64-bit ARM Android (`arm64-v8a`), or
   - `flappy-maker-bird-Android32` for 32-bit ARM Android (`armeabi-v7a`).
7. Extract the `.geode` file if GitHub downloaded it as a ZIP.
8. With Geode installed, copy the `.geode` file to:
   `/storage/emulated/0/Android/media/com.geode.launcher/game/geode/mods/`

Geode's current documentation says Android builds use the Android NDK and the Geode Android binaries, and are built with `geode build -p android64` or `geode build -p android32`. The official Geode build action can build Android32 and Android64 in GitHub Actions.

## Local Android/Termux note

A local Android build is possible only if the required Geode CLI, SDK, Android NDK, CMake/Ninja toolchain, and compatible dependencies are available. The included GitHub Actions workflow is the simpler phone-only route.
