---
title: "Temperature Monitor (ES005A_TmplMonr)"
description: "Temperature Monitor: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Temperature Monitor component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES005A_TmplMonr_Design` | Design package |
| `ES005A_TmplMonr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES005A_TmplMonr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES005A_TmplMonr_Impl` |  |
| C sources | `TmplMonr.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `TmplMonr.dcf`, `TmplMonr_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES005A_TmplMonr_Impl.gpj`, `RteGen.bat`, `TmplMonr.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES005A_TmplMonr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES005A_TmplMonr_Impl/src/TmplMonr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

6 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `A4412 WD State Diagram 2015_06_09.pdf`

- **Source path in repository:** `ES005A_TmplMonr_Design/Doc/A4412 WD State Diagram 2015_06_09.pdf`
- **Format:** `.pdf`
- **Size:** `13 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ES005 TmplMonr Requirements.pdf`

- **Source path in repository:** `ES005A_TmplMonr_Design/Doc/ES005 TmplMonr Requirements.pdf`
- **Format:** `.pdf`
- **Size:** `38 KiB`
- **Expected content:** Requirements trace (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Temporal Monitor Operation - Graphical Representation.pdf`

- **Source path in repository:** `ES005A_TmplMonr_Design/Doc/Temporal Monitor Operation - Graphical Representation.pdf`
- **Format:** `.pdf`
- **Size:** `101 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ES005A_TmplMonr_DDReport.txt`

- **Source path in repository:** `ES005A_TmplMonr_Design/Reports/ES005A_TmplMonr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `6 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES005A_TmplMonr_DataDict
28-Nov-2016 17:50:47
Tool Release:  2.48.0



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
Call_Spi_AsyncTransmit      	Name does not match required pattern.
Call_Spi_AsyncTransmit      	    Call_          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Transmit       Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_GetGpioPwrOutpEnaFb  	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioSysFlt2A      	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioSysFlt2B      	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioTmplMonrWdg   	.Client:	Name should not contain FDDs <ShoName>
IoHwAb_SetGpioTmplMonrWdg   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Write          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 9, errors: 14)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
(variables: 3, errors: 0)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
TmplMonrIninTestCmpl        	Name does not match required pattern.
(variables: 1, errors: 1)

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
```
*... truncated (66 more lines in the source file). ...*

### `TmplMonr_IntegrationManual.doc`

- **Source path in repository:** `ES005A_TmplMonr_Impl/doc/TmplMonr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TmplMonr_MDD.doc`

- **Source path in repository:** `ES005A_TmplMonr_Impl/doc/TmplMonr_MDD.doc`
- **Format:** `.doc`
- **Size:** `200 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
