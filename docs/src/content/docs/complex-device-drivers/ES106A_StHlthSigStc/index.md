---
title: "Steering Health Signal Static (ES106A_StHlthSigStc)"
description: "Steering Health Signal Static: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Steering Health Signal Static component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES106A_StHlthSigStc_Design` | Design package |
| `ES106A_StHlthSigStc_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES106A_StHlthSigStc_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES106A_StHlthSigStc_Impl` |  |
| C sources | `StHlthSigStc.c` |
| Public headers | `StHlthSigStc.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `StHlthSigStc.dcf`, `StHlthSigStc_attr_def.xml`, `StHlthSigStc_bswmd.arxml` |
| Generator output | `StHlthSigStc_Cfg.c.tt`, `StHlthSigStc_Cfg.h.tt`, `StHlthSigStc_Generate.bat`, `StHlthSigStc_helper.tt` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DVCfgCmd.log`, `ES106A_StHlthSigStc_Impl.gpj`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `ES106A_StHlthSigStc_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES106A_StHlthSigStc_Impl/src/StHlthSigStc.c`. 

Top-level functions defined in `StHlthSigStc.c` (factual extract, first 3):

- `NONTRUSTED_NtWrapS_StHlthSigStc_ClrDataSample`
- `NONTRUSTED_NtWrapS_StHlthSigStc_UpdNvmPim`
- `NONTRUSTED_NtWrapS_StHlthSigStc_UpdDataSample`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES106A_StHlthSigStc_DDReport.txt`

- **Source path in repository:** `ES106A_StHlthSigStc_Design/Reports/ES106A_StHlthSigStc_DDReport.txt`
- **Format:** `.txt`
- **Size:** `3 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES106A_StHlthSigStc_DataDict
21-Nov-2016 10:04:29
Tool Release:  2.51.0



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
(variables: 1, errors: 0)

--------------------------------------
SrvRunnable:	<TriggerName>
--------------------------------------
(variables: 4, errors: 0)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 2, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
StHlthSig                   	Cannot match name to list of known Nexteer signals.
(variables: 1, errors: 1)

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
(variables: 1, errors: 0)

------------------------------------------
DISPLAY VARIABLES:	d<ShoName><Identity>
------------------------------------------
(variables: 0, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
-----------------------------------------------
(variables: 6, errors: 0)

--------------------------------------------------------------------------------------------
CONSTANTS:	(ALL CAPS) required: 
						 For "Global" CONSTANTS --- <SHONAME>_<IDENTITY>_<UNITS>_<DATATYPE>
```
*... truncated (34 more lines in the source file). ...*

### `StHlthSigStc_IntegrationManual.doc`

- **Source path in repository:** `ES106A_StHlthSigStc_Impl/doc/StHlthSigStc_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `181 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `StHlthSigStc_MDD.doc`

- **Source path in repository:** `ES106A_StHlthSigStc_Impl/doc/StHlthSigStc_MDD.doc`
- **Format:** `.doc`
- **Size:** `212 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
