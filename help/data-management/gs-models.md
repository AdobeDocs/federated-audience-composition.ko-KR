---
audience: end-user
title: 데이터 모델 시작
description: 데이터 모델로 시작하는 방법 알아보기
badge: label="Beta" type="Informative"
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 2%

---

# 데이터 모델 시작 {#data-model-beta}

>[!AVAILABILITY]
>
>캔버스 보기가 있는 데이터 모델은 현재 사용자를 선택하는 베타로 사용할 수 있습니다.

## 데이터 모델이란? {#data-model-start}

데이터 모델은 스키마, 대상 및 두 스키마 간의 링크 집합입니다. 데이터베이스 데이터로 대상자를 연합하는 데 사용됩니다.

Federated Audience Composition에서는 캔버스 보기에서 직접 데이터 모델을 만들고 관리할 수 있습니다. 여기에는 스키마 및 대상자 추가와 사용 사례를 기반으로 스키마 및 대상자 간 링크 정의가 포함됩니다.

[스키마](../customer/schemas.md#schema-start) 및 [대상](../start/audiences.md)에 대해 자세히 알아보세요.

예를 들어, 데이터 모델의 표현 아래에 이름과 테이블 간의 링크를 볼 수 있습니다.

![](assets/datamodel.png){zoomable="yes"}

## 데이터 모델 만들기 {#data-model-create}

데이터 모델을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL 페더레이션 데이터]** 섹션에서 **[!UICONTROL 모델]** 메뉴에 액세스하고 **[!UICONTROL 데이터 모델]** 탭으로 이동합니다.

   **[!UICONTROL 데이터 모델 만들기]** 단추를 클릭합니다.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. 데이터 모델의 이름을 정의하고 **[!UICONTROL 만들기]** 단추를 클릭합니다.

1. 데이터 모델 대시보드에서 **[!UICONTROL 스키마 추가]**&#x200B;를 클릭하여 데이터 모델과 연결된 스키마를 선택합니다.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. 대상 그룹을 정의하려면 **[!UICONTROL 대상 추가]**&#x200B;를 클릭하십시오.

1. 데이터 모델에서 테이블 간의 연결을 설정하여 정확한 데이터 관계를 보장합니다. [자세히 알아보기](#data-model-links)

1. 구성을 완료한 후 **[!UICONTROL 저장]**&#x200B;을 클릭하여 변경 내용을 적용합니다.

## 링크 만들기 {#data-model-links}

>[!BEGINTABS]

>[!TAB 테이블 보기]

표 보기 탭에서 데이터 모델의 표 사이에 연결을 만들려면 다음 단계를 수행합니다.

1. 표 중 하나의 **[!UICONTROL 링크 만들기]** 메뉴를 클릭하거나 **[!UICONTROL 링크 만들기]** 단추를 클릭하고 두 개의 표를 선택합니다.

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. 링크를 정의하려면 주어진 양식을 입력합니다.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **카디널리티**

   * **1-N**: 원본 테이블의 발생 항목 하나는 대상 테이블의 여러 발생 항목을 가질 수 있지만, 대상 테이블의 발생 항목 하나는 원본 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **N-1**: 대상 테이블의 발생 항목 하나는 원본 테이블의 여러 발생 항목을 가질 수 있지만, 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **1-1**: 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

데이터 모델에 대해 정의된 모든 링크가 다음과 같이 나열됩니다.

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB 캔버스 보기]

캔버스 보기 탭에서 데이터 모델의 테이블 사이에 링크를 만들려면 다음 단계를 수행합니다.

1. 데이터 모델의 캔버스 보기에 액세스하고 연결할 두 테이블을 선택합니다

1. Source 조인 옆에 있는 ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) 단추를 클릭한 다음 화살표를 드래그하여 Target 조인 방향으로 안내하여 연결을 설정합니다.

   ![](assets/datamodel.gif){zoomable="yes"}

1. 지정된 양식을 입력하여 링크를 정의하고 구성된 후 **[!UICONTROL 적용]**&#x200B;을 클릭합니다.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **카디널리티**

   * **1-N**: 원본 테이블의 발생 항목 하나는 대상 테이블의 여러 발생 항목을 가질 수 있지만, 대상 테이블의 발생 항목 하나는 원본 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **N-1**: 대상 테이블의 발생 항목 하나는 원본 테이블의 여러 발생 항목을 가질 수 있지만, 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

   * **1-1**: 원본 테이블의 발생 항목 하나는 대상 테이블의 해당 발생 항목을 최대 한 개까지 가질 수 있습니다.

1. 데이터 모델에 정의된 모든 링크는 캔버스 보기에서 화살표로 표시됩니다. 세부 정보를 보거나, 편집하거나, 필요에 따라 링크를 제거하려면 두 테이블 사이의 화살표를 클릭합니다.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

1. 도구 모음을 사용하여 캔버스를 사용자 정의하고 조정합니다.

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL 확대]**: 데이터 모델의 세부 정보를 더 명확하게 보려면 캔버스를 확대하십시오.
   * **[!UICONTROL 축소]**: 데이터 모델을 더 넓게 보려면 캔버스 크기를 줄이십시오.
   * **[!UICONTROL 보기 맞춤]**: 표시 영역 내의 모든 스키마 및/또는 대상에 맞게 확대/축소를 조정하십시오.
   * **[!UICONTROL 상호 작용 전환]**: 캔버스와의 사용자 상호 작용을 활성화하거나 비활성화합니다.
   * **[!UICONTROL 필터]**: 캔버스 내에 표시할 스키마를 선택합니다.
   * **[!UICONTROL 자동 레이아웃 강제 적용]**: 더 나은 조직을 위해 스키마 및/또는 대상을 자동으로 정렬합니다.

>[!ENDTABS]

## 비디오 방법 {#data-model-video}

이 비디오에서는 데이터 모델을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
