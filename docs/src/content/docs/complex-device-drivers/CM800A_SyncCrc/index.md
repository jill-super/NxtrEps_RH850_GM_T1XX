---
title: "Synchronous Cyclic Redundancy Check (CM800A_SyncCrc)"
description: "Synchronous Cyclic Redundancy Check: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Synchronous Cyclic Redundancy Check component belongs to **Synchronisation and Cyclic Redundancy Check** in the **Complex Device Drivers** layer. It provides synchronous cyclic-redundancy-check computation.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM800A_SyncCrc_Design` | Design package |
| `CM800A_SyncCrc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM800A_SyncCrc_Design` |  |
| Documentation folders | `Design/`, `Reports/` |
| `CM800A_SyncCrc_Impl` |  |
| C sources | `CDD_SyncCrc.c`, `CDD_SyncCrcNonRte.c` |
| Public headers | `CDD_SyncCrc.h`, `CDD_SyncCrc_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `SyncCrc.dcf`, `SyncCrc_attr_def.xml`, `SyncCrc_bswmd.arxml` |
| Generator output | `CDD_SyncCrc_Cfg_private.h.tt`, `SyncCrc_Generate.bat` |
| Tooling and integration scripts | `CM800A_SyncCrc_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `Integrate.bat`, `RteGen.bat`, `SyncCrc.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM800A_SyncCrc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM800A_SyncCrc_Impl/src/CDD_SyncCrc.c`. 

Top-level functions defined in `CDD_SyncCrc.c` (factual extract, first 2):

- `NONTRUSTED_NtWrapS_SyncCrc_RelsCrcHwUnit`
- `NONTRUSTED_NtWrapS_SyncCrc_GetAvlCrcHwUnit`

Additional implementation units: `CM800A_SyncCrc_Impl/src/CDD_SyncCrcNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM800A_SyncCrc_FDD.docx`

