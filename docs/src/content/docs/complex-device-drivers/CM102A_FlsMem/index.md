---
title: "Flash Memory (CM102A_FlsMem)"
description: "Flash Memory: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Flash Memory component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM102A_FlsMem_Design` | Design package |
| `CM102A_FlsMem_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM102A_FlsMem_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM102A_FlsMem_Impl` |  |
| C sources | `CDD_FlsMem.c`, `CDD_FlsMemNonRte.c` |
| Public headers | `CDD_FlsMem.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `FlsMem.dcf`, `FlsMem_attr_def.xml`, `FlsMem_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `CDD_FlsMem_Cfg.c.tt`, `CDD_FlsMem_Cfg_private.h.tt`, `FlsMem_Generate.bat` |
| Tooling and integration scripts | `CM102A_FlsMem_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreateQACProject.bat`, `FlsMem.dpa`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `CM102A_FlsMem_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM102A_FlsMem_Impl/src/CDD_FlsMem.c`. 

Top-level functions defined in `CDD_FlsMem.c` (factual extract, first 1):

- `DtsClnUp`

Additional implementation units: `CM102A_FlsMem_Impl/src/CDD_FlsMemNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM102A_FlsMem.doc`

- **Source path in repository:** `CM102A_FlsMem_Design/Design/CM102A_FlsMem.doc`
- **Format:** `.doc`
- **Size:** `607 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM102A_FlsMem_DDReport.txt`

- **Source path in repository:** `CM102A_FlsMem_Design/Reports/CM102A_FlsMem_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM102A_FlsMem_DataDict
31-Aug-2016 16:25:18
Tool Release:  2.41.0



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
CodFlsSngBitEcc             	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
FlsMemInit2                 	.Runnnable:	TimeStep should be a either 'ISR' or 'MotorControl' or 'MotorControlx2' when Context is 'NonRte'.
(variables: 4, errors: 2)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 5, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
RegInpINTIFPINT0            	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpINTIFPINT0            	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpINTIFPINT0            	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 1, errors: 3)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
CodFlsCrcChkCmpl            	Cannot match name to list of known Nexteer signals.
RegOutINTIFPINTCLR0         	Cannot match name to list of known Nexteer signals.
RegOutINTIFPINTCLR0         	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutINTIFPINTCLR0         	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutINTIFPINTCLR0         	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 2, errors: 5)

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
```
*... truncated (42 more lines in the source file). ...*

### `FlsMem Integration Manual.doc`

- **Source path in repository:** `CM102A_FlsMem_Impl/doc/FlsMem Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `160 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `FlsMem Module Design Document.docx`

- **Source path in repository:** `CM102A_FlsMem_Impl/doc/FlsMem Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `314 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

FlsMem

Aug 25 , 2016

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

| Initial Version | Lucas  Wendling | 1 .0 | 10/06/15 |

| Updated with changes for DTS configuration for Flash CRC check | Avinash  James | 2.0 | 03 / 18 /16 |

| Updates for DTS Transfer Clear | Avinash  James | 3.0 | 3/29/16 |

| Updated for removing the flash ECC single bit error handling  and disabling the DTS channels  after c a l culation | Avinash  James | 4.0 | 3/31/16 |

| Trusted function call for the DTS clean up updates | Avinash  James | 5.0 | 04/18/16 |

| Function name changes and added  CodFlsSngBitEcc  handler for single bit code flash  ecc | Avinash  James | 6.0 | 08/25/16 |

Description

Author

Version

Date

Initial Version

Lucas Wendling

1.0

10/06/15

Updated with changes for DTS configuration for Flash CRC check

Avinash James

2.0

03/18/16

Updates for DTS Transfer Clear

Avinash James

3.0

3/29/16

Updated for removing the flash ECC single bit error handling and disabling the DTS channels after calculation

Avinash James

4.0

3/31/16

Trusted function call for the DTS clean up updates

Avinash James

5.0

04/18/16

Function name changes and added CodFlsSngBitEcc handler for single bit code flash ecc

Avinash James

6.0

08/25/16

Table of Contents1Introduction5

1.1Purpose5

1.2Scope5

2FlsMem & High-Level Description6

3Design details of software module7

3.1Graphical representation of FlsMem7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Variable Data Dictionary9

5.1User defined typedef definition/declaration9

5.2Variable definition for enumerated types9

6Software Component Implementation10

6.1Sub-Module Functions10

6.1.1Init: FlsMemInit110

6.1.1.1Design Rationale10

6.1.1.2Module Outputs10

6.1.2Init: FlsMemInit210

6.1.2.1Design Rationale10

6.1.2.2Module Outputs10

6.1.3Per: FlsMemPer210

6.1.3.1Design Rationale10

6.1.3.2Store Module Inputs to Local copies10

