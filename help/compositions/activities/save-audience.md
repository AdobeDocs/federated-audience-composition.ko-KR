---
audience: end-user
title: 대상자 저장 활동 사용
description: 대상자 저장 활동을 사용하는 방법 알아보기
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 28%

---

# 대상자 저장 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="대상자 저장"
>abstract="이 활동을 사용하여 컴포지션에서 업스트림으로 계산한 모집단에서 새 대상자를 만들 수 있습니다. 생성된 대상자는 대상자 목록에 추가되며 **대상자** 메뉴를 통해 사용할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="아웃바운드 전환 생성"
>abstract="**대상자 저장** 활동 후에 전환을 추가하려면 이 옵션을 사용합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="기본 ID 필드"
>abstract="프로필에 사용할 기본 ID를 선택합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Experience Platform 설명서에서 자세히 알아보십시오."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="ID 네임스페이스"
>abstract="프로필에 사용할 네임스페이스를 선택합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces" text="Experience Platform 설명서에서 자세히 알아보십시오."

**대상 저장** 활동을 사용하면 컴포지션에서 업스트림으로 계산한 모집단에서 새 대상을 만들 수 있습니다. 만든 대상자는 Adobe Experience Platform 대상자 목록에 추가되고 **대상자** 메뉴를 통해 사용할 수 있습니다. [대상자를 사용한 작업 방법 알아보기](../../start/audiences.md)

이 활동은 기본적으로 모집단 그룹을 재사용 가능한 대상으로 전환하여 동일한 컴포지션에서 계산되도록 하는 데 사용됩니다. **대상자 작성** 또는 **결합** 활동과 같은 다른 타깃팅 활동에 연결합니다.

**[!UICONTROL 대상자 저장]** 활동은 새 대상자 스키마와 데이터 집합을 생성합니다. 대상자가 만들어지면 책임자와 조정하여 적절한 데이터 거버넌스 레이블을 할당하십시오. [데이터 사용 레이블에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/labels/user-guide)

>[!IMPORTANT]
>
>**대상자 저장** 활동에는 프로필이 활성화된 스키마와 데이터 세트가 필요합니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}.

## 대상자 저장 활동 구성 {#save-audience-configuration}

**대상자 저장** 활동을 구성하려면 다음 단계를 따르십시오.

1. 컴포지션에 **대상자 저장** 활동을 추가합니다.

   ![](../assets/save-audience.png)

1. 만들 대상자의 레이블을 지정합니다.

   >[!IMPORTANT]
   >
   >대상 레이블은 현재 샌드박스 내에서 고유해야 합니다. 기존 대상자와 동일한 레이블이 될 수 없습니다.

1. 대상 매핑 섹션을 사용하여 새로 만든 대상으로 가져올 필드를 선택합니다. 이렇게 하려면 **대상 매핑 추가**&#x200B;를 클릭한 다음 원본 및 대상 대상 필드를 선택하십시오.

   작업을 반복하여 필요한 만큼 대상 매핑을 추가합니다.

1. 데이터베이스에서 타겟팅된 프로필을 식별하는 데 사용할 기본 ID 및 네임스페이스를 선택하십시오.

   * **기본 ID 필드**: 프로필을 식별하는 데 사용할 필드를 선택합니다. 예를 들어 이메일 주소나 전화번호 등이 있습니다.
   * **ID 네임스페이스**: 프로필을 식별하는 데 사용할 네임스페이스(예: 식별 키로 사용할 데이터 유형)를 선택합니다. 예를 들어 전자 메일 주소를 기본 ID 필드로 선택한 경우 ID 네임스페이스 **전자 메일**&#x200B;을(를) 선택해야 합니다. 고유 식별자가 전화번호인 경우 ID 네임스페이스 **Phone**&#x200B;을(를) 선택해야 합니다.

## Access Adobe Experience Platform에서 대상자에 액세스 {#access-audience}

컴포지션을 실행한 후에 생성된 대상자는 Adobe Experience Platform에 외부 대상자로 저장되며, Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer에서 사용할 수 있습니다. 이 기능은 **대상자** 메뉴에서 액세스할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

생성된 대상에는 대상자 매핑 섹션에서 선택한 모든 필드가 포함됩니다. Journey Optimizer에서 이 대상을 타기팅하거나 Adobe Experience Platform에서 지원하는 모든 대상으로 활성화할 수 있습니다.

[Adobe Experience Platform 설명서에서 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
