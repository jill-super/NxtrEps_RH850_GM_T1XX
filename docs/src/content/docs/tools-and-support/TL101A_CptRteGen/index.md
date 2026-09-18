---
title: "Component Runtime Environment Generator (TL101A_CptRteGen)"
description: "Component Runtime Environment Generator: purpose, files, interfaces and reference documents."
---

:::note[Module origin — Vector-provided]
Host-side tooling supplied by Vector.
:::

## Purpose and responsibility

The Component Runtime Environment Generator component belongs to **Host Tools and Support Packages** in the **Tools and Support** layer. It is a host-side tool, generator or support package; it is not flashed onto the controller.

This is a single-directory package holding configuration, tooling or support files.

## Repository locations

| Directory | Role |
|---|---|
| `TL101A_CptRteGen` | Package directory |

## Key files

| Area | Files |
|---|---|
| `TL101A_CptRteGen` |  |
| Documentation folders | `doc/` |

## Public interface and usage

This package ships no C sources of its own; it provides configuration, tooling or documentation consumed by other modules.

## Dependencies and configuration

- Third-party delivery: keep the supplied files pristine and carry project changes as configuration deltas.

## Reference documents

1 reference file(s) ship with this module. legacy Word and PDF files are summarised with their repository path so the original can be opened.

### `CptRteGenNotes.txt`

- **Source path in repository:** `TL101A_CptRteGen/doc/CptRteGenNotes.txt`
- **Format:** `.txt`
- **Size:** `1 KiB`
- **Expected content:** Reference document (inferred from the file name — assumption).

**Content (plain text, first 80 lines):**

```text
This component is intended to be used for generation of contract phase headers and c implementation templates of core software components.

The RTE generator license used for this is based of the one delivered for a GM project (see SIPLicense.lic in the RteGen4.3.0 directory).

The limitation due to this is that all components will get generated with this SIP identifier and the GM OEM name as part of the comments in the generated files.

Discussions with Vector are currently on-going to see if a license can be generated that will not contain OEM identifiers, but is currently not available. 
```

Back to [Tools and Support](../).
