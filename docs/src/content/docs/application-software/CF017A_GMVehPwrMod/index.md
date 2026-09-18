---
title: "General Motors Vehicle Power Mode (CF017A_GMVehPwrMod)"
description: "General Motors Vehicle Power Mode: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Vehicle Power Mode component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `CF017A_GMVehPwrMod_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF017A_GMVehPwrMod_Impl` |  |
| C sources | `GmVehPwrMod.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmVehPwrMod.dcf`, `GmVehPwrMod_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF017A_GMVehPwrMod_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmVehPwrMod.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF017A_GMVehPwrMod_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF017A_GMVehPwrMod_Impl/src/GmVehPwrMod.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `GmVehPwrMod_IntegrationManual.doc`

- **Source path in repository:** `CF017A_GMVehPwrMod_Impl/doc/GmVehPwrMod_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `136 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmVehPwrMod_MDD.docx`

- **Source path in repository:** `CF017A_GMVehPwrMod_Impl/doc/GmVehPwrMod_MDD.docx`
- **Format:** `.docx`
- **Size:** `123 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmVehPwrMod

VERSION:6.0

Dec 13, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser

Saginaw, MI, USA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | N. Saxton | 1.0 | 28 -Sep-2015 |

| Updated with new graphical representation and local function | N. Saxton | 2.0 | 01-Oct-2015 |

| New graphical representation | N. Saxton | 3.0 | 12-Nov-2015 |

| Changes to local constants and functions | N. Saxton | 4.0 | 15-Apr-2016 |

| Updated  as  per design rev. 2.1.0 | TATA | 5.0 | 22-Nov-2016 |

| Updated as per design rev. 2.2.0 /2.3.0  and to fix Anomaly EA4#8982 | M. Leser | 6.0 | 13-Dec-2016 |

Description

Author

Version

Date

Initial Version

N. Saxton

1.0

28-Sep-2015

Updated with new graphical representation and local function

N. Saxton

2.0

01-Oct-2015

New graphical representation

N. Saxton

3.0

12-Nov-2015

Changes to local constants and functions

N. Saxton

4.0

15-Apr-2016

Updated as per design rev. 2.1.0

TATA

5.0

22-Nov-2016

Updated as per design rev. 2.2.0/2.3.0 and to fix Anomaly EA4#8982

M. Leser

6.0

13-Dec-2016

Table of Contents

1GmVehPwrMod & High-Level Description5

2Design details of software module6

2.1Graphical representation of GmVehPwrMod6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Per: GmVehPwrModPer18

4.1.1.1Design Rationale8

4.1.1.2Store Module Inputs to Local copies8

4.1.1.3(Processing of function)………8

4.1.1.4Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Design Rationale9

4.4.1.2Created to reduce static path count and cyclomatic complexity of periodic function. Processing9

4.4.2Local Function #29

4.4.2.1Design Rationale9

4.4.2.2Processing9

4.4.3Local Function #39

4.4.3.1Design Rationale9

4.4.3.2Processing9

4.5GLOBAL Function/Macro Definitions9

5Known Limitations with Design10

6UNIT TEST CONSIDERATION11

Appendix AAbbreviations and Acronyms12

Appendix BGlossary13

Appendix CReferences14

## GmVehPwrMod & High-Level Description

This GM specific function runs periodically to determine whether to enable assist (if not previously enabled) or to disable assist based on the inputs provided to the function.

## Design details of software module

### Graphical representation of GmVehPwrMod

### Data Flow Diagram

Refer FDD

#### Component level DFD

Refer FDD

#### Function level DFD

Refer FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Units | Value |

| --- | --- | --- |

| LOOKUPTBLSIZE_CNT_U16 | CNT | 512 |

| Refer .m file for other constants | N/A | N/A |

Constant Name

Units

Value

LOOKUPTBLSIZE_CNT_U16

CNT

512

Refer .m file for other constants

N/A

N/A

## Software Component Implementation

### Sub-Module Functions

### Per: GmVehPwrModPer1

### Design Rationale

None

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | GetTblIdx | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | GetGpioMcuEna_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | SysPwrModRun_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | EngRunActv_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehSpdAssiKeepMin_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | PrpnSysActvMsgInvld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VehSpdSnsrVld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | SysPwrModMsgInvld_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | BusOffHiSpd_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | HwTq_HwNwtMtr_T_f32 | Float32 | -10 | 10 |

| Output | TblIdxNr_Cnt_T_u16 | Uint16 | 0 | 511 |

Function Name

GetTblIdx

Type

Min

Max

Arguments Passed

GetGpioMcuEna_Cnt_T_logl

Boolean

FALSE

TRUE

SysPwrModRun_Cnt_T_logl

Boolean

FALSE

TRUE

EngRunActv_Cnt_T_logl

Boolean

FALSE

TRUE

VehSpdAssiKeepMin_Cnt_T_logl

Boolean

FALSE

TRUE

PrpnSysActvMsgInvld_Cnt_T_logl

Boolean

FALSE

TRUE

VehSpdSnsrVld_Cnt_T_logl

Boolean

FALSE

TRUE

SysPwrModMsgInvld_Cnt_T_logl

Boolean

FALSE

TRUE

BusOffHiSpd_Cnt_T_logl

Boolean

FALSE

TRUE

HwTq_HwNwtMtr_T_f32

Float32

-10

10

Output

TblIdxNr_Cnt_T_u16

Uint16

0

511

### Design Rationale

Created to reduce static path count and cyclomatic complexity of periodic function. Processing

Refer FDD

### Local Function #2

| Function Name | GetMotTqCmdSca | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | AssiEna_Cnt_T_logl | Boolean | FALSE | TRUE |

| Output | MotTqCmdSca_Cnt_T_f32 | Boolean | 0.0 | 1.0 |

Function Name

GetMotTqCmdSca

Type

Min

Max

Arguments Passed

AssiEna_Cnt_T_logl

Boolean

FALSE

TRUE

Output

MotTqCmdSca_Cnt_T_f32

Boolean

0.0

1.0

### Design Rationale

Created to reduce static path count and cyclomatic complexity of periodic function.

### Processing

Sets MotTqCmdSca to 1.0 if AssiEna is TRUE and sets it to 0.0 otherwise.

### Local Function #3

| Function Name | KeepAssiHwTqTmr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | HwTq_HwNwtMtr_T_f32 | Float32 | -10 | 10 |

|  | *   TblIdxNr_Cnt_T_u16 | Uint16 | 0 | 511 |

Function Name

KeepAssiHwTqTmr

Type

Min

Max

Arguments Passed

HwTq_HwNwtMtr_T_f32

Float32

-10

10

* TblIdxNr_Cnt_T_u16

Uint16

0

511

### Design Rationale

Created to reduce static path count and cyclomatic complexity of local function #2.

*TblIdxNr_Cnt_T_u16 is an output of this function.

### Processing

Refer ‘KeepAssi_HwTqTmr’ block in model.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

None

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

| 1 | AUTOSAR Specification of Memory Mapping (Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4  04.02.01 |

| 3 | EA4  Software Naming Conventions.doc | 04.02.01 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD:  CF01 7A_GmVehPwrMod _Design | See Synergy subproject version |

Ref. #

Title

Version

1

AUTOSAR Specification of Memory Mapping (Link:AUTOSAR_SWS_MemoryMapping.pdf)

v1.3.0 R4.0 Rev 2

2

MDD Guideline

EA4 04.02.01

3

EA4 Software Naming Conventions.doc

04.02.01

4

Software Design and Coding Standards.doc

2.1

5

FDD: CF017A_GmVehPwrMod_Design

See Synergy subproject version

Back to [Application Software](../).
