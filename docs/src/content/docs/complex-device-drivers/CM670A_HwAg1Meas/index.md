---
title: "Handwheel Ag1 Measurement (CM670A_HwAg1Meas)"
description: "Handwheel Ag1 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Handwheel Ag1 Measurement component belongs to **Serial Interfaces and Position Sensing** in the **Complex Device Drivers** layer. It configures serial peripherals or measures rotor, handwheel-torque and handwheel-angle sensors.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM670A_HwAg1Meas_Design` | Design package |
| `CM670A_HwAg1Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM670A_HwAg1Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM670A_HwAg1Meas_Impl` |  |
| C sources | `HwAg1Meas.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `HwAg1Meas.dcf`, `HwAg1Meas_attr_def.xml`, `HwAg1Meas_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `HwAg1Meas_Cfg.h.tt`, `HwAg1Meas_Generate.bat` |
| Tooling and integration scripts | `CM670A_HwAg1Meas_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `HwAg1Meas.dpa`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM670A_HwAg1Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM670A_HwAg1Meas_Impl/src/HwAg1Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM670A_HwAg1Meas_DDReport.txt`

- **Source path in repository:** `CM670A_HwAg1Meas_Design/Reports/CM670A_HwAg1Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM670A_HwAg1Meas_DataDict
10-Jun-2016 12:13:14
Tool Release:  2.40.0



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
(variables: 6, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
HwAg1MeasHwAg1AutTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg1MeasHwAg1AutTrim       	.Description: 	Field is empty.
HwAg1MeasHwAg1AutTrim       	.Description: 	Field is empty.
HwAg1MeasHwAg1ClrTrim       	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg1MeasHwAg1ClrTrim       	.Description: 	Field is empty.
HwAg1MeasHwAg1ClrTrim       	.Description: 	Field is empty.
HwAg1MeasHwAg1ReadTrim      	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg1MeasHwAg1ReadTrim      	.Description: 	Field is empty.
HwAg1MeasHwAg1ReadTrim      	.Description: 	Field is empty.
HwAg1MeasHwAg1TrimPrfmdSts  	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg1MeasHwAg1TrimPrfmdSts  	.Description: 	Field is empty.
HwAg1MeasHwAg1TrimPrfmdSts  	.Description: 	Field is empty.
HwAg1MeasHwAg1WrTrim        	.SrvRunnnable:	Name should not contain FDDs <ShoName>
HwAg1MeasHwAg1WrTrim        	.Description: 	Field is empty.
HwAg1MeasHwAg1WrTrim        	.Description: 	Field is empty.
(variables: 5, errors: 15)

-----------------------
Client:	<TriggerName>
-------------------------
IoHwAb_SetFctPrphlHwAg1     	.Description: 	Field is empty.
IoHwAb_SetFctPrphlHwAg1     	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
SetNtcSts                   	.Description: 	Field is empty.
(variables: 6, errors: 3)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
HwAg1Phy                    	Cannot match name to list of known Nexteer signals.
HwAg1Phy                    	.Description: 	Field is empty.
HwAg1Phy                    	.ReadIn:	Field is empty.
HwAg1Polarity               	.Description: 	Field is empty.
RegInpRSENT2CS              	.Description: 	Field is empty.
RegInpRSENT2FND             	.Description: 	Field is empty.
RegInpRSENT2FRS             	.Description: 	Field is empty.
RegInpRSENT2FRXD            	.Description: 	Field is empty.
RegInpRSENT2NRS             	.Description: 	Field is empty.
(variables: 7, errors: 9)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
RegOutRSENT2NRC             	Cannot match name to list of known Nexteer signals.
RegOutRSENT2SPCT            	Cannot match name to list of known Nexteer signals.
(variables: 5, errors: 2)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 4, errors: 0)

```
*... truncated (61 more lines in the source file). ...*

### `HwAg1Meas_IntegrationManual.doc`

- **Source path in repository:** `CM670A_HwAg1Meas_Impl/doc/HwAg1Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `166 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `HwAg1Meas_MDD.docx`

- **Source path in repository:** `CM670A_HwAg1Meas_Impl/doc/HwAg1Meas_MDD.docx`
- **Format:** `.docx`
- **Size:** `193 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

HwAg1Meas

Jun 21,2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI

CHENNAI

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Selva Sengottaiyan | 1.0 | 21 -July-2015 |

| Updated to v1. 2 .0 of the FDD | Selva Sengottaiyan | 2.0 | 11-Sep-15 |

| Updated to v1. 4 .0 of the FDD | Selva Sengottaiyan | 3.0 | 2 3 -Dec-15 |

| Updated to v1. 11 .0 of the FDD | Ramachandran | 4.0 | 21-Jun-2016 |

Description

Author

Version

Date

Initial Version

Selva Sengottaiyan

1.0

21-July-2015

Updated to v1.2.0 of the FDD

Selva Sengottaiyan

2.0

11-Sep-15

Updated to v1.4.0 of the FDD

Selva Sengottaiyan

3.0

23-Dec-15

Updated to v1.11.0 of the FDD

Ramachandran

4.0

21-Jun-2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2HwAg1Meas High-Level Description5

3Design details of software module6

3.1Graphical representation of HwAg1Meas6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1.1Sub-Module Functions8

5.1.2Interrupt Service Routines8

5.1.3Server Runnable Functions9

5.1.4Module Internal (Local) Functions9

5.1.4.1Local Function #19

5.1.4.2Description9

5.1.5Transition Functions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

MDD for HwAg1.

### Scope

## HwAg1Meas High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of HwAg1Meas

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

HwAg1MeasInit1  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg1MeasPer1  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg1MeasPer2  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg1MeasPer3  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg1MeasPer4  (Refer FDD for details)

#### Periodic sub-module {_Per()}

HwAg1MeasPer5  (Refer FDD for details)

Design Rationale:

The implementation brings in the block “HwAg1Final” inside the True Condition of the “finalAbsAg”  as the other error condition will just retain the previous value and rolling counter will not change. It saves extra instructions in the implementation to the match the FDD. Final Functionality is still the same.

#### Interrupt Service Routines

None

#### Server Runnable Functions

#### Server Runnable: HwAg1MeasHwAg1AutTrim

Refer FDD for details

#### Server Runnable: HwAg1MeasHwAg1ClrTrim

Refer FDD for details

#### Server Runnable: HwAg1MeasHwAg1ReadTrim

Refer FDD for details

#### Server Runnable: HwAg1MeasHwAg1TrimPrfmdSts

Refer FDD for details

#### Server Runnable: HwAg1MeasHwAg1WrTrim

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

The implementation deviates from the FDD block “Intpn” block.   The implementation finds the minimum of  absolute values of the difference between HwAg1Step with all the values from the Calibration table and find the index  associated with minimum value of the difference in the calibration table.

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

*Rte_Pim_HwAg1Snsr0ComStsErrCntr()

*Rte_Pim_HwAg1Snsr0IdErrCntr()

*Rte_Pim_HwAg1Snsr0IntSnsrErrCntr()

*Rte_Pim_HwAg1Snsr0NoMsgErrCntr()

*Rte_Pim_HwAg1Snsr1ComStsErrCntr()

*Rte_Pim_HwAg1Snsr1IdErrCntr()

*Rte_Pim_HwAg1Snsr1IntSnsrErrCntr()

*Rte_Pim_HwAg1Snsr1NoMsgErrCntr()

(*Rte_Pim_HwAg1PrevRollCnt).

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

| 5 | FDD  -  CM670 A _ Hw Ag1 Meas _Design | See Synergy sub project version |

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

2.0

5

FDD  - CM670A_HwAg1Meas_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
