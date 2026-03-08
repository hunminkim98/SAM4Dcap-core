<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# output

## Purpose
This directory contains generated results from the packaged OpenCap reproduction run, including TRC files, IK outputs, scaled models, visualizer JSON, and copied media.

## Key Files
| File | Description |
|------|-------------|
| `Data/subject2_Session0/sessionMetadata.yaml` | Generated session metadata for the staged output copy. |
| `Data/subject2_Session0/MarkerData/mmpose_0.8/2-cameras/PostAugmentation_v0.2/static1_LSTM.trc` | Example augmented marker output from the static phase. |
| `Data/subject2_Session0/OpenSimData/mmpose_0.8/2-cameras/Model/LaiUhlrich2022_scaled.osim` | Example scaled OpenSim model emitted by the workflow. |
| `Data/subject2_Session0/VisualizerJsons/DJ1/` | Visualizer scenes used by the web viewer. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Data/` | Session-scoped OpenCap output tree mirroring the structure emitted by `opencap-core`. |

## For AI Agents

### Working In This Directory
- Treat everything here as generated output.
- If a file under `output/` is wrong, fix the code or inputs upstream and rerun the pipeline instead of hand-editing the artifact.
- Be cautious with large binary assets and copied videos.

### Testing Requirements
- After workflow changes, verify that expected TRC, MOT, `.osim`, and visualizer JSON files are regenerated.
- Smoke-test the corresponding web viewers under `../web/`.

### Common Patterns
- OpenCap output naming conventions.
- Deeply nested folders keyed by subject, session, pose detector, and camera setup.

## Dependencies

### Internal
- Written by `../code/run_subject2_session0_dj1.py`.
- Consumed by `../web/webviz/` and `../web/webviz_markerset/`.

### External
- `opencap-core` and OpenSim output generators.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
