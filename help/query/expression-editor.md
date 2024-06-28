---
audience: end-user
title: 쿼리 모델러를 사용하여 첫 번째 쿼리 작성
description: 쿼리 모델러에서 첫 번째 쿼리를 작성하는 방법을 알아봅니다.
source-git-commit: 96b578cab1ce328b7db5043539e3b58fa238ebfd
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 53%

---

# 표현식 편집 {#expression}

표현식을 편집하려면 수동으로 조건을 입력하여 규칙을 만듭니다. 이 모드에서는 날짜, 문자열, 숫자 필드, 정렬 등과 같은 특정 쿼리를 수행하는 데 사용되는 값을 조작할 수 있는 고급 함수를 사용할 수 있습니다.

>[!IMPORTANT]
>
>아래 섹션에서는 표현식 편집기를 사용하여 규칙을 작성하는 방법에 대한 정보를 제공합니다. 규칙을 만드는 데 사용되는 구문은 개인화를 추가하는 데 사용되는 구문과 다릅니다.

## 표현식 편집기 작업 {#edit}

표현식 편집기는 쿼리 모델러에서 사용할 수 있습니다 **[!UICONTROL 표현식 편집]** 버튼, 다음에 사용 가능 **[!UICONTROL 속성]** 및 **[!UICONTROL 값]** 사용자 지정 조건을 구성할 때 필드.

| 다음에서 액세스: **속성** 필드 | 다음에서 액세스: **값** 필드 |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

표현식 편집기에서 제공하는 사항:

* An **입력 필드 (1)** 표현식이 정의된 위치입니다.
* 사용 가능한 목록 **필드 (2)** 표현식에서 사용할 수 있으며 쿼리의 타겟팅 차원에 해당합니다.
* **도우미 기능 (3)**, 범주별로 정렬되었습니다.

입력 필드에 직접 표현식을 입력하여 표현식을 편집합니다. 필드나 도우미 함수를 추가하려면 추가할 식에 커서를 놓고 + 단추를 클릭합니다.

![](assets/expression-editor.png){zoomable="yes"}

표현식이 준비되면 **[!UICONTROL 확인]** 단추를 클릭합니다. 선택한 필드에 표현식이 표시됩니다. 편집하려면 표현식 편집기를 열고 원하는 대로 변경합니다.

아래 예제는 다음에 대해 구성된 표현식을 보여줍니다. **[!UICONTROL 값]** 필드. 편집하려면 다음을 사용하여 표현식 편집기를 열어야 합니다. **[!UICONTROL 표현식 편집]** 단추를 클릭합니다.

![](assets/edit-expression-value.png){zoomable="yes"}

## 도우미 함수

쿼리 편집 도구를 사용하면 고급 함수를 사용하여 원하는 결과와 조작된 데이터 유형에 따라 복잡한 필터링을 수행할 수 있습니다. 다음 기능을 사용할 수 있습니다.

### 집계

