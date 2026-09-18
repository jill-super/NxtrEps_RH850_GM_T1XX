---
title: "Adc1 Configuration And Use (CM320A_Adc1CfgAndUse)"
description: "Adc1 Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Adc1 Configuration And Use component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM320A_Adc1CfgAndUse_Design` | Design package |
| `CM320A_Adc1CfgAndUse_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM320A_Adc1CfgAndUse_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM320A_Adc1CfgAndUse_Impl` |  |
| C sources | `CDD_Adc1CfgAndUse.c` |
| Public headers | `CDD_Adc1CfgAndUse.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `Adc1CfgAndUse.dcf`, `Adc1CfgAndUse_attr_def.xml`, `CDD_Adc1CfgAndUse_bswmd.arxml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `Adc1CfgAndUse_Generate.bat`, `CDD_Adc1CfgAndUse_Cfg.h.tt` |
| Tooling and integration scripts | `Adc1CfgAndUse.dpa`, `CM320A_Adc1CfgAndUse_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM320A_Adc1CfgAndUse_Impl/autosar/CDD_Adc1CfgAndUse_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM320A_Adc1CfgAndUse_Impl/src/CDD_Adc1CfgAndUse.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM320A_Adc1CfgAndUse_DDReport.txt`

- **Source path in repository:** `CM320A_Adc1CfgAndUse_Design/Reports/CM320A_Adc1CfgAndUse_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM320A_Adc1CfgAndUse_DataDict
07-Sep-2016 16:09:19
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
Adc1CfgAndUseAdc1EnaCnvn    	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 1, errors: 1)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
AdcDiagcEndPtrOutp          	Cannot match name to list of known Nexteer signals.
AdcDiagcStrtPtrOutp         	Cannot match name to list of known Nexteer signals.
AdcStrtOfCnvn2              	Cannot match name to list of known Nexteer signals.
AdcStrtOfCnvn2              	.ReadIn:	Field should contain only valid Periodic & Server Runnable names.	Adc1CfgAndUse is not allowed.
RegInpADCD1SGSR1            	Cannot match name to list of known Nexteer signals.
RegInpADCD1SGSR1            	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 4, errors: 6)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
DmaAdc1ResTrig              	Cannot match name to list of known Nexteer signals.
DmaAdc1ResTrig              	.WrittenIn:	Field should contain only valid Periodic & Server Runnable names.	Adc1CfgAndUse is not allowed.
RegOutpADCD1SGCR1           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGCR2           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGCR3           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGSTCR0         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGVCEP1         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGVCEP1         	    V              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGVCSP1         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD1SGVCSP1         	    V              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 7, errors: 10)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

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
```
*... truncated (51 more lines in the source file). ...*

### `Adc1CfgAndUse_IntegrationManual.docx`

- **Source path in repository:** `CM320A_Adc1CfgAndUse_Impl/doc/Adc1CfgAndUse_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `79 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

Adc1 Cfg And Use

VERSION: 3.0

DATE: 09-Jun-2016

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Selva Sengottaiyan | 1.0 | 4-May -2015 |

| 2 | Updated for design rev. 2.0.0 | Rijvi | 2.0 | 05-Feb-2016 |

| 3 | Added Newperiodic and removed one server runnable | Avinash James | 3.0 | 9-Jun-2016 |

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

Updated for design rev. 2.0.0

Rijvi

2.0

05-Feb-2016

3

Added Newperiodic and removed one server runnable

Avinash James

3.0

9-Jun-2016

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

| 1 | FDD  –   CM3 2 0 A  Adc 1 CfgAndUse | See synergy sub  project  version |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – CM320A Adc1CfgAndUse

See synergy sub project version

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

| None |  |  |

Modules

Notes

None

### Configuration Files to be provided by Integration Project

Yes

### Da Vinci Parameter Configuration Changes

| Parameter | Notes | SWC |

| --- | --- | --- |

| Refer the . m file in the design |  |  |

Parameter

Notes

SWC

Refer the . m file in the design

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

| Adc 1 CfgAndUse Init1 | None | RTE |

|  |  |  |

Init

Scheduling Requirements

Trigger

Adc1CfgAndUseInit1

None

RTE

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| Adc 1 CfgAndUse Per1 | None | 2ms(RTE) |

| Adc 1 CfgAndUse Per 2 | None | 2ms(RTE) |

| Adc1CfgAndUseAdc1EnaCnvn _Oper | None | On event |

|  |  |  |

Runnable

Scheduling Requirements

Trigger

Adc1CfgAndUsePer1

None

2ms(RTE)

Adc1CfgAndUsePer2

None

2ms(RTE)

Adc1CfgAndUseAdc1EnaCnvn_Oper

None

On event

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

### NvM Blocks

*See DataDict.m

## Compiler Settings

### Preprocessor MACRO

None

### Optimization Settings

None

## Appendix

None

### `Adc1CfgAndUse_MDD.doc`

- **Source path in repository:** `CM320A_Adc1CfgAndUse_Impl/doc/Adc1CfgAndUse_MDD.doc`
- **Format:** `.doc`
- **Size:** `174 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
