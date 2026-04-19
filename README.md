# CorsixTH Snap

This repository contains the Snap packaging for [CorsixTH](https://github.com/CorsixTH/CorsixTH).

The current refresh targets:

- CorsixTH `0.69.2`
- `core24`
- strict confinement
- the GNOME extension on Ubuntu 24.04

## Build

The preferred build path for this repository is GitHub Actions rather than a local Snapcraft run.

Pushing a branch triggers `.github/workflows/snap-build.yml`, which:

- builds the snap
- runs review checks
- installs the built snap in a temporary VM
- launches CorsixTH and captures screenshots
- uploads the generated snap as a workflow artifact

The launch smoke test only verifies that the GUI starts; it does not provide
Theme Hospital game data.

## Notes

- CorsixTH requires Theme Hospital game data from an original copy or the demo for actual gameplay; the snap does not bundle it.
- The main packaging definition lives in `snap/snapcraft.yaml`.
