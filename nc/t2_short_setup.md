# Setup sheet — op10

- Machine: Haas Automation VF-2 (`vf2/axes`)
- Program: `op10`, 67 lines
- Cycle: 68.5 s — cutting 49.4 s, rapids 10.7 s, standing 8.4 s, 2 tool changes
- Machine functions, in order (the cell's time, not in the cycle above): M71 vise unclamp (line 60), M180 door open (line 61), M21 arm: part out, blank in (line 62), M70 vise clamp (line 63), M22 arm: let go and leave (line 64), M181 door closed (line 65)

## Stock

- `part` (WP-40): 40.0 x 40.0 x 60.0 mm
- Centre from the middle of the table's top: X+330.000 Y+0.000 Z+95.000 mm (top face 125.0 mm above the table)

## Fixtures

| obstacle | article | size [mm] | centre on the table [mm] |
|---|---|---|---|
| `vise/body` | botrail VQ-125 | 145.0 x 360.0 x 60.0 | X+330.000 Y-108.000 Z+30.000 |
| `vise/jaw_fixed` | botrail VQ-125 | 125.0 x 30.0 x 40.0 | X+330.000 Y+37.000 Z+80.000 |
| `vise/jaw_moving` | botrail VQ-125 | 125.0 x 30.0 x 40.0 | X+330.000 Y-37.000 Z+80.000 |

## Work offsets

| offset | machine coordinates [mm] | work zero from the stock's centre [mm] |
|---|---|---|
| G54 | X-51.000 Y-211.500 Z-485.000 | X+0.000 Y+0.000 Z+30.000 |

## Tools

| T | tool | flutes [mm] | holder ⌀ x length [mm] | length [mm] | table entry H [mm] | |
|---|---|---|---|---|---|---|
| T1 | 10 mm flat end mill | 22 | 40 x 75 | 110.000 | 110.000 |  |
| T2 | 5 mm drill | 45 | 40 x 75 | 135.000 | 115.000 | **entry -20.000 mm from the tool** |

Spindle, as programmed: T1 S6000; T2 S4000.

## Dry run

- Axes within X-762.000 Y-227.500 Z-378.500 to X-24.000 Y-160.500 Z+0.000 mm (machine coordinates); travel X -762 to 0, Y -406 to 0, Z -508 to 0 mm
- Removed: 5.51 cm³ of 96.00 — T1 1.74 cm³, T2 3.77 cm³
- **op10 line 46: the cutter meets `part` at rapid (T2, 88.1 mm³, at 40.75 s)**
- **op10 line 48: the cutter meets `part` at rapid (T2, 254.6 mm³, at 40.82 s)**
- **op10 line 49: the cutter meets `part` at rapid (T2, 885.4 mm³, at 46.98 s)**
- **op10 line 50: the cutter meets `part` at rapid (T2, 879.2 mm³, at 53.28 s)**
- **op10 line 51: the cutter meets `part` at rapid (T2, 879.2 mm³, at 59.58 s)**
- **First part against the design (±0.05 mm): 0.0 mm³ left over, 3152.6 mm³ missing.**
