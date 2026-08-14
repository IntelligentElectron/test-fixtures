# License Attribution

This repository contains EDA design files from third-party open-source
hardware projects, collected as test fixtures for
[universal-netlist](https://github.com/IntelligentElectron/universal-netlist)
and [pcb-lens](https://github.com/IntelligentElectron/pcb-lens).

Each fixture retains its original license. See the individual license files
within each directory where available.

## Altium Fixtures

| Fixture | Upstream | License | Copyright |
|---------|----------|---------|-----------|
| Altium-STM32-PCB | [akhilaprabodha/Altium-STM32-PCB](https://github.com/akhilaprabodha/Altium-STM32-PCB) | No license file | akhilaprabodha |
| LimeSDR-USB | [myriadrf/LimeSDR-USB](https://github.com/myriadrf/LimeSDR-USB) | Apache 2.0 | Lime Microsystems Ltd |
| aberrant-sound-module | [aberranthacker/aberrant_sound_module](https://github.com/aberranthacker/aberrant_sound_module) | No license file | aberranthacker, zloiMOZG |
| nRF52840-Development-Kit | [NordicSemiconductor/nrf52840-development-kit](https://www.nordicsemi.com/) | Nordic BSD | Nordic Semiconductor ASA |
| HELIOS-R | [pulp-bio/HELIOS-R](https://github.com/pulp-bio/HELIOS-R) | Solderpad Hardware Licence v0.51 (Apache-2.0 option) | ETH Zurich |
| cube-sat-eps | [Dominik-Workshop/cube-sat-eps](https://github.com/Dominik-Workshop/cube-sat-eps) | MIT | Dominik-Workshop |
| heron-hardware | [PA-OST-2023/heron-hardware](https://github.com/PA-OST-2023/heron-hardware) | MIT | PA-OST-2023 |
| qfsae-harness | [qfsae/pcb](https://github.com/qfsae/pcb) | MIT | Queen's Formula SAE |
| mixr-power | [MIXR-FYDP/mixr-hardware](https://github.com/MIXR-FYDP/mixr-hardware) | MIT | Taiping Li |
| misko3 | [mjankovec/MiSKo3](https://github.com/mjankovec/MiSKo3) | GPL-3.0 | Matic Jankovec |
| solarcar-bms | [zbrozek/solarcar-batterypack](https://github.com/zbrozek/solarcar-batterypack) | MIT | Kevin Brozek |

## Cadence Fixtures

| Fixture | Upstream | License | Copyright |
|---------|----------|---------|-----------|
| BeagleBone-Black | [beagleboard/beaglebone-black](https://github.com/beagleboard/beaglebone-black) | No license file (OSHWA US000236) | BeagleBoard.org Foundation |
| BeagleBone-Black-barebone | Derived from BeagleBone-Black | No license file | BeagleBoard.org Foundation |
| BeagleBone-Black-copy | Derived from BeagleBone-Black | No license file | BeagleBoard.org Foundation |
| BeagleBoard-xM | [beagleboard/beagleboard-xm](https://github.com/beagleboard/beagleboard-xm) | No license file | BeagleBoard.org Foundation |
| CutiePi | [cutiepi-io/cutiepi-board](https://github.com/cutiepi-io/cutiepi-board) | BSD 3-Clause | Zhang "Iron Pillar" Hogan, Raspberry Pi (Trading) Ltd |
| LAUNCHXL-CC1310 | [peterkappelt/kHome](https://github.com/peterkappelt/kHome) | No license file | Peter Kappelt |
| OSHW-Jetson-Series | [Seeed-Studio/OSHW-Jetson-Series](https://github.com/Seeed-Studio/OSHW-Jetson-Series) | Apache 2.0 | Seeed Studio |

## KiCad Fixtures

A deliberately diverse set selected to exercise the KiCad parser: flat → deep
hierarchy, simple → complex, with buses, global/hierarchical labels, power
symbols, and varied domains. All redistributable (permissive / OSHW licenses).

| Fixture | Upstream | License | Copyright | Exercises |
|---------|----------|---------|-----------|-----------|
| gameboy-DMG-QLA-01 | [Gekkio/gb-schematics](https://github.com/Gekkio/gb-schematics) | CC-BY-4.0 | Joonas Javanainen | single-sheet baseline (no hierarchy), many net labels |
| easyduino-rp2040 | [Hanqaqa/Easyduino](https://github.com/Hanqaqa/Easyduino) | CERN-OHL-P-2.0 | Hanqaqa | minimal hierarchy (2 sheets), MCU |
| cm5-minima | [piecol/CM5_MINIMA_REV3](https://github.com/piecol/CM5_MINIMA_REV3) | CERN-OHL-S-2.0 | piecol | hierarchical SBC carrier + buses |
| openmd-motordriver | [CrabLabsLLC/OpenMD](https://github.com/CrabLabsLLC/OpenMD) | CERN-OHL-W-2.0 | Crab Labs LLC | depth-2 hierarchy, motor/power |
| yddraig-68k | [ddraig68k/hardware](https://github.com/ddraig68k/hardware) | MIT | ddraig68k | extreme bus count (~610), retro |
| gameboy-AGS-CPU-11 | [Gekkio/gb-schematics](https://github.com/Gekkio/gb-schematics) | CC-BY-4.0 | Joonas Javanainen | large hierarchical + buses + global labels |
| cynthion-usb-fpga | [greatscottgadgets/cynthion-hardware](https://github.com/greatscottgadgets/cynthion-hardware) | CERN-OHL-P-2.0 | Great Scott Gadgets | 17 sheets, FPGA/USB, many buses + global labels |
| rdimm-ddr4-tester | [antmicro/rdimm-ddr4-tester](https://github.com/antmicro/rdimm-ddr4-tester) | Apache 2.0 | Antmicro | DDR4 byte lanes (buses), hierarchical |
| leftymobo-ham-trx | [hwstar/Lefty-MOBO](https://github.com/hwstar/Lefty-MOBO) | CC0-1.0 | hwstar | deepest hierarchy (depth 5), 23 sheets, ham-radio transceiver |
| modular-synth-vco | [JordanAceto/josh_Ox_ribbon_synth](https://github.com/JordanAceto/josh_Ox_ribbon_synth) | CC-BY-4.0 | Jordan Aceto | most sheets (24), analog modular synth |

## IPC-2581 Fixtures

Public sample boards published by the IPC-2581 Consortium
(<http://www.ipc2581.com/>) as reference data for the IPC-2581 standard. Spanning
revisions A/B/C and multiple EDA exporters. **Not committed** — downloaded on
demand by `ipc2581/download-fixtures.sh` (see `ipc2581/README.md`).

| Fixture | Board | Rev | Source |
|---------|-------|-----|--------|
| testcase3 (A/B/C) | Round test card | A, B, C | IPC-2581 Consortium |
| testcase4-RevA-Zuken | Zuken CR5000 board | A | IPC-2581 Consortium |
| testcase5-RevA / testcase6-RevA | Network boards | A | IPC-2581 Consortium |
| testcase1-RevC | Network card | C | IPC-2581 Consortium |
| testcase9-RevC | LED display card | C | IPC-2581 Consortium |
| BeagleBone_Black_RevB6 | BeagleBone Black | B | IPC-2581 Consortium |
| parallella-RevB | Parallella | B | IPC-2581 Consortium |

## Notes

- **LimeSDR-USB**: Only the `hardware/` subdirectory is included. Gateware
  and firmware were excluded to reduce repository size.
- **nRF52840-Development-Kit**: The Nordic BSD license permits redistribution
  with attribution. See `altium/nRF52840-Development-Kit/License.txt`.
- **KiCad fixtures**: Non-design files (3D models, gerbers, images, PDFs,
  backups, software, documentation) were pruned; only KiCad design files are
  included.
- Fixtures without explicit license files are included for testing purposes
  under fair use. If you are the copyright holder and would like your files
  removed, please open an issue.
- **misko3** is GPL-3.0, which is redistributable but copyleft rather than
  permissive. Its `LICENSE` is vendored alongside the design. It is test data,
  read by the parsers and never linked into them, so it does not place the
  consuming repositories under the GPL. It is kept because it is the only
  design found that reproduces the sheet-local net over-merge against its own
  board; if a permissively licensed reproducer turns up, prefer it.

## Altium construct coverage

These fixtures were added for signal harness, multi-channel and net-scoping
parser work. Only the sub-project exercising each construct is kept; unrelated
boards, gerbers and 3D models from upstream are omitted. None of the harness or
multi-channel upstream repositories ships a schematic PDF.

| Fixture | Construct | Why it is here |
|---------|-----------|----------------|
| HELIOS-R | signal harness + multi-channel | The only design combining both. `Repeat(CHAN, 1,9)` feeding a harness-typed sheet entry, and harness types that **nest** (`Channel_interface`'s `PGND` entry is itself a `PGND_Domain` harness). Two sheets, 300 KB. |
| qfsae-harness | signal harness, dense | 11 `.Harness` definitions across a Formula SAE loom; harness usage at realistic scale. |
| cube-sat-eps | multi-channel, `$Component$ChannelAlpha` | Non-default channel designator format, and ships no `.PrjPcbStructure`, so channels must be recovered from the sheet symbols. |
| heron-hardware | multi-channel, 8 channels x 4 sheets | Largest channel expansion in the set: 40 components on disk become 320 when expanded. |
| misko3 | sheet-local net scoping, **reproduces the over-merge** | The design that catches issue #128. `AppendSheetNumberToLocalNets=1` with `HierarchyMode=2` (Hierarchical) and a unique `SheetNumber` on all 13 sheets, so Altium numbers each sheet's own nets rather than fusing them. Its board is the ground truth: it carries `VBAT_8`, `YU_7`, `XR_7`, `STM_JTMS_5` and six more for labels drawn on one sheet each, where merging by name yields a single bare net. Note `VBAT` is drawn on sheet 8 **alone**, which is what shows the suffix follows from a net being the sheet's own and not from a name collision. Ships `.Harness` sidecars too. |
| solarcar-bms | net named on one sheet, pinned on another | 31 sheets, the deepest hierarchy in the Altium set. A signal labelled on the top sheet and wired straight into a sheet entry has its pins on the child sheet, so the sheet that names it holds no pins of its own. The board numbers such a net after the naming sheet (`LVB_DIV_1`), which only works if a sheet's claim on a name survives its own copy having no pins. Also the set's reproducer for harness-member numbering, still open: its board carries `USART2.TX_1` and 33 more that we do not yet number. |
| mixr-power | sheet-local net scoping, no collisions | Also sets `AppendSheetNumberToLocalNets=1`, but no name is drawn on two sheets, so it exercises the flag without the split: useful as the case that must **not** be pulled apart. Treat its board as indicative only, not ground truth. It is stale with respect to the schematic (it carries `USB_CC1_2` for a label whose sheet now numbers 3, and leaves other sheet-local labels unsuffixed), so it disagrees with its own sources. 8 sheets. |
