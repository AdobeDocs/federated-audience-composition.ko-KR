---
audience: end-user
title: 쿼리 모델러로 작업
description: 쿼리 모델러를 사용하여 작업하는 방법을 알아봅니다.
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 8%

---

# 쿼리 모델러로 작업 {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="쿼리 모델러"
>abstract="데이터베이스에서 수신자 또는 기타 스키마(타겟팅 차원이라고도 함)에 대한 필터링 기준을 정의합니다."

쿼리 모델러는 다양한 기준에 따라 데이터베이스를 필터링하는 프로세스를 단순화합니다. 또한 쿼리 모델러는 매우 복잡하고 긴 쿼리를 효율적으로 관리하여 향상된 유연성과 정밀도를 제공합니다. 또한 조건 내에 사전 정의된 필터를 지원하므로 포괄적인 대상 타기팅 및 세그멘테이션 전략에 고급 표현식 및 연산자를 활용하는 동시에 쿼리를 쉽게 세분화할 수 있습니다.

## 쿼리 모델러에 액세스

쿼리 모델러는 데이터를 필터링하기 위한 규칙을 정의해야 하는 모든 상황에서 사용할 수 있습니다.

| 사용 | 예 |
|  ---  |  ---  |
| **대상자 정의**: 컴포지션에서 타깃팅할 모집단을 지정하고 필요에 따라 맞춤화된 새 대상을 손쉽게 만들 수 있습니다. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **워크플로우 활동 사용자 지정**: 워크플로 활동 내에 규칙 적용(예: ) **분할** 및 **조정**&#x200B;을 입력하여 특정 요구 사항에 맞게 조정하십시오. [워크플로우 활동에 대해 자세히 알아보기](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **사전 정의된 필터**: 데이터 목록을 사용하거나 게재 대상을 구성하는 경우와 상관없이 다양한 필터링 작업 중에 바로 가기 역할을 하는 사전 정의된 필터를 만듭니다. | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **목록 사용자 지정**: 사용자 지정 규칙을 만들어 수신자, 게재 목록 등과 같은 목록에 표시되는 데이터를 필터링합니다. | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## 쿼리 모델러 인터페이스 {#interface}

쿼리 모델러는 쿼리를 작성하는 중앙 캔버스와 쿼리에 대한 정보를 제공하는 오른쪽 창을 제공합니다.

![](assets/query-interface.png){zoomable="yes"}

### 중앙 캔버스 {#canvas}

쿼리 모델러 중앙 캔버스는 쿼리를 작성하는 다른 구성 요소를 추가하고 결합하는 곳입니다. [쿼리를 작성하는 방법 알아보기](build-query.md)

캔버스의 오른쪽 위 모서리에 있는 도구 모음은 쿼리 구성 요소를 쉽게 조작하고 캔버스에서 탐색할 수 있는 옵션을 제공합니다.

* **다중 선택 모드**: 여러 필터링 구성 요소를 선택하여 선택한 위치에 복사하여 붙여넣습니다.
* **회전**: 캔버스를 세로로 전환합니다.
* **화면에 맞춤**: 캔버스 확대/축소 수준을 화면에 적용합니다.
* **축소** / **확대**: 캔버스를 축소하거나 축소합니다.
* **맵 표시**: 현재 위치를 보여주는 캔버스의 스냅샷을 엽니다.

### 규칙 속성 창 {#rule-properties}

오른쪽에는 **[!UICONTROL 규칙 속성]** 창은 쿼리에 대한 정보를 제공합니다. 다양한 작업을 수행하여 쿼리를 확인하고 요구 사항에 맞는지 확인할 수 있습니다. [쿼리 확인 및 유효성 검사 방법 알아보기](build-query.md#check-and-validate-your-query)
