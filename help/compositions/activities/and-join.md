---
audience: end-user
title: AND-join 활동 사용
description: AND-join 활동을 사용하는 방법 알아보기
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 57%

---

# AND-결합 {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-결합 활동"
>abstract="**AND-결합** 활동을 사용하면 구성의 여러 실행 분기를 동기화할 수 있습니다. 이전 활동이 모두 완료되면 트리거됩니다. 이로써 구성을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다."

다음 **AND-결합** 활동을 사용하면 컴포지션의 여러 실행 분기를 동기화할 수 있습니다.

이 활동은 모든 인바운드 전환이 활성화되었을 때, 즉 앞선 활동이 모두 완료된 다음에만 아웃바운드 전환을 트리거합니다. 이렇게 하면 컴포지션을 계속 실행하기 전에 특정 활동이 완료되었는지 확인할 수 있습니다.

## AND-결합 활동 구성 {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="AND-결합 활동 구성"
>abstract="참여하고자 하는 활동을 선택합니다. **기본 세트** 드롭다운에서 유지하고자 하는 인바운드 전환 모집단을 선택합니다."

**AND-결합** 활동을 구성하려면 다음 단계를 따르십시오.

1. 여러 활동을 추가하여 두 개 이상의 실행 분기를 만듭니다.
1. 임의의 분기에 **AND-결합** 활동을 추가합니다.

   ![](../assets/and-join.png)

1. 다음에서 **병합 옵션** 섹션에서 동기화하려는 모든 이전 활동을 확인합니다.
1. **기본 세트** 드롭다운에서 유지하고자 하는 인바운드 전환 모집단을 선택합니다. 아웃바운드 전환은 인바운드 전환 모집단 중 하나만 포함할 수 있습니다. 활동이 구성되지 않은 경우 아웃바운드 전환은 인바운드 모집단 중 하나를 임의로 선택합니다.
