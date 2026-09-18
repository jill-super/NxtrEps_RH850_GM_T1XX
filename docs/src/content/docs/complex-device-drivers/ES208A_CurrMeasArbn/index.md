---
title: "Current Measurement Arbitration (ES208A_CurrMeasArbn)"
description: "Current Measurement Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Current Measurement Arbitration component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES208A_CurrMeasArbn_Design` | Design package |
| `ES208A_CurrMeasArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES208A_CurrMeasArbn_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES208A_CurrMeasArbn_Impl` |  |
| C sources | `CDD_CurrMeasArbn.c`, `CDD_CurrMeasArbn_MotCtrl.c` |
| Public headers | `CDD_CurrMeasArbn.h`, `CDD_CurrMeasArbn_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CurrMeasArbn.dcf`, `CurrMeasArbn_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `CurrMeasArbn.dpa`, `ES208A_CurrMeasArbn_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES208A_CurrMeasArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES208A_CurrMeasArbn_Impl/src/CDD_CurrMeasArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES208A_CurrMeasArbn_Impl/src/CDD_CurrMeasArbn_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES208A FR v1.1.pdf`

- **Source path in repository:** `ES208A_CurrMeasArbn_Design/Doc/ES208A FR v1.1.pdf`
- **Format:** `.pdf`
- **Size:** `48 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ES208A_CurrMeasArbn_DDReport.txt`

- **Source path in repository:** `ES208A_CurrMeasArbn_Design/Reports/ES208A_CurrMeasArbn_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES208A_CurrMeasArbn_DataDict
29-Sep-2015 10:29:37
Tool Release:  2.21.0



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
(variables: 13, errors: 0)

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
(variables: 1, errors: 0)

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
(variables: 4, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
						 For "Local" CONSTANTS  --- <IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `CurrMeasArbn_IntegrationManual.docx`

- **Source path in repository:** `ES208A_CurrMeasArbn_Impl/doc/CurrMeasArbn_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `79 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

CURRENT MEASUREMENT ARBITRATION

VERSION: 1.2

DATE: 14-APR-2015

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva Sengottaiyan | 1.0 | 14 - Apr -2015 |

|  |  |  |  |  |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial version

Selva Sengottaiyan

1.0

14-Apr-2015

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

7.3Non  RTE NvM Blocks10

7.4RTE NvM Blocks10

8Compiler Settings11

8.1Preprocessor MACRO11

8.2Optimization Settings11

9Appendix12

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  | <ADD  more to the table if applicable> |

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

<ADD  more to the table if applicable>

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| <1> | FDD - ES2 0 8 A  Current  Measurement   Arbitration | See synergy subversion |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

<1>

FDD - ES208A Current Measurement Arbitration

See synergy subversion

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None | N/A |

Module

Required Feature

None

N/A

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

CurrMeasArbnPer1()

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

| N/A |  |  |

Parameter

Notes

SWC

N/A

### DaVinci Interrupt Configuration Changes

| ISR Name | VIM # | Priority Dependency | Notes |

| --- | --- | --- | --- |

| N/A |  |  |  |

ISR Name

VIM #

Priority Dependency

Notes

N/A

### Manual Configuration Changes

| Constant | Notes | SWC |

| --- | --- | --- |

| N/A |  |  |

Constant

Notes

SWC

N/A

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

| CurrMeas ArbnInit1 | None | RTE |

|  |  |  |

Init

Scheduling Requirements

Trigger

CurrMeasArbnInit1

None

RTE

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CurrMeas Arbn Per1 | None | MOTCTRL ISR*2 |

Runnable

Scheduling Requirements

Trigger

CurrMeasArbnPer1

None

MOTCTRL ISR*2

.

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| MotCtrl_START_SEC_CODE | Code section for Motor Control scheduled functions |  |

|  |  |  |

Memory Section

Contents

Notes

MotCtrl_START_SEC_CODE

Code section for Motor Control scheduled functions

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

### Non  RTE NvM Blocks

| Block Name |

| --- |

| None |

Block Name

None

Note : Size of the NVM block if configured in developer

### RTE NvM Blocks

| Block Name |

| --- |

| None |

Block Name

None

Note : Size of the NVM block if configured in developer

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `CurrMeasArbn_MDD.doc`

- **Source path in repository:** `ES208A_CurrMeasArbn_Impl/doc/CurrMeasArbn_MDD.doc`
- **Format:** `.doc`
- **Size:** `160 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
