# Domain 1 - 생성형 AI 기본 이해

- **비중 25-30%**
- Microsoft 365 Copilot의 context, chat과 agent, app별 experience, responsible AI와 data protection을 다룹니다.

## 구성

| 문서 | 내용 |
| --- | --- |
| [Microsoft 365의 생성형 AI](01-m365-experiences.md) | 조직 data 보호, context, chat과 agent, app별 capability |
| [Responsible AI와 data protection](02-responsible-ai.md) | fabrication, prompt injection, verification, sensitive data |

## 핵심 판단 흐름

1. 사용자의 업무 목표와 현재 app을 확인합니다.
2. Copilot이 사용할 수 있는 업무 data, web data, 대화 context를 구분합니다.
3. 일회성 대화는 chat, 반복적이고 전문화된 작업은 agent를 고려합니다.
4. response의 근거와 sensitive data 노출 가능성을 검증합니다.

!!! abstract "요약"
    Copilot response는 model만으로 결정되지 않습니다. 현재 app, prompt, Microsoft Graph를 통해 접근 가능한 업무 data, web grounding, 사용자의 permission이 함께 결과를 구성합니다. Copilot은 사용자가 원래 볼 수 없는 조직 data에 새 permission을 부여하지 않습니다.

!!! info "출처"
    [Microsoft Learn - Study guide for Exam AB-730](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ab-730#understand-generative-ai-fundamentals-25-30), [Microsoft Learn - Microsoft 365 Copilot overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-overview)