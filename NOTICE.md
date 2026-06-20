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
