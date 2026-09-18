---
title: "Motor Torque Translational Damping (SF050A_MotTqTranlDampg)"
description: "Motor Torque Translational Damping: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Torque Translational Damping component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF050A_MotTqTranlDampg_Design` | Design package |
| `SF050A_MotTqTranlDampg_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF050A_MotTqTranlDampg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF050A_MotTqTranlDampg_Impl` |  |
| C sources | `MotTqTranlDampg.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotTqTranlDampg.dcf`, `MotTqTranlDampg_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotTqTranlDampg.dpa`, `RteGen.bat`, `SF050A_MotTqTranlDampg_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF050A_MotTqTranlDampg_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF050A_MotTqTranlDampg_Impl/src/MotTqTranlDampg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF050A_MotTqTranlDampg_DDReport.txt`

- **Source path in repository:** `SF050A_MotTqTranlDampg_Design/Reports/SF050A_MotTqTranlDampg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF050A_MotTqTranlDampg_DataDict
11-Apr-2016 09:03:13
Tool Release:  2.37.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits
and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits
and has been limited to 4294967295.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits
and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits
and has been limited to 4294967295.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits
and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits
and has been limited to 4294967295.
Please update your saved files.] 
(errors: 6)

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
(variables: 8, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotTqTranlDampgCmpl         	Name does not match required pattern.
(variables: 3, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 2, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 8, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

```
*... truncated (50 more lines in the source file). ...*

### `MotTqTranlDampg_IntegrationManual.doc`

- **Source path in repository:** `SF050A_MotTqTranlDampg_Impl/doc/MotTqTranlDampg_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotTqTranlDampg_MDD.docx`

- **Source path in repository:** `SF050A_MotTqTranlDampg_Impl/doc/MotTqTranlDampg_MDD.docx`
- **Format:** `.docx`
- **Size:** `111 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Transistional Damping (SF-50A)

August 12, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Kanth Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | EA4 01.00.01 | 12-Aug-2015 |

Description

Author

Version

Date

Initial Version

Krishna Kanth Anne

EA4 01.00.01

12-Aug-2015

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotTqTranlDampg & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotTqTranlDampg7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: MotTqTranlDampgInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: MotTqTranlDampgPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.4.2Local Function #211

5.4.2.1Design Rationale11

5.4.2.2Processing11

5.5GLOBAL Function/Macro Definitions11

5.5.1GLOBAL Function #111

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

MDD for Motor Torque Transistional Damping.

### Scope

## MotTqTranlDampg & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of MotTqTranlDampg

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file |  |  |  |

Constant Name

Resolution

Units

Value

Please refer .m file

## Software Component Implementation

### Sub-Module Functions

#### Init: MotTqTranlDampgInit1

### Design Rationale

None

### Module Outputs

None

### Per: MotTqTranlDampgPer1

### Design Rationale

None

### Store Module Inputs to Local copies

Please refer FDD

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | SwOpCtrlPart1 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | TranlDampgTiElpsd_MilliSec_T_f32 | float32 | 0.0 | 1000.0 |

|  | AbslMotVelCrf_MotRadPerSec_T_f32 | float32 | 0.0 | 1350.0 |

| Return Value | MotTqTranlDampgCmpl_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

SwOpCtrlPart1

Type

Min

Max

Arguments Passed

TranlDampgTiElpsd_MilliSec_T_f32

float32

0.0

1000.0

AbslMotVelCrf_MotRadPerSec_T_f32

float32

0.0

1350.0

Return Value

MotTqTranlDampgCmpl_Cnt_T_lgc

boolean

FALSE

TRUE

### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “SwOutputCntrl” block of the Simulink model of the design.

### Local Function #2

| Function Name | SwOpCtrlPart 2 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsCtrldShtDwnFltPrsnt_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | CtrlDampTrq_MotNwtMtr_T_f32 | float32 | -3.0 | 3.0 |

|  | SysSt_Cnt_T_enum | SysSt1 | 0 | 3 |

|  | MotTqCmdCrf_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | MotTqTranlDampgCmpl_Cnt_T_lgc | boolean | FALSE | TRUE |

| Return Value | MotTqCmdCrfDampd_MotNwtMtr_T_f32 | float32 | -11.8 | 11.8 |

Function Name

SwOpCtrlPart2

Type

Min

Max

Arguments Passed

DiagcStsCtrldShtDwnFltPrsnt_Cnt_T_lgc

boolean

FALSE

TRUE

CtrlDampTrq_MotNwtMtr_T_f32

float32

-3.0

3.0

SysSt_Cnt_T_enum

SysSt1

0

3

MotTqCmdCrf_MotNwtMtr_T_f32

float32

-8.8

8.8

MotTqTranlDampgCmpl_Cnt_T_lgc

boolean

FALSE

TRUE

Return Value

MotTqCmdCrfDampd_MotNwtMtr_T_f32

float32

-11.8

11.8

### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “SwOutputCntrl” block of the Simulink model of the design.

### GLOBAL Function/Macro Definitions

None

### GLOBAL Function #1

| Function Name | NA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | NA |  |  |  |

Function Name

NA

Type

Min

Max

Arguments Passed

None

Return Value

NA

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

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

| 5 | FDD :  SF050A_MotTqTranlDampg_ Design  (V 1.1.0) | See Synergy sub project version |

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

FDD : SF050A_MotTqTranlDampg_Design (V 1.1.0)

See Synergy sub project version

Back to [Application Software](../).
