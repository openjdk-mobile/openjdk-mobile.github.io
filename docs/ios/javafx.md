# JavaFX Applications on iOS

This track enables full **JavaFX applications** to run as native iOS apps.

## Requirements

- **JavaFX runtime adapted for iOS** – platform layer and native peers integrated with iOS.
- **Platform integration** – integrate JavaFX lifecycle with `UIApplication` lifecycle.
- **Rendering pipeline** – map JavaFX rendering to iOS graphics APIs, handle touch events.
- **Packaging & deployment** – bundle VM, JavaFX runtime, resources, and app code into installable iOS app.

## Acceptance Criteria

- Simple JavaFX scene renders on iOS and handles touch input.
- App lifecycle (background/foreground/rotation) works correctly.
- Packaging produces a deployable iOS app that passes basic stability and UI responsiveness tests.

## Approach

Both OpenJDK and OpenJFX have several requirements for the underlying operating system and environment,
and both rely on a variety of tools (including compilers and linkers) to build artifacts.
To minimize overlap and increase consistency, we aim to leverage the same tools. Therefore,
we will first build the OpenJFX code using the OpenJDK build system.

Although, in theory, we only need to build OpenJFX for iOS and Android, using the same approach for 
building OpenJFX on desktop platforms offers benefits. Work of this is ongoing in the
https://github.com/organizations/openjdk-mobile repository



