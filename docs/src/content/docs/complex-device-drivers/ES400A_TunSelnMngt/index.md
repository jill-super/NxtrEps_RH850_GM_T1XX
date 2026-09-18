---
title: "Tuning Selection Management (ES400A_TunSelnMngt)"
description: "Tuning Selection Management: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Tuning Selection Management component belongs to **Tuning and Global Parameters** in the **Complex Device Drivers** layer. It manages selectable tuning sets or project-wide global parameters.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES400A_TunSelnMngt_Design` | Design package |
| `ES400A_TunSelnMngt_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES400A_TunSelnMngt_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES400A_TunSelnMngt_Impl` |  |
| C sources | `TunSelnMngt.c`, `TunSelnMngt_private.c` |
| Public headers | `TunSelnMngt.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `TunSelnMngt.dcf`, `TunSelnMngt_attr_def.xml`, `TunSelnMngt_bswmd.arxml` |
| Generator output | `TunSelnMngt_Cfg_private.c.tt`, `TunSelnMngt_Cfg_private.h.tt`, `TunSelnMngt_Generate.bat` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `ES400A_TunSelnMngt_Impl.gpj`, `Integrate.bat`, `RteGen.bat`, `TunSelnMngt.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `ES400A_TunSelnMngt_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `ES400A_TunSelnMngt_Impl/src/TunSelnMngt.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES400A_TunSelnMngt_Impl/src/TunSelnMngt_private.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES400A_TunSelnMngt_FDD.docx`

- **Source path in repository:** `ES400A_TunSelnMngt_Design/Doc/ES400A_TunSelnMngt_FDD.docx`
- **Format:** `.docx`
- **Size:** `722 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

**Converted content:**

Tuning Selection Management

FDD #ES-400A

1.High Level Description4

2.Derived Requirements4

3.Sub-Function Data Flow4

4.Design Rationale5

4.1.Design Overview5

4.2.Flash Calibration Table5

4.3.RAM Calibration Table6

4.4.Calibration Components6

4.4.1.Flash Memory Location6

4.4.2.Calibration Usage7

4.4.3.Calibration Indexing7

4.4.4.Online Calibration Grouping7

4.5.Changing Calibration Indexes7

4.6.Copying Calibrations to RAM for Online Calibration9

5.Sub-Functions11

5.1.1.Initialization (TunSelnMngtInit1)11

5.1.1.1.Design Rationale11

5.1.1.2.Inputs11

5.1.1.3.Operation11

5.1.1.4.Outputs12

5.1.2.Periodic (TunSelnMngtPer1)13

5.1.2.1.Design Rationale13

5.1.2.2.Inputs13

5.1.2.3.Operation13

5.1.2.4.Outputs14

5.1.3.Sub-Function: CopyCalPageReq15

5.1.3.1.Design Rationale15

5.1.3.2.Inputs15

5.1.3.3.Operation15

5.1.3.4.Outputs15

5.1.4.Sub-Function: GetCalPageReq16

5.1.4.1.Design Rationale16

5.1.4.2.Inputs16

5.1.4.3.Operation16

5.1.4.4.Outputs16

5.1.5.Sub-Function: GetSegInfoReq17

5.1.5.1.Design Rationale17

5.1.5.2.Inputs17

5.1.5.3.Operation17

5.1.5.3.1.Mode Decision17

5.1.5.3.2.SegModAdrInfo17

5.1.5.3.2.1.Operation17

5.1.5.3.3.SegModStdInfo18

5.1.5.3.3.1.Operation18

5.1.5.3.4.SegModAdrMpg18

5.1.5.3.4.1.Operation18

5.1.5.4.Outputs18

5.1.6.Sub-Function: OnlineTunRamAdrMpg19

5.1.6.1.Design Rationale19

5.1.6.2.Inputs19

5.1.6.3.Operation19

5.1.6.4.Outputs19

5.1.7.Sub-Function: SetCalPageReq20

5.1.7.1.Design Rationale20

5.1.7.2.Inputs20

5.1.7.3.Operation20

5.1.7.4.Outputs20

5.1.8.Sub-Function: IdxChgMngt21

5.1.8.1.Design Rationale21

5.1.8.2.Inputs21

5.1.8.3.Operation21

5.1.8.4.Outputs22

5.1.9.Sub-Function: MemCopy32Bit and MemCopy8Bit23

