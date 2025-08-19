# Mission & Philosophy

## Our Goal

We want to re-establish Java as a top-quality, cross-platform language for mobile. This means providing the real Java — fully aligned with OpenJDK — along with the tools and documentation needed to run it on iOS and Android.

## Core Principles

- **Real Java Only** – We stay as close as possible to OpenJDK. Mobile developers should be able to use all features available in the upstream JDK without hacks or workarounds.
- **Developer-first Alignment** – If something exists in OpenJDK, mobile developers should have access to it. There should be no “mobile-only” divergence in functionality.
- **Infrastructure Focus** – The project creates the *tools, code, and documentation* needed to bring Java to mobile. We are not writing tutorials for building apps — the community can build on this foundation.
- **Two Primary Use Cases**:
  1. **Libraries**: Enable Java libraries to be compiled and packaged as first-class components on mobile platforms.
  2. **Applications**: Enable full Java apps (including JavaFX) to run on mobile platforms with minimal platform-specific code.

## Vision

By adhering to these principles, we aim to create a sustainable ecosystem where:

- Java developers can confidently build for mobile using the standard JDK.
- Mobile platforms gain robust, maintainable Java support.
- Contributions are guided by clear philosophy rather than ad hoc decisions.

## Managing Complexity

The OpenJDK project itself is complex, and a mobile operating system with its ecosystem and specific requirements is complex as well. When complex components need to work together or be integrated, overall complexity increases, and maintenance costs can rise sharply. To keep the system maintainable and reliable, we aim to minimize the number of components and the number of build tools, ensuring a lean and coherent architecture.

## Keeping Mobile in Sync

All commits applied to **OpenJDK/jdk** are automatically merged into OpenJDK/mobile. This ensures that the downstream repository always contains the **latest Java**, avoiding discrepancies between server, cloud, desktop, and mobile development. Maintaining this alignment is a key requirement, so that mobile developers can rely on the same Java platform as other environments while we continue to evolve mobile support.

