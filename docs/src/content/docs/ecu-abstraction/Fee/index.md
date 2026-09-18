---
title: "Flash EEPROM Emulation (Fee)"
description: "Flash EEPROM Emulation: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Flash EEPROM Emulation component belongs to **Hardware Abstraction Interfaces** in the **Electronic Control Unit Abstraction** layer. It abstracts the microcontroller hardware behind an AUTOSAR interface.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Fee` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Fee` |  |
| C sources | `Fee.c`, `Fee_ChunkInfo.c`, `Fee_Partition.c`, `Fee_Processing.c`, `Fee_Sector.c` |
| Public headers | `Fee.h`, `Fee_Cbk.h`, `Fee_ChunkInfo.h`, `Fee_ChunkInfoDefs.h`, `Fee_InitEx.h`, `Fee_Int.h`, `Fee_IntBase.h`, `Fee_JobParams.h`, `Fee_Partition.h`, `Fee_PartitionDefs.h`, `Fee_Sector.h`, `Fee_SectorDefs.h` (+1 more) |
| AUTOSAR model | `Fee_bswmd.arxml`, `Fee_preo.arxml` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Fee.gpj`, `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `Fee/autosar/Fee_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 5 C source file(s), starting with `Fee/src/Fee.c`. 

Top-level functions defined in `Fee.c` (factual extract, first 5):

- `FEE_INLINE_FUNC`
- `Fee_InitEx`
- `Fee_Read`
- `Fee_Write`
- `FEE_LOCAL_FUNC`

Additional implementation units: `Fee/src/Fee_ChunkInfo.c`, `Fee/src/Fee_Partition.c`, `Fee/src/Fee_Processing.c`, `Fee/src/Fee_Sector.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

2 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AN-ISC-8-1161_FEE_alignments_to_reduce_data_loss_through_ECC.pdf`

- **Source path in repository:** `Fee/doc/AN-ISC-8-1161_FEE_alignments_to_reduce_data_loss_through_ECC.pdf`
- **Format:** `.pdf`
- **Size:** `1017 KiB`
- **Expected content:** Application note (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_Fee.pdf`

- **Source path in repository:** `Fee/doc/TechnicalReference_Fee.pdf`
- **Format:** `.pdf`
- **Size:** `1165 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Electronic Control Unit Abstraction](../).