- **Source path in repository:** `CM800A_SyncCrc_Design/Design/CM800A_SyncCrc_FDD.docx`
- **Format:** `.docx`
- **Size:** `290 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

**Converted content:**

Synchronous Cyclic Redundancy Check

FDD #CM-800A

1.High Level Description3

2.Derived Requirements3

3.Sub-Function Data Flow3

4.Design Rationale3

5.Sub-Functions4

5.1.Management of CRC Hardware Units4

5.1.1.Initialization of Management RAM (SyncCrcInit0)5

5.1.2.RTE Initialization (SyncCrcInit1)5

5.1.3.Sub-Function: RelsCrcHwUnit5

5.1.4.Sub-Function: GetAvlCrcHwUnit6

5.1.5.Sub-Function: ResvCrcHwUnit7

5.2.SyncCrc API Functions9

5.2.1.Sub-Function: 32-Bit Ethernet CRC10

5.2.1.1.Hardware Related Design10

5.2.1.2.Software Related Design10

5.2.1.2.1.Calc32BitCrc_u0810

5.2.1.2.2.Calc32BitCrc_u1611

5.2.1.2.3.Calc32BitCrc_u3211

5.2.2.Sub-Function: 16-Bit CRC12

5.2.2.1.Hardware Related Design12

5.2.2.2.Software Related Design12

5.2.2.2.1.Calc16BitCrc_u0812

5.2.2.2.2.Calc16BitCrc_u1612

5.2.3.Sub-Function: 8-Bit SAE-J1850 CRC13

5.2.3.1.Hardware Related Design13

5.2.3.2.Software Related Design13

5.2.3.2.1.Calc8BitCrc13

5.2.4.Sub-Function: 8-Bit 0x2F CRC14

5.2.4.1.Hardware Related Design14

5.2.4.2.Software Related Design14

5.2.4.2.1.Calc8BitCrc0X2F14

5.3.Sub-Function: AUTOSAR API Wrapper15

5.3.1.Sub-Function: Crc_CalculateCRC3215

5.3.2.Sub-Function: Crc_CalculateCRC1615

5.3.3.Sub-Function: Crc_CalculateCRC815

5.3.4.Sub-Function: Crc_CalculateCRC8H2F15

6.Timing / Execution Constraints16

6.1.Rationale / Comments16

6.2.Rates and State Execution16

7.Serial Communications Interfaces16

8.Additional Information16

9.Revision Record & Change Approval17

## High Level Description

This document describes the design of the application programming interface (API) to allow application software components (SWCs) to interact with the cyclic redundancy check (CRC) hardware peripheral included in the microcontroller in EA4 hardware.

## Derived Requirements

N/A

## Sub-Function Data Flow

The follow block diagram depicts how the data flow inside the microcontroller CRC peripheral.

## Design Rationale

The design of the API was intended to meet the AUTOSAR CRC API definition as closely as possible. This allows the software configuration to utilize the hardware instead of using software libraries to save on throughput for software calculations. While the direct API does not match the AUTOSAR API definitions, wrapper functions are included to interface with components using the AUTOSAR API with the SyncCRC API.

## Sub-Functions

### Management of CRC Hardware Units

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_48, CM800A_49, CM800A_50, CM800A_67, CM800A_68, CM800A_69, CM800A_70, CM800A_81

The software implementation shall provide a mechanism to utilize one of the CRC hardware units for a synchronous CRC calculation from a software component calling one of the API functions. Upon completion of the job, the software shall release the hardware unit to be available by another software component. This management shall be implemented by a RAM table that has holds the task ID and the of the CRC hardware index. No periodic function is required to manage the RAM since the calculations are synchronous, released at the end of the API call, or permanently reserved. Furthermore, each API function will update the RAM after the job has been completed.

The implementation shall also provide a way to reserve one or more units to dedicate to a particular function if a program requires. The reservation shall be done by the pre-compile configuration or by a function call. The pre-compile configuration shall provide a permanent reservation of the CRC hardware unit. The reservation shall start from the highest hardware index. Any hardware CRC unit that is permanently reserved shall not be used by the SyncCRC API or a temporary reservation of a hardware CRC unit and should be considered as not enabled or available.

The function call shall provide a temporary allocation of one of the available, non-permanently reserved, CRC hardware units. This CRC hardware unit shall be reserved until the calling function releases it. The details of this function are described later in this document.

The management shall also provide protection from preemption of higher priority tasks by utilizing the OS task ID of the calling function as an authority to use that CRC hardware unit.

An example of the RAM table is shown below. Hardware index 0 is temporarily reserved. Hardware index 1 is assigned to task ID 2 until the calculation has completed. Index 2 is available for the next caller. Hardware index 3 is permanently reserved and not available to software applications invoking the API, but is be available to a dedicated source if required by the program.

#### Initialization of Management RAM (SyncCrcInit0)

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_71, CM800A_50

The RAM shall be initialized according to the following pseudo code. This allows the pre-compile configuration to block access to the CRC hardware units that are not available to the application software components. In order for this to be effective, the initialization is required to be scheduled before any software components invoke the API. This function shall be called from outside of the RTE during “cold init.”

For each CRC Hardware Unit:

CrcHwSts[HwUnit].TaskId = Invalid Task ID

If HwIdx < Number of Active Hardware Units:

CrcHwSts[HwUnit].CrcHwSts = Available

Else:

CrcHwSts[HwUnit].CrcHwSts = Crc Not Enabled

End If

End For Loop

#### RTE Initialization (SyncCrcInit1)

This function stub is required to properly place the SyncCrc component within the correct application within a program. This function is called by the RTE during initialization.

#### Sub-Function: RelsCrcHwUnit

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_48

This sub-function shall be used by the API to release a CRC hardware unit. This shall be called after the CRC calculation is complete for any of the API functions calls. The operation of the function shall meet the following pseudo code.

Function Inputs:

CrcHwIdx := This value represents which hardware index the action should go against.

Function Outputs:

Void

Function:

CrcHwSts[CrcHwIdx].TaskId = Invalid Task ID

CrcHwSts[CrcHwIdx].CrcHwSts = Available

#### Sub-Function: GetAvlCrcHwUnit

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_48, CM800A_67, CM800A_81

This sub-function shall be used by the API to allocate a CRC hardware unit for the caller. This shall be called at the start of any of the CRC API functions calls. The operation of the function shall meet the following pseudo code. The ReserveTaskId is a set of four (4) known values that will be used for the task ID of a hardware unit that is temporarily reserved.

Function Inputs:

ResvCrcCall := Input to decide if the call is for a Crc unit reservation or a standard synchronous

calculation.

Function Outputs:

Void

Function:

GetTaskId(TaskId)

EnterExclusiveArea()

For each Active CRC Hardware Unit:

If CrcHwIdxSts == Available:

If ResvCrcCall == False:

CrcHwSts[CrcHwIdx].CrcHwSts = Busy

CrcHwSts[CrcHwIdx].TaskId = TaskId

Else:

CrcHwSts[CrcHwIdx].CrcHwSts = Reserve

CrcHwSts[CrcHwIdx].TaskId = ReserveTaskId[CrcHwIdx]

End If

Break For Loop

End If

End For Loop

ExitExclusiveArea()

#### Sub-Function: ResvCrcHwUnit

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_48, CM800A_67, CM800A_68, CM800A_70

This function shall allow components to reserve a single hardware unit to compute a larger CRC utilizing hardware features, such as DMA. The function shall temporarily reserve the hardware unit until released by the component. A reservation key will be provided when an index is reserved. This key will need to be stored in the caller’s RAM as it is used to determine which hardware index to release when called.

Pseudo code notes:

The function CrcRegConfig() is not a function

It represents setting the DCRA register sections ISZ and POL, and setting COUT to the StartValue to meet the desired CRC calculation as desired by CrcConfg.

LoopCrcHwIdxInReg and LoopCrcHwIdxOutReg are the CIN and COUT for each of the CRC hardware units.

Function Inputs:

In: Mode := 1= CRCHWRESVMOD_RESV, 0= CRCHWRESVMOD_RELS

In: CrcConfig := See table below

| Enumeration | CrcConfig (Enum Value) | DCRAnISZ | DCRAnPOL | Meaning |

| --- | --- | --- | --- | --- |

| CRCHWRESVCFG_32BITCRC32BITWIDTH | 0 | 0 | 0 | 32-Bit CRC / 32-Bit Access Width |

| CRCHWRESVCFG_32BITCRC16BITWIDTH | 1 | 0 | 1 | 32-Bit CRC / 16-Bit Access Width |

| CRCHWRESVCFG_32BITCRC8BITWIDTH | 2 | 0 | 2 | 32-Bit CRC / 8-Bit Access Width |

| CRCHWRESVCFG_16BITCRC16BITWIDTH | 3 | 1 | 1 | 16-Bit CRC / 16-Bit Access Width |

| CRCHWRESVCFG_16BITCRC8BITWIDTH | 4 | 1 | 2 | 16-Bit CRC / 8-Bit Access Width |

| CRCHWRESVCFG_8BITCRC | 5 | 2 | 2 | 8-Bit CRC / 8-Bit Access Width (SAE-J 1850) |

| CRCHWRESVCFG_8BITCRCH2F | 6 | 3 | 2 | 8-Bit CRC / 8-Bit Access Width (Polynomial 0x2F) |

Enumeration

CrcConfig (Enum Value)

DCRAnISZ

DCRAnPOL

Meaning

CRCHWRESVCFG_32BITCRC32BITWIDTH

0

0

0

32-Bit CRC / 32-Bit Access Width

CRCHWRESVCFG_32BITCRC16BITWIDTH

1

0

1

32-Bit CRC / 16-Bit Access Width

CRCHWRESVCFG_32BITCRC8BITWIDTH

2

0

2

32-Bit CRC / 8-Bit Access Width

CRCHWRESVCFG_16BITCRC16BITWIDTH

3

1

1

16-Bit CRC / 16-Bit Access Width

CRCHWRESVCFG_16BITCRC8BITWIDTH

4

1

2

16-Bit CRC / 8-Bit Access Width

CRCHWRESVCFG_8BITCRC

5

2

2

8-Bit CRC / 8-Bit Access Width (SAE-J 1850)

CRCHWRESVCFG_8BITCRCH2F

6

3

2

8-Bit CRC / 8-Bit Access Width (Polynomial 0x2F)

Out: CrcHwIdxInReg

Out: CrcHwIdxOutReg

In: StartValue

In/Out: ResvKey

Function Outputs:

Standard Return

OK = Successful reservation.

NOT_OK = Reservation failed, CRC not configured.

Function:

FuncReturn = NOT_OK

If Mode == Reserve and CrcConfig < 7:

For each Active CRC Hardware Unit:

If CrcHwIdxSts == Available:

GetAvlCrcHwUnit(TRUE)

ResvKey = ReserveTaskId[CrcHwLoopIdx]

CrcResvd = TRUE

CrcHwIdx = CrcHwLoopIdx

Break For Loop

End If

End For Loop

If (CrcResvd == TRUE):

CrcRegConfig(CrcConfig, StartValue)

CrcHwIdxInReg = Address of Selected Index Input Register

CrcHwIdxOutReg = Address of Selected Output Register

FuncReturn = OK

End If

If(FuncReturn == NOT_OK):

CrcHwIdxInReg = 0

CrcHwIdxOutReg = 0

ResvKey = 0

End If

Else If Mode == Release:

/* Release path */

For each Active CRC Hardware Unit:

If ((CrcHwIdxSts == Reserved) and

(ResvKey = CrcHwSts[CrcHwIdx].Taskid)):

RelsCrcHwUnit(CrcHwIdx)

FuncReturn = OK

Break For Loop

End If

End For Loop

If(FuncReturn == NOT_OK):

CrcHwIdxInReg = 0

CrcHwIdxOutReg = 0

ResvKey = 0

End If

Else:

FuncReturn = NOT_OK

CrcHwIdxInReg = 0

CrcHwIdxOutReg = 0

ResvKey = 0

End If

### SyncCrc API Functions

#REQ: The following requirement(s) are met by the design feature below: Requirement ID:  CM800A_64, CM800A_66

The functions defined in the following sub sections shall follow the following format and functionally meet the pseudo code.

Function Inputs:

In/Out: DataPtr_Arg†

In: Len_Arg

In: StrtVal_Arg†

In: FirstCall_Arg

In/Out: CalcCrcRes_Arg†

† - Argument data type depends on the API function (choices are 8, 16, or 32-bit).

Function Outputs:

Standard Return

OK = Successful CRC calculation.

NOT_OK = CRC Hardware unit could not be reserved, no calculation performed. CalcCrcRes_Arg shall be set to 0.

Function:

ErrRtn = OK

GetTaskId(TaskId)

GetAvlCrcHwUnit()

For each Active CRC Hardware Unit:

If TaskId == RAMTable.TaskId:

CrcHwIdx = LoopIdx

Break For Loop

End If

End For Loop

If CrcHwIdx != Invalid CRC Index:

CrcRegConfig() /* Configure Registers for the function type */

If FirstCall_Arg == True:

COUT = Default CRC Init Value

Else:

COUT = StrtVal_Arg

End If

For 0 to Len_Arg:

CIN = DataPtr[LenIdx]

End For

CalcCrcRes_Arg = COUT

RelsCrcHwUnit(CrcHwIdx)

Else:

CalcCrcRes_Arg = 0

ErrRtn = NOT_OK

End If

#### Sub-Function: 32-Bit Ethernet CRC

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_52, CM800A_64

The CRC module shall implement the CRC32 routine based on the IEEE-802.3 CRC32 Ethernet Standard. In the event a CRC cannot be calculated the function shall return a CRC result of 0 and notify the calling software component that the CRC result was not calculated.

#### Hardware Related Design

N/A

#### Software Related Design

#REQ: The following requirement(s) are met by the design feature below: Requirement ID: CM800A_53, CM800A_54


*... content truncated for brevity; see the source document in the repository. ...*

### `CM800A_SyncCrc_DDReport.txt`

- **Source path in repository:** `CM800A_SyncCrc_Design/Reports/CM800A_SyncCrc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM800A_SyncCrc_DataDict
13-Jan-2016 09:08:42
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
(variables: 2, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
Calc16BitCrc_u08            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Calc16BitCrc_u16            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Calc32BitCrc_u08            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Calc32BitCrc_u16            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Calc32BitCrc_u32            	    Crc_u          Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 8, errors: 5)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

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
```
*... truncated (37 more lines in the source file). ...*

### `CM800A_SycnCrc_MDD.docx`

- **Source path in repository:** `CM800A_SyncCrc_Impl/doc/CM800A_SycnCrc_MDD.docx`
- **Format:** `.docx`
- **Size:** `1392 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

