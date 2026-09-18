---
title: "End of Travel Protection Firewall (SF027A_EotProtnFwl)"
description: "End of Travel Protection Firewall: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The End of Travel Protection Firewall component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF027A_EotProtnFwl_Design` | Design package |
| `SF027A_EotProtnFwl_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF027A_EotProtnFwl_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF027A_EotProtnFwl_Impl` |  |
| C sources | `EotProtnFwl.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `EotProtnFwl.dcf`, `EotProtnFwl_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `EotProtnFwl.dpa`, `RteGen.bat`, `SF027A_EotProtnFwl_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF027A_EotProtnFwl_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF027A_EotProtnFwl_Impl/src/EotProtnFwl.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF027A_EotProtnFwl_DDReport.txt`

- **Source path in repository:** `SF027A_EotProtnFwl_Design/Reports/SF027A_EotProtnFwl_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF027A_EotProtnFwl_DataDict
02-Sep-2016 09:31:43
Tool Release:  2.45.0



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
(variables: 8, errors: 0)

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
(variables: 6, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 4, errors: 0)

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
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (33 more lines in the source file). ...*

### `EotProtnFwl_Integration Manual.doc`

- **Source path in repository:** `SF027A_EotProtnFwl_Impl/doc/EotProtnFwl_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `133 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `EotProtnFwl_MDD.docx`

- **Source path in repository:** `SF027A_EotProtnFwl_Impl/doc/EotProtnFwl_MDD.docx`
- **Format:** `.docx`
- **Size:** `104 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

EotProtnFwl

Feb 01, 2016

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

| Initial Version | Sarika Natu (KPIT Technologies) | 1.0 | 01-Feb-2016 |

Description

Author

Version

Date

Initial Version

Sarika Natu(KPIT Technologies)

1.0

01-Feb-2016

Table of Contents

1EotProtnFwl & High-Level Description5

2Design details of software module6

2.1Graphical representation of EotProtnFwl6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: EotProtnFwl_Init18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: EotProtnFwl_Per18

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

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## EotProtnFwl & High-Level Description

EOT Protection Firewall function is safety function which imposes a firewall limit to the Assist_EOTDamping and EOTActvCmd motor commands generated by SF-018A.

## Design details of software module

### Graphical representation of EotProtnFwl

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

Refer FDD

## Software Component Implementation

### Sub-Module Functions

### Init: EotProtnFwl_Init1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: EotProtnFwl_Per1

### Design Rationale

EotProtnFwl_Per1 function is divided into various functions to reduce the cyclomatic complexity.

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

| Function Name | DetEOTDamping | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EotDampgCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | EotProtnDi_Cnt_T_Logl | boolean | 0 | 1 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 .0 | 1440 .0 |

|  | MotVelCrf_MotRadPerSec_T_f32 | float32 | -   1118 .0 | 1118 .0 |

|  | EotProtnFwlPinionAgConfSts_Cnt_T_Logl | boolean | 0 | 1 |

|  | VehSpd_Kph_T_u9p7 | uint16 | 0 | 511 |

|  | MfgEnaSt_Cnt_T_Enum | Enum | 0 | 1 |

|  | *   EotDampgFwlReached_Cnt_T_Logl | boolean | 0 | 1 |

| Return  by  Value | EotDampgCmdLimd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

Function Name

DetEOTDamping

Type

Min

Max

Arguments Passed

EotDampgCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

EotProtnDi_Cnt_T_Logl

boolean

0

1

HwAg_HwDeg_T_f32

float32

-1440.0

1440.0

MotVelCrf_MotRadPerSec_T_f32

float32

- 1118.0

1118.0

EotProtnFwlPinionAgConfSts_Cnt_T_Logl

boolean

0

1

VehSpd_Kph_T_u9p7

uint16

0

511

MfgEnaSt_Cnt_T_Enum

Enum

0

1

* EotDampgFwlReached_Cnt_T_Logl

boolean

0

1

Return by Value

EotDampgCmdLimd_MotNwtMtr_T_f32

float32

-8.8

8.8

### Design Rationale

This function updates EotDampgFwlReached_Cnt_T_Logl

### Processing

Refer Active/Inactive region for EOTDamping Command implementation in model

### Local Function #2

| Function Name | DetEOTActive | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | EotActvCmd_MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

|  | EotProtnDi_Cnt_T_Logl | boolean | 0 | 1 |

|  | HwAg_HwDeg_T_f32 | float32 | -1440 .0 | 1440 .0 |

|  | EotProtnFwlPinionAgConfSts_Cnt_T_Logl | boolean | 0 | 1 |

|  | VehSpd_Kph_T_u9p7 | uint16 | 0 | 511 |

|  | MfgEnaSt_Cnt_T_Enum | Enum | 0 | 1 |

|  | *   EotActvCmdFwlReached_Cnt_T_Logl | boolean | 0 | 1 |

| Return Value | EotActvCmdLimd _MotNwtMtr_T_f32 | float32 | -8.8 | 8.8 |

Function Name

DetEOTActive

Type

Min

Max

Arguments Passed

EotActvCmd_MotNwtMtr_T_f32

float32

-8.8

8.8

EotProtnDi_Cnt_T_Logl

boolean

0

1

HwAg_HwDeg_T_f32

float32

-1440.0

1440.0

EotProtnFwlPinionAgConfSts_Cnt_T_Logl

boolean

0

1

VehSpd_Kph_T_u9p7

uint16

0

511

MfgEnaSt_Cnt_T_Enum

Enum

0

1

* EotActvCmdFwlReached_Cnt_T_Logl

boolean

0

1

Return Value

EotActvCmdLimd_MotNwtMtr_T_f32

float32

-8.8

8.8

### Design Rationale

This function updates EotActvCmdFwlReached_Cnt_T_Logl

### Processing

Refer Active/Inactive region for EOT Active Command implementation in model

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

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

| 5 | SF027_EotProtnFwl_Desgin | Please refer synergy subproject version |

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

SF027_EotProtnFwl_Desgin

Please refer synergy subproject version

Back to [Application Software](../).
