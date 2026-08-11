# Copilot agent 관리

## Agent Store와 새 agent

| 선택 | 사용 시점 |
| --- | --- |
| Agent Store | 이미 검증된 agent가 요구 사항을 충족하고 바로 사용할 수 있을 때 |
| 새 agent 작성 | 고유한 knowledge, instruction, capability, team workflow가 필요할 때 |

새 agent를 만들면 유지관리와 access review가 필요합니다. 먼저 기존 agent를 검색하고 capability와 publisher, permission을 확인합니다.

## Template에서 agent 작성

Template은 일반적인 use case에 맞는 초기 instruction과 구성을 제공해 시작 시간을 줄입니다.

1. 업무 목적에 가까운 template을 선택합니다.
2. Agent의 이름과 설명으로 대상과 역할을 명확히 합니다.
3. 필요한 knowledge source를 연결합니다.
4. Instruction과 capability를 업무 범위에 맞게 조정합니다.
5. Suggested prompt로 대표 작업을 제공합니다.
6. 실제 질문으로 test한 뒤 공유합니다.

## Knowledge 구성

Knowledge는 agent response의 업무 근거가 됩니다.

- 최신이며 authoritative한 source를 선택합니다.
- Agent의 목적과 관련 없는 broad source는 제외합니다.
- Source permission은 agent 사용자의 access와 함께 고려합니다.
- Version owner와 update 주기를 정합니다.
- Test question으로 누락, 충돌, outdated content를 확인합니다.

!!! warning "Agent가 permission을 우회하지 않음"
    Agent를 공유했다고 knowledge source의 permission이 자동으로 공유되는 것은 아닙니다. 사용자가 source에 접근할 수 없으면 기대한 response를 받지 못할 수 있습니다.

## 주요 setting

| Setting | 역할 | 좋은 구성 |
| --- | --- | --- |
| Instruction | Agent의 역할, 범위, behavior 정의 | 해야 할 일과 하지 말아야 할 일, source 우선순위 명시 |
| Capability | Agent가 수행할 수 있는 action이나 tool | 업무에 필요한 최소 capability만 활성화 |
| Suggested prompt | 사용자가 시작할 대표 질문 | 실제 업무 목표와 기대 output이 드러나는 문장 |
| Knowledge | Response를 grounding할 resource | 관리되는 최신 source와 명확한 owner |

## Instruction 작성 예시

```text
당신은 영업 team의 제품 정책 안내 agent다.
연결된 최신 제품 정책만 근거로 답하고 source link를 제공한다.
정책에서 확인되지 않는 가격이나 약속을 추정하지 않는다.
질문이 계약 해석을 요구하면 담당자 검토가 필요하다고 안내한다.
```

## Test와 공유

공유 전에는 정상 질문뿐 아니라 경계 사례도 test합니다.

- Knowledge에 답이 있는 질문
- Knowledge에 답이 없는 질문
- 서로 충돌하는 source에 대한 질문
- Sensitive data를 요구하는 질문
- Agent scope 밖 action을 요청하는 질문

Team member와 공유할 때는 대상 범위를 최소화하고, 설명과 suggested prompt를 제공하며, feedback과 update owner를 정합니다.

## 정리

- 기존 agent가 충족하면 Agent Store를 먼저 사용합니다.
- Template은 시작점이며 knowledge와 instruction을 반드시 업무에 맞춥니다.
- Capability는 최소한으로 구성하고 representative test를 수행합니다.
- Agent 공유와 knowledge permission은 별도로 확인합니다.

!!! info "출처"
    [Microsoft Learn - Build agents by using Agent Builder in Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents), [Microsoft Learn - Agent templates overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-templates-overview), [Microsoft Learn - Set up Agent Store in Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/copilot-agent-store)