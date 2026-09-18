---
title: "Assist Path Firewall (SF034A_AssiPahFwl)"
description: "Assist Path Firewall: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Assist Path Firewall component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF034A_AssiPahFwl_Design` | Design package |
| `SF034A_AssiPahFwl_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF034A_AssiPahFwl_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF034A_AssiPahFwl_Impl` |  |
| C sources | `AssiPahFwl.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `AssiPahFwl.dcf`, `AssiPahFwl_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `AssiPahFwl.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF034A_AssiPahFwl_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF034A_AssiPahFwl_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF034A_AssiPahFwl_Impl/src/AssiPahFwl.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF034A_AssiPahFwl_DDReport.txt`

- **Source path in repository:** `SF034A_AssiPahFwl_Design/Reports/SF034A_AssiPahFwl_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF034A_AssiPahFwl_DataDict
11-Feb-2016 08:28:32
Tool Release:  2.28.0



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
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
AssiLnrGainEna              	Cannot match name to list of known Nexteer signals.
MfgEnaSt                    	Cannot match name to list of known Nexteer signals.
(variables: 8, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

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
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 12, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 6, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (36 more lines in the source file). ...*

### `AssiPahFwl_IntegrationManual.doc`

- **Source path in repository:** `SF034A_AssiPahFwl_Impl/doc/AssiPahFwl_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `133 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AssiPahFwl_MDD.docx`

