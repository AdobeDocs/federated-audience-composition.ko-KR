---
title: 외부 데이터베이스 액세스 권한
description: 각 데이터베이스 엔진에 액세스하고 작업을 수행하는 데 필요한 권한에 대해 알아봅니다
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 5%

---

# FDA(Federated Data Access) 권한 매트릭스 {#fda-rights}

다음 표에서는 FDA(Federated Data Access)를 통해 외부 데이터베이스에서 작업을 수행할 수 있도록 각 시스템에 필요한 데이터베이스 권한을 간략하게 설명합니다.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **원격 데이터베이스에 연결** | `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` 및 `USAGE ON SCHEMA` 권한 | AWS 계정에 연결된 사용자 만들기 | 서비스 계정 만들기 및 프로젝트에 대한 사용자 액세스 권한 부여 | 카탈로그에 대한 `USE CATALOG` 권한과 SQL Warehouse에 대한 `CAN_USE` 권한 |
| **표 만들기** | `CREATE TABLE ON SCHEMA` 권한 | `CREATE` 권한 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create` 및 `bigquery.tables.create` 권한이 포함되어야 합니다. | `USE SCHEMA` 및 `CREATE TABLE` 권한 |
| **인덱스 만들기** | N/A | `CREATE` 권한 | BigQuery는 검색 인덱스만 지원합니다. 서비스 계정에 할당된 역할에는 `bigquery.jobs.create`, `bigquery.tables.getData` 및 `bigquery.tables.createIndex` 권한이 있어야 합니다. | N/A |
| **함수 만들기** | `CREATE FUNCTION ON SCHEMA` 권한 | 외부 Python 스크립트를 호출할 수 있는 `USAGE ON LANGUAGE plpythonu` 권한 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create` 및 `bigquery.routines.create` 권한이 포함되어야 합니다. | `CREATE FUNCTION` 권한 |
| **프로시저 만들기** | N/A | 외부 Python 스크립트를 호출할 수 있는 `USAGE ON LANGUAGE plpythonu` 권한 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create` 및 `bigquery.routines.create` 권한이 포함되어야 합니다. |  해당 사항 없음 |
| **개체(테이블, 인덱스, 함수, 프로시저) 제거** | 객체 소유 | 개체 소유 또는 수퍼유저 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` 및 `bigquery.tables.deleteIndex` 권한이 포함되어야 합니다. | N/A |
| **실행 모니터링** | 필요한 개체에 대한 `MONITOR` 권한 | `EXPLAIN` 명령을 사용하는 데 필요한 권한이 없습니다. | `monitoring.viewer` 역할 | `CAN_VIEW` 권한 |
| **데이터를 쓰는 중** | 쓰기 작업에 따라 `INSERT` 및/또는 `UPDATE` 권한 | `INSERT` 및 `UPDATE` 권한 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create` 및 `bigquery.tables.updateData`이(가) 포함되어야 합니다. | `MODIFY` 권한 |
| **테이블에 데이터 로드** | 대상 테이블 권한의 `CREATE STAGE ON SCHEMA`, `SELECT` 및 `INSERT` | `SELECT` 및 `INSERT` 권한 | 서비스 계정에 할당된 역할에는 `bigquery.jobs.create`, `bigquery.tables.getData` 및 `bigquery.tables.updateData`이(가) 포함되어야 합니다. | `SELECT` 및 `MODIFY` 권한 |
| **클라이언트 데이터에 액세스** | `SELECT on (FUTURE) TABLE(S)` 또는 `VIEW(S)` 권한 | `SELECT` 권한 | 서비스 계정에 할당된 역할에는 테이블 또는 `bigquery.dataViewer` 역할에 대해 `bigquery.jobs.create` 및 `bigquery.tables.getData`이(가) 포함되어야 합니다. | `SELECT` 권한 |
| **메타데이터에 액세스** | `SELECT on INFORMATION_SCHEMA SCHEMA` 권한 | `SELECT` 권한 | `bigquery.metadataViewer` 역할 |  `SELECT on INFORMATION_SCHEMA SCHEMA` 권한 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **원격 데이터베이스에 연결** | 읽기(기본값) 권한 | `CONNECT` 권한 | 권한 필요 없음 |
| **표 만들기** | `CREATE TABLE ON DATABASE`(웨어하우스) 및 `ALTER ON SCHEMA` | `CREATE TABLE` 권한 | `CREATE ON SCHEMA` 권한 |
| **인덱스 만들기** | N/A | `ALTER` 권한 | N/A |
| **함수 만들기** | N/A | `CREATE FUNCTION` 권한 | `CREATE ON SCHEMA` 권한 |
| **프로시저 만들기** | `CREATE PROCEDURE ON DATABASE`(웨어하우스) 및 `ALTER ON SCHEMA` | `CREATE PROCEDURE` 권한 | `CREATE ON SCHEMA` 권한 |
| **개체(테이블, 인덱스, 함수, 프로시저) 제거** | `ALTER ON SCHEMA` | `ALTER` 권한 | 개체 또는 개체에 대한 `DROP` 권한을 소유하고 있습니다. |
| **실행 모니터링** | Workspace 기여자 또는 권한(`queryinsights.exec_requests_history`) 이상 | `CONTROL` 권한 | `EXPLAIN` 문을 사용하는 데 필요한 권한이 없습니다. |
| **데이터를 쓰는 중** | `INSERT` 및/또는 `UPDATE ON OBJECT` | `INSERT` 및 `UPDATE` 권한 | `INSERT` 및 `UPDATE` 권한 |
| **테이블에 데이터 로드** | `SELECT ON OBJECT` 및 `INSERT ON OBJECT` | `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` 및 `ALTER` 권한 | 테이블의 `INSERT` 권한, 스키마의 `USAGE` 권한 |
| **클라이언트 데이터에 액세스** | `SELECT ON OBJECT` | `SELECT` 권한 | `SELECT` 권한 |
| **메타데이터에 액세스** | `SELECT ON INFORMATION_SCHEMA` | 표를 설명하는 데 필요한 권한이 없습니다. | `USAGE ON SCHEMA`, `SELECT on TABLE` 및 테이블 `v_catalog.columns` 및 `v_catalog.view_columns`에 대한 권한도 |
