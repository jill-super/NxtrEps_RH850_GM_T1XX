---
title: "Power Disconnect (ES003A_PwrDiscnct)"
description: "Power Disconnect: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Power Disconnect component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES003A_PwrDiscnct_Design` | Design package |
| `ES003A_PwrDiscnct_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES003A_PwrDiscnct_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES003A_PwrDiscnct_Impl` |  |
| C sources | `PwrDiscnct.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `PwrDiscnct.dcf`, `PwrDiscnct_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES003A_PwrDiscnct_Impl.gpj`, `PwrDiscnct.dpa`, `PwrDiscnct.pznywf.silent.dcusr`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES003A_PwrDiscnct_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES003A_PwrDiscnct_Impl/src/PwrDiscnct.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES003A_PwrDiscnct.pdf`

- **Source path in repository:** `ES003A_PwrDiscnct_Design/Doc/ES003A_PwrDiscnct.pdf`
- **Format:** `.pdf`
- **Size:** `37 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ES003A_PwrDiscnct_DDReport.txt`

- **Source path in repository:** `ES003A_PwrDiscnct_Design/Reports/ES003A_PwrDiscnct_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES003A_PwrDiscnct_DataDict
10-Apr-2015 14:16:16
Tool Release:  2.8.0



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

--------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init
--------------------------------------------------
(variables: 1, errors: 0)

-------------------------------------
SrvRunnable:	<ShoName><TriggerName>
-------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
BattVltg                    	Cannot match name to list of known Nexteer signals.
BattVltgSwd1                	Cannot match name to list of known Nexteer signals.
BattVltgSwd2                	Cannot match name to list of known Nexteer signals.
(variables: 5, errors: 3)

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
(variables: 5, errors: 0)

-------------------------------------------
NON-VOLATILE MEMORY:	<ShoName><Identity>
-------------------------------------------
(variables: 0, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<ShoName><Identity>Prev
-----------------------------------------------
PwrDiscnctDeltaVltg1        	Name does not match required pattern. Name should end with "Prev".
PwrDiscnctDeltaVltg2        	Name does not match required pattern. Name should end with "Prev".
PwrDiscnctSeqATestCmplPrev  	.DocUnits:  	Not on approved list.
(variables: 3, errors: 3)

------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: <IDENTITY>_<UNITS>_<DATATYPE>
------------------------------------------------------------------
```
*... truncated (23 more lines in the source file). ...*

### `PwrDiscnct_Integration Manual.docx`

- **Source path in repository:** `ES003A_PwrDiscnct_Impl/doc/PwrDiscnct_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘PwrDiscnct’

VERSION: 1.0

DATE: 09-Apr-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Sankardu   Varadapureddi | 1.0 | 09 - Apr -2015 |

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

09-Apr-2015

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

| 1 | FDD -  ES003A_PwrDiscnct_Design | See Synergy  sub  project version |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding Standards | Process 3.06.00 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD - ES003A_PwrDiscnct_Design

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

| None |  |  |

Init

Scheduling Requirements

Trigger

None

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| PwrDiscnct Per1 | None | RTE   ( 2 ms) |

Runnable

Scheduling Requirements

Trigger

PwrDiscnctPer1

None

RTE (2ms)

.

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| PwrDiscnct_ST ART _SEC_CODE |  |  |

|  |  |  |

Memory Section

Contents

Notes

PwrDiscnct_START_SEC_CODE

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

### `PwrDiscnct_MDD.docx`

- **Source path in repository:** `ES003A_PwrDiscnct_Impl/doc/PwrDiscnct_MDD.docx`
- **Format:** `.docx`
- **Size:** `94 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘PwrDiscnct’

VERSION: 1.0

DATE: 09-Apr-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sankardu   Varadapureddi | 1.0 | 09 - Apr -2015 |

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

09-Apr-2015

Table of Contents

1Abbrevations And Acronyms4

2References5

3Power Disconnect High-Level Description6

4Design details of software module7

4.1Graphical representation of POWER DISCONNECT7

4.2Data Flow Diagram7

4.2.1Module level DFD7

4.2.2Sub-Module level DFD7

4.3COMPONENT FLOW DIAGRAM7

5Variable Data Dictionary8

5.1User defined typedef definition/declaration8

5.2Variable definition for enumerated types8

6Constant Data Dictionary9

6.1Program(fixed) Constants9

6.1.1Embedded Constants9

6.1.1.1Local9

6.1.1.2Global9

6.1.2Module specific Lookup Tables Constants9

7Software Module Implementation10

7.1Sub-Module Functions10

7.1.1Initialization Functions10

7.1.2PERIODIC FUNCTIONS10

7.1.2.1Per: PwrDiscnct_Per110

7.1.2.1.1Design Rationale10

7.1.2.1.2Store Module Inputs to Local copies10

7.1.2.1.3(Processing of function)………10

7.1.2.1.4Store Local copy of outputs into Module Outputs10

7.1.3Interrupt Functions10

7.1.4Serial Communication Functions11

7.1.5Local Function/Macro Definitions11

7.1.6GLObAL Function/Macro Definitions11

7.1.7Tranisition FUNCTIONS11

8Known Limitations With Design12

9UNIT TEST CONSIDERATION13

10Appendix14

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

| 1 | MDD Guidelines | Process 3.06.00 |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding standards | Process 3.06.00 |

| 4 | FDD -  ES003A_PwrDiscnct_Design | See Synergy  sub  project version |

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

FDD - ES003A_PwrDiscnct_Design

See Synergy sub project version

## Power Disconnect High-Level Description

This function will verify that the PowerDisconnect is not stuck closed at init once per Ignition Cycle.

## Design details of software module

### Graphical representation of POWER DISCONNECT

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

| Typedef  Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

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

| Enum    Name | Element Name | Value |

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

| None |  |  |  |

Constant Name

Resolution

Units

Value

None

### Global

| Constant Name |

| --- |

|  |

Constant Name

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

None

### PERIODIC FUNCTIONS

### Per: PwrDiscnctPer1

### Design Rationale

Design follows implemenetation in FDD.

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD  (Block ‘PwrDiscnct’)

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Serial Communication Functions

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

## Appendix

None

Back to [Complex Device Drivers](../).
