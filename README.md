# 3D-Printed 6S Racing Drone

A fully 3D-printed 5-inch X-quad FPV racing drone designed in Onshape — frame, arms,
and waterproof enclosures are all printed. Designed for 6S power.

> **Draft README.** The facts, measurements, and file list below were compiled
> from the Onshape model and the exported STLs. The "Why I built this" section
> is a placeholder for the builder's own words.

## What it is

A first-person-view (FPV) racing quadcopter. The frame is a true-X layout with
four flat, tapered arms and a central top plate, designed in the Onshape
document ["racing drone"](https://cad.onshape.com/documents/57b30fe062deae315745b482/w/472712d7beec1ac27b6e40ff/e/95e0f703430a6ff77fdf3e90)
(current design: Part Studio **V4**, 389 features, 15 parts). The electronics
are protected from water by sealed 3D-printed enclosures: a waterproof ESC box,
a camera housing, an ESP32 case, and battery feet.

## What makes it unique

- **Fully 3D-printed.** The whole airframe is printed — arms, top plate,
  central enclosure, and all the accessories. No cut carbon fiber anywhere in
  the current design; the V1 tab is named "Carbon Fiber Tubes" because the
  first iteration used carbon-fiber tubes, and the current V4 design is printed
  throughout. The vulnerable electronics get custom sealed enclosures: the ESC
  lives in a lidded waterproof box (V3), the camera in its own printed housing,
  and the ESP32 in a printed case with a front port slot. The enclosures use a
  silicone seal — the design's shared variables include a 6.6 mm silicone size
  (`#sizeofsilicone`).
- **Kevlar-cord stiffening.** Holes in the arms carry Kevlar cord to stiffen
  the printed frame — the Ø5.0 mm holes at the arm tips (97.0 mm from center)
  are the cord holes.
- **6S power.** Built for 6S batteries, which is unusual for a small printed
  racing frame — most printed mini-quads run 4S. Higher voltage means more
  punch for the same current, at the cost of needing ESCs and motors rated
  for 6S.
- **Designed in four iterations.** V1 through V4 are all in the document, so
  the design history is visible: V1 (carbon-fiber tubes), V2, V3, and the
  current V4.

## Verified specifications

All measurements below were taken from the Onshape model with the Measure tool
(millimeters) or computed from the exported STLs. Nothing here is estimated.

| Spec | Value |
|---|---|
| Layout | True-X quad, 4 arms |
| Motor-to-motor diagonal | 233.5 mm |
| Adjacent-motor spacing | 165.1 mm |
| Motor axis distance from center | 116.75 mm |
| Motor mounting pattern | 4x M3 holes (Ø3.0 mm) on a 16.0 mm bolt circle, per arm tip |
| Extra hole at each arm tip | Ø5.0 mm, centered 97.0 mm from frame center (Kevlar cord hole) |
| Arm top-face area (one arm) | 1,626 mm² |
| Current design | V4 Part Studio, 389 features, 15 parts |
| Power | 6S (build intent) |
| Prop size | 5-inch (confirmed by the builder) |

Motor mounting uses M3 screws 10 mm long (`#motorscrewlength`), with a 3.0 mm
motor-bracket thickness (`#motorbracketthickness`) and 3.7 mm brass inserts
(`#brassinsertd`). Other shared variables: mounting screw Ø2.25 mm, hook
screw Ø2.7 mm, ESC screw hole Ø3.0 mm, motor screw head 3.0 mm thick.

**Prop size — 5-inch (confirmed by the builder).** The measured 233.5 mm
motor diagonal and 16 mm motor pattern are 5-inch class (3-inch motors use
9 mm or 12 mm patterns), matching the builder's confirmation that this is a
5-inch drone.

**Plate thickness / print material — not stated in the model.** The frame/arm
plate thickness was not measured, and the print material is not specified in
the model. The frame is 3D printed (confirmed by the builder); the V1 tab
name ("Carbon Fiber Tubes") refers to the first iteration, not the current
design.

## 3D-printed parts

All STLs are in `STL/`, exported from Onshape as binary STL, millimeters,
fine resolution. Each file was checked programmatically: valid binary STL,
zero degenerate triangles, and watertight.

| Part | File | Triangles | Size (mm) | Volume | Watertight |
|---|---|---|---|---|---|
| Battery Feet (left) | `STL/Battery-Feet/Battery-Feet-Part-1.stl` | 11,190 | 50.2 x 19.1 x 12.7 | 7,625 mm³ | Yes |
| Battery Feet (right) | `STL/Battery-Feet/Battery-Feet-Part-2.stl` | 11,330 | 50.2 x 19.1 x 12.7 | 7,625 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-1.stl` | 152 | 4.7 x 2.8 x 19.1 | 147 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-2.stl` | 968 | 11.0 x 11.0 x 5.1 | 313 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-3.stl` | 51,894 | 24.2 x 14.9 x 16.7 | 2,027 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-4.stl` | 24 | 15.0 x 34.4 x 14.5 | 3,583 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-5.stl` | 4,536 | 28.0 x 14.7 x 15.8 | 3,468 mm³ | Yes |
| Camera V2 | `STL/Camera-V2/Camera-V2-Part-6.stl` | 5,726 | 28.0 x 14.7 x 6.0 | 797 mm³ | Yes |
| Waterproof ESC V3 (box) | `STL/Waterproof-ESC-V3/Waterproof-ESC-V3-Part-1.stl` | 8,404 | 49.8 x 51.4 x 21.0 | 9,334 mm³ | Yes |
| Waterproof ESC V3 (lid) | `STL/Waterproof-ESC-V3/Waterproof-ESC-V3-Part-2.stl` | 13,768 | 49.8 x 51.4 x 4.1 | 4,392 mm³ | Yes |
| ESP32 Case | `STL/ESP32-Case/ESP32-Case-Part-1.stl` | 3,960 | 29.1 x 48.3 x 5.0 | 5,552 mm³ | Yes |
| ESP32 Case | `STL/ESP32-Case/ESP32-Case-Part-2.stl` | 24,862 | 33.7 x 56.5 x 17.7 | 13,521 mm³ | Yes |
| Controller Cap | `STL/Controller-Cap/Controller-Cap-Part-1.stl` | 20,356 | 28.5 x 28.5 x 17.0 | 2,430 mm³ | Yes |
| Controller Cap | `STL/Controller-Cap/Controller-Cap-Part-2.stl` | 5,214 | 11.6 x 11.7 x 16.6 | 588 mm³ | Yes |

Notes on the printed parts:

- **Battery Feet** are a mirrored pair: two U-shaped feet on a thin
  translucent battery pad.
- **Camera V2** is the current camera housing (6 parts: body, orange top,
  front lens opening, mount pieces). Camera V1 (4 parts) is a superseded
  iteration and is not in this repo.
- **Waterproof ESC V3** is a sealed translucent-blue box with a lid and a top
  window, plus a "MOTOR BELL" feature. V1 and V2 are superseded and not in
  this repo.
- **ESP32 Case** is a two-part enclosure with a dark-blue lid, rim holes, and
  a front port slot.
- **Controller Cap** is a small tapered cap built on an imported dual-axis
  joystick module part.
- **Camera V2 Part 3 re-checked watertight.** An earlier check flagged it as
  having 4 bad edges, but a re-check of the file in the repo (51,894
  triangles, 25,929 vertices, 77,841 edges — every edge shared by exactly two
  triangles, consistent winding, zero degenerate triangles) shows it is a
  closed mesh. No repair needed.

## Bought parts (not printed)

The frame, arms, top plate, and all enclosures are 3D printed (see `STL/`).
The bought parts are:

- Motors: 16 mm pattern (M3), 220x-size class. Specific motor model not
  stated in the model.
- 4-in-1 ESC board: the document holds a photograph of a red 4-in-1 ESC as a
  reference, but the exact model is not identified in the document.
- Dual-axis joystick module with 3-pin SH1.0 connectors (XA011): imported
  STEP, used under the Controller Cap.

## Electronics — to be confirmed

The flight controller, ESC model, motors, battery, VTX, and camera are not
specified in the Onshape model. Add them here once confirmed. The ESP32 case
implies an ESP32 is part of the build.

## Design history

| Version | Features | Parts | Notes |
|---|---|---|---|
| V1 | 101 | 9 | Carbon Fiber Tubes |
| V2 | 202 | 11 | Second iteration |
| V3 | 377 | 20 | Third iteration |
| **V4** | **389** | **15** | **Current design** |
| Waterproof Simulate | 391 | 1 | Single-solid test copy of the frame |

Camera V1, Waterproof ESC V1, and Waterproof ESC V2 are superseded iterations
kept in the Onshape document but not exported here.

## Files

```
.
├── README.md
├── LICENSE                     # MIT
├── LICENSE-HARDWARE            # CERN-OHL-S v2 (hardware)
├── CAD/
│   └── README.md               # full-assembly STEP location (in Onshape)
├── STL/
│   ├── Battery-Feet/           # 2 STLs, mirrored pair
│   ├── Camera-V2/              # 6 STLs, current camera housing
│   ├── Waterproof-ESC-V3/      # 2 STLs, sealed ESC box + lid
│   ├── ESP32-Case/             # 2 STLs, enclosure + lid
│   └── Controller-Cap/         # 2 STLs
```

The full-assembly STEP (`racing-drone-V4-assembly.step`, 2 MB, STEP AP242)
was exported from V4 in Onshape and is stored as a file tab in the
["racing drone" document](https://cad.onshape.com/documents/57b30fe062deae315745b482/w/472712d7beec1ac27b6e40ff/e/95e0f703430a6ff77fdf3e90)
— it is not in this repo yet because the download from Onshape failed. See
`CAD/README.md`.

## Printing

All 14 STLs were validated as printable meshes (see the table above). Print
material, layer height, and slicer settings are not specified in the model —
add them here once the parts have been test-printed.

## Why I built this

*[Write this in your own words: what made you design this drone, what problem
the waterproofing solves, and what you want to do with it.]*

## License

- Code and documentation: MIT — see `LICENSE`.
- Hardware design files: CERN Open Hardware Licence v2, Strongly Reciprocal
  (CERN-OHL-S v2) — see `LICENSE-HARDWARE`.
