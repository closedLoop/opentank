# Orientation audit

## Status: BLOCKED for assembly release

Local model placement has been checked against the footprint geometry and datasheet dimensions. The assembler preview remains pending, and J1/J2 use dimensionally constrained visualization models rather than detailed manufacturer CAD.

| Designator | Class | Exact MPN/package | Product-facing feature | Expected orientation | Datasheet locator | Footprint/pad evidence | Raw 2D artifact | Raw 3D artifact | Source rotation | Model offset / rotation | JLC preview | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| J1 | Connector | Phoenix Contact 1792960, PTS 1,5/12-5,0-H | Wire entry and push buttons | Linear row follows the labeled field-I/O edge | [Dimensions and drawing](../references/1792960.pdf) | Pads 1–12 at 5.00 mm pitch; F.Fab envelope 60 × 10.5 mm | [`pcb-top.svg`](../assets/images/pcb-top.svg) | [`pcb-isometric.png`](../assets/images/pcb-isometric.png) | 180° | 0,0,0 / 0° | pending | local envelope checked / detailed CAD blocked |
| J2 | Connector | G-Switch GT-USB-7051A, vertical USB-C | Top-entry mating mouth | Mating axis normal to the PCB at the USB edge | [Sheet 1 mechanical drawing](../references/GT-USB-7051A.pdf) | Symmetric 16-pin land pattern, four shell stakes, two locating features | [`pcb-top.svg`](../assets/images/pcb-top.svg) | [`pcb-isometric.png`](../assets/images/pcb-isometric.png) | 90° | 0,0,0 / 0° | pending | local envelope checked / detailed CAD blocked |
| U12 | Radio module | ESP32-C6-MINI-1U-N4 | Pin 1 and external antenna connector | Pin map and module boundary coincide with the four-sided land pattern | [Figures 10-2 and 11-2](../references/ESP32-C6-MINI-1U-N4.pdf) | 13.2 × 12.5 mm F.Fab body; pads 1–53 | [`pcb-top.svg`](../assets/images/pcb-top.svg) | [`pcb-isometric.png`](../assets/images/pcb-isometric.png) | 0° | -6.749,-1.515,0 / -90° X | pending | local-checked / JLC-pending |

The report remains blocked until exact detailed connector CAD and the final assembler preview have been reviewed. This does not invalidate the dimensionally corrected README render.
