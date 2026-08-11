# Microsoft 365의 생성형 AI

## Copilot response가 만들어지는 요소

| 요소 | 역할 | 예시 |
| --- | --- | --- |
| Prompt | 사용자의 목표와 요구 사항 | 지난 분기 결과를 임원용으로 요약 |
| App context | 현재 작업 중인 app과 artifact | Word document, Outlook thread, Teams meeting |
| Work data | 사용자가 접근 가능한 조직 정보 | email, file, chat, calendar |
| Web data | 공개 web의 최신 정보 | 시장 동향, 공개 회사 정보 |
| Model | 입력을 해석하고 response 생성 | 요약, 초안, 분석, 변환 |

같은 prompt라도 현재 app과 참조 resource가 다르면 결과가 달라집니다. 업무 자료가 중요한 질문은 file이나 message를 명시적으로 참조해 context를 좁혀야 합니다.

## 조직 정보 보호

Microsoft 365 Copilot은 Microsoft 365 service boundary와 기존 identity, permission, compliance control 안에서 작동합니다.

- 사용자는 원래 접근 권한이 있는 content만 grounding에 사용할 수 있습니다.
- prompt와 response에는 조직의 기존 retention, audit, sensitivity 정책이 적용될 수 있습니다.
- 조직 data가 공개 foundation model을 학습시키는 데 사용되는 것으로 가정해서는 안 됩니다.
- Copilot이 기존 과도한 permission을 고치는 것은 아닙니다. 잘못 공유된 file은 그대로 검색될 수 있으므로 permission hygiene가 필요합니다.

!!! warning "Permission이 핵심"
    Copilot은 access control을 우회하지 않지만, 사용자가 이미 접근 가능한 data를 더 쉽게 발견하게 만들 수 있습니다. 배포 전 oversharing과 sensitive data label을 점검해야 합니다.

## Chat과 agent

| 구분 | Chat experience | Agent experience |
| --- | --- | --- |
| 목적 | 자유로운 질문과 일회성 작업 | 특정 역할이나 반복 workflow 수행 |
| Context | 현재 대화와 사용자가 제공한 resource | 미리 구성한 knowledge, instruction, capability |
| 사용 방식 | 사용자가 매번 prompt를 조정 | 일관된 시작점과 suggested prompt 제공 |
| 적합한 사례 | email 초안, 즉석 요약, 아이디어 생성 | HR 정책 안내, project onboarding, 영업 자료 탐색 |

직접 agent를 만들기 전에 Agent Store에 목적에 맞는 agent가 있는지 확인합니다. 반복되는 지식 범위, instruction, tool이 필요하고 기존 agent로 해결되지 않을 때 새 agent가 적합합니다.

## App별 Copilot experience

| App | 강점 | 대표 작업 |
| --- | --- | --- |
| Outlook | email과 thread context | 답장 초안, 긴 thread 요약, action item 식별 |
| Word | 긴 형식의 document | 초안 작성, rewrite, summary, 기존 file 기반 작성 |
| Teams | meeting과 collaboration context | meeting recap, 질문, 결정과 action item 확인 |
| PowerPoint | slide와 presentation | prompt나 document에서 presentation 생성, slide 수정 |
| Excel | 표와 수치 data | trend 탐색, formula 지원, chart와 insight 생성 |
| Microsoft 365 Copilot | app을 넘나드는 work context | 여러 resource 검색, 통합 요약, Pages와 notebook 활용 |

!!! tip "시험 판단"
    app 선택 문제에서는 입력 data가 어디에 있고 최종 결과물이 무엇인지 봅니다. Meeting discussion은 Teams, email thread는 Outlook, 장문 deliverable은 Word가 자연스러운 시작점입니다.

## 정리

- Response 품질은 prompt, app, work data, web data의 context에 좌우됩니다.
- Copilot은 기존 permission을 존중하지만 oversharing 자체를 해결하지는 않습니다.
- Chat은 범용 대화, agent는 구성된 knowledge와 instruction을 사용하는 반복 업무에 적합합니다.
- Microsoft 365 app마다 현재 artifact에 맞춘 capability가 다릅니다.

!!! info "출처"
    [Microsoft Learn - Microsoft 365 Copilot overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-overview), [Microsoft Learn - Data, Privacy, and Security for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy), [Microsoft Learn - Overview of Microsoft 365 Copilot Chat](https://learn.microsoft.com/en-us/copilot/overview)