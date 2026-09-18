---
title: "Sine Voltage Generation (ES300A_SinVltgGenn)"
description: "Sine Voltage Generation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Sine Voltage Generation component belongs to **Motor Drive and Voltage Generation** in the **Complex Device Drivers** layer. It drives the power stage of the electric motor (gate drivers, voltage generation, drive diagnostics).

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES300A_SinVltgGenn_Design` | Design package |
| `ES300A_SinVltgGenn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES300A_SinVltgGenn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES300A_SinVltgGenn_Impl` |  |
| C sources | `CDD_SinVltgGenn.c`, `CDD_SinVltgGenn_MotCtrl.c` |
| Public headers | `CDD_SinVltgGenn.h`, `CDD_SinVltgGenn_MotCtrl_MemMap.h`, `CDD_SinVltgGenn_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SinVltgGenn.dcf`, `SinVltgGenn_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES300A_SinVltgGenn_Impl.gpj`, `RteGen.bat`, `SinVltgGenn.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES300A_SinVltgGenn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES300A_SinVltgGenn_Impl/src/CDD_SinVltgGenn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES300A_SinVltgGenn_Impl/src/CDD_SinVltgGenn_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES300A_SinVltgGenn_DDReport.txt`

- **Source path in repository:** `ES300A_SinVltgGenn_Design/Reports/ES300A_SinVltgGenn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES300A_SinVltgGenn_DataDict
09-May-2016 16:58:41
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
SinVltgGennPer1
            	Found in model but not in data dictionary.
(variables: 3, errors: 1)

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
(variables: 4, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 8, errors: 0)

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
(variables: 10, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `SinVltgGenn_IntegrationManual.doc`

- **Source path in repository:** `ES300A_SinVltgGenn_Impl/doc/SinVltgGenn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `137 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SinVltgGenn_MDD.doc`

- **Source path in repository:** `ES300A_SinVltgGenn_Impl/doc/SinVltgGenn_MDD.doc`
- **Format:** `.doc`
- **Size:** `103 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
