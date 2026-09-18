---
title: "Compliance Error (SF041A_CmplncErr)"
description: "Compliance Error: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Compliance Error component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF041A_CmplncErr_Design` | Design package |
| `SF041A_CmplncErr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF041A_CmplncErr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF041A_CmplncErr_Impl` |  |
| C sources | `CmplncErr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CmplncErr.dcf`, `CmplncErr_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CmplncErr.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF041A_CmplncErr_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF041A_CmplncErr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF041A_CmplncErr_Impl/src/CmplncErr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF041A_CmplncErr_DDReport.txt`

- **Source path in repository:** `SF041A_CmplncErr_Design/Reports/SF041A_CmplncErr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF041A_CmplncErr_DataDict
21-Jan-2016 11:14:20
Tool Release:  2.29.0



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
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 2, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
CmplncErrMotToPinion        	Name does not match required pattern.
CmplncErrPinionToHw         	Name does not match required pattern.
(variables: 2, errors: 2)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
CmplncErrHwAgNonLinCmplncDepTblY 	.DocUnits:	Not on approved list.
CmplncErrMotAgNonLinCmplncDepTblY	.DocUnits:	Not on approved list.
(variables: 4, errors: 2)

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

```
*... truncated (35 more lines in the source file). ...*

### `CmplncErr_IntegrationManual.doc`

- **Source path in repository:** `SF041A_CmplncErr_Impl/doc/CmplncErr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CmplncErr_MDD.docx`

- **Source path in repository:** `SF041A_CmplncErr_Impl/doc/CmplncErr_MDD.docx`
- **Format:** `.docx`
- **Size:** `129 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

CmplncErr

Jan 11, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Kannappa Chidambaram,

Tata Elxsi, INDIA

Change History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Kannappa  Chidambaram P R | 1.0 | 01/11/2016 |

Sl. No.

Description

Author

Version

Date

1

Initial version

Kannappa Chidambaram P R

1.0

01/11/2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2CmplncErr & High-Level Description5

3Design details of software module6

3.1Graphical representation of CmplncErr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: CmplncErrInit18

5.1.2Per: CmplncErrPer18

5.2Server Runnable8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.5GLOBAL Function/Macro Definitions8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

## CmplncErr & High-Level Description

Please refer FDD

## Design details of software module

### Graphical representation of CmplncErr

### Data Flow Diagram

Please refer FDD

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer .m file |  |  |  |

Constant Name

Resolution

Units

Value

Please refer .m file

## Software Component Implementation

### Sub-Module Functions

#### Init: CmplncErrInit1

#### Design Rationale

None

#### Module Outputs

None

#### Per: CmplncErrPer1

#### Design Rationale

None

#### Store Module Inputs to Local copies

None

#### (Processing of function)………

Please refer FDD

#### Store Local copy of outputs into Module Outputs

Please refer FDD

### Server Runnable

None

### Interrupt Functions

None

### Module Internal (Local) Functions

None

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

| 3 | Software Naming Conventions.doc | Process 4.02.00 |

| 4 | Software Design and Coding Standards.doc | Process 4.02.00 |

| 5 | FDD:  SF041A_  CmplncErr _Design | See Synergy sub project version |

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

Process 4.02.00

4

Software Design and Coding Standards.doc

Process 4.02.00

5

FDD: SF041A_ CmplncErr_Design

See Synergy sub project version

Back to [Application Software](../).
