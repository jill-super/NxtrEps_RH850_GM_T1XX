---
title: "Nexteer Fixed-Point Library (AR103A_NxtrFixdPt)"
description: "Nexteer Fixed-Point Library: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Nexteer Fixed-Point Library component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `AR103A_NxtrFixdPt_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR103A_NxtrFixdPt_Impl` |  |
| Public headers | `NxtrFixdPt.h` |
| Tooling and integration scripts | `AR103A_NxtrFixdPt_Impl.gpj`, `CreateGHSProject.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `NxtrFixdPt Integration Manual.doc`

- **Source path in repository:** `AR103A_NxtrFixdPt_Impl/doc/NxtrFixdPt Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `146 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Libraries](../).
