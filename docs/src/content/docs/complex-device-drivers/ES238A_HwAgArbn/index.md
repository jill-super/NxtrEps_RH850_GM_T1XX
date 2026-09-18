---
title: "Handwheel Angle Arbitration (ES238A_HwAgArbn)"
description: "Handwheel Angle Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Arbitration component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES238A_HwAgArbn_Design` | Design package |
| `ES238A_HwAgArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES238A_HwAgArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES238A_HwAgArbn_Impl` |  |
| C sources | `HwAgArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgArbn.dcf`, `HwAgArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES238A_HwAgArbn_Impl.gpj`, `HwAgArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES238A_HwAgArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES238A_HwAgArbn_Impl/src/HwAgArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES238A_HwAgArbn_DDReport.txt`

- **Source path in repository:** `ES238A_HwAgArbn_Design/Reports/ES238A_HwAgArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES238A_HwAgArbn_DataDict
14-Aug-2015 14:40:28
Tool Release:  2.16.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF99A
--------------------------------------------------------------
(variable: 1, errors: 0)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
Unable to find model for comparison to data dictionary.
(errors:  1)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 1, errors: 0)

--------------------------------------
SrvRunnable:	<ShoName><TriggerName>
--------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwAgA                       	Cannot match name to list of known Nexteer signals.
HwAgAQlfr                   	Cannot match name to list of known Nexteer signals.
HwAgARollgCntr              	Cannot match name to list of known Nexteer signals.
HwAgB                       	Cannot match name to list of known Nexteer signals.
HwAgB                       	    B              Unknown Keyword used.Only Nexteer approved Keywords should be used.
HwAgBQlfr                   	Cannot match name to list of known Nexteer signals.
HwAgBQlfr                   	    B              Unknown Keyword used.Only Nexteer approved Keywords should be used.
HwAgBRollgCntr              	Cannot match name to list of known Nexteer signals.
HwAgBRollgCntr              	    B              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 7, errors: 9)

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
HwAgArbnHwAgMaxStall             	.PortName:   	.PortName should be same as Calibration Name.
(variables: 1, errors: 1)

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
```
*... truncated (45 more lines in the source file). ...*

### `HwAgArbn_IntegrationManual.doc`

- **Source path in repository:** `ES238A_HwAgArbn_Impl/doc/HwAgArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgArbn_MDD.docx`

- **Source path in repository:** `ES238A_HwAgArbn_Impl/doc/HwAgArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `98 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgArbn

Aug 4, 2015

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

| Initial Version | SB | 1.0 | 04-Aug-2015 |

Description

Author

Version

Date

Initial Version

SB

1.0

04-Aug-2015

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2HwAgArbn & High-Level Description6

3Design details of software module7

3.1Graphical representation of HwAgArbn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: <Component Name>_Init<n>9

5.1.2Per: HwAgArbnPer19

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

### Scope

## HwAgArbn & High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of HwAgArbn

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

| CORRLNSTSMASKSIGA_CNT_U08 | 1 | Cnt | 0x0 1 |

| CORRLNSTSMASKSIGB_CNT_U08 | 1 | Cnt | 0x0 2 |

Constant Name

Resolution

Units

Value

CORRLNSTSMASKSIGA_CNT_U08

1

Cnt

0x01

CORRLNSTSMASKSIGB_CNT_U08

1

Cnt

0x02

## Software Component Implementation

Refer FDD

### Sub-Module Functions

### Init: <Component Name>_Init<n>

None

### Per: HwAgArbnPer1

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | CorrSigAvlChkRev1 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | *   LstRollgCnt_Cnt_T_u08 | uint8 | 0 | 255 |

|  | *   StallCnt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | 0 | 1 |

Function Name

CorrSigAvlChkRev1

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

Refer FDD CorrSigAvlChkRev1 State flow Chart

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

| 5 | FDD – ES238A_HwAgArbn_Design | See Synergy  SubProject  version |

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

FDD – ES238A_HwAgArbn_Design

See Synergy SubProject version

Back to [Complex Device Drivers](../).
