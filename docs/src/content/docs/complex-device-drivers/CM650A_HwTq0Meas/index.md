---
title: "Handwheel Tq0 Measurement (CM650A_HwTq0Meas)"
description: "Handwheel Tq0 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Tq0 Measurement component belongs to **Serial Interfaces and Position Sensing** in the **Complex Device Drivers** layer. It configures serial peripherals or measures rotor, handwheel-torque and handwheel-angle sensors.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM650A_HwTq0Meas_Design` | Design package |
| `CM650A_HwTq0Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM650A_HwTq0Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM650A_HwTq0Meas_Impl` |  |
| C sources | `CDD_HwTq0Meas.c` |
| Public headers | `CDD_HwTq0Meas.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwTq0Meas.dcf`, `HwTq0Meas_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM650A_HwTq0Meas_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwTq0Meas.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM650A_HwTq0Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM650A_HwTq0Meas_Impl/src/CDD_HwTq0Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM650A_HwTq0Meas_DDReport.txt`

- **Source path in repository:** `CM650A_HwTq0Meas_Design/Reports/CM650A_HwTq0Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM650A_HwTq0Meas_DataDict
24-Mar-2016 15:51:00
Tool Release:  2.34.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

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
HwTq0MeasHwTq0AutTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq0MeasHwTq0ClrTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq0MeasHwTq0ReadTrim      	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq0MeasHwTq0TrimPrfmdSts  	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq0MeasHwTq0WrTrim        	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq0MeasTrigStrt           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 6, errors: 6)

-----------------------
Client:	<TriggerName>
-------------------------
IoHwAb_SetFctPrphlHwTq0     	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 8, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwTq0Phy                    	Cannot match name to list of known Nexteer signals.
HwTq0Phy                    	.ReadIn:	Field is empty.
(variables: 8, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
RackLimrCcwEotSig0          	Cannot match name to list of known Nexteer signals.
RackLimrCwEotSig0           	Cannot match name to list of known Nexteer signals.
RackLimrEotSig0Avl          	Cannot match name to list of known Nexteer signals.
RegOutRSENT0NRC             	Cannot match name to list of known Nexteer signals.
RegOutRSENT0SPCT            	Cannot match name to list of known Nexteer signals.
(variables: 8, errors: 5)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 2, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 1, errors: 0)

```
*... truncated (53 more lines in the source file). ...*

### `HwTq0Meas_IntegrationManual.doc`

- **Source path in repository:** `CM650A_HwTq0Meas_Impl/doc/HwTq0Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwTq0Meas_MDD.doc`

- **Source path in repository:** `CM650A_HwTq0Meas_Impl/doc/HwTq0Meas_MDD.doc`
- **Format:** `.doc`
- **Size:** `228 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
