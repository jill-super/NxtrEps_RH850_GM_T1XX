---
title: "Timer Synchronous Generator 31 Configuration And Use (CM475A_TSG31CfgAndUse)"
description: "Timer Synchronous Generator 31 Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Timer Synchronous Generator 31 Configuration And Use component belongs to **Analog Acquisition and Timers** in the **Complex Device Drivers** layer. It configures analog-to-digital converters, sensor-measurement triggering or hardware timers.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM475A_TSG31CfgAndUse_Design` | Design package |
| `CM475A_TSG31CfgAndUse_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM475A_TSG31CfgAndUse_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM475A_TSG31CfgAndUse_Impl` |  |
| C sources | `CDD_TSG31CfgAndUse.c`, `CDD_TSG31CfgAndUse_MotCtrl.c` |
| Public headers | `CDD_TSG31CfgAndUse.h`, `CDD_TSG31CfgAndUse_MotCtrl_MemMap.h`, `CDD_TSG31CfgAndUse_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml`, `TSG31CfgAndUse.dcf`, `TSG31CfgAndUse_attr_def.xml` |
| Tooling and integration scripts | `CM475A_TSG31CfgAndUse_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `RteGen.bat`, `TSG31CfgAndUse.dpa` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM475A_TSG31CfgAndUse_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM475A_TSG31CfgAndUse_Impl/src/CDD_TSG31CfgAndUse.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM475A_TSG31CfgAndUse_Impl/src/CDD_TSG31CfgAndUse_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TSG31 Register IO Definitions.txt`

- **Source path in repository:** `CM475A_TSG31CfgAndUse_Design/Doc/TSG31 Register IO Definitions.txt`
- **Format:** `.txt`
- **Size:** `325 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
RegOutpTSG30IOC2 = DataDict.OpSignal;
RegOutpTSG30IOC2.LongName = 'Register TSG30IOC2';
RegOutpTSG30IOC2.Description = 'Register TSG30IOC2';
RegOutpTSG30IOC2.DocUnits = 'Cnt';
RegOutpTSG30IOC2.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30IOC2.EngDT = dt.u16;
RegOutpTSG30IOC2.EngInit = 0;
RegOutpTSG30IOC2.EngMin = 0;
RegOutpTSG30IOC2.EngMax = 65535;
RegOutpTSG30IOC2.TestTolerance = 1;
RegOutpTSG30IOC2.WrittenIn = {};
RegOutpTSG30IOC2.WriteType = 'Phy';

RegOutpTSG30TO1 = DataDict.OpSignal;
RegOutpTSG30TO1.LongName = 'Register TSG30TO1';
RegOutpTSG30TO1.Description = 'Register TSG30TO1';
RegOutpTSG30TO1.DocUnits = 'Cnt';
RegOutpTSG30TO1.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30TO1.EngDT = dt.u08;
RegOutpTSG30TO1.EngInit = 0;
RegOutpTSG30TO1.EngMin = 0;
RegOutpTSG30TO1.EngMax = 1;
RegOutpTSG30TO1.TestTolerance = 1;
RegOutpTSG30TO1.WrittenIn = {};
RegOutpTSG30TO1.WriteType = 'Phy';

RegOutpTSG30TO2 = DataDict.OpSignal;
RegOutpTSG30TO2.LongName = 'Register TSG30TO2';
RegOutpTSG30TO2.Description = 'Register TSG30TO2';
RegOutpTSG30TO2.DocUnits = 'Cnt';
RegOutpTSG30TO2.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30TO2.EngDT = dt.u08;
RegOutpTSG30TO2.EngInit = 0;
RegOutpTSG30TO2.EngMin = 0;
RegOutpTSG30TO2.EngMax = 1;
RegOutpTSG30TO2.TestTolerance = 1;
RegOutpTSG30TO2.WrittenIn = {};
RegOutpTSG30TO2.WriteType = 'Phy';

RegOutpTSG30TO3 = DataDict.OpSignal;
RegOutpTSG30TO3.LongName = 'Register TSG30TO3';
RegOutpTSG30TO3.Description = 'Register TSG30TO3';
RegOutpTSG30TO3.DocUnits = 'Cnt';
RegOutpTSG30TO3.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30TO3.EngDT = dt.u08;
RegOutpTSG30TO3.EngInit = 0;
RegOutpTSG30TO3.EngMin = 0;
RegOutpTSG30TO3.EngMax = 1;
RegOutpTSG30TO3.TestTolerance = 1;
RegOutpTSG30TO3.WrittenIn = {};
RegOutpTSG30TO3.WriteType = 'Phy';

RegOutpTSG30TO4 = DataDict.OpSignal;
RegOutpTSG30TO4.LongName = 'Register TSG30TO4';
RegOutpTSG30TO4.Description = 'Register TSG30TO4';
RegOutpTSG30TO4.DocUnits = 'Cnt';
RegOutpTSG30TO4.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30TO4.EngDT = dt.u08;
RegOutpTSG30TO4.EngInit = 0;
RegOutpTSG30TO4.EngMin = 0;
RegOutpTSG30TO4.EngMax = 1;
RegOutpTSG30TO4.TestTolerance = 1;
RegOutpTSG30TO4.WrittenIn = {};
RegOutpTSG30TO4.WriteType = 'Phy';

RegOutpTSG30TO5 = DataDict.OpSignal;
RegOutpTSG30TO5.LongName = 'Register TSG30TO5';
RegOutpTSG30TO5.Description = 'Register TSG30TO5';
RegOutpTSG30TO5.DocUnits = 'Cnt';
RegOutpTSG30TO5.SwcShoName = 'TSG31CfgAndUse';
RegOutpTSG30TO5.EngDT = dt.u08;
RegOutpTSG30TO5.EngInit = 0;
RegOutpTSG30TO5.EngMin = 0;
RegOutpTSG30TO5.EngMax = 1;
RegOutpTSG30TO5.TestTolerance = 1;
RegOutpTSG30TO5.WrittenIn = {};
RegOutpTSG30TO5.WriteType = 'Phy';

RegOutpTSG30TO6 = DataDict.OpSignal;
RegOutpTSG30TO6.LongName = 'Register TSG30TO6';
```
*... truncated (10000 more lines in the source file). ...*

