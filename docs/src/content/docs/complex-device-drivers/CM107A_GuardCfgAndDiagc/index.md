---
title: "Guard Configuration And Diagnostics (CM107A_GuardCfgAndDiagc)"
description: "Guard Configuration And Diagnostics: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Guard Configuration And Diagnostics component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM107A_GuardCfgAndDiagc_Design` | Design package |
| `CM107A_GuardCfgAndDiagc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM107A_GuardCfgAndDiagc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM107A_GuardCfgAndDiagc_Impl` |  |
| C sources | `CDD_GuardCfgAndDiagc.c`, `CDD_GuardCfgAndDiagcNonRte.c` |
| Public headers | `CDD_GuardCfgAndDiagc.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `GuardCfgAndDiagc.dcf`, `GuardCfgAndDiagc_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM107A_GuardCfgAndDiagc_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreateQACProject.bat`, `GuardCfgAndDiagc.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `CM107A_GuardCfgAndDiagc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM107A_GuardCfgAndDiagc_Impl/src/CDD_GuardCfgAndDiagc.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM107A_GuardCfgAndDiagc_Impl/src/CDD_GuardCfgAndDiagcNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM107A_GuardCfgAndDiagc.docx`

- **Source path in repository:** `CM107A_GuardCfgAndDiagc_Design/Design/CM107A_GuardCfgAndDiagc.docx`
- **Format:** `.docx`
- **Size:** `2020 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Guard Configuration And Diagnostics RH850

( GuardCfgAndDiagc )

FDD CM107A

1.High Level Description3

1.1. Overview3

1.2. Slave Guards3

1.2.1. IPG – Internal Peripheral Guard4

1.2.2. PEG – PE Guard Function4

2.Sub-Functions in this Document5

3.Sub-functions5

3.1Sub-function: (GuardCfgAndDiagcInit1)5

3.1.2.Guard Configuration Section: PEG Slave Guard Configuration6

3.1.3.Guard Configuration Section: IPG Slave Guard Configuration13

3.1.4.Guard Configuration Section: PBG Slave Guard Configuration19

4.1Sub-Function (GuardCfgAndDiagcInit2)28

4.2Sub-Function: (GuardCfgAndDiagcInit3)28

3.1.5.NTCs28

3.1.6.SAN Linkage28

3.1.7.Description29

3.1.8.Rationale29

3.1.9.Implementation30

3.1.10.Reference39

3.1.11.Verification Method50

4.Revision Record & Change Approval50

## High Level Description

This document describes the microcontroller configuration for the micro slave guard function.  This function will selectively enable access to microcontroller resources.  On reset most of these resources are unprotected so the net behavior of the slave guard function is to constrain access.

Ref. Renesas’ Hardware User’s Manual  Ver 1.10  Dtd Feb 2016

### 1.1. Overview

The RH850 P1M MCU provides protection features to prevent erroneous access to memory and the control registers of the peripheral circuits using the slave guard function.

### 1.2. Slave Guards

There are three sections to the guard function:

PEG – Processor Element Guard

IPG – Internal Peripheral Guard

PBG – Peripheral Bus Guard

Fig 4.1-1 from SAN 1.20 edited to correct the Flexray PROTSPID to match the value shown in the HWUM 1.1

#### 1.2.1. IPG – Internal Peripheral Guard

The IPG section protects the CPU peripherals against illegal accesses by SW components running on the CPU itself.

The IPG provides the following features:

Detects violation of peripheral device protection.

Stores unauthorized access information

Blocks unauthorized access.

Notifies violation through an exception.

Invalidates subsequent access (post violation).

#### 1.2.2. PEG – PE Guard Function

The PE guard system section prevents unauthorized access to the resources in the PE from an external master. This section protects access to the local RAM in the PE.

The PEG provides the following features:

Protects local RAM against illegal access from FlexRay and the DMA.

Detects PE access violation.

Blocks unauthorized access.

Provides notification of an unauthorized access through the ECM.

Allows protection of up to 4 areas with 4K granularity.

#### 1.2.3. PBG – Peripheral Bus Guards

The PBG protects the control registers in the peripheral circuits and memories from illegal access by the PE, Flexray and the DMA. The PBG module is divided into multiple PBG groups, each of which is provided a maximum of 16 protection channels.

A single PBG channel can designate the access against which a single peripheral circuit should be protected.  Each PBG group can hold the information of the access that has been rejected.

The PBG provides the following features:

For protection against read access, an undefined value is read.

For protection against write access, the write access is ignored.

Provides notification of an unauthorized access through the ECM.

Stores unauthorized access information.

## Sub-Functions in this Document

Below is a linked list of all sub-functions owned by this document.

| Sub-Function Name | Link |

| --- | --- |

| GuardCfgAndDiagcInit1 | 4.1 |

| GuardCfgAndDiagcInit2 | 4.2 |

| GuardCfgAndDiagcInit3 | 4.3 |

Sub-Function Name

Link

GuardCfgAndDiagcInit1

4.1

GuardCfgAndDiagcInit2

4.2

GuardCfgAndDiagcInit3

4.3

## Sub-functions

### Sub-function: (GuardCfgAndDiagcInit1)

Return to subfunction list: return

#### NTCs

N/A

#### SAN Linkage

See the SAN Linkage paragraph of each of the sections which make up this sub-function.

#### Description

This sub-function configures the RH850/P1M.  This has been described in three sections which correspond to the portions of the guard hardware facilities which the microcontroller provides.

#### Rationale

This sub-function has been defined in terms of the sections which correspond to the hardware resources.  This seems to have helped to organize the information but what was thought to be an additional benefit, supporting distinct initialization times for the different guard hardware, has not been used and has not been maintained.

#### Implementation

See the Implementation paragraph of each of the sections which make up this sub-function.

#### Initialization (GuardCfgAndDiagcInit1)

PegInin();

IpgInin();

PbgInin();

#### Reference

See the Reference paragraph of each of the sections which make up this sub-function.

#### Verification Method

See the Verification Method paragraph of each of the sections which make up this sub-function.

#### Guard Configuration Section: PEG Slave Guard Configuration

Return to sub-function list link: return

Provides notification of an unauthorized access to the ECM.

#### NTCs

N/A

#### SAN Linkage

SAN-169: After reset, the access to the local RAM by bus masters other than the PE (CPU) itself is disabled. Thus, protection- setting registers shall be configured to authorize desired accesses by the DMA and FlexRay. These registers are not protected by PEG and can be thus protected by means of the MPU or the IPG.

#### Description

This sub-function configures the RH850/P1M for the PEG.  The PEG provides and limits access of masters other than the PE (the Flexray and DMA channels) to LRAM.

#### Rationale

Using the 4Kbyte resolution of the PEGG memory protection capability, the external masters (Flexray and DMA channels) have write access to the same one 4K block of LRAM and may read all 128Kbytes.  PEG0 registers define and control the writable 4Kbyte memory block in the highest 4K addresses of LRAM: 0xFEBFF000 through 0xFEBFFFFF.  PEGG1 registers define and control the readable 128Kbyte memory block which is all of LRAM: 0xFEBE0000 through 0xFEBFFFFF.   Two PEGG register sets remain unused.

DMA channels which move data from peripheral to LRAM, from LRAM to peripheral, or from LRAM to LRAM will have different SPIDs.  Their access rights will be determined by the SPIDs.

#### Implementation

PEG Protection Targets – Following access types are allowed or restricted for bus masters of each SPID:

SPID 0 – Read access allowed, Write access allowed.

SPID 1 – Read access restricted, Write access restricted.

SPID 2 – Read access allowed, Write access restricted.

SPID 3 – Read access allowed, Write access allowed.

Per the IPG setup in section 4.1, the PEG registers cannot be changed in user mode.

DMA channels will be assigned SPIDs corresponding to their respective LRAM and peripheral access requirements (SPID 2 or 3).

Flexray uses SPID 3.  Currently, the intent is to make no use of the Flexray’s memory access capability but the SPID 3 ability to write to only the special 4K block and to read the entire LRAM matches well with possible future designs.

The CPU is, thus far, only using the Reset initialized SPID value of 1.

The “CAUTION” note following Table 3.63 of the HWUM states “PEGGnBA.GnEN is cleared by writing to the PEGGnMK register.”  Therefore, the PEGGnMK must be written before PEGGnBA for every PEGGnBA where a “1” is desired in the GnEN bit.

Register Configuration Summary:

| Register | Value | Comments | Access |  |

| --- | --- | --- | --- | --- |

|  |  |  | SV | UM |

| PEGSP | 0x0001 | Enable detection of accesses by any external master with an enabled SPID. | RW | RW* |

| PEGG0BA | 0xFEBF F095 PEGG0BA.G0BASE = 0xFEBFF PEGG0BA.G0SP3 = 1 PEGG0BA.G0SP2 = 0 PEGG0BA.G0SP1 = 0 PEGG0BA.G0SP0 = 1 PEGG0BA.G0WR = 1 PEGG0BA.G0RD = 0 PEGG0BA.G0EN = 1 | Initialized to Local RAM start address  in high order 20 bits .   Write a ccess allowed for SPID 3 and SPID  0 .  Write  Acc ess not allowed for SPID 2 and 1 . | RW | RW* |

| PEGG0MK | 0x0000 0000 PEGG0MK.G0MASK = 0x00000 | This memory region consists of one 4Kbyte block so a zero mask makes all 20 bits of the G0BASE field of PEGG0BA significant. | RW | RW* |

| PEGG1BA | 0xFEBE 00D3 PEGG1BA.G1BASE = 0xFEBE0 PEGG1BA.G1SP3 = 1 PEGG1BA.G1SP2 = 1 PEGG1BA.G1SP1 = 0 PEGG1BA.G1SP0 = 1 PEGG1BA.G1WR = 0 PEGG1BA.G1RD = 1 PEGG1BA.G1EN = 1 | Initialized to 128Kb Local RAM’s start address.   Read access allowed for SPID 2 , SPID 3  and SPID 0. Read Access not allowed for SPID 1. | RW | RW* |

| PEGG1MK | 0x0001 F000 PEGG1MK.G1MASK = 0x0001F | With five mask bits set to one, only fifteen of  the  20 bits of the G1BASE field of PEGG1BA are compared.  The entire local RAM is  made read accessible  here  since (32- 15 =) 17 bits addresses 128 Kbyte . | RW | RW* |

| PEGG2BA | 0 | Set to or allow to remain at the value of zero established by reset. | RW | RW* |

| PEGG2MK | 0 | Set to or allow to remain at the value of zero established by reset. | RW | RW* |

| PEGG3BA | 0 | Set to or allow to remain at the value of zero established by reset. | RW | RW* |

| PEGG3MK | 0 | Set to or allow to remain at the value of zero established by reset. | RW | RW* |

Register

Value

Comments

Access

SV

UM

PEGSP

0x0001

Enable detection of accesses by any external master with an enabled SPID.

RW

RW*

PEGG0BA

0xFEBF F095

PEGG0BA.G0BASE = 0xFEBFF

PEGG0BA.G0SP3 = 1

PEGG0BA.G0SP2 = 0

PEGG0BA.G0SP1 = 0

PEGG0BA.G0SP0 = 1

PEGG0BA.G0WR = 1

PEGG0BA.G0RD = 0

PEGG0BA.G0EN = 1

Initialized to Local RAM start address in high order 20 bits.

Write access allowed for SPID 3 and SPID 0. Write Access not allowed for SPID 2 and 1.

RW

RW*

PEGG0MK

0x0000 0000

PEGG0MK.G0MASK = 0x00000

This memory region consists of one 4Kbyte block so a zero mask makes all 20 bits of the G0BASE field of PEGG0BA significant.

RW

RW*

PEGG1BA

0xFEBE 00D3

PEGG1BA.G1BASE = 0xFEBE0

PEGG1BA.G1SP3 = 1

PEGG1BA.G1SP2 = 1

PEGG1BA.G1SP1 = 0

PEGG1BA.G1SP0 = 1

PEGG1BA.G1WR = 0

PEGG1BA.G1RD = 1

PEGG1BA.G1EN = 1

Initialized to 128Kb Local RAM’s start address.

Read access allowed for SPID 2, SPID 3 and SPID 0. Read Access not allowed for SPID 1.

RW

RW*

PEGG1MK

0x0001 F000

PEGG1MK.G1MASK = 0x0001F

With five mask bits set to one, only fifteen of the 20 bits of the G1BASE field of PEGG1BA are compared.  The entire local RAM is made read accessible here since (32- 15 =) 17 bits addresses 128 Kbyte.

RW

RW*

PEGG2BA

0

Set to or allow to remain at the value of zero established by reset.

RW

RW*

PEGG2MK

0

Set to or allow to remain at the value of zero established by reset.

RW

RW*

PEGG3BA

0

Set to or allow to remain at the value of zero established by reset.

RW

RW*

PEGG3MK

0

Set to or allow to remain at the value of zero established by reset.

RW

RW*

* the access rights shown are the “after reset” defaults, these are modified by the value written to IPGPMTUM4 as described in this document.

#### Initialization (PegInin)

PEGG0MK = 0x0000 0000;  //write each MK before the corresponding BA!!!

//side effect of writing PEGGnMK: it clears PEGGnBA.GnEN

PEGG0BA = 0xFEBF F095;

PEGG1MK = 0x0001 F000;

PEGG1BA = 0xFEBE 00D3;

//PEGG2MK = 0x0000 0000;  // no register write is required as default values are appropriate

//PEGG2BA = 0x0000 0000;   // no register write is required as default values are appropriate

//PEGG3MK = 0x0000 0000;  // no register write is required as default values are appropriate

//PEGG3BA = 0x0000 0000;   // no register write is required as default values are appropriate

PEGSP =    0x0001;  //enable PEG

#### Reference

#### Verification Method

N/A

#### Guard Configuration Section: IPG Slave Guard Configuration

Return to sub-function list link: return

Provides notification of an unauthorized access to the ECM.

#### NTCs

N/A

#### SAN Linkage

SAN-153: The IPG function is not automatically enabled (initial setting).  If a specific protection of the mentioned peripherals is intended, then the CPU shall set the E bit in IPGENUM while in the supervisor mode or if write permission for user mode is set by IPGPMTUM4 register.

#### Description

This sub-function configures the RH850/P1M IPG.

#### Rationale

It is desired to allow the processor (PE) user mode read access to all peripherals including H-bus (Flexray). In contrast, user mode write access will be allowed only to necessary devices: P-bus groups 0 to 3 and 5 and the H Bus.  The processor (PE) has been granted no user mode execute access to any peripherals.  All other IPG protected resources: COMPTEST, INTC1, SysErrGen, and user mode access to IPG and PBG registers are limited to read access.


*... content truncated for brevity; see the source document in the repository. ...*

### `CM107A_GuardCfgAndDiagc_DDReport.txt`

- **Source path in repository:** `CM107A_GuardCfgAndDiagc_Design/Reports/CM107A_GuardCfgAndDiagc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM107A_GuardCfgAndDiagc_DataDict
10-Feb-2016 16:46:41
Tool Release:  2.28.0



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
(variables: 3, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 1, errors: 0)

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
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 0, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (32 more lines in the source file). ...*

