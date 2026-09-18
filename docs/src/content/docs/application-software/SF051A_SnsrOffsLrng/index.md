---
title: "Sensor Offset Learning (SF051A_SnsrOffsLrng)"
description: "Sensor Offset Learning: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Sensor Offset Learning component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF051A_SnsrOffsLrng_Design` | Design package |
| `SF051A_SnsrOffsLrng_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF051A_SnsrOffsLrng_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF051A_SnsrOffsLrng_Impl` |  |
| C sources | `SnsrOffsLrng.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SnsrOffsLrng.dcf`, `SnsrOffsLrng_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF051A_SnsrOffsLrng_Impl.gpj`, `SnsrOffsLrng.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF051A_SnsrOffsLrng_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF051A_SnsrOffsLrng_Impl/src/SnsrOffsLrng.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF051A_SnsrOffsLrng_DDReport.txt`

- **Source path in repository:** `SF051A_SnsrOffsLrng_Design/Reports/SF051A_SnsrOffsLrng_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF051A_SnsrOffsLrng_DataDict
06-Dec-2016 17:04:16
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
(variables: 8, errors: 0)

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
(variables: 3, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 50, errors: 0)

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
(variables: 29, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 42, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `SnsrOffLrng_MDD.docx`

- **Source path in repository:** `SF051A_SnsrOffsLrng_Impl/doc/SnsrOffLrng_MDD.docx`
- **Format:** `.docx`
- **Size:** `142 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Sensor Offset Learning

Dec 7, 2016

Prepared By:

Shruthi Raghavan,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Version | Description | Author | Date |

| --- | --- | --- | --- |

| 1 | Initial Version | Selva   Sengottaiyan | 07-Feb-2016 |

| 2 | Updated as per FDD v 1.2.0 | Krishna Anne | 07-Mar-2016 |

| 3 | Updated graphical representation | Nick Saxton | 17-Aug-2016 |

| 4 | Updated design limitations for FDD v1.5.0 | Shruthi Raghavan | 7-Dec-2016 |

Version

Description

Author

Date

1

Initial Version

Selva Sengottaiyan

07-Feb-2016

2

Updated as per FDD v 1.2.0

Krishna Anne

07-Mar-2016

3

Updated graphical representation

Nick Saxton

17-Aug-2016

4

Updated design limitations for FDD v1.5.0

Shruthi Raghavan

7-Dec-2016

Table of Contents1Introduction6

2SnsrOffsLrng & High-Level Description7

3Design details of software module8

3.1Graphical representation of SnsrOffsLrng9

4Constant Data Dictionary11

4.1Program (fixed) Constants11

4.1.1Embedded Constants11

5Software Component Implementation12

5.1Sub-Module Functions12

5.1.1Init: SnsrOffsLrngInit112

5.1.1.1Design Rationale12

5.1.1.2Module Outputs12

5.1.2Per: SnsrOffsLrngPer112

5.1.2.1Design Rationale12

5.1.2.2Store Module Inputs to Local copies12

5.1.2.3(Processing of function)………12

5.1.2.4Store Local copy of outputs into Module Outputs12

5.1.1Per: SnsrOffsLrngPer212

5.1.1.1Design Rationale12

5.1.1.2Store Module Inputs to Local copies12

5.1.1.3(Processing of function)………12

5.1.1.4Store Local copy of outputs into Module Outputs12

5.2Server Runables13

5.2.1SnsrOffsLrng_RstHwTq13

5.2.1.1Design Rationale13

5.2.1.2Store Module Inputs to Local copies13

5.2.1.3(Processing of function)………13

5.2.1.4Store Local copy of outputs into Module Outputs13

5.2.2SnsrOffsLrng_RstYawAndAg13

5.2.2.1Design Rationale13

5.2.2.2Store Module Inputs to Local copies13

5.2.2.3(Processing of function)………13

5.2.2.4Store Local copy of outputs into Module Outputs13

5.2.3SnsrOffsLrng_SetHwAgOffs13

5.2.3.1Design Rationale13

5.2.3.2Store Module Inputs to Local copies13

5.2.3.3(Processing of function)………13

5.2.3.4Store Local copy of outputs into Module Outputs13

5.2.4SnsrOffsLrng_GetHwAgOffs14

5.2.4.1Design Rationale14

5.2.4.2Store Module Inputs to Local copies14

5.2.4.3(Processing of function)………14

5.2.4.4Store Local copy of outputs into Module Outputs14

5.2.5SnsrOffsLrng_SetHwTqOffs14

5.2.5.1Design Rationale14

5.2.5.2Store Module Inputs to Local copies14

5.2.5.3(Processing of function)………14

5.2.5.4Store Local copy of outputs into Module Outputs14

