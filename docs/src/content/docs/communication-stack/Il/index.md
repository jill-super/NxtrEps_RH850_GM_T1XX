---
title: "Interaction Layer (Il)"
description: "Interaction Layer: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Interaction Layer component belongs to **Protocols and Interaction** in the **Communication Stack** layer. It implements a communication protocol, the interaction layer or diagnostic transport.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Il` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Il` |  |
| C sources | `il.c` |
| Public headers | `il_def.h` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Il.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `Il/src/il.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_GENy_InteractionLayer.pdf`

- **Source path in repository:** `Il/doc/TechnicalReference_GENy_InteractionLayer.pdf`
- **Format:** `.pdf`
- **Size:** `2202 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_InteractionLayer_GM.pdf`

- **Source path in repository:** `Il/doc/TechnicalReference_InteractionLayer_GM.pdf`
- **Format:** `.pdf`
- **Size:** `1095 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `UserManual_GENy_InteractionLayer.pdf`

- **Source path in repository:** `Il/doc/UserManual_GENy_InteractionLayer.pdf`
- **Format:** `.pdf`
- **Size:** `341 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Communication Stack](../).
