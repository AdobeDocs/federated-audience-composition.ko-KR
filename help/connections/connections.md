---
audience: end-user
title: 페더레이션 데이터베이스와의 연결 만들기 및 관리
description: Federated Database와의 연결을 만들고 관리하는 방법 알아보기
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 4%

---

# 연결 만들기 {#connections-fdb}

Experience Platform Federated Audience Composition을 통해 고객은 서드파티 데이터 웨어하우스에서 대상을 구축 및 강화하고 해당 대상을 Adobe Experience Platform으로 가져올 수 있습니다. 지원되는 데이터 웨어하우스는 [이 섹션](../start/access-prerequisites.md#supported-systems)에 나열되어 있습니다.

페더레이션 데이터베이스 및 Adobe Experience Platform을 사용하여 작업하려면 먼저 연결을 설정해야 합니다. 이 연결은 이 페이지에 설명된 대로 Adobe Experience Platform 사용자 인터페이스에서 사용할 수 있는 전용 사용자 인터페이스에서 설정됩니다.

데이터베이스와의 연결을 설정하려면 다음 단계를 수행합니다.

1. 왼쪽 레일에서 **[!UICONTROL 페더레이션 데이터]** 섹션으로 이동합니다.

1. **[!UICONTROL 페더레이션 데이터베이스]** 링크에서 **[!UICONTROL 페더레이션 데이터베이스 추가]** 단추를 클릭합니다.

   ![](assets/connections_list.png){zoomable="yes"}

1. 데이터베이스 이름과 형식을 사용하여 연결 **[!UICONTROL 속성]**&#x200B;을 설정합니다.

   ![](assets/connections_name.png){zoomable="yes"}

   유형을 선택하면 채울 다른 속성에 액세스할 수 있습니다. [이 페이지](federated-db.md)에서 지원되는 데이터베이스에 대해 자세히 알아보세요.

   ![](assets/connections_details.png){zoomable="yes"}

   구성 설정은 데이터베이스 유형에 따라 다릅니다. 연결을 설정하는 데 필요한 세부 정보에 액세스하려면 아래 링크를 찾아보십시오.

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)
   * [Microsoft Fabric](federated-db.md#microsoft-fabric)

1. 지원되는 각 데이터베이스에 대해 **[!UICONTROL 서버 IP]** 단추를 선택하십시오. Federated Audience Composition 인스턴스와 연결된 모든 IP 목록이 표시됩니다.

   ![](assets/connections_server_IPs.png){zoomable="yes"}

   목록에서 IP를 클릭하여 시스템에 복사하고 이 IP가 데이터베이스에 연결되도록 승인합니다.

   >[!NOTE]
   >
   >주어진 데이터베이스에 대해 Federated Audience Composition을 사용하려면 해당 데이터베이스와 연관된 모든 IP 주소를 허용 목록 해야 합니다.

1. 세부 정보를 입력한 후 **[!UICONTROL 연결 테스트]** 단추와 **[!UICONTROL 함수 배포]** 단추를 클릭합니다.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. **[!UICONTROL 저장]** 단추를 클릭하여 연결 만들기를 완료합니다.

   아래와 같이 Federated 데이터베이스 연결에 대한 개요를 사용할 수 있습니다.

   ![](assets/connections_overview.png){zoomable="yes"}
