---
title: "Nexteer Development Error Tracer (AR998A_NxtrDet)"
description: "Nexteer Development Error Tracer: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Nexteer Development Error Tracer component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `AR998A_NxtrDet_Design` | Design package |
| `AR998A_NxtrDet_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR998A_NxtrDet_Design` |  |
| Documentation folders | `Doc/`, `Design/` |
| `AR998A_NxtrDet_Impl` |  |
| Public headers | `NxtrDet.h` |
| Tooling and integration scripts | `AR998A_NxtrDet_Impl.gpj`, `CreateGHSProject.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AR998A NxtrDet Functional Design Document.doc`

- **Source path in repository:** `AR998A_NxtrDet_Design/Design/AR998A NxtrDet Functional Design Document.doc`
- **Format:** `.doc`
- **Size:** `166 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AR998A_NxtrDet_DDReport.txt`

- **Source path in repository:** `AR998A_NxtrDet_Impl/doc/AR998A_NxtrDet_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of AR998A_NxtrDet_DataDict
11-Mar-2016 10:00:49
Tool Release:  2.34.0



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
(variables: 0, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

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

### `NxtrDet Integration Manual.doc`

- **Source path in repository:** `AR998A_NxtrDet_Impl/doc/NxtrDet Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `NxtrDet Module Design Document.docx`

- **Source path in repository:** `AR998A_NxtrDet_Impl/doc/NxtrDet Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `90 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

NxtrDet

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

1Introduction4

1.1Purpose4

1.2Scope4

2NxtrDet High-Level Description5

3Design details of software module6

3.1Graphical representation of NxtrDet6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: NxtrDet8

5.1.2Per: NxtrDet8

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.4.1Local Function #18

5.4.1.1Design Rationale8

5.4.1.2Processing8

5.5GLOBAL Function/Macro Definitions8

5.5.1GLOBAL Function #18

5.5.1.1Design Rationale8

5.5.1.2Processing8

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## NxtrDet High-Level Description

See FDD

## Design details of software module

### Graphical representation of NxtrDet

None

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Constants containing the Nexteer ModuleIDs defined for Det functionality are defined in the .m file included in the doc folder of this component.  This is to allow new SWCs adding new Det errors to not drive changes to the design project, only to the implementation project.

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

### Init: NxtrDet

None

### Per: NxtrDet

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

Back to [Basic Software Services](../).
