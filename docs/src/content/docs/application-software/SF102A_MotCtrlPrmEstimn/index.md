---
title: "Motor Control Parameter Estimation (SF102A_MotCtrlPrmEstimn)"
description: "Motor Control Parameter Estimation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Control Parameter Estimation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF102A_MotCtrlPrmEstimn_Design` | Design package |
| `SF102A_MotCtrlPrmEstimn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF102A_MotCtrlPrmEstimn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF102A_MotCtrlPrmEstimn_Impl` |  |
| C sources | `MotCtrlPrmEstimn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotCtrlPrmEstimn.dcf`, `MotCtrlPrmEstimn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotCtrlPrmEstimn.dpa`, `RteGen.bat`, `SF102A_MotCtrlPrmEstimn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF102A_MotCtrlPrmEstimn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF102A_MotCtrlPrmEstimn_Impl/src/MotCtrlPrmEstimn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF102A_MotCtrlPrmEstimn_DDReport.txt`

- **Source path in repository:** `SF102A_MotCtrlPrmEstimn_Design/Reports/SF102A_MotCtrlPrmEstimn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF102A_MotCtrlPrmEstimn_DataDict
01-Apr-2016 16:49:48
Tool Release:  2.37.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been
limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been
limited to 255.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin whose data type is dt.lgc must be 0.
Please update your saved files.In workspace, 0.EngMin whose data type is dt.lgc must be 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax whose data type is dt.lgc must be 1.
Please update your saved files.In workspace, 1.EngMax whose data type is dt.lgc must be 1.
Please update your saved files.] 
(errors: 4)

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
(variables: 2, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 6, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 4, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 26, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 1, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
```
*... truncated (43 more lines in the source file). ...*

### `MotCtrlPrmEstimn_IntegrationManual.doc`

- **Source path in repository:** `SF102A_MotCtrlPrmEstimn_Impl/doc/MotCtrlPrmEstimn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `148 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotCtrlPrmEstimn_MDD.doc`

- **Source path in repository:** `SF102A_MotCtrlPrmEstimn_Impl/doc/MotCtrlPrmEstimn_MDD.doc`
- **Format:** `.doc`
- **Size:** `212 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Application Software](../).
