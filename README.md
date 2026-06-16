# Cyberdeck

CAD source and printable parts for a custom cyberdeck build. Parts are
modeled in [FreeCAD](https://www.freecad.org/) and exported to STL for 3D
printing.

See [`hardware_list.md`](hardware_list.md) for the full electronics and
hardware BOM.

## Repository layout

```
3D_models/   FreeCAD source files (.FCStd)
print_ready/ Export-ready STL meshes
notes/       Design notes and reference dimensions
```

Files ending in `.FCBak` are FreeCAD's automatic backups and can be ignored
or used to recover an earlier revision.

## Parts

### Base housing (`3D_models/BaseHousing.FCStd`)

The main enclosure that houses the Raspberry Pi 5. Features:

- Integrated hinges for the monitor panel
- Chamfered edges and wrist rest
- Mounting holes for the Raspberry Pi

| STL | Description |
| --- | --- |
| `print_ready/BaseHousing-Body-v2.stl` | Current revision — use this one |
| `print_ready/BaseHousing.stl` | Earlier revision (kept for reference) |

Reference dimensions from `notes/baseHousing.txt`:

| Parameter | Value |
| --- | --- |
| Hinge center X | 2.38" |
| Hinge center Y | 0.39" |

### Monitor mount (`3D_models/MonitorMount.FCStd`)

Holds both 7" displays. Pivots on a friction-fit pin.

| STL | Description |
| --- | --- |
| `print_ready/MonitorMount-Body.stl` | Print-ready mesh |

Reference dimensions from `notes/monitorMount.txt` (inches):

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
2. Open the `.FCStd` file you want to edit from `3D_models/`.
3. To regenerate a printable mesh, select the body and use
   **File → Export** (or right-click → *Export*) and choose STL, then save
   into `print_ready/`.

## Printing

The STLs in `print_ready/` can be sliced directly in your slicer of choice
(PrusaSlicer, Cura, OrcaSlicer, etc.). Re-export from the `.FCStd` source if
you change the model.
