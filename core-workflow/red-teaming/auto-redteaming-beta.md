---
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

# Auto-Redteaming (beta)

{% hint style="danger" %}
**변경 필요!**&#x20;

\- docs 프로덕션 내용은 아직 미사용 예정으로 최신화가 안되어있을 수 있습니다.

-(beta)가 있는 기능은 event성으로 개발 된 사항으로 정식 배포에 포함되지 않을 수 있습니다
{% endhint %}

### Overview

DATUMO의 **Auto-Redteaming (beta)** 기능은 무해한 시드 문장을 기반으로, AI 모델의 콘텐츠 대응 능력을 자동으로 평가하는 기능입니다.\
이 기능은 실제 공격자가 활용할 수 있는 전략을 시뮬레이션하여, 모델이 잠재적으로 **부적절하거나 위험한 응답을 생성하는지 여부**를 자동으로 검증합니다.

전략 생성, 반복 평가, 결과 판정에 이르는 전 과정을 자동화함으로써, 반복 가능하고 신뢰도 높은 평가 결과를 제공합니다.\
이는 콘텐츠 모더레이션 시스템의 보안성을 사전에 점검하고 강화하는 데 효과적으로 활용될 수 있습니다.

### 기능 설명

{% hint style="info" %}
* **Seed 기반 공격 시뮬레이션**\
  업로드된 무해한 문장을 기반으로 다양한 공격 시나리오를 자동 생성하고, 모델의 응답을 유도합니다.
* **Judge 모델 기반의 자동 평가**\
  생성된 응답은 Judge 모델에 의해 정량적으로 채점되며, 사용자가 설정한 기준 점수(Threshold Score)를 기준으로 **Safe/Unsafe 여부가 판단**됩니다.
* **반복적 전략 평가**\
  시드 문장별로 최대 50회까지 반복 공격을 수행하며, 이 과정을 통해 가장 효과적인 전략 또한 함께 기록됩니다.
* **정량적 리포트 제공**\
  전략별 방어 실패 비율, 평균 점수, 반복 횟수 등 다양한 통계 정보와 함께, 시드 단위 평가 결과를 테이블 형식으로 제공하여 상세한 분석이 가능합니다.
{% endhint %}

## <mark style="color:blue;">① Auto-Redteaming 프로젝트 생성 절차</mark>

#### Step 1. 기능 페이지 진입

좌측 내비게이션 바에서 **\[Auto-Redteaming]** 메뉴를 클릭하여 해당 기능 페이지로 이동합니다.\
기능 사용을 위해 사전 등록된 프로젝트가 없다면, 새 프로젝트를 먼저 생성해야 합니다.

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

***

#### Step 2. 신규 프로젝트 생성

우측 상단의 **\[Add Red Teaming Project]** 버튼을 클릭하여 프로젝트 생성을 시작합니다.\
이 단계에서는 평가 대상 모델, 시드 데이터, 반복 횟수 등 핵심 설정값을 입력하게 됩니다.

*   핵심 설정값

    * [**Upload File**](#user-content-fn-1)[^1]
    * [**Target Model**](#user-content-fn-2)[^2]
    * [**Max Red Teaming Runs**](#user-content-fn-3)[^3]
    * [**Select Taxonomy**](#user-content-fn-4)[^4]

    <figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
프로젝트는 **모든 항목을 정확하게 입력해야만 생성 가능**하며, 한 번 생성된 프로젝트는 삭제할 수 없습니다.\
설정값과 업로드된 시드 데이터를 반드시 사전에 검토하시기 바랍니다.
{% endhint %}

***

#### Step 3. 프로젝트 생성 및 실행

프로젝트 설정이 완료되면 \[Add Red Teaming Project] 버튼을 클릭하여 평가를 시작합니다.\
생성된 프로젝트는 프로젝트 리스트에 추가되며, 시스템 내부에서 자동 평가가 비동기적으로 시작됩니다.

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

***



## <mark style="color:blue;">② 레드티밍 진행 및 결과 확인</mark> &#x20;

#### Step 4. 평가 진행 중

평가가 실행되면 프로젝트 리스트에서 해당 항목의 상태가 **"진행 중"** 으로 표시됩니다.\
상세 페이지에 진입하면, 시드 문장 단위로 진행률을 확인할 수 있는 **진행 바(Progress Bar)** 가 표시되며, 시스템이 공격 전략 생성 → 모델 응답 → Judge 평가의 단계를 자동으로 반복 수행합니다.

<div><figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure></div>

***

#### Step 5. 평가 완료 및 리포트 확인

평가가 완료되면, 프로젝트 상세 화면에서 통계 기반 리포트가 자동으로 제공됩니다.\
리포트에는 전체 프로젝트의 성과를 요약하는 핵심 지표들이 포함되어 있어, 모델의 방어 능력을 직관적으로 파악할 수 있습니다.

**리포트 주요 항목 예시:**

* 모델명, 반복 횟수, Safe/Unsafe 결과 등
* 전략별 취약점 요약 제공

📌 리포트는 모델의 안전성 추세 분석 및 취약 영역 파악에 활용됩니다.

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>



***

#### Step 6. 상세 결과 확인

리포트 하단의 평가 테이블에서는 각 시드 문장에 대한 개별 평가 결과를 확인할 수 있습니다.\
표에는 반복 시도 횟수, 평가 점수, 사용된 전략 등 핵심 정보가 요약되어 표시됩니다.

📌 반복적으로 Unsafe 판정을 받은 시드 문장을 중심으로 대응 전략을 수립하거나, 문제 유형별 성능 개선에 활용할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

***

### **요약**

**Auto-Redteaming**은 AI 모델의 대응 능력을 자동으로 평가하는 기능으로, 다음과 같은 이점을 제공합니다:

* **전 과정 자동화**: 전략 생성부터 평가, 리포트까지 자동 수행
* **공격 전략 다양성**: 다양한 유형의 시나리오를 통해 모델 방어력 실험
* **정량적 평가**: Judge 모델 기반의 객관적 판정 (Safety / Unsafety)
* **상세 리포트 제공**: 전략·시드·Taxonomy별 평가 결과를 통해 취약점 분석 가능

***

#### 🏁 마무리

평가가 완료되었습니다.\
리포트를 바탕으로 모델의 방어 성능을 분석하고, 효과적인 개선 전략을 수립해보시기 바랍니다.



[^1]: * 시드 문장이 포함된 파일을 업로드하세요.

    - _1열 구성의 CSV/XLSX 파일 사용, 첫 행은 자동 제외됩니다._

[^2]: * **공격을 수행할 LLM을 선택하세요.**
    * _등록된 API 기반 모델만 사용 가능합니다._

[^3]: * 문장당 최대 반복 횟수를 설정하세요.\
      (1\~50회까지 가능.)

[^4]: * **위험 콘텐츠 유형을 선택하세요.**\
      (_유해 콘텐츠, 불공정 표현 등 중 1개 선택.)_
