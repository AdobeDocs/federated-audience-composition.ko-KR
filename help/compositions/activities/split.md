---
audience: end-user
title: 분할 활동 사용
description: 분할 활동을 사용하는 방법 알아보기
exl-id: 6346eef6-b164-40cf-9402-b5ff208af97f
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '923'
ht-degree: 77%

---

# 분할 {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="분할 활동"
>abstract="**분할** 활동은 필터링 규칙 또는 집단 크기와 같은 다양한 선택 기준에 따라 수신 집단을 여러 하위 집합으로 세그먼트화할 수 있습니다."

**분할** 활동은 필터링 규칙 또는 집단 크기와 같은 다양한 선택 기준에 따라 수신 집단을 여러 하위 집합으로 세그먼트화할 수 있습니다.

## 분할 활동 구성 {#split-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="분할 활동용 세그먼트"
>abstract="수신 집단을 세그먼트로 나누려면 원하는 만큼 하위 집합을 추가합니다.<br/></br>**분할** 활동이 실행되면 집단이 활동에 추가된 순서대로 여러 하위 집합에 걸쳐 세그먼트로 나뉩니다. 컴포지션을 시작하기 전에 화살표 버튼을 사용하여 필요에 맞게 하위 집합의 순서를 지정했는지 확인해야 합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="분할 활동 필터"
>abstract="하위 집합에 필터링 조건을 적용하려면 **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하고 쿼리 모델러를 사용하여 원하는 필터링 조건을 구성합니다. 예를 들어 데이터베이스에 이메일 주소가 존재하는 수신 집단의 프로필을 포함합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="분할 활동 제한"
>abstract="하위 집합에서 선택한 프로필 수를 제한하려면 **[!UICONTROL 제한 활성화]** 옵션을 토글하고 포함할 집단의 수 또는 백분율을 지정합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="분할 활동 정렬"
>abstract="하위 집합에 대해 집단 제한을 설정할 때 특정 프로필 속성을 기준으로 선택한 프로필의 등급을 오름차순 또는 내림차순으로 지정할 수 있습니다. 이렇게 하려면 정렬 활성화 옵션을 토글합니다. 이렇게 하려면 **정렬 활성화** 옵션을 토글합니다. 예를 들어 구매 금액이 가장 높은 상위 50개 프로필만 포함하도록 하위 집합을 제한할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="여집합 생성 분할"
>abstract="모든 하위 집합을 구성한 후에는 하위 집합과 일치하지 않는 나머지 집단을 선택하여 추가 아웃바운드 전환에 포함할 수 있습니다. 이렇게 하려면 **여집합 생성** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="동일 테이블의 모든 하위 집합 생성"
>abstract="모든 하위 집합을 단일 출력 전환으로 그룹화하려면 이 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="빈 전환 건너뛰기"
>abstract="수신 집단이 비어 있는 경우, **[!UICONTROL 빈 전환 건너뛰기]** 옵션을 토글하여 이 하위 집합에 대한 출력 전환을 비활성화합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="출력 집단의 중복 활성화"
>abstract="**[!UICONTROL 출력 집단의 중복 활성화]** 옵션을 사용하면 여러 하위 집합에 속하는 집단을 관리할 수 있습니다. 확인란을 선택하지 않으면 분할 활동은 수신자가 여러 하위 집합의 기준을 충족하더라도 여러 출력 전환에 표시되지 않습니다. 기준이 일치하는 첫 번째 탭의 대상에 포함됩니다. 확인란을 선택하면 필터 조건을 충족하는 경우 여러 하위 집합에서 수신자를 찾을 수 있습니다. "

**분할** 활동을 구성하려면 다음 단계를 따르십시오.

1. 컴포지션에 **분할** 활동을 추가합니다.

1. 활동 구성 창이 기본 하위 집합과 함께 열립니다. 수신 모집단을 세그먼트화하기 위해 원하는 만큼 하위 집합을 추가하려면 **세그먼트 추가** 버튼을 클릭합니다.

   >[!IMPORTANT]
   >
   >**분할** 활동이 실행되면 집단이 활동에 추가된 순서대로 여러 하위 집합에 걸쳐 세그먼트로 나뉩니다. 예를 들어 첫 번째 하위 집합이 초기 모집단의 70%를 복구하는 경우 다음으로 추가된 하위 집합은 나머지 30%에만 선택 기준을 적용하는 식입니다.
   >
   >작성을 시작하기 전에 요구 사항에 맞는 순서로 하위 세트를 주문했는지 확인하십시오. 이렇게 하려면 화살표 단추를 사용하여 하위 집합의 위치를 변경합니다.

