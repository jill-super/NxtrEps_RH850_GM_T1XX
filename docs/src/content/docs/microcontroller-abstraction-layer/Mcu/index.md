---
title: "Microcontroller Unit (Mcu)"
description: "Microcontroller Unit: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Microcontroller Unit component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Mcu` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Mcu` |  |
| C sources | `Mcu.c`, `Mcu_Irq.c`, `Mcu_Ram.c`, `Mcu_Version.c`, `NxtrMcuIrqPatch.c` |
| Public headers | `Mcu.h`, `Mcu_Debug.h`, `Mcu_Irq.h`, `Mcu_PBTypes.h`, `Mcu_Ram.h`, `Mcu_RegWrite.h`, `Mcu_Types.h`, `Mcu_Version.h` |
| AUTOSAR model | `Mcu_bswmd_rec.arxml`, `R403_MCU_P1M_04_05.arxml`, `R403_MCU_P1M_10_to_15_18_to_23.arxml` |
| Generator output | `Mcu_P1x.cfgxml`, `Mcu_P1x.dll`, `P1M.trxml`, `P1x_translation.h`, `R403_MCU_P1x_BSWMDT.arxml`, `RUCG.exe`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h` (+8 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `Mcu.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `Mcu/autosar/Mcu_bswmd_rec.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 5 C source file(s), starting with `Mcu/src/Mcu.c`. 

Top-level functions defined in `Mcu.c` (factual extract, first 13):

- `Mcu_Init`
- `Mcu_InitRamSection`
- `Mcu_InitClock`
- `Mcu_DistributePllClock`
- `Mcu_GetPllStatus`
- `Mcu_GetResetReason`
- `Mcu_GetResetRawValue`
- `FUNC`
- `Mcu_SetMode`
- `Mcu_GetRamState`
- `Mcu_GetVersionInfo`
- `Mcu_EcmReleaseErrorOutPin`
- `Mcu_LockStepSelfDiagnosticTest`

Additional implementation units: `Mcu/src/Mcu_Irq.c`, `Mcu/src/Mcu_Ram.c`, `Mcu/src/Mcu_Version.c`, `Mcu/src/NxtrMcuIrqPatch.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

4 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `Mcu Integration Manual.doc`

- **Source path in repository:** `Mcu/doc/Mcu Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `130 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3720EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Mcu/doc/R20UT3720EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `1105 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3721EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Mcu/doc/R20UT3721EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `588 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3754EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Mcu/doc/R20UT3754EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `435 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
