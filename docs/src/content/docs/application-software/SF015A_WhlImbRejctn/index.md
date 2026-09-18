---
title: "Wheel Imbalance Rejection (SF015A_WhlImbRejctn)"
description: "Wheel Imbalance Rejection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Wheel Imbalance Rejection component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF015A_WhlImbRejctn_Design` | Design package |
| `SF015A_WhlImbRejctn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF015A_WhlImbRejctn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF015A_WhlImbRejctn_Impl` |  |
| C sources | `WhlImbRejctn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `WhlImbRejctn.dcf`, `WhlImbRejctn_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF015A_WhlImbRejctn_Impl.gpj`, `WhlImbRejctn.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF015A_WhlImbRejctn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF015A_WhlImbRejctn_Impl/src/WhlImbRejctn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF015A_WhlImbRejctn_DDReport.txt`

- **Source path in repository:** `SF015A_WhlImbRejctn_Design/Reports/SF015A_WhlImbRejctn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF015A_WhlImbRejctn_DataDict
13-Feb-2017 16:39:20
Tool Release:  2.53.0



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
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
WhlImbRejctnCustEna         	Name does not match required pattern.
WhlImbRejctnDi              	Name does not match required pattern.
(variables: 9, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
WhlImbRejctnActv            	Name does not match required pattern.
WhlImbRejctnAmp             	Name does not match required pattern.
WhlImbRejctnCmd             	Name does not match required pattern.
(variables: 3, errors: 3)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 9, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 60, errors: 0)

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
(variables: 10, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 67, errors: 0)
```
*... truncated (37 more lines in the source file). ...*

### `WhlImbRejctn_IntegrationManual.doc`

- **Source path in repository:** `SF015A_WhlImbRejctn_Impl/doc/WhlImbRejctn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `WhlImbRejctn_MDD.docx`

