---
title: 페더레이션된 대상자 구성의 개인정보보호 및 보안
description: 페더레이션된 대상자 구성이 데이터 거버넌스, 동의 시행, 액세스 제어, 데이터 암호화 및 개인정보보호 규정 준수와 같은 기능을 포함하여 사용자 데이터의 개인정보보호 및 보안을 어떻게 처리하는지 알아봅니다.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# 페더레이션된 대상자 구성의 개인정보보호 및 보안

페더레이션된 대상자 구성은 데이터를 처리하는 동안 데이터를 보호하기 위해 수많은 보안 관행을 준수합니다.

## Privacy Service {#privacy}

페더레이션된 대상자 구성은 Adobe Experience Platform과 Adobe Journey Optimizer가 사용할 수 있도록 페더레이션된 데이터를 제공합니다. 하지만 페더레이션된 대상자 구성은 데이터 웨어하우스의 고객 데이터를 **저장하지 않습니다**. 따라서 Adobe Experience Platform Privacy Service를 사용하여 데이터 주체 및 데이터 삭제 요청을 준수할 수 있습니다.

예를 들어 컴포지션 캔버스의 저장 활동 블록을 사용하여 대상자를 생성하면 결과 대상자가 Experience Platform의 데이터 레이크에 외부 대상자로 저장됩니다. 이 외부 대상자는 ID 필드와 ID 네임스페이스로 표시됩니다. 따라서 Privacy Service를 사용하여 외부 대상자의 해당 프로필에 액세스하고 삭제할 수 있습니다.

또는 컴포지션 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 생성된 강화를 프로필 활성화 스키마와 프로필 활성화 데이터 세트로 Experience Platform에 저장합니다. 이 강화 데이터는 ID 필드와 ID 네임스페이스로 표시됩니다. 따라서 Privacy Service를 사용하여 이러한 프로필에 액세스하고 이를 정리할 수 있습니다.

Privacy Service에 대한 자세한 내용은 [Privacy Service 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/home){target="_blank"}를 참조하십시오.

### 개인정보보호 요청 {#privacy-requests}

Privacy Service에서 페더레이션된 대상자 구성의 고객 데이터에 액세스하고 삭제하기 위한 개별 개인정보보호 요청을 만들고 관리할 수 있습니다. Privacy Service는 고객 데이터 요청을 관리하는 데 도움이 되는 [사용자 인터페이스](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ko-KR){target="_blank"} 및 [RESTful API](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/api/overview){target="_blank"}를 제공합니다.

개인정보보호 요청 만들기 및 관리에 대한 자세한 내용은 [Privacy Service UI 안내서의 개인정보보호 작업](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/ui/user-guide){target="_blank"}을 참조하십시오.

## 동의 정책 시행 {#consent}

Experience Platform을 통한 페더레이션된 대상자 구성은 고객에게 제공된 동의에 따라 대상자를 활성화할 수 있도록 동의 시행을 자동화하는 도구를 제공합니다.

