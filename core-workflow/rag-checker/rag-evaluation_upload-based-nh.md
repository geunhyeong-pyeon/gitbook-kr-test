# RAG Evaluation\_Upload-based (NH)

(NH 전달용에만 내용 필요)

* 쿼리 및 엔티티 관계(ER) 업로드
* 평가 진행
* 결과 Tableview 확인

***

## Overview

{% hint style="info" %}
RAG Evaluation (Upload-based)는 사용자가 직접 준비한 질문-응답 데이터셋을 업로드하여, 해당 응답이 문서(Context)에 기반하고 있는지를 자동으로 평가하는 기능입니다.\
평가는 다음 두 모델을 활용해 이루어집니다:

* **Decomposition**: 질문 또는 응답을 검증 가능한 단위(Claim)로 분해
* **Entailment**: Claim이 실제 문서 내용에 의해 수반되는지를 판단

이를 통해 생성형 AI의 응답이 실제 문서 기반인지 여부를 정량적으로 판단할 수 있으며, 내부 문서 QA 시스템의 정확도 검증, 모델 비교 평가 등 다양한 용도로 활용됩니다.
{% endhint %}



## Quick Flow

* **파일 업로드**: 평가를 위한 기반 데이터 업로드\
  &#xNAN;_(필수 컬럼: query, expected\_response, model\_response, retrieved\_context1)_
* **모델 선택**: Decomposition 및 Entailment 모델 설정
* **평가 진행**: 업로드된 데이터 기반 자동 평가 실행
* **결과 확인**: Table 형태의 평가 결과 확인 및 다운로드



## **Step-by-step Flow**

### &#x20; 1. RAG Checker 화면 진입

상단 메뉴에서 \[Evaluation > RAG Evaluation (Upload-based)] 항목을 클릭해 평가 화면으로 이동합니다.\
기존 프로젝트 목록이 표시되며, 원하는 프로젝트를 선택해 상세 페이지로 진입할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (122).png" alt="" width="563"><figcaption></figcaption></figure>

### &#x20; 2. 데이터셋 생성 화면 진입

평가를 진행할 프로젝트를 클릭한 후, 상단의 \[Dataset] 탭으로 이동합니다.\
우측 상단의 \[New Dataset] 버튼을 클릭하면 새로운 데이터셋 생성을 시작할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### &#x20; 3. 평가용 파일 업로드

쿼리, 응답, 기대 응답, 문서 문맥이 포함된 평가용 파일을 업로드합니다.\
**지원 형식**: `.csv`, `.xlsx`\
**필수 컬럼**: `query` `expected_response` `target_response` `retrieved_context1`&#x20;

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### &#x20; 4. 샘플 데이터 확인

파일 업로드가 완료되면, 최대 100건의 샘플 데이터가 자동으로 미리보기 형태로 표시됩니다.\
⚠️ 이 화면에서는 **데이터 수정 및 삭제가 불가능**하며, 문제가 있을 경우 파일을 수정한 후 다시 업로드해야 합니다.

<div><figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>업로드 후 샘플로 최대 100개의 데이터 미리보기가 제공됩니다.</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>각 문서는 Data Detail 화면에서 상세 내용을 확인할 수 있습니다.</p></figcaption></figure></div>

### &#x20; 5. 데이터셋 저장

샘플 검수 후, **데이터셋 이름을 입력하고 저장**합니다.\
데이터셋 저장이 완료되면, 해당 프로젝트 내에서 평가 대상으로 바로 사용할 수 있습니다

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption><p>우측 하단 [Upload Full Dataset] 버튼 클릭</p></figcaption></figure>

### **6. 평가 실행**

데이터셋이 저장되면, **\[Start Evaluation]** 버튼이 활성화됩니다.

* 평가에 사용할 모델(Decomposition, Entailment)을 선택한 후
* 다시 한 번 **\[Start]** 버튼을 클릭하면 평가가 시작됩니다.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



### **7. 평가 결과 확인 및 분석**

자동 평가가 완료되면, Table View 화면에서 각 샘플의 평가 결과를 확인하고 상세 분석을 진행할 수 있습니다.

특정 셀을 클릭하면 우측 Detail 패널이 열려, 해당 응답의 세부 평가 내역을 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

지표에대한 자세한 설명을 원하신다면 [#gt-answer-rag-checker](../../key-concepts-and-terminology/key-concepts-and-terminology/evaluation-overview/evaluation-category.md#gt-answer-rag-checker "mention")에서 참고해주시기 바랍니다.

