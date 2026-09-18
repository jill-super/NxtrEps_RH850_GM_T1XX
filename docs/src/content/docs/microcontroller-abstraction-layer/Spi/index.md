---
title: "Serial Peripheral Interface (Spi)"
description: "Serial Peripheral Interface: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Serial Peripheral Interface component belongs to **Microcontroller Drivers** in the **Microcontroller Abstraction Layer** layer. It is a microcontroller-abstraction driver for one on-chip peripheral.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Spi` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Spi` |  |
| C sources | `Spi.c`, `Spi_Driver.c`, `Spi_Irq.c`, `Spi_Ram.c`, `Spi_Scheduler.c`, `Spi_Version.c` |
| Public headers | `Spi.h`, `Spi_Driver.h`, `Spi_Irq.h`, `Spi_LTTypes.h`, `Spi_PBTypes.h`, `Spi_Ram.h`, `Spi_Scheduler.h`, `Spi_Types.h`, `Spi_Version.h` |
| AUTOSAR model | `R403_SPI_P1M_04_05_12_13_20_21.arxml`, `R403_SPI_P1M_10_11_14_15_18_19_22_23.arxml`, `Spi_bswmd_rec.arxml` |
| Generator output | `P1M.trxml`, `P1x_translation.h`, `R403_SPI_P1x_BSWMDT.arxml`, `Spi_X1x.cfgxml`, `Spi_X1x.exe`, `dr7f701304_0.h`, `dr7f701305_0.h`, `dr7f701310_0.h`, `dr7f701311_0.h`, `dr7f701312_0.h`, `dr7f701313_0.h`, `dr7f701314_0.h` (+7 more) |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Integrate.bat`, `Spi.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (3 file(s), e.g. `Spi/autosar/R403_SPI_P1M_04_05_12_13_20_21.arxml`); the Runtime Environment generates the callable interface from this model. 
Implementation lives in 6 C source file(s), starting with `Spi/src/Spi.c`. 

Top-level functions defined in `Spi.c` (factual extract, first 14):

- `FUNC`
- `Spi_DeInit`
- `Spi_WriteIB`
- `Spi_AsyncTransmit`
- `Spi_ReadIB`
- `Spi_SetupEB`
- `Spi_GetStatus`
- `Spi_GetJobResult`
- `Spi_GetSequenceResult`
- `Spi_SyncTransmit`
- `Spi_GetHWUnitStatus`
- `Spi_Cancel`
- `Spi_SetAsyncMode`
- `Spi_MainFunction_Handling`

Additional implementation units: `Spi/src/Spi_Driver.c`, `Spi/src/Spi_Irq.c`, `Spi/src/Spi_Ram.c`, `Spi/src/Spi_Scheduler.c`, `Spi/src/Spi_Version.c`.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

2 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `AUTOSAR_SPI_Component_UserManual.pdf`

- **Source path in repository:** `Spi/doc/AUTOSAR_SPI_Component_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `1121 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `AUTOSAR_SPI_Tool_UserManual.pdf`

- **Source path in repository:** `Spi/doc/AUTOSAR_SPI_Tool_UserManual.pdf`
- **Format:** `.pdf`
- **Size:** `364 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Microcontroller Abstraction Layer](../).
