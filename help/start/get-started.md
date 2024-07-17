---
title: Federated Audience 구성 시작
description: Adobe Federated Audience Composition이란 무엇이며 Adobe Experience Platform에서 이를 사용하는 방법을 알아봅니다.
badge: label="제한된 가용성" type="Informative"
source-git-commit: 63192ea583aca7bc4a30b4a9d2071b83d0a46406
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 7%

---


# Federated Audience 구성 시작 {#gs-fac}

Adobe Experience Platform Federated Audience Composition은 Adobe Real-time Customer Data Platform 및/또는 Adobe Journey Optimizer 내에서 직접 엔터프라이즈 데이터 웨어하우스를 연결하고 데이터 웨어하우스 테이블에서 쿼리를 수행하는 쉽고 강력한 솔루션을 제공합니다.

Adobe Federated Audience Composition을 통해 Adobe Experience Platform 앱 사용자는 엔터프라이즈 데이터 웨어하우스에 저장된 고객 데이터에 액세스할 수 있습니다. 고객 데이터는 여러 데이터 웨어하우스에서 사용할 수 있으며, 이제 복제 없이 즉시 액세스할 수 있습니다.


## 사용 사례 {#rn-uc}

마케팅 친화적인 UI를 통해 마케팅 캠페인에 필요한 특정 세그먼트에 적합한 사용자 목록을 데이터 웨어하우스에 쿼리하는 세그먼트 규칙을 만들거나, 활성화를 위해 웨어하우스의 기존 대상에 액세스하거나, 웨어하우스에 존재하는 추가 데이터 포인트로 Adobe Experience Platform 대상을 보강합니다.

이 버전에서는 대상 세그멘테이션 및 대상 보강의 두 가지 사용 사례를 사용할 수 있습니다. 향후 릴리스에서 프로필 강화를 사용할 수 있습니다.

![다이어그램](assets/fac-use-cases.png){zoomable="yes"}

## 주요 단계 {#gs-steps}

Adobe Federated Audience Composition을 사용하면 수집 프로세스 없이 데이터베이스에서 직접 Adobe Experience Platform 대상을 만들고 업데이트할 수 있습니다.

![다이어그램](assets/steps-diagram.png){zoomable="yes"}

주요 단계:

* **구성**

   1. Adobe Experience Platform 및 엔터프라이즈 데이터 웨어하우스를 연결합니다.
지원되는 데이터베이스는 Snowflake, Google Big Query, Azure synapse, Redshift입니다.
[이 페이지](../connections/federated-db.md)에서 자세히 알아보기
   1. 스키마를 만들어 사용자 인터페이스에서 액세스할 수 있는 데이터를 선택하십시오.
[이 페이지](../customer/schemas.md)에서 자세히 알아보기
   1. 데이터 모델에 대한 링크를 만듭니다.
[이 페이지](../data-management/gs-models.md)에서 자세히 알아보기

* **대상자 작성**

   1. 컴포지션을 디자인 및 실행하여 대상자를 만듭니다.
[이 페이지](../compositions/gs-compositions.md)에서 자세히 알아보기
   1. Adobe Experience Platform Audience Portal 및 Destinations를 통해 기존 대상자를 업데이트하거나 재사용합니다.
[이 페이지](../connections/destinations.md)에서 자세히 알아보기

## 자주 묻는 질문 {#faq}

다음은 Federated Audience 구성에 대한 FAQ 목록입니다. [이 페이지](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}의 Adobe Experience Platform 세분화 서비스에 대한 전역 FAQ도 사용할 수 있습니다.


+++Federated Audience Composition에 액세스하는 데 필요한 권한은 무엇입니까?

Federated Audience Composition에 대한 특정 권한은 없습니다. 이 기능에 액세스하기 위한 유일한 전제 조건은 Federated Audience Composition 추가 기능을 구입한 것입니다.

+++

+++어떤 클라우드 웨어하우스가 지원됩니까?

이 릴리스의 경우 Federated Audience Composition은 다음과 호환됩니다.

* Snowflake
* Google BigQuery
* Azure synapse
* Amazon Redshift

+++


+++동일한 구성에서 여러 데이터 웨어하우스를 쿼리할 수 있습니까?

예. 동일한 구성에서 여러 웨어하우스를 쿼리하고 여러 소스의 데이터를 결합할 수 있습니다.  일반적으로 각 [컴포지션 활동](../compositions/orchestrate-activities.md)(쿼리, 데이터 보강, 분할 등)은 작업 구성, 타겟팅된 데이터베이스(여러 경우 통합 데이터 액세스 가능) 및 실행 결과가 있는 하나 이상의 작업 테이블의 출력에 따라 하나 이상의 SQL 문을 실행합니다. 이러한 작업테이블은 연속적인 활동에 대한 입력으로 사용됩니다.

+++

+++ Federated Audience Composition을 사용하여 전체 데이터베이스에 액세스할 수 있습니까?

아니요. 전용 또는 공유 데이터베이스/스키마에 대한 액세스를 구성하는 것은 사용자의 책임입니다. Federated Audience Composition에 대한 전용 스키마를 만들고 비즈니스 사례 데이터 세트만 복사/공유하는 것이 좋습니다.
+++



+++전용 스키마의 모든 테이블에 액세스할 수 있습니까?

예. 연결되면 Federated Audience Composition을 사용하여 정의된 초기 권한을 기반으로 모든 테이블을 검색한 다음, 시각적 스키마 편집기를 사용하여 다음을 수행할 수 있습니다.

