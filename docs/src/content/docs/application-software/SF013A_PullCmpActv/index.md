---
title: "Pull Compensation Active (SF013A_PullCmpActv)"
description: "Pull Compensation Active: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Pull Compensation Active component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF013A_PullCmpActv_Design` | Design package |
| `SF013A_PullCmpActv_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF013A_PullCmpActv_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF013A_PullCmpActv_Impl` |  |
| C sources | `PullCmpActv.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `PullCmpActv.dcf`, `PullCmpActv_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `PullCmpActv.dpa`, `RteGen.bat`, `SF013A_PullCmpActv_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF013A_PullCmpActv_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF013A_PullCmpActv_Impl/src/PullCmpActv.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF013A_PullCmpActv_DDReport.txt`

- **Source path in repository:** `SF013A_PullCmpActv_Design/Reports/SF013A_PullCmpActv_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF013A_PullCmpActv_DataDict
10-Jan-2017 17:06:23
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
(variables: 3, errors: 0)

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
PullCmpActvDi               	Name does not match required pattern.
PullCmpCustLrngDi           	Cannot match name to list of known Nexteer signals.
(variables: 13, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 1, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 33, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 1, errors: 0)

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
(variables: 21, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `PullCmpActv_IntegrationManual.doc`

- **Source path in repository:** `SF013A_PullCmpActv_Impl/doc/PullCmpActv_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `PullCmpActv_MDD.docx`

