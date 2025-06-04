# Model Configuration

## Overview&#x20;

DATUMO의 모델 설정(Model Settings) 기능은 프로젝트 수행을 위한 핵심 과정으로, 평가에 사용할 다양한 모델을 구성하고 관리할 수 있도록 지원합니다.\
기본 제공되는 모델이 있으며, 사용자는 프로젝트 목적과 상황에 맞추어 별도의 모델을 추가하거나 원하는 모델로 구성을 확장할 수 있습니다.

모델 설정을 통해 다음과 같은 모델을 등록하고 관리할 수 있습니다:

* Target Model: 평가 대상이 되는 모델
* Query Generation Model: 평가를 위한 질문(Query)을 생성하는 모델
* Evaluation Model: 모델 응답을 평가하는 모델

등록된 모든 모델은 프로젝트 생성 및 데이터셋 평가 시 선택하여 활용할 수 있으며, \
필요에 따라 모델 명을 수정하거나 비활성화하여 관리할 수 있습니다.

## 기능 설명

{% hint style="info" %}
* **모델 등록 및 관리**\
  사용자는 원하는 모델을 자유롭게 등록하고, 각 모델의 API 정보 및 평가 방식을 지정할 수 있습니다.
* **유효성 검사**\
  모델 등록 시 API URL과 Key에 대한 유효성 검사가 자동으로 수행되어 잘못된 입력을 사전에 방지합니다.
* **강제 저장 기능**\
  유효성 검사가 불가능하거나 모델 이름이 없는 경우, 임의의 모델명을 입력하여 강제로 저장할 수 있습니다.\
  이 기능은 Response 업로드 데이터 평가(Response Upload Data Evaluation) 과정에서 유용하게 활용됩니다.
* **모델 수정 및 삭제**\
  등록된 모델은 필요에 따라 모델명(Model Name) 만 수정할 수 있습니다.\
  단, 등록된 모델은 삭제도 가능하며, 비활성화(Deactivate)를 통해 목록에서 제외할 수 있습니다.
* **상태 관리 (활성/비활성)**\
  등록된 모델은 활성화(Active) 및 비활성화(Inactive)할 수 있으며, 비활성화된 모델은 평가 항목 선택 목록에서 제외됩니다.
{% endhint %}



## 모델 설정 절차

#### **1단계. 모델 설정 페이지 접속**

좌측 내비게이션 메뉴에서 **\[Model Settings]** 항목을 클릭하여 모델 관리 페이지로 이동합니다.

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>





#### **2단계. 모델 유형 선택**

페이지 상단에서 추가할 모델의 유형을 선택합니다. 각 모델 유형별로 별도의 추가 버튼이 제공됩니다.

* **Target Model :** 이 모델은 평가를 위한 대상 모델입니다. 새로운 프로젝트를 설정할 때 선택할 수 있습니다.
* **Query Generation Model :** 이 모델은 평가에 사용할 질문(Query)을 생성하는 데 사용됩니다. 데이터셋 생성 시 선택할 수 있습니다.
* **Evaluation Model :** 이 모델은 LLM이 생성한 응답을 평가하는 데 사용됩니다. 데이터셋 평가 단계에서 선택할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>





#### **3단계. 모델 정보 입력**

모델 등록을 위해 다음 정보를 입력합니다:\
&#x20; **- Model Name**: 등록할 모델의 이름\
&#x20; **- API Request Name**: API 호출 시 사용할 이름\
&#x20; **- API URL**: 모델의 API 호출 경로(URL)\
&#x20; **- API Key** (Optional): 인증용 Key (필요한 경우 입력)\
&#x20; **- Evaluation Type**: 평가 방식(Standard 또는 RAG 기반)

**참고:** API URL 및 API Key는 입력 시 유효성 검사가 수행됩니다.\
&#x20;        모든 필수 항목이 입력되어야 \[Add] 버튼이 활성화됩니다.

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

#### **4단계. 모델 추가 및 확인**

모든 정보를 입력한 후 \[Add Model] 버튼을 클릭하여 모델을 등록합니다.\
등록된 모델은 목록 상단에 표시되며, "Active" 상태로 관리됩니다.

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>





#### **5단계. 모델 수정 및 비활성화**

* 등록된 모델 옆의 \[Edit] 버튼을 클릭하여 모델 정보를 수정할 수 있습니다.
* 필요 시 토글 스위치를 통해 모델을 비활성화할 수 있습니다. 비활성화된 모델은 이후 평가 대상 목록에서 제외됩니다.

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>







#### 6단계. 모델 수정 및 삭제(선택 사항)

* 모델을 수정하거나 삭제하려는 경우, 다음 절차를 따릅니다.
  * **Edit** 버튼을 클릭하여 수정 모드로 진입합니다.
  * 수정 모드에서는 **모델명 변경** 및 **모델 삭제**가 가능합니다.
* 모델을 삭제하려면, 수정 모드 화면의 좌측 하단에 위치한 **\[Delete]** 버튼을 클릭합니다.\
  삭제된 모델은 복구할 수 없으므로, 삭제 전 반드시 신중하게 검토하시기 바랍니다.
*

<figure><img src="../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

이제  마지막 단계입니다.\
프로젝트 생성하여 평가를 진행해보세요.

