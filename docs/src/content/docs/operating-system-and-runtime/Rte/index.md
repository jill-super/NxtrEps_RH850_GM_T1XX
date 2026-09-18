---
title: "Runtime Environment (Rte)"
description: "Runtime Environment: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided, customised]
Vector MICROSAR module with project-specific configuration and custom code.
:::

## Purpose and responsibility

The Runtime Environment component belongs to **Operating System and Runtime** in the **Operating System and Runtime Environment** layer. It provides the real-time operating system or the runtime environment for software components.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Rte` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Rte` |  |
| AUTOSAR model | `Rte_bswmd.arxml` |
| Generator output | `AllowedTemplateVariants.json`, `DCFServer.dll`, `DVApplicationManifest.dll`, `DVCfgRteGen.exe`, `DVCvt.exe`, `DVExternalEventAPI.dll`, `DVGenAPI.dll`, `DVImExRes.dll`, `DVImExSrv.dll`, `DVImExSrv4.XmlSerializers.dll`, `DVImExSrv4.dll`, `DVModelServiceAPI.dll` (+13 more) |
| Tooling and integration scripts | `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (1 file(s), e.g. `Rte/autosar/Rte_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

5 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AN-ISC-8-1166_RTE_BRE_without_AUTOSAR_OS.pdf`

- **Source path in repository:** `Rte/doc/AN-ISC-8-1166_RTE_BRE_without_AUTOSAR_OS.pdf`
- **Format:** `.pdf`
- **Size:** `283 KiB`
- **Expected content:** Application note (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `SafetyGuide_Rte.pdf`

- **Source path in repository:** `Rte/doc/SafetyGuide_Rte.pdf`
- **Format:** `.pdf`
- **Size:** `677 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Rte.pdf`

- **Source path in repository:** `Rte/doc/TechnicalReference_Rte.pdf`
- **Format:** `.pdf`
- **Size:** `2239 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_RteAnalyzer.pdf`

- **Source path in repository:** `Rte/doc/TechnicalReference_RteAnalyzer.pdf`
- **Format:** `.pdf`
- **Size:** `539 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AnalysisReport.txt`

- **Source path in repository:** `Rte/tools/RteAnalyzer/demo/Reports/AnalysisReport.txt`
- **Format:** `.txt`
- **Size:** `18 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
/*********************************************************************************************************************
 *  !! B E T A   V E R S I O N !!
 *
 *  These programs are fully operative programs.
 *  However, they are not thoroughly tested yet (beta-version).
 *  With regard to the fact that the programs are a beta-version only,
 *  Vector Informatik's liability shall be expressly excluded in cases of ordinary negligence,
 *  to the extent admissible by law or statute.
 ********************************************************************************************************************/
MICROSAR RTE Analyzer Report
Analyzer Version: 0.7.0 (Beta)
Analysis Time: 15:54:33 2016-07-16
User Name: visso
Computer Name: VISSO6378NBH

Analyzed Files:

GenData/RteAnalyzer/Rte.c
GenData/RteAnalyzer/Rte_OsApplASILCore0.c
GenData/RteAnalyzer/Rte_OsApplQMCore0.c
GenData/RteAnalyzer/Rte_OsApplQMCore1.c
GenData/RteAnalyzer/TSC_ctASILSwc0.c
GenData/RteAnalyzer/TSC_ctASILSwc1.c
GenData/RteAnalyzer/TSC_ctQMSwc0.c
GenData/RteAnalyzer/TSC_ctQMSwc1.c
GenData/RteAnalyzer/TSC_ctQMSwc2.c
GenData/RteAnalyzer/TestControl.c
GenData/RteAnalyzer/ctASILSwc0.c
GenData/RteAnalyzer/ctASILSwc1.c
GenData/RteAnalyzer/ctQMSwc0.c
GenData/RteAnalyzer/ctQMSwc1.c
GenData/RteAnalyzer/ctQMSwc2.c

Configuration:

MaxAtomicMemoryAccess: 2
BswOsApplication: OsApplQMCore0
OsApplications:

  OsApplASILCore0
	CoreId: 0
	IsTrusted: 0
	SafetyLevel: ASIL_B
	Tasks:
	 ASILTaskCore0
		 Priority: 4
		 Preemption: 0
  OsApplQMCore0
	CoreId: 0
	IsTrusted: 0
	SafetyLevel: QM
	Tasks:
	 HighPrioQMTaskCore0
		 Priority: 100
		 Preemption: 0
	 PreemptiveQMTaskCore0
		 Priority: 2
		 Preemption: 1
  OsApplQMCore1
	CoreId: 1
	IsTrusted: 0
	SafetyLevel: QM
	Tasks:
	 QMTaskCore1
		 Priority: 4
		 Preemption: 0

Findings:
------------------------------------------------------------

Found 4 findings of category: 11002 Function may be called recursively
Function TSC_ctQMSwc0_Rte_Call_csRecursion_Operation may be called recursively
D:\Rte\Rte_Analyzer\trunk\Application\demo\GenData\RteAnalyzer\Source\TSC_ctQMSwc0.c 102

Function TSC_ctQMSwc1_Rte_Call_csRecursion_1_Operation may be called recursively
D:\Rte\Rte_Analyzer\trunk\Application\demo\GenData\RteAnalyzer\Source\TSC_ctQMSwc1.c 50

Function csRecursion_1_Operation may be called recursively
D:\Rte\Rte_Analyzer\trunk\Application\demo\GenData\RteAnalyzer\Source\ctQMSwc0.c 267

```
*... truncated (254 more lines in the source file). ...*

Back to [Operating System and Runtime Environment](../).
