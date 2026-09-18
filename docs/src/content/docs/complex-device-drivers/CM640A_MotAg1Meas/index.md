---
title: "Motor Ag1 Measurement (CM640A_MotAg1Meas)"
description: "Motor Ag1 Measurement: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Motor Ag1 Measurement component belongs to **Serial Interfaces and Position Sensing** in the **Complex Device Drivers** layer. It configures serial peripherals or measures rotor, handwheel-torque and handwheel-angle sensors.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM640A_MotAg1Meas_Design` | Design package |
| `CM640A_MotAg1Meas_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM640A_MotAg1Meas_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM640A_MotAg1Meas_Impl` |  |
| C sources | `CDD_MotAg1Meas.c`, `CDD_MotAg1Meas_MotCtrl.c` |
| Public headers | `CDD_MotAg1Meas.h`, `CDD_MotAg1Meas_MotCtrl_MemMap.h`, `CDD_MotAg1Meas_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `MotAg1Meas.dcf`, `MotAg1Meas_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM640A_MotAg1Meas_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `MotAg1Meas.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM640A_MotAg1Meas_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `CM640A_MotAg1Meas_Impl/src/CDD_MotAg1Meas.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `CM640A_MotAg1Meas_Impl/src/CDD_MotAg1Meas_MotCtrl.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

4 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `csih_regs.txt`

- **Source path in repository:** `CM640A_MotAg1Meas_Design/Doc/csih_regs.txt`
- **Format:** `.txt`
- **Size:** `573 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
RegOutpCSIH0CTL0 = DataDict.OpSignal;
RegOutpCSIH0CTL0.LongName = 'Register CSIH0CTL0';
RegOutpCSIH0CTL0.Description = 'Register CSIH0CTL0';
RegOutpCSIH0CTL0.DocUnits = 'Cnt';
RegOutpCSIH0CTL0.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0CTL0.EngDT = dt.u08;
RegOutpCSIH0CTL0.EngInit = 0;
RegOutpCSIH0CTL0.EngMin = 0;
RegOutpCSIH0CTL0.EngMax = 255;
RegOutpCSIH0CTL0.TestTolerance = 1;
RegOutpCSIH0CTL0.WrittenIn = {};
RegOutpCSIH0CTL0.WriteType = 'Phy';

RegOutpCSIH0MBS = DataDict.OpSignal;
RegOutpCSIH0MBS.LongName = 'Register CSIH0MBS';
RegOutpCSIH0MBS.Description = 'Register CSIH0MBS';
RegOutpCSIH0MBS.DocUnits = 'Cnt';
RegOutpCSIH0MBS.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0MBS.EngDT = dt.u08;
RegOutpCSIH0MBS.EngInit = 0;
RegOutpCSIH0MBS.EngMin = 0;
RegOutpCSIH0MBS.EngMax = 1;
RegOutpCSIH0MBS.TestTolerance = 1;
RegOutpCSIH0MBS.WrittenIn = {};
RegOutpCSIH0MBS.WriteType = 'Phy';

RegOutpCSIH0JOBE = DataDict.OpSignal;
RegOutpCSIH0JOBE.LongName = 'Register CSIH0JOBE';
RegOutpCSIH0JOBE.Description = 'Register CSIH0JOBE';
RegOutpCSIH0JOBE.DocUnits = 'Cnt';
RegOutpCSIH0JOBE.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0JOBE.EngDT = dt.u08;
RegOutpCSIH0JOBE.EngInit = 0;
RegOutpCSIH0JOBE.EngMin = 0;
RegOutpCSIH0JOBE.EngMax = 1;
RegOutpCSIH0JOBE.TestTolerance = 1;
RegOutpCSIH0JOBE.WrittenIn = {};
RegOutpCSIH0JOBE.WriteType = 'Phy';

