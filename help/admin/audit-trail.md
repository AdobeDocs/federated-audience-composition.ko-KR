---
audience: end-user
title: 감사 추적
description: 작업 및 이벤트가 기록되고 감사 추적에서 액세스할 수 있는 방법을 알아봅니다
exl-id: 97142f54-53ce-4c2a-9d89-fdcb2a47b159
source-git-commit: 16d307172ec6ad2d64f50b686d2d251267ce29ae
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 14%

---

# 감사 추적 {#audit-trail}

>[!AVAILABILITY]
>
>감사 추적에 액세스하려면 다음 권한이 필요합니다.
>
>-**감사 추적 보기**
>
>필요한 권한에 대한 자세한 내용은 [액세스 제어 안내서](/help/governance-privacy-security/access-control.md)를 참조하십시오.

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="감사 추적"
>abstract="감사 추적 기능은 Adobe Experience Platform 페더레이션된 대상자 컴포지션 환경에 발생한 모든 액션과 이벤트에 대한 자세한 시간순 기록을 실시간으로 제공합니다."

**[!UICONTROL 감사 추적]** 기능은 Adobe Federated Composition 인스턴스 내에서 발생하는 작업 및 이벤트에 대한 자세한 로그를 실시간으로 지속적으로 기록합니다. 편리한 방법을 사용하여 데이터의 시간 기록 레코드에 액세스하고, 워크플로 상태, 이를 수정할 최신 개인 또는 인스턴스 내에서 사용자가 수행한 활동과 같은 쿼리를 해결합니다.

+++ 감사 추적 사용 가능한 엔터티에 대해 자세히 알아보기

* **Source 스키마 감사 추적**&#x200B;을 통해 Adobe Federated Audience Composition 인스턴스 내에서 스키마에 대한 활동 및 최근 수정 사항을 모니터링할 수 있습니다.

  스키마에 대한 자세한 내용은 이 [페이지](../customer/schemas.md)를 참조하세요.

* **워크플로우 감사 추적**&#x200B;을 통해 다음과 같은 현재 상태를 포함하여 워크플로우에 대한 활동 및 최근 변경 사항을 추적할 수 있습니다.

   * 시작
   * 일시 정지
   * 정지
   * 다시 시작
   * 정리 - 작업 삭제 내역에 해당합니다.
   * 시뮬레이션 모드에서 시작 작업과 동일한 시뮬레이션
   * 지금 대기 중인 작업 실행 작업과 동일한 절전 모드 해제
   * 무조건 정지

  워크플로우에 대한 자세한 내용은 이 [페이지](../compositions/gs-compositions.md)를 참조하세요.

* **외부 계정**&#x200B;을(를) 사용하면 Adobe 대상 구성 인스턴스에서 외부 계정에 대한 수정 사항을 확인할 수 있습니다.

  외부 계정에 대한 자세한 내용은 이 [페이지](../connections/home.md)를 참조하세요.

+++

## 감사 추적 액세스 {#accessing-audit-trail}

인스턴스의 **[!UICONTROL 감사 추적]**&#x200B;에 액세스하려면:

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 감사 추적]**&#x200B;을 선택합니다.

1. 엔터티 목록과 함께 **[!UICONTROL 감사 추적]** 창이 열립니다. Federated Audience Composition은 워크플로우, 옵션, 게재 및 스키마에 대한 만들기, 편집 및 삭제 작업을 감사합니다.

   ![](assets/audit_trail.png)

1. **[!UICONTROL 감사 엔터티]** 창은 다음과 같이 선택한 엔터티에 대한 자세한 정보를 제공합니다.

   * **[!UICONTROL 유형]**: 워크플로, 옵션, 게재 또는 스키마.
   * **[!UICONTROL 엔터티]**: 활동의 내부 이름입니다.
   * **[!UICONTROL 수정한 사람]**: 이 엔터티를 마지막으로 수정한 사람의 사용자 이름입니다.
   * **[!UICONTROL Action]**: 이 엔터티에서 마지막으로 수행한 작업이 생성, 수정 또는 삭제되었습니다.
   * **[!UICONTROL 수정 날짜]**: 이 엔터티에서 마지막으로 수행한 작업의 날짜입니다.
