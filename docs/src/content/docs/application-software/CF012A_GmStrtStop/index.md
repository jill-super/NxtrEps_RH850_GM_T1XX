---
title: "General Motors Start Stop (CF012A_GmStrtStop)"
description: "General Motors Start Stop: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Start Stop component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CF012A_GmStrtStop_Design` | Design package |
| `CF012A_GmStrtStop_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF012A_GmStrtStop_Design` |  |
| Documentation folders | `doc/`, `Design/`, `Reports/` |
| `CF012A_GmStrtStop_Impl` |  |
| C sources | `GmStrtStop.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmStrtStop.dcf`, `GmStrtStop_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF012A_GmStrtStop_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmStrtStop.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF012A_GmStrtStop_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF012A_GmStrtStop_Impl/src/GmStrtStop.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CF012A_GmStrtStop_DDReport.txt`

- **Source path in repository:** `CF012A_GmStrtStop_Design/Reports/CF012A_GmStrtStop_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CF012A_GmStrtStop_DataDict
18-May-2016 15:52:06
Tool Release:  2.40.0



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
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 7, errors: 0)

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
(variables: 21, errors: 0)

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
(variables: 4, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `GmStrtStop_IntegrationManual.doc`

- **Source path in repository:** `CF012A_GmStrtStop_Impl/doc/GmStrtStop_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmStrtStop_MDD.docx`

- **Source path in repository:** `CF012A_GmStrtStop_Impl/doc/GmStrtStop_MDD.docx`
- **Format:** `.docx`
- **Size:** `139 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmStrtStop

June 27, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1 | 1 - Oct -2015 |

| Added local function  GetTmrElpsdThd | Nick Saxton | 2 | 4-Feb-2016 |

| Updated for FDD v1.3.0 | Nick Saxton | 3 | 27-Jun-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

1-Oct-2015

Added local function GetTmrElpsdThd

Nick Saxton

2

4-Feb-2016

Updated for FDD v1.3.0

Nick Saxton

3

27-Jun-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2GmStrtStop High-Level Description6

3Design details of software module7

3.1Graphical representation of GmStrtStop7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: None9

5.1.2Per: GmStrtStopPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Description9

5.4.2Local Function #29

5.4.2.1Description10

5.4.3Local Function #310

5.4.3.1Description10

5.4.4Local Function #410

5.4.4.1Description10

5.4.5Local Function #511

5.4.5.1Description11

5.4.6Local Function #611

5.4.6.1Description11

5.4.6.2Design Rationale11

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

## GmStrtStop High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of GmStrtStop

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: None

### Per: GmStrtStopPer1

### Design Rationale

Refer FDD for the overall functionality.

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

| Function Name | DtrmnRateLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ActSt_Cnt_T_u08 | uint8 | 0 | 5 |

|  | VehStrtStopSt_Cnt_T_u08 | uint8 | 0 | 5 |

| Return Value | VehStrtStopRampRate_UlsPerSec_T_f32 | float32 | 0 | 5 |

Function Name

DtrmnRateLim

Type

Min

Max

Arguments Passed

ActSt_Cnt_T_u08

uint8

0

5

VehStrtStopSt_Cnt_T_u08

uint8

0

5

Return Value

VehStrtStopRampRate_UlsPerSec_T_f32

float32

0

5

### Description

Determination of 'VehStrtStopRampRate_UlsPerSec_T_f32' for different mode transitions.

### Local Function #2

| Function Name | NormModExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EngSpd_Rpm_T_f32 | float32 | 0 | 5110 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | * VehStrtStopSt_Cnt_T_u08 | uint8 | 0 | 5 |

|  | * VehStrtStopMotTqCmdSca_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | None |  |  |  |

Function Name

NormModExitCdnsChk

Type

Min

Max

Arguments Passed

EngSpd_Rpm_T_f32

float32

0

5110

VehSpd_Kph_T_f32

float32

0

511

*VehStrtStopSt_Cnt_T_u08

uint8

0

5

*VehStrtStopMotTqCmdSca_Uls_T_f32

float32

0

1

Return Value

None

### Description

This function validates conditions for all state transitions from 'Normal mode'. ‘*VehStrtStopSt_Cnt_T_u08’ and ‘*VehStrtStopMotTqCmdSca_Uls_T_f32’ are outputs of this function.

### Local Function #3

| Function Name | Inter1ModExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EngSpd_Rpm_T_f32 | float32 | 0 | 5110 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwVel_HwRadPerSec_T_f32 | float32 | -42 | 42 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | ToStopModFlg_T_logl | boolean | FALSE | TRUE |

