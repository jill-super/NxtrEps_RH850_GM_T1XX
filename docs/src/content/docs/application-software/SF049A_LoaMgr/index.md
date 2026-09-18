---
title: "Loss of Assist Manager (SF049A_LoaMgr)"
description: "Loss of Assist Manager: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Loss of Assist Manager component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF049A_LoaMgr_Design` | Design package |
| `SF049A_LoaMgr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF049A_LoaMgr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF049A_LoaMgr_Impl` |  |
| C sources | `LoaMgr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `LoaMgr.dcf`, `LoaMgr_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `LoaMgr.dpa`, `RteGen.bat`, `SF049A_LoaMgr_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF049A_LoaMgr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF049A_LoaMgr_Impl/src/LoaMgr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF049A_LoaMgr_DDReport.txt`

- **Source path in repository:** `SF049A_LoaMgr_Design/Reports/SF049A_LoaMgr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF049A_LoaMgr_DataDict
23-Nov-2016 13:59:10
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
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 1, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 8, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 7, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 35, errors: 0)

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
(variables: 14, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `LoaMgr_IntegrationManual.doc`

- **Source path in repository:** `SF049A_LoaMgr_Impl/doc/LoaMgr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `LoaMgr_MDD.docx`

- **Source path in repository:** `SF049A_LoaMgr_Impl/doc/LoaMgr_MDD.docx`
- **Format:** `.docx`
- **Size:** `175 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

LoaMgr

Nov 30, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI,

CHENNAI, INDIA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 04-Aug-2015 |

| Updated to design version 2.0.0 | Sarika Natu | 2 | 22-Jun-16 |

| Updated to design version 2.1 .0 | TATA | 3 | 30-Nov-16 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

04-Aug-2015

Updated to design version 2.0.0

Sarika Natu

2

22-Jun-16

Updated to design version 2.1.0

TATA

3

30-Nov-16

Table of Contents1Introduction5

1.1Purpose5

2LoaMgr High-Level Description6

3Design details of software module7

3.1Graphical representation of LoaMgr7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: LoaMgrInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: LoaMgrPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing11

5.4.2Local Function #211

5.4.2.1Design Rationale11

5.4.2.2Processing11

5.4.3Local Function #311

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.4Local Function #411

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Local Function #512

5.4.5.1Design Rationale12

5.4.5.2Processing12

5.4.6Local Function #612

5.4.6.1Design Rationale12

5.4.6.2Processing12

5.4.7Local Function #712

5.4.7.1Design Rationale12

5.4.7.2Processing13

5.4.8Local Function #813

5.4.8.1Design Rationale13

5.4.8.2Processing13

5.5GLOBAL Function/Macro Definitions13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Introduction

### Purpose

MDD for Loss of Assist Manager

## LoaMgr High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of LoaMgr

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer .m file |  |  |  |

Constant Name

Resolution

Units

Value

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: LoaMgrInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: LoaMgrPer1

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

| Function Name | ReqHwTqResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqIdptMin_Cnt_T_u08 | uint8 | 0 | 4 |

|  | TqLoaAvl_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | HwTqResp_Cnt_T_u08 | uint8 | 0 | 5 |

Function Name

ReqHwTqResp

Type

Min

Max

Arguments Passed

HwTqIdptMin_Cnt_T_u08

uint8

0

4

TqLoaAvl_Cnt_T_lgc

boolean

FALSE

TRUE

Return Value

HwTqResp_Cnt_T_u08

uint8

0

5

### Design Rationale

None

### Processing

Refer to ‘HwTqResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #2

| Function Name | ReqMotAgResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgIdptMin_Cnt_T_u08 | uint8 | 0 | 3 |

|  | MotAgSnsrlsAvl_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | MotAgResp_Cnt_T_u08 | uint8 | 0 | 5 |

Function Name

ReqMotAgResp

Type

Min

Max

Arguments Passed

MotAgIdptMin_Cnt_T_u08

uint8

0

3

MotAgSnsrlsAvl_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

MotAgResp_Cnt_T_u08

uint8

0

5

### Design Rationale

None

### Processing

Refer to ‘MotAgResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #3

| Function Name | ReqCurrMeasResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CurrMeasIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | CurrMeasResp_Cnt_T_u08 | uint8 | 0 | 5 |

Function Name

ReqCurrMeasResp

Type

Min

Max

Arguments Passed

CurrMeasIdptMin_Cnt_T_u08

uint8

0

2

Return Value

CurrMeasResp_Cnt_T_u08

uint8

0

5

### Design Rationale

None

### Processing

Refer to ‘CurrMeasResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #4

| Function Name | ReqInvtrResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IvtrIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | InvtrResp_Cnt_T_u08 | uint8 | 0 | 5 |

Function Name

ReqInvtrResp

Type

Min

Max

Arguments Passed

IvtrIdptMin_Cnt_T_u08

uint8

0

2

Return Value

InvtrResp_Cnt_T_u08

uint8

0

5

### Design Rationale

None

### Processing

Refer to ‘CurrMeasResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Request_Responses’

### Local Function #5

| Function Name | CntSwBasdMtgtnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Resp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | PrevMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | MtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

CntSwBasdMtgtnChk

Type

Min

Max

Arguments Passed

Resp_Cnt_T_u08

uint8

0

5

PrevMtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

Return Value

MtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

### Design Rationale

None

### Processing

This function corresponds to common logic (for all requests) in ‘CntSwBasdMtgtn’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Arbitrate_Responses’

### Local Function #6

| Function Name | SelFinalResp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MultiMtgtnResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | HwTqResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | MotAgResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | CurrMeasResp_Cnt_T_u08 | uint8 | 0 | 5 |

|  | InvtrResp_Cnt_T_u08 | uint8 | 0 | 5 |

| Return Value | LoaSt_Cnt_T_enum | LoaSt1 | 0 | 5 |

Function Name

SelFinalResp

Type

Min

Max

Arguments Passed

MultiMtgtnResp_Cnt_T_u08

uint8

0

5

HwTqResp_Cnt_T_u08

uint8

0

5

MotAgResp_Cnt_T_u08

uint8

0

5

CurrMeasResp_Cnt_T_u08

uint8

0

5

InvtrResp_Cnt_T_u08

uint8

0

5

Return Value

LoaSt_Cnt_T_enum

LoaSt1

0

5

### Design Rationale

None

### Processing

This function corresponds to ‘SelFinalResp’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Arbitrate_Responses’

### Local Function #7

| Function Name | SetFaults | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LoaSt_Cnt_T_enum | LoaSt1 | 0 | 5 |

|  | HwTqIdptMin_Cnt_T_u08 | uint8 | 0 | 4 |

|  | MotAgIdptMin_Cnt_T_u08 | uint8 | 0 | 3 |

|  | CurrMeasIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

|  | IvtrIdptMin_Cnt_T_u08 | uint8 | 0 | 2 |

| Return Value | None |  |  |  |

Function Name

SetFaults

Type

Min

Max

Arguments Passed

LoaSt_Cnt_T_enum

LoaSt1

0

5

HwTqIdptMin_Cnt_T_u08

uint8

0

4

MotAgIdptMin_Cnt_T_u08

uint8

0

3

CurrMeasIdptMin_Cnt_T_u08

uint8

0

2

IvtrIdptMin_Cnt_T_u08

uint8

0

2

Return Value

None

### Design Rationale

None

### Processing

This function corresponds to ‘Set_Faults’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1’

### Local Function #8

| Function Name | SwMtgtnEn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | MotAgLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | CurrMeasLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | IvtrLoaMtgtnEna_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | * LoaSca_Uls_T_f32 | float32 | 0 | 1 |

|  | * LoaRateLim_UlsPerSec_T_f32 | float32 | 0.01 | 500 |

| Return Value | None |  |  |  |

Function Name

SwMtgtnEn

Type

Min

Max

Arguments Passed

HwTqLoaMtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

MotAgLoaMtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

CurrMeasLoaMtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

IvtrLoaMtgtnEna_Cnt_T_lgc

boolean

FALSE

TRUE

*LoaSca_Uls_T_f32

float32

0

1

*LoaRateLim_UlsPerSec_T_f32

float32

0.01

500

Return Value

None

### Design Rationale

None

### Processing

This function corresponds to ‘SwMtgtn’ block in FDD at ‘SF049A_LoaMgr/LoaMgr/LoaMgrPer1/Assign_Scale’.

Note that ‘*LoaSca_Uls_T_f32’ and ‘*LoaRateLim_UlsPerSec_T_f32’ are the outputs of this function.

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

| 5 | FDD :  SF049A_LoaMgr_Design | See Synergy sub project version |

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

FDD : SF049A_LoaMgr_Design

See Synergy sub project version

Back to [Application Software](../).
