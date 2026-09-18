---
title: "Tauj1 Configuration And Use (CM460A_Tauj1CfgAndUse)"
description: "Tauj1 Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Tauj1 Configuration And Use component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM460A_Tauj1CfgAndUse_Design` | Design package |
| `CM460A_Tauj1CfgAndUse_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM460A_Tauj1CfgAndUse_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM460A_Tauj1CfgAndUse_Impl` |  |
| C sources | `CDD_Tauj1CfgAndUse.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `Tauj1CfgAndUse.dcf`, `Tauj1CfgAndUse_attr_def.xml` |
| Tooling and integration scripts | `CM460A_Tauj1CfgAndUse_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `Tauj1CfgAndUse.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM460A_Tauj1CfgAndUse_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM460A_Tauj1CfgAndUse_Impl/src/CDD_Tauj1CfgAndUse.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `Tauj1 Registers.txt`

- **Source path in repository:** `CM460A_Tauj1CfgAndUse_Design/Doc/Tauj1 Registers.txt`
- **Format:** `.txt`
- **Size:** `76 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
RegOutpTAUJ1CDR0 = DataDict.OpSignal;
RegOutpTAUJ1CDR0.LongName = 'Register TAUJ0CDR0';
RegOutpTAUJ1CDR0.Description = 'Register TAUJ0CDR0';
RegOutpTAUJ1CDR0.DocUnits = 'Cnt';
RegOutpTAUJ1CDR0.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CDR0.EngDT = dt.u32;
RegOutpTAUJ1CDR0.EngInit = 0;
RegOutpTAUJ1CDR0.EngMin = 0;
RegOutpTAUJ1CDR0.EngMax = 4294967295;
RegOutpTAUJ1CDR0.TestTolerance = 0;
RegOutpTAUJ1CDR0.WrittenIn = {};
RegOutpTAUJ1CDR0.WriteType = 'Phy';

RegOutpTAUJ1CDR1 = DataDict.OpSignal;
RegOutpTAUJ1CDR1.LongName = 'Register TAUJ0CDR1';
RegOutpTAUJ1CDR1.Description = 'Register TAUJ0CDR1';
RegOutpTAUJ1CDR1.DocUnits = 'Cnt';
RegOutpTAUJ1CDR1.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CDR1.EngDT = dt.u32;
RegOutpTAUJ1CDR1.EngInit = 0;
RegOutpTAUJ1CDR1.EngMin = 0;
RegOutpTAUJ1CDR1.EngMax = 4294967295;
RegOutpTAUJ1CDR1.TestTolerance = 0;
RegOutpTAUJ1CDR1.WrittenIn = {};
RegOutpTAUJ1CDR1.WriteType = 'Phy';

RegOutpTAUJ1CDR2 = DataDict.OpSignal;
RegOutpTAUJ1CDR2.LongName = 'Register TAUJ0CDR2';
RegOutpTAUJ1CDR2.Description = 'Register TAUJ0CDR2';
RegOutpTAUJ1CDR2.DocUnits = 'Cnt';
RegOutpTAUJ1CDR2.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CDR2.EngDT = dt.u32;
RegOutpTAUJ1CDR2.EngInit = 0;
RegOutpTAUJ1CDR2.EngMin = 0;
RegOutpTAUJ1CDR2.EngMax = 4294967295;
RegOutpTAUJ1CDR2.TestTolerance = 0;
RegOutpTAUJ1CDR2.WrittenIn = {};
RegOutpTAUJ1CDR2.WriteType = 'Phy';

RegOutpTAUJ1CDR3 = DataDict.OpSignal;
RegOutpTAUJ1CDR3.LongName = 'Register TAUJ0CDR3';
RegOutpTAUJ1CDR3.Description = 'Register TAUJ0CDR3';
RegOutpTAUJ1CDR3.DocUnits = 'Cnt';
RegOutpTAUJ1CDR3.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CDR3.EngDT = dt.u32;
RegOutpTAUJ1CDR3.EngInit = 0;
RegOutpTAUJ1CDR3.EngMin = 0;
RegOutpTAUJ1CDR3.EngMax = 4294967295;
RegOutpTAUJ1CDR3.TestTolerance = 0;
RegOutpTAUJ1CDR3.WrittenIn = {};
RegOutpTAUJ1CDR3.WriteType = 'Phy';

RegOutpTAUJ1CNT0 = DataDict.OpSignal;
RegOutpTAUJ1CNT0.LongName = 'Register TAUJ0CNT0';
RegOutpTAUJ1CNT0.Description = 'Register TAUJ0CNT0';
RegOutpTAUJ1CNT0.DocUnits = 'Cnt';
RegOutpTAUJ1CNT0.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CNT0.EngDT = dt.u32;
RegOutpTAUJ1CNT0.EngInit = 0;
RegOutpTAUJ1CNT0.EngMin = 0;
RegOutpTAUJ1CNT0.EngMax = 4294967295;
RegOutpTAUJ1CNT0.TestTolerance = 0;
RegOutpTAUJ1CNT0.WrittenIn = {};
RegOutpTAUJ1CNT0.WriteType = 'Phy';

