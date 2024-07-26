---
audience: end-user
title: 페더레이션된 데이터베이스 시작하기
description: 페더레이션 데이터베이스를 만들고 관리하는 방법 알아보기
badge: label="제한된 가용성" type="Informative"
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: fa968e0c221befa7a0ddaef0f5908752f681c535
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 6%

---

# 페더레이션된 데이터베이스 시작하기 {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="페더레이션된 데이터베이스"
>abstract="페더레이션된 데이터베이스에 대해 이전에 처리된 연결이 이 화면에 나열됩니다. 새 연결을 생성하려면 **[!UICONTROL 페더레이션된 데이터베이스 추가]** 버튼을 클릭하십시오."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="페더레이션된 데이터베이스 속성"
>abstract="새 페더레이션된 데이터베이스의 이름을 입력하고 해당 유형을 선택합니다."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="페더레이션된 데이터베이스 세부 정보"
>abstract="새 페더레이션된 데이터베이스에 연결하기 위한 설정을 입력합니다. **[!UICONTROL 연결 테스트]** 버튼을 사용하여 구성을 검사합니다."

Experience Platform 연합 대상 구성을 통해 고객은 서드파티 데이터 웨어하우스에서 대상을 구축 및 강화하고 해당 대상을 Adobe Experience Platform으로 가져올 수 있습니다.

이 페이지에서 외부 데이터베이스에 대한 연결을 생성, 구성, 테스트 및 저장하는 방법을 알아봅니다.

## 지원되는 데이터베이스 {#supported-db}

Federated Audience Composition을 사용하여 다음 데이터베이스에 연결할 수 있습니다. 각 데이터베이스에 대한 구성은 아래에 자세히 설명되어 있습니다.

* [Amazon Redshift](#amazon-redshift)
* [Azure synapse](#azure-synapse-redshift)
* [Google BigQuery](#google-big-query)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)

## Amazon Redshift {#amazon-redshift}

통합 데이터베이스를 사용하여 외부 데이터베이스에 저장된 정보를 처리합니다. Amazon Redshift에 대한 액세스를 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합 데이터베이스 추가]**&#x200B;를 클릭합니다.

   ![](assets/federated_database_1.png)

1. 페더레이션 데이터베이스에 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Type]** 드롭다운에서 Amazon Redshift를 선택합니다.

   ![](assets/federated_database_6.png)

1. Amazon Redshift 인증 설정을 구성합니다.

   * **[!UICONTROL 서버]**: DNS 이름을 추가합니다.

   * **[!UICONTROL 계정]**: 사용자 이름을 추가합니다.

   * **[!UICONTROL 암호]**: 계정 암호를 추가합니다.

   * **[!UICONTROL 데이터베이스]**: DSN에 지정되지 않은 경우 데이터베이스의 이름입니다. DSN에 지정된 경우 비워 둘 수 있습니다.

   * **[!UICONTROL 작업 스키마]**: 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. [자세히 알아보기](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

     >[!NOTE]
     >
     >이 스키마에 연결하는 데 필요한 권한이 있는 한 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스의 모든 스키마를 사용할 수 있습니다.

1. 구성을 확인하려면 **[!UICONTROL 연결 테스트]** 옵션을 선택하십시오.

1. 함수를 만들려면 **[!UICONTROL 함수 배포]** 단추를 클릭하십시오.

1. 구성이 완료되면 **[!UICONTROL 추가]**&#x200B;를 클릭하여 통합 데이터베이스를 만듭니다.

## Azure synapse Redshift {#azure-synapse-redshift}

통합 데이터베이스를 사용하여 외부 데이터베이스에 저장된 정보를 처리합니다. azure synapse Redshift에 대한 액세스를 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합 데이터베이스 추가]**&#x200B;를 클릭합니다.

   ![](assets/federated_database_1.png)

1. 페더레이션 데이터베이스에 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Type]** 드롭다운에서 Redshift Azure synapse을 선택합니다.

   ![](assets/federated_database_4.png)

