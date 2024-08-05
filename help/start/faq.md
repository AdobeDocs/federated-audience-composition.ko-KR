---
title: 자주 묻는 질문
description: Adobe Experience Platform 페더레이션된 대상자 구성에 대한 자주 묻는 질문
badge: label="제한된 가용성" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: dd19c6a8170a87c10fd8534bf2aa63adcf360529
workflow-type: ht
source-wordcount: '834'
ht-degree: 100%

---

# 자주 묻는 질문 {#faq}

다음은 Adobe Experience Platform 페더레이션된 대상자 구성과 관련하여 자주 묻는 질문 목록입니다. [이 페이지](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/faq){target="_blank"}에서는 Adobe Experience Platform Segmentation Service에 대한 글로벌 FAQ도 제공됩니다.


+++페더레이션된 대상자 구성에 액세스하려면 어떤 권한이 필요합니까?

페더레이션된 대상자 구성을 위해서는 Adobe Real-Time Customer Data Platform 및 Adobe Journey Optimizer Prime 또는 Ultimate 패키지가 필요합니다. 또한 페더레이션된 대상자 구성 추가 기능을 구매해야 합니다.

페더레이션된 대상자 구성을 사용하려면 각 사용자를 각 샌드박스에 대해 생성된 특정 프로필에 추가해야 합니다. 자세한 내용은 [페더레이션된 대상자 구성 액세스](access-prerequisites.md) 페이지를 참조하십시오.

+++

+++어떤 클라우드 데이터 웨어하우스가 지원됩니까?

이번 릴리스의 경우 페더레이션된 대상자 구성은 다음과 호환됩니다.

* Amazon Redshift
* Azure Synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++여러 개의 데이터 웨어하우스를 동일한 구성으로 쿼리할 수 있습니까?

예, 여러 개의 데이터 웨어하우스를 동일한 구성으로 쿼리할 수 있으며 여러 소스의 데이터를 결합할 수 있습니다.  일반적으로 각 [구성 활동](../compositions/orchestrate-activities.md)(쿼리, 강화, 분할 등)은 활동 구성, 대상 데이터베이스(여러 개의 페더레이션된 데이터 액세스 사례가 있을 수 있음) 및 실행 결과가 포함된 하나 이상의 작업 테이블의 출력에 따라 하나 또는 여러 개의 SQL 문을 실행합니다. 해당 작업 테이블은 연속적인 활동을 위한 입력으로 사용됩니다.

+++

+++ 페더레이션된 대상자 구성을 사용하여 전체 데이터베이스에 액세스할 수 있습니까?

아니요, 전용 또는 공유 데이터베이스/스키마에 대한 액세스를 구성하는 것은 사용자에게 달려 있습니다. 페더레이션된 대상자 구성을 위한 전용 스키마를 만들고 비즈니스 사례 데이터 세트만 복사/공유하는 것이 좋습니다.
+++



+++전용 스키마의 모든 테이블에 액세스할 수 있습니까?

예, 일단 연결되면 페더레이션된 대상자 구성을 사용하여 정의된 초기 권한을 기반으로 모든 테이블을 검색할 수 있으며, 시각적 스키마 편집기를 사용하여 다음 작업을 수행할 수 있습니다.

* 테이블에서 열과 기본 키를 검색
* 해당 테이블에 친숙한 라벨 만들기
* 각 열에 대해 친숙한 레이블 만들기
* 불필요한 열 숨기기
* 해당 테이블 설명 저장
+++


+++페더레이션된 대상자 구성에 임시 스토리지가 있습니까?

아니요. 페더레이션된 대상자 구성은 메타데이터(스키마 설명)만 저장합니다. 고객 데이터는 전송되지 않습니다. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++페더레이션된 대상자 구성은 다운스트림 시스템으로 보낼 사람들 목록의 물리적 사본을 저장합니까?

페더레이션된 대상자 구성은 데이터의 물리적 사본을 유지하지 않습니다. 이 데이터를 새로 고칠 빈도를 정의하기 위해 구성에서 빈도를 구성합니다. 결과 대상자 데이터는 고객의 사용 사례 또는 액션에 필요한 기간 이상으로 Adobe Experience Platform에 저장되지 않습니다.

예:

* 대상자 생성의 경우 대상자가 데이터 웨어하우스에 생성되며, Adobe Experience Platform 대상자 포털을 통해 결과 대상자 및 관련 속성을 게시하기 전에 추가 구성 작업 및 데이터 조작에 페더레이션된 대상자 구성을 사용할 수 있습니다. 대상자 정의 및 관련 속성은 Adobe Experience Platform으로 전달됩니다.
외부에서 생성된 대상자에 대한 현재 데이터 만료 기간은 30일입니다. 이러한 데이터 만료로 인해 조직 내에 저장되는 초과 데이터의 양이 줄어듭니다. 데이터 만료 기간이 지난 후에도 관련 데이터 세트는 데이터 세트 인벤토리 내에 계속 표시되지만 대상자를 활성화할 수 없으며 프로필 수가 0으로 표시됩니다. 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}를 참조하십시오.

* 대상자 강화의 경우 시작점은 기존의 Adobe Experience Platform 대상자입니다. 여기서는 두 가지 시나리오를 볼 수 있습니다.
   1. 페더레이션된 데이터 웨어하우스에서 추가 대상자 페이로드 속성을 가져옵니다. 이 경우 추가되는 추가 속성은 이 대상자 정의의 일부로 제공됩니다. 외부에서 생성된 대상자에 대한 데이터 만료는 위에서 설명한 것과 동일하며 30일입니다.
   1. 데이터 웨어하우스에 존재하는 추가 속성을 기반으로 기존 Adobe Experience Platform 대상자를 구체화합니다. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++대상자 생성 및 대상자 강화 사용 사례 패턴에 대한 데이터가 유지되지 않는 경우 어떻게 일시적으로 저장됩니까?

결과 대상자 데이터는 Adobe Experience Platform 또는 페더레이션된 대상자 구성에서 무기한 유지되지 않습니다. 사용 사례에 필요한 것보다 더 오래 보관되지 않습니다. 대상자 페이로드의 일부로 가져온 대상자 속성은 대상자 정의의 일부로만 유지됩니다. 지속 기간은 모든 대상자에 대한 TTL을 기반으로 하며 기본값은 30일입니다.

+++

+++사용자 정의 업로드 대상자를 삭제할 수 있습니까?

아니요, 현재 버전에서는 사용자 정의 업로드된 대상자를 삭제할 수 없습니다. <!--that are not used in downstream activation directly in Audience Portal by simply selecting delete from the actions menu. Learn more in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.-->

+++

+++여러 소스의 데이터를 결합하는 경우 데이터를 어떻게 참여시킵니까? ID 서비스를 사용하고 있습니까?

아니요, 구성 중에는 ID 서비스가 활용되지 않습니다. 구성에 사용된 다양한 소스 간의 데이터는 CRM ID, 사용자 계정 번호 등과 같은 사용자 정의 로직(기본 모델에 표시)을 통해 참여됩니다. 데이터 웨어하우스에서 선택할 대상자의 식별자로 사용되는 ID를 선택해야 합니다. 페더레이션된 대상자 구성의 결과 대상자에서 결과 데이터 세트의 ID에 대한 ID 네임스페이스를 식별해야 합니다.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
