---
audience: end-user
title: 차원 변경 활동 사용
description: 차원 변경 활동을 사용하는 방법 알아보기
source-git-commit: 92d4a7cf1414ae74b2684619d295eca065a92ce2
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 41%

---

# 차원 변경 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="보조 항목 생성"
>abstract="중복으로 제외되었던 나머지 모집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **보조 항목 생성** 옵션을 토글합니다"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="차원 활동 변경"
>abstract="이 활동을 통해 대상자를 구축하면서 타겟팅 차원을 변경할 수 있습니다. 데이터 템플릿과 입력 차원에 따라 축이 이동됩니다. 예를 들어 “계약” 차원에서 “클라이언트” 차원으로 전환할 수 있습니다."

다음 **차원 변경** 활동을 사용하면 대상을 구축할 때 타겟팅 차원을 변경할 수 있습니다. 데이터 템플릿과 입력 차원에 따라 축을 이동합니다. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->


## 차원 변경 활동 구성 {#configure}

다음 단계에 따라 **차원 변경** 활동:

1. 추가 **차원 변경** 활동을 컴포지션에 추가합니다.

1. 다음을 정의합니다. **새 대상 차원**. 차원 변경 중에는 모든 레코드가 유지됩니다.

1. 컴포지션을 실행하여 결과를 확인합니다. 변경 차원 활동 전후의 테이블에 있는 데이터를 비교하고, 구성 테이블의 구조를 비교합니다.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->
