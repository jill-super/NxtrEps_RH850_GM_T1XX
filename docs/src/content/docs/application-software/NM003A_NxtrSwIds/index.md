---
title: "Nexteer Software Identifiers (NM003A_NxtrSwIds)"
description: "Nexteer Software Identifiers: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Nexteer Software Identifiers component belongs to **Manufacturing Services** in the **Application Software** layer. It provides manufacturing, programming or identification services used in production and service.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `NM003A_NxtrSwIds_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM003A_NxtrSwIds_Impl` |  |
| C sources | `NxtrSwIds.c` |
| Public headers | `NxtrSwIds.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NxtrSwIds.dcf`, `NxtrSwIds_attr_def.xml`, `NxtrSwIds_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `NxtrSwIdsCfg.c.tt`, `NxtrSwIds_Generate.bat` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `NM003A_NxtrSwIds_Impl.gpj`, `NxtrSwIds.dpa`, `RteGen.bat`, `UpdateNxtrSwIds.py` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `NM003A_NxtrSwIds_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `NM003A_NxtrSwIds_Impl/src/NxtrSwIds.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
