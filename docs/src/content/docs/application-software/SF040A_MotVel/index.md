---
title: "Motor Velocity (SF040A_MotVel)"
description: "Motor Velocity: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Velocity component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF040A_MotVel_Design` | Design package |
| `SF040A_MotVel_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF040A_MotVel_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF040A_MotVel_Impl` |  |
| C sources | `CDD_MotVel.c`, `CDD_MotVel_MotCtrl.c` |
| Public headers | `CDD_MotVel.h`, `CDD_MotVel_MotCtrl_MemMap.h`, `CDD_MotVel_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotVel.dcf`, `MotVel_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotVel.dpa`, `RteGen.bat`, `SF040A_MotVel_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF040A_MotVel_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `SF040A_MotVel_Impl/src/CDD_MotVel.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `SF040A_MotVel_Impl/src/CDD_MotVel_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF040A_MotVel_DDReport.txt`

- **Source path in repository:** `SF040A_MotVel_Design/Reports/SF040A_MotVel_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF040A_MotVel_DataDict
29-Nov-2016 11:38:09
Tool Release:  2.51.0



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
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotCtrlMotAgBuf_SigIn       	Found in model but not in data dictionary.
MotCtrlMotAgTiBuf_SigIn     	Found in model but not in data dictionary.
(variables: 7, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotVelCrf                   	Name does not match required pattern.
MotVelMrf                   	Name does not match required pattern.
MotVelVld                   	Name does not match required pattern.
MotCtrlMotAgBuf_SigOut      	Found in model but not in data dictionary.
MotCtrlMotAgTiBuf_SigOut    	Found in model but not in data dictionary.
(variables: 6, errors: 5)

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
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 3, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
```
*... truncated (39 more lines in the source file). ...*

### `MotVel_Integration Manual.docx`

- **Source path in repository:** `SF040A_MotVel_Impl/doc/MotVel_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘MotVel’

VERSION: 1.0

DATE: 12-April-2016

Prepared By:

Software Group

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Rijvi  Ahmed | 1.0 | 12 - April -201 6 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial version

Rijvi Ahmed

1.0

12-April-2016

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

|  |  |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| 1 | FDD  –   SF 40A _ MotVel _Design | See Synergy  sub  project version |

| 2 | Software Naming Conventions | Process 04.02 .0 1 |

| 3 | Software Design and Coding Standards | Process 04.02.01 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – SF40A_MotVel_Design

See Synergy sub project version

2

Software Naming Conventions

Process 04.02.01

3

Software Design and Coding Standards

Process 04.02.01

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

Module

Required Feature

None

### Global Functions(Non RTE) to be provided to Integration Project

MotVelPer1

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

Refer DataDict.m file in the FDD

### Required Global Data Outputs

Refer DataDict.m file file in the FDD

### Specific Include Path present

Yes

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotVelInit1 | None | RTE/ Init |

Init

Scheduling Requirements

Trigger

MotVelInit1

None

RTE/Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| MotVel Per1 | None | Motor Control ISR |

| MotVelPer2 | None | RTE/2ms |

Runnable

Scheduling Requirements

Trigger

MotVelPer1

None

Motor Control ISR

MotVelPer2

None

RTE/2ms

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

| < Memmap   usuage  info> |  |  |

Feature

RAM

ROM

<Memmap usuage info>

Table 1: ARM Cortex R4 Memory Usage

### Non  RTE NvM Blocks

| Block Name |

| --- |

| None |

Block Name

None

### RTE NvM Blocks

| Block Name |

| --- |

| none |

Block Name

none

## Compiler Settings

### Preprocessor MACRO

None.

### Optimization Settings

None

## Appendix

None

### `MotVel_MDD.docx`

- **Source path in repository:** `SF040A_MotVel_Impl/doc/MotVel_MDD.docx`
- **Format:** `.docx`
- **Size:** `112 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘MotVel’

VERSION: 2.0

DATE:  18-Nov-2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

TATA ELXSI

CHENNAI, INDIA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Rijvi  Ahmed | 1.0 | 12 - April -201 6 |

| 2 | Updated per design rev. 2.0.0 | TATA | 2.0 | 18-Nov-2016 |

|  |  |  |  |  |

