<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# viewer

## Purpose
This directory contains the static UI used to inspect aligned SMPL meshes, marker comparisons, and mapping overlays for the manual selection workflow.

## Key Files
| File | Description |
|------|-------------|
| `export_osim_markerset_scene.py` | Exports OpenSim marker scenes for comparison in the viewer. |
| `export_static_frame_scene.py` | Builds the base scene for the static frame used during selection. |
| `index.html` | Main viewer page for marker and mesh inspection. |
| `main.js` | Viewer runtime logic. |
| `smpl_frame0_aligned_mesh.json` | Current aligned SMPL mesh rendered in the viewer. |
| `scene_updated_mapping_overlay.json` | Current overlay scene rebuilt from the updated mapping. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | OpenSim mesh assets used by the viewer. |
| `smpl_mapper/` | Secondary static viewer focused on raw SMPL mesh inspection (see `smpl_mapper/AGENTS.md`). |

## For AI Agents

### Working In This Directory
- Keep generated scene names synchronized with the Python exporters and the JS loader.
- Treat `Geometry/` and generated JSON meshes/scenes as derived assets unless you are explicitly fixing viewer output.
- If you add a new inspection scene, document how it is produced from the scripts in `../`.

### Testing Requirements
- Serve the directory via `python -m http.server` or `../select.sh`.
- Verify the viewer loads the aligned mesh, comparison scenes, and mapping overlay without missing assets.

### Common Patterns
- Static HTML/CSS/JS with multiple pre-generated scene JSON files.

## Dependencies

### Internal
- `../data/` provides the mapping assets and SMPL inputs.
- Scripts in `../` regenerate most of the JSON files hosted here.

### External
- Browser-side rendering and OpenSim VTP geometry.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
