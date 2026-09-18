---
title: "Motor Angle Arbitration (ES248A_MotAgArbn)"
description: "Motor Angle Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Angle Arbitration component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES248A_MotAgArbn_Design` | Design package |
| `ES248A_MotAgArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES248A_MotAgArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES248A_MotAgArbn_Impl` |  |
| C sources | `CDD_MotAgArbn.c`, `CDD_MotAgArbn_MotCtrl.c` |
| Public headers | `CDD_MotAgArbn.h`, `CDD_MotAgArbn_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotAgArbn.dcf`, `MotAgArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES248A_MotAgArbn_Impl.gpj`, `MotAgArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES248A_MotAgArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES248A_MotAgArbn_Impl/src/CDD_MotAgArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES248A_MotAgArbn_Impl/src/CDD_MotAgArbn_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES248A_MotAgArbn_DDReport.txt`

- **Source path in repository:** `ES248A_MotAgArbn_Design/Reports/ES248A_MotAgArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES248A_MotAgArbn_DataDict
21-Apr-2016 10:32:46
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
MotCtrlMotAgAMecl           	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgAMeclQlfr       	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgAMeclRollgCntr  	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgBMecl           	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgBMeclQlfr       	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgBMeclRollgCntr  	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgMeclCorrlnSt    	Cannot match name to list of known Nexteer signals.
(variables: 7, errors: 7)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotCtrlMotAgMecl
           	Found in model but not in data dictionary.
(variables: 1, errors: 1)

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
*... truncated (43 more lines in the source file). ...*

### `MotAgArbn_IntegrationManual.doc`

- **Source path in repository:** `ES248A_MotAgArbn_Impl/doc/MotAgArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotAgArbn_MDD.docx`

- **Source path in repository:** `ES248A_MotAgArbn_Impl/doc/MotAgArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `93 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotAgArbn

Aug 5, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Spandana Balani,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | SB | 1.0 | 05-Aug-2015 |

Description

Author

Version

Date

Initial Version

SB

1.0

05-Aug-2015

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotAgArbn  & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotAgArbn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotAgArbnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotAgArbnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

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

## MotAgArbn  & High-Level Description

Refer FDD.

## Design details of software module

<The Data Flow Diagrams should be created in the absence of this representation with the FDD.>

### Graphical representation of MotAgArbn

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

| CORRLNSTSMASKSIGA_CNT_U08 | 1 | Cnt | 0x01 |

| CORRLNSTS MASKSIGB _CNT_U08 | 1 | Cnt | 0x02 |

| MAXSTALLCNTR_CNT_U08 | 1 | Cnt | 255 |

Constant Name

Resolution

Units

Value

Refer .m file

CORRLNSTSMASKSIGA_CNT_U08

1

Cnt

0x01

CORRLNSTSMASKSIGB_CNT_U08

1

Cnt

0x02

MAXSTALLCNTR_CNT_U08

1

Cnt

255

## Software Component Implementation

### Sub-Module Functions

### Init: MotAgArbnInit1

### Design Rationale

Init1 function is created so that it will allow a RTE model to be created in the AUTOSAR tools which allows  Per-Instance Memory and calibration definition needs.  The initialization function is doing nothing

### Module Outputs

None

### Per: MotAgArbnPer1

### Design Rationale

None

### Store Module Inputs to Local copies

MotCtrlMotAgAMecl_MotRev_T_u0p16       = MOTCTRLMGR_MotCtrlMotAgAMecl;

MotCtrlMotAgBMecl_MotRev_T_u0p16       = MOTCTRLMGR_MotCtrlMotAgBMecl;

MotCtrlMotAgMeclCorrlnSt_Cnt_T_u08     = MOTCTRLMGR_MotCtrlMotAgMeclCorrlnSt;

MotCtrlMotAgAMeclRollgCntr_Cnt_T_u08   = MOTCTRLMGR_MotCtrlMotAgAMeclRollgCntr;

MotCtrlMotAgBMeclRollgCntr_Cnt_T_u08   = MOTCTRLMGR_MotCtrlMotAgBMeclRollgCntr;

MotCtrlMotAgAMeclQlfr_T_enum           = MOTCTRLMGR_MotCtrlMotAgAMeclQlfr;

MotCtrlMotAgBMeclQlfr_T_enum           = MOTCTRLMGR_MotCtrlMotAgBMeclQlfr;

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

MOTCTRLMGR_MotCtrlMotAgMecl = MotCtrlMotAgMecl_MotRev_T_u0p16

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | SigAvlChkRev | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigCorrChk_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | *   LstRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | *   StallCnt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | 0 | 1 |

Function Name

SigAvlChkRev

Type

Min

Max

Arguments Passed

SigCorrChk_Cnt_T_u08

uint8

0

255

SigRollgCnt_Cnt_T_u08

uint8

0

255

SigQlfr_Cnt_T_enum

SigQlfr1

SIGQLFR_NORES

SIGQLFR_FAILD

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

0

1

### Design Rationale

None

### Processing

Refer FDD SigAvlChkRev2 State flow Chart

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

| 2 | MDD Guideline | EA4 01.00.00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

| 5 | FDD – ES248A_MotAgArbn_Design | See Synergy Subproject  verison |

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

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.0

5

FDD – ES248A_MotAgArbn_Design

See Synergy Subproject verison

Back to [Complex Device Drivers](../).
