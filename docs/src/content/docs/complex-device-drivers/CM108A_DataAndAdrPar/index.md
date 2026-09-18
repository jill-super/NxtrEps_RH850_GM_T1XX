---
title: "Data And Address Parity (CM108A_DataAndAdrPar)"
description: "Data And Address Parity: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Data And Address Parity component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM108A_DataAndAdrPar_Design` | Design package |
| `CM108A_DataAndAdrPar_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM108A_DataAndAdrPar_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM108A_DataAndAdrPar_Impl` |  |
| C sources | `CDD_DataAndAdrPar.c`, `CDD_DataAndAdrParNonRte.c` |
| Public headers | `CDD_DataAndAdrPar.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataAndAdrPar.dcf`, `DataAndAdrPar_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM108A_DataAndAdrPar_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DataAndAdrPar.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `CM108A_DataAndAdrPar_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM108A_DataAndAdrPar_Impl/src/CDD_DataAndAdrPar.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM108A_DataAndAdrPar_Impl/src/CDD_DataAndAdrParNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM108A_DataAndAdrPar.doc`

- **Source path in repository:** `CM108A_DataAndAdrPar_Design/Design/CM108A_DataAndAdrPar.doc`
- **Format:** `.doc`
- **Size:** `870 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM108A_DataAndAdrPar_DDReport.txt`

- **Source path in repository:** `CM108A_DataAndAdrPar_Design/Reports/CM108A_DataAndAdrPar_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM108A_DataAndAdrPar_DataDict
15-Mar-2016 17:02:53
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
Missing Model 	Unable to find model for comparison to data dictionary.
(errors:  1)

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
(variables: 0, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 0, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 0, errors: 0)

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
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `DataAndAdrPar Integration Manual.doc`

- **Source path in repository:** `CM108A_DataAndAdrPar_Impl/doc/DataAndAdrPar Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `143 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DataAndAdrPar Module Design Document.docx`

- **Source path in repository:** `CM108A_DataAndAdrPar_Impl/doc/DataAndAdrPar Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `94 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

DataAndAdrPar

Mar 15, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Avinash  James | 1 | 03/1 5 /16 |

Description

Author

Version

Date

Initial Version

Avinash James

1

03/15/16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2DataAndAdrPar & High-Level Description6

3Design details of software module7

3.1Graphical representation of DataAndAdrPar7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init:DataAndAdrParInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Init:DataAndAdrParInit29

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1ChkForECMBit289

5.4.1.1Design Rationale9

5.4.1.2Processing9

5.4.2WrTestModeCtrReg9

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale10

5.5.1.2Processing10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## DataAndAdrPar & High-Level Description

See FDD

## Design details of software module

### Graphical representation of DataAndAdrPar

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| VCIFERRSETBFRTEST_CNT_U32 | 1 | Counts | ((uint32)1U<<0U) |

| ECMERRSETBFRTEST_CNT_U32 | 1 | Counts | ((uint32)1U<<1U) |

| READOPERECMERR_CNT_U32 | 1 | Counts | ((uint32)1U<<2U) |

| WROPERECMERR_CNT_U32 | 1 | Counts | ((uint32)1U<<3U) |

| WROPERADRPARERR_CNT_U32 | 1 | Counts | ((uint32)1U<<4U) |

| CLRERRSTSFLGFAIL_CNT_U32 | 1 | Counts | ((uint32)1U<<5U) |

| TESTMODCTRLREGWRFAIL_CNT_U32 | 1 | Counts | ((uint32)1U<<6U) |

| TOUT_MICROSEC_U32 | 1 | MicroSec | 2U |

Constant Name

Resolution

Units

Value

VCIFERRSETBFRTEST_CNT_U32

1

Counts

((uint32)1U<<0U)

ECMERRSETBFRTEST_CNT_U32

1

Counts

((uint32)1U<<1U)

READOPERECMERR_CNT_U32

1

Counts

((uint32)1U<<2U)

WROPERECMERR_CNT_U32

1

Counts

((uint32)1U<<3U)

WROPERADRPARERR_CNT_U32

1

Counts

((uint32)1U<<4U)

CLRERRSTSFLGFAIL_CNT_U32

1

Counts

((uint32)1U<<5U)

TESTMODCTRLREGWRFAIL_CNT_U32

1

Counts

((uint32)1U<<6U)

TOUT_MICROSEC_U32

1

MicroSec

2U

## Software Component Implementation

### Sub-Module Functions

### Init:DataAndAdrParInit1

### Design Rationale

Non-RTE Init function to verify the Data Parity Data Transfer Path micro diagnostic. Refer FDD for more details

### Module Outputs

None

### Init:DataAndAdrParInit2

### Design Rationale

RTE empty Init function

### Module Outputs

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### ChkForEcmBit28

| Function Name | ChkForEcmBit28 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

| Return Value | RetVal_Cnt_T_logl | Boolean | 0 | 1 |

Function Name

ChkForEcmBit28

Type

Min

Max

Arguments Passed

None

Return Value

RetVal_Cnt_T_logl

Boolean

0

1

### Design Rationale

Static function to check whether ECM bit was set or not within a time out interval of max 2uSec

### Processing

To be called from DataAndAdrParInit1 function

### WrTestModeCtrReg

| Function Name | WrTestMod CtrlReg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Val | Uint32 | 0 | 0xFFFFFFFF |

|  | ErrFlg_Cnt_T_u32 | Uint32 | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |

Function Name

WrTestModCtrlReg

Type

Min

Max

Arguments Passed

Val

Uint32

0

0xFFFFFFFF

ErrFlg_Cnt_T_u32

Uint32

0

0xFFFFFFFF

Return Value

None

### Design Rationale

Static function to write to the Test Mode Control register and verify the write was successful

### Processing

To be called from DataAndAdrParInit1 function

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

(Exact name used)

Type

Min

Max

Arguments Passed

None

<Refer MDD guidelines[1]>

<Refer MDD guidelines[1]>

<Refer MDD guidelines[1]>

Return Value

### Design Rationale

### Processing

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

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

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

1.0

4

Software Design and Coding Standards.doc

2.0

Back to [Complex Device Drivers](../).
