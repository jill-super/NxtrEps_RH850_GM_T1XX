---
title: "Vehicle Speed Limiter (SF016A_VehSpdLimr)"
description: "Vehicle Speed Limiter: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Vehicle Speed Limiter component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF016A_VehSpdLimr_Design` | Design package |
| `SF016A_VehSpdLimr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF016A_VehSpdLimr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF016A_VehSpdLimr_Impl` |  |
| C sources | `VehSpdLimr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `VehSpdLimr.dcf`, `VehSpdLimr_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF016A_VehSpdLimr_Impl.gpj`, `VehSpdLimr.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF016A_VehSpdLimr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF016A_VehSpdLimr_Impl/src/VehSpdLimr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF016A_VehSpdLimr_DDReport.txt`

- **Source path in repository:** `SF016A_VehSpdLimr_Design/Reports/SF016A_VehSpdLimr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF016A_VehSpdLimr_DataDict
25-Apr-2016 09:22:39
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
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 5, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 1, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 4, errors: 0)

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
(variables: 4, errors: 0)

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

### `VehSpdLimr_IntegrationManual.doc`

- **Source path in repository:** `SF016A_VehSpdLimr_Impl/doc/VehSpdLimr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `139 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `VehSpdLimr_MDD.docx`

- **Source path in repository:** `SF016A_VehSpdLimr_Impl/doc/VehSpdLimr_MDD.docx`
- **Format:** `.docx`
- **Size:** `98 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

VehSpdLimr

August 10, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sarika Natu ,

KPIT Technologies,

IndiaChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sarika Natu (KPIT Technologies) | 1.0 | 10-Aug-2015 |

Description

Author

Version

Date

Initial Version

Sarika Natu(KPIT Technologies)

1.0

10-Aug-2015

Table of Contents

1VehSpdLimr High-Level Description4

2Design details of software module5

2.1Graphical representation of VehSpdLimr5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: VehSpdLimr_Init7

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.1.2Per: VehSpdLimr_Per17

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

## VehSpdLimr High-Level Description

The Vehicle Speed Limiting Function determines a limited assist torque command value as a function of vehicle speed and handwheel position to manage mechanical fatigue near end-of-travel positions.

## Design details of software module

### Graphical representation of VehSpdLimr

### Data Flow Diagram

See FDD.

#### Component level DFD

See FDD.

#### Function level DFD

See FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

NA

## Software Component Implementation

### Sub-Module Functions

### Init<Component Name>_Init<n>

### Design Rationale

None

### Module Outputs

None

### Per: VehSpdLimrPer1

### Design Rationale

FDD model contains a block named VehSpdLimrPer1

### Store Module Inputs to Local copies

See FDD

### (Processing of function)………

See FDD

### Store Local copy of outputs into Module Outputs

See FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

Referring to anomaly EA4#1276, following are the discrepancies found:

1) Min/max values of HwAgEotCw, HwAgEotCcw, VehSpdLimrPosMaxOffs1, and VehSpdLimrPosMaxOffs2 need to be set to more realistic values; With the current ranges, there is a possiblity of converting negative numbers to unsigned data types.  Note these ranges need to be coordinated with SF011A and SF018A.

2) Table VehSpdLimrMaxAssiY monotony needs to be identified as "Decreasing" ­­ the implementation assumes that VehSpdLimrMaxAssiY[0] is the maximum value of the table.

3) The concatenate block that creates the Y table for the linear interpolation block has the two inputs reversed ­­ the first input to the concatenation should be the max value of the VehSpdLimrMaxAssiY table, and the second input to the concatenation should be the output of the 1­D Lookup block.

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | EA4  Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | SF016A_VehSpdLimr_Design | See Synergy subproject version |

|  |  |  |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 01.00.00

3

EA4 Software Naming Conventions.doc

01.00.00

4

Software Design and Coding Standards.doc

2.1

5

SF016A_VehSpdLimr_Design

See Synergy subproject version

Back to [Application Software](../).