5.2.6SnsrOffsLrng_GetHwTqOffs14

5.2.6.1Design Rationale14

5.2.6.2Store Module Inputs to Local copies14

5.2.6.3(Processing of function)………14

5.2.6.4Store Local copy of outputs into Module Outputs14

5.2.7SnsrOffsLrng_SetYawRateOffs15

5.2.7.1Design Rationale15

5.2.7.2Store Module Inputs to Local copies15

5.2.7.3(Processing of function)………15

5.2.7.4Store Local copy of outputs into Module Outputs15

5.2.8SnsrOffsLrng_GetYawRateOffs15

5.2.8.1Design Rationale15

5.2.8.2Store Module Inputs to Local copies15

5.2.8.3(Processing of function)………15

5.2.8.4Store Local copy of outputs into Module Outputs15

5.3Module Internal (Local) Functions15

5.3.1Module Internal (Local) Functions15

6Known Limitations with Design19

7UNIT TEST CONSIDERATION20

Appendix AAbbreviations and Acronyms21

Appendix BGlossary22

Appendix CReferences23

## Introduction

Refer the Design Subproject.

## SnsrOffsLrng & High-Level Description

Refer the Design Subproject.

## Design details of software module

### Graphical representation of SnsrOffsLrng

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| HWTQOFFSHILIM_HWNWTMTR_F32 | Single precision float | HwNwtMtr | 4 |

| HWTQOFFSLOLIM_HWNWTMTR_F32 | Single precision float | HwNwtMtr | -4 |

| VEHYAWRATEOFFSHILIM_VEHDEGPERSEC_F32 | Single precision float | VehDegPerSec | 20 |

| VEHYAWRATEOFFSLO LIM_VEHDEGPERSEC_F32 | Single precision float | VehDegPerSec | -20 |

| HWAGOFFSHILIM_HWDEG_F32 | Single precision float | HwDeg | -30 |

| HWAGOFFS LO LIM_HWDEG_F32 | Single precision float | HwDeg | -30 |

| MTRXSIZE_CNT_U08 | 1 | Cnt | 3 |

Constant Name

Resolution

Units

Value

HWTQOFFSHILIM_HWNWTMTR_F32

Single precision float

HwNwtMtr

4

HWTQOFFSLOLIM_HWNWTMTR_F32

Single precision float

HwNwtMtr

-4

VEHYAWRATEOFFSHILIM_VEHDEGPERSEC_F32

Single precision float

VehDegPerSec

20

VEHYAWRATEOFFSLOLIM_VEHDEGPERSEC_F32

Single precision float

VehDegPerSec

-20

HWAGOFFSHILIM_HWDEG_F32

Single precision float

HwDeg

-30

HWAGOFFSLOLIM_HWDEG_F32

Single precision float

HwDeg

-30

MTRXSIZE_CNT_U08

1

Cnt

3

## Software Component Implementation

### Sub-Module Functions

#### Init: SnsrOffsLrngInit1

### Design Rationale

Refer the Design.

### Module Outputs

Refer the Design.

#### Per: SnsrOffsLrngPer1

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### Per: SnsrOffsLrngPer2

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

### Server Runables

#### SnsrOffsLrng_RstHwTq

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_RstYawAndAg

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_SetHwAgOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_GetHwAgOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_SetHwTqOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_GetHwTqOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_SetYawRateOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

#### SnsrOffsLrng_GetYawRateOffs

### Design Rationale

Refer the Design.

### Store Module Inputs to Local copies

Refer the Design.

### (Processing of function)………

Refer the Design.

### Store Local copy of outputs into Module Outputs

Refer the Design.

### Module Internal (Local) Functions

#### Module Internal (Local) Functions

#### Calculate LearnHwAg

| Function Name | LearnHwAg | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | HwAgLrngLrngCdnVld_Cnt _T_logl | Boolean | FALSE | TRUE |  |

|  | HwAgLrngEna_Cnt _T_logl | Boolean | FALSE | TRUE |  |

|  | SysTqFild_HwNm_T_f32 | float32 | -8.8 | 8.8 |  |

|  | HandwheelPosition_HwDeg_T_f32 | float32 | -1440 | 1440 |  |

| Return Value | None |  |  |  |  |

Function Name

LearnHwAg

Type

Min

Max

UTP Tol.

Arguments Passed

HwAgLrngLrngCdnVld_Cnt_T_logl

Boolean

FALSE

TRUE

HwAgLrngEna_Cnt_T_logl

Boolean

FALSE

TRUE

SysTqFild_HwNm_T_f32

float32

-8.8

8.8

HandwheelPosition_HwDeg_T_f32

float32

-1440

1440

Return Value

None

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate SOaCHierarchyManager