SyncCrc

January 11, 2016

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

| Initial Version | K. Smith | 1 | 07-Oct-15 |  |

| Updates to meet the Rev1 of the FDD | K. Smith | 2 | 1 1 - Jan -1 6 |  |

Description

Author

Version

Date

Approved By

Initial Version

K. Smith

1

07-Oct-15

Updates to meet the Rev1 of the FDD

K. Smith

2

11-Jan-16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2SyncCrc & High-Level Description6

3Design details of software module7

3.1Graphical representation of SyncCrc7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

4.2Variable Data Dictionary8

4.2.1User Defined Typedef Definition/Declaration8

4.2.2User Defined Enumerated Types9

5Software Component Implementation10

5.1Sub-Module Functions10

5.1.1Init: SyncCrcInit010

5.1.1.1Design Rationale10

5.1.1.2Processing10

5.1.1.3Module Outputs10

5.1.2Init: SyncCrcInit110

5.1.2.1Design Rationale10

5.1.2.2Processing10

5.1.2.3Module Outputs10

5.2Server Runnables11

5.2.1ResvCrcHwUnit11

5.2.1.1Design Rationale11

5.2.1.2(Processing of function)………11

5.2.1.3Module Outputs13

5.2.2CRC API Server Runnables14

5.2.2.1API Design Rationale14

