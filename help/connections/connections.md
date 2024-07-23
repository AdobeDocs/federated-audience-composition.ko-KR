---
audience: end-user
title: 페더레이션 데이터베이스와의 연결 만들기 및 관리
description: Federated Database와의 연결을 만들고 관리하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
source-git-commit: 98689f24fc7eeffa4cdfa5418c160c13abba7527
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# 연결 만들기 {#connections-fdb}

AEP에서 직접 통합 데이터베이스를 사용하여 작업하면 통합 데이터베이스와의 연결을 설정할 수 있습니다.

데이터베이스와 연결을 설정하려면 **[!UICONTROL FEDERATED DATA]** 섹션으로 이동한 다음 **[!UICONTROL FEDERATED DATABASES]** 링크에서 **[!UICONTROL FEDERATED DATABASE 추가]** 단추를 클릭하십시오.

![](assets/connections_list.png){zoomable="yes"}

데이터베이스 이름과 유형을 사용하여 연결 **[!UICONTROL 속성]**&#x200B;에 대한 창에 액세스합니다.

![](assets/connections_name.png){zoomable="yes"}

유형을 선택하면 채울 다른 속성에 액세스할 수 있습니다. [지원되는 데이터베이스에 대해 자세히 알아보세요](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

데이터베이스 유형에 따라 연결을 설정하는 데 필요한 정보 아래의 링크에서 알아보십시오.
* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google BigQuery](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

세부 정보를 입력한 후 **[!UICONTROL 연결 테스트]** 단추와 **[!UICONTROL 함수 배포]** 단추를 클릭합니다.
**[!UICONTROL 저장]** 단추를 클릭하여 연결 만들기를 완료합니다.

![](assets/connections_testdeploy.png){zoomable="yes"}

다음과 같이 Federated 데이터베이스 연결에 대한 개요를 보게 됩니다.

![](assets/connections_overview.png){zoomable="yes"}