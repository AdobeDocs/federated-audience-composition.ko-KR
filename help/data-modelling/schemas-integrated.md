---
audience: end-user
title: 스키마 개요
description: Adobe Experience Platform UI 내에서 Federated Audience Composition에 대한 스키마를 만들고 사용하는 방법을 알아봅니다.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%
---
# 스키마 개요 {#schemas}

>[!AVAILABILITY]
>
>새 스키마 경험은 일부 고객만 사용할 수 있습니다. 자세한 내용은 Adobe 고객 지원 센터에 문의하십시오.
>
>새 스키마 환경에 대한 액세스 권한이 없는 경우 [스키마 개요](./schemas.md)를 읽어 보십시오.
>
>스키마에 액세스하려면 다음 권한 중 하나가 필요합니다.
>
>-**Federated 스키마 관리**
>-**연결된 스키마 보기**
>
>필요한 권한에 대한 자세한 내용은 [액세스 제어 안내서](/help/governance-privacy-security/access-control.md)를 참조하십시오.

스키마는 데이터베이스의 테이블을 나타냅니다. 데이터가 데이터베이스 테이블에 연결되는 방식을 정의하는 애플리케이션 내의 객체입니다.

스키마를 생성하여 Experience Platform Federated Audience Composition에서 표 표현을 정의할 수 있습니다.

