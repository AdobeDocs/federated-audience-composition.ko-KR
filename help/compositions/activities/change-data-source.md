---
audience: end-user
title: 데이터 변경 Source 활동
description: 데이터 소스 변경 활동을 사용하여 작성에서 사용하는 데이터 소스를 변경함으로써 작성에서 데이터를 보다 유연하게 관리하는 방법에 대해 알아봅니다.
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# 데이터 소스 변경

>[!IMPORTANT]
>
>**[!UICONTROL 차원 변경]** 및 **[!UICONTROL 데이터 원본 변경]** 활동은 한 행에 추가되지 **않아야**&#x200B;합니다. 두 활동을 연속해서 사용해야 하는 경우 **[!UICONTROL 데이터 보강]** 활동을 두 활동 사이에 포함하십시오. 이렇게 하면 적절한 실행이 보장되며 잠재적인 충돌 또는 오류가 방지됩니다.

**[!UICONTROL 데이터 원본 변경]** 활동을 사용하면 컴포지션에서 사용하는 데이터 원본을 변경할 수 있습니다.

## 구성 {#configure}

**[!UICONTROL 데이터 원본 변경]** 활동을 캔버스에 추가한 후 워크플로우의 데이터 원본을 정의할 수 있습니다.

![데이터 원본 옵션이 Federated Audience Composition 작업 영역에서 강조 표시됩니다.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}{align="center"}

| 소스 | 설명 |
| ------ | ----------- |
| FDA 외부 계정 | Federated Audience Composition을 통해 Adobe Campaign에 연결된 외부 클라우드 데이터베이스. |

**[!UICONTROL FDA 외부 계정]**&#x200B;을(를) 선택한 후 연결할 외부 계정을 선택할 수 있습니다.

![외부 계정 옵션을 표시하는 팝오버가 표시됩니다.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}{align="center"}
