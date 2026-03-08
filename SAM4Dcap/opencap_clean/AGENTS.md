<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# opencap_clean

## Purpose
This directory is a leaner OpenCap bundle used by `opencap.sh`. It keeps the execution scripts and viewer assets without checking in the large generated output tree that exists under `../opencap/`.

## Key Files
| File | Description |
|------|-------------|
| `code/prepare_subject2_session0.py` | Stages local subject/session data for the clean OpenCap workflow. |
| `code/run_subject2_session0_dj1.py` | Executes the packaged clean OpenCap run phases. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `code/` | Clean workflow staging and run scripts (see `code/AGENTS.md`). |
| `data/` | Input session tree for the clean workflow (see `data/AGENTS.md`). |
| `web/` | Static viewers for the clean workflow (see `web/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep behavior aligned with `../opencap/` unless there is a deliberate reason to diverge.
- This tree is the one called directly by `../opencap.sh`, so interface changes here need script and doc updates.

### Testing Requirements
- Run the clean workflow shell entry point or at least the Python wrappers after changes.
- Serve the viewer assets locally and verify exported scenes still load.

### Common Patterns
- Mirrors the structure of `../opencap/` but omits the checked-in output tree.

## Dependencies

### Internal
- `../opencap/` is the fuller sibling containing generated outputs and a similar viewer stack.

### External
- `opencap-core`, OpenSim geometry assets, and the local dataset source.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
