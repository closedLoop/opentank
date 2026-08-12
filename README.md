# opentank
(WORK IN PROGRESS) A smart home sensor hub with ESP32-C6, rich analog capabilities, and full self-powering.
https://youtu.be/-s6jZ4U3TzU

## Design views

### Isometric 3D view

![OpenTank PCB isometric 3D render](assets/images/pcb-isometric.png)

The render now uses repository-local models instead of machine-local CAD paths. U12 uses Espressif's exact manufacturer STEP model; J1, J2, and the previously missing small packages use footprint-aligned, datasheet-sized visualization models documented in [`assets/3d/README.md`](assets/3d/README.md). Confirm connector details and enclosure fit with exact manufacturer CAD before assembly release. The TH1 solder-wire footprint intentionally has no fitted component body.

### PCB top view

![OpenTank PCB top copper and silkscreen](assets/images/pcb-top.svg)

### PCB bottom view

![OpenTank PCB bottom copper and silkscreen](assets/images/pcb-bottom.svg)

### Schematic

![OpenTank circuit schematic](assets/images/schematic.svg)

## Changes versus `main`

These comparisons use matching KiCad layers, scale, and sheet coordinates. Magenta marks geometry present only on `main` (removed or moved), green marks geometry present only on this branch (added or moved), and gray provides unchanged context.

### PCB top comparison

![OpenTank PCB top view compared with main](assets/images/diffs/pcb-top-vs-main.png)

### PCB bottom comparison

![OpenTank PCB bottom view compared with main](assets/images/diffs/pcb-bottom-vs-main.png)

### Schematic comparison

![OpenTank schematic compared with main](assets/images/diffs/schematic-vs-main.png)

## Important note

The USB D-/D+ routing and U17 SDA/SCL routing have been corrected in both the schematic and PCB. Both USB data pairs now remain on F.Cu without vias; the MCU-side pair is length tuned to 0.001 mm routed skew and assigned to a 0.127 mm / 0.150 mm USB width/gap net class targeting 90-ohm differential impedance.

The `templateforconfiguration.yaml` Home Assistant example is still somewhat broken because its current logic never reports a value below 0. `fulldevicecode.yaml` is the configuration programmed onto the PCB and has been observed running reliably for more than two months. Questions? Email rain@haaseindustries.com or comment on the linked YouTube video.
