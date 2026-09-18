---
title: "Assist Summation Limiter (SF004B_AssiSumLim)"
description: "Assist Summation Limiter: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Assist Summation Limiter component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF004B_AssiSumLim_Design` | Design package |
| `SF004B_AssiSumLim_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF004B_AssiSumLim_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF004B_AssiSumLim_Impl` |  |
| C sources | `AssiSumLim.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `AssiSumLim.dcf`, `AssiSumLim_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `AssiSumLim.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `SF004B_AssiSumLim_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF004B_AssiSumLim_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF004B_AssiSumLim_Impl/src/AssiSumLim.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF004B_AssiSumLim.pdf`

- **Source path in repository:** `SF004B_AssiSumLim_Design/Doc/SF004B_AssiSumLim.pdf`
- **Format:** `.pdf`
- **Size:** `1627 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SF004B_AssiSumLim_DDReport.txt`

- **Source path in repository:** `SF004B_AssiSumLim_Design/Reports/SF004B_AssiSumLim_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF004B_AssiSumLim_DataDict
15-Jul-2015 15:15:55
Tool Release:  2.13.0



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
SetManTqCmd                 	.SrvRunnnable:	Name must end with "Server Runnable Name"
SetManTqCmd                 	.Return.Name	Field is empty.
SetManTqCmd                 	.Return.TestTolerance	Field is empty.
(variables: 1, errors: 3)

------------
Client:	
------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
EotAssiSca                  	Cannot match name to list of known Nexteer signals.
EotMotTqLim                 	Cannot match name to list of known Nexteer signals.
MotTqCmdLimDi               	Cannot match name to list of known Nexteer signals.
MotTqCmdOvrl                	Cannot match name to list of known Nexteer signals.
PinionCentrLrnCmd           	Cannot match name to list of known Nexteer signals.
PinionCentrLrnEna           	Cannot match name to list of known Nexteer signals.
PwrLimrRednFac              	Cannot match name to list of known Nexteer signals.
StallMotTqLim               	Cannot match name to list of known Nexteer signals.
ThermRednFac                	Cannot match name to list of known Nexteer signals.
TqLoaCmd                    	Cannot match name to list of known Nexteer signals.
TqSteerMtgtnCmd             	Cannot match name to list of known Nexteer signals.
VehSpdMotTqLim              	Cannot match name to list of known Nexteer signals.
(variables: 23, errors: 12)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 5, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 2, errors: 0)

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
```
*... truncated (41 more lines in the source file). ...*

### `AssiSumLim_Integration Manual.docx`

- **Source path in repository:** `SF004B_AssiSumLim_Impl/doc/AssiSumLim_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `79 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘AssiSumLim’

VERSION: 1.0

DATE: 04-June-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Sankardu   Varadapureddi | 1.0 | 22 - May -2015 |

|  |  |  |  |  |

Sl. No.

Description

Author

Version

Date

1

Initial version

Sankardu Varadapureddi

1.0

22-May-2015

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

| 1 | FDD  –   SF004B_AssiSumLim_Design | See Synergy  sub  project version |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding Standards | Process 3.06.00 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – SF004B_AssiSumLim_Design

See Synergy sub project version

2

Software Naming Conventions

Process 3.06.00

3

Software Design and Coding Standards

Process 3.06.00

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

Module

Required Feature

None

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

Refer DataDict.m file in the FDD

### Required Global Data Outputs

Refer DataDict.m file file in the FDD

### Specific Include Path present

No

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| AssiSumLimInit1 | None | Init |

Init

Scheduling Requirements

Trigger

AssiSumLimInit1

None

Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| AssiSumLimPer1 SetManTqCmd _Oper | None None | 2ms on event |

Runnable

Scheduling Requirements

Trigger

AssiSumLimPer1

SetManTqCmd_Oper

None

None

2ms

on event

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

| None |

Block Name

None

## Compiler Settings

### Preprocessor MACRO

None.

### Optimization Settings

None

## Appendix

None

### `AssiSumLim_MDD.docx`

- **Source path in repository:** `SF004B_AssiSumLim_Impl/doc/AssiSumLim_MDD.docx`
- **Format:** `.docx`
- **Size:** `108 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘AssiSumLim’

VERSION: 1.0