5.1.9.1.Design Rationale23

5.1.9.2.Inputs23

5.1.9.3.Operation23

5.1.9.4.Outputs23

5.1.10.Sub-Function: SwtCalIdx24

5.1.10.1.Design Rationale24

5.1.10.2.Inputs24

5.1.10.3.Operation24

5.1.10.4.Outputs24

6.Timing / Execution Constraints25

6.1.Rationale / Comments25

6.2.Rates and State Execution25

7.Serial Communications Interfaces25

8.Additional Information25

9.Revision Record & Change Approval26

## High Level Description

This document describes the design of the tuning selection management software component.

## Derived Requirements

None

## Sub-Function Data Flow

The following table describes the data flow in and out of this module.

| Type | Name |

| --- | --- |

| Input | DesIninIdx |

| Input | DesRtIdx |

| Output | ActvGroup |

| Output | ActvIninIdx |

| Output | ActvRtIdx |

| Client | Calc32BitCrc_u32 |

| Client | RtCalChgReq |

| Client | SetNtcSts |

| Server | CopyCalPageReq |

| Server | GetCalPageReq |

| Server | GetSegInfoReq |

| Server | OnlineTunRamAdrMpg |

| Server | SetCalPageReq |

Type

Name

Input

DesIninIdx

Input

DesRtIdx

Output

ActvGroup

Output

ActvIninIdx

Output

ActvRtIdx

Client

Calc32BitCrc_u32

Client

RtCalChgReq

Client

SetNtcSts

Server

CopyCalPageReq

Server

GetCalPageReq

Server

GetSegInfoReq

Server

OnlineTunRamAdrMpg

Server

SetCalPageReq

## Design Rationale

### Design Overview

Tuning selection management creates two copies of the RTE generated calibration table. This table contains pointers to all the calibration software components integrated for a given software application. The component manages the pointers to provide the ability for initialization and runtime calibration changes based on inputs provided by outside applications. These inputs can be, but are not limited to, NvM values, serial communication inputs, or inputs from other software components. This component also manages a RAM buffer for online calibration over XCP.

The following sub sections will show an example of how this component operates.

### Flash Calibration Table

The flash table is generated by the RTE and uses the double pointer method defined by AUTOSAR for accessing calibrations. This provides a base pointer at the start of the flash table, and allows software to index into the calibration tables by an array index instead of knowing the direct names of the calibration structures. When the calibration source ports are connected to the receiver port within another software module, a linkage is generated by the RTE through the base pointer with the software components generated header file. An overview of this configuration is shown in the image below.

### RAM Calibration Table

Tuning Selection Management creates two copies of the flash memory calibration table. Along with each copy a CRC is maintained over each of the copies memory to ensure that the values are correct and were not modified by an outside source.

It is important to note that the cross functional team needs to ensure that the flash calibrations generated by the RTE can be used independently of the EPS system variants, such as but not limited to, motor sizing and C-factor. In the event of a RAM failure or CRC error, the default fault response is to go back using the flash calibration table and the default response is to remove assist immediately. If it can be ensured that the flash defaults are safe to drive for all program variants, the NTC can be reduced to an informative fault to and keep assist active. However, this needs to have all cross functional teams ensure that all criteria are met to make that change.

### Calibration Components

The RTE generated table of pointers point to structures of calibrations that are represented by calibration components. These components do not have any run-time actions (such as initialization or periodic functions) and only provide source ports for the calibrations. Based on the configuration provided by the program team, the description of these components is generated by an outside tool. The names of these calibration components are created based on the following sections. An example of a calibration component name is as follows:

CalRegn01Inin00GroupA

<Flash Memory Location><Calibration Usage><Calibration Indexing><Online Calibration Grouping>

#### Flash Memory Location

The flash memory location describes where the calibration is located in flash memory from Nexteer calibration memory regions to customer locations. The region is identified by the prefix “CalRegnXX”, where XX represents the region number. These regions are generic in name, but are defined by the cross-functional team to identify which locations these calibrations are located. For example, CalRegn00 could represent Nexteer calibrations and CalRegn01 could represent customer calibrations.

#### Calibration Usage

