---
title: Gestion des groupes dans Exchange Online Protection (EOP)
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs dans les organisations Exchange Online Protection (EOP) autonomes peuvent apprendre à créer, modifier et supprimer des groupes de distribution et des groupes de sécurité à extension messagerie dans le centre d’administration Exchange et dans Exchange Online Protection (EOP) autonome.
ms.openlocfilehash: a395c0738093a00c0225aea22a6e556863eebee5
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201876"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="1f9e5-103">Gestion des groupes dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="1f9e5-103">Manage groups in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="1f9e5-104">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez créer, modifier et supprimer les types de groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-104">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can create, modify, and remove the following types of groups:</span></span>

- <span data-ttu-id="1f9e5-105">**Groupes de distribution**: collection d’utilisateurs de messagerie ou d’autres groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-105">**Distribution groups**: A collection of mail users or other distribution groups.</span></span> <span data-ttu-id="1f9e5-106">Par exemple, les équipes ou autres groupes ad hoc qui doivent recevoir ou envoyer des courriers électroniques dans un domaine d’intérêt commun.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-106">For example, teams or other ad hoc groups who need to receive or send email in a common area of interest.</span></span> <span data-ttu-id="1f9e5-107">Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques et ne sont pas des principaux de sécurité (ils ne peuvent pas avoir d’autorisations associées).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-107">Distribution groups are exclusively for distributing email messages, and are not security principals (they can't have permissions assigned to them).</span></span>

- <span data-ttu-id="1f9e5-108">**Groupes de sécurité à extension messagerie**: collection d’utilisateurs de messagerie et d’autres groupes de sécurité qui ont besoin d’autorisations d’accès pour les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-108">**Mail-enabled security groups**: A collection of mail users and other security groups who need access permissions for admin roles.</span></span> <span data-ttu-id="1f9e5-109">Par exemple, vous pouvez accorder à un groupe spécifique d’utilisateurs des autorisations d’administrateur afin qu’ils puissent configurer les paramètres de blocage du courrier indésirable et des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-109">For example, you might want to give specific group of users admin permissions so they can configure anti-spam and anti-malware settings.</span></span>

    > [!NOTE]
    >
    > - <span data-ttu-id="1f9e5-110">Par défaut, les nouveaux groupes de sécurité à extension messagerie refusent les messages provenant d’expéditeurs externes (non authentifiés).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-110">By default, new mail-enabled security groups reject messages from external (unauthenticated) senders.</span></span>
    >
    > - <span data-ttu-id="1f9e5-111">N’ajoutez pas de groupes de distribution aux groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-111">Don't add distribution groups to mail-enabled security groups.</span></span>

<span data-ttu-id="1f9e5-112">Vous pouvez gérer les groupes dans le centre d’administration Exchange (Centre d’administration Exchange) et dans la version PowerShell d’EOP autonome.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-112">You can manage groups in the Exchange admin center (EAC) and in standalone EOP PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1f9e5-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1f9e5-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1f9e5-114">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-114">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="1f9e5-115">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-115">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="1f9e5-116">Lorsque vous gérez des groupes dans une version autonome d’EOP PowerShell, il se peut que vous rencontriez une limitation.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-116">When you manage groups in standalone EOP PowerShell, you might encounter throttling.</span></span> <span data-ttu-id="1f9e5-117">Les procédures PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-117">The PowerShell procedures in this topic use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="1f9e5-118">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-118">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="1f9e5-119">Plus précisément, vous avez besoin du rôle groupes de distribution, qui est affecté aux groupes de rôles OrganizationManagement (administrateurs globaux) et RecipientManagement par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-119">Specifically, you need the Distribution Groups role, which is assigned to the OrganizationManagement (global admins) and RecipientManagement role groups by default.</span></span> <span data-ttu-id="1f9e5-120">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-120">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="1f9e5-121">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-121">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="1f9e5-122">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="1f9e5-122">Having problems?</span></span> <span data-ttu-id="1f9e5-123">Demandez de l’aide dans le Forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-123">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-exchange-admin-center-to-manage-distribution-groups"></a><span data-ttu-id="1f9e5-124">Utiliser le centre d’administration Exchange pour gérer les groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="1f9e5-124">Use the Exchange admin center to manage distribution groups</span></span>

