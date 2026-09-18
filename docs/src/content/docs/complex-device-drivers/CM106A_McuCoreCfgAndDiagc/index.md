---
title: "Microcontroller Unit Core Configuration And Diagnostics (CM106A_McuCoreCfgAndDiagc)"
description: "Microcontroller Unit Core Configuration And Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Microcontroller Unit Core Configuration And Diagnostics component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM106A_McuCoreCfgAndDiagc_Design` | Design package |
| `CM106A_McuCoreCfgAndDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM106A_McuCoreCfgAndDiagc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM106A_McuCoreCfgAndDiagc_Impl` |  |
| C sources | `CDD_McuCoreCfgAndDiagc.c`, `CDD_McuCoreCfgAndDiagcNonRte.c` |
| Public headers | `CDD_McuCoreCfgAndDiagc.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `McuCoreCfgAndDiagc.dcf`, `McuCoreCfgAndDiagc_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM106A_McuCoreCfgAndDiagc_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreateQACProject.bat`, `McuCoreCfgAndDiagc.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `CM106A_McuCoreCfgAndDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM106A_McuCoreCfgAndDiagc_Impl/src/CDD_McuCoreCfgAndDiagc.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM106A_McuCoreCfgAndDiagc_Impl/src/CDD_McuCoreCfgAndDiagcNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM106A_McuCoreCfgAndDiagc.doc`

- **Source path in repository:** `CM106A_McuCoreCfgAndDiagc_Design/Design/CM106A_McuCoreCfgAndDiagc.doc`
- **Format:** `.doc`
- **Size:** `1301 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM106A_McuCoreCfgAndDiagc_DDReport.txt`

- **Source path in repository:** `CM106A_McuCoreCfgAndDiagc_Design/Reports/CM106A_McuCoreCfgAndDiagc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM106A_McuCoreCfgAndDiagc_DataDict
11-Feb-2016 15:18:19
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
(variables: 3, errors: 0)

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
(variables: 1, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `McuCoreCfgAndDiagc Integration Manual.doc`

- **Source path in repository:** `CM106A_McuCoreCfgAndDiagc_Impl/doc/McuCoreCfgAndDiagc Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `McuCoreCfgAndDiagc Module Design Document.docx`

- **Source path in repository:** `CM106A_McuCoreCfgAndDiagc_Impl/doc/McuCoreCfgAndDiagc Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `96 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

McuCoreCfgAndDiagc

Oct 6, 2015

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

| Initial Version | Lucas  Wendling | 1 | 10/06/15 |

Description

Author

Version

Date

Initial Version

Lucas Wendling

1

10/06/15

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2<Component Name> & High-Level Description6

3Design details of software module7

3.1Graphical representation of <Component Name>7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: <Component Name>_Init<n>9

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: <Component Name>_Per<n>9

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1<Server Runable Name>9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………10

5.3Interrupt Functions10

5.3.1Interrupt Function Name10

5.3.1.1Design Rationale10

5.3.1.2(Processing of the ISR function)…..10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale11

5.5.1.2processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## McuCoreCfgAndDiagc & High-Level Description

See FDD

## Design details of software module

### Graphical representation of McuCoreCfgAndDiagc

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

| None |  |  |  |

Constant Name

Resolution

Units

Value

None

## Software Component Implementation

### Sub-Module Functions

### Init: McuCoreCfgAndDiagcInit1

### Design Rationale

Temporary variables were created to read register values into in order to avoid MISRA violations that appear when volatile values are used in conditional statements.

### Module Outputs

Refer to FDD

### Init: McuCoreCfgAndDiagcInit2

### Design Rationale

Temporary variables were created to read register values into in order to avoid MISRA violations that appear when volatile values are used in conditional statements.

### Module Outputs

Refer to FDD

### Init: McuCoreCfgAndDiagcInit3

### Design Rationale

Empty function for purposes of memory mapping

### Module Outputs

None

### Per: McuCoreCfgAndDiagc_Per<n>

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

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
