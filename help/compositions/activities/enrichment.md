---
audience: end-user
title: 데이터 보강 활동 사용
description: 데이터 보강 활동을 사용하는 방법 알아보기
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 47%

---


# 보강 {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="보강 활동"
>abstract="**보강** 활동을 사용하면 데이터베이스의 추가 정보로 타겟팅된 데이터를 보강할 수 있습니다. 일반적으로 활동을 세분화한 후 구성에서 사용됩니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="보강 활동"
>abstract="보강 데이터가 구성에 추가되면 **보강** 활동 이후에 추가된 활동에서 이를 사용하여 비헤이비어, 환경 설정 및 선택 사항을 기준으로 프로필을 별개의 그룹으로 분류할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="링크 정의"
>abstract="작업 테이블 데이터와 페더레이션된 데이터베이스 간의 링크를 만듭니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="보강 조정"
>abstract="조정 매개변수를 설정합니다."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="보강 데이터"
>abstract="구성을 강화하는 데 사용할 데이터를 선택합니다. 보강 데이터의 두 가지 유형, 즉 타겟팅 차원의 단일 보강 속성 또는 테이블 간에 1-N 카디널리티가 있는 링크인 컬렉션 링크를 선택할 수 있습니다."

다음 **데이터 보강** 활동을 사용하면 페더레이션 데이터베이스의 추가 정보를 사용하여 타깃팅된 데이터를 향상시킬 수 있습니다. 이는 일반적으로 세그먼테이션 활동 후 컴포지션에서 사용됩니다.

보강 데이터의 출처는 다음 중 하나일 수 있습니다.

* **동일한 작업 테이블에서** 을(를) 작성 대상으로 지정합니다.

  *고객 그룹을 타겟팅하고 현재 작업 표에 &quot;생년월일&quot; 필드를 추가합니다.*.

* **다른 작업 테이블**:

  *고객 그룹 타겟팅 후 “구매” 테이블의 “수량” 및 “제품 유형” 필드 추가*

보강 데이터가 컴포지션에 추가되면 이후에 추가된 활동에 사용할 수 있습니다. **데이터 보강** 활동 을 통해 고객의 비헤이비어, 환경 설정 및 선택 사항에 따라 고객을 고유한 그룹으로 분류할 수 있습니다.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## 데이터 보강 활동 추가 {#enrichment-configuration}

**보강** 활동을 구성하려면 다음 단계를 따르십시오.

1. **대상자 빌드** 및 **결합** 활동과 같은 활동을 추가합니다.
1. **보강** 활동을 추가합니다.
1. 컴포지션에 여러 개의 전환이 구성된 경우 **[!UICONTROL 기본 세트]** 데이터로 보강할 기본 집합으로 사용할 전환을 정의하는 필드입니다.

## 데이터 보강 추가 {#enrichment-add}