DATE: 03-June-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sankardu Varadapureddi | 1.0 | 03 - June -2015 |

|  |  |  |  |  |

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

Sankardu Varadapureddi

1.0

03-June-2015

Table of Contents

1Abbrevations And Acronyms5

2References6

3AssiSumLim High-Level Description7

4Design details of software module8

4.1Graphical representation of AssiSumLim8

4.2Data Flow Diagram8

4.2.1Module level DFD8

4.2.2Sub-Module level DFD9

4.3COMPONENT FLOW DIAGRAM9

5Variable Data Dictionary10

5.1User defined typedef definition/declaration10

5.2Variable definition for enumerated types10

6Constant Data Dictionary11

6.1Program(fixed) Constants11

6.1.1Embedded Constants11

6.1.1.1Local11

6.1.1.2Global11

6.1.2Module specific Lookup Tables Constants11

7Software Module Implementation12

7.1Sub-Module Functions12

7.1.1Initialization Functions12

7.1.1.1INIT: AssiSumLimInit112

7.1.1.1.1Design Rationale12

7.1.1.1.2Module Outputs12

7.1.1.1.3Module Internal12

7.1.2PERIODIC FUNCTIONS12

7.1.2.1Per: AssiSumLimPer112

7.1.2.1.1Design Rationale12

7.1.2.1.2Store Module Inputs to Local copies12

7.1.2.1.3(Processing of function)………12

7.1.2.1.4Store Local copy of outputs into Module Outputs12

7.1.3Interrupt Functions12

7.1.4Server runnables13

7.1.4.1SetManTqCmd13

7.1.4.1.1Design Rationale13

7.1.4.1.2Store Module Inputs to Local copies13

7.1.4.1.3(Processing of function)………13

7.1.4.1.4Store Local copy of outputs into Module Outputs13

7.1.5Local Function/Macro Definitions13

7.1.5.1Local Function #113

7.1.5.1.1Description13

7.1.5.2Local Function #213

7.1.5.2.1Description13

7.1.6GLObAL Function/Macro Definitions13

7.1.7Tranisition FUNCTIONS13

8Known Limitations With Design14

9UNIT TEST CONSIDERATION15

10Appendix16

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

| 1 | MDD Guidelines | Process  3 .06.00 |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding standards | Process 3.06.00 |

| 4 | FDD -  SF004B_AssiSumLim_Design | See Synergy  sub  project version |

|  |  |  |

Sr. No.

Title

Version

1

MDD Guidelines

Process 3.06.00

2

Software Naming Conventions

Process 3.06.00

3

Software Design and Coding standards

Process 3.06.00

4

FDD - SF004B_AssiSumLim_Design

See Synergy sub project version

## AssiSumLim High-Level Description

## Design details of software module

### Graphical representation of AssiSumLim

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

<This section documents any user types uniquely used for the module.>

| Typedef Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| None |  |  |  |  |

|  |  |  |  |  |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

None

### Variable definition for enumerated types

| Enum   Name | Element Name | Value |

| --- | --- | --- |

| None |  |  |

Enum  Name

Element Name

Value

None

## Constant Data Dictionary

### Program(fixed) Constants

### Embedded Constants

### Local

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

|  |  |  |  |

Constant Name

Resolution

Units

Value

Note: Refer .m file for constants definitions.

### Global

| Constant Name |

| --- |

| None |

Constant Name

None

### Module specific Lookup Tables Constants

| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

| None |  |  |  |

Constant Name

Resolution

Value

Software Segment

None

## Software Module Implementation

### Sub-Module Functions

### Initialization Functions

AssiSumLimInit1

### INIT: AssiSumLimInit1

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Refer ‘AssiSumLimInit1’ block in FDD

### Module Internal

None

### PERIODIC FUNCTIONS

### Per: AssiSumLimPer1

### Design Rationale

Design follows implementation in FDD.

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD  (Block ‘AssiSumLmtPer1’)

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Server runnables

### SetManTqCmd

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer ‘SetManTqCmd’ block in FDD

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

None

### GLObAL Function/Macro Definitions

None

### Tranisition FUNCTIONS

None

## Known Limitations With Design

None

## UNIT TEST CONSIDERATION

None

## Appendix

None

Back to [Application Software](../).
