---
title: "Electrical Global Parameters (ES999A_ElecGlbPrm)"
description: "Electrical Global Parameters: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Electrical Global Parameters component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES999A_ElecGlbPrm_Design` | Design package |
| `ES999A_ElecGlbPrm_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES999A_ElecGlbPrm_Design` |  |
| Documentation folders | `Design/`, `Reports/` |
| `ES999A_ElecGlbPrm_Impl` |  |
| C sources | `ElecGlbPrm.c` |
| Public headers | `ElecGlbPrm.h`, `ElecGlbPrm_MemMap.h` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `ES999A_ElecGlbPrm_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `ES999A_ElecGlbPrm_Impl/src/ElecGlbPrm.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES999A_ElecGlbPrm_DDReport.txt`

- **Source path in repository:** `ES999A_ElecGlbPrm_Design/Reports/ES999A_ElecGlbPrm_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES999A_ElecGlbPrm_DataDict
12-Jul-2016 10:44:03
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
Missing Model 	Unable to find model for comparison to data dictionary.
(errors:  1)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 0, errors: 0)

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

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

Back to [Libraries](../).
