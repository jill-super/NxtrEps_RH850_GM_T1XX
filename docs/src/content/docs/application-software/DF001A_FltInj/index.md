---
title: "Fault Injection (DF001A_FltInj)"
description: "Fault Injection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Fault Injection component belongs to **Diagnostic and Fault-Injection Functions** in the **Application Software** layer. It supports diagnostics, fault injection or test sweeps used during development and verification.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `DF001A_FltInj_Design` | Design package |
| `DF001A_FltInj_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `DF001A_FltInj_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `DF001A_FltInj_Impl` |  |
| C sources | `FltInj.c` |
| Public headers | `FltInj.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `FltInj.dcf`, `FltInj_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DF001A_FltInj_Impl.gpj`, `FltInj.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `DF001A_FltInj_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `DF001A_FltInj_Impl/src/FltInj.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `DF001A_FltInj_DDReport.txt`

- **Source path in repository:** `DF001A_FltInj_Design/Reports/DF001A_FltInj_DDReport.txt`
- **Format:** `.txt`
- **Size:** `11 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of DF001A_FltInj_DataDict
14-Jun-2016 06:43:45
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
FltInj_logl                 	    Inj_logl       Unknown Keyword used.Only Nexteer approved Keywords should be used.
UpdUsrPrm                   	Found in model but not in data dictionary.
(variables: 4, errors: 2)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
FltInjUsrPrm_ArgIn          	Found in model but not in data dictionary.
SigPah_ArgIn1               	Found in model but not in data dictionary.
SigPah_ArgIn2               	Found in model but not in data dictionary.
SigPah_ArgIn3               	Found in model but not in data dictionary.
SigPah_ArgIn4               	Found in model but not in data dictionary.
(variables: 1, errors: 5)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
SigPah_ArgOut1              	Found in model but not in data dictionary.
SigPah_ArgOut4              	Found in model but not in data dictionary.
SigPah_ArgOut2              	Found in model but not in data dictionary.
SigPah_ArgOut3              	Found in model but not in data dictionary.
(variables: 0, errors: 4)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
FltInjPahGain               	Name does not match required pattern.
FltInjPahOffs               	Name does not match required pattern.
(variables: 2, errors: 2)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 0, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
```
*... truncated (131 more lines in the source file). ...*

### `FltInj_IntegrationManual.doc`

- **Source path in repository:** `DF001A_FltInj_Impl/doc/FltInj_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `141 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `FltInj_MDD.docx`

- **Source path in repository:** `DF001A_FltInj_Impl/doc/FltInj_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

FltInj

04/29/2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Lucas  Wendling | 1.0 | 08/26/15 |

| U pdates are per FDD v2.1.0 | Krishna Anne | 2.0 | 04/29/16 |

Description

Author

Version

Date

Initial Version

Lucas Wendling

1.0

08/26/15

Updates are per FDD v2.1.0

Krishna Anne

2.0

04/29/16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2<Component Name> & High-Level Description6

3Design details of software module7

3.1Graphical representation of <Component Name>7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: <Component Name>_Init<n>9

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: <Component Name>_Per<n>9

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1<Server Runable Name>9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………10

5.3Interrupt Functions10

5.3.1Interrupt Function Name10

5.3.1.1Design Rationale10

5.3.1.2(Processing of the ISR function)…..10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale11

5.5.1.2processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

MDD for FltInj (DF001A).

## FltInj High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of FltInj

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| TICNVN_MICROTOMILLI_F32 | Single precision float | MicroToMilli | 0.001 |

Constant Name

Resolution

Units

Value

TICNVN_MICROTOMILLI_F32

Single precision float

MicroToMilli

0.001

For other constants, refer DataDict.m

## Software Component Implementation

### Sub-Module Functions

### Init:

None

### Design Rationale

N/A

### Module Outputs

N/A

### Per: FltInjPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### FltInj_f32_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### FltInj_logl_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### FltInj_u08_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### FltInj_u0p16_Oper

### Design Rationale

Refer FDD

### (Processing of function)………

Refer FDD

### Interrupt Functions

None

### Interrupt Function Name

N/A

### Design Rationale

N/A

### (Processing of the ISR function)…..

N/A

### Module Internal (Local) Functions

NA

|  |  |  |  |  |

| --- | --- | --- | --- | --- |

|  |  |  |  |  |

|  |  |  |  |  |

|  |  |  |  |  |

### GLOBAL Function/Macro Definitions

NA

|  |  |  |  |  |

| --- | --- | --- | --- | --- |

|  |  |  |  |  |

|  |  |  |  |  |

|  |  |  |  |  |

## Known Limitations with Design

## UNIT TEST CONSIDERATION

Unit testing should be performed for when the build constant FLTINJENA is set to STD_ON in order to enable core functionality of this module.  This will have to be done by manually altering FltInj.h to change the value of this #define.

The SigPah_Arg signal of the FltInj_f32 server runnable has a special unit test consideration (MIL, SIL, PIL) that the range called out in the data dictionary should only be used for defining "input" vectors, and the range check that is normal done on the "output" is skipped in this special instance. (This second point is copied from the FDD).

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

| 4 | DF001A_FltInj_Design | See Synergy subproject version |

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

4

DF001A_FltInj_Design

See Synergy subproject version

Back to [Application Software](../).
