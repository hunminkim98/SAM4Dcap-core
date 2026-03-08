<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# SAM4Dcap

## Purpose
This directory is the main experiment workspace. It contains the one-click entry scripts, the alignment helpers, the OpenCap-based reproduction path, the AddBiomechanics path, the 43-marker OpenCap path, and the interactive marker-selection tooling.

## Key Files
| File | Description |
|------|-------------|
| `opencap.sh` | Runs the packaged OpenCap reproduction flow and serves the bundled viewer. |
| `pipeline1.sh` | End-to-end AddBiomechanics workflow for the 105-marker monocular path. |
| `pipeline2.sh` | End-to-end OpenCap/OpenSim workflow for the 43-marker monocular path. |
| `select.sh` | Serves the manual marker-selection viewer. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `align/` | Alignment utilities for the 105-marker/AddBiomechanics path (see `align/AGENTS.md`). |
| `align_43marks/` | Alignment utilities for the 43-marker/OpenCap path (see `align_43marks/AGENTS.md`). |
| `opencap/` | Local OpenCap-style session staging, generated outputs, and web viewers (see `opencap/AGENTS.md`). |
| `opencap_clean/` | Cleaner OpenCap bundle without the checked-in output tree (see `opencap_clean/AGENTS.md`). |
| `output_viz/` | Static output bundle for sharing pipeline2 visualization results (see `output_viz/AGENTS.md`). |
| `pipeline1/` | AddBiomechanics-oriented monocular pipeline workspace (see `pipeline1/AGENTS.md`). |
| `pipeline2/` | OpenCap/OpenSim-oriented monocular pipeline workspace (see `pipeline2/AGENTS.md`). |
| `select/` | Manual marker-mapping and inspection tooling (see `select/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Entry scripts are path-sensitive wrappers; keep them synchronized with the subdirectory scripts they call.
- Generated media, JSON, TRC, MOT, and mesh assets live beside source code. Avoid broad file operations.
- If you need to generalize these workflows, document the new assumptions because most current scripts are subject- and session-specific.

### Testing Requirements
- For shell-script changes, rerun only the affected stage rather than the entire repo.
- For viewer changes, serve the target directory locally and verify that the expected JSON and geometry assets resolve.

### Common Patterns
- Bash entry points activate different conda environments for each stage.
- Python scripts frequently use absolute `/root/TVB/...` paths.
- Visualization directories are static assets, not framework builds.

## Dependencies

### Internal
- `../MHRtoSMPL/` is part of both pipeline1 and pipeline2.
- All subdirectories here feed one another through generated TRC, JSON, model, and mesh artifacts.

### External
- `sam-body4d`, `opencap-core`, OpenSim, AddBiomechanics, and SMPL assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
