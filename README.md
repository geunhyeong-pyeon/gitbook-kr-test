---
icon: house-blank
cover: .gitbook/assets/Frame 3071 (3).png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# What is DATUMO Evaluation

## **DATUMO Evaluation은 무엇인가요?**

**DATUMO Evaluation은 대규모 언어 모델(LLM)의 신뢰성과 안전성을 평가하는** [<sup>**ⓧ**</sup>**자동화 플랫폼**](#user-content-fn-1)[^1]입니다.\
LLM이 실제 서비스에 도입되기 전과 후, 모델이 생성하는 응답의 품질과 리스크를 체계적으로 점검할 수 있도록 설계되었습니다.

이 솔루은 다음과 같은 평가 과정을 하나의 일관된 워크플로우로 제공합니다:

> **평가기준 관리 → 평가 데이터 생성 → 평가 수행 → 결과 분석 → 레드팀 운영**

DATUMO Evaluation은 최신 LLM 평가 연구를 바탕으로, DATUMO 자체의 검증 경험을 반영하여 설계되었습니다.\
객관적인 지표를 기반으로 모델의 품질과 위험 요소를 정량적으로 측정할 수 있으며,\
사용자의 도메인 특성에 맞춰 커스터마이징된 평가 시나리오와 Agent 기반 자동 평가 기능도 지원합니다.\
이를 통해 LLM 검증 업무를 보다 정확하고 효율적으로 수행할 수 있습니다.

***



## **어떤 기능을 제공하나요?**

DATUMO Evaluation은 다음과 같은 핵심 기능을 제공합니다:

| <p><strong>평가기준 관리</strong><br>기본 제공되는 최신 평가 지표(Preset) 외에도, 사용자의 도메인에 특화된 커스텀 기준을 설정할 수 있습니다.</p>               |
| ---------------------------------------------------------------------------------------------------------------- |
| <p><strong>평가 데이터 생성</strong><br>문서 기반 자동 질의 생성을 지원하며, 사용자 정의 파라미터를 통해 다양한 시나리오를 구성할 수 있습니다.</p>                 |
| <p><strong>평가 수행</strong><br>Query-only, Query+Response 등의 다양한 평가 흐름을 지원하며, 모든 과정은 자동화되어 있습니다.</p>               |
| <p><strong>결과 분석</strong><br>대시보드 및 테이블 형태의 시각화를 통해 정량 지표 기반 분석 결과를 확인할 수 있습니다.</p>                              |
| <p><strong>레드팀 운영</strong><br>전략 기반 시나리오 생성, 민감 응답 탐지, Human-in-the-loop 검토 등의 기능을 통해 위험 요소를 사전에 식별할 수 있습니다.</p> |



***

## **어떻게 활용할 수 있나요?**

DATUMO Evaluation은 다음과 같은 목적으로 활용할 수 있습니다.

* 신모델 도입 전 품질/안전성 기준 점검 및 벤치마킹
* RAG 기반 응답의 정합성 및 출처 일치도 평가
* 기업/서비스 맞춤형 평가 기준 설계 및 운영
* 모델 취약성 진단 및 인시던트 대응 체계 마련



***

## Guide **Quick Link**

DATUMO Evaluation의 실제 사용을 위한 가이드는 다음과 같은 순서로 제공됩니다.

**Set up**

<table data-view="cards"><thead><tr><th data-type="content-ref"></th><th data-type="content-ref"></th><th data-type="content-ref"></th><th data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="setting-up-your-first-project/setting-up-your-first-project/account-settings.md">account-settings.md</a></td><td><a href="setting-up-your-first-project/setting-up-your-first-project/model-configuration.md">model-configuration.md</a></td><td><a href="setting-up-your-first-project/setting-up-your-first-project/metric-configuration.md">metric-configuration.md</a></td><td><a href="setting-up-your-first-project/setting-up-your-first-project/create-your-first-project.md">create-your-first-project.md</a></td></tr></tbody></table>

**Evaluation**

<table data-view="cards"><thead><tr><th data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="core-workflow/basic-evaluation/">basic-evaluation</a></td></tr><tr><td><a href="core-workflow/rag-checker/">rag-checker</a></td></tr><tr><td><a href="core-workflow/red-teaming/">red-teaming</a></td></tr></tbody></table>

***



📌 다음 페이지에서는 DATUMO Evaluation에서 사용하는 주요 개념과 용어들을 정리합니다.

[^1]: 대치어 및 용어 확정 필요

    End-to-End Solution(?)\
    All-in-one 솔루션(?)
