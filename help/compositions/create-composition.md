---
audience: end-user
title: 컴포지션 만들기
description: 컴포지션 만들기 방법 알아보기
badge: label="제한된 가용성" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 1a90702a02e30712e95fdf48342f1dea3b92e360
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 21%

---

# 구성 만들기 {#create}

컴포지션을 만드는 첫 번째 단계는 해당 레이블을 정의하고 필요한 경우 추가 설정을 구성하는 것입니다.

## 컴포지션 만들기 {#create-the-composition}

1. **[!UICONTROL 대상자]** 메뉴에 액세스하고 **[!UICONTROL 통합 구성]** 탭을 선택합니다.

1. **[!UICONTROL 컴포지션 만들기]** 단추를 클릭합니다.

   ![](assets/composition-create.png)

1. **[!UICONTROL 속성]** 섹션에서 컴포지션에 대한 레이블을 지정하고 데이터 모델을 선택합니다. 이 데이터 모델과 연결된 스키마만 컴포지션의 활동에서 사용할 수 있습니다.

   ![](assets/composition-select-schema.png)

1. Click **[!UICONTROL Create]**. 컴포지션 캔버스가 표시됩니다. 이제 실행하기 전에 필요에 맞게 활동을 추가하여 컴포지션을 구성할 수 있습니다.

   * [활동 오케스트레이션 방법 알아보기](#action-activities)
   * [컴포지션을 시작하고 모니터링하는 방법 알아보기](#save)

## 구성 설정을 구성합니다. {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="구성 속성"
>abstract="이 섹션에서는 구성을 생성할 때도 액세스할 수 있는 일반 구성 속성을 제공합니다."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="구성 세분화"
>abstract="기본적으로 구성의 마지막 실행에 대한 작업 테이블만 유지됩니다. 이 옵션을 활성화하여 테스트 목적으로 작업 테이블을 유지할 수 있습니다. 개발 또는 스테이징 환경&#x200B;**에서만** 사용해야 합니다. 프로덕션 환경에서는 체크해서는 안 됩니다."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="오류 관리 설정"
>abstract="이 섹션에서는 실행 중 오류를 관리하는 방법을 정의할 수 있습니다. 프로세스를 일시 중지하거나, 특정 수의 오류를 무시하거나, 구성 실행을 중지하도록 선택할 수 있습니다."

컴포지션에 액세스할 때 고급 설정에 액세스하여 오류 발생 시 컴포지션의 동작 방식 등을 정의할 수 있습니다. 이러한 추가 옵션에 액세스하려면 컴포지션 만들기 화면의 위쪽 섹션에 있는 **[!UICONTROL 설정]** 단추를 클릭합니다.

![](assets/composition-create-settings.png)

사용 가능한 설정은 다음과 같습니다.

* **[!UICONTROL 레이블]**: 컴포지션의 레이블을 변경합니다.

* **[!UICONTROL 두 실행 사이의 중간 모집단 결과를 유지합니다]**: 기본적으로 마지막 컴퍼지션 실행의 작업 테이블만 유지됩니다. 이전 실행의 작업 테이블은 매일 실행되는 기술 구성에 의해 삭제됩니다.

  이 옵션을 활성화하면 컴포지션이 실행된 후에도 작업 테이블이 유지됩니다. 테스트 목적으로 사용할 수 있으므로 개발 또는 스테이징 환경에서 **전용**&#x200B;을 사용해야 합니다. 프로덕션 구성에서 확인하지 않아야 합니다.

* **[!UICONTROL 오류 관리]**: 이 옵션을 사용하면 작성 활동에 오류가 있는 경우 수행할 작업을 정의할 수 있습니다. 다음과 같은 세 가지 옵션이 있습니다.

   * **[!UICONTROL 프로세스 일시 중단]**: 컴포지션이 자동으로 일시 중지되고 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 문제가 해결되면 **[!UICONTROL 다시 시작]** 단추를 사용하여 작성을 다시 시작하십시오.
   * **[!UICONTROL 무시]**: 오류를 트리거한 작업의 상태가 **[!UICONTROL 실패]**(으)로 변경되지만 컴포지션은 **[!UICONTROL 시작됨]** 상태를 유지합니다.
   * **[!UICONTROL 프로세스 중단]**: 컴포지션이 자동으로 중지되고 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 문제가 해결되면 **[!UICONTROL 시작]** 단추를 사용하여 작성을 다시 시작하십시오.

* **[!UICONTROL 연속 오류]**: 프로세스를 중지하기 전에 무시할 수 있는 오류 수를 지정합니다. 이 수에 도달하면 컴포지션 상태가 **[!UICONTROL 실패]**(으)로 변경됩니다. 이 필드의 값이 0이면 오류 수에 관계없이 작성을 중지하지 않습니다.
