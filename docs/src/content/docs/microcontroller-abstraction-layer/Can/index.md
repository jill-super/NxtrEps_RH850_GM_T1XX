---
title: "Controller Area Network (Can)"
description: "Controller Area Network: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Controller Area Network component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Can` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Can` |  |
| C sources | `can_drv.c` |
| Public headers | `can_def.h` |
| Tooling and integration scripts | `Can.gpj`, `CreateGHSProject.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `Can/src/can_drv.c`. 

Top-level functions defined in `can_drv.c` (factual extract, first 3):

- `V_DEF_FUNC_API`
- `V_DEF_FUNC`
- `ISR`

## Dependencies and configuration

- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_CANDriver.pdf`

- **Source path in repository:** `Can/doc/TechnicalReference_CANDriver.pdf`
- **Format:** `.pdf`
- **Size:** `1139 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Rh850_Rscan.pdf`

- **Source path in repository:** `Can/doc/TechnicalReference_Rh850_Rscan.pdf`
- **Format:** `.pdf`
- **Size:** `1055 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `UserManual_CanDriver.pdf`

- **Source path in repository:** `Can/doc/UserManual_CanDriver.pdf`
- **Format:** `.pdf`
- **Size:** `697 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
