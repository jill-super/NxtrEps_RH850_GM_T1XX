---
title: "General Motors 001 A Checkpoint (GM_001A_ChkPt)"
description: "General Motors 001 A Checkpoint: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The General Motors 001 A Checkpoint component belongs to **Platform Services** in the **Application Software** layer. It provides a platform-level service (communication machine, checkpoints, part numbers, diagnostics) to the application.

This is an **implementation package**: it holds source code, the AUTOSAR model, configuration and integration scripts.

## Repository locations

| Directory | Role |
|---|---|
| `GM_001A_ChkPt_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `GM_001A_ChkPt_Impl` |  |
| C sources | `CDD_ChkPtAppl10.c`, `CDD_ChkPtAppl6.c`, `CDD_ChkPt_Bsw.c` |
| Public headers | `CDD_ChkPt_Bsw.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `ChkPt.dcf`, `ChkPt_attr_def.xml`, `ChkPt_bswmd.arxml`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `ChkPt.dpa`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `GM_001A_ChkPt_Impl.gpj`, `Integrate.bat`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `GM_001A_ChkPt_Impl/autosar/ChkPt_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 3 C source file(s), starting with `GM_001A_ChkPt_Impl/src/CDD_ChkPtAppl10.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `GM_001A_ChkPt_Impl/src/CDD_ChkPtAppl6.c`, `GM_001A_ChkPt_Impl/src/CDD_ChkPt_Bsw.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `ChkPt Integration Manual.doc`

- **Source path in repository:** `GM_001A_ChkPt_Impl/doc/ChkPt Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `159 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Application Software](../).
