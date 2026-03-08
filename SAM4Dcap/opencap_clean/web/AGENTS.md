<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# web

## Purpose
This directory holds the clean-workflow static viewers for motion and marker-set inspection.

## Key Files
| File | Description |
|------|-------------|
| `webviz/index.html` | Motion-viewer entry point. |
| `webviz_markerset/export_osim_markerset_scene.py` | Marker-set scene exporter for the clean workflow. |
| `webviz_markerset/index.html` | Marker-set viewer entry point. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `webviz/` | Motion viewer assets (see `webviz/AGENTS.md`). |
| `webviz_markerset/` | Marker-set viewer assets and exporter (see `webviz_markerset/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep this viewer stack aligned with `../../opencap/web/` unless there is a reason to split behavior.
- Use relative file references so `python -m http.server` works from the directory root.

### Testing Requirements
- Serve the directory and verify both viewer entry points load successfully.

### Common Patterns
- Static HTML/CSS/JS plus copied OpenSim geometry.

## Dependencies

### Internal
- Consumes assets staged by `../code/prepare_subject2_session0.py`.

### External
- Browser rendering plus OpenSim geometry/model assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
