# Schematic audit reconciliation

This branch reconciles the independent schematic and part audits against the
actual KiCad schematic, PCB, and current manufacturer data.

## Corrected

- USB D+ now reaches ESP32-C6 GPIO13 and USB D- reaches GPIO12 through U16.
- U17 SCL now uses GPIO18 and U17 SDA uses GPIO19, matching the main I2C bus
  and `fulldevicecode.yaml`.
- R4 is 681 ohms, which programs the BQ25185 charge current to approximately
  440 mA instead of approximately 910 mA.
- U6 and U11 metadata now consistently identify the real, orderable
  TPS22916CYFPR and link the TPS22916 datasheet.
- U13 and U14 metadata now link the Diodes Incorporated LXS0102 datasheet,
  matching the populated MPN.
- U1 pin 1 is identified as VT/Test and remains intentionally unconnected.
- The overlapping U4 VOUT zones now have distinct priorities.

The USB and U17 crossovers use 0.30 mm / 0.10 mm F.Cu-to-In1.Cu microvias.
Fabricator support for laser microvias must be confirmed before ordering.

## Audit claims not applied

- The TPS61099 feedback divider is already 1.1 Mohm / 249 kohm, producing
  approximately 5.4 V. The reported 1 Mohm value and consequent LDO-headroom
  failure do not match the source files.
- U8 uses the TLV9004 RUC/X2QFN pinout. Its four output-to-inverting-input
  connections are valid voltage followers; outputs are not shorted together.
- U7 pins 7 and 12 are separate unconnected nets in the current source.
- TPS22916CYFPR is a valid TI orderable part, not a nonexistent MPN.

## Remaining release checks

- KiCad ERC still reports legacy symbol-model warnings and six power-pin
  errors. These predate this change and need a separate library/ERC cleanup.
- PCB DRC retains two USB-C footprint edge-clearance errors involving the
  connector's NPTH locating feature and adjacent ground pads. Confirm these
  against the GT-USB-7051A drawing before waiving or altering the footprint.
- Complete a worst-case power and thermal budget before manufacturing.
- Confirm enclosure grounding strategy for H1-H4 and the intended ESD voltage
  for each external interface before changing those parts or connections.
