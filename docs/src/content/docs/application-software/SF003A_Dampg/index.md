---
title: "Damping (SF003A_Dampg)"
description: "Damping: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Damping component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF003A_Dampg_Design` | Design package |
| `SF003A_Dampg_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF003A_Dampg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF003A_Dampg_Impl` |  |
| C sources | `Dampg.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `Dampg.dcf`, `Dampg_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Dampg.dpa`, `RteGen.bat`, `SF003A_Dampg_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF003A_Dampg_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF003A_Dampg_Impl/src/Dampg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF003A_Dampg_DDReport.txt`

- **Source path in repository:** `SF003A_Dampg_Design/Reports/SF003A_Dampg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF003A_Dampg_DataDict
29-Nov-2016 16:22:55
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
DampgCmdBasDi               	Name does not match required pattern.
DampgCmdOvrl                	Name does not match required pattern.
DampgCmdSca                 	Name does not match required pattern.
(variables: 8, errors: 3)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
DampgCmdBas                 	Name does not match required pattern.
(variables: 1, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 24, errors: 0)

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
------------------------------------------
(variables: 9, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 7, errors: 0)

```
*... truncated (36 more lines in the source file). ...*

### `Dampg_IntegrationManual.doc`

- **Source path in repository:** `SF003A_Dampg_Impl/doc/Dampg_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Dampg_MDD.docx`

- **Source path in repository:** `SF003A_Dampg_Impl/doc/Dampg_MDD.docx`
- **Format:** `.docx`
- **Size:** `114 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Dampg

July 1, 2015

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

| Initial Version | Sankardu   Varadapureddi | 1.0 | 01-July-2015 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1.0

01-July-2015

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2Dampg High-Level Description5

3Design details of software module6

3.1Graphical representation of <Component Name>6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1.1Sub-Module Functions9

5.1.2Interrupt Service Routines9

5.1.3Server Runnable Functions9

5.1.4Module Internal (Local) Functions9

5.1.4.1Local Function #19

5.1.4.2Description9

5.1.4.3Local Function #29

5.1.4.4Description9

5.1.5Transition Functions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## Dampg High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of Dampg

### Data Flow Diagram

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

None

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {_Init()}

DampgInit1  (Refer FDD for details)

#### Periodic sub-module {_Per()}

DampgPer1  (Refer FDD for details)

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

### Local Function #1

| Function Name | MotVelDampgCmd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | TSca_Uls_T_f32 | float32 | 0 | 10 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

| Return Value | ActvDampg_MotNwtMtr_T_f32 | float32 | -176 | 176 |

Function Name

MotVelDampgCmd

Type

Min

Max

Arguments Passed

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

HwTq_HwNwtMtr_T_f32

float32

-10

10

TSca_Uls_T_f32

float32

0

10

VehSpd_Kph_T_f32

float32

0

511

Return Value

ActvDampg_MotNwtMtr_T_f32

float32

-176

176

### Description

‘MotVelDampgCmd’ block implementation.

### Local Function #2

| Function Name | HydPwrSteerDampgCmd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | TSca_Uls_T_f32 | float32 | 0 | 10 |

|  | AssiCmdBas_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | HydDampg_MotNwtMtr_T_f32 | float32 | - 8.8 | 8.8 |

Function Name

HydPwrSteerDampgCmd

Type

Min

Max

Arguments Passed

VehSpd_Kph_T_f32

float32

0

511

TSca_Uls_T_f32

float32

0

10

AssiCmdBas_MotNwtMtr_T_f32

float32

-8.8

8.8

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

Return Value

HydDampg_MotNwtMtr_T_f32

float32

-8.8

8.8

### Description

‘HydPwrSteerDampgCmd’ block implementation.

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

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

| 5 | FDD  -  SF003A_Dampg_Design | See Synergy sub project version |

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

FDD  - SF003A_Dampg_Design

See Synergy sub project version

Back to [Application Software](../).