1. 하위 집합이 추가되면 해당 활동은 하위 집합만큼이 출력 전환을 표시합니다. 컴포지션 캔버스에서 각 하위 집합을 쉽게 식별할 수 있도록 레이블을 변경하는 것이 좋습니다.

   ![](../assets/split.png)

1. 각 하위 집합이 수신 모집단을 필터링하는 방법을 구성합니다. 이렇게 하려면 다음 단계를 수행합니다.

   1. 하위 집합을 확장하여 해당 속성을 표시합니다.

      ![](../assets/split-subset.png)

   1. 하위 집합에 필터링 조건을 적용하려면 **[!UICONTROL 필터 만들기]**&#x200B;를 클릭하고 쿼리 모델러를 사용하여 원하는 필터링 조건을 구성합니다. 예를 들어 데이터베이스에 이메일 주소가 있는 수신 모집단의 프로필을 포함합니다. [쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다](../../query/query-modeler-overview.md)

   1. 하위 집합에서 선택한 프로필 수를 제한하려면 **[!UICONTROL 제한 활성화]** 옵션을 토글하고 포함할 집단의 수 또는 백분율을 지정합니다.

   1. 들어오는 모집단이 비어 있는 경우 전환을 비활성화하려면 **[!UICONTROL 빈 전환 건너뛰기]** 옵션을 켜십시오. 하위 집합과 일치하는 프로필이 없으면 컴포지션이 다음 활동으로 전환되지 않습니다.

   >[!NOTE]
   >
   >하위 집합에 대해 집단 제한을 설정할 때 특정 프로필 속성을 기준으로 선택한 프로필의 등급을 오름차순 또는 내림차순으로 지정할 수 있습니다. 이렇게 하려면 정렬 활성화 옵션을 토글합니다. 이렇게 하려면 **[!UICONTROL 정렬 활성화]** 옵션을 토글합니다. 예를 들어 구매 금액이 가장 높은 상위 50개 프로필만 포함하도록 하위 집합을 제한할 수 있습니다.

1. 모든 하위 집합을 구성한 후에는 하위 집합과 일치하지 않는 나머지 집단을 선택하여 추가 아웃바운드 전환에 포함할 수 있습니다. 이렇게 하려면 **[!UICONTROL 여집합 생성]** 옵션을 토글합니다.

1. **[!UICONTROL 동일한 테이블에 모든 하위 집합 생성]** 옵션을 사용하면 모든 하위 집합을 단일 출력 전환으로 그룹화할 수 있습니다.

1. **[!UICONTROL 출력 모집단의 중복 사용]** 옵션을 사용하면 여러 하위 집합에 속하는 모집단을 관리할 수 있습니다.

   * 확인란을 선택하지 않으면 분할 활동은 수신자가 여러 하위 집합의 기준을 충족하더라도 여러 출력 전환에 표시되지 않습니다. 첫 번째 탭의 타겟에서 기준이 일치합니다.
   * 확인란을 선택하면 필터 조건을 충족하는 경우 여러 하위 집합에서 수신자를 찾을 수 있습니다. 모범 사례는 제외 기준을 사용하는 것입니다.

이제 활동이 구성되었습니다. 실행 시 모집단은 활동에 추가된 순서대로 다른 하위 집합으로 분할됩니다.

<!--
## Example{#split-example}

In the following example, the **[!UICONTROL Split]** activity is used to segment an audience into distinct subsets based on the communication channel that we want to use :

* **Subset 1 "push"**: This subset comprises all profiles who have installed our mobile application.
* **Subset 2 "sms"**: Mobile phone users: For the remaining population that did not fall into Subset 1, subset 2 applies a filtering rule to select profiles with mobile phones in the database.
* **Complement transition**: This transition captures all the remaining profiles that did not match Subset 1 or Subset 2. Specifically, it includes profiles who neither installed the mobile application nor have a mobile phone, such as users who haven't installed the mobile app or lack a registered mobile number.

![](../assets/workflow-split-example.png)
-->
