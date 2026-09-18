---
title: "Direct Memory Access Configuration And Use (CM200A_DmaCfgAndUse)"
description: "Direct Memory Access Configuration And Use: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Direct Memory Access Configuration And Use component belongs to **Direct Memory Access** in the **Complex Device Drivers** layer. It configures and uses the direct-memory-access controller.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `CM200A_DmaCfgAndUse_Design` | Design package |
| `CM200A_DmaCfgAndUse_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `CM200A_DmaCfgAndUse_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `CM200A_DmaCfgAndUse_Impl` |  |
| C sources | `CDD_DmaCfgAndUse.c` |
| Public headers | `CDD_DmaCfgAndUse.h`, `NxtrDmaRegs.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `DmaCfgAndUse.dcf`, `DmaCfgAndUse_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `CM200A_DmaCfgAndUse_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreateQACProject.bat`, `DmaCfgAndUse.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `CM200A_DmaCfgAndUse_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `CM200A_DmaCfgAndUse_Impl/src/CDD_DmaCfgAndUse.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CM200A_DmaCfgAndUse_DDReport.txt`

- **Source path in repository:** `CM200A_DmaCfgAndUse_Design/Reports/CM200A_DmaCfgAndUse_DDReport.txt`
- **Format:** `.txt`
- **Size:** `9 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of CM200A_DmaCfgAndUse_DataDict
21-Dec-2015 13:02:33
Tool Release:  2.22.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------
(errors: 0)

---------------------------------------------------------------
FDD DEFINITION VARIABLE:	<Type><Number><Variant>  e.g. SF099A
--------------------------------------------------------------
CM200A              	.DesignASIL: Field is empty.
CM200A              	.Dependencies: Wrong format is being used. Convert it into a new format Ex:{'<FDD ShoName>','SignlCondn','MotCtrlPrmEstimn'}.
CM200A              	.Dependencies: Wrong format is being used. Convert it into a new format Ex:{'<FDD ShoName>','SignlCondn','MotCtrlPrmEstimn'}.
(variable: 1, errors: 3)

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
DmaWaitForMotCtrlTo2MilliSecTrf	.Return.TestTolerance	Field is empty.
(variables: 2, errors: 1)

-----------------------
Client:	<TriggerName>
-------------------------
(variables: 3, errors: 0)

----------------------------
INPUT SIGNALS:	<Identity>
----------------------------
DmaAdc0ResTrig              	Cannot match name to list of known Nexteer signals.
DmaAdc1ResTrig              	Cannot match name to list of known Nexteer signals.
DmaMotAg0RawData            	Cannot match name to list of known Nexteer signals.
DmaMotAg0SpiStrt            	Cannot match name to list of known Nexteer signals.
DmaMotAg1RawData            	Cannot match name to list of known Nexteer signals.
DmaMotAg1SpiStrt            	Cannot match name to list of known Nexteer signals.
DmaTSG31Upd                 	Cannot match name to list of known Nexteer signals.
DmaTSG31Upd                 	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
DmaVlyTrig                  	Cannot match name to list of known Nexteer signals.
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	Name does not match required pattern. Correct format is <ShoName>_<Identity>_<Element>
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	Cannot match name to list of known Nexteer signals.
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	.EngInit:    	Field is empty.
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	    Mgr_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	    Two            Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_MotCtrlToTwoMilliSec_Rec	    Sec_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	Name does not match required pattern. Correct format is <ShoName>_<Identity>_<Element>
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	Cannot match name to list of known Nexteer signals.
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	.EngInit:    	Field is empty.
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	    Mgr_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	    Two            Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_TwoMilliSecToMotCtrl_Rec	    Ctrl_          Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31CMPWE           	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlTSG31DCMP0E          	    G              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpCSIH1RX0W             	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpCSIH1RX0W             	    H              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpCSIH3RX0W             	    I              Unknown Keyword used.Only Nexteer approved Keywords should be used.
RegInpCSIH3RX0W             	    H              Unknown Keyword used.Only Nexteer approved Keywords should be used.
(variables: 17, errors: 27)

-----------------------------
OUTPUT SIGNALS:	<Identity>
-----------------------------
MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec	Name does not match required pattern. Correct format is <ShoName>_<Identity>_<Element>
MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec	.EngInit:    	Field is empty.
MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec	    Mgr_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec	    Two            Unknown Keyword used.Only Nexteer approved Keywords should be used.
MotCtrlMgr_MotCtrlFromTwoMilliSec_Rec	    Sec_           Unknown Keyword used.Only Nexteer approved Keywords should be used.
```
*... truncated (90 more lines in the source file). ...*

### `DmaCfgAndUse_Integration_Manual.doc`

- **Source path in repository:** `CM200A_DmaCfgAndUse_Impl/doc/DmaCfgAndUse_Integration_Manual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DmaCfgAndUse_MDD.doc`

- **Source path in repository:** `CM200A_DmaCfgAndUse_Impl/doc/DmaCfgAndUse_MDD.doc`
- **Format:** `.doc`
- **Size:** `191 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
