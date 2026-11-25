# Digital convertor

A small OrCAD Capture schematic (15 parts, one page) with the Allegro netlist
Capture exported from it.

- Upstream: <https://github.com/wodykr/orcad_project>, path `Digital_Convertor/`,
  commit `2a4e37d684b965bd60ac2a944f31f6e3c19bb12c`
- License: LGPL-3.0 (`LICENSE`, the upstream `LICENSE`)
- `DIGITAL_CONVERTOR.DSN` is unmodified
  (SHA-256 `ec90050d82b830e59a6c197937f2e6c6b0fc8f97c054797a8d673ef973453179`)
- `allegro/pstxnet.dat,3`, `pstchip.dat,3` and `pstxprt.dat,3` are Capture's
  export of the design (PSTWRITER 17.2, 2021-02-18), under the names upstream
  ships them: Allegro keeps earlier exports with a `,N` suffix, and `,3` is the
  latest in the repository. They are a reference to compare a reader against,
  kept under those names so tooling that looks for `pstxnet.dat` does not take
  the folder for a current export.

## What it exercises

The design's Cache holds two parts named `R`, from two libraries. The first is
from `LIBRARY\DISCRETE.OLB`, with pin map `1, 2`. The second is from
`LIBRARY\PSPICE\ANALOG.OLB`, with pin map `2, 1`, and it is the one all nine
resistors on the page were placed from. A placed part names its library, and
Capture's export names it on every node (`INS350@ANALOG.R.NORMAL`). A reader
that takes the first part called `R` swaps pins 1 and 2 of every resistor, and
12 of the export's 14 nets come out with different pins.

`U1` (7414) has its supply on pins 14 and 7. Capture exports those through
`pstchip.dat` (`POWER_PINS='(VCC:14)'` and `'(GND:7)'`) and leaves them out of
the `pstxnet.dat` node lists, so a reader that puts `U1.14` on `VCC` and `U1.7`
on `GND` agrees with the export although the node lists do not show them.
