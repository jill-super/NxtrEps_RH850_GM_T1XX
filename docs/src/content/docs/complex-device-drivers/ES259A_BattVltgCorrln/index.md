---
title: "Battery Voltage Correlation (ES259A_BattVltgCorrln)"
description: "Battery Voltage Correlation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Battery Voltage Correlation component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES259A_BattVltgCorrln_Design` | Design package |
| `ES259A_BattVltgCorrln_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES259A_BattVltgCorrln_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES259A_BattVltgCorrln_Impl` |  |
| C sources | `BattVltgCorrln.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `BattVltgCorrln.dcf`, `BattVltgCorrln_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `BattVltgCorrln.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES259A_BattVltgCorrln_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES259A_BattVltgCorrln_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES259A_BattVltgCorrln_Impl/src/BattVltgCorrln.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES259A_BattVltgCorrln_DDReport.txt`

- **Source path in repository:** `ES259A_BattVltgCorrln_Design/Reports/ES259A_BattVltgCorrln_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES259A_BattVltgCorrln_DataDict
10-May-2016 10:45:15
Tool Release:  2.38.0



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
(variables: 1, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
BattVltgAdcFaild            	Cannot match name to list of known Nexteer signals.
BattVltgSwd1AdcFaild        	Cannot match name to list of known Nexteer signals.
BattVltgSwd2AdcFaild        	Cannot match name to list of known Nexteer signals.
InhbBattVltgDiagc           	Cannot match name to list of known Nexteer signals.
(variables: 11, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
BattVltgCorrlnIdptSig       	Name does not match required pattern.
DftBrdgVltgActv             	Cannot match name to list of known Nexteer signals.
(variables: 4, errors: 2)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
BattVltgCorrlnNtc0x03C0x0440x04CFailStep	    0x             Unknown Keyword used.Only Nexteer approved Keywords should be used.
BattVltgCorrlnNtc0x03C0x0440x04CFailStep	    0440x          Unknown Keyword used.Only Nexteer approved Keywords should be used.
BattVltgCorrlnNtc0x03C0x0440x04CPassStep	    0x             Unknown Keyword used.Only Nexteer approved Keywords should be used.
BattVltgCorrlnNtc0x03C0x0440x04CPassStep	    0440x          Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 18, errors: 4)

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
(variables: 9, errors: 0)
```
*... truncated (48 more lines in the source file). ...*

### `BattVltgCorrln_IntegrationManual.doc`

- **Source path in repository:** `ES259A_BattVltgCorrln_Impl/doc/BattVltgCorrln_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `BattVltgCorrln_MDD.doc`

- **Source path in repository:** `ES259A_BattVltgCorrln_Impl/doc/BattVltgCorrln_MDD.doc`
- **Format:** `.doc`
- **Size:** `236 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
