---
audience: end-user
title: 컴포지션 만들기
description: 컴포지션 만들기 방법 알아보기
exl-id: 1f288312-dd6a-4a62-8ee6-fa2417954d5c
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 1%

---

# 구성 시작 및 모니터링 {#start-monitor}

컴포지션을 만들고 캔버스에서 수행할 작업을 디자인한 후에는 해당 컴포지션을 시작하고 실행 방법을 모니터링할 수 있습니다.

## 컴포지션 시작 {#start}

컴포지션을 시작하려면 화면 오른쪽 상단에 있는 **[!UICONTROL 시작]** 단추를 클릭하세요. 컴포지션이 실행 중일 때 캔버스의 각 활동은 컴포지션의 끝에 도달할 때까지 순차적 순서로 실행됩니다.

시각적인 흐름을 사용하여 실시간으로 타겟팅된 프로필의 진행 상황을 추적할 수 있습니다. 이렇게 하면 각 활동의 상태와 활동 간에 전환되는 프로필 수를 빠르게 식별할 수 있습니다.

![](assets/composition-visual-flow.png)

## 컴포지션 전환 {#transitions}

컴포지션에서는 전환을 통해 한 활동에서 다른 활동으로 전송된 데이터가 임시 작업 표에 저장됩니다. 각 전환에 대해 이 데이터를 표시할 수 있습니다. 이렇게 하려면 전환을 선택하여 화면 오른쪽에서 속성을 엽니다.

* 작업 테이블의 스키마를 표시하려면 **[!UICONTROL 스키마 미리 보기]**&#x200B;를 클릭하십시오.
* 선택한 전환에서 전송된 데이터를 시각화하려면 **[!UICONTROL 결과 미리 보기]**&#x200B;를 클릭하십시오. 이 옵션은 **[!UICONTROL 두 실행 사이에 중간 모집단 결과 유지]** 옵션이 활성화된 경우에만 사용할 수 있습니다. [자세히 알아보기](create-composition.md#settings).

![](assets/transition-preview.png)

## 활동 실행 모니터링 {#activities}

각 활동 상자의 오른쪽 위 모서리에 있는 시각적 표시기를 사용하여 실행을 확인할 수 있습니다.

| 시각적 표시기 | 설명 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 활동이 현재 실행 중입니다. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 이 활동에는 주의가 필요합니다. 여기에는 게재 전송을 확인하거나 필요한 조치를 취하는 작업이 포함될 수 있습니다. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 활동에 오류가 발생했습니다. 문제를 해결하려면 구성 로그에서 자세한 정보를 엽니다. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 활동이 정상적으로 실행되었습니다. |

## 로그 및 작업 모니터링 {#logs-tasks}

컴포지션 로그 및 작업 모니터링은 컴포지션을 분석하고 제대로 실행되고 있는지 확인하는 중요한 단계입니다. 작업 도구 모음 및 각 활동의 속성 창에서 사용할 수 있는 **[!UICONTROL 로그]** 단추에서 액세스할 수 있습니다.

![](assets/logs-button.png)

**[!UICONTROL 작성 로그 및 작업]** 화면에서 모든 사용자 작업을 기록하고 오류가 발생한 작성 실행 기록을 제공합니다.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

내역은 아래에 자세히 설명된 여러 탭으로 구성됩니다.

* **[!UICONTROL 로그]** 탭에는 모든 작성 작업의 실행 기록이 들어 있습니다. 시간 순서대로 수행된 작업과 실행 오류를 색인화합니다.
* **[!UICONTROL 작업]** 탭은 활동의 실행 시퀀싱에 대해 자세히 설명합니다. 각 작업의 끝에 있는 버튼을 사용하면 활동을 통해 전달된 이벤트 변수를 나열할 수 있습니다.
* **[!UICONTROL 변수]** 탭에는 컴포지션에서 전달된 모든 변수가 나열됩니다. 작성 캔버스에서 로그 및 작업에 액세스할 때만 사용할 수 있습니다. 이제 활동의 속성 창에서 로그에 액세스할 때 사용할 수 있습니다.  <!-- à confirmer-->

![](assets/logs-tasks.png)

모든 탭에서 표시된 열과 해당 순서를 선택하고 필터를 적용한 다음 검색 필드를 사용하여 원하는 정보를 빠르게 찾을 수 있습니다.

## 컴포지션 실행 명령 {#execution-commands}

오른쪽 위 모서리의 작업 표시줄은 작성 실행을 관리할 수 있는 명령을 제공합니다.

![](assets/execution-actions.png)

사용 가능한 작업은 다음과 같습니다.

* **[!UICONTROL 시작]**: 컴포지션 실행을 시작하고 **[!UICONTROL 진행 중]** 상태가 됩니다. 작성이 시작되고 초기 활동이 활성화됩니다.

* **[!UICONTROL 다시 시작]**: 일시 중지된 컴포지션 실행을 다시 시작합니다. 컴포지션이 **[!UICONTROL 진행 중]** 상태입니다.

* 컴포지션 실행을 **[!UICONTROL 일시 중지]**&#x200B;한 다음 **[!UICONTROL 일시 중지됨]** 상태로 전환합니다. 다시 시작될 때까지 새 활동이 활성화되지 않지만 진행 중인 작업은 중단되지 않습니다.

* 실행 중인 컴포지션을 **[!UICONTROL 중지]**&#x200B;하고 **[!UICONTROL 완료됨]** 상태로 전환합니다. 진행 중인 작업은 가능한 경우 중단됩니다. 중지된 동일한 위치에서 컴포지션을 다시 시작할 수 없습니다.

* **[!UICONTROL 다시 시작]**: 컴포지션을 중지했다가 다시 시작합니다. 대부분의 경우, 중지하는 데 일정 시간이 소요되고 중지하는 데 유효한 경우에만 **[!UICONTROL 시작]** 단추를 사용할 수 있으므로 더 빠르게 다시 시작할 수 있습니다.
