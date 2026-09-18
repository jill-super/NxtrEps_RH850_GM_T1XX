---
title: "Non-Volatile Memory (NvM)"
description: "Non-Volatile Memory: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Non-Volatile Memory component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `NvM` | Package directory |

## Key files

| Area | Files |
|---|---|
| `NvM` |  |
| C sources | `NvM.c`, `NvM_Act.c`, `NvM_Crc.c`, `NvM_JobProc.c`, `NvM_Qry.c`, `NvM_Queue.c` |
| Public headers | `NvM.h`, `NvM_Act.h`, `NvM_Cbk.h`, `NvM_Crc.h`, `NvM_JobProc.h`, `NvM_Qry.h`, `NvM_Queue.h`, `NvM_Types.h` |
| AUTOSAR model | `NvM_bswmd.arxml`, `NvM_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `NvM.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `NvM/autosar/NvM_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 6 C source file(s), starting with `NvM/src/NvM.c`. 

Top-level functions defined in `NvM.c` (factual extract, first 22):

- `NvM_Init`
- `NvM_SetDataIndex`
- `NvM_GetDataIndex`
- `NvM_SetBlockProtection`
- `NvM_GetErrorStatus`
- `NvM_GetVersionInfo`
- `NvM_SetRamBlockStatus`
- `NvM_ReadBlock`
- `NvM_WriteBlock`
- `NvM_RestoreBlockDefaults`
- `NvM_EraseNvBlock`
- `NvM_InvalidateNvBlock`
- `NvM_CancelJobs`
- `NvM_ReadAll`
- `NvM_WriteAll`
- `NvM_CancelWriteAll`
- `NvM_KillWriteAll`
- `NvM_RepairRedundantBlocks`
- `NvM_MainFunction`
- `NvM_JobEndNotification`
- `NvM_JobErrorNotification`
- `NvM_SetBlockLockStatus`

Additional implementation units: `NvM/src/NvM_Act.c`, `NvM/src/NvM_Crc.c`, `NvM/src/NvM_JobProc.c`, `NvM/src/NvM_Qry.c`, `NvM/src/NvM_Queue.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_NvM.pdf`

- **Source path in repository:** `NvM/doc/TechnicalReference_NvM.pdf`
- **Format:** `.pdf`
- **Size:** `1808 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
