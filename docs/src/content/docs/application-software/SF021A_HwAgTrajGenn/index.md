---
title: "Handwheel Angle Trajectory Generation (SF021A_HwAgTrajGenn)"
description: "Handwheel Angle Trajectory Generation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Trajectory Generation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF021A_HwAgTrajGenn_Design` | Design package |
| `SF021A_HwAgTrajGenn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF021A_HwAgTrajGenn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF021A_HwAgTrajGenn_Impl` |  |
| C sources | `HwAgTrajGenn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgTrajGenn.dcf`, `HwAgTrajGenn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAgTrajGenn.dpa`, `RteGen.bat`, `SF021A_HwAgTrajGenn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF021A_HwAgTrajGenn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF021A_HwAgTrajGenn_Impl/src/HwAgTrajGenn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF021A_HwAgTrajGenn_DDReport.txt`

- **Source path in repository:** `SF021A_HwAgTrajGenn_Design/Reports/SF021A_HwAgTrajGenn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF021A_HwAgTrajGenn_DataDict
07-Apr-2016 08:56:29
Tool Release:  2.37.0



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
(variables: 1, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwAgTrajGennEna             	Name does not match required pattern.
(variables: 2, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 1, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 3, errors: 0)

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

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 10, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `HwAgTrajGenn_IntegrationManual.doc`

- **Source path in repository:** `SF021A_HwAgTrajGenn_Impl/doc/HwAgTrajGenn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgTrajGenn_MDD.docx`

- **Source path in repository:** `SF021A_HwAgTrajGenn_Impl/doc/HwAgTrajGenn_MDD.docx`
- **Format:** `.docx`
- **Size:** `103 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgTrajGenn

Feb 4, 2016

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

| Initial Version | Sankardu   Varadapureddi | 1 | 4 - Feb -201 6 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

4-Feb-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2HwAgTrajGenn High-Level Description6

3Design details of software module7

3.1Graphical representation of HwAgTrajGenn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: None9

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: HwAgTrajGennPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1SetTrajTarPrm_Oper9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #19

5.4.1.1Description10

5.4.2Local Function #210

5.4.2.1Description10

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## HwAgTrajGenn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of HwAgTrajGenn

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

### Init: HwAgTrajGennInit1

### Design Rationale

Dummy init function created to meet coding standards.

### Module Outputs

### Per: HwAgTrajGennPer1

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### SetTrajTarPrm_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | HwAgTrajInitVaris | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | CalcFlg_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwATar_HwDegPerSecPerSec_T_f32 | float32 | 10 | 2000 |

|  | HwAgTar_HwDeg_T_f32 | float32 | -800 | 800 |

|  | HwVelTar_HwDegPerSec_T_f32 | float32 | 10 | 1000 |

| Return Value | None |  |  |  |

Function Name

HwAgTrajInitVaris

Type

Min

Max

Arguments Passed

HwPosn_HwDeg_T_f32

float32

-1440

1440

CalcFlg_Cnt_T_logl

boolean

FALSE

TRUE

HwATar_HwDegPerSecPerSec_T_f32

float32

10

2000

HwAgTar_HwDeg_T_f32

float32

-800

800

HwVelTar_HwDegPerSec_T_f32

float32

10

1000

Return Value

None

### Description

"Initialize Variables" block implementation.

### Local Function #2

| Function Name | HwAgTrajGenSigs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | CalcFlg_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | HwAgTrakgServoCmd_HwDeg_T_f32 | float32 | -1440 | 1440 |

Function Name

HwAgTrajGenSigs

Type

Min

Max

Arguments Passed

HwPosn_HwDeg_T_f32

float32

-1440

1440

CalcFlg_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

HwAgTrakgServoCmd_HwDeg_T_f32

float32

-1440

1440

### Description

"Generate Signals" block implementation.

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

| 2 | MDD Guideline | Process 4.02. 01 |

| 3 | Software Naming Conventions.doc | Process 4.02. 01 |

| 4 | Software Design and Coding Standards.doc | Process 4.02. 01 |

| 5 | FDD :  SF021A _   HwAgTrajGenn _Design | See Synergy sub project version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

Process 4.02.01

3

Software Naming Conventions.doc

Process 4.02.01

4

Software Design and Coding Standards.doc

Process 4.02.01

5

FDD : SF021A_ HwAgTrajGenn_Design

See Synergy sub project version

Back to [Application Software](../).
