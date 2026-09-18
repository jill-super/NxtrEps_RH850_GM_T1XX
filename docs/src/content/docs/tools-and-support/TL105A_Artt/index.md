---
title: "AUTOSAR Template Tool (TL105A_Artt)"
description: "AUTOSAR Template Tool: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Host-side tooling supplied by Vector.
:::

## Purpose and responsibility

The AUTOSAR Template Tool component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL105A_Artt` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL105A_Artt` |  |
| Tooling and integration scripts | `AddSswcCertificate.bat`, `AutosarDirectiveProcessor.dll`, `Microsoft.VisualStudio.TextTemplating.dll`, `ReleaseNotes_Artt_Generator.pdf`, `SswcT4EngineHost.dll`, `artt.chm`, `artt.chw`, `artt.exe`, `artt.exe.config` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ReleaseNotes_Artt_Generator.pdf`

- **Source path in repository:** `TL105A_Artt/tools/ReleaseNotes_Artt_Generator.pdf`
- **Format:** `.pdf`
- **Size:** `44 KiB`
- **Expected content:** Release notes (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Tools and Support](../).
