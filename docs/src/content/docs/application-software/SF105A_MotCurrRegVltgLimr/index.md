---
title: "Motor Current Regulator Voltage Limiter (SF105A_MotCurrRegVltgLimr)"
description: "Motor Current Regulator Voltage Limiter: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Current Regulator Voltage Limiter component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF105A_MotCurrRegVltgLimr_Design` | Design package |
| `SF105A_MotCurrRegVltgLimr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF105A_MotCurrRegVltgLimr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF105A_MotCurrRegVltgLimr_Impl` |  |
| C sources | `CDD_MotCurrRegVltgLimr.c`, `CDD_MotCurrRegVltgLimr_MotCtrl.c` |
| Public headers | `CDD_MotCurrRegVltgLimr.h`, `CDD_MotCurrRegVltgLimr_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotCurrRegVltgLimr.dcf`, `MotCurrRegVltgLimr_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotCurrRegVltgLimr.dpa`, `RteGen.bat`, `SF105A_MotCurrRegVltgLimr_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF105A_MotCurrRegVltgLimr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `SF105A_MotCurrRegVltgLimr_Impl/src/CDD_MotCurrRegVltgLimr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `SF105A_MotCurrRegVltgLimr_Impl/src/CDD_MotCurrRegVltgLimr_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF105A_MotCurrRegVltgLimr_DDReport.txt`

- **Source path in repository:** `SF105A_MotCurrRegVltgLimr_Design/Reports/SF105A_MotCurrRegVltgLimr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF105A_MotCurrRegVltgLimr_DataDict
04-Nov-2016 14:12:03
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
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 27, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 5, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 17, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 5, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 28, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 11, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `MotCurrRegVltgLimr_Integration Manual.docx`

- **Source path in repository:** `SF105A_MotCurrRegVltgLimr_Impl/doc/MotCurrRegVltgLimr_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘MotCurrRegVltgLimr’

VERSION: 1.0

DATE: 26-May-2015

Prepared By:

Selva Sengottaiyan

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva   Sengottaiyan | 1.0 | 4 - June -2015 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial version

Selva Sengottaiyan

1.0

4-June-2015

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

7.3Non  RTE NvM Blocks10

7.4RTE NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD  –   SF105 A_ MotCurrRegVltgLimr _Design | See Synergy  sub  project version |

| 2 | Software Naming Conventions | Process  4 .0 0 .00 |

| 3 | Software Design and Coding Standards | Process  4.00.00 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – SF105A_MotCurrRegVltgLimr_Design

See Synergy sub project version

2

Software Naming Conventions

Process 4.00.00

3

Software Design and Coding Standards

Process 4.00.00

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

| None |  |  |

Modules

Notes

None

### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes

| Parameter | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Parameter

Notes

SWC

None

### DaVinci Interrupt Configuration Changes

| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| None |  |  |  |

ISR Name

VIM #

Priority Dependency

Notes

None

### Manual Configuration Changes

| Constant | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Constant

Notes

SWC

None

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file in the FDD

### Required Global Data Outputs

Refer DataDict.m file file in the FDD

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotCurrRegVltgLimr Init 1 | None | Init |

Init

Scheduling Requirements

Trigger

MotCurrRegVltgLimrInit1

None

Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotCurrRegVltgLimr Per1 |  | Motor Control ISR*2 |

Runnable

Scheduling Requirements

Trigger

MotCurrRegVltgLimrPer1

Motor Control ISR*2

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotCtrl_START_SEC_CODE | Code section for Motor Control scheduled functions |  |

|  |  |  |

Memory Section

Contents

Notes

MotCtrl_START_SEC_CODE

Code section for Motor Control scheduled functions

* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage

| Feature | RAM | ROM |

| --- | --- | --- |

| < Memmap   usuage  info> |  |  |

Feature

RAM

ROM

<Memmap usuage info>

Table 1: ARM Cortex R4 Memory Usage

### Non  RTE NvM Blocks

| Block Name |

| --- |

| None |

Block Name

None

### RTE NvM Blocks

| Block Name |

| --- |

| none |

Block Name

none

## Compiler Settings

### Preprocessor MACRO