| Function Name | SOaCHierarchyManager | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | * EnableYOC_Cnt _T_logl | Boolean | FALSE | TRUE |  |

|  | * HwAgLrngEna_Cnt _T_logl | Boolean | FALSE | TRUE |  |

|  | * HwAgLrngRst_Cnt _T_logl | Boolean | FALSE | TRUE |  |

| Return Value |  |  |  |  |  |

Function Name

SOaCHierarchyManager

Type

Min

Max

UTP Tol.

Arguments Passed

*EnableYOC_Cnt_T_logl

Boolean

FALSE

TRUE

*HwAgLrngEna_Cnt_T_logl

Boolean

FALSE

TRUE

*HwAgLrngRst_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate Perform_TqInpDetn

| Function Name | Perform_TqInpDetn | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |  |

|  |  |  |  |  |  |

| Return Value |  |  |  |  |  |

Function Name

Perform_TqInpDetn

Type

Min

Max

UTP Tol.

Arguments Passed

None

Return Value

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate EnableLearning

| Function Name | EnableLearning | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed |  |  |  |  |  |

|  |  |  |  |  |  |

| Return Value | HwTqLrngEna_Cnt _T_logl | Boolean | FALSE | TRUE |  |

Function Name

EnableLearning

Type

Min

Max

UTP Tol.

Arguments Passed

Return Value

HwTqLrngEna_Cnt_T_logl

Boolean

FALSE

TRUE

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate CalculateKVector

| Function Name | CalculateKVector | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | TqMdlXAry_HwRadpS_T_f32 [3] | float32 | -42 | 42 |  |

|  | KVect_Uls_T_f32 [3] | float32 | -42 | 42 |  |

| Return Value |  |  |  |  |  |

Function Name

#### CalculateKVector

Type

Min

Max

UTP Tol.

Arguments Passed

TqMdlXAry_HwRadpS_T_f32[3]

float32

-42

42

KVect_Uls_T_f32[3]

float32

-42

42

Return Value

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate EnablePreProcessing

| Function Name | EnablePreProcessing | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | HwTqPreproc_dB_T_f32 | float32 | -100 | 30 |  |

|  | SampleCntrLim_Cnt_T_u16 | Uint16 | 1 | 65535 |  |

|  | TqInpPrsntVld_Cnt _T_logl | Boolean | FALSE | TRUE |  |

|  | TqInpPrsnt_Cnt _T_logl | Boolean | FALSE | TRUE |  |

| Return Value |  |  |  |  |  |

Function Name

EnablePreProcessing

Type

Min

Max

UTP Tol.

Arguments Passed

HwTqPreproc_dB_T_f32

float32

-100

30

SampleCntrLim_Cnt_T_u16

Uint16

1

65535

TqInpPrsntVld_Cnt_T_logl

Boolean

FALSE

TRUE

TqInpPrsnt_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

#### Calculate UpdateCovarianceMatrix

| Function Name | UpdateCovarianceMatrix | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | TqMdlXAry_HwRadpS_T_f32 [3] | float32 | -42 | 42 |  |

|  | KVect_Uls_T_f32 [3] | float32 | -42 | 42 |  |

| Return Value |  |  |  |  |  |

Function Name

UpdateCovarianceMatrix

Type

Min

Max

UTP Tol.

Arguments Passed

TqMdlXAry_HwRadpS_T_f32[3]

float32

-42

42

KVect_Uls_T_f32[3]

float32

-42

42

Return Value

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing

TblSize_Cnt_T_u16 is size of the single dimension of TqMdlAryKVect_Uls_T_f32.

#### Calculate UpdateHwTqOffs

| Function Name | UpdateHwTqOffs | Type | Min | Max | UTP  Tol . |

| --- | --- | --- | --- | --- | --- |

| Arguments Passed | HwTqEstimnVld_Cnt _T_logl | boolean | FALSE | TRUE |  |

|  | HwTqDriftEstimnOnCentr_HwNm_T_f32 | float32 | -10 | 10 |  |

| Return Value | None |  |  |  |  |

Function Name

UpdateHwTqOffs

Type

Min

Max

UTP Tol.

Arguments Passed

HwTqEstimnVld_Cnt_T_logl

boolean

FALSE

TRUE

HwTqDriftEstimnOnCentr_HwNm_T_f32

float32

-10

10

Return Value

None

#### Description

No flowchart added. For Unit test FDD should provide the information needed regarding function processing


*... content truncated for brevity; see the source document in the repository. ...*

### `SnsrOffsLrng_IntegrationManual.doc`

- **Source path in repository:** `SF051A_SnsrOffsLrng_Impl/doc/SnsrOffsLrng_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `156 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Application Software](../).
