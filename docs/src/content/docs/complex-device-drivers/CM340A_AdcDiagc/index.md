---
title: "Analog to Digital Converter Diagnostics (CM340A_AdcDiagc)"
description: "Analog to Digital Converter Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Analog to Digital Converter Diagnostics component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM340A_AdcDiagc_Design` | Design package |
| `CM340A_AdcDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM340A_AdcDiagc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM340A_AdcDiagc_Impl` |  |
| C sources | `CDD_AdcDiagc.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `AdcDiagc.dcf`, `AdcDiagc_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `AdcDiagc.dpa`, `CM340A_AdcDiagc_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM340A_AdcDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM340A_AdcDiagc_Impl/src/CDD_AdcDiagc.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM340A_AdcDiagc_DDReport.txt`

- **Source path in repository:** `CM340A_AdcDiagc_Design/Reports/CM340A_AdcDiagc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM340A_AdcDiagc_DataDict
28-Sep-2016 15:13:13
Tool Release:  2.46.0



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
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
Adc0ScanGroup2Ref0          	Cannot match name to list of known Nexteer signals.
Adc0ScanGroup2Ref1          	Cannot match name to list of known Nexteer signals.
Adc0ScanGroup3Ref0          	Cannot match name to list of known Nexteer signals.
Adc0ScanGroup3Ref1          	Cannot match name to list of known Nexteer signals.
Adc0SelfDiag0               	Cannot match name to list of known Nexteer signals.
Adc0SelfDiag2               	Cannot match name to list of known Nexteer signals.
Adc0SelfDiag4               	Cannot match name to list of known Nexteer signals.
Adc1ScanGroup2Ref0          	Cannot match name to list of known Nexteer signals.
Adc1ScanGroup2Ref1          	Cannot match name to list of known Nexteer signals.
Adc1ScanGroup3Ref0          	Cannot match name to list of known Nexteer signals.
Adc1ScanGroup3Ref1          	Cannot match name to list of known Nexteer signals.
(variables: 16, errors: 11)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
Adc0Faild                   	Cannot match name to list of known Nexteer signals.
Adc1Faild                   	Cannot match name to list of known Nexteer signals.
AdcDiagcEndPtrOutp          	Name does not match required pattern.
AdcDiagcEndPtrOutp          	Cannot match name to list of known Nexteer signals.
AdcDiagcStrtPtrOutp         	Name does not match required pattern.
AdcDiagcStrtPtrOutp         	Cannot match name to list of known Nexteer signals.
(variables: 6, errors: 6)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 4, errors: 0)

----------------------------------------------
IMPORTED CALIBRATIONS:	<ShoName><Identity>
---------------------------------------------
(variables: 0, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<Identity>
```
*... truncated (54 more lines in the source file). ...*

### `AdcDiagc_IntegrationManual.doc`

- **Source path in repository:** `CM340A_AdcDiagc_Impl/doc/AdcDiagc_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AdcDiagc_MDD.docx`

