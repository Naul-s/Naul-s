<div align="center">

# Naul

**게임 클라이언트 개발자 · AI Native 워크플로**

AI 에이전트 팀으로 Unity 게임을 만듭니다. 명세·역할·검증 게이트는 제가 설계하고, 구현은 그 안에서 에이전트가 합니다.

[English](README.md) · [itch.io](https://naul-ds.itch.io)

</div>

---

## 기술 스택

| | |
|---|---|
| **Game** | ![Unity](https://img.shields.io/badge/Unity_6-222c37?style=flat-square&logo=unity&logoColor=white) ![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white) ![URP](https://img.shields.io/badge/URP-222c37?style=flat-square&logo=unity&logoColor=white) ![Photon](https://img.shields.io/badge/Photon_Fusion_2-004480?style=flat-square) ![FMOD](https://img.shields.io/badge/FMOD-000000?style=flat-square) ![OpenXR](https://img.shields.io/badge/OpenXR_·_Quest-1C1E20?style=flat-square&logo=meta&logoColor=white) ![PlayFab](https://img.shields.io/badge/PlayFab-F26522?style=flat-square) |
| **AI** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) ![Codex](https://img.shields.io/badge/Codex-412991?style=flat-square&logo=openai&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square) ![Transformers.js](https://img.shields.io/badge/Transformers.js-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square) |
| **Web / Tools** | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

---

## 대표 프로젝트

### [Floor F](https://github.com/Naul-s/Floor-F) — 1인 · Official 2026 Unity Game Jam

손님마다 다른 행운·불운의 숫자를 읽으며 운전하는 엘리베이터 퍼즐 시뮬레이션. 에이전트 8종을 지휘해 1주 만에 완성.

- **게임:** Unity 6 · URP · WebGL. 엔진 비의존 C# 규칙 코어, Gameplay / Rendering / UI / Audio 어셈블리 분리, 640×360 픽셀화 렌더 파이프라인, 10일차 · 엔딩 6종, 한/영 지원
- **AI Native:** 역할별 에이전트 8종을 Git worktree로 격리, 디렉터리 소유권을 훅으로 강제, 공유 계약 변경은 오케스트레이터만 수행
- **검증:** L0 컴파일 → L1 규칙 테스트 → L2 런타임 화면 캡처 → L3 WebGL 빌드 · 테스트 케이스 860개

[▶ itch.io에서 플레이](https://naul-ds.itch.io/floor-f)

### [The Pawntom Heist](https://github.com/EwhaKing/The-Pawntom-Heist) — 5인 팀 · 협동 잠입

1~4인 1인칭 협동 잠입 게임. 적 AI가 없던 프로젝트에 합류해 PR로 통합.

- **게임:** Unity 6 · Photon Fusion 2 · NavMesh. 시야·청각·흔적 추적을 갖춘 K-9 적 상태머신, 적 스폰과 격벽 상태 네트워크 동기화, 튜토리얼 시스템, 1인칭 팔 연출과 상호작용
- **AI Native:** 고정 4역할 직렬 구조에서 7역할 동적 오케스트레이션으로 하네스 재설계, 위험도별 R0~R3 라우팅, 계획 승인 게이트, 검증 기록 38건 보존
- **기여:** main 기준 C# 약 2.2만 줄 · PR 6건 병합

### Project SR — 1인 · 3D 리듬게임 + 채보 에디터

4레인·트리거·기어 시프트를 조합한 건반형 리듬게임과 채보 에디터. Steam 출시 목표.

- **게임:** Unity 6 · FMOD · Input System. Domain / Application / Infrastructure / Presentation 계층 분리, 엔진·FMOD 비의존 판정 코어, DSP 스케줄 재생, 저지연 입력 시계 상관
- **툴:** 파형·템포맵·미리듣기를 갖춘 채보 에디터
- **AI Native:** 판정 계약·JSON Schema·golden vector를 구현 전에 고정 · 테스트 케이스 589개 · 도메인 전용 Codex 스킬

`Private`

### [SlopLens](https://github.com/Naul-s/slop-lens) — 1인 · 오픈소스

AI로 만든 게임·웹이 왜 "AI 슬롭"처럼 느껴지는지 근거와 수정안으로 설명하는 Claude Code 플러그인 · MCP 서버.

- 플레이 프레임과 믹스 오디오를 캡처하는 Unity 자동 플레이 패키지
- Claude Code, Gemini CLI, Codex, Cursor 지원
- 실패 결과를 포함한 검증 수치 공개

---

## 기타 프로젝트

| 프로젝트 | 유형 | 내용 |
|---|---|---|
| **SHELTER** | Quest VR 디펜스 · 3인 팀 | 라운드 루프, 좀비 AI, 경제 시스템 · Quest 최적화(메시 병합, LOD, 라이트맵, 포비에이티드 렌더링) · 기획을 에이전트용 스킬로 문서화 · `Private` |
| **[Snow Removal Master](https://snow-removal-master.vercel.app)** | 웹 3D 퍼즐 · 1인 | React · Three.js · Rapier · 절차 생성 Endless 모드, 스테이지 에디터 · 작업 42건 전부 지시 → 보고 → 독립 리뷰로 추적 |
| **Local Real-Time Translator** | Chrome 확장 · 온디바이스 AI | WebGPU에서 Whisper + Qwen2.5 / OPUS-MT 실행, AudioWorklet VAD, 토큰 스트리밍 자막, API 호출 0건 |
| **UniTrio Game 2026** | 액션 게임 · 3인 팀 | 차지 스킬, 속성 디버프, 인벤토리, 제작, 몬스터 AI, 오디오 매니저, 서리 오라 셰이더 |
| **Rhythm Game (2025)** | 리듬게임 · 온라인 대전 | Photon PUN 대전, PlayFab 로그인·리더보드, 채보 에디터 · G-STAR 2025 전시 |

---

## AI 활용 방식

| 원칙 | 실천 |
|---|---|
| **명세 우선** | 에이전트가 코드를 쓰기 전에 계약·스키마·golden vector를 고정 |
| **역할 분리** | 계획·구현·리뷰를 별도 에이전트로 분리, 리뷰어는 수정하지 않음 |
| **소유권** | 에이전트별 쓰기 가능 디렉터리를 Git 훅으로 강제 |
| **말이 아닌 증거** | "완료"는 컴파일·테스트·런타임 캡처·빌드 결과로만 판정 |
| **사람의 판단** | 손맛·밸런스·기획 결정은 직접 판단 |
| **하네스 개선** | 고정 멀티에이전트 구조를 운영해 한계를 확인하고, 위험도 기반 동적 오케스트레이션으로 교체 |

```
2025      에이전트 없이 게임 개발 기본기 — 리듬게임 G-STAR 전시
2026.04   규칙 파일과 Unity MCP를 보조 도구로 활용
2026.08   고정 역할(계획 → 구현 → 리뷰)과 작업 원장
2026.09   계약·테스트 우선 개발, 고정 MAS 폐기
2026.10   위험도 라우팅, 동적 오케스트레이션, 증거 게이트
2026.11   병렬 에이전트 팀으로 1주 만에 게임 완성, AI 결과물 검증 도구 제작
```

---

## 수상 · 활동

| 시기 | |
|---|---|
| 2026.11 | Official 2026 Unity Game Jam — *Floor F* |
| 2026.07 | 고등학교 프로그래밍 보조 강사 |
| 2025.12 | 전주시 청소년 IP 해커톤 — **금상** (시각장애인용 AI 비전 보조 장치) |
| 2025.11 | G-STAR 2025 — 리듬게임 전시 |
| 2025.10 | 남원 드론 페스티벌 — 리듬게임 전시 |
| 2025.06 | 프로그래밍기능사 |
| 2025.04 – | 교내 게임 개발 동아리 공동 설립 · 회장, C#·Unity 교육 |
| 2024.04 | 지방기능경기대회 — **은메달** |
