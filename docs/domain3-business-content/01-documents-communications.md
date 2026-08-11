# 문서와 communication 작성

## Prompt에서 새 document 작성

새 document를 만들 때는 audience와 목적, 필수 section, tone, 길이, source를 제공합니다.

```text
신규 고객 onboarding 개선안을 작성해 줘.
대상은 운영 책임자이며 현재 문제, 제안, 기대 효과, risk, 다음 action 순서로 구성해.
연결한 고객 feedback document만 근거로 사용하고 2 page 이내로 작성해.
```

생성된 document는 outline과 초안으로 사용하고, 사실 관계와 조직의 writing standard를 검토합니다.

## 기존 document에서 생성

기존 content를 source로 사용하면 구조와 detail을 다른 audience나 format에 맞게 변환할 수 있습니다.

| Source | 생성 결과 | 변환 기준 |
| --- | --- | --- |
| 상세 project plan | 임원용 brief | decision, risk, 일정 중심으로 압축 |
| 제품 설명서 | 고객 안내 email | 기술 용어를 줄이고 benefit 강조 |
| 조사 보고서 | presentation outline | 핵심 insight와 supporting evidence 분리 |
| Meeting note | action plan | owner, due date, dependency 추출 |

Source에서 생성한다는 것은 단순 요약과 다릅니다. Audience와 목적에 맞춰 재구성하되 원문에 없는 사실을 추가하지 않도록 요구합니다.

## Management summary

Management summary는 전체 document를 읽지 않아도 의사결정에 필요한 정보를 파악하게 해야 합니다.

- 목적과 현재 상태
- 핵심 insight 또는 business impact
- 주요 risk와 dependency
- 필요한 decision
- 다음 action과 owner

!!! tip "좋은 summary"
    Background를 길게 반복하기보다 무엇이 달라졌고, 왜 중요하며, 누가 무엇을 결정해야 하는지를 앞에 둡니다. 숫자는 원문과 대조합니다.

## App 사이에서 data와 insight 이동

Microsoft 365 app은 결과물의 lifecycle에 따라 연결됩니다.

| 시작 | 이동 | 목적 |
| --- | --- | --- |
| Teams meeting recap | Word | 결정과 action을 정식 project document로 발전 |
| Excel analysis | PowerPoint | trend와 chart를 presentation으로 전달 |
| Word proposal | Outlook | stakeholder에게 concise summary와 review 요청 |
| Copilot chat result | Copilot Pages | 결과를 editable collaboration content로 공유 |

### 이동할 때 확인할 것

- 숫자, table, citation이 손실되거나 바뀌지 않았는지 확인합니다.
- 새 app의 audience와 공유 permission을 확인합니다.
- 원본 source link와 version을 유지합니다.
- Destination format에 맞게 길이와 structure를 조정합니다.

## 실무 판단

| 요구 사항 | 적합한 접근 |
| --- | --- |
| 빈 화면에서 기획안 시작 | Prompt로 outline과 draft 생성 |
| 긴 정책을 임원이 빠르게 검토 | Management summary 생성 |
| 기존 자료를 다른 audience에 전달 | Source 기반 rewrite |
| 분석 결과를 발표 자료로 사용 | Excel insight를 PowerPoint로 이동 |

## 정리

- 새 document는 audience, 목적, structure, source를 명확히 합니다.
- 기존 document는 다른 format이나 audience에 맞게 변환할 수 있습니다.
- Management summary는 decision, impact, risk, action 중심입니다.
- App 사이 이동 시 data integrity와 permission을 다시 확인합니다.

!!! info "출처"
    [Microsoft Learn - Microsoft 365 Copilot overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-overview#copilot-features-in-microsoft-365-apps), [Microsoft Support - Draft and add content with Copilot in Word](https://support.microsoft.com/en-us/office/draft-and-add-content-with-copilot-in-word-069c91f0-9e42-4c9a-bbce-fddf5d581541), [Microsoft Learn - Study guide for Exam AB-730](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ab-730#draft-business-documents-and-communications)