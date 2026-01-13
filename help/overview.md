---
title: 페더레이션 대상 구성 개요
description: Adobe Federated Audience Composition 및 Adobe Experience Platform 및 Adobe Journey Optimizer과 같은 다운스트림 서비스에서 이를 사용하는 방법에 대해 알아봅니다
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# 페더레이션 대상 구성 개요

Federated Audience Composition을 사용하면 서드파티 데이터 웨어하우스에서 대상을 구축 및 강화하고 해당 대상을 Adobe Experience Platform으로 가져올 수 있습니다. 이 솔루션은 Adobe Real-Time Customer Data Platform 또는 Adobe Journey Optimizer과 같은 다운스트림 서비스 내에서 직접 엔터프라이즈 데이터 웨어하우스를 연결하고 데이터 웨어하우스 테이블에서 쿼리를 수행하는 간단하고 강력한 솔루션입니다. 따라서 데이터 웨어하우스와 Amazon Redshift 및 Azure Synapse Analytics와 같은 클라우드 스토리지 플랫폼에 저장된 고객 데이터에 액세스할 수 있습니다.

## 기능 {#rn-capabilities}

페더레이션된 대상자 컴포지션은 대상자 큐레이션 및 활성화에 대한 포괄적인 접근 방식을 통해 Real-Time CDP 및 Journey Optimizer의 가치를 확장합니다.

* **중요한 웨어하우스 기반 데이터 세트에 대한 액세스를 확장하여 고부가가치 대상 만들기**: 기존 데이터 웨어하우스를 주 기록 시스템으로 사용하는 동시에 동급 최강의 애플리케이션을 활용하여 우수한 고객 경험을 제공할 수 있습니다.

* **Power Engagement 사용 사례에 대한 포괄적인 지원**: Real-Time CDP 또는 Journey Optimizer과 함께 Federated Audience Composition은 Federated Audiences를 통해 브랜드에서 시작한 개인화된 경험을 지원하며, 실시간 이벤트에 의해 트리거된 즉각적인 경험을 팀 간의 사용 사례 요구 사항을 충족하도록 개인 속성과 결합합니다.

* **데이터 이동 및 복제 최소화**: 기본 데이터를 복사하지 않고 엔터프라이즈 데이터 웨어하우스에 있는 데이터 세트에서 대상을 만들어 실행 가능한 마케팅 프로필 및 대상을 관리할 수 있습니다.

* **경험 기반 워크플로우에 단일 시스템 사용**: Adobe Experience Platform에서 수집된 대상과 페더레이션 대상을 모두 큐레이션하고 모든 채널에서 아웃바운드 경험을 조정할 수 있습니다.

* **멀티 에디션 지원**: B2C 및 B2B CDP 고객은 Federated Audience Composition을 활용하여 지원되는 엔터프라이즈 데이터 웨어하우스의 데이터를 통합하여 사용자 기반 대상을 구축할 수 있습니다. 또한 엔터프라이즈 데이터 웨어하우스에서 사용할 수 있는 관련 속성을 통합하여 기존 Experience Platform 사용자 기반 대상을 보강하고 대상 프로필을 향상시켜 보다 개인화되고 타겟팅된 참여를 제공할 수 있습니다.

## 사용 사례 {#use-cases}

페더레이션된 대상자 컴포지션은 대상자 생성, 대상자 보강, 고객 프로필 보강의 **세 가지** 사용 사례를 지원합니다.

* **대상 만들기**: 데이터 웨어하우스에서 대상을 만들고 마케팅 담당자의 친숙한 드래그 앤 드롭 사용자 인터페이스를 통해 Real-Time CDP 또는 Journey Optimizer에서 사용할 수 있도록 해당 대상을 Experience Platform에 연결할 수 있습니다. 결과적으로, 민감한 기본 데이터를 복사하거나 기존 데이터를 복제하지 않고도 데이터 웨어하우스를 쿼리할 수 있습니다.
   * **예:** 웨어하우스의 과거 트랜잭션 데이터를 사용하여 높은 가치의 과거 구매자로 구성된 대상자를 생성하지만 해당 트랜잭션을 Experience Platform에 복사하지 않습니다.

* **대상 강화**: 기본 데이터를 Experience Platform에 복사하지 않고 데이터 웨어하우스의 추가 데이터 세트를 사용하고 이 정보로 대상을 오버레이하여 Experience Platform의 기존 대상에 더 자세한 정보를 추가할 수 있습니다. 대상자 보강을 통해 강화된 대상자에게 더 나은 개인화 경험을 제공할 수 있습니다.
   * **예:** 장바구니를 포기한 사용자로 구성된 Experience Platform 대상자를 높은 가치의 과거 구매자로 구성된 페더레이션된 대상자 컴포지션 대상자로 보강하여 타기팅된 오퍼를 제공합니다.

* **프로필 보강**: 데이터 웨어하우스에서 개별 고객 특성을 선택하여 Experience Platform 프로필을 개선할 수 있습니다. 이들 프로필에 페더레이션된 데이터를 추가하면 유입되는 고객 신호에 따라 트리거되는 즉각적인 경험을 더욱 효과적으로 제공할 수 있습니다.
   * **예:** 페더레이션된 대상자로부터의 정보로 Experience Platform 프로필을 보강합니다. 이제 높은 가치의 과거 구매자 페더레이션된 대상자에 속하는 사이트 방문자에게 사이트 내에서의 행동에 따라 트리거되는 타기팅된 오퍼를 통해 마케팅할 수 있습니다.

