---
audience: end-user
title: 차원 변경 활동 사용
description: 차원 변경 활동을 사용하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 42%

---

# 차원 변경 {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="여집합 생성"
>abstract="중복으로 제외했던 나머지 모집단으로 추가 아웃바운드 전환을 생성할 수 있습니다. 이렇게 하려면 **[!UICONTROL 여집합 생성]** 옵션을 토글합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="차원 활동 변경"
>abstract="이 활동을 통해 대상자를 빌드하면서 스키마(즉, 타기팅 차원)을 변경할 수 있습니다. 데이터 템플릿과 입력 스키마에 따라 축이 이동됩니다. 예를 들어 “계약” 스키마에서 “클라이언트” 스키마로 전환할 수 있습니다."

**차원 변경** 활동을 사용하면 대상을 구축할 때 스키마를 변경할 수 있습니다. 타겟팅 차원이라고도 합니다. 데이터 템플릿과 입력 스키마에 따라 축이 이동합니다.

## 차원 변경 활동 구성 {#configure}

**차원 변경** 활동을 구성하려면 다음 단계를 따르십시오.

1. 컴포지션에 **차원 변경** 활동을 추가합니다.

   ![](../assets/change-dimension.png)

1. **새 스키마**&#x200B;를 정의합니다. 스키마 변경 중에는 모든 레코드가 유지됩니다.

1. 컴포지션을 실행하여 결과를 확인합니다. **차원 변경** 활동 전후의 표에 있는 데이터를 비교하고, 컴퍼지션 표의 구조를 비교합니다.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

