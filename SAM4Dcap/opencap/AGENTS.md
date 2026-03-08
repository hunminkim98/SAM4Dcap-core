<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# opencap

## Purpose
This directory packages a local OpenCap-style reproduction path, including dataset staging code, checked-in session data, generated outputs, and static viewers for both motion and marker-set inspection.

## Key Files
| File | Description |
|------|-------------|
| `code/prepare_subject2_session0.py` | Copies LabValidation assets into the local OpenCap session layout. |
| `code/run_subject2_session0_dj1.py` | Runs the staged static/DJ1 OpenCap workflow through `opencap-core`. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `code/` | Executable session-preparation and run scripts (see `code/AGENTS.md`). |
| `data/` | Local input session tree mirroring the structure expected by OpenCap (see `data/AGENTS.md`). |
| `output/` | Generated results emitted by the OpenCap run (see `output/AGENTS.md`). |
| `web/` | Static viewers and exported scenes for inspecting the output (see `web/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- This tree intentionally mixes source and generated data; inspect paths carefully before editing.
- Most scripts assume `opencap-core` is available at `/root/TVB/opencap-core`.
- Prefer changing the staging or export scripts over manually rewriting files under `data/` or `output/`.

### Testing Requirements
- Run the prepare script before rerunning the workflow if you change the data layout.
- After pipeline changes, smoke-test both the motion viewer and the marker-set viewer under `web/`.

### Common Patterns
- Session-specific wrappers around `opencap-core`.
- Generated output tree mirrors the OpenCap folder layout.
- Static viewers consume JSON and VTP geometry without a build system.

## Dependencies

### Internal
- `../opencap_clean/` is a leaner sibling with the same execution model.
- `../pipeline2/` borrows the same OpenSim/OpenCap concepts and some of the same assets.

### External
- `opencap-core`, OpenSim geometry assets, LabValidation data, and MMpose/OpenCap dependencies.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
