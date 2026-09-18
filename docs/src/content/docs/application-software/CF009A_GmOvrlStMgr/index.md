---
title: "General Motors Overall State Manager (CF009A_GmOvrlStMgr)"
description: "General Motors Overall State Manager: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Overall State Manager component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CF009A_GmOvrlStMgr_Design` | Design package |
| `CF009A_GmOvrlStMgr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF009A_GmOvrlStMgr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CF009A_GmOvrlStMgr_Impl` |  |
| C sources | `GmOvrlStMgr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmOvrlStMgr.dcf`, `GmOvrlStMgr_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF009A_GmOvrlStMgr_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmOvrlStMgr.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF009A_GmOvrlStMgr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF009A_GmOvrlStMgr_Impl/src/GmOvrlStMgr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CF009A_GmOvrlStMgr_DDReport.txt`

- **Source path in repository:** `CF009A_GmOvrlStMgr_Design/Reports/CF009A_GmOvrlStMgr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CF009A_GmOvrlStMgr_DataDict
05-Dec-2016 18:19:27
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
(variables: 2, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 2, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 5, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 36, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 10, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 38, errors: 0)

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
(variables: 2, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 27, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `GmOvrlStMgr_IntegrationManual.doc`

- **Source path in repository:** `CF009A_GmOvrlStMgr_Impl/doc/GmOvrlStMgr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `145 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmOvrlStMgr_MDD.docx`

