---
title: "Nexteer Startup (AR400A_NxtrStrtUp)"
description: "Nexteer Startup: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Nexteer Startup component belongs to **Unclassified Support Content** in the **Tools and Support** layer. It is a support package; see the repository directory for details.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `AR400A_NxtrStrtUp_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR400A_NxtrStrtUp_Impl` |  |
| C sources | `NxtrStrtUp.c`, `NxtrStrtUpLo.850` |
| Public headers | `NxtrStrtUp.h` |
| Tooling and integration scripts | `AR400A_NxtrStrtUp_Impl.gpj`, `CreateGHSProject.bat` |

## Public interface and usage

Implementation lives in 1 C source file(s), starting with `AR400A_NxtrStrtUp_Impl/src/NxtrStrtUp.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Tools and Support](../).
