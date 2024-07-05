---
audience: end-user
title: 대상자 작성 활동 사용
description: 대상자 작성 활동을 사용하는 방법 알아보기
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 50%

---


# 대상자 빌드 {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="대상자 빌드 활동"
>abstract="**대상자 빌드** 활동을 통해 구성에 참여할 대상자를 정의할 수 있습니다."

**대상자 빌드** 활동을 통해 구성에 참여할 대상자를 정의할 수 있습니다.

대상자 모집단을 정의하기 위해 수행할 수 있는 작업은 다음과 같습니다.

<!--* Select an existing audience, created as a list in the client console.-->
* Adobe Experience Platform 대상자를 선택합니다.
* 필터링 기준을 정의하고 결합하여 쿼리 모델러 빌더로 새 대상을 작성합니다.

다음 **대상자 작성** 활동은 컴포지션의 시작 부분이나 다른 활동 뒤에 배치할 수 있습니다. 모든 활동은 다음 뒤에 배치할 수 있습니다. **대상자 작성**.

## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="대상자를 선택합니다."

**대상자 빌드** 활동을 구성하려면 다음 단계를 따르십시오.

1. **대상자 빌드** 활동을 추가합니다.
1. 레이블을 정의합니다.
1. **직접 만들기** 또는 **대상자 읽기 만들기**&#x200B;로 대상자 유형을 정의합니다.
1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.

>[!BEGINTABS]

>[!TAB 나만의 쿼리 만들기]

자체 쿼리를 만들려면 다음 단계를 수행합니다.

1. **직접 만들기(쿼리)**&#x200B;를 선택합니다.
1. **차원 타겟팅**&#x200B;을 선택합니다. 타겟팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타겟팅하는 모집단을 정의할 수 있습니다. 기본적으로 대상은 수신자에서 선택됩니다.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. **계속을 클릭합니다**.
1. 새 이메일을 디자인할 때 대상을 만드는 것과 같은 방식으로 쿼리 모델러를 사용하여 쿼리를 정의합니다. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB 대상자 읽기]

기존 대상자를 선택하려면 다음 단계를 따르십시오.

1. **대상자 읽기**&#x200B;를 선택합니다.
1. **계속을 클릭합니다**.
1. 새 게재를 디자인할 때 대상을 사용하는 것과 동일한 방법으로 대상을 선택합니다. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