RegOutpCSIH0RXE = DataDict.OpSignal;
RegOutpCSIH0RXE.LongName = 'Register CSIH0RXE';
RegOutpCSIH0RXE.Description = 'Register CSIH0RXE';
RegOutpCSIH0RXE.DocUnits = 'Cnt';
RegOutpCSIH0RXE.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0RXE.EngDT = dt.u08;
RegOutpCSIH0RXE.EngInit = 0;
RegOutpCSIH0RXE.EngMin = 0;
RegOutpCSIH0RXE.EngMax = 1;
RegOutpCSIH0RXE.TestTolerance = 1;
RegOutpCSIH0RXE.WrittenIn = {};
RegOutpCSIH0RXE.WriteType = 'Phy';

RegOutpCSIH0TXE = DataDict.OpSignal;
RegOutpCSIH0TXE.LongName = 'Register CSIH0TXE';
RegOutpCSIH0TXE.Description = 'Register CSIH0TXE';
RegOutpCSIH0TXE.DocUnits = 'Cnt';
RegOutpCSIH0TXE.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0TXE.EngDT = dt.u08;
RegOutpCSIH0TXE.EngInit = 0;
RegOutpCSIH0TXE.EngMin = 0;
RegOutpCSIH0TXE.EngMax = 1;
RegOutpCSIH0TXE.TestTolerance = 1;
RegOutpCSIH0TXE.WrittenIn = {};
RegOutpCSIH0TXE.WriteType = 'Phy';

RegOutpCSIH0PWR = DataDict.OpSignal;
RegOutpCSIH0PWR.LongName = 'Register CSIH0PWR';
RegOutpCSIH0PWR.Description = 'Register CSIH0PWR';
RegOutpCSIH0PWR.DocUnits = 'Cnt';
RegOutpCSIH0PWR.SwcShoName = 'MotAg0Meas';
RegOutpCSIH0PWR.EngDT = dt.u08;
RegOutpCSIH0PWR.EngInit = 0;
RegOutpCSIH0PWR.EngMin = 0;
RegOutpCSIH0PWR.EngMax = 1;
RegOutpCSIH0PWR.TestTolerance = 1;
RegOutpCSIH0PWR.WrittenIn = {};
RegOutpCSIH0PWR.WriteType = 'Phy';

RegOutpCSIH0STR0 = DataDict.OpSignal;
RegOutpCSIH0STR0.LongName = 'Register CSIH0STR0';
```
*... truncated (18088 more lines in the source file). ...*

### `CM640A_MotAg1Meas_DDReport.txt`

- **Source path in repository:** `CM640A_MotAg1Meas_Design/Reports/CM640A_MotAg1Meas_DDReport.txt`
- **Format:** `.txt`
- **Size:** `4 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM640A_MotAg1Meas_DataDict
13-Mar-2016 14:27:38
Tool Release:  2.34.0



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
MotAg1MeasMotAg1CoeffTblRead	.SrvRunnnable:	Name should not contain FDDs <ShoName>
MotAg1MeasMotAg1CoeffTblWr  	.SrvRunnnable:	Name should not contain FDDs <ShoName>
(variables: 2, errors: 2)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 4, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
MotAg1ErrReg                	Cannot match name to list of known Nexteer signals.
MotAg1ParFltCnt             	Cannot match name to list of known Nexteer signals.
MotAg1VltgFltCnt            	Cannot match name to list of known Nexteer signals.
MotCtrlMotAgMecl1Polarity   	Cannot match name to list of known Nexteer signals.
(variables: 5, errors: 4)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
DmaMotAg1RawData            	Cannot match name to list of known Nexteer signals.
(variables: 7, errors: 1)

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
(variables: 3, errors: 0)

-----------------------------------------------
PER-INSTANCE MEMORY:	<Identity>
```
*... truncated (45 more lines in the source file). ...*

### `MotAg1Meas_IntegrationManual.doc`

- **Source path in repository:** `CM640A_MotAg1Meas_Impl/doc/MotAg1Meas_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `147 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MotAg1Meas_MDD.doc`

- **Source path in repository:** `CM640A_MotAg1Meas_Impl/doc/MotAg1Meas_MDD.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
