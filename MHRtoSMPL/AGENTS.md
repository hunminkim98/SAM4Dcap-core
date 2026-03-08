<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# MHRtoSMPL

## Purpose
This directory contains the local utilities used to convert Meta MHR outputs into SMPL parameters and meshes, plus small rendering helpers used for sanity checks.

## Key Files
| File | Description |
|------|-------------|
| `README.md` | Environment setup notes and caveats for the MHR-to-SMPL conversion flow. |
| `convert_mhr_to_smpl.py` | Main converter that optimizes SMPL parameters from per-frame MHR outputs. |
| `convert_smpl_chumpy_free.py` | Converts an original SMPL pickle into a chumpy-free model artifact. |
| `render_smpl.py` | Renders converted SMPL outputs for visual inspection. |
| `render_smpl_test.py` | Lightweight rendering test harness. |
| `SMPL_NEUTRAL.pkl` | Source SMPL model asset used by the conversion utilities. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories in this packaged copy. |

## For AI Agents

### Working In This Directory
- `convert_mhr_to_smpl.py` is meant to run from the upstream MHR `tools/mhr_smpl_conversion` directory because it relies on relative asset loading there.
- Keep the documented import ordering constraint (`pymomentum` before `torch`) intact when editing the converter.
- Treat model pickle files as large binary assets; add scripts or notes around them rather than editing them directly.

### Testing Requirements
- Run the converter on a small frame directory and verify that `.npz` outputs are produced.
- Use `render_smpl.py` or `render_smpl_test.py` for a visual smoke test after conversion changes.

### Common Patterns
- Per-frame `.npz` input/output conventions.
- Hardcoded environment and model paths.
- Geometry validation through simple render scripts instead of formal tests.

## Dependencies

### Internal
- `../SAM4Dcap/pipeline1/` and `../SAM4Dcap/pipeline2/` call into this directory during end-to-end runs.

### External
- `pymomentum-cpu` and the upstream MHR conversion code.
- `smplx`, `torch`, `numpy`, and `tqdm`.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
