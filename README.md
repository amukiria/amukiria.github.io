# HazardXR

![Unity 6](https://img.shields.io/badge/Unity-6-FF6B00?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Meta%20Quest%203-00C2A8?style=flat-square)
![Status](https://img.shields.io/badge/Status-In%20Development-1A1A2E?style=flat-square)

Mixed reality safety training simulations built for the Meta Quest 3. One app, eleven episodes — each a golden-rule scenario drawn from a standardised, globally enforced safety domain.

## Overview

HazardXR is a modular MR/VR simulation platform. Each episode teaches one critical safety behaviour through immersive, consequence-driven experience rather than passive instruction. The shell handles common systems (session management, progression, scoring, and UI); episodes are self-contained modules that load on top of it.

The build order is shell first, then E01 Fire, then subsequent episodes in sequence. No episode is started until the one before it ships.

## Episodes

| # | Title | Safety domain | Standard | Status |
|---|-------|---------------|----------|--------|
| E01 | Fire | Fire safety | NFPA 10 · OSHA 1910.157 | Active build |
| E02 | Lockout / Tagout | Energy control · Machinery safety | ISO 14118 · OSHA 1910.147 | Planned |
| E03 | Working at Height | Fall protection · Construction | ISO 45001 · OSHA 1926.502 | Planned |
| E04 | Hazard Identification | General industry · Risk awareness | ISO 31000 · ISO 45001 | Planned |
| E05 | Line of Fire | Struck-by / caught-in hazards | ISO 45001 Cl. 6.1 · BBS | Planned |
| E06 | Confined Space Entry | Permit-required spaces · Atmosphere hazards | ISO 45001 · OSHA 1910.146 | Planned |
| E07 | Chemical Handling | Hazmat · Toxic substance exposure | GHS · OSHA 1910.1200 | Planned |
| E08 | Respiratory Protection | PPE selection · Hazardous atmospheres | ISO 16972 · OSHA 1910.134 | Planned |
| E09 | Powered Industrial Trucks | Forklift safety · Warehouse operations | ISO 3691 · OSHA 1910.178 | Planned |
| E10 | Stop Work Authority | Behaviour-based safety | IOGP Report 459 | Planned |
| E11 | Disaster Response | Emergency preparedness | NFPA 1600 · ICS | Planned |

## Tech stack

- **Engine:** Unity 6
- **Platform:** Meta Quest 3 — MR passthrough and VR
- **SDK:** Meta XR SDK
- **Version control:** Git / GitHub

## Project structure

```
HazardXR/
├── Assets/
│   ├── _Core/              # Shell systems: session, progression, scoring, UI
│   ├── Episodes/
│   │   ├── E01_Fire/       # Active build
│   │   ├── E02_LOTO/       # Planned
│   │   ├── E03_Height/     # Planned
│   │   ├── E04_HazardID/   # Planned
│   │   ├── E05_LineOfFire/ # Planned
│   │   ├── E06_ConfinedSpace/ # Planned
│   │   ├── E07_Chemical/   # Planned
│   │   ├── E08_Respiratory/ # Planned
│   │   ├── E09_Forklift/   # Planned
│   │   ├── E10_StopWork/   # Planned
│   │   └── E11_Disaster/   # Planned
│   ├── Shared/             # Prefabs, materials, audio used across episodes
│   └── XR/                 # Meta XR SDK integrations
├── Packages/
├── ProjectSettings/
└── .gitignore
```

## Build instructions

1. Clone the repo: `git clone https://github.com/<your-username>/HazardXR.git`
2. Open in Unity Hub — Unity 6 required.
3. Install Meta XR SDK via Package Manager if not already present.
4. Set build target to Android (Quest 3 platform).
5. Open `Assets/_Core/Scenes/Main.unity` to begin.

## Commit conventions

| Prefix | Use for |
|--------|---------|
| `feat:` | New feature or episode content |
| `fix:` | Bug fix |
| `wip:` | Work in progress checkpoint |
| `refactor:` | Structural change with no behaviour change |
| `docs:` | Documentation only |
| `assets:` | 3D models, textures, audio |

## Brand

| Token | Value |
|-------|-------|
| Navy | `#1A1A2E` |
| Amber | `#FF6B00` |
| Teal | `#00C2A8` |
| White | `#F0F0F0` |
| Red | `#FF2D2D` |

---

© Albert Mukiria — All rights reserved. Not licensed for public use.