1. azure synapse Redshift 인증 설정을 구성합니다.

   * **[!UICONTROL 서버]**: Azure synapse 서버의 URL을 입력하십시오.

   * **[!UICONTROL 계정]**: 사용자 이름을 입력하십시오.

   * **[!UICONTROL 암호]**: 계정 암호를 입력하십시오.

   * **[!UICONTROL 데이터베이스]**(선택 사항): DSN에 지정되지 않은 경우 데이터베이스 이름을 입력하십시오.

   * **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

1. 구성을 확인하려면 **[!UICONTROL 연결 테스트]** 옵션을 선택하십시오.

1. 함수를 만들려면 **[!UICONTROL 함수 배포]** 단추를 클릭하십시오.

1. 구성이 완료되면 **[!UICONTROL 추가]**&#x200B;를 클릭하여 통합 데이터베이스를 만듭니다.

| 옵션 | 설명 |
|---|---|
| 인증 | 커넥터에서 지원하는 인증 유형입니다. 현재 지원되는 값: ActiveDirectoryMSI. 자세한 내용은 [SQL 문서](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings)(연결 문자열 n°8 예제)를 참조하십시오. |


## Google BigQuery {#google-big-query}

통합 데이터베이스를 사용하여 외부 데이터베이스에 저장된 정보를 처리합니다. Google Big Query에 대한 액세스를 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합 데이터베이스 추가]**&#x200B;를 클릭합니다.

   ![](assets/federated_database_1.png)

1. 페더레이션 데이터베이스에 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Type]** 드롭다운에서 Google Big Query를 선택합니다.

   ![](assets/federated_database_3.png)

1. Google Big Query 인증 설정을 구성합니다.

   * **[!UICONTROL 서비스 계정]**: **[!UICONTROL 서비스 계정]**&#x200B;의 전자 메일을 입력하십시오. 자세한 내용은 [Google Cloud 설명서](https://cloud.google.com/iam/docs/creating-managing-service-accounts)를 참조하세요.

   * **[!UICONTROL 프로젝트]**: **[!UICONTROL 프로젝트]**&#x200B;의 이름을 입력하십시오. 자세한 내용은 [Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects)를 참조하세요.

   * **[!UICONTROL 데이터 집합]**: **[!UICONTROL 데이터 집합]**&#x200B;의 이름을 입력하십시오. 자세한 내용은 [Google Cloud 설명서](https://cloud.google.com/bigquery/docs/datasets-intro)를 참조하세요.

   * **[!UICONTROL 키 파일 경로]**: 서버에 키 파일을 업로드합니다. .json 파일만 허용됩니다.

   * **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

1. 구성을 확인하려면 **[!UICONTROL 연결 테스트]** 옵션을 선택하십시오.

1. 함수를 만들려면 **[!UICONTROL 함수 배포]** 단추를 클릭하십시오.

1. 구성이 완료되면 **[!UICONTROL 추가]**&#x200B;를 클릭하여 통합 데이터베이스를 만듭니다.

