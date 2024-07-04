---
audience: end-user
title: 대상자 저장 활동 사용
description: 대상자 저장 활동을 사용하는 방법 알아보기
source-git-commit: c151cc316eb9b5df6fa1d09f01455313195dfd07
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 12%

---


# 대상자 저장 {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="대상자 저장"
>abstract="이 활동을 사용하여 기존 대상자를 업데이트하거나 컴포지션에서 업스트림으로 계산된 모집단에서 새 대상자를 만듭니다. 생성된 대상자는 대상자 목록에 추가되며 **대상자** 메뉴를 통해 사용할 수 있습니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="아웃바운드 전환 생성"
>abstract="**대상자 저장** 활동 후에 전환을 추가하려면 이 옵션을 사용합니다."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="기본 ID 필드"
>abstract="프로필에 사용할 기본 ID를 선택합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Experience Platform 설명서에서 자세히 알아보기"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="ID 네임스페이스"
>abstract="프로필에 사용할 네임스페이스를 선택합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-platform/identity/features/namespaces" text="Experience Platform 설명서에서 자세히 알아보기"

다음 **대상자 저장** 활동을 사용하면 컴포지션에서 업스트림으로 계산한 모집단에서 기존 대상자를 업데이트하거나 새 대상자를 만들 수 있습니다. 생성된 대상자는 애플리케이션 대상자 목록에 추가되고, 를 통해 사용할 수 있습니다. **대상** 메뉴 아래의 제품에서 사용할 수 있습니다.

이 활동은 기본적으로 모집단 그룹을 재사용 가능한 대상으로 전환하여 동일한 컴포지션에서 계산되도록 하는 데 사용됩니다. 다음과 같은 다른 타겟팅 활동에 연결 **대상자 작성** 또는 **결합** 활동.

## 대상자 저장 활동 구성 {#save-audience-configuration}

다음 단계에 따라 **대상자 저장** 활동:

1. 추가 **대상자 저장** 활동을 컴포지션에 추가합니다.

   ![](../assets/save-audience.png)

1. 만들 대상자의 레이블을 지정합니다.

1. 클릭 **대상 매핑 추가** 그런 다음 소스 및 타겟 대상 필드를 선택합니다.

   * **Source 대상 필드**:
   * **타겟 대상 필드**:

   작업을 반복하여 필요한 만큼 대상 매핑을 추가합니다.

1. 데이터베이스에서 타겟팅된 프로필을 식별하는 데 사용할 기본 ID 및 네임스페이스를 선택하십시오.

   * **기본 ID 필드**: 프로필을 식별하는 데 사용할 필드를 선택합니다. 예를 들어 이메일 주소나 전화번호 등이 있습니다.
   * **ID 네임스페이스**: 프로필을 식별하는 데 사용할 네임스페이스(예: 식별 키로 사용할 데이터 유형)를 선택합니다. 예를 들어 이메일 주소가 기본 ID 필드로 선택된 경우 ID 네임스페이스 **이메일** 을 선택해야 합니다. 고유 식별자가 전화번호인 경우 ID 네임스페이스입니다 **전화** 을 선택해야 합니다.

컴포지션을 실행한 후에는 결과 대상자가 Adobe Experience Platform에 저장되고 **대상** 메뉴 아래의 제품에서 사용할 수 있습니다.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
