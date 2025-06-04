---
hidden: true
---

# Uploading Documents & Generating Queries

## Overview

***

DATUMO Evaluation 플랫폼에서는 프로젝트 생성 이후, 평가를 진행하기 위해 데이터셋을 구축해야 합니다.\
데이터셋 구축에는 두 가지 플로우가 존재합니다. 사용 목적과 데이터 구성 방식에 따라 적절한 플로우를 선택하여 데이터셋을 준비하고 업로드할 수 있습니다.

* **Context-only 플로우**: 문서(Context)만 제공하고, 평가용 쿼리를 AI를 통해 생성하는 방식
* **Context+Query 플로우**: 문서와 쿼리가 모두 준비된 파일을 업로드하는 방식

두 플로우 중 하나를 선택하여 데이터셋 생성을 진행하시기 바랍니다.



***

### 어떤 플로우로 진행하시겠습니까?

<table data-header-hidden><thead><tr><th width="180.1890869140625">플로우 유형</th><th width="409">설명</th><th>바로가기</th></tr></thead><tbody><tr><td><strong>1️⃣ Context-only</strong></td><td>평가에 사용할 쿼리(Query)나 응답(Response) 없이, 참고 문서(Context)만 보유한 경우. <br>AI를 통해 <strong>쿼리를 생성하여 평가 데이터셋 구성</strong></td><td><a href="uploading-documents-and-generating-queries.md#id-1-context-only">👉튜토리얼</a></td></tr><tr><td><strong>2️⃣ Context+Query</strong></td><td>쿼리(Query)는 보유 중이나, 모델의 응답은 없는 경우. <br><strong>모델 응답 생성과 평가</strong>를 자동으로 진행</td><td><a href="uploading-documents-and-generating-queries.md#id-1-context-only">👉</a><a href="uploading-documents-and-generating-queries.md#id-2-contextquery">튜토리얼</a></td></tr><tr><td><strong>3️⃣ Query+Response</strong></td><td>쿼리와 해당 응답을 모두 보유하고 있어, <br><strong>평가만</strong> 빠르게 진행하고 싶은 경우</td><td></td></tr></tbody></table>



***

### 1️⃣ Context-only 플로우 가이드

본 가이드는 문서만 업로드하고, AI를 통해 쿼리(Query)를 생성하여 평가 데이터셋을 만드는 방식입니다.\
AI 모델을 활용하여 문서 기반 쿼리를 생성하며, 생성된 데이터는 이후 모델 평가에 활용됩니다



#### Step1. Dataset 진입

프로젝트 내 \[Dataset] 탭으로 이동하여 \[New Dataset] 버튼을 클릭합니다. 새 데이터셋 생성을 위한 화면으로 이동하게 됩니다.

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>



***

#### 2단계. Evaluation Metric 및 Generation Type 선택

데이터셋에 적용할 평가 지표(Evaluation Metric)와 생성 타입(Generation Type)을 선택합니다.\
평가 지표는 이 데이터셋이 어떤 기준으로 성능을 평가받을지 결정하는 항목으로, 정확도(Accuracy), 정답 포함 여부(Recall), 랭킹 기준 등을 설정할 수 있습니다.\
⚠️ 사전에 \[[Metric Setting Page](../../../setting-up-your-first-project/setting-up-your-first-project/metric-configuration.md)]에서 평가 지표를 등록해두어야 선택 가능합니다.

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>



***

#### Step3. Base 문서 업로드

평가용 쿼리 생성을 위해 문서(Context)를 업로드합니다. 업로드된 문서는 자동으로 청킹 처리되며, RAG 시스템과 동일한 청킹 방식을 적용하는 것을 권장합니다.

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**`Context File Format`**

Context 파일은 단일 컬럼(context) 형식으로 준비해야 하며, 샘플 파일을 다운로드하여 형식을 확인할 수 있습니다.

***

**① Context-only 파일**

* 단일 컬럼 : `context`&#x20;
*   예시:

    | context    |
    | ---------- |
    | context 내용 |
{% endhint %}



***

#### Step4. Query Generation Model 선택

업로드된 문서를 기반으로 쿼리를 생성할 AI 모델을 선택합니다. 선택한 모델은 생성 결과의 품질에 직접적인 영향을 미치므로 신중히 선택해야 합니다.

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>



#### Step5. Custom Parameter 선택

***

쿼리 생성을 보다 정밀하게 제어하기 위해 다양한 커스텀 파라미터를 설정할 수 있습니다.\
이를 통해 실제 사용자 질문처럼 자연스럽고, 평가 목적에 부합하는 쿼리를 생성할 수 있습니다.

