---
audience: end-user
title: 증분 쿼리 활동 사용
description: 증분 쿼리 활동을 사용하는 방법을 알아봅니다
hide: true
hidefromtoc: true
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 21%

---

# 증분 쿼리 {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="증분 쿼리"
>abstract="**증분 쿼리** 활동을 사용하면 쿼리 모델러를 사용하여 데이터베이스를 쿼리할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타겟팅할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="증분 쿼리 기록"
>abstract="증분 쿼리 기록"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="증분 쿼리 처리된 데이터"
>abstract="증분 쿼리 처리된 데이터"

다음 **증분 쿼리** 활동을 사용하면 일정에 따라 데이터베이스를 쿼리할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타겟팅할 수 있습니다.

다음 **[!UICONTROL 증분 쿼리]** 활동은 다양한 용도로 사용할 수 있습니다.

* 메시지, 대상자 등의 타겟을 정의하기 위한 개인 세그먼트화.
* 데이터를 내보내는 중입니다. 예를 들어 활동을 사용하여 파일에서 새 로그를 정기적으로 내보낼 수 있습니다. 이 기능은 외부 보고 또는 BI 도구에서 로그 데이터를 사용하려는 경우 유용할 수 있습니다.

이전 실행에서 이미 타겟팅한 모집단은 컴포지션에 저장됩니다. 즉, 동일한 템플릿에서 시작된 두 개의 컴포지션이 동일한 로그를 공유하지 않습니다. 그러나 동일한 구성에서 동일한 증분 쿼리를 기반으로 하는 두 작업은 동일한 로그를 사용합니다.

증분 쿼리의 결과가 실행 중 0과 같은 경우 쿼리가 다음에 프로그래밍될 때까지 작성이 일시 중지됩니다. 따라서 증분 쿼리 다음에 오는 전환 및 활동은 다음 실행 전에 처리되지 않습니다.

## 증분 쿼리 활동 구성 {#incremental-query-configuration}

다음 단계에 따라 **증분 쿼리** 활동:

1. 추가 **증분 쿼리** 활동을 작성에 추가합니다.

1. 다음에서 **[!UICONTROL 대상자]** 섹션에서 다음을 선택합니다. **타겟팅 차원** 그런 다음 을 클릭합니다. **[!UICONTROL 계속]**.

   타겟팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타겟팅하는 모집단을 정의할 수 있습니다. 기본적으로 대상은 수신자에서 선택됩니다. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. 새 이메일을 디자인할 때 대상을 만드는 것과 같은 방식으로 쿼리 모델러를 사용하여 쿼리를 정의합니다. [쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다](../../query/query-modeler-overview.md)

1. 다음에서 **[!UICONTROL 처리된 데이터]** 섹션에서 사용할 증분 모드를 선택합니다.

   * **[!UICONTROL 이전 실행의 결과 제외]**: 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다.

     이전 실행에서 이미 타겟팅한 레코드는 타겟팅한 날로부터 최대 일 수로 기록할 수 있습니다. 이렇게 하려면 **[!UICONTROL 기록(일)]** 필드. 이 값이 0이면 수신자는 로그에서 삭제되지 않습니다.

   * **[!UICONTROL 날짜 필드 사용]**: 이 옵션을 사용하면 특정 날짜 필드를 기반으로 이전 실행에서 결과를 제외할 수 있습니다. 이렇게 하려면 선택한 타겟팅 차원에 사용할 수 있는 속성 목록에서 원하는 날짜 필드를 선택합니다. 컴포지션의 다음 실행에서는 마지막 실행 날짜 이후에 수정되거나 만들어진 데이터만 검색됩니다.

     컴포지션의 첫 번째 실행 후 **[!UICONTROL 마지막 실행 일자]** 필드를 사용할 수 있습니다. 다음 실행에 사용될 날짜를 지정하며, 컴포지션이 실행될 때마다 자동으로 업데이트됩니다. 필요에 맞게 새 값을 수동으로 입력하여 이 값을 재정의할 수 있습니다.

   >[!NOTE]
   >
   >다음 **[!UICONTROL 날짜 필드 사용]** 모드에서는 선택한 날짜 필드에 따라 보다 유연하게 대처할 수 있습니다. 예를 들어 지정된 필드가 수정 날짜에 해당하는 경우 날짜 필드 모드에서는 최근에 업데이트된 데이터를 검색할 수 있고, 다른 모드에서는 컴포지션의 마지막 실행 이후 이미 수정되었더라도 이전 실행에서 이미 타겟팅된 레코딩은 제외합니다.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
