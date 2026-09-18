---
title: "Manufacturing Services Support (TL113A_MfgSrvSuprt)"
description: "Manufacturing Services Support: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Manufacturing Services Support component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL113A_MfgSrvSuprt` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL113A_MfgSrvSuprt` |  |
| Tooling and integration scripts | `OdxArxml.py`, `OdxDoc.py`, `OdxGen.py`, `OdxMerge.py`, `OdxTest.py`, `OdxTrim.py`, `RunOdxTest.bat` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Tools and Support](../).
