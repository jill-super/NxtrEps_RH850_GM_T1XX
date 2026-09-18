---
title: "Calibration Protocol Interface (ES104A_XcpIf)"
description: "Calibration Protocol Interface: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Calibration Protocol Interface component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `ES104A_XcpIf_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES104A_XcpIf_Impl` |  |
| C sources | `CDD_XcpIf.c` |
| Public headers | `CDD_XcpIf.h`, `CDD_XcpIf_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `CDD_XcpIf.dcf`, `CDD_XcpIf_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CDD_XcpIf.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES104A_XcpIf_Impl.gpj`, `RteGen.bat`, `XcpIf.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES104A_XcpIf_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES104A_XcpIf_Impl/src/CDD_XcpIf.c`. 

Top-level functions defined in `CDD_XcpIf.c` (factual extract, first 14):

- `ApplXcpGetTimestamp`
- `ApplXcpGetPointer`
- `ApplXcpCalibrationWrite`
- `ApplXcpWrCmn`
- `ApplXcpCalibrationRead`
- `ApplXcpCheckWriteAccess`
- `ApplXcpCheckReadAccess`
- `ApplXcpCheckDAQAccess`
- `ApplXcpGetCalPage`
- `ApplXcpCopyCalPage`
- `ApplXcpUserService`
- `ApplXcpOpenCmdIf`
- `NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper`
- `NONTRUSTED_NtWrapS_Rte_Call_SetCalPageReq_Oper`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `XcpIf Integration Manual.docx`

- **Source path in repository:** `ES104A_XcpIf_Impl/doc/XcpIf Integration Manual.docx`
- **Format:** `.docx`
- **Size:** `81 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

**Converted content:**

Integration Manual

For

XCP Interface (XcpIf)

VERSION: 2.0

DATE: 09-Oct-2015

Prepared By:

Kevin Smith

ESG Software,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date | Approved By |

| --- | --- | --- | --- | --- | --- |

| 1 | Initial version | K. Smith | 1.0 | 6-Jun-15 |  |

| 2 | Updates for  intial   online calibration support | K. Smith | 2.0 | 9-Oct-15 |  |

Sl. No.

Description

Author

Version

Date

Approved By

1

Initial version

K. Smith

1.0

6-Jun-15

2

Updates for intial online calibration support

K. Smith

2.0

9-Oct-15

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

4.6OS Configuration Changes7

5Integration  DATAFLOW REQUIREMENTS8

5.1Required Global Data Inputs8

5.2Required Global Data Outputs8

5.3Specific Include Path present8

5.4Other Header Changes8

6Runnable Scheduling9

7Memory Map REQUIREMENTS10

7.1Mapping10

7.2Usage10

7.3NvM Blocks10

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

| 1 | MDD Guidelines | Process 0 4 .0 2 .0 0 |

| 2 | Software Naming Conventions | Process 04.02.00 |

| 3 | Coding  standards | Process 04.02.00 |

| 4 | FDD | Not available |

|  | <Add if more available> |  |

Sr. No.

Title

Version

1

MDD Guidelines

Process 04.02.00

2

Software Naming Conventions

Process 04.02.00

3

Coding standards

Process 04.02.00

4

FDD

Not available

<Add if more available>

## Dependencies

### SWCs

| Module | Required Feature |

| --- | --- |

| None |  |

Module

Required Feature

None

Note : Referencing the external components should be avoided in most cases. Only in unavoidable circumstance external components should be referred. Developer should track the references.

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

### OS Configuration Changes

| Trusted Function | Parameters | Notes |

| --- | --- | --- |

| ApplXcpWrCmn | MTABYTEPTR  addr vuint8 size const   BYTEPTR data | This function should be defined as trusted. |

| Rte_Call_SetCalPageReq_Oper |  | This function shall be defined as a non-trusted function call to the application that  TunSelnMngt  is integrated. |

| Rte_Call_CopyCalPageReq_Oper |  | This function shall be defined as a non-trusted function call to the application that  TunSelnMngt  is integrated. |

Trusted Function

Parameters

Notes

ApplXcpWrCmn

MTABYTEPTR addr

vuint8 size

const BYTEPTR data

This function should be defined as trusted.

Rte_Call_SetCalPageReq_Oper

This function shall be defined as a non-trusted function call to the application that TunSelnMngt is integrated.

Rte_Call_CopyCalPageReq_Oper

This function shall be defined as a non-trusted function call to the application that TunSelnMngt is integrated.

## Integration  DATAFLOW REQUIREMENTS

### Required Global Data Inputs

None

### Required Global Data Outputs

None

