---
audience: end-user
title: 페더레이션 데이터베이스와의 연결 만들기 및 관리
description: Federated Database와의 연결을 만들고 관리하는 방법 알아보기
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 3f9980840bd9a8e5052d34835c40440c722d13cb
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 11%

---

# 연결 만들기 {#connections-fdb}

>[!AVAILABILITY]
>
>연결에 액세스하려면 다음 권한 중 하나가 필요합니다.
>
>-**페더레이션 데이터베이스 관리**
>&#x200B;>-**페더레이션 데이터베이스 보기**
>
>필요한 권한에 대한 자세한 내용은 [액세스 제어 안내서](/help/governance-privacy-security/access-control.md)를 참조하십시오.

Experience Platform Federated Audience Composition을 사용하면 서드파티 데이터 웨어하우스에서 대상을 구축 및 강화하고 해당 대상을 Adobe Experience Platform으로 가져올 수 있습니다.

## 지원되는 데이터베이스 {#supported-databases}

페더레이션 데이터베이스와 Adobe Experience Platform을 사용하여 작업하려면 먼저 두 소스 간에 연결을 설정해야 합니다. Federated Audience Composition을 사용하여 다음 데이터베이스에 연결할 수 있습니다.

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## 연결 만들기 {#create}

연결을 만들려면 Federated Data 섹션 내에서 **[!UICONTROL Federated database]**&#x200B;를 선택하십시오.

