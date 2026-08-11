# Responsible AI와 data protection

## 주요 risk

| Risk | 의미 | 징후 | 완화 방법 |
| --- | --- | --- | --- |
| Fabrication | 근거 없는 내용을 사실처럼 생성 | 존재하지 않는 숫자, citation, 정책 | 원본과 citation 대조, human review |
| Prompt injection | content 안의 악의적 instruction이 원래 목표를 바꿈 | 무관한 작업 수행, data 공개 요구 | 신뢰할 수 있는 source 사용, output 검토 |
| Over-reliance | 사용자가 AI output을 검증 없이 채택 | 중요한 결정에 자동 적용 | 책임자 승인, 업무 위험에 맞는 검토 |
| Sensitive data exposure | prompt나 output에 보호 대상 data 포함 | 공유 범위를 넘는 개인정보나 기밀 | permission, sensitivity label, 공유 대상 확인 |

## Verification 수준 선택

모든 output에 같은 검증 비용을 쓸 필요는 없습니다. 영향도와 되돌릴 수 있는 정도에 따라 검증을 강화합니다.

| 작업 | 적절한 검증 |
| --- | --- |
| 개인 brainstorming | 논리와 관련성 확인 |
| 내부 email 초안 | 수신자, tone, 사실 관계 확인 |
| 임원 보고서 | source와 숫자 대조, 담당자 review |
| 외부 발표나 고객 약속 | citation 원문 확인, 법무 또는 domain owner 승인 |
| 인사, 재무, 안전 관련 결정 | AI 단독 결정을 피하고 정식 review process 적용 |

### Citation 확인

1. Citation이 실제 source를 가리키는지 엽니다.
2. Source가 주장한 내용을 실제로 뒷받침하는지 확인합니다.
3. 작성 시점과 version이 현재 질문에 맞는지 확인합니다.
4. 여러 source가 충돌하면 authoritative source를 우선합니다.

## Data protection이 response를 제한하는 방식

Copilot이 response를 만들 때 사용자의 identity와 resource permission이 적용됩니다. 접근할 수 없는 file은 grounding source가 될 수 없으며, policy가 차단하는 content나 action은 결과에서 제한될 수 있습니다.

!!! note "제한된 결과의 해석"
    원하는 답이 나오지 않는다고 protection을 우회하려 해서는 안 됩니다. 먼저 올바른 account인지, source permission이 적절한지, 필요한 resource를 prompt에 참조했는지 확인합니다.

## Sensitive data를 다루는 순서

- Prompt에 꼭 필요한 data만 포함합니다.
- File의 sharing permission과 sensitivity label을 확인합니다.
- Output을 다른 app이나 Page로 옮길 때 새 공유 범위를 확인합니다.
- 개인정보, credential, 계약 정보가 불필요하게 남지 않았는지 검토합니다.
- 중요한 action은 human owner가 최종 승인합니다.

## 시험 포인트

- 그럴듯한 response는 정확성의 증거가 아닙니다.
- Citation 존재 여부와 citation의 실제 내용 검증은 다른 단계입니다.
- Copilot protection은 기존 permission과 policy를 기반으로 합니다.
- 가장 좋은 완화책은 작업의 risk에 비례한 human review와 최소 권한입니다.