---
title: "Stability Compensation (SF029A_StabyCmp)"
description: "Stability Compensation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Stability Compensation component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF029A_StabyCmp_Design` | Design package |
| `SF029A_StabyCmp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF029A_StabyCmp_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF029A_StabyCmp_Impl` |  |
| C sources | `StabyCmp.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `StabyCmp.dcf`, `StabyCmp_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF029A_StabyCmp_Impl.gpj`, `StabyCmp.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF029A_StabyCmp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF029A_StabyCmp_Impl/src/StabyCmp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF029A_StabyCmp_DDReport.txt`

- **Source path in repository:** `SF029A_StabyCmp_Design/Reports/SF029A_StabyCmp_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF029A_StabyCmp_DataDict
14-Sep-2016 16:03:38
Tool Release:  2.46.0



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
(variables: 5, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 1, errors: 0)

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
(variables: 11, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 9, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `StabyCmp_IntegrationManual.doc`

- **Source path in repository:** `SF029A_StabyCmp_Impl/doc/StabyCmp_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `StabyCmp_MDD.docx`

- **Source path in repository:** `SF029A_StabyCmp_Impl/doc/StabyCmp_MDD.docx`
- **Format:** `.docx`
- **Size:** `132 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

StabyCmp

Jan 27, 2017

Prepared By:

Shruthi Raghavan,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1.0 | 2 1-July-2015 |

| Updated for FDD version 1.1.0 | Sankardu   Varadapureddi | 2.0 | 11-Mar-2016 |

| Updated to FDD version 1.3.0 | Shruthi Raghavan | 3.0 | 27-Jan-2017 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1.0

21-July-2015

Updated for FDD version 1.1.0

Sankardu Varadapureddi

2.0

11-Mar-2016

Updated to FDD version 1.3.0

Shruthi Raghavan

3.0

27-Jan-2017

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2StabyCmp High-Level Description5

3Design details of software module6

3.1Graphical representation of ‘StabyCmp’6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1.1Sub-Module Functions8

5.1.2Interrupt Service Routines8

5.1.3Server Runnable Functions8

5.1.4Module Internal (Local) Functions8

5.2Local Function #18

5.3Description8

5.4Local Function #29

5.5Description9

5.5.1Transition Functions9

6Known Limitations with Design10

7UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## Introduction

### Purpose

Module design document for Stability Compensation.

## StabyCmp High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of ‘StabyCmp’

### Data Flow Diagram

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

Local Constants

None

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {StabyCmpInit1}

#### StabyCmpInit1

Design Rational:

FDD details are not complete for notch filter initialization. Upon discussion with FDD owner, implemented in line with EA3 implementation.

#### Periodic sub-module {StabyCmpPer1}

Refer FDD for details

Design Rational:

In design version 1.3.0, .m file has some additional PIMs for notch filters, which are not required in the notch filter implementation.

Notch filter implementation in SW based on design 1.0.0 .m file PIMs is not changed.

New FDD model was requested but this wasn’t done on time and due to time crunch the difference between implementation and the model still exists.

#### Interrupt Service Routines

None

#### Server Runnable Functions

None

#### Module Internal (Local) Functions

#### Local Function #1

| Function Name | FilNotchInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | None |  |  |  |

Function Name

FilNotchInit

Type

Min

Max

Arguments Passed

Inp

float32

See unit test consideration

FilNotchStRecPtr

FilNotchStRec1

FilNotchGainRecPtr

FilNotchGainRec1

Return Value

None

#### Description

Notch filter initialization function implemented based on EA3 design.

#### Local Function #2

| Function Name | FilNotchFullUpdOutp_f32 | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Inp | float32 | See unit test consideration |  |

|  | FilNotchStRecPtr | FilNotchStRec1 |  |  |

|  | FilNotchGainRecPtr | FilNotchGainRec1 |  |  |

| Return Value | FilOut | float32 |  |  |

Function Name

FilNotchFullUpdOutp_f32

Type

Min

Max

Arguments Passed

Inp

float32

See unit test consideration

FilNotchStRecPtr

FilNotchStRec1

FilNotchGainRecPtr

FilNotchGainRec1

Return Value

FilOut

float32

#### Description

Notch filter output calculation. Implemented based on ‘Compensator1’ block functionality. Compensator2, Compensator3 and Compensator4 also have the same functionality.

#### Transition Functions

None

## Known Limitations with Design

Design has 8 PIMs to represent notch filters and a model block for notch filter has not been designed. This hasn’t been done yet in this revision due to the need to baseline on time for builds. No anomaly has been written but the Systems group was notified.

## UNIT TEST CONSIDERATION

Since the notch filter implementation used in this module is dynamic in nature, absolute ranges are difficult to determine without pre-defined knowledge on the combination of coefficient values (A1, A2, B0, B1, B2).  Because of this, the systems group ran simulations on 10 different combinations of coefficients (2 with defined default calibrations, 8 considered extreme cases of notch filters) and logged the ranges of the filter state variables and outputs during a frequency sweep.  The ranges given throughout this module were taken as the worst case results of all of the given test cases.

To provide useful cases for unit testing, the boundary checks tested during unit testing should be altered to test the state variable minimum and maximum for each of the 10 test cases with the given coefficients set to the values given in that test case.  In the case where the default values of the coefficients are used in a vector, the unit tester should not test the corresponding state variables with values over the range defined for that set of coefficients.  See attached simulation results.

(Note: this section is copied from EA3 Stability Compensation documentation)

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

| 5 | FDD  -  SF029A_StabyCmp_Design | See Synergy sub project version |

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

FDD  - SF029A_StabyCmp_Design

See Synergy sub project version

Back to [Application Software](../).
