---
title: "Programming Manufacturing Services (NM010A_ProgMfgSrv)"
description: "Programming Manufacturing Services: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Programming Manufacturing Services component belongs to **Manufacturing Services** in the **Application Software** layer. It provides manufacturing, programming or identification services used in production and service.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `NM010A_ProgMfgSrv_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM010A_ProgMfgSrv_Impl` |  |
| C sources | `ProgMfgSrv.c`, `SrvFED0.c`, `SrvFED1.c`, `SrvFED2.c`, `SrvFED3.c`, `SrvFED4.c`, `SrvFED5.c`, `SrvFED6.c`, `SrvFED7.c`, `SrvFED8.c`, `SrvFED9.c`, `SrvFEDA.c` (+5 more) |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `ProgMfgSrv.dcf`, `ProgMfgSrv_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `NM010A_ProgMfgSrv_Impl.gpj`, `OdxGen.bat`, `ProgMfgSrv.dpa`, `ProgMfgSrvCfg.arxml`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `NM010A_ProgMfgSrv_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 17 C source file(s), starting with `NM010A_ProgMfgSrv_Impl/src/ProgMfgSrv.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `NM010A_ProgMfgSrv_Impl/src/SrvFED0.c`, `NM010A_ProgMfgSrv_Impl/src/SrvFED1.c`, `NM010A_ProgMfgSrv_Impl/src/SrvFED2.c`, `NM010A_ProgMfgSrv_Impl/src/SrvFED3.c`, `NM010A_ProgMfgSrv_Impl/src/SrvFED4.c` (and 11 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
