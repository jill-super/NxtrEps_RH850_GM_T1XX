---
title: "Return (SF002A_Rtn)"
description: "Return: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Return component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF002A_Rtn_Design` | Design package |
| `SF002A_Rtn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF002A_Rtn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF002A_Rtn_Impl` |  |
| C sources | `Rtn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `Rtn.dcf`, `Rtn_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `Rtn.dpa`, `SF002A_Rtn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF002A_Rtn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF002A_Rtn_Impl/src/Rtn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF002A_Rtn_DDReport.txt`

- **Source path in repository:** `SF002A_Rtn_Design/Reports/SF002A_Rtn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF002A_Rtn_DataDict
18-Nov-2016 16:21:47
Tool Release:  2.50.0



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
RtnCmdDi                    	Name does not match required pattern.
RtnCmdDiagcDi               	Name does not match required pattern.
RtnCmdSca                   	Name does not match required pattern.
RtnCmdScaServo              	Name does not match required pattern.
(variables: 12, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
RtnCmd                      	Name does not match required pattern.
(variables: 1, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 14, errors: 0)

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
(variables: 7, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 2, errors: 0)
```
*... truncated (37 more lines in the source file). ...*

### `Rtn_Integration Manual.doc`

- **Source path in repository:** `SF002A_Rtn_Impl/doc/Rtn_Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `152 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Rtn_Module Design Document.docx`

- **Source path in repository:** `SF002A_Rtn_Impl/doc/Rtn_Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `136 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Return

Nov 29, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI

CHENNAI, INDIA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | SB | 1 | 30-Jun-2015 |

| Updated per design rev. 2.0.0 | TATA | 2.0 | 29-Nov-2016 |

Description

Author

Version

Date

Initial Version

SB

1

30-Jun-2015

Updated per design rev. 2.0.0

TATA

2.0

29-Nov-2016

Table of Contents

1Introduction3

1.1Purpose3

2Rtn High-Level Description4

3Design details of software module5

3.1Graphical representation of Rtn5

3.2Data Flow Diagram5

3.2.1Component level DFD5

3.2.2Function level DFD5

4Constant Data Dictionary6

4.1Program (fixed) Constants6

4.1.1Embedded Constants6

5Software Component Implementation7

5.1.1Sub-Module Functions7

5.1.2Interrupt Service Routines7

5.1.3Server Runnable Functions7

5.1.4Module Internal (Local) Functions7

5.1.5Transition Functions7

6Known Limitations with Design8

7UNIT TEST CONSIDERATION9

Appendix AAbbreviations and Acronyms10

Appendix BGlossary11

Appendix CReferences12

## Introduction

### Purpose

MDD for Return

## Rtn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of Rtn

### Data Flow Diagram

#### Component level DFD

Refer to FDD

#### Function level DFD

Refer to FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

None

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module RtnInit1

#### Periodic sub-module RtnPer1

Design Rationale - Fault Injection client call is conditional compiled based on “FLTINJENA” build constant.

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

None

#### Transition Functions

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

| 3 | Software Naming Conventions.doc | 2 .0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD – SF002A_Rtn_Design | See Synergy Sub project ver s ion |

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

FDD – SF002A_Rtn_Design

See Synergy Sub project version

Back to [Application Software](../).
