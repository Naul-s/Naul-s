<div align="center">

# Naul

**Game Client Developer · AI-Native Workflow**

I build Unity games with AI agent teams: I design the specs, roles, and verification gates; agents implement inside them.

[한국어](README.ko.md) · [itch.io](https://naul-ds.itch.io)

<br>

![Unity](https://img.shields.io/badge/Unity_6-222c37?style=flat-square&logo=unity&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white) ![Photon](https://img.shields.io/badge/Photon_Fusion_2-004480?style=flat-square) ![FMOD](https://img.shields.io/badge/FMOD-000000?style=flat-square) ![OpenXR](https://img.shields.io/badge/OpenXR_·_Quest-1C1E20?style=flat-square&logo=meta&logoColor=white) ![PlayFab](https://img.shields.io/badge/PlayFab-F26522?style=flat-square) ![Unreal Engine 5](https://img.shields.io/badge/Unreal_Engine_5-0E1128?style=flat-square&logo=unrealengine&logoColor=white) ![Blender](https://img.shields.io/badge/Blender-E87D0D?style=flat-square&logo=blender&logoColor=white)<br>
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) ![Codex](https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![Transformers.js](https://img.shields.io/badge/Transformers.js-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square)<br>
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)

</div>

---

## Featured Games

### [Floor F](https://github.com/Naul-s/Floor-F)

<sub>Solo · 1 week · Unity 6 · WebGL · Official 2026 Unity Game Jam</sub> · [▶ Play on itch.io](https://naul-ds.itch.io/floor-f)

Elevator puzzle sim where every guest has a lucky and an unlucky number.

<img src="assets/floor-f/nights.gif" alt="Floor F" width="100%">

- Engine-free C# rule core; Gameplay / Rendering / UI / Audio split into assemblies
- 640×360 pixelated render pipeline, 10 nights, 6 endings, English and Korean
- **AI:** 8 role agents in isolated Git worktrees, ownership enforced by hooks, L0 compile → L1 tests → L2 screen capture → L3 WebGL build, 860 test cases

<details>
<summary>Screenshots</summary>
<br>
<img src="assets/floor-f/lucky_shop.png" width="49%"> <img src="assets/floor-f/friday13_rain.jpg" width="49%">
</details>

### [The Pawntom Heist](https://github.com/EwhaKing/The-Pawntom-Heist)

<sub>Team of 6 · Unity 6 · Photon Fusion 2 · NavMesh</sub>

1–4 player co-op stealth game. Joined when the game had no enemy AI and shipped it through PRs.

<img src="assets/pawntom/title.jpg" alt="The Pawntom Heist" width="100%">

- K-9 enemy AI with sight, hearing, and trace tracking, synced over the network
- Tutorial system, first-person interaction, codebase-wide review and refactor
- **AI:** Harness redesigned from 4 fixed roles to 7-role dynamic orchestration with risk-based routing · 6 PRs merged

<details>
<summary>Screenshots</summary>
<br>
<img src="assets/pawntom/tutorial.jpg" width="49%"> <img src="assets/pawntom/escape.jpg" width="49%">
</details>

### Project SR

<sub>Solo · In development · Unity 6 · FMOD · Windows API · Private</sub>

3D four-lane rhythm game with gear shifts and a chart editor. Targeting Steam.

<img src="assets/project-sr/gear.jpg" alt="Project SR" width="100%">

- Low-latency audio with FMOD and Windows API, DSP-scheduled playback, automatic offset calibration
- Judgment core independent of the engine and FMOD; auto-detects WAV, OGG, MP3
- **AI:** Judgment contract, JSON Schema, and golden vectors fixed before implementation · 589 test cases

<details>
<summary>Screenshots</summary>
<br>
<img src="assets/project-sr/select.jpg" width="49%"> <img src="assets/project-sr/editor.jpg" width="49%">
</details>

### More Games

| Project | Description |
|---|---|
| **SHELTER**<br><sub>Team of 3 · VR · Private</sub> | VR zombie survival for Meta Quest. Enemy AI, pooled spawning, ScriptableObject data, Quest optimization (LOD, lightmaps, foveated rendering).<details><summary>Screenshots</summary><img src="assets/shelter/1.jpg" width="300"> <img src="assets/shelter/2.jpg" width="300"></details> |
| **Trincle**<br><sub>Team of 6 · Unity</sub> | Top-down pixel action. Shader-based weapon skills, hit VFX, Perlin-noise map generation, ScriptableObject item drops and dialogue, inventory and crafting UI.<details><summary>Screenshots</summary><img src="assets/trincle/shader.png" width="300"> <img src="assets/trincle/drop.png" width="300"> <img src="assets/trincle/ui-1.jpg" width="300"> <img src="assets/trincle/dialog.png" width="300"></details> |
| **Music of the Soul**<br><sub>Solo · Unity · 2025</sub> | Rhythm game with online versus. PlayFab login and data sync, Photon multiplayer, object pooling and Profiler-driven optimization.<details><summary>Screenshots</summary><img src="assets/music-of-the-soul/title.jpg" width="300"> <img src="assets/music-of-the-soul/play.jpg" width="300"></details> |
| **Snow Removal Master**<br><sub>Solo · Web</sub> | Low-poly 3D one-stroke puzzle in React and Three.js with a procedural Endless mode and stage editor. [▶ Play](https://snow-removal-master.vercel.app) |

---

## AI Projects

### AI Development Workflow

<sub>How my agent workflow grew · 2026.08 → 2026.11</sub>

I started with a fixed pipeline of process roles. After running it on real projects, I rebuilt it around module ownership and automated checks.

| | Then · Fixed pipeline | Now · Orchestrated team |
|---|---|---|
| **Structure** | 6 roles in a serial chain: plan → review → build → review → report | Orchestrator plus 8 domain agents (gameplay, render, UI, audio, content, assets, QA, release) |
| **Parallelism** | One task at a time | Up to 3 writing agents at once, each in its own Git worktree |
| **Conflicts** | Allowed-file list per task | Directory ownership enforced by hooks; shared contracts fixed first and changed only by the orchestrator |
| **"Done" means** | A reviewer agent returns PASS | Automated checks pass: L0 compile (4s) → L1 tests → L2 runtime screen capture → L3 WebGL build |
| **Integration** | Manual | Trial merge + compile; on failure develop is untouched and the work goes back to its agent |
| **Human role** | Approve each plan, sometimes twice | Set contracts and direction, approve assets and pushes, judge game feel |
| **Used on** | Snow Removal Master, Project SR | Floor F: playable WebGL game in one week, 860 test cases |

**Kept from the first version:** human approval for decisions, evidence over claims, short fixed-format briefs and reports instead of full logs.

<details>
<summary>Current pipeline and timeline</summary>

```mermaid
flowchart LR
    O[Orchestrator] -- brief --> A1[gameplay-dev]
    O -- brief --> A2[render-dev]
    O -- brief --> A3[ui-dev]
    A1 & A2 & A3 -- report --> I{Trial merge<br/>+ L0 compile}
    I -- pass --> D[(develop)]
    I -- fail --> O
```

```
2025      Game dev fundamentals without agents
2026.04   Rule files and Unity MCP as assistants
2026.08   Fixed role pipeline with a task ledger
2026.09   Contract- and test-first development; dropped the fixed roles
2026.10   Risk-based routing, dynamic orchestration, evidence gates
2026.11   Orchestrated parallel team ships a game in a week; built an AI-output QA tool
```

</details>

### More AI Projects

| Project | Description |
|---|---|
| **[SlopLens](https://github.com/Naul-s/slop-lens)**<br><sub>Solo · Open source</sub> | Claude Code plugin and MCP server that explains why an AI-made game or website feels like "AI slop". Unity autoplay capture of frames and audio; validation results published, including failures. |
| **Real-Time Translator**<br><sub>Solo · Chrome extension</sub> | Live subtitles for YouTube and Twitch, fully in-browser. Whisper STT and Qwen2.5 / OPUS-MT on WebGPU with q4/q8 quantization, VAD, token streaming, no cloud API.<details><summary>Screenshots</summary><img src="assets/translator/1.png" width="180"> <img src="assets/translator/2.jpg" width="420"></details> |
| **AI Vision Assistive Device**<br><sub>Solo · 8 hours · Hackathon Gold</sub> | Raspberry Pi camera sends images to a vision AI API and describes the scene to visually impaired users. Prompts tuned to stay short and never state uncertain details as fact.<details><summary>Photos</summary><img src="assets/assistive-device/1.jpg" width="300"> <img src="assets/assistive-device/2.jpg" width="200"></details> |

---

## Awards & Activities

| Date | |
|---|---|
| 2025.12 | Jeonju Youth IP Hackathon — **Gold Prize** |
| 2025.06 | Craftsman Information Processing (정보처리기능사) |
| 2025.04 – | Co-founder & president, school game development club · taught C# and Unity |
| 2024.04 | Regional Skills Competition — **Silver Medal** |
