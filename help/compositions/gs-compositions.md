---
audience: end-user
title: 컴포지션 시작하기
description: 컴포지션을 시작하는 방법 알아보기
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# 컴포지션 시작하기 {#compositions}

>[!AVAILABILITY]
>
>컴포지션에 액세스하려면 다음 권한 중 하나가 필요합니다.
>
>-**페더레이션된 컴포지션 관리**
>>-**페더레이션된 컴포지션 보기**
>
>필요한 권한에 대한 자세한 내용은 [페더레이션된 대상자 컴포지션 액세스 안내서](/help/start/feature-access.md)를 참조하십시오.

## 컴포지션이란? {#what}

Adobe 대상자 컴포지션을 사용하면 다양한 활동(분할, 제외…)을 시각적 캔버스로 활용하여 대상자를 생성할 수 있는 컴포지션을 만들 수 있습니다. 완료되면 결과 대상자는 기존 대상자와 함께 Adobe Experience Platform에 저장되며, 이를 Adobe Experience Platform 대상 및 Adobe Journey Optimizer에서 활용하여 고객을 타기팅할 수 있습니다. [대상자를 사용한 작업 방법 알아보기](../start/audiences.md)

![](assets/composition-example.png)

## 컴포지션 액세스 및 관리 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="컴포지션"
>abstract="이 화면에서 컴포지션 전체 목록에 액세스하고 현재 상태, 마지막/다음 실행 일자를 확인하고 새 컴포지션을 만들 수 있습니다."

컴포지션은 Adobe Experience Platform **[!UICONTROL 대상자]** 메뉴의 **[!UICONTROL 페더레이션된 컴포지션]** 탭에서 액세스할 수 있습니다.

이 화면에서 새 컴포지션을 만들고 기존 컴포지션에 액세스할 수 있습니다. 이름 옆에 있는 줄임표 버튼을 클릭하여 기존 컴포지션을 복제하거나 삭제할 수도 있습니다.

![](assets/compositions-list.png)

목록을 세분화하고 원하는 컴포지션을 쉽게 찾으려면 목록을 검색하고 상태나 마지막 처리 날짜를 기준으로 컴포지션을 필터링할 수 있습니다.

열을 추가하거나 제거하여 목록을 사용자 정의할 수도 있습니다. 이렇게 하려면 **[!UICONTROL 열 구성]** 버튼을 클릭하고 원하는 출력 열을 추가하거나 제거합니다.

![](assets/compositions-columns.png)

## 컴포지션 상태 {#status}

컴포지션에는 여러 가지 상태가 있을 수 있습니다.

* **[!UICONTROL 초안]**: 컴포지션이 생성되어 저장되었습니다.
* **[!UICONTROL 진행 중]**: 컴포지션이 실행되었으며 현재 실행 중입니다.
* **[!UICONTROL 중지됨]**: 컴포지션 실행이 완료되어 중지되었습니다.
* **[!UICONTROL 일시 정지됨]**: 컴포지션 실행이 일시 정지되었습니다.
* **[!UICONTROL 오류]**: 컴포지션 실행 중에 오류가 발생했습니다. 컴포지션을 열고 로그와 작업에 액세스하여 오류를 식별하고 해결합니다.

컴포지션을 시작하고 모니터링하는 방법에 대한 자세한 내용은 [이 섹션](../compositions/start-monitor-composition.md)에서 확인할 수 있습니다.