None.

### Optimization Settings

None

## Appendix

None

### `MotCurrRegVltgLimr_MDD.docx`

- **Source path in repository:** `SF105A_MotCurrRegVltgLimr_Impl/doc/MotCurrRegVltgLimr_MDD.docx`
- **Format:** `.docx`
- **Size:** `125 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘MotCurrRegVltgLimr’

VERSION: 4.0

DATE: 04-Jan-2017

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Selva   Sengottaiyan | 1.0 | 26 - May -2015 |

| 2 | Updated graphical representation  and added local function information | Nick Saxton | 2.0 | 13-Apr-2016 |

| 3 | Updated for FDD v2.1 .0 | Matthew Leser | 3.0 | 7-Nov-2016 |

| 4 | Updated to fix Anomaly EA4#9045 | Matthew Leser | 4.0 | 04-Jan-2017 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial Version

Selva Sengottaiyan

1.0

26-May-2015

2

Updated graphical representation and added local function information

Nick Saxton

2.0

13-Apr-2016

3

Updated for FDD v2.1.0

Matthew Leser

3.0

7-Nov-2016

4

Updated to fix Anomaly EA4#9045

Matthew Leser

4.0

04-Jan-2017

Table of Contents

1Abbrevations And Acronyms5

2References6

3High-Level Description7

4Design details of software module8

4.1Graphical representation8

4.2Data Flow Diagram8

4.2.1Module level DFD8

4.2.2Sub-Module level DFD8

4.3COMPONENT FLOW DIAGRAM8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Constant Data Dictionary10

6.1Program(fixed) Constants10

6.1.1Embedded Constants10

6.1.1.1Local10

6.1.1.2Global10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation11

7.1Sub-Module Functions11

7.1.1Initialization Functions11

7.1.1.1INIT: MotCurrRegVltgLimrInit111

7.1.1.1.1Design Rationale11

7.1.1.1.2Module Outputs11

7.1.1.1.3Module Internal11

7.1.2PERIODIC FUNCTIONS11

7.1.2.1INIT: MotCurrRegVltgLimrPER111

7.1.2.1.1Design Rationale11

7.1.2.1.2Module Outputs11

7.1.3Interrupt Functions11

7.1.4Server runnables12

7.1.4.1.1Store Local copy of outputs into Module Outputs12

7.1.5Local Function/Macro Definitions12

7.1.5.1.1 Local function #112

7.1.5.1.2Local function #212

7.1.5.1.3Local function #312

7.1.6GLObAL Function/Macro Definitions12

7.1.7Tranisition FUNCTIONS13

8Known Limitations With Design14

9UNIT TEST CONSIDERATION15

10Appendix16

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

FDD

Functional Design Document

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | MDD Guidelines | Process  4.02.01 |

| 2 | Software Naming Conventions | Process  4.02.01 |

| 3 | Software Design and Coding standards | Process  4.02.01 |

| 4 | FDD  –   SF105 A_ MotCurrRegVltgLimr _Design | See Synergy  sub  project version |

|  |  |  |

Sr. No.

Title

Version

1

MDD Guidelines

Process 4.02.01

2

Software Naming Conventions

Process 4.02.01

3

Software Design and Coding standards

Process 4.02.01

4

FDD – SF105A_MotCurrRegVltgLimr_Design

See Synergy sub project version

## High-Level Description

None

## Design details of software module

### Graphical representation

### Data Flow Diagram

Refer FDD

### Module level DFD

Refer FDD

### Sub-Module level DFD

Refer FDD

### COMPONENT FLOW DIAGRAM

Refer FDD

## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>

| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None |  |  |  |  |

|  |  |  |  |  |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

None

### Variable definition for enumerated types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

| None |  |  |

Enum  Name

Element Name

Value

None

## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MODIDXHILIM_VOLT_F32 | Single precision float | Volt | 1 |

| MODIDXLOLIM_VOLT_F32 | Single precision float | Volt | 0 |

Constant Name

Resolution

Units

Value

MODIDXHILIM_VOLT_F32

Single precision float

Volt

1

MODIDXLOLIM_VOLT_F32

Single precision float

Volt

0

### Global

| Constant Name |

| --- |

|  |

Constant Name

### Module specific Lookup Tables Constants

None

## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

MotCurrRegVltgLimrInit1

### INIT: MotCurrRegVltgLimrInit1

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Refer ‘MotCurrRegVltgLimrInit’ block in FDD

### Module Internal

None

### PERIODIC FUNCTIONS

### INIT: MotCurrRegVltgLimrPER1

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Design follows implemenetation in FDD.

### Interrupt Functions

None

### Server runnables

None

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

### Local function #1

| Function Name | KpKiCtrl | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotPropGain_Ohm_T_f32 | Float32 | 0 | 2.25 |

|  | MotIntglGain_Ohm_T_f32 | Float32 | 0 | 3.6 |

|  | SysSt_Cnt_T_enum | Enum | SYSST_DI | SYSST_WRMININ |

|  | CmdErr_Ampr_T_f32 | Float32 | -200 | 400 |

|  | * MotVltgIntglCmdPrev_Volt_T_f32 | Float32 | -1000 | 1000 |

|  | * MotCurrRegVltgLimrMotVltgPropCmd_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | * MotCurrRegVltgLimrMotVltgIntglPreLim_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | MotVltgIntglLoLim_Volt_T_f32 | Float32 | -31 | 0 |

|  | MotVltgIntglHiLim_Volt_T_f32 | Float32 | 0 | 31 |

|  | * MotVltgPropCmd_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | * MotVltgIntglCmd_Volt_T_f32 | Float32 | 6 | 26.5 |

Function Name

KpKiCtrl

Type

Min

Max

Arguments Passed

MotPropGain_Ohm_T_f32

Float32

0

2.25

MotIntglGain_Ohm_T_f32

Float32

0

3.6

SysSt_Cnt_T_enum

Enum

SYSST_DI

SYSST_WRMININ

CmdErr_Ampr_T_f32

Float32

-200

400

*MotVltgIntglCmdPrev_Volt_T_f32

Float32

-1000

1000

*MotCurrRegVltgLimrMotVltgPropCmd_Volt_T_f32

Float32

-26.5

26.5

*MotCurrRegVltgLimrMotVltgIntglPreLim_Volt_T_f32

Float32

-26.5

26.5

MotVltgIntglLoLim_Volt_T_f32

Float32

-31

0

MotVltgIntglHiLim_Volt_T_f32

Float32

0

31

*MotVltgPropCmd_Volt_T_f32

Float32

-26.5

26.5

*MotVltgIntglCmd_Volt_T_f32

Float32

6

26.5

* MotVltgPropCmd_Volt_T_f32 and * MotVltgIntglCmd_Volt_T_f32 are outputs of this function.

### Local function #2

| Function Name | ErrorCalcQax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | QaxCurrCmd_Ampr_T_f32 | Float32 | - 200 | 200 |

|  | QaxRplCmd_Ampr_T_f32 | Float32 | -29 | 29 |

|  | QaxCoggCmd_Ampr_T_f32 | Float32 | -6 | 6 |

|  | QaxCurrModif_Ampr_T_f32 | Float32 | -200 | 200 |

|  | *   QaxCmdFinal_Ampr_T_f32 | Float32 | -200 | 200 |

| Returns | CmdErrQax_Ampr_T_f32 | Float32 | -200 | 400 |

Function Name

ErrorCalcQax

Type

Min

Max

Arguments Passed

QaxCurrCmd_Ampr_T_f32

Float32

-200

200

QaxRplCmd_Ampr_T_f32

Float32

-29

29

QaxCoggCmd_Ampr_T_f32

Float32

-6

6

QaxCurrModif_Ampr_T_f32

Float32

-200

200

* QaxCmdFinal_Ampr_T_f32

Float32

-200

200

Returns

CmdErrQax_Ampr_T_f32

Float32

-200

400

*QaxCmdFinal_Ampr_T_f32 is also an output of this function.

### Local function #3

| Function Name | LoaScaFac | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CurrLoaMtgtnEn_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | IvtrLoaMtgtnEn_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | MotCtrl DualEcuMotCtrlMtgtnEna_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * CurrLoaScaFac_Uls_T_f32 | Float32 | 0 | 1 |

|  | *IvtrLoaScaFac_Uls_T_f32 | Float32 | 0 | 1 |

|  | *DualEcuScaFac_Uls_T_f32 | Float32 | 0 | 1 |

Function Name

LoaScaFac

Type

Min

Max

Arguments Passed

CurrLoaMtgtnEn_Cnt_T_logl

Boolean

FALSE

TRUE

IvtrLoaMtgtnEn_Cnt_T_logl

Boolean

FALSE

TRUE

MotCtrlDualEcuMotCtrlMtgtnEna_Cnt_T_logl

Boolean

FALSE

TRUE

*CurrLoaScaFac_Uls_T_f32

Float32

0

1

*IvtrLoaScaFac_Uls_T_f32

Float32

0

1

*DualEcuScaFac_Uls_T_f32

Float32

0

1

*CurrLoaScaFac_Uls_T_f32, *IvtrLoaScaFac_Uls_T_f32, and *DualEcuScaFac_Uls_T_f32  are outputs of this function.

### Local function #4

| Function Name | MotCurr_Pred | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotInduQaxEstimdIvs_IvsHenry_T_f32 | Float32 | 2240 | 33334 |

|  | MotREstimd_Ohm_T_f32 | Float32 | 0.005 | 0.12565 |

|  | CurrQax_Ampr_T_f32 | Float32 | -200 | 200 |

|  | MotVltgQaxPrev_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | CurrDax_Ampr_T_f32 | Float32 | -200 | 200 |

|  | MotVltgDaxPrev_Volt_T_f32 | Float32 | -26.5 | 26.5 |

|  | MotBackEmfVltg_Volt_T_f32 | Float32 | -101.25 | 101.25 |

|  | ReacncQax_Ohm_T_f32 | Float32 | -0.5 | 0.5 |

|  | ReacncDax_Ohm_T_f32 | Float32 | -0.5 | 0.5 |

|  | MotInduDaxEstimdIvs_IvsHenry_T_f32 | Float32 | 2240 | 33334 |

|  | MotCurrRegVltgLimrMotCurrPredEna_Cnt_T_f32 | Boolean | FALSE | TRUE |

|  | MotCtrlCurrPredTi_NanoSec_T_f32 | Float32 | 0 | 125000 |

|  | *MotCurrQaxPred_Ampr_T_f32 | Float32 | -200 | 200 |

|  | *MotCurrDaxPred_Ampr_T_f32 | Float32 | -200 | 200 |

Function Name

MotCurr_Pred

Type

Min

Max

Arguments Passed

MotInduQaxEstimdIvs_IvsHenry_T_f32

Float32

2240

33334

MotREstimd_Ohm_T_f32

Float32

0.005

0.12565

CurrQax_Ampr_T_f32

Float32

-200

200

MotVltgQaxPrev_Volt_T_f32

Float32

-26.5

26.5

CurrDax_Ampr_T_f32

Float32

-200

200

MotVltgDaxPrev_Volt_T_f32

Float32

-26.5

26.5

MotBackEmfVltg_Volt_T_f32

Float32

-101.25

101.25

ReacncQax_Ohm_T_f32

Float32

-0.5

0.5

ReacncDax_Ohm_T_f32

Float32

-0.5

0.5

MotInduDaxEstimdIvs_IvsHenry_T_f32

Float32

2240

33334

MotCurrRegVltgLimrMotCurrPredEna_Cnt_T_f32

Boolean

FALSE

TRUE

MotCtrlCurrPredTi_NanoSec_T_f32

Float32

0

125000

*MotCurrQaxPred_Ampr_T_f32

Float32

-200

200

*MotCurrDaxPred_Ampr_T_f32

Float32

-200

200

*MotCurrQaxPred_Ampr_T_f32 and *MotCurrDaxPred_Ampr_T_f32 are outputs of this function.

### GLObAL Function/Macro Definitions

None

### Tranisition FUNCTIONS

None

## Known Limitations With Design

None

## UNIT TEST CONSIDERATION

None

## Appendix

None

Back to [Application Software](../).
