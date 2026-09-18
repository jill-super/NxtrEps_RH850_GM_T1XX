---
title: "General Motors T1XX Platform Microcontroller Unit Configuration (CM010A_GmT1xxMcuCfg)"
description: "General Motors T1XX Platform Microcontroller Unit Configuration: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The General Motors T1XX Platform Microcontroller Unit Configuration component belongs to **Top-Level Integration** in the **System Integration** layer. It integrates the configured software stack for the target controller and vehicle platform.

This is a **design package**: it holds the functional/design documents; the implementation lives in the matching implementation package.

## Repository locations

| Directory | Role |
|---|---|
| `CM010A_GmT1xxMcuCfg_Design` | Design package |

## Key files

| Area | Files |
|---|---|
| `CM010A_GmT1xxMcuCfg_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

2 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `pic_regs.txt`

- **Source path in repository:** `CM010A_GmT1xxMcuCfg_Design/Doc/pic_regs.txt`
- **Format:** `.txt`
- **Size:** `587 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
RegOutpPIC1ASST = DataDict.OpSignal;
RegOutpPIC1ASST.LongName = 'Register PIC1ASST';
RegOutpPIC1ASST.Description = 'Register PIC1ASST';
RegOutpPIC1ASST.DocUnits = 'Cnt';
RegOutpPIC1ASST.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASST.EngDT = dt.u08;
RegOutpPIC1ASST.EngInit = 0;
RegOutpPIC1ASST.EngMin = 0;
RegOutpPIC1ASST.EngMax = 255;
RegOutpPIC1ASST.TestTolerance = 1;
RegOutpPIC1ASST.WrittenIn = {};
RegOutpPIC1ASST.WriteType = 'Phy';

RegOutpPIC1ASYNCTRG = DataDict.OpSignal;
RegOutpPIC1ASYNCTRG.LongName = 'Register PIC1ASYNCTRG';
RegOutpPIC1ASYNCTRG.Description = 'Register PIC1ASYNCTRG';
RegOutpPIC1ASYNCTRG.DocUnits = 'Cnt';
RegOutpPIC1ASYNCTRG.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASYNCTRG.EngDT = dt.u08;
RegOutpPIC1ASYNCTRG.EngInit = 0;
RegOutpPIC1ASYNCTRG.EngMin = 0;
RegOutpPIC1ASYNCTRG.EngMax = 1;
RegOutpPIC1ASYNCTRG.TestTolerance = 1;
RegOutpPIC1ASYNCTRG.WrittenIn = {};
RegOutpPIC1ASYNCTRG.WriteType = 'Phy';

RegOutpPIC1ASSER0 = DataDict.OpSignal;
RegOutpPIC1ASSER0.LongName = 'Register PIC1ASSER0';
RegOutpPIC1ASSER0.Description = 'Register PIC1ASSER0';
RegOutpPIC1ASSER0.DocUnits = 'Cnt';
RegOutpPIC1ASSER0.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASSER0.EngDT = dt.u16;
RegOutpPIC1ASSER0.EngInit = 0;
RegOutpPIC1ASSER0.EngMin = 0;
RegOutpPIC1ASSER0.EngMax = 65535;
RegOutpPIC1ASSER0.TestTolerance = 1;
RegOutpPIC1ASSER0.WrittenIn = {};
RegOutpPIC1ASSER0.WriteType = 'Phy';

RegOutpPIC1ASSER000 = DataDict.OpSignal;
RegOutpPIC1ASSER000.LongName = 'Register PIC1ASSER000';
RegOutpPIC1ASSER000.Description = 'Register PIC1ASSER000';
RegOutpPIC1ASSER000.DocUnits = 'Cnt';
RegOutpPIC1ASSER000.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASSER000.EngDT = dt.u08;
RegOutpPIC1ASSER000.EngInit = 0;
RegOutpPIC1ASSER000.EngMin = 0;
RegOutpPIC1ASSER000.EngMax = 1;
RegOutpPIC1ASSER000.TestTolerance = 1;
RegOutpPIC1ASSER000.WrittenIn = {};
RegOutpPIC1ASSER000.WriteType = 'Phy';

