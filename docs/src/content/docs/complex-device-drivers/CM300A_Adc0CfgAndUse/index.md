---
title: "Adc0 Configuration And Use (CM300A_Adc0CfgAndUse)"
description: "Adc0 Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Adc0 Configuration And Use component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `CM300A_Adc0CfgAndUse_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM300A_Adc0CfgAndUse_Impl` |  |
| C sources | `CDD_Adc0CfgAndUse.c`, `CDD_Adc0CfgAndUse_MotCtrl.c` |
| Public headers | `CDD_Adc0CfgAndUse.h`, `CDD_Adc0CfgAndUse_MotCtrl_MemMap.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `Adc0CfgAndUse.dcf`, `Adc0CfgAndUse_attr_def.xml`, `CDD_Adc0CfgAndUse_bswmd.arxml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `Adc0CfgAndUse_Generate.bat`, `CDD_Adc0CfgAndUse_Cfg.h.tt` |
| Tooling and integration scripts | `Adc0CfgAndUse.dpa`, `CM300A_Adc0CfgAndUse_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM300A_Adc0CfgAndUse_Impl/autosar/CDD_Adc0CfgAndUse_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM300A_Adc0CfgAndUse_Impl/src/CDD_Adc0CfgAndUse.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM300A_Adc0CfgAndUse_Impl/src/CDD_Adc0CfgAndUse_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `Adc0CfgAndUse_IntegrationManual.docx`

- **Source path in repository:** `CM300A_Adc0CfgAndUse_Impl/doc/Adc0CfgAndUse_IntegrationManual.docx`
- **Format:** `.docx`
- **Size:** `83 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

Adc0 Cfg And Use

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

| 3 | Updated fro design rev 2.1.0 | Avinash James | 3.0 | 09-Jun-2016 |

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

Updated fro design rev 2.1.0

Avinash James

3.0

09-Jun-2016

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

1Appendix12

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

| <1> | FDD  –   CM3 0 0 A  Adc0CfgAndUse | See synergy sub  project  version |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

<1>

FDD – CM300A Adc0CfgAndUse

See synergy sub project version

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| MotCtrlMgr | Generated struct type declarations for the Motor Control loop / RTE interface data; macros for access of Motor Control loop data |

Module

Required Feature

MotCtrlMgr

Generated struct type declarations for the Motor Control loop / RTE interface data; macros for access of Motor Control loop data

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

### Global Functions(Non RTE) to be provided to Integration Project

Adc0CfgAndUsePer1 : To be called ever other motor control ISR loop and updates the start and end pointers of ADC diagnostics and scan group 1

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

| Adc0CfgAndUse Init1 | None | RTE /Init |

Init

Scheduling Requirements

Trigger

Adc0CfgAndUseInit1

None

RTE/Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

|  |  |  |

| Adc0CfgAndUsePer1 | None | Non RTE/2xMotor Control ISR rate |

Runnable

Scheduling Requirements

Trigger

Adc0CfgAndUsePer1

None

Non RTE/2xMotor Control ISR rate

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| CDD_Adc0CfgAndUse_MotCtrl_START_SEC |  |  |

|  |  |  |

Memory Section

Contents

Notes

CDD_Adc0CfgAndUse_MotCtrl_START_SEC

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

### `Adc0CfgAndUse_MDD.doc`

- **Source path in repository:** `CM300A_Adc0CfgAndUse_Impl/doc/Adc0CfgAndUse_MDD.doc`
- **Format:** `.doc`
- **Size:** `173 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
