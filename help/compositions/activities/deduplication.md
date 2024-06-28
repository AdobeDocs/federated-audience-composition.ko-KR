---
audience: end-user
title: 중복 제거 활동 사용
description: 중복 제거 활동을 사용하는 방법 알아보기
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 60%

---

# 중복 제거 {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="중복 항목을 식별할 수 있는 필드"
>abstract="**중복 항목을 식별할 수 있는 필드** 섹션에서 **속성 추가** 버튼을 클릭하여 동일한 값을 통해 중복 항목을 식별할 수 있는 필드(이메일 주소, 이름, 성 등)를 지정할 수 있습니다. 필드 순서를 사용하면 먼저 처리할 항목을 지정할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="중복 제거 활동"
>abstract="**중복 제거** 활동을 통해 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다. 주로 타겟팅 활동 이후에 사용되며 타겟팅된 데이터의 사용을 허용하는 활동 이전에 사용됩니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="보조 항목 생성"
>abstract="중복으로 제외되었던 나머지 모집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **보조 항목 생성** 옵션을 토글합니다"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="중복 제거 설정"
>abstract="수신 데이터에서 중복 항목을 삭제하려면 아래 필드에서 중복 제거 방법을 정의하십시오. 기본적으로 하나의 레코드만 유지됩니다. 또한 표현식이나 속성을 기반으로 중복 제거 모드를 선택해야 합니다. 기본적으로 중복되지 않는 레코드는 무작위로 선택됩니다."

다음 **중복 제거** 활동을 사용하면 인바운드 활동의 결과에서 중복을 삭제할 수 있습니다(예: 수신자 목록에서 중복된 프로필). 다음 **중복 제거** 활동은 일반적으로 타겟팅 활동 다음부터 타겟팅된 데이터를 사용할 수 있는 활동 전에 사용됩니다.

## 중복 제거 활동 구성{#deduplication-configuration}

다음 단계에 따라 **중복 제거** 활동:

1. 추가 **중복 제거** 활동을 컴포지션에 추가합니다.

1. **중복 항목을 식별할 수 있는 필드** 섹션에서 **속성 추가** 버튼을 클릭하여 동일한 값을 통해 중복 항목을 식별할 수 있는 필드(이메일 주소, 이름, 성 등)를 지정할 수 있습니다. 필드 순서를 사용하면 먼저 처리할 항목을 지정할 수 있습니다.

1. 다음에서 **중복 제거 설정** 섹션에서 고유한 수를 선택합니다. **유지할 중복 항목**. 이 필드의 기본값은 1입니다. 값 0을 사용하면 모든 중복을 유지할 수 있습니다.

   예를 들어 레코드 A와 B가 레코드 Y의 중복으로 간주되고 레코드 C가 레코드 Z의 중복으로 간주되는 경우:

   * 필드의 값이 1인 경우 레코드 Y와 Z만 유지됩니다.
   * 필드의 값이 0인 경우 모든 레코드가 유지됩니다.
   * 필드의 값이 2인 경우 레코드 C와 Z는 유지되고 A, B 및 Y의 두 레코드는 우연히 또는 이후에 선택한 중복 제거 방법에 따라 유지됩니다.

1. 다음 항목 선택 **중복 제거 방법** 사용 방법:

   * **무작위 선택**: 중복 중에서 유지할 레코드를 임의로 선택합니다.
   * **표현식 사용**: 입력한 표현식의 값이 가장 작거나 가장 큰 레코드를 유지할 수 있습니다.
   * **값 목록 팔로우**: 하나 이상의 필드에 대한 값 우선 순위를 정의할 수 있습니다. 값을 정의하려면 **속성** 필드를 선택하거나 표현식을 만든 다음 해당 테이블에 값을 추가합니다. 새 필드를 정의하려면 값 목록 위에 있는 추가 버튼을 클릭합니다.

1. 다음 확인: **보조 항목 생성** 나머지 모집단을 활용하려면 옵션을 선택합니다. 보완은 모든 중복으로 구성됩니다. 그런 다음 추가 전환이 활동에 추가됩니다.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