### Specific Include Path present

Yes

### Other Header Changes

| File | Change | Reason |

| --- | --- | --- |

| usrostyp.h | Add include statement for  CDD_XcpIf.h | The  include  is needed since for the OS has the function prototypes and datatypes required for the trusted function call. |

File

Change

Reason

usrostyp.h

Add include statement for CDD_XcpIf.h

The include is needed since for the OS has the function prototypes and datatypes required for the trusted function call.

## Runnable Scheduling

This section specifies the required runnable scheduling.

| Init | Scheduling Requirements | Trigger |

| --- | --- | --- |

| CDD_XcpIfInit | None | Rte |

Init

Scheduling Requirements

Trigger

CDD_XcpIfInit

None

Rte

| Runnable | Scheduling Requirements | Trigger |

| --- | --- | --- |

| Xcp2msDaq | 2ms | RTE |

Runnable

Scheduling Requirements

Trigger

Xcp2msDaq

2ms

RTE

## Memory Map REQUIREMENTS

### Mapping

| Memory Section | Contents | Notes |

| --- | --- | --- |

| None |  |  |

Memory Section

Contents

Notes

None

* Each …START_SEC… constant is terminated by a …STOP_SEC… constant as specified in the AUTOSAR Memory Mapping requirements.

### Usage

| Feature | RAM | ROM |

| --- | --- | --- |

| None |  |  |

Feature

RAM

ROM

None

Table 1: ARM Cortex R4 Memory Usage

### NvM Blocks

None

## Compiler Settings

### Preprocessor MACRO

The file xcp.cfg needs to have “#define XCP_ENABLE_CALIBRATION_MEM_ACCESS_BY_APPL” added. When the XCP component is generated in GENy, this will enable the application read/write calls.

The #defile XCPIF_MAXCALSEG_CNT_U08 points to a generated value by the Xcp component. Vector currently only allows one segment to be defined. This will have to be manually changed in the xcp.cfg file by the following:

#undef kXcpMaxSegment

#define kXcpMaxSegment  XX

XX is the number of tuning groups that are defined in your program.

### Optimization Settings

None

## Appendix

N/A

### `XcpIf_MDD.docx`

