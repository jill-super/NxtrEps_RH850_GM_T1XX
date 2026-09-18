---
title: "Motor Angle 2 Measurement (ES241A_MotAg2Meas)"
description: "Motor Angle 2 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Angle 2 Measurement component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES241A_MotAg2Meas_Design` | Design package |
| `ES241A_MotAg2Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES241A_MotAg2Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES241A_MotAg2Meas_Impl` |  |
| C sources | `MotAg2Meas.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotAg2Meas.dcf`, `MotAg2Meas_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES241A_MotAg2Meas_Impl.gpj`, `MotAg2Meas.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES241A_MotAg2Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES241A_MotAg2Meas_Impl/src/MotAg2Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES241A_MotAg2Meas_DDReport.txt`

- **Source path in repository:** `ES241A_MotAg2Meas_Design/Reports/ES241A_MotAg2Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES241A_MotAg2Meas_DataDict
31-Aug-2016 15:26:57
Tool Release:  2.44.0



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
MotAg2MeasEolPrmRead        	.SrvRunnnable:	Name should not contain FDDs <ShoName>
MotAg2MeasEolPrmWr          	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 2, errors: 2)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 5, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotAg2CosAdcFaild           	Cannot match name to list of known Nexteer signals.
MotAg2SinAdcFaild           	Cannot match name to list of known Nexteer signals.
(variables: 5, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotAg2VltgSqd               	Cannot match name to list of known Nexteer signals.
(variables: 4, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 1, errors: 0)

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
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 2, errors: 0)
```
*... truncated (38 more lines in the source file). ...*

### `MotAg2Meas_IntegrationManual.doc`

- **Source path in repository:** `ES241A_MotAg2Meas_Impl/doc/MotAg2Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotAg2Meas_MDD.docx`

- **Source path in repository:** `ES241A_MotAg2Meas_Impl/doc/MotAg2Meas_MDD.docx`
- **Format:** `.docx`
- **Size:** `103 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

MotAg2Meas

Apr 22, 2016

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

| Initial Version | Sankardu   Varadapureddi | 1 | 28 -Aug-2015 |

| Updates of FDD v 1.5.0 and 1.6.0 | Krishna Anne | 2 | 16-Mar-2016 |

| Updates of FDD v 1.7.0 | Krishna Anne | 3 | 14-Apr-2016 |

| Fixed issue found w.r.t  MotPosTestOk_Cnt_T_lgc  during manual inspection | Krishna Anne | 4 | 14-Apr-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

28-Aug-2015

Updates of FDD v 1.5.0 and 1.6.0

Krishna Anne

2

16-Mar-2016

Updates of FDD v 1.7.0

Krishna Anne

3

14-Apr-2016

Fixed issue found w.r.t MotPosTestOk_Cnt_T_lgc during manual inspection

Krishna Anne

4

14-Apr-2016

Table of Contents1Introduction5

1.1.1.1Purpose5

1.1.1.2Scope5

2MotAg2Meas High-Level Description6

3Design details of software module7

3.1.1.1Graphical representation of MotAg2Meas7

3.1.1.2Data Flow Diagram7

3.1.2Component level DFD7

3.1.3Function level DFD7

4Constant Data Dictionary8

4.1.1.1Program (fixed) Constants8

4.1.2Embedded Constants8

5Software Component Implementation9

5.1.1.1Sub-Module Functions9

5.1.1.2Init: MotAg2MeasInit19

5.1.1.3Design Rationale9

5.1.1.4Module Outputs9

5.1.1.5Per: MotAg2MeasPer19

5.1.1.6Design Rationale9

5.1.1.79

5.1.1.8(Processing of function)………9

5.1.1.9Store Local copy of outputs into Module Outputs9

5.1.1.10Server Runables9

5.1.1.11MotAg2MeasEolPrmRead_Oper9

5.1.1.12Design Rationale9

5.1.1.13Store Module Inputs to Local copies9

5.1.1.14(Processing of function)………9

5.1.1.15MotAg2MeasEolPrmWr_Oper10

5.1.1.16Design Rationale10

5.1.1.17Store Module Inputs to Local copies10

5.1.1.18(Processing of function)………10

5.1.1.19Interrupt Functions10

5.1.1.20Module Internal (Local) Functions10

5.1.1.21GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## MotAg2Meas High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of MotAg2Meas

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| SINCOSMINERR_CNT_U08 | 1 | Cnt | 0x01 |

| SINCOSMAXERR_CNT_U08 | 1 | Cnt | 0x0 2 |

| ROLLCNTMAX_CNT_U08 | 1 | Cnt | 255 |

| MOTAG2VLTGSQDMIN | 1 | Volt | 0.0F |

| MOTAG2VLTGSQDMAX | 1 | Volt | 25.0F |

Constant Name

Resolution

Units

Value

SINCOSMINERR_CNT_U08

1

Cnt

0x01

SINCOSMAXERR_CNT_U08

1

Cnt

0x02

ROLLCNTMAX_CNT_U08

1

Cnt

255

MOTAG2VLTGSQDMIN

1

Volt

0.0F

MOTAG2VLTGSQDMAX

1

Volt

25.0F

## Software Component Implementation

### Sub-Module Functions

### Init: MotAg2MeasInit1

### Design Rationale

Refer FDD for the functionality.

### Module Outputs

Refer FDD

### Per: MotAg2MeasPer1

### Design Rationale

Refer FDD for the functionality.

In the path ES241A_MotAg2Meas/MotAg2Meas/MotAg2MeasPer1/AnalogMsbDiagnostics of the FDD model, the 4 input OR block would be redundantly doing the same functionality as done in the TestFail block of respective if action sub-system.

Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

### MotAg2MeasEolPrmRead_Oper

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### MotAg2MeasEolPrmWr_Oper

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

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

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  ES 241 A_   MotAg2Meas _Design | See Synergy sub project version |

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

FDD : ES241A_ MotAg2Meas_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