![다이어그램](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

페더레이션된 대상자 컴포지션 사용 사례에 대한 자세한 내용은 [페더레이션된 대상자 컴포지션 백서](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html)를 참조하십시오.

## 주요 단계 {#gs-steps}

Adobe 페더레이션된 대상자 컴포지션을 사용하면 수집 프로세스 없이 데이터베이스에서 Adobe Experience Platform 대상자를 직접 생성하고 업데이트할 수 있습니다.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **연결 만들기**: 다양한 원본의 데이터를 가져와서 통합 데이터 집합에 병합합니다. Adobe Experience Platform 앱을 Enterprise Data Warehouse, 지원되는 데이터베이스에 연결하고 연결을 구성하는 방법에 대한 자세한 내용은 [연결 개요](./connections/home.md)를 참조하십시오.

2. **데이터 모델링**: 데이터의 구조, 관계 및 제약 조건을 정의하는 스키마와 데이터 모델을 디자인하고 만듭니다. 스키마에 대한 자세한 내용은 [스키마 개요](./data-modelling/schemas.md)를 참조하십시오. 데이터 모델에 대한 자세한 내용은 [데이터 모델 개요](./data-modelling/models.md)를 참조하십시오.

3. **데이터 변환**: 데이터 조작 기술을 적용하여 데이터 요소의 형식, 구조 또는 값을 수정하여 특정 분석 또는 응용 프로그램에 호환되거나 적합하도록 만듭니다.

4. **대상자 구성**: 대상자를 만들고, 조정하고, 빌드합니다. 대상자 작성에 대한 자세한 내용은 [작성 개요](./compositions/home.md)를 참조하십시오. Adobe Experience Platform 대상자 포털 및 대상을 통해 기존 대상자를 업데이트하거나 재사용할 수도 있습니다. [이 페이지](./connections/destinations.md)에서 자세히 알아보십시오.

>[!NOTE]
>
>컴포지션을 실행한 후에 생성된 대상자는 Adobe Experience Platform에 외부 대상자로 저장되며, Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer에서 사용할 수 있습니다. 이 기능은 **대상자** 메뉴에서 액세스할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 거버넌스, 개인 정보 및 보안 {#governance-privacy-security}

### 개인 정보 요청 {#gov-privacy-requests}

컴포지션을 만들면 최종 대상자가 Adobe Experience Platform에 저장됩니다.

그런 다음 Adobe Experience Platform **Privacy Service**&#x200B;를 통해 이러한 대상자에 해당하는 프로필 데이터에 액세스하거나 삭제하기 위해 개인 정보 요청을 할 수 있으며, 고객 데이터 요청을 관리하는 데 도움이 되는 [사용자 인터페이스](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko-KR){target="_blank"}와 [RESTful API](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/api/overview){target="_blank"}를 제공합니다.

>[!NOTE]
>
>Privacy Service에 대한 자세한 내용은 [Adobe Experience Platform 설명서](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ko-KR){target="_blank"}를 참조하십시오.

Adobe 페더레이션된 대상자 컴포지션에서 고객 데이터에 액세스하고 삭제하기 위한 개별 요청을 만들고 관리할 수 있습니다. **액세스 요청**&#x200B;을 제출하고 **삭제 요청**&#x200B;을 하는 단계는 [실시간 고객 프로필 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/privacy){target="_blank"}에 자세히 나와 있습니다.

### 감사 추적 {#gov-audit-trail}

감사 추적 기능은 실시간으로 환경에 수행된 모든 작업 및 이벤트에 대한 세부 기록 및 시간 기록을 제공합니다. 감사 추적에 대한 자세한 내용은 [감사 추적 개요](./admin/audit-trail.md)를 참조하세요.

## 자세히 알아보기 {#learn}

<!-- Workflow + Workflow activities-->

[이 페이지](./start/access-prerequisites.md)에서 페더레이션된 대상자 컴포지션, 가드레일 및 제한 사항에 액세스하는 방법에 대해 알아보십시오.

FAQ에 대한 답변은 [Federated Audience Composition FAQ](./faq.md)를 참조하십시오.

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


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="증분 쿼리"
>abstract="**증분 쿼리** 활동을 사용하면 쿼리 모델러를 사용하여 데이터베이스를 쿼리할 수 있습니다. 이 활동이 실행될 때마다 이전 실행의 결과가 제외됩니다. 이를 통해 새 요소만 타기팅할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="증분 쿼리 기록"
>abstract="증분 쿼리 기록"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="증분 쿼리 처리된 데이터"
>abstract="증분 쿼리 처리된 데이터"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="증분 쿼리 모드"
>abstract="증분 쿼리를 사용하면 새로운 실행마다 이전 실행의 결과를 제외함으로써 동일한 쿼리를 여러 번 실행할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="증분 쿼리 모드"
>abstract="증분 쿼리를 사용하면 마지막 실행 날짜와 같거나 그 이후인 날짜 필드의 결과만 고려하여 동일한 쿼리를 여러 번 실행할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="타기팅 차원 선택"
>abstract="타기팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타기팅하는 집단을 정의할 수 있습니다. 기본적으로 이메일 및 SMS의 경우 기본 제공 수신자 테이블에서 타깃이 선택됩니다. 푸시 알림의 경우 기본 타기팅 차원은 구독자 애플리케이션입니다."

