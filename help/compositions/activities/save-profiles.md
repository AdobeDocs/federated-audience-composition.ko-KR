---
audience: end-user
title: 프로필 저장 활동 사용
description: 프로필 저장 활동을 사용하는 방법 알아보기
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# 프로필 저장 {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="프로필 저장"
>abstract="프로필 저장 활동을 사용하면 외부 웨어하우스의 데이터를 페더레이션하여 Experience Platform 프로필을 보강할 수 있으므로 추가 속성으로 고객 프로필을 향상시킬 수 있습니다. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="AEP 스키마 선택"
>abstract="프로필에 대한 Experience Platform 스키마를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="기본 ID 필드 선택"
>abstract="데이터베이스에서 타겟팅된 프로필을 식별하는 데 사용할 기본 ID를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="AEP 스키마 선택"
>abstract="프로필에 대한 Experience Platform 스키마를 선택합니다."

**프로필 저장** 활동을 사용하면 외부 웨어하우스에서 페더레이션된 데이터로 Adobe Experience Platform 프로필을 보강할 수 있습니다.

이 활동은 일반적으로 데이터를 플랫폼으로 물리적으로 이동하거나 복제하지 않고 추가 속성 및 통찰력을 가져와 고객 프로필을 개선하는 데 사용됩니다

## 프로필 저장 활동 구성 {#save-profile-configuration}

**프로필 저장** 활동을 구성하려면 다음 단계를 따르십시오.

1. 컴포지션에 **프로필 저장** 활동을 추가합니다.

   ![](../assets/save-profile.png)

1. 만들 프로필의 레이블을 지정합니다.

   >[!IMPORTANT]
   >
   >대상 레이블은 현재 샌드박스 내에서 고유해야 합니다. 기존 대상자와 동일한 레이블이 될 수 없습니다.

1. 사용할 Adobe Experience Platform 스키마를 선택합니다.

   ![](../assets/save-profile-2.png)

1. 데이터베이스에서 프로필을 식별하는 데 사용할 기본 ID 필드를 선택합니다.

1. 추가 데이터 특성을 조정하려면 **특성 추가**&#x200B;를 클릭하세요.

   그런 다음 매핑할 각 특성에 대해 **Source** 필드(외부 데이터)와 **대상** 필드(스키마 필드)를 지정합니다.

   ![](../assets/save-profile-3.png)

1. 구성이 완료되면 **시작**&#x200B;을 클릭하세요.
