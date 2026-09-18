---
title: "General Motors T1XX Platform EPS RH 850 (GM_T1XX_EPS_RH850)"
description: "General Motors T1XX Platform EPS RH 850: purpose, files, interfaces and reference documents."
---

:::caution[Module origin — Joint integration (Vector + in-house)]
Top-level integration of Vector modules and in-house components.
:::

## Purpose and responsibility

The General Motors T1XX Platform EPS RH 850 component belongs to **Top-Level Integration** in the **System Integration** layer. It integrates the configured software stack for the target controller and vehicle platform.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `GM_T1XX_EPS_RH850` | Package directory |

## Key files

| Area | Files |
|---|---|
| `GM_T1XX_EPS_RH850` |  |
| C sources | `BswM_Callout_Stubs.c`, `CDD_GMLANSdl.c`, `CDD_GmT1xxMcuCfg_Stub.c`, `CalDummy_Stub.c`, `Can_Callouts.c`, `EcuM_Callout_Stubs.c`, `Fee_Callouts.c`, `IoHwAb_30.c`, `Mcal_Callouts_Stub.c`, `OS_Callout_Stubs.c`, `gmheader.c`, `main.c` |
| Public headers | `Appl_Det.h`, `Appl_Mcu.h`, `BswM_UserTypes.h`, `CDD_GmT1xxMcuCfg.h`, `CDD_HwTq0Meas_Cfg.h`, `CDD_HwTq1Meas_Cfg.h`, `CDD_HwTq2Meas_Cfg.h`, `CDD_HwTq3Meas_Cfg.h`, `CDD_MotAg0Meas_Cfg.h`, `CDD_MotAg1Meas_Cfg.h`, `ComM.h`, `ComM_EcuMBswM.h` (+13 more) |
| AUTOSAR model | `EPS.dpa` |
| Generator output | `AR300A_MotCtrlMgr_DDReport.txt`, `AR300A_MotCtrlMgr_DataDict.m`, `Adc0CfgAndUse_GenErrors.log`, `Adc1CfgAndUse_GenErrors.log`, `BswM_Cfg.h`, `BswM_Lcfg.c`, `BswM_PBcfg.c`, `BswM_Private_Cfg.h`, `BswM_XMI21.xml`, `CDD_Adc0CfgAndUse_Cfg.h`, `CDD_Adc1CfgAndUse_Cfg.h`, `CDD_FlsMem_Cfg.c` (+13 more) |
| Tooling and integration scripts | `CreateGenerateGHSProject.bat`, `CreateIncludeGHSProject.bat`, `CreateScriptsGHSProject.bat`, `CreateSrcGHSProject.bat`, `T1xx.gpj`, `dr7f701311.ld`, `generate.gpj`, `include.gpj`, `scripts.gpj`, `src.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 12 C source file(s), starting with `GM_T1XX_EPS_RH850/src/BswM_Callout_Stubs.c`. 

Top-level functions defined in `BswM_Callout_Stubs.c` (factual extract, first 7):

- `BswM_INIT_NvMReadAll`
- `BswM_SHUTDOWN_NvMWriteAll`
- `BswM_ShtdwnHndlg_PrepShutdown`
- `BswM_Restart`
- `BswM_FinalizeShtdwn`
- `BswM_DiagcMgrPwrDwn`
- `BwmM_GetShutdownOngoing`

Additional implementation units: `GM_T1XX_EPS_RH850/src/CDD_GMLANSdl.c`, `GM_T1XX_EPS_RH850/src/CDD_GmT1xxMcuCfg_Stub.c`, `GM_T1XX_EPS_RH850/src/CalDummy_Stub.c`, `GM_T1XX_EPS_RH850/src/Can_Callouts.c`, `GM_T1XX_EPS_RH850/src/EcuM_Callout_Stubs.c` (and 6 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

25 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `DVCfg_AutomationInterfaceDocumentation.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/DaVinciConfigurator/Core/AutomationInterface/_doc/DVCfg_AutomationInterfaceDocumentation.pdf`
- **Format:** `.pdf`
- **Size:** `2251 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AN-ISC-8-1153_ThirdPartyModules.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/ApplicationNotes/AN-ISC-8-1153_ThirdPartyModules.pdf`
- **Format:** `.pdf`
- **Size:** `627 KiB`
- **Expected content:** Application note (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AN-ISC-8-1170_Use_AR3_SWCs_in_AR4.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/ApplicationNotes/AN-ISC-8-1170_Use_AR3_SWCs_in_AR4.pdf`
- **Format:** `.pdf`
- **Size:** `251 KiB`
- **Expected content:** Application note (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AN-ISC-8-1184_Compiler_Warnings.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/ApplicationNotes/AN-ISC-8-1184_Compiler_Warnings.pdf`
- **Format:** `.pdf`
- **Size:** `395 KiB`
- **Expected content:** Application note (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `2482.0_ADD_Nexteer_Nexteer_MSR_GM_Renesas RH850-CBDE1400351.D04.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/DeliveryInformation/2482.0_ADD_Nexteer_Nexteer_MSR_GM_Renesas RH850-CBDE1400351.D04.pdf`
- **Format:** `.pdf`
- **Size:** `35 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `IssueReport_CBD1400351.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/DeliveryInformation/IssueReport_CBD1400351.pdf`
- **Format:** `.pdf`
- **Size:** `359 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ProductInformation_2_MICROSAR_SoftwarePackagesAndMaintenance.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/DeliveryInformation/ProductInformation_2_MICROSAR_SoftwarePackagesAndMaintenance.pdf`
- **Format:** `.pdf`
- **Size:** `219 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Readme_CBD1400351.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/DeliveryInformation/Readme_CBD1400351.pdf`
- **Format:** `.pdf`
- **Size:** `340 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `ReleaseNotes_3rdPartyMCAL_VectorIntegration.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/ReleaseNotes/ReleaseNotes_3rdPartyMCAL_VectorIntegration.pdf`
- **Format:** `.pdf`
- **Size:** `307 KiB`
- **Expected content:** Release notes (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `MICROSAR_Safety_Guide.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/SafetyManuals/MICROSAR_Safety_Guide.pdf`
- **Format:** `.pdf`
- **Size:** `893 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SafetyManual_CBD1400351_D04.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/SafetyManuals/SafetyManual_CBD1400351_D04.pdf`
- **Format:** `.pdf`
- **Size:** `833 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Startup_GM_SLP2.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/Startup_GM_SLP2.pdf`
- **Format:** `.pdf`
- **Size:** `6909 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `Startup_GM_SLP2_vVIRTUALtarget.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/Startup_GM_SLP2_vVIRTUALtarget.pdf`
- **Format:** `.pdf`
- **Size:** `7278 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_3rdParty-MCAL-Integration.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_3rdParty-MCAL-Integration.pdf`
- **Format:** `.pdf`
- **Size:** `692 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Asr_MemoryMapping.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_Asr_MemoryMapping.pdf`
- **Format:** `.pdf`
- **Size:** `477 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Cdd.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_Cdd.pdf`
- **Format:** `.pdf`
- **Size:** `981 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_ComStackLib.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_ComStackLib.pdf`
- **Format:** `.pdf`
- **Size:** `977 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_DaVinciConfigurator_Licenses.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_DaVinciConfigurator_Licenses.pdf`
- **Format:** `.pdf`
- **Size:** `304 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_DiagA2lGen.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_DiagA2lGen.pdf`
- **Format:** `.pdf`
- **Size:** `197 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_ExternalDependenciesOfGenerators.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_ExternalDependenciesOfGenerators.pdf`
- **Format:** `.pdf`
- **Size:** `159 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_GenTool_CsAsrLegacyDb2SystemDescr_Vector.pdf`
- **Format:** `.pdf`
- **Size:** `716 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_MSSV.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_MSSV.pdf`
- **Format:** `.pdf`
- **Size:** `624 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_MSSV_legacy.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_MSSV_legacy.pdf`
- **Format:** `.pdf`
- **Size:** `624 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_SipModificationChecker.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/Doc/TechnicalReferences/TechnicalReference_SipModificationChecker.pdf`
- **Format:** `.pdf`
- **Size:** `437 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `DocumentationGuide_VectorAUTOSAR.pdf`

- **Source path in repository:** `GM_T1XX_EPS_RH850/tools/SIP/DocumentationGuide_VectorAUTOSAR.pdf`
- **Format:** `.pdf`
- **Size:** `75 KiB`
- **Expected content:** Hardware / AUTOSAR reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [System Integration](../).
