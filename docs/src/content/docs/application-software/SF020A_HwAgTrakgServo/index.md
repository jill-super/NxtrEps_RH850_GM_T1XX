---
title: "Handwheel Angle Tracking Servo (SF020A_HwAgTrakgServo)"
description: "Handwheel Angle Tracking Servo: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Tracking Servo component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF020A_HwAgTrakgServo_Design` | Design package |
| `SF020A_HwAgTrakgServo_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF020A_HwAgTrakgServo_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF020A_HwAgTrakgServo_Impl` |  |
| C sources | `HwAgTrakgServo.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgTrakgServo.dcf`, `HwAgTrakgServo_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAgTrakgServo.dpa`, `RteGen.bat`, `SF020A_HwAgTrakgServo_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF020A_HwAgTrakgServo_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF020A_HwAgTrakgServo_Impl/src/HwAgTrakgServo.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF020A_HwAgTrakgServo_DDReport.txt`

- **Source path in repository:** `SF020A_HwAgTrakgServo_Design/Reports/SF020A_HwAgTrakgServo_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF020A_HwAgTrakgServo_DataDict
23-Sep-2016 11:03:54
Tool Release:  2.47.0



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
HwAgTrakgServoCmd           	Name does not match required pattern.
HwAgTrakgServoEna           	Name does not match required pattern.
(variables: 6, errors: 2)

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
(variables: 24, errors: 0)

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
(variables: 8, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 8, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `HwAgTrakgServo_IntegrationManual.doc`

- **Source path in repository:** `SF020A_HwAgTrakgServo_Impl/doc/HwAgTrakgServo_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `137 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgTrakgServo_MDD.docx`

- **Source path in repository:** `SF020A_HwAgTrakgServo_Impl/doc/HwAgTrakgServo_MDD.docx`
- **Format:** `.docx`
- **Size:** `97 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgTrakgServo

Dec 18, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Kannappa Chidambaram (Tata Elxsi),

Trivandrum, INDIA.

Change History

| Initial Version | Kannappa C | EA4 01.00.01 | 1 8 -Dec-2015 |

| --- | --- | --- | --- |

Initial Version

Kannappa C

EA4 01.00.01

18-Dec-2015

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2HwAgTrakgServo & High-Level Description6

3Design details of software module7

3.1Graphical representation of HwAgTrakgServo7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: HwAgTrakgServoInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: HwAgTrakgServoPer110

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

5.4.3Local Function #311

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.4Local Function #411

5.4.4.1Design Rationale12

5.4.4.2Processing12

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

MDD for Handwheel Angle Tracking Servo.

## HwAgTrakgServo & High-Level Description

Please refer FDD

## Design details of software module

### Graphical representation of HwAgTrakgServo

### Data Flow Diagram

Please refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| SECTOMILLISEC_ULS_F32 | Float32 | Uls | 1000.0F |

| Please refer .m file  for the rest | NA | NA | NA |

Constant Name

Resolution

Units

Value

SECTOMILLISEC_ULS_F32

Float32

Uls

1000.0F

Please refer .m file for the rest

NA

NA

NA

## Software Component Implementation

### Sub-Module Functions

### Init: HwAgTrakgServoInit1

### Design Rationale

None

### Module Outputs

None

### Per: HwAgTrakgServoPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

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

| Function Name | FilterDesiredAngle | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_u8p8 | u8p8 | 0U | 511U |

|  | HwAgTrakgServoEna_Uls_T_logl | boolean | FALSE | TRUE |

|  | HwAgTrakgServoCmd_HwDeg_T_f32 | float32 | -1440.0F | 1440.0F |

|  | HwAg_HwDeg_T_f32 | float32 | -1440.0F | 1440.0F |

|  | RampComplete_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | HWATrgtFilt_HwDeg_T_f32 | float32 | -1440.0F | 1440.0F |

Function Name

FilterDesiredAngle

Type

Min

Max

Arguments Passed

VehSpd_Kph_T_u8p8

u8p8

0U

511U

HwAgTrakgServoEna_Uls_T_logl

boolean

FALSE

TRUE

HwAgTrakgServoCmd_HwDeg_T_f32

float32

-1440.0F

1440.0F

HwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

RampComplete_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

HWATrgtFilt_HwDeg_T_f32

float32

-1440.0F

1440.0F

### Design Rationale

NA

### Processing

Please refer FilterDesiredAngle block of the FDD.

(Path : SF020A_HwAgTrakgServo/HwAgTrakgServo/HwAgTrakgServoPer1/FilterDesiredAngle)

### GLOBAL Function/Macro Definitions

None.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

None.

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

| 5 | FDD:  SF020A_HwAgTrakgServo_Design | See Synergy sub project version |

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

FDD: SF020A_HwAgTrakgServo_Design

See Synergy sub project version

Back to [Application Software](../).
