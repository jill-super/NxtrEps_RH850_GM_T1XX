---
title: Build System and Toolchain
description: Compilers, projects, generators and host tools used to build the firmware.
---

## Target and compiler

- **Target microcontroller**: Renesas RH850 family (see the
  [top-level integration project](/integration/GM_T1XX_EPS_RH850/)).
- **Compiler toolchain**: Green Hills Software MULTI (per-module `*.gpj`
  project files and `CreateGHSProject.bat` scripts, e.g. in the
  [Microcontroller Unit driver](/microcontroller-abstraction-layer/Mcu/) and
  [Operating System](/operating-system-and-runtime/Os/) modules).
- **Make fragments**: `renesas_mcu_*.mak` definition/check/rule files
  (see the Microcontroller Unit driver module).

## Configuration and generation workflow

1. **Model the software** — AUTOSAR XML (`autosar/*.arxml`, DaVinci
   `*.dcf`) edited in [DaVinci Configurator](/tools-and-support/TL102A_Davinci/).
2. **Generate** — Runtime Environment and Basic Software configuration via the
   [Runtime Environment generator](/tools-and-support/TL101A_CptRteGen/),
   [GENy framework](/tools-and-support/TL104A_GENyFramework/) and the
   [AUTOSAR template tool](/tools-and-support/TL105A_Artt/).
3. **Integrate** — each module ships `tools/Integrate.bat` plus an
   `IntegrationCopy` list consumed by the top-level integration project.
4. **Compile and link** — Green Hills projects assembled by the
   [top-level integration project](/integration/GM_T1XX_EPS_RH850/).
5. **Verify** — [Quality Assurance for C](/tools-and-support/TL100A_QACSuprt/)
   and [Polyspace](/tools-and-support/TL108A_PolyspaceSuprt/) static analysis,
   [common checks](/tools-and-support/TL111A_CmnChksTool/), and the
   [coupling support](/tools-and-support/TL103A_CplrSuprt/) tooling.

## Host prerequisites

- Green Hills MULTI toolchain for RH850.
- Vector DaVinci Configurator and GENy (see [Tools and Support](/tools-and-support/)).
- Python tooling (see the [Python tools](/tools-and-support/TL112A_Python/) package).
- Quality Assurance for C and Polyspace for static analysis.