6.1.3.3(Processing of function)………10

6.1.3.4Store Local copy of outputs into Module Outputs10

6.2Server Runnables11

6.3Interrupt Functions11

6.4Module Internal (Local) Functions11

6.4.1Local Function #111

6.4.1.1Design Rationale11

6.4.1.2Processing11

6.5GLOBAL Function/Macro Definitions11

6.5.1DTSInit11

6.5.1.1Design Rationale11

6.5.1.2Processing14

6.5.2DTSClnUp14

6.5.2.1Design Rationale14

6.5.2.2Processing14

7Known Limitations with Design15

8UNIT TEST CONSIDERATION16

Appendix AAbbreviations and Acronyms17

Appendix BGlossary18

Appendix CReferences19

## Introduction

### Purpose

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## FlsMem & High-Level Description

See FDD

## Design details of software module

### Graphical representation of FlsMem

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

| CPU1PEID_CNT_U32 | 1 | uint32 | 0x01U |

| CODFLSTOCRCSPID_CNT_U32 | 1 | uint32 | 0x02U |

| CRCTOLCLRAMSPID_CNT_U32 | 1 | uint32 | 0x00U |

| USRMODDIS_CNT_U32 | 1 | uint32 | 0x00U |

| FLSBLKLEN_CNT_U32 | 1 | uint32 | 0x0003FFFCU |

| DTSDATALEN_CNT_U32 | 1 | uint32 | 4U |

| CRCCHKMAXALLWDTI_CNT_U32 | 1 | uint32 | 2000 |

| MAXNROFDTSCH_CNT_U32 | 1 | uint32 | 32 |

| DUMMYREADADDR1_CNT_U32 | 1 | uint32 | (0xFFFFFE1FU) |

| DUMMYREADADDR2_CNT_U32 | 1 | uint32 | (0xFFFFFE2FU) |

| DUMMYREADADDR3_CNT_U32 | 1 | uint32 | (0xFFFFFE4FU) |

| DUMMYREADADDR4_CNT_U32 | 1 | uint32 | (0xFFFFFE8FU) |

Constant Name

Resolution

Units

Value

CPU1PEID_CNT_U32

1

uint32

0x01U

CODFLSTOCRCSPID_CNT_U32

1

uint32

0x02U

CRCTOLCLRAMSPID_CNT_U32

1

uint32

0x00U

USRMODDIS_CNT_U32

1

uint32

0x00U

FLSBLKLEN_CNT_U32

1

uint32

0x0003FFFCU

DTSDATALEN_CNT_U32

1

uint32

4U

CRCCHKMAXALLWDTI_CNT_U32

1

uint32

2000

MAXNROFDTSCH_CNT_U32

1

uint32

32

DUMMYREADADDR1_CNT_U32

1

uint32

(0xFFFFFE1FU)

DUMMYREADADDR2_CNT_U32

1

uint32

(0xFFFFFE2FU)

DUMMYREADADDR3_CNT_U32

1

uint32

(0xFFFFFE4FU)

DUMMYREADADDR4_CNT_U32

1

uint32

(0xFFFFFE8FU)

## Variable Data Dictionary

### User defined typedef definition/declaration

<This section documents any user types uniquely used for the module.>

| Typedef  Name | Element Name | User Defined Type | Legal Range (min) | Legal Range (max) |

| --- | --- | --- | --- | --- |

| FlsCrcCfgBlkRec | CrcFlsBlkStrtAdr | uint32 | 0 | 0xFFFFFFFF H |

|  | CrcFlsBlkLen | uint32 | 0 | 0xFFFFFFFF H |

|  | PreCalcnCrcFlsAdr | uint32 * | 0 | 0xFFFFFFFF H |

Typedef Name

Element Name

User Defined Type

Legal Range

(min)

Legal Range

(max)

FlsCrcCfgBlkRec

CrcFlsBlkStrtAdr

uint32

0

0xFFFFFFFFH

CrcFlsBlkLen

uint32

0

0xFFFFFFFFH

PreCalcnCrcFlsAdr

uint32*

0

0xFFFFFFFFH

### Variable definition for enumerated types

| Enum    Name | Element Name | Value |

| --- | --- | --- |

| < (Name given for the user defined  typdef  of type  struct /union) (Variable name qualified  in refer[2] ) > | < (Variable name qualified  Refer[2] ) > | <Define the value > |

Enum  Name

Element Name

Value

<(Name given for the user defined typdef of type struct/union)

(Variable name qualified in refer[2])>

<(Variable name qualified Refer[2])>

<Define the value >

## Software Component Implementation

### Sub-Module Functions

### Init: FlsMemInit1

### Design Rationale

Empty function for purposes of memory mapping

### Module Outputs

None

