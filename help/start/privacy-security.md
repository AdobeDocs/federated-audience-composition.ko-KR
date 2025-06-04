---
title: Federated Audience Composition의 개인 정보 및 보안
description: 데이터 거버넌스, 동의 시행, 액세스 제어, 데이터 암호화 및 개인 정보 보호 규정 준수와 같은 기능을 포함하여 Federated Audience Composition이 사용자 데이터에 대한 개인 정보 및 보안을 처리하는 방법에 대해 알아봅니다.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Federated Audience Composition의 개인 정보 및 보안

Federated Audience Composition은 처리 중에 데이터를 보호하기 위한 다양한 보안 사례를 준수합니다.

## Privacy Service {#privacy}

Federated Audience Composition은 Adobe Experience Platform 및 Adobe Journey Optimizer에서 사용할 수 있는 federated 데이터를 제공합니다. 그러나 Federated Audience Composition은 데이터 웨어하우스의 고객 데이터를 저장하지 **않습니다**. 따라서 Adobe Experience Platform Privacy Service을 사용하여 데이터 주체 및 데이터 삭제 요청을 준수할 수 있습니다.

예를 들어, 컴포지션 캔버스에서 활동 저장 블록을 사용하여 대상을 만들면 결과 대상은 Experience Platform의 데이터 레이크에 외부 대상으로 저장됩니다. 이 외부 대상은 ID 필드 및 ID 네임스페이스로 표시됩니다. 따라서 Privacy Service을 사용하여 외부 대상자가 있는 프로필에 액세스하고 제거할 수 있습니다.

또는 작성 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 결과 보강은 Experience Platform에 프로필 활성화 스키마 및 프로필 활성화 데이터 세트로 저장됩니다. 이 데이터 보강 데이터는 ID 필드 및 ID 네임스페이스로 표시됩니다. 따라서 Privacy Service을 사용하여 이러한 프로필에 액세스하고 정리할 수 있습니다.

Privacy Service에 대한 자세한 내용은 [Privacy Service 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/home){target="_blank"}를 참조하십시오.

### 개인 정보 요청 {#privacy-requests}

Privacy Service에서는 Federated Audience Composition에서 고객 데이터에 액세스하고 삭제하기 위한 개별 개인 정보 보호 요청을 만들고 관리할 수 있습니다. Privacy Service은 고객 데이터 요청을 관리하는 데 도움이 되는 [사용자 인터페이스](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko-KR){target="_blank"}와 [RESTful API](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/api/overview){target="_blank"}를 모두 제공합니다.

개인 정보 보호 요청 만들기 및 관리에 대한 자세한 내용은 Privacy Service UI 가이드의 [개인 정보 보호 작업](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/ui/user-guide){target="_blank"}을 참조하세요.

## 동의 정책 시행 {#consent}

Experience Platform을 통해 Federated Audience Composition은 동의 적용을 자동화할 수 있는 도구를 제공하므로, 고객에게 제공된 동의에 따라 대상을 활성화할 수 있습니다.

