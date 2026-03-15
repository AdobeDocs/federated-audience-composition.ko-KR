---
title: Federated Audience Composition 릴리스 정보
description: Federated Audience Composition에 대한 최신 업데이트 및 릴리스 정보입니다.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 7d12773b36cb963f3d4251a9b88486864056a0fb
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 11%

---


# 릴리스 정보

[!DNL Federated Audience Composition]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 모든 변경 사항은 이 릴리스 정보에서 통합됩니다. [!DNL Federated Audience Composition] 은(는) 기본적으로 [!DNL Adobe Experience Platform]을(를) 기반으로 구축되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=ko){target="_blank"}를 참조하십시오.

## 2026년 2월 릴리스 {#fac-26-02}

Federated Audience Composition에 대한 2월 릴리스는 다음 기능을 지원합니다.

### 새로운 기능 {#fac-26-02-feature}

| 필드 보강 지원 |
| --- |
| 이제 컴포지션 내에서 필드 저장 활동을 사용할 수 있습니다. 필드 저장 활동을 사용하면 외부 웨어하우스의 데이터를 페더레이션하여 Experience Platform 스키마를 보강할 수 있으므로, 추가 속성을 사용하여 Experience Platform 스키마를 향상시킬 수 있습니다. 필드 저장 활동은 B2B 및 B2C 스키마를 모두 지원합니다. 이 활동 사용에 대한 자세한 내용은 [활동 개요](../compositions/activities.md#save-fields)를 참조하십시오. |

| Databricks에 대한 고급 인증 지원 |
| --- |
| 이제 서비스 주체 인증 또는 OAuth 2.0을 사용하여 Databricks로 Federated Audience Composition에 연결할 수 있습니다. 연결 만들기에 대한 자세한 내용은 [연결 개요](../connections/home.md#create)를 참조하십시오. |

## 2026년 1월 릴리스 {#fac-26-01}

Federated Audience Composition에 대한 1월 릴리스는 다음과 같은 새로운 기능 및 개선 사항을 지원합니다.

### 새로운 기능 {#fac-26-01-feature}

| Azure Synapse Service Principal 인증 지원 |
| --- |
| 이제 서비스 주체를 사용하여 Azure Synapse에서 Federated Audience Composition에 연결할 수 있습니다. 연결 만들기에 대한 자세한 내용은 [연결 개요](../connections/home.md#create)를 참조하십시오. |

| Amazon Web Services(AWS)에서 Adobe Experience Platform 고객을 위한 가용성 |
| --- |
| 이제 Experience Platform 인스턴스가 AWS에 있는 경우 Federated Audience Composition을 사용할 수 있습니다. AWS의 Experience Platform에 대한 자세한 내용은 [멀티 클라우드 개요](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud)를 참조하십시오. |

### 개선 사항 {#fac-26-01-improvements}

이 릴리스는 다음과 같은 개선 사항과 함께 제공됩니다.

- **대상자에 대한 데이터 만료 구성**

  이제 컴포지션에서 **대상자 저장** 활동을 사용할 때 데이터 만료를 설정할 수 있습니다.

  Federated Audience Composition의 데이터 만료에 대한 자세한 내용은 [활동 안내서](../compositions/activities.md#save-audience)를 참조하십시오.