- **Source path in repository:** `ES104A_XcpIf_Impl/doc/XcpIf_MDD.docx`
- **Format:** `.docx`
- **Size:** `1131 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

XCP Interface (XcpIf)

VERSION: 2.0

DATE: 29-Aug-2016

Prepared By:

Kevin Smith

EPS Software,

Nexteer Automotive,

Saginaw, MI, USA

Location: The official version of this document is stored in the Nexteer Configuration Management System.

Revision History

| Sl. No. | Description | Author | Version | Date | Approved  By |

| --- | --- | --- | --- | --- | --- |

| 1 | Initial Version | K. Smith | 1.0 | 16 - Jun - 15 |  |

| 2 | Updates for anomaly EA4#6672 | K. Smith | 2.0 | 29-Aug-16 |  |

Sl. No.

Description

Author

Version

Date

Approved By

1

Initial Version

K. Smith

1.0

16-Jun-15

2

Updates for anomaly EA4#6672

K. Smith

2.0

29-Aug-16

Table of Contents

1Abbrevations And Acronyms5

2References6

3XCP Interface & High-Level Description7

4Design details of software module8

4.1Graphical representation of XCP Interface8

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

7Software Module Implementation11

7.1Sub-Module Functions11

7.2Initialization Functions11

7.3PERIODIC FUNCTIONS11

7.3.1Xcp2msDaq11

7.3.1.1Design Rationale11

7.3.1.2Store Module Inputs to Local copies11

7.3.1.3(Processing of function)………11

7.3.1.4Store Local copy of outputs into Module Outputs11

7.4Non PERIODIC FUNCTIONS11

7.5Interrupt Functions11

7.6Serial Communication Functions11

7.7Local Function/Macro Definitions11

7.8GLObAL Function/Macro Definitions11

7.8.1ApplXcpGetTimestamp11

7.8.1.1Description12

7.8.2ApplXcpGetPointer12

7.8.2.1Description12

7.8.3ApplXcpCalibrationWrite12

7.8.3.1Description12

7.8.4ApplXcpWrCmn13

7.8.4.1Description13

7.8.5ApplXcpCalibrationRead13

7.8.5.1Description13

7.9TRANSIENT FUNCTIONS13

8Unit Test Considerations14

9Known Limitations With Design15

10Appendix16

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| DFD | Design functional diagram |

| MDD | Module design Document |

|  | <ADD  more to the table if applicable> |

|  |  |

Abbreviation

Description

DFD

Design functional diagram

MDD

Module design Document

<ADD  more to the table if applicable>

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| < 1 > | < MDD Guidelines > | 4.0.0 |

| <2> | < Software Naming Conventions > | 4.0.0 |

| <3> | <Coding  standards > | 4.0.0 |

| <4> | <FDD > | Not available |

|  | <Add if more available> |  |

Sr. No.

Title

Version

<1>

<MDD Guidelines>

4.0.0

<2>

<Software Naming Conventions>

4.0.0

<3>

<Coding standards>

4.0.0

<4>

<FDD >

Not available

<Add if more available>

## XCP Interface & High-Level Description

XCP Interface provides multiple functions that allow XCP end users and tools to interface with software components contained in the application.

## Design details of software module

### Graphical representation of XCP Interface

None

### Data Flow Diagram

None

### Module level DFD

None

### Sub-Module level DFD

None

### COMPONENT FLOW DIAGRAM

None

## Variable Data Dictionary

### User defined typedef definition/declaration

| Typedef  Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

|  |  |  |  |  |

|  |  |  |  |  |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

### Variable definition for enumerated types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

|  |  |  |

Enum  Name

Element Name

Value

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

### Global

| Constant Name |

| --- |

| XcpEventChannel_2ms_DAQ_2 |

Constant Name

XcpEventChannel_2ms_DAQ_2

### Module specific Lookup Tables Constants

| Constant Name | Resolution | Value | Software Segment |

| --- | --- | --- | --- |

|  |  |  |  |

Constant Name

Resolution

Value

Software Segment

## Software Module Implementation

### Sub-Module Functions

None

### Initialization Functions

None

### PERIODIC FUNCTIONS

### Xcp2msDaq

### Design Rationale

This function is called every 2ms for executing the XcpEvent functions for the 2ms DAQ.

### Store Module Inputs to Local copies

None

### (Processing of function)………

### Store Local copy of outputs into Module Outputs

None

### Non PERIODIC FUNCTIONS

None

### Interrupt Functions

None

### Serial Communication Functions

None

### Local Function/Macro Definitions

None

### GLObAL Function/Macro Definitions

### ApplXcpGetTimestamp

| Function Name | ApplXcpGetTimestamp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value | Timestamp_Cnt_T_u32 | XcpDaqTimestampType | See description | See description |

Function Name

ApplXcpGetTimestamp

Type

Min

Max

Arguments Passed

None

Return Value

Timestamp_Cnt_T_u32

XcpDaqTimestampType

See description

See description

### Description

This function returns the timestamp that is based on a reference timer. The range of return values vary depending on the configuration of the Xcp Component. The data type can range from a full range of a uint8 to a uint32 value.

### ApplXcpGetPointer

| Function Name | ApplXcpGetPointer | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr_ext | vuint8 | 0 | 255 |

|  | addr | vuint32 | 1 | 4294967295 |

| Return Value | RtnAddr_Cnt_T_u32 | MTABYTEPTR | 1 | 4294967295 |

Function Name

ApplXcpGetPointer

Type

Min

Max

Arguments Passed

addr_ext

vuint8

0

255

addr

vuint32

1

4294967295

Return Value

RtnAddr_Cnt_T_u32

MTABYTEPTR

1

4294967295

### Description

This function takes the extension and address of and returns the physical address of the item.

### ApplXcpCalibrationWrite

| Function Name | ApplXcpCalibrationWrite | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | size | Vuint8 | 0 | 255 |

|  | data | BYTEPTR | 1 | 4294967295 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpCalibrationWrite

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

size

Vuint8

0

255

data

BYTEPTR

1

4294967295

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function calls the common XCP writing function. For this deisgn, the function call will be translated into a trusted function call.

### ApplXcpWrCmn

| Function Name | ApplXcpWrCmn | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | size | Vuint8 | 0 | 255 |

|  | data | BYTEPTR | 1 | 4294967295 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpWrCmn

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

size

Vuint8

0

255

data

BYTEPTR

1

4294967295

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function writes the data passed in by the XCP user to the designated address.

### ApplXcpCalibrationRead

| Function Name | ApplXcpCalibrationRead | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | size | Vuint8 | 0 | 255 |

|  | data | BYTEPTR | 1 | 4294967295 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpCalibrationRead

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

size

Vuint8

0

255

data

BYTEPTR

1

4294967295

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function reads the data in the designated address and returns it to the XCP user.

### ApplXcpCheckWriteAccess

| Function Name | ApplXcp CheckWriteAccess | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | Size_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpCheckWriteAccess

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

Size_Cnt_T_u08

Vuint8

0

255

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function checks access for XCP writes. Since the functions in tuning selection management handle the presmissions for writes, this function shall always return a positive response.

### ApplXcpCheckReadAccess

| Function Name | ApplXcp Check Read Access | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | Size_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpCheckReadAccess

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

Size_Cnt_T_u08

Vuint8

0

255

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function checks access for XCP reads. Since the functions in tuning selection management handle the presmissions for reads, this function shall always return a positive response.

### ApplXcpCheckDAQAccess

| Function Name | ApplXcp Check DAQ Access | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | addr | MTABYTEPTR | 1 | 4294967295 |

|  | Size_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0 |

Function Name

ApplXcpCheckDAQAccess

Type

Min

Max

Arguments Passed

addr

MTABYTEPTR

1

4294967295

Size_Cnt_T_u08

Vuint8

0

255

Return Value

XCP_CMD_OK

Uint8

0

0

### Description

This function checks access for XCP DAQ access. Since all reads are allowed, this function will also always return a positive response.

### ApplXcpSetCalPage

| Function Name | ApplXcp SetCalPage | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Seg_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | Page_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | Mod_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | Rtn_Cnt_T_u08 | Uint8 | 0 | 0x28 |

Function Name

ApplXcpSetCalPage

Type

Min

Max

Arguments Passed

Seg_Cnt_T_u08

Vuint8

0

255

Page_Cnt_T_u08

Vuint8

0

255

Mod_Cnt_T_u08

Vuint8

0

255

Return Value

Rtn_Cnt_T_u08

Uint8

0

0x28

### Description

This function sets the calibration page access. It directly calls the functions used in tuning selection management.

### ApplXcpGetCalPage

| Function Name | ApplXcp G etCalPage | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Seg_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | Mod_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | Rtn_Cnt_T_u08 | Uint8 | 0 | 0 x28 |

Function Name

ApplXcpGetCalPage

Type

Min

Max

Arguments Passed

Seg_Cnt_T_u08

Vuint8

0

255

Mod_Cnt_T_u08

Vuint8

0

255

Return Value

Rtn_Cnt_T_u08

Uint8

0

0x28

### Description

This function sets the calibration page access. It directly calls the functions used in tuning selection management.

### ApplXcpCopyCalPage

| Function Name | ApplXcp Copy CalPage | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SrcSeg_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | SrcPage_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | DestSeg_Cnt_T_u08 | Vuint8 | 0 | 255 |

|  | DestPage_Cnt_T_u08 | Vuint8 | 0 | 255 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0x28 |

Function Name

ApplXcpCopyCalPage

Type

Min

Max

Arguments Passed

SrcSeg_Cnt_T_u08

Vuint8

0

255

SrcPage_Cnt_T_u08

Vuint8

0

255

DestSeg_Cnt_T_u08

Vuint8

0

255

DestPage_Cnt_T_u08

Vuint8

0

255

Return Value

XCP_CMD_OK

Uint8

0

0x28

### Description

This function sets the calibration page access. It directly calls the functions used in tuning selection management.

### ApplXcpUserService

| Function Name | ApplXcp UserService | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | pCmd | BYTEPTR | 0 | 4294967295 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0x 3 |

Function Name

ApplXcpUserService

Type

Min

Max

Arguments Passed

pCmd

BYTEPTR

0

4294967295

Return Value

XCP_CMD_OK

Uint8

0

0x3

### Description

This function handles user service requests.

### ApplXcpOpenCmdIf

| Function Name | ApplXcp OpenCmdIf | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | pCmd | BYTEPTR | 0 | 4294967295 |

|  | pRes | BYTEPTR | 0 | 4294967295 |

|  | pLength | BYTEPTR | 0 | 4294967295 |

| Return Value | XCP_CMD_OK | Uint8 | 0 | 0x3 |

Function Name

ApplXcpOpenCmdIf

Type

Min

Max

Arguments Passed

pCmd

BYTEPTR

0

4294967295

pRes

BYTEPTR

0

4294967295

pLength

BYTEPTR

0

4294967295

Return Value

XCP_CMD_OK

Uint8

0

0x3

### Description

This function handles XCP service requests that are not supported by the driver but defined by the XCP protocol specification.

### NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper

| Function Name | NONTRUSTED_NtWrapS_Rte_Call_CopyCalPageReq_Oper | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FunctionIndex | NonTrustedFunctionIndexType | 0 | 65535 |

|  | FunctionParams | NonTrustedFunctionParameterRefType | N/A | N/A |

| Return Value | N/A | N/A | N/A | N/A |


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Complex Device Drivers](../).