예를 들어, 컴포지션 캔버스에서 활동 저장 블록을 사용하여 대상을 만들면 결과 대상은 Experience Platform의 데이터 레이크에 외부 대상으로 저장됩니다. Experience Platform은 활성화 중에 동의 유효성 검사를 자동으로 지원합니다. 자세한 내용은 [세그먼테이션 서비스 FAQ](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/faq#consent){target="_blank"}를 참조하십시오.

또는 작성 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 결과 보강은 Experience Platform에 프로필 활성화 스키마 및 프로필 활성화 데이터 세트로 저장됩니다. 기존 프로필의 경우 활성화 중에 사용 가능한 동의 속성이 자동으로 적용됩니다. 새 프로필의 경우 프로필 수집 중에 제공된 동의 속성은 활성화 중에 자동으로 적용됩니다. 프로필에 동의를 적용하는 방법에 대한 자세한 내용은 [동의 및 환경 설정 필드 그룹 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}를 참조하십시오.

동의 적용에 대한 자세한 내용은 [정책 관리 UI 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}를 참조하십시오.

## 데이터 라이프사이클 {#data-lifecycle}

Federated Audience Composition은 데이터 웨어하우스의 고객 데이터를 **저장하지**&#x200B;않으므로, Experience Platform을 사용하여 데이터 수명 주기를 처리할 수 있습니다. 고급 데이터 수명주기 관리를 통해 데이터 세트와 레코드 레벨에서 데이터 수명주기를 관리할 수 있습니다.

예를 들어, 컴포지션 캔버스에서 활동 저장 블록을 사용하여 대상을 만들면 결과 대상은 Experience Platform의 데이터 레이크에 외부 대상으로 저장됩니다. 이 데이터는 Federated Audience Composition에 저장된 **not**&#x200B;이므로 Audience Portal에서 대상이 삭제되면 대상 데이터 및 해당 데이터 세트가 자동으로 삭제됩니다.

또는 작성 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 결과 보강은 Experience Platform에 프로필 활성화 스키마 및 프로필 활성화 데이터 세트로 저장됩니다. 따라서 데이터 라이프사이클에서 프로필에 액세스하고 정리할 수 있습니다.

데이터 수명 주기 사용에 대한 자세한 내용은 [데이터 수명 주기 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/data-lifecycle/home){target="_blank"}를 참조하십시오.

## 데이터 사용 레이블 {#data-usage-labels}

데이터 사용 레이블을 사용하면 해당 데이터에 적용되는 거버넌스 정책을 기반으로 데이터 세트와 필드를 분류할 수 있습니다. 컴포지션을 사용하여 대상자를 만든 후 결과 스키마에 적절한 데이터 레이블을 적용하여 필요한 사용 제한 사항을 준수하도록 할 수 있습니다.

데이터 레이블 사용에 대한 자세한 내용은 [데이터 사용 레이블 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/labels/overview){target="_blank"}를 참조하십시오.

## 암호화 {#encryption}

유연한 대상 구성은 활용도가 낮은 데이터 암호화, 전송 중인 데이터 암호화 및 고객 관리 키를 통해 암호화를 제공합니다.

사용 중인 데이터는 Federated Audience Composition 내에서 사용되는 고객 데이터를 나타냅니다. 데이터는 클라우드 서비스 공급자에 의해 암호화되며, 암호화된 형태로 Federated Audience Composition에 사용됩니다.

전송 중인 데이터는 Federated Audience Composition에서 한 구성 요소에서 다른 구성 요소로 이동할 때 고객 데이터를 참조합니다. 데이터는 HTTPS에서 TLS 1.3을 사용하여 Federated Audience Composition 구성 요소 전체에서 암호화됩니다.

Adobe에서 데이터 암호화를 처리하는 방법에 대한 자세한 내용은 Experience Platform의 [데이터 암호화](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}에 대한 안내서를 참조하십시오.

### 고객 관리 키 {#customer-managed-keys}

고객 관리 키를 사용하면 자체 암호화 키를 사용하여 데이터를 암호화할 수 있으므로 데이터를 제어할 수 있습니다. Federated Audience Composition은 고객 데이터를 **저장하지**&#x200B;하므로, 고객 관리 키는 Experience Platform의 데이터 레이크에 저장되므로 결과 대상 및 풍부에서 바로 사용할 수 있습니다.

고객 관리 키에 대한 자세한 내용은 [고객 관리 키 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}를 참조하십시오.

## 감사 로그 {#audit-log}

Federated Audience Composition에서 수행된 모든 만들기, 읽기, 업데이트 및 삭제 작업은 감사 추적에 기록됩니다. 이 감사 로그를 사용하여 이러한 작업을 추적하고, 책임을 적용하며, 규정 준수 감사를 지원할 수 있습니다.

자세한 내용은 [감사 추적 개요](/help/admin/audit-trail.md){target="_blank"}를 참조하십시오.

## 액세스 제어 {#access-control}

필드 및 역할 기반 수준 모두에서 Federated Audience Composition에 대한 액세스를 제어할 수 있습니다. 이러한 액세스 제어를 사용하여 데이터 거버넌스 정책을 시행하고, 중요한 정보의 노출을 제한하며, 사용자 책임에 따라 액세스를 조정할 수 있습니다.

Federated Audience Composition의 액세스 제어에 대한 자세한 내용은 [Access Federated Audience Composition 안내서](/help/start/feature-access.md){target="_blank"}를 참조하십시오.

## 데이터 로컬라이제이션 {#data-localization}

Federated Audience Composition에서 고객 데이터를 저장하지 **않습니다**. 따라서 데이터를 동일한 지역에 보관하려면 **only**&#x200B;에서 외부 데이터베이스를 일치하는 샌드박스 지역과 연결해야 합니다. 다른 지역의 데이터베이스를 샌드박스에 연결하는 경우 Adobe은 데이터 현지화를 **담당하지 않습니다**.

## 다음 단계 {#next-steps}

이 안내서를 읽은 후에는 데이터 거버넌스, 개인 정보 보호 규정 준수, 동의 시행, 데이터 라이프사이클 관리 및 액세스 제어를 포함하여 Federated Audience Composition에 사용 중인 개인 정보 보호 및 보안 기능에 대해 더 잘 이해할 수 있습니다.
