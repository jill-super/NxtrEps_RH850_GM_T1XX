---
title: "Power Limiter (SF019B_PwrLimr)"
description: "Power Limiter: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Power Limiter component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF019B_PwrLimr_Design` | Design package |
| `SF019B_PwrLimr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF019B_PwrLimr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF019B_PwrLimr_Impl` |  |
| C sources | `PwrLimr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `PwrLimr.dcf`, `PwrLimr_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `PwrLimr.dpa`, `RteGen.bat`, `SF019B_PwrLimr_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF019B_PwrLimr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF019B_PwrLimr_Impl/src/PwrLimr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF019B_PwrLimr_DDReport.txt`

- **Source path in repository:** `SF019B_PwrLimr_Design/Reports/SF019B_PwrLimr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `7 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF019B_PwrLimr_DataDict
31-Mar-2016 13:46:32
Tool Release:  2.36.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 4294967295.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 4294967295.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 4294967295.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 65535.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 255.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 255.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMin is not within the data types Min/Max limits and has been limited to 0.
Please update your saved files.] 
[Warning: In workspace, CSArguments.EngMax is not within the data types Min/Max limits and has been limited to 65535.
Please update your saved files.] 
(errors: 14)

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
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
AltFltActv                  	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
PwrLimrRednFac              	Name does not match required pattern.
(variables: 2, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
MotEnvlpSpd                 	.Description: 	Field is empty.
```
*... truncated (82 more lines in the source file). ...*

### `PwrLimr_IntegrationManual.doc`

- **Source path in repository:** `SF019B_PwrLimr_Impl/doc/PwrLimr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `PwrLimr_MDD.docx`

- **Source path in repository:** `SF019B_PwrLimr_Impl/doc/PwrLimr_MDD.docx`
- **Format:** `.docx`
- **Size:** `129 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

PwrLimr

August 14, 2015

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

| Initial Version | Nick Saxton | 1.0 | 14-Aug-2015 |

Description

Author

Version

Date

Initial Version

Nick Saxton

1.0

14-Aug-2015

Table of Contents

1PwrLimr High-Level Description4

2Design details of software module5

2.1Graphical representation of PwrLimr5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: PwrLimrInit17

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.1.2Per: PwrLimrPer17

4.1.2.1Design Rationale7

4.1.2.2Store Module Inputs to Local copies7

4.1.2.3(Processing of function)………7

4.1.2.4Store Local copy of outputs into Module Outputs7

4.1.3Per: PwrLimrPer27

4.1.3.1Design Rationale7

4.1.3.2Store Module Inputs to Local copies7

4.1.3.3(Processing of function)………7

4.1.3.4Store Local copy of outputs into Module Outputs7

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Design Rationale8

4.4.1.2Processing8

4.5GLOBAL Function/Macro Definitions8

5Known Limitations with Design9

6UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## PwrLimr High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of PwrLimr

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MAXNRIVTRS_CNT_F32 | Single precision float | Cnt | 2.0 |

Constant Name

Resolution

Units

Value

MAXNRIVTRS_CNT_F32

Single precision float

Cnt

2.0

For other constants, refer DataDict.m

## Software Component Implementation

### Sub-Module Functions

### Init: PwrLimrInit1

### Design Rationale

Init function is present in DataDict.m file but not shown in FDD model. Per the note in SF019B_PwrLimr/PwrLimr in the model, the init function is responsible for updating the low pass filters used in the periodic functions. Additionally, the init function starts up a timer used in the ‘Asst_Lmt_Condition_Determination’ block in the model.

### Module Outputs

Refer FDD

### Per: PwrLimrPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Per: PwrLimrPer2

### Design Rationale

GetTiSpan100MicroSec32bit returns elapsed time in counts where one count is equal to 100 microseconds. Therefore, the value returned from that function is divided by 10 to get the elapsed time in milliseconds.

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

| 3 | EA4  Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | SF019B_PwrLimr_Design | See Synergy subproject version |

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

SF019B_PwrLimr_Design

See Synergy subproject version

Back to [Application Software](../).
