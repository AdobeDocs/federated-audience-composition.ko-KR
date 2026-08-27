---
title: 비공개 연결을 사용하여 Federated Audience Composition에 연결
description: 비공개 연결을 사용하여 Federated Audience Composition을 설정하고 연결하는 방법에 대해 알아봅니다. 여기에는 PrivateLink 또는 사이트 간 VPN이 포함됩니다.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Federated Audience Composition에 대한 비공개 연결

Federated Audience Composition은 여러 데이터베이스를 사용하는 비공개 연결을 지원합니다. 비공개 연결을 사용하면 공용 인터넷을 거치지 않고 고객이 호스팅하는 데이터 웨어하우스에 연결할 수 있습니다.

## 지원되는 데이터베이스 {#supported-databases}

다음 데이터베이스는 Federated Audience Composition에 대한 개인 연결을 지원합니다.

| 데이터베이스 | 클라우드 | 비공개 연결 유형 |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services]&#x200B;(AWS) | AWS PrivateLink (VPC 인터페이스 엔드포인트) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (비공개 엔드포인트) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services]&#x200B;(AWS) | AWS PrivateLink(관리되는 VPC 끝점) |
| [!DNL Databricks] | [!DNL Amazon Web Services]&#x200B;(AWS) | AWS PrivateLink (VPC 인터페이스 엔드포인트) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | 사이트 간 VPN |
| [!DNL Databricks] | [!DNL Google Cloud Platform]&#x200B;(GCP) | 사이트 간 VPN |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | 사이트 간 VPN |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform]&#x200B;(GCP) | 사이트 간 VPN |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>[!DNL Snowflake]과(와)의 개인 연결을 사용하려면 **이(가) 비즈니스 크리티컬 계층 또는 그 이상의 [!DNL Snowflake]에 있어야**&#x200B;합니다. [!DNL Snowflake]을(를) 통한 개인 연결에 대한 자세한 내용은 Snowflake 설명서의 [개인 연결 안내서](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound)를 참조하십시오.

[!DNL Snowflake]에서 개인 연결을 사용하는 것은 [!DNL Snowflake] 인스턴스가 사용하는 클라우드 공급자에 따라 다릅니다.

### Amazon Web Services(AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>계속하기 전에 Adobe 고객 지원 센터에서 AWS 계정 ID를 얻어야 합니다. AWS 계정 ID를 얻으면 [!DNL Snowflake] 지원팀에 문의하여 [!DNL Snowflake]에서 PrivateLink를 사용하도록 AWS 계정을 인증할 수 있습니다.

AWS 계정이 [!DNL Snowflake]에서 사용할 수 있도록 승인되면 VPC 인터페이스 끝점을 가져올 수 있도록 `privatelink-vpce-id`, `privatelink-account-url` 및 `privatelink_ocsp-url`을(를) 포함하는 값을 가져와야 합니다.

[!DNL Snowflake] 계정에서 ACCOUNTADMIN으로 다음 명령을 실행하여 이러한 값을 가져올 수 있습니다.

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

이러한 명령을 실행하면 전체 SQL 출력을 Adobe 고객 지원 센터로 전송하여 Adobe에서 VPC 인터페이스 엔드포인트를 자동으로 만들 수 있습니다.

