---
title: "Diagnostic Event Manager (Dem)"
description: "Diagnostic Event Manager: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Diagnostic Event Manager component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Dem` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Dem` |  |
| C sources | `Dem.c` |
| Public headers | `Dem.h`, `Dem_Cbk.h`, `Dem_Cdd_Types.h`, `Dem_Cfg_Declarations.h`, `Dem_Cfg_Definitions.h`, `Dem_Cfg_Macros.h`, `Dem_Cfg_Types.h`, `Dem_Dcm.h`, `Dem_Types.h`, `Dem_Validation.h` |
| AUTOSAR model | `Dem_Pre.arxml`, `Dem_bswmd.arxml`, `Dem_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Dem.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `Dem/autosar/Dem_Pre.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `Dem/src/Dem.c`. 

Top-level functions defined in `Dem.c` (factual extract, first 25):

- `Dem_Mem_GetDebounceStatus`
- `Dem_Mem_SetDebounceStatus`
- `Dem_Mem_TestDebounceDirection`
- `Dem_Mem_GetStoredStatus`
- `Dem_Mem_SetStoredStatus`
- `Dem_Mem_TestEventSuppressedStatus`
- `Dem_Mem_SetEventSuppressedStatus`
- `Dem_Mem_ResetEventSuppressedStatus`
- `Dem_Mem_TestDtcSuppressedStatus`
- `Dem_Mem_SetDtcSuppressedStatus`
- `Dem_Mem_ResetDtcSuppressedStatus`
- `Dem_Mem_TestEventDisconnectedStatus`
- `Dem_Mem_SetEventDisconnectedStatus`
- `Dem_Mem_ResetEventDisconnectedStatus`
- `Dem_Mem_TestFdcTripStatus`
- `Dem_Mem_SetFdcTripStatus`
- `Dem_Mem_ResetFdcTripStatus`
- `Dem_Mem_TestFdcMaxStatus`
- `Dem_Mem_SetFdcMaxStatus`
- `Dem_Mem_ResetFdcMaxStatus`
- `Dem_Mem_TestFdcTocStatus`
- `Dem_Mem_SetFdcTocStatus`
- `Dem_Mem_ResetFdcTocStatus`
- `Dem_Mem_TestAvailableInVariantStatus`
- `Dem_Mem_SetAvailableInVariantStatus`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_Dem.pdf`

- **Source path in repository:** `Dem/doc/TechnicalReference_Dem.pdf`
- **Format:** `.pdf`
- **Size:** `1817 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
