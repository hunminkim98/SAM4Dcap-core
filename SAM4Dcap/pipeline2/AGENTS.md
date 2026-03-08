<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# pipeline2

## Purpose
This directory is the 43-marker monocular OpenCap/OpenSim workflow workspace. It prepares aligned TRC files, runs scaling and IK, exports viewer JSON, and serves a local static viewer.

## Key Files
| File | Description |
|------|-------------|
| `run_prepare_trc.py` | Full monocular preprocessing stage: body4d, MHR-to-SMPL, alignment, and TRC writing. |
| `run_scale.py` | Scales the OpenSim model from the generated static TRC. |
| `run_ik.py` | Runs inverse kinematics on the generated dynamic TRC. |
| `run_vis.py` | Exports visualizer JSON from the IK result. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `webviz/` | Static viewer assets for the pipeline2 result (see `webviz/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- `run_prepare_trc.py` encodes many absolute paths, fixed interpreters, and session-specific assumptions; refactor carefully.
- The pipeline writes into subfolders such as `motion/`, `static/`, `scaling_out/`, `ik_out/`, and `vis/`; treat those as generated artifacts.
- Keep the scale, IK, and viewer-export scripts synchronized on output filenames.

### Testing Requirements
- Run the smallest affected stage (`run_scale.py`, `run_ik.py`, or `run_vis.py`) when possible.
- For preprocessing changes, rerun `run_prepare_trc.py` on a representative clip.
- Serve `webviz/` and confirm the updated output still visualizes correctly.

### Common Patterns
- Sequential pipeline scripts with file handoff through well-known names.
- Reliance on `opencap-core` utility functions for OpenSim operations.

## Dependencies

### Internal
- `../align_43marks/` and `../opencap/` provide related marker definitions and reference assets.
- `../../MHRtoSMPL/` participates in the preprocessing stage.

### External
- `sam-body4d`, MHR tooling, OpenSim, `opencap-core`, `smplx`, `torch`, `yaml`, and `scipy`.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
