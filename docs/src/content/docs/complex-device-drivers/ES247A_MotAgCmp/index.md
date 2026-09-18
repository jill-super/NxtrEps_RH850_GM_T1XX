---
title: "Motor Angle Comparison (ES247A_MotAgCmp)"
description: "Motor Angle Comparison: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Angle Comparison component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES247A_MotAgCmp_Design` | Design package |
| `ES247A_MotAgCmp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES247A_MotAgCmp_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES247A_MotAgCmp_Impl` |  |
| C sources | `CDD_MotAgCmp.c`, `CDD_MotAgCmp_MotCtrl.c` |
| Public headers | `CDD_MotAgCmp.h`, `CDD_MotAgCmp_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotAgCmp.dcf`, `MotAgCmp_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES247A_MotAgCmp_Impl.gpj`, `MotAgCmp.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES247A_MotAgCmp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES247A_MotAgCmp_Impl/src/CDD_MotAgCmp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES247A_MotAgCmp_Impl/src/CDD_MotAgCmp_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES247A_MotAgCmp_DDReport.txt`

- **Source path in repository:** `ES247A_MotAgCmp_Design/Reports/ES247A_MotAgCmp_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES247A_MotAgCmp_DataDict
10-Nov-2016 09:28:02
Tool Release:  2.47.0



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
MotAgCmpBackEmfRead         	.SrvRunnnable:	Name should not contain FDDs <ShoName>
MotAgCmpBackEmfWr           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 2, errors: 2)

-----------------------
Client:	<TriggerName>
-------------------------
MotAgCmpMotAgBackEmf_SetRamBlockStatus	.Client:	Name should not contain FDDs <ShoName>
(variables: 1, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotAgCumvAlgndMrfRev        	Cannot match name to list of known Nexteer signals.
MotAgCumvInid               	Cannot match name to list of known Nexteer signals.
(variables: 4, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotAgCumvAlgndVld           	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgCumvInid        	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 2)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 0, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 2, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
MotAgCmpMotAgBackEmf        	Name does not match required pattern.
(variables: 1, errors: 1)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
```
*... truncated (49 more lines in the source file). ...*

### `MotAgCmp_IntegrationManual.doc`

- **Source path in repository:** `ES247A_MotAgCmp_Impl/doc/MotAgCmp_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotAgCmp_MDD.doc`

- **Source path in repository:** `ES247A_MotAgCmp_Impl/doc/MotAgCmp_MDD.doc`
- **Format:** `.doc`
- **Size:** `176 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
