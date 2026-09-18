---
title: "Electronic Control Unit State Manager (EcuM)"
description: "Electronic Control Unit State Manager: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Electronic Control Unit State Manager component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `EcuM` | Package directory |

## Key files

| Area | Files |
|---|---|
| `EcuM` |  |
| C sources | `EcuM.c` |
| Public headers | `EcuM.h`, `EcuM_Cbk.h`, `EcuM_Error.h` |
| AUTOSAR model | `EcuM_bswmd.arxml`, `EcuM_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `EcuM.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `EcuM/autosar/EcuM_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `EcuM/src/EcuM.c`. 

Top-level functions defined in `EcuM.c` (factual extract, first 25):

- `EcuM_SetState`
- `EcuM_KillAllRUNRequests`
- `EcuM_KillAllPostRUNRequests`
- `EcuM_MainFunction`
- `EcuM_Init`
- `EcuM_Shutdown`
- `EcuM_SelectShutdownTarget`
- `EcuM_GetShutdownTarget`
- `EcuM_GetLastShutdownTarget`
- `EcuM_SelectShutdownCause`
- `EcuM_GetPendingWakeupEvents`
- `EcuM_ClearWakeupEvent`
- `EcuM_ClearValidatedWakeupEvent`
- `EcuM_GetValidatedWakeupEvents`
- `EcuM_GetExpiredWakeupEvents`
- `EcuM_CB_NfyNvMJobEnd`
- `EcuM_GetStateWrapper`
- `EcuM_GetState`
- `EcuM_GetBootTarget`
- `EcuM_SelectBootTarget`
- `EcuM_StartupTwo`
- `EcuM_SetWakeupEvent`
- `EcuM_ValidateWakeupEvent`
- `EcuM_GoHalt`
- `EcuM_GoPoll`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_EcuM.pdf`

- **Source path in repository:** `EcuM/doc/TechnicalReference_EcuM.pdf`
- **Format:** `.pdf`
- **Size:** `2656 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
