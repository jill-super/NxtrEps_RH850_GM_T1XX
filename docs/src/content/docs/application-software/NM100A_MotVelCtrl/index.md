---
title: "Motor Velocity Control (NM100A_MotVelCtrl)"
description: "Motor Velocity Control: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Velocity Control component belongs to **Motor Velocity Control** in the **Application Software** layer. It controls the velocity of the steering-assist motor as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `NM100A_MotVelCtrl_Design` | Design package |
| `NM100A_MotVelCtrl_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `NM100A_MotVelCtrl_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `NM100A_MotVelCtrl_Impl` |  |
| C sources | `MotVelCtrl.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotVelCtrl.dcf`, `MotVelCtrl_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotVelCtrl.dpa`, `NM100A_MotVelCtrl_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `NM100A_MotVelCtrl_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `NM100A_MotVelCtrl_Impl/src/MotVelCtrl.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `NM100A_MotVelCtrl_DDReport.txt`

- **Source path in repository:** `NM100A_MotVelCtrl_Design/Reports/NM100A_MotVelCtrl_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of NM100A_MotVelCtrl_DataDict
23-Jun-2016 18:10:16
Tool Release:  2.39.0



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
(variables: 4, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 1, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 0, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 7, errors: 0)

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

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 13, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `MotVelCtrl_IntegrationManual.doc`

- **Source path in repository:** `NM100A_MotVelCtrl_Impl/doc/MotVelCtrl_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotVelCtrl_MDD.docx`

- **Source path in repository:** `NM100A_MotVelCtrl_Impl/doc/MotVelCtrl_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotVelCtrl

May 4, 2016

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

| Initial Version | Sankardu   Varadapureddi | 1 | 17 - Feb -201 6 |

| Input name change | Nick Saxton | 2 | 04-May-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

17-Feb-2016

Input name change

Nick Saxton

2

04-May-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2MotVelCtrl High-Level Description6

3Design details of software module7

3.1Graphical representation of MotVelCtrl7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotVelCtrlInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotVelCtrlPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1GetCtrlPrm_Oper9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………9

5.2.2SetCtrlPrm_Oper9

5.2.2.1Design Rationale9

5.2.2.2(Processing of function)………9

5.2.3StopCtrl_Oper10

5.2.3.1Design Rationale10

5.2.3.2(Processing of function)………10

5.2.4StrtCtrl_Oper10

5.2.4.1Design Rationale10

5.2.4.2(Processing of function)………10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Description10

5.5GLOBAL Function/Macro Definitions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## MotVelCtrl High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of MotVelCtrl

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| ONEOVERTWOMPLR_ULS_F32 | 1 | Cnt | 0 .5 |

Constant Name

Resolution

Units

Value

ONEOVERTWOMPLR_ULS_F32

1

Cnt

0.5

For other constants, refer .m file.

#### Local Constants

## Software Component Implementation

### Sub-Module Functions

### Init: MotVelCtrlInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: MotVelCtrlPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### GetCtrlPrm_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### SetCtrlPrm_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### StopCtrl_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### StrtCtrl_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | FPIDControl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotVelTarSlewed_MotRadPerSec_T_f32 | float32 | -   183500 | 183500 |

|  | MotVel C rf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | PIDCmdLimid_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

Function Name

FPIDControl

Type

Min

Max

Arguments Passed

MotVelTarSlewed_MotRadPerSec_T_f32

float32

- 183500

183500

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

Return Value

PIDCmdLimid_MotNwtMtr_T_f32

float32

-8.8

8.8

### Description

Blocks "F_PID Control_1" , "F_PID Control_2"  and "F_PID Control_3" are of same functionality in the FDD.  This sub function corresponds to those blocks implementation.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None.

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

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD :  NM100A _   MotVelCtrl _Design | See Synergy sub project version |

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

2.0

4

Software Design and Coding Standards.doc

2.1

5

FDD : NM100A_ MotVelCtrl_Design

See Synergy sub project version

Back to [Application Software](../).
