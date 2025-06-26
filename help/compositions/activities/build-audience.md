---
audience: end-user
title: 대상자 작성 활동 사용
description: 대상자 작성 활동을 사용하는 방법 알아보기
exl-id: 6fad3e49-e654-4f68-a125-50056c4ae980
source-git-commit: 2c706e8c7d7d282f8ef2f00875608f06e35ffdf8
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 29%

---

# 대상자 빌드 {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="대상자 빌드 활동"
>abstract="**대상자 빌드** 활동을 통해 컴포지션에 참여할 대상자를 정의할 수 있습니다."

**대상자 작성** 활동을 통해 컴포지션을 입력할 대상자를 정의할 수 있습니다. 대상자 모집단을 정의하기 위해 수행할 수 있는 작업은 다음과 같습니다.

* 기존 Adobe Experience Platform 대상자를 선택합니다.
* 필터링 기준을 정의하고 결합하여 쿼리 모델러로 새 대상을 만듭니다.

## 대상자 빌드 활동 구성 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="대상자를 선택합니다."

**대상자 빌드** 활동을 구성하려면 다음 단계를 따르십시오.

1. **대상자 빌드** 활동을 추가합니다.
1. 레이블을 정의합니다.
1. 대상을 만들지 또는 기존 대상을 선택할지를 지정합니다.
1. 아래 탭에 자세히 나와 있는 단계에 따라 대상자를 구성합니다.

>[!BEGINTABS]

>[!TAB 대상자 만들기]

나만의 대상을 만들려면 다음 단계를 수행합니다.

1. **대상 만들기**&#x200B;를 선택합니다.
1. **스키마**(타겟팅 차원이라고도 함)를 선택합니다. 스키마를 사용하면 작업을 통해 타겟팅되는 모집단(수신자, 계약 수혜자, 운영자, 구독자 등)을 정의할 수 있습니다. 기본적으로 스키마는 수신자에서 선택됩니다.

   ![](../assets/build-audience-create.png)

1. **계속을 클릭합니다**.
1. 쿼리 모델러를 사용하여 쿼리를 정의한 다음 확인합니다. [쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다](../../query/query-modeler-overview.md)

>[!TAB 대상자 읽기]

기존 대상자를 선택하려면 다음 단계를 따르십시오.

1. **대상자 읽기**&#x200B;를 선택합니다.
1. **계속을 클릭합니다**.

   ![](../assets/build-audience-read.png)

1. 대상자를 선택합니다.

>[!ENDTABS]

>[!NOTE]
>
>**아웃바운드 전환 생성** 옵션을 사용하면 대상 모집단이 비어 있는 경우 활동 실행 끝에 활성화될 아웃바운드 전환을 추가할 수 있습니다.

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
