---
title: "General Motors Vehicle Speed Arbitration (CF016A_GMVehSpdArbn)"
description: "General Motors Vehicle Speed Arbitration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors Vehicle Speed Arbitration component belongs to **Customer Functions (General Motors)** in the **Application Software** layer. It implements a vehicle-level customer function required by General Motors as an AUTOSAR software component.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `CF016A_GMVehSpdArbn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CF016A_GMVehSpdArbn_Impl` |  |
| C sources | `GmVehSpdArbn.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GmVehSpdArbn.dcf`, `GmVehSpdArbn_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CF016A_GmVehSpdArbn_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `GmVehSpdArbn.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CF016A_GMVehSpdArbn_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CF016A_GMVehSpdArbn_Impl/src/GmVehSpdArbn.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `GmVehSpdArbn_IntegrationManual.doc`

- **Source path in repository:** `CF016A_GMVehSpdArbn_Impl/doc/GmVehSpdArbn_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GmVehSpdArbn_MDD.docx`

- **Source path in repository:** `CF016A_GMVehSpdArbn_Impl/doc/GmVehSpdArbn_MDD.docx`
- **Format:** `.docx`
- **Size:** `147 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GmVehSpdArbn

March 15, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Nick Saxton,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | N. Saxton | 1.0 | 03-Sep-2015 |

| Updated graphical representation | N. Saxton | 2.0 | 12-Nov-2015 |

| Added  Init  function to sub-module functions and  Updated graphical representation for addition of timer functions | N. Saxton | 3.0 | 15-Mar-2016 |

Description

Author

Version

Date

Initial Version

N. Saxton

1.0

03-Sep-2015

Updated graphical representation

N. Saxton

2.0

12-Nov-2015

Added Init function to sub-module functions and Updated graphical representation for addition of timer functions

N. Saxton

3.0

15-Mar-2016

Table of Contents

1GmVehSpdArbn High-Level Description5

2Design details of software module6

2.1Graphical representation of GmVehSpdArbn6

2.2Data Flow Diagram6

2.2.1Component level DFD6

2.2.2Function level DFD6

3Constant Data Dictionary7

3.1Program (fixed) Constants7

3.1.1Embedded Constants7

4Software Component Implementation8

4.1Sub-Module Functions8

4.1.1Per: GmVehSpdArbnPer18

4.1.1.1Design Rationale8

4.1.1.2Store Module Inputs to Local copies8

4.1.1.3(Processing of function)………8

4.1.1.4Store Local copy of outputs into Module Outputs8

4.1.2Init: GmVehSpdArbnInit18

4.1.2.1Design Rationale8

4.1.2.2Store Module Inputs to Local copies8

4.1.2.3(Processing of function)………8

4.1.2.4Store Local copy of outputs into Module Outputs8

4.2Server Runables8

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.4.1Local Function #18

4.4.1.1Design Rationale9

4.4.1.2Processing9

4.4.2Local Function #29

4.4.2.1Design Rationale9

4.4.2.2Processing9

4.4.3Local Function #39

4.4.3.1Design Rationale9

4.4.3.2Processing9

4.4.4Local Function #49

4.4.4.1Design Rationale10

4.4.4.2Processing10

4.4.5Local Function #510

4.4.5.1Design Rationale10

4.4.5.2Processing10

4.5GLOBAL Function/Macro Definitions10

5Known Limitations with Design11

6UNIT TEST CONSIDERATION12

Appendix AAbbreviations and Acronyms13

Appendix BGlossary14

Appendix CReferences15

## GmVehSpdArbn High-Level Description

This GM specific function determines how EPS shall calculate Secure Vehicle Speed, Non-Secure Vehicle Speed, and how to arbitrate between those signals in addition to a serial communication supplied vehicle speed signal.

## Design details of software module

### Graphical representation of GmVehSpdArbn

### Data Flow Diagram

Simulink model being created for component in near future

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Refer DataDict.m file.

## Software Component Implementation

### Sub-Module Functions

The sub-module functions are grouped based on similar functionality that needs to be executed in a given “State” of the system (refer States and Modes).  For a given module, the MDD will identify the type and number of sub-modules required.  The sub-module types are described below.

### Per: GmVehSpdArbnPer1

### Design Rationale

Simulink model being created for component in near future

### Store Module Inputs to Local copies

### (Processing of function)………

### Store Local copy of outputs into Module Outputs

### Init: GmVehSpdArbnInit1

### Design Rationale

Simulink model being created for component in near future

### Store Module Inputs to Local copies

### (Processing of function)………

### Store Local copy of outputs into Module Outputs

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | DetVld | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VldSig1 _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VldSig2_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | Stuck Sig1 _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | StuckSig2_Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | OverallVld _Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

DetVld

Type

Min

Max

Arguments Passed

VldSig1_Cnt_T_logl

Boolean

FALSE

TRUE

VldSig2_Cnt_T_logl

Boolean

FALSE

TRUE

StuckSig1_Cnt_T_logl

Boolean

FALSE

TRUE

StuckSig2_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

OverallVld_Cnt_T_logl

Boolean

FALSE

TRUE

### Design Rationale

Created to reduce static path count and avoid repeated code.

### Processing

This function checks to see if at least one of the input valid signals is FALSE (invalid) or input stuck signals is TRUE (stuck) , returning an overall validity (OverallVld) of FALSE (invalid) if so, and TRUE (valid) otherwise.

### Local Function #2

| Function Name | DetInvld | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VldSig1 _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VldSig2 _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VldSig3 _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VldSig4 _Cnt_T_logl | Boolean | FALSE | TRUE |

| Return Value | OverallInv ld _Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

DetInvld

Type

Min

Max

Arguments Passed

VldSig1_Cnt_T_logl

Boolean

FALSE

TRUE

VldSig2_Cnt_T_logl

Boolean

FALSE

TRUE

VldSig3_Cnt_T_logl

Boolean

FALSE

TRUE

VldSig4_Cnt_T_logl

Boolean

FALSE

TRUE

Return Value

OverallInvld_Cnt_T_logl

Boolean

FALSE

TRUE

### Design Rationale

Created to reduce static path count and avoid repeated code.

### Processing

This function checks to see if all of the input signals (VldSig1 – 4) are FALSE (invalid), returning an overall invalidity (OverallInvld) of TRUE (invalid) if so, and FALSE (valid) otherwise.

### Local Function #3

| Function Name | UpdtAvg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VldSig _Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VelSig _Kph_T_f32 | Float32 | 0.0 | 511.0 |

|  | *AvgSum_Kph_T_f32 | Float32 | 0.0 | 2044.0 |

|  | *AvgCnt_Cnt_T_f32 | Float32 | 0.0 | 4.0 |

Function Name

UpdtAvg

Type

Min

Max

Arguments Passed

VldSig_Cnt_T_logl

Boolean

FALSE

TRUE

VelSig_Kph_T_f32

Float32

0.0

511.0

*AvgSum_Kph_T_f32

Float32

0.0

2044.0

*AvgCnt_Cnt_T_f32

Float32

0.0

4.0

### Design Rationale

Created to reduce static path count and avoid repeated code

* AvgSum and AvgCnt are outputs of this function

### Processing

This function adds the velocity signal input (VelSig) to the average sum (AvgSum) and increments the average count (AvgCnt) if the input signal is valid (VldSig).

### Local Function #4

| Function Name | CondMax | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VldSig_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VelSig 1 _Kph_T_f32 | Float32 | 0.0 | 511.0 |

|  | VelSig2_Kph_T_f32 | Float32 | 0.0 | 511.0 |

|  | * MaxVel_Kph_T_f32 | Float32 | 0.0 | 511.0 |

Function Name

CondMax

Type

Min

Max

Arguments Passed

VldSig_Cnt_T_logl

Boolean

FALSE

TRUE

VelSig1_Kph_T_f32

Float32

0.0

511.0

VelSig2_Kph_T_f32

Float32

0.0

511.0

*MaxVel_Kph_T_f32

Float32

0.0

511.0

### Design Rationale

Created to reduce static path count and avoid repeated code.

* MaxVel_Kph_T_f32 is an output of this function

### Processing

This function sets max velocity (MaxVel) to the maximum of the previous value of max velocity, velocity signal 1 (VelSig1), and velocity signal 2 (VelSig2) given that the valid signal condition (VldSig) is TRUE (valid).

### Local Function #5

| Function Name | CondMin | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | VldSig_Cnt_T_logl | Boolean | FALSE | TRUE |

|  | VelSig1_Kph_T_f32 | Float32 | 0.0 | 511.0 |

|  | VelSig2_Kph_T_f32 | Float32 | 0.0 | 511.0 |

|  | *MinVel_Kph_T_f32 | Float32 | 0.0 | 511.0 |

Function Name

CondMin

Type

Min

Max

Arguments Passed

VldSig_Cnt_T_logl

Boolean

FALSE

TRUE

VelSig1_Kph_T_f32

Float32

0.0

511.0

VelSig2_Kph_T_f32

Float32

0.0

511.0

*MinVel_Kph_T_f32

Float32

0.0

511.0

### Design Rationale

Created to reduce static path count and avoid repeated code.

* MinVel_Kph_T_f32 is an output of this function

### Processing

This function sets minimum velocity (MinVel) to the minimum of the previous value of minimum velocity, velocity signal 1 (VelSig1), and velocity signal 2 (VelSig2), given that VldSig is TRUE.

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

Simulink model being created for component in near future

## UNIT TEST CONSIDERATION

Simulink model being created for component in near future

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

| 3 | EA4  Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | CF016A_GmVehSpdArbn_Design | See Synergy subproject version |

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

EA4 Software Naming Conventions.doc

01.00.00

4

Software Design and Coding Standards.doc

2.1

5

CF016A_GmVehSpdArbn_Design

See Synergy subproject version

Back to [Application Software](../).
