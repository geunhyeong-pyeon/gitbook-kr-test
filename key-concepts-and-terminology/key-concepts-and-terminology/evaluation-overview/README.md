---
icon: diamonds-4
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Evaluation Overview (평가 기능 안내)

{% hint style="info" %}
모델 응답의 품질을 정량적으로 평가하고 모니터링할 수 있도록, 본 제품은 다양한 평가 기능을 제공합니다.\
평가 체계는 **기능 목적에 따른 평가 지표**와, **구체적인 평가 방법론**으로 구성됩니다.
{% endhint %}

## **📌 평가 지표 (What to Evaluate)**

* **BASIC 평가**
  * _<mark style="background-color:blue;">Safety</mark> 평가_: 편향, 차별, 유해 표현 등
  * _<mark style="background-color:blue;">RAG Quality</mark> 평가_: 정보 활용도 및 응답 일관성 (① GT Answer 미존재 시 RAG Quality 평가 지표)
* **RAG Checker 평가** ( <mark style="background-color:blue;">MHTS / RAG Upload</mark> )
  * 검색된 문서와 응답의 정합성(Factual Consistency) 평가
  * RAG 시스템 품질 점검에 특화

## **⚙️ 평가 방법론 (How to Evaluate)**

다양한 평가 항목은 아래의 방법론을 기반으로 구성됩니다:

<table data-column-title-hidden data-view="cards"><thead><tr><th>방법론</th><th>설명</th></tr></thead><tbody><tr><td><strong>Likert 평가</strong></td><td>등급형 척도로 품질을 정성 평가</td></tr><tr><td><strong>AND 연산 평가</strong></td><td>모든 기준 충족 시만 통과</td></tr><tr><td><strong>Weighted Sum 평가</strong></td><td>기준별 가중치 적용 후 종합 점수 산정</td></tr><tr><td><strong>Text Decomposition 평가</strong></td><td>응답을 Claim 단위로 분해하여 판단</td></tr><tr><td><strong>Entailment 기반 평가</strong></td><td>응답이 문서에서 논리적으로 도출되는지 자동 판단</td></tr></tbody></table>

***

## 🔗 **자세한 평가 기준 보기**

> 평가 항목과 적용 방법론에 대한 자세한 내용을 확인하려면 아래 문서를 참고하세요.

{% content-ref url="evaluation-category.md" %}
[evaluation-category.md](evaluation-category.md)
{% endcontent-ref %}

{% content-ref url="evaluation-method.md" %}
[evaluation-method.md](evaluation-method.md)
{% endcontent-ref %}