The usage part of the name identifies of it is an initialization (Inin), a runtime (Rt) calibration, or a common calibration (Cmn). Common calibrations are common among all initialization and runtime calibrations. Initialization calibrations are selected at start up and cannot be changed during operation. Runtime calibrations are selected at startup and can be changed during operation. These indexes can be changed according to the rules that govern those indexes described in the section 4.5.

#### Calibration Indexing

The calibration indexing describes that index of the desired initialization and runtime ports a given calibration component belongs.  The initialization and runtime indexes are designed to be independent of each other to give systems engineering more flexibility in defining calibrations that need to change at start up or during operation.

#### Online Calibration Grouping

The online calibration grouping defines the segment for XCP access. This section of the name is optional and if no grouping is defined then the calibration contained with that calibration component are not allowed to be tuned by XCP.

### Changing Calibration Indexes

During initialization or during runtime, the application may require an index to be changed. Calibrations marked as initialization calibrations can only be changed during initialization and will remain the same values for the rest of the ignition cycle. Runtime calibrations can change at initialization and during runtime operations.

Below is an example of calibrations in the RAM table. The calibration components highlighted in yellow represent the current active components. In this example, the desired run-time and initialization indexes are both zero (0). It is also important to note that only one of the RAM tables is active at any given time by the ECU. This allows tuning selection management the ability to modify the table contents of the unused table and update the base pointer to point to the unused table once all the changes are in place and the checksum is recalculated.

If we assume that the desired runtime index changes from a zero (0) to one (1), tuning selection management will update unused index to reflect the changes as highlighted in red below.

Once all the changes are completed, the base pointer will be updated to point to ram memory index 1 and index 0 will become the ‘scratchpad’ for any further updates.

It is important to note that the references made by the software components do not change the index they are configured to look in to. In the example above if we assume Cal Port 1 is part of the calibration components CalRegnXXRtXXGroupA, the pointer will also point to the same index. As a result, tuning selection management will need to modify the pointer to point from CalRegn01Rt00GroupA to CalRegn01Rt01GroupA to allow the software component to read the new value of the calibration.

### Copying Calibrations to RAM for Online Calibration

When a segment is enabled for online calibration, the software will move the active indexes within the requested group into the XCP RAM buffer. In the example previously provided, if we assume index zero (0) was active for both initialization and runtime calibrations the memory layout would look as follows. Note that CalRegn01Rt01GroupA is not in RAM, because it is not the active index.

XCP can provide the following access during online calibration. This design requires that two pages exists, Flash and RAM. By default, ECU and XCP access both read from Flash and XCP services will need to be executed to change the access to RAM. These services are not covered in this document. For clarification, ECU access simply means where the software components are looking for their calibration values. XCP access simple means where XCP will perform actions, such as read and write.

| ECU Access | XCP Access |

| --- | --- |

| Flash | Flash |

| Flash | RAM |

| RAM | Flash |

| RAM | RAM |

ECU Access

XCP Access

Flash

Flash

Flash

RAM

RAM

Flash

RAM

RAM

When the ECU is given access to the RAM buffer for software component access, the pointers will change to point to the RAM image instead of the flash table. This will allow the user to modify the calibration values during operation of the ECU.

## Sub-Functions

#### Initialization (TunSelnMngtInit1)

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: ES400A_48, ES400A_50, ES400A_51

#### Design Rationale

The tuning select management RAM shall be initialized according to the following pseudo code.

#### Inputs

None

#### Implementation

Read DesIninIdx Port

Read DesRtIdx Port

Set all PIMs to default values (0).

Set Page access to Flash for XCP and ECU access

Copy flash table into both MngtRamTbl indexes with MemCopy32Bit

Calculate CRC32Bit over the Flash table, and update both CRC values for the MngtRamTbl with calculated result

IF DesIninIdx not equal to PIM value:

IninIdxFound = IdxChngMngt

IF (IninIdxFound equal TRUE):

Set NTC 1F6, parameter 0 to passed

Update PIM value

Write ActiveIninIdx Port value with DesIninIdx

ELSE:

Set NTC 1F6, parameter 1

ELSE:

Set NTC 1F6, parameter 0 to passed

Write ActiveIninIdx Port value with DesIninIdx

ENDIF

IF DesRtIdx not equal to PIM value:

RtIdxFound = IdxChngMngt

IF (RtIdxFound equal TRUE):

Set NTC 1F7, parameter 0 to passed

Update PIM value

Write ActiveRtIdx Port value with DesRtIdx

