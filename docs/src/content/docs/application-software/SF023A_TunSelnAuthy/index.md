---
title: "Tuning Selection Authority (SF023A_TunSelnAuthy)"
description: "Tuning Selection Authority: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Tuning Selection Authority component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF023A_TunSelnAuthy_Design` | Design package |
| `SF023A_TunSelnAuthy_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF023A_TunSelnAuthy_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF023A_TunSelnAuthy_Impl` |  |
| C sources | `TunSelnAuthy.c` |
| Public headers | `TunSelnAuthy.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `TunSelnAuthy.dcf`, `TunSelnAuthy_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF023A_TunSelnAuthy_Impl.gpj`, `TunSelnAuthy.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF023A_TunSelnAuthy_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF023A_TunSelnAuthy_Impl/src/TunSelnAuthy.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF023A_TunSelnAuthy_DDReport.txt`

- **Source path in repository:** `SF023A_TunSelnAuthy_Design/Reports/SF023A_TunSelnAuthy_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF023A_TunSelnAuthy_DataDict
14-Jun-2016 15:57:03
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
(errors:  0)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 1, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 2, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 4, errors: 0)

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
(variables: 4, errors: 0)

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
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (33 more lines in the source file). ...*

### `TunSelnAuthy_IntegrationManual.doc`

- **Source path in repository:** `SF023A_TunSelnAuthy_Impl/doc/TunSelnAuthy_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TunSelnAuthy_MDD.docx`

- **Source path in repository:** `SF023A_TunSelnAuthy_Impl/doc/TunSelnAuthy_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

TunSelnAuthy

June 17, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Date |

| --- | --- | --- |

| Initial Version | N. Saxton | 09-Oct-2015 |

| Updated as per FDD v1.1.0 | Krishna Anne | 17-Jun-2016 |

Description

Author

Date

Initial Version

N. Saxton

09-Oct-2015

Updated as per FDD v1.1.0

Krishna Anne

17-Jun-2016

Table of Contents1TunSelnAuthy High-Level Description4

2Design details of software module5

2.1Graphical representation of TunSelnAuthy5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: TunSelnAuthyInit17

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.2Server Runables7

4.2.1RtCalChgReq7

4.2.1.1Design Rationale7

4.2.1.2(Processing of function)………7

4.2.2XcpCalChgReq7

4.2.2.1Design Rationale7

4.2.2.2(Processing of function)………7

4.3Interrupt Functions7

4.3.1Interrupt Function Name7

4.4Module Internal (Local) Functions7

4.5GLOBAL Function/Macro Definitions7

5Known Limitations with Design9

6UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## TunSelnAuthy High-Level Description

Refer FDD

## Design details of software module

Refer FDD

### Graphical representation of TunSelnAuthy

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

| Refer .m file for constants |  |  |  |

Constant Name

Resolution

Units

Value

Refer .m file for constants

## Software Component Implementation

### Sub-Module Functions

### Init: TunSelnAuthyInit1

### Design Rationale

Refer FDD

### Module Outputs

None

### Server Runables

### RtCalChgReq

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### XcpCalChgReq

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Interrupt Function Name

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD – SF023A_TunSelnAuthy_Design | See Synergy subproject version |

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

2.1

5

FDD – SF023A_TunSelnAuthy_Design

See Synergy subproject version

Back to [Application Software](../).
