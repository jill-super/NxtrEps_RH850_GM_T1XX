---
title: "Exception Handling (CM101A_ExcpnHndlg)"
description: "Exception Handling: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Exception Handling component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM101A_ExcpnHndlg_Design` | Design package |
| `CM101A_ExcpnHndlg_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM101A_ExcpnHndlg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM101A_ExcpnHndlg_Impl` |  |
| C sources | `CDD_ExcpnHndlg.c`, `CDD_ExcpnHndlgIrq.c`, `CDD_ExcpnHndlgNonRte.c` |
| Public headers | `CDD_ExcpnHndlg.h`, `CDD_ExcpnHndlg_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `ExcpnHndlg.dcf`, `ExcpnHndlg_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM101A_ExcpnHndlg_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `ExcpnHndlg.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM101A_ExcpnHndlg_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `CM101A_ExcpnHndlg_Impl/src/CDD_ExcpnHndlg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM101A_ExcpnHndlg_Impl/src/CDD_ExcpnHndlgIrq.c`, `CM101A_ExcpnHndlg_Impl/src/CDD_ExcpnHndlgNonRte.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM101A_ExcpnHndlg.doc`

- **Source path in repository:** `CM101A_ExcpnHndlg_Design/Design/CM101A_ExcpnHndlg.doc`
- **Format:** `.doc`
- **Size:** `2392 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `CM101A_ExcpnHndlg_DDReport.txt`

- **Source path in repository:** `CM101A_ExcpnHndlg_Design/Reports/CM101A_ExcpnHndlg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM101A_ExcpnHndlg_DataDict
31-Mar-2016 16:21:55
Tool Release:  2.35.0



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
AlgnErrIrq                  	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
FpuErrIrq                   	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
ResdOperIrq                 	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
SysErrIrq                   	.Runnnable:	Name must end with 'Init' or 'Per1', 'Per2', etc.
(variables: 7, errors: 4)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
FeNmiOperModErrSngChipInactv	    Chip           Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 24, errors: 1)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 1, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 1, errors: 0)

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
*... truncated (38 more lines in the source file). ...*

### `ExcpnHndlg Integration Manual.doc`

- **Source path in repository:** `CM101A_ExcpnHndlg_Impl/doc/ExcpnHndlg Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `144 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ExcpnHndlg Module Design Document.docx`

- **Source path in repository:** `CM101A_ExcpnHndlg_Impl/doc/ExcpnHndlg Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `109 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

ExcpnHndlg

April 5, 2016

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

| Initial Version | Avinash James | 1.0 | 05 - Apr -201 6 |

Description

Author

Version

Date

Initial Version

Avinash James

1.0

05-Apr-2016

Table of Contents

1Introduction7

1.1Purpose7

1.2Scope7

2ExcpnHndlg & High-Level Description8

3Design details of software module9

3.1Graphical representation of ExcpnHndlg9

3.2Data Flow Diagram9

3.2.1Component level DFD9

3.2.2Function level DFD9

4Constant Data Dictionary10

4.1Program (fixed) Constants10

4.1.1Embedded Constants10

5Software Component Implementation13

5.1Sub-Module Functions13

5.1.1Init: ExcpnHndlgInit113

5.1.1.1Design Rationale13

5.1.1.2Module Outputs13

5.1.2Init: ExcpnHndlgInit213

5.1.2.1Design Rationale13

5.1.2.2Module Outputs13

5.1.3Per: ExcpnHndlgPer113

5.1.3.1Design Rationale13

5.1.3.2Store Module Inputs to Local copies13

5.1.3.3(Processing of function)………13

5.1.3.4Store Local copy of outputs into Module Outputs13

5.2Server Runables13

5.2.1ChkForStrtUpTest13

5.2.1.1Design Rationale13

5.2.1.2(Processing of function)………13

5.2.2FeNmiClkMonr0RtLowrLimFlt14

5.2.2.1Design Rationale14

5.2.2.2(Processing of function)………14

5.2.3FeNmiClkMonr0RtUpprLimFlt14

5.2.3.1Design Rationale14

5.2.3.2(Processing of function)………14

5.2.4FeNmiClkMonr1RtLowrLimFlt14

5.2.4.1Design Rationale14

5.2.4.2(Processing of function)………14

5.2.5FeNmiClkMonr1RtUpprLimFlt14

5.2.5.1Design Rationale14

5.2.5.2(Processing of function)………14

5.2.6FeNmiClkMonr2RtLowrLimFlt14