5.2.2.2API Processing14

5.3Interrupt Functions17

5.4Module Internal (Local) Functions17

5.4.1RelsCrcHwUnit17

5.4.1.1Design Rationale17

5.4.1.2Processing17

5.4.2NONTRUSTED_NtWrapS_SyncCrc_RelsCrcHwUnit17

5.4.2.1Design Rationale17

5.4.2.2Processing18

5.4.3GetAvlCrcHwUnit18

5.4.3.1Design Rationale18

5.4.3.2Processing18

5.4.4NONTRUSTED_NtWrapS_SyncCrc_GetAvlCrcHwUnit19

5.4.4.1Design Rationale19

5.4.4.2Processing19

5.4.5CrcRegCfg19

5.4.5.1Design Rationale19

5.4.5.2Processing19

5.5GLOBAL Function/Macro Definitions21

6Known Limitations with Design22

7UNIT TEST CONSIDERATION23

Appendix AAbbreviations and Acronyms24

Appendix BGlossary25

Appendix CReferences26

## Introduction

### Purpose

This MDD aids in documenting the implementation of CM800A for the synchronous CRC API with the EA4 hardware CRC units.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## SyncCrc & High-Level Description

Provides an API interface for other BSW and application level software components to calculate a synchronous CRC calculation using the EA4 hardware peripherals.