### `GuardCfgAndDiagc Integration Manual.doc`

- **Source path in repository:** `CM107A_GuardCfgAndDiagc_Impl/doc/GuardCfgAndDiagc Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `GuardCfgAndDiagc Module Design Document.docx`

- **Source path in repository:** `CM107A_GuardCfgAndDiagc_Impl/doc/GuardCfgAndDiagc Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `108 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

GuardCfgAndDiagc

Mar 31 , 2016

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

| Initial Version | Avinash  James | 1 .0 | 02/16/16 |

| Updates for PBG Register Lock bits and  Syncm  inclusion | Avinash  James | 2.0 | 03/31/16 |

Description

Author

Version

Date

Initial Version

Avinash James

1.0

02/16/16

Updates for PBG Register Lock bits and Syncm inclusion

Avinash James

2.0

03/31/16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2GuardCfgAndDiagc & High-Level Description6

3Design details of software module7

3.1Graphical representation of GuardCfgAndDiagc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: GuardCfgAndDiagcInit19

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Init: GuardCfgAndDiagcInit29

5.1.2.1Design Rationale9

5.1.2.2Module Outputs9

5.1.3Init: GuardCfgAndDiagcInit39

5.1.3.1Design Rationale9

5.1.3.2Module Outputs9

5.1.4Per: None9

5.2Server Runables9

5.3Interrupt Functions9

5.4Module Internal (Local) Functions10

5.4.1ConfigureFilterN10

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.4.2ChkForPBGErr10

5.4.2.1Design Rationale10

5.4.2.2Processing10

5.4.3ChkForECMErr10

5.4.3.1Design Rationale10

5.4.3.2Processing11

5.4.4Vrfy32BitPBGRegAcs11

5.4.4.1Design Rationale11

5.4.4.2Processing11

5.4.5Vrfy16BitPBGRegAcs11

5.4.5.1Design Rationale11

5.4.5.2Processing11

5.4.6Vrfy8BitPBGRegAcs11

5.4.6.1Design Rationale11

5.4.6.2Processing11

5.5GLOBAL Function/Macro Definitions12

5.5.1GLOBAL Function #112

5.5.1.1Design Rationale12

5.5.1.2Processing12

6Known Limitations with Design13

7UNIT TEST CONSIDERATION14

Appendix AAbbreviations and Acronyms15

Appendix BGlossary16

Appendix CReferences17

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## GuardCfgAndDiagc & High-Level Description

See FDD

## Design details of software module

### Graphical representation of GuardCfgAndDiagc

### Data Flow Diagram

#### Component level DFD

See FDD

#### Function level DFD

See FDD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| PBGPROTNCMN_CNT_U32 | 1 | uint32 | 0x0405FE1FU |

| PBGUSRMODENA_CNT_U32 | 1 | uint32 | 0x02000000U |

| PBGUSRMODDI_CNT_U32 | 1 | uint32 | 0x00000000U |

| PBGSPID321ENA_CNT_U32 | 1 | uint32 | 0x000001C0U |

| PBGSPID31ENA_CNT_U32 | 1 | uint32 | 0x00000140U |

| PBGSPID21ENA_CNT_U32 | 1 | uint32 | 0x000000C0U |

| PBGSPID1ENA_CNT_U32 | 1 | uint32 | 0x00000040U |

| PBGSETNOREADWRACS_CNT_U32 | 1 | uint32 | 0x405FE5CU |

| NROF8BITREG_CNT_U08 | 1 | uint8 | ((uint8)0x09) |

| NROF32BITREG_CNT_U08 | 1 | uint8 | ((uint8)0x02) |

| READERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<6U) |

| WRERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<7U) |

| CFGERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<8U) |

| PBGERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<9U) |

| ECMERRBIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<10U) |

| REGTYPE8BIT_CNT_U32 | 1 | uint32 | ((uint32)0U<<4U) |

| REGTYPE16BIT_CNT_U32 | 1 | uint32 | ((uint32)1U<<4U) |

| REGTYPE32BIT_CNT_U32 | 1 | uint32 | ((uint32)2U<<4U) |

| PBGSTRTUPTESTNOFAILR_CNT_U32 | 1 | uint32 | 0x0U |

| PBGPROTNLOCKENA_CNT_U32 | 1 | uint32 | 0x80000000U |

Constant Name

Resolution

Units

Value

PBGPROTNCMN_CNT_U32

1

uint32

0x0405FE1FU

PBGUSRMODENA_CNT_U32

1

uint32

0x02000000U

PBGUSRMODDI_CNT_U32

1

uint32

0x00000000U

PBGSPID321ENA_CNT_U32

1

uint32

0x000001C0U

PBGSPID31ENA_CNT_U32

1

uint32

0x00000140U

PBGSPID21ENA_CNT_U32

1

uint32

0x000000C0U

PBGSPID1ENA_CNT_U32

1

uint32

0x00000040U

PBGSETNOREADWRACS_CNT_U32

1

uint32

0x405FE5CU

NROF8BITREG_CNT_U08

1

uint8

((uint8)0x09)

NROF32BITREG_CNT_U08

1

uint8

((uint8)0x02)

READERRBIT_CNT_U32

1

uint32

((uint32)1U<<6U)

WRERRBIT_CNT_U32

1

uint32

((uint32)1U<<7U)

CFGERRBIT_CNT_U32

1

uint32

((uint32)1U<<8U)

PBGERRBIT_CNT_U32

1

uint32

((uint32)1U<<9U)

ECMERRBIT_CNT_U32

1

uint32

((uint32)1U<<10U)

REGTYPE8BIT_CNT_U32

1

uint32

((uint32)0U<<4U)

REGTYPE16BIT_CNT_U32

1

uint32

((uint32)1U<<4U)

REGTYPE32BIT_CNT_U32

1

uint32

((uint32)2U<<4U)

PBGSTRTUPTESTNOFAILR_CNT_U32

1

uint32

0x0U

PBGPROTNLOCKENA_CNT_U32

1

uint32

0x80000000U

## Software Component Implementation

### Sub-Module Functions

#### Init: GuardCfgAndDiagcInit1

### Design Rationale

Non-RTE function for Guard configuration initialization of PEG, IPG, and PBG so that guard protection can be initialized and enabled before the RTE is started

### Module Outputs

Configuration registers for PEG, IPG, and PBG

#### Init: GuardCfgAndDiagcInit2

### Design Rationale

RTE Empty function for purposes of memory mapping

See FDD for more.

### Module Outputs

None

#### Init: GuardCfgAndDiagcInit3

### Design Rationale

Non-RTE function for Start Up Initialization test of PBG of Group 3A

See FDD for more.

### Module Outputs

None

### Per: None

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

#### ConfigureFilterN

| Function Name | ConfigureFilterN | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgProtReg | volatile uint32* | 0 | 0xFFFFFFFF |

|  | Val | uint32 | 0 | 0xFFFFFFFF |

|  | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |

Function Name

ConfigureFilterN

Type

Min

Max

Arguments Passed

PbgProtReg

volatile uint32*

0

0xFFFFFFFF

Val

uint32

0

0xFFFFFFFF

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This local function sets the value Val to the register address PbgProtReg passed as the arguments and verifies the write operation was successful. If not a diagnostic is set.

### Processing

Figure 4.5.3 from SAN ver 1.20

#### ChkForPBGErr

| Function Name | ChkForPBGErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

ChkForPBGErr

Type

Min

Max

Arguments Passed

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This local function checks PBG access violation error is captured. If not set diagnostic, clear the error and if the error doesn’t clear set diagnostic.

### Processing

Figure 4.5.3 from SAN ver 1.20

#### ChkForECMErr

| Function Name | ChkForECMErr | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

ChkForECMErr

Type

Min

Max

Arguments Passed

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This local function checkscwhether ECM captures the error sets diagnostic message and clears the ECM errors after the check else set diagnostic.

### Processing

Refer FDD 4.5.3 Implementation

#### Vrfy32BitPBGRegAcs

| Function Name | Vrfy32BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

Vrfy32BitPBGRegAcs

Type

Min

Max

Arguments Passed

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This is defined to reduce the path count and modularizes the check for the 32 bit Access registers alone.

### Processing

#### Vrfy16BitPBGRegAcs

| Function Name | Vrfy 16 BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

Vrfy16BitPBGRegAcs

Type

Min

Max

Arguments Passed

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This is defined to reduce the path count and modularizes the check for the 16 bit Access registers alone.

### Processing

#### Vrfy8BitPBGRegAcs

| Function Name | Vrfy 8 BitPBGRegAcs | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | PbgStrtUpTestFailSts | Uint32 * | 0 | 0xFFFFFFFF |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

Vrfy8BitPBGRegAcs

Type

Min

Max

Arguments Passed

PbgStrtUpTestFailSts

Uint32 *

0

0xFFFFFFFF

Return Value

None

### Design Rationale

This is defined to reduce the path count and modularizes the check for the 8 bit Access registers alone.

### Processing

### GLOBAL Function/Macro Definitions

### GLOBAL Function #1

| Function Name |  | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed |  |  |  |  |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

Type

Min

Max

Arguments Passed

Return Value

### Design Rationale

### Processing

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

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 .0 1 |

| 3 | Software Naming Conventions.doc | 2 .0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

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

2.0

4

Software Design and Coding Standards.doc

2.1

Back to [Complex Device Drivers](../).
