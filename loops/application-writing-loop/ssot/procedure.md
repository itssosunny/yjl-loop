# Procedure — 자기소개서 작성 루프 표준 절차 (`application-writing-loop`)

채용공고 1건을 목표로 자기소개서를 완성할 때는 아래 4단계를 순서대로 실행합니다.
각 실행 결과물은 `runs/<날짜>_<기관명>_<직무명>/` 폴더(및 루트 `초안.md` · `판정결과.md`)에 기록됩니다.

```text
1. Collect (공고 확인) → 2. Analyze [Gate A] → 3. Map [Gate M] → 4. Draft & Check [Gate W] → 사람 최종 승인
```

---

## 1. Collect (공고 및 내 경험 확인)

- 지원할 채용공고의 담당 업무, 자격요건, 우대사항, 자기소개서 문항 및 글자 수 제한을 확인합니다.
- `career/canonical-fact-ledger.md`와 `career/experience-episodes.md`에 기록된 내 경험 사실과 수치를 불러옵니다.

## 2. Analyze → `analysis.md` (`Gate A`)

- 채용공고가 찾는 핵심 역량(KSA: 지식·기술·태도)과 핵심 키워드를 분석하여 `analysis.md`에 정리합니다.
- 지원 기관과 직무에서 내가 어떤 강점으로 기여할지 **한 줄 핵심 메시지(Governing Message)**를 세웁니다.
- 강조할 주장(Claim)과 지어내지 말아야 할 금지 주장(Do-not-claim)을 명확히 구분합니다.

## 3. Map → `mapping.md` (`Gate M`)

- 채용공고의 각 요구사항 행마다 `career/experience-episodes.md`의 에피소드 ID(`EP-001`, `EP-002`, `EP-003`)와 공식 사실 ID(`CF-FACT-001`~`003`)를 1:1로 짝짓습니다 (**관점 4: 요구사항 추적성 그래프**).
- 각 문단에 적용할 작성 틀(`STAR`, `Why-How-What`, `TRACE`)을 지정합니다.

## 4. Draft & Check → `drafts/자기소개서.md` 및 루트 `초안.md` (`Gate W`)

- `ssot/writing-frameworks.md`의 작성 틀과 `mapping.md`의 허용 표현 범위 안에서 자기소개서 본문을 작성합니다.
- 제출용 본문은 반드시 ```` ```text ... ``` ```` 코드 블록 안에 분리하여 글자 수를 정확히 잽니다.
- 초안 작성 후 곧바로 `ssot/checks.md` 및 `기준표.md`에 따라 **검수 판정(`판정결과.md`)**을 실행합니다.
- 미통과 항목이나 사람이 `기준표.md`에 새로 추가한 조건이 있으면 다시 실행 단계로 돌아가 문장을 고칩니다.
