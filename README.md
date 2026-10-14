# Kodak Gold 200: film scans and matching digital captures

Raw files behind a Fotufilm vs spektrafilm comparison on a real roll of Kodak Gold 200.
Three scenes were shot on Gold 200 and on a Sony A7C II from roughly the same spot (handheld, so
viewpoint and framing differ slightly). The developed film was scanned with the same A7C II over a
SmallRig RM120 light, one exposure per LED colour.

Download: [gold200-dataset-2026-10-14.zip](https://github.com/DhaliwalX/gold200-dataset/releases/download/v1.0/gold200-dataset-2026-10-14.zip) (555 MB)

Licence: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

## Contents

| Folder | What |
|---|---|
| `film-scans/frameNN/` | Three raw scans of each film frame, one per LED: `red`, `green`, `blue` |
| `clear-base/` | Clear (unexposed, developed) film from the same roll, one raw per LED, for flat-fielding |
| `digital/` | The matching A7C II capture of each scene |

| Film frame | Digital capture | Scene | Post |
|---|---|---|---|
| 13 | UPS02715 | Barn | Frame 1 |
| 17 | UPS02735 | Sunflowers | Frame 2 |
| 18 | UPS02736 | Gladiolus | Frame 3 |

The original camera file number is kept in every filename.

## Scanning notes

- RM120 channels, estimated from raw shots of each LED and the A7C II's published spectral
  response (rawtoaces-data, `Sony_ILCE-7CM2_380_780_5.json`): blue ≈455 nm, green ≈522 nm,
  red ≈625 nm, each ±5 nm.
- The scans were shot in aperture priority, so exposure differs between files and the EXIF shutter
  speeds are rounded. Take each frame's base level from its own clear border (left, right and top
  of the picture area) rather than from the shutter speed; use `clear-base` only for the shape of
  the light falloff.
- Each colour comes from that LED's own photosites (red sites for the red LED, and so on).