1. 클릭 **데이터 보강 추가** 데이터를 보강하는 데 사용할 속성을 선택합니다.

   데이터 보강 데이터의 두 가지 유형인 대상 차원의 단일 보강 속성이나 컬렉션 링크를 선택할 수 있습니다. 이러한 각 유형은 아래 예제에 자세히 설명되어 있습니다.

   * [단일 보강 속성](#single-attribute)
   * [컬렉션 링크](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## 테이블 간 링크 만들기 {#create-links}

다음 **[!UICONTROL 링크 정의]** 섹션에서는 작업 테이블 데이터와 데이터베이스 간에 링크를 생성할 수 있습니다. 예를 들어 수신자의 계정 번호, 국가 및 이메일이 포함된 파일에서 데이터를 로드하는 경우 이제 국가 테이블에 대한 링크를 생성하여 프로필에서 이 정보를 업데이트해야 합니다.

사용 가능한 링크에는 몇 가지 유형이 있습니다.

* **[!UICONTROL 1개의 단순 카디널리티 링크]**: 기본 세트의 각 레코드는 연결된 데이터의 하나의 레코드에만 연결할 수 있습니다.
* **[!UICONTROL 0 또는 1개의 단순 카디널리티 링크]**: 기본 세트의 각 레코드는 연결된 데이터의 0개 또는 1개 레코드와 연결할 수 있지만 1개 이하여야 합니다.
* **[!UICONTROL N 카디널리티 컬렉션 링크]**: 기본 세트의 각 레코드는 연결된 데이터의 0개, 1개 또는 그 이상의 (N)개 레코드와 연결할 수 있습니다.

링크를 만들려면 다음 단계를 수행합니다.

1. 다음에서 **[!UICONTROL 링크 정의]** 섹션에서 **[!UICONTROL 링크 추가]** 단추를 클릭합니다.

1. 다음에서 **관계 유형** 드롭다운 목록에서 만들려는 링크 유형을 선택합니다.

1. 기본 세트를 연결할 대상을 식별합니다.

   * 데이터베이스의 기존 테이블을 연결하려면 **[!UICONTROL 데이터베이스 스키마]** 다음에서 원하는 테이블을 선택합니다. **[!UICONTROL 대상 스키마]** 필드.
   * 입력 전환의 데이터와 연결하려면 **임시 스키마** 을 클릭하고 데이터를 사용할 전환을 선택합니다.

1. 기본 세트의 데이터를 연결된 스키마와 일치하도록 조정 기준을 정의합니다. 두 가지 유형의 조인 사용 가능

   * **단순 조인**: 특정 속성을 선택하여 두 스키마의 데이터와 일치시킵니다. 클릭 **조인 추가** 및 선택 **Source** 및 **대상** 조정 기준으로 사용할 속성입니다.
   * **고급 조인**: 고급 조건을 사용하여 조인을 만듭니다. 클릭 **조인 추가** 을(를) 클릭하고 **조건 만들기** 단추를 클릭하여 쿼리 모델러를 엽니다.

링크를 사용하는 컴포지션 샘플은 [예](#link-example) 섹션.

## 예시 {#example}

### 단일 보강 속성 {#single-attribute}

여기에서 생년월일과 같은 단일 보강 속성만 추가합니다. 다음 단계를 수행하십시오.

1. **속성** 필드 내부를 클릭합니다.
1. 타겟팅 차원에서 간단한 필드(이 예시에서는 생년월일)를 선택합니다.
1. **확인**&#x200B;을 클릭합니다.

### 컬렉션 링크 {#collection-link}

이보다 복잡한 사용 사례에서는 테이블 간에 1-N 카디널리티가 있는 링크인 컬렉션 링크를 선택합니다. 100$ 미만의 최근 구매 내역 3개를 검색해 보겠습니다. 이렇게 하려면 다음을 정의해야 합니다.

* 보강 속성: **총 금액** 필드
* 검색할 라인 수: 3
* 필터: 100$보다 큰 항목을 필터링합니다.
* 정렬: **주문 날짜** 필드에 대한 하위 정렬

#### 속성 추가 {#add-attribute}

보강 데이터로 사용할 컬렉션 링크를 선택하는 곳입니다.

1. **속성** 필드 내부를 클릭합니다.
1. **고급 속성 표시**&#x200B;를 클릭합니다.
1. **구매** 테이블에서 **총 금액** 필드를 선택합니다.

#### 컬렉션 설정 정의{#collection-settings}

그런 다음 데이터가 수집되는 방식과 검색할 레코드 수를 정의합니다.

1. **데이터 수집 방법 선택** 드롭다운에서 **데이터 수집**&#x200B;을 선택합니다.
1. **검색할 라인(작성할 열)** 필드에 “3”을 입력합니다.

예를 들어 고객의 평균 구매 금액을 도출하려면 대신 **집계된 데이터**&#x200B;를 선택하고 **집계 함수** 드롭다운에서 **평균**&#x200B;을 선택합니다.

#### 필터 정의{#collection-filters}

여기에서 보강 속성의 최대값을 정의합니다. 100$보다 큰 항목을 필터링합니다. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. **필터 편집**&#x200B;을 클릭합니다.
1. 두 필터(**총 금액**&#x200B;이 존재함, **총 금액**&#x200B;이 100 미만임)를 추가합니다. 첫 번째 필터는 가장 큰 값으로 표시되는 NULL 값을 필터링합니다.
1. **확인**&#x200B;을 클릭합니다.

#### 정렬 정의{#collection-sorting}

이제 세 개의 **최신** 구매 항목을 검색하기 위해 정렬을 적용해야 합니다.

1. **정렬 활성화** 옵션을 활성화합니다.
1. **속성** 필드 내부를 클릭합니다.
1. **주문 날짜** 필드를 선택합니다.
1. **확인**&#x200B;을 클릭합니다.
1. **정렬** 드롭다운에서 **내림차순**&#x200B;을 선택합니다.


### 연결된 데이터를 사용한 데이터 보강 {#link-example}

아래 예제는 두 전환 사이에 링크를 만들도록 구성된 컴포지션을 보여 줍니다. 첫 번째 전환은 쿼리 활동을 사용하여 프로필 데이터를 타겟팅하는 반면, 두 번째 전환은 파일 로드 활동을 통해 로드된 파일에 저장된 구매 데이터를 포함합니다.

* 첫 번째 **데이터 보강** 활동은 기본 세트(의 데이터)를 연결합니다. **쿼리** 작업)을 참조하십시오. **파일 로드** 활동. 이를 통해 쿼리가 타겟팅한 각 프로필을 해당 구매 데이터와 일치시킬 수 있습니다.
* 1초 **데이터 보강** 활동은에서 오는 구매 데이터로 구성 테이블의 데이터를 보강하기 위해 추가됩니다. **파일 로드** 활동. 이를 통해 이러한 데이터를 추가 활동에서 사용할 수 있습니다. 예를 들어, 구매 정보를 통해 고객에게 전송된 메시지를 개인화할 수 있습니다.





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
