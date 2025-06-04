# Upload file format

### view

DATUMO Evaluation 플랫폼에서는 다양한 평가 플로우에 따라 데이터셋을 구성할 수 있으며, 각 플로우에서 사용하는 파일의 컬럼 구성이 상이합니다.

**본 가이드는 모든 평가 플로우에서 업로드 파일이 갖추어야 할 컬럼의 구조, 필수 여부, 설명을 명확하게 제공합니다.**\
데이터셋 업로드 시 포맷 오류나 컬럼 누락을 방지하고, 원활한 평가 흐름을 지원하기 위해 이 문서를 참고해 주세요.

사용 목적에 따라 적절한 파일 포맷을 준비해야 합니다. 어떤기능을사용하실예정이신가요?

1️⃣ Basic Evaluation\
2️⃣ RAG Checker (MTHS) - Context Only\
3️⃣ RAG Checker (Upload Based)\
4️⃣ Auto-Redteaming Seed Upload

***

{% tabs %}
{% tab title="Basic Evaluation" %}
### 1️⃣ Basic Evaluation Dataset Upload&#x20;

**Basic Evaluation**은 DATUMO Evaluation 플랫폼의 핵심 기능으로, 다양한 형태의 쿼리/응답 데이터를 기반으로 모델의 성능을 자동으로 평가할 수 있습니다.\
사용자가 보유한 데이터 유형에 따라 총 3가지 업로드 플로우 중 하나를 선택해 파일을 준비해야 합니다



### 🧾 용어 설명&#x20;

* `query` : 모델에게 입력으로 주어지는 질문 문장입니다. 직접 평가의 대상은 아니며, 타겟 모델이 응답을 생성하기 위한 기준 정보로 사용됩니다.
* `context` : 모델이 질문에 답할 때 참고하는 문서 정보입니다. context는 실제로 활용된 chunk의 개념과 가낭 유사합니다.
* `response` : 모델이 생성한 응답입니다. 평가 대상이 되는 텍스트이며, \
  정답과 얼마나 일치하는지를 판단합니다.&#x20;
* `Retrived context`



<table><thead><tr><th width="146">구분</th><th>Context-only</th><th>Context+Query / Query-only</th><th>Query+Response</th></tr></thead><tbody><tr><td>내가 가진 데이터</td><td>문서만 있음</td><td>질문 있음 (문서 유/무)</td><td>질문 + 응답 모두 있음</td></tr><tr><td>AI가 하는 일</td><td>쿼리 생성 + 응답 생성 + 평가</td><td>응답 생성 + 평가</td><td>평가만 수행</td></tr><tr><td>필수 컬럼</td><td><a data-footnote-ref href="#user-content-fn-1"><strong>context</strong> <sup>ⓘ</sup></a></td><td>query<sup>ⓘ</sup><br>(옵션: context)</td><td>query, response<sup>ⓘ</sup> , Retrived context 1 <sup>ⓘ</sup><br>(옵션: context 2~4)</td></tr><tr><td>평가 플로우</td><td>문서 업로드 <br>→ 쿼리 생성 <br>→ 응답 생성 <br>→ 평가</td><td>쿼리 업로드 → 응답 생성 → 평가 </td><td>응답 업로드 → 평가만 진행</td></tr></tbody></table>

{% hint style="danger" %}
🧷 업로드 시 유의사항

* 파일 형식: `.csv`, `.xlsx`
* 첫 줄은 **컬럼명(header)**
* 컬럼명은 영어 소문자, 공백 없음
* 각 행(row)은 하나의 평가 단위
{% endhint %}

#### 🔍 어떤 유형을 선택해야 할지 모르겠다면?

> 아래 질문을 스스로에게 던져보세요:

1. 문서만 있어? → ✅ **Context-only**
2. 질문은 있는데, 응답은 없어? → ✅ **Context+Query**
3. 질문이랑 응답 다 있어? → ✅ **Query+Response**
{% endtab %}

{% tab title="RAG Checker (MTHS)" %}
RAG checker는 두가지 형식으로 구분되

{% hint style="info" %}

{% endhint %}
{% endtab %}

{% tab title="RAG Checker (Upload Based)" %}

{% endtab %}

{% tab title="Auto-Redteaming" %}

{% endtab %}
{% endtabs %}



***



[^1]: <sup>모델에 입력되는 질문입니다. 직접 평가의 대상은 아니며, 타겟 모델이 응답을 생성하기 위한 기준 정보로 사용됩니다.</sup>
