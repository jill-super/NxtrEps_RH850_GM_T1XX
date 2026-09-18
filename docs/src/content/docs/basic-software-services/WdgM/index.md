---
title: "Watchdog Manager (WdgM)"
description: "Watchdog Manager: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Watchdog Manager component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `WdgM` | Package directory |

## Key files

| Area | Files |
|---|---|
| `WdgM` |  |
| C sources | `NxtrWdgM.c`, `WdgM.c`, `WdgM_Checkpoint.c` |
| Public headers | `NxtrWdgM.h`, `WdgM.h`, `WdgM_Cfg.h` |
| AUTOSAR model | `WdgM_Bswmd.arxml`, `WdgM_BswmdIntBeh.arxml`, `WdgM_preo.arxml` |
| Generator output | `LICENSE`, `SWC_WdgM.xsl`, `Wdg_Mgr_Cfg_Gen.exe` |
| Tooling and integration scripts | `Integrate.bat`, `NxtrWdgM.gpj`, `WdgM.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `WdgM/autosar/WdgM_Bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `WdgM/src/NxtrWdgM.c`. 

Top-level functions defined in `NxtrWdgM.c` (factual extract, first 1):

- `NxtrWdgM_Init`

Additional implementation units: `WdgM/src/WdgM.c`, `WdgM/src/WdgM_Checkpoint.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

5 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `S-WdgM_ReleaseNotes.pdf`

- **Source path in repository:** `WdgM/doc/S-WdgM_ReleaseNotes.pdf`
- **Format:** `.pdf`
- **Size:** `458 KiB`
- **Expected content:** Release notes (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgM_SafetyManual.pdf`

- **Source path in repository:** `WdgM/doc/S-WdgM_SafetyManual.pdf`
- **Format:** `.pdf`
- **Size:** `3764 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgM_Stack_SafetyCase.pdf`

- **Source path in repository:** `WdgM/doc/S-WdgM_Stack_SafetyCase.pdf`
- **Format:** `.pdf`
- **Size:** `335 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgM_UserManual.pdf`

- **Source path in repository:** `WdgM/doc/S-WdgM_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `3104 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `WdgM Integration Manual.doc`

- **Source path in repository:** `WdgM/doc/WdgM Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `130 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
