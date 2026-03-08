<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# smpl_mapper

## Purpose
This directory contains a focused static viewer for inspecting the aligned SMPL mesh and marker placements during manual mapping work.

## Key Files
| File | Description |
|------|-------------|
| `export_smpl_template_mesh.py` | Exports the template SMPL mesh used by this viewer. |
| `index.html` | Standalone SMPL-mapper viewer page. |
| `main.js` | Viewer runtime. |
| `smpl_frame0_aligned_mesh.json` | Aligned mesh rendered in this specialized viewer. |
| `smpl_markers_aligned.json` | Marker overlay data for the aligned mesh. |
| `smpl_template_mesh.json` | Template mesh asset. |
| `style.css` | Viewer styling. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Keep this viewer aligned with the mesh export format produced by the selection scripts.
- If you change JSON schema or naming, update both exporter and runtime loader together.

### Testing Requirements
- Serve the parent viewer directory and verify the SMPL mapper still renders the mesh and marker overlays.

### Common Patterns
- Standalone static viewer consuming pre-generated mesh JSON.

## Dependencies

### Internal
- `../` provides the main viewer context and shares the aligned mesh artifacts.
- `../../data/` provides the source SMPL model and alignment inputs.

### External
- Browser-side rendering and SMPL mesh data.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