| 옵션 | 설명 |
|---|---|
| ProxyType | ODBC 및 SDK 커넥터를 통해 BigQuery에 연결하는 데 사용되는 프록시 유형입니다. </br>HTTP(기본값), http_no_tunnel, socks4 및 socks5가 현재 지원됩니다. |
| ProxyHost | 프록시에 연결할 수 있는 호스트 이름 또는 IP 주소입니다. |
| ProxyPort | 프록시가 실행 중인 포트 번호(예: 8080) |
| ProxyUid | 인증된 프록시에 사용되는 사용자 이름 |
| 프록시 로드 | ProxyUid 암호 |
| bqpath | 이 기능은 대량 로드 도구(Cloud SDK)에만 적용할 수 있습니다. </br> PATH 변수를 사용하지 않거나 google-cloud-sdk 디렉터리를 다른 위치로 이동해야 하는 경우 이 옵션을 사용하여 서버의 cloud sdk bin 디렉터리에 대한 정확한 경로를 지정할 수 있습니다. |
| GCloudConfigName | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> Google Cloud SDK는 구성을 사용하여 데이터를 BigQuery 테이블에 로드합니다. 이름이 `accfda`인 구성은 데이터를 로드하기 위한 매개 변수를 저장합니다. 그러나 이 옵션을 사용하면 구성에 대해 다른 이름을 지정할 수 있습니다. |
| GCloudDefaultConfigName | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> 활성 태그를 새 구성으로 먼저 전송하지 않으면 활성 Google Cloud SDK 구성을 삭제할 수 없습니다. 이 임시 구성은 데이터 로드를 위한 기본 구성을 다시 만드는 데 필요합니다. 임시 구성의 기본 이름은 `default`입니다. 필요한 경우 변경할 수 있습니다. |
| GCloudRecreateConfig | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> `false`(으)로 설정된 경우 벌크 로드 메커니즘은 Google Cloud SDK 구성을 다시 만들거나 삭제하거나 수정하지 않습니다. 대신 시스템의 기존 구성을 사용하여 데이터 로드를 계속 진행합니다. 이 기능은 다른 작업이 Google Cloud SDK 구성에 따라 달라질 때 유용합니다. </br> 사용자가 적절한 구성 없이 이 엔진 옵션을 사용하도록 설정하면 대량 로드 메커니즘에서 경고 메시지가 표시됩니다. `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. 추가 오류를 방지하기 위해 기본 ODBC 배열 삽입 대량 로드 메커니즘을 사용하는 것으로 돌아갑니다. |


## Snowflake {#snowflake}

통합 데이터베이스를 사용하여 외부 데이터베이스에 저장된 정보를 처리합니다. Snowflake 액세스를 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합 데이터베이스 추가]**&#x200B;를 클릭합니다.

   ![](assets/federated_database_1.png)

1. 페더레이션 데이터베이스에 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL 유형]** 드롭다운에서 Snowflake을 선택합니다.

   ![](assets/federated_database_2.png)

1. Snowflake 인증 설정을 구성합니다.

   * **[!UICONTROL 서버]**: 서버 이름을 입력하십시오.

   * **[!UICONTROL 사용자]**: 사용자 이름을 입력하십시오.

   * **[!UICONTROL 암호]**: 계정 암호를 입력하십시오.

   * **[!UICONTROL 데이터베이스]**(선택 사항): DSN에 지정되지 않은 경우 데이터베이스 이름을 입력하십시오.

   * **[!UICONTROL 작업 스키마]**(선택 사항): 작업 테이블에 사용할 데이터베이스 스키마의 이름을 입력합니다.

     >[!NOTE]
     >
     >이 스키마에 연결하는 데 필요한 권한이 있는 한 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스의 모든 스키마를 사용할 수 있습니다.

   * **[!UICONTROL 개인 키]**: **[!UICONTROL 개인 키]** 필드를 클릭하여 로케일 폴더에서 .pem 파일을 선택합니다.

   * **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

1. 구성을 확인하려면 **[!UICONTROL 연결 테스트]** 옵션을 선택하십시오.

1. 함수를 만들려면 **[!UICONTROL 함수 배포]** 단추를 클릭하십시오.

1. 구성이 완료되면 **[!UICONTROL 추가]**&#x200B;를 클릭하여 통합 데이터베이스를 만듭니다.

커넥터는 다음 옵션을 지원합니다.

| 옵션 | 설명 |
|---|---|
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마 |
| warehouse | 사용할 기본 웨어하우스 이름. 사용자의 기본값보다 우선 적용됩니다. |
| 시간대 이름 | 기본적으로 비어 있음, 즉 Campaign Classic 앱 서버의 시스템 시간대가 사용됩니다. 옵션을 사용하여 시간대 세션 매개 변수를 강제 적용할 수 있습니다. <br>자세한 정보는 [이 페이지](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone)를 참조하세요. |
| WeekStart | WEEK_START 세션 매개 변수. 기본적으로 0으로 설정됩니다. <br>자세한 정보는 [이 페이지](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start)를 참조하세요. |
| UseCachedResult | USE_CACHED_RESULTS 세션 매개 변수 기본적으로 TRUE로 설정됩니다. 이 옵션은 캐시된 Snowflake 결과를 비활성화하는 데 사용할 수 있습니다. <br>자세한 정보는 [이 페이지](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html)를 참조하세요. |
| bulkThread | Snowflake 벌크 로더에 사용할 스레드 수. 더 많은 스레드는 더 큰 벌크 로드에 대해 더 나은 성능을 의미합니다. 기본적으로 1로 설정됩니다. 컴퓨터 스레드 수에 따라 숫자를 조정할 수 있습니다. |
| 청크 크기 | 대량 로더 청크의 파일 크기를 결정합니다. 기본적으로 128MB로 설정됩니다. bulkThreads와 함께 사용할 때 최적의 성능을 위해 수정할 수 있습니다. 동시에 활성화된 스레드가 많을수록 성능이 향상됩니다. <br>자세한 내용은 [Snowflake 설명서](https://docs.snowflake.net/manuals/sql-reference/sql/put.html)를 참조하세요. |
| StageName | 사전 프로비저닝된 내부 단계의 이름입니다. 새 임시 단계를 만드는 대신 일괄 로드에서 사용됩니다. |


## Vertica Analytics {#vertica-analytics}

통합 데이터베이스를 사용하여 외부 데이터베이스에 저장된 정보를 처리합니다. vertica analytics에 대한 액세스를 구성하려면 아래 단계를 따르십시오.

1. **[!UICONTROL 페더레이션 데이터]** 메뉴에서 **[!UICONTROL 페더레이션 데이터베이스]**&#x200B;를 선택합니다.

1. **[!UICONTROL 통합 데이터베이스 추가]**&#x200B;를 클릭합니다.

   ![](assets/federated_database_1.png)

1. 페더레이션 데이터베이스에 **[!UICONTROL 이름]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL 유형]** 드롭다운에서 Vertica analytics을 선택합니다.

   ![](assets/federated_database_5.png)

1. vertica analytics 인증 설정을 구성합니다.

   * **[!UICONTROL 서버]**: [!DNL Vertica Analytics] 서버의 URL을 추가합니다.

   * **[!UICONTROL 계정]**: 사용자 이름을 추가합니다.

   * **[!UICONTROL 암호]**: 계정 암호를 추가합니다.

   * **[!UICONTROL 데이터베이스]**(선택 사항): DSN에 지정되지 않은 경우 데이터베이스 이름을 입력하십시오.

   * **[!UICONTROL 작업 스키마]**(선택 사항): 작업 테이블에 사용할 데이터베이스 스키마의 이름을 입력합니다.

     >[!NOTE]
     >
     >이 스키마에 연결하는 데 필요한 권한이 있는 한 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스의 모든 스키마를 사용할 수 있습니다.

   * **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

1. 구성을 확인하려면 **[!UICONTROL 연결 테스트]** 옵션을 선택하십시오.

1. 함수를 만들려면 **[!UICONTROL 함수 배포]** 단추를 클릭하십시오.

1. 구성이 완료되면 **[!UICONTROL 추가]**&#x200B;를 클릭하여 통합 데이터베이스를 만듭니다.

커넥터는 다음 옵션을 지원합니다.

| 옵션 | 설명 |
|---|---|
| 시간대 이름 | 기본적으로 비어 있음, 즉 Campaign Classic 앱 서버의 시스템 시간대가 사용됩니다. 옵션을 사용하여 시간대 세션 매개 변수를 강제 적용할 수 있습니다. |
