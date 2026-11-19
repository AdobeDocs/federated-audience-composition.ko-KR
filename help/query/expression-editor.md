---
audience: end-user
title: 표현식 편집기 개요
description: 표현식 편집기 내의 함수를 사용하여 쿼리 모델러 내에서 쿼리를 작성하는 방법에 대해 알아봅니다.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
TQID: https://experienceleague.adobe.com/CEu72QK6dqP1LCl8Ip1JSdZpZtubK0nyDJvj3QM75FU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
source-git-commit: 6dc582548645bffd85b612256b79aefd613f9185
workflow-type: tm+mt
source-wordcount: '4215'
ht-degree: 8%
---
# 표현식 편집기 개요 {#expression}

표현식을 편집하려면 수동으로 조건을 입력하여 규칙을 형성해야 합니다. 이 모드에서는 날짜, 문자열, 숫자 필드, 정렬 등과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있는 고급 함수를 사용할 수 있습니다.

## 표현식 편집기를 사용하여 작업 {#edit}

표현식 편집기는 쿼리 모델러 **[!UICONTROL 표현식 편집]** 단추에서 사용할 수 있습니다. 이 단추는 사용자 지정 조건을 구성할 때 **[!UICONTROL 특성]** 및 **[!UICONTROL 값]** 필드에 사용할 수 있습니다.

| **[!UICONTROL 속성]** 필드에서 액세스 | **[!UICONTROL 값]** 필드에서 액세스 |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

표현식 편집기에서 제공하는 사항:

* 식이 정의된 **입력 필드(1)**&#x200B;입니다.
* 표현식에서 사용할 수 있고 쿼리의 스키마(타겟팅 차원이라고도 함)에 해당하는 사용 가능한 **필드(2)** 목록입니다.
* 범주별로 정렬된 **도우미 함수(3)**&#x200B;입니다.

입력 필드에 직접 표현식을 입력하여 표현식을 편집합니다. 필드 또는 도우미 함수를 추가하려면 추가할 식에 커서를 놓고 + 단추를 선택합니다.

![](assets/expression-editor.png){zoomable="yes"}

식이 준비되면 **[!UICONTROL 확인]**&#x200B;을 선택합니다. 선택한 필드에 표현식이 표시됩니다. 편집하려면 표현식 편집기를 열고 원하는 대로 변경합니다.

아래 예제에서는 **[!UICONTROL 값]** 필드에 대해 구성된 식을 보여 줍니다. 편집하려면 **[!UICONTROL 표현식 편집]** 단추를 사용하여 표현식 편집기를 열어야 합니다.

![](assets/edit-expression-value.png){zoomable="yes"}

## 도우미 함수

쿼리 편집 도구를 사용하면 고급 함수를 사용하여 원하는 결과와 조작된 데이터 유형에 따라 복잡한 필터링을 수행할 수 있습니다. 다음 함수를 사용할 수 있습니다.

### 일자