예를 들어 컴포지션 캔버스의 저장 활동 블록을 사용하여 대상자를 생성하면 결과 대상자가 Experience Platform의 데이터 레이크에 외부 대상자로 저장됩니다. Experience Platform은 활성화 시 동의 유효성 검사를 자동으로 지원합니다. 자세한 내용은 [세분화 서비스 FAQ](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/faq#consent){target="_blank"}를 참조하십시오.

또는 컴포지션 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 생성된 강화를 프로필 활성화 스키마와 프로필 활성화 데이터 세트로 Experience Platform에 저장합니다. 기존 프로필의 경우 활성화 시 사용 가능한 동의 속성이 자동으로 적용됩니다. 새로운 프로필의 경우 활성화 시 프로필 수집 중 제공된 동의 속성이 자동으로 적용됩니다. 프로필에 동의를 적용하는 방법에 대한 자세한 내용은 [동의 및 기본 설정 필드 그룹 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}를 참조하십시오.

동의 적용에 대한 자세한 내용은 [정책 관리 UI 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}를 참조하십시오.

## 데이터 라이프사이클 {#data-lifecycle}

페더레이션된 대상자 구성은 데이터 웨어하우스의 고객 데이터를 **저장하지 않으므로** Experience Platform을 사용하여 데이터 라이프사이클을 처리할 수 있습니다. 고급 데이터 라이프사이클 관리를 통해 데이터 세트와 레코드 수준 모두에서 데이터 라이프사이클을 관리할 수 있습니다.

예를 들어 컴포지션 캔버스의 저장 활동 블록을 사용하여 대상자를 생성하면 결과 대상자가 Experience Platform의 데이터 레이크에 외부 대상자로 저장됩니다. 이 데이터는 페더레이션된 대상자 구성에 **저장되지 않으므로** 대상자 포털에서 해당 대상자를 삭제하면 대상자 데이터와 해당 데이터 세트도 자동으로 삭제됩니다.

또는 컴포지션 캔버스에서 프로필 저장 활동을 사용하여 프로필 강화를 만든 후 생성된 강화를 프로필 활성화 스키마와 프로필 활성화 데이터 세트로 Experience Platform에 저장합니다. 따라서 데이터 라이프사이클을 통해 프로필에 접근하고 정리할 수 있습니다.

데이터 라이프사이클에 대한 자세한 내용은 [데이터 라이프사이클 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/data-lifecycle/home){target="_blank"}를 참조하십시오.

## 데이터 사용 레이블 {#data-usage-labels}

데이터 사용 레이블을 사용하면 해당 데이터에 적용되는 거버넌스 정책에 따라 데이터 세트와 필드를 분류할 수 있습니다. 컴포지션을 사용하여 대상자를 만든 후 결과 스키마에 적절한 데이터 레이블을 적용하여 필요한 사용 제한을 준수하는지 확인할 수 있습니다.

데이터 레이블 사용에 대한 자세한 내용은 [데이터 사용 레이블 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/labels/overview){target="_blank"}를 참조하십시오.

## 암호화 {#encryption}

유연한 대상자 구성은 사용하지 않는 데이터 암호화, 전송 중인 데이터 암호화 및 고객 관리 키를 통해 암호화를 제공합니다.

사용하지 않는 데이터는 페더레이션된 대상자 구성에서 사용되는 고객 데이터를 말합니다. 해당 데이터는 클라우드 서비스 제공업체에 의해 암호화되며, 암호화된 형태로 페더레이션된 대상자 구성에 사용됩니다.

전송 중인 데이터는 페더레이션된 대상자 구성의 한 구성 요소에서 다른 구성 요소로 이동하는 고객 데이터를 의미합니다. 해당 데이터는 HTTPS를 통한 TLS 1.3을 사용하여 페더레이션된 대상자 구성 요소 전체에 걸쳐 암호화된 상태로 유지됩니다.

Adobe에서 데이터 암호화를 처리하는 방법에 대한 자세한 내용은 [Experience Platform의 데이터 암호화 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}를 참조하십시오.

### 고객 관리 키 {#customer-managed-keys}

고객 관리 키를 사용하면 고객이 암호화 키를 사용하여 데이터를 암호화하여 데이터를 제어할 수 있습니다. 페더레이션된 대상자 구성은 고객 데이터를 **저장하지 않고**, Experience Platform의 데이터 레이크에 저장되므로, 결과 대상자와 시행에 고객 관리 키를 직접 사용할 수 있습니다.

고객 관리 키에 대한 자세한 내용은 [고객 관리 키 안내서](https://experienceleague.adobe.com/ko/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}를 참조하십시오.

## 감사 로그 {#audit-log}

페더레이션된 대상자 구성에서 수행된 모든 생성, 읽기, 업데이트 및 삭제 작업은 감사 추적에 기록됩니다. 이 감사 로그를 사용하여 이들 액션을 추적하고, 책임을 강화하며, 규정 준수 감사를 지원할 수 있습니다.

자세한 내용은 [감사 추적 개요](/help/admin/audit-trail.md){target="_blank"}를 참조하십시오.

## 액세스 제어 {#access-control}

필드 및 역할 기반 수준에서 페더레이션된 대상자 구성에 대한 액세스를 제어할 수 있습니다. 이러한 액세스 제어를 사용하여 데이터 거버넌스 정책을 시행하고, 민감한 정보의 노출을 제한하며, 액세스를 사용자 책임에 맞게 조정할 수 있습니다.

페더레이션된 대상자 구성의 액세스 제어에 대한 자세한 내용은 [페더레이션된 대상자 구성 액세스 안내서](/help/start/feature-access.md){target="_blank"}를 참조하십시오.

## 데이터 지역화 {#data-localization}

페더레이션된 대상자 구성 모든 고객 데이터를 **저장하지 않습니다**. 따라서 데이터를 동일한 지역에 보관하려면 외부 데이터베이스를 일치하는 샌드박스 지역에 **연결만** 해야 합니다. 다른 지역의 데이터베이스를 샌드박스에 연결하는 경우 Adobe는 데이터 지역화 대한 **책임이 없습니다**.

## 다음 단계 {#next-steps}

이 안내서를 읽고 나면 데이터 거버넌스, 개인정보보호 규정 준수, 동의 시행, 데이터 라이프사이클 관리, 액세스 제어 등 페더레이션된 대상자 구성에 사용되는 개인정보 보호 및 보안 기능에 대해 더 잘 이해할 수 있습니다.
