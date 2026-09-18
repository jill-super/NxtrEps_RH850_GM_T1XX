---
title: "Assist High Frequency (SF028A_AssiHiFrq)"
description: "Assist High Frequency: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Assist High Frequency component belongs to **Steering Functions** in the **Application Software** layer. It implements one steering-control feature (assist, damping, return, compensation or protection) as an AUTOSAR software component.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `SF028A_AssiHiFrq_Design` | Design package |
| `SF028A_AssiHiFrq_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `SF028A_AssiHiFrq_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `SF028A_AssiHiFrq_Impl` |  |
| C sources | `AssiHiFrq.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `AssiHiFrq.dcf`, `AssiHiFrq_attr_def.xml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `AssiHiFrq.dpa`, `AssiHiFrq.nz63rn.silent.dcusr`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DVCfgCmd.log`, `RteGen.bat`, `SF028A_AssiHiFrq_Impl.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `SF028A_AssiHiFrq_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `SF028A_AssiHiFrq_Impl/src/AssiHiFrq.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. Modern Word files are converted inline below; legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `SF028A_AssiHiFrq_DDReport.txt`

- **Source path in repository:** `SF028A_AssiHiFrq_Design/Reports/SF028A_AssiHiFrq_DDReport.txt`
- **Format:** `.txt`
- **Size:** `7 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of SF028A_AssiHiFrq_DataDict
02-Jun-2016 10:29:21
Tool Release:  2.40.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
[Warning: In workspace, Struct.EngMin has been increased to the EngMin of the
Struct data type. Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.40.0\+bt\@struct\struct.m',44,1)">struct.struct>struct.validateUserEngMin at 44</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.40.0\+DataDict\@PIM\PIM.m',139,1)">PIM.PIM>PIM.set.EngMin at 139</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\01. EA4_FDDs\SF028A_AssiHiFrq_Design\02_June_2016\SF028A_AssiHiFrq_Design\SF028A_AssiHiFrq_Design\Design\SF028A_AssiHiFrq_DataDict.m',401,1)">SF028A_AssiHiFrq_DataDict at 401</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>ImportVars at 1798
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 240] 
[Warning: In workspace, Struct.EngMax has been increased to the EngMax of the
Struct data type. Please update your saved files.] 
[> In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.40.0\+bt\@struct\struct.m',72,1)">struct.struct>struct.validateUserEngMax at 72</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Data_Management v2.40.0\+DataDict\@PIM\PIM.m',149,1)">PIM.PIM>PIM.set.EngMax at 149</a>
  In <a href="matlab: opentoline('C:\Users\xzb1db\Desktop\Sneha_Work\01. EA4_FDDs\SF028A_AssiHiFrq_Design\02_June_2016\SF028A_AssiHiFrq_Design\SF028A_AssiHiFrq_Design\Design\SF028A_AssiHiFrq_DataDict.m',402,1)">SF028A_AssiHiFrq_DataDict at 402</a>
  In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\matlab\lang\run.m',63,1)">run at 63</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>ImportVars at 1798
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 240] 
(errors: 2)
[Warning: SF028A_AssiHiFrq (blockdiagram.xml, line 2334):
"<a href="matlab:open_and_hilite_system ('SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrqPer1/FilHpUpdGain','error')">SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrqPer1/FilHpUpdGain</a>" is a parameterized link.
To view, discard, or propagate the changes for this link, use the "Library Link"
menu item] 
[> In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\simulink\simulink\load_system.m',21,1)">load_system at 21</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2226
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 
[Warning: SF028A_AssiHiFrq (blockdiagram.xml, line 2361):
"<a href="matlab:open_and_hilite_system ('SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrqPer1/FilHpUpdOutp','error')">SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrqPer1/FilHpUpdOutp</a>" is a parameterized link.
To view, discard, or propagate the changes for this link, use the "Library Link"
menu item] 
[> In <a href="matlab: opentoline('C:\Program Files\MATLAB\R2013b\toolbox\simulink\simulink\load_system.m',21,1)">load_system at 21</a>
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>ModelDDTest at 2226
  In C:\Users\xzb1db\Desktop\Sneha_Work\04. FDD_Tools\Tools v1.12.0\Design_Tools\VerifyDD.p>VerifyDD at 281] 

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
(variables: 2, errors: 0)

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
(variables: 3, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
AssiHiFrqCmd                	Name does not match required pattern.
(variables: 1, errors: 1)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
```
*... truncated (62 more lines in the source file). ...*

### `AssiHiFrq_Integration_Manual.doc`

- **Source path in repository:** `SF028A_AssiHiFrq_Impl/doc/AssiHiFrq_Integration_Manual.doc`
- **Format:** `.doc`
- **Size:** `137 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AssiHiFrq_MDD.docx`

