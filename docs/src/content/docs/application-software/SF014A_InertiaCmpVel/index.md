---
title: "Inertia Compensation Velocity (SF014A_InertiaCmpVel)"
description: "Inertia Compensation Velocity: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Inertia Compensation Velocity component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF014A_InertiaCmpVel_Design` | Design package |
| `SF014A_InertiaCmpVel_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF014A_InertiaCmpVel_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF014A_InertiaCmpVel_Impl` |  |
| C sources | `InertiaCmpVel.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `InertiaCmpVel.dcf`, `InertiaCmpVel_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `InertiaCmpVel.dpa`, `RteGen.bat`, `SF014A_InertiaCmpVel_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF014A_InertiaCmpVel_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF014A_InertiaCmpVel_Impl/src/InertiaCmpVel.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF014A_InertiaCmpVel_DDReport.txt`

- **Source path in repository:** `SF014A_InertiaCmpVel_Design/Reports/SF014A_InertiaCmpVel_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF014A_InertiaCmpVel_DataDict
19-Sep-2016 14:05:20
Tool Release:  2.46.0



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
InertiaCmpVelCmdDi          	Name does not match required pattern.
(variables: 8, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
InertiaCmpVelCmd            	Name does not match required pattern.
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
(variables: 3, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 11, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 9, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (34 more lines in the source file). ...*

### `InertiaCmpVel_IntegrationManual.docx`

- **Source path in repository:** `SF014A_InertiaCmpVel_Impl/doc/InertiaCmpVel_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

InertiaCmpVel

VERSION: 1.0

DATE: 23-Jul-2015

Prepared By:

Spandana Balani

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | SB | 1.0 | 23-July-2015 |

|  |  |  |  |  |

|  |  |  |  |  |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial version

SB

1.0

23-July-2015

Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3Da Vinci Parameter Configuration Changes7

4.4DaVinci Interrupt Configuration Changes7

4.5Manual Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  | <ADD  more to the table if applicable> |

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

<ADD  more to the table if applicable>

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| < 1 > | < MDD Guidelines > | Process 4. 0 1 .00 |

| <2> | < Software Naming Conventions > | Process 4. 0 1 .00 |

| <3> | <Coding  standards > | Process 4. 0 1 .00 |

| <4> | FDD – SF014 A_InertiaCmpVel_Design | See Synergy Subproject version |

|  |  |  |

Sr. No.

Title

Version

<1>

<MDD Guidelines>

Process 4.01.00

<2>

<Software Naming Conventions>

Process 4.01.00

<3>

<Coding standards>

Process 4.01.00

<4>

FDD – SF014A_InertiaCmpVel_Design

See Synergy Subproject version

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

Module

Required Feature

None

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config

| Modules | Notes |  |

| --- | --- | --- |

| FLTINJENA | Set to  STD_ON  for Fault injection |  |

Modules

Notes

FLTINJENA

Set to STD_ON for Fault injection

### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes

| Parameter | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |

Parameter

Notes

SWC

N/A

### DaVinci Interrupt Configuration Changes

| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| N/A |  |  |  |

ISR Name

VIM #

Priority Dependency

Notes

N/A

### Manual Configuration Changes

| Constant | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |

Constant

Notes

SWC

N/A

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

No

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| InertiaCmpVelInit1 | On  Init | RTE _Init |

Init

Scheduling Requirements

Trigger

InertiaCmpVelInit1

On Init

RTE_Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| InertiaCmpVelPer1 | None | RTE (2 ms) |

Runnable

Scheduling Requirements

Trigger

InertiaCmpVelPer1

None

RTE(2ms)

.

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |

|  |  |  |

Memory Section

Contents

Notes

None

* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage

| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |

Feature

RAM

ROM

None

Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `InertiaCmpVel_MDD.docx`

