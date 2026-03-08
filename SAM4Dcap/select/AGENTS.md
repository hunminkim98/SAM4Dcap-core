<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# select

## Purpose
This directory contains the manual marker-selection and mapping workflow used to align SMPL mesh vertices with the OpenCap 43-marker set and generate viewer-ready comparison scenes.

## Key Files
| File | Description |
|------|-------------|
| `add_adjusted_markers.py` | Adds adjusted thigh/shank markers by searching SMPL vertices and mirroring them. |
| `align_smpl_to_markers.py` | Performs the one-shot Procrustes alignment between SMPL outputs and OpenCap markers. |
| `build_scene_updated_mapping.py` | Rebuilds the overlay scene from the current mapping CSV. |
| `export_mapping_csv.py` | Exports the updated manual/symmetric marker mapping into CSV form. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `data/` | Mapping inputs, SMPL assets, and intermediate scene files (see `data/AGENTS.md`). |
| `viewer/` | Static review UI plus exported scenes and aligned mesh assets (see `viewer/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep marker names synchronized across Python scripts, CSV/YAML mapping files, and viewer scene JSON.
- Most scripts assume absolute roots under `/root/TVB/SAM4Dcap/select`; update callers if you generalize them.
- When adjusting manual picks, regenerate downstream CSV/scene artifacts rather than editing all files independently.

### Testing Requirements
- Run the smallest affected script and then reload the viewer served by `../select.sh`.
- Verify that generated scene JSON still loads and marker colors/labels match expectations.

### Common Patterns
- Geometry alignment through Procrustes and symmetry tables.
- Static viewer assets paired with generated JSON scene files.

## Dependencies

### Internal
- `../align_43marks/` and `../pipeline2/` share the same 43-marker semantics.
- `../../MHRtoSMPL/` provides the SMPL assets used by the alignment scripts.

### External
- `smplx`, `torch`, `numpy`, `yaml`, and browser-side rendering for the viewer.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
