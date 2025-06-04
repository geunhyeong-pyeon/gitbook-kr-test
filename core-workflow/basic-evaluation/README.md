---
icon: vial-virus
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

# Basic Evaluation

## Evaluation Overview

DATUMO에서 프로젝트를 생성한 후, **평가** 단계로 넘어가게 됩니다. 이 단계에서는 모델의 성능을 평가하기 위한 다양한 방식의 **평가 지표**를 설정하고, 평가를 수행할 수 있습니다. 평가 지표는 크게 **BASIC 평가**와 **RAG Checker 평가** 두 가지로 구분되며, 각 항목은 평가 목적에 맞게 선택적으로 활용할 수 있습니다.

***

## 평가 지표

* **BASIC 평가**: 모델의 전반적인 응답 품질을 평가하며, 주로 사용자 경험, 윤리성, 정보 전달 정확성 등에 중점을 둡니다.
* **RAG Checker 평가**: Retrieval-Augmented Generation 방식을 기반으로, 생성된 응답의 정확성과 원본 문서와의 일관성을 평가합니다.

(※ 각 평가 범주는 [Evaluation Category](../../key-concepts-and-terminology/key-concepts-and-terminology/evaluation-overview/evaluation-category.md) 항목에서 자세히 확인할 수 있습니다.)

{% content-ref url="../../key-concepts-and-terminology/key-concepts-and-terminology/evaluation-overview/evaluation-category.md" %}
[evaluation-category.md](../../key-concepts-and-terminology/key-concepts-and-terminology/evaluation-overview/evaluation-category.md)
{% endcontent-ref %}

***

### 빠른 평가 시작 방법

프로젝트가 생성되면, **BASIC 평가**부터 시작할 수 있습니다. \
Evaluation 페이지에서는 프로젝트 단위로 다양한 평가 항목을 실험하고, 대시보드를 통해 평가 결과를 시각화하여 확인할 수 있습니다.\
프로젝트 평가 과정은 **데이터셋 생성** → **검수** → **평가**의 흐름으로 진행됩니다. 각 항목에서는 '빠른 시작' 버튼을 통해 평가를 간편하게 진행할 수 있습니다.

#### Evaluation Test 평가 유형

* [**Basic Evaluation**](overview-of-evaluation-flows/): 모델의 품질을 평가하는 기본적인 방식입니다.
* [**RAG\_MHTS**](../rag-checker/rag-evaluation_mhts-based-beta/)<sup>**pro**</sup>: 특정 검색 기반 평가 방식을 적용하여 평가를 수행합니다.
* [**RAG**](../rag-checker/rag-evaluation_upload-based-nh.md)<sup>**pro**</sup>: 모델의 정확성 및 문서 기반 응답 품질을 평가합니다.
* [**Red-teaming**](../red-teaming/red-teaming-framework.md): 모델의 취약점 및 리스크를 평가하는 방식입니다.
