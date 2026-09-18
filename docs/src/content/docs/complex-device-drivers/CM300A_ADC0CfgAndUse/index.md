---
title: "Analog to Digital Converter 0 Configuration And Use (CM300A_ADC0CfgAndUse)"
description: "Analog to Digital Converter 0 Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Analog to Digital Converter 0 Configuration And Use component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This is a **design package**: it holds the functional/design documents; the implementation lives in the matching implementation package.

## Repository locations

| Directory | Role |
|---|---|
| `CM300A_ADC0CfgAndUse_Design` | Design package |

## Key files

| Area | Files |
|---|---|
| `CM300A_ADC0CfgAndUse_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM300A_Adc0CfgAndUse_DDReport.txt`

- **Source path in repository:** `CM300A_ADC0CfgAndUse_Design/Reports/CM300A_Adc0CfgAndUse_DDReport.txt`
- **Format:** `.txt`
- **Size:** `7 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM300A_Adc0CfgAndUse_DataDict
07-Sep-2016 15:46:06
Tool Release:  2.43.0



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
(variables: 0, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
AdcStrtOfCnvnMotCtrlPeak    	Cannot match name to list of known Nexteer signals.
AdcStrtOfCnvnMotCtrlPeak    	.ReadIn:	Field should contain only valid Periodic & Server Runnable names.	Adc0CfgAndUse is not allowed.
AdcStrtOfCnvnMotCtrlVly     	Cannot match name to list of known Nexteer signals.
AdcStrtOfCnvnMotCtrlVly     	.ReadIn:	Field should contain only valid Periodic & Server Runnable names.	Adc0CfgAndUse is not allowed.
MotCtrlAdcDiagcEndPtrOutp   	Cannot match name to list of known Nexteer signals.
MotCtrlAdcDiagcStrtPtrOutp  	Cannot match name to list of known Nexteer signals.
RegInpADCD0SGSR1            	Cannot match name to list of known Nexteer signals.
RegInpADCD0SGSR1            	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 5, errors: 8)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
DmaAdc0ResTrig              	Cannot match name to list of known Nexteer signals.
DmaAdc0ResTrig              	.WrittenIn:	Field should contain only valid Periodic & Server Runnable names.	Adc0CfgAndUse is not allowed.
RegOutpADCD0SGSTCR0         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD0SGVCEP1         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD0SGVCEP1         	    V              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD0SGVCSP1         	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpADCD0SGVCSP1         	    V              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 4, errors: 7)

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
*... truncated (81 more lines in the source file). ...*

Back to [Complex Device Drivers](../).
