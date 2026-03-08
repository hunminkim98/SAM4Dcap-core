<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# code

## Purpose
This directory contains the clean-workflow equivalents of the OpenCap staging and run scripts.

## Key Files
| File | Description |
|------|-------------|
| `prepare_subject2_session0.py` | Creates the clean local OpenCap input tree and stages geometry. |
| `run_subject2_session0_dj1.py` | Invokes `opencap-core` for the clean workflow's static and DJ1 phases. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Keep CLI behavior aligned with `../../opencap/code/` unless you are intentionally maintaining a fork.
- Hardcoded defaults still point at `/root/TVB`; document any new path assumptions.

### Testing Requirements
- Run the prepare script and then a targeted `--phase` execution after editing either file.

### Common Patterns
- Thin `argparse` wrappers over filesystem staging and `opencap-core`.

## Dependencies

### Internal
- Writes to `../data/` and feeds `../web/`.

### External
- `yaml`, `shutil`, and the local `opencap-core` installation.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
