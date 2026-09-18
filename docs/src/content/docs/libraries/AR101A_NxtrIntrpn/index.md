---
title: "Nexteer Interpolation Library (AR101A_NxtrIntrpn)"
description: "Nexteer Interpolation Library: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Nexteer Interpolation Library component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `AR101A_NxtrIntrpn_Design` | Design package |
| `AR101A_NxtrIntrpn_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR101A_NxtrIntrpn_Design` |  |
| Documentation folders | `Doc/` |
| `AR101A_NxtrIntrpn_Impl` |  |
| C sources | `NxtrIntrpn.c` |
| Public headers | `NxtrIntrpn.h`, `NxtrIntrpn_MemMap.h` |
| Tooling and integration scripts | `AR101A_NxtrIntrpn_Impl.gpj`, `CreateGHSProject.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `AR101A_NxtrIntrpn_Impl/src/NxtrIntrpn.c`. 

Top-level functions defined in `NxtrIntrpn.c` (factual extract, first 19):

- `LnrIntrpn_u16_u16FixdXu16VariY`
- `LnrIntrpn_s16_u16FixdXs16VariY`
- `LnrIntrpn_u16_u16VariXu16VariY`
- `LnrIntrpn_u16_s16VariXu16VariY`
- `LnrIntrpn_s16_s16VariXs16VariY`
- `LnrIntrpn_s16_u16VariXs16VariY`
- `LnrIntrpnWithRound_u16_u16FixdXu16VariY`
- `LnrIntrpnWithRound_s16_u16FixdXs16VariY`
- `LnrIntrpnWithRound_u16_u16VariXu16VariY`
- `LnrIntrpnWithRound_u16_s16VariXu16VariY`
- `LnrIntrpnWithRound_s16_s16VariXs16VariY`
- `LnrIntrpnWithRound_s16_u16VariXs16VariY`
- `BilnrIntrpnWithRound_u16_u16CmnXu16MplY`
- `BilnrIntrpnWithRound_s16_u16CmnXs16MplY`
- `BilnrIntrpnWithRound_s16_s16CmnXs16MplY`
- `BilnrIntrpnWithRound_u16_u16MplXu16MplY`
- `BilnrIntrpnWithRound_u16_s16MplXu16MplY`
- `BilnrIntrpnWithRound_s16_s16MplXs16MplY`
- `BilnrIntrpnWithRound_s16_u16MplXs16MplY`

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

2 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `NxtrIntrpn FDD.docx`

- **Source path in repository:** `AR101A_NxtrIntrpn_Design/Doc/NxtrIntrpn FDD.docx`
- **Format:** `.docx`
- **Size:** `303 KiB`
- **Expected content:** Functional design document (inferred from the file name — assumption).

**Converted content:**

Functional Design Document

For

NxtrIntrpn

VERSION: 1.0

DATE: 20-Feb-2015

Prepared By:

Nexteer Automotive,

Saginaw, MI, USA

Revision History

| Version | Description | Author | Section Modified | Date | Approved By |

| --- | --- | --- | --- | --- | --- |

| 1 .0 | Initial Version | K. Smith | All | 20 -Feb-2015 | Nexteer |

Version

Description

Author

Section Modified

Date

Approved By

1.0

Initial Version

K. Smith

All

20-Feb-2015

Nexteer

Table of Contents

1Abbrevations And Acronyms4

2References5

3Purpose6

4Interpolation Design7

4.1Linear Interpolation7

4.1.1Linear Interpoliation Accuracy8

4.2Fixed X-Axis Linear Interpolation Functions9

4.2.1API9

4.2.1.1Truncating Functions9

4.2.1.2Rounding Functions9

4.3Variable X-Axis Linear Interpolation Functions10

4.3.1API10

4.3.1.1Truncating Functions10

4.3.1.2Rounding Functions12

4.4Bilinear Interpolation14

4.4.1Common X Axis Bilinear Interpolation Functions16

4.4.1.1API16

4.4.2Variable X Axis Bilinear Interpolation Functions19

4.4.2.1API19

5Know Limitations With Design22

6Appendix A23

7Appendix B24

7.1Truncating Linear Interpolation Functions24

7.1.1Fixed X-Axis Interpolation Function24

7.1.2Variable X-Axis Interpolation Function24

7.2Rounding Linear Interpolation Functions24

7.2.1Fixed X-Axis Interpolation Function24

7.2.2Variable X-Axis Interpolation Function24

8Appendix C25

## Abbrevations And Acronyms

| Abbreviation | Description |

| --- | --- |

| BS | Bilinear Select ion |

| API | Application Program Interface |

Abbreviation

Description

BS

Bilinear Selection

API

Application Program Interface

## References

This section lists the title & version of all the documents that are referred for development of this document

| Sr. No. | Title | Version |

| --- | --- | --- |

| Appendix C | RH850/P1x Series User’s Manual: Software | 0.10 Jan, 2014 |

Sr. No.

Title

Version

Appendix C

RH850/P1x Series User’s Manual: Software

0.10 Jan, 2014

## Purpose

The purpose of this document is to describe the functions contained within the Nexteer interpolation library and as an API reference in designing functional requirements, models, and software components.

## Interpolation Design

### Linear Interpolation

Linear interpolation is used to determine an output value between a set of known data points for a given input. In the image below, the input point (x) is between the known points (x0,y0) and (x1,y1).

The linear interpolant is defined as the straight line between the two known points (x0,y0) and (x1,y1) and is defined in equation (1).

|  |  | (1) |

| --- | --- | --- |

(1)

Solving equation (1) for the desired output (y) is described below in equation (2).

|  |  | (2) |

| --- | --- | --- |

(2)

If the delta between neighboring points on the X-axis is the same, equation (2) can be modified with that delta as shown in equation (3).

|  |  | (3) |

| --- | --- | --- |

(3)

### Linear Interpoliation Accuracy

The operations required to perform equations (2) and (3) shall be implemented using fixed point math. This is to save on execution time to perform the interpolation compared to using floating point math functions (See Appendix C). This also means that there can be information loss because the operations can produce results that have more bits than the operands. In order to keep the same number of bits as the operands, the answer must be rounded or truncated.

The interpolation library shall support both truncation and rounding methods in all linear interpolation functions. These methods are described in Appendix B. The error produced by the truncated function results can be +/- one count. Depending on the resolution of the calibration and the resolution required by the design, this may be negligible. The function designer shall use the truncation library functions in all cases where this error is acceptable in order to save on execution time.

### Fixed X-Axis Linear Interpolation Functions

The following functions are available for linear interpolation with a fixed X-axis and are based on equation (3). The table below defines each argument used in the API. Note that some functions require and/or return unsigned or signed values. It is up to the designer to pick the proper interpolation function for their design.

| Argument | Notes |

| --- | --- |

| DeltaX | Provides the delta between points in the  X-axis for  interpolation.  A value of 0 shall return the first value in YTbl. |

| YTbl[] | Y table  values |

| Size | Number of elements in YTbl |

| Inp | Input value (x) . Values that are less than or equal to DeltaX or larger than DeltaX * (Size – 1) will return the first or last value  respectively  from YTbl. |

Argument

Notes

DeltaX

Provides the delta between points in the X-axis for interpolation. A value of 0 shall return the first value in YTbl.

YTbl[]

Y table values

Size

Number of elements in YTbl

Inp

Input value (x). Values that are less than or equal to DeltaX or larger than DeltaX * (Size – 1) will return the first or last value respectively from YTbl.

### API

The input and output variables are defined as uint16 or sint16 for purposes of min and max ranges. However, calibrations with different resolutions, for example u8p8, can be used because they are still represented as a 16-bit value within these functions.

### Truncating Functions

| Function Name | LnrIntrpn_u16_u16FixdXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DeltaX | uint16 | 0 | 65535 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpn_u16_u16FixdXu16VariY

Type

Min

Max

Arguments Passed

DeltaX

uint16

0

65535

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

uint16

0

65535

| Function Name | LnrIntrpn_s16_u16FixdXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DeltaX | uint16 | 0 | 65535 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpn_s16_u16FixdXs16VariY

Type

Min

Max

Arguments Passed

DeltaX

uint16

0

65535

YTbl[]

sint16[]

-32768

32767

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

sint16

-32768

32767

### Rounding Functions

| Function Name | LnrIntrpn WithRound _u16_u16FixdXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DeltaX | uint16 | 0 | 65535 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpnWithRound_u16_u16FixdXu16VariY

Type

Min

Max

Arguments Passed

DeltaX

uint16

0

65535

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

uint16

0

65535

| Function Name | LnrIntrpn WithRound _s16_u16FixdXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | DeltaX | uint16 | 0 | 65535 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpnWithRound_s16_u16FixdXs16VariY

Type

Min

Max

Arguments Passed

DeltaX

uint16

0

65535

YTbl[]

sint16[]

-32768

32767

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

sint16

-32768

32767

### Variable X-Axis Linear Interpolation Functions

The following functions are available for linear interpolation with a variable X-axis and are based on equation (2). The table below defines each argument used in the API. Note that some functions require and/or return unsigned or signed values. It is up to the designer to pick the proper interpolation function for their design.

| Argument | Notes |

| --- | --- |

| XTbl[] | X Table |

| YTbl[] | Y Table |

| Size | Number of elements in  the XTbl and  YTbl |

| Inp | Input value (x) . Values that are less than or equal to XTbl[0] or larger than XTbl[Size – 1] will return the first or last value  respectively  from YTbl. |

Argument

Notes

XTbl[]

X Table

YTbl[]

Y Table

Size

Number of elements in the XTbl and YTbl

Inp

Input value (x). Values that are less than or equal to XTbl[0] or larger than XTbl[Size – 1] will return the first or last value respectively from YTbl.

### API

The input and output variables are defined as uint16 or sint16 for purposes of min and max ranges. However, calibrations with different resolutions, for example u8p8, can be used because they are still represented as a 16-bit value within these functions.

### Truncating Functions

| Function Name | LnrIntrpn_u16_u16VariXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | uint16[] | 0 | 65535 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpn_u16_u16VariXu16VariY

Type

Min

Max

Arguments Passed

XTbl[]

uint16[]

0

65535

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

uint16

0

65535

| Function Name | LnrIntrpn_u16_s16VariXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | sint16[] | -32768 | 32767 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | sint16 | -32768 | 32767 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpn_u16_s16VariXu16VariY

Type

Min

Max

Arguments Passed

XTbl[]

sint16[]

-32768

32767

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

sint16

-32768

32767

Return Value

uint16

0

65535

| Function Name | LnrIntrpn_s16_s16VariXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | sint16[] | -32768 | 32767 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | sint16 | -32768 | 32767 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpn_s16_s16VariXs16VariY

Type

Min

Max

Arguments Passed

XTbl[]

sint16[]

-32768

32767

YTbl[]

sint16[]

-32768

32767

Size

uint16

1

65535

Inp

sint16

-32768

32767

Return Value

sint16

-32768

32767

| Function Name | LnrIntrpn_s16_u16VariXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | uint16[] | 0 | 65535 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpn_s16_u16VariXs16VariY

Type

Min

Max

Arguments Passed

XTbl[]

uint16[]

0

65535

YTbl[]

sint16[]

-32768

32767

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

sint16

-32768

32767

### Rounding Functions

| Function Name | LnrIntrpn WithRound _u16_u16VariXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | uint16[] | 0 | 65535 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpnWithRound_u16_u16VariXu16VariY

Type

Min

Max

Arguments Passed

XTbl[]

uint16[]

0

65535

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

uint16

0

65535

Return Value

uint16

0

65535

| Function Name | LnrIntrpn WithRound _u16_s16VariXu16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | sint16[] | -32768 | 32767 |

|  | YTbl[] | uint16[] | 0 | 65535 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | sint16 | -32768 | 32767 |

| Return Value | uint16 | 0 | 65535 |  |

Function Name

LnrIntrpnWithRound_u16_s16VariXu16VariY

Type

Min

Max

Arguments Passed

XTbl[]

sint16[]

-32768

32767

YTbl[]

uint16[]

0

65535

Size

uint16

1

65535

Inp

sint16

-32768

32767

Return Value

uint16

0

65535

| Function Name | LnrIntrpn WithRound _s16_s16VariXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | sint16[] | -32768 | 32767 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | sint16 | -32768 | 32767 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpnWithRound_s16_s16VariXs16VariY

Type

Min

Max

Arguments Passed

XTbl[]

sint16[]

-32768

32767

YTbl[]

sint16[]

-32768

32767

Size

uint16

1

65535

Inp

sint16

-32768

32767

Return Value

sint16

-32768

32767

| Function Name | LnrIntrpn WithRound _s16_u16VariXs16VariY | Type | Min | Max |

| --- | --- | --- | --- | --- |

| Arguments Passed | XTbl[] | uint16[] | 0 | 65535 |

|  | YTbl[] | sint16[] | -32768 | 32767 |

|  | Size | uint16 | 1 | 65535 |

|  | Inp | uint16 | 0 | 65535 |

| Return Value | sint16 | -32768 | 32767 |  |

Function Name

LnrIntrpnWithRound_s16_u16VariXs16VariY


*... content truncated for brevity; see the source document in the repository. ...*

### `NxtrIntrpn Integration Manual.doc`

- **Source path in repository:** `AR101A_NxtrIntrpn_Impl/doc/NxtrIntrpn Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Libraries](../).