|  | * VehStrtStopSt_Cnt_T_u08 | uint8 | 0 | 5 |

|  | * VehStrtStopMotTqCmdSca_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | None |  |  |  |

Function Name

Inter1ModExitCdnsChk

Type

Min

Max

Arguments Passed

EngSpd_Rpm_T_f32

float32

0

5110

VehSpd_Kph_T_f32

float32

0

511

HwVel_HwRadPerSec_T_f32

float32

-42

42

HwTq_HwNwtMtr_T_f32

float32

-10

10

ToStopModFlg_T_logl

boolean

FALSE

TRUE

*VehStrtStopSt_Cnt_T_u08

uint8

0

5

*VehStrtStopMotTqCmdSca_Uls_T_f32

float32

0

1

Return Value

None

### Description

This function validates conditions for all state transitions from ‘Intermediate 1 mode’.

‘*VehStrtStopSt_Cnt_T_u08’ and ‘*VehStrtStopMotTqCmdSca_Uls_T_f32’ are outputs of this function.

### Local Function #4

| Function Name | StopModExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EngSpd_Rpm_T_f32 | float32 | 0 | 5110 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | * VehStrtStopSt_Cnt_T_u08 | uint8 | 0 | 5 |

|  | * VehStrtStopMotTqCmdSca_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | None |  |  |  |

Function Name

StopModExitCdnsChk

Type

Min

Max

Arguments Passed

EngSpd_Rpm_T_f32

float32

0

5110

VehSpd_Kph_T_f32

float32

0

511

*VehStrtStopSt_Cnt_T_u08

uint8

0

5

*VehStrtStopMotTqCmdSca_Uls_T_f32

float32

0

1

Return Value

None

### Description

This function validates conditions for all state transitions from ‘Stop mode’. ‘*VehStrtStopSt_Cnt_T_u08’ and ‘*VehStrtStopMotTqCmdSca_Uls_T_f32’ are outputs of this function.

### Local Function #5

| Function Name | Inter 2 ModExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EngSpd_Rpm_T_f32 | float32 | 0 | 5110 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwVel_HwRadPerSec_T_f32 | float32 | -42 | 42 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | ToStopModFlg_T_logl | boolean | FALSE | TRUE |

|  | * VehStrtStopSt_Cnt_T_u08 | uint8 | 0 | 5 |

|  | * VehStrtStopMotTqCmdSca_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | None |  |  |  |

Function Name

Inter2ModExitCdnsChk

Type

Min

Max

Arguments Passed

EngSpd_Rpm_T_f32

float32

0

5110

VehSpd_Kph_T_f32

float32

0

511

HwVel_HwRadPerSec_T_f32

float32

-42

42

HwTq_HwNwtMtr_T_f32

float32

-10

10

ToStopModFlg_T_logl

boolean

FALSE

TRUE

*VehStrtStopSt_Cnt_T_u08

uint8

0

5

*VehStrtStopMotTqCmdSca_Uls_T_f32

float32

0

1

Return Value

None

### Description

This function validates conditions for all state transitions from 'Intermediate 2 mode'.

‘*VehStrtStopSt_Cnt_T_u08’ and ‘*VehStrtStopMotTqCmdSca_Uls_T_f32’ are outputs of this function.

### Local Function #6

| Function Name | GetTmrElpsdThd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | StrtStopStChk_Cnt_T_u08 | uint8 | 0 | 5 |

|  | * RefTmr_Cnt_T_u32 | uint32 | 0 | 4294967295 |

|  | ModTmrThd_MilliSec_T_f32 | float32 | 0 | 5000 |

| Return Value | TmrElpsdThd_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

GetTmrElpsdThd

Type

Min

Max

Arguments Passed

StrtStopStChk_Cnt_T_u08

uint8

0

5

*RefTmr_Cnt_T_u32

uint32

0

4294967295

ModTmrThd_MilliSec_T_f32

float32

0

5000

Return Value

TmrElpsdThd_Cnt_T_logl

boolean

FALSE

TRUE

### Description

This function determines whether exit conditions for states Mod1 and Mod2 have been valid for a long enough period of time.

### Design Rationale

This function was created to avoid duplicate code and lower static path count and cyclomatic complexity.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

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

| 5 | FDD :  C F0 12 A _   GmStrtStop _Design | See Synergy sub project version |

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

FDD : CF012A_ GmStrtStop_Design

See Synergy sub project version

Back to [Application Software](../).
