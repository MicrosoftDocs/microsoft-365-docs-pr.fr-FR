---
title: Octroi de l’accès au Centre de conformité et sécurité aux utilisateurs
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: how-to
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Les utilisateurs doivent disposer d’autorisations dans le centre de conformité Microsoft 365 Security & pour pouvoir gérer les fonctionnalités de sécurité ou de conformité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 1bf8da85a0e090a9d74934ea5084f547d6a8794f
ms.sourcegitcommit: ee39faf3507d0edc9497117b3b2854955c959c6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49616607"
---
# <a name="give-users-access-to-the-security--compliance-center"></a><span data-ttu-id="b2c09-103">Octroi de l’accès au Centre de conformité et sécurité aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b2c09-103">Give users access to the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="b2c09-104">Les utilisateurs doivent disposer d’autorisations dans le centre de conformité & de sécurité avant de pouvoir gérer les fonctionnalités de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="b2c09-104">Users need to be assigned permissions in the Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="b2c09-105">En tant qu’administrateur général ou membre du groupe de rôles OrganizationManagement dans le centre de sécurité & conformité, vous pouvez accorder ces autorisations aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b2c09-105">As a global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="b2c09-106">Ceux-ci pourront uniquement gérer les fonctionnalités de sécurité ou de conformité auxquelles vous leur donnez accès.</span><span class="sxs-lookup"><span data-stu-id="b2c09-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span>

<span data-ttu-id="b2c09-107">Pour plus d’informations sur les différentes autorisations que vous pouvez accorder aux utilisateurs dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b2c09-107">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b2c09-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b2c09-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b2c09-109">Vous devez être un administrateur général ou un membre du groupe de rôles OrganizationManagement dans le centre de sécurité & Compliance Center pour effectuer les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b2c09-109">You need to be a global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="b2c09-110">Les groupes de rôles pour le centre de sécurité & conformité peuvent avoir des noms similaires aux groupes de rôles dans Exchange Online, mais ils ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="b2c09-110">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="b2c09-111">Les appartenances aux groupes de rôles ne sont pas partagées entre Exchange Online et le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b2c09-111">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="b2c09-112">Les autorisations des partenaires DAP (Delegated Access permission) avec administrer de la part de (administrateur) ne peuvent pas accéder au centre de conformité &.</span><span class="sxs-lookup"><span data-stu-id="b2c09-112">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-security--compliance-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="b2c09-113">Utiliser le centre de sécurité & conformité pour accorder à un autre utilisateur l’accès au centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="b2c09-113">Use the Security & Compliance Center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="b2c09-114">Ouvrez le centre de sécurité & conformité à l’adresse <https://protection.office.com> , puis accédez à **autorisations**.</span><span class="sxs-lookup"><span data-stu-id="b2c09-114">Open the Security & Compliance Center at <https://protection.office.com> and then go to **Permissions**.</span></span> <span data-ttu-id="b2c09-115">Pour accéder directement à l’onglet **autorisations** , ouvrez <https://protection.office.com/permissions> .</span><span class="sxs-lookup"><span data-stu-id="b2c09-115">To go directly to the **Permissions** tab, open <https://protection.office.com/permissions>.</span></span>

2. <span data-ttu-id="b2c09-116">Dans la liste des groupes de rôles, sélectionnez le groupe de rôles, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/O365-MDM-CreatePolicy-EditIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b2c09-116">From the list of role groups, choose the role group, and then click **Edit** ![Edit icon](../../media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

3. <span data-ttu-id="b2c09-117">Dans la page des propriétés du groupe de rôles sous **membres**, cliquez sur **Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.gif) et sélectionnez le nom de l’utilisateur (ou des utilisateurs) que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="b2c09-117">In the role group's properties page under **Members**, click **Add**![Add Icon](../../media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

4. <span data-ttu-id="b2c09-118">Une fois que vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur **ajouter- \>** puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2c09-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

5. <span data-ttu-id="b2c09-119">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b2c09-119">When you're finished, click **Save**.</span></span>

## <a name="use-security--compliance-center-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="b2c09-120">Utiliser la sécurité & Centre de conformité PowerShell pour accorder à un autre utilisateur l’accès au centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="b2c09-120">Use Security & Compliance Center PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="b2c09-121">[Connectez-vous au Centre de conformité et sécurité PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="b2c09-121">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="b2c09-122">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b2c09-122">Use the following syntax:</span></span>

   ```powershell
   Add-RoleGroupMember -Identity <RoleGroup> -Member <UserIdentity>

   - _Identity_ is the role group.
   - _Member_ is the user or universal security group (USG). You can specify only one member at a time.

   This example adds MatildaS to the Organization Management role group.

   ```PowerShell
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

<span data-ttu-id="b2c09-123">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Add-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/add-rolegroupmember)</span><span class="sxs-lookup"><span data-stu-id="b2c09-123">For detailed syntax and parameter issues, see [Add-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/add-rolegroupmember)</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="b2c09-124">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="b2c09-124">How do you know this worked?</span></span>

<span data-ttu-id="b2c09-125">Pour vérifier que vous avez bien autorisé l’accès au centre de sécurité & conformité, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2c09-125">To verify that you've successfully granted access to the Security & Compliance Center, do either of the following steps:</span></span>

- <span data-ttu-id="b2c09-126">Dans le centre de sécurité & conformité, accédez à **autorisations** et sélectionnez le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="b2c09-126">In the Security & Compliance Center, go to **Permissions** and select the role group.</span></span> <span data-ttu-id="b2c09-127">Dans la fenêtre mobile des détails qui s’ouvre, vérifiez les membres du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="b2c09-127">In the details flyout that opens, verify the members of the role group.</span></span>

- <span data-ttu-id="b2c09-128">Dans sécurité & Centre de conformité PowerShell, remplacez \<RoleGroupName\> par le nom du groupe de rôles, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b2c09-128">In Security & Compliance Center PowerShell, replace \<RoleGroupName\> with the name of the role group, and run the following command:</span></span>

  ```powershell
  Get-RoleGroupMember -Identity "<RoleGroupName>"
  ```

  <span data-ttu-id="b2c09-129">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroupMember).</span><span class="sxs-lookup"><span data-stu-id="b2c09-129">For detailed syntax and parameter information, see [Get-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroupMember).</span></span>
