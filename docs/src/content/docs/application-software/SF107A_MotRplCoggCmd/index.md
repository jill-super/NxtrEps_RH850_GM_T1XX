---
title: "Motor Ripple Cogging Command (SF107A_MotRplCoggCmd)"
description: "Motor Ripple Cogging Command: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Ripple Cogging Command component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF107A_MotRplCoggCmd_Design` | Design package |
| `SF107A_MotRplCoggCmd_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF107A_MotRplCoggCmd_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF107A_MotRplCoggCmd_Impl` |  |
| C sources | `CDD_MotRplCoggCmd.c`, `CDD_MotRplCoggCmd_MotCtrl.c` |
| Public headers | `CDD_MotRplCoggCmd.h`, `CDD_MotRplCoggCmd_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotRplCoggCmd.dcf`, `MotRplCoggCmd_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DVCfgCmd.log`, `MotRplCoggCmd.dpa`, `RteGen.bat`, `SF107A_MotRplCoggCmd_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF107A_MotRplCoggCmd_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `SF107A_MotRplCoggCmd_Impl/src/CDD_MotRplCoggCmd.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `SF107A_MotRplCoggCmd_Impl/src/CDD_MotRplCoggCmd_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF107A_MotRplCoggCmd_DDReport.txt`

- **Source path in repository:** `SF107A_MotRplCoggCmd_Design/Reports/SF107A_MotRplCoggCmd_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF107A_MotRplCoggCmd_DataDict
19-Jul-2016 11:39:48
Tool Release:  2.45.0



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
(variables: 2, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 10, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 3, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 1, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 4, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `MotRplCoggCmd_IntegrationManual.doc`

- **Source path in repository:** `SF107A_MotRplCoggCmd_Impl/doc/MotRplCoggCmd_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `151 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotRplCoggCmd_MDD.docx`

- **Source path in repository:** `SF107A_MotRplCoggCmd_Impl/doc/MotRplCoggCmd_MDD.docx`
- **Format:** `.docx`
- **Size:** `98 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotRplCoggCmd

Feb 9, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Selva Sengottaiyan

Nexteer Automotive,

Saginaw, MI, USAChange History

| Version | Description | Author | Date |

| --- | --- | --- | --- |

| 1 | Initial Version | Selva   Sengottaiyan | 09-Feb-2016 |

Version

Description

Author

Date

1

Initial Version

Selva Sengottaiyan

09-Feb-2016

Table of Contents

1Introduction5

2MotRplCoggCmd & High-Level Description6

3Design details of software module7

3.1Graphical representation of MotRplCoggCmd7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: MotRplCoggCmdInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: MotRplCoggCmdPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1GetMotCoggCmdPrm_Oper9

5.2.1.1Design Rationale9

5.2.1.2Store Module Inputs to Local copies10

5.2.1.3(Processing of function)………10

5.2.1.4Store Local copy of outputs into Module Outputs10

5.2.1SetMotCoggCmdPrm_Oper10

5.2.1.1Design Rationale10

5.2.1.2Store Module Inputs to Local copies10

5.2.1.3(Processing of function)………10

5.2.1.4Store Local copy of outputs into Module Outputs10

5.3Module Internal (Local) Functions10

5.3.1Local Function #110

5.3.1.1Design Rationale10

5.3.1.2Processing10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

Refer the Design Subproject.

## MotRplCoggCmd & High-Level Description

Refer the Design Subproject.

## Design details of software module

### Graphical representation of MotRplCoggCmd

Refer the Design Subproject.

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer the Design Subproject. | Refer the Design Subproject. | Refer the Design Subproject. | Refer the Design Subproject. |

Constant Name

Resolution

Units

Value

Refer the Design Subproject.

Refer the Design Subproject.

Refer the Design Subproject.

Refer the Design Subproject.

## Software Component Implementation

<The detailed design of the function is provided in the FDD. The detail design shall only be added to the MDD when it is not provided in the FDD or the FDD is not adequate and clarification is needed.>

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

<(Note: For multiple init or per functions, insert new headers at the “Header 3” level – subset of “Sub-Module Functions section above” and follow the same sub-section design shown below .  If none required, place the text “None”))>

### Init: MotRplCoggCmdInit1

### Design Rationale

Refer the Design Subproject

### Module Outputs

Refer the Design Subproject

### Per: MotRplCoggCmdPer1

### Design Rationale

Refer the Design Subproject

### Store Module Inputs to Local copies

Refer the Design Subproject

### (Processing of function)………

Refer the Design Subproject

### Store Local copy of outputs into Module Outputs

Refer the Design Subproject

### Server Runables

#### GetMotCoggCmdPrm_Oper

### Design Rationale

Refer the Design Subproject

### Store Module Inputs to Local copies

Refer the Design Subproject

### (Processing of function)………

Refer the Design Subproject

### Store Local copy of outputs into Module Outputs

Refer the Design Subproject

#### SetMotCoggCmdPrm_Oper

### Design Rationale

Refer the Design Subproject

### Store Module Inputs to Local copies

Refer the Design Subproject

### (Processing of function)………

Refer the Design Subproject

### Store Local copy of outputs into Module Outputs

Refer the Design Subproject

### Module Internal (Local) Functions

### Local Function #1

| Function Name | SinLookup | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Theta_Rad_T_f32 | Float32 | 0 | 2*PI |

|  |  |  |  |  |

| Return Value | Result_Uls_T_f32 | Float32 | 0 | 1 |

Function Name

SinLookup

Type

Min

Max

Arguments Passed

Theta_Rad_T_f32

Float32

0

2*PI

Return Value

Result_Uls_T_f32

Float32

0

1

### Design Rationale

### Processing

Refer the design

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

| 2 | MDD Guideline | EA4 01.00 .0 1 |

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

EA4 01.00.01

3

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.0

Back to [Application Software](../).
