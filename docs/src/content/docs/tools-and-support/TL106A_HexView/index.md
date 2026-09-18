---
title: "Hex Viewer (TL106A_HexView)"
description: "Hex Viewer: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Source headers reference Vector; no in-house authorship found.
:::

## Purpose and responsibility

The Hex Viewer component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL106A_HexView` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL106A_HexView` |  |
| Tooling and integration scripts | `Disclaimstatic.dll`, `InfoWindow.dll`, `PBuild.dll`, `ReferenceManual_HexView.pdf`, `disclaimer.txt`, `expdatproc.dll`, `gl_inst.dll`, `hexview.exe`, `license.liz` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ReferenceManual_HexView.pdf`

- **Source path in repository:** `TL106A_HexView/tools/ReferenceManual_HexView.pdf`
- **Format:** `.pdf`
- **Size:** `2374 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Tools and Support](../).
