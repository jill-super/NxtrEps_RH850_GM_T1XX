---
title: "End of Travel Protection (SF018A_EotProtn)"
description: "End of Travel Protection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The End of Travel Protection component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF018A_EotProtn_Design` | Design package |
| `SF018A_EotProtn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF018A_EotProtn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF018A_EotProtn_Impl` |  |
| C sources | `EotProtn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `EotProtn.dcf`, `EotProtn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `EotProtn.dpa`, `RteGen.bat`, `SF018A_EotProtn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF018A_EotProtn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF018A_EotProtn_Impl/src/EotProtn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF018A_EotProtn_DDReport.txt`

- **Source path in repository:** `SF018A_EotProtn_Design/Reports/SF018A_EotProtn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF018A_EotProtn_DataDict
05-Oct-2016 17:55:07
Tool Release:  2.48.0



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
EotProtnDi                  	Name does not match required pattern.
(variables: 11, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 4, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 33, errors: 0)

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
(variables: 9, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `EotProtn_Integration Manual.doc`

- **Source path in repository:** `SF018A_EotProtn_Impl/doc/EotProtn_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `EotProtn_MDD.docx`

- **Source path in repository:** `SF018A_EotProtn_Impl/doc/EotProtn_MDD.docx`
- **Format:** `.docx`
- **Size:** `154 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

EotProtn

Jul 1, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Spandana Balani,

Change History

| SNo . | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sarika   Natu (KPIT Technologies) | 1.0 | 01-Oct-2015 |

| 2 | Implemented  SF018A design version 1.5.0 | SB | 2.0 | 01-Jul-2016 |

SNo.

Description

Author

Version

Date

1

Initial Version

Sarika Natu(KPIT Technologies)

1.0

01-Oct-2015

2

Implemented SF018A design version 1.5.0

SB

2.0

01-Jul-2016

Table of Contents

1EotProtn & High-Level Description5

2Design details of software module6

2.1Graphical representation of EotProtn6

2.2Data Flow Diagram7

2.2.1Component level DFD7

2.2.2Function level DFD7

3Constant Data Dictionary8

3.1Program (fixed) Constants8

3.1.1Embedded Constants8

4Software Component Implementation9

4.1Sub-Module Functions9

4.1.1Init: EotProtn_Init19

4.1.1.1Design Rationale9

4.1.1.2Module Outputs9

4.1.2Per: EotProtn_Per19

4.1.2.1Design Rationale9

4.1.2.2Store Module Inputs to Local copies9

4.1.2.3(Processing of function)………9

4.1.2.4Store Local copy of outputs into Module Outputs9

4.2Server Runables9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.4.1Local Function #19

4.4.1.1Design Rationale10

4.4.1.2Processing10

4.4.2Local Function #210

4.4.2.1Design Rationale10

4.4.2.2Processing10

4.4.3Local Function #310

4.4.3.1Design Rationale10

4.4.3.2Processing10

4.4.4Local Function #411

4.4.4.1Design Rationale11

4.4.4.2Processing11

4.4.5Local Function #511

4.4.5.1Design Rationale11

4.4.5.2Processing11

4.4.6Local Function #611

4.4.6.1Design Rationale11

4.4.6.2Processing11

4.4.7Local Function #711

4.4.7.1Design Rationale12

4.4.7.2Processing12

4.4.8Local Function #812

4.4.8.1Design Rationale12

4.4.8.2Processing12

4.4.9Local Function #912

4.4.9.1Design Rationale13

4.4.9.2Processing13

4.5GLOBAL Function/Macro Definitions13

5Known Limitations with Design14

6UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## EotProtn & High-Level Description

The End of Travel Protection function specifies performance attributes as the steering system approaches the mechanical end of travel of the steering gear.

## Design details of software module

### Graphical representation of EotProtn

### Data Flow Diagram

See FDD

#### Component level DFD

See FDD

#### Function level DFD

See FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant | Value |

| --- | --- |

| DAMPGPTSIZE_CNT_U08 | 2 |

| DAMPGVEHSPDSIZE_CNT_U08 | 4 |

| GAINVEHSPDSIZE_CNT_U08 | 5 |

Constant

Value

DAMPGPTSIZE_CNT_U08

2

DAMPGVEHSPDSIZE_CNT_U08

4

GAINVEHSPDSIZE_CNT_U08

5

## Software Component Implementation

### Sub-Module Functions

### Init: EotProtn_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: EotProtn_Per1

### Design Rationale

EotProtn_Per1 function is divided into various functions to reduce the cyclomatic complexity.

The limiting of ‘EotAssiSca’ output is performed in SoftEndStop subsystem in FDD. But in code it is limiting calculations are done where the output is calculated i.e. FildEotGain function.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | EotVelImpct | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | EotMotTqLim_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

Function Name

EotVelImpct

Type

Min

Max

Arguments Passed

HwAgEotCw_HwDeg_T_f32

float32

360

900

HwAgEotCcw_HwDeg_T_f32

float32

-900

-360

HwAg_HwDeg_T_f32

float32

-1440

1440

VehSpd_Kph_T_f32

float32

0

511

HwAgAuthy_Uls_T_f32

float32

0

1

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

Return Value

EotMotTqLim_MotNwtMtr_T_f32

float32

0

8.8

### Design Rationale

None

Note: Outputs of “EotVelImpct” function is - EotMotTqLim_MotNwtMtr_T_f32.

### Processing

Refer to the “EotVelImpct” subsystem of the Simulink model of the design

### Local Function #2

| Function Name | LimPosnDetd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RackTrvlLimrRngEna_Cnt_T_lo gl | boolean | False | True |

|  | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

| Return Value | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

Function Name

LimPosnDetd

Type

Min

Max

Arguments Passed

RackTrvlLimrRngEna_Cnt_T_logl

boolean

False

True

HwAgEotCw_HwDeg_T_f32

float32

360

900

HwAgEotCcw_HwDeg_T_f32

float32

-900

-360

HwAg_HwDeg_T_f32

float32

-1440

1440

Return Value

LimPosn_HwDeg_T_f32

float32

-1440

1440

### Design Rationale

None

Note: Outputs of “LimPosnDetd” function is - LimPosn_HwDeg_T_f32.

### Processing

Refer to the “LimPosnDetd” subsystem of the Simulink model of the design

### Local Function #3

| Function Name | CalcEntrGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

| Return Value | EntrGain_Uls_T_f32 | float32 | 0 | 1 |

Function Name

CalcEntrGain

Type

Min

Max

Arguments Passed

HwAg_HwDeg_T_f32

float32

-1440

1440

VehSpd_Kph_T_f32

float32

0

511

LimPosn_HwDeg_T_f32

float32

-1440

1440

Return Value

EntrGain_Uls_T_f32

float32

0

1

### Design Rationale

None

Note: Outputs of “CalcEntrGain” function is - EntrGain_Uls_T_f32.

### Processing

Refer to the “CalcEntrGain” subsystem of the Simulink model of the design

### Local Function #4

| Function Name | CalcExitGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | ExitGain_Uls_T_f32 | float32 | 0 | 1 |

Function Name

CalcExitGain

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10

10

Return Value

ExitGain_Uls_T_f32

float32

0

1

### Design Rationale

Calculation of Filtered Handwheel torque is done after ‘CalcExitGain’ function is executed.

Note: Outputs of “CalcExitGain” function is - FildHwTq_HwNwtMtr_T_f32

### Processing

Refer to the “CalcExitGain” subsystem of the Simulink model of the design

### Local Function #5

| Function Name | CalcEotGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EntrGain_Uls_T_f32 | float32 | 0 | 1 |

|  | ExitGain_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | EotGain_Uls_T_f32 | float32 | 0 | 1 |

Function Name

CalcEotGain

Type

Min

Max

Arguments Passed

EntrGain_Uls_T_f32

float32

0

1

ExitGain_Uls_T_f32

float32

0

1

Return Value

EotGain_Uls_T_f32

float32

0

1

### Design Rationale

None

Note: Outputs of “CalcEotGain” function is - EotGain_Uls_T_f32

### Processing

Refer to the “CalcEotGain” subsystem of the Simulink model of the design

### Local Function #6

| Function Name | FildEotGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EotGain_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | EotAssiSca_Uls_T_f32 | float32 | 0 | 1 |

Function Name

FildEotGain

Type

Min

Max

Arguments Passed

EotGain_Uls_T_f32

float32

0

1

Return Value

EotAssiSca_Uls_T_f32

float32

0

1

### Design Rationale

Limit of EotAssiSca is moved to local function FildEotGain.

Note: Outputs of “FildEotGain” function is - EotAssiSca_Uls_T_f32

### Processing

Refer to the “FildEotGain” subsystem of the Simulink model of the design

### Local Function #7

| Function Name | CalcEotDampg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAgEotCw_HwDeg_T_f32 | float32 | 360 | 900 |

|  | HwAgEotCcw_HwDeg_T_f32 | float32 | -900 | -360 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

| Return Value | EotDampgCmd_MotNwtMtr_T_f32 | float32 | - 8.8 | 8.8 |

Function Name

CalcEotDampg

Type

Min

Max

Arguments Passed

HwAg_HwDeg_T_f32

float32

-1440

1440

VehSpd_Kph_T_f32

float32

0

511

HwAgEotCw_HwDeg_T_f32

float32

360

900

HwAgEotCcw_HwDeg_T_f32

float32

-900

-360

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

Return Value

EotDampgCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

### Design Rationale

None

Note: Outputs of “CalcEotDampg” function is - EotDampgCmd_MotNwtMtr_T_f32

### Processing

Refer to the “CalcEotDampg” calculation of the Simulink model of the design

### Local Function #8

| Function Name | EotActvCmdCalc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RackTrvlLimrDi_Cnt_T_ l ogl | boolean | False | True |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

| Return Value | EotActvCmd_MotNwtMtr_T_f32 | float32 | - 8.8 | 8.8 |

Function Name

EotActvCmdCalc

Type

Min

Max

Arguments Passed

RackTrvlLimrDi_Cnt_T_logl

boolean

False

True

HwAgAuthy_Uls_T_f32

float32

0

1

VehSpd_Kph_T_f32

float32

0

511

HwAg_HwDeg_T_f32

float32

-1440

1440

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

LimPosn_HwDeg_T_f32

float32

-1440

1440

Return Value

EotActvCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

### Design Rationale

None

Note: Outputs of “EotActvCmdCalc” function is - EotActvCmd_MotNwtMtr_T_f32

### Processing

Refer to the “EotActvCmdCalc” calculation of the Simulink model of the design

### Local Function #9

| Function Name | SoftEndStopStCtrl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | HwAgAuthy_Uls_T_f32 | float32 | 0 | 1 |

|  | EotProtnDi_Cnt_T_Logl | boolean | 0 | 1 |

|  | EotDetd_Cnt_T_Logl | boolean | 0 | 1 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | FildHwTq_HwNwtMtr_T_f32 | float32 | -3.4E+38 | 3.4E+38 |

|  | SysMotTqCmdSca_Uls_T_f32 | float32 | 0 | 1 |

|  | LimPosn_HwDeg_T_f32 | float32 | -1440 | 1440 |

| Return Value | None | float32 | - 8.8 | 8.8 |

Function Name

SoftEndStopStCtrl

Type

Min

Max

Arguments Passed

VehSpd_Kph_T_f32

float32

0

511

HwAgAuthy_Uls_T_f32

float32

0

1

EotProtnDi_Cnt_T_Logl

boolean

0

1

EotDetd_Cnt_T_Logl

boolean

0

1

HwAg_HwDeg_T_f32

float32

-1440

1440

FildHwTq_HwNwtMtr_T_f32

float32

-3.4E+38

3.4E+38

SysMotTqCmdSca_Uls_T_f32

float32

0

1

LimPosn_HwDeg_T_f32

float32

-1440

1440

Return Value

None

float32

-8.8

8.8

### Design Rationale

None

### Processing

Refer to the “SoftEndStopStCtrl” calculation of the Simulink model of the design

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### Abbreviations and Acronyms

| Abbreviation  or Acronym | Description |

| --- | --- |

| FDD | Functional Design Document |

Abbreviation or Acronym

Description

FDD

Functional Design Document

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

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | Process release 04.02.01 |

| 2 | MDD Guideline | Process release 04.02.01 |

| 3 | Software Naming Conventions.doc | Process release 04.02.01 |

| 4 | Software Design and Coding Standards.doc | Process release 04.02.01 |

| 5 | SF018A_EotProtn_Design | See Synergy subproject version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

Process release 04.02.01

2

MDD Guideline

Process release 04.02.01

3

Software Naming Conventions.doc


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Application Software](../).
