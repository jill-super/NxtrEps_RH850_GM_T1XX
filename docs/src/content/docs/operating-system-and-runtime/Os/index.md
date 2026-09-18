---
title: "Operating System (Os)"
description: "Operating System: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Operating System component belongs to **Operating System and Runtime** in the **Operating System and Runtime Environment** layer. It provides the real-time operating system or the runtime environment for software components.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Os` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Os` |  |
| C sources | `NxtrOsErrHndlg.c`, `atosappl.c`, `atostime.c`, `osOstmHiRes.c`, `osSysCall.c`, `osek.c`, `osekalrm.c`, `osekasm.c`, `osekerr.c`, `osekevnt.c`, `osekrsrc.c`, `oseksched.c` (+3 more) |
| Public headers | `NxtrOsErrHndlg.h`, `Os.h`, `Os_Cfg.h`, `emptymac.h`, `osDerivatives.h`, `osINTC2.h`, `osRH850_P1M.h`, `osSysCallTable.dld`, `osek.h`, `osekasm.h`, `osekasrt.h`, `osekcov.h` (+5 more) |
| AUTOSAR model | `Os_RH850_P1M_bswmd.arxml` |
| Generator output | `Os_gen.bat`, `RH850.lic`, `RH850_P1M.i41`, `RH850_P1M.s41`, `StyleSheet.xsl`, `genRH850.exe` |
| Tooling and integration scripts | `ConfigViewer.exe`, `CreateGHSProject.bat`, `Integrate.bat`, `Os.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (1 file(s), e.g. `Os/autosar/Os_RH850_P1M_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 15 C source file(s), starting with `Os/src/NxtrOsErrHndlg.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `Os/src/atosappl.c`, `Os/src/atostime.c`, `Os/src/osOstmHiRes.c`, `Os/src/osSysCall.c`, `Os/src/osek.c` (and 9 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

7 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `MicrosarOS_RH850_SafeContext_SafetyManual.pdf`

- **Source path in repository:** `Os/doc/MicrosarOS_RH850_SafeContext_SafetyManual.pdf`
- **Format:** `.pdf`
- **Size:** `967 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Os Integration Manual.doc`

- **Source path in repository:** `Os/doc/Os Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `130 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Os Module Design Document.docx`

