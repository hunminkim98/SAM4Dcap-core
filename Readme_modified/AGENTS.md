<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# Readme_modified

## Purpose
This directory stores hand-maintained notes about local changes applied to upstream projects, plus path and checkpoint references needed to run the full SAM4Dcap workflow.

## Key Files
| File | Description |
|------|-------------|
| `README.md` | Summary of uncommitted or local-only changes across integrated upstream repositories. |
| `check_again.txt` | Pre-run checklist for paths and environment assumptions. |
| `checkpoints.txt` | Reference list for model checkpoint locations. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Update these notes whenever a script starts depending on a new external repo path, environment name, or model checkpoint.
- Treat this directory as operational documentation, not source code.

### Testing Requirements
- Cross-check that referenced paths still match the runnable scripts after any edits.
- When updating checkpoint notes, verify that the corresponding model-loading scripts still resolve correctly.

### Common Patterns
- Human-readable inventory files rather than executable tooling.
- Cross-references into external repos under `/root/TVB`.

## Dependencies

### Internal
- `../README.md` points users here for details about local modifications.
- `../SAM4Dcap/` scripts depend on the path and checkpoint assumptions documented here.

### External
- The local clones of AddBiomechanics, MHR, SMPL2AddBiomechanics, `opencap-core`, and `sam-body4d`.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