- **Source path in repository:** `CM340A_AdcDiagc_Impl/doc/AdcDiagc_MDD.docx`
- **Format:** `.docx`
- **Size:** `134 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

AdcDiagc

Aug 25, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Software Group,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Rijvi Ahmed | 1.0 | 02-Feb-2016 |

| Updated per design rev. 1.1.0 | Rijvi Ahmed | 2.0 | 23-Mar-2016 |

| Updated per design rev. 1. 4 .0 | Avinash James | 3.0 | 21-Jun-2016 |

| Updated per design rev. 1. 6 .0 | Avinash James | 4.0 | 15-Jul-2016 |

| Updated per design rev. 1. 7 .0 | Avinash James | 5.0 | 25-Aug-2016 |

Description

Author

Version

Date

Initial Version

Rijvi Ahmed

1.0

02-Feb-2016

Updated per design rev. 1.1.0

Rijvi Ahmed

2.0

23-Mar-2016

Updated per design rev. 1.4.0

Avinash James

3.0

21-Jun-2016

Updated per design rev. 1.6.0

Avinash James

4.0

15-Jul-2016

Updated per design rev. 1.7.0

Avinash James

5.0

25-Aug-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2AdcDiagc & High-Level Description6

3Design details of software module7

3.1Graphical representation of AdcDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: AdcDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: AdcDiagcPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1SetAdcParFlt9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………9

5.3Interrupt Functions10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2Local Function #210

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.4.3Local Function #310

5.4.3.1Design Rationale11

5.4.3.2Processing11

5.4.4Local Function #411

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Local Function #511

5.4.5.1Design Rationale11

5.4.5.2Processing11

5.4.6Local Function #611

5.4.6.1Design Rationale12

5.4.6.2Processing12

5.5GLOBAL Function/Macro Definitions12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

MDD for AdcDiagc

### Scope

## AdcDiagc & High-Level Description

Refer to FDD.

## Design details of software module

### Graphical representation of AdcDiagc

### Data Flow Diagram

None.

#### Component level DFD

Refer FDD.

#### Function level DFD

Refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MAXADCDIAGCST_CNT_U08 | 1 | CNT | 7 U |

| Refer to the FDD |  |  |  |

| MASKFLTCNTR_CNT_U08 | 1 | CNT | 127U |

Constant Name

Resolution

Units

Value

MAXADCDIAGCST_CNT_U08

1

CNT

7U

Refer to the FDD

MASKFLTCNTR_CNT_U08

1

CNT

127U

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

#### Init: AdcDiagcInit1

### Design Rationale

None

### Module Outputs

None

#### Per: AdcDiagcPer1

### Design Rationale

Refer FDD.

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD.

### Server Runables

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | St 2 Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | * RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |

Function Name

St2Proc

Type

Min

Max

Arguments Passed

AdcSelfDiag0_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag2_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag4_Volt_T_f32

float32

0.0

5.0

AdcDiagcSt_Uls_T_u08

Uint8

0

3

*RollgCntr_Cnt_T_u08

*uint8

0

255

Return Value

AdcNtcStInfo_Uls_T_u08

Uint8

0

255

### Design Rationale

### Processing

See “State 2” block in the Simulink model of the design.

### Local Function #2

| Function Name | St 4 Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | * RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |

Function Name

St4Proc

Type

Min

Max

Arguments Passed

AdcSelfDiag0_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag2_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag4_Volt_T_f32

float32

0.0

5.0

AdcDiagcSt_Uls_T_u08

Uint8

0

3

*RollgCntr_Cnt_T_u08

*uint8

0

255

Return Value

AdcNtcStInfo_Uls_T_u08

Uint8

0

255

### Design Rationale

### Processing

See “State 4” block in the Simulink model of the design.

### Local Function #3

| Function Name | St 6 Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcDiagcSt_Uls_T_u08 | Uint8 | 0 | 3 |

|  | * RollgCntr_Cnt_T_u08 | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |

Function Name

St6Proc

Type

Min

Max

Arguments Passed

AdcSelfDiag0_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag2_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag4_Volt_T_f32

float32

0.0

5.0

AdcDiagcSt_Uls_T_u08

Uint8

0

3

*RollgCntr_Cnt_T_u08

*uint8

0

255

Return Value

AdcNtcStInfo_Uls_T_u08

Uint8

0

255

### Design Rationale

### Processing

See “State 6” block in the Simulink model of the design.

### Local Function #4

| Function Name | St0 Proc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcSelfDiag0_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag2_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcSelfDiag4_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | * RollgCntr_Cnt_T_u08 | *uint8 | 00 | 3255 |

|  |  | *uint8 | 0 | 255 |

| Return Value | AdcNtcStInfo_Uls_T_u08 | Uint8 | 0 | 255 |

Function Name

St0Proc

Type

Min

Max

Arguments Passed

AdcSelfDiag0_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag2_Volt_T_f32

float32

0.0

5.0

AdcSelfDiag4_Volt_T_f32

float32

0.0

5.0

*RollgCntr_Cnt_T_u08

*uint8

00

3255

*uint8

0

255

Return Value

AdcNtcStInfo_Uls_T_u08

Uint8

0

255

### Design Rationale

### Processing

See “State 0” block in the Simulink model of the design.

### Local Function #5

| Function Name | Adc0StBasdProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Adc0ParFlt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | None | N/A | N/A | N/A |

Function Name

Adc0StBasdProc

Type

Min

Max

Arguments Passed

Adc0ParFlt_Cnt_T_u08

uint8

0

255

Return Value

None

N/A

N/A

N/A

### Design Rationale

### Processing

See “Adc0 State Based Processing” block in the Simulink model of the design.

### Local Function #6

| Function Name | Adc1 StBasdProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Adc 1 ParFlt_Cnt_T_u08 | uint8 | 0 | 255 |

| Return Value | None | N/A | N/A | N/A |

Function Name

Adc1StBasdProc

Type

Min

Max

Arguments Passed

Adc1ParFlt_Cnt_T_u08

uint8

0

255

Return Value

None

N/A

N/A

N/A

### Design Rationale

### Processing

See “Adc1 State Based Processing” block in the Simulink model of the design.

### Local Function #7

| Function Name | AdcDiagcPtrProc | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | N/A | N/A | N/A |

| Return Value | None | N/A | N/A | N/A |

Function Name

AdcDiagcPtrProc

Type

Min

Max

Arguments Passed

None

N/A

N/A

N/A

Return Value

None

N/A

N/A

N/A

### Design Rationale

### Processing

See “Adc Daigc Pointer” block in the Simulink model of the design.

### Local Function #8

| Function Name | ScanGroupAccrcyChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AdcScanGroupInpRefVltg_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcScanGroupRefVltg_Volt_T_f32 | float32 | 0.0 | 5.0 |

|  | AdcScanGroupInpRefPrm_Cnt_T_u08 | Uint8 | 0 | 255 |

| Return Value | ScanGroupAccrcyChkRefPrm_Cnt_u08 | Uint8 | 0 | 255 |

Function Name

ScanGroupAccrcyChk

Type

Min

Max

Arguments Passed

AdcScanGroupInpRefVltg_Volt_T_f32

float32

0.0

5.0

AdcScanGroupRefVltg_Volt_T_f32

float32

0.0

5.0

AdcScanGroupInpRefPrm_Cnt_T_u08

Uint8

0

255

Return Value

ScanGroupAccrcyChkRefPrm_Cnt_u08

Uint8

0

255

### Design Rationale

### Processing

See “Scan Group Accuracy Check” block in the Simulink model of the design.

### Local Function #9

| Function Name | SetAdcParFlt | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | * Adc0ParFlt_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | * Adc1ParFlt_Cnt_T_u08 | Uint8 | 0 | 255 |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

SetAdcParFlt

Type

Min

Max

Arguments Passed

*Adc0ParFlt_Cnt_T_u08

Uint8

0

255

*Adc1ParFlt_Cnt_T_u08

Uint8

0

255

Return Value

### Design Rationale

### Processing

See “Adc Parity Fault” block in the Simulink model of the design.

### GLOBAL Function/Macro Definitions

Note: The server runnable of this component are non-rte. So they are actually global functions which should belong to this section. But as they are already described under Server Runnable section so it’s omitted here.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

The overflow for the following PIMs are intentional as they are used as rolling counter.

Rte_Pim_Adc0FltCntSt0

Rte_Pim_Adc0FltCntSt2

Rte_Pim_Adc0FltCntSt4

Rte_Pim_Adc0FltCntSt6

Rte_Pim_Adc1FltCntSt0

Rte_Pim_Adc1FltCntSt2

Rte_Pim_Adc1FltCntSt4

Rte_Pim_Adc1FltCntSt6

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

| 2 | MDD Guideline | EA4 01.00.01 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.1 |

| 5 | FDD  - CM340 A_ AdcDiagc _Design | See Synergy sub project version |

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

1.0

4

Software Design and Coding Standards.doc

2.1

5

FDD  - CM340A_AdcDiagc_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
