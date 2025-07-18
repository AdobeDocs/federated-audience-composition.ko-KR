---
audience: end-user
title: 프로필 저장 활동 사용
description: 프로필 저장 활동을 사용하는 방법 알아보기
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: c76ef4b64a58d3d43e78b489a1efe1a97a8c09f7
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 37%

---

# 프로필 저장 {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="프로필 저장"
>abstract="프로필 저장 활동을 통해 외부 웨어하우스의 데이터를 통합하여 Adobe Experience Platform 프로필을 강화하고, 추가 속성을 통해 고객 프로필을 개선할 수 있습니다. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Experience Platform 스키마 선택"
>abstract="프로필에 대해 Experience Platform 스키마를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="기본 식별 필드 선택"
>abstract="데이터베이스에서 타기팅된 프로필을 식별하는 데 사용할 기본 ID를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Experience Platform 스키마 선택"
>abstract="프로필에 대해 Experience Platform 스키마를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="프로필 업데이트 모드 저장"
>abstract="프로필 저장 활동에 사용할 수 있는 업데이트 모드에는 전체 업데이트와 증분 업데이트가 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="전체 업데이트"
>abstract="전체 업데이트 모드는 강화를 위해 전체 프로필 세트를 업데이트합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="증분 업데이트"
>abstract="증분 업데이트 모드는 마지막 강화가 실행된 이후 수정된 프로필을 업데이트합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="기본 ID 필드"
>abstract="기본 ID 필드는 프로필을 병합하여 강화할 때 진실의 소스를 나타냅니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="필수 필드 기준"
>abstract="필수 필드는 데이터를 내보낼 때 모든 프로필이나 레코드에 대해 작성해야 하는 속성입니다. 필수 필드가 누락된 경우 내보내기가 완료되지 않거나 유효하지 않습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="기본 ID 필드 기준"
>abstract="각 프로필이나 레코드에 대한 고유 식별자입니다. 이를 통해 모든 레코드를 명확히 인식하고 일치시켜 데이터 중복을 방지합니다."

**[!UICONTROL 프로필 저장]** 활동을 사용하면 외부 웨어하우스에서 페더레이션된 데이터로 Adobe Experience Platform 프로필을 보강할 수 있습니다.

이 활동은 일반적으로 데이터를 플랫폼으로 물리적으로 이동하거나 복제하지 않고 추가 속성 및 통찰력을 가져와 고객 프로필을 개선하는 데 사용됩니다.

## [!UICONTROL 프로필 저장] 활동 구성 {#save-profile-configuration}

>[!IMPORTANT]
>
>**프로필 저장** 활동에는 프로필이 활성화된 스키마와 데이터 세트가 필요합니다. 프로필을 활성화하기 위해 데이터 세트를 활성화하는 방법에 대해 알아보려면 [데이터 세트 사용 안내서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}를 읽어 보십시오.
>
>또한 선택한 데이터 세트에 업데이트를 사용하도록 **설정하지 않은**&#x200B;경우 프로필의 데이터는 **대체**&#x200B;됩니다. 데이터 세트에 대한 업데이트를 활성화하는 방법에 대해 알아보려면 [업데이트 사용 안내서](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/enable-upsert)를 읽어 보십시오.

**[!UICONTROL 프로필 저장]** 활동을 구성하려면 다음 단계를 따르십시오.

1. **[!UICONTROL 프로필 저장]** 활동을 컴포지션에 추가합니다.

   ![활동 내에서 프로필 저장 단추가 강조 표시됩니다.](../assets/save-profiles/save-profiles.png){width="1500" zoomable="yes"}

1. 만들 프로필의 레이블을 지정합니다.

   >[!IMPORTANT]
   >
   >대상 레이블은 현재 샌드박스 내에서 고유해야 합니다. 기존 대상자와 동일한 레이블이 될 수 없습니다.

1. 사용할 Adobe Experience Platform 스키마를 선택합니다.

   ![사용 가능한 스키마가 표시됩니다.](../assets/save-profiles/select-schema.png){width="1500" zoomable="yes"}

1. 데이터 강화를 저장할 데이터 세트를 선택합니다.

   ![데이터 집합 드롭다운이 강조 표시됩니다.](../assets/save-profiles/select-dataset.png){width="300" zoomable="yes"}

1. 데이터 세트를 선택하면 데이터베이스에서 프로필을 식별하는 데 사용될 기본 ID 필드를 볼 수 있습니다.

1. 기본 및 필수 ID 필드를 추가하려면 **[!UICONTROL 필드 추가]**&#x200B;를 선택하십시오.

   ![필드 추가 단추가 강조 표시됩니다.](../assets/save-profiles/add-fields.png){width="300" zoomable="yes"}

   매핑할 각 특성에 대해 **Source** 필드(외부 데이터)와 **대상** 필드(스키마 필드)를 지정할 수 있습니다.

   ![Source 및 대상 필드가 강조 표시되어 필드 간 매핑을 만들 위치를 표시합니다](../assets/save-profiles/specify-mapping.png){width="300" zoomable="yes"}

1. 데이터 보강 업데이트 모드를 지정할 수도 있습니다.

   ![업데이트 모드 유형이 표시됩니다.](../assets/save-profiles/select-update-mode.png){width="300" zoomable="yes"}

   | 업데이트 모드 | 설명 |
   | ----------- | ----------- |
   | 전체 업데이트 | 전체 프로필 세트가 보강되도록 업데이트됩니다. |
   | 증분 업데이트 | 마지막 데이터 보강 실행 이후 수정된 프로필만 데이터 보강에 대해 업데이트됩니다. |

   [!UICONTROL 증분 업데이트]를 선택하는 경우 전송할 데이터를 확인하려면 마지막으로 수정한 날짜도 선택해야 합니다.

1. 구성이 완료되면 **시작**&#x200B;을 선택합니다.
