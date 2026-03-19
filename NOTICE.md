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

## Notes

- **LimeSDR-USB**: Only the `hardware/` subdirectory is included. Gateware
  and firmware were excluded to reduce repository size.
- **nRF52840-Development-Kit**: The Nordic BSD license permits redistribution
  with attribution. See `altium/nRF52840-Development-Kit/License.txt`.
- Fixtures without explicit license files are included for testing purposes
  under fair use. If you are the copyright holder and would like your files
  removed, please open an issue.
