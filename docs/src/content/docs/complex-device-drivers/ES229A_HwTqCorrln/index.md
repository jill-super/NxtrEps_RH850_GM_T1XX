---
title: "Handwheel Torque Correlation (ES229A_HwTqCorrln)"
description: "Handwheel Torque Correlation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Torque Correlation component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES229A_HwTqCorrln_Design` | Design package |
| `ES229A_HwTqCorrln_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES229A_HwTqCorrln_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES229A_HwTqCorrln_Impl` |  |
| C sources | `HwTqCorrln.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwTqCorrln.dcf`, `HwTqCorrln_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES229A_HwTqCorrln_Impl.gpj`, `HwTqCorrln.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES229A_HwTqCorrln_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES229A_HwTqCorrln_Impl/src/HwTqCorrln.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES229A_HwTqCorrln_DDReport.txt`

- **Source path in repository:** `ES229A_HwTqCorrln_Design/Reports/ES229A_HwTqCorrln_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES229A_HwTqCorrln_DataDict
12-Sep-2016 11:16:52
Tool Release:  2.45.0



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
(variables: 4, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 5, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwTqA                       	Cannot match name to list of known Nexteer signals.
HwTqAQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqARollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqB                       	Cannot match name to list of known Nexteer signals.
HwTqBQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqBRollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqC                       	Cannot match name to list of known Nexteer signals.
HwTqCQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqCRollgCntr              	Cannot match name to list of known Nexteer signals.
HwTqD                       	Cannot match name to list of known Nexteer signals.
HwTqDQlfr                   	Cannot match name to list of known Nexteer signals.
HwTqDRollgCntr              	Cannot match name to list of known Nexteer signals.
(variables: 14, errors: 12)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HwTqChACorrlnTraErr         	Cannot match name to list of known Nexteer signals.
HwTqChBCorrlnTraErr         	Cannot match name to list of known Nexteer signals.
HwTqCorrlnSts               	Name does not match required pattern.
(variables: 4, errors: 3)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 4, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 30, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 2, errors: 0)
```
*... truncated (51 more lines in the source file). ...*

### `HwTqCorrln_IntegrationManual.doc`

- **Source path in repository:** `ES229A_HwTqCorrln_Impl/doc/HwTqCorrln_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwTqCorrln_MDD.docx`

