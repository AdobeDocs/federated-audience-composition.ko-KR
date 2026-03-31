---
title: AI Assistant 개요
description: 제품 지식, 운영 인사이트, 페더레이션 대상 구성 만들기 등 AI Assistant를 사용하는 방법을 알아봅니다.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: d3a97b5887778f910ca8f09f7cb8fa99360a612c
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# AI 어시스턴트 개요 {#ai-assistant}

AI 어시스턴트는 Adobe 개념을 탐색하고 이해하는 데 도움이 되도록 설계된 사용자 인터페이스 기능입니다. AI Assistant를 사용하여 Federated Audience Composition을 비롯한 Adobe Experience Cloud의 여러 제품에서 제품 지식 사용 사례를 더 잘 이해할 수 있습니다.

>[!CAUTION]
>
>AI 어시스턴트를 사용하려면 먼저 Adobe Experience Cloud 생성형 AI 사용자 가이드라인에 동의해야 합니다. [AI Assistant(이전) 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/ai-assistant/home){target="_blank"}에서 계약에 대해 자세히 알아보세요.

페더레이션된 대상자 구성에서 프로세스의 다양한 부분과 관련된 Adobe 개념을 알아보기 위한 제품 지식에 액세스할 수 있습니다. AI Assistant는 다음 네 가지 사용 사례를 지원합니다. **검색 열기**(Experience League 설명서를 기반으로 제품 개념 살펴보기), **타깃팅된 학습 및 문제 해결**(특정 기능 관련 질문), **Operational Insights**(Federated Audience Composition 내 개체에 대한 질문) 및 **Federated Audience Composition 만들기**.

## 액세스 {#access}

AI Assistant에 액세스하려면 상단 막대에서 ![AI Assistant 아이콘](/help/start/assets/ai-assistant/icon.png)을 선택하십시오. AI 어시스턴트는 화면의 오른쪽 섹션에 표시됩니다. ![이미지 대체 텍스트 다운로드](assets/do-not-localize/Smock_FullScreen_18_N.svg "확장 아이콘")을 선택하여 AI Assistant 창을 확장할 수 있습니다.

![AI Assistant 아이콘이 강조 표시되어 AI Assistant에 액세스하는 방법을 보여 줍니다.](/help/start/assets/ai-assistant/access.png)

## AI Assistant 사용 {#using}

AI Assistant를 열면 화면 하단의 필드에 질문을 입력하고 Enter 키를 누릅니다. 이제 질문에 대한 답변이 표시됩니다. 엄지 손가락을 위로 또는 아래로 사용하여 답변을 평가할 수 있습니다.

![AI Assistant에 샘플 질문과 대답이 표시됩니다.](/help/start/assets/ai-assistant/sample-question-answer.png)

## 샘플 질문 {#sample-questions}

다음 쿼리는 AI Assistant에 물을 수 있는 사용 가능한 질문 유형을 보여 줍니다.

| 쿼리 유형 | 샘플 질문 |
| ---------- | --------------- |
| 검색 열기 | <ul><li>페더레이션된 대상자 구성이란 무엇입니까?</li></ul> |
| 타깃팅된 학습 | <ul><li>Snowflake Federated 데이터베이스 계정을 구성하려면 어떻게 해야 합니까?</li><li>페더레이션된 대상자 구성을 만드는 방법은 무엇입니까?</li></ul> |
| 운영 인사이트 | <ul><li>내 샌드박스에 몇 개의 페더레이션 데이터베이스가 있습니까?</li><li>지난 30일 동안 몇 개의 스키마를 만들었습니까?</li></ul> |
| 연합 대상 구성 만들기 | <ul><li>영국에 거주하는 고객의 연합 대상을 만듭니다.</li></ul> |

또한 AI Assistant를 사용하여 자율적으로 통합 대상 구성을 생성할 수 있습니다.

## 대상자 만들기 {#create-audience}

AI Assistant를 사용하여 자연어 프롬프트를 사용하여 통합 대상 구성을 생성할 수 있습니다. AI Assistant를 사용하여 대상자를 생성하면 AI Assistant는 프롬프트에 따라 계획을 수립하여 AI 기반 자동화를 사용하여 브라우저 내에서 실행합니다.

예를 들어, AI Assistant에 &quot;CUSTOMERS_Table 스키마를 사용하여 영국에 거주하는 고객의 연합 대상 만들기&quot;를 요청하는 경우 AI Assistant는 연합 구성 페이지로 이동하는 단계, 에이전트가 구성을 만드는 방법, 완료된 후 대상을 저장하는 등의 단계를 포함하여 대상 생성을 위해 수행할 계획을 설계합니다.

![샘플 질문과 응답이 표시됩니다.](/help/start/assets/ai-assistant/ask-create.png)

플랜이 정확해 보이는 경우 **[!UICONTROL 실행]**&#x200B;을 선택하여 에이전트가 자동화되도록 할 수 있습니다. 에이전트는 브라우저 내에서 요청된 컴포지션을 Federated Audience Composition UI 내에 만드는 단계를 자체적으로 수행합니다. 언제든지 자동화를 중지하려면 **[!UICONTROL 중지]**&#x200B;를 선택하세요.

![플랜이 실행되었으며 에이전트에서 플랜을 자체적으로 실행하고 있습니다.](/help/start/assets/ai-assistant/execute-plan.png)

현재 대상 만들기 기술은 다음과 같은 추가 기능을 지원합니다.

- 스케줄러
   - 되풀이하는 일정에 따라 실행되는 통합 구성을 만들 수 있습니다. 지원되는 값은 **한 번** 및 **일별**&#x200B;입니다.
- 중복 제거
   - 데이터 조정 중에 페더레이션 데이터 레코드를 중복 제거할 수 있습니다

## 다음 단계

AI Assistant를 통해 달성할 수 있는 목표 예제와 AI Assistant 작동 방식 등 AI Assistant에 대한 자세한 내용은 [AI Assistant 개요](https://experienceleague.adobe.com/ko/docs/experience-platform/ai-assistant/home){target="_blank"}를 참조하십시오.

Federated Audience 구성에 대해 요청할 수 있는 Operational Insight에 대한 전체 질문 목록은 [operational insights 섹션](https://experienceleague.adobe.com/ko/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}을 참조하십시오.
