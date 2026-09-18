---
title: "Duty Cycle Thermal Protection (SF009A_DutyCycThermProtn)"
description: "Duty Cycle Thermal Protection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Duty Cycle Thermal Protection component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF009A_DutyCycThermProtn_Design` | Design package |
| `SF009A_DutyCycThermProtn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF009A_DutyCycThermProtn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF009A_DutyCycThermProtn_Impl` |  |
| C sources | `DutyCycThermProtn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `DutyCycThermProtn.dcf`, `DutyCycThermProtn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DutyCycThermProtn.dpa`, `RteGen.bat`, `SF009A_DutyCycThermProtn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF009A_DutyCycThermProtn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF009A_DutyCycThermProtn_Impl/src/DutyCycThermProtn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF009A_DutyCycThermProtn_DDReport.txt`

- **Source path in repository:** `SF009A_DutyCycThermProtn_Design/Reports/SF009A_DutyCycThermProtn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF009A_DutyCycThermProtn_DataDict
23-Sep-2016 12:16:07
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
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
DutyCycThermProtnDi         	Name does not match required pattern.
(variables: 11, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
DutyCycThermProtnMaxOutp    	Name does not match required pattern.
(variables: 4, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 34, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 1, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 15, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 14, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `DutyCycThermProtn_Integration Manual.doc`

- **Source path in repository:** `SF009A_DutyCycThermProtn_Impl/doc/DutyCycThermProtn_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `139 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DutyCycThermProtn_MDD.docx`

- **Source path in repository:** `SF009A_DutyCycThermProtn_Impl/doc/DutyCycThermProtn_MDD.docx`
- **Format:** `.docx`
- **Size:** `168 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

DutyCycThermProtn

Sep 29, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Anne

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sarika Natu (KPIT Technologies) | 1.0 | 02-Oct -2015 |

| Updated to version 2.0.0 of FDD | Krishna Anne | 2.0 | 07-Apr-2016 |

| Fix for anomaly EA4#   7558 | Krishna Anne | 3.0 | 29-Sep-2016 |

Description

Author

Version

Date

Initial Version

Sarika Natu(KPIT Technologies)

1.0

02-Oct-2015

Updated to version 2.0.0 of FDD

Krishna Anne

2.0

07-Apr-2016

Fix for anomaly EA4# 7558

Krishna Anne

3.0

29-Sep-2016

Table of Contents

1DutyCycThermProtn & High-Level Description5

2Design details of software module6

2.1Graphical representation of DutyCycThermProtn6

2.2Data Flow Diagram7

2.2.1Component level DFD7

2.2.2Function level DFD7

3Constant Data Dictionary8

3.1Program (fixed) Constants8

3.1.1Embedded Constants8

4Software Component Implementation9

4.1Sub-Module Functions9

4.1.1Init: DutyCycThermProtn_Init19

4.1.1.1Design Rationale9

4.1.1.2Module Outputs9

4.1.2Per: DutyCycThermProtn_Per19

4.1.2.1Design Rationale9

4.1.2.2Store Module Inputs to Local copies9

4.1.2.3(Processing of function)………9

4.1.2.4Store Local copy of outputs into Module Outputs9

4.2Server Runables9

4.3Interrupt Functions9

4.4Module Internal (Local) Functions9

4.4.1Local Function #19

4.4.1.1Design Rationale9

4.4.1.2Processing10

4.4.2Local Function #210

4.4.2.1Design Rationale10

4.4.2.2Processing10

4.4.3Local Function #310

4.4.3.1Design Rationale10

4.4.3.2Processing10

4.4.4Local Function #410

4.4.4.1Design Rationale11

4.4.4.2Processing11

4.4.5Local Function #511

4.4.5.1Design Rationale11

4.4.5.2Processing11

4.4.6Local Function #611

4.4.6.1Design Rationale11

4.4.6.2Processing12

4.5GLOBAL Function/Macro Definitions12

5Known Limitations with Design13

6UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## DutyCycThermProtn & High-Level Description

The purpose of the Thermal Duty Cycle Protection is to limit and protect the system from excessive use, based on motor rotational velocity and system temperature. It also provides protection status information for use by other functions.

## Design details of software module

### Graphical representation of DutyCycThermProtn

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

Refer .m file

| Constant Name | Value |

| --- | --- |

| DUTYCYCTHERMSIZE_CNT_U08 | 5 |

| THERMLOADLIMSIZE_CNT_U08 | 8 |

| MULTFILTERSIZE_CNT_U08 | 6 |

Constant Name

Value

DUTYCYCTHERMSIZE_CNT_U08

5

THERMLOADLIMSIZE_CNT_U08

8

MULTFILTERSIZE_CNT_U08

6

## Software Component Implementation

### Sub-Module Functions

### Init: DutyCycThermProtn_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: DutyCycThermProtn_Per1

### Design Rationale

DutyCycThermProtn_Per1 function is divided into various functions to reduce the cyclomatic complexity.

The subsystems ‘Multiplier’ and ‘FilterPercMax’ are clubbed into ‘MultiFilterPercMax’ local function.

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

| Function Name | FiltSVReinit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | IgnTiOff_Cnt_T_u32 | uint 32 | 0 | 1720000 |

|  | VehTiVld_Cnt_T_Logl | Boolean | 0 | 1 |

| Return Value | None |  |  |  |

Function Name

FiltSVReinit

Type

Min

Max

Arguments Passed

IgnTiOff_Cnt_T_u32

uint32

0

1720000

VehTiVld_Cnt_T_Logl

Boolean

0

1

Return Value

None

### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

### Local Function #2

| Function Name | TemperatureSelection | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DiagcStsLimdTPrfmnc_Cnt_T_Logl | boolean | 0 | 1 |

|  | EcuTFild_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotFetT_DegCgrd_T_f32 | float32 | -50 | 200 |

|  | MotMagT_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotWidgT_DegCgrd_T_f32 | float32 | -50 | 300 |

|  | * Mult12Temp_DegCgrd_T_  s15p0 | Sint16 | -50 | 200 |

|  | * Mult36 Temp_DegCgrd_T_ s15p0 | Sint16 | -50 | 300 |

| Return Value | SlcTemp_DegCgrd_T_s15p0 | sint16 | -50 | 300 |

Function Name

TemperatureSelection

Type

Min

Max

Arguments Passed

DiagcStsLimdTPrfmnc_Cnt_T_Logl

boolean

0

1

EcuTFild_DegCgrd_T_f32

float32

-50

150

MotFetT_DegCgrd_T_f32

float32

-50

200

MotMagT_DegCgrd_T_f32

float32

-50

150

MotWidgT_DegCgrd_T_f32

float32

-50

300

*Mult12Temp_DegCgrd_T_ s15p0

Sint16

-50

200

*Mult36Temp_DegCgrd_T_s15p0

Sint16

-50

300

Return Value

SlcTemp_DegCgrd_T_s15p0

sint16

-50

300

### Design Rationale

Name of local function matches with subsystem name from FDD

Note: The outputs of the function are Mult12Temp_DegCgrd_T_s15p0, Mult36Temp_DegCgrd_T_s15p0 and SlcTemp_DegCgrd_T_f32.

### Processing

None

### Local Function #3

| Function Name | TemperatureLimiting | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EcuTFild_DegCgrd_T_f32 | float32 | -50 | 150 |

|  | MotWidgT_DegCgrd_T_f32 | float32 | -50 | 300 |

| Return Value | AbsTempLimitSlew_MotNwtMtrPerSec_T_f32 | float32 | 0 | 8 .79 |

Function Name

TemperatureLimiting

Type

Min

Max

Arguments Passed

EcuTFild_DegCgrd_T_f32

float32

-50

150

MotWidgT_DegCgrd_T_f32

float32

-50

300

Return Value

AbsTempLimitSlew_MotNwtMtrPerSec_T_f32

float32

0

8.79

### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

None

### Local Function #4

| Function Name | MultiFilterPercMax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Mult12Temp_DegCgrd_T_ s15p0 | sint16 | -50 | 200 |

|  | Mult36Temp_DegCgrd_T_ s15p0 | sint16 | -50 | 300 |

|  | DutyCycThermProtnDi_Cnt_T_Logl | boolean | 0 | 1 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | MotCurrPeakEstimd_AmprSqd_T_f32 | float32 | 0 | 62500 |

|  | MotCurrPeakEstimdFild_AmprSqd_T_f32 | float32 | 0 | 62500 |

|  | * MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

| Return Value | ThermLimSlowFilMax_Uls_T_f32 | float32 | 0 | 200 |

Function Name

MultiFilterPercMax

Type

Min

Max

Arguments Passed

Mult12Temp_DegCgrd_T_s15p0

sint16

-50

200

Mult36Temp_DegCgrd_T_s15p0

sint16

-50

300

DutyCycThermProtnDi_Cnt_T_Logl

boolean

0

1

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

MotCurrPeakEstimd_AmprSqd_T_f32

float32

0

62500

MotCurrPeakEstimdFild_AmprSqd_T_f32

float32

0

62500

*MaxOut_Uls_T_u16p0

uint16

0

200

Return Value

ThermLimSlowFilMax_Uls_T_f32

float32

0

200

### Design Rationale

The subsystems ‘Multiplier’ and ‘FilterPercMax’ are clubbed into ‘MultiFilterPercMax’ local function.

Note: The outputs of the function are MaxOut_Uls_T_u16p0 and ThermLimSlowFilMax_Uls_T_f32.

### Processing

None

### Local Function #5

| Function Name | ThermalLoadLimit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | MotVelCrf_MotRadPerSec_T_f32 | float32 | -1350 | 1350 |

|  | SlcTemp_DegCgrd_T_s15p0 | sint16 | -50 | 300 |

|  | MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

| Return Value | ThermalLoadLmt_MotNwtMtr_T_f32 | float32 | 0 | 8.79 |

Function Name

ThermalLoadLimit

Type

Min

Max

Arguments Passed

MotVelCrf_MotRadPerSec_T_f32

float32

-1350

1350

SlcTemp_DegCgrd_T_s15p0

sint16

-50

300

MaxOut_Uls_T_u16p0

uint16

0

200

Return Value

ThermalLoadLmt_MotNwtMtr_T_f32

float32

0

8.79

### Design Rationale

Name of local function matches with subsystem name from FDD

### Processing

None

### Local Function #6

| Function Name | ThermalLimitStatus | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AbsTempLimitSlew_MotNwtMtrPerSec_T_f32 | float32 | 0 | 8.79 |

|  | DutyCycThermProtnDi_Cnt_T_Logl | Boolean | 0 | 1 |

|  | ThermalLoadLmt_MotNwtMtr_T_f32 | float32 | 0 | 8.79 |

|  | MaxOut_Uls_T_u16p0 | uint16 | 0 | 200 |

|  | * ThermMotTqLim_MotNwtMtr_T_f32 | float32 | 0 | 8.8 |

| Return Value | ThermRednFac_Uls_T_f32 | float32 | 0 | 1 |

Function Name

ThermalLimitStatus

Type

Min

Max

Arguments Passed

AbsTempLimitSlew_MotNwtMtrPerSec_T_f32

float32

0

8.79

DutyCycThermProtnDi_Cnt_T_Logl

Boolean

0

1

ThermalLoadLmt_MotNwtMtr_T_f32

float32

0

8.79

MaxOut_Uls_T_u16p0

uint16

0

200

*ThermMotTqLim_MotNwtMtr_T_f32

float32

0

8.8

Return Value

ThermRednFac_Uls_T_f32

float32

0

1

### Design Rationale

Name of local function matches with subsystem name from FDD

Note: The outputs of the function are ThermMotTqLim_MotNwtMtr_T_f32 and ThermRednFac_Uls_T_f32.

### Local Function #6

| Function Name | UseInpLowr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | * TableX_Cnt_T_s16 | sint16 | FULL | FULL |

|  | * TableY_Cnt_T_u16 | uint16 | FULL | FULL |

|  | Size_Cnt_T_u16 | uint16 | 1 | 20 |

|  | Input_Cnt_T_s16 | sint16 | FULL | FULL |

| Return Value | TableY_Cnt_T_u16[Idx_Cnt_T_u08] | uint16 | FULL | FULL |

Function Name

UseInpLowr

Type

Min

Max

Arguments Passed

*TableX_Cnt_T_s16

sint16

FULL

FULL

*TableY_Cnt_T_u16

uint16

FULL

FULL

Size_Cnt_T_u16

uint16

1

20

Input_Cnt_T_s16

sint16

FULL

FULL

Return Value

TableY_Cnt_T_u16[Idx_Cnt_T_u08]

uint16

FULL

FULL

### Design Rationale

None.

### Processing

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

Function UseInpLowr to be tested only as called by the component; input and output ranges will not be reached.

Function UseInpLowr’s TableX must have strictly increasing elements.

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

| 2 | MDD Guideline | EA4 02 .00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD –  SF009A_DutyCycThermProtn _Design | See Synergy sub project version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 02.00.00

3

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.1

5

FDD – SF009A_DutyCycThermProtn_Design

See Synergy sub project version

Back to [Application Software](../).
