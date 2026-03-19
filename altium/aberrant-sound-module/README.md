# Aberrant Sound Module

## About the Device
A sound card based on AY-3-8912 for the microcomputer "[Elektronika MS 0511](https://ru.wikipedia.org/wiki/%D0%AD%D0%BB%D0%B5%D0%BA%D1%82%D1%80%D0%BE%D0%BD%D0%B8%D0%BA%D0%B0_%D0%9C%D0%A1_0511)" (UKNC).
![photo-of-the-module](Doc/IMG_5550.JPG)

## Project Contributors
* Schematic - [aberranthacker](https://github.com/aberranthacker)
* Final schematic revision and PCB layout - [zloiMOZG](https://github.com/zloiMOZG)

## Features
* **3 AY-3-8912 sound generators**
* **Bus drivers with inversion**, no more software bit-flipping :)
* **Expansion connector** (feature connector), allows connecting additional
  devices to the peripheral processor without duplicating bus logic and address decoding
* Address range 0177360-0177377
  * Addresses 0177360, 0177362, and 0177364 are used by AY-3-8912
  * Address detector lines for range 0177366-0177377 are routed to the future
    connector (P2)
* Implemented with discrete logic in classic **DIP packages** -
  an authentic "retro" solution
* Communication with sound generators is implemented the same way as on BK-series computers
  * Writing a word sends the AY register address
  * Writing a byte sends data to the sound generator register

## Known Issues with Current Board Revision
* The key notch at the bottom of the board does not align with the peripheral processor slot key; the notch needs to be extended to the left by half its width
* The crystal oscillator footprint is mirrored; the oscillator must be rotated 180 degrees and a jumper wire added

## Address Map
* 0o177360 AY1
* 0o177362 AY2
* 0o177364 AY3
* 0o177366 -unused- (MIDI control in the alternative FPGA implementation)
* 0o177370 -unused- (MIDI data in the alternative FPGA implementation)
* 0o177372 DAC (Covox)
* 0o177374 YM3812 (OPL2)
* 0o177376 -unused-

## Is There Any Software?
Currently, sound output works in the game [ChibiAkuma's](https://github.com/aberranthacker/chibiakumas), and in the music demo [timeCS](https://github.com/aberranthacker/timeCS).

[The AKG (generic) player](https://github.com/aberranthacker/akg_player) has been ported, for music created in arguably the most advanced [Arkos Tracker 2](http://www.julien-nevo.com/arkostracker/). It can also be used to create sound effects without diving deep into AY specifics.

Additionally, the BK-0011M version of the `*.pt3` player has been [adapted](https://github.com/aberranthacker/timeCS/blob/master/pt3play2.s).
A distinctive feature of the UKNC version is that it is designed to work with a track stored in
one of the memory banks. Track data is read byte-by-byte from a specific
memory bank using address/data registers. When using banks 1
or 2 (or if overwriting CPU RAM in HALT mode is acceptable), this
allows playing tracks up to 36K per chip.

## Where Are the Gerber Files?
`./Project Outputs for aberrant_sound_module/aberrant_sound_module 1.0.0/`

## Background
The sound capabilities of the UKNC are limited to a 1-bit beeper. Unfortunately, they were never
expanded back when the grass was greener and these computers were still being manufactured and widely used.

The idea of creating a sound card for the UKNC came up long ago, but its implementation became
relevant only during the porting of the ChibiAkuma's game, when a real need for such a device arose.

### Core Design Principles:
* **Authenticity**: The device is built from components available in the early 1990s,
  making it a kind of fantasy about what a sound expansion for the UKNC could have been,
  had this computer gained wider adoption as a home PC.
* **Compactness**: The board size does not exceed that of a standard floppy drive controller module.
* **Expansion connector (future connector)**: This connector allows connecting
  additional devices to the peripheral processor with minimal effort.
