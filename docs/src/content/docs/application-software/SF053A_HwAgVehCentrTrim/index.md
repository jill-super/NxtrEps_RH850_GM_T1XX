---
title: "Handwheel Angle Vehicle Centering Trim (SF053A_HwAgVehCentrTrim)"
description: "Handwheel Angle Vehicle Centering Trim: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Vehicle Centering Trim component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF053A_HwAgVehCentrTrim_Design` | Design package |
| `SF053A_HwAgVehCentrTrim_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF053A_HwAgVehCentrTrim_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF053A_HwAgVehCentrTrim_Impl` |  |
| C sources | `HwAgVehCentrTrim.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgVehCentrTrim.dcf`, `HwAgVehCentrTrim_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAgVehCentrTrim.dpa`, `RteGen.bat`, `SF053A_HwAgVehCentrTrim_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF053A_HwAgVehCentrTrim_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF053A_HwAgVehCentrTrim_Impl/src/HwAgVehCentrTrim.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF053A_HwAgVehCentrTrim_DDReport.txt`

- **Source path in repository:** `SF053A_HwAgVehCentrTrim_Design/Reports/SF053A_HwAgVehCentrTrim_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF053A_HwAgVehCentrTrim_DataDict
22-Nov-2016 10:59:56
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
(variables: 4, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 7, errors: 0)

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
(variables: 2, errors: 0)

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
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `HwAgVehCentrTrim_IntegrationManual.doc`

- **Source path in repository:** `SF053A_HwAgVehCentrTrim_Impl/doc/HwAgVehCentrTrim_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `148 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgVehCentrTrim_MDD.docx`

- **Source path in repository:** `SF053A_HwAgVehCentrTrim_Impl/doc/HwAgVehCentrTrim_MDD.docx`
- **Format:** `.docx`
- **Size:** `114 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgVehCentrTrim

December 6, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Nick Saxton | 1 | 24 - Feb- 201 6 |

| Updated graphical representation | Nick Saxton | 2 | 04-Apr-2016 |

| Updated graphical representation for FDD v1.3.0 | Nick Saxton | 3 | 15-Jun-2016 |

| Added  Init  function to sub-module functions | Nick Saxton | 4 | 12-Sep-2016 |

| Updated to fix Anomaly EA4# 8204 | Matthew  Leser | 5 | 06-Dec-2016 |

Description

Author

Version

Date

Initial Version

Nick Saxton

1

24-Feb-2016

Updated graphical representation

Nick Saxton

2

04-Apr-2016

Updated graphical representation for FDD v1.3.0

Nick Saxton

3

15-Jun-2016

Added Init function to sub-module functions

Nick Saxton

4

12-Sep-2016

Updated to fix Anomaly EA4#8204

Matthew Leser

5

06-Dec-2016

Table of Contents

1HwAgVehCentrTrim High-Level Description4

2Design details of software module5

2.1Graphical representation of HwAgVehCentrTrim5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: None7

4.1.2Per: GmStrtStopPer17

4.1.2.1Design Rationale7

4.1.2.2Store Module Inputs to Local copies7

4.1.2.3(Processing of function)………7

4.1.2.4Store Local copy of outputs into Module Outputs7

4.2Server Runables7

4.3Interrupt Functions7

4.4Module Internal (Local) Functions7

4.5GLOBAL Function/Macro Definitions7

5Known Limitations with Design8

6UNIT TEST CONSIDERATION9

Appendix AAbbreviations and Acronyms10

Appendix BGlossary11

Appendix CReferences12

## HwAgVehCentrTrim High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of HwAgVehCentrTrim

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

| Constant Name | Units | Value |

| --- | --- | --- |

| HALFFACTOR_ULS _F32 | ULS | 0.5 |

Constant Name

Units

Value

HALFFACTOR_ULS_F32

ULS

0.5

Refer .m file for other constants

## Software Component Implementation

### Sub-Module Functions

### Init: HwAgVehCentrTrimInit1

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: HwAgVehCentrTrimPer1

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### ClrHwAgTrimVal_Oper

Refer FDD

### GetHwAgTrimVal_ Oper

Refer FDD

### SetHwAgTrimVal_Oper

Refer FDD

### UpdHwAgTrimVal_Oper

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms

| Abbreviation  or Acronym | Description |

| --- | --- |

|  |  |

|  |  |

Abbreviation or Acronym

Description

#### Glossary

Note: Terms and definitions from the source “Nexteer Automotive” take precedence over all other definitions of the same term.  Terms and definitions from the source “Nexteer Automotive” are formulated from multiple sources, including the following:

ISO 9000

ISO/IEC 12207

ISO/IEC 15504

Automotive SPICE® Process Reference Model (PRM)

Automotive SPICE® Process Assessment Model (PAM)

ISO/IEC 15288

ISO 26262

IEEE Standards

SWEBOK

PMBOK

Existing Nexteer Automotive documentation

| Term | Definition | Source |

| --- | --- | --- |

| MDD | Module Design Document |  |

| DFD | Data Flow Diagram |  |

Term

Definition

Source

MDD

Module Design Document

DFD

Data Flow Diagram

#### References

| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  SF053A_HwAgVehCentrTrim_Design | See Synergy sub project version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 01.00.01

3

Software Naming Conventions.doc

EA4 01.00.00

4

Software Design and Coding Standards.doc

2.1

5

FDD : SF053A_HwAgVehCentrTrim_Design

See Synergy sub project version

Back to [Application Software](../).