## Design details of software module

### Graphical representation of SyncCrc

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

Values between the brackets [] are the ranges that the configurable constants could be defined as for a given integration. These values are generated by Configurator before the software build.

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| CRCININVAL8BIT_CNT_U08 | Uint8 | Cnt | 0xFF |

| CRCININVAL16BIT_CNT_U16 | Uint16 | Cnt | 0xFFFF |

| CRCININVAL32BIT_CNT_U32 | Uint32 | Cnt | 0xFFFFFFFF |

| CRCERRVAL_CNT_U08 | Uint8 | Cnt | 0 |

| CRCHWRESVCFGRNG_CNT_U08 | Uint8 | Cnt | 7 |

| INVLDTASKID_CNT_U16 | Uint16 | Cnt | 0xFFFF |

| NROFCRCHWUNIT_CNT_U08 | Uint8 | Cnt | 4 |

| NROFACTVCRCHWUNIT_CNT_U08 | Uint8 | Cnt | [0 – 4]* |

| ARWRPRENAD_CNT_U08 | Uint8 | Cnt | [STD_O FF  – STD_O N ]** |

| CRCOSREF_CNT_U08 | Uint8 | Cnt | [0-255]*** |

Constant Name

Resolution

Units

Value

CRCININVAL8BIT_CNT_U08

Uint8

Cnt

0xFF

CRCININVAL16BIT_CNT_U16

Uint16

Cnt

0xFFFF

CRCININVAL32BIT_CNT_U32

Uint32

Cnt

0xFFFFFFFF

CRCERRVAL_CNT_U08

