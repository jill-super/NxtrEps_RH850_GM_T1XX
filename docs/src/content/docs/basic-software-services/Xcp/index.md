---
title: "Universal Measurement and Calibration Protocol (Xcp)"
description: "Universal Measurement and Calibration Protocol: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Third-party MICROSAR module supplied by Vector.
:::

## Purpose and responsibility

The Universal Measurement and Calibration Protocol component belongs to **System Services** in the **Basic Software Services** layer. It is an AUTOSAR Basic Software service module managing modes, diagnostics, memory or calibration access.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `Xcp` | Package directory |

## Key files

| Area | Files |
|---|---|
| `Xcp` |  |
| C sources | `XcpProf.c`, `xcp_can.c` |
| Public headers | `XcpProf.h`, `xcp_can.h` |
| Tooling and integration scripts | `CreateGHSProject.bat`, `Xcp.gpj` |
| Documentation folders | `doc/` |

## Public interface and usage

Implementation lives in 2 C source file(s), starting with `Xcp/src/XcpProf.c`. 
No top-level function definitions were extracted from the main source file; consult the source and the integration manual below.

Additional implementation units: `Xcp/src/xcp_can.c`.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

3 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `TechnicalReference_XCP_Protocol_Layer.pdf`

- **Source path in repository:** `Xcp/doc/TechnicalReference_XCP_Protocol_Layer.pdf`
- **Format:** `.pdf`
- **Size:** `922 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `TechnicalReference_XCP_on_CAN.pdf`

- **Source path in repository:** `Xcp/doc/TechnicalReference_XCP_on_CAN.pdf`
- **Format:** `.pdf`
- **Size:** `349 KiB`
- **Expected content:** Technical reference manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

### `UserManual_XCP.pdf`

- **Source path in repository:** `Xcp/doc/UserManual_XCP.pdf`
- **Format:** `.pdf`
- **Size:** `578 KiB`
- **Expected content:** User manual (inferred from the file name — assumption).

> **Note:** this legacy Word/PDF binary cannot be converted automatically with the tooling available here. The summary above is based on the file name and module context. To read the full text, open the source file at the path given.

Back to [Basic Software Services](../).
