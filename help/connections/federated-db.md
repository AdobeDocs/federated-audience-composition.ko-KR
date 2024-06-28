---
audience: end-user
title: 통합 데이터베이스 시작
description: 페더레이션 데이터베이스를 만들고 관리하는 방법 알아보기
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 2%

---

# 통합 데이터베이스 시작 {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="페더레이션된 데이터베이스"
>abstract="페더레이션 데이터베이스에 대한 기존 연결이 이 화면에 나열됩니다. 새 연결을 만들려면 **통합 데이터베이스 추가** 단추를 클릭합니다."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="페더레이션 데이터베이스 속성"
>abstract="새 Federated Database의 이름을 입력하고 유형을 선택합니다."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="페더레이션 데이터베이스 세부 정보"
>abstract="새 페더레이션 데이터베이스에 연결할 설정을 입력하십시오. 사용 **연결 테스트** 단추를 클릭하여 구성을 확인합니다."

외부 데이터베이스에 대한 연결을 생성, 구성, 테스트 및 저장합니다.

지원되는 외부 데이터베이스:

* Snowflake
* Google BigQuery
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL 서버]**:

* **[!UICONTROL 사용자]**: 사용자의 이름입니다.

* **[!UICONTROL 암호]**: 사용자 계정 암호.

* **[!UICONTROL 데이터베이스]**:

* **[!UICONTROL 작업 스키마]**:

* **[!UICONTROL 개인 키]**: .pem 파일만 허용됩니다.

* **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

