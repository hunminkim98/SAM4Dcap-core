<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# align_43marks

## Purpose
This directory holds the 43-marker alignment logic used by the OpenCap/OpenSim branch of the project. It packages the marker definitions, model references, and comparison viewer for the pipeline2 path.

## Key Files
| File | Description |
|------|-------------|
| `README.md` | Minimal run instructions for the 43-marker alignment flow. |
| `generate_aligned_trc_43.py` | Generates an aligned 43-marker TRC for inspection or downstream use. |
| `generate_aligned_trc_43_to_pipeline2.py` | Adapts the 43-marker alignment output into the pipeline2 workspace. |
| `markers_lai_43.yaml` | Marker-index mapping for the LaiUhlrich 43-marker setup. |
| `updated_mapping.csv` | Manual/derived mapping updates used by the alignment flow. |
| `LaiUhlrich2022.osim` | OpenSim model reference for the 43-marker path. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `webviz_compare/` | Static viewer for inspecting 43-marker alignment output (see `webviz_compare/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep the YAML/CSV marker definitions synchronized with `../pipeline2/` and `../select/` when changing marker names or indices.
- Model file names here are consumed by scripts; renaming them without updating callers will break the pipeline.

### Testing Requirements
- Run the relevant generator script and inspect the emitted TRC or copied pipeline2 artifact.
- Serve `webviz_compare/` to visually verify marker placement after mapping changes.

### Common Patterns
- Mapping-heavy scripts with absolute paths into the packaged repo.
- Static comparison viewer for manual QA.

## Dependencies

### Internal
- `../pipeline2/` consumes the aligned 43-marker outputs.
- `../select/` shares the same mapping concepts and manual marker adjustments.

### External
- OpenSim model assets and local scientific Python tooling.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