날짜 함수는 날짜 또는 시간 값을 조작하는 데 사용됩니다.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **AddYears** | 지정된 날짜/시간에 지정된 연도 수를 추가합니다. | AddYears(&lt;날짜/시간>, &lt;숫자>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | 지정된 날짜/시간에 지정된 개월 수를 추가합니다. | AddMonths(&lt;날짜/시간>, &lt;숫자>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | 지정된 일수를 제공된 날짜/시간에 추가합니다. | AddDays(&lt;날짜/시간>, &lt;숫자>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | 지정된 시간(시)을 제공된 날짜/시간에 추가합니다. | AddHours(&lt;날짜/시간>, &lt;숫자>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | 지정된 날짜/시간에 지정된 시간(분)을 추가합니다. | AddMinutes(&lt;날짜/시간>, &lt;숫자>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | 지정된 날짜/시간에 지정된 시간(초)을 추가합니다. | AddSeconds(&lt;날짜/시간>, &lt;숫자>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | 지정된 날짜/시간에 지정된 연도 수를 뺍니다. | SubYears(&lt;날짜/시간>, &lt;숫자>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | 지정된 날짜/시간에 지정된 개월 수를 뺍니다. | SubMonths(&lt;날짜/시간>, &lt;숫자>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | 지정된 날짜/시간에 지정된 일 수를 뺍니다. | SubDays(&lt;날짜/시간>, &lt;숫자>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | 지정한 날짜/시간에 지정한 시간 수를 뺍니다. | SubHours(&lt;날짜/시간>, &lt;숫자>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | 지정한 날짜/시간에 지정한 시간(분)을 뺍니다. | SubMinutes(&lt;날짜/시간>, &lt;숫자>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | 지정된 날짜/시간에 지정된 시간(초)을 뺍니다. | SubSeconds(&lt;날짜/시간>, &lt;숫자>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | 지정된 datetime 개체에서 연도를 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Month** | 지정된 datetime 개체에서 월을 추출합니다. | Month(&lt;날짜/시간>) | Month(&quot;2019-12-15 15:30:0&quot;) |
| **Day** | 지정된 datetime 개체에서 일을 추출합니다. | Day(&lt;날짜/시간>) | Day(&quot;2019-12-15 15:30:0&quot;) |
| **DayOfYear** | 지정된 datetime 객체에서 연간 일자를 추출합니다. 예를 들어 입력한 날짜/시간이 2월 2일인 경우 33을 반환합니다. | DayOfYear(&lt;날짜/시간>) | DayOfYear(&quot;2019-12-15 15:30:0&quot;) |
| **WeekDay** | 지정된 datetime 개체에서 요일을 0에서 6 사이의 숫자로 추출하며 0은 일요일을 나타냅니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Hour** | 지정된 datetime 개체에서 시간 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Minute** | 지정된 datetime 개체에서 분 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Second** | 지정된 datetime 개체에서 두 번째 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **YearsDiff** | 연도 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | YearsDiff(&lt;날짜 시간>, &lt;날짜 시간>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | 지정된 날짜/시간 간의 차이를 월 단위로 검색합니다. | MonthsDiff(&lt;날짜/시간>, &lt;날짜/시간>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | 일 단위의 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | DaysDiff(&lt;날짜/시간>, &lt;날짜/시간>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | 시간 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | HoursDiff(&lt;날짜 시간>, &lt;날짜 시간>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | 분 단위로 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | MinutesDiff(&lt;날짜/시간>, &lt;날짜/시간>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | 초 단위로 세부기간을 사용하여 지정된 날짜 사이의 차이를 검색합니다. | SecondsDiff(&lt;날짜/시간>, &lt;날짜/시간>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **YearsOld** | 지정된 날짜/시간과 현재 날짜 사이의 차이점을 찾습니다(단위: 년). | YearsOld(&lt;날짜/시간>) | YearsOld(&quot;2019-12-25 15:30:00&quot;) |
| **MonthsOld** | 지정된 날짜/시간과 현재 날짜 사이의 차이점을 찾습니다(단위: 월). | MonthsOld(&lt;날짜/시간>) | MonthsOld(&quot;2019-12-25 15:30:0&quot;) |
| **DaysOld** | 지정된 날짜/시간과 현재 날짜 사이의 차이점을 찾습니다(일 단위). | DaysOld(&lt;날짜/시간>) | DaysOld(&quot;2019-12-25 15:30:0&quot;) |
| **GetDate** | 서버의 현재 날짜를 가져옵니다. | GetDate() | GetDate() |
| **DateOnly** | 날짜/시간을 연도, 월, 일로 자릅니다. | DateOnly(&lt;날짜/시간>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | 필드를 날짜 필드로 변환합니다. | ToDate(&lt;날짜/시간>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | 필드를 날짜/시간 필드로 변환합니다. | ToDateTime(&lt;날짜>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | 필드를 타임스탬프 필드로 변환합니다. | ToTimestamp(&lt;날짜/시간>) | ToTimestamp(&quot;2019-12-25 15:30:0&quot;) |
| **Oldest** | 제공된 두 날짜 중 가장 오래된 날짜를 반환합니다. | Oldest(&lt;날짜/시간>, &lt;날짜/시간>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | 지정된 숫자 값을 기준으로 날짜/시간을 가장 가까운 단위로 자릅니다. 숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. 숫자 값이 86400과 같으면 가장 가까운 날로 잘립니다. 그렇지 않으면 가장 가까운 두 번째 조각으로 잘립니다. | TruncDate(&lt;날짜/시간>, &lt;숫자>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | 지정된 숫자 값을 기준으로 날짜/시간을 가장 가까운 단위로 자르고 날짜/시간을 지정된 시간대로 설정합니다. 숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. 숫자 값이 86400과 같으면 가장 가까운 날로 잘립니다. | TruncDateTZ(&lt;날짜/시간>, &lt;숫자>, &lt;시간대>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | 날짜/시간을 2000년 1월 1일로 설정하고 지정된 숫자 값을 기준으로 나머지 날짜/시간을 가장 가까운 단위로 반올림합니다.숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. | TruncTime(&lt;날짜/시간>, &lt;숫자>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | 날짜/시간을 가장 가까운 분기의 첫 번째 날짜로 자릅니다. | TruncQuarter(&lt;날짜/시간>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | 날짜/시간을 가장 가까운 연도의 첫 번째 날짜로 자릅니다. | TruncYear(&lt;날짜/시간>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | 날짜/시간을 가장 가까운 주의 일요일로 자릅니다. | TruncWeek(&lt;날짜/시간>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **AddYears** | 지정된 날짜/시간에 지정된 연도 수를 추가합니다. | AddYears(&lt;날짜/시간>, &lt;숫자>) | AddYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMonths** | 지정된 날짜/시간에 지정된 개월 수를 추가합니다. | AddMonths(&lt;날짜/시간>, &lt;숫자>) | AddMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **AddDays** | 지정된 일수를 제공된 날짜/시간에 추가합니다. | AddDays(&lt;날짜/시간>, &lt;숫자>) | AddDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **AddHours** | 지정된 시간(시)을 제공된 날짜/시간에 추가합니다. | AddHours(&lt;날짜/시간>, &lt;숫자>) | AddHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **AddMinutes** | 지정된 날짜/시간에 지정된 시간(분)을 추가합니다. | AddMinutes(&lt;날짜/시간>, &lt;숫자>) | AddMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **AddSeconds** | 지정된 날짜/시간에 지정된 시간(초)을 추가합니다. | AddSeconds(&lt;날짜/시간>, &lt;숫자>) | AddSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **SubYears** | 지정된 날짜/시간에 지정된 연도 수를 뺍니다. | SubYears(&lt;날짜/시간>, &lt;숫자>) | SubYears(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMonths** | 지정된 날짜/시간에 지정된 개월 수를 뺍니다. | SubMonths(&lt;날짜/시간>, &lt;숫자>) | SubMonths(&quot;2019-12-25 15:30:00&quot;, 6) |
| **SubDays** | 지정된 날짜/시간에 지정된 일 수를 뺍니다. | SubDays(&lt;날짜/시간>, &lt;숫자>) | SubDays(&quot;2019-12-25 15:30:00&quot;, 10) |
| **SubHours** | 지정한 날짜/시간에 지정한 시간 수를 뺍니다. | SubHours(&lt;날짜/시간>, &lt;숫자>) | SubHours(&quot;2019-12-25 15:30:00&quot;, 3) |
| **SubMinutes** | 지정한 날짜/시간에 지정한 시간(분)을 뺍니다. | SubMinutes(&lt;날짜/시간>, &lt;숫자>) | SubMinutes(&quot;2019-12-25 15:30:00&quot;, 32) |
| **SubSeconds** | AdSubtract지정한 날짜/시간에 지정된 시간(초)을 더합니다. | SubSeconds(&lt;날짜/시간>, &lt;숫자>) | SubSeconds(&quot;2019-12-25 15:30:00&quot;, 37) |
| **Year** | 지정된 datetime 개체에서 연도를 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Month** | 지정된 datetime 개체에서 월을 추출합니다. | Month(&lt;날짜/시간>) | Month(&quot;2019-12-15 15:30:0&quot;) |
| **Day** | 지정된 datetime 개체에서 일을 추출합니다. | Day(&lt;날짜/시간>) | Day(&quot;2019-12-15 15:30:0&quot;) |
| **DayOfYear** | 지정된 datetime 객체에서 연간 일자를 추출합니다. 예를 들어 입력한 날짜/시간이 2월 2일인 경우 33을 반환합니다. | DayOfYear(&lt;날짜/시간>) | DayOfYear(&quot;2019-12-15 15:30:0&quot;) |
| **WeekDay** | 지정된 datetime 개체에서 요일을 1부터 7까지의 숫자로 추출하며 1은 일요일을 나타냅니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Hour** | 지정된 datetime 개체에서 시간 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Minute** | 지정된 datetime 개체에서 분 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **Second** | 지정된 datetime 개체에서 두 번째 값을 추출합니다. | Year(&lt;날짜/시간>) | Year(&quot;2019-12-15 15:30:0&quot;) |
| **YearsDiff** | 연도 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | YearsDiff(&lt;날짜 시간>, &lt;날짜 시간>) | YearsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsDiff** | 지정된 날짜/시간 간의 차이를 월 단위로 검색합니다. | MonthsDiff(&lt;날짜/시간>, &lt;날짜/시간>) | MonthsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **DaysDiff** | 일 단위의 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | DaysDiff(&lt;날짜/시간>, &lt;날짜/시간>) | DaysDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **HoursDiff** | 시간 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | HoursDiff(&lt;날짜 시간>, &lt;날짜 시간>) | HoursDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MinutesDiff** | 분 단위로 세부기간을 사용하여 지정된 날짜/시간 사이의 차이를 검색합니다. | MinutesDiff(&lt;날짜/시간>, &lt;날짜/시간>) | MinutesDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **SecondsDiff** | 초 단위로 세부기간을 사용하여 지정된 날짜 사이의 차이를 검색합니다. | SecondsDiff(&lt;날짜/시간>, &lt;날짜/시간>) | SecondsDiff(&quot;2019-12-25 15:30:00&quot;, &quot;2018-10-14 18:35:27&quot;) |
| **MonthsOld** | 지정된 날짜/시간과 현재 날짜 사이의 차이점을 찾습니다(단위: 월). | MonthsOld(&lt;날짜/시간>) | MonthsOld(&quot;2019-12-25 15:30:0&quot;) |
| **DaysOld** | 지정된 날짜/시간과 현재 날짜 사이의 차이점을 찾습니다(일 단위). | DaysOld(&lt;날짜/시간>) | DaysOld(&quot;2019-12-25 15:30:0&quot;) |
| **GetDate** | 서버의 현재 날짜를 가져옵니다. | GetDate() | GetDate() |
| **DateOnly** | 날짜/시간을 연도, 월, 일로 자릅니다. | DateOnly(&lt;날짜/시간>) | DateOnly(&quot;2019-12-25 15:30:00&quot;) |
| **ToDate** | 필드를 날짜 필드로 변환합니다. | ToDate(&lt;날짜/시간>) | ToDate(&quot;2019-12-25 15:30:00&quot;) |
| **ToDateTime** | 필드를 날짜/시간 필드로 변환합니다. | ToDateTime(&lt;날짜>) | ToDateTime(&quot;2019-12-25 15:30:00&quot;) |
| **ToTimestamp** | 필드를 타임스탬프 필드로 변환합니다. | ToTimestamp(&lt;날짜/시간>) | ToTimestamp(&quot;2019-12-25 15:30:0&quot;) |
| **Oldest** | 제공된 두 날짜 중 가장 오래된 날짜를 반환합니다. | Oldest(&lt;날짜/시간>, &lt;날짜/시간>) | Oldest(&quot;2015-02-13 11:59:59&quot;, &quot;2016-04-13 19:28:14&quot;) |
| **TruncDate** | 지정된 숫자 값을 기준으로 날짜/시간을 가장 가까운 단위로 자릅니다. 숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. 숫자 값이 86400과 같으면 가장 가까운 날로 잘립니다. 그렇지 않으면 가장 가까운 두 번째 조각으로 잘립니다. | TruncDate(&lt;날짜/시간>, &lt;숫자>) | TruncDate(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncDateTZ** | 지정된 숫자 값을 기준으로 날짜/시간을 가장 가까운 단위로 자르고 날짜/시간을 지정된 시간대로 설정합니다. 숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. 숫자 값이 86400과 같으면 가장 가까운 날로 잘립니다. | TruncDateTZ(&lt;날짜/시간>, &lt;숫자>, &lt;시간대>) | TruncDateTZ(&quot;2016-04-13 19:28:14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | 날짜/시간을 2000년 1월 1일로 설정하고 지정된 숫자 값을 기준으로 나머지 날짜/시간을 가장 가까운 단위로 반올림합니다.숫자 값이 60과 같으면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. | TruncTime(&lt;날짜/시간>, &lt;숫자>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | 날짜/시간을 가장 가까운 분기의 첫 번째 날짜로 자릅니다. | TruncQuarter(&lt;날짜/시간>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | 날짜/시간을 가장 가까운 연도의 첫 번째 날짜로 자릅니다. | TruncYear(&lt;날짜/시간>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | 날짜/시간을 가장 가까운 주의 일요일로 자릅니다. | TruncWeek(&lt;날짜/시간>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |
| **ConvertNTZ** | 시간대가 없는 타임스탬프를 시간대가 있는 타임스탬프로 변환합니다. 첨부된 시간대는 외부 계정의 시간대가 됩니다. | ConvertNTZ(&lt;날짜/시간>) | ConvertNTZ(&quot;2024-06-24 14:43:49&quot;) |

>[!ENDTABS]

>[!NOTE]
>
>**Dateonly** 함수는 연산자의 시간대가 아니라 서버의 시간대를 고려합니다.

### 지오마케팅

지오마케팅 함수는 지리적 값을 조작하는 데 사용됩니다.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Distance** | 경도 및 위도로 정의된 두 지점 사이의 거리를 도 단위로 더블 반환합니다. | Distance(&lt;숫자>, &lt;숫자>, &lt;숫자>, &lt;숫자>) | 거리(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Distance** | 경도 및 위도로 정의된 두 지점 사이의 거리를 도 단위로 더블 반환합니다. | Distance(&lt;숫자>, &lt;숫자>, &lt;숫자>, &lt;숫자>) | 거리(40.345, 39.2345, -35.5834, 34.599) |

>[!ENDTABS]

### 숫자

숫자 함수는 텍스트를 숫자로 변환하는 데 사용됩니다.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Mod** | 첫 번째 숫자를 두 번째 숫자로 나눈 나머지 숫자 반환 | Mod(&lt;숫자>, &lt;숫자>) | Mod (3, 2) |
| **Percent** | 첫 번째 숫자가 두 번째 숫자의 백분율을 계산합니다. | Percent(&lt;숫자>, &lt;숫자>) | 백분율(1, 2) |
| **Random** | 0(포함)과 1(제외) 사이의 난수를 반환합니다. | Random() | 무작위 () |
| **Round** | 제공된 숫자를 요청된 가장 가까운 소수 자릿수로 반환합니다. | Round(&lt;숫자>, &lt;숫자>) | Round(4.5394, 2) |
| **ToDouble** | 제공된 숫자를 double로 변환합니다. | ToDouble(&lt;숫자>) | ToDouble(5) |
| **ToInteger** | 제공된 숫자를 정수로 변환합니다. | ToInteger(&lt;숫자>) | ToInteger(45) |
| **ToInt64** | 제공된 숫자를 64비트 정수로 변환합니다. | ToInt64(&lt;숫자>) | ToInt64(493) |
| **Trunc** | 제공된 숫자를 요청한 소수점 이하 자리 수로 자릅니다. | Trunc(&lt;숫자>, &lt;숫자>) | Trunc(36.9348934, 3) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Mod** | 첫 번째 숫자를 두 번째 숫자로 나눈 나머지 숫자 반환 | Mod(&lt;숫자>, &lt;숫자>) | Mod (3, 2) |
| **Percent** | 첫 번째 숫자가 두 번째 숫자의 백분율을 계산합니다. | Percent(&lt;숫자>, &lt;숫자>) | 백분율(1, 2) |
| **Random** | 0(포함)과 1(제외) 사이의 난수를 반환합니다. | Random() | 무작위 () |
| **ToDouble** | 제공된 숫자를 double로 변환합니다. | ToDouble(&lt;숫자>) | ToDouble(5) |
| **ToInteger** | 제공된 숫자를 정수로 변환합니다. | ToInteger(&lt;숫자>) | ToInteger(45) |
| **ToInt64** | 제공된 숫자를 64비트 정수로 변환합니다. | ToInt64(&lt;숫자>) | ToInt64(493) |
| **Trunc** | 제공된 숫자를 요청한 소수점 이하 자리 수로 자릅니다. | Trunc(&lt;숫자>, &lt;숫자>) | Trunc(36.9348934, 3) |

>[!ENDTABS]

### 기타

이 테이블에는 사용 가능한 나머지 함수가 포함되어 있습니다.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Case** | 표현식이 true인 경우 첫 번째 값을 반환합니다. 그렇지 않으면 두 번째 값을 반환합니다. | Case(When(&lt;표현식> &lt;값>), Else(&lt;값>)) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;)) |
| **When** | Case 함수의 일부로 사용됩니다. 대/소문자 내 표현식을 확인하는 데 사용됩니다. | When(&lt;표현식> &lt;값>) | When(a > b, &quot;yes&quot;) |
| **Else** | Case 함수의 일부로 사용됩니다. When 표현식이 false인 경우 다른 옵션을 선택하는 데 사용됩니다. | Else(&lt;값>) | Else(&quot;no&quot;) |
| **Coalesce** | null이 아닌 첫 번째 값을 반환합니다. | Coalesce(&lt;값>, &lt;값>) | Coalesce (&quot;&quot;, &quot;string&quot;) |
| **Decode** | 값이 동일한 경우 첫 번째 옵션을 반환합니다. 값이 같지 않은 경우 두 번째 옵션을 반환합니다. | Decode(&lt;값>, &lt;값>, &lt;값>, &lt;값>) | Decode(1, 2, &quot;true&quot;, &quot;false&quot;) |
| **GetEmailDomain** | 제공된 이메일 주소에서 도메인을 추출합니다. | GetEmailDomain(&lt;문자열>) | GetEmailDomain(&quot;`sample@example.com`&quot;) |
| **Iif** | 조건이 true인 경우 첫 번째 옵션을 반환하고 조건이 false인 경우 두 번째 옵션을 반환합니다. | Iif(&lt;조건>, &lt;값>, &lt;값>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | 문자열이 비어 있으면 첫 번째 옵션을 반환합니다. 그렇지 않으면 두 번째 옵션을 반환합니다. | IsEmptyString( &lt;문자열> ,&lt;값>, &lt;값>) | IsEmptyString(&quot;문자열&quot;, &quot;예&quot;, &quot;아니요&quot;) |
| **NewUUID** | 새 고유 UUID를 생성합니다. | NewUUID() | NewUUID() |
| **NoNull** | 비어 있지 않으면 제공된 문자열을 반환하고, 제공된 문자열이 비어 있으면 빈 문자열을 반환합니다. | NoNull(&lt;문자열>) | NoNull(&quot;test&quot;) |
| **IsBitSet** | 제공된 숫자에 대해 비트 및 (&amp;)를 수행합니다. 이렇게 하면 첫 번째 매개 변수 내의 비트가 두 번째 매개 변수에서 제공된 위치에 설정되어 있는지 확인할 수 있습니다. | IsBitSet(&lt;숫자>, &lt;숫자>) | IsBitSet(5, 3) |
| **ClearBit** | 이렇게 하면 첫 번째 매개 변수 내의 비트를 두 번째 매개 변수에서 제공된 위치에서 지울 수 있습니다. | ClearBit(&lt;숫자>, &lt;숫자>) | |
| **SetBit** | 제공된 숫자에 대해 비트 또는 (\|)를 수행합니다. 이렇게 하면 첫 번째 매개변수 내의 비트가 두 번째 매개변수에서 제공된 위치에 설정되도록 설정할 수 있습니다. | SetBit(&lt;숫자>, &lt;숫자>) | SetBit(5, 3) |
| **RowId** | 행 번호를 반환합니다. | RowId() | RowId() |
| **ToBoolean** | 값을 부울로 변환합니다. | ToBoolean(&lt;값>) | ToBoolean(a=b) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Case** | 표현식이 true인 경우 첫 번째 값을 반환합니다. 그렇지 않으면 두 번째 값을 반환합니다. | Case(When(&lt;표현식> &lt;값>), Else(&lt;값>)) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;)) |
| **When** | Case 함수의 일부로 사용됩니다. 대/소문자 내 표현식을 확인하는 데 사용됩니다. | When(&lt;표현식> &lt;값>) | When(a > b, &quot;yes&quot;) |
| **Else** | Case 함수의 일부로 사용됩니다. When 표현식이 false인 경우 다른 옵션을 선택하는 데 사용됩니다. | Else(&lt;값>) | Else(&quot;no&quot;) |
| **GetEmailDomain** | 제공된 이메일 주소에서 도메인을 추출합니다. | GetEmailDomain(&lt;문자열>) | GetEmailDomain(&quot;`sample@example.com`&quot;) |
| **Iif** | 조건이 true인 경우 첫 번째 옵션을 반환하고 조건이 false인 경우 두 번째 옵션을 반환합니다. | Iif(&lt;조건>, &lt;값>, &lt;값>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | 문자열이 비어 있으면 첫 번째 옵션을 반환합니다. 그렇지 않으면 두 번째 옵션을 반환합니다. | IsEmptyString( &lt;문자열> ,&lt;값>, &lt;값>) | IsEmptyString(&quot;문자열&quot;, &quot;예&quot;, &quot;아니요&quot;) |
| **ToBoolean** | 값이 true이면 1을 반환합니다. 값이 false이면 0을 반환합니다. | ToBoolean(&lt;값>) | ToBoolean(a=b) |
| **ToBooleanType** | 값을 부울로 변환합니다. | ToBooleanType(&lt;값>) | ToBooleanType(a=b) |
| **IsBitSet** | 제공된 숫자에 대해 비트 및 (&amp;)를 수행합니다. 이렇게 하면 첫 번째 매개 변수 내의 비트가 두 번째 매개 변수에서 제공된 위치에 설정되어 있는지 확인할 수 있습니다. | IsBitSet(&lt;숫자>, &lt;숫자>) | IsBitSet(5, 3) |
| **ClearBit** | 이렇게 하면 첫 번째 매개 변수 내의 비트를 두 번째 매개 변수에서 제공된 위치에서 지울 수 있습니다. | ClearBit(&lt;숫자>, &lt;숫자>) | |
| **SetBit** | 제공된 숫자에 대해 비트 또는 (\|)를 수행합니다. 이렇게 하면 첫 번째 매개변수 내의 비트가 두 번째 매개변수에서 제공된 위치에 설정되도록 설정할 수 있습니다. | SetBit(&lt;숫자>, &lt;숫자>) | SetBit(5, 3) |
| **RowId** | 행 번호를 반환합니다. | RowId() | RowId() |
| **NewUUID** | 새 고유 UUID를 생성합니다. | NewUUID() | NewUUID() |
| **NoNull** | 비어 있지 않으면 제공된 문자열을 반환하고, 제공된 문자열이 비어 있으면 빈 문자열을 반환합니다. | NoNull(&lt;문자열>) | NoNull(&quot;test&quot;) |
| **AESEncrypt** | 제공된 문자열을 AES 암호화 유형으로 암호화합니다. | AESEncrypt() | AESEncrypt(&quot;hello&quot;) |
| **ObjectConstruct** | 제공된 키/값 쌍을 기반으로 개체를 만듭니다. | ObjectConstruct(&lt;문자열>, &lt;문자열>) | ObjectConstruct(&quot;key&quot;, &quot;value&quot;) |

>[!ENDTABS]

### 문자열

문자열 함수는 문자열 집합을 조작하는 데 사용됩니다.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | 2개의 문자열을 사용하여 모든 문자열이 null이 아니고 비어 있지 않은지 확인합니다. | AllNonNull2(&lt;문자열>, &lt;문자열>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | 3개의 문자열을 사용하여 모든 문자열이 null이 아니고 비어 있지 않은지 확인합니다. | AllNonNull3(&lt;문자열>, &lt;문자열>, &lt;문자열>) | AllNonNull3(&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Ascii** | 문자열을 가져오고 결과 를 반환합니다. | Ascii(&lt;문자열>) | Ascii(&quot;foo&quot;) |
| **Char** | 유니코드 코드 포인트 배열을 가져와 결과 문자열을 반환합니다. | Char(&lt;배열>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | 기본 문자열 내에서 지정된 하위 문자열의 첫 번째 발생 횟수를 찾습니다. | Charindex(&lt;문자열>, &lt;하위 문자열>) | Charindex(&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | 문자열에서 바이트 수를 반환합니다. | dataLength(&lt;문자열>) | dataLength(&quot;내 문자열&quot;) |
| **GetLine** | 제공된 문자열의 요청된 줄을 반환합니다. | GetLine(&lt;문자열>, &lt;숫자>) | GetLine(multilinestring, 5) |
| **IfEquals** | 4개의 문자열을 취하고 처음 두 문자열이 같으면 세 번째 문자열을 반환하고 처음 두 문자열이 같지 않으면 네 번째 문자열을 반환합니다. | IfEquals(&lt;문자열>, &lt;문자열>, &lt;문자열>, &lt;문자열>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | 문자열이 null이면 1을 반환하고, 그렇지 않으면 0을 반환합니다. | IsMemoNull(&lt;문자열>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | 2개의 문자열을 가져와 단일 문자열로 결합합니다. 필요한 경우 문자열 사이의 공백이 추가됩니다. | JuxtWords(&lt;문자열>, &lt;문자열>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | 세 개의 문자열을 취하여 하나의 문자열로 결합합니다. 필요한 경우 문자열 사이의 공백이 추가됩니다. | JuxtWords3(&lt;문자열>, &lt;문자열>, &lt;문자열>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | 문자열을 가져오고 지정된 대로 가장 왼쪽 문자를 반환합니다. | Left(&lt;문자열>, &lt;숫자>) | Left(&quot;하위 문자열&quot;, 3) |
| **Length** | 문자열의 길이를 반환합니다. | Length(&lt;문자열>) | Length(&quot;MyString&quot;) |
| **Md5Digest** | MD5 해시된 문자열을 16진수로 변환합니다. | Md5Digest(&lt;문자열>) | Md5Digest(&quot;문자열&quot;) |
| **MemoContains** | 문자열에 제공된 하위 문자열이 포함되어 있는지 확인합니다. | MemoContains(&lt;문자열>, &lt;문자열>) | MemoContains(&quot;string&quot;, &quot;str&quot;) |
| **Right** | 문자열을 가져오고 지정된 대로 가장 오른쪽 문자를 반환합니다. | Right(&lt;문자열>, &lt;숫자>) | 오른쪽(&quot;하위 문자열&quot;, 3) |
| **Smart** | 각 단어의 첫 번째 문자가 대문자로 표시된 문자열을 반환합니다. | Smart(&lt;문자열>) | Smart(&quot;hello world&quot;) |
| **Substring** | 문자열을 가져오고 제공된 위치를 기반으로 제공된 문자열의 일부를 반환합니다. | Substring(&lt;문자열>, &lt;왼쪽_숫자>, 오른쪽_숫자>) | Substring(&quot;하위 문자열&quot;, 3, 5) |
| **Sha256Digest** | SHA256 해시된 문자열을 16진수로 변환합니다. | Sha256Digest(&lt;문자열>) | Sha256Digest(&quot;문자열&quot;) |
| **Sha512Digest** | SHA512 해시된 문자열을 16진수로 변환합니다. | Sha512Digest(&lt;문자열>) | Sha512Digest(&quot;문자열&quot;) |
| **ToString** | 값을 문자열로 반환합니다. | ToString(&lt;값>) | ToString(123) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | 2개의 문자열을 사용하여 모든 문자열이 null이 아니고 비어 있지 않은지 확인합니다. | AllNonNull2(&lt;문자열>, &lt;문자열>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | 3개의 문자열을 사용하여 모든 문자열이 null이 아니고 비어 있지 않은지 확인합니다. | AllNonNull3(&lt;문자열>, &lt;문자열>, &lt;문자열>) | AllNonNull3(&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Char** | 유니코드 코드 포인트 배열을 가져와 결과 문자열을 반환합니다. | Char(&lt;배열>) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | 기본 문자열 내에서 지정된 하위 문자열의 첫 번째 발생 횟수를 찾습니다. | Charindex(&lt;문자열>, &lt;하위 문자열>) | Charindex(&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | 문자열에서 바이트 수를 반환합니다. | dataLength(&lt;문자열>) | dataLength(&quot;내 문자열&quot;) |
| **GetLine** | 제공된 문자열의 요청된 줄을 반환합니다. | GetLine(&lt;문자열>, &lt;숫자>) | GetLine(multilinestring, 5) |
| **IfEquals** | 4개의 문자열을 취하고 처음 두 문자열이 같으면 세 번째 문자열을 반환하고 처음 두 문자열이 같지 않으면 네 번째 문자열을 반환합니다. | IfEquals(&lt;문자열>, &lt;문자열>, &lt;문자열>, &lt;문자열>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | 문자열이 null이면 1을 반환하고, 그렇지 않으면 0을 반환합니다. | IsMemoNull(&lt;문자열>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | 2개의 문자열을 가져와 단일 문자열로 결합합니다. 필요한 경우 문자열 사이의 공백이 추가됩니다. | JuxtWords(&lt;문자열>, &lt;문자열>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | 세 개의 문자열을 취하여 하나의 문자열로 결합합니다. 필요한 경우 문자열 사이의 공백이 추가됩니다. | JuxtWords3(&lt;문자열>, &lt;문자열>, &lt;문자열>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | 문자열을 가져오고 지정된 대로 가장 왼쪽 문자를 반환합니다. | Left(&lt;문자열>, &lt;숫자>) | Left(&quot;하위 문자열&quot;, 3) |
| **Length** | 문자열의 길이를 반환합니다. | Length(&lt;문자열>) | Length(&quot;MyString&quot;) |
| **Line** | 문자열에서 지정된 숫자 줄을 반환합니다. | Line(&lt;문자열>, &lt;숫자>) | Line(multilinestring, 5) |
| **Md5Digest** | MD5 해시된 문자열을 16진수로 변환합니다. | Md5Digest(&lt;문자열>) | Md5Digest(&quot;문자열&quot;) |
| **Replace** | 문자열을 가져와 하위 문자열의 모든 인스턴스를 대체 하위 문자열로 바꿉니다. | Replace(&lt;문자열>, &lt;문자열&amp;gt, &lt;문자열&amp;gt) | Replace(&quot;Captain Steve&quot;, &quot;Captain&quot;, &quot;Engineer&quot;) |
| **Right** | 문자열을 가져오고 지정된 대로 가장 오른쪽 문자를 반환합니다. | Right(&lt;문자열>, &lt;숫자>) | 오른쪽(&quot;하위 문자열&quot;, 3) |
| **Sha256Digest** | SHA256 해시된 문자열을 16진수로 변환합니다. | Sha256Digest(&lt;문자열>) | Sha256Digest(&quot;문자열&quot;) |
| **Sha512Digest** | SHA512 해시된 문자열을 16진수로 변환합니다. | Sha512Digest(&lt;문자열>) | Sha512Digest(&quot;문자열&quot;) |
| **Smart** | 각 단어의 첫 번째 문자가 대문자로 표시된 문자열을 반환합니다. | Smart(&lt;문자열>) | Smart(&quot;hello world&quot;) |
| **ToString** | 값을 문자열로 반환합니다. | ToString(&lt;값>) | ToString(123) |

>[!ENDTABS]

### Window

>[!BEGINTABS]

>[!TAB Google BigQuery]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **RowNum** | 테이블 파티션 및 정렬 순서를 기준으로 행 시퀀스를 반환합니다. | RowNum(PartitionBy(&lt;표현식>), OrderBy(&lt;표현식>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | 제공된 표현식에 따라 입력 행을 다른 파티션으로 구분합니다. | PartitionBy(&lt;표현식>) | PartitionBy(division) |
| **OrderBy** | 파티션 결과를 정렬합니다. | OrderBy(&lt;표현식>) | OrderBy(age) |
| **Desc** | OrderBy를 오름차순이 아닌 내림차순으로 정렬할 수 있습니다. | Desc(OrderBy(&lt;표현식>)) | Desc(OrderBy(age)) |

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **RowNum** | 테이블 파티션 및 정렬 순서를 기준으로 행 시퀀스를 반환합니다. | RowNum(PartitionBy(&lt;표현식>), OrderBy(&lt;표현식>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | 제공된 표현식에 따라 입력 행을 다른 파티션으로 구분합니다. | PartitionBy(&lt;표현식>) | PartitionBy(division) |
| **OrderBy** | 파티션 결과를 정렬합니다. | OrderBy(&lt;표현식>) | OrderBy(age) |
| **Desc** | OrderBy를 오름차순이 아닌 내림차순으로 정렬할 수 있습니다. | Desc(OrderBy(&lt;표현식>)) | Desc(OrderBy(age)) |

>[!ENDTABS]
