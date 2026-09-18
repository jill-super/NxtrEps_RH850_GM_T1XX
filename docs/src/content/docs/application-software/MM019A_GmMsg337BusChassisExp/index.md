---
title: "General Motors Msg337 Bus Chassis Expansion (MM019A_GmMsg337BusChassisExp)"
description: "General Motors Msg337 Bus Chassis Expansion: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Msg337 Bus Chassis Expansion component belongs to **Serial Communication Input Proxies** in the **Application Software** layer. It proxies an incoming serial-communication message into RTE ports for the application software.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `MM019A_GmMsg337BusChassisExp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `MM019A_GmMsg337BusChassisExp_Impl` |  |
| C sources | `GmMsg337BusChassisExp.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmMsg337BusChassisExp.dcf`, `GmMsg337BusChassisExp_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmMsg337BusChassisExp.dpa`, `MM019A_GmMsg337BusChassisExp_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `MM019A_GmMsg337BusChassisExp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `MM019A_GmMsg337BusChassisExp_Impl/src/GmMsg337BusChassisExp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
