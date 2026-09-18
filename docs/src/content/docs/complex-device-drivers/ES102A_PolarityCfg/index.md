---
title: "Polarity Configuration (ES102A_PolarityCfg)"
description: "Polarity Configuration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Polarity Configuration component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES102A_PolarityCfg_Design` | Design package |
| `ES102A_PolarityCfg_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES102A_PolarityCfg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES102A_PolarityCfg_Impl` |  |
| C sources | `PolarityCfg.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PolarityCfg.dcf`, `PolarityCfg_attr_def.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES102A_PolarityCfg_Impl.gpj`, `PolarityCfg.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES102A_PolarityCfg_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES102A_PolarityCfg_Impl/src/PolarityCfg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES102A_PolarityCfg_DDReport.txt`

- **Source path in repository:** `ES102A_PolarityCfg_Design/Reports/ES102A_PolarityCfg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES102A_PolarityCfg_DataDict
29-Apr-2016 13:35:42
Tool Release:  2.38.0



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
PolarityCfgRead             	.SrvRunnnable:	Name should not contain FDDs <ShoName>
PolarityCfgWr               	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 2, errors: 2)

-----------------------
Client:	<TriggerName>
-------------------------
PolarityCfgSaved_SetRamBlockStatus	.Client:	Name should not contain FDDs <ShoName>
(variables: 1, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 0, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 26, errors: 0)

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
PolarityCfgSaved            	Name does not match required pattern.
(variables: 1, errors: 1)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

```
*... truncated (35 more lines in the source file). ...*

### `PolarityCfg_Integration Manual.docx`

- **Source path in repository:** `ES102A_PolarityCfg_Impl/doc/PolarityCfg_Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `78 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

‘PolarityCfg’

VERSION: 1.0

DATE: 26-May-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial version | Sankardu   Varadapureddi | 1.0 | 26 - May -2015 |

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

26-May-2015

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

| 1 | FDD  –   ES 102 A_ PolarityCfg _Design | See Synergy  sub  project version |

| 2 | Software Naming Conventions | Process 3.06.00 |

| 3 | Software Design and Coding Standards | Process 3.06.00 |

|  |  |  |

|  |  |  |

Sr. No.

Title

Version

1

FDD – ES102A_PolarityCfg_Design

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

| PolarityCfgInit 1 | None | Init |

Init

Scheduling Requirements

Trigger

PolarityCfgInit1

None

Init

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| PolarityCfgRead_Oper PolarityCfgWr_Oper |  | On event On event |

Runnable

Scheduling Requirements

Trigger

PolarityCfgRead_Oper

PolarityCfgWr_Oper

On event

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

| PolarityCfgSaved |

Block Name

PolarityCfgSaved

## Compiler Settings

### Preprocessor MACRO

None.

### Optimization Settings

None

## Appendix

None

### `PolarityCfg_MDD.docx`

