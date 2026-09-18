---
title: "Watchdog (Wdg)"
description: "Watchdog: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Watchdog component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Wdg` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Wdg` |  |
| C sources | `Wdg_59_DriverA.c`, `Wdg_59_DriverA_Irq.c`, `Wdg_59_DriverA_Private.c`, `Wdg_59_DriverA_Ram.c`, `Wdg_59_DriverA_Version.c` |
| Public headers | `Wdg_59_DriverA.h`, `Wdg_59_DriverA_Debug.h`, `Wdg_59_DriverA_Irq.h`, `Wdg_59_DriverA_PBTypes.h`, `Wdg_59_DriverA_Private.h`, `Wdg_59_DriverA_Ram.h`, `Wdg_59_DriverA_RegWrite.h`, `Wdg_59_DriverA_Types.h`, `Wdg_59_DriverA_Version.h` |
| AUTOSAR model | `R403_WDG_P1M_04_05_10_to_15_18_to_23.arxml`, `Wdg_bswmd_rec.arxml` |
| Generator output | `P1M.trxml`, `P1x_translation.h`, `R403_WDG_P1x_BSWMDT.arxml`, `RUCG.exe`, `Wdg_X1x.cfgxml`, `Wdg_X1x.dll`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h` (+8 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `Wdg.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `Wdg/autosar/R403_WDG_P1M_04_05_10_to_15_18_to_23.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 5 C source file(s), starting with `Wdg/src/Wdg_59_DriverA.c`. 

Top-level functions defined in `Wdg_59_DriverA.c` (factual extract, first 4):

- `Wdg_59_DriverA_Init`
- `Wdg_59_DriverA_SetMode`
- `Wdg_59_DriverA_SetTriggerCondition`
- `Wdg_59_DriverA_GetVersionInfo`

Additional implementation units: `Wdg/src/Wdg_59_DriverA_Irq.c`, `Wdg/src/Wdg_59_DriverA_Private.c`, `Wdg/src/Wdg_59_DriverA_Ram.c`, `Wdg/src/Wdg_59_DriverA_Version.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `R20UT3728EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Wdg/doc/R20UT3728EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `942 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3729EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Wdg/doc/R20UT3729EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `550 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3754EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Wdg/doc/R20UT3754EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `435 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
