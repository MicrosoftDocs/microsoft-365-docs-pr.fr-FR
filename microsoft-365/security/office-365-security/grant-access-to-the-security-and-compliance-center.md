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
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Des autorisations doivent être attribuées aux utilisateurs dans le Centre de conformité et sécurité Microsoft 365 & avant de pouvoir gérer l’une de ses fonctionnalités de sécurité ou de conformité.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: e1a619b184c575e3750b2499adc661627b4d27d6
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289876"
---
# <a name="give-users-access-to-the-security--compliance-center"></a><span data-ttu-id="9d8de-103">Octroi de l’accès au Centre de conformité et sécurité aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9d8de-103">Give users access to the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="9d8de-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9d8de-104">**Applies to**</span></span>
- [<span data-ttu-id="9d8de-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="9d8de-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="9d8de-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="9d8de-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="9d8de-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9d8de-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="9d8de-108">Des autorisations doivent être attribuées aux utilisateurs dans le Centre de sécurité & conformité avant de pouvoir gérer l’une de ses fonctionnalités de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="9d8de-108">Users need to be assigned permissions in the Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="9d8de-109">En tant qu’administrateur global ou membre du groupe de rôles OrganizationManagement dans le Centre de sécurité & conformité, vous pouvez accorder ces autorisations aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9d8de-109">As a global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="9d8de-110">Ceux-ci pourront uniquement gérer les fonctionnalités de sécurité ou de conformité auxquelles vous leur donnez accès.</span><span class="sxs-lookup"><span data-stu-id="9d8de-110">Users will only be able to manage the security or compliance features that you give them access to.</span></span>

<span data-ttu-id="9d8de-111">Pour plus d’informations sur les différentes autorisations que vous pouvez accorder aux utilisateurs dans le Centre de sécurité & conformité, consultez [Autorisations](permissions-in-the-security-and-compliance-center.md)dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="9d8de-111">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9d8de-112">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9d8de-112">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9d8de-113">Vous devez être un administrateur global ou un membre du groupe de rôles OrganizationManagement dans le Centre de sécurité & conformité, pour effectuer les étapes de cet article.</span><span class="sxs-lookup"><span data-stu-id="9d8de-113">You need to be a global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="9d8de-114">Les groupes de rôles pour le Centre de sécurité & conformité peuvent avoir des noms similaires aux groupes de rôles dans Exchange Online, mais ils ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="9d8de-114">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="9d8de-115">Les appartenances aux groupes de rôles ne sont pas partagées entre Exchange Online et le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="9d8de-115">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="9d8de-116">Les partenaires avec autorisation d’accès délégué avec des autorisations Administrer de la part de (AOBO) ne peuvent pas accéder au Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="9d8de-116">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-security--compliance-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="9d8de-117">Utiliser le Centre de sécurité & conformité pour accorder à un autre utilisateur l’accès au Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="9d8de-117">Use the Security & Compliance Center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="9d8de-118">Ouvrez le Centre de sécurité & conformité, puis <https://protection.office.com> allez à **Autorisations.**</span><span class="sxs-lookup"><span data-stu-id="9d8de-118">Open the Security & Compliance Center at <https://protection.office.com> and then go to **Permissions**.</span></span> <span data-ttu-id="9d8de-119">Pour aller directement à **l’onglet Autorisations,** ouvrez <https://protection.office.com/permissions> .</span><span class="sxs-lookup"><span data-stu-id="9d8de-119">To go directly to the **Permissions** tab, open <https://protection.office.com/permissions>.</span></span>

2. <span data-ttu-id="9d8de-120">Dans la liste des groupes de rôles,  choisissez le groupe de rôles, puis cliquez sur Modifier ![ l’icône ](../../media/O365-MDM-CreatePolicy-EditIcon.gif) Modifier.</span><span class="sxs-lookup"><span data-stu-id="9d8de-120">From the list of role groups, choose the role group, and then click **Edit** ![Edit icon](../../media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

3. <span data-ttu-id="9d8de-121">Dans la page des propriétés du groupe de rôles sous **Membres,** cliquez sur Ajouter une icône et sélectionnez le nom de l’utilisateur (ou des ![ utilisateurs) que vous ](../../media/ITPro-EAC-AddIcon.gif) souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="9d8de-121">In the role group's properties page under **Members**, click **Add**![Add Icon](../../media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

4. <span data-ttu-id="9d8de-122">Lorsque vous avez sélectionné tous les utilisateurs que vous souhaitez ajouter au groupe de rôles, cliquez sur **Ajouter, \>** puis **SUR OK.**</span><span class="sxs-lookup"><span data-stu-id="9d8de-122">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

5. <span data-ttu-id="9d8de-123">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9d8de-123">When you're finished, click **Save**.</span></span>

## <a name="use-security--compliance-center-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="9d8de-124">Utiliser le Centre de sécurité & conformité PowerShell pour accorder à un autre utilisateur l’accès au Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="9d8de-124">Use Security & Compliance Center PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="9d8de-125">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="9d8de-125">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="9d8de-126">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9d8de-126">Use the following syntax:</span></span>

   ```powershell
   Add-RoleGroupMember -Identity <RoleGroup> -Member <UserIdentity>

   - _Identity_ is the role group.
   - _Member_ is the user or universal security group (USG). You can specify only one member at a time.

   This example adds MatildaS to the Organization Management role group.

   ```PowerShell
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

<span data-ttu-id="9d8de-127">Pour des problèmes de syntaxe et de paramètres détaillés, voir [Add-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/add-rolegroupmember)</span><span class="sxs-lookup"><span data-stu-id="9d8de-127">For detailed syntax and parameter issues, see [Add-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/add-rolegroupmember)</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="9d8de-128">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="9d8de-128">How do you know this worked?</span></span>

<span data-ttu-id="9d8de-129">Pour vérifier que vous avez bien accordé l’accès au Centre de sécurité & conformité, vous devez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d8de-129">To verify that you've successfully granted access to the Security & Compliance Center, do either of the following steps:</span></span>

- <span data-ttu-id="9d8de-130">Dans le Centre de sécurité & conformité, sélectionnez le groupe de **rôles Autorisations.**</span><span class="sxs-lookup"><span data-stu-id="9d8de-130">In the Security & Compliance Center, go to **Permissions** and select the role group.</span></span> <span data-ttu-id="9d8de-131">Dans le volant d’informations qui s’ouvre, vérifiez les membres du groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9d8de-131">In the details flyout that opens, verify the members of the role group.</span></span>

- <span data-ttu-id="9d8de-132">Dans le Centre & de sécurité PowerShell, remplacez-le par le nom du groupe de rôles \<RoleGroupName\> et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9d8de-132">In Security & Compliance Center PowerShell, replace \<RoleGroupName\> with the name of the role group, and run the following command:</span></span>

  ```powershell
  Get-RoleGroupMember -Identity "<RoleGroupName>"
  ```

  <span data-ttu-id="9d8de-133">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-RoleGroupMember.](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroupMember)</span><span class="sxs-lookup"><span data-stu-id="9d8de-133">For detailed syntax and parameter information, see [Get-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroupMember).</span></span>
