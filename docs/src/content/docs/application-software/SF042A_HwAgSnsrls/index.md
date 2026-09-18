---
title: "Handwheel Angle Sensorless (SF042A_HwAgSnsrls)"
description: "Handwheel Angle Sensorless: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle Sensorless component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF042A_HwAgSnsrls_Design` | Design package |
| `SF042A_HwAgSnsrls_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF042A_HwAgSnsrls_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF042A_HwAgSnsrls_Impl` |  |
| C sources | `HwAgSnsrls.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgSnsrls.dcf`, `HwAgSnsrls_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAgSnsrls.dpa`, `RteGen.bat`, `SF042A_HwAgSnsrls_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF042A_HwAgSnsrls_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF042A_HwAgSnsrls_Impl/src/HwAgSnsrls.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF042A_HwAgSnsrls_DDReport.txt`

- **Source path in repository:** `SF042A_HwAgSnsrls_Design/Reports/SF042A_HwAgSnsrls_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF042A_HwAgSnsrls_DataDict
09-Nov-2016 08:14:54
Tool Release:  2.49.0



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
(variables: 2, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 4, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 14, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HwAgSnsrls                  	Name does not match required pattern.
HwAgSnsrlsConf              	Name does not match required pattern.
(variables: 2, errors: 2)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 2, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 26, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 2, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 1, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 4, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 26, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (34 more lines in the source file). ...*

### `HwAgSnsrls_IntegrationManual.doc`

- **Source path in repository:** `SF042A_HwAgSnsrls_Impl/doc/HwAgSnsrls_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgSnsrls_MDD.docx`

- **Source path in repository:** `SF042A_HwAgSnsrls_Impl/doc/HwAgSnsrls_MDD.docx`
- **Format:** `.docx`
- **Size:** `118 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgSnsrls

VERSION: 4.0

DATE:  17-Nov-2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI

CHENNAI, INDIA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | TATA | 1.0 | 29-Jun-2016 |

| Implemented design 1.2.0, 1.3.0 and fixed anomaly 6881 | Hari Mattupalli | 2.0 | 22-Sep-2016 |

| Implemented design 1.4.0 and fixed anomaly 7844 | Hari Mattupalli | 3.0 | 21-Oct-2016 |

| Updated per design rev. 1.6.0 | TATA | 4.0 | 17-Nov-2016 |

Description

Author

Version

Date

Initial Version

TATA

1.0

29-Jun-2016

Implemented design 1.2.0, 1.3.0 and fixed anomaly 6881

Hari Mattupalli

2.0

22-Sep-2016

Implemented design 1.4.0 and fixed anomaly 7844

Hari Mattupalli

3.0

21-Oct-2016

Updated per design rev. 1.6.0

TATA

4.0

17-Nov-2016

Table of Contents

1Introduction5

1.1Purpose5

2HwAgSnsrls & High-Level Description6

3Design details of software module7

3.1Graphical representation of HwAgSnsrls7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: HwAgSnsrlsInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: HwAgSnsrlsPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.2Server Runnables10

5.2.1FSnsrlsHwCentr10

5.2.1.1Design Rationale10

5.2.1.2(Processing of function)………10

5.2.2RstSnsrlsHwCentr11

5.2.2.1Design Rationale11

5.2.2.2(Processing of function)………11

5.3Interrupt Functions11

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Design Rationale11

5.4.1.2Processing11

5.4.2Local Function #212

5.4.2.1Design Rationale12

5.4.2.2Processing12

5.4.3Local Function #312

5.4.3.1Design Rationale12

5.4.3.2Processing13

5.4.4Local Function #413

5.4.4.1Design Rationale13

5.4.4.2Processing13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Introduction

### Purpose

MDD for Handwheel Angle Sensorless.

## HwAgSnsrls & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation of HwAgSnsrls

### Data Flow Diagram

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Units | Value |

| --- | --- | --- |

| Please refer Data Dictionary .m file | NA | NA |

Constant Name

Units

Value

Please refer Data Dictionary .m file

NA

NA

## Software Component Implementation

### Sub-Module Functions

### Init: HwAgSnsrlsInit1

### Design Rationale

None

### Module Outputs

None

### Per: HwAgSnsrlsPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Server Runnables

### FSnsrlsHwCentr

### Design Rationale

None

### (Processing of function)………

Please see FSnsrlsHwCentr block in FDD

### RstSnsrlsHwCentr

### Design Rationale

None

### (Processing of function)………

Please see RstSnsrlsHwCentr block in FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | WhlSpdAutocentr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WhlFrqVld_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | WhlLeFrq_Hz_T_f32 | float32 | 0.01 F | 60 .0F |

|  | Whl Ri Frq_Hz_T_f32 | float32 | 0.01 F | 60.0F |

|  | VehSpd_Kph_T_f32 | float32 | 0.0F | 511.0F |

|  | RelHwAg_HwDeg_T_f32 | float32 | - 1440.0F | 1440.0F |

|  | * WhlSpdHwConf_Uls_T_f32 | fl oat32 | 0.0F | 1.0F |

| Return Value | None |  |  |  |

Function Name

WhlSpdAutocentr

Type

Min

Max

Arguments Passed

WhlFrqVld_Cnt_T_lgc

boolean

FALSE

TRUE

