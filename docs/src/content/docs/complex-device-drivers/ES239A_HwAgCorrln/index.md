---
title: "Handwheel Angle Correlation (ES239A_HwAgCorrln)"
description: "Handwheel Angle Correlation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Correlation component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES239A_HwAgCorrln_Design` | Design package |
| `ES239A_HwAgCorrln_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES239A_HwAgCorrln_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES239A_HwAgCorrln_Impl` |  |
| C sources | `HwAgCorrln.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgCorrln.dcf`, `HwAgCorrln_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES239A_HwAgCorrln_Impl.gpj`, `HwAgCorrln.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES239A_HwAgCorrln_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES239A_HwAgCorrln_Impl/src/HwAgCorrln.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES239A_HwAgCorrln_DDReport.txt`

- **Source path in repository:** `ES239A_HwAgCorrln_Design/Reports/ES239A_HwAgCorrln_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES239A_HwAgCorrln_DataDict
14-Apr-2016 10:53:17
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
(variables: 1, errors: 0)

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
HwAgA                       	Cannot match name to list of known Nexteer signals.
HwAgAQlfr                   	Cannot match name to list of known Nexteer signals.
HwAgARollgCntr              	Cannot match name to list of known Nexteer signals.
HwAgB                       	Cannot match name to list of known Nexteer signals.
HwAgBQlfr                   	Cannot match name to list of known Nexteer signals.
HwAgBRollgCntr              	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 6)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HwAgCorrlnSt                	Name does not match required pattern.
(variables: 2, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
HwAgCorrlnHwAgAbsltDif           	.PortName:   	.PortName should be same as Calibration Name.
HwAgCorrlnHwAgMaxStall           	.PortName:   	.PortName should be same as Calibration Name.
HwAgCorrlnNtc0x092FailStep       	.PortName:   	.PortName should be same as Calibration Name.
HwAgCorrlnNtc0x092PassStep       	.PortName:   	.PortName should be same as Calibration Name.
(variables: 4, errors: 4)

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
*... truncated (47 more lines in the source file). ...*

### `HwAgCorrln_IntegrationManual.doc`

- **Source path in repository:** `ES239A_HwAgCorrln_Impl/doc/HwAgCorrln_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgCorrln_MDD.docx`

- **Source path in repository:** `ES239A_HwAgCorrln_Impl/doc/HwAgCorrln_MDD.docx`
- **Format:** `.docx`
- **Size:** `118 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgCorrln

Dec 15, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Selva Sengottaiyan

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1.0 | 2 8 -July-2015 |

| Anomoly  3047,1982   fixed | Selva   Sengottaiyan | 2.0 | 15-Dec-15 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1.0

28-July-2015

Anomoly 3047,1982   fixed

Selva Sengottaiyan

2.0

15-Dec-15

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2HwAgCorrln High-Level Description5

3Design details of software module6

3.1Graphical representation of ‘HwAgCorrln’6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1.1Sub-Module Functions8

5.1.2Interrupt Service Routines8

5.1.3Server Runnable Functions8

5.1.4Module Internal (Local) Functions8

5.1.5Transition Functions8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

### Scope

## HwAgCorrln High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of ‘HwAgCorrln’

### Data Flow Diagram

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| AANDBUSABLE_CNT_U08 | 1 | uint08 | 3 |

| ONLYBUSABLE_CNT_U08 | 1 | uint08 | 2 |

| ONLYAUSABLE_CNT_U08 | 1 | uint08 | 1 |

| NONEUSABLE_CNT_U08 | 1 | uint08 | 0 |

| BOTHVALID_CNT_U08 | 1 | uint08 | 2 |

| ONEISVALID_CNT_U08 | 1 | uint08 | 1 |

| NONEVALID_CNT_U08 | 1 | uint08 | 0 |

Constant Name

Resolution

Units

Value

AANDBUSABLE_CNT_U08

1

uint08

3

ONLYBUSABLE_CNT_U08

1

uint08

2

ONLYAUSABLE_CNT_U08

1

uint08

1

NONEUSABLE_CNT_U08

1

uint08

0

BOTHVALID_CNT_U08

1

uint08

2

ONEISVALID_CNT_U08

1

uint08

1

NONEVALID_CNT_U08

1

uint08

0

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {_Init()}

None

#### Periodic sub-module {_Per()}

HwAgCorrlnPer1 (Refer FDD for details)

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Local Function #1

| Function Name | HwAg Sig AvlChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SigRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | SigQlfr_Cnt_T_enum | SigQlfr1 | SIGQLFR_NORES | SIGQLFR_FAILD |

|  | * LstRollg_Cnt_T_u08 | uint8 | 0 | 255 |

|  | * LstStall_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | SigAvl_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

HwAgSigAvlChk

Type

Min

Max

Arguments Passed

SigRollg_Cnt_T_u08

uint8

0

255

SigQlfr_Cnt_T_enum

SigQlfr1

SIGQLFR_NORES

SIGQLFR_FAILD

*LstRollg_Cnt_T_u08

uint8

0

255

*LstStall_Cnt_T_u08

uint8

0

255

Return Value

SigAvl_Cnt_T_lgc

boolean

FALSE

TRUE

#### Description

‘HwAgAAvlChk’ and ‘HwAgBAvlChk’ blocks in FDD have same functionality. This routine is implemented for that logic.

#### Transition Functions

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 2 .0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD  -  ES239A_HwAgCorrln_ Design | See Synergy sub project version |

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

2.0

4

Software Design and Coding Standards.doc

2.1

5

FDD  - ES239A_HwAgCorrln_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