- **Source path in repository:** `SF015A_WhlImbRejctn_Impl/doc/WhlImbRejctn_MDD.docx`
- **Format:** `.docx`
- **Size:** `128 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

WhlImbRejctn

Version: 9

Jan 26, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matt Leser,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 4 - Mar -201 6 |

| Updated for FDD ver 1.2.0 | Sankardu Varadapureddi | 2 | 21-Mar-2016 |

| Updated for FDD ver 1. 6 .0 | Matt Leser | 3 (Version 4 in Synergy) | 21-Sep-2016 |

| Updated version number to match Synergy Database | Matt Leser | 6 | 28-Sep-2016 |

| Updated for FDD ver 1.7.0 | Matt Leser | 7 | 13-Oct-2016 |

| Updated to fix Anomaly EA4#8205 | Matt Leser | 8 | 2-Dec-2016 |

| Updated for FDD ver 1.9.0, Fixed Anoma ies  EA4#8955 /EA4#9065 | Matt Leser | 9 | 26-Jan-2017 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

4-Mar-2016

Updated for FDD ver 1.2.0

Sankardu Varadapureddi

2

21-Mar-2016

Updated for FDD ver 1.6.0

Matt Leser

3 (Version 4 in Synergy)

21-Sep-2016

Updated version number to match Synergy Database

Matt Leser

6

28-Sep-2016

Updated for FDD ver 1.7.0

Matt Leser

7

13-Oct-2016

Updated to fix Anomaly EA4#8205

Matt Leser

8

2-Dec-2016

Updated for FDD ver 1.9.0, Fixed Anomaies EA4#8955/EA4#9065

Matt Leser

9

26-Jan-2017

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2WhlImbRejctn High-Level Description6

3Design details of software module7

3.1Graphical representation of WhlImbRejctn7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: WhlImbRejctnInit110

5.1.1.1Design Rationale10

5.1.1.2Module Outputs10

5.1.2Per: WhlImbRejctnPer110

5.1.2.1Design Rationale10

5.1.2.2Store Module Inputs to Local copies10

5.1.2.3(Processing of function)………10

5.1.2.4Store Local copy of outputs into Module Outputs10

5.1.3Per: WhlImbRejctnPer210

5.1.3.1Design Rationale10

5.1.3.2Store Module Inputs to Local copies10

5.1.3.3(Processing of function)………10

5.1.3.4Store Local copy of outputs into Module Outputs10

5.2Server Runables10

5.3Interrupt Functions10

5.4Module Internal (Local) Functions11

5.4.1Local Function #111

5.4.1.1Description11

5.4.2Local Function #211

5.4.2.1Description11

5.4.3Local Function #312

5.4.3.1Description12

5.4.4Local Function #412

5.4.4.1Description12

5.4.5Local Function #512

5.4.5.1Description12

5.4.6Local Function #613

5.4.6.1Description13

5.4.7Local Function #713

5.4.7.1Description13

5.4.8Local Function #813

5.4.8.1Description14

5.4.9Local Function #914

5.4.9.1Description14

5.4.10Local Function #1014

5.4.10.1Description14

5.4.11Local Function #1114

5.4.11.1Description14

5.4.12Local Function #1214

5.4.12.1Description15

5.4.13Local Function #1315

5.4.13.1Description15

5.5GLOBAL Function/Macro Definitions15

6Known Limitations with Design16

7UNIT TEST CONSIDERATION17

Appendix AAbbreviations and Acronyms18

Appendix BGlossary19

Appendix CReferences20

## Introduction

### Purpose

### Scope

## WhlImbRejctn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of WhlImbRejctn

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MAXMGNMASK_CNT_U08 | 1 | Cnt | 1 |

| QUALMASK_CNT_U08 | 1 | Cnt | 2 |

| DCTRENDMASK_CNT_U08 | 1 | Cnt | 4 |

| FREQDIAGCMASK_CNT_U08 | 1 | Cnt | 8 |

| WHLSPDCORRLNMASK_CNT_U08 | 1 | Cnt | 16 |

| MINSTOMILLISEC_ULS_F32 | 1 | Cnt | 60000 |

Constant Name

Resolution

Units

Value

MAXMGNMASK_CNT_U08

1

Cnt

1

QUALMASK_CNT_U08

1

Cnt

2

DCTRENDMASK_CNT_U08

1

Cnt

4

FREQDIAGCMASK_CNT_U08

1

Cnt

8

WHLSPDCORRLNMASK_CNT_U08

1

Cnt

16

MINSTOMILLISEC_ULS_F32

1

Cnt

60000

For other constants, refer .m file.

#### Local Constants

## Software Component Implementation

### Sub-Module Functions

### Init: WhlImbRejctnInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: WhlImbRejctnPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: WhlImbRejctnPer2

### Design Rationale

Refer FDD

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

| Function Name | UGRFilOutp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Y_Hz_T_f32 | float32 | -8.8 | 376.991118 |

|  | FreqEst_Hz_T_f32 | float32 | 0.0 05 | 60 |

|  | PoleMag_Uls_T_f32 | float32 | 0 | 1 |

|  | *   Ugr1_MotRadPerSec_T_f32 | float32 | 0 | 256 |

|  | *   Ugr2_MotRadPerSec_T_f32 | float32 | 0 | 256 |

| Return Value | YFild_Hz_T_f32 | float32 | 0 | 127 |

Function Name

UGRFilOutp

Type

Min

Max

Arguments Passed

Y_Hz_T_f32

float32

-8.8

376.991118

FreqEst_Hz_T_f32

float32

0.005

60

PoleMag_Uls_T_f32

float32

0

1

* Ugr1_MotRadPerSec_T_f32

float32

0

256

* Ugr2_MotRadPerSec_T_f32

float32

0

256

Return Value

YFild_Hz_T_f32

float32

0

127

### Description

‘UGR’ filter implementation. ‘Ugr1_MotRadPerSec_T_f32’ and ‘Ugr2_MotRadPerSec_T_f32’ corresponds to PIMs used in internal calculations.

### Local Function #2

| Function Name | DtrmnEnadAmnt | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FreqEstAvg_Hz_T_f32 | float32 | 0.005 | 60 |

|  | WhlSpdLFilt_MotRadPerSec_T_f32 | float32 | -100 | 100 |

|  | WhlSpdRFilt_MotRadPerSec_T_f32 | float32 | -100 | 100 |

|  | VehSpd_Kph_T_f32 | float32 | 0 | 511 |

|  | VehSpdVld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | WhlImbRejctnCustEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | WhlImbRejctnDi_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysSt_Cnt_T_enum | SysSt1 | SYSST_DI | SYSST_WRMININ |

|  | * Enable_Uls_T_f32 | float32 | 0 | 1 |

| Return Value | WhlImbRejctnActv_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

DtrmnEnadAmnt

Type

Min

Max

Arguments Passed

FreqEstAvg_Hz_T_f32

float32

0.005

60

WhlSpdLFilt_MotRadPerSec_T_f32

float32

-100

100

WhlSpdRFilt_MotRadPerSec_T_f32

float32

-100

100

VehSpd_Kph_T_f32

float32

0

511

VehSpdVld_Cnt_T_logl

boolean

FALSE

TRUE

WhlImbRejctnCustEna_Cnt_T_logl

boolean

FALSE

TRUE

WhlImbRejctnDi_Cnt_T_logl

boolean

FALSE

TRUE

SysSt_Cnt_T_enum

SysSt1

SYSST_DI

SYSST_WRMININ

*Enable_Uls_T_f32

float32

0

1

Return Value

WhlImbRejctnActv_Cnt_T_logl

boolean

FALSE

TRUE

### Description

"Determine Enabled Amt" block implementation. In determination of ‘DistbnMagEnadPrev’, ‘ScaleL’ and ‘ScaleR’ values, some if-else loops were combined in software for optimization.

*Enable_Uls_T_f32 is an output of this function.

### Local Function #3

| Function Name | EnaRamp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EnableFac_Uls_T_f32 | float32 | 0 | 1 |

|  | SysSt_Cnt_T_enum | SysSt1 | SYSST_DI | SYSST_WRMININ |

| Return Value | RampEna_Uls_T_f32 | float32 | 0 | 1 |

Function Name

EnaRamp

Type

Min

Max

Arguments Passed

EnableFac_Uls_T_f32

float32

0

1

SysSt_Cnt_T_enum

SysSt1

SYSST_DI

SYSST_WRMININ

Return Value

RampEna_Uls_T_f32

float32

0

1

### Description

"Enable Ramp" block implementation.

### Local Function #4

| Function Name | DistMag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WhlSpd_MotRadPerSec_T_f32 | float32 | -10 0 | 10 0 |

|  | Freq_Hz_T_f32 | float32 | 0.005 | 60 |

|  | *   PeakPrev_Uls_T_f32 | float32 | 0 | 127 |

|  | *   CurrMag_Uls_T_f32 | float32 | 0 | 127 |

|  | *LpFilOut_Cnt_T_FilLpRec1 | FilLpRec1 |  |  |

| Return Value | DistMag_Uls_T_f32 | float32 | 0 | 127 |

Function Name

DistMag

Type

Min

Max

Arguments Passed

WhlSpd_MotRadPerSec_T_f32

float32

-100

100

Freq_Hz_T_f32

float32

0.005

60

* PeakPrev_Uls_T_f32

float32

0

127

* CurrMag_Uls_T_f32

float32

0

127

*LpFilOut_Cnt_T_FilLpRec1

FilLpRec1

Return Value

DistMag_Uls_T_f32

float32

0

127

### Description

"DistMagL/DistMagR" block implementation. ‘PeakPrev_Uls_T_f32’ is a PIM used in the internal implementation.

‘LePeakPrev’ is output of this function.

### Local Function #5

| Function Name | ActvRejctnCmd | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

|  | Enable_Uls_T_f32 | float32 | 0 | 1 |

|  | FreqEst_Hz_T_f32 | float32 | 0.005 | 60 |

|  |  |  |  |  |

| Return Value | WhlImbRejctnCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

Function Name

ActvRejctnCmd

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10

10

Enable_Uls_T_f32

float32

0

1

FreqEst_Hz_T_f32

float32

0.005

60

Return Value

WhlImbRejctnCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

### Description

"Active Rejection Command " block implementation. “WhlImbRejctnAmp_MtrNm_T_f32” is the output of this function.

PIMs ‘StordValLe’ and ‘StordValRi’ directly used in the software for signals ‘FiltWhlSpdLScld’ and ‘FiltWhlSpdRScld’ in the FDD.

### Local Function #6

| Function Name | AdjSigFil | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | In1_MotNwtMtr_T_f32 | float32 | -127 | 127 |

|  | Zm_Uls_T_f32 | float32 | 0.244742 | 1.0 |

|  | Pk_Uls_T_f32 | float32 | 0.244742 | 1.0 |

|  | B0_Uls_T_f32 | float32 | 0.249683 | 4.005074 |

|  | MagAtFreq_Uls_T_f32 | float32 | 0.414213562 | 2.414213562 |

|  | *   Coeff1_Uls_T_f32 | float32 | 0 | 127 |

|  | *   Coeff1_Uls_T_f32 | float32 | 0 | 127 |

| Return Value | Out_MotNwtMtr_T_f32 | float32 | -127 | 127 |

Function Name

AdjSigFil

Type

Min

Max

Arguments Passed

In1_MotNwtMtr_T_f32

float32

-127

127

Zm_Uls_T_f32

float32

0.244742

1.0

Pk_Uls_T_f32

float32

0.244742

1.0

B0_Uls_T_f32

float32

0.249683

4.005074

MagAtFreq_Uls_T_f32

float32

0.414213562

2.414213562

* Coeff1_Uls_T_f32

float32

0

127

* Coeff1_Uls_T_f32

float32

0

127

Return Value

Out_MotNwtMtr_T_f32

float32

-127

127

### Description

"Filter1 / Filter2 " block implementation.

### Local Function #7

| Function Name | SetNTCBlk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed |  |  |  |  |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

SetNTCBlk

Type

Min

Max

Arguments Passed

Return Value

None

### Description

'Set NTC Block' implementation.

### Local Function #8

| Function Name | MaxMagDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CmdAmp_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | FltStat_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

MaxMagDiag

Type

Min

Max

Arguments Passed

CmdAmp_MotNwtMtr_T_f32

float32

-8.8

8.8

Return Value

FltStat_Cnt_T_lgc

boolean

FALSE

TRUE

### Description

"MaxMagDiag" block implementation.

### Local Function #9

| Function Name | DcTrendDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WIRCmd_MtrNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | FltStat_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

DcTrendDiag

Type

Min

Max

Arguments Passed

WIRCmd_MtrNwtMtr_T_f32

float32

-8.8

8.8

Return Value

FltStat_Cnt_T_lgc

boolean

FALSE

TRUE

### Description

" DcTrendDiag" block implementation.

### Local Function #10

| Function Name | FrequencyDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WIRCmd_MtrNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | FreqEst_Hz_T_f32 | float32 | 0.005 | 60 |

|  | Enable_Uls_T_f32 | float32 | 0 | 1 |

|  | CmdAmp_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

| Return Value | FltStat_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

FrequencyDiag

Type

Min

Max

Arguments Passed

WIRCmd_MtrNwtMtr_T_f32

float32

-8.8

8.8

FreqEst_Hz_T_f32

float32

0.005

60

Enable_Uls_T_f32

float32

0

1

CmdAmp_MotNwtMtr_T_f32

float32

-8.8

8.8

Return Value

FltStat_Cnt_T_lgc

boolean

FALSE

TRUE

### Description

' FrequencyDiag ' block implementation.

### Local Function #11

| Function Name | WhlSpdCorrDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WhlRiFrq_Hz_T_f32 | float32 | 0.01 | 60 |

|  | WhlLeFrq_Hz_T_f32 | float32 | 0.01 | 60 |

| Return Value | FltStat_Cnt_T_lgc | boolean | FALSE | TRUE |

Function Name

WhlSpdCorrDiag

Type

Min

Max

Arguments Passed

WhlRiFrq_Hz_T_f32

float32

0.01

60

WhlLeFrq_Hz_T_f32

float32

0.01

60

Return Value

FltStat_Cnt_T_lgc

boolean

FALSE

TRUE

### Description

" WhlSpdCorrDiag" block implementation.

### Local Function #12

| Function Name | ElpdTi | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FltStsTrue_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | PrevFltStsTrue_Cnt_T_lgc | boolean | FALSE | TRUE |

|  | RefTi_Sec_T_u32 | uint 32 | Full range | Full range |

| Return Value | ElpdTi_MilliSec_T_f32 | float32 | Full range | Full range |


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Application Software](../).
