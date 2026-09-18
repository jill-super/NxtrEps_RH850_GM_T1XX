---
title: "Digital Input Output (Dio)"
description: "Digital Input Output: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Digital Input Output component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Dio` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Dio` |  |
| C sources | `Dio.c`, `Dio_Ram.c`, `Dio_Version.c` |
| Public headers | `Dio.h`, `Dio_Debug.h`, `Dio_PBTypes.h`, `Dio_Ram.h`, `Dio_RegWrite.h`, `Dio_Version.h` |
| AUTOSAR model | `Dio_bswmd_rec.arxml`, `R403_DIO_P1M_04_05_12_13_20_21.arxml`, `R403_DIO_P1M_10_11_14_15_18_19_22_23.arxml` |
| Generator output | `Dio_X1x.cfgxml`, `Dio_X1x.dll`, `P1M.trxml`, `P1x_translation.h`, `R403_DIO_P1x_BSWMDT.arxml`, `RUCG.exe`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h` (+8 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Dio.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `Dio/autosar/Dio_bswmd_rec.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `Dio/src/Dio.c`. 

Top-level functions defined in `Dio.c` (factual extract, first 9):

- `Dio_Init`
- `Dio_WritePort`
- `Dio_ReadChannel`
- `Dio_WriteChannel`
- `Dio_FlipChannel`
- `Dio_ReadChannelGroup`
- `Dio_WriteChannelGroup`
- `Dio_MaskedWritePort`
- `Dio_GetVersionInfo`

Additional implementation units: `Dio/src/Dio_Ram.c`, `Dio/src/Dio_Version.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `R20UT3708EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Dio/doc/R20UT3708EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `773 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3709EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Dio/doc/R20UT3709EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `380 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3754EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Dio/doc/R20UT3754EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `435 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
