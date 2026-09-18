---
title: "AUTOSAR Support (AR200A_ArSuprt)"
description: "AUTOSAR Support: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The AUTOSAR Support component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `AR200A_ArSuprt_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR200A_ArSuprt_Impl` |  |
| Tooling and integration scripts | `Sup_ASR_ASR4.0.3.gpj` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Tools and Support](../).