RegOutpPIC1ASSER001 = DataDict.OpSignal;
RegOutpPIC1ASSER001.LongName = 'Register PIC1ASSER001';
RegOutpPIC1ASSER001.Description = 'Register PIC1ASSER001';
RegOutpPIC1ASSER001.DocUnits = 'Cnt';
RegOutpPIC1ASSER001.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASSER001.EngDT = dt.u08;
RegOutpPIC1ASSER001.EngInit = 0;
RegOutpPIC1ASSER001.EngMin = 0;
RegOutpPIC1ASSER001.EngMax = 1;
RegOutpPIC1ASSER001.TestTolerance = 1;
RegOutpPIC1ASSER001.WrittenIn = {};
RegOutpPIC1ASSER001.WriteType = 'Phy';

RegOutpPIC1ASSER002 = DataDict.OpSignal;
RegOutpPIC1ASSER002.LongName = 'Register PIC1ASSER002';
RegOutpPIC1ASSER002.Description = 'Register PIC1ASSER002';
RegOutpPIC1ASSER002.DocUnits = 'Cnt';
RegOutpPIC1ASSER002.SwcShoName = 'GmT1xxMcuCfg';
RegOutpPIC1ASSER002.EngDT = dt.u08;
RegOutpPIC1ASSER002.EngInit = 0;
RegOutpPIC1ASSER002.EngMin = 0;
RegOutpPIC1ASSER002.EngMax = 1;
RegOutpPIC1ASSER002.TestTolerance = 1;
RegOutpPIC1ASSER002.WrittenIn = {};
RegOutpPIC1ASSER002.WriteType = 'Phy';

RegOutpPIC1ASSER003 = DataDict.OpSignal;
RegOutpPIC1ASSER003.LongName = 'Register PIC1ASSER003';
```
*... truncated (15424 more lines in the source file). ...*

### `CM010A_GmT1xxMcuCfg_DDReport.txt`

- **Source path in repository:** `CM010A_GmT1xxMcuCfg_Design/Reports/CM010A_GmT1xxMcuCfg_DDReport.txt`
- **Format:** `.txt`
- **Size:** `14 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM010A_GmT1xxMcuCfg_DataDict
06-Dec-2016 14:45:45
Tool Release:  2.49.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF099A
--------------------------------------------------------------
CM010A              	1xx		Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variable: 1, errors: 1)

----------------------------
DATA DICTIONARY FILENAME:
----------------------------
(errors:  0)

------------------------------------------------------------
RUNNABLE:	<ShoName>Per<Number>  or  <ShoName>Init<Number>
------------------------------------------------------------
GmT1xxMcuCfgInit1           	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
GmT1xxMcuCfgInit2           	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
GmT1xxMcuCfgInit3           	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
GmT1xxMcuCfgPer1            	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
GmT1xxMcuCfgPer2            	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
GmT1xxMcuCfgPer3            	    1xx            Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 6, errors: 6)

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
Adc1RawRes                  	Name does not match required pattern. Correct format is MotCtrl<Identity>.
(variables: 28, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
BattVltgSwd2AdcFaild        	Cannot match name to list of known Nexteer signals.
MotAg2CosAdcFaild           	Cannot match name to list of known Nexteer signals.
MotAg2SinAdcFaild           	Cannot match name to list of known Nexteer signals.
MotCurrAdcPeakDAdcFaild     	Cannot match name to list of known Nexteer signals.
MotCurrAdcPeakEAdcFaild     	Cannot match name to list of known Nexteer signals.
MotCurrAdcPeakFAdcFaild     	Cannot match name to list of known Nexteer signals.
MotCurrAdcVlyDAdcFaild      	Cannot match name to list of known Nexteer signals.
MotCurrAdcVlyEAdcFaild      	Cannot match name to list of known Nexteer signals.
MotCurrAdcVlyFAdcFaild      	Cannot match name to list of known Nexteer signals.
MotCurrSnsrOffs2AdcFaild    	Cannot match name to list of known Nexteer signals.
(variables: 54, errors: 10)

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
```
*... truncated (182 more lines in the source file). ...*

Back to [System Integration](../).
