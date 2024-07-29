---
title: Federated Audience 컴포지션 액세스
description: Federated Audience Composition에 액세스하는 방법을 알아봅니다.
badge: label="제한된 가용성" type="Informative"
source-git-commit: 618d1675c28213d7a316f40cd624d282e01297f1
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# Federated Audience 컴포지션 액세스 {#fac-access}

## 패키지 및 추가 기능 {#package}

Federated Audience Composition을 사용하려면 Adobe Real-time Customer Data Platform 및 Adobe Journey Optimizer Prime 또는 Ultimate 패키지가 필요합니다. 이 기능에 액세스하려면 Federated Audience Composition 추가 기능을 구입해야 합니다.

>[!AVAILABILITY]
>
>Adobe에서 환영 이메일 알림을 받은 후 인터페이스 및 사용 가능한 기능을 업데이트하는 데 몇 시간이 더 걸릴 수 있습니다.

## 권한 {#permissions}

Federated Audience Composition 추가 기능을 구매하면 해당 시점의 각 활성 샌드박스에 대해 제품 프로필이 생성됩니다. 이 제품 프로필은 **Adobe Experience Platform** 제품 카드 아래의 Admin Console에서 만들어지며, 명명 규칙을 따릅니다. `ACP_FAC - <<SandboxName>> - admin.` 특정 샌드박스의 Federated Audience Composition에 액세스하려면 해당 샌드박스에 대해 만들어진 제품 프로필에 사용자를 추가해야 합니다.

예를 들어 &quot;fac-test&quot;라는 새 샌드박스가 활성화된 경우 해당 제품 프로필 &quot;ACP_FAC - fac-test - admin&quot;이 생성됩니다. 이 샌드박스로 Federated Audience Composition에 액세스하려면 사용자를 이 제품 프로필에 추가해야 합니다.

## IP 허용 목록 {#ip}

Data Warehouse에 대한 액세스를 활성화하고 Federated Audience Composition을 사용하려면 IP 주소를 허용 목록에 추가해야 합니다. IP 주소를 허용 목록에 추가하려면 Adobe 담당자에게 문의하십시오.

## 가드레일 및 제한 사항 {#fac-guardrails}

* Federated Audience Composition은 Privacy &amp; Security Shield와 호환되며, 의료 산업을 제외한 모든 버티컬에서 사용할 수 있습니다. 현재, 상태 데이터를 수집하려는 고객은 Federated Audience Composition에 라이선스를 부여할 수 없습니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* [Adobe Real-time Customer Data Platform 설명서](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"}에 나열된 자격, 제품 제한 및 성능 보호가 이 추가 기능에 적용됩니다.
