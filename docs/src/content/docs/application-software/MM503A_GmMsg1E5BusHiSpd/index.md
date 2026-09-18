---
title: "General Motors Msg1 E5 Bus High Speed (MM503A_GmMsg1E5BusHiSpd)"
description: "General Motors Msg1 E5 Bus High Speed: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Msg1 E5 Bus High Speed component belongs to **Serial Communication Output Proxies** in the **Application Software** layer. It proxies application data into an outgoing serial-communication message via the RTE.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `MM503A_GmMsg1E5BusHiSpd_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `MM503A_GmMsg1E5BusHiSpd_Impl` |  |
| C sources | `GmMsg1E5BusHiSpd.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GM1E5HS_attr_def.xml`, `GmMsg1E5BusHiSpd.dcf`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmMsg1E5BusHiSpd.dpa`, `MM503A_GmMsg1E5BusHiSpd_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `MM503A_GmMsg1E5BusHiSpd_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `MM503A_GmMsg1E5BusHiSpd_Impl/src/GmMsg1E5BusHiSpd.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
