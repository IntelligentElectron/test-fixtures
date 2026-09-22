# OpenCellular OC-CONNECT1 SDR, rev C

Software-defined radio board of the OpenCellular access platform, by the Telecom
Infra Project. OrCAD Capture schematic with 34 pages in one flat view.

- Upstream: <https://github.com/Telecominfraproject/OpenCellular>, path
  `electronics/radio/SDR/schematics/DSN/OC_CONNECT1_SDR_REV_C_V1P1.DSN`,
  commit `0d5d7b005327e4378bd5c7fd44d7b8dc5ab796f6`
- License: CC BY 4.0 (`LICENSE`, the upstream `LICENSE-HARDWARE`)
- `OC_CONNECT1_SDR_REV_C_BOM_ASSEMBLY_V1.5.xlsx` is the upstream assembly BOM,
  the reference for the components the parser reports

## What it exercises

The design sets per-page reference ranges (seven pages, named `B210_1` to
`B210_7` when the ranges were set, numbering their parts 100 to 199 through 700
to 799) and was re-annotated afterwards. Capture records the ranges in the
top-level scope's property bag of the `Hierarchy` stream, so the preamble before
the occurrence count carries trailing data, and the reference designators
annotated on the occurrences differ from the inline copies on the page records.

A parser that reads the Hierarchy stream reports every reference on the BOM. A
parser that skips a fixed 8 bytes there fails to read the stream, falls back to
the inline references, and reports stale designators such as `R10642` in place
of `R100`.