- **Source path in repository:** `CF009A_GmOvrlStMgr_Impl/doc/GmOvrlStMgr_MDD.docx`
- **Format:** `.docx`
- **Size:** `148 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmOvrlStMgr

Feb 02, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Jayakrishnan T,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu Varadapureddi | 1 | 6 - Oct -2015 |

| Added HwTq based intervention for LKA, handwheel buzz based on LoA key cycles | Nick Saxton | 2 | 11-Feb-2016 |

| Changed argument names of ESCFlt local function | Nick Saxton | 3 | 13-Jun-2016 |

| Updated graphical representation and edited local function section | Nick Saxton | 4 | 24-Jun-2016 |

| Updated for FDD v4.0.0 | Nick Saxton | 5 | 22-Aug-2016 |

| Updated to design version 4.1 .0 | TATA | 6 | 12-Dec-16 |

| Anomaly fix EA4#8726, Removed local function LkaCheck | JK | 7 | 02-Feb-17 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

6-Oct-2015

Added HwTq based intervention for LKA, handwheel buzz based on LoA key cycles

Nick Saxton

2

11-Feb-2016

Changed argument names of ESCFlt local function

Nick Saxton

3

13-Jun-2016

Updated graphical representation and edited local function section

Nick Saxton

4

24-Jun-2016

Updated for FDD v4.0.0

Nick Saxton

5

22-Aug-2016

Updated to design version 4.1.0

TATA

6

12-Dec-16

Anomaly fix EA4#8726, Removed local function LkaCheck

JK

7

02-Feb-17

Table of Contents

1GmOvrlStMgr High-Level Description6

2Design details of software module7

2.1Graphical representation of GmOvrlStMgr7

2.2Data Flow Diagram8

2.2.1Component level DFD8

2.2.2Function level DFD8

3Constant Data Dictionary9

3.1Program (fixed) Constants9

3.1.1Embedded Constants9

4Software Component Implementation10

4.1Sub-Module Functions10

4.1.1Init: GmOvrlStMgrInit110

4.1.1.1Design Rationale10

4.1.1.2Module Outputs10

4.1.2Per: GmOvrlStMgrPer110

4.1.2.1Design Rationale10

4.1.2.2Store Module Inputs to Local copies10

4.1.2.3(Processing of function)………10

4.1.2.4Store Local copy of outputs into Module Outputs10

4.2Server Runables10

4.2.1GetGmLoaIgnCntr_Oper10

4.2.1.1Design Rationale10

4.2.1.2Store Module Inputs to Local copies10

4.2.1.3(Processing of function)………10

4.2.1.4Store Local copy of outputs into Module Outputs10

4.2.2SetGmLoaIgnCntr_Oper11

4.2.2.1Design Rationale11

4.2.2.2Store Module Inputs to Local copies11

4.2.2.3(Processing of function)………11

4.2.2.4Store Local copy of outputs into Module Outputs11

4.3Interrupt Functions11

4.4Module Internal (Local) Functions11

4.4.1Local Function #111

4.4.1.1Description11

4.4.2Local Function #211

4.4.2.1Description11

4.4.3Local Function #311

4.4.3.1Description12

4.4.4Local Function #412

4.4.4.1Description12

4.4.5Local Function #512

4.4.5.1Description12

4.4.6Local Function #612

4.4.6.1Description12

4.4.7Local Function #713

4.4.7.1Description13

4.4.8Local Function #813

4.4.8.1Description13

4.4.9Local Function #913

4.4.9.1Description14

4.4.10Local Function #1014

4.4.10.1Description14

4.4.11Local Function #1114

4.4.11.1Description15

4.4.12Local Function #1215

4.4.12.1Description15

4.4.13Local Function #1316

4.4.13.1Description16

4.4.14Local Function #1416

4.4.14.1Description16

4.4.15Local Function #1516

4.4.15.1Description16

4.4.16Local Function #1616

4.4.16.1Description17

4.4.17Local Function #1717

4.4.17.1Description17

4.4.18Local Function #1817

4.4.18.1Description17

4.4.19Local Function #1917

4.4.19.1Description17

4.4.20Local Function #2017

4.4.20.1Description18

4.4.21Local Function #2118

4.4.21.1Description18

4.4.22Local Function #2218

4.4.22.1Description18

4.4.23Local Function #2318

4.4.23.1Description19

4.4.24Local Function #2419

4.4.24.1Description19

4.5GLOBAL Function/Macro Definitions19

5Known Limitations with Design20

6UNIT TEST CONSIDERATION21

Appendix AAbbreviations and Acronyms22

Appendix BGlossary23

Appendix CReferences24

## GmOvrlStMgr High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of GmOvrlStMgr

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: GmOvrlStMgrInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: GmOvrlStMgrPer1

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

#### GetGmLoaIgnCntr_Oper

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

#### SetGmLoaIgnCntr_Oper

### Design Rationale

Refer FDD for the overall functionality.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | VehStandStillTmrElpdChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpdSecurMax_Kph_T_f32 | float32 | 0 | 5 11 |

| Return Value | VehStandStillTiExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

VehStandStillTmrElpdChk

Type

Min

Max

Arguments Passed

VehSpdSecurMax_Kph_T_f32

float32

0

511

Return Value

VehStandStillTiExcdd_Cnt_T_logl

boolean

FALSE

TRUE

### Description

"Timer for VehStandStill" block implementation.

### Local Function #2

| Function Name | ShiftLvrRvsTmrElpdChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ShiftLvrRvs_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | ShiftLvrRvsTiExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ShiftLvrRvsTmrElpdChk

Type

Min

Max

Arguments Passed

ShiftLvrRvs_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

ShiftLvrRvsTiExcdd_Cnt_T_logl

boolean

FALSE

TRUE

### Description

"Timer for ShiftLvrRvs" block implementation.

### Local Function #3

| Function Name | ApaIntv | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | float32 | -10 | 10 |

| Return Value | ApaIntv_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ApaIntv

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

float32

-10

10

Return Value

ApaIntv_Cnt_T_logl

boolean

FALSE

TRUE

### Description

"ApaIntv" block implementation.

### Local Function #4

| Function Name | HaptcEnaDurnElpdChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwHaptcEna_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | HwHaptcEnaDurnExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

HaptcEnaDurnElpdChk

Type

Min

Max

Arguments Passed

HwHaptcEna_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

HwHaptcEnaDurnExcdd_Cnt_T_logl

boolean

FALSE

TRUE

### Description

"Timer for HwHaptcEna" block implementation.

### Local Function #5

| Function Name | LkaFltActvChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Msg17DBusHiSpdMiss_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg180BusHiSpdMiss_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg180BusHiSpdInvld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg1E9BusHiSpdMiss_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg214BusHiSpdInvld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg214BusHiSpdMiss_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehSpdSecurMax Vld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehSpdSecurMin Vld_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | LkaFlt_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

LkaFltActvChk

Type

Min

Max

Arguments Passed

Msg17DBusHiSpdMiss_Cnt_T_logl

boolean

FALSE

TRUE

Msg180BusHiSpdMiss_Cnt_T_logl

boolean

FALSE

TRUE

Msg180BusHiSpdInvld_Cnt_T_logl

boolean

FALSE

TRUE

Msg1E9BusHiSpdMiss_Cnt_T_logl

boolean

FALSE

TRUE

Msg214BusHiSpdInvld_Cnt_T_logl

boolean

FALSE

TRUE

Msg214BusHiSpdMiss_Cnt_T_logl

boolean

FALSE

TRUE

VehSpdSecurMaxVld_Cnt_T_logl

boolean

FALSE

TRUE

VehSpdSecurMinVld_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

LkaFlt_Cnt_T_logl

boolean

FALSE

TRUE

### Description

Determination of 'LkaFlt'.

### Local Function #6

| Function Name | LkaInhbChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Msg17DBusHiSpdInvld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehStabyEnhmtActv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | AbsActvProtd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | Msg1E9BusHiSpdInvld_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | LkaInhb_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

LkaInhbChk

Type

Min

Max

Arguments Passed

Msg17DBusHiSpdInvld_Cnt_T_logl

boolean

FALSE

TRUE

VehStabyEnhmtActv_Cnt_T_logl

boolean

FALSE

TRUE

AbsActvProtd_Cnt_T_logl

boolean

FALSE

TRUE

Msg1E9BusHiSpdInvld_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

LkaInhb_Cnt_T_logl

boolean

FALSE

TRUE

### Description

Determination of ' LkaInhb'.

### Local Function #7

| Function Name | ApaRcvrlFltChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Msg1F5BusHiSpdInvld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehSpdSecurMax Vld_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehSpdSecurMin Vld_Cnt_T_logl | boolean | FALSE | TRUE |

| Return Value | ApaRcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

Function Name

ApaRcvrlFltChk

Type

Min

Max

Arguments Passed

Msg1F5BusHiSpdInvld_Cnt_T_logl

boolean

FALSE

TRUE

VehSpdSecurMaxVld_Cnt_T_logl

boolean

FALSE

TRUE

VehSpdSecurMinVld_Cnt_T_logl

boolean

FALSE

TRUE

Return Value

ApaRcvrlFlt_Cnt_T_logl

boolean

FALSE

TRUE

### Description

Determination of ‘ ApaRcvrlFlt’.

### Local Function #8

| Function Name | ApaTmpInhbExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ApaNrcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | LoaSt_Cnt_T_enum | LoaSt1  (enum) | LOAST_NORM | LOAST_IMDTSHTDWNREQD |

|  | VehSpdSecurMax_Kph_T_f32 | float32 | 0 | 511 |

|  | ApaEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwHaptcEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ApaRcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysSt_Cnt_T_enum | SysSt1 | SYSST_DI | SYSST_WRMIN |

|  | * ApaSt_Cnt_T_u08 | uint8 | 0 | 4 |

| Return Value | None |  |  |  |

Function Name

ApaTmpInhbExitCdnsChk

Type

Min

Max

Arguments Passed

ApaNrcvrlFlt_Cnt_T_logl

boolean

FALSE

TRUE

LoaSt_Cnt_T_enum

LoaSt1 (enum)

LOAST_NORM

LOAST_IMDTSHTDWNREQD

VehSpdSecurMax_Kph_T_f32

float32

0

511

ApaEna_Cnt_T_logl

boolean

FALSE

TRUE

HwHaptcEna_Cnt_T_logl

boolean

FALSE

TRUE

ApaRcvrlFlt_Cnt_T_logl

boolean

FALSE

TRUE

SysSt_Cnt_T_enum

SysSt1

SYSST_DI

SYSST_WRMIN

*ApaSt_Cnt_T_u08

uint8

0

4

Return Value

None

### Description

This function validates conditions for all state transitions from ‘ APA Temporarily Inhibited’ state.

‘*ApaSt_Cnt_T_u08’ is an output of this function.

### Local Function #9

| Function Name | ApaActvExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | ApaNrcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | LoaSt_Cnt_T_enum | LoaSt1  (enum) | LOAST_NORM | LOAST_IMDTSHTDWNREQD |

|  | VehSpdSecurMax_Kph_T_f32 | float32 | 0 | 511 |

|  | ApaEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwHaptcEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ApaRcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ApaIntv_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysSt_Cnt_T_enum | SysSt1 | SYSST_DI | SYSST_WRMININ |

|  | * ApaSt_Cnt_T_u08 | uint8 | 0 | 4 |

| Return Value | None |  |  |  |

Function Name

ApaActvExitCdnsChk

Type

Min

Max

Arguments Passed

ApaNrcvrlFlt_Cnt_T_logl

boolean

FALSE

TRUE

LoaSt_Cnt_T_enum

LoaSt1 (enum)

LOAST_NORM

LOAST_IMDTSHTDWNREQD

VehSpdSecurMax_Kph_T_f32

float32

0

511

ApaEna_Cnt_T_logl

boolean

FALSE

TRUE

HwHaptcEna_Cnt_T_logl

boolean

FALSE

TRUE

ApaRcvrlFlt_Cnt_T_logl

boolean

FALSE

TRUE

ApaIntv_Cnt_T_logl

boolean

FALSE

TRUE

SysSt_Cnt_T_enum

SysSt1

SYSST_DI

SYSST_WRMININ

*ApaSt_Cnt_T_u08

uint8

0

4

Return Value

None

### Description

This function validates conditions for all state transitions from ‘ APA Active’ state.

‘*ApaSt_Cnt_T_u08’ is an output of this function.

### Local Function #10

| Function Name | ApaCtrlAvlExitCdnsChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpdSecurMax_Kph_T_f32 | float32 | 0 | 511 |

|  | ApaRcvrlFlt_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwHaptcEnaDurnExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | VehStandStillTiExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ShiftLvrRvsTiExcdd_Cnt_T_logl | boolean | FALSE | TRUE |

|  | ApaEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HwHaptcEna_Cnt_T_logl | boolean | FALSE | TRUE |

|  | HaptcStTranActvToWaitFlg_Cnt_T_logl | boolean | FALSE | TRUE |

|  | TranHaptcWaitToApaStActvFlg_Cnt_T_logl | boolean | FALSE | TRUE |

|  | SysSt_Cnt_T_enum | SysSt1 | SYSST_DI | SYSST_WRMININ |

|  | * HaptcSt_Cnt_T_u08 | uint8 | 0 | 2 |

|  | * ApaSt_Cnt_T_u08 | uint8 | 0 | 4 |

| Return Value | None |  |  |  |


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Application Software](../).
