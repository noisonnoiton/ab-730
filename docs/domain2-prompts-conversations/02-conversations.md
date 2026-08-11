# Conversation 관리

## 이전 conversation 찾기

Conversation history는 과거의 prompt, response, follow-up context를 이어서 사용할 수 있게 합니다. Topic이나 생성 시점을 기준으로 찾고, 반복 사용할 conversation은 알아보기 쉬운 이름으로 변경합니다.

좋은 이름은 결과물이 아니라 **업무와 기간**을 드러냅니다.

- `Q3 제품 출시 risk 검토`
- `고객 A renewal meeting 요약`
- `주간 운영 보고서 prompt 개선`

## 이름 변경과 삭제

| 작업 | 사용 시점 | 주의 사항 |
| --- | --- | --- |
| 이름 변경 | 자동 생성 이름으로 목적을 식별하기 어려울 때 | team이나 project naming convention 사용 |
| 삭제 | 불필요하거나 잘못된 sensitive data가 포함된 chat | retention과 compliance policy에 따른 처리 차이 확인 |

삭제는 화면에서 conversation을 정리하는 동작과 조직의 전체 compliance record 제거가 항상 같은 의미는 아닙니다. 조직 policy가 적용되는 환경에서는 retention과 eDiscovery 요구 사항을 따릅니다.

## Conversation을 notebook에 추가

Notebook은 관련 conversation과 reference를 한곳에 모아 특정 project나 주제를 지속적으로 탐색하는 데 사용합니다.

### 적합한 사례

- 여러 meeting과 document를 바탕으로 project status 추적
- 시장 조사 conversation과 source를 모아 비교 분석
- 장기간 진행되는 planning의 가정과 결론 유지

### 관리 원칙

- Notebook의 주제를 명확하게 정합니다.
- 관련성이 높은 conversation만 추가합니다.
- 오래되거나 상충하는 source를 구분합니다.
- Notebook의 context를 믿고 끝내지 말고 최종 output의 source를 검증합니다.

## 새 conversation을 시작할 때

다음 상황에서는 기존 chat의 follow-up보다 새 conversation이 명확합니다.

- 업무 목적과 audience가 완전히 달라졌을 때
- 이전 가정이나 잘못된 response가 새 결과에 영향을 주면 안 될 때
- 다른 sensitive data 범위로 작업해야 할 때
- 다른 project의 context가 섞일 가능성이 클 때

!!! tip "시험 포인트"
    단순히 과거 기록을 다시 보는 것은 conversation history, 장기 주제의 conversation과 source를 함께 관리하는 것은 notebook이 적합합니다.