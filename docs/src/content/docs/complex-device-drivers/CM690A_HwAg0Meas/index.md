---
title: "Handwheel Ag0 Measurement (CM690A_HwAg0Meas)"
description: "Handwheel Ag0 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Ag0 Measurement component belongs to **Serial Interfaces and Position Sensing** in the **Complex Device Drivers** layer. It configures serial peripherals or measures rotor, handwheel-torque and handwheel-angle sensors.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM690A_HwAg0Meas_Design` | Design package |
| `CM690A_HwAg0Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM690A_HwAg0Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM690A_HwAg0Meas_Impl` |  |
| C sources | `HwAg0Meas.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAg0Meas.dcf`, `HwAg0Meas_attr_def.xml`, `HwAg0Meas_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `HwAg0Meas_Cfg.h.tt`, `HwAg0Meas_Generate.bat` |
| Tooling and integration scripts | `CM690A_HwAg0Meas_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAg0Meas.dpa`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM690A_HwAg0Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM690A_HwAg0Meas_Impl/src/HwAg0Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM690A_HwAg0Meas_DDReport.txt`

- **Source path in repository:** `CM690A_HwAg0Meas_Design/Reports/CM690A_HwAg0Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `10 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM690A_HwAg0Meas_DataDict
10-Jun-2016 12:07:58
Tool Release:  2.40.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)
[Warning: Model 'NxtrNvM' was created with a newer version (R2015b) of Simulink
To create a model that is compatible with this version of Simulink, load the model in Simulink R2015b and select File > Export Model to > Previous Version.] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 60): block_diagram does not have a parameter named 'ShowVisualizeInsertedRTB' in group 'EditorSettings'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 61): block_diagram does not have a parameter named 'ShowMarkup' in group 'EditorSettings'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2335): annotation does not have a parameter named 'InternalMargins'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2336): annotation does not have a parameter named 'FixedHeight'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2337): annotation does not have a parameter named 'FixedWidth'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2348): annotation does not have a parameter named 'InternalMargins'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2349): annotation does not have a parameter named 'FixedHeight'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2350): annotation does not have a parameter named 'FixedWidth'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2360): annotation does not have a parameter named 'InternalMargins'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2361): annotation does not have a parameter named 'FixedHeight'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: NxtrNvM (blockdiagram.xml, line 2362): annotation does not have a parameter named 'FixedWidth'] 
[> In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2229
  In C:\D_Projects\EA4\Guideline_Template\FDD Dependencies\FDDDependencies v2.40.0\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 

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
(variables: 6, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
HwAg0MeasHwAg0AutTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg0MeasHwAg0AutTrim       	.Description: 	Field is empty.
HwAg0MeasHwAg0AutTrim       	.Description: 	Field is empty.
HwAg0MeasHwAg0ClrTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg0MeasHwAg0ClrTrim       	.Description: 	Field is empty.
HwAg0MeasHwAg0ClrTrim       	.Description: 	Field is empty.
HwAg0MeasHwAg0ReadTrim      	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg0MeasHwAg0ReadTrim      	.Description: 	Field is empty.
HwAg0MeasHwAg0ReadTrim      	.Description: 	Field is empty.
HwAg0MeasHwAg0TrimPrfmdSts  	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg0MeasHwAg0TrimPrfmdSts  	.Description: 	Field is empty.
HwAg0MeasHwAg0TrimPrfmdSts  	.Description: 	Field is empty.
HwAg0MeasHwAg0WrTrim        	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg0MeasHwAg0WrTrim        	.Description: 	Field is empty.
```
*... truncated (100 more lines in the source file). ...*

### `HwAg0Meas_IntegrationManual.doc`

- **Source path in repository:** `CM690A_HwAg0Meas_Impl/doc/HwAg0Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `160 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAg0Meas_MDD.docx`

- **Source path in repository:** `CM690A_HwAg0Meas_Impl/doc/HwAg0Meas_MDD.docx`
- **Format:** `.docx`
- **Size:** `207 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAg0Meas

Jun 21, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI

Chennai

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Selva   Sengottaiyan | 1.0 | 21 - July -2015 |

| Updated for V1.5.0 | Selva   Sengottaiyan | 2.0 | 9-Sep-2015 |

| Updated for v1.6.0 | Selva   Sengottaiyan | 4 .0 | 2 3-Dec-2015 |

| Updated for v1.11.0 | TATA | 5.0 | 21-Jun-2016 |

Description

Author

Version

Date

Initial Version

Selva Sengottaiyan

1.0

21-July-2015

Updated for V1.5.0

Selva Sengottaiyan

2.0

9-Sep-2015

Updated for v1.6.0

Selva Sengottaiyan

4.0

23-Dec-2015

Updated for v1.11.0

TATA

5.0

21-Jun-2016

Table of Contents

1Introduction6

1.1Purpose6

1.2Scope6

2HwAg0Meas High-Level Description7

3Design details of software module8

3.1Graphical representation of HwAg0Meas8

3.2Data Flow Diagram8

3.2.1Component level DFD8

3.2.2Function level DFD8

4Constant Data Dictionary9

4.1Program (fixed) Constants9

4.1.1Embedded Constants9

5Software Component Implementation10

5.1.1Sub-Module Functions10

5.1.2Interrupt Service Routines11

5.1.3Server Runnable Functions11

5.1.4Module Internal (Local) Functions11

5.1.4.1Local Function #111

5.1.4.2Description12

5.1.5Transition Functions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

## HwAg0Meas High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of HwAg0Meas

### Data Flow Diagram

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Value |

| --- | --- |

| MAXWAITININ_MICROSEC_U32 | ((uint32)2U) |

| DATAAVLMAXWAIT_MICROSEC_U32 | ((uint32)300U) |

| COMSTSMAXWAIT_MICROSEC_U32 | ((uint32)5U) |

| PRTCLFLTMASK_CNT_U32 | 0xFEU |

| SNSRIDMASK_CNT_U08 | 0x00FU |

| MSGSTSMASK_CNT_U08 | 0x01U |

| COMSTSMASK_CNT_U32 | 0x30000000UL |

| DATAMASK_CNT_U16 | 0xFFF0U |

Constant Name

Value

MAXWAITININ_MICROSEC_U32

((uint32)2U)

DATAAVLMAXWAIT_MICROSEC_U32

((uint32)300U)

COMSTSMAXWAIT_MICROSEC_U32

((uint32)5U)

PRTCLFLTMASK_CNT_U32

0xFEU

SNSRIDMASK_CNT_U08

0x00FU

MSGSTSMASK_CNT_U08

0x01U

COMSTSMASK_CNT_U32

0x30000000UL

DATAMASK_CNT_U16

0xFFF0U

## Software Component Implementation

#### Sub-Module Functions

#### Initialization sub-module {_Init()}

HwAg0MeasInit1  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg0MeasPer1  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg0MeasPer2  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg0MeasPer3  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg0MeasPer4  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg0MeasPer5  (Refer FDD for details)

Design Rationale:

The implementation brings in the block “HwAg0Final” inside the  True Condition of the “finalAbsAg”  as the other error condition will just retain the previous value and rolling counter will not change. It saves extra instructions in the implementation to the match the FDD. Final Functionality is still the same.

#### Interrupt Service Routines

None

#### Server Runnable Functions

#### Server Runnable: HwAg0MeasHwAg0AutTrim

Refer FDD for details

#### Server Runnable: HwAg0MeasHwAg0ClrTrim

Refer FDD for details

#### Server Runnable: HwAg0MeasHwAg0ReadTrim

Refer FDD for details

#### Server Runnable: HwAg0MeasHwAg0TrimPrfmdSts

Refer FDD for details

#### Server Runnable: HwAg0MeasHwAg0WrTrim

Refer FDD for details

#### Module Internal (Local) Functions

### Local Function #1

| Function Name | CalcHwAgIdx | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwA gStep_HwDeg_T_f32 | f loat32 | - 900 | 900 |

|  |  |  |  |  |

|  |  |  |  |  |

|  |  |  |  |  |

| Return Value | Index_Cnt_T_u08 | uint16 | 0 | 22 |

Function Name

CalcHwAgIdx

Type

Min

Max

Arguments Passed

HwAgStep_HwDeg_T_f32

float32

-900

900

Return Value

Index_Cnt_T_u08

uint16

0

22

### Description

The implementation deviates from the FDD block “Intpn” block.   The implementation finds the minimum of  absolute values of the difference between HwAg0Step with all the values from the Calibration table and find the index  associated with minimum value of the difference in the calibration table.

### Local Function #2

| Function Name | ReadRegister | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | RegisterDummyRead_Cnt_T_u32 | N/A | N/A | N/A |

| Return Value | RegisterDummyRead_Cnt_T_u32 | N/A | N/A | N/A |

Function Name

ReadRegister

Type

Min

Max

Arguments Passed

RegisterDummyRead_Cnt_T_u32

N/A

N/A

N/A

Return Value

RegisterDummyRead_Cnt_T_u32

N/A

N/A

N/A

### Design Rationale

This function can be used both for read-and-use and for read-and-discard

#### Transition Functions

None

## Known Limitations with Design

None

## UNIT TEST CONSIDERATION

Roll Over is intentional for

*Rte_Pim_HwAg0Snsr0ComStsErrCntr()

*Rte_Pim_HwAg0Snsr0IdErrCntr()

*Rte_Pim_HwAg0Snsr0IntSnsrErrCntr()

*Rte_Pim_HwAg0Snsr0NoMsgErrCntr()

*Rte_Pim_HwAg0Snsr1ComStsErrCntr()

*Rte_Pim_HwAg0Snsr1IdErrCntr()

*Rte_Pim_HwAg0Snsr1IntSnsrErrCntr()

*Rte_Pim_HwAg0Snsr1NoMsgErrCntr()

(*Rte_Pim_HwAg0PrevRollCnt).

Thus counter acts in circular

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

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD  -  CM690 A _ HwAg0Meas _Design | See Synergy sub project version |

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

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.1

5

FDD  - CM690A_HwAg0Meas_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