|  |  |  |  |  |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial Version

Rijvi Ahmed

1.0

12-April-2016

2

Updated per design rev. 2.0.0

TATA

2.0

18-Nov-2016

Table of Contents

1Abbrevations And Acronyms5

2References6

3MotVel & High-Level Description7

4Design details of software module8

4.1Graphical representation OF MotVel8

4.2Data Flow Diagram8

4.2.1Module level DFD8

4.2.2Sub-Module level DFD8

4.3COMPONENT FLOW DIAGRAM8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Constant Data Dictionary10

6.1Program(fixed) Constants10

6.1.1Embedded Constants10

6.1.1.1Local10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation11

7.1Sub-Module Functions11

7.1.1Initialization Functions11

7.1.2PERIODIC FUNCTIONS11

7.1.2.1INIT: MotVelPER111

7.1.2.1.1Design Rationale11

7.1.2.2Design Rationale11

7.1.2.3Store Module Inputs to Local copies11

7.1.2.4(Processing of function)………11

7.1.2.5Store Local copy of outputs into Module Outputs11

7.1.3PERIODIC FUNCTIONS11

7.1.3.1INIT: MotVelPER211

7.1.3.1.1Design Rationale11

7.1.3.2Design Rationale11

7.1.3.3Store Module Inputs to Local copies11

7.1.3.4(Processing of function)………11

7.1.3.5Store Local copy of outputs into Module Outputs11

7.1.4Interrupt Functions12

Server runnables12

7.1.4.1.1Store Local copy of outputs into Module Outputs12

7.1.4.2Local Function/Macro Definitions12

7.1.5GLObAL Function/Macro Definitions12

7.1.6Tranisition FUNCTIONS12

8Known Limitations With Design13

9UNIT TEST CONSIDERATION14

10Appendix15

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

| FDD | Functional Design Document |

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

| 1 | MDD Guidelines | Process 04.02 .0 1 |

| 2 | Software Naming Conventions | Process 04.02.01 |

| 3 | Software Design and Coding standards | Process 04.02.01 |

| 4 | FDD  :  SF 40A _ MotVel _Design | See Synergy  sub  project version |

|  |  |  |

Sr. No.

Title

Version

1

MDD Guidelines

Process 04.02.01

2

Software Naming Conventions

Process 04.02.01

3

Software Design and Coding standards

Process 04.02.01

4

FDD : SF40A_MotVel_Design

See Synergy sub project version

## MotVel & High-Level Description

Please refer FDD.

## Design details of software module

### Graphical representation OF MotVel

### Data Flow Diagram

Refer FDD

### Module level DFD

Refer FDD

### Sub-Module level DFD

Refer FDD

### COMPONENT FLOW DIAGRAM

Refer FDD

## Variable Data Dictionary

### User defined typedef definition/declaration

| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None | N/A | N/A | N/A | N/A |

|  |  |  |  |  |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

None

N/A

N/A

N/A

N/A

### Variable definition for enumerated types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

| None | N/A | N/A |

Enum  Name

Element Name

Value

None

N/A

N/A

## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer the m files |  |  |  |

Constant Name

Resolution

Units

Value

Refer the m files

6.1.1.2       Global

| Constant Name |

| --- |

| N/A |

Constant Name

N/A

### Module specific Lookup Tables Constants

| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

| None | N/A | N/A | N/A |

Constant Name

Resolution

Value

Software Segment

None

N/A

N/A

N/A

## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

None

### PERIODIC FUNCTIONS

### INIT: MotVelPER1

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### PERIODIC FUNCTIONS

### INIT: MotVelPER2

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Server runnables

None

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

None

### GLObAL Function/Macro Definitions

None

### Tranisition FUNCTIONS

None

## Known Limitations With Design

In SF040A datadictionary (Ver 2.0.0), MotAgBufIdx input signal is removed. But it is used in the SF040A implementation(ver 2.0.0)’MotVelPer2’. This leads mismatch between DD and Design.

MotCtrlMotAgBuf and MotCtrlMotAgTiBuf are removed in data dictionary but used in the model in MotVelPer1. This leads mismatch between DD and Design.

## UNIT TEST CONSIDERATION

None

## Appendix

None

Back to [Application Software](../).
