# Architecture

This project is organized around a modular architecture that separates the concerns of the Java runtime, the Java standard library, application code, and supporting tooling. The main components are:

---

## 1. VM

The **Virtual Machine (VM)** is built from [OpenJDK/mobile](openjdk-mobile.md). It provides the core runtime functionality of OpenJDK on mobile platforms and is implemented natively on each target OS.  

- Delivered as a **shared or static library**.  
- Contains the standard OpenJDK VM features adapted for mobile environments.  
- Ensures compatibility between server/cloud/desktop Java and mobile Java.  

---

## 2. JDK Classes

The **JDK classes** component is also built from OpenJDK/mobile and contains the standard Java libraries for mobile:  

- Includes **class files** in bytecode form (jars, jmods, or optionally AOT-compiled classes).  
- Includes **native code** required by these class files.  
- Ensures that mobile developers can use standard Java APIs without writing platform-specific code.  

---

## 3. Application Code and Dependencies

Application-specific code represents the project or app being developed:  

- Can contain **Java and native code**.  
- May depend on external libraries or frameworks.  
- Is **project-specific** and built separately from the VM and JDK classes.  

---

## 4. Tooling

The **tooling** component ties everything together:  

- Bundles the VM, JDK classes, and application code efficiently.  
- Produces outputs ready for **mobile deployment** (e.g., Play Store, App Store) or **development integration** (e.g., Xcode, Android Studio).  
- Configurable to allow different use cases, from full apps to reusable Java libraries for mobile.  

---

This architecture ensures a **clear separation of concerns**, maintains alignment with upstream OpenJDK, and enables developers to work with standard Java on mobile platforms without compromise.

