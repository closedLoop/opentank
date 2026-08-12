# 3D model provenance

These models keep the KiCad project portable and make the assembly render dimensionally meaningful. They are checked into the repository and referenced through `${KIPRJMOD}`.

| Model | Designator(s) | Evidence and status |
| --- | --- | --- |
| `ESP32-C6-MINI-1U.STEP` | U12 | Exact Espressif manufacturer model for the 13.2 × 12.5 × 2.4 mm module, downloaded from the [ESP32-C6-MINI-1U product page](https://www.espressif.com/en/module/esp32-c6-mini-1u-en). |
| `Phoenix_1792960.step` | J1 | Dimensionally constrained visualization model: 60 × 10.5 × 13.6 mm installed envelope and 5.00 mm pitch from the [1792960 datasheet](../../references/1792960.pdf). It is not detailed manufacturer CAD. |
| `GT-USB-7051A.step` | J2 | Dimensionally constrained visualization model: 11 × 7 × 11.45 mm vertical/top-entry envelope, centered on the published land pattern from the [GT-USB-7051A datasheet](../../references/GT-USB-7051A.pdf). It is not detailed manufacturer CAD. |
| `TLV803EA29DPW.step` | U15 | Datasheet package envelope: DPW X2SON-5, 0.8 × 0.8 × 0.4 mm ([datasheet](../../references/TLV803EA29DPWR.pdf)). |
| `TPS22916YFP.step` | U6, U11 | Footprint-matched YFP DSBGA-4 visualization envelope, 0.75 × 0.75 × 0.5 mm ([datasheet](../../references/TPS22916CYFPR.pdf)). |
| `TPS61099YFF.step` | U4 | Footprint-matched YFF DSBGA-6 visualization envelope, 0.88 × 1.23 × 0.62 mm ([datasheet](../../references/TPS61099YFFR.pdf)). |
| `ADS1115RUG.step` | U10 | Datasheet package envelope: RUG X2QFN-10, 1.5 × 2.0 × 0.4 mm ([datasheet](../../references/ADS1115IRUGR.pdf)). |
| `TPS7A2050YCK.step` | U5 | Datasheet package envelope: YCK DSBGA-4, 0.62 × 0.62 × 0.33 mm ([datasheet](../../references/TPS7A2050PYCKR.pdf)). |
| `TLV9004RUC.step` | U8 | Datasheet package envelope: RUC X2QFN-14, 2.0 × 2.0 × 0.4 mm ([datasheet](../../references/TLV9004IRUCR.pdf)). |
| `TMUX1511RSV.step` | U7 | Datasheet package envelope: RSV UQFN-16, 1.8 × 2.6 × 0.55 mm ([datasheet](../../references/TMUX1511RSVR.pdf)). |

Package-envelope models are suitable for board visualization and gross clearance review. Use exact manufacturer CAD for final enclosure, connector-access, and interference validation.
