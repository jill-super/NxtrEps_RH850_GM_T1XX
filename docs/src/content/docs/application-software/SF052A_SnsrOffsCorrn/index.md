---
title: "Sensor Offset Correction (SF052A_SnsrOffsCorrn)"
description: "Sensor Offset Correction: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Sensor Offset Correction component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF052A_SnsrOffsCorrn_Design` | Design package |
| `SF052A_SnsrOffsCorrn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF052A_SnsrOffsCorrn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF052A_SnsrOffsCorrn_Impl` |  |
| C sources | `SnsrOffsCorrn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SnsrOffsCorrn.dcf`, `SnsrOffsCorrn_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF052A_SnsrOffsCorrn_Impl.gpj`, `SnsrOffsCorrn.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF052A_SnsrOffsCorrn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF052A_SnsrOffsCorrn_Impl/src/SnsrOffsCorrn.c`. 

Top-level functions defined in `SnsrOffsCorrn.c` (factual extract, first 1):

- `Rte_Read`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF052A_SnsrOffsCorrn_DDReport.txt`

- **Source path in repository:** `SF052A_SnsrOffsCorrn_Design/Reports/SF052A_SnsrOffsCorrn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF052A_SnsrOffsCorrn_DataDict
03-Feb-2016 14:19:10
Tool Release:  2.30.0



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
(variables: 6, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 3, errors: 0)

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

### `SnsrOffsCorrn Integration Manual.doc`

- **Source path in repository:** `SF052A_SnsrOffsCorrn_Impl/doc/SnsrOffsCorrn Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `139 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SnsrOffsCorrn Module Design Document.docx`

- **Source path in repository:** `SF052A_SnsrOffsCorrn_Impl/doc/SnsrOffsCorrn Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `160 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

SnsrOffsCorrn

Jan 27, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Avinash James | 1.0 | 27-Jan-2016 |

Description

Author

Version

Date

Initial Version

Avinash James

1.0

27-Jan-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2SnsrOffsCorrn High-Level Description6

3Design details of software module7

3.1Graphical representation of SnsrOffsCorrn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: SnsrOffsCorrnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: SnsrOffsCorrnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences16

## Introduction

### Purpose

This document defines the module level design for the Sensor Offset and Correction Component. Major part of design has been captured in the FDD and any design rationale that has not been identified in the FDD and has been used to implement the component has been documented in the MDD

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## SnsrOffsCorrn High-Level Description

Sensor Offset and Correction (SnsrOffsCorrn) corrects the Yaw rate, Hand wheel Position and Hand wheel Torque signals using their corresponding offset learnt values.  Each offset value is learnt by the SF051A Sensor Offset Learning.

## Design details of software module

See FDD.

### Graphical representation of SnsrOffsCorrn

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

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| HWAGHILIM_HWDEG_F32 | Single Precision Floating Point | HwDeg | 1440 .0F |

| HWAGLOLIM_HWDEG_F32 | Single Precision Floating Point | HwDeg | - 1440 .0F |

| VEHYAWRATEHILIM_VEHDEGPERSEC_F32 | Single Precision Floating Point | VehDegPerSec | 120 .0F |

| VEHYAWRATELOLIM_VEHDEGPERSEC_F32 | Single Precision Floating Point | VehDegPerSec | - 120 .0F |

Constant Name

Resolution

Units

Value

HWAGHILIM_HWDEG_F32

Single Precision Floating Point

HwDeg

1440.0F

HWAGLOLIM_HWDEG_F32

Single Precision Floating Point

HwDeg

-1440.0F

VEHYAWRATEHILIM_VEHDEGPERSEC_F32

Single Precision Floating Point

VehDegPerSec

120.0F

VEHYAWRATELOLIM_VEHDEGPERSEC_F32

Single Precision Floating Point

VehDegPerSec

-120.0F

## Software Component Implementation

<The detailed design of the function is provided in the FDD. The detail design shall only be added to the MDD when it is not provided in the FDD or the FDD is not adequate and clarification is needed.>

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

<(Note: For multiple init or per functions, insert new headers at the “Header 3” level – subset of “Sub-Module Functions section above” and follow the same sub-section design shown below .  If none required, place the text “None”))>

### Init: SnsrOffsCorrnInit1

### Design Rationale

None – Empty Init Function

### Module Outputs

None

### Per: SnsrOffsCorrnPer1

### Design Rationale

The periodic function reads the input port values and based on the calibration defined, applies the offset to the Yaw rate, Hand wheel Position and Hand wheel Torque signals and writes the corrected value to the corresponding output ports

### Store Module Inputs to Local copies

None

### (Processing of function)………

See FDD.

### Store Local copy of outputs into Module Outputs

None

### Server Runables

None

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 .01 |

| 3 | Software Naming Conventions.doc | 2. 0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

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

2.0

4

Software Design and Coding Standards.doc

2.1

Back to [Application Software](../).
