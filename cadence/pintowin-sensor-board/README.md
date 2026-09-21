# pintowin-sensor-board Cadence fixture

Source: [`4lc0n/PinToWin`](https://github.com/4lc0n/PinToWin) at commit
`2340f6710558ff82d130679e885fdab28af93bb0`, file `schematics/sensor_matrix/SENSOR_BOARD.DSN`.

`SENSOR_BOARD.DSN` is an OrCAD Capture 17.4 schematic of a light-sensor
matrix. It is included because its hierarchy nests three deep: the root places
one matrix block, the matrix places eleven column blocks, and each column places
eight sensor-unit blocks, so one drawn sensor unit stands for 88 components. The
design is annotated by occurrence: the drawings keep `R?` and `col?`, and the
Hierarchy stream carries every occurrence's own reference.

The upstream repository ships an Allegro netlist export beside the schematic.
Its parts and pins agree with this file, and its block-local nets are named
`<net>_<outer>_<middle>_<inner>`, which is what the nested suffix rule was
verified against. The export is not included here: its block instance names
come from an earlier annotation pass than the one this file carries, so an
exact name comparison against it is not meaningful.

The upstream `LICENSE` is MIT. The DSN SHA-256 is
`7c058a15629e918b1ee8887eac905c873032da6edc2e121a874436ba0f075368`.
