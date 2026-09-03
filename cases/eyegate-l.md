# EyeGate-L

**University prototype of a two-door access-control / mantrap system for Luckfox-class edge hardware.**

Repository: [ShapArt/eyegate-l-luckfox-scud](https://github.com/ShapArt/eyegate-l-luckfox-scud)

## Context

The project combines computer vision with a physical access-control sequence. That makes the system boundary more important than a face-recognition demo alone: camera input, recognition, access policy and the state of two doors should not collapse into one handler.

## Built

The repository currently has separate layers for:

- camera ingest;
- OpenCV-based vision services, embeddings/matching and people counting;
- access policy;
- a gate controller and dedicated finite-state machine;
- serial/hardware-facing integration;
- FastAPI API and WebSocket status updates;
- authentication, token handling and rate limiting;
- React + TypeScript + Vite web UI.

The central separation is deliberate:

```text
camera → vision result → policy / decision → gate FSM → hardware action
```

Recognition output does not directly become a door command.

## Current state

EyeGate-L is a **prototype / educational system**, not production physical-security equipment. The repo includes tests, QA/checklist material, hardware/deployment notes and Luckfox-specific pieces, but it should be evaluated as an engineering prototype.

## Constraints

- Real biometric/access-control assurance requires far more validation than the repository claims.
- Hardware and camera behaviour are environment-specific.
- The project is intentionally edge/local-oriented, so deployment constraints are part of the system rather than abstracted away.

## Evidence

- [Project README](https://github.com/ShapArt/eyegate-l-luckfox-scud)
- [`server/main.py`](https://github.com/ShapArt/eyegate-l-luckfox-scud/blob/main/server/main.py)
- [`gate/`](https://github.com/ShapArt/eyegate-l-luckfox-scud/tree/main/gate)
- [`vision/`](https://github.com/ShapArt/eyegate-l-luckfox-scud/tree/main/vision)
- [`web/app/`](https://github.com/ShapArt/eyegate-l-luckfox-scud/tree/main/web/app)
