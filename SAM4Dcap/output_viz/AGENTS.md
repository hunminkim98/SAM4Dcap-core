<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# output_viz

## Purpose
This directory packages a shareable, static visualization bundle for the pipeline2/OpenCap-style results.

## Key Files
| File | Description |
|------|-------------|
| `web.txt` | Small note about serving the visualization bundle. |
| `vis/subject2_43markers_aligned.json` | Generated visualizer JSON used by the static web bundle. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `vis/` | Generated motion scene data referenced by the static viewer. |
| `webviz_pipeline2/` | Static viewer bundle for the packaged pipeline2 output (see `webviz_pipeline2/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Treat `vis/` as generated data and `webviz_pipeline2/` as the runtime viewer shell.
- Prefer updating `../pipeline2/run_vis.py` and regenerating assets instead of editing scene JSON manually.

### Testing Requirements
- Serve the directory with `python -m http.server` and verify `webviz_pipeline2/` loads the packaged scene.

### Common Patterns
- Portable static bundle copied out of the live pipeline workspace.

## Dependencies

### Internal
- `../pipeline2/` generates the source motion and viewer assets for this bundle.

### External
- Browser-side rendering and OpenSim VTP geometry assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
