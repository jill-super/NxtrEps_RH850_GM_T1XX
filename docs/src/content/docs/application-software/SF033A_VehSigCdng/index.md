---
title: "Vehicle Signal Coding (SF033A_VehSigCdng)"
description: "Vehicle Signal Coding: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Vehicle Signal Coding component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF033A_VehSigCdng_Design` | Design package |
| `SF033A_VehSigCdng_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF033A_VehSigCdng_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF033A_VehSigCdng_Impl` |  |
| C sources | `VehSigCdng.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `VehSigCdng.dcf`, `VehSigCdng_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF033A_VehSigCdng_Impl.gpj`, `VehSigCdng.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF033A_VehSigCdng_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF033A_VehSigCdng_Impl/src/VehSigCdng.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF033A_VehSigCdng_DDReport.txt`

- **Source path in repository:** `SF033A_VehSigCdng_Design/Reports/SF033A_VehSigCdng_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF033A_VehSigCdng_DataDict
10-Nov-2016 14:30:24
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
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 1, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 11, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 10, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 13, errors: 0)

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
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (35 more lines in the source file). ...*

### `VehSigCdng_Integration Manual.doc`

- **Source path in repository:** `SF033A_VehSigCdng_Impl/doc/VehSigCdng_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `VehSigCdng_Module Design Document.docx`

- **Source path in repository:** `SF033A_VehSigCdng_Impl/doc/VehSigCdng_Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `132 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

VehSigCdng

Sep 20, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Spandana BalaniChange History

|  |  |  |  |

| --- | --- | --- | --- |

|  |  |  |  |

|  |  |  |  |

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1 | 13-Jul-2015 |

| 2 | Updated for FDD v2.0.0 | NS | 2 | 2-Jun-2016 |

| 3 | Updated for FDD v2.2.0 | SB | 3 | 20-Sep-2016 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial Version

SB

1

13-Jul-2015

2

Updated for FDD v2.0.0

NS

2

2-Jun-2016

3

Updated for FDD v2.2.0

SB

3

20-Sep-2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2VehSigCdng High-Level Description5

3Design details of software module6

3.1Graphical representation of VehSigCdng6

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1.1Sub-Module Functions10

5.1.2Interrupt Service Routines10

5.1.3Server Runnable Functions10

5.1.4Module Internal (Local) Functions10

5.1.5Transition Functions11

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

## VehSigCdng High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of VehSigCdng

### Data Flow Diagram

#### Component level DFD

Refer to FDD

#### Function level DFD

Refer to FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

See .m file

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module VehSigCdngInit1()

#### Periodic sub-module VehSigCdngPer1()

Design Rationale - Fault Injection client call is conditional compiled based on “FLTINJENA” build constant.

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Local Function #1

Refer to VehSpd block in the model

| Function Name | VehSigCdng_VehSpd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpdSerlCom_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehSpdOvrd_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdOvrdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehSpd_Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | N/A |  |  |  |

Function Name

VehSigCdng_VehSpd

Type

Min

Max

Arguments Passed

VehSpdSerlCom_Kph_T_f32

Float32

0

511

VehSpdVldSerlCom_Cnt_T_lgc

Boolean

FALSE

TRUE

VehSpdOvrd_Kph_T_f32

Float32

0

511

VehSpdOvrdVld_Cnt_T_logl

Boolean

FALSE

TRUE

VehSpd_Kph_T_f32

Float32

0

511

VehSpdVld_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

N/A

Notes: VehSpd_Kph_T_f32,  VehSpdVld_Cnt_T_logl are the outputs of the function

#### Local Function #2

Refer to VehLgtA block in the model

| Function Name | VehSigCdng_VehLgtA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLgtASerlCom_MpSecSq_T_f32 | Float32 | -180 | 180 |

|  | VehLgtAVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehLgtA_KphpS_T_f32 | Float32 | -50 | 50 |

|  | VehLgtAVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |

Function Name

VehSigCdng_VehLgtA

Type

Min

Max

Arguments Passed

VehLgtASerlCom_MpSecSq_T_f32

Float32

-180

180

VehLgtAVldSerlCom_Cnt_T_lgc

Boolean

FALSE

TRUE

VehLgtA_KphpS_T_f32

Float32

-50

50

VehLgtAVld_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

(if no value returned, write N/A)

Notes: VehLgtA_KphpS_T_f32, VehLgtAVld_Cnt_T_logl are the outputs of the function

#### Local Function #3

Refer to VehLatA block in the model

| Function Name | VehSigCdng_VehLatA | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLatASerlCom_MpSecSq_T_f32 | Float32 | -10 | 10 |

|  | VehLatAVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehLatA_MpSecSq_T_f32 | Float32 | -10 | 10 |

|  | VehLatAVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |

Function Name

VehSigCdng_VehLatA

Type

Min

Max

Arguments Passed

VehLatASerlCom_MpSecSq_T_f32

Float32

-10

10

VehLatAVldSerlCom_Cnt_T_lgc

Boolean

FALSE

TRUE

VehLatA_MpSecSq_T_f32

Float32

-10

10

VehLatAVld_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

(if no value returned, write N/A)

Notes: VehLatA_MpSecSq_T_f32, VehLatAVld_Cnt_T_logl are the outputs of the function

#### Local Function #4

Refer to VehYawRate block in the model

| Function Name | VehSigCdng_VehYawRate | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehYawRateSerlCom_DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVldSerlCom_Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehYawRate_DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |

Function Name

VehSigCdng_VehYawRate

Type

Min

Max

Arguments Passed

VehYawRateSerlCom_DegpS_T_f32

Float32

-120

120

VehYawRateVldSerlCom_Cnt_T_lgc

Boolean

FALSE

TRUE

VehYawRate_DegpS_T_f32

Float32

-120

120

VehYawRateVld_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

(if no value returned, write N/A)

Notes: VehYawRate_DegpS_T_f32, VehYawRateVld_Cnt_T_logl are the outputs of the function

#### Local Function #5

Refer to “Lateral Acceleration Estimation” block in the model

| Function Name | VehSigCdng_ LatAEstmn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehYawRate _DegpS_T_f32 | Float32 | -120 | 120 |

|  | VehYawRateVld _Cnt_T_lgc | Boolean | FALSE | TRUE |

|  | VehSpd _Kph_T_f32 | Float32 | 0 | 511 |

|  | VehSpdVld _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehLatAEstimd_MtrPerSecSqd_T_f32 | Float32 | -10 | 10 |

|  | VehLatAEstimdVld_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | (if no value returned, write N/A) |  |  |  |

Function Name

VehSigCdng_LatAEstmn

Type

Min

Max

Arguments Passed

VehYawRate_DegpS_T_f32

Float32

-120

120

VehYawRateVld_Cnt_T_lgc

Boolean

FALSE

TRUE

VehSpd_Kph_T_f32

Float32

0

511

VehSpdVld_Cnt_T_logl

Boolean

FALSE

TRUE

VehLatAEstimd_MtrPerSecSqd_T_f32

Float32

-10

10

VehLatAEstimdVld_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

(if no value returned, write N/A)

Notes: VehLatAEstimd_MtrPerSecSqd_T_f32, VehLatAEstimdVld_Cnt_T_logl  are the outputs of the function

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

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

| 5 | FDD – SF0 33 A_ VehSigCdng _Design | See Synergy Sub project ver s ion |

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

FDD – SF033A_VehSigCdng_Design

See Synergy Sub project version

Back to [Application Software](../).
