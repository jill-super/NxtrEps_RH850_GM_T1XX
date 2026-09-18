---
title: "Motor Drive Diagnostics (ES320A_MotDrvDiagc)"
description: "Motor Drive Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Drive Diagnostics component belongs to **Motor Drive and Voltage Generation** in the **Complex Device Drivers** layer. It drives the power stage of the electric motor (gate drivers, voltage generation, drive diagnostics).

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES320A_MotDrvDiagc_Design` | Design package |
| `ES320A_MotDrvDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES320A_MotDrvDiagc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES320A_MotDrvDiagc_Impl` |  |
| C sources | `MotDrvDiagc.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotDrvDiagc.dcf`, `MotDrvDiagc_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES320A_MotDrvDiagc_Impl.gpj`, `MotDrvDiagc.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES320A_MotDrvDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES320A_MotDrvDiagc_Impl/src/MotDrvDiagc.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES320A_MotDrvDiagc_DDReport.txt`

- **Source path in repository:** `ES320A_MotDrvDiagc_Design/Reports/ES320A_MotDrvDiagc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES320A_MotDrvDiagc_DataDict
08-Apr-2016 14:07:57
Tool Release:  2.36.0



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
PhaOnTiSumA                 	Cannot match name to list of known Nexteer signals.
PhaOnTiSumB                 	Cannot match name to list of known Nexteer signals.
PhaOnTiSumC                 	Cannot match name to list of known Nexteer signals.
(variables: 12, errors: 3)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotDrvErrA                  	Cannot match name to list of known Nexteer signals.
MotDrvErrB                  	Cannot match name to list of known Nexteer signals.
MotDrvErrC                  	Cannot match name to list of known Nexteer signals.
MotDrvErrD                  	Cannot match name to list of known Nexteer signals.
MotDrvErrE                  	Cannot match name to list of known Nexteer signals.
MotDrvErrF                  	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 6)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 3, errors: 0)

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

```
*... truncated (53 more lines in the source file). ...*

### `MotDrvDiagc_IntegrationManual.doc`

- **Source path in repository:** `ES320A_MotDrvDiagc_Impl/doc/MotDrvDiagc_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotDrvDiagc_MDD.docx`

- **Source path in repository:** `ES320A_MotDrvDiagc_Impl/doc/MotDrvDiagc_MDD.docx`
- **Format:** `.docx`
- **Size:** `107 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotDrvDiagc

Apr 18, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 19 -Aug-2015 |

| ‘ MotDrvDiagcInit1 ’ design rational updated | Sankardu Varadapureddi | 2 | 21-Aug-2015 |

| Updating MDD to incorporate the changes in FDD 1.4.0 | Basavaraja Ganeshappa | 3 | 18-Apr-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

19-Aug-2015

‘MotDrvDiagcInit1’ design rational updated

Sankardu Varadapureddi

2

21-Aug-2015

Updating MDD to incorporate the changes in FDD 1.4.0

Basavaraja Ganeshappa

3

18-Apr-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotDrvDiagc High-Level Description6

3Design details of software module7

3.1Graphical representation of MotDrvDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotDrvDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotDrvDiagcPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## MotDrvDiagc High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of MotDrvDiagc

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

| BITMASK0_CNT_U08 | 1 | Cnt | 0x01 |

| BITMASK2_CNT_U08 | 1 | Cnt | 0x04 |

| BITMASK4_CNT_U08 | 1 | Cnt | 0x10 |

| MOTDRVERRMIN_NANOSEC_F32 | 1 | NoanoSec | 0.0 F |

| MOTDRVERRMAX_NANOSEC_F32 | 1 | NoanoSec | 40000000 .0 F |

Constant Name

Resolution

Units

Value

BITMASK0_CNT_U08

1

Cnt

0x01

BITMASK2_CNT_U08

1

Cnt

0x04

BITMASK4_CNT_U08

1

Cnt

0x10

MOTDRVERRMIN_NANOSEC_F32

1

NoanoSec

0.0F

MOTDRVERRMAX_NANOSEC_F32

1

NoanoSec

40000000.0F

## Software Component Implementation

### Sub-Module Functions

### Init: MotDrvDiagcInit1

### Design Rationale

Refer FDD for the functionality.

### Module Outputs

Refer FDD

### Per: MotDrvDiagcPer1

### Design Rationale

In blocks ‘MeasdPhaFltChkABC’ and ‘MeasdPhaFltChkDEF’, inputs to filters are in integer datatypes. They are converted to float type in order to be compatible with filter SW library functions.

As per discussion with FDD owner, ‘BitsetStsA’ block sets bit 0 of ‘NtcStInfoA’. ‘BitsetStsA1’ sets bit 1 of ‘NtcStInfoA’. ‘DetermineBitsetA1’ block resets both bit0 and bit1.  Same is applicable for phase B (bits 2 and 3) and phase C (bits 4 and 5).

In SW implementation, since NTC state info (NtcStInfoABC_Uls_T_u08) is initialized to ‘0’, clearing of state bits logic (DetermineBitsetA1) is not implemented. It is redundant.

Same logic repeated in case of phase D, E and F signals.

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

| Function Name | SetNtcStInfo | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PhaOnTiMeasd_NanoSec_T_u32 | u int 32 | 0 | 4294967295 |

|  | PhaOnTiSumExp_NanoSec_T_u32 | uint32 | 0 | 4294967295 |

|  | Err_NanoSec_T_f32 | float32 | -3.4E+38 | +3.4E+38 |

|  | BitMask_Cnt_u08 | uint8 | 0x01 | 0x10 |

|  | * NtcStInfo_Uls_T_u08 | uint8 | 0x00 | 0x1F |

| Return Value | Flt_Uls_T_lgc | boolean | FALSE | TRUE |

Function Name

SetNtcStInfo

Type

Min

Max

Arguments Passed

PhaOnTiMeasd_NanoSec_T_u32

uint32

0

4294967295

PhaOnTiSumExp_NanoSec_T_u32

uint32

0

4294967295

Err_NanoSec_T_f32

float32

-3.4E+38

+3.4E+38

BitMask_Cnt_u08

uint8

0x01

0x10

*NtcStInfo_Uls_T_u08

uint8

0x00

0x1F

Return Value

Flt_Uls_T_lgc

boolean

FALSE

TRUE

### Design Rationale

‘BitMask_Cnt_u08’ takes only 0x01, 0x04 and 0x10.

### Processing

Determines ‘NTC State Info’ for Phase on time signals.  Corresponds to implementation of 'MeasdPhaFltChkABC' and ‘MeasdPhaFltChkDEF’ functional blocks.

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | Process 4.02.01 |

| 2 | MDD Guideline | Process 4.02.01 |

| 3 | Software Naming Conventions.doc | Process 4.02.01 |

| 4 | Software Design and Coding Standards.doc | Process 4.02.01 |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

Process 4.02.01

2

MDD Guideline

Process 4.02.01

3

Software Naming Conventions.doc

Process 4.02.01

4

Software Design and Coding Standards.doc

Process 4.02.01

Back to [Complex Device Drivers](../).
