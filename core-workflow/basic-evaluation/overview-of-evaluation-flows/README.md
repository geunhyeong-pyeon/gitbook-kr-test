# Overview of Evaluation Flows



## Overview of Evaluation Flows

DATUMO의 기본 평가는 사용 가능한 데이터 형태에 따라 아래 3가지 흐름으로 나뉩니다:

<table><thead><tr><th width="178">평가 플로우 유형</th><th>보유 중인 데이터</th><th>설명</th></tr></thead><tbody><tr><td><strong>Context-only</strong></td><td>Context only<br>참고 문서만 있음</td><td>문서 기반으로 LLM이 쿼리를 생성하고, 응답 생성 및 평가까지 자동 진행됩니다.</td></tr><tr><td><strong>Context + Query</strong></td><td>Context + Query<br>문서와 쿼리는 있음, 응답은 없음</td><td>사용자가 쿼리를 제공하고, LLM이 응답을 생성한 뒤 평가를 수행합니다.</td></tr><tr><td><strong>Query + Response</strong></td><td>Query + Response only<br>쿼리와 응답 모두 있음</td><td>기존 데이터를 기반으로 평가만 빠르게 수행합니다.</td></tr></tbody></table>

➡ 본인의 데이터 형태에 맞는 플로우를 선택한 후, '[managing-evaluation-datasets.md](managing-evaluation-datasets.md "mention")’부터 공통 흐름으로 진행해 주세요.

### 관련 가이드

{% content-ref url="uploading-documents-and-generating-queries.md" %}
[uploading-documents-and-generating-queries.md](uploading-documents-and-generating-queries.md)
{% endcontent-ref %}

{% content-ref url="flow-1-context-only/setting-custom-parameters.md" %}
[setting-custom-parameters.md](flow-1-context-only/setting-custom-parameters.md)
{% endcontent-ref %}

{% content-ref url="managing-evaluation-datasets.md" %}
[managing-evaluation-datasets.md](managing-evaluation-datasets.md)
{% endcontent-ref %}
