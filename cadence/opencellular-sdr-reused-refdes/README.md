# OpenCellular OC-CONNECT1 SDR, rev C, with a reused reference designator

A copy of the `opencellular-sdr` fixture with two values changed, so that one
reference designator names two different parts and one part draws a section
twice. Capture lets a schematic do both, but the Allegro netlister refuses
the design, and a reader that keys parts by reference designator merges the
two parts' pins.

- Derived from: `cadence/opencellular-sdr/OC_CONNECT1_SDR_REV_C_V1P1.DSN`
  (upstream <https://github.com/Telecominfraproject/OpenCellular>, path
  `electronics/radio/SDR/schematics/DSN/OC_CONNECT1_SDR_REV_C_V1P1.DSN`,
  commit `0d5d7b005327e4378bd5c7fd44d7b8dc5ab796f6`)
- License: CC BY 4.0 (`LICENSE`, the upstream `LICENSE-HARDWARE`). This copy is
  modified, as listed below.

## Changes from the original

The file differs from the original in two bytes:

1. On page `PAGE 25 REG_12V_3P7V_LDO_3P3V`, capacitor `C4003` (0.1 uF) is
   renamed `R4003`, the reference of a 0 ohm resistor on the same page. The
   page record's inline reference is the only place the design names this part.
2. On page `PAGE 06 FPGA_1`, the `XC7A100T-3FGG484` instance drawing section E
   of `U9` records section index 2 (section C) instead of 4. Section C is also
   drawn on page `PAGE 10 FPGA_4`. The part's pin numbers come from its
   occurrences, so both instances keep their own pins.

Both edits keep every record's length, and the Library, Cache and Hierarchy
streams are unchanged.

## What it exercises

- `R4003` names two different parts (a resistor and a capacitor, with different
  packages and values), so a reader must keep them apart: two parts, each with
  its own pins, rather than one part with a mix of both.
- `U9` draws section C twice with no pin wired to two different nets, so it is
  one part with every pin of the original, drawing one section twice.
