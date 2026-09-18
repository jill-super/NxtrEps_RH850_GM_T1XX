---
title: "Cyclic Redundancy Check (Crc)"
description: "Cyclic Redundancy Check: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Cyclic Redundancy Check component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Crc` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Crc` |  |
| C sources | `Crc.c` |
| Public headers | `Crc.h` |
| AUTOSAR model | `Crc_bswmd.arxml` |
| Tooling and integration scripts | `Crc.gpj`, `CreateGHSProject.bat`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (1 file(s), e.g. `Crc/autosar/Crc_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `Crc/src/Crc.c`. 

Top-level functions defined in `Crc.c` (factual extract, first 6):

- `Crc_CalculateCRC8`
- `Crc_CalculateCRC8H2F`
- `Crc_CalculateCRC16`
- `Crc_CalculateCRC32`
- `Crc_CalculateCRC32P4`
- `Crc_GetVersionInfo`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_Crc.pdf`

- **Source path in repository:** `Crc/doc/TechnicalReference_Crc.pdf`
- **Format:** `.pdf`
- **Size:** `630 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Libraries](../).
