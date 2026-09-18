---
title: "Current Measurement (ES200A_CurrMeas)"
description: "Current Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Current Measurement component belongs to **Measurement and Arbitration** in the **Complex Device Drivers** layer. It acquires a sensed quantity (current, torque, angle, voltage, temperature) and arbitrates or correlates redundant measurements.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES200A_CurrMeas_Design` | Design package |
| `ES200A_CurrMeas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES200A_CurrMeas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES200A_CurrMeas_Impl` |  |
| C sources | `CDD_CurrMeas.c`, `CDD_CurrMeas_MotCtrl.c` |
| Public headers | `CDD_CurrMeas.h`, `CDD_CurrMeas_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CurrMeas.dcf`, `CurrMeas_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `CurrMeas.dpa`, `ES200A_CurrMeas_Impl.gpj`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES200A_CurrMeas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES200A_CurrMeas_Impl/src/CDD_CurrMeas.c`. 

Top-level functions defined in `CDD_CurrMeas.c` (factual extract, first 1):

- `Rte_Prm_CurrMeasEolOffsHiBrdgVltgMin_Val`

Additional implementation units: `ES200A_CurrMeas_Impl/src/CDD_CurrMeas_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES200A_CurrMeas_DDReport.txt`

- **Source path in repository:** `ES200A_CurrMeas_Design/Reports/ES200A_CurrMeas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES200A_CurrMeas_DataDict
02-Aug-2016 17:04:17
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
(variables: 4, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
CurrMeasEolGainReq          	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasEolGainStsReq       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasEolOffsReq          	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasEolOffsStsReq       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasGainReadReq         	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasGainWrReq           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasOffsReadReq         	.SrvRunnnable:	Name should not contain FDDs <ShoName>
CurrMeasOffsWrReq           	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 8, errors: 8)

-----------------------
Client:	<TriggerName>
-------------------------
CurrMeasEolGainCalSet_SetRamBlockStatus	.Client:	Name should not contain FDDs <ShoName>
CurrMeasEolOffsCalSet_SetRamBlockStatus	.Client:	Name should not contain FDDs <ShoName>
(variables: 6, errors: 2)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotCtrlMotCurrAdcVlyAAdcFaild	Cannot match name to list of known Nexteer signals.
MotCtrlMotCurrAdcVlyBAdcFaild	Cannot match name to list of known Nexteer signals.
MotCtrlMotCurrAdcVlyCAdcFaild	Cannot match name to list of known Nexteer signals.
MotCtrlMotCurrAdcVlyDAdcFaild	Cannot match name to list of known Nexteer signals.
MotCtrlMotCurrAdcVlyEAdcFaild	Cannot match name to list of known Nexteer signals.
MotCtrlMotCurrAdcVlyFAdcFaild	Cannot match name to list of known Nexteer signals.
(variables: 41, errors: 6)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
CurrMeasWrmIninTestCmpl     	Name does not match required pattern.
(variables: 15, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
CurrMeasEolFixdPwmPerd      	Found in data dictionary but not in model.
(variables: 22, errors: 1)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 1, errors: 0)

-------------------------------------------
```
*... truncated (54 more lines in the source file). ...*

### `CurrMeas_IntegrationManual.docx`

- **Source path in repository:** `ES200A_CurrMeas_Impl/doc/CurrMeas_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `80 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

CURRENT MEASUREMENT

VERSION: 4.0

DATE: 30-Mar-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva Sengottaiyan | 1.0 | 4-May -2015 |

| 2 | Added fault injection | Nick Saxton | 2.0 | 10-Aug-2015 |

| 3 | Updated to v 3.1.0 of FDD | Selva Sengottaiyan | 3.0 | 29-Sep-2015 |

| 4 | Updated per design rev. 4.2.0 | Rijvi Ahmed | 4 .0 | 30-Mar-2016 |

Sl. No.

Description

Author

Version

Date

1

Initial version

Selva Sengottaiyan

1.0

4-May-2015

2

Added fault injection

Nick Saxton

2.0

10-Aug-2015

3

Updated to v 3.1.0 of FDD

Selva Sengottaiyan

3.0

29-Sep-2015

4

Updated per design rev. 4.2.0

Rijvi Ahmed

4.0

30-Mar-2016

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

| <1> | FDD  –  ES2 0 0 A  Current  Measurement | See synergy subversion |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

<1>

FDD – ES200A Current Measurement

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

CurrMeasPer2()

## Configuration REQUIREMeNTS

### Build Time Config

| Modules | Notes |  |

| --- | --- | --- |

| FLTINJENA | Set to STD_ON for Fault Injection |  |

Modules

Notes

FLTINJENA

Set to STD_ON for Fault Injection

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

| CurrMeas Init1 | None | RTE |

|  |  |  |

Init

Scheduling Requirements

Trigger

CurrMeasInit1

None

RTE

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CurrMeasPer 1 | None | 2ms(RTE) |

| CurrMeasPer 2 | None | MOTCTRL ISR*2 |

| CurrMeasPer3 | None | 2ms(RTE) |

| CurrMeasEolGainReq | None | On Event |

| CurrMeasEolGain St s Req | None | On Event |

| CurrMeasEol Offs Req | None | On Event |

| CurrMeasEol OffsSt s Req | None | On Event |

| CurrMeasGainWrReq | None | On Event |

| CurrMeasGain Read Req | None | On Event |

| CurrMeasOffsWrReq | None | On Event |

| CurrMeasOffsReadReq | None | On Event |

Runnable

Scheduling Requirements

Trigger

CurrMeasPer1

None

2ms(RTE)

CurrMeasPer2

None

MOTCTRL ISR*2

CurrMeasPer3

None

2ms(RTE)

CurrMeasEolGainReq

None

On Event

CurrMeasEolGainStsReq

None

On Event

CurrMeasEolOffsReq

None

On Event

CurrMeasEolOffsStsReq

None

On Event

CurrMeasGainWrReq

None

On Event

CurrMeasGainReadReq

None

On Event

CurrMeasOffsWrReq

None

On Event

CurrMeasOffsReadReq

None

On Event

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

| CurrMeasEolGainCalSet     CurrMeasEolOffsCalSet |

Block Name

CurrMeasEolGainCalSet

CurrMeasEolOffsCalSet

Note : Size of the NVM block if configured in developer

The NVM block needs not used.

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `CurrMeas_MDD.doc`

- **Source path in repository:** `ES200A_CurrMeas_Impl/doc/CurrMeas_MDD.doc`
- **Format:** `.doc`
- **Size:** `266 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