5.2.6.1Design Rationale14

5.2.6.2(Processing of function)………14

5.2.7FeNmiClkMonr2RtUpprLimFlt14

5.2.7.1Design Rationale14

5.2.7.2(Processing of function)………15

5.2.8FeNmiClkMonr3RtLowrLimFlt15

5.2.8.1Design Rationale15

5.2.8.2(Processing of function)………15

5.2.9FeNmiClkMonr3RtUpprLimFlt15

5.2.9.1Design Rationale15

5.2.9.2(Processing of function)………15

5.2.10FeNmiDmaTrf15

5.2.10.1Design Rationale15

5.2.10.2(Processing of function)………15

5.2.11FeNmiDmaRegAcsProtnErr15

5.2.11.1Design Rationale15

5.2.11.2(Processing of function)………15

5.2.12FeNmiEcmMstChkrCmp15

5.2.12.1Design Rationale15

5.2.12.2(Processing of function)………15

5.2.13FeNmiOperModErrFlsProgmModStrtd16

5.2.13.1Design Rationale16

5.2.13.2(Processing of function)………16

5.2.14FeNmiOperModErrSngChipInactv16

5.2.14.1Design Rationale16

5.2.14.2(Processing of function)………16

5.2.15FeNmiOperModErrTestModStrtd16

5.2.15.1Design Rationale16

5.2.15.2(Processing of function)………16

5.2.16FeNmiPeg16

5.2.16.1Design Rationale16

5.2.16.2(Processing of function)………16

5.2.17FeNmiWdg16

5.2.17.1Design Rationale16

5.2.17.2(Processing of function)………16

5.2.18GetMcuDiagcIdnData17

5.2.18.1Design Rationale17

5.2.18.2(Processing of function)………17

5.2.19ProcMpuExcpnErr17

5.2.19.1Design Rationale17

5.2.19.2(Processing of function)………17

5.2.20ProcNonCritOsErr17

5.2.20.1Design Rationale17

5.2.20.2(Processing of function)………17

5.2.21ProcPrmntOsErr17

5.2.21.1Design Rationale17

5.2.21.2(Processing of function)………17

5.2.22ProcPrvlgdInstrExcpnErr17

5.2.22.1Design Rationale17

5.2.22.2(Processing of function)………17

5.2.23ProcUkwnExcpnErr18

5.2.23.1Design Rationale18

5.2.23.2(Processing of function)………18

5.2.24SetMcuDiagcIdnData18

5.2.24.1Design Rationale18

5.2.24.2(Processing of function)………18

5.3Interrupt Functions18

5.3.1AlgnErrIrq18

5.3.1.1Design Rationale18

5.3.1.2(Processing of the ISR function)…..18

5.3.2FpuErrIrq18

5.3.2.1Design Rationale18

5.3.2.2(Processing of the ISR function)…..18

5.3.3SysErrIrq18

5.3.3.1Design Rationale18

5.3.3.2(Processing of the ISR function)…..18

5.3.4ResdOperIrq19

5.3.4.1Design Rationale19

5.3.4.2(Processing of the ISR function)…..19

5.4Module Internal (Local) Functions19

5.4.1ProcStrtUpOrSwRst19

5.4.1.1Design Rationale19

5.4.1.2Processing19

5.4.2ProcEcmRst19

5.4.2.1Design Rationale19

5.4.2.2Processing19

5.4.3ProcPinRst19

5.4.3.1Design Rationale20

5.4.3.2Processing20

5.5GLOBAL Function/Macro Definitions20

5.5.1GLOBAL Function #120

5.5.1.1Design Rationale20

5.5.1.2processing20

6Known Limitations with Design21

7UNIT TEST CONSIDERATION22

Appendix AAbbreviations and Acronyms23

Appendix BGlossary24

Appendix CReferences25

## Introduction

### Purpose

This document details the design in the FDD and also lists out any deviations which were made from the design for the implementation due to any constraints in development. ExcpnHndlg MDD describes the exception handling / reset cause determination for microcontroller diagnostics

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## ExcpnHndlg & High-Level Description

Refer FDD

## Design details of software module

### Graphical representation of ExcpnHndlg

### Data Flow Diagram

#### Component level DFD

N/A

#### Function level DFD

N/A

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| FPCFGININVAL_CNT_T_U32 | 1 | Counts | 0x0000001CU |

| FPCFGREGID_CNT_S32 | 1 | Counts | 10 |