- **Source path in repository:** `SF013A_PullCmpActv_Impl/doc/PullCmpActv_MDD.docx`
- **Format:** `.docx`
- **Size:** `135 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Active Pull Compensation

Jan 17, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Akhil Krishna N D | 1.0 | 16-Oct-2015 |

| 2 | Updated to FDD version  SF013A_PullCmpActv_Design_1.4.0 | SB | 2.0 | 29 -Feb-2016 |

| 3 | Updated to design version  SF013A_PullCmpActv_Design_ 1.6.0 | SN | 3.0 | 20-Jun-2016 |

| 4 | Updated to design version 2.0.0 | ML | 4.0 | 17-Jan-2017 |

Sl. No.

Description

Author

Version

Date

1

Initial Version

Akhil Krishna N D

1.0

16-Oct-2015

2

Updated to FDD version SF013A_PullCmpActv_Design_1.4.0

SB

2.0

29-Feb-2016

3

Updated to design version SF013A_PullCmpActv_Design_1.6.0

SN

3.0

20-Jun-2016

4

Updated to design version 2.0.0

ML

4.0

17-Jan-2017

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2Active Pull Compensation & High-Level Description6

3Design details of software module7

3.1Graphical representation of Active Pull Compensation7

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: PullCmpActvInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: PullCmpActvPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.1.3Per: PullCmpActvPer210

5.1.3.1Design Rationale10

5.1.3.2Store Module Inputs to Local copies10

5.1.3.3(Processing of function)………10

5.1.3.4Store Local copy of outputs into Module Outputs10

5.2Server Runnables11

5.2.1GetPullCmpPrm11

5.2.1.1Design Rationale11

5.2.1.2(Processing of function)………11

5.2.2RstPullCmp11

5.2.2.1Design Rationale11

5.2.2.2(Processing of function)………11

5.2.3SetPullCmpLongTerm11

5.2.3.1Design Rationale11

5.2.3.2(Processing of function)………11

5.2.4SetPullCmpShoTerm11

5.2.4.1Design Rationale11

5.2.4.2(Processing of function)………11

5.3Interrupt Functions11

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Design Rationale12

5.4.1.2Processing12

5.4.2Local Function #212

5.4.2.1Design Rationale12

5.4.2.2Processing12

5.4.3Local Function #112

5.4.3.1Design Rationale13

5.4.3.2Processing13

5.5GLOBAL Function/Macro Definitions13

5.5.1GLOBAL Function #113

5.5.1.1Design Rationale13

5.5.1.2processing13

6Known Limitations with Design14

7UNIT TEST CONSIDERATION15

Appendix AAbbreviations and Acronyms16

Appendix BGlossary17

Appendix CReferences18

## Active Pull Compensation & High-Level Description

The Active Pull Compensation Function corrects vehicle pull issues by compensating for HW torque offsets detected by the steering system.  These torque offsets are classified as short-term and long-term, each of which is compensated for independently by the algorithm.  When the compensation is applied, the need for the driver to provide a constant input torque to counter these offsets is greatly reduced.

## Design details of software module

### Graphical representation of Active Pull Compensation

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

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

### Init: PullCmpActvInit1

### Design Rationale

None

### Module Outputs

None

### Per: PullCmpActvPer1

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Please refer FDD

### Store Local copy of outputs into Module Outputs

Please refer FDD

### Per: PullCmpActvPer2

### Design Rationale

Please refer FDD.

### Store Module Inputs to Local copies

Please refer FDD and design rationale noted above.

### (Processing of function)………

Please refer FDD.

### Store Local copy of outputs into Module Outputs

None

### Server Runnables

### GetPullCmpPrm

### Design Rationale

None

### (Processing of function)………

See GetPullCmpPrm block in FDD

### RstPullCmp

### Design Rationale

None

### (Processing of function)………

See RstPullCmp block in FDD

### SetPullCmpLongTerm

### Design Rationale

None

### (Processing of function)………

See SetPullCmpLongTerm block in FDD

### SetPullCmpShoTerm

### Design Rationale

None

### (Processing of function)………

See SetPullCmpShoTerm block in FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | ActvCmpEna | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PullCmpActvShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AbslHwTqFild_HwNwtMtr_T_f32 | float32 | 0 .0 | 10 .0 |

|  | AbslHwAg_HwDeg_T_f32 | float32 | 0 .0 | 1440 .0 |

|  | AbslVehYawRateFild_VehDegPerSec_T_f32 | float32 | 0 .0 | 128 .0 |

|  | AbslVehLatA_MtrPerSecSqd_T_f32 | float32 | 0.0 | 10.0 |

|  | PinionAgConf_Uls_T_f32 | float32 | 0 .0 | 1 .0 |

|  | VehSpd_Kph_T_f32 | float32 | 0 .0 | 511 .0 |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AbslHwVel_HwRadPerSec_T_f32 | float32 | 0 .0 | 42 .0 |

|  | PullCmpCustLrngDi_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehYawRateVld_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | LrngEnad_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ActvCmpEna

Type

Min

Max

Arguments Passed

PullCmpActvShoTermRst_Cnt_T_logl

boolean

FALSE

TRUE

AbslHwTqFild_HwNwtMtr_T_f32

float32

0.0

10.0

AbslHwAg_HwDeg_T_f32

float32

0.0

1440.0

AbslVehYawRateFild_VehDegPerSec_T_f32

float32

0.0

128.0

AbslVehLatA_MtrPerSecSqd_T_f32

float32

0.0

10.0

PinionAgConf_Uls_T_f32

float32

0.0

1.0

VehSpd_Kph_T_f32

float32

0.0

511.0

VehSpdVld_Cnt_T_logl

boolean

FALSE

TRUE

AbslHwVel_HwRadPerSec_T_f32

float32

0.0

42.0

PullCmpCustLrngDi_Cnt_T_logl

Boolean

FALSE

TRUE

VehYawRateVld_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

LrngEnad_Cnt_T_logl

boolean

FALSE

TRUE

### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “ActvCmpEna” block of the Simulink model of the design.

### Local Function #2

| Function Name | CalcIntgrGain | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 .0 | 10 .0 |

|  | PullCmpShoTermPrev_HwNwtMtr_T_f32 | float32 | -10 .0 | 10 .0 |

| Return Value | IntgtrGainShoTerm_Uls_T_f32 | float32 | 0 .0 | 1 .0 |

Function Name

CalcIntgrGain

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10.0

10.0

PullCmpShoTermPrev_HwNwtMtr_T_f32

float32

-10.0

10.0

Return Value

IntgtrGainShoTerm_Uls_T_f32

float32

0.0

1.0

### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “CalcIntgtrGain” block of the Simulink model of the design

### Local Function #3

| Function Name | ErrIntgtrActvLim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PullCmpActvShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

|  | IntgtrGainShoTerm_Uls_T_f32 | float32 | 0 .0 | 1 .0 |

|  | PullErrShoTerm_HwNwtMtr_T_f32 | float32 | - 10 .0 | 10 .0 |

|  | PullCmpShoTermPrev_HwNwtMtr_T_f32 | float32 | -10 .0 | 10 .0 |

|  | RampDwnStepSize_HwNwtMtr_T_f32 | float32 | 0 .0 | 0.6 |

|  | ShoTermRst_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | PullCmpShoTerm_HwNwtMtr_T_f32 | float32 | - 10 .0 | 10 .0 |

Function Name

ErrIntgtrActvLim

Type

Min

Max

Arguments Passed

PullCmpActvShoTermRst_Cnt_T_logl

boolean

FALSE

TRUE

IntgtrGainShoTerm_Uls_T_f32

float32

0.0

1.0

PullErrShoTerm_HwNwtMtr_T_f32

float32

-10.0

10.0

PullCmpShoTermPrev_HwNwtMtr_T_f32

float32

-10.0

10.0

RampDwnStepSize_HwNwtMtr_T_f32

float32

0.0

0.6

ShoTermRst_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

PullCmpShoTerm_HwNwtMtr_T_f32

float32

-10.0

10.0

### Design Rationale

None

### Processing

(Place flowchart/design for local function)

Refer to the “ErrIntgtr&ActvLim” block of the Simulink model of the design.

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

None

### Design Rationale

### processing

(Place flowchart/design for local function)

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

| 2 | MDD Guideline | Process release 04.02.01 |

| 3 | Software Naming Conventions.doc | Process release 04.02.01 |

| 4 | Software Design and Coding Standards.doc | Process release 04.02.01 |

| 5 | FDD : SF013A_PullCmpActv_Design | See Synergy sub project version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

Process release 04.02.01

3

Software Naming Conventions.doc

Process release 04.02.01

4

Software Design and Coding Standards.doc

Process release 04.02.01

5

FDD : SF013A_PullCmpActv_Design

See Synergy sub project version

Back to [Application Software](../).
