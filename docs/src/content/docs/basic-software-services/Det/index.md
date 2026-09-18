---
title: "Development Error Tracer (Det)"
description: "Development Error Tracer: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Development Error Tracer component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Det` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Det` |  |
| C sources | `Det.c` |
| Public headers | `Det.h` |
| AUTOSAR model | `Det_bswmd.arxml`, `Det_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Det.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `Det/autosar/Det_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `Det/src/Det.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- References the Vector GENy configuration tool.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_Det.pdf`

- **Source path in repository:** `Det/doc/TechnicalReference_Det.pdf`
- **Format:** `.pdf`
- **Size:** `806 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