| FPCFGSELNID_CNT_S32 | 1 | Counts | 0 |

| FPUINVLDOPERSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00004000U)) |

| FPUDIVBYZEROSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00002000U)) |

| FPUOVFSTSBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00001000U)) |

| MEMERRINFOREADWRBIT_CNT_U32 | 1 | Counts | ((uint32)(0x00000001U)) |

| CF1STERSTRADRPARMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000004U)) |

| CF1STERSTRDBLBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000002U)) |

| CF1STERSTRSNGBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x00000001U)) |

| PRPHLBUSDATAPARMASK_CNT_U32 | 1 | Counts | ((uint32)(0x10000000U)) |

| DTSDBLBITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x80000000U)) |

| CODFLSSNGBITHARDFLT_CNT_U08 | 1 | Counts | 1U |

| CODFLSECCDBLBIT_CNT_U08 | 1 | Counts | 2U |

| CODFLSADRPAR_CNT_U08 | 1 | Counts | 4U |

| MEMBISTSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 1U |

| LCLRAMECCSNGBITHARDFLT_CNT_U08 | 1 | Counts | 1U |

| LCLRAMECCDBLBIT_CNT_U08 | 1 | Counts | 2U |

| INVLDRAMAREA_CNT_U08 | 1 | Counts | 4U |

| DTSDBLBIT_CNT_U08 | 1 | Counts | 2U |

| SPI0PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |

| SPI1PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |

| SPI2PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |

| SPI3PRPHLRAMDBLBIT_CNT_U08 | 1 | Counts | 2U |

| BISTCODECCFAILR_CNT_U08 | 1 | Counts | 1U |

| LOGLBISTSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 4U |

| BISTNOTCMPL_CNT_U08 | 1 | Counts | 16U |

| CPULOCKSTEPSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 32U |

| LOCKSTEPCOMP_CNT_U08 | 1 | Counts | 1U |

| SYSVCIE_CNT_U08 | 1 | Counts | 2U |

| RESDOPER_CNT_U08 | 1 | Counts | 4U |

| ALGNREAD_CNT_U08 | 1 | Counts | 8U |

| ALGNWR_CNT_U08 | 1 | Counts | 16U |

| INSTRFETCH_CNT_U08 | 1 | Counts | 32U |

| CLKMONR0RTLOWRLIMFLT_CNT_U08 | 1 | Counts | 4U |

| CLKMONR0RTUPPRLIMFLT_CNT_U08 | 1 | Counts | 8U |

| CLKMONR2RTLOWRLIMFLT_CNT_U08 | 1 | Counts | 64U |

| CLKMONR2RTUPPRLIMFLT_CNT_U08 | 1 | Counts | 128U |

| OPERMODERRFLSPROGMMODSTRTD_CNT_U08 | 1 | Counts | 1U |

| OPERMODERRTESTMODSTRTD_CNT_U08 | 1 | Counts | 2U |

| OPERMODERRSNGCHIPINACTV_CNT_U08 | 1 | Counts | 4U |

| CLKMONR1RTLOWRLIMFLT_CNT_U08 | 1 | Counts | 4U |

| CLKMONR1RTUPPRLIMFLT_CNT_U08 | 1 | Counts | 8U |

| CLKMONR3RTLOWRLIMFLT_CNT_U08 | 1 | Counts | 64U |

| CLKMONR3RTUPPRLIMFLT_CNT_U08 | 1 | Counts | 128U |

| DATAPROTNERR_CNT_U08 | 1 | Counts | 1U |

| INSTRPROTNERR_CNT_U08 | 1 | Counts | 2U |

| ECMSTSFLT_CNT_U08 | 1 | Counts | 1U |

| ECMMSTSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 4U |

| ECMCHKRSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 8U |

| ECMRTMSTCHKRCOMPFLT_CNT_U08 | 1 | Counts | 128U |

| FPUINVLDOPEREXCPN_CNT_U08 | 1 | Counts | 2U |

| FPUDIVBYZEROEXCPN_CNT_U08 | 1 | Counts | 4U |

| FPUOVFEXCPN_CNT_U08 | 1 | Counts | 8U |

| FPUUKWNEXCPN_CNT_U08 | 1 | Counts | 16U |

| UKWNRST_CNT_U08 | 1 | Counts | 1U |

| UKWNECMRST_CNT_U08 | 1 | Counts | 2U |

| UKWNSWRST_CNT_U08 | 1 | Counts | 16U |