* 테이블에서 열 및 기본 키 검색
* 해당 테이블에 친숙한 레이블 만들기
* 각 열에 대해 친숙한 레이블 만들기
* 불필요한 열 숨기기
* 해당 테이블 설명 저장
+++


+++Federated Audience 구성에 임시 저장소가 있습니까?

아니요. Federated Audience Composition은 메타데이터(스키마 설명)만 저장합니다. 전송 중인 고객 데이터가 없습니다. 대상 내보내기 흐름은 Adobe Experience Platform 대상 포털([대상](../connections/destinations.md)을 통해)에서 고객 데이터베이스로 직접 수행됩니다. 작성 및 업데이트 흐름은 데이터 웨어하우스 데이터베이스에서 Adobe Experience Platform 대상 포털로 직접 수행됩니다.

+++

+++Federated Audience Composition은 다운스트림 시스템으로 전송할 해당 사용자 목록의 물리적 사본을 저장합니까?

Federated Audience Composition은 데이터의 물리적 사본을 유지 관리하지 않습니다. 이 데이터를 새로 고치는 빈도를 정의하기 위해 컴포지션에 빈도가 구성됩니다. 결과 대상 데이터는 고객의 사용 사례 또는 작업에서 요구하는 것보다 더 이상 Adobe Experience Platform에 의해 저장되지 않습니다.

예:

* 대상 세그멘테이션의 경우 대상이 웨어하우스에 만들어지므로, 결과 대상 및 관련 특성을 Adobe Experience Platform 대상 포털을 통해 게시하기 전에 추가 구성 작업 및 데이터 조작에 Federated Audience Composition을 사용할 수 있습니다. 대상 정의 및 관련 속성은 Adobe Experience Platform으로 넘어갑니다.
외부에서 생성된 대상에 대한 현재 데이터 만료는 30일입니다. 이 데이터 만료는 조직 내에 저장된 초과 데이터의 양을 줄입니다. 데이터 만료 기간이 지난 후에도 연결된 데이터 세트는 데이터 세트 인벤토리 내에 계속 표시되지만 대상자를 활성화할 수 없으며 프로필 카운트는 0으로 표시됩니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}를 참조하세요.

* 대상 강화의 경우 시작점은 기존 Adobe Experience Platform 대상입니다. 하나는 여기에서 두 가지 시나리오를 볼 수 있습니다.
   1. Federated Data Warehouse에서 추가 대상 페이로드 속성을 가져옵니다. 이 경우 추가되는 추가 속성은 이 대상 정의의 일부로 가져옵니다. 외부에서 생성된 대상에 대한 데이터 만료는 위에서 설명한 30일과 동일합니다.
   1. 데이터 웨어하우스에 있는 추가 속성을 기반으로 기존 Adobe Experience Platform 대상을 세분화합니다. 예를 들어 지난 2개월 동안 웹 사이트에서 특정 제품에 관심을 보인 고객 대상이 있습니다. 이제 이 대상을 가져와서 크레딧 점수가 높은 고객만 포함하도록 Federated Audience Composition을 사용하여 추가로 세그먼트화하려고 합니다. 신용 점수는 민감한 것으로 간주되며 개별 신용 점수 데이터 포인트는 Data Warehouse에서 복사되지 않습니다.
+++

+++대상 세분화 및 대상 강화 사용 사례 패턴에 대한 데이터가 지속되지 않는 경우 임시 저장되는 방법은 무엇입니까?

결과 대상 데이터는 Adobe Experience Platform 또는 Federated Audience Composition에서 무기한 지속되지 않습니다. 사용 사례에서 요구하는 것보다 더 이상 유지되지 않습니다. 대상 페이로드의 일부로 가져온 대상 속성은 대상 정의의 일부로서만 유지됩니다. 지속성 기간은 모든 대상의 TTL을 기반으로 합니다. 기본값은 30일입니다.

+++

+++업로드한 사용자 지정 대상자를 삭제할 수 있습니까?

작업 메뉴에서 삭제를 선택하면 Audience Portal에서 직접 다운스트림 활성화에 사용되지 않는 대상을 삭제할 수 있습니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}를 참조하세요.

+++

+++여러 소스의 데이터를 결합하는 경우 데이터를 결합하는 방법은 무엇입니까? ID 서비스를 사용하고 있습니까?

아니요. 작성 중에는 ID 서비스가 활용되지 않습니다. 컴포지션에 사용되는 다양한 소스 간의 데이터는 CRM ID, 사용자 계정 번호 등과 같은 사용자 정의 논리(기본 모델에서 표현됨)를 통해 연결됩니다. Data Warehouse에서 선택하기 위해 대상에서 식별자로 사용되는 ID를 선택해야 합니다. Federated Audience Composition의 결과 대상의 경우 결과 데이터 세트에서 ID에 대한 ID 네임스페이스를 식별해야 합니다.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->

## 추가 정보 {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="실행 설정"
>abstract="이 섹션에서는 작성 기록이 유지되는 일 수와 같이 워크플로우 실행과 관련된 설정을 구성할 수 있습니다."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="활동 편집 불가"
>abstract="**쿼리** 또는 **보강** 활동이 콘솔에서 추가 데이터로 구성된 경우, 보강 데이터가 고려되어 아웃바운드 전환으로 전달되지만 편집할 수는 없습니다."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="링크 만들기"
>abstract="링크 설정을 정의합니다."
