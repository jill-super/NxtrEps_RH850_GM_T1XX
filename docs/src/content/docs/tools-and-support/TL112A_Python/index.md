---
title: "Python Tooling (TL112A_Python)"
description: "Python Tooling: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house developed component.
:::

## Purpose and responsibility

The Python Tooling component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL112A_Python` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL112A_Python` |  |
| Tooling and integration scripts | `Microsoft.VC90.CRT.manifest`, `msvcm90.dll`, `msvcp90.dll`, `msvcr90.dll`, `python.exe`, `python27.dll`, `pythoncom27.dll`, `pythoncomloader27.dll`, `pythonw.exe`, `pywintypes27.dll`, `qt.conf`, `w9xpopen.exe` |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Depends on shared libraries and global parameters where referenced; see Libraries.

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Tools and Support](../).
