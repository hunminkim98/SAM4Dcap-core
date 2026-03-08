<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz_markerset

## Purpose
This directory contains the static viewer and exporter used to inspect OpenSim marker-set placement on packaged OpenCap models.

## Key Files
| File | Description |
|------|-------------|
| `export_osim_markerset_scene.py` | Builds scene JSON from an OpenSim model for the marker-set viewer. |
| `index.html` | Marker-set viewer shell page. |
| `main.js` | Browser-side viewer logic for marker scenes. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim VTP meshes used by the marker-set viewer. |

## For AI Agents

### Working In This Directory
- Keep exporter output names stable or update the viewer loader in the same change.
- Geometry assets are copied from OpenSim; do not treat them as hand-maintained source.

### Testing Requirements
- Run `python export_osim_markerset_scene.py --help` or a real export after changing the exporter.
- Serve the directory and verify both markers and meshes render.

### Common Patterns
- Static viewer paired with a small scene-export script.

## Dependencies

### Internal
- `../../output/` provides the generated model artifacts used for exports.
- `../../code/prepare_subject2_session0.py` stages the geometry directory.

### External
- OpenSim model files and browser-side rendering.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