WhlLeFrq_Hz_T_f32

float32

0.01F

60.0F

WhlRiFrq_Hz_T_f32

float32

0.01F

60.0F

VehSpd_Kph_T_f32

float32

0.0F

511.0F

RelHwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

*WhlSpdHwConf_Uls_T_f32

float32

0.0F

1.0F

Return Value

None

### Design Rationale

None.

### Processing

Refer to the “WhlSpdAutocentr” block of the Simulink model of the design.

### Local Function #2

| Function Name | VehDynAutoCentr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdCrf_MotNwtMtr_T_f32 | f loat32 | -8.8 | 8.8 |

|  | HwTq_HwNwtMtr_T_f32 | f loat32 | -10 .0F | 10 .0F |

|  | VehYawRate_VehDegPerSec_T_f32 | f loat32 | -120 .0F | 120 .0F |

|  | VehSpd_Kph_T_f32 | f loat32 | 0 .0F | 511 .0F |

|  | MotVelCrf_MotRadPerSec_T_f32 | f loat32 | -1350 .0F | 1350 .0F |

|  | VehSpdVld_Cnt_T_logl | B oolean | FALSE | TRUE |

|  | RelHwAg_HwDeg_T_f32 | f loat32 | - 1440 .0F | 1440 .0F |

|  | * VehDynHwConf_Uls_T_f32 | f loat32 | 0 .0F | 1 .0F |

| Return Value | None |  |  |  |

Function Name

VehDynAutoCentr

Type

Min

Max

Arguments Passed

MotTqCmdCrf_MotNwtMtr_T_f32

float32

-8.8

8.8

HwTq_HwNwtMtr_T_f32

float32

-10.0F

10.0F

VehYawRate_VehDegPerSec_T_f32

float32

-120.0F

120.0F

VehSpd_Kph_T_f32

float32

0.0F

511.0F

MotVelCrf_MotRadPerSec_T_f32

float32

-1350.0F

1350.0F

VehSpdVld_Cnt_T_logl

Boolean

FALSE

TRUE

RelHwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

*VehDynHwConf_Uls_T_f32

float32

0.0F

1.0F

Return Value

None

### Design Rationale

None.

### Processing

Refer to the “VehDynAutoCentr” block of the Simulink model of the design.

### Local Function #3

| Function Name | PinionTqCalcandLpFilOneEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotTqCmdCrf_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | HwTq_HwNwtMtr_T_f32 | float32 | -10 .0F | 10 .0F |

|  | VehYawRate_VehDegPerSec_T_f32 | float32 | -120 .0F | 120 .0F |

|  | VehSpd_Kph_T_f32 | float32 | 0 .0F | 511 .0F |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 .0F | 1350 .0F |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | RelHwAg_HwDeg_T_f32 | float32 | - 1440 .0F | 1440 .0F |

| Return Value | FilOneEna_MilliSec_T_lgc | boolean | FALSE | TRUE |

Function Name

PinionTqCalcandLpFilOneEna

Type

Min

Max

Arguments Passed

MotTqCmdCrf_MotNwtMtr_T_f32

float32

-8.8

8.8

HwTq_HwNwtMtr_T_f32

float32

-10.0F

10.0F

VehYawRate_VehDegPerSec_T_f32

float32

-120.0F

120.0F

VehSpd_Kph_T_f32

float32

0.0F

511.0F

MotVelCrf_MotRadPerSec_T_f32

float32

-1350.0F

1350.0F

VehSpdVld_Cnt_T_logl

boolean

FALSE

TRUE

RelHwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

Return Value

FilOneEna_MilliSec_T_lgc

boolean

FALSE

TRUE

### Design Rationale

None.

### Processing

Refer to the “PinionTqCalc” and “LpFilOneEna” blocks of the Simulink model of the design.

### Local Function #4

| Function Name | ArbtrtnSmthng | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FCentrHwConf_Uls_T_f32 | float32 | 0 .0F | 1 .0F |

|  | VehDynHwConf_Uls_T_f32 | float32 | 0 .0F | 1 .0F |

|  | WhlSpdHwConf_Uls_T_f32 | float32 | 0 .0F | 1 .0F |

|  | RelHwAg_HwDeg_T_f32 | float32 | - 1440 .0F | 1440 .0F |

|  | * LrndHwConf_Uls_T_f32 | float32 | 0 .0F | 1 .0F |

| Return Value | None |  |  |  |

Function Name

ArbtrtnSmthng

Type

Min

Max

Arguments Passed

FCentrHwConf_Uls_T_f32

float32

0.0F

1.0F

VehDynHwConf_Uls_T_f32

float32

0.0F

1.0F

WhlSpdHwConf_Uls_T_f32

float32

0.0F

1.0F

RelHwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

*LrndHwConf_Uls_T_f32

float32

0.0F

1.0F

Return Value

None

### Design Rationale

None.

### Processing

Please refer to the “Arbitration” and “Smoothing” blocks of the Simulink model of the design.

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software  Coding Standards .doc | 2.1 |

| 5 | FDD : SF042A_ HwAgSnsrls _Design | See Synergy Sub-project version |

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

Software Coding Standards.doc

2.1

5

FDD : SF042A_HwAgSnsrls_Design

See Synergy Sub-project version

Back to [Application Software](../).
