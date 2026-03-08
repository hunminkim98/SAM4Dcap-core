<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz

## Purpose
This directory contains the static viewer for replaying packaged OpenCap/OpenSim motion output.

## Key Files
| File | Description |
|------|-------------|
| `index.html` | Motion-viewer shell page. |
| `main.js` | Loads motion scene data and hooks up the browser-side renderer. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim VTP meshes used by the viewer; these are staged assets, not authored source. |

## For AI Agents

### Working In This Directory
- Keep file paths relative so the viewer works when served from the folder root.
- Avoid renaming geometry files unless you also update all scene JSON references.

### Testing Requirements
- Serve the parent `web/` directory and confirm the motion viewer loads meshes and animation data.

### Common Patterns
- Static site with adjacent geometry assets.
- Scene JSON generated elsewhere and consumed at runtime.

## Dependencies

### Internal
- `../../output/` provides the visualizer JSON referenced by the viewer.

### External
- Browser rendering stack plus OpenSim mesh assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
