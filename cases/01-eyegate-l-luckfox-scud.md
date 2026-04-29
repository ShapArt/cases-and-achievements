# Case Study 01 — EyeGate-L / Luckfox SCUD

Computer vision and access-control prototype for constrained edge hardware.

## Problem

Access-control systems are a good engineering problem because they combine several difficult constraints at once:

- identity verification;
- local hardware limits;
- real-time or near-real-time response;
- secure storage of sensitive data;
- integration with physical control signals;
- the need to avoid treating a computer-vision demo as a finished security product.

The challenge was to explore how a compact edge-oriented device could support face-related access-control logic while keeping the system practical enough to deploy outside a notebook environment.

## Solution

The project explores an access-control prototype around a Luckfox / RV1106-style constrained device.

The system direction includes:

- face / eye detection;
- embedding-based comparison;
- liveness / PAD-oriented checks;
- local encrypted storage concepts;
- GPIO / relay-style control boundary;
- service-oriented deployment thinking;
- a lightweight management surface.

The most important part of the project is not only the model logic. It is the attempt to place computer vision inside a system that has hardware, storage, service, and security boundaries.

## Stack

- Python
- OpenCV / computer vision tooling
- Embedded Linux-style deployment
- SQLCipher-style encrypted storage concept
- MicroPython / GPIO-oriented control path
- systemd-style service thinking
- REST / gRPC-oriented management direction

## Result

The project is one of the strongest technical pieces in the portfolio because it shows work beyond a simple script:

- computer vision pipeline thinking;
- constrained hardware awareness;
- access-control domain modeling;
- security-sensitive storage and deployment considerations;
- interest in real device integration rather than notebook-only experimentation.

The repository should be presented as a **prototype**, not as a finished commercial access-control product.

## What I learned

- Computer vision becomes much more interesting when it has to run near real hardware constraints.
- Access-control projects must be described carefully: a working prototype is not automatically a secure product.
- Liveness, false acceptance, storage, and physical control boundaries matter as much as the detection model.
- A good technical portfolio project should show not only code, but also the system boundaries around the code.

## Portfolio role

This is a flagship technical project.

It is best used to show:

- computer vision interest;
- security-minded system thinking;
- edge deployment awareness;
- ability to build beyond CRUD/web-only projects.

## Related repository

- [`eyegate-l-luckfox-scud`](https://github.com/ShapArt/eyegate-l-luckfox-scud)
