---
title: "Serial Communication Output Proxy (MM500A_SerlComOutpProxy)"
description: "Serial Communication Output Proxy: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Serial Communication Output Proxy component belongs to **Serial Communication Output Proxies** in the **Application Software** layer. It proxies application data into an outgoing serial-communication message via the RTE.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `MM500A_SerlComOutpProxy_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `MM500A_SerlComOutpProxy_Impl` |  |
| C sources | `SerlComOutpProxy.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SerlComOutpProxy.dcf`, `SerlComOutpProxy_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MM500A_SerlComOutpProxy_Impl.gpj`, `RteGen.bat`, `SerlComOutpProxy.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `MM500A_SerlComOutpProxy_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `MM500A_SerlComOutpProxy_Impl/src/SerlComOutpProxy.c`. 

Top-level functions defined in `SerlComOutpProxy.c` (factual extract, first 6):

- `ApplNwmBusoff`
- `SerlComOutpProxy_184CfmFct`
- `SerlComOutpProxy_1CACfmFct`
- `SerlComOutpProxy_1E5HiSpdCfmFct`
- `SerlComOutpProxy_1E5ChassisExpCfmFct`
- `SerlComOutpProxy_335CfmFct`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
