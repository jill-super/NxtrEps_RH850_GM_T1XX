---
title: "General Motors Road Wheel Input Qualifier (CF018A_GmRoadWhlInQlfr)"
description: "General Motors Road Wheel Input Qualifier: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Road Wheel Input Qualifier component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CF018A_GmRoadWhlInQlfr_Design` | Design package |
| `CF018A_GmRoadWhlInQlfr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF018A_GmRoadWhlInQlfr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CF018A_GmRoadWhlInQlfr_Impl` |  |
| C sources | `GmRoadWhlInQlfr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmRoadWhlInQlfr.dcf`, `GmRoadWhlInQlfr_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF018A_GmRoadWhlInQlfr_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmRoadWhlInQlfr.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF018A_GmRoadWhlInQlfr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF018A_GmRoadWhlInQlfr_Impl/src/GmRoadWhlInQlfr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CF018A_GmRoadWhlInQlfr_DDReport.txt`

- **Source path in repository:** `CF018A_GmRoadWhlInQlfr_Design/Reports/CF018A_GmRoadWhlInQlfr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CF018A_GmRoadWhlInQlfr_DataDict
30-Nov-2016 18:31:44
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
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
WhlPlsPerRev                	.DocUnits:	Not on approved list.
(variables: 8, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 3, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 2, errors: 0)

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
PrevRawLeWhlFrq             	.EngMax:    	Value is unusually high.
PrevRawRiWhlFrq             	.EngMax:    	Value is unusually high.
(variables: 12, errors: 2)

--------------------------------------------------------------------------------------------
```
*... truncated (34 more lines in the source file). ...*

### `GmRoadWhlInQlfr_IntegrationManual.doc`

- **Source path in repository:** `CF018A_GmRoadWhlInQlfr_Impl/doc/GmRoadWhlInQlfr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmRoadWhlInQlfr_MDD.docx`

