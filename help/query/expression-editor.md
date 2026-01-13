---
audience: end-user
title: 표현식 편집기 개요
description: 표현식 편집기 내의 함수를 사용하여 쿼리 모델러 내에서 쿼리를 작성하는 방법에 대해 알아봅니다.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '4108'
ht-degree: 9%

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

<!-- ### Aggregate

The aggregate functions are used to perform calculations on a set of values.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StdDev** | Returns the standard deviation of the values given. | StdDev(&lt;VALUE&gt;) | StdDev([0,3,5]) | -->

<!-- 

>[!TAB Databricks]

Aggregate functions are not available.

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") |

>[!TAB Redshift]

Aggregate functions are not available. -->

<!-- 

>[!TAB Snowflake]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") | -->

<!-- 
>[!TAB Vertica]

Aggregate functions are not available. -->

<!-- 
>[!ENDTABS] 
-->

### Date

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
| **TruncTime** | 날짜/시간을 2000년 1월 1일로 설정하고 지정된 숫자 값을 기준으로 나머지 날짜/시간을 가장 가까운 단위로 반올림합니다. 숫자 값이 60이면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. | TruncTime(&lt;날짜/시간>, &lt;숫자>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | 날짜/시간을 가장 가까운 분기의 첫 번째 날짜로 자릅니다. | TruncQuarter(&lt;날짜/시간>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | 날짜/시간을 가장 가까운 연도의 첫 번째 날짜로 자릅니다. | TruncYear(&lt;날짜/시간>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | 날짜/시간을 가장 가까운 주의 일요일로 자릅니다. | TruncWeek(&lt;날짜/시간>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- | **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | -->


<!-- 
>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncDateTZ** | Truncates the datetime to the nearest unit, based on the numerical value given, and sets the datetime to the specified timezone. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. | TruncDateTZ(&lt;DATETIME&gt;, &lt;NUMBER&gt;, &lt;TIMEZONE&gt;) | TruncDateTZ("2016-04-13 19:28:14", 3600, "America/Los_Angeles") |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |

>[!TAB Redshift]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **ConvertTimezone** | Converts the datetime from its timezone to the timezone of the external account. | ConvertTimezone(&lt;DATETIME&gt;) | ConvertTimezone("2019-12-25 15:30:00") |

 -->

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
| **TruncTime** | 날짜/시간을 2000년 1월 1일로 설정하고 지정된 숫자 값을 기준으로 나머지 날짜/시간을 가장 가까운 단위로 반올림합니다. 숫자 값이 60이면 가장 가까운 분으로 잘립니다. 숫자 값이 3600이면 가장 가까운 시간으로 잘립니다. | TruncTime(&lt;날짜/시간>, &lt;숫자>) | TruncTime(&quot;2016-04-13 19:28:14&quot;, 3600) |
| **TruncQuarter** | 날짜/시간을 가장 가까운 분기의 첫 번째 날짜로 자릅니다. | TruncQuarter(&lt;날짜/시간>) | TruncQuarter(&quot;2016-04-13 19:28:14&quot;) |
| **TruncYear** | 날짜/시간을 가장 가까운 연도의 첫 번째 날짜로 자릅니다. | TruncYear(&lt;날짜/시간>) | TruncYear(&quot;2016-04-13 19:28:14&quot;) |
| **TruncWeek** | 날짜/시간을 가장 가까운 주의 일요일로 자릅니다. | TruncWeek(&lt;날짜/시간>) | TruncWeek(&quot;2016-04-13 19:28:14&quot;) |
| **ConvertNTZ** | 시간대가 없는 타임스탬프를 시간대가 있는 타임스탬프로 변환합니다. 첨부된 시간대는 외부 계정의 시간대가 됩니다. | ConvertNTZ(&lt;날짜/시간>) | ConvertNTZ(&quot;2024-06-24 14:43:49&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- 
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | 
-->

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") |
-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Redshift]

Geomarketing functions are not available.

-->

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Distance** | 경도 및 위도로 정의된 두 지점 사이의 거리를 도 단위로 더블 반환합니다. | Distance(&lt;숫자>, &lt;숫자>, &lt;숫자>, &lt;숫자>) | 거리(40.345, 39.2345, -35.5834, 34.599) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

-->

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

<!-- 
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Floor** | Rounds down the provided number to the nearest integer. For example, if the provided number is 3.8, it will return 3. | Floor(&lt;NUMBER&gt;) | Floor(3.8) |
| **Greatest** | Returns the larger number between the two provided numbers. | Greatest(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Greatest(1, 2) |
| **Least** | Returns the smaller number between the two provided numbers. | Least(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Least (1,2) |
 -->

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Redshift]

Numeric functions are not available.

--->

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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

--->

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
| **GetEmailDomain** | 제공된 이메일 주소에서 도메인을 추출합니다. | GetEmailDomain(&lt;문자열>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | 조건이 true인 경우 첫 번째 옵션을 반환하고 조건이 false인 경우 두 번째 옵션을 반환합니다. | Iif(&lt;조건>, &lt;값>, &lt;값>) | Iif(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | 문자열이 비어 있으면 첫 번째 옵션을 반환합니다. 그렇지 않으면 두 번째 옵션을 반환합니다. | IsEmptyString( &lt;문자열> ,&lt;값>, &lt;값>) | IsEmptyString(&quot;문자열&quot;, &quot;예&quot;, &quot;아니요&quot;) |
| **NewUUID** | 새 고유 UUID를 생성합니다. | NewUUID() | NewUUID() |
| **NoNull** | 비어 있지 않으면 제공된 문자열을 반환하고, 제공된 문자열이 비어 있으면 빈 문자열을 반환합니다. | NoNull(&lt;문자열>) | NoNull(&quot;test&quot;) |
| **IsBitSet** | 제공된 숫자에 대해 비트 및 (&amp;)를 수행합니다. 이렇게 하면 첫 번째 매개 변수 내의 비트가 두 번째 매개 변수에서 제공된 위치에 설정되어 있는지 확인할 수 있습니다. | IsBitSet(&lt;숫자>, &lt;숫자>) | IsBitSet(5, 3) |
| **ClearBit** | 이렇게 하면 첫 번째 매개 변수 내의 비트를 두 번째 매개 변수에서 제공된 위치에서 지울 수 있습니다. | ClearBit(&lt;숫자>, &lt;숫자>) | |
| **SetBit** | 제공된 숫자에 대해 비트 또는 (\|)를 수행합니다. 이렇게 하면 첫 번째 매개변수 내의 비트가 두 번째 매개변수에서 제공된 위치에 설정되도록 설정할 수 있습니다. | SetBit(&lt;숫자>, &lt;숫자>) | SetBit(5, 3) |
| **RowId** | 행 번호를 반환합니다. | RowId() | RowId() |
| **ToBoolean** | 값을 부울로 변환합니다. | ToBoolean(&lt;값>) | ToBoolean(a=b) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBool(&lt;VALUE&gt;) | ToBool(a=b) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |

>[!TAB Redshift]

Other functions are not available.

--->

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **Case** | 표현식이 true인 경우 첫 번째 값을 반환합니다. 그렇지 않으면 두 번째 값을 반환합니다. | Case(When(&lt;표현식> &lt;값>), Else(&lt;값>)) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;)) |
| **When** | Case 함수의 일부로 사용됩니다. 대/소문자 내 표현식을 확인하는 데 사용됩니다. | When(&lt;표현식> &lt;값>) | When(a > b, &quot;yes&quot;) |
| **Else** | Case 함수의 일부로 사용됩니다. When 표현식이 false인 경우 다른 옵션을 선택하는 데 사용됩니다. | Else(&lt;값>) | Else(&quot;no&quot;) |
| **GetEmailDomain** | 제공된 이메일 주소에서 도메인을 추출합니다. | GetEmailDomain(&lt;문자열>) | GetEmailDomain(&quot;sample@example.com&quot;) |
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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **Coalesce** | Returns the first non-null value. | Coalesce(&lt;VALUE&gt;, &lt;VALUE&gt;) | Coalesce ("", "string") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBoolean(&lt;VALUE&gt;) | ToBoolean(a=b) |

-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **IsMemoNull** |  Returns 1 if the string is null, otherwise it returns 0. | IsMemoNull(&lt;STRING&gt;) | IsMemoNull("hello") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Redshift]

String functions are not available.

-->

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

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |

-->

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

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Redshift]

Window functions are not available.

--->

>[!TAB Snowflake]

| 이름 | 설명 | 구문 | 예 |
| ---- | ----------- | ------ | ------- |
| **RowNum** | 테이블 파티션 및 정렬 순서를 기준으로 행 시퀀스를 반환합니다. | RowNum(PartitionBy(&lt;표현식>), OrderBy(&lt;표현식>)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | 제공된 표현식에 따라 입력 행을 다른 파티션으로 구분합니다. | PartitionBy(&lt;표현식>) | PartitionBy(division) |
| **OrderBy** | 파티션 결과를 정렬합니다. | OrderBy(&lt;표현식>) | OrderBy(age) |
| **Desc** | OrderBy를 오름차순이 아닌 내림차순으로 정렬할 수 있습니다. | Desc(OrderBy(&lt;표현식>)) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

-->

>[!ENDTABS]
