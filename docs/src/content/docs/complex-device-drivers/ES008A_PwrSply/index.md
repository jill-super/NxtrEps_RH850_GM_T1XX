---
title: "Power Supply (ES008A_PwrSply)"
description: "Power Supply: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Power Supply component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES008A_PwrSply_Design` | Design package |
| `ES008A_PwrSply_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES008A_PwrSply_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES008A_PwrSply_Impl` |  |
| C sources | `PwrSply.c` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `PwrSply.dcf`, `PwrSply_attr_def.xml` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `ES008A_PwrSply_Impl.gpj`, `PwrSply.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `ES008A_PwrSply_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `ES008A_PwrSply_Impl/src/PwrSply.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES008A_PwrSply_DDReport.txt`

- **Source path in repository:** `ES008A_PwrSply_Design/Reports/ES008A_PwrSply_DDReport.txt`
- **Format:** `.txt`
- **Size:** `6 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES008A_PwrSply_DataDict
12-Sep-2016 15:55:16
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
Call_Spi_AsyncTransmit      	Name does not match required pattern.
Call_Spi_AsyncTransmit      	    Call_          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Call_Spi_AsyncTransmit      	    Transmit       Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_ReadIB                  	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Spi_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    Write          Unknown Keyword used.Only Nexteer approved Keywords should be used.
Spi_WriteIB                 	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 4, errors: 9)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
PhyElecPwrSteerEna          	Cannot match name to list of known Nexteer signals.
PhyTurnOffDly               	Cannot match name to list of known Nexteer signals.
(variables: 3, errors: 2)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
(variables: 8, errors: 0)

---------------------------------------
INTER-RUNNABLE VARIABLES:	<Identity>
---------------------------------------
(variables: 0, errors: 0)

------------------------------------
CALIBRATIONS:	<ShoName><Identity>
------------------------------------
(variables: 6, errors: 0)

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
*... truncated (65 more lines in the source file). ...*

### `PwrSply_IntegrationManual.doc`

- **Source path in repository:** `ES008A_PwrSply_Impl/doc/PwrSply_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `138 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `PwrSply_MDD.doc`

- **Source path in repository:** `ES008A_PwrSply_Impl/doc/PwrSply_MDD.doc`
- **Format:** `.doc`
- **Size:** `130 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