- **Source path in repository:** `SF014A_InertiaCmpVel_Impl/doc/InertiaCmpVel_MDD.docx`
- **Format:** `.docx`
- **Size:** `159 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

InertiaCmpVel

Jul 14, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| SNo | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | SB | 1.0 | 23-Jul-2015 |

| 2 | Updated  to version 1.3.0 of design | SB | 2.0 | 11-Mar-2016 |

| 3 | Updated to version 1.7.0 and 1.8.0 of design | KK | 3.0 | 21-Jun-2016 |

| 4 | Updated to version 1. 9.0  of design | KK | 4 .0 | 1 4 -Ju l -2016 |

SNo

Description

Author

Version

Date

1

Initial Version

SB

1.0

23-Jul-2015

2

Updated to version 1.3.0 of design

SB

2.0

11-Mar-2016

3

Updated to version 1.7.0 and 1.8.0 of design

KK

3.0

21-Jun-2016

4

Updated to version 1.9.0 of design

KK

4.0

14-Jul-2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2InertiaCmpVel & High-Level Description5

3Design details of software module6

3.1Graphical representation of InertiaCmpVel6

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1.1Sub-Module Functions9

5.1.2Interrupt Service Routines9

5.1.3Server Runnable Functions9

5.1.4Module Internal (Local) Functions9

5.1.5Transition Functions11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

## InertiaCmpVel & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of InertiaCmpVel

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

#### Global Constants

Refer .m file

#### User defined typedef definition/declaration

This section documents any user types uniquely used for the module.

| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| typedef  struct   FilCoeffRec | b0_Uls_f32 | Float32 | FULL | FULL |

|  | b1_Uls_f32 | Float32 | FULL | FULL |

|  | b2_Uls_f32 | Float32 | FULL | FULL |

|  | a0_Uls_f32 | Float32 | FULL | FULL |

|  | a1_Uls_f32 | Float32 | FULL | FULL |

|  | a2_Uls_f32 | Float32 | FULL | FULL |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

typedef struct FilCoeffRec

b0_Uls_f32

Float32

FULL

FULL

b1_Uls_f32

Float32

FULL

FULL

b2_Uls_f32

Float32

FULL

FULL

a0_Uls_f32

Float32

FULL

FULL

a1_Uls_f32

Float32

FULL

FULL

a2_Uls_f32

Float32

FULL

FULL

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module InertiaCmpVelInit1()

Design Rational:

Init function is not present in the model but in reference to the Init.txt  text file Low pass filter and Notch filter are initialized.

For Low pass filter standard EA4 LPF implementation from NxtrFil.h is followed and for Notch filter initialization, EA3 implementation is followed.

#### Periodic sub-module InertiaCmpVelPer1()

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Calculate Driver Velocity

| Function Name | DrvrVelCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1 350 | 1 350 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 51 1 |

| Return Value | ScadDrvrVel_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

Function Name

DrvrVelCalc

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10

10

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

VehSpd_Kph_T_f32

float32

0

511

Return Value

ScadDrvrVel_MotRadPerSec_T_f32

float32

-1350

1350

#### Calculate ADD Coefficient

| Function Name | ADDCoeffCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AssiCmdBas_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | WhlImbRejctnAmp_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 51 1 |

| Return Value | ADDCoeffCalc_MotNwtMtrSpRad_T_f32 | float32 | 0.0 | 0.00007 |

Function Name

ADDCoeffCalc

Type

Min

Max

Arguments Passed

AssiCmdBas_MotNwtMtr_T_f32

float32

-8.8

8.8

WhlImbRejctnAmp_MotNwtMtr_T_f32

float32

0

8.8

VehSpd_Kph_T_f32

float32

0

511

Return Value

ADDCoeffCalc_MotNwtMtrSpRad_T_f32

float32

0.0

0.00007

#### Calculate Gain

| Function Name | DecelGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehLgtA_KphPerSec_T_f32 | float32 | - 35 | 35 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1 350 | 1 350 |

| Return Value | DecelGain_Uls_T_f32 | float32 | 0 | 1 |

Function Name

DecelGain

Type

Min

Max

Arguments Passed

VehLgtA_KphPerSec_T_f32

float32

-35

35

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

Return Value

DecelGain_Uls_T_f32

float32

0

1

#### Calculate Filter Coefficients

| Function Name | FilCoeffCalc | Type | Min | Max |  |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | ADDCoeff_MotNwtMtrPerMotRadPerSec_T_f32 | float32 | 0.0 | 0.041306 |  |

|  | WhlImbRejctnAmp_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |  |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 51 1 |  |

| Return Value | * FilCoeff_T_Rec | b0_Uls_f32 | float32 | -2.74156205240179 | 0 |

|  |  | b1_Uls_f32 | float32 | 0.0 | 0.330448 |

|  |  | b2_Uls_f32 | float32 | -0.160083862455113 | 2.41111405240179 |

|  |  | a0_Uls_f32 | float32 | 0.5525885 | 3.9498924 |

|  |  | a1_Uls_f32 | float32 | -7. 9996842 | -4.8417266 |

|  |  | a2_Uls_f32 | float32 | 4.0504234 | 10.6056849 |

Function Name

FilCoeffCalc

Type

Min

Max

Arguments Passed

ADDCoeff_MotNwtMtrPerMotRadPerSec_T_f32

float32

0.0

0.041306

WhlImbRejctnAmp_MotNwtMtr_T_f32

float32

0

8.8

VehSpd_Kph_T_f32

float32

0

511

Return Value

*FilCoeff_T_Rec

b0_Uls_f32

float32

-2.74156205240179

0

b1_Uls_f32

float32

0.0

0.330448

b2_Uls_f32

float32

-0.160083862455113

2.41111405240179

a0_Uls_f32

float32

0.5525885

3.9498924

a1_Uls_f32

float32

-7.9996842

-4.8417266

a2_Uls_f32

float32

4.0504234

10.6056849

#### Generate Command

| Function Name | GenFddIcCmd | Type | Min | Max |  |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | ScadDrvrVel_MotRadPerSec_T_f32 | float32 | - 7226.652 | 7226.652 |  |

|  | * FilCoeff_T_Rec | b0_Uls_f32 | float32 | -2.74156205240179 | 0 |

|  |  | b1_Uls_f32 | float32 | 0.0 | 0.330448 |

|  |  | b2_Uls_f32 | float32 | -0.166262133009164 | 2.41111405240179 |

|  |  | a0_Uls_f32 | float32 | 0.5525885 | 3.9498924 |

|  |  | a1_Uls_f32 | float32 | -7. 9996842 | -4.8417266 |

|  |  | a2_Uls_f32 | float32 | 4.0504234 | 10.6056849 |

| Return Value | InertiaCmp_MotNwtMtr_T_f32 | Float | -8.8 | 8.8 |  |

Function Name

GenFddIcCmd

Type

Min

Max

Arguments Passed

ScadDrvrVel_MotRadPerSec_T_f32

float32

-7226.652

7226.652

*FilCoeff_T_Rec

b0_Uls_f32

float32

-2.74156205240179

0

b1_Uls_f32

float32

0.0

0.330448

b2_Uls_f32

float32

-0.166262133009164

2.41111405240179

a0_Uls_f32

float32

0.5525885

3.9498924

a1_Uls_f32

float32

-7.9996842

-4.8417266

a2_Uls_f32

float32

4.0504234

10.6056849

Return Value

InertiaCmp_MotNwtMtr_T_f32

Float

-8.8

8.8

#### NotchCmp

| Function Name | NotchCmp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | InertiaCmp_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | NotchCmp   _ MotNwtMtr _T_f32 | float32 | -8.8 | 8.8 |

Function Name

NotchCmp

Type

Min

Max

Arguments Passed

VehSpd_Kph_T_f32

float32

0

511

InertiaCmp_MotNwtMtr_T_f32

float32

-8.8

8.8

Return Value

NotchCmp _MotNwtMtr_T_f32

float32

-8.8

8.8

#### FilNotchFullUpdOutp_f32

| Function Name | FilNotchFullUpdOutp _f32 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | None |  |  |  |

Function Name

FilNotchFullUpdOutp_f32

Type

Min

Max

Arguments Passed

Inp

float32

See unit test consideration

FilNotchStRecPtr

FilNotchStRec1

FilNotchGainRecPtr

FilNotchGainRec1

Return Value

None

#### Description

Notch filter output calculation implemented based on ‘Inertia Comp Notch’ block functionality.

#### FilNotchInit

| Function Name | FilNotchInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | FilOut | float32 |  |  |

Function Name

FilNotchInit

Type

Min

Max

Arguments Passed

Inp

float32

See unit test consideration

FilNotchStRecPtr

FilNotchStRec1

FilNotchGainRecPtr

FilNotchGainRec1

Return Value

FilOut

float32

#### Description

Notch filter initialization function implemented based on EA3 design.

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

Since the notch filter implementation used in this module is dynamic in nature, absolute ranges are difficult to determine without pre-defined knowledge on the combination of coefficient values (A1, A2, B0, B1, B2).  Because of this, the systems group ran simulations on 10 different combinations of coefficients (2 with defined default calibrations, 8 considered extreme cases of notch filters) and logged the ranges of the filter state variables and outputs during a frequency sweep.  The ranges given throughout this module were taken as the worst case results of all of the given test cases.

To provide useful cases for unit testing, the boundary checks tested during unit testing should be altered to test the state variable minimum and maximum for each of the 10 test cases with the given coefficients set to the values given in that test case.  In the case where the default values of the coefficients are used in a vector, the unit tester should not test the corresponding state variables with values over the range defined for that set of coefficients.  See attached simulation results.

GenFddIcCmd function is designed to work with argument values from the calling function as used with the other functions in the module, and outputs may be out of the expected range if tested with arbitrary combinations of input values.  Unit testing of this function should use only passed argument value combinations coming from the calling function.

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

| 5 | FDD – SF014A_InetiaCmpVel_Design | See Synergy Sub project version |

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

FDD – SF014A_InetiaCmpVel_Design

See Synergy Sub project version

Back to [Application Software](../).
