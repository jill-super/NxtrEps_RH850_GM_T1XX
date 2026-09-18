---
title: "Diagnostics Manager (ES101A_DiagcMgr)"
description: "Diagnostics Manager: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Diagnostics Manager component belongs to **Power, Thermal and System State** in the **Complex Device Drivers** layer. It manages power supply, power sequencing, temperature monitoring or system state for the electronics.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `ES101A_DiagcMgr_Design` | Design package |
| `ES101A_DiagcMgr_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `ES101A_DiagcMgr_Design` |  |
| Documentation folders | `Doc/`, `Design/`, `Reports/` |
| `ES101A_DiagcMgr_Impl` |  |
| C sources | `DiagcMgr.c`, `DiagcMgrNonRTE.c`, `DiagcMgrProxyAppl0.c`, `DiagcMgrProxyAppl1.c`, `DiagcMgrProxyAppl10.c`, `DiagcMgrProxyAppl2.c`, `DiagcMgrProxyAppl3.c`, `DiagcMgrProxyAppl4.c`, `DiagcMgrProxyAppl5.c`, `DiagcMgrProxyAppl6.c`, `DiagcMgrProxyAppl7.c`, `DiagcMgrProxyAppl8.c` (+3 more) |
| Public headers | `DiagcMgr.h`, `DiagcMgrStaticTypes.h`, `DiagcMgr_private.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `DiagcMgr.dcf`, `DiagcMgr_attr_def.xml`, `DiagcMgr_bswmd.arxml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Generator output | `DiagcMgr_Cfg.c.tt`, `DiagcMgr_Cfg.h.tt`, `DiagcMgr_Generate.bat` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `ES101A_DiagcMgr_Impl.gpj`, `ES101A_DiagcMgr_Impl_Appl0.gpj`, `ES101A_DiagcMgr_Impl_Appl1.gpj`, `ES101A_DiagcMgr_Impl_Appl10.gpj`, `ES101A_DiagcMgr_Impl_Appl2.gpj`, `ES101A_DiagcMgr_Impl_Appl3.gpj`, `ES101A_DiagcMgr_Impl_Appl4.gpj`, `ES101A_DiagcMgr_Impl_Appl5.gpj`, `ES101A_DiagcMgr_Impl_Appl6.gpj`, `ES101A_DiagcMgr_Impl_Appl7.gpj`, `ES101A_DiagcMgr_Impl_Appl8.gpj` (+4 more) |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `ES101A_DiagcMgr_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 15 C source file(s), starting with `ES101A_DiagcMgr_Impl/src/DiagcMgr.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `ES101A_DiagcMgr_Impl/src/DiagcMgrNonRTE.c`, `ES101A_DiagcMgr_Impl/src/DiagcMgrProxyAppl0.c`, `ES101A_DiagcMgr_Impl/src/DiagcMgrProxyAppl1.c`, `ES101A_DiagcMgr_Impl/src/DiagcMgrProxyAppl10.c`, `ES101A_DiagcMgr_Impl/src/DiagcMgrProxyAppl2.c` (and 9 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

5 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ES101A_DiagcMgrProxyX_DDReport.txt`

- **Source path in repository:** `ES101A_DiagcMgr_Design/Reports/ES101A_DiagcMgrProxyX_DDReport.txt`
- **Format:** `.txt`
- **Size:** `7 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES101A_DiagcMgrProxyX_DataDict
21-Jun-2016 18:57:01
Tool Release:  2.38.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------

DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

```
*... truncated (157 more lines in the source file). ...*

### `ES101A_DiagcMgr_DDReport.txt`

- **Source path in repository:** `ES101A_DiagcMgr_Design/Reports/ES101A_DiagcMgr_DDReport.txt`
- **Format:** `.txt`
- **Size:** `9 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Verification of ES101A_DiagcMgr_DataDict
21-Jun-2016 18:57:16
Tool Release:  2.38.0



--------------------------------
DATA CLASS VIOLATION CHECKS
--------------------------------

DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

    Description: ''
      DataScope: 'Auto'
     HeaderFile: 'Rte_Type.h'
      Alignment: -1
       Elements: [2x1 Simulink.BusElement]


DiagcDataRec1 = 

  <a href="matlab:helpPopup Simulink.Bus" style="font-weight:bold">Bus</a> with properties:

```
*... truncated (178 more lines in the source file). ...*

### `DiagcMgrProxy_MDD.doc`

- **Source path in repository:** `ES101A_DiagcMgr_Impl/doc/DiagcMgrProxy_MDD.doc`
- **Format:** `.doc`
- **Size:** `1356 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DiagcMgr_IntegrationManual.doc`

- **Source path in repository:** `ES101A_DiagcMgr_Impl/doc/DiagcMgr_IntegrationManual.doc`
- **Format:** `.doc`
- **Size:** `180 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DiagcMgr_MDD.doc`

- **Source path in repository:** `ES101A_DiagcMgr_Impl/doc/DiagcMgr_MDD.doc`
- **Format:** `.doc`
- **Size:** `6482 KiB`
- **Expected content:** Module design document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Complex Device Drivers](../).
