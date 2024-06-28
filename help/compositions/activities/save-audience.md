---
audience: end-user
title: 대상자 저장 활동 사용
description: 포크 활동 사용 방법 알아보기
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
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

1. 다음에서 **모드** 드롭다운에서 수행할 작업을 선택합니다.

   * **기존 대상자 만들기 또는 업데이트**: 정의 **대상 레이블**. 대상이 이미 있으면 업데이트되고, 그렇지 않으면 새 대상이 만들어집니다.

   * **기존 대상자 업데이트**: 다음을 선택합니다. **대상자** 기존 대상자 목록 중에서 업데이트하려고 합니다.

1. 다음 항목 선택 **업데이트 모드** 기존 대상에 적용되는 사항:

   * **대상 콘텐츠를 새 데이터로 바꾸기**: 모든 대상 콘텐츠가 바뀝니다. 이전 데이터는 손실됩니다. 대상자 저장 활동의 인바운드 전환에서 수집한 데이터만 유지됩니다. 이 옵션은 업데이트한 대상자의 대상자 유형과 타겟팅 차원을 지웁니다.

   * **새 데이터로 대상자 완료**: 이전 대상자 컨텐츠가 유지되고 대상자 저장 활동의 인바운드 전환에서 수집한 데이터가 여기에 추가됩니다.

1. 다음 확인: **아웃바운드 전환 생성** 다음 항목 뒤에 전환을 추가하려면 옵션 **대상자 저장** 활동.

대상자에 대한 세부 사항 보기에서 저장한 대상자의 콘텐츠를 사용할 수 있습니다. 이 뷰에는 다음에서 액세스할 수 있습니다. **대상** 메뉴 아래의 제품에서 사용할 수 있습니다. 이 보기에서 사용할 수 있는 열은 의 인바운드 전환 열에 해당합니다. **대상자 저장** 활동.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
