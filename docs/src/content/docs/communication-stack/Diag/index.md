---
title: "Diagnostics (Diag)"
description: "Diagnostics: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Diagnostics component belongs to **Protocols and Interaction** in the **Communication Stack** layer. It implements a communication protocol, the interaction layer or diagnostic transport.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Diag` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Diag` |  |
| C sources | `ggda.c` |
| Public headers | `ggda.h` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Diag.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `Diag/src/ggda.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_GGDA.pdf`

- **Source path in repository:** `Diag/doc/TechnicalReference_GGDA.pdf`
- **Format:** `.pdf`
- **Size:** `485 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Communication Stack](../).
