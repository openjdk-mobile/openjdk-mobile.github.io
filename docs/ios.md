# iOS Support

This section describes the work needed to run Java and JavaFX on iOS.

---

## 1. Mobile JVM

The core strategy is enabling Java applications to run inside iOS containers by compiling the JVM into a library.

### Approach
- Use VM functionality directly from **OpenJDK** instead of GraalVM.
- Start with the **Zero interpreter**.
- Explore **Project Leyden** for AOT in the future.

### Tasks
- Set up build pipeline for OpenJDK Mobile for iOS.

### End Result
- Downloadable JDK that runs on iOS.

---

## 2. Optimizations

Exploring **AOT compilation** in parallel:
- Supply native code for methods.
- Reduce app size by excluding bytecode when AOT is available.
- Leverage Project Leyden for maintainability.

### End Result
- A smaller, more performant iOS library.

---

## 3. Native/Java Bridge

Enable integration between **native iOS UI code** and **Java business logic**.

### Tasks
- Define bridging strategy.
- Provide generated APIs to interface with Java code.

### End Result
- Usable bridge layer for iOS developers.

---

## 4. Xcode Framework

Combine JVM + bridge into a framework usable by iOS developers.

### Work Plan
1. Build a simple C library (`add`, `multiply`).
2. Create a Hello World Xcode project.
3. Integrate C library into the project.
4. Document the developer workflow.

### End Result
- A usable Xcode framework.
- Documentation on usage.

---

## 5. JavaFX Integration with JDK Build

Challenges:
- Native code management.
- Disparate build systems (OpenJFX Gradle vs. OpenJDK make).
- Cumbersome cross-compilation.

### Goal
Unify builds into **1 toolchain per platform**, simplifying maintenance.

---

## 6. JavaFX on iOS

- Explore Metal rendering backend.
- Define if dependent on step 5.

---

## 7. App Packaging

- Define IPA packaging approach.
- Document deployment flow.

