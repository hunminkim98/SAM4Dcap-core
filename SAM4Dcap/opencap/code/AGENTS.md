<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# code

## Purpose
This directory contains the executable scripts that stage a local OpenCap session and drive the actual `opencap-core` run.

## Key Files
| File | Description |
|------|-------------|
| `prepare_subject2_session0.py` | Copies and patches dataset files into a local session directory and stages geometry for web viewers. |
| `run_subject2_session0_dj1.py` | Wraps `opencap-core.main` for static and dynamic phases on the staged session. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Preserve command-line flags because the shell wrappers and docs depend on them.
- Keep the staging script compatible with OpenCap's expected folder names (`Videos`, `InputMedia`, `neutral`, and so on).
- When adjusting run phases, update both the code and the operational docs under `../../README.md` and `../../Readme_modified/`.

### Testing Requirements
- Run `python prepare_subject2_session0.py --help` or a real staging pass after interface changes.
- Run `python run_subject2_session0_dj1.py --phase static` and/or `--phase dj1` for targeted validation.

### Common Patterns
- `argparse`-driven wrappers around filesystem copy operations and `opencap-core`.
- Hardcoded defaults for subject, session, and environment roots.

## Dependencies

### Internal
- `../data/` is written by the prepare script.
- `../output/` is written by the run script.
- `../web/` consumes the staged geometry and generated scene files.

### External
- `yaml`, `shutil`, and the local `opencap-core` Python API.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
