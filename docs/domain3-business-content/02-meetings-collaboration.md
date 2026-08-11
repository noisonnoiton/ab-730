# Meeting과 collaboration

## Meeting에서 Copilot 사용

Copilot은 meeting 전후의 업무를 연결하는 데 사용할 수 있습니다.

| 시점 | 대표 작업 |
| --- | --- |
| 전 | Agenda 작성, 관련 file 요약, 질문 준비 |
| 중 | 지금까지의 논의 요약, 찬반 의견 확인, 놓친 내용 질문 |
| 후 | Recap, decision, action item, owner, unresolved question 정리 |

Meeting response의 범위는 transcript와 recording availability, 조직 policy, 사용자의 access에 영향을 받습니다. Copilot summary가 공식 회의록을 자동으로 확정하는 것은 아니므로 participant가 decision과 owner를 검토해야 합니다.

### 좋은 follow-up 질문

- `합의된 decision과 아직 합의되지 않은 항목을 분리해 줘.`
- `각 action item의 owner와 due date를 표로 정리해 줘.`
- `고객이 제기한 risk와 우리 team의 response를 source와 함께 보여 줘.`
- `다음 meeting에서 결정해야 할 질문을 우선순위로 정리해 줘.`

## Copilot Pages

Copilot Pages는 Copilot response를 지속적으로 편집하고 다른 사람과 함께 발전시킬 수 있는 collaboration surface입니다.

### 적합한 상황

- Chat 결과를 일회성 response가 아닌 shared working content로 전환
- 여러 사람이 초안, table, plan을 함께 편집
- 조사 결과와 source를 project artifact로 유지
- Copilot을 사용해 Page content를 계속 보완

### Chat과 Page 구분

| Chat | Copilot Pages |
| --- | --- |
| 질문과 response를 빠르게 반복 | 선택한 결과를 durable content로 구성 |
| 개인 탐색과 초안에 적합 | 공유와 공동 편집에 적합 |
| Conversation 흐름이 중심 | 편집 가능한 artifact가 중심 |

Page로 옮길 때는 필요 없는 prompt나 sensitive detail을 제거하고 공유 범위를 확인합니다.

## Memory와 instruction

| 개념 | 역할 |
| --- | --- |
| Memory | 반복되는 preference나 context를 이후 experience에 활용 |
| Instruction | Copilot이 response를 만드는 방식에 대한 지속적인 지침 |

예를 들어 선호하는 concise tone은 instruction으로 지정할 수 있지만, 특정 분기 보고서의 수치는 현재 source에서 가져와야 합니다. Memory나 instruction을 authoritative fact source처럼 사용해서는 안 됩니다.

!!! warning "지속 context 관리"
    저장된 memory와 instruction은 이후 response에 영향을 줄 수 있습니다. 오래되었거나 더 이상 적절하지 않은 항목을 검토하고 sensitive data를 불필요하게 지속 context로 남기지 않습니다.

## Meeting 결과를 collaboration artifact로 만드는 흐름

1. Teams에서 recap, decision, action item을 생성합니다.
2. Transcript와 participant 확인으로 정확성을 검증합니다.
3. 지속적으로 편집할 내용은 Copilot Page나 Word document로 옮깁니다.
4. 공유 permission과 owner를 설정합니다.
5. 다음 meeting에서 action status를 source와 함께 갱신합니다.

## 정리

- Meeting 전, 중, 후에 Copilot을 사용할 수 있습니다.
- Decision과 action item은 human review 후 확정합니다.
- Copilot Pages는 response를 shared, editable artifact로 전환합니다.
- Memory와 instruction은 지속 context이며 최신 사실의 source를 대신하지 않습니다.