---
audience: end-user
title: 스케줄러 활동 사용
description: 스케줄러 활동을 사용하는 방법 알아보기
exl-id: 3e8be2a2-2227-42f4-a512-b9e686ba0f66
source-git-commit: 8fa60d20dc574bbddc0106508d57a1cd3f3d3db8
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 29%

---

# 스케줄러 {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="스케줄러 활동"
>abstract="**스케줄러** 활동을 사용하면 대상자 컴포지션이 시작되는 시기를 예약할 수 있습니다. 이 활동은 시작을 예약하는 것으로 생각해야 합니다. 컴포지션의 첫 번째 활동으로만 사용할 수 있습니다."

**스케줄러** 활동은 **흐름 제어** 활동입니다. 이를 통해 컴포지션이 시작되는 시기를 예약할 수 있습니다. 이 활동은 시작을 예약하는 것으로 생각해야 합니다. 컴포지션의 첫 번째 활동으로만 사용할 수 있습니다.

Federated Audience Composition 대상에 대한 연결을 구성한 경우 이 활동을 사용하여 Adobe Experience Platform 대상자를 정기적인 빈도로 보낼 수 있습니다. [외부 데이터로 Adobe Experience Platform 대상자를 보강하는 방법을 알아봅니다](../../connections/destinations.md)

![](../assets/scheduler.png)

## 스케줄러 활동 구성 {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="스케줄러 유효성"
>abstract="스케줄러의 유효 기간을 정의할 수 있습니다. 영구적(기본값)이거나 특정 날짜까지 유효할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="스케줄러 옵션"
>abstract="스케줄러의 빈도를 정의합니다. 특정 순간, 하루에 한 번 또는 여러 번, 일주일 또는 한 달로 실행할 수 있습니다."

**스케줄러** 활동을 구성하려면 다음 단계를 따르십시오.

1. 작성에 **스케줄러** 활동을 추가합니다.

1. **실행 빈도**&#x200B;를 구성합니다.

   * **한 번**: 컴포지션이 한 번 실행됩니다.
   * **일별**: 컴포지션이 하루에 한 번, 특정 시간에 실행됩니다.
   * **하루에 여러 번:** 컴포지션이 하루에 여러 번 규칙적으로 실행됩니다. 특정 시간에 실행되거나 주기적으로 실행되도록 설정할 수 있습니다.

     >[!NOTE]
     >
     >전체 시스템 성능을 저해하고 데이터베이스에 블록을 만들 수 있으므로 컴포지션을 15분 간격으로 이상 실행하도록 예약하지 마십시오.

   * **주별**: 컴포지션이 일주일에 한 번 또는 여러 번, 지정한 시점에 실행됩니다.
   * **월별**: 컴포지션이 한 달에 한 번 또는 여러 번, 지정한 시점에 실행됩니다. 컴포지션을 실행해야 하는 월을 선택할 수 있습니다. 해당 월의 지정된 요일(예: 해당 월의 두 번째 화요일)에 실행을 설정할 수도 있습니다.

1. 선택한 빈도에 따라 실행의 세부 정보를 정의합니다. 세부 정보 필드는 사용하는 빈도(시간, 반복 빈도, 지정된 날짜 등)에 따라 달라질 수 있습니다.

1. **실행 시간 미리 보기**&#x200B;를 클릭하여 컴포지션의 다음 10개 실행 일정을 확인합니다.

1. 스케줄러의 유효 기간을 정의합니다.

   * **영구(만료되지 않음)**: 시간 프레임이나 반복 횟수 제한 없이 지정한 빈도대로 컴포지션이 실행됩니다.

   * **유효 기간**: 특정 날짜까지 지정한 빈도대로 컴포지션이 실행됩니다. 시작 및 종료 날짜를 지정해야 합니다.

>[!NOTE]
>
>작성을 바로 시작하려면 스케줄러의 상단 작업 표시줄에서 **보류 중인 작업 실행**&#x200B;을 클릭합니다. 이 단추는 작성을 시작한 경우에만 사용할 수 있습니다.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->
