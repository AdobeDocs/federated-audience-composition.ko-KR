---
title: Experience Platform 페더레이션된 대상자 구성의 새로운 기능
description: 최신 업데이트 및 릴리스 정보
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: eee35ac94be4192a2e4f9372caec164fbf0e2471
workflow-type: ht
source-wordcount: '1246'
ht-degree: 100%

---

# 릴리스 정보 {#rn-new}

[!DNL Federated Audience Composition]은 지속적으로 새로운 기능, 기존 기능 개선, 버그 해결을 제공합니다. 이 릴리스 정보에는 모든 변경 사항이 통합되어 있습니다. [!DNL Federated Audience Composition]은 기본적으로 [!DNL Adobe Experience Platform] 기반으로 빌드되었으며 최신 혁신 및 향상된 기능을 활용할 수 있습니다. 변경 사항에 대한 자세한 내용은 [Adobe Experience Platform 릴리스 정보](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}를 참조하십시오.

## 2025년 5월 릴리스 {#fac-25-5}

### 새로운 기능 {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>데이터 모델 캔버스 보기 - 일반 가용성</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>이제 캔버스 보기가 포함된 데이터 모델을 모든 고객이 이용할 수 있습니다.</p>
<p>데이터 모델에 대한 캔버스 보기 섹션이 기존의 표 형식으로 보기와 함께 캔버스 레이아웃에서 데이터 모델과 해당 링크를 시각화할 수 있도록 함으로써 사용자 경험이 개선되었습니다. </p>
<p>캔버스 보기에 대한 자세한 내용은 <a href="../data-management/gs-models.md">데이터 모델 개요</a>를 참조하십시오.</p>
</br>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#fac-25-5-improvements}

이번 릴리스는 다음과 같은 개선 사항과 함께 제공됩니다.

* **역할 기반 액세스 제어**

  5월 릴리스부터 [!DNL Federated Audience Composition]이 액세스 제어를 위한 새로운 세부적인 권한을 지원합니다. 사용자는 이들 권한을 사용자 역할에 할당하여 [!DNL Federated Audience Composition]에 대해 더욱 정밀한 액세스 권한을 얻을 수 있습니다.

  새로운 권한에 대해 자세히 알아보려면 [페더레이션된 대상자 컴포지션 액세스 안내서](feature-access.md)를 참조하십시오.

## 2025년 4월 릴리스 {#fac-25-4}

### 새로운 기능 {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>데이터 모델 캔버스 보기 - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>데이터 모델에 대한 캔버스 보기 섹션이 기존의 표 형식으로 보기와 함께 캔버스 레이아웃에서 데이터 모델과 해당 링크를 시각화할 수 있도록 함으로써 사용자 경험이 개선되었습니다. </p>
<p>캔버스 보기가 포함된 데이터 모델은 현재 Beta 버전으로 일부 사용자에게만 제공됩니다.</p>
<p>자세한 내용은 <a href="../data-management/gs-models.md">세부 설명서</a>를 참조하십시오.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>제품 지식에 대한 AI 어시스턴트 지원</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>AI 어시스턴트는 Adobe의 개념을 탐색 및 이해하고 사용자의 특정 환경에 대한 운영 인사이트를 얻는 데 사용할 수 있도록 설계된 사용자 인터페이스 기능입니다. 페더레이션된 대상자 구성을 비롯한 Adobe Experience Cloud 전체의 여러 제품에서 사용할 수 있습니다.</p>
<p>자세한 내용은 <a href="../start/ai-assistant.md">세부 설명서</a>를 참조하십시오.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>프로필 활동 저장</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> 이제 페더레이션된 대상자 구성이 프로필 보강 사용 사례를 지원하여 외부 데이터 웨어하우스의 데이터로 기존 Experience Platform 프로필을 개선할 수 있도록 해 줍니다.
</p>
<p>자세한 내용은 <a href="../compositions/activities/save-profiles.md">세부 설명서</a>를 참조하십시오.</p>
</br>
</td>
</tr>
</tbody>
</table>

### 개선 사항 {#fac-25-4-improvements}

이번 릴리스는 아래의 개선 사항과 함께 제공됩니다.

* **데이터 모델 이름**

  이제 대상자 메뉴에서 **페더레이션된 컴포지션** 탭에 ID 대신 데이터 모델 이름이 표시되어 명확성과 더불어 전반적인 사용성이 향상되었습니다.

* **대상자**

  이제 사용자가 연관된 대상자가 없는 데이터 모델을 선택하는 경우에도 선택한 데이터 모델의 이름 또는 레이블이 대상자 메뉴에 표시됩니다.

