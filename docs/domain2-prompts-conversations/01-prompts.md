# Prompt 작성과 관리

## 효과적인 prompt의 요소

| 요소 | 질문 | 예시 |
| --- | --- | --- |
| Goal | 무엇을 해야 하는가? | 고객 meeting의 management summary 작성 |
| Context | 누구를 위한 어떤 상황인가? | 제품 담당 임원을 위한 주간 보고 |
| Source | 어떤 resource를 근거로 삼는가? | meeting transcript와 분기 계획 document |
| Expectation | 형식, tone, 길이, 기준은 무엇인가? | 5개 bullet, risk와 owner 포함, 간결한 tone |

```text
지난 고객 meeting transcript와 분기 계획 document를 사용해
제품 담당 임원용 management summary를 작성해 줘.
결정 사항, risk, action item과 owner를 5개 이내 bullet로 정리하고,
source에서 확인되지 않는 내용은 추정하지 마.
```

처음부터 완벽한 prompt를 만들기보다 response를 보고 누락된 context나 output 기준을 추가하는 iterative prompting이 효과적입니다.

## 적절한 resource 선택

- 질문과 직접 관련된 최신 file을 우선합니다.
- 중복되거나 오래된 version을 함께 넣어 ambiguity를 만들지 않습니다.
- 조직 내부 사실은 work data, 외부 동향은 web data가 적합합니다.
- 민감한 resource를 참조하기 전 permission과 공유 범위를 확인합니다.
- Source가 여러 개면 우선순위와 충돌 처리 기준을 prompt에 적습니다.

!!! tip "적은 context가 더 나을 때"
    Resource가 많다고 항상 정확해지지 않습니다. 관련성이 낮은 file은 noise가 되므로 task를 뒷받침하는 최소한의 authoritative source를 선택합니다.

## Follow-up prompt

Conversation context를 활용하면 처음부터 모든 내용을 반복할 필요가 없습니다.

- `두 번째 bullet을 재무 관점에서 더 구체화해 줘.`
- `원본에 없는 주장은 제거하고 각 bullet에 source를 표시해 줘.`
- `같은 내용을 고객에게 보낼 email tone으로 바꿔 줘.`

Follow-up이 다른 주제로 크게 이동하면 새 conversation을 시작해 context 혼선을 줄입니다.

## Prompt 저장, 예약, 공유

| 기능 | 적합한 상황 | 확인 사항 |
| --- | --- | --- |
| 저장 | 좋은 prompt를 나중에 다시 사용 | 이름으로 목적을 식별할 수 있는가 |
| 예약 | 정해진 주기로 같은 작업 실행 | source가 최신화되는가, 결과 검토 owner가 있는가 |
| 공유 | team이 검증된 prompt를 재사용 | 개인 정보나 개인 전용 link가 포함되지 않았는가 |

### 예약 전 점검

- 반복 주기와 time zone이 업무 요구와 맞는지 확인합니다.
- 동적으로 갱신되는 source인지 확인합니다.
- 자동 생성 결과를 누가 검토하고 어디에 사용할지 정합니다.
- 더 이상 필요하지 않은 schedule은 중지하거나 삭제합니다.

## 개선이 필요한 prompt

| 문제 | 개선 방향 |
| --- | --- |
| `보고서 써 줘` | audience, source, 목적, 형식 추가 |
| 서로 다른 업무를 한 번에 요청 | 단계별 prompt로 분리 |
| `완벽하게`, `알아서` 같은 모호한 기준 | 평가 가능한 길이, 항목, tone 명시 |
| 최신 수치 요청에 source 없음 | 최신 authoritative resource 참조 |

## 정리

- Goal, context, source, expectation을 명시합니다.
- Task에 직접 관련된 authoritative resource를 선택합니다.
- 검증된 반복 prompt는 저장, 예약, 공유로 운영합니다.
- 자동화해도 output 검토 책임은 사라지지 않습니다.

!!! info "출처"
    [Microsoft Learn - Schedule Copilot prompts](https://learn.microsoft.com/en-us/microsoft-365/copilot/scheduled-prompts), [Microsoft Support - Sharing prompts with a team](https://support.microsoft.com/en-us/topic/sharing-prompts-with-a-team-2fa7a228-8645-4dc4-beec-d75d6d0bc752), [Microsoft Learn - Study guide for Exam AB-730](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ab-730#create-and-manage-prompts-in-microsoft-365-copilot)