- **Source path in repository:** `Os/doc/Os Module Design Document.docx`
- **Format:** `.docx`
- **Size:** `283 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

Os

1/6/16

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

| Initial Version | Lucas  Wendling | 1 | 1/6/16 |

Description

Author

Version

Date

Initial Version

Lucas Wendling

1

1/6/16

Table of Contents

1Introduction5

1.1Purpose5

1.2Scope5

2Os & High-Level Description6

3Design details of software module7

3.1Graphical representation of Os7

3.2Data Flow Diagram7

3.2.1Component level DFD7

3.2.2Function level DFD7

4Constant Data Dictionary8

4.1Program (fixed) Constants8

4.1.1Embedded Constants8

5Software Component Implementation9

5.1Sub-Module Functions9

5.1.1Init: Os_Init<n>9

5.1.1.1Design Rationale9

5.1.1.2Module Outputs9

5.1.2Per: Os_Per<n>9

5.1.2.1Design Rationale9

5.1.2.2Store Module Inputs to Local copies9

5.1.2.3(Processing of function)………9

5.1.2.4Store Local copy of outputs into Module Outputs9

5.2Server Runables9

5.2.1<Server Runable Name>9

5.2.1.1Design Rationale9

5.2.1.2(Processing of function)………10

5.3Interrupt Functions10

5.3.1Interrupt Function Name10

5.3.1.1Design Rationale10

5.3.1.2(Processing of the ISR function)…..10

5.4Module Internal (Local) Functions10

5.4.1Local Function #110

5.4.1.1Design Rationale10

5.4.1.2Processing10

5.5GLOBAL Function/Macro Definitions10

5.5.1GLOBAL Function #110

5.5.1.1Design Rationale11

5.5.1.2processing11

6Known Limitations with Design12

7UNIT TEST CONSIDERATION13

Appendix AAbbreviations and Acronyms14

Appendix BGlossary15

Appendix CReferences16

## Introduction

### Purpose

This design document will capture the design of the Nexteer Os Error Handling (NxtrOsErrHndlg) functionality.  This is the only portion of this component that is designed by Nexteer rather than a 3rd party.

### Scope

The following definitions are used throughout this document:

Shall: indicates a mandatory requirement without exception in compliance.

Should: indicates a mandatory requirement; exceptions allowed only with documented justification.

May: indicates an optional action.

## High-Level Description

The Nexteer designed portions of the Os component consist of the Os error processing.  This Nexteer specific design was embedded within the Os component itself since this functionality is specifically tied to the errors and names that this particular Os supports.  This error handling is expected to be called by the Os protection and error callout functions in any given project.  It interfaces with the Exception Handler that is created to react to the different categories of Os errors.

## Design details of software module

<The Data Flow Diagrams should be created in the absence of this representation with the FDD.>

### Graphical representation of NxtrOsErrHndlg (Expected External Intefaces)

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| None |  |  |  |

Constant Name

Resolution

Units

Value

None

## Software Component Implementation

### Sub-Module Functions

### Init:

None

### Per:

None

### Server Runables

### NxtrOsErrHndlg

### Design Rationale

This runnable will parse through the different Os errors that can be detected and interface into the Exception Handler component for handling of the different categories of errors.  This runnable is expected to be called by both the Os ErrorHook and the Os ProtectionHook as it handles all categories of Os errors.

### Processing

switch (OSErrorGetosCANError())

case osdErrUEUnhandledException:

case osdErrUEUnhandledCoreException:

case osdErrUEUnhandledDirectBranch:

/* Unhandled Exceptions */

ProcUkwnExcpnErr(OSErrorGetosCANError())

break

case osdErrEXMemoryViolation:

/* MPU Violations */

ProcMpuExcpnErr(OSErrorGetosCANError());

break

case osdErrEXPrivilegedInstruction:

/* Privileged Instruction Exceptions */

ProcPrvlgdInstrExcpnErr(OSErrorGetosCANError());

break

case osdErrATWrongTaskPrio:

case osdErrTTNotActivated:

case osdErrTTNoImmediateTaskSwitch:

case osdErrTTWrongActiveTaskID:

case osdErrHTNotActivated:

case osdErrHTNoImmediateTaskSwitch:

case osdErrHTWrongActiveTaskID:

case osdErrSHScheduleNotAllowed:

case osdErrSHWrongActiveTaskID:

case osdErrGSOddInvocation:

case osdErrGIOddInvocation:

case osdErrMTMissingTerminateTask:

case osdErrEAIntAPIWrongSequence:

case osdErrDAIntAPIDisabled:

case osdErrSDWrongCounter:

case osdErrREWrongCounter:

case osdErrSGWrongCounter:

case osdErrRGWrongCounter:

case osdErrGRPriorityOccupied:

case osdErrGRNoAccessRights:

case osdErrGRWrongTaskID:

case osdErrRRCeilingPriorityNotSet:

case osdErrRRWrongTask:

case osdErrRRNoReadyTaskFound:

case osdErrRRWrongTaskID:

case osdErrRRWrongHighRdyPrio:

case osdErrSEWrongTaskPrio:

case osdErrGEOddInvocation:

case osdErrCAAlarmInternal:

case osdErrWAWrongIDonHeap:

case osdErrWAHeapOverflow:

case osdErrWAUnknownAction:

case osdErrWAWrongCounterID:

case osdErrSOStackOverflow:

case osdErrSUWrongTaskID:

case osdErrCLWrongLibrary:

case osdErrEHInterruptsEnabled:

case osdErrSTMemoryError:

case osdErrSTNoImmediateTaskSwitch:

case osdErrSTWrongAppMode:

case osdErrSTConfigCRCError:

case osdErrSTConfigMagicNrError:

case osdErrSTInvalidMajorVersion:

case osdErrSTInvalidMinorVersion:

case osdErrSTInvalidSTCfg:

case osdErrQIWrongTaskPrio:

case osdErrQRInterruptsEnabled:

case osdErrQRWrongTaskID:

case osdErrQRWrongTaskPrio:

case osdErrQRWrongHighRdyPrio:

case osdErrQSInterruptsEnabled:

case osdErrQSNoReadyTaskFound:

case osdErrQSWrongPriority:

case osdErrQOWrongTaskID:

case osdErrSPUnknownCase:

case osdErrSGOddInvocation:

case osdErrWSUnknownAction:

case osdErrWSUnknownReaction:

case osdErrWSWrongID:

case osdErrGCOddInvocation:

case osdErrBMResAlreadyMeasured:

case osdErrBMInvalidProcessInStart:

case osdErrBMInvalidProcessInStop:

case osdErrBMInvalidResource:

case osdErrETNoCurrentProcess:

case osdErrASOddInvocation:

case osdErrTAInvalidTaskState:

case osdErrRSWrongTaskPrio:

case osdErrPAInvalidAreaIndex:

case osdErrPANoAccessRight:

case osdErrPAInvalidAddress:

case osdErrYOSystemStackOverflow:

case osdErrYOTaskStackOverflow:

case osdErrYOISRStackOverflow:

case osdErrSCWrongSysCallParameter:

case osdErrDPStartValidContext:

case osdErrDPResumeInvalidContext:

case osdErrDPInvalidTaskIndex:

case osdErrDPInvalidApplicationID:

case osdErrSUInvalidTaskIndex:

case osdErrSUInvalidIsrIndex:

case osdErrSUInvalidIsrPrioLevel:

case osdErrCIInvalidIsrIndex:

case osdErrCIInvalidIsrPrioLevel:

case osdErrCIInvalidApplicationID:

case osdErrCIMissingIntRequest:

case osdErrCIInterruptIsMasked:

case osdErrCIWrongIntPriority:

case osdErrPIGetIMRInvalidIndex:

case osdErrPISetIMRInvalidIndex:

case osdErrPIClearIMRInvalidIndex:

case osdErrPIWriteIMR8InvalidAddr:

case osdErrPIWriteIMR16InvalidAddr:

case osdErrPIWriteIMR32InvalidAddr:

case osdErrPISetICRMaskInvalidAddr:

case osdErrPIClearICRMaskInvalidAddr:

case osdErrPISetICRReqInvalidAddr:

case osdErrPIClearICRReqInvalidAddr:

case osdErrPIWriteICR8InvalidAddr:

case osdErrPIWriteICR16InvalidAddr:

case osdErrPIWriteICRxLoInvalidIndex:

case osdErrPIWriteICRxHiInvalidIndex:

case osdErrPIWriteICRx16InvalidIndex:

case osdErrCRInvalidSettingOSTM:

case osdErrCRInvalidSettingMPU:

/* Fatal OS fault for assertion / syscheck errors - set data for reset cause */

ProcPrmntOsErr(OSErrorGetosCANError())

break

default:

/* Assumed to be a non-fatal OSEK fault - Set data for periodic sweep up */

ProcNonCritOsErr(OSErrorGetosCANError())

break

### Interrupt Functions

None

### Module Internal (Local) Functions

### Local Function #1

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

<Any known limitations with the design shall be documented clearly in this section.>

## UNIT TEST CONSIDERATION

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

### `ProductInformation_2_Restrictions-for-MSR-OS-SafeContext-SC3.pdf`

- **Source path in repository:** `Os/doc/ProductInformation_2_Restrictions-for-MSR-OS-SafeContext-SC3.pdf`
- **Format:** `.pdf`
- **Size:** `203 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ReleaseNotes_Microsar_Os.txt`

- **Source path in repository:** `Os/doc/ReleaseNotes_Microsar_Os.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Release notes (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
******************************************************************************
Readme.txt          MICROSAR OS RH850 SC3                           2016-07-12
******************************************************************************

This file describes hints to the installation and last changes on the products.

Contents
========
1. Versions
2. Examples
3. Supported C-compilers
4. Documentation
5. History of changes
6. Limitations


1. Versions
===========
   MICROSAR OS RH850 SC3: v1.06.08


2. Examples
===========
MICROSAR OS RH850 is delivered without application example programs.


3. Supported C-compilers
========================
Green Hills MULTI IDE v6.1.4 2013.x.x with register mode 22, 26 and 32
Green Hills MULTI IDE v6.1.6 2014.x.x with register mode 22, 26 and 32
Green Hills MULTI IDE v6.1.6 2015.x.x with register mode 22, 26 and 32


4. Documentation
================
The installation contains all documentation in electronically readable format (PDF-files):
TechnicalReference_Microsar_Os.pdf:      General part of the MICROSAR OS user manual
TechnicalReference_MICROSAROS_RH850.pdf: RH850 specific part of the MICROSAR OS user manual


5. History of changes
=====================

v1.00.00 beta
=============
- initial version

v1.01.00 beta
=============
- added support for D1L, E1L and F1M

v1.02.00 beta
=============
- added support for F1H and P1M

v1.03.00 beta
=============
- added support for D1M and E1M

v1.04.00 beta
=============
- support Interrupt API for RTE
- support optimized API calls
- support Timing Hooks

v1.05.00 beta
=============
- support FE level interrupt handling
- update to core code version 9.01.04

v1.06.00
=============
- final release

v1.06.01
=============
- support RH850 F1K

v1.06.02
=============
```
*... truncated (53 more lines in the source file). ...*

### `TechnicalReference_MICROSAROS_RH850.pdf`

- **Source path in repository:** `Os/doc/TechnicalReference_MICROSAROS_RH850.pdf`
- **Format:** `.pdf`
- **Size:** `754 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Os.pdf`

- **Source path in repository:** `Os/doc/TechnicalReference_Os.pdf`
- **Format:** `.pdf`
- **Size:** `3089 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Operating System and Runtime Environment](../).
