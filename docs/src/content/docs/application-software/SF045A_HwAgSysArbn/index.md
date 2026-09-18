---
title: "Handwheel Angle System Arbitration (SF045A_HwAgSysArbn)"
description: "Handwheel Angle System Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Angle System Arbitration component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF045A_HwAgSysArbn_Design` | Design package |
| `SF045A_HwAgSysArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF045A_HwAgSysArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF045A_HwAgSysArbn_Impl` |  |
| C sources | `HwAgSysArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAgSysArbn.dcf`, `HwAgSysArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAgSysArbn.dpa`, `RteGen.bat`, `SF045A_HwAgSysArbn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF045A_HwAgSysArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF045A_HwAgSysArbn_Impl/src/HwAgSysArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF045A_HwAgSysArbn_DDReport.txt`

- **Source path in repository:** `SF045A_HwAgSysArbn_Design/Reports/SF045A_HwAgSysArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF045A_HwAgSysArbn_DataDict
24-Jan-2017 12:47:27
Tool Release:  2.52.0



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
(variables: 4, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 9, errors: 0)

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
(variables: 15, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 2, errors: 0)

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
(variables: 14, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (35 more lines in the source file). ...*

### `HwAgSysArbn_Integration Manual.doc`

- **Source path in repository:** `SF045A_HwAgSysArbn_Impl/doc/HwAgSysArbn_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAgSysArbn_MDD.docx`

- **Source path in repository:** `SF045A_HwAgSysArbn_Impl/doc/HwAgSysArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `177 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAgSysArbn

DEC 07, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI,

CHENNAI, INDIA

Change History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sarika   Natu (KPIT Technologies) | 1.0 | 07-Sept-2015 |

| 2 | SF045A_HwAgSysArbn_Design  version 2 implementation | SB | 2.0 | 20-Jun-2016 |

| 3 | Updated to design version 2.2 .0 | TATA | 3 .0 | 07-Dec-16 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial Version

Sarika Natu(KPIT Technologies)

1.0

07-Sept-2015

2

SF045A_HwAgSysArbn_Design version 2 implementation

SB

2.0

20-Jun-2016

3

Updated to design version 2.2.0

TATA

3.0

07-Dec-16

Table of Contents

1HwAgSysArbn & High-Level Description5

2Design details of software module6

2.1Graphical representation of HwAgSysArbn6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: HwAgSysArbn_Init18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: HwAgSysArbn_Per18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function)………8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Design Rationale9

4.4.1.2Processing9

4.4.2Local Function #29

4.4.2.1Design Rationale9

4.4.2.2Processing9

4.5GLOBAL Function/Macro Definitions9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AReferences12

HwAgSysArbn & High-Level Description

The Handwheel angle system arbitration function accepts inputs from the various angle sources available in the EPS system and selects the angle source to be used for the system handwheel angle value. It also provides for compliance compensation of the angle value and determines the angle value and angle validity to be output on the vehicle data bus.

## Design details of software module

### Graphical representation of HwAgSysArbn

### Data Flow Diagram

See FDD.

#### Component level DFD

See FDD.

#### Function level DFD

See FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: HwAgSysArbn_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: HwAgSysArbn_Per1

### Design Rationale

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

| Function Name | HwAgVelSeriCom | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwAgCorrdConf_Uls_T_f32 | uint8 | 0 | 1 |

|  | HwAgSnsrlsConf_Uls_T_f32 | uint8 | 0 | 1 |

|  | HwAgCorrd_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | HwAgSnsrls_HwDeg_T_f32 | float32 | -1440 | 1440 |

|  | HwVel_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |

|  | PinionVelConf_Uls_T_f32 | float32 | 0.0F | 1.0F |

|  | * HwAgStsToSerlCom_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | * HwVelToSerlCom_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |

| Return Value | HwAgToSerlCom_HwDeg_T_f32 | float32 | -1440 | 1440 |

Function Name

HwAgVelSeriCom

Type

Min

Max

Arguments Passed

HwAgCorrdConf_Uls_T_f32

uint8

0

1

HwAgSnsrlsConf_Uls_T_f32

uint8

0

1

HwAgCorrd_HwDeg_T_f32

float32

-1440

1440

HwAgSnsrls_HwDeg_T_f32

float32

-1440

1440

HwVel_HwRadPerSec_T_f32

float32

-42.0F

42.0F

PinionVelConf_Uls_T_f32

float32

0.0F

1.0F

*HwAgStsToSerlCom_Cnt_T_lgc

boolean

FALSE

TRUE

*HwVelToSerlCom_HwRadPerSec_T_f32

float32

-42.0F

42.0F

Return Value

HwAgToSerlCom_HwDeg_T_f32

float32

-1440

1440

### Design Rationale

None

### Processing

Refer to the Handwheel signal serial communication arbitration functionality of “HwAgVelSeriCom” subsystem in the Simulink model.

### Local Function #2

| Function Name | CalcPinionVel | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float3 2 | -10.0F | 1 0.0F |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350.0F | 1 350.0F |

|  | MotVelVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | PinionAgConf_Uls_T_f32 | float32 | 0.0F | 1.0F |

|  | HwAg_HwDeg_T_f32 | float32 | -1440.0F | 1440.0F |

|  | *   PinionVel_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |

|  | *   PinionVelConf_Uls_T_f32 | float32 | 0.0F | 1 .0F |

| Return Value | HwVel_HwRadPerSec_T_f32 | float32 | -42.0F | 42.0F |

Function Name

CalcPinionVel

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10.0F

10.0F

MotVelCrf_MotRadPerSec_T_f32

float32

-1350.0F

1350.0F

MotVelVld_Cnt_T_logl

boolean

FALSE

TRUE

PinionAgConf_Uls_T_f32

float32

0.0F

1.0F

HwAg_HwDeg_T_f32

float32

-1440.0F

1440.0F

* PinionVel_HwRadPerSec_T_f32

float32

-42.0F

42.0F

* PinionVelConf_Uls_T_f32

float32

0.0F

1.0F

Return Value

HwVel_HwRadPerSec_T_f32

float32

-42.0F

42.0F

### Design Rationale

None

### Processing

Refer to the functionality of “CalcPinionVel” subsystem in the Simulink model.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

None

#### References

| Ref. # | Title | Version |

| --- | --- | --- |

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | Process Release  04.02.01 |

| 3 | Software Naming Conventions.doc | Process  Release  04.02.01 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | SF045A_HwAgSysArbn_Design | See Synergy subproject version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

Process Release 04.02.01

3

Software Naming Conventions.doc

Process Release 04.02.01

4

Software Design and Coding Standards.doc

2.1

5

SF045A_HwAgSysArbn_Design

See Synergy subproject version

Back to [Application Software](../).
