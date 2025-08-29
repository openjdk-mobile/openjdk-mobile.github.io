# HelloWorld on iOS

**HelloWorld** is the first milestone to bring Java to iOS. It validates the runtime and ensures core components work correctly.

## Why HelloWorld First

- **Validate VM + classlibs** – confirms that the OpenJDK/mobile VM and standard class libraries work on iOS.
- **Close to upstream** – minimal program stays aligned with OpenJDK to surface regressions.
- **Continuous regression testing** – daily builds of `HelloWorld.jar` detect issues early.

## Acceptance Criteria

- VM launches on simulator and device and executes `HelloWorld` output without crashes.
- Classloaders, basic reflection, and standard library calls succeed.
- Artifact is reproducible and integrated into CI for regression detection.

## Steps to get it working

- Running `helloworld` involves a number of steps described in the [ios-tools repo](https://github.com/openjdk-mobile/ios-tools/blob/main/docs/helloworld.md)
- For each step you can choose to build (e.g. OpenJDK/mobile) yourself or download a build from the repo's releases

