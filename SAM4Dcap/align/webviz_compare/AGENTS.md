<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz_compare

## Purpose
This is a static viewer used to inspect the output of the `align/` step.

## Key Files
| File | Description |
|------|-------------|
| `data.json` | Pre-generated scene data rendered by the viewer. |
| `index.html` | Self-contained page for visual comparison. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Keep asset references relative so the folder can be served with a plain HTTP server.
- Prefer regenerating `data.json` from the alignment pipeline instead of manually rewriting coordinates.

### Testing Requirements
- Run `python -m http.server` inside this directory.
- Open the served page and verify the scene renders without missing assets.

### Common Patterns
- No build tooling.
- Data is loaded from checked-in JSON beside the HTML.

## Dependencies

### Internal
- `../generate_aligned_trc.py` produces the underlying alignment data visualized here.

### External
- Browser-only JavaScript and whichever visualization library is embedded in `index.html`.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
