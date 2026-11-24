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
| **Game** | ![Unity](https://img.shields.io/badge/Unity_6-222c37?style=flat-square&logo=unity&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white) ![URP](https://img.shields.io/badge/URP-222c37?style=flat-square&logo=unity&logoColor=white) ![Photon](https://img.shields.io/badge/Photon_Fusion_2-004480?style=flat-square) ![FMOD](https://img.shields.io/badge/FMOD-000000?style=flat-square) ![OpenXR](https://img.shields.io/badge/OpenXR_·_Quest-1C1E20?style=flat-square&logo=meta&logoColor=white) ![PlayFab](https://img.shields.io/badge/PlayFab-F26522?style=flat-square) ![Unreal Engine 5](https://img.shields.io/badge/Unreal_Engine_5-0E1128?style=flat-square&logo=unrealengine&logoColor=white) ![Blender](https://img.shields.io/badge/Blender-E87D0D?style=flat-square&logo=blender&logoColor=white) |
| **AI** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) ![Codex](https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![Transformers.js](https://img.shields.io/badge/Transformers.js-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square) |
| **Web / Tools** | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

---

## Game Projects

### [Floor F](https://github.com/Naul-s/Floor-F)

`Solo` `1 week` `Unity 6` `WebGL` · Official 2026 Unity Game Jam · [▶ Play on itch.io](https://naul-ds.itch.io/floor-f)

Elevator puzzle sim where every guest has a lucky and an unlucky number.

<img src="assets/floor-f/nights.gif" alt="Floor F gameplay" width="100%">

- Engine-free C# rule core; Gameplay / Rendering / UI / Audio split into separate assemblies
- 640×360 pixelated render pipeline, 10 nights, 6 endings, English and Korean
- Built in one week by directing an 8-agent Claude Code team

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/floor-f/lucky_shop.png" width="49%"> <img src="assets/floor-f/friday13_rain.jpg" width="49%">
<img src="assets/floor-f/korean_ui.jpg" width="49%">
</details>

<details>
<summary><b>AI workflow</b></summary>

- 8 role agents (gameplay, render, UI, audio, content, asset, QA, release) in isolated Git worktrees
- Directory ownership enforced by hooks; shared contracts changed only by the orchestrator
- Verification ladder: L0 compile → L1 rule tests → L2 runtime screen capture → L3 WebGL build
- 860 test cases

</details>

### [The Pawntom Heist](https://github.com/EwhaKing/The-Pawntom-Heist)

`Team of 6` `Unity 6` `Photon Fusion 2` `NavMesh`

1–4 player co-op stealth game: steal the treasure from an enemy base and escape. I joined when the game had no enemy AI and shipped it through PRs.

- K-9 enemy AI: state machine with sight, hearing, and trace tracking
- Networked enemy spawn and bulkhead state sync
- Tutorial system and text UI, first-person interaction, codebase-wide review and refactor

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/pawntom/1.jpg" width="49%"> <img src="assets/pawntom/2.jpg" width="49%">
</details>

<details>
<summary><b>AI workflow</b></summary>

- Harness redesigned from 4 fixed serial roles to 7-role dynamic orchestration
- Risk-based R0–R3 routing, plan approval gate, 3-perspective independent review
- 38 verification records preserved · ~22k lines of C# on main · 6 PRs merged

</details>

### Project SR

`Solo` `In development` `Unity 6` `FMOD` `Windows API` · Private

3D four-lane rhythm game with gear shifts, plus a chart editor. Targeting Steam.

- Low-latency audio with FMOD and Windows API, DSP-scheduled playback, automatic offset calibration
- Auto-detects WAV, OGG, and MP3 songs
- Layered architecture with a judgment core independent of the engine and FMOD

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/project-sr/gear.jpg" width="100%">
<img src="assets/project-sr/select.jpg" width="49%"> <img src="assets/project-sr/editor.jpg" width="49%">
</details>

<details>
<summary><b>AI workflow</b></summary>

- Judgment contract, JSON Schema, and golden vectors fixed before implementation
- 589 test cases · domain-specific Codex skills for latency, judgment, and visual review
- Ran a fixed 5-role multi-agent system, found its limits, replaced it with a single owner plus skills

</details>

### SHELTER

`Team of 3` `Unity 6` `OpenXR` `Meta Quest` · Private

VR zombie survival: hold the shelter for 10 rounds.

- Enemy AI, resource and enemy spawning with object pooling
- ScriptableObject-driven data, VR camera tracking
- Quest optimization: mesh merging, LOD, lightmaps, foveated rendering

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/shelter/1.jpg" width="49%"> <img src="assets/shelter/2.jpg" width="49%">
</details>

### Trincle

`Team of 6` `4 months` `Unity` · Development paused

Top-down pixel action game with weapon skills, crafting, and procedural maps.

- Top-down movement and state-based sprite animation
- Shader-based weapon skills, hit VFX, and an optimized attack shader
- Perlin-noise procedural map generation
- ScriptableObject-driven item drops and dialogue, inventory and crafting UI, all SFX

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/trincle/move-1.png" width="24%"> <img src="assets/trincle/move-2.png" width="24%"> <img src="assets/trincle/move-3.png" width="40%">
<img src="assets/trincle/shader.png" width="40%"> <img src="assets/trincle/drop.png" width="58%">
<img src="assets/trincle/ui-1.jpg" width="56%"> <img src="assets/trincle/ui-2.png" width="40%">
<img src="assets/trincle/dialog.png" width="100%">
</details>

### Music of the Soul

`Solo` `8 months` `Unity` `PlayFab` `Photon`

Rhythm game with online versus mode. My first full game, built before using AI agents.

- PlayFab sign-up, login, and in-game data sync
- Photon multiplayer
- Object pooling and Profiler-driven memory and script optimization

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/music-of-the-soul/title.jpg" width="49%"> <img src="assets/music-of-the-soul/play.jpg" width="49%">
</details>

### Snow Removal Master

`Solo` `TypeScript` `React` `Three.js` · [▶ Play](https://snow-removal-master.vercel.app)

Low-poly 3D one-stroke puzzle with a procedural Endless mode and a stage editor. All 42 tasks tracked as brief → report → independent review.

---

## AI Projects

### Multi-Agent Development Workflow

`Personal architecture` · Applied across the game projects above

Single agents drifted out of scope, guessed at unstated requirements, and missed their own bugs. I split the work across role agents with explicit approval gates.

- **Roles:** Coordinator, Planner, Plan Reviewer, Builder, Code Reviewer, Reporter. Reviewers never edit.
- **Risk tiers:** T0 / T1 / T2. Plan review and a second approval only for risky work.
- **Decision states:** Confirmed / Candidate / Open Gate, so a guess never becomes a requirement.
- **Handoffs:** pass objective, approvals, and constraints instead of full logs to cut token use.

<details>
<summary><b>Workflow</b></summary>

```mermaid
flowchart LR
    U[Request] --> C[Coordinator]
    C -->|T0| A0([Approve]) --> B0[Builder] --> R0[Reporter]
    C -->|T1| A1([Approve]) --> P1[Planner] --> B1[Builder] --> R1[Reporter]
    C -->|T2| A2([Approve]) --> P2[Planner] --> PR[Plan Reviewer] --> A3([2nd Approve]) --> B2[Builder] --> CR[Code Reviewer] --> R2[Reporter]
```

</details>

<details>
<summary><b>How it evolved</b></summary>

```
2025      Game dev fundamentals without agents
2026.04   Rule files and Unity MCP as assistants
2026.08   Fixed roles (plan → build → review) with a task ledger
2026.09   Contract- and test-first development; dropped the fixed roles
2026.10   Risk-based routing, dynamic orchestration, evidence gates
2026.11   Parallel agent team ships a game in a week; built an AI-output QA tool
```

</details>

### [SlopLens](https://github.com/Naul-s/slop-lens)

`Solo` `Open source` `Python` `MCP` `Unity`

Claude Code plugin and MCP server that explains why an AI-made game or website feels like "AI slop", with evidence and fixes.

- Unity autoplay package that captures gameplay frames and mixed audio for review
- Works with Claude Code, Gemini CLI, Codex, and Cursor
- Validation results published, including failures

### Local Real-Time Translator

`Solo` `3 days` `Chrome extension` `WebGPU`

Translates live audio from YouTube or Twitch into subtitles entirely in the browser, with no cloud API.

- Tab audio → AudioWorklet VAD → Whisper STT → Qwen2.5 or OPUS-MT, each model in its own Web Worker
- q4/q8 quantized models on WebGPU, WASM fallback for STT
- System prompt, few-shot examples, and decoding settings tuned so the LLM outputs only the translation; token-streamed subtitles

<details>
<summary><b>Screenshots</b></summary>
<br>
<img src="assets/translator/1.png" width="30%"> <img src="assets/translator/2.jpg" width="68%">
</details>

### AI Vision Assistive Device

`Solo` `8 hours` `Raspberry Pi` `Python` · Jeonju Youth IP Hackathon **Gold Prize**

A camera on a Raspberry Pi sends images to a vision AI API and describes what is in front of a visually impaired user.

- Set up the Raspberry Pi Linux environment and wired camera input to the API in Python
- Tuned prompts so answers stay short and never state uncertain details as fact

<details>
<summary><b>Photos</b></summary>
<br>
<img src="assets/assistive-device/1.jpg" width="52%"> <img src="assets/assistive-device/2.jpg" width="35%">
</details>

---

## Awards & Activities

| Date | |
|---|---|
| 2025.12 | Jeonju Youth IP Hackathon — **Gold Prize** |
| 2025.06 | Craftsman Information Processing (정보처리기능사) |
| 2025.04 – | Co-founder & president, school game development club · taught C# and Unity |
| 2024.04 | Regional Skills Competition — **Silver Medal** |
