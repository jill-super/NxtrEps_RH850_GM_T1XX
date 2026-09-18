---
title: "Port (Port)"
description: "Port: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Port component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Port` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Port` |  |
| C sources | `Port.c`, `Port_Ram.c`, `Port_Version.c` |
| Public headers | `Port.h`, `Port_Debug.h`, `Port_PBTypes.h`, `Port_Ram.h`, `Port_RegWrite.h`, `Port_Types.h`, `Port_Version.h` |
| AUTOSAR model | `Port_bswmd_rec.arxml`, `R403_PORT_P1M_04_05.arxml`, `R403_PORT_P1M_10_11_14_15.arxml`, `R403_PORT_P1M_12_13.arxml`, `R403_PORT_P1M_18_19_22_23.arxml`, `R403_PORT_P1M_20_21.arxml` |
| Generator output | `P1M.trxml`, `P1x_translation.h`, `Port_X1x.cfgxml`, `Port_X1x.dll`, `R403_PORT_P1x_BSWMDT.arxml`, `RUCG.exe`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h` (+8 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `Port.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (6 file(s), e.g. `Port/autosar/Port_bswmd_rec.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `Port/src/Port.c`. 

Top-level functions defined in `Port.c` (factual extract, first 5):

- `Port_SearchDioAltModePin`
- `FUNC`
- `Port_SearchModeChangeablePin`
- `Port_SearchDirChangeablePin`
- `Port_GetVersionInfo`

Additional implementation units: `Port/src/Port_Ram.c`, `Port/src/Port_Version.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `R20UT3722EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Port/doc/R20UT3722EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `789 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3723EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Port/doc/R20UT3723EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `475 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `R20UT3754EJ0100-AUTOSAR.pdf`

- **Source path in repository:** `Port/doc/R20UT3754EJ0100-AUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `435 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
