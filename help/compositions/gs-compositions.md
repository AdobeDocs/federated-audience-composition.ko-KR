---
audience: end-user
title: 컴포지션 시작
description: 컴포지션으로 시작하는 방법 알아보기
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 8%

---

# 컴포지션 시작 {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="컴포지션 속성"
>abstract="이 단원에서는 컴포지션을 만들 때도 액세스할 수 있는 일반 컴포지션 속성을 제공합니다."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="컴포지션 세그멘테이션"
>abstract="기본적으로 컴포지션의 마지막 실행의 작업 테이블만 유지됩니다. 이 옵션을 활성화하면 테스트 목적으로 작업 테이블을 유지할 수 있습니다. 사용해야 합니다. **전용** 개발 또는 스테이징 환경에서 프로덕션 환경에서는 확인하지 않아야 합니다."




## 컴포지션이란 무엇입니까? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="컴포지션"
>abstract="이 화면에서 전체 컴포지션 목록에 액세스하고, 현재 상태, 마지막/다음 실행 날짜를 확인하고, 새 컴포지션을 만들 수 있습니다."


## 오류 관리 설정  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="오류 관리 설정"
>abstract="이 섹션에서는 실행 중에 오류를 관리하는 방법을 정의할 수 있습니다. 프로세스를 일시 중지하거나 특정 오류 수를 무시하거나 작성 실행을 중지하도록 선택할 수 있습니다."

* **[!UICONTROL 오류 관리]**: 이 필드에서는 작성 활동에 오류가 있을 경우 수행할 작업을 정의할 수 있습니다.
다음과 같은 세 가지 옵션이 있습니다.

   * **[!UICONTROL 프로세스 일시 중단]**: 컴포지션이 자동으로 일시 중지되고 상태가 (으)로 변경됩니다. **[!UICONTROL 실패]**. 문제가 해결되면 **[!UICONTROL 다시 시작]** 단추.
   * **[!UICONTROL 무시]**: 오류를 트리거한 작업의 상태가 (으)로 변경됩니다. **[!UICONTROL 실패]**, 그러나 컴포지션은 **[!UICONTROL 시작됨]** 상태.
   * **[!UICONTROL 프로세스 중단]**: 컴포지션이 자동으로 중지되고 상태가 다음으로 변경됨 **[!UICONTROL 실패]**. 문제가 해결되면 **[!UICONTROL 시작]** 단추를 클릭합니다.

* **[!UICONTROL 연속 오류]**: 이 필드는 다음과 같은 경우에 사용할 수 있습니다. **[!UICONTROL 무시]** 다음에서 값이 선택됨: **[!UICONTROL 오류가 있는 경우]** 필드. 프로세스가 중지되기 전에 무시할 수 있는 오류 수를 지정할 수 있습니다. 이 수에 도달하면 작성 상태가 (으)로 변경됩니다. **[!UICONTROL 실패]**. 이 필드의 값이 0이면 오류 수에 관계없이 작성을 중지하지 않습니다.
