---
title: "Nexteer Time Library (AR102A_NxtrTi)"
description: "Nexteer Time Library: purpose, files, interfaces and reference documents."
---

:::tip[Module origin — In-house (custom)]
In-house implementation using Vector MICROSAR generator templates.
:::

## Purpose and responsibility

The Nexteer Time Library component belongs to **Shared Libraries and Global Parameters** in the **Libraries** layer. It is a shared library or a global-parameter package reused across the project.

This logical module combines a **design package** (`*_Design`, functional and design documents) with an **implementation package** (`*_Impl`, source code, AUTOSAR model and configuration).

## Repository locations

| Directory | Role |
|---|---|
| `AR102A_NxtrTi_Design` | Design package |
| `AR102A_NxtrTi_Impl` | Implementation package |

## Key files

| Area | Files |
|---|---|
| `AR102A_NxtrTi_Design` |  |
| Documentation folders | `Design/` |
| `AR102A_NxtrTi_Impl` |  |
| C sources | `CDD_NxtrTi.c`, `CDD_NxtrTi_Init.c` |
| Public headers | `CDD_NxtrTi.h` |
| AUTOSAR model | `AUTOSAR_4-0-3.xsd`, `DataTypes.arxml`, `DataTypes_gen_attr.xml`, `NxtrTi.dcf`, `NxtrTi_attr_def.xml`, `Packages.arxml`, `Packages_gen_attr.xml`, `PortInterfaces.arxml`, `PortInterfaces_gen_attr.xml`, `ProfileSettings.xml` |
| Tooling and integration scripts | `AR102A_NxtrTi_Impl.gpj`, `Component.ecuc.arxml`, `Component_Rte_ecuc.arxml`, `CreateGHSProject.bat`, `NxtrTi.dpa`, `RteGen.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `AR102A_NxtrTi_Impl/autosar/DataTypes.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 2 C source file(s), starting with `AR102A_NxtrTi_Impl/src/CDD_NxtrTi.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `AR102A_NxtrTi_Impl/src/CDD_NxtrTi_Init.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `NxtrTi Integration Manual.doc`

- **Source path in repository:** `AR102A_NxtrTi_Impl/doc/NxtrTi Integration Manual.doc`
- **Format:** `.doc`
- **Size:** `148 KiB`
- **Expected content:** Integration manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Libraries](../).
