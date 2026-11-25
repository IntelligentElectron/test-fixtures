# BeagleBone AI, rev A

Single-board computer built on the TI AM5729, by BeagleBoard.org. OrCAD Capture
schematic, with the netlist of the board it was laid out from.

- Upstream: <https://github.com/beagleboard/beaglebone-ai>, commit
  `819b6268c33ed85f1030205eea24a68261d30681`
- License: CC BY 4.0 (`LICENSE`, the upstream `LICENSE`)
- `BeagleBone-AI.dsn` is the upstream `HW/BeagleBone-AI.dsn`, unmodified
  (SHA-256 `2ff3d34d662e795ab62b39b175fb26114d7fdda93fa4f0ba75349f1fc1331f8c`)
- `board-netlist.txt` is derived from the upstream `HW/cds2f_BeagleBone-AI.txt`,
  the Allegro extract of the board `HW/BeagleBone-AI.brd`. It keeps one section
  of that 10 MB file unchanged, the net table
  (`A!NET_NAME!REFDES!PIN_NUMBER!PIN_NAME!PIN_GROUND!PIN_POWER!` and its 3,135
  `S!` rows), and drops the rest (geometry, padstacks, symbols). An empty net
  name is a pin on no net.

## What it exercises

`U4`, the AM5729, is one part drawn as 29 sections on 7 pages. Its package
numbers the sections `-1` to `-29`, and Capture still names the symbols of the
first 25 with letters: the instances are `AM57XA.Normal` to `AM57XY.Normal`,
then `AM57X-26.Normal` to `AM57X-29.Normal`, while the pin maps are stored
under `AM57X-1` to `AM57X-29`. A reader that looks a section's pin map up by
the letter finds none for 25 sections, and each of their pins takes its
position in the symbol as its number: 760 balls collapse onto 367 pin numbers
and most land on two nets.

The record's section index (0 to 28) names the section in every case. Read
that way, the schematic has the board's 3,135 pins on its 716 parts, and 3,124
are on the net the board gives them. The other 11 are `U4` balls on three 1.8 V
rails that the schematic names `1V8_PLLB` (5 balls), `1V8_PHY_PCIE` (3) and
`1V8_PHY_USB` (3), and that the board joins to `1V8_PLLA`, `1V8_PHY_HDMI` and
`1V8_PHY_SATA`.