Uint8

Cnt

0

CRCHWRESVCFGRNG_CNT_U08

Uint8

Cnt

7

INVLDTASKID_CNT_U16

Uint16

Cnt

0xFFFF

NROFCRCHWUNIT_CNT_U08

Uint8

Cnt

4

NROFACTVCRCHWUNIT_CNT_U08

Uint8

Cnt

[0 – 4]*

ARWRPRENAD_CNT_U08

Uint8

Cnt

[STD_OFF – STD_ON]**

CRCOSREF_CNT_U08

Uint8

Cnt

[0-255]***

* Based on the value of “Available CRC Hardware Units” as defined in Configurator.** Based on the value of “Autosar Wrapper Enable” as defined in Configurator.***Based on the value of “Crc Os Application Reference” as defined in Configurator.

### Variable Data Dictionary

The following type definitions are found in the private header of this component.

#### User Defined Typedef Definition/Declaration

| Typedef  Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| NtCrcIdRec | CrcHwIdx | Uint8 | 0 | 255 |

| NtResvCallRec | ResvCall | Boolean | FALSE | TRUE |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

NtCrcIdRec

CrcHwIdx

Uint8

0

255

NtResvCallRec

ResvCall

Boolean

FALSE

TRUE

#### User Defined Enumerated Types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

| CrcDataAcsWidth1 | CRCDATAACSWIDTH_32BIT | 0 |

|  | CRCDATAACSWIDTH_16BIT | 1 |

|  | CRCDATAACSWIDTH_8BIT | 2 |

| CrcAlg1 | CRCALG_32BITETH | 0 |

|  | CRCALG_16BIT | 1 |

|  | CRCALG_8BIT | 2 |

|  | CRCALG_8BITH2F | 3 |

Enum  Name

Element Name

Value

CrcDataAcsWidth1

CRCDATAACSWIDTH_32BIT

0

CRCDATAACSWIDTH_16BIT

1

CRCDATAACSWIDTH_8BIT

2

CrcAlg1

CRCALG_32BITETH

0

CRCALG_16BIT

1

CRCALG_8BIT

2

CRCALG_8BITH2F

3

## Software Component Implementation

### Sub-Module Functions

### Init: SyncCrcInit0

### Design Rationale

This function initializes the PIM with the proper status for the CRC hardware units for use by the application components.  This function is defined in the CDD_SyncCrcNonRte.c file as it shall be called prior to the RTE Init functions.

### Processing

### Module Outputs

None

### Init: SyncCrcInit1

### Design Rationale

Stub function for mapping the server runnable functions within a memory region.

### Processing

None

### Module Outputs

None

### Server Runnables

### ResvCrcHwUnit

### Design Rationale

This function allows the caller to reserve a single CRC hardware unit until it is released. This will allow features such as the DMA to perform a CRC calculation over a large portion of data and does not need to permanently reserve a CRC hardware unit. This function can be called from within or outside a task. This server runnables must be defined with “can be invoked concurrently” enabled in Developer.

### (Processing of function)………

#### Top Level Logic

#### Reserve CRC

#### Release CRC

### Module Outputs

None

### CRC API Server Runnables

### API Design Rationale

The following flow chart is applicable to all CRC API functions in this document. However, the highlighted green squares vary by the API. These differences will be pointed out in each sub-function section. All API client calls must be called from within a task. These server runnables must be defined with “can be invoked concurrently” enabled in Developer.

### API Processing

#### Calc8BitCrc_Oper

