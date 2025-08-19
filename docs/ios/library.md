# Java Libraries for iOS

This track enables **Java libraries to be first-class components** in iOS projects, callable from Objective-C/Swift.

## Requirements

- **Explicit export model** – annotate or map Java methods/classes to be exposed to iOS.
- **Code generation** – auto-generate native glue (C/Objective-C headers, shims, registration code) packaged with the native library.
- **Runtime bridging** – native entry points that call the JVM embedding API, handle threading, and manage lifetimes.
- **Data marshaling rules** – primitives, strings, arrays, objects, callbacks, exceptions.
- **Packaging** – produce iOS deliverables (static library / xcframework + headers or Xcode module).

## Example

```
// Java
public class HelloLib {
    @ExportToNative("greet")
    public static String greet(String name) { return "Hello " + name; }
}

would result in

```
// Generated native header
const char* HelloLib_greet(const char* name);
```
Call from Objective-C/Swift like any native function.

## Acceptance Criteria
- Example Java library exposes several methods callable from Objective-C/Swift.

- Generated glue is reproducible and minimal.

- Unit tests cover marshaling, error mapping, and callbacks.
