---
title: "Architecture Global Parameters (AR999A_ArchGlbPrm)"
description: "Architecture Global Parameters: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Architecture Global Parameters component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `AR999A_ArchGlbPrm_Design` | Design package |
| `AR999A_ArchGlbPrm_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR999A_ArchGlbPrm_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `AR999A_ArchGlbPrm_Impl` |  |
| Public headers | `ArchGlbPrm.h` |
| Tooling and integration scripts | `AR999A_ArchGlbPrm_Impl.gpj`, `CreateGHSProject.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AR999A ArchGlbPrm.docx`

- **Source path in repository:** `AR999A_ArchGlbPrm_Design/Doc/AR999A ArchGlbPrm.docx`
- **Format:** `.docx`
- **Size:** `136 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Converted content:**

Functional Design Document

For

Architecture Global Parameters

VERSION: 1.0

DATE: 05-Mar-2015

Prepared By:

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Version | Description | Author | Section Modified | Date |

| --- | --- | --- | --- | --- |

| 1.0 | Initial Version | Kathleen  Creager | All | 05-Mar-2015 |

Version

Description

Author

Section Modified

Date

1.0

Initial Version

Kathleen Creager

All

05-Mar-2015

Table of Contents

1Abbrevations And Acronyms4

2References5

3Purpose6

4ArchGlbPrm Design7

4.1constants7

4.1.1float32 Constant specification7

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

Abbreviation

Description

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

|  |  |  |

Sr. No.

Title

Version

## Purpose

The purpose of this document is to describe the design of the Architecture Global Parameters component including the selection criteria for items to be included in the component and the method used for specifying the values of the items.

## ArchGlbPrm Design

### constants

The ArchGlbPrm component contains global constants that are either “mathematical” (e.g. the value of pi) or software-oriented (e.g. the value to be used as the zero threshold for float32 comparisons) in nature.  The constants are defined in AR999A_ArchGlbPrm_DataDict.m and implemented as #define statements in “ArchGlbPrm.h”.

### float32 Constant specification

For each float32 constant, the number of digits was chosen based on the smallest number of digits needed to give the same float32 representation as the value calculated by Excel.  Rationale: this gives the most accurate representation possible for float32, while not containing a misleading number of digits beyond the resolution actually possible with float32.

Example procedure for determining the number of digits to use:

Enter the desired constant in Excel as a formula, e.g. “=PI()/2”

Copy the cell and paste as value into another cell

Select the new cell and copy the displayed value to the clipboard

Paste this value in a IEEE floating point conversion tool; record the single precision floating point representation (in hex), both rounded and unrounded.

Val = the pasted Excel value

X = number of digits in Val

Y = X

Do:

Y = Y - 1

Val1 = Val rounded to Y digits

While ((rounded single float representation of Val == rounded single float representation of Val1) AND              (unrounded single float representation of Val == unrounded single float representation of Val1))

Val2 = Val rounded to Y + 1 digits

Use Val2 as the constant value in the .h and .m files

### `AR999A_ArchGlbPrm_DDReport.txt`

- **Source path in repository:** `AR999A_ArchGlbPrm_Design/Reports/AR999A_ArchGlbPrm_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
KMC 6/23/2015: latest VerifyDD crashes on latest AR999A_ArchGlbPrm_DataDict.m file.  Report is from an intermediate draft.

Verification of AR999A_ArchGlbPrm_DataDict
23-Jun-2015 13:34:49
Tool Release:  2.14.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF99A
--------------------------------------------------------------
AR999A              	.DesignASIL: Field is empty.
AR999A              	.Description: Field is empty.
(variable: 1, errors: 2)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
Unable to find model for comparison to data dictionary.
(errors:  1)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
(variables: 0, errors: 0)

--------------------------------------
SrvRunnable:	<ShoName><TriggerName>
--------------------------------------
(variables: 0, errors: 0)

------------
Client:	
------------
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
(variables: 0, errors: 0)
```
*... truncated (45 more lines in the source file). ...*

Back to [Libraries](../).
