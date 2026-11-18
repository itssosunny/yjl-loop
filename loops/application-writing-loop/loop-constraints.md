---
type: loop-constraints
loop_name: application-writing-loop
status: active
updated: 2026-11-18
owning_sot: "[[AGENTS.md]]"
---

# Loop Constraints — application-writing-loop

## 1. 핵심 금지선 (Prohibition Lines)
- **사실 왜곡(환각) 금지**: `career/canonical-fact-ledger.md`와 `career/experience-episodes.md`에 없는 연도, 기간, 수치, 수상 실적, 기관명을 임의로 지어내지 않습니다 (관점 3: 도메인 온톨로지 및 모순 검증).
- **사람 승인 관문 우회 금지**: `Gate A (공고 분석) → Gate M (경험 매핑) → Gate W (초안 작성 및 검수)` 순서와 사람의 최종 확인 관문을 건너뛰지 않습니다 (관점 1: 제어 흐름 및 관문 위상).
- **금지 표현 사용 금지**: `ssot/style-lexicon.md` 및 `ssot/evaluator-wording.md`에 등록된 모호한 추측 표현이나 막연한 다짐 표현을 본문에 남기지 않습니다.
