---
audience: end-user
title: 조정 활동 사용
description: 조정 활동을 사용하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 39%

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

**조정** 활동을 사용하면 데이터베이스의 데이터와 작업 테이블의 데이터(예: 외부 시스템에서 로드한 데이터) 간의 연결을 정의할 수 있습니다.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

**조정** 활동을 사용하면 미식별 데이터를 기존 리소스에 연결할 수 있습니다. 조정 작업은 조인하려는 데이터가 이미 데이터베이스에 있음을 의미합니다. 예를 들어 어떤 제품을, 어떤 시간에, 어떤 고객이 구매했는지 등을 표시하는 구매 정보를 조정하려면 데이터베이스에는 이미 고객과 제품이 존재해야 합니다.

## 조정 활동 구성 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="스키마"
>abstract="데이터에 적용할 새 스키마를 선택하십시오. 스키마(즉, 타겟팅 차원)을 사용하여 대상 모집단(수신자, 앱 구독자, 운영자, 구독자 등)을 정의할 수 있습니다. 기본적으로 컴포지션 현재 스키마가 선택되어 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="조정 규칙"
>abstract="중복 제거에 사용할 조정 규칙을 선택합니다. 속성을 사용하려면 **단순 속성** 옵션을 선택하고 소스 및 대상 필드를 선택합니다. 쿼리 모델러를 사용하여 자체 조정 조건을 만들려면 **고급 조정 조건** 옵션을 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="타겟팅 차원 선택"
>abstract="스키마(즉, 타겟팅 차원)를 선택하고 조정할 인바운드 데이터의 타겟팅 차원을 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="조정되지 않은 데이터 유지"
>abstract="기본적으로 조정되지 않은 데이터는 아웃바운드 전환에 보관되며 나중에 작업 테이블에서 사용할 수 있습니다. 조정되지 않은 데이터를 제거하려면 **조정되지 않은 데이터 유지** 옵션을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="조정 속성"
>abstract="데이터 조정에 사용할 속성을 선택하고 확인을 선택합니다."

**조정** 활동을 구성하려면 다음 단계를 따르십시오.

1. **조정** 활동을 컴포지션에 추가합니다.

1. **새 스키마**&#x200B;를 선택하십시오. 타겟팅 차원이라고도 하는 스키마를 사용하면 타겟팅된 모집단(수신자, 앱 구독자, 운영자, 구독자 등)을 정의할 수 있습니다.

1. 조정에 사용할 필드를 선택합니다. 조정 기준을 하나 이상 사용할 수 있습니다.

   1. 특성을 사용하여 데이터를 조정하려면 **단순 특성** 옵션을 선택한 다음 **규칙 추가** 단추를 클릭하십시오.
   1. 조정할 **Source** 및 **대상** 필드를 선택하십시오. **Source** 필드. **대상** 필드는 선택한 스키마의 필드에 해당합니다.

      소스와 대상이 같을 때 데이터가 조정됩니다. 예를 들어 **이메일** 필드를 선택하여 이메일 주소를 기반으로 프로필을 중복 제거합니다.

      다른 조정 기준을 추가하려면 **규칙 추가** 단추를 클릭하십시오. 여러 조인 조건이 지정된 경우 데이터를 함께 연결할 수 있도록 모두 를 확인해야 합니다.

      ![](../assets/reconciliation-rules.png)

   1. 다른 특성을 사용하여 데이터를 조정하려면 **고급 조정 조건** 옵션을 선택한 다음 **조건 만들기** 단추를 클릭하십시오. 그런 다음 쿼리 모델러를 사용하여 자신의 조정 조건을 만들 수 있습니다. [쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다](../../query/query-modeler-overview.md)

      ![](../assets/reconciliation-advanced.png)

1. **필터 만들기** 단추를 사용하여 조정할 데이터를 필터링할 수 있습니다. 이렇게 하면 쿼리 모델러를 사용하여 사용자 지정 조건을 만들 수 있습니다.

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
