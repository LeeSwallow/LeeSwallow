<p align="center">
  <img src="../assets/profile-header.svg" width="960" alt="LeeSwallow — Backend &amp; AI Services. Build with purpose. Verify with evidence." />
</p>

<h1 align="center">이민형 · LeeSwallow</h1>

<p align="center">
  <strong>업무의 기준을 코드로, AI의 판단을 검증 가능한 결과로 만듭니다.</strong><br />
  Backend · AI Services · Workflow Automation
</p>

<p align="center">
  <a href="mailto:lmh2157@outlook.kr">Email</a> ·
  <a href="https://github.com/LeeSwallow?tab=repositories">Repositories</a> ·
  <a href="https://github.com/team-minswon">HeyMoa Team</a>
</p>

---

Java·Spring Boot로 인증과 업무 API를, Python·FastAPI·LangGraph로 회의 분석 AI를 개발합니다. **백엔드 · AI 서비스 개발 직무**를 찾고 있습니다.

- **업무를 먼저 이해합니다.** 회의의 결정·할 일을 구분하는 기준, 권한과 데이터 보존 규칙을 정하고 구현합니다.
- **실패를 추적할 수 있게 만듭니다.** 원문 근거와 실행 기록을 남겨 검색 누락과 모델 판단 오류를 나눠 확인합니다.
- **실험으로 선택합니다.** 같은 평가 기준으로 변경 전후를 비교하고, 효과가 없는 접근은 철회합니다.

## Selected work

### 01 / HeyMoa — 회의를 업무 맥락으로 연결하는 AI

**2026.07–현재 · AI·SW마에스트로 17기 · 3인 팀 · AI 서버 주 개발**

회의에서 결정·할 일·안건을 추출하고, 원문 근거와 함께 조회하는 AI 회의록 서비스입니다.

- **도메인 설계:** 결정·할 일의 판정 기준을 팀과 정의하고, 실시간 추출 → 회의 후 분석 → 근거 기반 질의응답을 연결했습니다.
- **분석 구조:** 긴 회의의 일괄 분석을 안건별 병렬 해석과 결과 종합으로 나눴습니다. 별도 검증 회의 **15개에서 분석을 완료**했습니다.
- **연결 자원 관리:** LLM 응답을 기다리는 동안 DB 연결을 점유하던 잠금 구조를 작업별 배타 수단으로 바꿨습니다. **모의 LLM·회의 100건·태스크 2개·5분 부하에서 풀 대기 타임아웃 0건**을 확인했습니다.

`Python` `FastAPI` `LangGraph` `PostgreSQL / pgvector` `Valkey` `AWS`

