<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# webviz_compare

## Purpose
This directory serves the static viewer for the 43-marker alignment workflow.

## Key Files
| File | Description |
|------|-------------|
| `index.html` | Comparison page for manually checking 43-marker alignment results. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `-` | No tracked subdirectories. |

## For AI Agents

### Working In This Directory
- Keep the viewer dependency-free and directly servable with `python -m http.server`.
- Reference generated alignment outputs using relative paths only.

### Testing Requirements
- Serve the directory locally and verify the page loads without console errors.

### Common Patterns
- Single-file static viewer.

## Dependencies

### Internal
- `../generate_aligned_trc_43.py` and related mapping files supply the scene data shown here.

### External
- Browser-only JavaScript.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
