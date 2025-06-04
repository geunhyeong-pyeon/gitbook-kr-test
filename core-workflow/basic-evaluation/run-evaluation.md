# Run Evaluation

### Overview

***

DATUMO Evaluation 플랫폼에서는 다양한 평가 기능과 함께 평가 실행 과정을 직관적으로 제공합니다.\
본 가이드에서는 비교 모델 설정부터 평가 실행, 그리고 결과 확인까지의 전체 흐름을 단계별로 안내합니다.

👉 평가를 시작하기 전에, 데이터셋의 최종 쿼리 및 컨텍스트는 [평가용 데이터셋 관리](overview-of-evaluation-flows/managing-evaluation-datasets.md) 페이지를 통해 점검하시기 바랍니다.





***

### Step 1. 비교 모델 선택 및 평가 실행

\[Evaluation] 탭으로 이동하여, 평가를 실행할 데이터셋을 선택합니다.\
선택한 데이터셋에 대해 \[Evaluate] 버튼을 클릭하면 평가 실행 설정 화면으로 이동합니다.

설정 화면에서는 평가를 진행할 대상 모델(Target Model)과 비교 모델(Judge Model)을 선택할 수 있습니다.

* **Target Model**: 평가할 주 모델
* **Judge Model**: 비교 기준이 될 보조 모델

모델 선택이 완료되면, 연결된 평가 지표(Evaluation Metric)에 따라 일괄 평가가 자동으로 진행됩니다.

💡 Judge Model을 설정하면, 두 모델의 성능 차이를 비교 분석할 수 있습니다.\
💡 평가 시작 이후 설정 변경은 불가능하므로, 모델 및 지표 선택을 신중히 확인하시기 바랍니다.





***



데이터셋 생성이 완료되면, `Evaluate` 버튼을 클릭하여 평가를 실행할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>



타겟 모델에 대해 비교할 저지(Judge) 모델을 선택합니다.&#x20;

연결된 모델 및 메트릭 기준으로 일괄 평가 실행이 진행됩니다.

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>



***

#### Step 3. 평가 진행 상황 확인

평가 실행 중에는 평가 진행 상태를 상세하게 확인할 수 있습니다.

오류 발생 시 각 오류의 원인을 확인하고, 재시도할 수 있도록 지원됩니다.

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>
