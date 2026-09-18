---
title: "Current Measurement Correlation (ES209A_CurrMeasCorrln)"
description: "Current Measurement Correlation: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Current Measurement Correlation component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES209A_CurrMeasCorrln_Design` | Design package |
| `ES209A_CurrMeasCorrln_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES209A_CurrMeasCorrln_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES209A_CurrMeasCorrln_Impl` |  |
| C sources | `CurrMeasCorrln.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CurrMeasCorrln.dcf`, `CurrMeasCorrln_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `CurrMeasCorrln.dpa`, `ES209A_CurrMeasCorrln_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES209A_CurrMeasCorrln_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES209A_CurrMeasCorrln_Impl/src/CurrMeasCorrln.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES209A_CurrMeasCorrln_DDReport.txt`

- **Source path in repository:** `ES209A_CurrMeasCorrln_Design/Reports/ES209A_CurrMeasCorrln_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES209A_CurrMeasCorrln_DataDict
15-Aug-2016 11:24:50
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
(variables: 1, errors: 0)

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
(variables: 14, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
CurrMeasCorrlnSts           	Name does not match required pattern.
CurrMotSumABC               	Cannot match name to list of known Nexteer signals.
CurrMotSumDEF               	Cannot match name to list of known Nexteer signals.
(variables: 4, errors: 3)

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
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 4, errors: 0)

--------------------------------------------------------------------------------------------
```
*... truncated (37 more lines in the source file). ...*

### `CurrMeasCorrln_IntegrationManual.docx`

- **Source path in repository:** `ES209A_CurrMeasCorrln_Impl/doc/CurrMeasCorrln_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `80 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

CURRENT MEASUREMENT CORRELATION

VERSION: 2.0

DATE: 27-Jun-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva   Sengottaiyan | 1.0 | 09 - Apr -2015 |

| 2 | Added  FltInj  point for an output | Krishna Anne | 2.0 | 27-Jun-16 |

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

09-Apr-2015

2

Added FltInj point for an output

Krishna Anne

2.0

27-Jun-16

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

| <1> | FDD - ES2 09 A  Current  Measurement  Correlation | < . 2 . 7. 0> |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

<1>

FDD - ES209A Current Measurement Correlation

<.2.7.0>

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

None

## Configuration REQUIREMeNTS

### Build Time Config

| Modules | Notes |  |

| --- | --- | --- |

| CurrMeasCorrln | FLTINJENA  should be set to  STD_ON  as required |  |

Modules

Notes

CurrMeasCorrln

FLTINJENA should be set to STD_ON as required

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

No

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| None |  |  |

|  |  |  |

Init

Scheduling Requirements

Trigger

None

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CurrMeasCorrlnPer1 | None | RTE  2 ms Task |

Runnable

Scheduling Requirements

Trigger

CurrMeasCorrlnPer1

None

RTE 2ms Task

.

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |

|  |  |  |

Memory Section

Contents

Notes

None

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

### `CurrMeasCorrln_MDD.doc`

- **Source path in repository:** `ES209A_CurrMeasCorrln_Impl/doc/CurrMeasCorrln_MDD.doc`
- **Format:** `.doc`
- **Size:** `185 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
