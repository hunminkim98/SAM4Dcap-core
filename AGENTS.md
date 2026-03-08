<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# SAM4Dcap-core

## Purpose
This repository packages the local glue code, run scripts, sample assets, and derived data used to reproduce SAM4Dcap experiments. It bridges external projects such as sam-body4d, MHR, OpenCap, OpenSim, and AddBiomechanics through a set of path-sensitive scripts and static viewers.

## Key Files
| File | Description |
|------|-------------|
| `README.md` | Main project overview, setup notes, and one-click workflow entry points. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `MHRtoSMPL/` | MHR-to-SMPL conversion helpers and rendering utilities (see `MHRtoSMPL/AGENTS.md`). |
| `Readme_modified/` | Notes describing local changes made in upstream dependencies (see `Readme_modified/AGENTS.md`). |
| `SAM4Dcap/` | Main experiment workspace containing alignment, OpenCap, pipeline, and selection tooling (see `SAM4Dcap/AGENTS.md`). |
| `example/` | Example image and video artifacts used in the root README (see `example/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Most scripts assume the full project is mounted at `/root/TVB`; avoid changing path conventions without updating all entry points.
- Source code and generated artifacts are mixed together. Prefer adding new files or regenerating outputs instead of rewriting derived data in place.
- The git worktree is often intentionally dirty because it mirrors multiple upstream projects; do not revert unrelated modifications.

### Testing Requirements
- There is no single automated test suite at the repo root.
- Validate changes by rerunning the affected pipeline script and, when applicable, serving the corresponding static viewer with `python -m http.server`.

### Common Patterns
- Bash wrappers activate a specific conda environment before invoking Python.
- Python scripts frequently hardcode upstream repo locations and model paths.
- Static visualization folders are plain HTML/CSS/JS with pre-generated JSON/VTP assets and no build step.

## Dependencies

### Internal
- `SAM4Dcap/` holds the end-to-end workflows and generated experiment outputs.
- `MHRtoSMPL/` supplies SMPL conversion utilities consumed by the pipeline scripts.
- `Readme_modified/` captures local upstream modifications that explain many absolute-path assumptions.

### External
- `sam-body4d` for monocular 4D body reconstruction.
- Meta MHR tooling for momentum-human-rig outputs.
- `opencap-core` and OpenSim for scaling, IK, and visualization export.
- AddBiomechanics and SMPL/SMPL-X assets for alternate biomechanical pipelines.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
