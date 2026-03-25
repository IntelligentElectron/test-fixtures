# License Attribution

This repository contains EDA design files from third-party open-source
hardware projects, collected as test fixtures for
[universal-netlist](https://github.com/IntelligentElectron/universal-netlist).

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

| Fixture | Upstream | License | Copyright |
|---------|----------|---------|-----------|
| 555-blinker-pcb | [yendiDev/555-blinker-pcb](https://github.com/yendiDev/555-blinker-pcb) | No license file | yendiDev |
| ESP32-C3-DevBoard | [21km43/ESP32-C3-DevBoard](https://github.com/21km43/ESP32-C3-DevBoard) | No license file | 21km43 |
| Getting-to-Blinky | [pdnataraj/Getting-to-Blinky](https://github.com/pdnataraj/Getting-to-Blinky) | MIT | Paul Natarajan |
| KiCad-Arduino-Boards | [sabogalc/KiCad-Arduino-Boards](https://github.com/sabogalc/KiCad-Arduino-Boards) | WTFPL | sabogalc |
| kicad_usbc_breakout | [jhugon/kicad_usbc_breakout](https://github.com/jhugon/kicad_usbc_breakout) | No license file | jhugon |
| kintex-410t-devboard | [antmicro/kintex-410t-devboard](https://github.com/antmicro/kintex-410t-devboard) | Apache 2.0 | Antmicro |
| muVox | [muvox-io/muVox](https://github.com/muvox-io/muVox) | CC-BY-SA | muvox-io |
| OLINUXINO | [OLIMEX/OLINUXINO](https://github.com/OLIMEX/OLINUXINO) | CC-BY-SA 3.0 US (HW), GPL v3 (SW) | Olimex LTD |
| rdimm-ddr4-tester | [antmicro/rdimm-ddr4-tester](https://github.com/antmicro/rdimm-ddr4-tester) | Apache 2.0 | Antmicro |
| robotont-electronics-driver-board | [robotont/robotont-electronics-driver-board](https://github.com/robotont/robotont-electronics-driver-board) | CERN-OHL-P v2 | University of Tartu |

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