| BACKUPRAMTSTFAILR_CNT_U08 | 1 | Counts | 32U |

| FLSBTLDRPREOSSRTUPEXCPN_CNT_U08 | 1 | Counts | 64U |

| STRTUPRSTINFOFAILD_CNT_U08 | 1 | Counts | 128U |

| PROGFLOW_CNT_U08 | 1 | Counts | 1U |

| DEADLINEMONR_CNT_U08 | 1 | Counts | 2U |

| ALVMONR_CNT_U08 | 1 | Counts | 4U |

| WDGTOUT_CNT_U08 | 1 | Counts | 1U |

| PEGRTFLT_CNT_U08 | 1 | Counts | 2U |

| IPGRTFLT_CNT_U08 | 1 | Counts | 8U |

| PBGSTRTUPTSTAILR_CNT_U08 | 1 | Counts | 16U |

| PBGRTFLT_CNT_U08 | 1 | Counts | 32U |

| DBGRST_CNT_U08 | 1 | Counts | 1U |

| OSCRITFLT_CNT_U08 | 1 | Counts | 1U |

| UKWNEXCPN_CNT_U08 | 1 | Counts | 2U |

| OSNONCRITFLT_CNT_U08 | 1 | Counts | 1U |

| DMATRFERR_CNT_U08 | 1 | Counts | 1U |

| DMAREGACSPROTCNERR_CNT_U08 | 1 | Counts | 2U |

| PRPHLBUSDATAPARSTRTUPFLT_CNT_U08 | 1 | Counts | 64U |

| PRPHLBUSDATAPARPRTFLT_CNT_U08 | 1 | Counts | 128U |

| CVMOVERVLTGSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 1U |

| CVMUNDERVLTGSTRTUPTESTFAILR_CNT_U08 | 1 | Counts | 2U |

| INTCVMOVERVLTGMONR_CNT_U08 | 1 | Counts | 1U |

| INTCVMUNDERVLTGMONR_CNT_U08 | 1 | Counts | 2U |

| INTMONRLOVCCFLT_CNT_U08 | 1 | Counts | 16U |

| EXTVLTGMONRFLT_CNT_U08 | 1 | Counts | 128U |

| UPPR16BITMASK_CNT_U32 | 1 | Counts | ((uint32)(0xFFFF0000U)) |

| LOWR16BITMASK_CNT_U32 | 1 | Counts | ((uint32)(0x0000FFFFU)) |

Constant Name

Resolution

Units

Value

FPCFGININVAL_CNT_T_U32

1

Counts

0x0000001CU

FPCFGREGID_CNT_S32

1

Counts

10

FPCFGSELNID_CNT_S32

1

Counts

0

FPUINVLDOPERSTSBIT_CNT_U32

1

Counts

((uint32)(0x00004000U))

FPUDIVBYZEROSTSBIT_CNT_U32

1

Counts

((uint32)(0x00002000U))

FPUOVFSTSBIT_CNT_U32

1

Counts

((uint32)(0x00001000U))

MEMERRINFOREADWRBIT_CNT_U32

1

Counts

((uint32)(0x00000001U))

CF1STERSTRADRPARMASK_CNT_U32

1

Counts

((uint32)(0x00000004U))

CF1STERSTRDBLBITMASK_CNT_U32

1

Counts

((uint32)(0x00000002U))

CF1STERSTRSNGBITMASK_CNT_U32

1

Counts

((uint32)(0x00000001U))

PRPHLBUSDATAPARMASK_CNT_U32

1

Counts

((uint32)(0x10000000U))

DTSDBLBITMASK_CNT_U32

1

Counts

((uint32)(0x80000000U))

CODFLSSNGBITHARDFLT_CNT_U08

1

Counts

1U

CODFLSECCDBLBIT_CNT_U08

1

Counts

2U

CODFLSADRPAR_CNT_U08

1

Counts

4U

MEMBISTSTRTUPTESTFAILR_CNT_U08

1

Counts

1U

LCLRAMECCSNGBITHARDFLT_CNT_U08

1

Counts

1U

LCLRAMECCDBLBIT_CNT_U08

1

Counts

2U

INVLDRAMAREA_CNT_U08

1

Counts

4U

DTSDBLBIT_CNT_U08

1

Counts

2U

SPI0PRPHLRAMDBLBIT_CNT_U08

1

Counts

2U

SPI1PRPHLRAMDBLBIT_CNT_U08

1

Counts

2U

