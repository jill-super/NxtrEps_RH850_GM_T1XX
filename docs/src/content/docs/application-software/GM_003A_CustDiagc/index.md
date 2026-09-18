---
title: "General Motors 003 A Customer Diagnostics (GM_003A_CustDiagc)"
description: "General Motors 003 A Customer Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors 003 A Customer Diagnostics component belongs to **Platform Services** in the **Application Software** layer. It provides a platform-level service (communication machine, checkpoints, part numbers, diagnostics) to the application.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `GM_003A_CustDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `GM_003A_CustDiagc_Impl` |  |
| C sources | `CustDiagc.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CustDiagc.dcf`, `CustDiagc_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `CustDiagc.dpa`, `GM_003A_CustDiagc_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `GM_003A_CustDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `GM_003A_CustDiagc_Impl/src/CustDiagc.c`. 

Top-level functions defined in `CustDiagc.c` (factual extract, first 8):

- `NONTRUSTED_NtWrapS_CustDiagc_UpdHwAgTrimVal`
- `NONTRUSTED_NtWrapS_CustDiagc_ClrHwAgTrimVal`
- `NONTRUSTED_NtWrapS_CustDiagc_ClrAllDiagc`
- `NONTRUSTED_NtWrapS_CustDiagc_DemDcmDisableDTCSetting`
- `NONTRUSTED_NtWrapS_CustDiagc_DemDcmEnableDTCSetting`
- `NONTRUSTED_NtWrapS_CustDiagc_GmFctDiReq`
- `NONTRUSTED_NtWrapS_CustDiagc_EnaDtcRecUpd`
- `NONTRUSTED_NtWrapS_CustDiagc_DiDtcRecUpd`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
