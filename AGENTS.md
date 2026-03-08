# Repository Guidelines

## Project Structure & Module Organization
This repository stores custom OrcaSlicer profiles, grouped by profile type:

- `machine/`: printer hardware profiles, such as `Creality Ender-3 Pro 0.4 nozzle - ED.json`
- `filament/`: material presets and tuned variants, such as `Creality CR-PETG (Ajustado V2).json`
- `process/`: print-process presets, such as `0.20mm Standard @Creality Ender3 Pro 0.4 - Custom.json`

Each profile is usually tracked as a `.json` file plus a matching `.info` sidecar. Keep pairs together and use the same base filename.

## Build, Test, and Development Commands
There is no build system in this repository. Treat changes as data updates and validate them before committing.

- `jq . filament/*.json machine/*.json process/*.json`
  Checks JSON syntax and pretty-prints files.
- `git diff -- filament/ machine/ process/`
  Reviews only profile changes before commit.
- `git status --short`
  Confirms both `.json` and `.info` files were added or updated together.

Import changed profiles into OrcaSlicer and verify they load cleanly before opening a pull request.

## Coding Style & Naming Conventions
Use the existing JSON style: 4-space indentation, quoted string values, and no trailing comments. Preserve current key ordering unless there is a clear reason to regroup related settings.

Name files after the profile shown in the `name` field. Keep filenames descriptive and aligned with existing patterns:

- machine: `Printer Model nozzle - Variant.json`
- filament: `Brand Material (Variant).json`
- process: `Layer Height @Printer - Variant.json`

## Testing Guidelines
There is no automated test suite or coverage target. Validation is manual:

- run `jq` against edited JSON files
- confirm `.info` metadata still matches the profile pair
- load the profile in OrcaSlicer and check inheritance, temperatures, nozzle settings, and support parameters

## Commit & Pull Request Guidelines
This repository currently has no commit history, so use a simple, consistent convention: short imperative subjects such as `Add PETG tuned filament profile` or `Adjust Ender-3 Pro retraction`.

Pull requests should include:

- a brief summary of what changed
- affected profile paths
- the printer, filament, or process scenario tested
- screenshots only if they clarify slicer settings or print results
