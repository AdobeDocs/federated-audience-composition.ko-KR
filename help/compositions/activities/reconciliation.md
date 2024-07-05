---
audience: end-user
title: 조정 활동 사용
description: 조정 활동을 사용하는 방법 알아보기
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 44%

---


# 조정 {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="조정 활동"
>abstract="**조정** 활동을 통해 데이터베이스의 데이터와 작업 테이블의 데이터 간의 링크를 정의할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="조정 필드 선택"
>abstract="조정 필드 선택"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="조정 생성 조건"
>abstract="조정 생성 조건"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="조정 보조 항목 생성"
>abstract="조정 보조 항목 생성"

다음 **조정** 활동을 사용하면 데이터베이스의 데이터와 작업 테이블의 데이터(예: 외부 시스템에서 로드된 데이터) 간의 링크를 정의할 수 있습니다.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

## 모범 사례 {#reconciliation-best-practices}

동안 **데이터 보강** 활동을 사용하면 작성에서 처리할 추가 데이터를 정의할 수 있습니다(다음을 사용할 수 있음). **데이터 보강** 활동은 여러 세트에서 가져온 데이터를 결합하거나 임시 리소스에 대한 링크를 만듭니다. **조정** 활동을 사용하면 미식별 데이터를 기존 리소스에 연결할 수 있습니다.

>[!NOTE]
>조정 작업은 연결된 차원의 데이터가 이미 데이터베이스에 있음을 의미합니다.  예를 들어 어떤 제품을, 어떤 시간에, 어떤 고객이 구매했는지 등을 표시하는 구매 파일을 가져올 경우, 데이터베이스에는 이미 고객과 제품이 존재할 것입니다.

## 조정 활동 구성 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="타겟팅 차원"
>abstract="새로운 타겟팅 차원을 선택합니다. 차원을 사용하여 대상 모집단(수신자, 앱 구독자, 운영자, 구독자 등)을 정의할 수 있습니다. 기본적으로 현재 타겟팅 차원이 선택됩니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="조정 규칙"
>abstract="중복 제거에 사용할 조정 규칙을 선택합니다. 속성을 사용하려면 **단순 속성** 옵션을 선택하고 소스 및 대상 필드를 선택합니다. 쿼리 모델러를 사용하여 자체 조정 조건을 만들려면 **고급 조정 조건** 옵션을 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="타겟팅 차원 선택"
>abstract="조정할 인바운드 데이터의 타겟팅 차원을 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="조정되지 않은 데이터 유지"
>abstract="기본적으로 조정되지 않은 데이터는 아웃바운드 전환에 보관되며 나중에 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="조정 속성"
>abstract="데이터 조정에 사용할 속성을 선택하고 확인을 선택합니다."

다음 단계에 따라 **조정** 활동:

1. 추가 **조정** 활동을 작성에 추가합니다. <!--This activity should be added following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. -->

1. 새로운 타겟팅 차원을 선택합니다. 차원을 사용하면 타겟팅된 모집단(수신자, 앱 구독자, 연산자, 구독자 등)을 정의할 수 있습니다. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions).-->

1. 조정에 사용할 필드를 선택합니다. 조정 기준을 하나 이상 사용할 수 있습니다.

   1. 속성을 사용하여 데이터를 조정하려면 **단순 속성** 옵션을 선택합니다. 다음 **Source** 필드는 조정할 입력 전환에서 사용할 수 있는 필드를 나열합니다. 다음 **대상** 필드는 선택한 타겟팅 차원의 필드에 해당합니다. 소스와 대상이 같을 때 데이터가 조정됩니다. 예를 들어 **이메일** 이메일 주소를 기반으로 프로필을 중복 제거하는 필드입니다.

      다른 조정 기준을 추가하려면 **규칙 추가** 단추를 클릭합니다. 여러 조인 조건이 지정된 경우 데이터를 함께 연결할 수 있도록 모두 를 확인해야 합니다.

   <!--     ![](../assets/workflow-reconciliation-criteria.png)-->

   1. 다른 속성을 사용하여 데이터를 조정하려면 **고급 조정 조건** 옵션을 선택합니다. 그런 다음 쿼리 모델러를 사용하여 자신의 조정 조건을 만들 수 있습니다. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md).-->

1. 를 사용하여 조정할 데이터를 필터링할 수 있습니다. **필터 만들기** 단추를 클릭합니다. 이렇게 하면 쿼리 모델러를 사용하여 사용자 지정 조건을 만들 수 있습니다. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

기본적으로, 조정되지 않은 데이터는 아웃바운드 전환에 유지되고 나중에 사용할 수 있도록 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
