---
title: "Sweep (DF002A_Swp)"
description: "Sweep: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Sweep component belongs to **Diagnostic and Fault-Injection Functions** in the **Application Software** layer. It supports diagnostics, fault injection or test sweeps used during development and verification.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `DF002A_Swp_Design` | Design package |
| `DF002A_Swp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `DF002A_Swp_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `DF002A_Swp_Impl` |  |
| C sources | `Swp.c` |
| Public headers | `Swp.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `Swp.dcf`, `Swp_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DF002A_Swp_Impl.gpj`, `RteGen.bat`, `Swp.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `DF002A_Swp_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `DF002A_Swp_Impl/src/Swp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

5 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `Init1.txt`

- **Source path in repository:** `DF002A_Swp_Design/Design/Init1.txt`
- **Format:** `.txt`
- **Size:** `2 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Swp Initialzing Variables to be used in Init1

- SwpTranTi
[2000	500	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	250	1000];

-SwpFrqList
[0	1	1.2	1.4	1.6	1.8	2	2.25	2.5	2.75	3	3.25	3.5	3.75	4	4.25	4.5	4.75	5	5.25	5.5	5.75	6	6.25	6.5	6.75	7	7.25	7.5	7.75	8	8.25	8.5	8.75	9	9.25	9.5	9.75	10	10.25	10.5	10.75	11	11.25	11.5	11.75	12	12.25	12.5	12.75	13	13.25	13.5	13.75	14	14.25	14.5	14.75	15	15.5	16	16.5	17	17.5	18	18.5	19	19.5	20	21	22	23	24	25	26	27	28	29	30	32	34	36	38	40	42	44	46	48	50	55	60	65	70	75	80	85	90	95	100	105];

- SwpGain

 0.45

- SwpCfg

 1

- SwpDwellTi
[0	32000	18333	10714	9375	8333	7500	6667	6000	5455	4667	4308	3714	3467	3000	2824	2667	2526	2400	2286	2182	2087	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000	2000];

- SwpVehSpdMax

 1 

-SwpVehSpdChkEna

 1

-SwpOffs

 0

-SwpSwtSt

 0

-SwpSinAmp
 
 0.5

-SwpLstStSinArg

 0

-SwpInstsFrq

 0

-SwpGenHwTq

 0

-SwpFrqIdx

 1 (Index 1 in MATLAB corresponds to index 0 in C code)

-SwpCosTq

 1

-SwpSinTq

 0

-SwpModEna

 1 

-SwpDwellStrtTi

 0

-SwpTranStrtTi

 0
```

### `DF002A_Swp_PeerReview.docx`

- **Source path in repository:** `DF002A_Swp_Design/Doc/DF002A_Swp_PeerReview.docx`
- **Format:** `.docx`
- **Size:** `13 KiB`
- **Expected content:** Peer-review record (inferred from the file name — assumption).

**Converted content:**

Changes based on software group Peer Review (Selva, Anne, Creager):

1) Outputs are not range limited. -Modifications done to add saturation on outputs of sweep.

2) Req Tags and legacy comments are to be removed from the model - Done

3) SWPTIUNITCNVN shall be used instead of 1/10 -Done

### `DF002A_Swp_DDReport.txt`

- **Source path in repository:** `DF002A_Swp_Design/Reports/DF002A_Swp_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of DF002A_Swp_DataDict
03-Feb-2016 17:21:43
Tool Release:  2.26.0



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
(variables: 3, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 4, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 2, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
SwpSinTq                    	Name does not match required pattern.
(variables: 1, errors: 1)

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
SwpCfg                      	Name does not match required pattern.
SwpCosTq                    	Name does not match required pattern.
SwpDwellStrtTi              	Name does not match required pattern.
SwpDwellTi                  	Name does not match required pattern.
SwpFrqIdx                   	Name does not match required pattern.
```
*... truncated (54 more lines in the source file). ...*

