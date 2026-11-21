# clay-r6 Cadence fixture

Source: [`ah-cog/Clay`](https://github.com/ah-cog/Clay) at commit
`31a84237d09eb93affb9b2587ff1d5b9a2b8c6a6`, directory `Circuit/R6`.

Clay R6 is an OrCAD Capture 16.6 design for a Kinetis K64 board. It is included
because the Allegro netlister renames its long net names. The microcontroller
block names each net after every function of the pin it serves, such as
`PTA2/JTAG_TDO/TRACE_SWO/EZP_D0/UART0_TX/FTM0_CH7`. Allegro net names have a
31-character limit, so the export writes that net as
`PTA2/JTAG_TDO/TRACE_SWO/EZP_D0/` (Capture warning `ORCAP-36005`, "Net is
renamed"). The schematic path line in the export keeps the full name.

Files, at their upstream paths below `Circuit/R6` except where noted:

- `MK64FN1M0VLL12/MK64FN1M0VLL12.DSN` and `.opj`: the microcontroller block,
  a standalone Capture design. It carries 63 net names longer than 31
  characters.
- `allegro/pstxnet.dat`, `pstxprt.dat`, `pstchip.dat`: the Allegro export of
  the whole board, written by PSTWRITER 16.6 on 2016-02-08. 27 of its nets are
  truncated names of nets in the block; the export never uses the full name.
- `top/CLAYR6.DSN` (upstream `CLAYR6.DSN`): the board's top level. It draws
  one page and places its blocks from separate `.DSN` files, which are not
  included, so the parser reads 16 of the export's 133 parts. It is included
  for its parts with shorted package pins: the `GPIO_3X3_100` connectors
  `J3`-`J6` mark pins 5-8 (`VDD1`, `VDD2`, `GND2`, `GND1`) Pin Ignore, and the
  library part's `PACK_SHORT` property, `(VDD,VDD1,VDD2)(GND,GND1,GND2)`, ties
  them to `VDD` and `GND`. The export puts all 16 of those pins on `VCC` and
  `GND`, although none is wired. Top-level parts keep the board's reference
  designators.

The block was annotated on its own, so its reference designators differ from
the board's: the block's `J1` and `U1` are the board's `J7` and `U5`. Pin
numbers agree.

Both `.DSN` files sit outside the export's directory, so discovery pairs
neither with it.

The upstream `LICENSE` is MIT. SHA-256:

- `MK64FN1M0VLL12.DSN`: `d940cab68d005712a27a80d906ac0c30e123fc440e3b143780be4b4afcf058c1`
- `CLAYR6.DSN`: `594f2fd47827dae0b510fe6c4adad264d1791a0e48853bab5463ddab8b4dd77b`
- `pstxnet.dat`: `be92b0a89f1d60fa211b118f68eeaafcc56f9ba88ceb192778f5e7dd0b8cfdb7`
