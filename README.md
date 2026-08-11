# opentank
(WORK IN PROGRESS) A smart home sensor hub with ESP32-C6, rich analog capabilities, and full self-powering.
https://youtu.be/-s6jZ4U3TzU

## Important note

The USB D-/D+ routing and U17 SDA/SCL routing have been corrected in both the schematic and PCB. The corrected crossovers use F.Cu-to-In1.Cu microvias, so confirm that the selected board stackup and fabricator support 0.30 mm / 0.10 mm laser microvias before ordering.

The `templateforconfiguration.yaml` Home Assistant example is still somewhat broken because its current logic never reports a value below 0. `fulldevicecode.yaml` is the configuration programmed onto the PCB and has been observed running reliably for more than two months. Questions? Email rain@haaseindustries.com or comment on the linked YouTube video.
