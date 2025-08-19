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
