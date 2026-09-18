---
title: "Input Output Hardware Abstraction (IoHwAb)"
description: "Input Output Hardware Abstraction: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided, customised]
Vector MICROSAR module with project-specific configuration and custom code.
:::

## Purpose and responsibility

The Input Output Hardware Abstraction component belongs to **Hardware Abstraction Interfaces** in the **Electronic Control Unit Abstraction** layer. It abstracts the microcontroller hardware behind an AUTOSAR interface.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `IoHwAb` | Package directory |

## Key files

| Area | Files |
|---|---|
| `IoHwAb` |  |
| Public headers | `IoHwAb.h` |
| AUTOSAR model | `IoHwAb_bswmd.arxml`, `IoHwAb_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `IoHwAb.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `IoHwAb/autosar/IoHwAb_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_IoHwAb.pdf`

- **Source path in repository:** `IoHwAb/doc/TechnicalReference_IoHwAb.pdf`
- **Format:** `.pdf`
- **Size:** `1107 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Electronic Control Unit Abstraction](../).
