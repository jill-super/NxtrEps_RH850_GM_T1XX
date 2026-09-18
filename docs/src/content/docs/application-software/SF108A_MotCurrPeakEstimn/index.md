---
title: "Motor Current Peak Estimation (SF108A_MotCurrPeakEstimn)"
description: "Motor Current Peak Estimation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Current Peak Estimation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF108A_MotCurrPeakEstimn_Design` | Design package |
| `SF108A_MotCurrPeakEstimn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF108A_MotCurrPeakEstimn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF108A_MotCurrPeakEstimn_Impl` |  |
| C sources | `MotCurrPeakEstimn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotCurrPeakEstimn.dcf`, `MotCurrPeakEstimn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotCurrPeakEstimn.dpa`, `RteGen.bat`, `SF108A_MotCurrPeakEstimn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF108A_MotCurrPeakEstimn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF108A_MotCurrPeakEstimn_Impl/src/MotCurrPeakEstimn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF108A_MotCurrPeakEstimn_DDReport.txt`

- **Source path in repository:** `SF108A_MotCurrPeakEstimn_Design/Reports/SF108A_MotCurrPeakEstimn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF108A_MotCurrPeakEstimn_DataDict
23-Nov-2015 16:46:08
Tool Release:  2.26.0



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
(variables: 3, errors: 0)

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
(variables: 5, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 1, errors: 0)

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
(variables: 2, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 3, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `MotCurrPeakEstimn_IntegrationManual.doc`

- **Source path in repository:** `SF108A_MotCurrPeakEstimn_Impl/doc/MotCurrPeakEstimn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotCurrPeakEstimn_MDD.docx`

- **Source path in repository:** `SF108A_MotCurrPeakEstimn_Impl/doc/MotCurrPeakEstimn_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotCurrPeakEstimn

April 25, 2016

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

| Initial Version | SB | 1.0 | 0 5 -Aug-2015 |

| Updated graphical representation due to changes from FDD v1.2.0 | NS | 2.0 | 25-Apr-2016 |

Description

Author

Version

Date

Initial Version

SB

1.0

05-Aug-2015

Updated graphical representation due to changes from FDD v1.2.0

NS

2.0

25-Apr-2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2MotCurrPeakEstimn& High-Level Description5

3Design details of software module6

3.1Graphical representation of MotCurrPeakEstimn6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: MotCurrPeakEstimnInit18

5.1.2Per: MotCurrPeakEstimnPer18

5.1.3Per: MotCurrPeakEstimnPer28

5.2Server Runables8

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

### Scope

## MotCurrPeakEstimn & High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of MotCurrPeakEstimn

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

| Refer .m File |  |  |  |

Constant Name

Resolution

Units

Value

Refer .m File

## Software Component Implementation

Refer FDD

### Sub-Module Functions

### Init: MotCurrPeakEstimnInit1

Refer FDD

### Per: MotCurrPeakEstimnPer1

Refer FDD

### Per: MotCurrPeakEstimnPer2

Refer FDD

### Server Runables

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

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | Process 04.02.00 |

| 3 | Software Naming Conventions.doc | Process 04.02.00 |

| 4 | Software Design and Coding Standards.doc | Process 04.02.00 |

| 5 | FDD – SF10 8A_ MotCurrPeakEstimn _Design | See Synergy  SubProject  version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

Process 04.02.00

3

Software Naming Conventions.doc

Process 04.02.00

4

Software Design and Coding Standards.doc

Process 04.02.00

5

FDD – SF108A_MotCurrPeakEstimn_Design

See Synergy SubProject version

Back to [Application Software](../).
