<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz_pipeline2

## Purpose
This directory is the static viewer shell for the packaged pipeline2 visualization bundle.

## Key Files
| File | Description |
|------|-------------|
| `index.html` | Pipeline2 viewer entry page. |
| `main.js` | Loads the packaged motion JSON and geometry. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim mesh assets bundled with the viewer. |

## For AI Agents

### Working In This Directory
- Keep all asset paths relative so the bundle can be copied and served from anywhere.
- Avoid editing geometry assets directly; regenerate or restage them from the source pipeline when possible.

### Testing Requirements
- Serve `../` or this directory and verify the viewer loads the packaged motion scene and meshes.

### Common Patterns
- Self-contained static viewer with adjacent generated assets.

## Dependencies

### Internal
- `../vis/subject2_43markers_aligned.json` supplies the packaged motion scene.

### External
- Browser-side rendering and OpenSim VTP mesh assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
