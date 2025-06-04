# Flow 2: Context + Query

## Overview

Context + Query 플로우는 문서(Context)와 쿼리(Query)가 모두 포함된 데이터를 기반으로 평가 데이터셋을 구성하는 방식입니다.\
이 플로우에서는 사용자가 보유한 쿼리 데이터를 기반으로, DATUMO가 모델 응답을 생성하고 평가를 자동으로 수행합니다.

이 플로우는 다음과 같은 경우에 적합합니다:

* 내부에서 수집한 질문 데이터가 이미 존재하는 경우
* 사용자 행동 기반 로그 데이터를 평가용으로 활용하고자 할 경우
* 모델 응답 생성 및 평가를 함께 자동화하고자 할 경우

***

## Quick flow:

1. 문서 + 쿼리 포함된 파일 업로드 (CSV 또는 XLSX)
2. 평가 지표 및 생성 타입 선택
3. 샘플 쿼리 확인
4. 데이터셋 이름 설정 및 저장
5. 자동 응답 생성 및 평가 진행

***

## Step-by-step  Flow

### 1. 데이터셋 생성 화면 진입

프로젝트 내 \[Dataset] 탭으로 이동하여 \[New Dataset] 버튼을 클릭합니다. 새 데이터셋 생성을 위한 화면으로 이동하게 됩니다.

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

***





### 2. 평가 지표 및 생성 타입 선택

데이터셋에 적용할 Evaluation Metric과 Generation Type을 선택합니다.\
Evaluation Metric은 해당 데이터셋의 평가 기준을 정의하는 항목으로, 모델의 성능을 어떤 방식으로 측정할지를 결정합니다.\
⚠️ 사전에 \[[Metric Setting Page](../../../setting-up-your-first-project/setting-up-your-first-project/metric-configuration.md)]에서 평가 지표가 등록되어 있어야 선택 가능합니다.

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

***





### 3. 문서 + 쿼리 포함된 파일 업로드

문서(Context)와 쿼리(Query)가 포함된 파일을 업로드합니다.\
업로드된 데이터는 자동으로 청킹 처리되며, 가능할 경우 RAG 시스템과 동일한 전처리 방식을 사용하는 것을 권장합니다.

{% hint style="info" %}
**`Context File Format`**

* **지원 형식**: CSV 또는 XLSX
* **컬럼 구성**: `id` _(선택)_ → `context` _(선택)_ → `query`
{% endhint %}

> 화면 내 \[Context + Query] 샘플 파일을 다운로드하여 형식을 확인할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>





***

### 4. 샘플 쿼리 확인

파일 업로드가 완료되면, 100개의 샘플 쿼리가 자동으로 생성되어 표시됩니다.\
해당 샘플을 통해 데이터 포맷 및 콘텐츠가 정상적으로 반영되었는지 확인해야 합니다.

* 컬럼 순서 및 형식이 요구사항에 맞는지 검토합니다.
* 쿼리 내용이 비어 있거나 비정상적으로 로딩된 항목이 없는지 확인합니다.

문제가 있을 경우, 업로드 파일을 수정하여 다시 업로드할 수 있습니다.

<div><figure><img src="../../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure></div>

***

### 5. 데이터셋 저장

샘플 데이터를 확인하여 업로드된 파일의 형식과 내용이 정상적인지 검토합니다.\
문제가 없을 경우, 데이터셋 이름을 입력하고 저장을 완료하면 **데이터셋 구성이 완료됩니다.**

💡 저장된 데이터셋은 이후 평가 탭에서 바로 사용 가능합니다.

<figure><img src="../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>



### 다음 단계

→ 데이터셋 구성이 완료되었으므로, 이후 평가를 진행할 수 있습니다.

