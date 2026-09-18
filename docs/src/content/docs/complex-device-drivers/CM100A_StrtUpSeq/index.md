---
title: "Startup Sequence (CM100A_StrtUpSeq)"
description: "Startup Sequence: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Startup Sequence component belongs to **System, Memory and Startup** in the **Complex Device Drivers** layer. It configures or supervises microcontroller cores, guards, clocks, flash and RAM, or the startup sequence.

This is a **design package**: it holds the functional/design documents; the implementation lives in the matching implementation package.

## Repository locations

| Directory | Role |
|---|---|
| `CM100A_StrtUpSeq_Design` | Design package |

## Key files

| Area | Files |
|---|---|
| `CM100A_StrtUpSeq_Design` |  |
| Documentation folders | `Doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Complex Device Drivers](../).
