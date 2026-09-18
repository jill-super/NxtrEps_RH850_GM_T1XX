---
title: "Verify Critical Registers (CM111A_VrfyCritReg)"
description: "Verify Critical Registers: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Verify Critical Registers component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM111A_VrfyCritReg_Design` | Design package |
| `CM111A_VrfyCritReg_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM111A_VrfyCritReg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM111A_VrfyCritReg_Impl` |  |
| C sources | `CDD_VrfyCritReg.c` |
| Public headers | `CDD_VrfyCritReg.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CDD_VrfyCritReg_bswmd.arxml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `VrfyCritReg.dcf`, `VrfyCritReg_attr_def.xml` |
| Generator output | `CDD_VrfyCritReg_Cfg.c.tt`, `CDD_VrfyCritReg_Cfg_private.h.tt`, `CDD_VrfyCritReg_Generate.bat`, `CDD_VrfyCritReg_helper.tt` |
| Tooling and integration scripts | `CM111A_VrfyCritReg_Impl.gpj`, `CreateGHSProject.bat`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM111A_VrfyCritReg_Impl/autosar/CDD_VrfyCritReg_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM111A_VrfyCritReg_Impl/src/CDD_VrfyCritReg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM111A_VrfyCritReg.doc`

- **Source path in repository:** `CM111A_VrfyCritReg_Design/Design/CM111A_VrfyCritReg.doc`
- **Format:** `.doc`
- **Size:** `104 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM111A_VrfyCritReg_DDReport.txt`

- **Source path in repository:** `CM111A_VrfyCritReg_Design/Reports/CM111A_VrfyCritReg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM111A_VrfyCritReg_DataDict
25-Apr-2016 12:42:42
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
Missing Model 	Unable to find model for comparison to data dictionary.
(errors:  1)

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
SetNtcSts                   	.Description: 	Field is empty.
(variables: 1, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 0, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 0, errors: 0)

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
(variables: 6, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
```
*... truncated (33 more lines in the source file). ...*

### `VrfyCritReg_IntegrationManual.doc`

- **Source path in repository:** `CM111A_VrfyCritReg_Impl/doc/VrfyCritReg_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `153 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `VrfyCritReg_MDD.docx`

- **Source path in repository:** `CM111A_VrfyCritReg_Impl/doc/VrfyCritReg_MDD.docx`
- **Format:** `.docx`
- **Size:** `104 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

VrfyCritReg

Apr 14, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Selva Sengottaiyan

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1 | 14 - Jan -201 6 |

| Updated to “ Critical register” checks at  init  and periodic functions | Selva   Sengottaiyan | 2 | 14-Apr-2016 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

14-Jan-2016

Updated to “ Critical register” checks at init and periodic functions

Selva Sengottaiyan

2

14-Apr-2016

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2VrfyCritReg High-Level Description6

3Design details of software module7

3.1Graphical representation of VrfyCritReg7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: VrfyCritRegInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: VrfyCritRegPer19

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions9

5.4.1Local Function #29

5.4.1.1Description9

5.5GLOBAL Function/Macro Definitions10

6Known Limitations with Design11

7UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## Introduction

### Purpose

### Scope

## VrfyCritReg High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of VrfyCritReg

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

Refer .m file

#### Local Constants

| Constant Name | Data Type | Value |

| --- | --- | --- |

| SYSCRITREGFLT_CNT_U08 | uint8 | 2 |

| CRITREGFLT_CNT_U08 | uint8 | 1 |

| NOFLT_CNT_U08 | uint8 | 0 |

|  |  |  |

|  |  |  |

|  |  |  |

|  |  |  |

Constant Name

Data Type

Value

SYSCRITREGFLT_CNT_U08

uint8

2

CRITREGFLT_CNT_U08

uint8

1

NOFLT_CNT_U08

uint8

0

## Software Component Implementation

### Sub-Module Functions

### Init: VrfyCritRegInit1

### Design Rationale

Refer FDD

### Module Outputs

None

### Per: VrfyCritRegPer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

None

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | SysCritReg <Register Short Name > IninChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | & SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |

Function Name

SysCritReg<Register Short Name>IninChk

Type

Min

Max

Arguments Passed

NA

Return Value

&SysRegsOk_Uls_T_lgc

boolean

FALSE

TRUE

### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### Local Function #2

| Function Name | SysCritReg <Register Short Name > Per Chk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | & SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |

Function Name

SysCritReg<Register Short Name>PerChk

Type

Min

Max

Arguments Passed

NA

Return Value

&SysRegsOk_Uls_T_lgc

boolean

FALSE

TRUE

### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### Local Function #2

| Function Name | SvCritRegChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | SysRegsOk_Uls_T_lgc | Boolean | FALSE | TRUE |

Function Name

SvCritRegChk

Type

Min

Max

Arguments Passed

NA

Return Value

SysRegsOk_Uls_T_lgc

Boolean

FALSE

TRUE

### Description

Set 'SysRegsOk_Uls_T_lgc' to 'FALSE' if CPU System Register values are not equal  to  expected values. This is configured as a trusted function because it needs to run in supervisor mode

### GLOBAL Function/Macro Definitions

### Global Function #1

| Function Name | CritRegPerChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | NtcParamInfo_Cnt_T_u08 | uint8 | 0 U | 2U |

Function Name

CritRegPerChk

Type

Min

Max

Arguments Passed

NA

Return Value

NtcParamInfo_Cnt_T_u08

uint8

0U

2U

### Description

Set ' NtcParamInfo_Cnt_T_u08 to 1 if CPU Non System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 2 if CPU System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 0 if none of the above conditions are true.  This is configured as a trusted function because it needs to run in supervisor mode

### Global Function #2

| Function Name | CritReg Init Chk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | NtcParamInfo_Cnt_T_u08 | uint8 | 0U | 2U |

Function Name

CritRegInitChk

Type

Min

Max

Arguments Passed

NA

Return Value

NtcParamInfo_Cnt_T_u08

uint8

0U

2U

### Description

Set ' NtcParamInfo_Cnt_T_u08 to 1 if CPU Non System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 2 if CPU System Register values are not equal to expected values. Set ' NtcParamInfo_Cnt_T_u08 to 0 if none of the above conditions are true.  This is configured as a trusted function because it needs to run in supervisor mode

### Global Function #3

| Function Name | SysCritRegIninChk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |

Function Name

SysCritRegIninChk

Type

Min

Max

Arguments Passed

NA

Return Value

SysRegsOk_Uls_T_lgc

boolean

FALSE

TRUE

### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

### Global Function #4

| Function Name | SysCritReg Per Chk | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | NA |  |  |  |

| Return Value | SysRegsOk_Uls_T_lgc | boolean | FALSE | TRUE |

Function Name

SysCritRegPerChk

Type

Min

Max

Arguments Passed

NA

Return Value

SysRegsOk_Uls_T_lgc

boolean

FALSE

TRUE

### Description

Set ' SysRegsOk_Uls_T_lgc to FALSE if CPU System Register values are not equal to expected values.  This is configured to be called from trusted function because it needs to run in supervisor mode

## Known Limitations with Design

## UNIT TEST CONSIDERATION

None

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

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0. 01 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  CM111A_ VrfyCritReg _Design | See Synergy sub project version |

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

EA4 01.00.01

4

Software Design and Coding Standards.doc

2.1

5

FDD : CM111A_VrfyCritReg_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