집계 함수는 값 집합에 대한 계산을 수행하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>평균</strong><br /> </td> 
   <td> 숫자 유형 열의 평균 반환<br /> </td> 
   <td> Avg(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>카운트</strong><br /> </td> 
   <td> 열의 null이 아닌 값 계산<br /> </td> 
   <td> Count(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong><br /> </td> 
   <td> 반환된 값 계산(모든 필드)<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Countdistinct</strong><br /> </td> 
   <td> 열의 null이 아닌 개별 값 계산<br /> </td> 
   <td> Countdistinct(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>최대</strong><br /> </td> 
   <td> 숫자, 문자열 또는 날짜 유형 열의 최대값 반환<br /> </td> 
   <td> Max(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>분</strong><br /> </td> 
   <td> 숫자, 문자열 또는 날짜 유형 열의 최소값 반환<br /> </td> 
   <td> Min(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>표준 개발</strong><br /> </td> 
   <td> 숫자, 문자열 또는 날짜 열의 표준 편차 반환<br /> </td> 
   <td> StdDev(&lt;value&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>문자열 집계</strong><br /> </td> 
   <td> 두 번째 인수의 문자로 구분된 문자열 형식 열의 값 연결을 반환합니다.<br /> </td> 
   <td> StringAg(&lt;value&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>합계</strong><br /> </td> 
   <td> 숫자, 문자열 또는 날짜 유형 열 값의 합계 반환<br /> </td> 
   <td> Sum(&lt;value&gt;)<br /></td> 
  </tr> 
 </tbody> 
</table>

### 날짜

날짜 함수는 날짜 또는 시간 값을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> 날짜에 일자 숫자 추가<br /> </td> 
   <td> AddDays(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> 날짜에 시간(시) 숫자 추가<br /> </td> 
   <td> AddHours(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> 날짜에 시간(분) 숫자 추가<br /> </td> 
   <td> AddMinutes(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> 날짜에 개월 숫자 추가<br /> </td> 
   <td> AddMonths(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> 날짜에 시간(초) 숫자 추가<br /> </td> 
   <td> AddSeconds(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> 날짜에 연도 숫자 추가<br /> </td> 
   <td> AddYears(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>변환 NTZ</strong><br /> </td> 
   <td> 타임스탬프 NTZ(timestamp without timezone)를 정의된 세션 TZ가 적용된 TZ(timestamp with timezone)로 변환<br/> </td> 
   <td> ConvertNTZ(&lt;date time=""&gt;)<br /> </td>  
  </tr>
  <tr> 
   <!--<td> <strong>ConvertTimezone</strong><br /> </td> 
   <td> <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>-->
  <tr> 
   <td> <strong>DateCmp</strong><br /> </td> 
   <td> 두 날짜 비교<br/> </td> 
   <td> DateCmp(&lt;date&gt;,&lt;date&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> 날짜만 반환(00:00 시간 포함)*<br /> </td> 
   <td> DateOnly(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> 날짜의 일자를 나타내는 숫자 반환<br /> </td> 
   <td> Day(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> 날짜의 연도를 반환합니다.<br /> </td> 
   <td> DayOfYear(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> 현재 날짜에서 n일을 뺀 날짜 반환<br /> </td> 
   <td> DaysAgo(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> 현재 날짜에서 n일을 뺀 날짜(정수 yymmdd) 반환<br /> </td> 
   <td> DaysAgoInt(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 일자 수<br /> </td> 
   <td> DaysDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> 날짜를 일 단위로 반환<br /> </td> 
   <td> DaysOld(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> 서버의 현재 시스템 날짜 반환<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> 날짜의 시간 반환<br /> </td> 
   <td> Hour(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(시) 숫자 반환<br /> </td> 
   <td> HoursDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> 날짜의 시간(분) 반환<br /> </td> 
   <td> Minute(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(분) 숫자 반환<br /> </td> 
   <td> MinutesDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> 날짜의 월을 나타내는 숫자 반환<br /> </td> 
   <td> Month(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> 현재 날짜에서 n개월을 뺀 날짜 반환<br /> </td> 
   <td> MonthsAgo(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 개월 숫자 반환<br /> </td> 
   <td> MonthsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> 날짜를 월 단위로 반환<br /> </td> 
   <td> MonthsOld(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> 범위에서 가장 오래된 날짜 반환<br /> </td> 
   <td> 가장 오래된 항목 (&lt;date date=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> 날짜의 시간(초) 반환<br /> </td> 
   <td> Second(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 시간(초) 숫자 반환<br /> </td> 
   <td> SecondsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> 날짜에서 일자 숫자 빼기<br /> </td> 
   <td> SubDays(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> 날짜에서 시간(시) 숫자 빼기<br /> </td> 
   <td> SubHours(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> 날짜에서 시간(분) 숫자 빼기<br /> </td> 
   <td> SubMinutes(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> 날짜에서 개월 숫자 빼기<br /> </td> 
   <td> SubMonths(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> 날짜에서 시간(초) 숫자 빼기<br /> </td> 
   <td> SubSeconds(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> 날짜에서 연도 숫자 빼기<br /> </td> 
   <td> SubYears(&lt;날짜&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> 날짜 + 시간을 날짜로 변환<br /> </td> 
   <td> ToDate(&lt;날짜 + 시간&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> 문자열을 날짜 + 시간으로 변환<br /> </td> 
   <td> ToDateTime(&lt;문자열&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>타임스탬프 지정</strong><br /> </td> 
   <td> 문자열을 타임스탬프로 변환<br /> </td> 
   <td> To타임스탬프(&lt;string&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>시간대 지정</strong><br /> </td> 
   <td> 날짜 + 시간을 표준 시간대로 변환<br /> </td> 
   <td> ToTimezone(&lt;date&gt;,&lt;time zone=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> 날짜+시간을 가장 가까운 시간(초)으로 반올림<br /> </td> 
   <td> TruncDate(@lastModified, &lt;시간(초) 숫자&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> 날짜 + 시간을 초 단위의 특정 정밀도로 반올림<br /> </td> 
   <td> TruncDateTZ(&lt;날짜&gt;, &lt;시간(초) 숫자&gt;, &lt;시간대&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> 날짜를 분기로 반올림<br /> </td> 
   <td> TruncQuarter(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> 시간 부분을 가장 가까운 시간(초)으로 반올림<br /> </td> 
   <td> TruncTime(e)&lt;date&gt;, &lt;number of="" seconds=""&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> 날짜를 요일로 반올림<br /> </td> 
   <td> TruncWeek(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> 날짜 + 시간을 연도의 1월 1일로 반올림<br /> </td> 
   <td> TruncYear(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> 날짜의 요일을 나타내는 숫자 반환(0=Monday, 6=Sunday)<br /> </td> 
   <td> WeekDay(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> 날짜의 연도를 나타내는 숫자 반환<br /> </td> 
   <td> Year(&lt;날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearAnd Month</strong><br /> </td> 
   <td> 날짜의 연도 및 월을 나타내는 숫자 반환<br /> </td> 
   <td> YearAndMonth(&lt;날짜&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong>YearsAgo</strong><br /> </td> 
   <td> 지정된 날짜와 현재 날짜 사이의 연도 수를 반환합니다.<br /> </td> 
   <td> YearsAgo(&lt;date&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> 두 날짜 사이의 연도 숫자 반환<br /> </td> 
   <td> YearsDiff(&lt;종료 날짜&gt;, &lt;시작 날짜&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> 날짜를 연 단위로 반환<br /> </td> 
   <td> YearsOld(&lt;날짜&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>다음 사항에 주의하십시오. **Dateonly** 함수는 연산자의 시간대가 아니라 서버의 시간대를 고려합니다.

### 지오마케팅

지오마케팅 함수는 지리적 값을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> 경도 및 위도로 정의된 두 지점 사이의 거리를 도 단위로 반환합니다.<br /> </td> 
   <td> Distance(&lt;경도 A&gt;, &lt;위도 A&gt;, &lt;경도 B&gt;, &lt;위도 B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 숫자

숫자 함수는 텍스트를 숫자로 변환하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> 숫자의 절대값 반환<br /> </td> 
   <td> Abs(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 최소 정수 반환<br /> </td> 
   <td> Ceil(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> 숫자보다 크거나 같은 최대 정수 반환<br /> </td> 
   <td> Floor(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> 두 숫자 중 큰 숫자 반환<br /> </td> 
   <td> Greatest(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> 두 숫자 중 작은 숫자 반환<br /> </td> 
   <td> Least(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> n1에서 n2까지 정수 분기의 나머지 반환<br /> </td> 
   <td> Mod(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> 백분율로 표현된 두 수의 비율 반환<br /> </td> 
   <td> Percent(&lt;숫자 1&gt;, &lt;숫자 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> 임의 값 반환<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> 숫자를 n개의 소수로 반올림<br /> </td> 
   <td> Round(&lt;숫자&gt;, &lt;소수 자리수&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> 숫자 기호 반환<br /> </td> 
   <td> Sign(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 정수를 실수로 변환<br /> </td> 
   <td> ToDouble(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 실수를 64비트 정수로 변환<br /> </td> 
   <td> ToInt64(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 실수를 정수로 변환<br /> </td> 
   <td> ToInteger(&lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> n1에서 n2까지의 소수점 자르기<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 기타

이 표에는 사용 가능한 나머지 함수가 포함되어 있습니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> 인수에 제공된 암호화 문자열<br /> </td> 
   <td> AESEncrypt(&lt;value&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> 조건이 true이면 값 1 반환 그렇지 않으면 값 2를 반환합니다.<br /> </td> 
   <td> Case(When(&lt;조건&gt;, &lt;값 1&gt;), Else(&lt;값 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 값에서 플래그 삭제<br /> </td> 
   <td> ClearBit(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> 값 1이 0이거나 null이면 값 2 반환, 그렇지 않으면 값 1 반환<br /> </td> 
   <td> Coalesce(&lt;값 1&gt;, &lt;값 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> 값 1 = 값 2이면 값 3 반환 가 아닌 경우 값 4를 반환합니다.<br /> </td> 
   <td> Decode(&lt;값 1&gt;, &lt;값 2&gt;, &lt;값 3&gt;, &lt;값 4&gt;)<br /> </td>  
  </tr> 
  <!--<tr> 
   <td> <strong>DefaultFolder</strong><br /> </td> 
   <td> Returns value 3 if value 1 = value 2. If not returns value 4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr> -->
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> 값 1 반환(case 함수의 매개 변수로만 사용할 수 있음)<br /> </td> 
   <td> Else(&lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 이메일 주소에서 도메인 추출<br /> </td> 
   <td> GetEmailDomain(&lt;값&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 미러 페이지 서버의 URL 검색<br /> </td> 
   <td> GetMirrorURL(&lt;값&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 표현식이 true인 경우 값 1 반환 그렇지 않으면 값 2 반환<br /> </td> 
   <td> Iif(&lt;조건&gt;, &lt;값 1&gt;, &lt;값 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 플래그가 값에 있는지 표시<br /> </td> 
   <td> IsBitSet(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 문자열 1이 비어 있으면 값 2 반환, 그렇지 않으면 값 3 반환<br /> </td> 
   <td> IsEmptyString(&lt;value&gt;, &lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> 고유 ID 반환<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 인수가 NULL이면 빈 문자열 반환<br /> </td> 
   <td> NoNull(&lt;값&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 행 번호 반환<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> 값에 플래그 강제 적용<br /> </td> 
   <td> SetBit(&lt;식별자&gt;, &lt;플래그&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 숫자를 부울로 변환<br /> </td> 
   <td> ToBoolean(&lt;숫자&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> 표현식이 true인 경우 값 1 반환 그렇지 않으면 값 2 를 반환합니다(case 함수의 매개 변수로만 사용할 수 있음).<br /> </td> 
   <td> When(&lt;조건&gt;, &lt;값 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 문자열

문자열 함수는 문자열 집합을 조작하는 데 사용됩니다.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 모든 매개 변수가 null이 아니고 비어 있지 않은지 표시<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 모든 매개 변수가 null이 아니고 비어 있지 않은지 표시<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> 문자열에서 첫 번째 문자의 ASCII 값을 반환합니다.<br /> </td> 
   <td> Ascii(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 'n' ASCII 코드에 해당하는 문자 반환<br /> </td> 
   <td> Char(&lt;number&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 문자열 1에서 문자열 2의 위치를 반환합니다.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> 문자열의 크기(바이트) 반환<br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 문자열의 n번째(1에서 n까지) 행 반환<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 처음 두 매개 변수가 동일한 경우 세 번째 매개 변수를 반환합니다. 그렇지 않으면 마지막 매개 변수를 반환합니다.<br /> </td> 
   <td> IfEquals(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 매개 변수로 전달된 메모가 null인지 표시<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 매개 변수로 전달된 문자열을 연결합니다. 필요한 경우 문자열 사이에 공백을 추가합니다.<br /> </td> 
   <td> JuxtWords(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 매개 변수로 전달된 문자열을 연결합니다. 필요한 경우 문자열 사이에 공백을 추가합니다.<br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> 문자열의 처음 n자 반환<br /> </td> 
   <td> Left(&lt;string&gt;, &lt;number&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> 문자열의 길이 반환<br /> </td> 
   <td> Length(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>라인</strong><br /> </td> 
   <td> 문자열에서 n행 추출<br /> </td> 
   <td> Line(&lt;string&gt;,&lt;number&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> 문자열을 소문자로 반환<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 왼쪽에서 완성된 문자열 반환<br /> </td> 
   <td> LPad (&lt;string&gt;, &lt;number&gt;, &lt;char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 문자열 왼쪽의 공백 제거<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 문자열의 MD5 키를 16진수로 반환<br /> </td> 
   <td> Md5Digest(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> 메모에 매개 변수로 전달된 문자열이 포함되어 있는지 지정<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> XPath 및 필드 데이터에서 XML 필드의 값을 추출합니다.<br /> </td> 
   <td> NodeValue (&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> 지정된 문자열 값의 모든 발생 항목을 다른 문자열 값으로 바꿉니다.<br /> </td> 
   <td> Replace(&lt;string&gt;,&lt;string&gt;,&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> 문자열의 마지막 n자 반환<br /> </td> 
   <td> Right(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 오른쪽에 완성된 문자열 반환<br /> </td> 
   <td> RPad(&lt;string&gt;, &lt;number&gt;, &lt;character&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 문자열 오른쪽의 공백 제거<br /> </td> 
   <td> Rtrim(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 문자열의 SHA256 키를 16진수로 표시합니다.<br /> </td> 
   <td> Sha256Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 문자열의 SHA512 키의 16진수 표현입니다.<br /> </td> 
   <td> Sha512Digest (&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> 각 단어의 첫 번째 문자가 대문자로 표시된 문자열 반환<br /> </td> 
   <td> Smart(&lt;문자열&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> 문자열의 문자 n1에서 시작하여 길이 n2의 하위 문자열 추출<br /> </td> 
   <td> Substring(&lt;문자열&gt;, &lt;오프셋&gt;, &lt;길이&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 숫자를 문자열로 변환<br /> </td> 
   <td> ToString(&lt;number&gt;, &lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> 문자열을 대문자로 반환<br /> </td> 
   <td> Upper(&lt;문자열&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외부 키 반환<br /> </td> 
   <td> VirtualLink(&lt;숫자&gt;, &lt;&lt;숫자&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 다른 두 매개 변수가 동일한 경우 매개 변수로 전달된 링크의 외부(텍스트) 키 반환<br /> </td> 
   <td> VirtualLinkStr(&lt;문자열&gt;, &lt;숫자&gt;, &lt;숫자&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 창

<table> 
 <tbody> 
  <tr> 
   <td> <strong>이름</strong><br /> </td> 
   <td> <strong>설명</strong><br /> </td> 
   <td> <strong>구문</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> 첫 번째 매개 변수로 입력한 SQL 함수 호출 실행, 파티션 또는 두 번째 매개 변수로 입력한 정렬 기준 필드<br /> </td> 
   <td> _Over_ (&lt;value&gt;, &lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> 내림차순 정렬 적용<br /> </td> 
   <td> Desc(&lt;값 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 파티션 내의 결과 정렬<br /> </td> 
   <td> OrderBy(&lt;값 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 테이블에서 쿼리 결과 분할<br /> </td> 
   <td> PartitionBy(&lt;값 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> 테이블 파티션 및 정렬 시퀀스에 따라 행 번호를 생성합니다.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;값 1&gt;), OrderBy(&lt;값 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
