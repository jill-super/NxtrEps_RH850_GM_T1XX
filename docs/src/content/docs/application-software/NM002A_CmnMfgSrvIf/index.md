---
title: "Common Manufacturing Services Interface (NM002A_CmnMfgSrvIf)"
description: "Common Manufacturing Services Interface: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Common Manufacturing Services Interface component belongs to **Manufacturing Services** in the **Application Software** layer. It provides manufacturing, programming or identification services used in production and service.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `NM002A_CmnMfgSrvIf_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM002A_CmnMfgSrvIf_Impl` |  |
| C sources | `CmnMfgSrvIf.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CmnMfgSrvIf.dcf`, `CmnMfgSrv_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NxtrMfgSrvIf_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `NxtrMfgSrvIf_Cfg.h.tt`, `NxtrMfgSrvIf_Generate.bat` |
| Tooling and integration scripts | `CmnMfgSrvIf.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `NM002A_CmnMfgSrvIf_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `NM002A_CmnMfgSrvIf_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `NM002A_CmnMfgSrvIf_Impl/src/CmnMfgSrvIf.c`. 

Top-level functions defined in `CmnMfgSrvIf.c` (factual extract, first 5):

- `ApplTpRxGetBuffer`
- `ApplTpRxIndication`
- `ApplTpTxConfirmation`
- `ApplTpRxErrorIndication`
- `ApplTpTxErrorIndication`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
