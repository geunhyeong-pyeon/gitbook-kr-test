# Flow 3: Query + Response

**3️⃣ Query+Response**

이미 쿼리와 응답까지 모두 준비된 경우. 즉시 평가만 수행할 수 있습니다.



## Overview

Query + Response 플로우는 평가 대상인 모델의 응답(Response)과 이를 평가할 쿼리(Query)를 이미 보유하고 있는 경우에 사용하는 방식입니다.\
이 플로우에서는 별도의 응답 생성 없이, 기존 응답을 기반으로 평가 지표에 따라 직접 평가가 진행됩니다.

응답 생성이 완료된 상태에서 모델 성능을 빠르고 정확하게 검증하고자 할 때 적합합니다.

#### 주요 사용 사례 (Query + Response 플로우)

* 기존 시스템 또는 외부 모델에서 생성된 응답 데이터를 평가하고자 하는 경우
* 서비스 로그, 대화 기록 등 이미 확보된 쿼리–응답 페어를 평가 지표에 따라 분석하려는 경우
* 재생성 없이, 모델의 응답 품질을 빠르게 검증하고자 하는 경우
* 베이스라인 모델 간 성능 비교를 수행하려는 경우



***

## Quick flow

1. 평가용 파일 업로드 (Query + Response 포함)
2. 평가 지표 및 생성 타입 선택
3. 샘플 데이터 확인
4. 데이터셋 이름 설정 및 저장
5. 평가 실행



***

## Step-by Step Flow

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

<div><figure><img src="../../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure></div>

***

### 5. 데이터셋 저장

샘플 데이터를 확인하여 업로드된 파일의 형식과 내용이 정상적인지 검토합니다.\
문제가 없을 경우, 데이터셋 이름을 입력하고 저장을 완료하면 **데이터셋 구성이 완료됩니다.**

💡 저장된 데이터셋은 이후 평가 탭에서 바로 사용 가능합니다.

<figure><img src="../../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>





### 다음 단계

→ 데이터셋 구성이 완료되었으므로, 이후 평가를 진행할 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>



***