AWS과의 PrivateLink 연결을 만드는 방법에 대한 자세한 내용은 [AWS PrivateLink 안내서](https://docs.snowflake.com/en/user-guide/admin-security-privatelink)를 참조하십시오.

내부 스테이징 환경에서 사용할 PrivateLink를 승인하려면 Adobe 고객 지원 센터에 문의하여 환경을 활성화하십시오.

내부 스테이징 환경을 위한 AWS과의 PrivateLink 연결을 만드는 방법에 대한 자세한 내용은 [내부 스테이지에 대한 AWS VPC 인터페이스 끝점 안내서](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws)를 참조하십시오.

### Microsoft Azure {#snowflake-azure}

Microsoft Azure의 경우 Azure 개인 끝점을 만들려면 `privatelink-pls-id`, `privatelink-account-url` 및 `privatelink_ocsp-url`을(를) 포함하는 값을 가져와야 합니다.

Snowflake 계정에서 다음 명령을 실행하여 이러한 값을 가져올 수 있습니다.

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

이 명령을 실행하면 전체 SQL 출력을 Adobe 고객 지원 센터로 전송하여 Adobe에서 Azure 개인 엔드포인트를 자동으로 생성할 수 있습니다.

Adobe에서 Azure 개인 끝점을 만들면 개인 끝점 리소스 ID를 가져올 수 있습니다. 이제 개인 끝점 리소스 ID가 있으므로 [!DNL Snowflake] 지원팀에 문의하여 [!DNL Snowflake] 계정을 인증하면서 리소스 ID를 제공하십시오.

Azure과의 PrivateLink 연결을 만드는 방법에 대한 자세한 내용은 [Azure PrivateLink 안내서](https://docs.snowflake.com/en/user-guide/privatelink-azure)를 참조하십시오.

내부 스테이징 환경에서 사용하도록 PrivateLink를 승인하려면 [!DNL Snowflake]에서 다음 명령을 실행하고 Adobe 고객 지원 센터에서 제공하는 내부 스테이징 리소스 ID를 제공하십시오.

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

내부 스테이징 환경을 위한 Azure과의 PrivateLink 연결을 만드는 방법에 대한 자세한 내용은 [내부 스테이지에 대한 Azure 개인 끝점 안내서](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure)를 참조하십시오.

## Amazon Redshift {#amazon-redshift}

프로비저닝된 클러스터와 Redshift Serverless 모두 Federated Audience Composition을 통한 비공개 연결을 지원합니다.

>[!IMPORTANT]
>
>시작하기 전에 Adobe 고객 지원 센터에 문의하여 Amazon Web Services(AWS) 계정 ID와 Virtual Private Cloud(VPC) ID를 받으십시오. 교차 계정 끝점 액세스를 얻으려면 이러한 값 중 **둘 다**&#x200B;이 필요합니다. VPC 액세스 권한 부여에 대한 자세한 내용은 [VPC 액세스 권한 부여](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html)를 참조하십시오.

AWS ID와 VPC ID가 모두 있으면 AWS Management Console로 이동하여 관리되는 VPC 종단점에 대해 교차 계정 액세스 권한을 부여합니다.

프로비저닝된 클러스터의 경우 **Redshift 클러스터 식별자**&#x200B;와 **클러스터 소유자 AWS 계정 ID** 값을 모두 메모하십시오. Redshift 서버를 사용하지 않는 경우 **작업 그룹 이름** 및 **소유자 AWS 계정 ID** 값을 모두 메모하십시오.

이러한 값을 얻은 후 Adobe에서 관리되는 VPC 엔드포인트를 만들 수 있도록 이러한 세부 정보를 Adobe 고객 지원 센터에 공유합니다. 그러면 Adobe에서 다음 연결 세부 정보를 공유합니다. **Redshift 끝점 URL**, **Redshift JDBC URL** 및 **Redshift ODBC URL**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Databricks에 대한 개인 연결을 사용하려면 **Databricks의 Enterprise 플랜에 있어야**&#x200B;합니다. Databricks와의 개인 연결에 대한 자세한 내용은 [개인 링크 개념 안내서](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts)를 참조하십시오.

Databricks와 개인 연결을 사용하는 것은 Databricks 인스턴스가 사용하는 클라우드 공급자에 따라 다릅니다.

### Amazon Web Services {#databricks-aws}

Amazon Web Services으로 구성하기 전에 Adobe 고객 지원 센터에 문의하여 데이터 블록을 가리키는 프론트엔드(인바운드) VPC 인터페이스 엔드포인트를 만들 수 있습니다. 이 끝점은 Databricks 작업 영역에 대한 Federated Audience Composition의 ODBC 연결을 다룹니다.

Adobe 고객 지원 센터에서 VPC 엔드포인트 ID 및 AWS 지역을 받으면 Adobe에서 제공하는 정보로 VPC 엔드포인트를 등록해야 합니다.

VPC 끝점을 등록한 후에는 개인 액세스 설정(PAS) 개체를 만들어야 합니다. 끝점을 만들 때 **개인 액세스 수준**&#x200B;을(를) **끝점** 수준으로 설정하고 이전에 만든 VPC 끝점을 선택합니다. 개인 액세스 설정을 만드는 방법에 대한 자세한 내용은 [인바운드 PrivateLink 구성 가이드](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings)를 참조하십시오.

개인 액세스 설정을 구성한 후 VPC 끝점을 작업 영역에 첨부할 수 있습니다. PrivateLink를 사용하여 작업 영역을 만드는 방법에 대한 자세한 내용은 [인바운드 PrivateLink 구성 가이드](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects)를 참조하십시오.

모든 설정이 구성되었으므로 이제 Databricks 작업 공간 URL을 Adobe 고객 지원 센터와 공유할 수 있습니다. Databricks 작업 공간 URL을 공유하면 Adobe이 요청을 작업 공간 끝점으로 라우팅하는 데 필요한 DNS 설정을 구성할 수 있습니다.

### Microsoft Azure {#databricks-azure}

사이트 간 VPN은 Adobe에서 Azure의 Databricks 작업 영역으로 안전하게 연결하는 데 사용됩니다. 데이터를 Azure으로 안전하게 전송하기 위해 VPN 터널을 설정하려면 Adobe VPN 게이트웨이를 설정해야 합니다.

Azure VPN 게이트웨이 및 Databricks 개인 끝점을 설정한 후에는 Adobe 고객 지원 센터 담당자에게 다음 세부 정보를 공유하십시오. **Azure Virtual Network Gateway**, **Databricks Private 끝점 IP**, **Databricks Workspace URL** 및 **ASN(Autonomous System Number)**.

이러한 세부 사항을 통해 Adobe은 연결에 필요한 VPN 터널을 설정할 수 있습니다. VPN 터널을 설정한 후 Adobe은 **VPN 터널 공용 및 개인 IP 주소**, **미리 공유한 키**&#x200B;와 **자동 시스템 번호**&#x200B;를 제공합니다.

이제 Azure VNet Gateway에서 VPN 터널을 구성할 수 있습니다. 자세한 내용은 [VPN 게이트웨이를 사용하여 AWS 및 Azure 연결](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)을 참조하세요.

### Google Cloud 플랫폼 {#databricks-gcp}

사이트 간 VPN은 Adobe에서 Google Cloud Platform의 Databricks 작업 영역으로 안전하게 연결하는 데 사용됩니다. 데이터를 Google에 안전하게 전송하기 위해 VPN 터널을 설정하려면 Adobe Cloud Platform 고가용성 VPN 게이트웨이 및 클라우드 라우터를 설정해야 합니다.

GCP HA VPN 게이트웨이 및 클라우드 라우터를 설정한 후에는 다음 세부 정보를 Adobe 고객 지원 센터 담당자에게 공유하십시오. **GCP HA VPN 게이트웨이**, **데이터 블록 Workspace URL**, **PSC(Private Service Connect) IP** 및 **ASN(Autonomous System Number)**.

이러한 세부 사항을 통해 Adobe은 연결에 필요한 VPN 터널을 설정할 수 있습니다. VPN 터널을 설정한 후 Adobe은 **VPN 터널 공용 및 개인 IP 주소**, **미리 공유한 키**&#x200B;와 **자동 시스템 번호**&#x200B;를 제공합니다.

이제 Google Cloud Platform 계정에서 VPN 터널을 구성할 수 있습니다. 자세한 내용은 [HA VPN 연결 만들기 안내서](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)를 참조하십시오.

## Azure Synapse Analytics {#azure-synapse}

Azure Synapse Analytics와 연결하려면 먼저 Azure 가상 네트워크 게이트웨이와 Synapse 개인 끝점을 만들어야 합니다. Azure 가상 네트워크 게이트웨이를 사용하면 Azure 가상 네트워크 간에 암호화된 트래픽을 Synapse로 보낼 수 있고, Synapse 개인 끝점을 사용하면 개인 연결을 통해 데이터를 안전하게 전송할 수 있습니다.

Azure 가상 네트워크 게이트웨이 및 Synapse 개인 끝점을 설정한 후에는 Adobe 고객 지원 센터 담당자에게 다음 세부 정보를 공유하십시오. **Azure 가상 네트워크 게이트웨이**, **Synapse 개인 끝점 IP**, **Synapse Workspace URL** 및 **ASN(Autonomous Service Number)**.

이러한 세부 사항을 통해 Adobe은 연결에 필요한 VPN 터널을 설정할 수 있습니다. VPN 터널을 설정한 후 Adobe은 **VPN 터널 연결**, **미리 공유한 키**&#x200B;와 **자율 시스템 번호**&#x200B;를 제공합니다.

이제 Azure VNet Gateway에서 VPN 터널을 구성할 수 있습니다. 자세한 내용은 [VPN 게이트웨이를 사용하여 AWS 및 Azure 연결](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp)을 참조하세요.

## Google Big Query {#gbq}

Google Big Query와 연결하려면 먼저 Google Cloud Platform 고가용성 VPN 게이트웨이 및 클라우드 라우터를 만들어야 합니다.

GCP HA VPN 게이트웨이 및 클라우드 라우터를 설정한 후에는 Adobe 고객 지원 센터 담당자에게 다음 세부 정보를 공유하십시오. **GCP HA VPN 게이트웨이**, **PSC(Private Service Connect) IP** 및 **ASN(Autonomous System Number)**.

이러한 세부 사항을 통해 Adobe은 연결에 필요한 VPN 터널을 설정할 수 있습니다. VPN 터널을 설정한 후 Adobe은 **VPN 터널 공용 및 개인 IP 주소**, **미리 공유한 키**&#x200B;와 **자동 시스템 번호**&#x200B;를 제공합니다.

이제 Google Cloud Platform 계정에서 VPN 터널을 구성할 수 있습니다. 자세한 내용은 [HA VPN 연결 만들기 안내서](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws)를 참조하십시오.
