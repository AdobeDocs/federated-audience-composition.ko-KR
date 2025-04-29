---
title: 외부 데이터베이스 액세스 권한
description: 각 데이터베이스 엔진에 대한 권한에 대해 알아봅니다.
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 3%

---

# FDA 권한 지표 {#fda-rights}

아래 표는 사용자가 FDA를 통해 외부 데이터베이스에서 작업을 수행할 수 있도록 각 시스템에 필요한 데이터베이스 권한을 간략하게 설명합니다.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **원격 데이터베이스에 연결** | 웨어하우스 사용량, 데이터베이스 사용량 및 스키마 권한 사용량 | AWS 계정에 연결된 사용자 만들기 | 서비스 계정 만들기 및 프로젝트에 대한 사용자 액세스 권한 부여 | 카탈로그에 대한 USE CATALOG 권한과 SQL Warehouse에 대한 CAN_USE 권한 |
| **표 만들기** | 스키마 권한에 대한 테이블 생성 | 권한 만들기 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create 및 bigquery.tables.create 권한이 포함되어야 합니다. | SCHEMA 권한 및 CREATE TABLE 권한 사용 |
| **인덱스 만들기** | N/A | 권한 만들기 | BigQuery는 검색 인덱스만 지원합니다. 서비스 계정에 할당된 역할에는 bigquery.jobs.create, bigquery.tables.getData 및 bigquery.tables.createIndex 권한이 포함되어야 합니다. | N/A |
| **함수 만들기** | 스키마 권한에 대한 함수 만들기 | 외부 python 스크립트를 호출할 수 있는 USAGE ON LANGUAGE plpythonu 권한 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create 및 bigquery.routines.create 권한이 포함되어야 합니다. | CREATE FUNCTION 권한 |
| **프로시저 만들기** | N/A | 외부 python 스크립트를 호출할 수 있는 USAGE ON LANGUAGE plpythonu 권한 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create 및 bigquery.routines.create 권한이 포함되어야 합니다. |  해당 사항 없음 |
| **개체(테이블, 인덱스, 함수, 프로시저) 제거** | 객체 소유 | 개체 소유 또는 수퍼유저 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete 및 bigquery.tables.deleteIndex 권한이 포함되어야 합니다. |
| **실행 모니터링** | 필수 개체에 대한 MONITOR 권한 | EXPLAIN 명령을 사용하는 데 필요한 권한이 없습니다. | monitoring.viewer 역할 | CAN_VIEW 권한 |
| **데이터를 쓰는 중** | INSERT 및/또는 UPDATE 권한(쓰기 작업에 따라 다름) | INSERT 및 UPDATE 권한 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create 및 bigquery.tables.updateData가 포함되어야 합니다. |  권한 수정 |
| **테이블에 데이터 로드** | 스키마에 단계 생성, 대상 테이블에 선택 및 삽입 권한 | SELECT 및 INSERT 권한 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create, bigquery.tables.getData 및 bigquery.tables.updateData가 포함되어야 합니다. | 권한 선택 및 수정 |
| **클라이언트 데이터에 액세스** | (향후) 테이블 또는 뷰 권한 선택 | 권한 선택 | 서비스 계정에 할당된 역할에는 bigquery.jobs.create 및 bigquery.tables.getData for tables 또는 bigquery.dataViewer 역할이 포함되어야 합니다. |  권한 선택 |
| **메타데이터에 액세스** | INFORMATION_SCHEMA 스키마 권한 선택 | 권한 선택 | bigquery.metadataViewer 역할 |  INFORMATION_SCHEMA 스키마 권한 선택 |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **원격 데이터베이스에 연결** | 읽기(기본값) 권한 | CONNECT 권한 | 권한 필요 없음 |
| **표 만들기** | 데이터베이스(웨어하우스)에서 테이블 만들기 및 ALTER ON 스키마 | 테이블 만들기 권한 | 스키마 권한 만들기 |
| **인덱스 만들기** | N/A | ALTER 권한 | N/A |
| **함수 만들기** | N/A | 함수 만들기 권한 | 스키마 권한 만들기 |
| **프로시저 만들기** | 데이터베이스(웨어하우스)에서 프로시저 만들기 및 ALTER ON 스키마 | 프로시저 만들기 권한 | 스키마 권한 만들기 |
| **개체(테이블, 인덱스, 함수, 프로시저) 제거** | ALTER ON 스키마 | ALTER 권한 | 객체 또는 객체에 대한 DROP 권한 소유 |
| **실행 모니터링** | Workspace 기여자 또는 권한 이상(queryinsights.exec_requests_history)  | 제어 권한 | EXPLAIN 문을 사용하는 데 필요한 권한이 없습니다. |
| **데이터를 쓰는 중** | 오브젝트에 삽입 및/또는 업데이트 | 권한 삽입 및 업데이트 | INSERT 및 UPDATE 권한 |
| **테이블에 데이터 로드** | [오브젝트]에서 선택 후 [오브젝트]에 삽입 | 테이블 만들기, 실행, 선택, 삽입, 업데이트, 권한 변경 | 테이블에 대한 INSERT 권한, 스키마에 대한 USAGE 권한 |
| **클라이언트 데이터에 액세스** | 개체에서 선택 | 권한 선택 | 권한 선택 |
| **메타데이터에 액세스** | INFORMATION_SCHEMA 선택 | 표를 설명하는 데 필요한 권한이 없습니다. | 스키마에 사용, 테이블에 대한 SELECT 및 테이블 v_catalog.columns 및 v_catalog.view_columns에 대한 권한 |
