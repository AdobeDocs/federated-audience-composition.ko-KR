---
audience: end-user
title: 컴포지션 시작하기
description: 컴포지션을 시작하는 방법 알아보기
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 100%

---

# 컴포지션 시작하기 {#compositions}

>[!AVAILABILITY]
>
>컴포지션에 액세스하려면 다음 권한 중 하나가 필요합니다.
>
>-**페더레이션된 컴포지션 관리**
>>-**페더레이션된 컴포지션 보기**
>
>필요한 권한에 대한 자세한 내용은 [액세스 제어 안내서](/help/governance-privacy-security/access-control.md)를 참조하십시오.

페더레이션된 대상자 컴포지션을 사용하면 다양한 활동을 시각적 캔버스로 활용하여 대상자를 생성할 수 있는 컴포지션을 만들 수 있습니다. 컴포지션을 만든 후 결과 대상자는 Adobe Experience Platform에 저장되며, 이를 Experience Platform 대상 및 Adobe Journey Optimizer에서 활용하여 고객을 타기팅할 수 있습니다.

![페더레이션된 대상자 컴포지션에는 샘플 컴포지션 워크플로가 표시됩니다.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## 컴포지션 액세스 및 관리 {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="컴포지션"
>abstract="이 화면에서 컴포지션 전체 목록에 액세스하고 현재 상태, 마지막/다음 실행 일자를 확인하고 새 컴포지션을 만들 수 있습니다."

컴포지션은 Adobe Experience Platform **[!UICONTROL 대상자]** 메뉴의 **[!UICONTROL 페더레이션된 컴포지션]** **[!UICONTROL 고객]** 섹션에서 액세스할 수 있습니다.

이 화면에서 새 컴포지션을 만들고 기존 컴포지션에 액세스할 수 있습니다. 이름 옆에 있는 ![줄임표](/help/assets/icons/more.png) 버튼을 선택하여 기존 컴포지션을 복제하거나 삭제할 수도 있습니다.

또한 이름, 상태, 작성자, 마지막 수정 날짜 등 컴포지션에 대한 정보를 볼 수 있습니다.

| 상태 | 설명 |
| ------ | ----------- |
| **[!UICONTROL 초안]** | 컴포지션이 생성되었으며 저장되었습니다. |
| **[!UICONTROL 진행 중]** | 컴포지션이 실행되었으며 현재 실행 중입니다. |
| **[!UICONTROL 중지됨]** | 컴포지션 실행이 완료되어 중지되었습니다. |
| **[!UICONTROL 일시 정지됨]** | 컴포지션 실행이 일시 정지되었습니다. |
| **[!UICONTROL 오류]** | 컴포지션 실행 중에 오류가 발생했습니다. 오류에 대한 자세한 내용을 보려면 컴포지션을 열고 로그에 액세스하십시오. |

[시작 및 모니터 컴포지션 안내서](./start-monitor-composition.md)에서 구성을 시작하거나 중지하는 방법을 알아볼 수 있습니다.

![사용 가능한 컴포지션이 표시됩니다.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}

목록을 세분화하고 원하는 컴포지션을 찾으려면 목록을 검색하고 상태나 마지막 처리 날짜를 기준으로 컴포지션을 필터링할 수 있습니다.

열을 추가하거나 제거하여 목록을 사용자 정의할 수도 있습니다. 이렇게 하려면 **[!UICONTROL 열 구성]** 버튼을 선택하고 원하는 출력 열을 추가하거나 제거합니다.

![컴포지션 검색 페이지에 추가할 수 있는 사용 가능한 열 목록이 표시됩니다.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}

### 액세스 레이블 적용 {#access-labels}

특정 컴포지션에 액세스 레이블을 적용하려면 해당 컴포지션을 선택한 다음 **[!UICONTROL 액세스 관리]**&#x200B;를 선택하십시오.

![“액세스 관리” 버튼이 컴포지션 캔버스 내에서 강조 표시됩니다.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}

**[!UICONTROL 액세스 관리]** 팝오버가 나타납니다. 이 페이지에서 해당 액세스 및 데이터 거버넌스 레이블을 컴포지션에 적용할 수 있습니다.

![액세스 관리 팝오버가 표시됩니다. 여기에는 컴포지션에 적용할 수 있는 모든 레이블 목록이 표시됩니다.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}

| 레이블 유형 | 설명 |
| ---------- | ----------- |
| 약정 레이블 | 약정 레이블 (“C” 레이블)은 계약 의무가 있거나 조직의 데이터 거버넌스 정책과 관련된 데이터를 분류하는 데 사용됩니다. |
| ID 레이블 | ID 레이블(“I” 레이블)은 특정 개인을 식별하거나 특정 개인에게 연락할 수 있는 데이터를 분류하는 데 사용됩니다. |
| 민감 레이블 | 민감 레이블(“S” 레이블)은 사용자 및 조직에서 민감하다고 간주하는 데이터를 분류하는 데 사용됩니다. |
| 파트너 에코시스템 레이블 | 파트너 에코시스템 레이블은 조직 외부 소스의 데이터를 분류하는 데 사용됩니다. |

액세스 및 데이터 거버넌스 레이블에 대한 자세한 내용은 [데이터 사용 레이블 용어](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/labels/reference)를 참조하십시오.

## 다음 단계

지금까지 이 안내서를 통해 컴포지션에 대한 액세스, 관리 및 액세스 레이블 생성 방법을 알아보았습니다. 대상자 전체를 대상으로 작업하는 데 대한 자세한 내용은 [대상자 안내서](../start/audiences.md)를 참조하십시오.
