<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz_markerset

## Purpose
This directory contains the clean OpenCap marker-set viewer and its scene exporter.

## Key Files
| File | Description |
|------|-------------|
| `export_osim_markerset_scene.py` | Exports a marker-set scene from an OpenSim model. |
| `index.html` | Marker-set viewer page. |
| `main.js` | Viewer runtime for marker scenes. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim mesh assets used by the viewer. |

## For AI Agents

### Working In This Directory
- Keep exporter output names and viewer loader assumptions in sync.
- Geometry files are staged assets copied from OpenSim and should rarely be edited.

### Testing Requirements
- Run the exporter after changes and then load the viewer via a local HTTP server.

### Common Patterns
- Small Python export helper plus static viewer files.

## Dependencies

### Internal
- Relies on model outputs and staged geometry from the clean OpenCap workflow.

### External
- OpenSim model assets and browser-side rendering.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