ELSE:

Set NTC 1F7, parameter 1

ELSE:

Set NTC 1F7, parameter 0 to passed

Write ActiveRtIdx Port value with DesRtIdx

ENDIF

IF IninIdxFound equals TRUE OR RtIdxFound equals TRUE:

SwtCalIdx()

ENDIF

#### Outputs

None

#### Periodic (TunSelnMngtPer1)

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: ES400A_18, ES400A_51, ES400A_69

#### Design Rationale

This function queues the request to move calibrations from flash to the RAM buffer for online calibration activities during the next periodic run of tuning selection management. It shall also capture the active initialization and runtime calibration indexes and the selected group (or segment).


*... content truncated for brevity; see the source document in the repository. ...*

### `ES400A_TunSelnMngt_DDReport.txt`

- **Source path in repository:** `ES400A_TunSelnMngt_Design/Reports/ES400A_TunSelnMngt_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES400A_TunSelnMngt_DataDict
24-Apr-2016 17:22:49
Tool Release:  2.38.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, Struct.EngMin has been increased to the EngMin of the Struct data type. Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Matlab\Dependencies\Data_Management v2.38.0\+bt\@struct\struct.m',44,1)">struct.struct>struct.validateUserEngMin at 44</a>
  In <a href="matlab: opentoline('C:\Matlab\Dependencies\Data_Management v2.38.0\+DataDict\@PIM\PIM.m',139,1)">PIM.PIM>PIM.set.EngMin at 139</a>
  In <a href="matlab: opentoline('C:\Component\ES400A_TunSelnMngt_Design\Design\ES400A_TunSelnMngt_DataDict.m',488,1)">ES400A_TunSelnMngt_DataDict at 488</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Matlab\Dependencies\Tools v1.11.0\Design_Tools\VerifyDD.p>ImportVars at 1798
  In C:\Matlab\Dependencies\Tools v1.11.0\Design_Tools\VerifyDD.p>VerifyDD at 240] 
[Warning: In workspace, Struct.EngMax has been increased to the EngMax of the Struct data type. Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Matlab\Dependencies\Data_Management v2.38.0\+bt\@struct\struct.m',72,1)">struct.struct>struct.validateUserEngMax at 72</a>
  In <a href="matlab: opentoline('C:\Matlab\Dependencies\Data_Management v2.38.0\+DataDict\@PIM\PIM.m',149,1)">PIM.PIM>PIM.set.EngMax at 149</a>
  In <a href="matlab: opentoline('C:\Component\ES400A_TunSelnMngt_Design\Design\ES400A_TunSelnMngt_DataDict.m',489,1)">ES400A_TunSelnMngt_DataDict at 489</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Matlab\Dependencies\Tools v1.11.0\Design_Tools\VerifyDD.p>ImportVars at 1798
  In C:\Matlab\Dependencies\Tools v1.11.0\Design_Tools\VerifyDD.p>VerifyDD at 240] 
(errors: 2)

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
(variables: 5, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
Calc32BitCrc_u32            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 3, errors: 1)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
DesIninIdx                  	Cannot match name to list of known Nexteer signals.
DesRtIdx                    	Cannot match name to list of known Nexteer signals.
(variables: 2, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
ActvGroup                   	Cannot match name to list of known Nexteer signals.
ActvIninIdx                 	Cannot match name to list of known Nexteer signals.
ActvRtIdx                   	Cannot match name to list of known Nexteer signals.
CalCopyCmpl                 	Cannot match name to list of known Nexteer signals.
(variables: 4, errors: 4)

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
```
*... truncated (53 more lines in the source file). ...*

### `ES400A_TunSelnMngt_Integration_Manual.doc`

- **Source path in repository:** `ES400A_TunSelnMngt_Impl/doc/ES400A_TunSelnMngt_Integration_Manual.doc`
- **Format:** `.doc`
- **Size:** `152 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ES400A_TunSelnMngt_MDD.docx`

