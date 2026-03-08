<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# data

## Purpose
This directory stores the input assets and intermediate files that drive the manual marker-selection workflow.

## Key Files
| File | Description |
|------|-------------|
| `SMPL_NEUTRAL_chumpy_free.pkl` | SMPL model used by the selection/alignment scripts. |
| `bsm_markers.yaml` | BSM marker vertex index definitions. |
| `manual_picks_new.json` | Saved manual vertex picks from the selection workflow. |
| `mapping_43_bsm105_smpl24.csv` | Baseline mapping between OpenCap markers and SMPL/BSM points. |
| `updated_mapping.csv` | Regenerated mapping with manual replacements and symmetry applied. |
| `sym_idxs.npy` | Symmetry lookup table used to mirror manually selected vertices. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `smpl_results/` | Frame-level SMPL outputs used as inputs to alignment and marker-placement scripts. |

## For AI Agents

### Working In This Directory
- Preserve consistency between YAML, CSV, JSON, and `.npy` mapping assets.
- Prefer regenerating `updated_mapping.csv` from the exporter script instead of hand-editing it.
- Large binary/model assets should usually be left untouched.

### Testing Requirements
- After mapping changes, rerun the affected exporter/build scripts and then reload the viewer.
- Confirm that manual pick notes still resolve to valid vertices and mirrored counterparts.

### Common Patterns
- Small data files used as canonical inputs for downstream scene generation.

## Dependencies

### Internal
- Read by the scripts in `../`.
- Exported scene files land in `../viewer/`.

### External
- SMPL model assets and NumPy/YAML parsers.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
