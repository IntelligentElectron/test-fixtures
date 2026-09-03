# KiCad multichannel mixer

Source: KiCad's `demos/multichannel` at tag `9.0.0`, commit
`286b0611feca00727bf70bfa184ec2c28a745dc3`:
https://github.com/KiCad/kicad-source-mirror/tree/286b0611feca00727bf70bfa184ec2c28a745dc3/demos/multichannel

Author: Tomasz Wlostowski and the KiCad contributors.
License: CC BY-SA 4.0. The upstream `LICENSE.README` explicitly covers
`demos/*`; both that notice and the license text are retained here.

The project and both schematic files are unmodified upstream files. PCB files,
footprints, and other assets are omitted. The `.net` is generated from these
schematics using KiCad 10.0.5, with the export machine's absolute source path
removed:

```sh
kicad-cli sch export netlist --format kicadsexpr \
  -o multichannel_mixer.net multichannel_mixer.kicad_sch
```

This design records both `Part Number` and `Manufacturer Part Number` on the
same components. For example, C1 has the design identifier
`CTEB_2.2UF_35V_10%_254-500X840`, manufacturer number `T350C225K035AT`, and
manufacturer `KEMET`. Reading the first matching field used to report the
design identifier as the manufacturer's number. Repeated channel sheets also
exercise preservation of these fields across flattened instances.
