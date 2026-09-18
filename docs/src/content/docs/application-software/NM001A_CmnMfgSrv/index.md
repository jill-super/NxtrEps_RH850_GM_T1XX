---
title: "Common Manufacturing Services (NM001A_CmnMfgSrv)"
description: "Common Manufacturing Services: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Common Manufacturing Services component belongs to **Manufacturing Services** in the **Application Software** layer. It provides manufacturing, programming or identification services used in production and service.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `NM001A_CmnMfgSrv_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM001A_CmnMfgSrv_Impl` |  |
| C sources | `CmnMfgSrv.c`, `CmnMfgSrvFct.c`, `SrvF000.c`, `SrvF001.c`, `SrvF002.c`, `SrvF010.c`, `SrvF100.c`, `SrvF101.c`, `SrvF110.c`, `SrvF111.c`, `SrvF112.c`, `SrvF113.c` (+13 more) |
| Public headers | `CmnMfgSrv.h`, `CmnMfgSrvFct.h`, `CmnMfgSrvTyp.h`, `CmnMfgSrv_NxtrMemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CmnMfgSrv.dcf`, `CmnMfgSrv_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NxtrMfgSrv_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `MfgSrvCfg.c.tt`, `MfgSrvCfg.h.tt`, `NxtrMfgSrv_Generate.bat` |
| Tooling and integration scripts | `CmnMfgSrv.dpa`, `CmnMfgSrvCfg.arxml`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `NM001A_CmnMfgSrv_Impl.gpj`, `OdxGen.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `NM001A_CmnMfgSrv_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 25 C source file(s), starting with `NM001A_CmnMfgSrv_Impl/src/CmnMfgSrv.c`. 

Top-level functions defined in `CmnMfgSrv.c` (factual extract, first 2):

- `NONTRUSTED_NtWrapS_CmnMfgSrv_Init`
- `NONTRUSTED_NtWrapS_CmnMfgSrv_DiAssi`

Additional implementation units: `NM001A_CmnMfgSrv_Impl/src/CmnMfgSrvFct.c`, `NM001A_CmnMfgSrv_Impl/src/SrvF000.c`, `NM001A_CmnMfgSrv_Impl/src/SrvF001.c`, `NM001A_CmnMfgSrv_Impl/src/SrvF002.c`, `NM001A_CmnMfgSrv_Impl/src/SrvF010.c` (and 19 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
