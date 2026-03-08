<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz

## Purpose
This directory contains the local static viewer for live pipeline2 results.

## Key Files
| File | Description |
|------|-------------|
| `index.html` | Viewer shell page. |
| `main.js` | Runtime loader for the pipeline2 motion scene. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim mesh assets used by the viewer. |

## For AI Agents

### Working In This Directory
- Keep paths relative and aligned with `../vis/`.
- Geometry assets are copied dependencies; change them only if scene references and upstream staging are handled too.

### Testing Requirements
- Serve `../` or this directory and confirm the viewer loads the latest exported motion JSON and meshes.

### Common Patterns
- Static viewer shell around generated motion data.

## Dependencies

### Internal
- `../run_vis.py` generates the JSON consumed by the viewer.

### External
- Browser-side rendering plus OpenSim mesh assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
