# Dashboard / Tableview

### &#x20;Overview

***

DATUMO Eval은 평가 결과를 효율적으로 분석하고 개선 인사이트를 도출할 수 있도록, Dashboard와 Table View 두 가지 시각화 도구를 제공합니다.

* **Dashboard**는 모델 성능을 시각적으로 비교 분석할 수 있도록 지원합니다.
* **Table View**는 개별 샘플 단위의 평가 결과를 상세하게 확인할 수 있어, 오류 분석 및 모델 개선 방향 수립에 유용합니다.

***

### Step 1. Dashboard 화면 확인

프로젝트에 진입하면 가장 먼저 Dashboard가 표시됩니다. \
Dashboard에서는 다양한 시각화 도구를 통해 모델 성능을 비교하고 인사이트를 얻을 수 있습니다.

① Category 정확도 비교\
② Metric 정확도 비교\
➂ Evaluation Result 세부 분석\
④ Score Heatmap

<figure><img src="../../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

***

#### ① Category 정확도 비교

모델별 카테고리 성능을 비교할 수 있습니다.\
상황에 따라 두 차트를 번갈아 보며 다양한 관점의 분석이 가능합니다.

* **Bar 차트:** 각 카테고리의 정확도를 모델별로 직접 비교할 수 있습니다
* **Radar 차트**: 지표가 3개 이상일 경우 제공되며, 모델 간 성능의 분포와 패턴을 비교할 수 있습니다

<div><figure><img src="../../../.gitbook/assets/image (79).png" alt="" width="563"><figcaption><p><strong>Bar Chart</strong></p></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (49).png" alt="" width="563"><figcaption><p>Radar Chart</p></figcaption></figure></div>

***

#### ② Metric 정확도 비교

전체 메트릭의 정확도 현황을 모델별로 비교하여 확인할 수 있습니다. \
카테고리와 동일하게 두 차트로 비교하며 분석이 가능합니다.

<figure><img src="../../../.gitbook/assets/image (76).png" alt=""><figcaption><p>② Metric 정확도 비교</p></figcaption></figure>

#### ➂ Evaluation Result 세부 분석

모델별 특정 메트릭의 전체 점수 분포를 막대그래프, 히스토그램 등을 통해 확인할 수 있습니다.\
특정 Rubric 및 세부적인 평가 결과 인사이트를 제공하여, 어떤 이유로 평가 점수가 나오게 되었는지 세부적으로 분석할 수 있는 뷰를 제공합니다.

#### ④ Score Heatmap

기존 데이터에 태그되어있는 Metadata를 기반으로 Score Heatmap을 제공하여 어느 종류의 데이터타입, 상황에서 성능이 낮게 나오는지 파악할 수 있습니다.

<div><figure><img src="../../../.gitbook/assets/image (75).png" alt=""><figcaption><p>➂ Evaluation Result 세부 분석</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (77).png" alt=""><figcaption><p>➂ Evaluation Result 세부 분석</p></figcaption></figure> <figure><img src="../../../.gitbook/assets/image (78).png" alt=""><figcaption><p>④ Score Heatmap</p></figcaption></figure></div>

***

#### Step 2. Table View

모든 대시보드의 그래프는 클릭 시 해당 정보를 세부적으로 알 수 있는 Table View와 연결됩니다. 또한 Table View에서 세부적인 필터 등을 통해 원하는 상황에서의 실제 모델 답변 및 평가 결과를 확인하실 수 있습니다.

<figure><img src="../../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

Basic Evaluation 평가가 완료되었습니다.\
다음은 레드 티밍 평가 방식에 대한 기능 설명도 필요하다면 다음 페이지도 확인 해보세요.
