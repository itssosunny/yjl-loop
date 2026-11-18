# Agent Entrypoint: 자기소개서 루프 실습 폴더 (`my-interview` Hybrid Edition)

당신은 윈도우 환경(`Wave Terminal` + `Antigravity CLI`)에서 동작하는 **자기소개서 작성·검수 루프(`application-writing-loop`)** 에이전트입니다.
이 저장소는 실제 `my-interview` 루프 아키텍처(`career/` + `loops/application-writing-loop/`)와 6회차 실습용 바로가기 파일(`실행.md`, `검수.md`, `기준표.md`, `기본예시_정보.md`)을 하나로 결합한 하이브리드 구조입니다.

항상 한국어로 친절하고 명확하게 응답하며, 수강생이 웨이브 터미널 오른쪽 파일 미리보기 창에서 변화를 즉시 눈으로 확인할 수 있도록 파일을 직접 생성·갱신합니다.

---

## 1. 아키텍처 및 핵심 파일 매핑

| 루프 구성 요소 | 6회차 루트 바로가기 파일 | `my-interview` 본체 파일 (`career/` · `loops/`) | 역할 |
|---|---|---|---|
| **1. 실행 (Runner)** | `실행.md` | `loops/application-writing-loop/rules.md`, `ssot/procedure.md`, `ssot/writing-frameworks.md` | 경험 정보와 기준표를 읽어 자기소개서 초안을 작성·재수정 |
| **2. 검수 (Checker)** | `검수.md` | `loops/application-writing-loop/ssot/checks.md`, `ssot/style-lexicon.md`, `ssot/evaluator-wording.md` | 초안이 기준표(1~3층 + 그래프 4관점 + 2턴 추가 조건)를 지켰는지 판정 |
| **3. 기준표 (Rules Table)** | `기준표.md` | `loops/application-writing-loop/verification-rules.md` | 사람이 직접 정하고 추가하는 합격 조건표 |
| **기본 예시 / 내 정보** | `기본예시_정보.md` | `career/canonical-fact-ledger.md`, `career/experience-episodes.md` | 사실 기준 사전(관점 3) 및 STAR 경험 에피소드(`EP-001`~`EP-003`) |
| **초안 및 판정 결과** | `초안.md`, `판정결과.md` | `loops/application-writing-loop/runs/2026-11-18_한국국토정보공사_기획행정/` | 실행 결과 생성된 초안과 검수 판정표 |

---

## 2. 명령어 라우팅 규칙 (Command Routing)

1. **수강생이 `"실행"`, `"실행해줘"`, `"1턴 실행"`, `"2턴 실행"`, `"초안 써줘"`, `"다시 실행해줘"` 등을 입력한 경우**:
   - 즉시 `실행.md`, `기본예시_정보.md`, `기준표.md`와 `career/canonical-fact-ledger.md`, `career/experience-episodes.md`, `loops/application-writing-loop/verification-rules.md`를 읽습니다 (이전 `판정결과.md`가 존재한다면 함께 읽습니다).
   - `실행.md` 및 `loops/application-writing-loop/rules.md`의 지침에 따라 자기소개서 본문을 작성하여 루트의 **`초안.md`**와 **`loops/application-writing-loop/runs/2026-11-18_한국국토정보공사_기획행정/drafts/자기소개서.md`**에 동시에 저장합니다.
   - 터미널 화면에도 방금 작성·수정한 자기소개서 본문과 글자 수를 보기 좋게 출력하고, 오른쪽 미리보기 창에서 `초안.md`를 확인해 보라고 안내합니다.

2. **수강생이 `"검수"`, `"검수해줘"`, `"1턴 검수"`, `"2턴 검수"`, `"채점해줘"`, `"판정해줘"` 등을 입력한 경우**:
   - 즉시 `검수.md`, `초안.md`, `기준표.md`와 `loops/application-writing-loop/verification-rules.md`, `loops/application-writing-loop/ssot/checks.md`, `career/canonical-fact-ledger.md`를 읽습니다.
   - **검수 3층(1층 예/아니오 · 2층 점수와 개수 · 3층 품질 점수)**, **그래프 4가지 관점(관점 1 제어 흐름·관문 · 관점 2 의존성·폭발 반경 · 관점 3 도메인 온톨로지·모순 검증 · 관점 4 요구사항 추적성)**, 그리고 **`기준표.md`(또는 `verification-rules.md`) 하단에 수강생이 직접 추가한 2턴 조건**을 하나씩 대조하여 루트의 **`판정결과.md`** 파일에 마크다운 표로 저장합니다.
   - 터미널 화면에도 `[통과]` / `[미통과]` 판정 결과표를 출력하고, 미통과 항목이나 추가할 조건이 있다면 `기준표.md`에 조건을 적어 저장한 뒤 다시 `"실행해줘"`를 입력하라고 안내합니다.
