<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# web

## Purpose
This directory contains the static viewers used to inspect packaged OpenCap results and exported marker sets.

## Key Files
| File | Description |
|------|-------------|
| `webviz/index.html` | Main motion viewer page for OpenCap/OpenSim output. |
| `webviz/main.js` | Viewer bootstrap logic for motion playback. |
| `webviz_markerset/index.html` | Marker-set inspection page. |
| `webviz_markerset/export_osim_markerset_scene.py` | Exports OpenSim marker-set scenes for the marker viewer. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `webviz/` | Motion viewer assets and geometry (see `webviz/AGENTS.md`). |
| `webviz_markerset/` | Marker-set viewer assets and scene exporter (see `webviz_markerset/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep viewer assets plain and directly servable; there is no bundler or transpilation step.
- Geometry files under `Geometry/` are staged assets and usually should not be edited by hand.
- When scene file names change, update both the exporters and the HTML/JS loaders.

### Testing Requirements
- Serve `../` or this directory with `python -m http.server`.
- Verify both viewer entry points load without missing JSON or VTP assets.

### Common Patterns
- Static HTML/CSS/JS.
- Separate motion and marker-set viewers sharing the same geometry conventions.

## Dependencies

### Internal
- `../output/` provides the generated scenes and motion data.
- `../code/prepare_subject2_session0.py` stages the geometry assets used here.

### External
- Browser-based rendering plus OpenSim VTP geometry assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
