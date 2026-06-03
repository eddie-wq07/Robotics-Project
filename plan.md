# Project Plan

## Repo Context

This repository is the **hardware foundation** for the project. It is a fork/copy of the open-source **SO-ARM100 / SO-101** robot arm design (originally by [RobotStudio](https://www.therobotstudio.com) in collaboration with Hugging Face / LeRobot).

For the MVP we are using **two of these robot arms** (leader + follower teleoperation setup, scaled to 4 arms total: 2 real + 2 follow). This entire repo — CAD, STL, STEP, simulation assets, and optional mounts — is what we work from for the duration of the project.

When we add the software layer later, it will live in a separate parent repo with this hardware folder included as a subdirectory. For now, this is the main repo.

### What's in here

| Path | Purpose |
|---|---|
| `README.md` | Full SO-101 build guide: BOM, sourcing links, kits, assembly. Primary reference. |
| `SO100.md` | Deprecated SO-100 docs (kept for reference). |
| `3DPRINT.md` | Print settings and material guidance for the 3D-printed parts. |
| `STL/` | Print-ready meshes — `SO100/`, `SO101/`, `Gauges/`. **Print from here.** |
| `STEP/` | Parametric CAD source (`SO100/`, `SO101/`) for modifying parts. |
| `Mini/` | Smaller variant of the arm. |
| `Optional/` | Add-ons: camera mounts (wrist + overhead, multiple webcam/RealSense variants), compliant gripper, raised base, 4040 mount, handles, springy trigger. |
| `Simulation/` | URDF / sim assets for SO100 and SO101 — useful once software layer is added. |
| `media/` | Reference images of the assembled arms. |
| `CHANGELOG.md`, `CITATION.cff`, `LICENSE` | Upstream project metadata. |

### Hardware decision for MVP
- Build target: **SO-101** (newer, easier assembly, improved wiring vs SO-100).
- Two arms: one leader (teleop) + one follower (actuated) — print files in `STL/SO101/`.
- Motors: STS3215 servos, 7.4V variants (see README BOM).

---

## MVP Concept — June 20th

- Two robot arms, no code, just hardware. Attached to main body.
- Able to replicate movement from the two leader arms. 4 arms total (2 real, 2 follow).
- Able to hard-code movements.

---

## Phases

### Phase 0 — June 2 → June 4
- ✔️ Finalize CAD file (ideally copy from upstream — using SO-101 from this repo)
- ✔️ Ready to 3D print real arm + fake arms (files in `STL/SO101/`)
- ⏳ Buy parts (BOM in `README.md`)

### Phase 1 — June 4 → June 8
- Receive parts
- Robot arms fully built

### Phase 2 — June 9 → June 18
- Attach arms to main body PVC
- Complete full computer vision → LLM → robot output logic
- Learn to sort coloured paper

**Complete**

---

## Meeting Notes

### June 2nd
Next steps (in order):
- ✔️ Pinpoint CAD file we want to use (SO-101, this repo)
- ⏳ Pinpoint 3D printer availability
- ⏳ Order parts

---

## Costs Breakdown

| Item | Est. Cost |
|---|---|
| Motors (STS3215 servos, per README BOM) | ~$500 |
| Microcontroller (MCU) | $20 |
| Webcam | $40 |
| 3D Printing | $30 |
| PVC pipes (body) | $30 |
| Shirt | Free |
