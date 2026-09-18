---
title: "Flash (Fls)"
description: "Flash: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Flash component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Fls` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Fls` |  |
| C sources | `Fls.c`, `Fls_Internal.c`, `Fls_Irq.c`, `Fls_Ram.c`, `Fls_Version.c`, `fdl_descriptor.c`, `r_fdl_hw_access.c`, `r_fdl_user_if.c`, `r_fdl_user_if_init.c` |
| Public headers | `Fls.h`, `Fls_Debug.h`, `Fls_Internal.h`, `Fls_Irq.h`, `Fls_PBTypes.h`, `Fls_Ram.h`, `Fls_Types.h`, `Fls_Version.h`, `fdl_cfg.h`, `r_fdl.h`, `r_fdl_env.h`, `r_fdl_global.h` (+3 more) |
| AUTOSAR model | `Fls_bswmd_rec.arxml`, `R403_FLS_P1M_04_05.arxml`, `R403_FLS_P1M_10_to_15.arxml`, `R403_FLS_P1M_18_to_23.arxml` |
| Generator output | `Fls_X1x.cfgxml`, `Fls_X1x.exe`, `P1M.trxml`, `P1x_translation.h`, `R403_FLS_P1x_BSWMDT.arxml`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h`, `dr7f701314_0.h` (+7 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Fls.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (4 file(s), e.g. `Fls/autosar/Fls_bswmd_rec.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 9 C source file(s), starting with `Fls/src/Fls.c`. 

Top-level functions defined in `Fls.c` (factual extract, first 14):

- `Fls_Init`
- `Fls_Erase`
- `Fls_Write`
- `Fls_Cancel`
- `Fls_GetStatus`
- `Fls_GetJobResult`
- `Fls_MainFunction`
- `Fls_Read`
- `Fls_Compare`
- `Fls_SetMode`
- `Fls_ReadImmediate`
- `Fls_BlankCheck`
- `Fls_Suspend`
- `Fls_Resume`

Additional implementation units: `Fls/src/Fls_Internal.c`, `Fls/src/Fls_Irq.c`, `Fls/src/Fls_Ram.c`, `Fls/src/Fls_Version.c`, `Fls/src/fdl_descriptor.c` (and 3 more).

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

2 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AUTOSAR_FLS_Component_UserManual.pdf`

- **Source path in repository:** `Fls/doc/AUTOSAR_FLS_Component_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `890 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AUTOSAR_FLS_Tool_UserManual.pdf`

- **Source path in repository:** `Fls/doc/AUTOSAR_FLS_Tool_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `508 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
