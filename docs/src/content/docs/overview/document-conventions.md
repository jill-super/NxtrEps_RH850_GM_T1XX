---
title: How to Read This Documentation
description: Conventions used across module pages, long names and converted documents.
---

## Long names first

Abbreviations are always expanded on first use: the **long name** is used in
titles and prose, with the repository short name in parentheses, e.g.
“Assist (SF001A Assi Implementation)”. A full
[glossary](/overview/glossary/) maps every short token to its long name.

## Module pages

Each module page contains:

1. An **origin badge** — Vector-provided or in-house (see
   [Vector versus in-house](/overview/vector-vs-inhouse/)).
2. **Purpose and responsibility** derived from the component name and folder role.
3. **Repository locations** — the one or two directories (`*_Design`,
   `*_Impl`) that form the logical module.
4. **Key files** — sources, headers, AUTOSAR model, generator output, tooling.
5. **Public interface and usage** — top-level functions found in the sources
   and how the component is reached (Runtime Environment ports or direct calls).
6. **Dependencies and configuration** — generators and configuration sources.
7. **Reference documents** — converted content of the Word/PDF files shipped
   with the module.

## Converted Word and PDF documents

- Modern Word (`*.docx`) files are converted to Markdown with headings,
  lists and tables preserved as far as the conversion allows.
- Legacy Word (`*.doc`) and PDF (`*.pdf`) binaries cannot be converted with
  the tooling available here; each gets a structured summary card stating the
  source path, format, size and expected content. Open the original file in
  the repository to read the full text.
- Statements derived from file names rather than file contents are marked as
  assumptions.
