---
title: "Basic Software Mode Manager (BswM)"
description: "Basic Software Mode Manager: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Basic Software Mode Manager component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `BswM` | Package directory |

## Key files

| Area | Files |
|---|---|
| `BswM` |  |
| C sources | `BswM.c` |
| Public headers | `BswM.h`, `BswM_CanSM.h`, `BswM_ComM.h`, `BswM_Dcm.h`, `BswM_EcuM.h`, `BswM_EthSM.h`, `BswM_FrSM.h`, `BswM_J1939Dcm.h`, `BswM_J1939Nm.h`, `BswM_LinSM.h`, `BswM_LinTp.h`, `BswM_Nm.h` (+4 more) |
| AUTOSAR model | `BswM_bswmd.arxml`, `BswM_preo.arxml` |
| Tooling and integration scripts | `BswM.gpj`, `CreateGHSProject.bat`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `BswM/autosar/BswM_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `BswM/src/BswM.c`. 

Top-level functions defined in `BswM.c` (factual extract, first 25):

- `BswM_ArbitrateRule`
- `BswM_ImmediateModeRequest`
- `BswM_Action_ActionListHandler`
- `BswM_InitMemory`
- `BswM_Init`
- `BswM_Deinit`
- `BswM_GetVersionInfo`
- `BswM_RequestMode`
- `BswM_RuleControl`
- `BswM_ComM_CurrentMode`
- `BswM_ComM_CurrentPNCMode`
- `BswM_Dcm_ApplicationUpdated`
- `BswM_Dcm_CommunicationMode_CurrentState`
- `BswM_CanSM_CurrentState`
- `BswM_EthSM_CurrentState`
- `BswM_FrSM_CurrentState`
- `BswM_J1939DcmBroadcastStatus`
- `BswM_J1939Nm_StateChangeNotification`
- `BswM_LinSM_CurrentSchedule`
- `BswM_LinSM_CurrentState`
- `BswM_LinSM_ScheduleEndNotification`
- `BswM_LinTp_RequestMode`
- `BswM_EcuM_CurrentState`
- `BswM_EcuM_CurrentWakeup`
- `BswM_EcuM_RequestedState`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_BswM.pdf`

- **Source path in repository:** `BswM/doc/TechnicalReference_BswM.pdf`
- **Format:** `.pdf`
- **Size:** `1862 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
