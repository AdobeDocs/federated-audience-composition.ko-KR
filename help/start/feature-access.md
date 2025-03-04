---
title: 페더레이션된 대상자 구성 액세스
description: 페더레이션된 대상자 구성에 필요한 권한 알아보기
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
hide: true
hidefromtoc: true
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 93%

---

# 페더레이션된 대상자 구성 액세스 {#feature-access}

## 샌드박스에 대한 액세스 관리 {#access-sandboxes}

Adobe Experience Platform Federated Audience Composition을 구매하면 해당 시점의 각 활성 샌드박스에 대해 제품 프로필이 생성됩니다. 이 제품 프로필은 Admin Console의 **Adobe Experience Platform** 제품 카드에서 생성되며 다음 명명 규칙을 따릅니다. `ACP_FAC - <<SandboxName>> - admin.` 특정 샌드박스의 페더레이션된 대상자 구성에 액세스하려면 해당 샌드박스에 대해 생성된 제품 프로필에 사용자를 추가해야 합니다.

예를 들어 “fac-test”라는 새 샌드박스가 활성화되면 해당 제품 프로필 “ACP_FAC - fac-test - admin”이 생성됩니다. 이 샌드박스를 사용하여 페더레이션된 대상자 구성에 액세스하려면 사용자를 이 제품 프로필에 추가해야 합니다.

## 페더레이션된 대상자 구성에 대한 액세스 관리

>[!AVAILABILITY]
>
>사용 권한은 3월 릴리스의 일부로 제공됩니다.

**페더레이션된 대상자 구성**&#x200B;에 액세스하려면 해당 역할에 **페더레이션된 데이터 관리** 권한이 할당되어 있는지 확인해야 합니다. 또한 이러한 역할은 **페더레이션된 대상자 구성**&#x200B;에 액세스해야 하는 사용자에게 할당되어야 합니다.

관리자만 이러한 권한을 할당할 수 있습니다.

1. **[!UICONTROL 사용 권한]** 메뉴로 이동합니다.

1. **[!UICONTROL 역할]** 메뉴에서 업데이트하려는 **[!UICONTROL 역할]**&#x200B;을 선택합니다.

   ![](assets/access_fda_1.png)

1. 역할의 권한을 수정하려면 **[!UICONTROL 편집]**&#x200B;을 클릭합니다.

   ![](assets/access_fda_2.png)

1. **페더레이션된 데이터** 리소스를 추가한 다음 드롭다운 메뉴에서 **[!UICONTROL 페더레이션된 데이터 관리]**&#x200B;를 선택합니다.

   ![](assets/access_fda_3.png)

1. 필요한 변경 내용을 적용한 후 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

이미 이 역할에 할당된 사용자는 권한이 자동으로 업데이트되며, 페더레이션된 대상자 구성에 액세스할 수 있게 됩니다.

새 사용자에게 이 역할을 할당하려면 다음 작업을 수행하십시오.

1. 역할 대시보드 내에서 **[!UICONTROL 사용자]** 탭으로 이동하고 **[!UICONTROL 사용자 추가]**&#x200B;를 클릭합니다.

   ![](assets/access_fda_4.png)

1. 사용자의 이름 또는 이메일 주소를 입력하거나, 사용 가능한 목록에서 선택합니다. 완료되면 **[!UICONTROL 저장]**&#x200B;을 클릭합니다.

그런 다음 사용자는 인스턴스에 액세스하기 위한 지침이 포함된 이메일을 받게 됩니다. 이전에 사용자를 생성하지 않은 경우 [이 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/access-control/abac/permissions-ui/users)를 참조하십시오.
