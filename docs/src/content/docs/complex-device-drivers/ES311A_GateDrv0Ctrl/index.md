---
title: "Gate Drv0 Control (ES311A_GateDrv0Ctrl)"
description: "Gate Drv0 Control: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Gate Drv0 Control component belongs to **Motor Drive and Voltage Generation** in the **Complex Device Drivers** layer. It drives the power stage of the electric motor (gate drivers, voltage generation, drive diagnostics).

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES311A_GateDrv0Ctrl_Design` | Design package |
| `ES311A_GateDrv0Ctrl_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES311A_GateDrv0Ctrl_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES311A_GateDrv0Ctrl_Impl` |  |
| C sources | `GateDrv0Ctrl.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GateDrv0Ctrl.dcf`, `GateDrv0Ctrl_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES311A_GateDrv0Ctrl_Impl.gpj`, `GateDrv0Ctrl.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES311A_GateDrv0Ctrl_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES311A_GateDrv0Ctrl_Impl/src/GateDrv0Ctrl.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES311A_GateDrv0Ctrl_DDReport.txt`

- **Source path in repository:** `ES311A_GateDrv0Ctrl_Design/Reports/ES311A_GateDrv0Ctrl_DDReport.txt`
- **Format:** `.txt`
- **Size:** `14 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES311A_GateDrv0Ctrl_DataDict
16-Jan-2017 14:54:47
Tool Release:  2.51.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: IpSignal.ReadIn property should be a group of Runnables. Ex: {'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
[Warning: OpSignal.WrittenIn property should be a group of Runnables. Ex:
{'MotVelPer1','MotVelPer2'}.] 
(errors: 15)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF099A
--------------------------------------------------------------
(variable: 1, errors: 0)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
(errors:  0)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 3, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
Call_Spi_AsyncTransmit      	Name does not match required pattern.
Call_Spi_AsyncTransmit      	    Call_          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Transmit       Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_GetGpioMotDrvr0Diag  	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioGateDrv0Rst   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioSysFlt2A      	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Write          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 7, errors: 12)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
PhaALowrCmd                 	Cannot match name to list of known Nexteer signals.
PhaALowrCmd                 	.ReadIn:	Field is empty.
PhaAUpprCmd                 	Cannot match name to list of known Nexteer signals.
PhaAUpprCmd                 	.ReadIn:	Field is empty.
PhaBLowrCmd                 	Cannot match name to list of known Nexteer signals.
```
*... truncated (177 more lines in the source file). ...*

### `GateDrv0Ctrl_IntegrationManual.doc`

- **Source path in repository:** `ES311A_GateDrv0Ctrl_Impl/doc/GateDrv0Ctrl_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GateDrv0Ctrl_MDD.doc`

- **Source path in repository:** `ES311A_GateDrv0Ctrl_Impl/doc/GateDrv0Ctrl_MDD.doc`
- **Format:** `.doc`
- **Size:** `205 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
