<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# data

## Purpose
This directory stores the staged OpenCap input data used for the packaged subject/session reproduction workflow.

## Key Files
| File | Description |
|------|-------------|
| `subject2/Session0/sessionMetadata.yaml` | Session metadata copied and patched for the local OpenCap run. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `subject2/` | Subject-scoped session tree containing `Session0` videos, calibration, and metadata. |

## For AI Agents

### Working In This Directory
- Treat this directory as staged input data, not primary source code.
- If the layout changes, make the change in `../code/prepare_subject2_session0.py` and regenerate this tree.
- Avoid manual edits inside per-camera `InputMedia` folders unless debugging a specific artifact.

### Testing Requirements
- After staging changes, confirm `sessionMetadata.yaml` and expected video/calibration files are recreated in the right locations.

### Common Patterns
- OpenCap-compatible `subject/session/Videos/Cam*/InputMedia/...` structure.
- Mixed YAML, pickle, and video assets copied from an external dataset.

## Dependencies

### Internal
- Written by `../code/prepare_subject2_session0.py`.
- Read by `../code/run_subject2_session0_dj1.py`.

### External
- LabValidation dataset files and OpenCap session-layout expectations.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
