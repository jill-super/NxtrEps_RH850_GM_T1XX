---
title: "Random Access Memory Memory (CM103A_RamMem)"
description: "Random Access Memory Memory: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Random Access Memory Memory component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM103A_RamMem_Design` | Design package |
| `CM103A_RamMem_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM103A_RamMem_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM103A_RamMem_Impl` |  |
| C sources | `CDD_RamMem.c`, `CDD_RamMemNonRte.c` |
| Public headers | `CDD_RamMem.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `RamMem.dcf`, `RamMem_attr_def.xml` |
| Tooling and integration scripts | `CM103A_RamMem_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreateQACProject.bat`, `RamMem.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM103A_RamMem_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM103A_RamMem_Impl/src/CDD_RamMem.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM103A_RamMem_Impl/src/CDD_RamMemNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM103A_RamMem.doc`

- **Source path in repository:** `CM103A_RamMem_Design/Design/CM103A_RamMem.doc`
- **Format:** `.doc`
- **Size:** `1301 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM103A_RamMem_DDReport.txt`

- **Source path in repository:** `CM103A_RamMem_Design/Reports/CM103A_RamMem_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM103A_RamMem_DataDict
01-Aug-2016 11:20:07
Tool Release:  2.41.0



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
RamMemLclRamSngBitEcc       	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
(variables: 3, errors: 1)

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
(variables: 0, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
LclRamEccSngBitCntrOutp     	Cannot match name to list of known Nexteer signals.
(variables: 1, errors: 1)

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
(variables: 12, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 4, errors: 0)

--------------------------------------------------------------------------------------------
```
*... truncated (34 more lines in the source file). ...*

### `RamMem_Integration Manual.doc`

- **Source path in repository:** `CM103A_RamMem_Impl/doc/RamMem_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `RamMem_Module Design Document.docx`

- **Source path in repository:** `CM103A_RamMem_Impl/doc/RamMem_Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `101 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

RamMem

Aug 23, 2016

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

| Initial Version | Selva Sengottaiyan | 1 | 04 /06/1 6 |

| Created local functions for reducing cyclometric complexity | Selva Sengottaiyan | 2 | 06/26/2016 |

| Changed SPI ECC handling from  interrupt to polling | Avinash James | 3 | 08/23/2016 |

Description

Author

Version

Date

Initial Version

Selva Sengottaiyan

1

04/06/16

Created local functions for reducing cyclometric complexity

Selva Sengottaiyan

2

06/26/2016

Changed SPI ECC handling from interrupt to polling

Avinash James

3

08/23/2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2RamMem & High-Level Description6

3Design details of software module7

3.1Graphical representation of RamMem7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: RamMemInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: RamMemPer19

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.2Server Runables9

5.2.1SpiDblBitEcc9

5.2.1.1Design Rationale9

5.2.1.2Processing9

5.2.2RamMemLclRamSngBitEcc9

5.2.2.1Design Rationale9

5.2.2.2Processing9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #210

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.4.3Local Function #310

5.4.3.1Design Rationale10

5.4.3.2Processing10

5.4.4Local Function #411

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Local Function #511

5.4.5.1Design Rationale11

5.4.5.2Processing11

5.5GLOBAL Function/Macro Definitions11

5.5.1GLOBAL Function #111

5.5.1.1Design Rationale11

5.5.1.2Processing11

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## RamMem & High-Level Description

See FDD

## Design details of software module

### Graphical representation of RamMem

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

| LCLRAMBASADR_CNT_U32 | 1 | Cnt | 0xFEB80000U |

| VLDADRTESTBITMASK_CNT_U32 | 1 | Cnt | 0xFFFE0000U |

| VLDADRTESTRES_CNT_U32 | 1 | Cnt | 0x00060000U |

| WORDLINEADRMASK_CNT_U32 | 1 | Cnt | 0xFFFFFF1FU |

| BNK0ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000001U |

| BNK1ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000002U |

| BNK2ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000004U |

| BNK3ERRCLRMASK_CNT_U32 | 1 | Cnt | 0x00000008U |

| BNK0SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00000001U |

| BNK1SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00000100U |

| BNK2SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x00010000U |

| BNK3SNGBITERRMASK_CNT_U32 | 1 | Cnt | 0x01000000U |

|  |  |  |  |

Constant Name

Resolution

Units

Value

LCLRAMBASADR_CNT_U32

1

Cnt

0xFEB80000U

VLDADRTESTBITMASK_CNT_U32

1

Cnt

0xFFFE0000U

VLDADRTESTRES_CNT_U32

1

Cnt

0x00060000U

WORDLINEADRMASK_CNT_U32

1

Cnt

0xFFFFFF1FU

BNK0ERRCLRMASK_CNT_U32

1

Cnt

0x00000001U

BNK1ERRCLRMASK_CNT_U32

1

Cnt

0x00000002U

BNK2ERRCLRMASK_CNT_U32

1

Cnt

0x00000004U

BNK3ERRCLRMASK_CNT_U32

1

Cnt

0x00000008U

BNK0SNGBITERRMASK_CNT_U32

1

Cnt

0x00000001U

BNK1SNGBITERRMASK_CNT_U32

1

Cnt

0x00000100U

BNK2SNGBITERRMASK_CNT_U32

1

Cnt

0x00010000U

BNK3SNGBITERRMASK_CNT_U32

1

Cnt

0x01000000U

## Software Component Implementation

### Sub-Module Functions

### Init: RamMemInit1

### Design Rationale

### Module Outputs

Refer to FDD

### Per: RamMemPer1

### Design Rationale

### Module Outputs

Refer to FDD

### Server Runables

### RamMemLclRamSngBitEcc

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

### Interrupt Functions

### Module Internal (Local) Functions

### Local Function #1

| Function Name | RamFailrModClassnChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

RamFailrModClassnChk

Type

Min

Max

Arguments Passed

None

Return Value

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

### Local Function #2

| Function Name | RamMemLclRamFailrChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | LclRamFailrAdr_Cnt_T_u32 | uint32 | 0 | 4294967295 |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

RamMemLclRamFailrChk

Type

Min

Max

Arguments Passed

LclRamFailrAdr_Cnt_T_u32

uint32

0

4294967295

Return Value

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

### Local Function #3

| Function Name | SpiEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

SpiEccErr

Type

Min

Max

Arguments Passed

None

Return Value

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

### Local Function #4

| Function Name | FrEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

FrEccErr

Type

Min

Max

Arguments Passed

None

Return Value

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

### Local Function #5

| Function Name | CanEccErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

CanEccErr

Type

Min

Max

Arguments Passed

None

Return Value

### Design Rationale

Refer the FDD

### Processing

Refer the FDD

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

Local RAM Single bit PIM for address store will be overwritten for each banks which can be avoided by defining Pims for each memory block. Will be reviewed POST IVER build

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

| 2 | MDD Guideline | EA4 01.00 .0 1 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 01.00.01

3

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.1

Back to [Complex Device Drivers](../).
