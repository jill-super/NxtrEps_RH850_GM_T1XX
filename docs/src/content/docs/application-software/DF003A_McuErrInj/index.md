---
title: "Microcontroller Error Injection (DF003A_McuErrInj)"
description: "Microcontroller Error Injection: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Microcontroller Error Injection component belongs to **Diagnostic and Fault-Injection Functions** in the **Application Software** layer. It supports diagnostics, fault injection or test sweeps used during development and verification.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `DF003A_McuErrInj_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `DF003A_McuErrInj_Impl` |  |
| Public headers | `McuErrInj.h` |
| Tooling and integration scripts | `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `CreatePolyspaceProject.bat`, `CreateQACProject.bat`, `DF003A_McuErrInj_Impl.gpj`, `McuErrInj.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

No Word, PDF or documentation text files were found in this module.

Back to [Application Software](../).
