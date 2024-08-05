---
title: 페더레이션된 대상자 구성을 위한 사전 요구 사항 및 가드레일
description: 페더레이션된 대상자 구성에 대한 사전 요구 사항, 권한 및 가드레일에 대해 알아보기
badge: label="제한된 가용성" type="Informative"
source-git-commit: 07170ee709c9e3c4ad0bb2390aa0d44adae3b059
workflow-type: ht
source-wordcount: '274'
ht-degree: 100%

---

# 사전 요구 사항 및 가드레일 {#fac-access}

페더레이션된 대상자 구성을 위해서는 Adobe Real-Time Customer Data Platform 및/또는 Adobe Journey Optimizer **Prime** 또는 **Ultimate** 패키지가 필요합니다. 이 기능에 액세스하기 위해서는 페더레이션된 대상자 구성 추가 기능을 구입해야 합니다.

>[!AVAILABILITY]
>
>Adobe로부터 환영 이메일 알림을 받은 후 인터페이스가 업데이트되고 기능을 사용할 수 있게 되기까지 몇 시간이 더 걸릴 수 있습니다.

## 권한 {#permissions}

페더레이션된 대상자 구성 추가 기능을 구매하면 해당 시점의 각 활성 샌드박스에 대한 제품 프로필이 생성됩니다. 이 제품 프로필은 Admin Console의 **Adobe Experience Platform** 제품 카드에서 생성되며 다음 명명 규칙을 따릅니다. `ACP_FAC - <<SandboxName>> - admin.` 특정 샌드박스의 페더레이션된 대상자 구성에 액세스하려면 해당 샌드박스에 대해 생성된 제품 프로필에 사용자를 추가해야 합니다.

예를 들어 “fac-test”라는 새 샌드박스가 활성화되면 해당 제품 프로필 “ACP_FAC - fac-test - admin”이 생성됩니다. 이 샌드박스를 사용하여 페더레이션된 대상자 구성에 액세스하려면 사용자를 이 제품 프로필에 추가해야 합니다.

## IP 허용 목록에 추가 {#ip}

페더레이션된 대상자 구성이 데이터베이스에 안전하게 액세스할 수 있도록 하려면 Adobe 담당자에게 문의하여 액세스할 페더레이션된 대상자 구성 서버의 IP 주소를 받으십시오.

IP 주소를 허용 목록에 추가하여 페더레이션된 대상자 구성에 대한 액세스 권한을 부여하십시오.

## 가드레일 및 제한 사항 {#fac-guardrails}

* [건강 데이터를 수집](https://experienceleague.adobe.com/ko/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}하는 고객과 Adobe Journey Optimizer Privacy 및 Security Shield 고객은 현재 페더레이션된 대상자 구성을 사용할 수 없습니다. [자세히 알아보기](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* 이 추가 기능에는 [Adobe Real-Time Customer Data Platform 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/profile/guardrails){target="_blank"}에 나열된 권한 부여, 제품 제한 및 성능 가드레일이 적용됩니다.
