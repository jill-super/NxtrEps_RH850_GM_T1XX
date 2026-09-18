---
title: "Handwheel Torque Arbitration (ES228A_HwTqArbn)"
description: "Handwheel Torque Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Torque Arbitration component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES228A_HwTqArbn_Design` | Design package |
| `ES228A_HwTqArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES228A_HwTqArbn_Design` |  |
| Documentation folders | `Design/`, `Reports/` |
| `ES228A_HwTqArbn_Impl` |  |
| C sources | `HwTqArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwTqArbn.dcf`, `HwTqArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES228A_HwTqArbn_Impl.gpj`, `HwTqArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES228A_HwTqArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES228A_HwTqArbn_Impl/src/HwTqArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES228A_HwTqArbn_DDReport.txt`

- **Source path in repository:** `ES228A_HwTqArbn_Design/Reports/ES228A_HwTqArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES228A_HwTqArbn_DataDict
18-May-2015 11:25:04
Tool Release:  2.9.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF99A
--------------------------------------------------------------
(variable: 1, errors: 0)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
Component block name does not correlate to model file name.
(errors:  1)

--------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init
--------------------------------------------------
(variables: 1, errors: 0)

-------------------------------------
SrvRunnable:	<ShoName><TriggerName>
-------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwTqA                       	Cannot match name to list of known Nexteer signals.
HwTqA                       	.LongName:	Violates AUTOSAR Std.  Suggested fix: 'Handwheel Torque Sensor a Value'.
HwTqAQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqAQlfr                   	.LongName:	Violates AUTOSAR Std.  Suggested fix: 'Handwheel Torque Sensor a Qualifier'.
HwTqARollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqARollgCntr              	.LongName:	Violates AUTOSAR Std.  Suggested fix: 'Handwheel Torque Sensor a Rolling Counter'.
HwTqB                       	Cannot match name to list of known Nexteer signals.
HwTqBQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqBRollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqC                       	Cannot match name to list of known Nexteer signals.
HwTqCQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqCRollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqD                       	Cannot match name to list of known Nexteer signals.
HwTqDQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqDRollgCntr              	Cannot match name to list of known Nexteer signals.
(variables: 13, errors: 15)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HwTqChA                     	.LongName:	Violates AUTOSAR Std.  Suggested fix: 'Handwheel Torque Channel a Value'.
(variables: 3, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
HwTqArbnMaxStallTqA              	.LongName:	Violates AUTOSAR Std.  Suggested fix: 'Handwheel Torque Arbitration Signal a Stall Counter Maximum Threshold'.
(variables: 4, errors: 1)

-------------------------------------------
NON-VOLATILE MEMORY:	<ShoName><Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
```
*... truncated (38 more lines in the source file). ...*

### `HwTqArbn_IntegrationManual.doc`

- **Source path in repository:** `ES228A_HwTqArbn_Impl/doc/HwTqArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwTqArbn_MDD.doc`

- **Source path in repository:** `ES228A_HwTqArbn_Impl/doc/HwTqArbn_MDD.doc`
- **Format:** `.doc`
- **Size:** `172 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
