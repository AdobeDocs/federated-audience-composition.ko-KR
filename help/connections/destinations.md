---
audience: end-user
title: 외부 데이터로 Adobe Experience Platform 대상자 강화
description: Federated Audience 구성 대상을 사용하여 통합 데이터베이스의 데이터로 Adobe Experience Platform 대상을 세분화하고 보강하는 방법을 알아봅니다.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 8%

---

# 외부 데이터로 Adobe Experience Platform 대상자 강화 {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="대상 만들기"
>abstract="새 페더레이션된 데이터베이스에 연결하기 위한 설정을 입력합니다. **[!UICONTROL 대상에 연결]** 버튼을 사용하여 구성을 확인합니다."

Adobe Experience Platform을 사용하면 **Adobe Federated Audience Composition 대상**&#x200B;을 사용하여 Audience Portal의 대상을 외부 데이터베이스와 원활하게 통합할 수 있습니다. 이 통합을 통해 기존 대상을 구성에 활용하고 외부 데이터베이스의 데이터를 사용하여 보강 또는 세분화하여 새 대상을 만들 수 있습니다.

이렇게 하려면 Adobe Experience Platform에서 Adobe Federated Audience Composition 대상에 대한 새 연결을 설정해야 합니다. 스케줄러를 사용하여 특정 대상을 정기적으로 보내고, 포함할 특정 속성(예: 데이터 조정을 위한 ID)을 선택할 수 있습니다. 거버넌스 및 개인정보 처리방침을 대상자에 적용한 경우 대상자가 업데이트되면 해당 대상자는 유지되고 대상자 포털로 다시 전송됩니다.

예를 들어 데이터 웨어하우스에 구매 정보를 저장하고 최근 2개월 이내에 특정 제품에 관심이 있는 고객을 타깃팅하는 Adobe Experience Platform 대상을 보유하고 있다고 가정해 보겠습니다. Federated Audience Composition 대상을 사용하여 다음을 수행할 수 있습니다.

* 구매 정보를 기반으로 대상자를 세분화합니다. 예를 들어 150$ 이상을 구매한 고객을 타겟팅하도록 대상을 필터링할 수 있습니다.
* 제품 이름 및 구매 수량 등 구매와 관련된 필드로 대상자를 보강합니다.

Adobe Experience Platform 대상을 Adobe Federated Audience Composition으로 전송하는 주요 단계는 다음과 같습니다.

1. Adobe Experience Platform 대상 카탈로그에 액세스하고 Federated Audience Composition 대상을 선택합니다.

   오른쪽 창에서 **[!UICONTROL 새 대상 구성]**&#x200B;을 선택합니다.

   ![](assets/destination-new.png)

1. 새 연결의 이름을 입력하고 사용 가능한 다음 연결에서 **[!UICONTROL 연결 유형]**&#x200B;을(를) 선택하십시오.

   * Amazon Redshift
   * Azure Synapse Analytics
   * Google BigQuery
   * Snowflake
   * Vertica Analytics
   * Databricks
   * Microsoft Fabric

1. 연결할 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택한 후 **[!UICONTROL 다음]**&#x200B;을 선택하십시오.

   ![](assets/destination-configure.png)

1. **[!UICONTROL 경고]** 섹션에서 경고를 활성화하여 대상에 대한 데이터 흐름 상태에 대한 알림을 받을 수 있습니다.

   경고에 대한 자세한 내용은 [UI를 사용하여 대상 경고 구독](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/ui/alerts){target="_blank"}에 대한 Adobe Experience Platform 설명서를 참조하십시오.

1. **[!UICONTROL 거버넌스 정책 및 시행 작업]** 단계에서는 데이터 거버넌스 정책을 정의하고 대상자를 보내고 활성화할 때 사용된 데이터가 준수되는지 확인할 수 있습니다.

   대상에 대해 원하는 마케팅 액션 선택을 마치면 **[!UICONTROL 만들기]**&#x200B;를 선택합니다.

1. 대상에 대한 새 연결이 만들어집니다. 이제 대상을 활성화하여 대상으로 전송할 수 있습니다. 이렇게 하려면 목록에서 선택한 후 **[!UICONTROL 다음]**&#x200B;을 선택합니다.

   ![](assets/destination-activate.png)

1. 전송하려는 원하는 대상을 선택합니다.

1. 내보내기 일정을 편집하려면 ![](assets/do-not-localize/Smock_Edit_18_N.svg) 아이콘을 선택하십시오.

   ![](assets/destination-schedule.png)

1. 내보내기 파일 옵션을 정의합니다. 대상자를 더 빨리 활성화하려면 **[!UICONTROL 세그먼트 평가 후]** 옵션을 선택하여 일별 플랫폼 일괄 처리 세분화 작업이 완료된 후 즉시 활성화 작업을 트리거합니다.

   ![](assets/destination-schedule-2.png)

   >[!NOTE]
   >
   >일정 및 파일 이름을 구성하는 방법에 대한 자세한 내용은 Adobe Experience Platform 설명서의 다음 섹션에서 확인할 수 있습니다.
   >
   >* [대상자 내보내기 예약](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
   >* [파일 이름 구성](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

1. **[!UICONTROL 매핑]** 단계에서 대상자를 위해 내보낼 특성 및 ID 필드를 선택합니다. 자세한 내용은 Adobe Experience Platform 설명서에서 [매핑 단계](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"}를 참조하십시오.

   ![](assets/destination-attributes.png)

1. 대상 구성 및 대상 설정을 검토한 다음 **[!UICONTROL 마침]**&#x200B;을 선택합니다.

   ![](assets/destination-review.png)

이제 선택한 대상이 새 연결에 대해 활성화됩니다. **[!UICONTROL 대상자 활성화]** 페이지로 다시 이동하여 이 연결로 보낼 대상을 더 추가할 수 있습니다. 대상자가 활성화되면 제거할 수 없습니다.
