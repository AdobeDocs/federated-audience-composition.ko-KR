---
audience: end-user
title: 데이터 모델 시작
description: 데이터 모델로 시작하는 방법 알아보기
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 61a7b66d16358a4a1c3d4b2ae153e856d8f682f7
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 15%

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

데이터 모델의 테이블 사이에 링크를 만들려면 다음 단계를 수행합니다.

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

## 비디오 방법 {#data-model-video}

이 비디오에서는 데이터 모델을 만드는 방법을 알아봅니다.

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