RegOutpTAUJ1CNT1 = DataDict.OpSignal;
RegOutpTAUJ1CNT1.LongName = 'Register TAUJ0CNT1';
RegOutpTAUJ1CNT1.Description = 'Register TAUJ0CNT1';
RegOutpTAUJ1CNT1.DocUnits = 'Cnt';
RegOutpTAUJ1CNT1.SwcShoName = 'Tauj0CfgAndUse';
RegOutpTAUJ1CNT1.EngDT = dt.u32;
RegOutpTAUJ1CNT1.EngInit = 0;
RegOutpTAUJ1CNT1.EngMin = 0;
RegOutpTAUJ1CNT1.EngMax = 4294967295;
RegOutpTAUJ1CNT1.TestTolerance = 0;
RegOutpTAUJ1CNT1.WrittenIn = {};
RegOutpTAUJ1CNT1.WriteType = 'Phy';

RegOutpTAUJ1CNT2 = DataDict.OpSignal;
RegOutpTAUJ1CNT2.LongName = 'Register TAUJ0CNT2';
```
*... truncated (2274 more lines in the source file). ...*

### `CM460A_Tauj1CfgAndUse_DDReport.txt`

- **Source path in repository:** `CM460A_Tauj1CfgAndUse_Design/Reports/CM460A_Tauj1CfgAndUse_DDReport.txt`
- **Format:** `.txt`
- **Size:** `5 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM460A_Tauj1CfgAndUse_DataDict
14-Mar-2016 17:07:10
Tool Release:  2.32.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF099A
--------------------------------------------------------------
CM460A              	Tauj		Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variable: 1, errors: 1)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
(errors:  0)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
Tauj1CfgAndUseInit1         	    Tauj           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Tauj1CfgAndUsePer1          	    Tauj           Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 2, errors: 2)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 0, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
PhaFbD                      	Cannot match name to list of known Nexteer signals.
PhaFbE                      	Cannot match name to list of known Nexteer signals.
PhaFbF                      	Cannot match name to list of known Nexteer signals.
RegInpTAUJ1CNT0             	    U              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpTAUJ1CNT0             	    J              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpTAUJ1CNT1             	    U              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpTAUJ1CNT1             	    J              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpTAUJ1CNT2             	    U              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpTAUJ1CNT2             	    J              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 6, errors: 9)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 3, errors: 0)

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
```
*... truncated (47 more lines in the source file). ...*

### `Tauj1CfgAndUse_IntegrationManual.doc`

- **Source path in repository:** `CM460A_Tauj1CfgAndUse_Impl/doc/Tauj1CfgAndUse_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `140 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Tauj1CfgAndUse_MDD.docx`

- **Source path in repository:** `CM460A_Tauj1CfgAndUse_Impl/doc/Tauj1CfgAndUse_MDD.docx`
- **Format:** `.docx`
- **Size:** `106 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Tauj1CfgAndUse

Aug 10, 2015

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Sankardu Varadapureddi,

Nexteer Automotive,

Saginaw, MI, USAChange History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Sankardu   Varadapureddi | 1 | 10 -Aug-2015 |

Description

Author

Version

Date

Initial Version

Sankardu Varadapureddi

1

10-Aug-2015

Table of Contents

1Introduction4

1.1Purpose4

1.2Scope4

2LoaMgr High-Level Description5

3Design details of software module6

3.1Graphical representation of LoaMgr6

3.2Data Flow Diagram6

3.2.1Component level DFD6

3.2.2Function level DFD6

4Constant Data Dictionary7

4.1Program (fixed) Constants7

4.1.1Embedded Constants7

5Software Component Implementation8

5.1Sub-Module Functions8

5.1.1Init: Tauj1CfgAndUseInit18

5.1.1.1Design Rationale8

5.1.1.2Module Outputs8

5.1.2Per: Tauj1CfgAndUsePer18

5.1.2.1Design Rationale8

5.1.2.2Store Module Inputs to Local copies8

5.1.2.3(Processing of function)………8

5.1.2.4Store Local copy of outputs into Module Outputs8

5.2Server Runables8

5.3Interrupt Functions8

5.4Module Internal (Local) Functions8

5.5GLOBAL Function/Macro Definitions8

6Known Limitations with Design9

7UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## Introduction

### Purpose

### Scope

## LoaMgr High-Level Description

Refer to FDD

## Design details of software module

### Graphical representation of LoaMgr

### Data Flow Diagram

Refer FDD

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| Refer .m file |  |  |  |

Constant Name

Resolution

Units

Value

Refer .m file

## Software Component Implementation

### Sub-Module Functions

### Init: Tauj1CfgAndUseInit1

### Design Rationale

Refer FDD

### Module Outputs

Refer FDD

### Per: Tauj1CfgAndUsePer1

### Design Rationale

Refer FDD

### Store Module Inputs to Local copies

Refer FDD

### (Processing of function)………

Refer FDD

### Store Local copy of outputs into Module Outputs

Refer FDD

### Server Runables

None

### Interrupt Functions

None

### Module Internal (Local) Functions

None

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

| 1 | AUTOSAR Specification of Memory Mapping ( Link: AUTOSAR_SWS_MemoryMapping.pdf ) | v1.3.0 R4.0 Rev 2 |

| 2 | MDD Guideline | EA4 01.00 . 01 |

| 3 | Software Naming Conventions.doc | EA4 0 1.0 0.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | FDD :  CM4 60 A _ Tauj1Cfg AndUse _Design | See Synergy sub project version |

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

EA4 01.00.00

4

Software Design and Coding Standards.doc

2.1

5

FDD : CM460A_Tauj1CfgAndUse_Design

See Synergy sub project version

Back to [Complex Device Drivers](../).