### `Swp_IntegrationManual.doc`

- **Source path in repository:** `DF002A_Swp_Impl/doc/Swp_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Swp_MDD.docx`

- **Source path in repository:** `DF002A_Swp_Impl/doc/Swp_MDD.docx`
- **Format:** `.docx`
- **Size:** `111 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Swp

Jan 20, 2016

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Krishna Kanth Anne,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Krishna Kanth Anne | 1. 0.0 | 20 - Oct -2015 |

| Fix for anomaly EA4#2461 | Krishna Kanth Anne | 1. 1 .0 | 20-Jan-2016 |

Description

Author

Version

Date

Initial Version

Krishna Kanth Anne

1.0.0

20-Oct-2015

Fix for anomaly EA4#2461

Krishna Kanth Anne

1.1.0

20-Jan-2016

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2PullCmpActv & High-Level Description5

3Design details of software module6

3.1Graphical representation of PullCmpActv6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: SwpInit18

5.1.2Per: SwpPer18

5.1.3Per: SwpPer28

5.2Module Internal (Local) Functions8

5.2.1Local Function #18

5.2.1.1Design Rationale8

5.2.1.2Processing8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

MDD for Sweep function

### Scope

NA

## Swp & High-Level Description

Please refer FDD.

## Design details of software module

Please refer FDD.

### Graphical representation of Swp

### Data Flow Diagram

Please refer FDD.

#### Component level DFD

Please refer FDD.

#### Function level DFD

Please refer FDD.

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Please refer  DF002A_Swp_DataDict.m | NA | NA | NA |

| SWPSTRT_CNT_U16 | NA | NA | 0 |

| SWPTRAN_CNT_U16 | NA | NA | 1 |

| SWPDWELL_CNT_U16 | NA | NA | 2 |

| SWPSTOP_CNT_U16 | NA | NA | 3 |

| SWPRAMP_CNT_U16 | NA | NA | 4 |

| SWPDONE_CNT_U16 | NA | NA | 5 |

Constant Name

Resolution

Units

Value

Please refer DF002A_Swp_DataDict.m

NA

NA

NA

SWPSTRT_CNT_U16

NA

NA

0

SWPTRAN_CNT_U16

NA

NA

1

SWPDWELL_CNT_U16

NA

NA

2

SWPSTOP_CNT_U16

NA

NA

3

SWPRAMP_CNT_U16

NA

NA

4

SWPDONE_CNT_U16

NA

NA

5

## Software Component Implementation

Please refer FDD.

### Sub-Module Functions

### Init: SwpInit1

Please refer FDD.

### Design Rationale

Dummy Initialization function to correlate with the FDD (.m file)

### Per: SwpPer1

Please refer FDD.

### Design Rationale

For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process. This is to give control over MemMap to avoid MPU violations while writing these variables using xcp.

All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

### Per: SwpPer2

Please refer FDD.

### Design Rationale

For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process. This is to give control over MemMap to avoid MPU violations while writing these variables using xcp.

All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

## Known Limitations with Design

None.

## UNIT TEST CONSIDERATION

Please refer Init.txt file in the FDD design: DF002A_Swp_Design for initial values of Function level and Module level variables.

For DFs, it was decided to use the module level variables in place of PIMs defined in the FDD (PIM section of .m file), This is a deviation from regular EA4 process.

All of the given PIMs from .m file are either defined as of Function level variables (if used in only one function) or Module level variables (if used in more than one function) in DFs.

Each of the Function level and Module level variables shall be volatile only when they are intended to be user modifiable as per the data dictionary .m file.

Deviations exist in the naming conventions for all of Function level and Module level variables from regular EA4 naming conventions.

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

| 5 | FDD: SF0 02 A_ Swp _Design | See Synergy  SubProject  version |

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

5

FDD: SF002A_Swp_Design

See Synergy SubProject version

Back to [Application Software](../).