- **Source path in repository:** `ES400A_TunSelnMngt_Impl/doc/ES400A_TunSelnMngt_MDD.docx`
- **Format:** `.docx`
- **Size:** `2634 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

TunSelnMngt

August 29, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Kevin Smith,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date | Approved By |

| --- | --- | --- | --- | --- |

| Initial Version | K. Smith | 1 | 07 - Apr - 16 |  |

| Updated program flow diagrams | N. Saxton | 2 | 06-May-16 |  |

| Updates to flow charts for anomaly EA4#6672 corrections | K. Smith | 3 | 29-Aug-16 |  |

Description

Author

Version

Date

Approved By

Initial Version

K. Smith

1

07-Apr-16

Updated program flow diagrams

N. Saxton

2

06-May-16

Updates to flow charts for anomaly EA4#6672 corrections

K. Smith

3

29-Aug-16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2TunSelnMngt & High-Level Description6

3Design details of software module7

3.1Graphical representation of TunSelnMngt7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

4.2Variable Data Dictionary8

4.2.1User Defined Typedef Definition/Declaration8

4.2.1.1Static Structures8

4.2.1.2Dynamic Structures and Enums9

4.2.2User Defined Enumerated Types10

5Software Component Implementation11

5.1Sub-Module Functions11

5.1.1Init: TunSelnMngtInit111

5.1.2Per: TunSelnMngtPer113

5.2Server Runnables15

5.2.1CopyCalPageReq15

5.2.2GetCalPageReq16

5.2.3GetSegInfoReq17

5.2.4OnlineTunRamAdrMpg18

5.2.5SetCalPageReq19

5.3Interrupt Functions20

5.4Module Internal (Local) Functions20

5.4.1SwtCalIdx20

5.4.2IdxChgMngt21

5.4.3MemCopy32Bit23

5.4.4MemCopy8Bit24

5.4.5SegModAdrInfo25

5.4.6SegModStdInfo26

5.4.7SegModAdrMpg27

5.5GLOBAL Function/Macro Definitions28

6Known Limitations with Design29

7UNIT TEST CONSIDERATION30

Appendix AAbbreviations and Acronyms31

Appendix BGlossary32

Appendix CReferences33

## Introduction

### Purpose

This MDD aids in documenting the implementation of ES400A Tuning Selection Management.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## TunSelnMngt & High-Level Description

Tuning Selection Management (TunSelnMngt) provides the ability to change run-time calibrations during operation. The component also provides a RAM buffer for online calibration changes over XCP for tuning processes.

## Design details of software module

### Graphical representation of TunSelnMngt

### Data Flow Diagram

None

#### Component level DFD

None

#### Function level DFD

None

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Values between the brackets [] are the ranges that the configurable constants could be defined as for a given integration. These values are generated by Configurator before the software build.

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| MAXINITIDXCNT_CNT_U08 | Uint8 | Cnt | [0-255] |

| MAXRTIDXCNT_CNT_U08 | Uint8 | Cnt | [0-255] |

| MAXONLINECALCFGCNT_CNT_U08 | Uint 8 | Cnt | [0-255] |

| ONLINECALGROUPS_CNT_U08 | Uint8 | Cnt | [0-255] |

| ONLINECALRAMTBL_CNT_U16 | Uint16 | Cnt | [0-65535] |

| PRMPTRTBLSIZEINWORD_CNT_U16 | Uint16 | Cnt | [0-65535] |

Constant Name

Resolution

Units

Value

MAXINITIDXCNT_CNT_U08

Uint8

Cnt

[0-255]

MAXRTIDXCNT_CNT_U08

Uint8

Cnt

[0-255]

MAXONLINECALCFGCNT_CNT_U08

Uint8

Cnt

[0-255]

ONLINECALGROUPS_CNT_U08

Uint8

Cnt

[0-255]

ONLINECALRAMTBL_CNT_U16

Uint16

Cnt

[0-65535]

PRMPTRTBLSIZEINWORD_CNT_U16

Uint16

Cnt

[0-65535]

### Variable Data Dictionary

The following type definitions are found in the private header of this component.

#### User Defined Typedef Definition/Declaration

### Static Structures

The following table contains structures are static in their definition. However, internal elements may change based on the configuration of the project but the high level content is the same. These elements are described at the bottom of the table.

| Typedef  Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| TunSelnRamTblRec1 | PrmRefTblPtr | Rte_ParameterRefTabType | N/A | N/A |

|  | PrmTblCrc_u32 | Uint32 | 0 | 4294967295 |

| TunSelnIdxTblRec1 | SrcIdx_u 16 | Uint16 | 0 | 65535 |

|  | DestIdx_u 16 | Uint16 | 0 | 65535 |

|  | SigIdx_u08 | Uint8 | 0 | 255 |

| TunSelnOnlineCalIdxTblRec1 | RamStructPtr_u08 | UInt8* | 0 | 255 |

|  | StructSize_u16 | Uint16 | 0 | 65535 |

|  | TblIdx_u 16 | Uint16 | 0 | 65535 |

|  | GroupIdx_u08 | Uint8 | 0 | 255 |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

TunSelnRamTblRec1

PrmRefTblPtr

Rte_ParameterRefTabType

N/A

N/A

PrmTblCrc_u32

Uint32

0

4294967295

TunSelnIdxTblRec1

SrcIdx_u16

Uint16

0

65535

DestIdx_u16

Uint16

0

65535

SigIdx_u08

Uint8

0

255

TunSelnOnlineCalIdxTblRec1

RamStructPtr_u08

UInt8*

0

255

StructSize_u16

Uint16

0

65535

TblIdx_u16

Uint16

0

65535

GroupIdx_u08

Uint8

0

255

Rte_ParameterRefTabType is a structure of void pointers that point to the various calibration component structures. This type is generated by the RTE based on the configuration of the integration.

### Dynamic Structures and Enums

The following table contains structures are dynamic in their definition. The contents contained will vary from project to project. The intent of this table is to document their purpose.

| Entry Type | Typedef  Name | Example Element(s) | Variable Type | Value | Comment |

| --- | --- | --- | --- | --- | --- |

| Enum | OnlineCalGroup 1 | GroupA | N/A | 0 | This  enum  contains a number representation for each calibration group that is generated for online calibration from A=0 to Z=26. Groups are defined by a letter suffix. |

|  |  | GroupB | N/A | 1 |  |

| Struct | < GroupName > Typ GroupATyp | <Cal Region><Cal  Cmp  Name><Online Group> CalRegn01CmnGroupA | RTE Generated | N/A | This structure is generated based on the online groups configured. Each group will generate a structure and contain all calibration software components within that group. |

| Union | OnlineCalTblRec1 | Byte[<RAM Size>] | Unit8 | N/A | This structure combines all the online calibration groups into data type for assignment to the RAM buffer. The ‘byte’ element is used to access the entire buffer on a byte-by-byte basis and ensure that the RAM is properly sized. |

|  |  | < GroupName > | < GroupName > Typ | N/A |  |

Entry Type

Typedef Name

Example Element(s)

Variable Type

Value

Comment

Enum

OnlineCalGroup1

GroupA

N/A

0

This enum contains a number representation for each calibration group that is generated for online calibration from A=0 to Z=26. Groups are defined by a letter suffix.

GroupB

N/A

1

Struct

<GroupName>Typ

GroupATyp

<Cal Region><Cal Cmp Name><Online Group>

CalRegn01CmnGroupA

RTE Generated

N/A

This structure is generated based on the online groups configured. Each group will generate a structure and contain all calibration software components within that group.

Union

OnlineCalTblRec1

Byte[<RAM Size>]

Unit8

N/A

This structure combines all the online calibration groups into data type for assignment to the RAM buffer. The ‘byte’ element is used to access the entire buffer on a byte-by-byte basis and ensure that the RAM is properly sized.

<GroupName>

<GroupName>Typ

N/A

#### User Defined Enumerated Types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

| GetSegModeSegInfo1 | GETSEGMODSEGINFO_ADR | 0 |

|  | GETSEGMODSEGINFO_LEN | 1 |

| GetSegModeMpgIdx1 | GETSEGMODMPGIDX_SRCADR | 0 |

|  | GETSEGMODMPGIDX_DESTADR | 1 |

|  | GETSEGMODMPGIDX_LEN | 2 |

Enum  Name

Element Name

Value

GetSegModeSegInfo1

GETSEGMODSEGINFO_ADR

0

GETSEGMODSEGINFO_LEN

1

GetSegModeMpgIdx1

GETSEGMODMPGIDX_SRCADR

0

GETSEGMODMPGIDX_DESTADR

1

GETSEGMODMPGIDX_LEN

2

## Software Component Implementation

### Sub-Module Functions

#### Init: TunSelnMngtInit1

#### Design Rationale

The initialization function creates two copies of the RTE generated flash table in to RAM. A CRC is performed on each of the copies to ensure that they match. The function also adjusts the tables to load the appropriate initialization and run-time calibrations indexes that are required by the application.

#### Processing

#### Module Outputs

None

#### Per: TunSelnMngtPer1

#### Design Rationale

#### Processing

#### Module Outputs

None

### Server Runnables

#### CopyCalPageReq

#### Design Rationale

This function is called by the XCP master and queues the copy of the calibrations contained in the selected group, or segment, into the RAM buffer. The actual copy is performed by TunSelnMngt’s main periodic function, but this runnable logs the current state of TunSelnMngt and marks the copy in progress.

#### (Processing of function)………

#### Module Outputs

None

#### GetCalPageReq

#### Design Rationale

This function is called by the XCP master and returns the page with the request XCP and ECU access for a given segment.

#### (Processing of function)………

#### Module Outputs

None

#### GetSegInfoReq

#### Design Rationale

This function is called by the XCP master and returns the requested information for the provided segment.

#### (Processing of function)………

#### Module Outputs

None

#### OnlineTunRamAdrMpg

#### Design Rationale

This function is called by the XCP master. During tuning, tools such as eTool and CANape will read calibration values from their flash addresses because that is how the A2L file is defined. However, when the calibrations are access from RAM, the user does not always know the exact address the calibration is located. This function calculates the RAM address for a given calibration to the XCP function for reading and writing.

#### (Processing of function)………

#### Module Outputs

None

#### SetCalPageReq

#### Design Rationale

This function is called by the XCP master. This function will set the status of the calibration page for a given segment.

#### (Processing of function)………

#### Module Outputs

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### SwtCalIdx

| Function Name | SwtCalIdx | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A |  |  |  |

| Return Value | N/A |  |  |  |

Function Name

SwtCalIdx

Type

Min

Max

Arguments Passed

N/A

Return Value

N/A

#### Design Rationale

This function manages the RAM buffer access and switches the calibration index between the two copies in RAM.

#### Processing

#### IdxChgMngt

| Function Name | IdxChgMngt | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | SeldIdx_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | GendCalTblSize_Cnt_T_u08 | Uint8 | 0 | 255 |

|  | GendCalTbl_T_rec | TunSelnIdxTblRec1 * | 0 | 4294967295 |

| Return Value | IdxFound_Cnt_T_logl | Boolean | FALSE | TRUE |

Function Name

IdxChgMngt

Type

Min

Max

Arguments Passed

SeldIdx_Cnt_T_u08

Uint8

0

255

GendCalTblSize_Cnt_T_u08

Uint8

0

255

GendCalTbl_T_rec

TunSelnIdxTblRec1*

0

4294967295

Return Value

IdxFound_Cnt_T_logl

Boolean

FALSE

TRUE

#### Design Rationale

#### Processing

#### MemCopy32Bit

| Function Name | MemCopy32Bit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Des_Arg | Void | 0 | 4294967295 |

|  | Src_Arg | Void | 0 | 4294967295 |

|  | Len_Arg | Uint16 | 0 | 65535 |

| Return Value | N/A |  |  |  |

Function Name

MemCopy32Bit

Type

Min

Max

Arguments Passed

Des_Arg

Void

0

4294967295

Src_Arg

Void

0

4294967295

Len_Arg

Uint16

0

65535

Return Value

N/A

#### Design Rationale

The 32-bit mem copy function is used to move calibration pointers from flash to RAM. The void pointers are internally assigned to a uint32 pointer before the processing loop begins.

#### Processing

#### MemCopy8Bit

| Function Name | MemCopy8Bit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | Des_Arg | Void | 0 | 4294967295 |

|  | Src_Arg | Void | 0 | 4294967295 |

|  | Len_Arg | Uint16 | 0 | 65535 |

| Return Value | N/A |  |  |  |

Function Name

MemCopy8Bit

Type

Min

Max

Arguments Passed

Des_Arg

Void

0

4294967295

Src_Arg

Void

0

4294967295

Len_Arg

Uint16

0

65535

Return Value

N/A

#### Design Rationale

The 8-bit mem copy function is used to move calibration segments into the RAM space. Since the length of the segments is not guaranteed to be a 32-bit even address, 8-bit was selected to ensure that only the bytes required to be moved are performed. The void pointers are internally assigned to a uint8 pointer before the processing loop begins.


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Complex Device Drivers](../).