[팀 페이지 →](https://github.com/team-minswon)

### 02 / 금정열린배움터 — 비영리 야학의 업무 백엔드

**2026.02–10 · 개발 4인 팀 / BE 2인 · 인증·권한·업무 API·운영 기반 개발**

교사와 직원이 사용하는 수업·출석·구입 요청·게시판 서비스의 백엔드를 개발했습니다.

- **인증과 권한:** 업무 사용자와 로그인 정보를 분리하고, 일반·Google 로그인과 토큰 재발급, 이메일 인증을 연결했습니다.
- **데이터 보존:** 구입 요청의 중복 상태 전이를 막고, 과목을 변경해도 이미 진행한 수업과 출석 기록을 보존하도록 수정했습니다.
- **조회 개선:** 반복 권한 조회에 캐시를 적용하고 변경 트랜잭션 완료 후 무효화했습니다. **동일 코드·H2·실제 HTTP 대조 10쌍에서 반복 요청 SQL 5→1회**를 확인했습니다. 첫 요청은 양쪽 모두 5회였습니다.

`Java` `Spring Boot` `Spring Security` `PostgreSQL` `Caffeine` `GCP`

### 03 / MoMeet — 위치 기반 취미 모임과 실시간 채팅

**2025.08–11 · 카카오 테크 캠퍼스 3기 · 6인 팀 / BE 3인 · BE 테크리더**

모임 검색·참가·채팅을 제공하는 서비스에서 백엔드 초기 구성과 인증, 실시간 채팅을 맡았습니다.

- **인증 연동:** 프론트엔드와의 쿠키 계약 문제를 해결하기 위해 30초 연결 전용 토큰과 프레임별 Access 검증, 세션 소유자 확인을 적용했습니다.
- **채팅 구현:** WebSocket/STOMP 메시지 검증·저장·발행, 이전 대화의 커서 조회와 입퇴장 알림을 구현했습니다.
- **장애 대응:** 같은 토픽을 참가자 수만큼 발행하던 코드를 수정했습니다. **실제 리스너 본문과 의존성 대역을 사용한 활성 16명 재현에서 메시징 호출 16→1회**를 확인했습니다.

`Java` `Spring Boot` `WebSocket / STOMP` `QueryDSL` `PostgreSQL / PostGIS` `Redis`

[백엔드 저장소 →](https://github.com/kakao-tech-campus-3rd-step3/Team11_BE)

<sub>수치는 2026년 10월 포트폴리오 검증 기록 기준입니다. 각 항목에 적은 부하·대조·재현 조건의 결과입니다.</sub>

## Toolkit

| 영역 | 프로젝트에서 사용한 기술 |
| --- | --- |
| Backend | Java · Spring Boot · Spring Security · JPA · QueryDSL · FastAPI |
| AI services | Python · LangGraph · 근거 검색 · 구조화 추출 · 모델 품질 평가 |
| Data | PostgreSQL · pgvector · PostGIS · Redis / Valkey · Caffeine |
| Delivery & observability | Docker · GitHub Actions · AWS ECS / EC2 · GCP · OpenTelemetry |

## More projects

AI를 제품과 도구에 연결하며 탐구한 프로젝트입니다.

| 프로젝트 | 무엇을 만들었나 | 담당·핵심 기술 |
| --- | --- | --- |
| [**petnudge**](https://github.com/LeeSwallow/petnudge) | 할 일·포모도로·코딩 에이전트를 연결하는 데스크톱 펫. 공개 빌드 준비 중 | 개인 프로젝트 · TypeScript · Electron · SQLite · 로컬 MCP |
| [**Detective Agent**](https://github.com/LeeSwallow/asm-team08-ai-study) | 자연어로 심문하고 증거를 교차검증하는 추리 게임. 게임 판정은 규칙 엔진, 대사는 LLM이 담당 | BE·AI 엔진 주 개발 · FastAPI · LangGraph · PostgreSQL · Neo4j · SSE |
| [**Detox-Agent**](https://github.com/GoInWater301/Detox-Agent) | 사용자별 DNS 사용량 집계·차단과 AI 사용 습관 리뷰를 연결한 팀 프로젝트 | WebServer·gRPC 인터페이스·AI 리뷰 연동 · Spring WebFlux · R2DBC · Redis · SSE |

## Term projects & prototypes

수업·교육 프로젝트에서 다룬 구현 주제입니다. 서비스 개발에서 데이터 분석, 하드웨어까지 직접 탐구한 범위를 담았습니다.

| 프로젝트 | 구현 주제 | 기술 |
| --- | --- | --- |
| [**SmartHome-MCP**](https://github.com/LeeSwallow/PNU-TERM_SmartHome-MCP) | MQTT 기기 등록·센서 조회·액추에이터 제어, MCP를 통한 자연어 기기 제어 | Python · FastAPI · MQTT · FastMCP · SQLite · Arduino |
| [**Emotion Diary**](https://github.com/LeeSwallow/PNU-TERM_Emotion-Diary-App) | Android 감정 일기 앱과 MCP 백엔드 | Kotlin · Android · Python · FastMCP · Supabase |
| [**PDF Summarizer**](https://github.com/LeeSwallow/PNU-BOOTCAMP_PDF-Summarizer) | PDF 업로드·뷰어·페이지 영역 선택·요약 생성 흐름 | Python · FastAPI · 웹 클라이언트 |
| [**Pomodoro Todo**](https://github.com/LeeSwallow/PNU-TERM_Pomodoro-Todo-Webapp) | 포모도로와 할 일을 함께 관리하는 웹 앱 | TypeScript · SvelteKit · Drizzle · SQLite · Docker |
| [**공공데이터 분석**](https://github.com/LeeSwallow/PNU-TERM_elderly-people-Research) | 부산 인구·고령화와 사고 데이터를 탐색하고 지도에 시각화 | Python · pandas · GeoPandas · Folium · Jupyter |
| [**FPGA 두더지 게임**](https://github.com/LeeSwallow/PNU-TERM-logic_circuit-mole_game) | 상태 머신으로 게임 진행·점수·생명·스테이지를 관리하고 키패드·LED·부저를 제어 | Verilog HDL · FPGA · Combo II |

## Research & developer tooling

비공개 저장소에서 진행한 작업은 코드·데이터 링크 없이 주제와 담당 범위만 소개합니다.

| 작업 | 목적과 담당 범위 |
| --- | --- |
| **HeyMoa 개발 하네스** | 팀 공통 개발 도구와 문서 절차 개발. 제품 결정·명세·구현 계획·이슈 마감 흐름을 정리하고 단계별 시간·토큰 사용량을 계측 |
| **HeyMoa 온톨로지 실험** | 회의 정보를 명제·관계·안건으로 표현하는 구조와 검색 방법을 실험. 데이터셋·평가 기준·실험 결과를 관리 |
| **LLM Wiki 도구** | 자료 수집·위키 정리·질의·링크 검사를 연결하는 개인 지식 관리 도구. 소스 수집과 구조 검증 스크립트, 플러그인 구성 |

## Education & recognition

- **부산대학교 컴퓨터공학전공 졸업** · 2024.03–2026.08 · 3.99 / 4.5
- **AI·SW마에스트로 17기** · HeyMoa 팀 프로젝트
- **카카오 테크 캠퍼스 3기** · MoMeet 팀 프로젝트
- **2025 부산대학교 × Upstage AI Agent 해커톤 대상** · 3인 팀
- 정보처리기사 · SQLD · 리눅스마스터 2급

---

<p align="center">
  업무의 규칙을 이해하고, 끝까지 작동하는 서비스를 만드는 팀을 찾습니다.<br />
  <a href="mailto:lmh2157@outlook.kr"><strong>lmh2157@outlook.kr</strong></a>
</p>
