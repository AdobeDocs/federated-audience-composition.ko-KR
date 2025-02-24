---
title: Experience Platform 페더레이션된 대상자 구성의 새로운 기능
description: 최신 업데이트 및 릴리스 정보
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 3e508a769856e66e3b1381c3996df01539668dbd
workflow-type: ht
source-wordcount: '647'
ht-degree: 100%

---

# 릴리스 정보 {#rn-new}

[!DNL Federated Audience Composition]는 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 이 릴리스 정보에는 모든 변경 사항이 통합되어 있습니다. [!DNL Federated Audience Composition]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}를 참조하십시오.

## 25년 2월 릴리스 {#fac-25-2}

이 릴리스는 아래 목록에 있는 변경 사항과 함께 제공됩니다.

* **Microsoft Fabric 지원**

  이제 페더레이션된 대상자 구성을 통해 Microsoft Fabric 데이터베이스에 대한 연결을 설정할 수 있습니다. [자세히 알아보기](../connections/federated-db.md)

* **Amazon Redshift Spectrum 지원**

  Amazon Redshift 데이터베이스 연결에서 이제 Amazon Redshift Spectrum을 지원합니다. [자세히 알아보기](../connections/federated-db.md#amazon-redshift)

* **향상된 스키마 생성 경험**

  스키마 생성 프로세스가 더욱 직관적이고 손쉽게 탐색할 수 있도록 업데이트된 사용자 인터페이스를 통해 개선되었습니다. 이러한 개선 사항은 데이터 실무자가 더욱 원활하고 효율적으로 데이터 모델을 개발할 수 있도록 합니다. [자세히 알아보기](../customer/schemas.md)

* **Databricks에 대한 대상자 강화 지원**

  이제 대상자 읽기 플로우에서 Databricks를 사용할 수 있으며, Databricks 데이터베이스의 활성화를 지원하고 새로운 대상으로 설정할 수 있습니다. [자세히 알아보기](../connections/destinations.md)

<!--
* **Federated Audience Composition permissions**

    Starting March release, [!DNL Federated Audience Composition] will start enforcing the access of **Federated data management** and **Federated Compositions** interfaces to user who have been granted the **Manage Federated Data** permission. 

    We recommend users to contact the administrators to have this permission added to their role in order to continue accessing the [!DNL Federated Audience Composition] user interface.

    To learn how to assign this permission, refer to the [detailed documentation](feature-access.md).
-->

## 2024년 11월 릴리스 {#fac-24-11}

### 개선 사항 {#fac-24-11-improvements}

이번 릴리스는 아래의 개선 사항과 함께 제공됩니다.

* **IP 주소 허용 목록**

  이제 Adobe Experience Platform 사용자 인터페이스에서 페더레이션된 데이터베이스를 추가할 때 페더레이션된 대상자 구성 인스턴스와 연관된 IP 주소를 직접 조회할 수 있습니다. 이를 통해 이들 IP를 손쉽게 복사 및 승인하고 데이터베이스에 연결하여 보안과 유연성을 향상시킬 수 있습니다. [자세히 알아보기](../connections/connections.md)

## 2024년 10월 릴리스 {#fac-24-10}

>[!AVAILABILITY]
>
>이전에는 조직 집합에만 사용할 수 있었던(LA) Adobe Experience Platform 페더레이션된 대상자 구성을 이제 모든 사용자가 사용할 수 있습니다(GA). 이 추가 기능은 귀하가 제공하는 서비스를 기반으로 활성화되며, 관련 권한이 있는 경우에만 볼 수 있습니다. [자세히 알아보기](access-prerequisites.md)
>

### 호환성 {#fac-24-10-compat}

이제 이 새 릴리스를 통해 페더레이션된 대상자 구성이 아래 나열된 시스템과 호환됩니다.

* **Databricks 지원**

  이제 페더레이션된 대상자 구성을 통해 Databricks 데이터베이스에 대한 연결을 설정할 수 있습니다. [자세히 알아보기](../connections/federated-db.md#databricks)

* **AWS PrivateLink를 통한 Snowflake에 대한 보안 액세스 지원**

  이제 비공개 링크를 통한 외부 Snowflake Data Warehouse에 대한 보안 액세스가 지원됩니다. Snowflake 계정은 AWS(Amazon Web Services)에서 호스팅되어야 하며 페더레이션된 대상자 구성 환경과 동일한 지역에 있어야 합니다. Snowflake 계정에 대한 보안 액세스를 설정하는 데 도움이 필요한 경우 Adobe 담당자에게 문의하십시오. [자세히 알아보기](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless 지원**

  이 새 릴리스를 통해, 페더레이션된 대상자 구성은 [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}를 지원합니다.

### 개선 사항 {#fac-24-10-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

* **기존 스키마 새로 고침**

  이제 페더레이션된 데이터베이스에서 열을 만들거나, 수정하거나, 삭제하면 해당 스키마에서 **[!UICONTROL 스키마 새로 고침]** 버튼을 클릭하여 변경 사항을 감지하고 적용할 수 있습니다. [자세히 알아보기](../customer/schemas.md#schema-refresh)

* **새 구성에 데이터 모델 연결**

  이제 구성을 만들 때 연결할 데이터 모델을 선택할 수 있습니다. 이 새 옵션을 사용하면 연결된 데이터 모델의 테이블만 사용할 수 있으므로 활동을 구성하기가 더 쉬워집니다. [자세히 알아보기](../compositions/create-composition.md)

## 2024년 7월 릴리스 - 페더레이션된 대상자 구성 (LA) {#fac-la}

페더레이션된 대상자 구성은 기업이 중요한 기업 데이터 세트를 사용하여 대상자를 구성하고 브랜드가 주도하는 즉각적 경험을 강화할 수 있도록 기업 데이터 웨어하우스에 대한 유연하고 확장된 액세스를 제공하는 추가 기능입니다. 이 새로운 접근 방식을 사용하면 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/home){target="_blank"} 및/또는 [Adobe Journey Optimizer](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/ajo-home){target="_blank"} 사용자는 기존 데이터 웨어하우스에서 직접 대상자 데이터를 페더레이션하여 Adobe Experience Platform 대상자와 속성을 하나의 시스템에 강화할 수 있습니다.

페더레이션된 대상자 구성은 웨어하우스 데이터 세트를 사용하여 대상자를 구성할 수 있는 유연성이 필요한 기업의 증가하는 시장 요구를 충족할 수 있습니다. 이를 통해 기업은 데이터 이동을 줄이는 동시에 중요한 대상자 데이터를 마케팅 팀에 제공하여 사용 사례 요구 사항을 충족하고 맞춤화된 경험을 제공할 수 있습니다. 

[이 페이지](get-started.md)와 [자주 묻는 질문(FAQ)](faq.md)에서 페더레이션된 대상자 구성에 대해 자세히 알아보십시오.

[이 페이지](access-prerequisites.md)에서 페더레이션된 대상자 구성에 액세스하기 위한 사전 요구 사항 및 현재 가드레일에 대한 자세한 내용을 알아보십시오.

