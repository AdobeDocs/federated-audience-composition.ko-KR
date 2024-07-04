---
audience: end-user
title: 대기 활동 사용
description: 대기 활동을 사용하는 방법 알아보기
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 60%

---

# 대기 {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="대기 활동"
>abstract="**대기** 활동을 사용하여 전환을 활동에서 다른 활동으로 지연합니다."

다음 **대기** 활동을 사용하면 실행 중인 두 활동 사이에 일정 시간이 경과할 수 있습니다. 예를 들어 이메일 게재 활동 후 며칠 동안 대기하고, 후속 작업(리마인더 이메일, 대상자 만들기 등)을 수행하기 전에 대기 기간 동안 발생한 열람수 및 클릭수를 분석하려 할 때 사용할 수 있습니다.

## 구성{#wait-configuration}

**대기** 활동을 구성하려면 다음 단계를 따르십시오.

1. 추가 **대기** 활동을 작성에 추가합니다.

1. 인바운드 전환과 아웃바운드 전환 사이의 대기 **기간**&#x200B;을 지정합니다.

1. 에서 시간 단위 선택 **마침표** 필드: 초, 분, 시간, 일.


