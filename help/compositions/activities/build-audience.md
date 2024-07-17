---
audience: end-user
title: 대상자 작성 활동 사용
description: 대상자 작성 활동을 사용하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 40%

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

**대상자 만들기** 활동은 컴포지션의 시작 부분이나 다른 활동 뒤에 배치할 수 있습니다. 모든 활동은 **대상자 빌드** 뒤에 배치할 수 있습니다.

## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="대상자를 선택합니다."

**대상자 빌드** 활동을 구성하려면 다음 단계를 따르십시오.

1. **대상자 빌드** 활동을 추가합니다.
1. 레이블을 정의합니다.
1. 대상을 만들거나 기존 대상을 선택하려는 경우 지정합니다.
1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.

>[!BEGINTABS]

>[!TAB 대상자 만들기]

나만의 대상을 만들려면 다음 단계를 수행합니다.

1. **대상 만들기**&#x200B;를 선택합니다.
1. **스키마**(타겟팅 차원이라고도 함)를 선택합니다. 스키마를 사용하면 작업을 통해 타겟팅되는 모집단(수신자, 계약 수혜자, 운영자, 구독자 등)을 정의할 수 있습니다. 기본적으로 스키마는 수신자에서 선택됩니다.
1. **계속을 클릭합니다**.
1. 쿼리 모델러를 사용하여 쿼리를 정의합니다. [쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다](../../query/query-modeler-overview.md)

>[!TAB 대상자 읽기]

기존 대상자를 선택하려면 다음 단계를 따르십시오.

1. **대상자 읽기**&#x200B;를 선택합니다.
1. **계속을 클릭합니다**.
1. 대상자를 선택합니다.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
