---
icon: dagger
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Red-Teaming

### Red-Teaming이란?

**Red-Teaming**은 인공지능 시스템에 대한 **적대적 시뮬레이션 공격**을 통해, 모델의 **안전성과 신뢰성**을 검증하는 프로세스를 말합니다. AI가 실제 서비스 환경에서 해를 끼치지 않도록 사전에 문제 가능성을 점검하는 중요한 활동입니다.

### Red-Teaming 방식의 분류

Red-Teaming은 운영 방식에 따라 두 가지 형태로 나뉩니다:

#### 1. Red-Teaming Framework (수동)

* 연구자, 평가자 등 **사람 중심**의 수작업 테스트
* 전략 구상부터 공격, 결과 평가까지 수동 수행
* 고난도 시나리오와 창의적 판단이 필요한 테스트에 적합

👉 자세히 보기 → [Red-Teaming Framework](./#id-1.-red-teaming-framework)

***

#### 2. Auto-Redteaming (beta)

* 전략 조합, 공격 수행, 평가까지 **자동화된 테스트 시스템**
* 사전 정의된 시드 문장을 기반으로 다양한 공격 쿼리 자동 생성
* 반복 가능한 대규모 테스트와 통계 분석에 적합

👉 자세히 보기 → [Auto-Redteaming (beta)](./#id-2.-auto-redteaming-beta)





### 수동 vs 자동 방식 비교

<table><thead><tr><th width="152.20001220703125">항목</th><th>Red-Teaming Framework</th><th>Auto-Redteaming</th></tr></thead><tbody><tr><td>전략 생성</td><td>사람(수동)</td><td>시스템(자동)</td></tr><tr><td>실행 방식</td><td>수작업 쿼리 입력</td><td>반복적 쿼리 생성</td></tr><tr><td>평가 방식</td><td>수동 검수</td><td>자동 채점 (Judge 모델)</td></tr><tr><td>장점</td><td>유연성, 고차원 테스트</td><td>속도, 반복성, 확장성</td></tr><tr><td>적합 사례</td><td>실험적 시나리오</td><td>대규모 안전성 검증</td></tr></tbody></table>
