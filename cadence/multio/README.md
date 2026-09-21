# multio Cadence fixture

Source: [`fenlogic/multio`](https://github.com/fenlogic/multio) at commit
`eee280535c9ab5b1b0f4a4cb277fa372a7bc5eb8`.

`MULTIO.DSN` is an OrCAD 16.4 schematic for a 128-channel I2C I/O board. It is
included because some Port records use the PlacedInstance (`13`) prefix type.
The strict Cadence parser fails at prefix offset 19,710; accepting both the Port
and PlacedInstance prefix types parses the design as 65 components and 147 nets.

The upstream `README` applies GPLv3 to all files. The included upstream
`LICENCE` contains the LGPLv3 text; both permit redistribution of this fixture.
The DSN SHA-256 is
`d225e342ef5933917828c7d50a6fa5133991b9f657f5938176911c48de1da402`.
