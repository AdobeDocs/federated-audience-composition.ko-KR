---
audience: end-user
title: Adobe Journey Optimizer의 Federated Audience Composition 대상이 있는 다중 엔티티 타깃팅
description: Adobe Journey Optimizer 여정의 Federated Audience Composition 대상에서 프로필을 타겟팅하는 방법에 대해 알아봅니다.
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# Adobe Journey Optimizer의 Federated Audience Composition 대상이 있는 다중 엔티티 타깃팅

다중 엔티티 타깃팅을 사용할 경우, Adobe Journey Optimizer 여정에서 Federated Audience Composition 대상 속성을 보조 식별자로 사용할 수 있습니다. 이러한 속성을 사용하면 계정 또는 구독 수준과 같은 여러 엔티티에서 대상을 활성화할 수 있습니다.

## Federated Audience Composition에서 대상 만들기 {#create}

다중 엔티티 타겟팅으로 시작하려면 먼저 Federated Audience Composition에서 대상을 만들고 저장해야 합니다.

대상 구성 UI 내에서 **대상 빌드** 활동을 추가하여 연합 구성 캔버스 내에 대상을 만들고 **대상 저장** 활동을 추가하여 대상의 매핑, 기본 ID 및 데이터 만료를 구성합니다.

![대상을 표시하는 Federated Audience Composition UI가 표시됩니다.](/help/connections/assets/multi-entity-targeting/build-activity.png)

대상자의 구성을 완료했으면 **시작**&#x200B;을 선택하여 컴포지션 실행을 시작합니다. 이 대상과 해당 데이터 세트는 Experience Platform에서 사용할 수 있습니다.

Federated Audience Composition에서 컴포지션을 만드는 방법에 대한 자세한 내용은 [컴포지션 만들기 안내서](/help/compositions/create-composition.md)를 참조하십시오.

## Adobe Journey Optimizer에서 대상 활성화 {#activate}

컴포지션 실행이 완료되면 Journey Optimizer에서 대상자를 활성화할 수 있습니다. Adobe Journey Optimizer의 **여정 관리** 섹션 내에서 **여정**, **여정 만들기**&#x200B;를 차례로 선택하여 여정 사용자 인터페이스를 엽니다.

![Adobe Journey Optimizer에서 여정 만들기 단추가 강조 표시됩니다.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

여정 인터페이스 내에서 **대상자 읽기** 노드를 추가하십시오. 레이블을 제공하고 이전에 만든 대상자를 선택하여 이 노드를 구성할 수 있습니다.

![대상 읽기 노드가 Journey Optimizer UI에 표시됩니다.](/help/connections/assets/multi-entity-targeting/read-journey.png)

이전에 만든 대상자를 선택한 후 **보조 식별자 사용**&#x200B;을 사용하도록 설정하십시오.

![보조 식별자 사용 확인란이 강조 표시되어 있습니다.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

이제 보조 식별자를 선택할 수 있습니다. 선택기 화면에서 **고급 모드**&#x200B;를 선택하고 **Experience Platform**(으)로 이동합니다. 이 페이지에서 이전에 만든 대상자의 이름을 선택하고 대상자에 사용할 보조 식별자를 선택합니다.

![식 편집기가 표시됩니다.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## 여정 조건 구성 {#configure-journey}

대상자 설정을 활성화하고 구성했으므로 이제 여정의 나머지 조건을 계속 구성할 수 있습니다. 이 사용 사례의 경우 **대상자 읽기** 노드 뒤에 **최적화 도구** 노드를 추가한 다음 **작업** 노드를 추가합니다.

나머지 노드를 구성한 후 **게시**&#x200B;를 선택하여 여정 만들기를 완료합니다.

![게시 단추가 강조 표시됩니다.](/help/connections/assets/multi-entity-targeting/select-publish.png)

이제 여정은 기본 식별자가 아닌 **보조 식별자**&#x200B;를 기준으로 대상 프로필을 타깃팅합니다. 이제 이 기능을 사용하여 구독 ID, 계정 ID 또는 주문 ID와 같은 여러 엔티티를 타겟팅하고 원하는 채널에 활성화할 수 있습니다.

## 다음 단계 {#next-steps}

이제 이 안내서를 읽고 Journey Optimizer 여정에서 Federated Audience Composition 대상의 보조 식별자를 사용하는 방법을 이해할 수 있습니다. 보조 여정 사용에 대한 자세한 내용은 여정 가이드의 [보조 식별자 사용](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier)을 참조하십시오.

