---
title: "Torque Estimation (SF006A_TEstimn)"
description: "Torque Estimation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Torque Estimation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF006A_TEstimn_Design` | Design package |
| `SF006A_TEstimn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF006A_TEstimn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF006A_TEstimn_Impl` |  |
| C sources | `TEstimn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `TEstimn.dcf`, `TEstimn_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF006A_TEstimn_Impl.gpj`, `TEstimn.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF006A_TEstimn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF006A_TEstimn_Impl/src/TEstimn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF006A_TEstimn_DDReport.txt`

- **Source path in repository:** `SF006A_TEstimn_Design/Reports/SF006A_TEstimn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF006A_TEstimn_DataDict
24-Sep-2015 16:16:52
Tool Release:  2.20.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF99A
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
SrvRunnable:	<ShoName><TriggerName>
--------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 8, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 4, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 35, errors: 0)

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
(variables: 14, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 12, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `TEstimn_IntegrationManual.doc`

- **Source path in repository:** `SF006A_TEstimn_Impl/doc/TEstimn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TEstimn_MDD.docx`

- **Source path in repository:** `SF006A_TEstimn_Impl/doc/TEstimn_MDD.docx`
- **Format:** `.docx`
- **Size:** `121 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

TEstimn

Sep 17, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1 | 17 - Sep -2015 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

17-Sep-2015

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2TEstimn High-Level Description5

3Design details of software module6

3.1Graphical representation of TEstimn6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: TEstimnInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: TEstimnPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.5GLOBAL Function/Macro Definitions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

### Scope

## TEstimn High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of TEstimn

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

#### Local Constants

## Software Component Implementation

### Sub-Module Functions

### Init: TEstimnInit1

### Design Rationale

Refer FDD for the functionality.

### Module Outputs

Refer FDD

### Per: TEstimnPer1

### Design Rationale

In ‘AssistMechanismLeadLagFilterRe-Initialization’ block, blocks ‘AssistMechanismInitEnable’ and ‘AssistMechanismInitDisable’ have similar logic except for some calculations related to inputs.  So the differences are implemented in ‘if-else’ statement and common logic is implemented after ‘if-else’ statements in the SW.

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

None

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

Due to the lead/lag filter implementation in this module, absolute ranges are difficult to determine without pre-defined knowledge on the combination of coefficient values (A1, B0, B1).  For unit test purposes, below four sets of lead/lag filter coefficient calibrations (TEstimnXXLLFilCoeffA1, TEstimnXXLLFilCoeffB0 and TEstimnXXLLFilCoeffB1) should be tested using the combinations of coefficient values in the table below, as well as the default values of the filter coefficient calibrations as given in the data dictionary.  The ranges given throughout this module were taken as the worst case results of the entire given filter coefficient sets.

| Fz | 0.0045 | 0.0045 | 0.00003 | 0.00003 |

| --- | --- | --- | --- | --- |

| Fp | 0.0045 | 0.00003 | 0.0045 | 0.00003 |

|  |  |  |  |  |

| B0 | 1 | 0.0066760330 | 149.78955 | 1 |

| B1 | -0.99717656 | -0.0066571836 | -149.78673 | -0.99998115 |

| A1 | 0.99717656 | 0.99998115 | 0.99717656 | 0.99998115 |

Fz

0.0045

0.0045

0.00003

0.00003

Fp

0.0045

0.00003

0.0045

0.00003

B0

1

0.0066760330

149.78955

1

B1

-0.99717656

-0.0066571836

-149.78673

-0.99998115

A1

0.99717656

0.99998115

0.99717656

0.99998115

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

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  SF006A _   TEstimn _Design | See Synergy sub project version |

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

EA4 01.00.00

4

Software Design and Coding Standards.doc

2.1

5

FDD : SF006A_ TEstimn_Design

See Synergy sub project version

Back to [Application Software](../).
