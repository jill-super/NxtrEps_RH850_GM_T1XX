---
title: "Hysteresis Compensation (SF012A_HysCmp)"
description: "Hysteresis Compensation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Hysteresis Compensation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF012A_HysCmp_Design` | Design package |
| `SF012A_HysCmp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF012A_HysCmp_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF012A_HysCmp_Impl` |  |
| C sources | `HysCmp.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HysCmp.dcf`, `HysCmp_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HysCmp.dpa`, `RteGen.bat`, `SF012A_HysCmp_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF012A_HysCmp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF012A_HysCmp_Impl/src/HysCmp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF012A_HysCmp.pdf`

- **Source path in repository:** `SF012A_HysCmp_Design/Doc/SF012A_HysCmp.pdf`
- **Format:** `.pdf`
- **Size:** `1145 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SF012A_HysCmp_DDReport.txt`

- **Source path in repository:** `SF012A_HysCmp_Design/Reports/SF012A_HysCmp_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF012A_HysCmp_DataDict
13-Dec-2016 17:17:25
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
HysCmpCmdDi                 	Name does not match required pattern.
HysCmpCmdDi                 	Cannot match name to list of known Nexteer signals.
(variables: 8, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HysCmpCmd                   	Name does not match required pattern.
(variables: 1, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 23, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 2, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 9, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 7, errors: 0)

--------------------------------------------------------------------------------------------
```
*... truncated (35 more lines in the source file). ...*

### `HysCmp_IntegrationManual.doc`

- **Source path in repository:** `SF012A_HysCmp_Impl/doc/HysCmp_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HysCmp_MDD.docx`

- **Source path in repository:** `SF012A_HysCmp_Impl/doc/HysCmp_MDD.docx`
- **Format:** `.docx`
- **Size:** `127 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HysCmp

Jan 04, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | SB | 1.0 | 04-Aug-2015 |

| Updated per Design vers. 1.2.0 | ML | 2.0 | 04-Jan-2017 |

Description

Author

Version

Date

Initial Version

SB

1.0

04-Aug-2015

Updated per Design vers. 1.2.0

ML

2.0

04-Jan-2017

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2HysCmp & High-Level Description6

3Design details of software module7

3.1Graphical representation of HysCmp7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: HysCmpInit110

5.1.2Per: HysCmpPer110

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #110

5.4.2.1Design Rationale10

5.4.2.2Processing11

5.4.3Local Function #111

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## HysCmp & High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of HysCmp

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

Constant Name

Resolution

Units

Value

Refer .m file

## Software Component Implementation

Refer FDD

### Sub-Module Functions

### Init: HysCmpInit1

Refer FDD

### Per: HysCmpPer1

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | MoreCmp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TqChg_HwNwtMtr_T_f32 | Float32 | 0 | 20 |

|  | * RiseXPtr_HwNwtMtr_T_f32 | Float32 | 0 | 1 |

|  | * RiseXFac_HwNwtMtr_T_f32 | Float32 | 0 | 1 |

| Return Value | RiseY_Uls_T_f32 | Float32 | 0 | 1 |

Function Name

MoreCmp

Type

Min

Max

Arguments Passed

TqChg_HwNwtMtr_T_f32

Float32

0

20

*RiseXPtr_HwNwtMtr_T_f32

Float32

0

1

*RiseXFac_HwNwtMtr_T_f32

Float32

0

1

Return Value

RiseY_Uls_T_f32

Float32

0

1

### Design Rationale

None

### Processing

Refer ‘MoreCmp’ block in Simulink model

### Local Function #1

| Function Name | LessCmp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TqChg_HwNwtMtr_T_f32 | Float32 | 0 | 20 |

|  | * RiseYPtr_Uls_T_f32 | Float32 | 0 | 1 |

|  | * RiseXFac_HwNwtMtr_T_f32 | Float32 | 0 | 1 |

| Return Value | RiseY_Uls_T_f32 | Float32 | 0 | 1 |

Function Name

LessCmp

Type

Min

Max

Arguments Passed

TqChg_HwNwtMtr_T_f32

Float32

0

20

*RiseYPtr_Uls_T_f32

Float32

0

1

*RiseXFac_HwNwtMtr_T_f32

Float32

0

1

Return Value

RiseY_Uls_T_f32

Float32

0

1

### Design Rationale

None

### Processing

Refer ‘LessCmp’ block in Simulink model

### Local Function #1

| Function Name | CalcAvlCmp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTqFildVal_HwNwtMtr_T_f32 | Float32 | -10 | 10 |

|  | AssiCmdFildVal_HwNwtMtr_T_f32 | Float32 | -352 | 352 |

| Return Value | HysCmpAvl_HwNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

Function Name

CalcAvlCmp

Type

Min

Max

Arguments Passed

HwTqFildVal_HwNwtMtr_T_f32

Float32

-10

10

AssiCmdFildVal_HwNwtMtr_T_f32

Float32

-352

352

Return Value

HysCmpAvl_HwNwtMtr_T_f32

Float32

-8.8

8.8

### Design Rationale

None

### Processing

Refer ‘CalcAvlCmp’ block in Simulink model

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

| 2 | MDD Guideline | Process 04.02.00 |

| 3 | Software Naming Conventions.doc | Process 04.02.00 |

| 4 | Software Design and Coding Standards.doc | Process 04.02.00 |

| 5 | FDD –  SF012 A_H ysCmp _Design | See Synergy SubProject version |

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

FDD – SF012A_HysCmp_Design

See Synergy SubProject version

Back to [Application Software](../).
