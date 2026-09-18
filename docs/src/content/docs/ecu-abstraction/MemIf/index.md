---
title: "Memory Abstraction Interface (MemIf)"
description: "Memory Abstraction Interface: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Memory Abstraction Interface component belongs to **Hardware Abstraction Interfaces** in the **Electronic Control Unit Abstraction** layer. It abstracts the microcontroller hardware behind an AUTOSAR interface.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `MemIf` | Package directory |

## Key files

| Area | Files |
|---|---|
| `MemIf` |  |
| C sources | `MemIf.c` |
| Public headers | `MemIf.h`, `MemIf_Types.h` |
| AUTOSAR model | `MemIf_bswmd.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `MemIf.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (1 file(s), e.g. `MemIf/autosar/MemIf_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `MemIf/src/MemIf.c`. 

Top-level functions defined in `MemIf.c` (factual extract, first 6):

- `MemIf_Read`
- `MemIf_Write`
- `MemIf_InvalidateBlock`
- `MemIf_EraseImmediateBlock`
- `MemIf_GetJobResult`
- `MemIf_SetMode`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_MemIf.pdf`

- **Source path in repository:** `MemIf/doc/TechnicalReference_MemIf.pdf`
- **Format:** `.pdf`
- **Size:** `730 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Electronic Control Unit Abstraction](../).
