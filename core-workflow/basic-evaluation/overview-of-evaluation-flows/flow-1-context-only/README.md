# Flow 1: Context-only

## Overview

Context-only 플로우는 평가에 사용할 쿼리(Query)나 응답(Response) 없이, 문서(Context)만 보유한 경우에 활용합니다.\
DATUMO는 업로드된 문서를 기반으로 쿼리를 자동 생성하며, 이후 모델 응답 생성 및 평가까지 전 과정을  수행해합니다.

이 플로우는 다음과 같은 경우에 적합합니다:

* 평가할 질문을 직접 만들기 어려운 경우
* 실제 문서 기반 RAG 평가를 사전 시뮬레이션하고 싶은 경우
* 쿼리 생성 품질 자체를 테스트하고자 하는 경우

***

## Quick flow:

1. 문서(Context) 업로드: 쿼리 생성을 위한 기반 정보                                                                                                                                                                                                                                                                                                                &#x20;
2. 커스텀 파라미터 설정: 쿼리 생성 방식 결정 (말투, 주제 등)
3. 샘플 쿼리 15건생성 및 확인: 전체 쿼리 생성 전 미리보기
4. 전체 쿼리 생성: 문서 전체 대상 쿼리 생성
5. 데이터셋 저장: 생성된 쿼리 포함된 데이터셋 저장

***

## Step-by-step  Flow

### 1. 데이터셋 생성 화면 진입

프로젝트 내 \[Dataset] 탭으로 이동하여 \[New Dataset] 버튼을 클릭합니다. 새 데이터셋 생성을 위한 화면으로 이동하게 됩니다.

<figure><img src="../../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>



***

### 2. 평가 지표 선택

데이터셋에 적용할 Evaluation Metric을 선택합니다.\
Evaluation Metric은 해당 데이터셋의 평가 기준을 정의하는 항목으로, 모델의 성능을 어떤 방식으로 측정할지를 결정합니다.\
⚠️ 사전에 \[[Metric Setting Page](../../../../setting-up-your-first-project/setting-up-your-first-project/metric-configuration.md)]에서 평가 지표를 등록해두어야 선택 가능합니다.

<figure><img src="../../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>



***

평가용 쿼리 생성을 위해 문서(Context)를 업로드합니다. 업로드된 문서는 자동으로 청킹 처리되며, RAG 시스템과 동일한 기준을 적용하는 것을 권장합니다.

<figure><img src="../../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
파일 형식 요구사항

Context 파일은 단일 컬럼(context) 형식으로 준비해야 하며, 샘플 파일을 다운로드하여 형식을 확인할 수 있습니다.

***

**① Context-only 파일**

* 단일 컬럼 : `context`&#x20;
* 파일 포맷: `.csv` 또는 `.xlsx`
*   예시:

    | context                                  |
    | ---------------------------------------- |
    | 이 상품은 최대 2억원까지 대출이 가능하며, 조건은 다음과 같습니다... |
{% endhint %}



***

### 4. 쿼리 생성 모델 선택

업로드된 문서를 기반으로 쿼리를 생성할 AI 모델을 선택합니다. 선택한 모델은 생성 결과의 품질에 직접적인 영향을 미치므로 신중히 선택해야 합니다.

<figure><img src="../../../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>



### 5. 커스텀 파라미터 설정 (옵션)

***

쿼리 생성을 보다 정밀하게 제어하기 위해 다양한 커스텀 파라미터를 설정할 수 있습니다.\
이를 통해 실제 사용자 질문처럼 자연스럽고, 평가 목적에 부합하는 쿼리를 생성할 수 있습니다.

* **Tone**: 질문의 말투를 지정합니다. (예: 일반체, 반말체, 화난 말투 등)
* **Topic**: 질문 주제를 설정하여 특정 도메인 성능을 테스트합니다. (예: 대출, 보험, 카드 발급 등)
* **User Persona**: 질문하는 사용자의 유형을 정의합니다. (예: 일반 고객, 전문 컨설턴트 등)
* **Intent Variation**: 질문 의도를 모호하게 설정하여 모델의 이해력과 유연성을 평가합니다. (예: 오타 포함, 문맥 오류 삽입 등)

커스텀 파라미터의 상세한 설정 방법은 [setting-custom-parameters.md](setting-custom-parameters.md "mention") 페이지를 참고해주시기 바랍니다.

<figure><img src="../../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>



### 6. 샘플 쿼리 확인

***

설정한 조건에 따라 AI가 생성한 **15개의 샘플 쿼리**를 미리 확인할 수 있습니다.\
톤, 길이, 주제 등이 기대하는 기준에 부합하는지 검토하고, 필요 시 파라미터를 수정하여 재생성할 수 있습니다.

<figure><img src="../../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>





### 7. 전체 쿼리 생성 및 데이터셋 저장

***

데이터셋 이름을 입력하고 저장을 완료하면, 전체 문서를 기준으로 쿼리가 자동 생성되며 데이터셋이 최종 구성됩니다.

<figure><img src="../../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

### 다음 단계

→ 데이터셋 구성이 완료되었으므로, 이후 평가를 진행할 수 있습니다.



***

