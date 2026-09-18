---
title: "Limiter Coding (SF038A_LimrCdng)"
description: "Limiter Coding: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Limiter Coding component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF038A_LimrCdng_Design` | Design package |
| `SF038A_LimrCdng_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF038A_LimrCdng_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF038A_LimrCdng_Impl` |  |
| C sources | `LimrCdng.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `LimrCdng.dcf`, `LimrCdng_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `LimrCdng.dpa`, `RteGen.bat`, `SF038A_LimrCdng_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF038A_LimrCdng_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF038A_LimrCdng_Impl/src/LimrCdng.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF038A_LimrCdng_DDReport.txt`

- **Source path in repository:** `SF038A_LimrCdng_Design/Reports/SF038A_LimrCdng_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF038A_LimrCdng_DataDict
14-Jul-2015 09:43:06
Tool Release:  2.15.0



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
Unable to find model for comparison to data dictionary.
(errors:  1)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 1, errors: 0)

--------------------------------------
SrvRunnable:	<ShoName><TriggerName>
--------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
FltInj_f32                  	    Inj_f          Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 1, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
EotAssiSca                  	Cannot match name to list of known Nexteer signals.
EotMotTqLim                 	Cannot match name to list of known Nexteer signals.
StallMotTqLim               	Cannot match name to list of known Nexteer signals.
VehSpdMotTqLim              	Cannot match name to list of known Nexteer signals.
(variables: 7, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
EotAssiScaCdnd              	Cannot match name to list of known Nexteer signals.
EotMotTqLimCdnd             	Cannot match name to list of known Nexteer signals.
StallMotTqLimCdnd           	Cannot match name to list of known Nexteer signals.
SysMotTqCmdScaCdnd          	Cannot match name to list of known Nexteer signals.
ThermMotTqLimCdnd           	Cannot match name to list of known Nexteer signals.
VehSpdMotTqLimCdnd          	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 6)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 6, errors: 0)

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
```
*... truncated (46 more lines in the source file). ...*

### `LimrCdng_IntegrationManual.doc`

- **Source path in repository:** `SF038A_LimrCdng_Impl/doc/LimrCdng_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `LimrCdng_MDD.docx`

- **Source path in repository:** `SF038A_LimrCdng_Impl/doc/LimrCdng_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

LimrCdng

July 22, 2015

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

| Initial Version | N. Saxton | 1.0.0 | 22-Jul-2015 |

Description

Author

Version

Date

Initial Version

N. Saxton

1.0.0

22-Jul-2015

Table of Contents

1LimrCdng High-Level Description4

2Design details of software module5

2.1Graphical representation of LimrCdng5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1.1Sub-Module Functions7

4.1.2Interrupt Service Routines7

4.1.3Server Runnable Functions7

4.1.4Module Internal (Local) Functions7

4.1.5Transition Functions7

5Known Limitations with Design8

6UNIT TEST CONSIDERATION9

Appendix AAbbreviations and Acronyms10

Appendix BGlossary11

Appendix CReferences12

## LimrCdng High-Level Description

This function provides a layer of protection from erroneous signals feeding into SF04 Sum & Limit. It is applied primarily to limiting signals that serve to reduce motor torque command under certain operating conditions. This function can prevent step response or toggling behavior that might cause undesirable vehicle feel. It includes fault injection capability at some inputs to facilitate tuning.

## Design details of software module

Refer FDD

### Graphical representation of LimrCdng

### Data Flow Diagram

Refer FDD

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer .m file

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {_Init()}

None

#### Periodic sub-module {LimrCdngPer1}

Refer FDD

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

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | SF038A  LimrCdng  FDD | See Synergy  subproject  version |

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

SF038A LimrCdng FDD

See Synergy subproject version

Back to [Application Software](../).