- **Source path in repository:** `SF028A_AssiHiFrq_Impl/doc/AssiHiFrq_MDD.docx`
- **Format:** `.docx`
- **Size:** `100 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

**Converted content:**

Module Design Document

For

AssiHiFrq

February 9, 2017

Prepared For:

Software Engineering

Nexteer Automotive,

Saginaw, MI, USA

Prepared By:

Matthew Leser,

Nexteer Automotive,

Saginaw, MI, USA

Change History

| Description | Author | Version | Date |

| --- | --- | --- | --- |

| Initial Version | Kathleen  Creager | 01.00.00 | 04-Aug-2015 |

| Updated per design  vers . 1.1.0 | Matthew Leser | 2.0 | 09-Feb-2017 |

Description

Author

Version

Date

Initial Version

Kathleen Creager

01.00.00

04-Aug-2015

Updated per design vers. 1.1.0

Matthew Leser

2.0

09-Feb-2017

Table of Contents

1AssiHiFrq High-Level Description4

2Design details of software module5

2.1Graphical representation of AssiHiFrq5

2.2Data Flow Diagram5

2.2.1Component level DFD5

2.2.2Function level DFD5

3Constant Data Dictionary6

3.1Program (fixed) Constants6

3.1.1Embedded Constants6

4Software Component Implementation7

4.1Sub-Module Functions7

4.1.1Init: AssiHiFrqInit17

4.1.1.1Design Rationale7

4.1.1.2Module Outputs7

4.1.2Per: AssiHiFrqPer17

4.1.2.1Design Rationale7

4.1.2.2Store Module Inputs to Local copies7

4.1.2.3(Processing of function)………7

4.1.2.4Store Local copy of outputs into Module Outputs7

4.2Server Runables7

4.3Interrupt Functions8

4.4Module Internal (Local) Functions8

4.5GLOBAL Function/Macro Definitions8

5Known Limitations with Design9

6UNIT TEST CONSIDERATION10

Appendix AAbbreviations and Acronyms11

Appendix BGlossary12

Appendix CReferences13

## AssiHiFrq High-Level Description

Implements the SF028A_AssiHiFrq_Design FDD. This function provides a means of compensating for system

inertia and road feedback. It is tunable over both vehicle speed and handwheel torque to obtain the desired

level of disturbance rejection under various operating conditions. It passes handwheel torque through a high-pass

filter and multiplies the resulting signal by a tunable gain factor. The output is known as high-frequency assist

and is simply added to the usual assist calculated elsewhere

## Design details of software module

### Graphical representation of AssiHiFrq

### Data Flow Diagram

#### Component level DFD

#### Function level DFD

## Constant Data Dictionary

### Program (fixed) Constants

#### Embedded Constants

#### Local Constants

| Constant Name | Resolution | Units | Value |

| --- | --- | --- | --- |

| None | <Refer MDD guidelines [1]> | <Refer MDD guidelines [1]> | <Refer MDD guidelines [1]> |

Constant Name

Resolution

Units

Value

None

<Refer MDD guidelines [1]>

<Refer MDD guidelines [1]>

<Refer MDD guidelines [1]>

## Software Component Implementation

### Sub-Module Functions

### Init: AssiHiFrqInit1

### Design Rationale

Init function is present in DataDict.m file but not shown in FDD model, and no initialization logic is needed.  This is implemented as an empty function.

### Module Outputs

None

### Per: AssiHiFrqPer1

### Design Rationale

FDD model does not contain a block named AssiHiFrqPer1; this function implements the AssiHiFrq block.

BilnrIntrpnWithRound_u16_u16MplXu16MplY function from NxtrIntrpn library used to implement the 2-D Lookup tables in the SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrq/Determine Gain model block.

Blnd_f32 function from NxtrMath library used to implement the part of the model that computes GainVal_MtrNmpHwNm from the outputs of the three bilinear interpolation functions in the SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrq/Determine Gain model block.

FilHpUpdGain  and FilHpUpdOutp_f32 functions from the NxtrFil library used to implement HP-CF Filter block in the SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrq model block.

A note in the model mentions that the frequency lookup table for the high pass filter cutoff frequency could be converted to the filter gain values at initialization.  This was not done because the DataDict.m file did not contain the necessary IRV for the converted table, and the FilHpUpdGain library function expects frequency in Hz; if this throughput improvement (converting the frequency table once in initialization) is made in the future, a new version of FilHpUpdGain will be needed.

LnrIntrpn_u16_u16VariXu16VariY function from NxtrIntrpn library used to implement the “freq lookup” block in the SF028A_AssiHiFrq/AssiHiFrq/AssiHiFrq model block.

### Store Module Inputs to Local copies

See FDD

### (Processing of function)………

See FDD, and design rationale noted above.

### Store Local copy of outputs into Module Outputs

See FDD

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

| 2 | MDD Guideline | EA4 01.00 .00 |

| 3 | EA4  Software Naming Conventions.doc | 01.00.00 |

| 4 | Software Design and Coding Standards.doc | 2. 1 |

| 5 | SF028A_AssiHiFrq_Design | See Synergy subproject version |

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

EA4 Software Naming Conventions.doc

01.00.00

4

Software Design and Coding Standards.doc

2.1

5

SF028A_AssiHiFrq_Design

See Synergy subproject version

Back to [Application Software](../).
