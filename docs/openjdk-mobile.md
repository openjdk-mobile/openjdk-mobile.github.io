# OpenJDK Mobile

The [OpenJDK/mobile](https://github.com/openjdk/mobile) repository is an official downstream project of OpenJDK/jdk. It currently contains a small set of iOS- and Android-specific patches required to build a JVM and class libraries that run on mobile devices.

## Project Goal

The ultimate goal is to make OpenJDK/mobile obsolete by upstreaming mobile-specific patches into **OpenJDK/jdk**. This ensures:

- Mobile support is integrated directly in the standard JDK.
- No long-term maintenance is required for a separate downstream repository.
- Consistency and quality are preserved across all platforms.

## Constraints

Upstreaming patches requires a very high-quality bar:

- Patches must **not introduce regressions** on other platforms.
- Patches must **not increase maintenance burden** for OpenJDK developers.
- Only patches with **clear benefits and no negative impact** will be proposed for upstreaming.

While it is technically "easier" to apply patches in OpenJDK/mobile than in upstream OpenJDK/jdk, this does **not** mean that anything goes. The quality bar for OpenJDK/mobile is still high, because only well-tested and maintainable patches can eventually be upstreamed.
Each patch is carefully evaluated for correctness, maintainability, and long-term sustainability.
