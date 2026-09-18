---
title: "General Motors Torque Arbitration (CF010A_GmTqArbn)"
description: "General Motors Torque Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Torque Arbitration component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CF010A_GmTqArbn_Design` | Design package |
| `CF010A_GmTqArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF010A_GmTqArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CF010A_GmTqArbn_Impl` |  |
| C sources | `GmTqArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmTqArbn.dcf`, `GmTqArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF010A_GmTqArbn_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmTqArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF010A_GmTqArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF010A_GmTqArbn_Impl/src/GmTqArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CF010A_GmTqArbn_DDReport.txt`

- **Source path in repository:** `CF010A_GmTqArbn_Design/Reports/CF010A_GmTqArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CF010A_GmTqArbn_DataDict
09-Feb-2017 13:23:05
Tool Release:  2.53.0



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
(variables: 10, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 9, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 16, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 1, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 5, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 4, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `GmTqArbn_IntegrationManual.doc`

- **Source path in repository:** `CF010A_GmTqArbn_Impl/doc/GmTqArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmTqArbn_MDD.docx`

- **Source path in repository:** `CF010A_GmTqArbn_Impl/doc/GmTqArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `124 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmTqArbn

Feb 9, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Jayakrishnan T,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 5 - Oct -2015 |

| Updated graphical representation to match anomaly EA4#2143 fixes | Nick Saxton | 2 | 1-Feb-2016 |

| Updated graphical representation | Nick Saxton | 3 | 6-Apr-2016 |

| Updates as per latest FDD version | Jayakrishnan T | 4 | 9-Feb-2017 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

5-Oct-2015

Updated graphical representation to match anomaly EA4#2143 fixes

Nick Saxton

2

1-Feb-2016

Updated graphical representation

Nick Saxton

3

6-Apr-2016

Updates as per latest FDD version

Jayakrishnan T

4

9-Feb-2017

Table of Contents1Introduction5

1.1Purpose5

1.2Scope5

2GmTqArbn High-Level Description6

3Design details of software module7

Graphical representation of GmTqArbn7

3.17

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: GmTqArbnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: GmTqArbnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Description10

5.4.2Local Function #210

5.4.2.1Description10

5.4.3Local Function #310

5.4.3.1Description10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## GmTqArbn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of GmTqArbn

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: GmTqArbnInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: GmTqArbnPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | PosnServoSmotRamp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PosSrvoCmd_HwNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | PosSrvoSmoothEnable_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | *APAOvrlCmd _Mot NwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | *ScaleFactor_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | none |  |  |  |

Function Name

PosnServoSmotRamp

Type

Min

Max

Arguments Passed

PosSrvoCmd_HwNwtMtr_T_f32

float32

-8.8

8.8

PosSrvoSmoothEnable_Cnt_T_logl

boolean

FALSE

TRUE

HwTq_HwNwtMtr_T_f32

float32

-10

10

*APAOvrlCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

*ScaleFactor_Uls_T_f32

float32

0

1

Return Value

none

### Description

'PosnServo_Smoothed_Ramp'  functional block implementation.

### Local Function #2

| Function Name | RampVal | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DesLKATqCmd_HwNwtMtr_T_f32 | float32 | -3 | 3 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | OutpTqOvrlCmd_MotNwtMtr_T_f32 | fl o a t32 | 0.0F | 8.8F |

| Return Value | LKAInterTqCmd_HwNwtMtr_T_f32 | float32 | -3 | 3 |

Function Name

RampVal

Type

Min

Max

Arguments Passed

DesLKATqCmd_HwNwtMtr_T_f32

float32

-3

3

VehSpd_Kph_T_f32

float32

0

511

OutpTqOvrlCmd_MotNwtMtr_T_f32

float32

0.0F

8.8F

Return Value

LKAInterTqCmd_HwNwtMtr_T_f32

float32

-3

3

### Description

'Ramp to Value' functional block implementation.

### Local Function #3

| Function Name | ESCLogic | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EscCmd_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | EscSt_Cnt_T_ enum | GmTqArbnEscSt1 | 0 | 4 |

|  | *ESCTqCmd_HwNwtMtr_T_f32 | float32 | - 3 | 3 |

|  | *EscLimdActv_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | ESCActv_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ESCLogic

Type

Min

Max

Arguments Passed

EscCmd_HwNwtMtr_T_f32

float32

-10

10

EscSt_Cnt_T_enum

GmTqArbnEscSt1

0

4

*ESCTqCmd_HwNwtMtr_T_f32

float32

-3

3

*EscLimdActv_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

ESCActv_Cnt_T_logl

boolean

FALSE

TRUE

### Description

'ESC Logic' functional block implementation.

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

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  C F0 1 0 A _   GmTqArbn _Design | See Synergy sub project version |

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

FDD : CF010A_ GmTqArbn_Design

See Synergy sub project version

Back to [Application Software](../).