- **Source path in repository:** `ES229A_HwTqCorrln_Impl/doc/HwTqCorrln_MDD.docx`
- **Format:** `.docx`
- **Size:** `155 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwTqCorrln

April 14, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | SB | 1.0 | 04-Aug-2015 |

| Updated to FDD v2.1.0 | NS | 2.0 | 07-Oct-2015 |

| Anomaly EA4#1980 fixed | NS | 3.0 | 20-Oct-2015 |

| Updated to FDD v3.0.0 | SV | 4.0 | 14-Apr-2016 |

Description

Author

Version

Date

Initial Version

SB

1.0

04-Aug-2015

Updated to FDD v2.1.0

NS

2.0

07-Oct-2015

Anomaly EA4#1980 fixed

NS

3.0

20-Oct-2015

Updated to FDD v3.0.0

SV

4.0

14-Apr-2016

Table of Contents

1HwTqCorrln & High-Level Description4

2Design details of software module5

2.1Graphical representation of HwTqCorrln5

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: HwTqCorrlnInit18

4.1.2Per: HwTqCorrlnPer18

4.1.3Per: HwTqCorrlnPer28

4.1.4Per: HwTqCorrlnPer38

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Design Rationale8

4.4.1.2Processing8

4.4.2Local Function #29

4.4.2.1Design Rationale9

4.4.2.2Processing9

4.5GLOBAL Function/Macro Definitions9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## HwTqCorrln & High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of HwTqCorrln

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer .m file |  |  |  |

| HWTQCORRLNSTSSIGA_CNT_U08 | 1 | Cnt | 0x01 |

| HWTQCORRLNSTSSIGB_CNT_U08 | 1 | Cnt | 0x02 |

| HWTQCORRLNSTSSIGC_CNT_U08 | 1 | Cnt | 0x04 |

| HWTQCORRLNSTSSIGD_CNT_U08 | 1 | Cnt | 0x08 |

| MAXSTALL_CNT_U08 | 1 | Cnt | 255 |

| HWTQIDPTSIGALL_CNT_U08 | 1 | Cnt | 4 |

| HWTQIDPTSIGHALF_CNT_U08 | 1 | Cnt | 2 |

| HWTQIDPTSIGNZERO_CNT_U08 | 1 | Cnt | 0 |

| HWTQCHCORRLNTRAERRMAXLMT_   HWNWTMTR _F32 | 1 | HWNWTMTR | 10.0 |

| HWTQCHCORRLNTRAERRM IN LMT_   HWNWTMTR _F32 | 1 | HWNWTMTR | -10.0 |

Constant Name

Resolution

Units

Value

Refer .m file

HWTQCORRLNSTSSIGA_CNT_U08

1

Cnt

0x01

HWTQCORRLNSTSSIGB_CNT_U08

1

Cnt

0x02

HWTQCORRLNSTSSIGC_CNT_U08

1

Cnt

0x04

HWTQCORRLNSTSSIGD_CNT_U08

1

Cnt

0x08

MAXSTALL_CNT_U08

1

Cnt

255

HWTQIDPTSIGALL_CNT_U08

1

Cnt

4

HWTQIDPTSIGHALF_CNT_U08

1

Cnt

2

HWTQIDPTSIGNZERO_CNT_U08

1

Cnt

0

HWTQCHCORRLNTRAERRMAXLMT_ HWNWTMTR_F32

1

HWNWTMTR

10.0

HWTQCHCORRLNTRAERRMINLMT_ HWNWTMTR_F32

1

HWNWTMTR

-10.0

## Software Component Implementation

Refer FDD

### Sub-Module Functions

### Init: HwTqCorrlnInit1

Refer FDD

### Per: HwTqCorrlnPer1

Refer FDD

### Per: HwTqCorrlnPer2

Refer FDD

### Per: HwTqCorrlnPer3

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | CorrlnSigAvlChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | MaxStallCnt_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | *   LstRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | *   StallCnt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

CorrlnSigAvlChk

Type

Min

Max

Arguments Passed

SigRollgCnt_Cnt_T_u08

uint8

0

255

SigQlfr_Cnt_T_enum

SigQlfr1

SIGQLFR_NORES

SIGQLFR_FAILD

MaxStallCnt_Cnt_T_u08

Uint8

0

255

* LstRollgCnt_Cnt_T_u08

uint8

0

255

* StallCnt_Cnt_T_u08

uint8

0

255

Return Value

SigAvl_Cnt_T_lgc

boolean

FALSE

TRUE

### Design Rationale

None

### Processing

Refer FDD CorrSigAvlChkRev1 State flow Chart

### Local Function #2

| Function Name | ImdtCorrlnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Sig 1 Avl_Cnt_T_lgc | Booelan | FALSE | TRUE |

|  | Sig 2 Avl_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | HwTq 1 _HwNwtMtr_T_f32 | Float32 | -10 .0 | 10 .0 |

|  | HwTq 2 _HwNwtMtr_T_f32 | Float32 | -10 .0 | 10 .0 |

|  | ImdtCorrlnChkFailThd_HwNwtMtr_T_f32 | Float32 | 0 .0 | 20 .0 |

|  | ImdtCorrlnChkPassThd_HwNwtMtr_T_f32 | Float32 | 0 .0 | 20 .0 |

|  | NtcNr_T_enum | Enum | 1 | 511 |

|  | * CorrlnSigAPass_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | * CorrlnSigBPass_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | * ImdtCorrlnChk_Cnt_T_lgc | Boolean | FALSE | TRUE |

| Return Value | ChAImdtCorrlnChk_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

ImdtCorrlnChk

Type

Min

Max

Arguments Passed

Sig1Avl_Cnt_T_lgc

Booelan

FALSE

TRUE

Sig2Avl_Cnt_T_lgc

Boolean

FALSE

TRUE

HwTq1_HwNwtMtr_T_f32

Float32

-10.0

10.0

HwTq2_HwNwtMtr_T_f32

Float32

-10.0

10.0

ImdtCorrlnChkFailThd_HwNwtMtr_T_f32

Float32

0.0

20.0

ImdtCorrlnChkPassThd_HwNwtMtr_T_f32

Float32

0.0

20.0

NtcNr_T_enum

Enum

1

511

*CorrlnSigAPass_Cnt_T_lgc

Boolean

FALSE

TRUE

*CorrlnSigBPass_Cnt_T_lgc

Boolean

FALSE

TRUE

*ImdtCorrlnChk_Cnt_T_lgc

Boolean

FALSE

TRUE

Return Value

ChAImdtCorrlnChk_Cnt_T_lgc

boolean

FALSE

TRUE

### Design Rationale

None

### Processing

Refer FDD ImdtCorrlnChk block

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

| 2 | MDD Guideline | Process 04.02.00 |

| 3 | Software Naming Conventions.doc | Process 04.02.00 |

| 4 | Software Design and Coding Standards.doc | Process 04.02.00 |

| 5 | FDD – ES229A_HwTqCorrln _Design | See Synergy  SubProject  version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

Process 04.02.00

3

Software Naming Conventions.doc

Process 04.02.00

4

Software Design and Coding Standards.doc

Process 04.02.00

5

FDD – ES229A_HwTqCorrln_Design

See Synergy SubProject version

Back to [Complex Device Drivers](../).
