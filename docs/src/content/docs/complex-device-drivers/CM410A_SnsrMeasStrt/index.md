---
title: "Sensor Measurement Start (CM410A_SnsrMeasStrt)"
description: "Sensor Measurement Start: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Sensor Measurement Start component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM410A_SnsrMeasStrt_Design` | Design package |
| `CM410A_SnsrMeasStrt_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM410A_SnsrMeasStrt_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM410A_SnsrMeasStrt_Impl` |  |
| C sources | `CDD_SnsrMeasStrt.c`, `CDD_SnsrMeasStrt_Irq.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SnsrMeasStrt.dcf`, `SnsrMeasStrt_attr_def.xml` |
| Tooling and integration scripts | `CM410A_SnsrMeasStrt_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SnsrMeasStrt.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM410A_SnsrMeasStrt_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM410A_SnsrMeasStrt_Impl/src/CDD_SnsrMeasStrt.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM410A_SnsrMeasStrt_Impl/src/CDD_SnsrMeasStrt_Irq.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM410A_SnsrMeasStrt_DDReport.txt`

- **Source path in repository:** `CM410A_SnsrMeasStrt_Design/Reports/CM410A_SnsrMeasStrt_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM410A_SnsrMeasStrt_DataDict
29-Nov-2016 09:28:46
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
SnsrMeasStrtIrq             	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
(variables: 3, errors: 1)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
SnsrMeasStrtIrq             	Found in model but not in data dictionary.
(variables: 0, errors: 1)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 4, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 0, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 0, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 1, errors: 0)

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

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `SnsrMeasStrt_IntegrationManual.doc`

- **Source path in repository:** `CM410A_SnsrMeasStrt_Impl/doc/SnsrMeasStrt_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `151 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SnsrMeasStrt_MDD.doc`

- **Source path in repository:** `CM410A_SnsrMeasStrt_Impl/doc/SnsrMeasStrt_MDD.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
