---
audience: end-user
title: 대상자를 사용한 작업
description: 대상자를 사용한 작업 방법 알아보기
badge: label="제한된 가용성" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: ht
source-wordcount: '311'
ht-degree: 100%

---

# 대상자를 사용한 작업 {#gs-audiences}

Experience Platform 페더레이션된 대상자 구성을 사용하면 다양한 활동을 시각적 캔버스로 활용하여 대상자를 생성하고 이를 Adobe Experience Platform 대상자 포털에 저장할 수 있는 [구성을 만들 수 있습니다](../compositions/gs-compositions.md).

그런 다음 Journey Optimizer에서 이들 대상자를 타겟팅하거나 Adobe Experience Platform에서 지원하는 모든 대상으로 이들 대상자를 활성화할 수 있습니다.

## 컴포지션을 이용한 대상자 생성 {#creation}

페더레이션된 대상자 구성을 사용하여 대상자를 만들려면 **[!UICONTROL 대상자 저장]** 활동을 포함하는 구성을 만들어야 합니다. 이 활동을 통해 대상자 포털에 대상자를 저장하고, 외부 데이터베이스에서 해당 대상자에 포함할 필드를 선택할 수 있습니다. [대상자 저장 활동을 구성하는 방법을 알아봅니다](../compositions/activities/save-audience.md).

Adobe 페더레이션된 데이터 구성을 사용하여 생성된 대상자에는 **[!UICONTROL 대상자 저장]** 활동에서 선택한 모든 필드가 포함되며, 모든 Adobe Experience Platform 대상 고객과 함께 대상자 포털에 저장됩니다.

구성을 실행한 후에 생성된 대상자는 Adobe Experience Platform에 외부 대상자로 저장되며, Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer에서 사용할 수 있습니다.

Adobe Experience Platform에서 지원하는 모든 대상으로 이들 대상자를 활성화할 수 있습니다. [Adobe Experience Platform](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/home){target="_blank"}에서 대상을 사용하는 방법에 대해 알아봅니다.

>[!NOTE]
>
>Adobe 페더레이션된 대상자 구성을 사용하여 생성된 대상자는 편집할 수 없습니다. 이 대상자 중 하나를 수정하려면 구성을 사용하여 새 대상자를 만들어야 합니다.

## Access Adobe Experience Platform에서 대상자에 액세스 {#access-audience}

페더레이션된 대상자 구성을 사용하여 생성된 대상자는 **대상자** 메뉴의 대상자 포털에서 액세스할 수 있습니다.

**[!UICONTROL 찾아보기]** 탭에는 Adobe Experience Platform에 저장된 기존 대상자의 전체 목록이 있습니다. **[!UICONTROL 원본]** 열이나 왼쪽 창에서 사용 가능한 필터를 사용하여 목록에서 페더레이션된 대상자 구성 대상자를 식별할 수 있습니다.

![](assets/audiences-list.png)

Adobe Experience Platform에서 대상자를 사용하여 작업하는 방법에 대한 자세한 내용은 [대상자 포털 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}를 참조하십시오.

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->