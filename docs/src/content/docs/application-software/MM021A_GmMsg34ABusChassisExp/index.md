---
title: "General Motors Msg34 A Bus Chassis Expansion (MM021A_GmMsg34ABusChassisExp)"
description: "General Motors Msg34 A Bus Chassis Expansion: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Msg34 A Bus Chassis Expansion component belongs to **Serial Communication Input Proxies** in the **Application Software** layer. It proxies an incoming serial-communication message into RTE ports for the application software.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `MM021A_GmMsg34ABusChassisExp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `MM021A_GmMsg34ABusChassisExp_Impl` |  |
| C sources | `GmMsg34ABusChassisExp.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GM34ACE_attr_def.xml`, `GmMsg34ABusChassisExp.dcf`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmMsg34ABusChassisExp.dpa`, `MM021A_GmMsg34ABusChassisExp_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `MM021A_GmMsg34ABusChassisExp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `MM021A_GmMsg34ABusChassisExp_Impl/src/GmMsg34ABusChassisExp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