### Init: FlsMemInit2

### Design Rationale

The FlsMemInit2 function is a non RTE function which shall be called to set up the DTS configuration for the Flash CRC check. The DTS channel configuration has to be applied only when the system is waking up from a Power On Reset or after a flash programming reset. In such a scenario a Hardware CRC unit is allocated by function call to the CRC module and once a hardware assignment is successful, the DTS channels are configured for chaining for the entire definition of the flash blocks (Boot, App, Cal1, Cal2 etc.). Record the time when the DTS transfer is initiated so that a check on a timeout can be made in the periodic function where a maximum timeout of 200 ms is checked for

This function shall be called in the startup sequence. Hence it is a non RTE function

See FDD for more.

### Module Outputs

None

None

### Per: FlsMemPer2

### Design Rationale

See FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Server Runnables - CodFlsSngBitEcc

### Design Rationale

See FDD

### Store Module Inputs to Local copies

Refer to FDD

### (Processing of function)………

Refer to FDD

### Store Local copy of outputs into Module Outputs

Refer to FDD

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

| Function Name | (Exact name used) | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> | <Refer MDD guidelines[1]> |

|  |  |  |  |  |

| Return Value |  |  |  |  |

Function Name

(Exact name used)

Type

Min

Max

Arguments Passed

None

<Refer MDD guidelines[1]>

<Refer MDD guidelines[1]>

<Refer MDD guidelines[1]>

Return Value

### Design Rationale

### Processing

### GLOBAL Function/Macro Definitions

### DtsInin

| Function Name | DTSInit | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | CrcHwIdxInReg | uint32 | 0 | 0xFFFFFFFF |

|  | CrcHwIdxOutReg | uint32 | 0 | 0xFFFFFFFF |

| Return Value | None |  |  |  |

Function Name

DTSInit

Type

Min

Max

Arguments Passed

CrcHwIdxInReg

uint32

0

0xFFFFFFFF

CrcHwIdxOutReg

uint32

0

0xFFFFFFFF

Return Value

None

### Design Rationale

Trusted function that performs all register initialization from the CM102A_FlsMem_DTSPeripheralCfg.xlsx spreadsheet in the FDD.  The DTSMstrCfg channel master registers can be written only in supervisor mode.  After the Channel master register for a given channel has been written, the selected Processor Element can write to that channel’s registers.  However, for simplicity, all DTS register initialization and chaining is being done in one trusted function.

The chaining is done in the following manner

Consider the first flash region to have the CRC calculated

Calculate the number of DTS chains required for the length of the CRC region. Each DTS channel can address up to a maximum of 0x3FFFC bytes of data (0xFFFF maximum transfer count multiplied by 4 bytes of data in each transfer).

Hence number of channel is equal to Region length/0x3FFFC + {1} if (Region length % 0x3FFFC is non zero)

Clear the DTS Transfer flag to make sure no pending requests are present for all the used channels

Configure the DTS channels starting from 0 using the configuration defined as per CM102A_FlsMem_DTSPeripheralCfg.xlsx for the above calculated number of chains

Configure the next DTS channel to transfer the CRC result from CRC HW output register to Per Instance Memory

Configure the next DTS channel to transfer zero value to the CRC HW output register to clear the output register to continue with next flash region operation

Repeat Step 1 thru 5 for all the flash regions(Boot, App, Cal1, Cal2 etc) The definition of the flash region is in the generated file CDD_FlsMem_Cfg.c which takes inputs defined in the Vector configurator Tool

Disable chaining on the last channel

Enable the Interrupt on the second last channel

Clear the interrupt status register which shall be monitored in the periodic

Start the DTS transfer

### Processing

### DtsClnUp

| Function Name | DTS ClnUp | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | None |  |  |  |

|  |  |  |  |  |

| Return Value | None |  |  |  |

Function Name

DTSClnUp

Type

Min

Max

Arguments Passed

None

Return Value

None

### Design Rationale

None

### Processing

None

## Known Limitations with Design

We have made use of a static constant global variable (static const uint32 CrcClrData_M = 0U)  for the purpose of clearing the CRC hardware

Also the result array (HwCrcCalcdRes_C[8]) has been also declared as a global array for the purpose of DTS write access in the MotCtrlMgr_MemMap memory map section

In the CodFlsSngBitEcc function in FDD the reads are done to the same variable. In the implementation we have used 4 different variables for the purpose that compiler wont optimize those reads. Any optimization settings change in the compiler would need a reevaluation of the use of volatile temporary variables

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | Software Naming Conventions.doc | 1.0 |

| 4 | Software Design and Coding Standards.doc | 2.0 |

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

Software Naming Conventions.doc

1.0

4

Software Design and Coding Standards.doc

2.0

Back to [Complex Device Drivers](../).