| 옵션 | 설명 |
|---|---|
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마 |
| warehouse | 사용할 기본 웨어하우스 이름. 사용자의 기본값보다 우선 적용됩니다. |
| 시간대 이름 | 기본적으로 비어 있음, 즉 Campaign Classic 앱 서버의 시스템 시간대가 사용됩니다. 옵션을 사용하여 시간대 세션 매개 변수를 강제 적용할 수 있습니다. <br>자세한 내용은 다음을 참조하십시오. [이 페이지](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | WEEK_START 세션 매개 변수. 기본적으로 0으로 설정됩니다. <br>자세한 내용은 다음을 참조하십시오. [이 페이지](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start). |
| UseCachedResult | USE_CACHED_RESULTS 세션 매개 변수 기본적으로 TRUE로 설정됩니다. 이 옵션은 캐시된 Snowflake 결과를 비활성화하는 데 사용할 수 있습니다. <br>자세한 내용은 다음을 참조하십시오. [이 페이지](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThread | Snowflake 벌크 로더에 사용할 스레드 수. 더 많은 스레드는 더 큰 벌크 로드에 대해 더 나은 성능을 의미합니다. 기본적으로 1로 설정됩니다. 컴퓨터 스레드 수에 따라 숫자를 조정할 수 있습니다. |
| 청크 크기 | 대량 로더 청크의 파일 크기를 결정합니다. 기본적으로 128MB로 설정됩니다. bulkThreads와 함께 사용할 때 최적의 성능을 위해 수정할 수 있습니다. 동시에 활성화된 스레드가 많을수록 성능이 향상됩니다. <br>자세한 내용은 다음을 참조하십시오. [Snowflake 설명서](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| StageName | 사전 프로비저닝된 내부 단계의 이름입니다. 새 임시 단계를 만드는 대신 일괄 로드에서 사용됩니다. |

## Google BigQuery {#google-big-query}

* **[!UICONTROL 서비스 계정]**: 의 이메일 **[!UICONTROL 서비스 계정]**. 자세한 내용은 다음을 참조하십시오. [Google Cloud 설명서](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL 프로젝트]**: 의 이름 **[!UICONTROL 프로젝트]**. 자세한 내용은 다음을 참조하십시오. [Google Cloud 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL 데이터 세트]**: 의 이름 **[!UICONTROL 데이터 세트]**. 자세한 내용은 다음을 참조하십시오. [Google Cloud 설명서](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL 키 파일 경로]**: 서버에 키 파일을 업로드합니다. .json 파일만 허용됩니다.

* **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

| 옵션 | 설명 |
|:-:|:-:|
| ProxyType | ODBC 및 SDK 커넥터를 통해 BigQuery에 연결하는 데 사용되는 프록시 유형입니다. </br>HTTP(기본값), http_no_tunnel, socks4 및 socks5가 현재 지원됩니다. |
| ProxyHost | 프록시에 연결할 수 있는 호스트 이름 또는 IP 주소입니다. |
| ProxyPort | 프록시가 실행 중인 포트 번호(예: 8080) |
| ProxyUid | 인증된 프록시에 사용되는 사용자 이름 |
| 프록시 로드 | ProxyUid 암호 |
| bqpath | 이 기능은 대량 로드 도구(Cloud SDK)에만 적용할 수 있습니다. </br> PATH 변수를 사용하지 않거나 google-cloud-sdk 디렉토리를 다른 위치로 이동해야 하는 경우 이 옵션을 사용하여 서버의 cloud sdk bin 디렉토리에 대한 정확한 경로를 지정할 수 있습니다. |
| GCloudConfigName | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> Google Cloud SDK는 구성을 사용하여 데이터를 BigQuery 테이블에 로드합니다. 이름이 인 구성 `accfda` 데이터를 로드하기 위한 매개 변수를 저장합니다. 그러나 이 옵션을 사용하면 구성에 대해 다른 이름을 지정할 수 있습니다. |
| GCloudDefaultConfigName | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> 활성 태그를 새 구성으로 먼저 전송하지 않으면 활성 Google Cloud SDK 구성을 삭제할 수 없습니다. 이 임시 구성은 데이터 로드를 위한 기본 구성을 다시 만드는 데 필요합니다. 임시 구성의 기본 이름은 입니다. `default`, 필요한 경우 변경할 수 있습니다. |
| GCloudRecreateConfig | 릴리스 7.3.4 릴리스부터 대량 로드 도구 전용(Cloud SDK)에 적용할 수 있습니다.</br> 로 설정된 경우 `false`, 벌크 로드 메커니즘은 Google Cloud SDK 구성을 다시 생성, 삭제 또는 수정하지 않습니다. 대신 시스템의 기존 구성을 사용하여 데이터 로드를 계속 진행합니다. 이 기능은 다른 작업이 Google Cloud SDK 구성에 따라 달라질 때 유용합니다. </br> 사용자가 적절한 구성 없이 이 엔진 옵션을 활성화하면 벌크 로드 메커니즘에서 다음과 같은 경고 메시지가 표시됩니다. `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. 추가 오류를 방지하기 위해 기본 ODBC 배열 삽입 대량 로드 메커니즘을 사용하는 것으로 돌아갑니다. |

## Azure synapse Redshift {#azure-synapse-redshift}

* **[!UICONTROL 서버]**: Azure synapse 서버의 URL

* **[!UICONTROL 계정]**: 사용자 이름

* **[!UICONTROL 암호]**: 사용자 계정 암호

* **[!UICONTROL 데이터베이스]**: 데이터베이스 이름

* **[!UICONTROL 옵션]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL 서버]**: 의 URL [!DNL Vertica Analytics] server

* **[!UICONTROL 계정]**: 사용자 이름

* **[!UICONTROL 암호]**: 사용자 계정 암호

* **[!UICONTROL 데이터베이스]**: 데이터베이스 이름

* **[!UICONTROL 작업 스키마]**: 작업 스키마의 이름입니다.

* **[!UICONTROL 옵션]**: 커넥터가 아래 표에 설명된 옵션을 지원합니다.

커넥터는 다음 옵션을 지원합니다.

| 옵션 | 설명 |
|---|---|
| 시간대 이름 | 기본적으로 비어 있음, 즉 Campaign Classic 앱 서버의 시스템 시간대가 사용됩니다. 옵션을 사용하여 시간대 세션 매개 변수를 강제 적용할 수 있습니다. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL 서버]**: DNS 이름

* **[!UICONTROL 계정]**: 사용자 이름

* **[!UICONTROL 암호]**: 사용자 계정 암호

* **[!UICONTROL 데이터베이스]**: DSN에 지정되지 않은 경우 데이터베이스의 이름입니다. DSN에 지정된 경우 비워 둘 수 있습니다.

* **[!UICONTROL 작업 스키마]**: 작업 스키마의 이름입니다. [자세히 알아보기](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

