<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# align

## Purpose
This directory contains the alignment step used by the 105-marker/AddBiomechanics workflow. It generates an aligned TRC file from pipeline1 outputs and includes a simple comparison viewer.

## Key Files
| File | Description |
|------|-------------|
| `README.md` | Minimal instructions for running the alignment script and viewer. |
| `generate_aligned_trc.py` | Produces the aligned TRC consumed later by pipeline1/OpenSim tooling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `webviz_compare/` | Static alignment-comparison viewer bundle (see `webviz_compare/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep output names and locations aligned with what `../pipeline1.sh` expects.
- Do not hand-edit generated TRC data unless you are explicitly debugging a single artifact.

### Testing Requirements
- Run `python generate_aligned_trc.py`.
- Serve `webviz_compare/` with `python -m http.server` and confirm the comparison scene loads.

### Common Patterns
- Single-purpose geometry scripts.
- Static HTML viewer with checked-in JSON data.

## Dependencies

### Internal
- `../pipeline1/` provides the SMPL and motion data consumed here.
- `../../MHRtoSMPL/` supplies the earlier conversion stage in the same workflow.

### External
- NumPy/SciPy-style geometry tooling and the local AddBiomechanics/OpenSim stack.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
