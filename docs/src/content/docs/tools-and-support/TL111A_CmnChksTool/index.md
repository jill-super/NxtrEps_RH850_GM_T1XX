---
title: "Common Checks Tool (TL111A_CmnChksTool)"
description: "Common Checks Tool: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Common Checks Tool component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL111A_CmnChksTool` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL111A_CmnChksTool` |  |
| Tooling and integration scripts | `BinaryCOFFMC.dll`, `BinaryCOFFTI.dll`, `BinaryELFTI.dll`, `BinaryHex.dll`, `BinaryInterface.dll`, `BinarySTI.dll`, `CCT.exe`, `CCT_Lib.dll`, `CCT_Lib.tlb`, `InstallerHelp.exe`, `nowECC.exe` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Tools and Support](../).