* 사용자에게 이해하기 쉬운 이름과 설명을 제공하십시오
* 실제 용도에 따라 각 필드의 가시성을 결정합니다
* 필요한 경우 [데이터 모델](../data-modelling/models.md#data-model-start)에서 기본 키를 선택하여 스키마 간에 스키마를 연결합니다

>[!CAUTION]
>
>동일한 데이터베이스를 사용하여 여러 샌드박스를 연결할 때 고유한 작업 스키마를 사용해야 합니다.

## 스키마 만들기 {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="구성 관리"
>abstract="임시 빈 콘텐츠."

Federated Audience Composition에서 스키마를 만들려면 Experience Platform UI의 **[!UICONTROL 데이터 관리]** 섹션에서 **[!UICONTROL 스키마]**&#x200B;를 선택하십시오. 스키마 UI에서 **[!UICONTROL 스키마 만들기]**&#x200B;를 선택합니다.

![스키마 및 스키마 만들기 단추가 모두 스키마 UI에서 강조 표시됩니다.](/help/data-modelling/assets/integrated/select-create-schema.png)

스키마 만들기 팝오버가 나타나면 **[!UICONTROL 관계형]**, **[!UICONTROL 스키마 검색]** 및 **[!UICONTROL 다음]**&#x200B;을 선택하여 Federated Audience Composition에 대한 스키마를 만듭니다.

![관계형 스키마 만들기 팝오버에서 스키마 검색 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/select-discover-schemas.png)

**[!UICONTROL 페더레이션된 데이터베이스 선택]** 팝오버가 나타납니다. 이 팝오버에서는 [소스 데이터베이스](/help/connections/home.md)를 선택한 후 **[!UICONTROL 다음]**&#x200B;을 선택할 수 있습니다.

![페더레이션된 데이터베이스 선택 팝오버가 표시됩니다.](/help/data-modelling/assets/integrated/select-federated-database.png)

## 스키마 정의 {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="복합 키"
>abstract="여러 스키마 열로 구성된 스키마 키. 복합 키로 사용할 열을 표시합니다."

이제 통합 데이터베이스를 선택한 후 스키마를 정의할 수 있습니다. **[!UICONTROL 데이터 추가]** 화면이 나타납니다. 이 페이지에서 **[!UICONTROL 테이블 추가]**&#x200B;를 선택하여 스키마에 추가할 테이블을 선택할 수 있습니다.

![데이터 추가 화면에서 테이블 추가 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/select-add-table.png)

**[!UICONTROL 테이블 선택]** 팝오버가 나타납니다. 이 팝오버에서는 스키마를 만드는 데 사용할 테이블을 선택할 수 있습니다.

![테이블 선택 팝오버가 표시됩니다.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

선택한 각 테이블은 선택한 열을 사용하여 스키마를 생성합니다. 각 테이블에 대해 스키마 레이블을 변경하고, 설명을 추가하고, 필드 레이블 이름을 변경하고, 필드 레이블 가시성을 설정하고, 스키마 기본 키를 선택할 수 있습니다.

![선택한 테이블이 데이터 추가 페이지에 표시됩니다.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>**[!UICONTROL 합성 키]**&#x200B;를 선택했지만 사용할 키를 하나만 선택하면 키가 표준 스키마 기본 키로 처리됩니다.

또한 여러 스키마 열로 구성된 키를 만들 수도 있습니다. **[!UICONTROL 복합 키]**&#x200B;를 선택하고 사용할 키를 복합 키로 표시합니다.

![복합 키 전환과 스키마가 모두 선택되어 있습니다.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

구성을 완료한 후 **[!UICONTROL 완료]**&#x200B;를 선택하여 스키마 만들기를 완료합니다.

## 스키마 편집 {#schema-edit}

스키마를 편집하려면 **스키마** 페이지에서 이전에 만든 스키마 옆에 있는 ![줄임표 아이콘](/help/assets/icons/more.png)을 선택한 후 **[!UICONTROL 편집]**&#x200B;을 선택하십시오.

![스키마 편집 단추가 강조 표시되어 있습니다.](/help/data-modelling/assets/integrated/edit-schema.png)

**[!UICONTROL 스키마 편집]** 창에 스키마 편집기가 표시됩니다. 스키마 편집기 사용에 대한 자세한 내용은 [스키마 UI 안내서](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#customize-schema)를 참조하십시오.

![스키마 편집기가 표시됩니다.](/help/data-modelling/assets/integrated/schema-editor.png)

### 관계 편집 {#relationship-edit}

스키마의 관계를 편집하려면 스키마 편집기에서 **[!UICONTROL 엔터티 다이어그램 보기]**&#x200B;를 선택하십시오.

![엔터티 다이어그램 보기 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

엔티티 다이어그램 페이지가 나타납니다. 이 페이지에서 스키마 간의 관계를 설정하는 링크를 만들 수 있습니다.

![엔터티 다이어그램이 표시됩니다.](/help/data-modelling/assets/integrated/entity-diagram.png)

링크 만들기에 대한 자세한 내용은 [데이터 모델 개요](/help/data-modelling/models.md#data-model-links)의 캔버스 보기 탭을 참조하십시오.

## 스키마에서 데이터 미리 보기 {#schema-preview}

스키마가 나타내는 테이블의 데이터를 미리 보려면 **[!UICONTROL 데이터 세트]** 섹션으로 이동한 다음 **[!UICONTROL 찾아보기]**&#x200B;를 선택하십시오.

![데이터 세트 및 찾아보기 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/datasets-browse.png)

![세 점](/help/assets/icons/more.png)을 선택한 다음 **[!UICONTROL 데이터 집합 미리 보기]**&#x200B;를 선택하여 스키마 내의 데이터 미리 보기를 확인합니다.

![데이터 집합 미리 보기 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## 스키마 새로 고침 {#schema-refresh}

통합 데이터베이스의 테이블은 업데이트, 추가 또는 제거할 수 있습니다. 이러한 경우 최신 변경 사항에 맞게 Adobe Experience Platform에서 스키마를 새로 고쳐야 합니다. 스키마를 새로 고치려면 **[!UICONTROL 자세히]** 단추와 **[!UICONTROL 구성 관리]**&#x200B;를 차례로 선택합니다.

![구성 관리 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/manage-configuration.png)

**[!UICONTROL 구성 편집]** 팝오버가 나타납니다. 스키마를 새로 고치려면 **[!UICONTROL 새로 고침]**&#x200B;을 선택하십시오.

![스키마 새로 고침 단추가 강조 표시됩니다.](/help/data-modelling/assets/integrated/refresh-schema.png)

## 스키마 삭제 {#schema-delete}

스키마 편집기 내에서 스키마를 삭제하려면 **[!UICONTROL 자세히]**, **[!UICONTROL 삭제]**&#x200B;를 차례로 선택하십시오.

![스키마 삭제 단추가 강조 표시되어 있습니다.](/help/data-modelling/assets/integrated/delete-schema.png)
