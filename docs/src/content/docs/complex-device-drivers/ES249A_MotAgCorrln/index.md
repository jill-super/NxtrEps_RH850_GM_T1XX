---
title: "Motor Angle Correlation (ES249A_MotAgCorrln)"
description: "Motor Angle Correlation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Angle Correlation component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES249A_MotAgCorrln_Design` | Design package |
| `ES249A_MotAgCorrln_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES249A_MotAgCorrln_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES249A_MotAgCorrln_Impl` |  |
| C sources | `MotAgCorrln.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotAgCorrln.dcf`, `MotAgCorrln_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES249A_MotAgCorrln_Impl.gpj`, `MotAgCorrln.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES249A_MotAgCorrln_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES249A_MotAgCorrln_Impl/src/MotAgCorrln.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES249A_MotAgCorrln_DDReport.txt`

- **Source path in repository:** `ES249A_MotAgCorrln_Design/Reports/ES249A_MotAgCorrln_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES249A_MotAgCorrln_DataDict
14-Apr-2016 10:21:28
Tool Release:  2.34.0



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
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotAgAMecl                  	Cannot match name to list of known Nexteer signals.
MotAgAMeclQlfr              	Cannot match name to list of known Nexteer signals.
MotAgAMeclRollgCntr         	Cannot match name to list of known Nexteer signals.
MotAgBMecl                  	Cannot match name to list of known Nexteer signals.
MotAgBMeclQlfr              	Cannot match name to list of known Nexteer signals.
MotAgBMeclRollgCntr         	Cannot match name to list of known Nexteer signals.
MotAgCMecl                  	Cannot match name to list of known Nexteer signals.
MotAgCMeclQlfr              	Cannot match name to list of known Nexteer signals.
MotAgCMeclRollgCntr         	Cannot match name to list of known Nexteer signals.
(variables: 9, errors: 9)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotAgABErrTerm              	Cannot match name to list of known Nexteer signals.
MotAgACErrTerm              	Cannot match name to list of known Nexteer signals.
MotAgBCErrTerm              	Cannot match name to list of known Nexteer signals.
(variables: 5, errors: 3)

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
(variables: 1, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
```
*... truncated (51 more lines in the source file). ...*

### `MotAgCorrln_Integration Manual.docx`

- **Source path in repository:** `ES249A_MotAgCorrln_Impl/doc/MotAgCorrln_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `77 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘MotAgCorrln’

VERSION: 3.0

DATE: 11 Nov 2015

Prepared By:

Software Engineering,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Sankardu   Varadapureddi | 1.0 | 22-May-2015 |

| 2 | Modified as per latest template EA4 01.00.01 and changes performed for FDD v02.1.01 | Sarika   Natu | 2.0 | 21-Aug-2015 |

| 3 | Updated for v3.0.0 of FDD | Selva | 3.0 | 11-Nov-2015 |

Sl. No.

Description

Author

Version

Date

1

Initial version

Sankardu Varadapureddi

1.0

22-May-2015

2

Modified as per latest template EA4 01.00.01 and changes performed for FDD v02.1.01

Sarika Natu

2.0

21-Aug-2015

3

Updated for v3.0.0 of FDD

Selva

3.0

11-Nov-2015

Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3Da Vinci Parameter Configuration Changes7

4.4DaVinci Interrupt Configuration Changes7

4.5Manual Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  |  |

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD –  ES249A_MotAgCorrln_ Design | See Synergy sub project version |

| 2 | Software Naming Conventions | Process 04.2.00 |

| 3 | Software Design and Coding Standards | Process 04.2.00 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – ES249A_MotAgCorrln_Design

See Synergy sub project version

2

Software Naming Conventions

Process 04.2.00

3

Software Design and Coding Standards

Process 04.2.00

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

Module

Required Feature

None

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config

| Modules | Notes |  |

| --- | --- | --- |

| FLTINJENA | Set Value to  STD_ON  to enable fault injection |  |

Modules

Notes

FLTINJENA

Set Value to STD_ON to enable fault injection

### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes

| Parameter | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Parameter

Notes

SWC

None

### DaVinci Interrupt Configuration Changes

| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| None |  |  |  |

ISR Name

VIM #

Priority Dependency

Notes

None

### Manual Configuration Changes

| Constant | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Constant

Notes

SWC

None

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file in the FDD

### Required Global Data Outputs

Refer DataDict.m file in the FDD

### Specific Include Path present

No

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotAgCorrlnInit1 | None | RTE |

Init

Scheduling Requirements

Trigger

MotAgCorrlnInit1

None

RTE

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotAgCorrlnPer1 | None | RTE (2ms) |

Runnable

Scheduling Requirements

Trigger

MotAgCorrlnPer1

None

RTE (2ms)

.

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotAgCorrln_START_SEC_CODE |  |  |

|  |  |  |

Memory Section

