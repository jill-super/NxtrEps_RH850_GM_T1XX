---
title: "Nexteer Calibration Identifiers (NM004A_NxtrCalIds)"
description: "Nexteer Calibration Identifiers: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Nexteer Calibration Identifiers component belongs to **Manufacturing Services** in the **Application Software** layer. It provides manufacturing, programming or identification services used in production and service.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `NM004A_NxtrCalIds_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM004A_NxtrCalIds_Impl` |  |
| C sources | `NxtrCalIds.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NxtrCalIds.dcf`, `NxtrCalIds_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `NM004A_NxtrCalIds_Impl.gpj`, `NxtrCalIds.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `NM004A_NxtrCalIds_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `NM004A_NxtrCalIds_Impl/src/NxtrCalIds.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
