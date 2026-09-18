---
title: "Hands On Wheel Detection (SF044A_HowDetn)"
description: "Hands On Wheel Detection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Hands On Wheel Detection component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF044A_HowDetn_Design` | Design package |
| `SF044A_HowDetn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF044A_HowDetn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF044A_HowDetn_Impl` |  |
| C sources | `HowDetn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HowDetn.dcf`, `HowDetn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HowDetn.dpa`, `RteGen.bat`, `SF044A_HowDetn_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF044A_HowDetn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF044A_HowDetn_Impl/src/HowDetn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF044A_HowDetn_DDReport.txt`

- **Source path in repository:** `SF044A_HowDetn_Design/Reports/SF044A_HowDetn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF044A_HowDetn_DataDict
21-Nov-2016 14:05:14
Tool Release:  2.50.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, Struct.EngMin has been increased to the EngMin of the Struct data type.
Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.50.0\+bt\@struct\struct.m',44,1)">struct.struct>struct.validateUserEngMin at 44</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.50.0\+DataDict\@PIM\PIM.m',139,1)">PIM.PIM>PIM.set.EngMin at 139</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\01_EA4_FDDs\SF044A_HowDetn_Design\21Nov2016\SF044A_HowDetn_DataDict.m',680,1)">SF044A_HowDetn_DataDict at 680</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v2.1.0\Design_Tools\VerifyDD.p>ImportVars at 2085
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v2.1.0\Design_Tools\VerifyDD.p>VerifyDD at 247] 
[Warning: In workspace, Struct.EngMax has been increased to the EngMax of the Struct data type.
Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.50.0\+bt\@struct\struct.m',72,1)">struct.struct>struct.validateUserEngMax at 72</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.50.0\+DataDict\@PIM\PIM.m',149,1)">PIM.PIM>PIM.set.EngMax at 149</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\01_EA4_FDDs\SF044A_HowDetn_Design\21Nov2016\SF044A_HowDetn_DataDict.m',681,1)">SF044A_HowDetn_DataDict at 681</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v2.1.0\Design_Tools\VerifyDD.p>ImportVars at 2085
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v2.1.0\Design_Tools\VerifyDD.p>VerifyDD at 247] 
(errors: 2)

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
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 2, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
HowDetnEstimn               	Name does not match required pattern.
HowDetnFlg                  	Name does not match required pattern.
HowDetnFlg                  	Cannot match name to list of known Nexteer signals.
HowDetnSt                   	Name does not match required pattern.
(variables: 3, errors: 4)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 17, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)
```
*... truncated (51 more lines in the source file). ...*

### `HowDetn_IntegrationManual.doc`

- **Source path in repository:** `SF044A_HowDetn_Impl/doc/HowDetn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HowDetn_MDD.docx`

- **Source path in repository:** `SF044A_HowDetn_Impl/doc/HowDetn_MDD.docx`
- **Format:** `.docx`
- **Size:** `138 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HowDetn

December 01, 2016

December 01, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI,

CHENNAI, INDIA Prepared By:

TATA ELXSI,

CHENNAI, INDIA Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | BG | 1 | 01/29/2016 |

| Se rver runnables, Interrupt functions, Module Internal (Local) Functions, GLOBAL Function/Macro Definitions - sub portions  were  removed Footer template updated to  EA4 01.00.01 | BG | 2 | 02/15/2016 |

| Updated to design version 2.0 .0 | TATA | 3 | 01-Dec-16 |

Description

Author

Version

Date

Initial Version

BG

1

01/29/2016

Server runnables, Interrupt functions, Module Internal (Local) Functions, GLOBAL Function/Macro Definitions - sub portions were removed

Footer template updated to EA4 01.00.01

BG

2

02/15/2016

Updated to design version 2.0.0

TATA

3

01-Dec-16

Table of Contents

1.Introduction5

1.1Purpose5

1.2Scope5

2HowDetn High-Level Description6

2.1Graphical representation of HowDetn6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Init: HowDetnInit18

4.1.1.1Design Rationale8

4.1.1.2Module Outputs8

4.1.2Per: HowDetnPer18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function)………8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.5GLOBAL Function/Macro Definitions8

5Known Limitations with Design9

6UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## 1. Introduction

### Purpose

The purpose of this document is to document the module level design for a HowDetn software module which is the part of the software related to Nexteer’s Electrical Steering Systems product line.

### Scope

Scope of the document is to capture the software implementation details of HowDetn Module.

## HowDetn High-Level Description

Determination of a continuous valued estimate that represents the likelihood that a driver's hands are on the steering wheel (value =1) or off the steering wheel (value=0).  A discrete value corresponding to the confidence of the estimate is also specified Design details of software module

### Graphical representation of HowDetn

### Data Flow Diagram

Refer to FDD

#### Component level DFD

Refer to FDD

#### Function level DFD

Refer to FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer  SF044A_HowDetn_DataDict .m | NA | NA | NA |

Constant Name

Resolution

Units

Value

Refer SF044A_HowDetn_DataDict.m

NA

NA

NA

## Software Component Implementation

Refer FDD

### Sub-Module Functions

### Init: HowDetnInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: HowDetnPer1

### Design Rationale

Refer FDD

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

| 2 | MDD Guideline | EA4 01.00 .0 1 |

| 3 | Software Naming Conventions.doc | 2.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD : SF044 A_ HowDetn _Design | See Synergy sub project version |

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

2.0

4

Software Design and Coding Standards.doc

2.1

5

FDD : SF044A_HowDetn_Design

See Synergy sub project version

Back to [Application Software](../).
