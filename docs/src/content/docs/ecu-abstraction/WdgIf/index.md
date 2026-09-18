---
title: "Watchdog Interface (WdgIf)"
description: "Watchdog Interface: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Watchdog Interface component belongs to **Hardware Abstraction Interfaces** in the **Electronic Control Unit Abstraction** layer. It abstracts the microcontroller hardware behind an AUTOSAR interface.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `WdgIf` | Package directory |

## Key files

| Area | Files |
|---|---|
| `WdgIf` |  |
| C sources | `WdgIf.c` |
| Public headers | `WdgIf.h`, `WdgIf_Cfg.h`, `WdgIf_Types.h` |
| AUTOSAR model | `WdgIf_Bswmd.arxml`, `WdgIf_preo.arxml` |
| Generator output | `LICENSE`, `Wdg_If_Cfg_Gen.exe` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `WdgIf.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `WdgIf/autosar/WdgIf_Bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 1 C source file(s), starting with `WdgIf/src/WdgIf.c`. 

Top-level functions defined in `WdgIf.c` (factual extract, first 1):

- `FUNC`

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

4 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `S-WdgIf_ReleaseNotes.pdf`

- **Source path in repository:** `WdgIf/doc/S-WdgIf_ReleaseNotes.pdf`
- **Format:** `.pdf`
- **Size:** `309 KiB`
- **Expected content:** Release notes (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgIf_SafetyCase.pdf`

- **Source path in repository:** `WdgIf/doc/S-WdgIf_SafetyCase.pdf`
- **Format:** `.pdf`
- **Size:** `291 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgIf_SafetyManual.pdf`

- **Source path in repository:** `WdgIf/doc/S-WdgIf_SafetyManual.pdf`
- **Format:** `.pdf`
- **Size:** `1794 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `S-WdgIf_UserManual.pdf`

- **Source path in repository:** `WdgIf/doc/S-WdgIf_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `2484 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Electronic Control Unit Abstraction](../).