- **Source path in repository:** `CF018A_GmRoadWhlInQlfr_Impl/doc/GmRoadWhlInQlfr_MDD.docx`
- **Format:** `.docx`
- **Size:** `104 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmRoadWhlInQlfr

March 2, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | N. Saxton | 1.0 | 02-Mar-2016 |

Description

Author

Version

Date

Initial Version

N. Saxton

1.0

02-Mar-2016

Table of Contents

1GmRoadWhlInQlfr High-Level Description5

2Design details of software module6

2.1Graphical representation of GmRoadWhlInQlfr6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: GmRoadWhlInQlfrInit18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: GmRoadWhlInQlfrPer18

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

4.4.3.1Design Rationale10

4.4.3.2Processing10

4.5GLOBAL Function/Macro Definitions10

5Known Limitations with Design11

6UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## GmRoadWhlInQlfr High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of GmRoadWhlInQlfr

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

Refer DataDict.m for constants

## Software Component Implementation

### Sub-Module Functions

Refer FDD

### Init: GmRoadWhlInQlfrInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: GmRoadWhlInQlfrPer1

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

| Function Name | CalcLeWhlFrqAndFrqVld | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WhlRotlStsTiStampResl_SecPerCnt_T_f32 | Float32 | 2e-09 | 4.084e-0 6 |

|  | WhlLeDstPlsCntr_Cnt_T_u16 | Uint16 | 0 | 1023 |

|  | WhlLeDstTiStamp_Cnt_T_u16 | Uint16 | 0 | 65535 |

|  | WhlPlsPerRev_CntPerRoadWhlRev_T_u08 | Uint08 | 1 | 127 |

|  | * LeWhlFrqVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * WhlLeFrq_Hz_T_f32 | Float32 | 0.01 | 60 |

|  | * LeFrqOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * LeFrqChgOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * LeWhlDiagFlg_Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

CalcLeWhlFrqAndFrqVld

Type

Min

Max

Arguments Passed

WhlRotlStsTiStampResl_SecPerCnt_T_f32

Float32

2e-09

4.084e-06

WhlLeDstPlsCntr_Cnt_T_u16

Uint16

0

1023

WhlLeDstTiStamp_Cnt_T_u16

Uint16

0

65535

WhlPlsPerRev_CntPerRoadWhlRev_T_u08

Uint08

1

127

*LeWhlFrqVld_Cnt_T_logl

Boolean

FALSE

TRUE

*WhlLeFrq_Hz_T_f32

Float32

0.01

60

*LeFrqOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

*LeFrqChgOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

*LeWhlDiagFlg_Cnt_T_logl

Boolean

FALSE

TRUE

* LeWhlFrqVld_Cnt_T_logl,  * WhlLeFrq_Hz_T_f32, *LeFrqOutOfRng_Cnt_T_logl, *LeFrqChgOutOfRng_Cnt_T_logl and *LeWhlDiagFlg_Cnt_T_logl  are outputs of this function

### Design Rationale

Implementation of "Chk Curr and Prev LeWhlDstTiStamp" block

### Processing

Refer FDD

### Local Function #2

| Function Name | CalcRi WhlFrqAndFrqVld | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | WhlRotlStsTiStampResl_SecPerCnt_T_f32 | Float32 | 2e-09 | 4.084e-06 |

|  | WhlRi DstPlsCntr_Cnt_T_u16 | Uint16 | 0 | 1023 |

|  | WhlRi DstTiStamp_Cnt_T_u16 | Uint16 | 0 | 65535 |

|  | WhlPlsPerRev_CntPerRoadWhlRev_T_u08 | Uint08 | 1 | 127 |

|  | * Ri WhlFrqVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * WhlRi Frq_Hz_T_f32 | Float32 | 0.01 | 60 |

|  | * Ri FrqOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * Ri FrqChgOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | * Ri WhlDiagFlg_Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

CalcRiWhlFrqAndFrqVld

Type

Min

Max

Arguments Passed

WhlRotlStsTiStampResl_SecPerCnt_T_f32

Float32

2e-09

4.084e-06

WhlRiDstPlsCntr_Cnt_T_u16

Uint16

0

1023

WhlRiDstTiStamp_Cnt_T_u16

Uint16

0

65535

WhlPlsPerRev_CntPerRoadWhlRev_T_u08

Uint08

1

127

*RiWhlFrqVld_Cnt_T_logl

Boolean

FALSE

TRUE

*WhlRiFrq_Hz_T_f32

Float32

0.01

60

*RiFrqOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

*RiFrqChgOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

*RiWhlDiagFlg_Cnt_T_logl

Boolean

FALSE

TRUE

* RiWhlFrqVld_Cnt_T_logl,  * WhlRiFrq_Hz_T_f32, *RiFrqOutOfRng_Cnt_T_logl, *RiFrqChgOutOfRng_Cnt_T_logl and *RiWhlDiagFlg_Cnt_T_logl  are outputs of this function

### Design Rationale

Implementation of "Chk Curr and Prev RiWhlDstTiStamp" block

### Processing

Refer FDD

### Local Function #3

| Function Name | NTCDiag | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LeWhlDiagFlag_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | RiWhlDiagFlag_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | LeFrqOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | RiFrqOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | LeFrqChgOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | RiFrqChgOutOfRng_Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

NTCDiag

Type

Min

Max

Arguments Passed

LeWhlDiagFlag_Cnt_T_logl

Boolean

FALSE

TRUE

RiWhlDiagFlag_Cnt_T_logl

Boolean

FALSE

TRUE

LeFrqOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

RiFrqOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

LeFrqChgOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

RiFrqChgOutOfRng_Cnt_T_logl

Boolean

FALSE

TRUE

### Design Rationale

Implementation of "NTC Diag" block and immediately preceding logic

### Processing

Refer FDD

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

| 3 | EA4  Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | CF018A_GmRoadWhlInQlfr _Design | See Synergy subproject version |

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

EA4 Software Naming Conventions.doc

01.00.00

4

Software Design and Coding Standards.doc

2.1

5

CF018A_GmRoadWhlInQlfr_Design

See Synergy subproject version

Back to [Application Software](../).
