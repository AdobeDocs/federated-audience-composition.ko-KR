---
audience: end-user
title: 중복 제거 활동 사용
description: 중복 제거 활동을 사용하는 방법 알아보기
exl-id: 55db2461-fcfb-4284-9ab7-7cb01071ed1c
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 42%

---

# 중복 제거 {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="중복 요소 식별을 위한 필드"
>abstract="**[!UICONTROL 중복 요소 식별을 위한 필드]** 섹션에서 **[!UICONTROL 속성 추가]** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="중복 제거 활동"
>abstract="**중복 제거** 활동을 통해 인바운드 활동의 결과에서 중복 요소를 삭제할 수 있습니다. 주로 타기팅 활동 이후와 대상 데이터를 사용할 수 있는 활동 이전에 사용됩니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="여집합 생성"
>abstract="중복으로 제외된 나머지 집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **[!UICONTROL 여집합 생성]** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="중복 제거 설정"
>abstract="수신 데이터에서 중복 요소를 삭제하려면 아래 필드에서 중복 제거 방법을 정의합니다. 기본적으로 하나의 레코드만 유지됩니다. 또한 표현식 또는 속성을 기반으로 중복 제거 모드를 선택해야 합니다. 기본적으로 중복에서 제외할 레코드는 무작위로 선택됩니다."

**중복 제거** 활동을 사용하면 인바운드 활동의 결과에서 중복 항목(예: 받는 사람 목록의 중복된 프로필)을 삭제할 수 있습니다. **중복 제거** 활동은 일반적으로 타겟팅 활동 다음부터 타겟팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

## 중복 제거 활동 구성{#deduplication-configuration}

**중복 제거** 활동을 구성하려면 다음 단계를 따르십시오.

1. **중복 제거** 활동을 컴포지션에 추가합니다.

1. 활동에 여러 개의 인바운드 전환이 있는 경우 **[!UICONTROL 기본 집합]** 드롭다운 목록에서 중복 제거를 수행하는 데 사용할 전환을 선택하십시오

1. **[!UICONTROL 중복 요소 식별을 위한 필드]** 섹션에서 **[!UICONTROL 속성 추가]** 버튼을 클릭하여 이메일 주소, 이름, 성 등 동일한 값으로 중복 요소를 식별할 수 있는 필드를 지정합니다. 필드 순서에 따라 먼저 처리할 필드를 지정할 수 있습니다.

   ![](../assets/deduplication.png)

1. **[!UICONTROL 중복 제거 설정]** 섹션에서 고유한 **[!UICONTROL 유지할 중복 항목 수]**&#x200B;를 선택하십시오. 이 필드의 기본값은 **1**&#x200B;입니다. 값 **0**&#x200B;을(를) 사용하면 모든 중복을 유지할 수 있습니다.

   예를 들어 레코드 A와 B가 레코드 Y의 중복으로 간주되고 레코드 C가 레코드 Z의 중복으로 간주되는 경우:

   * 필드의 값이 **1**&#x200B;인 경우 Y 및 Z 레코드만 유지됩니다.
   * 필드의 값이 **0**&#x200B;인 경우 모든 레코드가 유지됩니다.
   * 필드의 값이 **2**&#x200B;인 경우 레코드 C와 Z는 유지되고 A, B 및 Y의 두 레코드는 우연히 또는 이후에 선택한 중복 제거 방법에 따라 유지됩니다.

1. 사용할 **[!UICONTROL 중복 제거 방법]**&#x200B;을(를) 선택하십시오.

   * **[!UICONTROL 무작위 선택]**: 중복 중에서 유지할 레코드를 임의로 선택합니다.
   * **[!UICONTROL 식 사용]**: 입력한 식의 값이 가장 작거나 가장 큰 레코드를 유지합니다.
   * **[!UICONTROL 비어 있지 않은 값]**: 식이 비어 있지 않은 레코드를 유지합니다.
   * **[!UICONTROL 값 목록을 팔로우합니다]**: 하나 이상의 필드에 대한 값 우선 순위를 정의합니다. 값을 정의하려면 **[!UICONTROL 특성]**&#x200B;을(를) 클릭하여 필드를 선택하거나 식을 만든 다음 해당 테이블에 값을 추가합니다. 새 필드를 정의하려면 값 목록 위에 있는 **[!UICONTROL 추가 단추]**&#x200B;를 클릭합니다.

1. 나머지 모집단을 활용하려면 **[!UICONTROL 보조 항목 생성]** 옵션을 선택하십시오. 보완은 모든 중복으로 구성됩니다. 그런 다음 추가 전환이 활동에 추가됩니다.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