Contents

Notes

MotAgCorrln_START_SEC_CODE

* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage

| Feature | RAM | ROM |

| --- | --- | --- |

| < Memmap   usuage  info> |  |  |

Feature

RAM

ROM

<Memmap usuage info>

Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `MotAgCorrln_MDD.docx`

- **Source path in repository:** `ES249A_MotAgCorrln_Impl/doc/MotAgCorrln_MDD.docx`
- **Format:** `.docx`
- **Size:** `142 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘MotAgCorrln’

Apr 14,2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1.0 | 22-May-2015 |

| Modified as per latest template EA4 01.00.01 and changes performed for FDD v02.1.01 | Sarika   Natu | 2.0 | 21-Aug-2015 |

| Updated for v 3.0.0 of the FDD | Selva   Sengottaiyan | 3.0 | 11-Nov-2015 |

| Updated for v 3.1.0 of the FDD | Krishna Anne | 4.0 | 19-Mar-2016 |

| Updated for v 4 . 0 .0 of the FDD | Krishna Anne | 5 .0 | 1 4 - Ap r-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1.0

22-May-2015

Modified as per latest template EA4 01.00.01 and changes performed for FDD v02.1.01

Sarika Natu

2.0

21-Aug-2015

Updated for v 3.0.0 of the FDD

Selva Sengottaiyan

3.0

11-Nov-2015

Updated for v 3.1.0 of the FDD

Krishna Anne

4.0

19-Mar-2016

Updated for v 4.0.0 of the FDD

Krishna Anne

5.0

14-Apr-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotAgCorrln & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotAgCorrln7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotAgCorrlnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotAgCorrlnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3NoneInterrupt Functions9

5.3.1Interrupt Function Name9

5.3.1.1Design Rationale9

5.3.1.2(Processing of the ISR function)…..9

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #210

5.4.2.1Design Rationale10

5.4.2.2Processing11

5.4.3Local Function #311

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.1Local Function #211

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.5GLOBAL Function/Macro Definitions12

5.5.1GLOBAL Function #112

5.5.1.1Design Rationale12

5.5.1.2processing12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### MDD for MotAgCorrln .

## MotAgCorrln & High-Level Description

None

## Design details of software module

### Graphical representation of MotAgCorrln

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

| MOTAGMECLCORRLNSTMIN_CNT_U08 | None | NA | 0 |

| MOTAGMECLCORRLNSTMAX_CNT_U08 | None | NA | 7 |

| MOTAGMECLIDPTSIGMIN_CNT_U08 | None | Cnt | 0 |

| MOTAGMECLIDPTSIGMAX_CNT_U08 | None | Cnt | 3 |

Constant Name

Resolution

Units

Value

MOTAGMECLCORRLNSTMIN_CNT_U08

None

NA

0

MOTAGMECLCORRLNSTMAX_CNT_U08

None

NA

7

MOTAGMECLIDPTSIGMIN_CNT_U08

None

Cnt

0

MOTAGMECLIDPTSIGMAX_CNT_U08

None

Cnt

3

## Software Component Implementation

### Sub-Module Functions

### Init: MotAgCorrlnInit1

Refer FDD

### Design Rationale

Design follows implementation in FDD.

### Module Outputs

Refer FDD

### Per: MotAgCorrlnPer1

Refer FDD

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer to FDD  (Block ‘MotAgCorrlnPer1’)

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### NoneInterrupt Functions

None

### Interrupt Function Name

None

### Design Rationale

None

### (Processing of the ISR function)…..

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | MtrAgSigAvlCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | Enum  ( SigQlfr1 ) | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | LstRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | LstStall_Cnt_T_u08 | uint8 | 0 | 255 |

|  | * StallCntOutp_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

MtrAgSigAvlCheck

Type

Min

Max

Arguments Passed

SigRollg_Cnt_T_u08

uint8

0

255

SigQlfr_Cnt_T_enum

Enum (SigQlfr1)

SIGQLFR_NORES

SIGQLFR_FAILD

LstRollg_Cnt_T_u08

uint8

0

255

LstStall_Cnt_T_u08

uint8

0

255

*StallCntOutp_Cnt_T_u08

uint8

0

255

Return Value

SigAvl_Cnt_T_lgc

boolean

FALSE

TRUE

### Design Rationale

Checks Signal Availability of Motor. Implementation of 'MtrAgA SigAvlCheck', 'MtrAgB SigAvlCheck' and 'MtrAgC SigAvlCheck' blocks.

### Processing

Note: ‘* StallCntOutp_Cnt_T_u08’ is an output of this function.

#### Local Function #2

| Function Name | TestOkCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgAMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

|  | MotAgBMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

|  | MotAgCMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

|  | * MotAgOkA_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | * MotAgOkB_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | * MotAgOkC_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | * MotAgABErrTerm_T_u0p16 | uint16 | 0U | 32768U |

|  | * MotAgB C ErrTerm_T_u0p16 | uint16 | 0U | 32768U |

|  | * MotAgA C ErrTerm_T_u0p16 | uint16 | 0U | 32768U |

| Return Value | None |  |  |  |

Function Name

TestOkCheck

Type

Min

Max

Arguments Passed

MotAgAMecl_MotRev_T_u0p16

uint16

0

65535

MotAgBMecl_MotRev_T_u0p16

uint16

0

65535

MotAgCMecl_MotRev_T_u0p16

uint16

0

65535

*MotAgOkA_Cnt_T_lgc

boolean

FALSE

TRUE

*MotAgOkB_Cnt_T_lgc

boolean

FALSE

TRUE

*MotAgOkC_Cnt_T_lgc

boolean

FALSE

TRUE

*MotAgABErrTerm_T_u0p16

uint16

0U

32768U

*MotAgBCErrTerm_T_u0p16

uint16

0U

32768U

*MotAgACErrTerm_T_u0p16

uint16

0U

32768U

Return Value

None

### Design Rationale

Implementation of 'TestOk' check functionality. This function corresponds to blocks 'MotAgA vs MotAgB', 'MotAgA vs MotAgC', 'MotAgB vs MotAgC' and 'TestOk'.

### Processing

‘*MotAgOkA_Cnt_T_lgc’, ‘*MotAgOkB_Cnt_T_lgc’ and ‘*MotAgOkC_Cnt_T_lgc’ are outputs of this function

#### Local Function #3

| Function Name | MtrAgNotFailedCheck | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | *   MotAgANotFailed_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | *   MotAgBNotFailed_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | *   MotAgCNotFailed_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | *   MotAgMeclIdptSig_Cnt_T_u08 | uint8 | 0 | 3 |

|  | MotAgSigAvlA_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | MotAgSigAvlB_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | MotAgSigAvlC_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | None |  |  |  |

Function Name

MtrAgNotFailedCheck

Type

Min

Max

Arguments Passed

* MotAgANotFailed_Cnt_T_lgc

boolean

FALSE

TRUE

* MotAgBNotFailed_Cnt_T_lgc

boolean

FALSE

TRUE

* MotAgCNotFailed_Cnt_T_lgc

boolean

FALSE

TRUE

* MotAgMeclIdptSig_Cnt_T_u08

uint8

0

3

MotAgSigAvlA_Cnt_T_lgc

boolean

FALSE

TRUE

MotAgSigAvlB_Cnt_T_lgc

boolean

FALSE

TRUE

MotAgSigAvlC_Cnt_T_lgc

boolean

FALSE

TRUE

Return Value

None

### Design Rationale

Implementation of 'NotFailed'  block  functionality.

MotAgANotFailed_Cnt_T_lgc, MotAgBNotFailed_Cnt_T_lgc, MotAgCNotFailed_Cnt_T_lgc and MotAgMeclIdptSig_Cnt_T_u08 are outputs of this function.

### Processing

All arguments are outputs of this function

#### Local Function #2

| Function Name | CalcErrTerm | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotAgAMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

|  | MotAgBMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

|  | MotAgCMecl_MotRev_T_u0p16 | uint16 | 0 | 65535 |

| Return Value | ErrorTerm_Rev_T_u0p16 | uint16 | 0 | 32768 |

Function Name

CalcErrTerm

Type

Min

Max

Arguments Passed

MotAgAMecl_MotRev_T_u0p16

uint16

0

65535

MotAgBMecl_MotRev_T_u0p16

uint16

0

65535

MotAgCMecl_MotRev_T_u0p16

uint16

0

65535

Return Value

ErrorTerm_Rev_T_u0p16

uint16

0

32768

### Design Rationale

MotAg“X” vs MotAg“Y”  where X can be A,B and Y can be B, C block, the implementation will not result in negative values as sign of Switch2 and Abs are changed. Hence Abs1 function is redundant in implementation and ignored.. (Note: Switch 2 always results in MAX VALUE of U0P16 Datatype. So Subtraction of delta from it will not result in negative value)

### Processing

Delta between two input motor angle will outputs of this function

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

None

### Design Rationale

None

### processing

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms

| Abbreviation  or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document |

Abbreviation or Acronym

Description

FDD

Functional Design Document

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

| 2 | MDD Guideline | EA4 01.00.02 |

| 3 | Software Naming Conventions.doc | EA4 01.00.02 |

| 4 | Software Design and Coding Standards.doc | EA4 01.00.02 |

| 5 | ES249A_MotAgCorrln_Design | See Synergy subproject version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 01.00.02

3

Software Naming Conventions.doc

EA4 01.00.02

4

Software Design and Coding Standards.doc

EA4 01.00.02

5

ES249A_MotAgCorrln_Design

See Synergy subproject version

Back to [Complex Device Drivers](../).