![Federated Databases 단추가 왼쪽 탐색 내에서 강조 표시됩니다.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

[통합 데이터베이스] 섹션이 나타납니다. 연결을 만들려면 **[!UICONTROL 페더레이션 데이터베이스 추가]**&#x200B;를 선택하십시오.

![Federated 데이터베이스 추가 단추가 Federated 데이터베이스 표시 페이지 내에서 강조 표시됩니다.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

연결 속성 팝오버가 나타납니다. 연결의 이름을 지정하고 생성할 데이터베이스 유형을 선택할 수 있습니다.

![연결된 데이터베이스 형식이 표시됩니다.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

유형을 선택하면 **[!UICONTROL 세부 정보]** 섹션이 나타납니다. 이 섹션은 이전에 선택한 데이터베이스 유형에 따라 다릅니다.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Amazon Redshift AWS, Amazon Redshift Spectrum 및 Amazon Redshift Serverless만 지원됩니다.

Amazon Redshift를 선택한 후 다음 세부 사항을 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | 데이터 소스의 이름입니다. |
| 계정 | 계정의 사용자 이름. |
| 암호 | 계정의 암호입니다. |
| 데이터베이스 | 데이터베이스의 이름입니다. 서버 이름에 이 필드를 지정하면 이 필드를 비워 둘 수 있습니다. |
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. 이 기능에 대한 자세한 내용은 [Amazon 스키마 설명서](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}를 참조하세요.<br/><br/>**참고:** 이 스키마에 연결하는 데 필요한 권한이 있으면 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스의 모든 스키마를 사용할 수 있습니다. 그러나 **반드시**&#x200B;은(는) 동일한 데이터베이스를 사용하여 여러 샌드박스를 연결할 때 고유한 작업 스키마를 사용합니다. |

>[!TAB Azure Synapse 분석]

>[!NOTE]
>
>Azure Synapse Analytics를 사용하여 보안 연결을 만들려면 Adobe 고객 지원 센터 담당자에게 문의하십시오.

Azure Synapse Analytics를 선택한 후 다음 세부 정보를 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | Azure Synapse 서버의 URL입니다. |
| 계정 | Azure Synapse 계정의 사용자 이름입니다. |
| 암호 | Azure synapse 계정의 암호입니다. |
| 데이터베이스 | 데이터베이스의 이름입니다. 서버 이름에 이 필드를 지정하면 이 필드를 비워 둘 수 있습니다. |
| 옵션 | 연결에 대한 추가 옵션. Azure Synapse Analytics의 경우 커넥터에서 지원하는 인증 유형을 지정할 수 있습니다. 현재 Federated Audience Composition은 `ActiveDirectoryMSI`을(를) 지원합니다. 연결 문자열에 대한 자세한 내용은 Microsoft 설명서의 [연결 문자열 예제 섹션](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}을 참조하십시오. |

>[!TAB 데이터 블록]

>[!NOTE]
>
>비공개 링크를 통한 외부 Databricks 데이터 웨어하우스에 대한 보안 액세스가 지원됩니다. 여기에는 비공개 링크를 통해 Amazon Web Services(AWS)에 호스팅된 Databricks 데이터베이스에 대한 보안 연결과 VPN을 통해 Microsoft Azure에서 호스팅된 Databricks 데이터베이스에 대한 보안 연결이 포함됩니다. 보안 액세스를 설정하는 데 도움이 필요한 경우 Adobe 담당자에게 문의하십시오.

데이터 블록을 선택한 후 다음 세부 사항을 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | Databricks 서버의 이름입니다. |
| HTTP 경로 | 클러스터 또는 웨어하우스에 대한 경로입니다. 경로에 대한 자세한 내용은 연결 세부 정보에 대한 [Databricks 설명서](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}를 참조하십시오. |
| 암호 | Databricks 서버에 대한 액세스 토큰입니다. 이 값에 대한 자세한 내용은 개인 액세스 토큰에 대한 [Databricks 설명서](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}를 참조하십시오. |
| 카탈로그 | Databricks 카탈로그의 이름입니다. 데이터 블록의 카탈로그에 대한 자세한 내용은 카탈로그의 [데이터 블록 설명서](https://docs.databricks.com/aws/en/catalogs/){target="_blank"}를 참조하십시오. |
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. <br/><br/>**참고:** 이 스키마에 연결하는 데 필요한 권한이 있으면 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스에서 **any** 스키마를 사용할 수 있습니다. 그러나 **반드시**&#x200B;은(는) 동일한 데이터베이스를 사용하여 여러 샌드박스를 연결할 때 고유한 작업 스키마를 사용합니다. |
| 옵션 | 연결에 대한 추가 옵션. 다음 표에는 사용 가능한 옵션이 나열되어 있습니다. |

데이터 블록의 경우 다음과 같은 추가 옵션을 설정할 수 있습니다.

| 옵션 | 설명 |
| ------- | ----------- |
| TimeZoneName | 사용할 표준 시간대의 이름입니다. 이 값은 `TIMEZONE` 세션 매개 변수를 나타냅니다. 시간대에 대한 자세한 내용은 [시간대에 대한 Databricks 설명서](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}를 참조하십시오. |

>[!TAB Google BigQuery]

Google BigQuery를 선택한 후 다음 세부 사항을 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서비스 계정 | 서비스 계정의 이메일 주소입니다. 자세한 내용은 [Google Cloud Service 계정 설명서](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}를 참조하십시오. |
| 프로젝트 | 프로젝트의 ID입니다. 자세한 내용은 [Google Cloud 프로젝트 설명서](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}를 참조하십시오. |
| 데이터 세트 | 데이터 세트의 이름입니다. 자세한 내용은 [Google Cloud 데이터 세트 설명서](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}를 참조하십시오. |
| 키 파일 경로 | 서버에 대한 키 파일입니다. `json`개의 파일만 지원됩니다. |
| 옵션 | 연결에 대한 추가 옵션. 다음 표에는 사용 가능한 옵션이 나열되어 있습니다. |

Google BigQuery의 경우 다음과 같은 추가 옵션을 설정할 수 있습니다.

| 옵션 | 설명 |
| ------- | ----------- |
| ProxyType | BigQuery에 연결하는 데 사용되는 프록시 유형입니다. 지원되는 값은 `HTTP`, `http_no_tunnel`, `socks4` 및 `socks5`입니다. |
| ProxyHost | 프록시에 연결할 수 있는 호스트 이름 또는 IP 주소입니다. |
| ProxyUid | 프록시가 실행 중인 포트 번호입니다. |
| ProxyPwd | 프록시 암호. |
| bgpath | **참고:** **일괄 로드 도구**(Cloud SDK)에만 적용됩니다. <br/><br/> 서버의 Cloud SDK bin 디렉터리에 대한 경로입니다. `google-cloud-sdk` 디렉터리를 다른 위치로 이동했거나 PATH 변수를 사용하지 않으려면 이 설정만 하면 됩니다. |
| GCloudConfigName | **참고:** 버전 7.3.4 이상의 **대량 로드 도구**(Cloud SDK)에만 적용할 수 있습니다. <br/><br/> 데이터 로드를 위한 매개 변수를 저장하는 구성의 이름입니다. 기본적으로 이 값은 `accfda`입니다. |
| GCloudDefaultConfigName | **참고:** 이 방법은 버전 7.3.4 이상의 **대량 로드 도구**(Cloud SDK)에만 적용됩니다. <br/><br/> 데이터 로드를 위한 기본 구성을 다시 만들 임시 구성의 이름입니다. 기본적으로 이 값은 `default`입니다. |
| GCloudRecreateConfig | **참고:** 버전 7.3.4 이상의 **일괄 로드 도구**(Cloud SDK)에만 적용할 수 있습니다. <br/><br/> 일괄 로드 메커니즘이 Google Cloud SDK 구성을 자동으로 다시 만들거나, 삭제하거나, 수정해야 하는지 여부를 결정할 수 있는 부울 값입니다. 이 값을 `false`(으)로 설정하면 대량 로드 메커니즘이 컴퓨터의 기존 구성을 사용하여 데이터를 로드합니다. 이 값을 `true`(으)로 설정하면 구성이 올바르게 설정되었는지 확인하십시오. 그렇지 않으면 `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` 오류가 나타나고 로딩 메커니즘이 기본 로딩 메커니즘으로 되돌아갑니다. |

>[!TAB Microsoft 패브릭]

Microsoft Fabric 을 선택한 후 다음 세부 사항을 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | Microsoft 패브릭 서버의 URL입니다. |
| 애플리케이션 ID | Microsoft Fabric에 대한 애플리케이션 ID. 응용 프로그램 ID에 대한 자세한 내용은 응용 프로그램 설정의 [Microsoft Fabric 설명서](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}를 참조하십시오. |
| 클라이언트 암호 | 애플리케이션의 클라이언트 암호입니다. 클라이언트 암호에 대한 자세한 내용은 응용 프로그램 설치[의 ](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}Microsoft Fabric 설명서를 참조하십시오. |
| 옵션 | 연결에 대한 추가 옵션. 다음 표에는 사용 가능한 옵션이 나열되어 있습니다. |

Microsoft Fabric의 경우 다음과 같은 추가 옵션을 설정할 수 있습니다.

| 옵션 | 설명 |
| ------ | ----------- |
| 인증 | 커넥터에서 사용하는 인증 유형입니다. 지원되는 값은 `ActiveDirectoryMSI`입니다. 자세한 내용은 웨어하우스 연결에 대한 [Microsoft 문서](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}를 참조하십시오. |

>[!TAB Oracle]

>[!IMPORTANT]
>
>보안 연결을 사용하기 위한 Oracle 연결 설정을 포함하여 Oracle 데이터베이스를 설정하기 전에 Adobe 고객 지원 센터 담당자에게 문의하십시오.

Oracle을 선택한 후 다음 세부 정보를 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | Oracle 서버의 URL입니다. |
| 계정 | 계정의 사용자 이름입니다. |
| 암호 | 계정의 암호입니다. |

>[!TAB Snowflake]

>[!NOTE]
>
>비공개 링크를 통한 외부 Snowflake Data Warehouse에 대한 보안 액세스가 지원됩니다. Snowflake 계정은 AWS(Amazon Web Services) 또는 Azure에서 호스팅되어야 하고 페더레이션된 대상자 구성 환경과 동일한 지역에 있어야 합니다. Snowflake 계정에 대한 보안 액세스를 설정하는 데 도움이 필요한 경우 Adobe 담당자에게 문의하십시오.

Snowflake을 선택한 후 다음 세부 정보를 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | 서버 이름입니다. |
| 사용자 | 계정의 사용자 이름입니다. |
| 암호 | 계정 암호입니다. |
| 데이터베이스 | 데이터베이스의 이름입니다. 서버 이름에 이 필드를 지정하면 이 필드를 비워 둘 수 있습니다. |
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. <br/><br/>**참고:** 이 스키마에 연결하는 데 필요한 권한이 있으면 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스에서 **any** 스키마를 사용할 수 있습니다. 그러나 **반드시**&#x200B;은(는) 동일한 데이터베이스를 사용하여 여러 샌드박스를 연결할 때 고유한 작업 스키마를 사용합니다. |
| 개인 키 | 데이터베이스 연결을 위한 개인 키입니다. 로컬 시스템에서 `.pem` 파일을 업로드할 수 있습니다. |
| 옵션 | 연결에 대한 추가 옵션. 다음 표에는 사용 가능한 옵션이 나열되어 있습니다. |

Snowflake의 경우 다음과 같은 추가 옵션을 설정할 수 있습니다.

| 옵션 | 설명 |
| ------- | ----------- |
| workschema | 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. |
| TimeZoneName | 사용할 표준 시간대의 이름입니다. 이 값은 `TIMEZONE` 세션 매개 변수를 나타냅니다. 기본적으로 시스템 시간대가 사용됩니다. 시간대에 대한 자세한 내용은 [시간대에 대한 Snowflake 설명서](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}를 참조하세요. |
| WeekStart | 한 주를 시작하고 싶은 요일. 이 값은 `WEEK_START` 세션 매개 변수를 나타냅니다. 주 시작에 대한 자세한 내용은 주 시작 매개 변수에 대한 [Snowflake 설명서](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"}를 참조하세요. |
| UseCachedResult | Snowflake의 캐시된 결과가 사용될지 여부를 결정하는 부울입니다. 이 값은 `USE_CACHED_RESULTS` 세션 매개 변수를 나타냅니다. 기본적으로 이 값은 true로 설정됩니다. 이 매개 변수에 대한 자세한 내용은 [지속적인 결과에 대한 Snowflake 설명서](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}를 참조하십시오. |
| bulkThreads | Snowflake의 벌크 로더에 사용할 스레드 수입니다. 스레드가 추가될수록 더 큰 벌크 로드에 대해 성능이 향상됩니다. 기본적으로 이 값은 1로 설정됩니다. |
| chunkSize | 각 벌크 로더의 청크에 대한 파일 크기입니다. 더 많은 스레드와 동시에 사용할 경우 벌크 로드 성능을 향상시킬 수 있습니다. 기본적으로 이 값은 128MB로 설정됩니다. 청크 크기에 대한 자세한 내용은 데이터 파일 준비에 대한 [Snowflake 설명서](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}를 참조하세요. |
| StageName | 사전 프로비저닝된 내부 스테이징 환경의 이름입니다. 새 임시 단계를 만드는 대신 벌크 로드에 사용할 수 있습니다. |

>[!TAB Vertica Analytics]

Vertica Analytics을 선택한 후 다음 세부 정보를 추가할 수 있습니다.

| 필드 | 설명 |
| ----- | ----------- |
| 서버 | Vertica Analytics 서버의 URL입니다. |
| 계정 | 계정의 사용자 이름입니다. |
| 암호 | 계정의 암호입니다. |
| 데이터베이스 | 데이터베이스의 이름입니다. 서버 이름에 이 필드를 지정하면 이 필드를 비워 둘 수 있습니다. |
| 작업 스키마 | 작업 테이블에 사용할 데이터베이스 스키마의 이름입니다. <br/><br/>**참고:** 이 스키마에 연결하는 데 필요한 권한이 있으면 임시 데이터 처리에 사용되는 스키마를 포함하여 데이터베이스에서 **any** 스키마를 사용할 수 있습니다. 그러나 **반드시**&#x200B;은(는) 동일한 데이터베이스를 사용하여 여러 샌드박스를 연결할 때 고유한 작업 스키마를 사용합니다. |
| 옵션 | 연결에 대한 추가 옵션. 다음 표에는 사용 가능한 옵션이 나열되어 있습니다. |

Vertica Analytics의 경우 다음과 같은 추가 옵션을 설정할 수 있습니다.

| 옵션 | 설명 |
| ------- | ----------- |
| TimeZoneName | 사용할 표준 시간대의 이름입니다. 이 값은 `TIMEZONE` 세션 매개 변수를 나타냅니다. 시간대에 대한 자세한 내용은 [시간대에 대한 Vertica Analytics 설명서](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"}를 참조하세요. |

>[!ENDTABS]

연결의 세부 정보를 추가한 후 다음의 추가 설정을 참고하십시오.

>[!NOTE]
>
>지정된 데이터베이스에 대해 Federated Audience Composition을 사용하려면 해당 데이터베이스와 연결된 IP 주소의 **모두**&#x200B;를 허용 목록 해야 합니다.

| 설정 | 세부 사항 |
| -------- | ------- |
| 연결 활성화 | 연결을 자동으로 활성화할지 여부를 결정하는 부울 토글 |
| 서버 IP | 데이터베이스에 연결하기 위해 허용 목록에추가된으로 제공되어야 하는 IP 주소를 표시하는 팝오버입니다. |
| 연결 테스트 | 구성 세부 사항을 확인할 수 있습니다. |

이제 **[!UICONTROL 함수 배포]**&#x200B;를 선택한 다음 **[!UICONTROL 추가]**&#x200B;를 선택하여 페더레이션 데이터베이스와 Experience Platform 간의 연결을 완료할 수 있습니다.
