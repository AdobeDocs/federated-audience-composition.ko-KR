---
title: Federated Audience 구성 시작
description: Adobe Federated Audience Composition이란 무엇이며 Adobe Experience Platform에서 이를 사용하는 방법을 알아봅니다.
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Federated Audience 구성 시작 {#gs-fac}

Adobe Federated Audience Composition을 통해 Adobe Experience Platform 앱 사용자는 엔터프라이즈 데이터 웨어하우스에 저장된 고객 데이터에 액세스할 수 있습니다. 고객 데이터는 여러 데이터 웨어하우스에 상주할 수 있으므로 복제 없이 즉시 액세스할 수 있어야 합니다.

Adobe Experience Platform Federated Audience Composition은 Adobe Real-time Customer Data Platform 내에서 직접 엔터프라이즈 데이터 웨어하우스를 연결하고 데이터 웨어하우스 테이블에서 쿼리를 수행하는 간단하고 강력한 솔루션을 제공합니다.

## 주요 단계 {#gs-steps}

Adobe Federated Audience Composition을 사용하면 수집 프로세스 없이 데이터베이스에서 직접 Adobe Experience Platform 대상을 만들고 업데이트할 수 있습니다.

![다이어그램](assets/FAC-diagram.png)

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

## 추가 정보 {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="실행 설정"
>abstract="이 섹션에서는 워크플로 기록이 유지되는 일 수와 같이 워크플로 실행과 관련된 설정을 구성할 수 있습니다."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="활동 편집 불가"
>abstract="**쿼리** 또는 **보강** 활동이 콘솔에서 추가 데이터로 구성된 경우, 보강 데이터가 고려되어 아웃바운드 전환으로 전달되지만 편집할 수는 없습니다."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="링크 만들기"
>abstract="링크 설정을 정의합니다."