### `CM475A_TSG31CfgAndUse_DDReport.txt`

- **Source path in repository:** `CM475A_TSG31CfgAndUse_Design/Reports/CM475A_TSG31CfgAndUse_DDReport.txt`
- **Format:** `.txt`
- **Size:** `9 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM475A_TSG31CfgAndUse_DataDict
27-Sep-2016 08:29:33
Tool Release:  2.47.0



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
IoHwAb_SetFctGpioPhaALowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctGpioPhaAUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctGpioPhaBLowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctGpioPhaBUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctGpioPhaCLowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctGpioPhaCUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaALowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaALowrCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaAUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaAUpprCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaBLowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaBLowrCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaBUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaBUpprCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaCLowrCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaCLowrCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaCUpprCmd	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetFctPeriphPhaCUpprCmd	    Periph         Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaALowrCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaAUpprCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaBLowrCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaBUpprCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaCLowrCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
IoHwAb_SetGpioPhaCUpprCmd   	    Ab_            Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 18, errors: 24)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotCtrlMotCurrEolCalSt      	Cannot match name to list of known Nexteer signals.
(variables: 7, errors: 1)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotCtrlTSG31CMP0E           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMP12E          	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPUE           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPUE           	    U              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPVE           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPVE           	    V              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPWE           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31DCMP0E          	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpTSG31CMP0E           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpTSG31CMP11E          	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegOutpTSG31CMP12E          	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
```
*... truncated (82 more lines in the source file). ...*

### `TSG31CfgAndUse Integration Manual.doc`

- **Source path in repository:** `CM475A_TSG31CfgAndUse_Impl/doc/TSG31CfgAndUse Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `142 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TSG31CfgAndUse_MDD.doc`

- **Source path in repository:** `CM475A_TSG31CfgAndUse_Impl/doc/TSG31CfgAndUse_MDD.doc`
- **Format:** `.doc`
- **Size:** `216 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
