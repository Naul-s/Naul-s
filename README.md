<div align="center">

# Naul

**Game Client Developer · AI-Native Workflow**

I build Unity games with AI agent teams: I design the specs, roles, and verification gates; agents implement inside them.

[한국어](README.ko.md) · [itch.io](https://naul-ds.itch.io)

</div>

---

## Tech Stack

| | |
|---|---|
| **Game** | ![Unity](https://img.shields.io/badge/Unity_6-222c37?style=flat-square&logo=unity&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white) ![URP](https://img.shields.io/badge/URP-222c37?style=flat-square&logo=unity&logoColor=white) ![Photon](https://img.shields.io/badge/Photon_Fusion_2-004480?style=flat-square) ![FMOD](https://img.shields.io/badge/FMOD-000000?style=flat-square) ![OpenXR](https://img.shields.io/badge/OpenXR_·_Quest-1C1E20?style=flat-square&logo=meta&logoColor=white) ![PlayFab](https://img.shields.io/badge/PlayFab-F26522?style=flat-square) |
| **AI** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) ![Codex](https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square) ![Transformers.js](https://img.shields.io/badge/Transformers.js-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square) |
| **Web / Tools** | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

---

## Featured Projects

### [Floor F](https://github.com/Naul-s/Floor-F) — Solo · Official 2026 Unity Game Jam

Elevator puzzle sim where every guest has a lucky and an unlucky number. Built in one week by directing an 8-agent team.

- **Game:** Unity 6 · URP · WebGL. Engine-free C# rule core, assemblies split by Gameplay / Rendering / UI / Audio, 640×360 pixelated render pipeline, 10 nights, 6 endings, EN/KO
- **AI-native:** 8 role agents in isolated Git worktrees, directory ownership enforced by hooks, contract changes reserved to the orchestrator
- **Verification:** L0 compile → L1 rule tests → L2 runtime screen capture → L3 WebGL build · 860 test cases

[▶ Play on itch.io](https://naul-ds.itch.io/floor-f)

### [The Pawntom Heist](https://github.com/EwhaKing/The-Pawntom-Heist) — Team of 5 · Co-op Stealth

1–4 player first-person co-op stealth game. Joined a project with no enemy AI and shipped it through PRs.

- **Game:** Unity 6 · Photon Fusion 2 · NavMesh. K-9 enemy state machine with sight, hearing, and trace tracking; networked enemy spawn and bulkhead sync; tutorial system; first-person arms and interaction
- **AI-native:** Harness evolved from 4 fixed serial roles to 7-role dynamic orchestration, risk-based R0–R3 routing, plan approval gate, 38 preserved verification records
- **Scope:** ~22k lines of C# on main · 6 PRs merged

### Project SR — Solo · 3D Rhythm Game + Chart Editor

Four-lane rhythm game with triggers and gear shifts, plus a full chart editor. Targeting Steam.

- **Game:** Unity 6 · FMOD · Input System. Domain / Application / Infrastructure / Presentation layers, judgment core independent of engine and FMOD, DSP-scheduled playback, low-latency input clock correlation
- **Tools:** Chart editor with waveform, tempo map, and preview
- **AI-native:** Judgment contract, JSON Schema, and golden vectors fixed before implementation · 589 test cases · domain-specific Codex skills

`Private`

### [SlopLens](https://github.com/Naul-s/slop-lens) — Solo · Open Source

Claude Code plugin and MCP server that explains why an AI-made game or website feels like "AI slop", with evidence and fixes.

- Unity autoplay package that captures gameplay frames and mixed audio for review
- Works with Claude Code, Gemini CLI, Codex, Cursor
- Validation results published, including failures

---

## More Projects

| Project | Type | Highlights |
|---|---|---|
| **SHELTER** | Quest VR defense · Team of 3 | Round loop, zombie AI, economy · Quest optimization (mesh merge, LOD, lightmaps, foveated rendering) · game design written as agent-readable skills · `Private` |
| **[Snow Removal Master](https://snow-removal-master.vercel.app)** | Web 3D puzzle · Solo | React · Three.js · Rapier · procedural Endless mode and stage editor · 42 tasks each tracked as brief → report → independent review |
| **Local Real-Time Translator** | Chrome extension · On-device AI | Whisper + Qwen2.5 / OPUS-MT on WebGPU, AudioWorklet VAD, token-streamed subtitles, zero API calls |
| **UniTrio Game 2026** | Action game · Team of 3 | Charged skills, elemental debuffs, inventory, crafting, monster AI, audio manager, frost aura shader |
| **Rhythm Game (2025)** | Rhythm game · Online versus | Photon PUN versus mode, PlayFab login and leaderboard, chart editor · exhibited at G-STAR 2025 |

---

## How I Work with AI

| Principle | Practice |
|---|---|
| **Spec first** | Contracts, schemas, and golden vectors are fixed before agents write code |
| **Role separation** | Planner, builder, and reviewer are separate agents; reviewers never edit |
| **Ownership** | Each agent writes only to its own directories, enforced by Git hooks |
| **Evidence, not claims** | "Done" requires compile, tests, runtime capture, or build output |
| **Human judgment** | Game feel, balance, and design calls stay with me |
| **Iterate the harness** | Ran a fixed multi-agent system, found its limits, replaced it with risk-based dynamic orchestration |

```
2025      Game dev fundamentals without agents — rhythm game exhibited at G-STAR
2026.04   Rule files and Unity MCP as assistants
2026.08   Fixed roles (plan → build → review) with a task ledger
2026.09   Contract- and test-first development; dropped the fixed MAS
2026.10   Risk-based routing, dynamic orchestration, evidence gates
2026.11   Parallel agent team ships a game in a week; built an AI-output QA tool
```

---

## Awards & Activities

| Date | |
|---|---|
| 2026.11 | Official 2026 Unity Game Jam — *Floor F* |
| 2026.07 | Programming teaching assistant, high school |
| 2025.12 | Jeonju Youth IP Hackathon — **Gold Prize** (AI vision assistive device for the visually impaired) |
| 2025.11 | G-STAR 2025 — Exhibited rhythm game |
| 2025.10 | Namwon Drone Festival — Exhibited rhythm game |
| 2025.06 | Craftsman Programming certification |
| 2025.04 – | Co-founder & president, school game development club · taught C# and Unity |
| 2024.04 | Regional Skills Competition — **Silver Medal** |
