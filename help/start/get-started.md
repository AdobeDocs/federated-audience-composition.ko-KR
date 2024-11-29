---
title: Experience Platform 페더레이션된 대상자 구성 시작하기
description: Adobe 페더레이션된 대상자 구성이 무엇인지와 Adobe Experience Platform에서 사용하는 방법에 대해 알아봅니다.
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '931'
ht-degree: 100%

---

# 페더레이션된 대상자 구성 시작하기 {#gs-fac}

페더레이션된 대상자 구성은 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/home){target="_blank"} 및 [Adobe Journey Optimizer](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/ajo-home){target="_blank"}를 위한 추가 기능으로, 서드파티 데이터 웨어하우스에서 대상자를 빌드 및 강화하고, 대상자를 Adobe Experience Platform으로 가져올 수 있습니다. 페더레이션된 대상자 구성은 Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer 내에서 기업 데이터 웨어하우스를 직접 연결하고 데이터 웨어하우스 테이블에서 쿼리를 수행할 수 있는 쉽고 강력한 솔루션을 제공합니다.

Adobe 페더레이션된 대상자 구성은 Adobe Experience Platform 앱 사용자가 Amazon Redshift, Azure Synapse Analytics 등과 같은 데이터 웨어하우스 및 클라우드 스토리지 플랫폼에 저장된 고객 데이터에 액세스할 수 있도록 지원합니다. 고객 데이터는 여러 데이터 웨어하우스에 저장할 수 있으며, 이제 복제 없이 즉시 액세스할 수 있습니다. 지원되는 플랫폼은 [이 페이지](../connections/federated-db.md#supported-db)에 나열됩니다.

## 기능 {#rn-capabilities}

페더레이션된 대상자 구성은 대상자 큐레이션 및 활성화에 대한 포괄적인 접근 방식을 통해 Real-Time CDP 및 Journey Optimizer의 가치를 확장합니다.

* 중요한 웨어하우스 기반 데이터 세트에 대한 액세스를 확장하여 가치가 높은 대상자 생성: 기존 데이터 웨어하우스를 주요 레코드 시스템으로 활용하는 동시에 최고 수준의 애플리케이션을 활용하여 탁월한 고객 경험을 제공합니다.

* 참여 사용 사례를 강화하기 위한 포괄적인 지원: Real-Time CDP 또는 Journey Optimizer와 결합된 페더레이션된 대상자 구성은 페더레이션된 대상자를 통해 브랜드가 주도하는 맞춤화된 경험을 지원하고, 실시간 이벤트에 따라 트리거되는 즉각적 경험을 개인 속성과 결합하여 여러 팀에 걸쳐 사용 사례 요구 사항을 충족합니다.

* 데이터 이동 및 중복 최소화: 기본 데이터를 복사하지 않고도 기업 데이터 웨어하우스에 있는 데이터 세트에서 대상자를 만들어 실행 가능한 마케팅 프로필과 잠재 대상자를 관리합니다.

* 경험 기반 워크플로를 위한 단일 시스템 활용: Adobe Experience Platform에서 수집되고 페더레이션된 대상자를 선별하고 모든 채널에 걸쳐 아웃바운드 경험을 조정합니다.

## 사용 사례 {#rn-uc}

마케팅 친화적인 UI를 통해 마케팅 캠페인에 필요한 특정 세그먼트에 적합한 사용자 목록을 데이터 웨어하우스에 쿼리하고, 활성화를 위해 데이터 웨어하우스의 기존 대상자에 액세스하거나, 데이터 웨어하우스에 존재하는 추가 데이터 포인트로 Adobe Experience Platform 대상자를 강화하는 세그먼트 규칙을 만듭니다.

이 버전에서는 두 가지 사용 사례를 사용할 수 있습니다.

1. 대상자 생성: 기본 데이터를 복사하지 않고도 기업 데이터 세트에서 새로운 대상자를 빌드하고 미리 빌드된 대상을 통해 해당 대상자를 활성화합니다.

1. 대상자 강화: 기업 데이터 웨어하우스에서 페더레이션된 구성 대상자 데이터를 활용하여 Adobe Experience Platform의 기존 대상자를 강화합니다. 이 데이터는 Adobe Experience Platform 고객 프로필에 유지되지 않습니다.

![다이어그램](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## 주요 단계 {#gs-steps}

Adobe 페더레이션된 대상자 구성을 사용하면 수집 프로세스 없이 데이터베이스에서 Adobe Experience Platform 대상자를 직접 생성하고 업데이트할 수 있습니다.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

주요 단계:

1. **데이터 통합**: 다양한 소스의 데이터를 모아서 통합 데이터 세트로 병합합니다. Adobe Experience Platform 앱과 기업 데이터 웨어하우스, 지원되는 데이터베이스를 연결하는 방법 및 이를 구성하는 방법에 대해서는 [이 섹션](../connections/federated-db.md)에서 자세히 설명합니다.

1. **데이터 모델링**: 데이터의 구조, 관계 및 제약 조건을 정의하는 데이터 모델과 스키마를 설계하고 만듭니다. [이 페이지](../customer/schemas.md)에서 스키마에 대해 자세히 알아보십시오. [이 페이지](../data-management/gs-models.md)에서 데이터 모델에 대한 링크를 만드는 방법을 알아보십시오.

1. **데이터 변환**: 데이터 조작 기술을 적용하여 데이터 요소의 형식, 구조 또는 값을 수정하여 특정 분석이나 애플리케이션에 적합하거나 호환되도록 만듭니다.

1. **데이터 사용**: 대상자를 만들기, 조정 및 빌드합니다. [이 페이지](../compositions/gs-compositions.md)에서 대상자를 구성하는 방법을 알아봅니다». Adobe Experience Platform 대상자 포털 및 대상을 통해 기존 대상자를 업데이트하거나 재사용할 수도 있습니다. [이 페이지](../connections/destinations.md)에서 자세히 알아보기

>[!NOTE]
>
>구성을 실행한 후에 생성된 대상자는 Adobe Experience Platform에 외부 대상자로 저장되며, Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer에서 사용할 수 있습니다. 이 기능은 **대상자** 메뉴에서 액세스할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## 자세히 알아보기 {#learn}

<!-- Workflow + Workflow activities-->


[이 페이지](access-prerequisites.md)에서 페더레이션된 대상자 구성, 가드레일 및 제한 사항에 액세스하는 방법에 대해 알아보십시오.

또한 [이 페이지](faq.md)에서 자주 묻는 질문을 살펴보십시오.


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="실행 설정"
>abstract="이 섹션에서는 구성 기록이 유지되는 일 수와 같이 워크플로 실행과 관련된 설정을 구성할 수 있습니다."

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
>abstract="타기팅 차원을 사용하면 수신자, 약정 수혜자, 운영자, 구독자 등 작업에서 타기팅하는 모집단을 정의할 수 있습니다. 기본적으로 이메일 및 SMS의 경우 대상은 수신자 빌트인 테이블에서 선택됩니다. 푸시 알림의 경우 기본 대상 차원은 구독자 애플리케이션입니다."


<!-- save profile IDs-->

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="프로필 저장"
>abstract="프로필 저장"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="프로필 선택 AEP 스키마 저장"
>abstract="프로필 선택 AEP 스키마 저장"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="프로필 AEP 스키마 목록 저장"
>abstract="프로필 AEP 스키마 목록 저장"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepattribute"
>title="프로필 AEP 스키마 속성 저장"
>abstract="프로필 AEP 스키마 속성 저장"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectprimaryfield"
>title="프로필 선택 기본 식별 필드 저장"
>abstract="프로필 선택 기본 식별 필드 저장"
