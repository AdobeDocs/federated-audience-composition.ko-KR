---
title: Federated Audience Composition 사전 요구 사항 및 보호 기능
description: Federated Audience Composition의 사전 요구 사항, 권한 및 가드레일에 대해 알아봅니다.
badge: label="제한된 가용성" type="Informative"
source-git-commit: 61ad8899f7de601b64c7b42cb873a172fcaea145
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# 전제 조건 및 가드레일 {#fac-access}

Federated Audience Composition에는 Adobe Real-time Customer Data Platform 및/또는 Adobe Journey Optimizer **Prime** 또는 **Ultimate** 패키지가 필요합니다. 이 기능에 액세스하려면 Federated Audience Composition 추가 기능을 구매해야 합니다.

>[!AVAILABILITY]
>
>Adobe로부터 환영 이메일 알림을 받은 후 인터페이스가 업데이트되고 기능을 사용할 수 있게 되기까지 몇 시간이 더 걸릴 수 있습니다.

## 권한 {#permissions}

Federated Audience Composition 추가 기능을 구매하면 해당 시점의 각 활성 샌드박스에 대해 제품 프로필이 생성됩니다. 이 제품 프로필은 **Adobe Experience Platform** 제품 카드 아래의 Admin Console에서 만들어지며, 명명 규칙을 따릅니다. `ACP_FAC - <<SandboxName>> - admin.` 특정 샌드박스의 Federated Audience Composition에 액세스하려면 해당 샌드박스에 대해 만들어진 제품 프로필에 사용자를 추가해야 합니다.

예를 들어 &quot;fac-test&quot;라는 새 샌드박스가 활성화된 경우 해당 제품 프로필 &quot;ACP_FAC - fac-test - admin&quot;이 생성됩니다. 이 샌드박스로 Federated Audience Composition에 액세스하려면 사용자를 이 제품 프로필에 추가해야 합니다.

## IP 허용 목록 {#ip}

Federated Audience Composition이 데이터베이스에 액세스할 수 있도록 안전하게 활성화하려면 Adobe 담당자에게 문의하여 Federated Audience Composition 서버에 액세스할 IP 주소를 얻으십시오.

이러한 IP 주소를 허용 목록에 추가하여 Federated Audience Composition에 대한 액세스 권한을 부여합니다.

## 가드레일 및 제한 사항 {#fac-guardrails}

* Healthcare Shield 및 Privacy and Security Shield에서는 현재 Federated Audience Composition의 대상 및 속성을 사용할 수 없습니다.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* [Adobe Real-time Customer Data Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/guardrails){target="_blank"}에 나열된 자격, 제품 제한 및 성능 보호가 이 추가 기능에 적용됩니다.
