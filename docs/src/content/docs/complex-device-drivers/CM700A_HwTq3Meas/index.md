---
title: "Handwheel Tq3 Measurement (CM700A_HwTq3Meas)"
description: "Handwheel Tq3 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Tq3 Measurement component belongs to **Serial Interfaces and Position Sensing** in the **Complex Device Drivers** layer. It configures serial peripherals or measures rotor, handwheel-torque and handwheel-angle sensors.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM700A_HwTq3Meas_Design` | Design package |
| `CM700A_HwTq3Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM700A_HwTq3Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM700A_HwTq3Meas_Impl` |  |
| C sources | `CDD_HwTq3Meas.c` |
| Public headers | `CDD_HwTq3Meas.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwTq3Meas.dcf`, `HwTq3Meas_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM700A_HwTq3Meas_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwTq3Meas.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM700A_HwTq3Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM700A_HwTq3Meas_Impl/src/CDD_HwTq3Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM700A_HwTq3Meas_DDReport.txt`

- **Source path in repository:** `CM700A_HwTq3Meas_Design/Reports/CM700A_HwTq3Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM700A_HwTq3Meas_DataDict
21-Mar-2016 17:49:53
Tool Release:  2.35.0



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
HwTq3MeasHwTq3AutTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq3MeasHwTq3ClrTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq3MeasHwTq3ReadTrim      	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq3MeasHwTq3TrimPrfmdSts  	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq3MeasHwTq3WrTrim        	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwTq3MeasTrigStrt           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 6, errors: 6)

-----------------------
Client:	<TriggerName>
-------------------------
IoHwAb_SetFctPrphlHwTq3     	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 6, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwTq3Phy                    	Cannot match name to list of known Nexteer signals.
HwTq3Phy                    	.ReadIn:	Field is empty.
(variables: 8, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
GearIdn2                    	Cannot match name to list of known Nexteer signals.
GearIdn2Vld                 	Cannot match name to list of known Nexteer signals.
RegOutRSENT5CSC             	Cannot match name to list of known Nexteer signals.
RegOutRSENT5NRC             	Cannot match name to list of known Nexteer signals.
RegOutRSENT5SPCT            	Cannot match name to list of known Nexteer signals.
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
*... truncated (52 more lines in the source file). ...*

### `HwTq3Meas_IntegrationManual.doc`

- **Source path in repository:** `CM700A_HwTq3Meas_Impl/doc/HwTq3Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `156 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwTq3Meas_MDD.doc`

- **Source path in repository:** `CM700A_HwTq3Meas_Impl/doc/HwTq3Meas_MDD.doc`
- **Format:** `.doc`
- **Size:** `198 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
