---
hidden: true
---

# Red-Teaming Overview

* 자동레드티밍 개념
* 레드티밍 운영 프레임워크

()

#### 1. 레드팀(Red Team)이란?

* **기원**: 군사 전략에서 출발, ‘공격자 역할’을 수행하며 방어 시스템의 취약점을 파악하기 위한 팀
* **용어 유래**: 냉전기 미 국방부가 소련을 모의 공격하는 팀을 "Red Team", 미국을 방어하는 팀을 "Blue Team"이라 명명

***

#### 2. AI 레드팀의 개념

* **AI 시스템을 공격하는 모의 적대자 역할**
* 다양한 방식으로 AI의 취약한 반응을 유도하여 **안전성과 윤리성**을 검증
* 실제 악성 사용자(해커, 범죄자 등)의 관점에서 시스템을 시험함

#### 3. 레드티밍 방식 비교

<table><thead><tr><th width="133.79998779296875">항목</th><th>수동 레드티밍</th><th>자동 레드티밍</th></tr></thead><tbody><tr><td>수행 주체</td><td>사람 중심 (연구자, 보안 전문가 등)</td><td>코드 기반 자동화</td></tr><tr><td>전략 생성</td><td>수작업 (브레인스토밍, 실험)</td><td>프롬프트 조합 자동 생성</td></tr><tr><td>반복성</td><td>낮음</td><td>높음</td></tr><tr><td>속도</td><td>느림</td><td>빠름</td></tr><tr><td>확장성</td><td>제한적</td><td>고확장 가능</td></tr></tbody></table>

#### 4. 레드티밍 운영 프레임워크 (수동)

* 시나리오 기획 → 공격 쿼리 생성 → 모델 응답 수집 → 수동 평가 → 대응 방안 도출
* 일반적으로 소수 전문가가 인위적으로 수행
* 효과적이지만 **노동집약적이며 확장성이 낮음**

***

#### 5. 자동 레드티밍 개념

* 수동 레드티밍의 한계를 보완하기 위해 **AI 기반 자동화된 테스트 시스템**
* 기본 흐름:
  1. 무해한 시드 문장 입력
  2. 자동으로 공격 프롬프트 생성
  3. 타겟 모델 응답 분석 및 평가
  4. 성공 시나리오 저장
* 공격 전략 라이브러리 + 자동 평가기(Judge LLM)를 조합한 시스템
