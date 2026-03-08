<!-- Parent: ../AGENTS.md -->
<!-- Generated: 2026-03-08 11:44:52 +0900 | Updated: 2026-03-08 11:44:52 +0900 -->

# pipeline1

## Purpose
This directory is the AddBiomechanics-oriented monocular workflow workspace. It collects raw video, geometry assets, intermediate SMPL outputs, and the final files consumed by the local AddBiomechanics frontend preview.

## Key Files
| File | Description |
|------|-------------|
| `_subject.json` | Subject metadata/configuration used by downstream AddBiomechanics tooling. |
| `merge_to_smpl2ab.py` | Merges per-frame SMPL outputs into a single motion archive. |
| `subject2_DJ1_s0_cam1.mp4` | Example input video for the monocular run. |

## Subdirectories
| Directory | Purpose |
|-----------|---------|
| `Geometry/` | Large set of OpenSim/AddBiomechanics mesh assets copied into the pipeline workspace. |

## For AI Agents

### Working In This Directory
- This directory is mostly a working area for `../pipeline1.sh`; many files here are generated or copied assets.
- If pipeline structure changes, update `../align/` and the shell wrapper together.
- Avoid editing the copied geometry files directly unless you are debugging mesh resolution issues.

### Testing Requirements
- Run the relevant segment of `../pipeline1.sh` or `python merge_to_smpl2ab.py` for targeted validation.
- If the AddBiomechanics preview is part of the change, verify the local frontend can still read the produced `preview.bin`/trial tree.

### Common Patterns
- Mixed source scripts and derived pipeline artifacts.
- AddBiomechanics-compatible trial directory layout created by shell orchestration.

## Dependencies

### Internal
- `../align/` consumes outputs from this workspace.
- `../../MHRtoSMPL/` provides the SMPL conversion stage used before this directory is populated.

### External
- `sam-body4d`, MHR conversion tooling, AddBiomechanics, and OpenSim geometry assets.

<!-- MANUAL: Any manually added notes below this line are preserved on regeneration -->