SPI2PRPHLRAMDBLBIT_CNT_U08

1

Counts

2U

SPI3PRPHLRAMDBLBIT_CNT_U08

1

Counts

2U

BISTCODECCFAILR_CNT_U08

1

Counts

1U

LOGLBISTSTRTUPTESTFAILR_CNT_U08

1

Counts

4U

BISTNOTCMPL_CNT_U08

1

Counts

16U

CPULOCKSTEPSTRTUPTESTFAILR_CNT_U08

1

Counts

32U

LOCKSTEPCOMP_CNT_U08

1

Counts

1U

SYSVCIE_CNT_U08

1

Counts

2U

RESDOPER_CNT_U08

1

Counts

4U

ALGNREAD_CNT_U08

1

Counts

8U

ALGNWR_CNT_U08

1

Counts

16U

INSTRFETCH_CNT_U08

1

Counts

32U

CLKMONR0RTLOWRLIMFLT_CNT_U08

1

Counts

4U

CLKMONR0RTUPPRLIMFLT_CNT_U08

1

Counts

8U

CLKMONR2RTLOWRLIMFLT_CNT_U08

1

Counts

64U

CLKMONR2RTUPPRLIMFLT_CNT_U08

1

Counts

128U

OPERMODERRFLSPROGMMODSTRTD_CNT_U08

1

Counts

1U

OPERMODERRTESTMODSTRTD_CNT_U08

1

Counts

2U

OPERMODERRSNGCHIPINACTV_CNT_U08

1

Counts

4U

CLKMONR1RTLOWRLIMFLT_CNT_U08

1

Counts

4U

CLKMONR1RTUPPRLIMFLT_CNT_U08

1

Counts

8U

CLKMONR3RTLOWRLIMFLT_CNT_U08

1

Counts

64U

CLKMONR3RTUPPRLIMFLT_CNT_U08

1

Counts

128U

DATAPROTNERR_CNT_U08

1

Counts

1U

INSTRPROTNERR_CNT_U08

1

Counts

2U

ECMSTSFLT_CNT_U08

1

Counts

1U

ECMMSTSTRTUPTESTFAILR_CNT_U08

1

Counts

4U

ECMCHKRSTRTUPTESTFAILR_CNT_U08

1

Counts

8U

ECMRTMSTCHKRCOMPFLT_CNT_U08

1

Counts

128U

FPUINVLDOPEREXCPN_CNT_U08

1

Counts

2U

FPUDIVBYZEROEXCPN_CNT_U08

1

Counts

4U

FPUOVFEXCPN_CNT_U08

1

Counts

8U

FPUUKWNEXCPN_CNT_U08

1

Counts

16U

UKWNRST_CNT_U08

1

Counts

1U

UKWNECMRST_CNT_U08

1

Counts

2U

UKWNSWRST_CNT_U08

1

Counts

16U

BACKUPRAMTSTFAILR_CNT_U08

1

Counts

32U

FLSBTLDRPREOSSRTUPEXCPN_CNT_U08

1

Counts

64U

STRTUPRSTINFOFAILD_CNT_U08

1

Counts

128U

PROGFLOW_CNT_U08

1

Counts

1U

DEADLINEMONR_CNT_U08

1

Counts

2U

ALVMONR_CNT_U08

1

Counts

4U

WDGTOUT_CNT_U08

1

Counts

1U

PEGRTFLT_CNT_U08

1

Counts

2U

IPGRTFLT_CNT_U08

1

Counts

8U

PBGSTRTUPTSTAILR_CNT_U08

1

Counts

16U

PBGRTFLT_CNT_U08

1

Counts

32U

DBGRST_CNT_U08

1

Counts

1U

OSCRITFLT_CNT_U08

1

Counts

1U

UKWNEXCPN_CNT_U08

1

Counts

2U

OSNONCRITFLT_CNT_U08

1

Counts

1U

DMATRFERR_CNT_U08

1

Counts

1U

DMAREGACSPROTCNERR_CNT_U08

1

Counts

2U

PRPHLBUSDATAPARSTRTUPFLT_CNT_U08

1

Counts

64U

PRPHLBUSDATAPARPRTFLT_CNT_U08

1

Counts

128U

CVMOVERVLTGSTRTUPTESTFAILR_CNT_U08

1

Counts

1U

CVMUNDERVLTGSTRTUPTESTFAILR_CNT_U08


*... content truncated for brevity; see the source document in the repository. ...*

Back to [Complex Device Drivers](../).