DCRA[CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH_8BIT;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_8BIT;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL8BIT_CNT_U16;

#### Calc8BitCrc0X2F_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH_8BIT;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_8BITH2F;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL8BIT_CNT_U16;

#### Calc16BitCrc_u08_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_16BIT;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL16BIT_CNT_U16;

#### Calc16BitCrc_u16_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH_16BIT;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_16BIT;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL16BIT_CNT_U16;

#### Calc32BitCrc_u08_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_32BITETH;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL32BIT_CNT_U16;

#### Calc32BitCrc_u16_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH_16BIT;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_32BITETH;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL32BIT_CNT_U16;

#### Calc32BitCrc_u32_Oper

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.ISZ = CRCDATAACSWIDTH_32BIT;

DCRA [CrcHwIdx_Cnt_T_u08].CTL.BIT.POL = CRCALG_32BITETH;

DCRA [CrcHwIdx_Cnt_T_u08].COUT = CRCININVAL32BIT_CNT_U16;

### Interrupt Functions

None

### Module Internal (Local) Functions

### RelsCrcHwUnit

| Function Name | RelsCrcHwUnit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CrcHwIdx_Cnt_T_u08 | Uint8 | 0 | 3 |

| Return Value | N/A |  |  |  |

Function Name

RelsCrcHwUnit

Type

Min

Max

Arguments Passed

CrcHwIdx_Cnt_T_u08

Uint8

0

3

Return Value

N/A

### Design Rationale

To minimize time in Exclusive areas, the Enter and Exit calls were placed within this function. All API server runnables that use this function are defined in Developer to have access to the exclusive area.

### Processing

### NONTRUSTED_NtWrapS_SyncCrc_RelsCrcHwUnit

| Function Name | NONTRUSTED_NtWrapS_SyncCrc_RelsCrcHwUni t | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FunctionIndex | Uint16 | 0 | 65535 |

|  | FunctionParams | Void* | 0 | 2^32-1 |

| Return Value | N/A |  |  |  |

Function Name

NONTRUSTED_NtWrapS_SyncCrc_RelsCrcHwUnit

Type

Min

Max

Arguments Passed

FunctionIndex

Uint16

0

65535

FunctionParams

Void*

0

2^32-1

Return Value

N/A

### Design Rationale

Function is required to prevent MPU violations when the API modifies the per-instance-memory used by all API functions.

### Processing

### GetAvlCrcHwUnit

| Function Name | GetAvl CrcHwUnit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | N/A |  |  |  |

| Return Value | N/A |  |  |  |

Function Name

GetAvlCrcHwUnit

Type

Min

Max

Arguments Passed

N/A

Return Value

N/A

### Design Rationale

### Processing

### NONTRUSTED_NtWrapS_SyncCrc_GetAvlCrcHwUnit

| Function Name | NONTRUSTED_NtWrapS_SyncCrc_ GetAvl CrcHwUni t | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | FunctionIndex | Uint16 | 0 | 65535 |

|  | FunctionParams | Void* | 0 | 2^32-1 |

| Return Value | N/A |  |  |  |

Function Name

NONTRUSTED_NtWrapS_SyncCrc_GetAvlCrcHwUnit

Type

Min

Max

Arguments Passed

FunctionIndex

Uint16

0

65535

FunctionParams

Void*

0

2^32-1

Return Value

N/A

### Design Rationale

Function is required to prevent MPU violations when the API modifies the per-instance-memory used by all API functions.

### Processing

### CrcRegCfg

| Function Name | CrcRegCfg | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CrcHwIdx_Arg | Uint8 | 0 | 255 |

|  | CrcCfg_Arg | CrcHwResvCfg1 | 0 | 6 |

|  | StrtVal_Arg | Uint32 | 0 | 4294967295 |

| Return Value | N/A |  |  |  |

Function Name

CrcRegCfg

Type

Min

Max

Arguments Passed

CrcHwIdx_Arg

Uint8

0

255

CrcCfg_Arg

CrcHwResvCfg1

0

6

StrtVal_Arg

Uint32

0

4294967295

Return Value

N/A

### Design Rationale

Function created to reduce the complexity of the ResvCrcHwUnit_Oper function.

### Processing

### GLOBAL Function/Macro Definitions

None

## Known Limitations with Design

API client calls, except ResvCrcHwUnit, must be called from within a task.

To meet design and coding standards, ‘For’ loops called out by the FDD were implemented with ‘While’ loops to break out of the loops without using the ‘break’ keyword.

## UNIT TEST CONSIDERATION

The constants NROFACTVCRCHWUNIT_CNT_U08, ARWRPRENAD_CNT_U08, and CRCOSREF_CNT_U08 shall be tested to their full range as defined in the constant section.

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

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |


*... content truncated for brevity; see the source document in the repository. ...*

### `CM800A_SyncCrc_Integration_Manual.doc`

- **Source path in repository:** `CM800A_SyncCrc_Impl/doc/CM800A_SyncCrc_Integration_Manual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
