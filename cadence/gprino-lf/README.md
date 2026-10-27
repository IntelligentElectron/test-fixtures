# gprino-lf Cadence fixture

Source: [`miricip/GPRino`](https://github.com/miricip/GPRino) at commit
`ec8d739499d62d2da4a08aa502773d8ff3d182b0`, file
`Hardware/OrCAD + GERBER/LF(GPR_LF)/GPR_LF.DSN`.

`GPR_LF.DSN` is the low-frequency board of GPRino, a ground-penetrating radar
built around an Arduino Mega 2560. It is included because OrCAD Capture saved
it in an older format: its root `Library` stream reads version 2.0, where every
other Cadence fixture here reads 3.2 or 3.3. Its page records use the older
encoding, which opens `0A 00 00` and then the page name, with no 4-byte prefix
length. universal-netlist reads Library version 3 and later only, and refuses
this design with a message that names version 2.0 (universal-netlist issue
#246).

The design has one page, `PAGE1`, and two `Packages` streams, so a `Packages`
stream does not by itself mark a design as readable.

The upstream `LICENSE` is MIT, copyright 2024 Mirel Paun. The DSN is
byte-identical to upstream (git blob `5ed0beb5978ffdf7d89582c86298ccf1478b8386`).
Its SHA-256 is
`c74a0377a48dad82e0643ca8a117f4f98cfb3215a01943eaf0ab40439929d0d5`.