- **Source path in repository:** `SF034A_AssiPahFwl_Impl/doc/AssiPahFwl_MDD.docx`
- **Format:** `.docx`
- **Size:** `111 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

AssiPahFwl

Feb 05, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sarika Natu,

KPIT Technologies,

India

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sarika Natu(KPIT Technologies) | 1.0 | 05 -Feb-2016 |

Description

Author

Version

Date

Initial Version

Sarika Natu(KPIT Technologies)

1.0

05-Feb-2016

Table of Contents

1AssiPahFwl & High-Level Description5

2Design details of software module6

2.1Graphical representation of AssiPahFwl6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: AssiPahFwl_Init18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: AssiPahFwl_Per18

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

4.4.3Local Function #39

4.4.3.1Design Rationale9

4.4.3.2Processing10

4.4.4Local Function #410

4.4.4.1Design Rationale10

4.4.4.2Processing10

4.4.5Local Function #510

4.4.5.1Design Rationale10

4.4.5.2Processing10

4.5GLOBAL Function/Macro Definitions11

5Known Limitations with Design12

6UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## AssiPahFwl & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of AssiPahFwl

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| NODEBSTEP_CNT_U16 | NA | NA | 65535U |

Constant Name

Resolution

Units

Value

NODEBSTEP_CNT_U16

NA

NA

65535U

## Software Component Implementation

### Sub-Module Functions

### Init: AssiPahFwl_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: AssiPahFwl_Per1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runnables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | Dynamic_Assi_Boundary | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VehSpd_Kph_T_u9p7 | Uint16 | 0 | 511 |

|  | HwTq_HwNwtMtr_T_f32 | Float32 | -10.0 | 10.0 |

|  | LoFrqInp_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | * LowrBndLpFil_MotNwtMtr_T_f32 | F loat32 * | -16 | 16 |

|  | * UpprBndLpFil_MotNwtMtr_T_f32 | F loat32 * | -16 | 16 |

| Return Value | HiFrqAssiLimd_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

Function Name

Dynamic_Assi_Boundary

Type

Min

Max

Arguments Passed

VehSpd_Kph_T_u9p7

Uint16

0

511

HwTq_HwNwtMtr_T_f32

Float32

-10.0

10.0

LoFrqInp_MotNwtMtr_T_f32

Float32

-16

16

*LowrBndLpFil_MotNwtMtr_T_f32

Float32*

-16

16

*UpprBndLpFil_MotNwtMtr_T_f32

Float32*

-16

16

Return Value

HiFrqAssiLimd_MotNwtMtr_T_f32

Float32

-16

16

### Design Rationale

LowrBndLpFil_MotNwtMtr_T_f32  and UpprBndLpFil_MotNwtMtr_T_f32 will be updated in this function.

### Processing

Refer to the subsystems 'Determine HiFreqAsst Boundaries' and 'Low pass filter boundaries' in FDD.

### Local Function #2

| Function Name | Base_Assi_Boundary | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTrq_HwNwtMtr_T_f32 | Float32 | -20.0 | 20.0 |

|  | VehSpd_Kph_T_u9p7 | Uint16 | 0 | 511 |

|  | AssiCmdBas_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

|  | BasAssiLowrBnd_MotNwtMtr_T_f32 | float32* | -16 | 16 |

|  | BasAssiUpprBnd_MotNwtMtr_T_f32 | float32* | -16 | 16 |

| Return Value | BasAssiLimd_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

Function Name

Base_Assi_Boundary

Type

Min

Max

Arguments Passed

HwTrq_HwNwtMtr_T_f32

Float32

-20.0

20.0

VehSpd_Kph_T_u9p7

Uint16

0

511

AssiCmdBas_MotNwtMtr_T_f32

Float32

-8.8

8.8

BasAssiLowrBnd_MotNwtMtr_T_f32

float32*

-16

16

BasAssiUpprBnd_MotNwtMtr_T_f32

float32*

-16

16

Return Value

BasAssiLimd_MotNwtMtr_T_f32

Float32

-16

16

### Design Rationale

BasAssiLowrBnd_MotNwtMtr_T_f32 and BasAssiUpprBnd_MotNwtMtr_T_f32 will be updated in this function

### Processing

Refer the subsystem ‘Determine_BaseAsst_Boundaries’ implementation in FDD.

### Local Function #3

| Function Name | Det_Boundary_Lim | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AssiCmdBas_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

|  | BasAssiUpprBnd_MotNwtMtr_T_f32 | Float32 | - 16 | 16 |

|  | BasAssiLowrBnd_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | LowrBndLpFil_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | UpprBndLpFil_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | LoFrqInp_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | HiFrqOverBnd_MotNwtMtr_T_Logl | Boolean* | FALSE | TRUE |

|  | BasAssiOverBnd_MotNwtMtr_T_Logl | Boolean* | FALSE | TRUE |

| Return Value | AssiFwlFailSts_Cnt_T_Logl | Boolean | FALSE | TRUE |

Function Name

Det_Boundary_Lim

Type

Min

Max

Arguments Passed

AssiCmdBas_MotNwtMtr_T_f32

Float32

-8.8

8.8

BasAssiUpprBnd_MotNwtMtr_T_f32

Float32

-16

16

BasAssiLowrBnd_MotNwtMtr_T_f32

Float32

-16

16

LowrBndLpFil_MotNwtMtr_T_f32

Float32

-16

16

UpprBndLpFil_MotNwtMtr_T_f32

Float32

-16

16

LoFrqInp_MotNwtMtr_T_f32

Float32

-16

16

HiFrqOverBnd_MotNwtMtr_T_Logl

Boolean*

FALSE

TRUE

BasAssiOverBnd_MotNwtMtr_T_Logl

Boolean*

FALSE

TRUE

Return Value

AssiFwlFailSts_Cnt_T_Logl

Boolean

FALSE

TRUE

### Design Rationale

HiFrqOverBnd_MotNwtMtr_T_Logl  and BasAssiOverBnd_MotNwtMtr_T_Logl will be updated in this function.

### Processing

Refer to the section ‘Check both command paths for reaching boundary limits, if so begin de bounce counters’ in FDD.

### Local Function #4

| Function Name | Assist_Recovery_Cond | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AssiCmdBas_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

|  | DftAssi_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

|  | AssiFwlFailSts_Cnt_T_Logl | Boolean | FASLE | TRUE |

|  | SumInp_MotNwtMtr_T_f32 | Float32 | -17.6 | 17.6 |

|  | BasAssiLimd_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | HiFrqInp_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | HiFrqAssiLimd_MotNwtMtr_T_f32 | Float32 | -16 | 16 |

|  | BasAssiOverBnd_MotNwtMtr_T_Logl | Boolean | FALSE | TRUE |

|  | HiFrqOverBnd_MotNwtMtr_T_Logl | Boolean | FALSE | TRUE |

|  | * AssiPahLimrActv_Uls_T_f32 | Float32 | FASLE | TRUE |

| Return Value | CombdAssiDft_MotNwtMtr_T_f32 | Float32 | -8.8 | 8.8 |

Function Name

Assist_Recovery_Cond

Type

Min

Max

Arguments Passed

AssiCmdBas_MotNwtMtr_T_f32

Float32

-8.8

8.8

DftAssi_MotNwtMtr_T_f32

Float32

-8.8

8.8

AssiFwlFailSts_Cnt_T_Logl

Boolean

FASLE

TRUE

SumInp_MotNwtMtr_T_f32

Float32

-17.6

17.6

BasAssiLimd_MotNwtMtr_T_f32

Float32

-16

16

HiFrqInp_MotNwtMtr_T_f32

Float32

-16

16

HiFrqAssiLimd_MotNwtMtr_T_f32

Float32

-16

16

BasAssiOverBnd_MotNwtMtr_T_Logl

Boolean

FALSE

TRUE

HiFrqOverBnd_MotNwtMtr_T_Logl

Boolean

FALSE

TRUE

*AssiPahLimrActv_Uls_T_f32

Float32

FASLE

TRUE

Return Value

CombdAssiDft_MotNwtMtr_T_f32

Float32

-8.8

8.8

### Design Rationale

AssiPahLimrActv_Uls_T_f32 will be updated in this function

### Processing

Refer to the section ‘Check Input commands vs. Fwl Output command for Assist Recovery Conditions’ in FDD.

### Local Function #5

| Function Name | Set_Faults | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HiFrqOverBnd_MotNwtMtr_T_Logl | Boolean | FASLE | TRUE |

|  | BasAssiOverBnd_MotNwtMtr_T_Logl | Boolean | FASLE | TRUE |

| Return Value | None |  |  |  |

Function Name

Set_Faults

Type

Min

Max

Arguments Passed

HiFrqOverBnd_MotNwtMtr_T_Logl

Boolean

FASLE

TRUE

BasAssiOverBnd_MotNwtMtr_T_Logl

Boolean

FASLE

TRUE

Return Value

None

### Design Rationale

None

### Processing

Refer ‘Set_Faults’ subsystem in FDD.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

## UNIT TEST CONSIDERATION

None

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

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

Back to [Application Software](../).