* **대규모 대상자 내보내기**

  이제 페더레이션된 대상자 구성이 파일 크기가 1GB를 초과하는 대규모 대상자에 대한 내보내기를 지원합니다.

* **대상자 저장 활동**

  **대상자 저장** 활동에 사용자에게 대상자 생성 및 보강 중에 생성된 새 스키마와 데이터 세트에 거버넌스 레이블을 적용하기 위해 데이터 관리자와 협업하라는 알림이 추가되었습니다.
  [데이터 사용 레이블에 대해 자세히 알아보기](https://experienceleague.adobe.com/ko/docs/experience-platform/data-governance/labels/user-guide)

### 호환성 {#fac-25-4-compat}

* **Amazon Redshift 보안 연결**

  이번 새로운 릴리스에서는 페더레이션된 대상자 구성이 Amazon Redshift 데이터베이스에 대한 안전한 비공개 링크 연결을 지원합니다. [자세히 알아보기](../connections/federated-db.md#amazon-redshift)

* **Google Big Query**

  이번 새로운 릴리스를 통해 페더레이션된 대상자 구성이 Google Big Query 데이터베이스에 대한 안전한 VPN 연결을 지원합니다. [자세히 알아보기](../connections/federated-db.md#google-big-query)

## 2025년 3월 릴리스 {#fac-25-3}

### 개선 사항 {#fac-25-3-improvements}

이번 릴리스는 아래의 개선 사항과 함께 제공됩니다.

* **페더레이션된 대상자 구성 권한**

  3월 출시부터 [!DNL Federated Audience Composition]은 **페더레이션된 데이터 관리** 권한을 부여받은 사용자에게 **페더레이션된 데이터 관리** 및 **페더레이션된 컴포지션** 인터페이스에 대한 액세스 권한을 적용하기 시작합니다.

  사용자가 [!DNL Federated Audience Composition] 사용자 인터페이스에 계속 액세스하려면 관리자에게 연락하여 이 권한을 역할에 추가하는 것이 좋습니다.

  이 권한을 할당하는 방법을 알아보려면 [자세한 설명서](feature-access.md)를 참조하십시오.

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. 
-->


### 호환성 {#fac-25-3-compat}

* **Databricks 연결**

  이번 새로운 릴리스에서는 페더레이션된 대상자 구성이 이제 Databricks 데이터베이스 연결을 위한 개인 링크 연결을 지원합니다.
여기에는 비공개 링크를 통해 Amazon Web Services(AWS)에 호스팅된 Databricks 데이터베이스에 대한 보안 연결과 VPN을 통해 Microsoft Azure에서 호스팅된 Databricks 데이터베이스에 대한 보안 연결이 포함됩니다. [자세히 알아보기](../connections/federated-db.md#databricks)

* **B2B CDP 고객 지원**

  페더레이션된 대상자 구성은 이제 기업 간(B2B) 고객 데이터 플랫폼(CDP) 고객을 대상으로 사람 대상자 사용 사례를 제공합니다.

* **Snowflake 보안 연결**

  이번 새로운 릴리스에서는 페더레이션된 대상자 구성이 Microsoft Azure에서 호스팅되는 Snowflake 데이터베이스에 대한 안전한 개인 링크 연결을 지원합니다. [자세히 알아보기](../connections/federated-db.md#snowflake)

## 2025년 2월 릴리스 {#fac-25-2}

이 릴리스는 아래 목록에 있는 변경 사항과 함께 제공됩니다.

* **Microsoft Fabric 지원**

  이제 페더레이션된 대상자 구성을 통해 Microsoft Fabric 데이터베이스에 대한 연결을 설정할 수 있습니다. [자세히 알아보기](../connections/federated-db.md)

* **Amazon Redshift Spectrum 지원**

  Amazon Redshift 데이터베이스 연결에서 이제 Amazon Redshift Spectrum을 지원합니다. [자세히 알아보기](../connections/federated-db.md#amazon-redshift)

* **향상된 스키마 생성 경험**

  스키마 생성 프로세스가 더욱 직관적이고 손쉽게 탐색할 수 있도록 업데이트된 사용자 인터페이스를 통해 개선되었습니다. 이러한 개선 사항은 데이터 실무자가 더욱 원활하고 효율적으로 데이터 모델을 개발할 수 있도록 합니다. [자세히 알아보기](../customer/schemas.md)

* **Databricks에 대한 대상자 강화 지원**

  이제 대상자 읽기 플로우에서 Databricks를 사용할 수 있으며, Databricks 데이터베이스의 활성화를 지원하고 새로운 대상으로 설정할 수 있습니다. [자세히 알아보기](../connections/destinations.md)

## 2024년 11월 릴리스 {#fac-24-11}

### 개선 사항 {#fac-24-11-improvements}

이번 릴리스는 아래의 개선 사항과 함께 제공됩니다.

* **IP 주소 허용 목록**

  이제 Adobe Experience Platform 사용자 인터페이스에서 페더레이션된 데이터베이스를 추가할 때 페더레이션된 대상자 구성 인스턴스와 연관된 IP 주소를 직접 조회할 수 있습니다. 이를 통해 이들 IP를 손쉽게 복사 및 승인하고 데이터베이스에 연결하여 보안과 유연성을 향상시킬 수 있습니다. [자세히 알아보기](../connections/connections.md)

## 2024년 10월 릴리스 {#fac-24-10}

>[!AVAILABILITY]
>
>이전에는 조직 집합에만 사용할 수 있었던(LA) Adobe Experience Platform 페더레이션된 대상자 구성을 이제 모든 사용자가 사용할 수 있습니다(GA). 이 기능은 귀하가 제공하는 서비스를 기반으로 활성화되며, 관련 권한이 있는 경우에만 볼 수 있습니다. [자세히 알아보기](access-prerequisites.md)
>

### 호환성 {#fac-24-10-compat}

이제 이 새 릴리스를 통해 페더레이션된 대상자 구성이 아래 나열된 시스템과 호환됩니다.

* **Databricks 지원**

  이제 페더레이션된 대상자 구성을 통해 Databricks 데이터베이스에 대한 연결을 설정할 수 있습니다. [자세히 알아보기](../connections/federated-db.md#databricks)

* **AWS PrivateLink를 통한 Snowflake에 대한 보안 액세스 지원**

  이제 비공개 링크를 통한 외부 Snowflake Data Warehouse에 대한 보안 액세스가 지원됩니다. Snowflake 계정은 AWS(Amazon Web Services)에서 호스팅되어야 하며 페더레이션된 대상자 구성 환경과 동일한 지역에 있어야 합니다. Snowflake 계정에 대한 보안 액세스를 설정하는 데 도움이 필요한 경우 Adobe 담당자에게 문의하십시오. [자세히 알아보기](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless 지원**

  이번 새로운 릴리스를 통해 페더레이션된 대상자 구성이 [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}를 지원합니다.

### 개선 사항 {#fac-24-10-improvements}

이 릴리스는 아래 목록에 있는 개선 사항과 함께 제공됩니다.

* **기존 스키마 새로 고침**

  이제 페더레이션된 데이터베이스에서 열을 만들거나, 수정하거나, 삭제하면 해당 스키마에서 **[!UICONTROL 스키마 새로 고침]** 버튼을 클릭하여 변경 사항을 감지하고 적용할 수 있습니다. [자세히 알아보기](../customer/schemas.md#schema-refresh)

* **새 컴포지션에 데이터 모델 연결**

  이제 컴포지션을 만들 때 연결할 데이터 모델을 선택할 수 있습니다. 이 새 옵션을 사용하면 연결된 데이터 모델의 테이블만 사용할 수 있으므로 활동을 구성하기가 더 쉬워집니다. [자세히 알아보기](../compositions/create-composition.md)

## 2024년 7월 릴리스 - 페더레이션된 대상자 구성 (LA) {#fac-la}

페더레이션된 대상자 구성은 기업이 중요한 기업 데이터 세트를 사용하여 대상자를 조합하고 브랜드가 주도하는 즉각적 경험을 강화할 수 있도록 기업 데이터 웨어하우스에 대한 유연하고 확장된 액세스를 제공합니다. 이 새로운 접근 방식을 사용하면 [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/home){target="_blank"} 및/또는 [Adobe Journey Optimizer](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/ajo-home){target="_blank"} 사용자는 기존 데이터 웨어하우스에서 직접 대상자 데이터를 페더레이션하여 Adobe Experience Platform 대상자와 속성을 하나의 시스템에서 강화할 수 있습니다.

페더레이션된 대상자 구성은 웨어하우스 데이터 세트를 사용하여 유연하게 대상자를 조합할 필요가 있는 기업의 증가하는 시장 수요에 대응합니다. 이를 통해 기업은 데이터 이동을 줄이는 동시에 중요한 대상자 데이터를 마케팅 팀에 제공하여 사용 사례 요구 사항을 충족하고 맞춤화된 경험을 제공할 수 있습니다.

[이 페이지](get-started.md)와 [자주 묻는 질문](faq.md)에서 페더레이션된 대상자 구성에 대해 자세히 알아보십시오.

[이 페이지](access-prerequisites.md)에서 페더레이션된 대상자 구성에 액세스하기 위한 사전 요구 사항 및 현재 가드레일에 대한 자세한 내용을 알아보십시오.