### <a name="use-the-eac-to-create-groups"></a><span data-ttu-id="1f9e5-125">Utiliser le centre d’administration Exchange pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-125">Use the EAC to create groups</span></span>

1. <span data-ttu-id="1f9e5-126">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-126">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="1f9e5-127">Cliquez sur **nouvelle** ![ icône ](../../media/ITPro-EAC-AddIcon.png) , puis sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-127">Click **New** ![New icon](../../media/ITPro-EAC-AddIcon.png), and then select one of the following options:</span></span>

   - <span data-ttu-id="1f9e5-128">**Groupe de distribution**</span><span class="sxs-lookup"><span data-stu-id="1f9e5-128">**Distribution group**</span></span>

   - <span data-ttu-id="1f9e5-129">**Groupe de sécurité à extension messagerie**</span><span class="sxs-lookup"><span data-stu-id="1f9e5-129">**Mail-enabled security group**</span></span>

3. <span data-ttu-id="1f9e5-130">Dans la page nouveau groupe qui s’ouvre, configurez les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-130">In the new group page that opens, configure the following settings.</span></span> <span data-ttu-id="1f9e5-131">Les paramètres marqués par un <sup>\*</sup> sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-131">Settings marked with an <sup>\*</sup> are required.</span></span>

   - <span data-ttu-id="1f9e5-132"><sup>\*</sup>**Nom d’affichage**: ce nom s’affiche dans le carnet d’adresses de votre organisation, sur la ligne à : quand un message électronique est envoyé à ce groupe, et dans la liste **groupes** du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-132"><sup>\*</sup>**Display name**: This name appears in your organization's address book, on the To: line when email is sent to this group, and in the **Groups** list in the EAC.</span></span> <span data-ttu-id="1f9e5-133">Le nom complet est obligatoire, doit être unique et doit être convivial afin que les utilisateurs puissent reconnaître ce qu’il est.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-133">The display name is required, must be unique, and should be user-friendly so people recognize what it is.</span></span>

   - <span data-ttu-id="1f9e5-134"><sup>\*</sup>**Alias**: ce champ permet de taper le nom de l’alias du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-134"><sup>\*</sup>**Alias**: Use this box to type the name of the alias for the group.</span></span> <span data-ttu-id="1f9e5-135">L’alias ne peut pas dépasser 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-135">The alias can't exceed 64 characters and must be unique.</span></span> <span data-ttu-id="1f9e5-136">Lorsqu’un utilisateur tape l’alias dans la ligne à d’un message électronique, il est résolu en nom complet du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-136">When a user types the alias in the To line of an email message, it resolves to the group's display name.</span></span>

   - <span data-ttu-id="1f9e5-137"><sup>\*</sup>**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole arobase (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-137"><sup>\*</sup>**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="1f9e5-138">Par défaut, la valeur d' **alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-138">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="1f9e5-139">Pour la valeur Domain (domaine), cliquez sur le menu déroulant et sélectionnez le domaine accepté dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-139">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

   - <span data-ttu-id="1f9e5-140">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet d’informations du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-140">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

   - <span data-ttu-id="1f9e5-141"><sup>\*</sup>**Propriétaires**: un propriétaire de groupe peut gérer l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-141"><sup>\*</sup>**Owners**: A group owner can manage group membership.</span></span> <span data-ttu-id="1f9e5-142">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-142">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="1f9e5-143">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-143">All groups must have at least one owner.</span></span>

     <span data-ttu-id="1f9e5-144">Pour ajouter des propriétaires, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-144">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="1f9e5-145">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-145">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="1f9e5-146">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-146">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="1f9e5-147">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-147">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="1f9e5-148">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-148">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

   - <span data-ttu-id="1f9e5-149">**Membres**: ajouter et supprimer des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-149">**Members**: Add and remove group members.</span></span>

     <span data-ttu-id="1f9e5-150">Pour ajouter des membres, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-150">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="1f9e5-151">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-151">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="1f9e5-152">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-152">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="1f9e5-153">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-153">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="1f9e5-154">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-154">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

4. <span data-ttu-id="1f9e5-155">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-155">When you're finished, click **Save** to create the distribution group.</span></span>

### <a name="use-the-eac-to-modify-distribution-groups"></a><span data-ttu-id="1f9e5-156">Utiliser le centre d’administration Exchange pour modifier des groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="1f9e5-156">Use the EAC to modify distribution groups</span></span>

1. <span data-ttu-id="1f9e5-157">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-157">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="1f9e5-158">Dans la liste des groupes, sélectionnez le groupe de distribution ou le groupe de sécurité à extension messagerie à modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-158">In the list of groups, select the distribution group or mail-enabled security group that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

3. <span data-ttu-id="1f9e5-159">Dans la page des propriétés du groupe de distribution qui s’ouvre, cliquez sur l’un des onglets suivants pour afficher ou modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-159">On the distribution group properties page that opens, click one of the following tabs to view or change properties.</span></span>

   <span data-ttu-id="1f9e5-160">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-160">When you're finished, click **Save**.</span></span>

#### <a name="general"></a><span data-ttu-id="1f9e5-161">Général</span><span class="sxs-lookup"><span data-stu-id="1f9e5-161">General</span></span>

<span data-ttu-id="1f9e5-162">Utilisez cet onglet pour afficher ou modifier les informations de base relatives au groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-162">Use this tab to view or change basic information about the group.</span></span>

- <span data-ttu-id="1f9e5-163">**Nom d’affichage**: ce nom s’affiche dans le carnet d’adresses, sur la ligne à lorsque le courrier électronique est envoyé à ce groupe, et dans la **Liste groupes**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-163">**Display name**: This name appears in the address book, on the To line when email is sent to this group, and in the **Groups list**.</span></span> <span data-ttu-id="1f9e5-164">Le nom d'affichage est obligatoire et doit être convivial afin que les personnes identifient facilement de quoi il s'agit.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-164">The display name is required and should be user-friendly so people recognize what it is.</span></span> <span data-ttu-id="1f9e5-165">Il doit également être unique dans votre domaine.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-165">It also has to be unique in your domain.</span></span>

  <span data-ttu-id="1f9e5-166">Si vous avez implémenté une stratégie de noms de groupes, le nom d'affichage doit se conformer au format de nom défini par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-166">If you've implemented a group naming policy, the display name has to conform to the naming format defined by the policy.</span></span>

- <span data-ttu-id="1f9e5-167">**Alias**: il s’agit de la partie de l’adresse de messagerie qui apparaît à gauche du symbole arobase (@).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-167">**Alias**: This is the portion of the email address that appears to the left of the at (@) symbol.</span></span> <span data-ttu-id="1f9e5-168">Si vous modifiez l'alias, l'adresse SMTP principale du groupe est également modifiée et contient le nouvel alias.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-168">If you change the alias, the primary SMTP address for the group will also be changed, and contain the new alias.</span></span> <span data-ttu-id="1f9e5-169">De plus, l'adresse de messagerie électronique qui comprend l'alias précédent est gardée en tant qu'adresse de proxy du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-169">Also, the email address with the previous alias will be kept as a proxy address for the group.</span></span>

- <span data-ttu-id="1f9e5-170">**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole arobase (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-170">**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="1f9e5-171">Par défaut, la valeur d' **alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-171">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="1f9e5-172">Pour la valeur Domain (domaine), cliquez sur le menu déroulant et sélectionnez le domaine accepté dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-172">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

- <span data-ttu-id="1f9e5-173">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet d’informations du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-173">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

#### <a name="ownership"></a><span data-ttu-id="1f9e5-174">Propriété</span><span class="sxs-lookup"><span data-stu-id="1f9e5-174">Ownership</span></span>

<span data-ttu-id="1f9e5-175">Utilisez cet onglet pour affecter des propriétaires de groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-175">Use this tab to assign group owners.</span></span> <span data-ttu-id="1f9e5-176">Un propriétaire de groupe peut gérer l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-176">A group owner can manage group membership.</span></span> <span data-ttu-id="1f9e5-177">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-177">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="1f9e5-178">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-178">All groups must have at least one owner.</span></span>

<span data-ttu-id="1f9e5-179">Pour ajouter des propriétaires, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-179">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="1f9e5-180">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-180">In the dialog that appears, find and select a recipient, and then click **add ->**.</span></span> <span data-ttu-id="1f9e5-181">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-181">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="1f9e5-182">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-182">When you're finished, click **OK**.</span></span>

<span data-ttu-id="1f9e5-183">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-183">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

#### <a name="membership"></a><span data-ttu-id="1f9e5-184">Appartenance</span><span class="sxs-lookup"><span data-stu-id="1f9e5-184">Membership</span></span>

<span data-ttu-id="1f9e5-185">Utilisez cet onglet pour ajouter ou supprimer des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-185">Use this tab to add or remove group members.</span></span> <span data-ttu-id="1f9e5-186">Les propriétaires de groupe n’ont pas besoin d’être membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-186">Group owners don't need to be members of the group.</span></span>

<span data-ttu-id="1f9e5-187">Pour ajouter des membres, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-187">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="1f9e5-188">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-188">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="1f9e5-189">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-189">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="1f9e5-190">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-190">When you're finished, click **OK**.</span></span>

<span data-ttu-id="1f9e5-191">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-191">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

### <a name="use-the-eac-to-remove-groups"></a><span data-ttu-id="1f9e5-192">Utiliser le centre d’administration Exchange pour supprimer des groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-192">Use the EAC to remove groups</span></span>

1. <span data-ttu-id="1f9e5-193">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-193">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="1f9e5-194">Dans la liste des groupes, sélectionnez le groupe de distribution que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-194">In the list of groups, select the distribution group that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

## <a name="use-powershell-to-manage-groups"></a><span data-ttu-id="1f9e5-195">Utiliser PowerShell pour gérer les groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-195">Use PowerShell to manage groups</span></span>

### <a name="use-standalone-eop-powershell-to-view-groups"></a><span data-ttu-id="1f9e5-196">Utilisation d’EOP PowerShell autonome pour afficher des groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-196">Use standalone EOP PowerShell to view groups</span></span>

<span data-ttu-id="1f9e5-197">Pour renvoyer une liste récapitulative de tous les groupes de distribution et des groupes de sécurité à extension messagerie dans la version autonome d’EOP PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-197">To return a summary list of all distribution groups and mail-enabled security groups in standalone EOP PowerShell, run the following command:</span></span>

```powershell
Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
```

<span data-ttu-id="1f9e5-198">Pour renvoyer la liste des membres du groupe, remplacez \<GroupIdentity\> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-198">To return the list of group members, replace \<GroupIdentity\> with the name, alias, or email address of the group, and run the following command:</span></span>

```powershell
Get-DistributionGroupMember -Identity <GroupIdentity>
```

<span data-ttu-id="1f9e5-199">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) et [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/get-distributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-199">For detailed syntax and parameter information, see [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) and [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/get-distributiongroupmember).</span></span>

### <a name="use-standalone-eop-powershell-to-create-groups"></a><span data-ttu-id="1f9e5-200">Utilisation d’EOP PowerShell autonome pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-200">Use standalone EOP PowerShell to create groups</span></span>

<span data-ttu-id="1f9e5-201">Pour créer des groupes de distribution ou des groupes de sécurité à extension messagerie dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-201">To create distribution groups or mail-enabled security groups in standalone EOP PowerShell, use the following syntax:</span></span>

```PowerShell
New-EOPDistributionGroup -Name "<Unique Name>" -ManagedBy @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">) [-Alias <text>] [-DisplayName "<Descriptive Name>"] [-Members @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">)] [-Notes "<Optional Text>"] [-PrimarySmtpAddress <SmtpAddress>] [-Type <Distribution | Security>]
```

<span data-ttu-id="1f9e5-202">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-202">**Notes**:</span></span>

- <span data-ttu-id="1f9e5-203">Le paramètre _Name_ est obligatoire, sa longueur maximale est de 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-203">The _Name_ parameter is required, has a maximum length of 64 characters, and must be unique.</span></span> <span data-ttu-id="1f9e5-204">Si vous n’utilisez pas le paramètre _DisplayName_, la valeur du paramètre _Name_ est utilisée pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-204">If you don't use the _DisplayName_ parameter, the value of the _Name_ parameter is used for the display name.</span></span>

- <span data-ttu-id="1f9e5-205">Si vous n’utilisez pas le paramètre _alias_ , le paramètre _Name_ est utilisé pour la valeur alias.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-205">If you don't use the _Alias_ parameter, the _Name_ parameter is used for the alias value.</span></span> <span data-ttu-id="1f9e5-206">Les espaces sont supprimés et les caractères non pris en charge sont convertis en points d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-206">Spaces are removed and unsupported characters are converted to question marks (?).</span></span>

- <span data-ttu-id="1f9e5-207">Si vous n’utilisez pas le paramètre _PrimarySmtpAddress_ , la valeur d’alias est utilisée dans le paramètre _PrimarySmtpAddress_ .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-207">If you don't use the _PrimarySmtpAddress_ parameter, the alias value is used in the _PrimarySmtpAddress_ parameter.</span></span>

- <span data-ttu-id="1f9e5-208">Si vous n’utilisez pas le paramètre _type_ , la valeur par défaut est distribution.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-208">If you don't use the _Type_ parameter, the default value is Distribution.</span></span>

<span data-ttu-id="1f9e5-209">Cet exemple crée un groupe de distribution nommé administrateurs informatiques avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-209">This example creates a distribution group named IT Administrators with the specified properties.</span></span>

```PowerShell
New-EOPDistributionGroup -Name "IT Administrators" -Alias itadmin -Members @("michelle@contoso.com","laura@contoso.com","julia@contoso.com") -ManagedBy "chris@contoso.com"
```

<span data-ttu-id="1f9e5-210">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/New-EOPDistributionGroup).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-210">For detailed syntax and parameter information, see [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/New-EOPDistributionGroup).</span></span>

### <a name="use-standalone-eop-powershell-to-modify-groups"></a><span data-ttu-id="1f9e5-211">Utilisation d’EOP PowerShell autonome pour modifier des groupes</span><span class="sxs-lookup"><span data-stu-id="1f9e5-211">Use standalone EOP PowerShell to modify groups</span></span>

<span data-ttu-id="1f9e5-212">Pour modifier des groupes dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-212">To modify groups in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
Set-EOPDistributionGroup -Identity <GroupIdentity> [-Alias <Text>] [-DisplayName <Text>] [-ManagedBy @("User1","User2",..."UserN")] [-PrimarySmtpAddress <SmtpAddress>]

```powershell
Update-EOPDistributionGroupMember -Identity <GroupIdentity> -Members @("User1","User2",..."UserN")
```

<span data-ttu-id="1f9e5-213">Cet exemple utilise la modification de l’adresse SMTP principale (également appelée adresse de réponse) pour le groupe Seattle Employees vers sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-213">This example uses changes the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span>

```PowerShell
Set-EOPDistributionGroup "Seattle Employees" -PrimarySmtpAddress "sea.employees@contoso.com"
```

<span data-ttu-id="1f9e5-214">Cet exemple remplace les membres actuels du groupe d’équipe de sécurité par Kitty Petersen et Tyson Fawcett.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-214">This example replaces the current members of the Security Team group with Kitty Petersen and Tyson Fawcett.</span></span>

```powershell
Update-EOPDistributionGroupMember -Identity "Security Team" -Members @("Kitty Petersen","Tyson Fawcett")
```

<span data-ttu-id="1f9e5-215">Cet exemple ajoute un nouvel utilisateur appelé Tyson Fawcett au groupe nommé « équipe de sécurité » tout en conservant les membres actuels du groupe.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-215">This example adds a new user named Tyson Fawcett to the group named Security Team while preserving the current members of the group.</span></span>

```powershell
$CurrentMemberObjects = Get-DistributionGroupMember "Security Team"
$CurrentMemberNames = $CurrentMemberObjects | % {$_.name}
$CurrentMemberNames += "Tyson Fawcett"
Update-EOPDistributionGroupMember -Identity "Security Team" -Members $CurrentMemberNames
```

<span data-ttu-id="1f9e5-216">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/set-eopdistributiongroup) et [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/update-eopdistributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-216">For detailed syntax and parameter information, see [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/set-eopdistributiongroup) and [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/update-eopdistributiongroupmember).</span></span>

### <a name="remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="1f9e5-217">Supprimer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="1f9e5-217">Remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="1f9e5-218">Cet exemple utilise le groupe de distribution nommé administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-218">This example uses removes the distribution group named IT Administrators.</span></span>

```PowerShell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

<span data-ttu-id="1f9e5-219">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/remove-eopdistributiongroup).</span><span class="sxs-lookup"><span data-stu-id="1f9e5-219">For detailed syntax and parameter information, see [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/remove-eopdistributiongroup).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="1f9e5-220">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="1f9e5-220">How do you know these procedures worked?</span></span>

<span data-ttu-id="1f9e5-221">Pour vérifier que vous avez bien créé, modifié ou supprimé un groupe de distribution ou un groupe de sécurité à extension messagerie, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-221">To verify that you've successfully created, modified, or removed a distribution group or a mail-enabled security group, do any of the following steps:</span></span>

- <span data-ttu-id="1f9e5-222">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-222">In the EAC, go to **Recipients** \> **Groups**.</span></span> <span data-ttu-id="1f9e5-223">Vérifiez que le groupe est affiché (ou non), puis vérifiez la valeur du **type de groupe** .</span><span class="sxs-lookup"><span data-stu-id="1f9e5-223">Verify that the group is listed (or not listed), and verify the **Group Type** value.</span></span> <span data-ttu-id="1f9e5-224">Sélectionnez le groupe et affichez les informations dans le volet d’informations, ou cliquez sur **modifier** ![ l’icône modifier ](../../media/ITPro-EAC-AddIcon.png) pour afficher les paramètres.</span><span class="sxs-lookup"><span data-stu-id="1f9e5-224">Select the group and view the information in the Details pane, or click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png) to view the settings.</span></span>

- <span data-ttu-id="1f9e5-225">Dans la version autonome d’EOP PowerShell, exécutez la commande suivante pour vérifier que le groupe est affiché (ou non) :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-225">In standalone EOP PowerShell, run the following command to verify the group is listed (or isn't listed):</span></span>

  ```PowerShell
  Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
  ```

- <span data-ttu-id="1f9e5-226">Remplacez \<GroupIdentity\> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-226">Replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command to verify the settings:</span></span>

  ```PowerShell
  Get-Recipient -Identity <GroupIdentity> | Format-List
  ```

- <span data-ttu-id="1f9e5-227">Pour afficher les membres du groupe, remplacez \<GroupIdentity\> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1f9e5-227">To view the group members, replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command:</span></span>

  ```PowerShell
  Get-DistributionGroupMember -Identity "<GroupIdentity>"
  ```
