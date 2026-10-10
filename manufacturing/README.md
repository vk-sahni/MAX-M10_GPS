# Manufacturing notes

Outputs generated with KiCad 10.0.6 `kicad-cli` from the files in the repository root.

## Fabrication

| Item | Value |
|------|-------|
| Outline | Circular, 36.0025 mm diameter (Edge.Cuts) |
| Layers | 4 copper: F.Cu, In1.Cu, In2.Cu, B.Cu |
| Thickness | 1.6 mm FR4 (0.1 prepreg / 1.24 core / 0.1 prepreg) |
| Min track / clearance | 0.2 mm |
| Min drill | 0.3 mm (62 vias) |
| Mounting holes | 2 × 2.2 mm plated (H1, H2) |
| Surface finish | Not set in the design; specify with the fab (e.g. ENIG) |
| Solder mask / silkscreen | Both sides |

Files in `gerbers/`: copper, mask, paste, silkscreen, Edge_Cuts, Excellon drill (`.drl`) and the `.gbrjob` job file. Upload the folder (zipped) to the fabricator.

## Assembly

- `MAX-M10_GPS_BOM.csv` — bill of materials. Most parts lack manufacturer part numbers and `R11` is `TBD`; complete before ordering assembly.
- `MAX-M10_GPS_positions.csv` — component placement data.
- `MAX-M10_GPS.step` — mechanical model.

## Open items before release

See "Production readiness" in the top-level README (DRC mask bridge at BT2, ERC power flags, `R11`, BOM part numbers, surface finish).
