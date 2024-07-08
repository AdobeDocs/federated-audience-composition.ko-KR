---
audience: end-user
title: 쿼리 모델러로 작업
description: 쿼리 모델러를 사용하는 방법을 알아봅니다.
source-git-commit: 5d4bdbbb9c903e839b21d22455d870396ac1df7d
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---

# 쿼리 모델러로 작업 {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="쿼리 모델러"
>abstract="데이터베이스에서 받는 사람 또는 다른 스키마(타겟팅 차원라고도 함)에 대한 필터링 기준을 정의합니다."

쿼리 모델러는 다양한 기준에 따라 데이터베이스를 필터링하는 프로세스를 단순화합니다. 또한 쿼리 모델러는 매우 복잡하고 긴 쿼리를 효율적으로 관리 할 수 있으므로 향상된 유연성과 정밀도를 제공합니다. 또한 조건 내에서 사전 정의된 필터를 지원하여 포괄적인 대상자 타겟팅 및 세분화 전략을 위해 고급 표현식 및 연산자를 활용하면서 쿼리를 쉽게 구체화할 수 있습니다.

## 쿼리 모델러 액세스

쿼리 모델러는 데이터를 필터링하기 위한 규칙을 정의해야 하는 모든 상황에서 사용할 수 있습니다.

| 사용 | 예 |
|  ---  |  ---  |
| **잠재고객** 정의: 작곡에서 타겟 대상으로 지정할 모집단을 지정하고 필요에 맞는 새로운 잠재고객을 손쉽게 만들 수 있습니다. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **작업 과정 활동** 사용자 지정: 분할&#x200B;**및**&#x200B;조정&#x200B;**과 같은**&#x200B;컴포지션 활동 내에서 규칙을 적용하여 특정 요구 사항에 맞춥니다. [작곡 활동에 대해 자세히 알아보기](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## 쿼리 모델러 인터페이스 {#interface}

쿼리 모델러는 쿼리를 빌드 할 수있는 중앙 캔버스와 쿼리에 대한 정보를 제공하는 오른쪽 창을 제공합니다.

![](assets/query-interface.png){zoomable="yes"}

### 중앙 캔버스 {#canvas}

쿼리 모델러 중앙 캔버스는 쿼리를 작성하는 다양한 구성 요소를 추가하고 결합하는 곳입니다. [쿼리를 빌드 하는 방법을 알아봅니다](build-query.md)

캔버스의 오른쪽 위 모서리에 있는 도구 모음은 쿼리 구성 요소를 쉽게 조작하고 캔버스에서 탐색할 수 있는 옵션을 제공합니다.

* **다중 선택 모드**: 여러 필터링 구성 요소를 선택하여 선택한 위치에 복사하여 붙여넣습니다.
* **회전**: 캔버스를 세로로 전환합니다.
* **화면** 크기에 맞게 조정: 캔버스 확대/축소 수준을 화면에 맞게 조정합니다.
* **** 축소 / **확대**: 캔버스를 축소하거나 축소합니다.
* **지도** 표시: 현재 위치를 보여주는 캔버스의 스냅샷을 엽니다.

### 규칙 속성 창 {#rule-properties}

오른쪽의 **[!UICONTROL 규칙 속성]** 창은 쿼리에 대한 정보를 제공합니다. 다양한 작업을 수행하여 쿼리를 확인하고 요구 사항에 맞는지 확인할 수 있습니다. [쿼리를 확인하고 유효성을 검사하는 방법 알아보기](build-query.md#check-and-validate-your-query)
