---
title: Vector-Provided Code versus In-House Code
description: How to tell third-party Vector modules apart from in-house developed components.
---

Every module page carries an origin badge. Five origins are used:

| Origin badge | Meaning | Examples |
|---|---|---|
| `Vector-provided` | Third-party MICROSAR module supplied by Vector Informatik; used as delivered plus generated configuration | Controller Area Network driver, Operating System, Non-Volatile Memory, Diagnostic Event Manager |
| `Vector-provided, customised` | Vector module with project-specific customisation | Input Output Hardware Abstraction, Runtime Environment configuration, Electronic Control Unit Configuration |
| `In-house (custom)` | Developed in-house; implementation, design and tests live in this repository | All steering functions, customer functions, complex device drivers, message proxies |
| `Third-party (Renesas)` | Supplied by the microcontroller vendor | Renesas microcontroller support package |
| `Joint integration (Vector + in-house)` | Top-level project wiring Vector and in-house parts together | The top-level integration project |

## How the origin was determined

1. **Copyright and license headers** in C sources and headers (`Vector Informatik GmbH` versus in-house headers).
2. **Generator banners** (`MICROSAR RTE Generator`, `GENy`, `DaVinci`) marking generated files.
3. **Directory role**: `autosar/` model files plus `tools/Integrate.bat` integration scripts are typical of configured Vector modules; `Design/` functional documents plus `src/` hand code are typical of in-house components.

> Generated files (anything under `generate/` output folders, `GenData` artefacts,
> DaVinci/GENy output) must not be edited by hand; regenerate them with the
> tool noted on the module page instead.
