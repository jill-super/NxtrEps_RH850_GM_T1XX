---
title: "Microcontroller Diagnostics (ES002A_McuDiagc)"
description: "Microcontroller Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Microcontroller Diagnostics component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES002A_McuDiagc_Design` | Design package |
| `ES002A_McuDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES002A_McuDiagc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES002A_McuDiagc_Impl` |  |
| C sources | `CDD_McuDiagc.c`, `CDD_McuDiagc_MotCtrl.c` |
| Public headers | `CDD_McuDiagc.h`, `CDD_McuDiagc_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `McuDiagc.dcf`, `McuDiagc_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES002A_McuDiagc_Impl.gpj`, `McuDiagc.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES002A_McuDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES002A_McuDiagc_Impl/src/CDD_McuDiagc.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES002A_McuDiagc_Impl/src/CDD_McuDiagc_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES002A_McuDiagc_DDReport.txt`

- **Source path in repository:** `ES002A_McuDiagc_Design/Reports/ES002A_McuDiagc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES002A_McuDiagc_DataDict
04-Oct-2016 09:50:17
Tool Release:  2.43.0



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
(variables: 1, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
FastLoopCntr                	Cannot match name to list of known Nexteer signals.
MotCtrlLoopCntr2MilliSec    	Cannot match name to list of known Nexteer signals.
SlowLoopCntr                	Cannot match name to list of known Nexteer signals.
(variables: 3, errors: 3)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
LoopCntr2MilliSec           	Cannot match name to list of known Nexteer signals.
MotCtrlFastLoopCntr         	Cannot match name to list of known Nexteer signals.
MotCtrlSlowLoopCntr         	Cannot match name to list of known Nexteer signals.
(variables: 3, errors: 3)

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
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 3, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
```
*... truncated (40 more lines in the source file). ...*

### `McuDiagc_IntegrationManual.docx`

- **Source path in repository:** `ES002A_McuDiagc_Impl/doc/McuDiagc_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

McuDiagc

VERSION: 3.0

DATE: 28-Sep-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva | 1 .0 | 29 - Mar - 2016 |

| 2 | Added diagnostic for 2  milli  second to Motor Control | Avinash  James | 2.0 | 22-Jun-2016 |

| 3 | Optimized the diagnostic and removed periodic 3 | Avinash  James | 3.0 | 28-Sep-2016 |

Sl. No.

Description

Author

Version

Date

1

Initial version

Selva

1.0

29-Mar-2016

2

Added diagnostic for 2 milli second to Motor Control

Avinash James

2.0

22-Jun-2016

3

Optimized the diagnostic and removed periodic 3

Avinash James

3.0

28-Sep-2016

Table of Contents

1Abbrevations And Acronyms4

2References5

3Dependencies6

3.1SWCs6

3.2Global Functions(Non RTE) to be provided to Integration Project6

4Configuration REQUIREMeNTS7

4.1Build Time Config7

4.2Configuration Files to be provided by Integration Project7

4.3Da Vinci Parameter Configuration Changes7

4.4DaVinci Interrupt Configuration Changes7

4.5Manual Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

FDD

Functional Design Document

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD –  ES002A  McuDiagc | See Synergy subproject version |

| 2 | Software Naming Conventions | Process 04.02. 01 |

| 3 | Software Coding Standards | Process 04.02. 01 |

Sr. No.

Title

Version

1

FDD – ES002A McuDiagc

See Synergy subproject version

2

Software Naming Conventions

Process 04.02.01

3

Software Coding Standards

Process 04.02.01

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

|  |  |

|  |  |

|  |  |

Module

Required Feature

None

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

None

## Configuration REQUIREMeNTS

### Build Time Config

| Modules | Notes |  |

| --- | --- | --- |

| None |  |  |

Modules

Notes

None

### Configuration Files to be provided by Integration Project

None

### Da Vinci Parameter Configuration Changes

| Parameter | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Parameter

Notes

SWC

None

### DaVinci Interrupt Configuration Changes

| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| None |  |  |  |

ISR Name

VIM #

Priority Dependency

Notes

None

### Manual Configuration Changes

| Constant | Notes | SWC |

| --- | --- | --- |

| None |  |  |

Constant

Notes

SWC

None

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

Refer DataDict.m file

### Required Global Data Outputs

Refer DataDict.m file

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagc Init1 | None | RTE ( Init ) |

Init

Scheduling Requirements

Trigger

McuDiagcInit1

None

RTE (Init)

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| McuDiagc Per1 | None | MotorControl  ISR*2 |

| McuDiagc Per 2 | None | RTE (2  ms ) |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Runnable

Scheduling Requirements

Trigger

McuDiagcPer1

None

MotorControl ISR*2

McuDiagcPer2

None

RTE (2 ms)

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotCtrl_START_SEC_CODE | Code section for Motor Control scheduled functions | Constants are defined at function level. Memory mapping need to be adjusted accordingly. |

|  |  |  |

Memory Section

Contents

Notes

MotCtrl_START_SEC_CODE

Code section for Motor Control scheduled functions

Constants are defined at function level. Memory mapping need to be adjusted accordingly.

* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage

| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |

Feature

RAM

ROM

None

Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `McuDiagc_MDD.doc`

- **Source path in repository:** `ES002A_McuDiagc_Impl/doc/McuDiagc_MDD.doc`
- **Format:** `.doc`
- **Size:** `154 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
