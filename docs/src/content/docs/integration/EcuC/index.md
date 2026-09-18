---
title: "Electronic Control Unit Configuration (EcuC)"
description: "Electronic Control Unit Configuration: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided, customised]
Vector MICROSAR module with project-specific configuration and custom code.
:::

## Purpose and responsibility

The Electronic Control Unit Configuration component belongs to **Top-Level Integration** in the **System Integration** layer. It integrates the configured software stack for the target controller and vehicle platform.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `EcuC` | Package directory |

## Key files

| Area | Files |
|---|---|
| `EcuC` |  |
| AUTOSAR model | `EcuC_bswmd.arxml`, `EcuC_preo_Rh850_GreenHills.arxml` |
| Tooling and integration scripts | `Integrate.bat` |
| Documentation folders | `doc/` |

## Public interface and usage

The component interface is modelled in AUTOSAR XML (2 file(s), e.g. `EcuC/autosar/EcuC_bswmd.arxml`); the Runtime Environment generates the callable interface from this model. 
This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- AUTOSAR model files (`autosar/*.arxml`, DaVinci `*.dcf`) configure this component; regenerate rather than hand-editing generated output.
- Ships a per-module integration script (`tools/Integrate.bat`) consumed by the top-level integration project.
- References the Vector MICROSAR / DaVinci tool chain (see Tools and Support).
- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `EcuC Baseline Naming Help.txt`

- **Source path in repository:** `EcuC/doc/EcuC Baseline Naming Help.txt`
- **Format:** `.txt`
- **Size:** `0 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
Since the EcuC component doesn't have source or header files, the baseline name is based on the version embedded within the generator .jar file.  This is extracted from: EcuC_AsrEcuC.jar->ChangeHistor->ChangeHistory.txt file.
```

Back to [System Integration](../).
