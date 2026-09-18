---
title: "General Motors Function Diagnostic Arbitration (CF025A_GmFctDiArbn)"
description: "General Motors Function Diagnostic Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Function Diagnostic Arbitration component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CF025A_GmFctDiArbn_Design` | Design package |
| `CF025A_GmFctDiArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF025A_GmFctDiArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CF025A_GmFctDiArbn_Impl` |  |
| C sources | `GmFctDiArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmFctDiArbn.dcf`, `GmFctDiArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF025A_GmFctDiArbn_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmFctDiArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF025A_GmFctDiArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF025A_GmFctDiArbn_Impl/src/GmFctDiArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CF025A_GmFctDiArbn_DDReport.txt`

- **Source path in repository:** `CF025A_GmFctDiArbn_Design/Reports/CF025A_GmFctDiArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CF025A_GmFctDiArbn_DataDict
30-Jun-2016 07:24:57
Tool Release:  2.42.0



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
(variables: 1, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 8, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 8, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 2, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 6, errors: 0)

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
(variables: 9, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `GmFctDiArbn_IntegrationManual.doc`

- **Source path in repository:** `CF025A_GmFctDiArbn_Impl/doc/GmFctDiArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmFctDiArbn_MDD.docx`

- **Source path in repository:** `CF025A_GmFctDiArbn_Impl/doc/GmFctDiArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `116 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmFctDiArbn

June 30, 2016

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

| Initial Version | Nick Saxton | 1 | 30-June-2016 |

Description

Author

Version

Date

Initial Version

Nick Saxton

1

30-June-2016

Table of Contents

1GmStrtStop High-Level Description5

2Design details of software module6

2.1Graphical representation of GmStrtStop6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: None8

4.1.2Per: GmStrtStopPer18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function)………8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Description8

4.4.2Local Function #28

4.4.2.1Description9

4.4.3Local Function #39

4.4.3.1Description9

4.5GLOBAL Function/Macro Definitions9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

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

#### GmFctDiReq_Oper

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | GetElpdTi | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FctDi_Cnt_T_logl | boolean | FALSE | TRUE |

|  | FctDiStrtTi_MicroSec_T_u32 | uint32 | 0 | 10000000 |

| Return Value | ElpdTi_Sec_T_f32 | float32 | 0 | 10000000 |

Function Name

GetElpdTi

Type

Min

Max

Arguments Passed

FctDi_Cnt_T_logl

boolean

FALSE

TRUE

FctDiStrtTi_MicroSec_T_u32

uint32

0

10000000

Return Value

ElpdTi_Sec_T_f32

float32

0

10000000

### Description

Implementation of ‘FcnDi_ElpdTi’ block in the model.

### Local Function #2

| Function Name | ChkEotPosInRng | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FctDi_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwAgFinal_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | CwEot_HwDeg_T_f32 | float32 | 360 | 900 |

|  | CcwEot_HwDeg_T_f32 | float32 | -900 | -360 |

| Return Value | GmFctDiSts_Cnt_T_enum | GmFctDiArbnSts1 | GMFCTDIARBNSTS_WAIT | GMFCTDIARBNSTS_TIMEOUTFAIL |

Function Name

ChkEotPosInRng

Type

Min

Max

Arguments Passed

FctDi_Cnt_T_logl

boolean

FALSE

TRUE

HwAgFinal_HwDeg_T_f32

float32

-1440

1440

CwEot_HwDeg_T_f32

float32

360

900

CcwEot_HwDeg_T_f32

float32

-900

-360

Return Value

GmFctDiSts_Cnt_T_enum

GmFctDiArbnSts1

GMFCTDIARBNSTS_WAIT

GMFCTDIARBNSTS_TIMEOUTFAIL

### Description

Implementation of 'CheckEotPosInRng' block in the model.

### Local Function #3

| Function Name | ChkHwTqZeroAndHwAgZero | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAgFinal_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | OnCenterEna_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ChkHwTqZeroAndHwAgZero

Type

Min

Max

Arguments Passed

HwAgFinal_HwDeg_T_f32

float32

-1440

1440

HwTq_HwNwtMtr_T_f32

float32

-10

10

Return Value

OnCenterEna_Cnt_T_logl

boolean

FALSE

TRUE

### Description

Implementation of 'CheckHwTqZeroAndHwAgZero' block in the model.

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  C F0 25 A _   GmFctDiArbn _Design | See Synergy sub project version |

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

FDD : CF025A_ GmFctDiArbn_Design

See Synergy sub project version

Back to [Application Software](../).
