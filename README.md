# Cyberdeck

CAD source and printable parts for a custom cyberdeck build. Parts are
modeled in [FreeCAD](https://www.freecad.org/) and exported to STL for 3D
printing.

## Parts

| File | Description |
| --- | --- |
| `MonitorMount.FCStd` | FreeCAD model for the monitor mount. |
| `MonitorMount-Body.stl` | Print-ready mesh exported from the monitor mount. |
| `BaseHousing.FCStd` | FreeCAD model for the base housing/enclosure. |
| `notes/` | Design notes and reference dimensions. |

Files ending in `.FCBak` are FreeCAD's automatic backups (saved with a
timestamp) and can be ignored or used to recover an earlier revision.

## Monitor mount dimensions

From `notes/monitorMount.txt` (inches):

| Parameter | Value |
| --- | --- |
| X | 6.45" |
| Y | 4.9" |
| Inner diameter | 0.75" |
| Outer diameter | 1" |
| Pin size | 0.74" |

The matching pin (0.74") and inner diameter (0.75") give a close
friction/pivot fit.

## Working with the source files

1. Install FreeCAD (1.0 or newer recommended).
2. Open the `.FCStd` file you want to edit.
3. To regenerate a printable mesh, select the body and use
   **File → Export** (or right-click → *Export*) and choose STL.

## Printing

The included `.stl` files can be sliced directly in your slicer of choice
(PrusaSlicer, Cura, OrcaSlicer, etc.). Re-export from the `.FCStd` source if
you change the model.
