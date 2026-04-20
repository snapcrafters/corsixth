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
- uploads the generated snap as a workflow artifact

## Notes

- CorsixTH requires Theme Hospital game data from an original copy or the demo; the snap does not bundle it.
- The main packaging definition lives in `snap/snapcraft.yaml`.
- A smoke test workflow is intentionally omitted here because the app cannot launch usefully in CI without external game data.