- **Source path in repository:** `ES102A_PolarityCfg_Impl/doc/PolarityCfg_MDD.docx`
- **Format:** `.docx`
- **Size:** `99 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

‘PolarityCfg’

VERSION: 1.0

DATE: 26-May-2015

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date |

| --- | --- | --- | --- | --- |

| 1 | Initial Version | Sankardu Varadapureddi | 1.0 | 26 - May -2015 |

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

26-May-2015

Table of Contents

1Abbrevations And Acronyms5

2References6

3Power Disconnect High-Level Description7

4Design details of software module8

4.1Graphical representation of POWER DISCONNECT8

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

6.1.1.2Global10

6.1.2Module specific Lookup Tables Constants10

7Software Module Implementation12

7.1Sub-Module Functions12

7.1.1Initialization Functions12

7.1.1.1INIT: PolarityCfgInit12

7.1.1.1.1Design Rationale12

7.1.1.1.2Module Outputs12

7.1.1.1.3Module Internal12

7.1.2PERIODIC FUNCTIONS12

7.1.3Interrupt Functions12

7.1.4Server runnables13

7.1.4.1PolarityCfgRead13

7.1.4.1.1Design Rationale13

7.1.4.1.2Store Module Inputs to Local copies13

7.1.4.1.3(Processing of function)………13

7.1.4.1.4Store Local copy of outputs into Module Outputs13

7.1.4.2PolarityCfgWr13

7.1.4.2.1Design Rationale13

7.1.4.2.2Store Module Inputs to Local copies13

7.1.4.2.3(Processing of function)………13

7.1.4.2.4Store Local copy of outputs into Module Outputs13

7.1.5Local Function/Macro Definitions13

7.1.5.1Local Function #113

7.1.5.2Description13

7.1.6GLObAL Function/Macro Definitions13

7.1.7Tranisition FUNCTIONS14

8Known Limitations With Design15

9UNIT TEST CONSIDERATION16

10Appendix17

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

| 4 | FDD  –   ES 102 A_ PolarityCfg _Design | See Synergy  sub  project version |

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

FDD – ES102A_PolarityCfg_Design

See Synergy sub project version

## Power Disconnect High-Level Description

This function will identify polarity control settings for certain points in the design.

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

| HWAG0POL_CNT_U32 | Bitfield Mask | NA | 0x00000001U |

| HWAG1POL_CNT_U32 | Bitfield Mask | NA | 0x00000002U |

| HWAG2POL_CNT_U32 | Bitfield Mask | NA | 0x00000004U |

| HWAG3POL_CNT_U32 | Bitfield Mask | NA | 0x00000008U |

| HWAG4POL_CNT_U32 | Bitfield Mask | NA | 0x00000010U |

| HWAG5POL_CNT_U32 | Bitfield Mask | NA | 0x00000020U |

| HWAG6POL_CNT_U32 | Bitfield Mask | NA | 0x00000040U |

| HWAG7POL_CNT_U32 | Bitfield Mask | NA | 0x00000080U |

| HWTQ0POL_CNT_U32 | Bitfield Mask | NA | 0x00000100U |

| HWTQ1POL_CNT_U32 | Bitfield Mask | NA | 0x00000200U |

| HWTQ2POL_CNT_U32 | Bitfield Mask | NA | 0x00000400U |

| HWTQ3POL_CNT_U32 | Bitfield Mask | NA | 0x00000800U |

| HWTQ4POL_CNT_U32 | Bitfield Mask | NA | 0x00001000U |

| HWTQ5POL_CNT_U32 | Bitfield Mask | NA | 0x00002000U |

| HWTQ6POL_CNT_U32 | Bitfield Mask | NA | 0x00004000U |

| HWTQ7POL_CNT_U32 | Bitfield Mask | NA | 0x00008000U |

| MOTAGMECL0POL_CNT_U32 | Bitfield Mask | NA | 0x00010000U |

| MOTAGMECL1POL_CNT_U32 | Bitfield Mask | NA | 0x00020000U |

| MOTAGMECL2POL_CNT_U32 | Bitfield Mask | NA | 0x00040000U |

| MOTAGMECL3POL_CNT_U32 | Bitfield Mask | NA | 0x00080000U |

| MOTAGMECL4POL_CNT_U32 | Bitfield Mask | NA | 0x00100000U |

| MOTAGMECL5POL_CNT_U32 | Bitfield Mask | NA | 0x00200000U |

| MOTAGMECL6POL_CNT_U32 | Bitfield Mask | NA | 0x00400000U |

| MOTAGMECL7POL_CNT_U32 | Bitfield Mask | NA | 0x00800000U |

| MOTELECMECLPOL_CNT_U32 | Bitfield Mask | NA | 0x01000000U |

| ASSIMECHPOL_CNT_U32 | Bitfield Mask | NA | 0x02000000U |

Constant Name

Resolution

Units

Value

HWAG0POL_CNT_U32

Bitfield Mask

NA

0x00000001U

HWAG1POL_CNT_U32

Bitfield Mask

NA

0x00000002U

HWAG2POL_CNT_U32

Bitfield Mask

NA

0x00000004U

HWAG3POL_CNT_U32

Bitfield Mask

NA

0x00000008U

HWAG4POL_CNT_U32

Bitfield Mask

NA

0x00000010U

HWAG5POL_CNT_U32

Bitfield Mask

NA

0x00000020U

HWAG6POL_CNT_U32

Bitfield Mask

NA

0x00000040U

HWAG7POL_CNT_U32

Bitfield Mask

NA

0x00000080U

HWTQ0POL_CNT_U32

Bitfield Mask

NA

0x00000100U

HWTQ1POL_CNT_U32

Bitfield Mask

NA

0x00000200U

HWTQ2POL_CNT_U32

Bitfield Mask

NA

0x00000400U

HWTQ3POL_CNT_U32

Bitfield Mask

NA

0x00000800U

HWTQ4POL_CNT_U32

Bitfield Mask

NA

0x00001000U

HWTQ5POL_CNT_U32

Bitfield Mask

NA

0x00002000U

HWTQ6POL_CNT_U32

Bitfield Mask

NA

0x00004000U

HWTQ7POL_CNT_U32

Bitfield Mask

NA

0x00008000U

MOTAGMECL0POL_CNT_U32

Bitfield Mask

NA

0x00010000U

MOTAGMECL1POL_CNT_U32

Bitfield Mask

NA

0x00020000U

MOTAGMECL2POL_CNT_U32

Bitfield Mask

NA

0x00040000U

MOTAGMECL3POL_CNT_U32

Bitfield Mask

NA

0x00080000U

MOTAGMECL4POL_CNT_U32

Bitfield Mask

NA

0x00100000U

MOTAGMECL5POL_CNT_U32

Bitfield Mask

NA

0x00200000U

MOTAGMECL6POL_CNT_U32

Bitfield Mask

NA

0x00400000U

MOTAGMECL7POL_CNT_U32

Bitfield Mask

NA

0x00800000U

MOTELECMECLPOL_CNT_U32

Bitfield Mask

NA

0x01000000U

ASSIMECHPOL_CNT_U32

Bitfield Mask

NA

0x02000000U

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

PolarityCfgInit

### INIT: PolarityCfgInit

### Design Rationale

Design follows implemenetation in FDD.

### Module Outputs

Refer ‘PolarityCfgInit’ block in FDD

### Module Internal

None

### PERIODIC FUNCTIONS

None

### Interrupt Functions

None

### Server runnables

### PolarityCfgRead

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer ‘PolarityCfgRead’ block in FDD

### Store Local copy of outputs into Module Outputs

None

### PolarityCfgWr

### Design Rationale

None

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer  ‘PolarityCfgWr’ block in FDD

### Store Local copy of outputs into Module Outputs

None

### Local Function/Macro Definitions

### Local Function #1

| Function Name | GetPolarity | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Polarity_Cnt_T_u32 | uint32 | 0 | 0xFFFFFFFF |

|  | PolarityMask_Cnt_T_u32 | uint32 | 0 x00000001 | 0x0 2 000000 |

| Return Value | Polarity_Cnt_T_s08 | sint08 | -1 | 1 |

Function Name

GetPolarity

Type

Min

Max

Arguments Passed

Polarity_Cnt_T_u32

uint32

0

0xFFFFFFFF

PolarityMask_Cnt_T_u32

uint32

0x00000001

0x02000000

Return Value

Polarity_Cnt_T_s08

sint08

-1

1

### Description

Design:

if ( (Polarity_Cnt_T_u32 & PolarityMask_Cnt_T_u32) == PolarityMask_Cnt_T_u32 )

set  ‘Polarity_Cnt_T_s08’ to ‘1’

else

set  ‘Polarity_Cnt_T_s08’ to ‘-1’

Note:  ‘PolarityMask_Cnt_T_u32’ is a bit field mask and takes values mentioned in table at sec 6.1.1.1

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

Back to [Complex Device Drivers](../).
