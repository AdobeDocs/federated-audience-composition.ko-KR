---
audience: end-user
title: 데이터 모델 시작
description: 데이터 모델로 시작하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: e43c1061d33298d028ee8d5d873b6b1112f13abe
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 22%

---

# 데이터 모델 시작 {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="모델 작업"
>abstract="이 화면에는 스키마 및 데이터 모델이 나열됩니다. **만들기** 버튼을 통해 스키마 및 데이터 모델을 만들 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="스키마 선택"
>abstract="데이터 모델의 스키마를 선택합니다."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="대상자 선택"
>abstract="데이터 모델의 대상자를 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="데이터 모델 속성"
>abstract="데이터 모델의 레이블을 입력합니다."


## 데이터 모델이란? {#data-model-start}

데이터 모델은 스키마, 대상 및 두 스키마 간의 링크 집합입니다. 데이터베이스 데이터로 대상자를 연합하는 데 사용됩니다.

[스키마](../customer/schemas.md#schema-start)에 대해 자세히 알아보세요.

[대상](../start/audiences.md)에 대해 자세히 알아보세요.

예를 들어 데이터 모델의 표현(이름 포함 테이블 및 테이블 간 링크)이 아래에 표시되어 있습니다.

![](assets/datamodel.png){zoomable="yes"}

Federated Audience Composition에서는 여러 데이터 모델을 만들 수 있습니다.

작성은 사용 사례를 기반으로 합니다. 필요한 표를 선택하고 필요에 따라 연결합니다.

## 데이터 모델 만들기 {#data-model-create}

데이터 모델을 만들려면 다음 단계를 수행합니다.

1. **[!UICONTROL FEDERATED DATA]** 섹션에서 **[!UICONTROL 모델]** 링크로 이동하여 **[!UICONTROL 데이터 모델]** 탭으로 이동합니다.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. **[!UICONTROL 데이터 모델 만들기]** 단추를 클릭하여 데이터 모델의 이름을 정의하고 **[!UICONTROL 만들기]** 단추를 클릭합니다.

   ![](assets/datamodel_name.png){zoomable="yes"}

1. 그런 다음 데이터 모델의 스키마, 대상자 및 링크를 추가합니다.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### 링크 만들기 {#data-model-links}

데이터 모델의 테이블 사이에 링크를 만들려면 다음 단계를 수행합니다.

1. 표 중 하나의 **[!UICONTROL 링크 만들기]** 메뉴를 클릭하거나 **[!UICONTROL 링크 만들기]** 단추를 클릭하고 두 개의 표를 선택합니다.

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. 링크를 정의하려면 주어진 양식을 입력합니다.

   ![](assets/datamodel_link.png){zoomable="yes"}

   데이터 모델에 대해 정의된 모든 링크가 다음과 같이 나열됩니다.

   ![](assets/datamodel_alllinks.png){zoomable="yes"}

## 비디오 방법 {#data-model-video}

이 비디오에서는 데이터 모델을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
