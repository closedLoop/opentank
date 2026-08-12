# Component datasheet reference library

This directory contains a local PDF reference for every identified orderable
electrical or electromechanical part in `watertankv2.kicad_sch`. Repeated
components share one PDF. The mapping below was generated from the schematic
BOM and checked against the manufacturer part numbers.

## Schematic reference map

| Schematic reference(s) | Manufacturer part number | Local reference |
| --- | --- | --- |
| C1, C14, C15 | GRM155Z71A105KE01D | [GRM155Z71A105KE01D.pdf](GRM155Z71A105KE01D.pdf) |
| C2-C7, C23 | GRM21BR61A226ME44L | [GRM21BR61A226ME44L.pdf](GRM21BR61A226ME44L.pdf) |
| C8, C9 | GRM31CR71C106KAC7L | [GRM31CR71C106KAC7L.pdf](GRM31CR71C106KAC7L.pdf) |
| C10, C11 | GRM155Z71A225KE44D | [GRM155Z71A225KE44D.pdf](GRM155Z71A225KE44D.pdf) |
| C12, C13, C16-C22, C24-C28 | GRM033R61A104KE15D | [GRM033R61A104KE15D.pdf](GRM033R61A104KE15D.pdf) |
| D1, D2 | SM5817PL-TP | [SM5817PL-TP.pdf](SM5817PL-TP.pdf) |
| D3-D12 | DF2S8.2FS,L3M | [DF2S8.2FS_L3M.pdf](DF2S8.2FS_L3M.pdf) |
| F1 | C1F 3 | [C1F_series.pdf](C1F_series.pdf) |
| J1 | 1792960 | [1792960.pdf](1792960.pdf) |
| J2 | GT-USB-7051A | [GT-USB-7051A.pdf](GT-USB-7051A.pdf) |
| L1 | 74404043010A | [74404043010A.pdf](74404043010A.pdf) |
| L2 | LQM2HPN2R2MG0L | [LQM2HPN2R2MG0L.pdf](LQM2HPN2R2MG0L.pdf) |
| R1, R9, R11-R13 | RC0201JR-07100RL | [RC0201JR-07100RL.pdf](RC0201JR-07100RL.pdf) |
| R2, R5, R15, R16 | RC0201FR-07511KL | [RC0201FR-07511KL.pdf](RC0201FR-07511KL.pdf) |
| R3 | RC0402FR-076K8L | [RC0402FR-076K8L.pdf](RC0402FR-076K8L.pdf) |
| R4 | RC0402FR-07681RL | [RC0402FR-07681RL.pdf](RC0402FR-07681RL.pdf) |
| R6 | RC0201FR-0791KL | [RC0201FR-0791KL.pdf](RC0201FR-0791KL.pdf) |
| R7 | RC0201FR-071M1L | [RC0201FR-071M1L.pdf](RC0201FR-071M1L.pdf) |
| R8 | RC0201FR-07249KL | [RC0201FR-07249KL.pdf](RC0201FR-07249KL.pdf) |
| R10, R14, R17-R19 | RC0201FR-0710KL | [RC0201FR-0710KL.pdf](RC0201FR-0710KL.pdf) |
| R23, R24 | RC0402FR-075K1L | [RC0402FR-075K1L.pdf](RC0402FR-075K1L.pdf) |
| SW1, SW2 | HX-B3U-1000P-1.6N | [HX-B3U-1000P-1.6N.pdf](HX-B3U-1000P-1.6N.pdf) |
| TH1 | 103AT-4-70374 | [103AT-4-70374.pdf](103AT-4-70374.pdf) |
| U1 | DW03C | [DW03C.pdf](DW03C.pdf) |
| U2 | BQ25185DLHR | [BQ25185DLHR.pdf](BQ25185DLHR.pdf) |
| U3 | TPS631010YBGR | [TPS631010YBGR.pdf](TPS631010YBGR.pdf) |
| U4 | TPS61099YFFR | [TPS61099YFFR.pdf](TPS61099YFFR.pdf) |
| U5 | TPS7A2050PYCKR | [TPS7A2050PYCKR.pdf](TPS7A2050PYCKR.pdf) |
| U6, U11 | TPS22916CYFPR | [TPS22916CYFPR.pdf](TPS22916CYFPR.pdf) |
| U7 | TMUX1511RSVR | [TMUX1511RSVR.pdf](TMUX1511RSVR.pdf) |
| U8 | TLV9004IRUCR | [TLV9004IRUCR.pdf](TLV9004IRUCR.pdf) |
| U9 | TLV809EA46DBZR | [TLV809EA46DBZR.pdf](TLV809EA46DBZR.pdf) |
| U10 | ADS1115IRUGR | [ADS1115IRUGR.pdf](ADS1115IRUGR.pdf) |
| U12 | ESP32-C6-MINI-1U-N4 | [ESP32-C6-MINI-1U-N4.pdf](ESP32-C6-MINI-1U-N4.pdf) |
| U13, U14 | LXS0102GBAEX | [LXS0102GBAEX.pdf](LXS0102GBAEX.pdf) |
| U15 | TLV803EA29DPWR | [TLV803EA29DPWR.pdf](TLV803EA29DPWR.pdf) |
| U16 | USBLC6-2P6 | [USBLC6-2P6.pdf](USBLC6-2P6.pdf) |
| U17 | TMP102AIDRLR | [TMP102AIDRLR.pdf](TMP102AIDRLR.pdf) |

## Items without a distinct datasheet

- `BT1` is specified only as an NMC 21700 cell/holder combination and has no
  manufacturer or orderable part number in the schematic. A battery-cell safety
  datasheet must be added when the exact cell is selected.
- `TP1`-`TP10` use generic PCB test-point footprints and are not purchased parts.
- `JP1` is a copper solder jumper and is not a purchased part.
- `H1`-`H4` are bare PCB mounting holes and are not purchased parts.

## Source and validation notes

- Manufacturer PDFs were preferred. Exact manufacturer/distributor specification
  sheets are used where a manufacturer serves part data dynamically or blocks
  unattended downloads.
- `1792960.pdf` is the Phoenix Contact generated product sheet mirrored by RS.
- `103AT-4-70374.pdf` is Semitec's exact AT-4 assembly sheet mirrored by ATC
  Semitec.
- `USBLC6-2P6.pdf` is a distributor product sheet for the exact STMicroelectronics
  order code; the current manufacturer document is
  <https://www.st.com/resource/en/datasheet/usblc6-2.pdf>.
- All 38 files have a PDF signature and pass `pdfinfo` parsing.

Useful source portals: [Texas Instruments](https://www.ti.com/),
[Murata](https://www.murata.com/), [Yageo](https://www.yageogroup.com/),
[Espressif](https://www.espressif.com/),
[STMicroelectronics](https://www.st.com/), and
[G-Switch](https://www.dg-switch.com/).