* **Tone**: 질문의 말투를 지정합니다. (예: 일반체, 반말체, 화난 말투 등)
* **Topic**: 질문 주제를 설정하여 특정 도메인 성능을 테스트합니다. (예: 대출, 보험, 카드 발급 등)
* **User Persona**: 질문하는 사용자의 유형을 정의합니다. (예: 일반 고객, 전문 컨설턴트 등)
* **Intent Variation**: 질문 의도를 모호하게 설정하여 모델의 이해력과 유연성을 평가합니다. (예: 오타 포함, 문맥 오류 삽입 등)

커스텀 파라미터의 상세한 설정 방법은 [setting-custom-parameters.md](flow-1-context-only/setting-custom-parameters.md "mention") 페이지를 참고해주시기 바랍니다.

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>



#### Step6. Sample Query 확인

***

설정한 조건에 따라 AI가 생성한 15개의 샘플 쿼리를 미리 확인할 수 있습니다.\
쿼리의 톤, 길이, 주제 등이 기대하는 기준에 부합하는지 검토하고, 필요에 따라 파라미터를 조정합니다.\
💡 이 단계는 전체 쿼리 생성을 진행하기 전, 결과를 사전에 검토하고 튜닝하는 과정입니다.

<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>



#### Step7. 전체 쿼리 생성 및 데이터셋 저장

***

샘플 쿼리가 만족스러울 경우, 업로드된 전체 문서를 기준으로 쿼리를 생성합니다. 생성이 완료된 후 데이터셋 이름을 입력하고 저장하면, 평가용 데이터셋 구성이 완료됩니다.\


💡 완성된 데이터셋은 이후 \[Evaluation] 탭에서 모델 성능 평가에 사용됩니다.

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>



***

### 2️⃣ Context+Query 플로우 가이드

이미 `context`와 `query`가 모두 포함된 데이터를 보유하고 있는 경우, 업로드 후 타겟 모델 응답을 생성하고 평가까지 자동으로 진행됩니다.

***

#### Step1. Dataset 진입

프로젝트 내 \[Dataset] 탭으로 이동하여 \[New Dataset] 버튼을 클릭합니다.

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>



#### Step2. Evaluation Metric & Generation Type 선택

***

데이터셋에 적용할 평가 지표(Evaluation Metric)와 생성 타입(Generation Type)을 선택합니다.\
정확도(Accuracy), 정답 포함 여부(Recall), 랭킹 기준 등의 옵션을 설정할 수 있으며, 사전에 \[Metric Setting] 페이지에서 등록된 항목만 선택이 가능합니다.

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



***

#### Step3. 문서 + 쿼리 포함된 파일 업로드

문서와 쿼리가 모두 포함된 CSV 또는 XLSX 파일을 업로드합니다. 업로드된 데이터는 자동으로 청킹 처리되며, RAG 시스템과 동일한 방식 적용을 권장합니다.

{% hint style="info" %}
**`Context File Format`**

파일 포맷은 `id(선택)` → `context` → `query` 순서로 구성되어 있어야 하며, \
샘플 파일을 다운로드하여 참고할 수 있습니다

***

* **② Context+Query 파일**
  *   파일 포맷 형식

      | 필수 컬럼       | 설명                        |
      | ----------- | ------------------------- |
      | `id` _(선택)_ | 쿼리 식별자 (있으면 첫 번째 컬럼으로 배치) |
      | `context`   | 질문의 근거가 되는 문서 내용          |
      | `query`     | 실제 사용자의 질문                |
  *   **컬럼 순서** : `id`(선택) → `context` → `query`

      | id (optional) | context    | query    |
      | ------------- | ---------- | -------- |
      | 1             | context 내용 | query 내용 |
{% endhint %}



***

#### Step4. Sample Query 확인

업로드 완료 후, 약 15개의 샘플 쿼리가 자동으로 표시됩니다. 데이터 포맷과 내용이 정상적으로 업로드되었는지 확인합니다.

<figure><img src="../../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>



***

#### Step5. Dataset 저장

데이터 내용이 정상적으로 업로드되었는지 확인 후, 데이터셋 이름을 입력하고 저장하면 평가용 데이터셋 구성이 완료됩니다.

💡 저장된 데이터셋은 이후 평가 탭에서 바로 사용 가능합니다.

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>



***

**3️⃣ Query+Response**

이미 쿼리와 응답까지 모두 준비된 경우. 즉시 평가만 수행할 수 있습니다.

**Step 1. Dataset 생성 진입**

**Step 2. Metric & Generation Type 선택**

**Step 3. 평가용 파일 업로드**

* `query`, `response` (필요시 `context`) 포함된 파일
* 문서가 없더라도 평가 가능 (context는 선택사항)

예시 포맷:

```
scss복사편집id (옵션), query, response, context (옵션)
```

**Step 4. 샘플 데이터 확인 후 저장**

**Step 5. 평가 진행**

* 모델 응답 재생성 없이, 기존 응답을 기준으로 평가만 수행
