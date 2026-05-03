# HazardXR

![Unity 6](https://img.shields.io/badge/Unity-6-FF6B00?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Meta%20Quest%203-00C2A8?style=flat-square)
![Status](https://img.shields.io/badge/Status-In%20Development-1A1A2E?style=flat-square)

A B2B safety simulation platform built on Meta Quest 3. Two apps, eleven episodes — each grounded in a real, globally enforced safety standard. Built by **Axira Systems**.

## The Family

HazardXR is not a single app. It is a family of three products, each assigned to the medium that its scenarios demand.

| App | Medium | Episodes | Status |
|-----|--------|----------|--------|
| HazardMR | MR Passthrough | 8 | Active Build |
| HazardVR | Full VR | 3 | Planned |
| HazardAR | Mobile AR | TBD | Future |

## HazardMR — MR Passthrough

Your environment becomes the workplace. Hazards, equipment, and consequence are overlaid on your real space via Quest 3 passthrough. The danger feels present because your surroundings are real.

| # | Episode | Standard |
|---|---------|----------|
| E01 | Fire | NFPA 10 · OSHA 1910.157 |
| E02 | Lockout / Tagout | ISO 14118 · OSHA 1910.147 |
| E03 | Hazard Identification | ISO 31000 · ISO 45001 |
| E04 | Line of Fire | ISO 45001 Cl. 6.1 · BBS |
| E05 | Chemical Handling | GHS · OSHA 1910.1200 |
| E06 | Respiratory Protection | ISO 16972 · OSHA 1910.134 |
| E07 | Powered Industrial Trucks | ISO 3691 · OSHA 1910.178 |
| E08 | Stop Work Authority | IOGP Report 459 |

## HazardVR — Full VR

Scenarios where the physical environment itself is the hazard. Heights. Enclosed spaces. Large-scale disaster. Full immersion is not a preference — it is the only way to make these scenarios work.

| # | Episode | Standard |
|---|---------|----------|
| E01 | Working at Height | ISO 45001 · OSHA 1926.502 |
| E02 | Confined Space Entry | ISO 45001 · OSHA 1910.146 |
| E03 | Disaster Response | NFPA 1600 · ICS |

## HazardAR — Mobile AR (Future)

A safety manager walks the factory floor and sees hazard overlays in real time via phone or tablet. No headset. No setup. Episodes TBD. Build begins after HazardMR and HazardVR ship.

## Tech Stack

- **Engine:** Unity 6
- **Platform:** Meta Quest 3 — MR passthrough (HazardMR) and Full VR (HazardVR)
- **SDK:** Meta XR SDK
- **Backend:** Django / DRF · PostgreSQL · DigitalOcean · Docker
- **Version control:** Git / GitHub

## Project Structure

```
HazardXR/
├── Assets/
│   ├── _Core/                  # Shell systems: session, progression, scoring, UI
│   ├── HazardMR/
│   │   ├── E01_Fire/           # Active build
│   │   ├── E02_LOTO/
│   │   ├── E03_HazardID/
│   │   ├── E04_LineOfFire/
│   │   ├── E05_Chemical/
│   │   ├── E06_Respiratory/
│   │   ├── E07_Forklift/
│   │   └── E08_StopWork/
│   ├── HazardVR/
│   │   ├── E01_Height/
│   │   ├── E02_ConfinedSpace/
│   │   └── E03_Disaster/
│   ├── Shared/                 # Prefabs, materials, audio used across episodes
│   └── XR/                    # Meta XR SDK integrations
├── Packages/
├── ProjectSettings/
└── .gitignore
```

## Build Status

Shell architecture is the first deliverable. HazardMR E01 Fire builds on top of the shell. Episodes follow in sequence — no episode starts until the one before it ships. Django backend and dashboard are built after HazardMR E01 ships, before E02 starts.

## Build Instructions

1. Clone the repo: `git clone https://github.com/amukiria/HazardXR.git`
2. Open in Unity Hub — Unity 6 required.
3. Install Meta XR SDK via Package Manager if not already present.
4. Set build target to Android (Quest 3 platform).
5. Open `Assets/_Core/Scenes/Main.unity` to begin.

## Commit Conventions

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

© Axira Systems — All rights reserved. Not licensed for public use.
