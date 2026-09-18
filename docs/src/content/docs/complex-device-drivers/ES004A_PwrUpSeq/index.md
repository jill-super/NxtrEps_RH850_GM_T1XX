---
title: "Power-Up Sequence (ES004A_PwrUpSeq)"
description: "Power-Up Sequence: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Power-Up Sequence component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES004A_PwrUpSeq_Design` | Design package |
| `ES004A_PwrUpSeq_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES004A_PwrUpSeq_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES004A_PwrUpSeq_Impl` |  |
| C sources | `PwrUpSeq.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `PwrUpSeq.dcf`, `PwrUpSeq_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES004A_PwrUpSeq_Impl.gpj`, `PwrUpSeq.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES004A_PwrUpSeq_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES004A_PwrUpSeq_Impl/src/PwrUpSeq.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES004A_PwrUpSeq_DDReport.txt`

- **Source path in repository:** `ES004A_PwrUpSeq_Design/Design/ES004A_PwrUpSeq_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES004A_PwrUpSeq_DataDict
05-Dec-2016 14:44:51
Tool Release:  2.51.0



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
(variables: 2, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
IoHwAb_SetGpioPwrTurnOffCtrl	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 1, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
CodFlsCrcChkCmpl            	Cannot match name to list of known Nexteer signals.
MotDrvr0IninTestCmpl        	Cannot match name to list of known Nexteer signals.
MotDrvr1IninTestCmpl        	Cannot match name to list of known Nexteer signals.
TmplMonIninTestCmpl         	Cannot match name to list of known Nexteer signals.
(variables: 8, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

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
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 1, errors: 0)
```
*... truncated (36 more lines in the source file). ...*

### `ES004A_PwrUpSeq_DDReport.txt`

- **Source path in repository:** `ES004A_PwrUpSeq_Design/Reports/ES004A_PwrUpSeq_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES004A_PwrUpSeq_DataDict
12-Jul-2016 09:07:34
Tool Release:  2.43.0



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
(variables: 2, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
CodFlsCrcChkCmpl            	Cannot match name to list of known Nexteer signals.
MotDrvr0IninTestCmpl        	Cannot match name to list of known Nexteer signals.
MotDrvr1IninTestCmpl        	Cannot match name to list of known Nexteer signals.
TmplMonIninTestCmpl         	Cannot match name to list of known Nexteer signals.
(variables: 8, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

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
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

```
*... truncated (35 more lines in the source file). ...*

### `PwrUpSeq_IntegrationManual.doc`

- **Source path in repository:** `ES004A_PwrUpSeq_Impl/doc/PwrUpSeq_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `PwrUpSeq_MDD.doc`

- **Source path in repository:** `ES004A_PwrUpSeq_Impl/doc/PwrUpSeq_MDD.doc`
- **Format:** `.doc`
- **Size:** `198 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
