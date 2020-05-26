---
title: Gestion des groupes dans Exchange Online Protection (EOP)
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs dans les organisations Exchange Online Protection (EOP) autonomes peuvent apprendre à créer, modifier et supprimer des groupes de distribution et des groupes de sécurité à extension messagerie dans le centre d’administration Exchange et dans Exchange Online Protection (EOP) autonome.
ms.openlocfilehash: 4f1dbdb503f8baf02b7dd763dbf7fc6acdf5771a
ms.sourcegitcommit: 40ec697e27b6c9a78f2b679c6f5a8875dacde943
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2020
ms.locfileid: "44352190"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="b765d-103">Gestion des groupes dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="b765d-103">Manage groups in EOP</span></span>

<span data-ttu-id="b765d-104">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez créer, modifier et supprimer les types de groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="b765d-104">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can create, modify, and remove the following types of groups:</span></span>

- <span data-ttu-id="b765d-105">**Groupes de distribution**: collection d’utilisateurs de messagerie ou d’autres groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="b765d-105">**Distribution groups**: A collection of mail users or other distribution groups.</span></span> <span data-ttu-id="b765d-106">Par exemple, les équipes ou autres groupes ad hoc qui doivent recevoir ou envoyer des courriers électroniques dans un domaine d’intérêt commun.</span><span class="sxs-lookup"><span data-stu-id="b765d-106">For example, teams or other ad hoc groups who need to receive or send email in a common area of interest.</span></span> <span data-ttu-id="b765d-107">Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques et ne sont pas des principaux de sécurité (ils ne peuvent pas avoir d’autorisations associées).</span><span class="sxs-lookup"><span data-stu-id="b765d-107">Distribution groups are exclusively for distributing email messages, and are not security principals (they can't have permissions assigned to them).</span></span>

- <span data-ttu-id="b765d-108">**Groupes de sécurité à extension messagerie**: collection d’utilisateurs de messagerie et d’autres groupes de sécurité qui ont besoin d’autorisations d’accès pour les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="b765d-108">**Mail-enabled security groups**: A collection of mail users and other security groups who need access permissions for admin roles.</span></span> <span data-ttu-id="b765d-109">Par exemple, vous pouvez accorder à un groupe spécifique d’utilisateurs des autorisations d’administrateur afin qu’ils puissent configurer les paramètres de blocage du courrier indésirable et des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="b765d-109">For example, you might want to give specific group of users admin permissions so they can configure anti-spam and anti-malware settings.</span></span>

    > [!NOTE]
    > <ul><li><span data-ttu-id="b765d-110">Par défaut, les nouveaux groupes de sécurité à extension messagerie refusent les messages provenant d’expéditeurs externes (non authentifiés).</span><span class="sxs-lookup"><span data-stu-id="b765d-110">By default, new mail-enabled security groups reject messages from external (unauthenticated) senders.</span></span></li><li><span data-ttu-id="b765d-111">N’ajoutez pas de groupes de distribution aux groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="b765d-111">Don't add distribution groups to mail-enabled security groups.</span></span></li></ul><span data-ttu-id="b765d-112">.</span><span class="sxs-lookup"><span data-stu-id="b765d-112">.</span></span>

<span data-ttu-id="b765d-113">Vous pouvez gérer les groupes dans le centre d’administration Exchange (Centre d’administration Exchange) et dans la version PowerShell d’EOP autonome.</span><span class="sxs-lookup"><span data-stu-id="b765d-113">You can manage groups in the Exchange admin center (EAC) and in standalone EOP PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b765d-114">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b765d-114">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b765d-115">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="b765d-115">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="b765d-116">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="b765d-116">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="b765d-117">Lorsque vous gérez des groupes dans une version autonome d’EOP PowerShell, il se peut que vous rencontriez une limitation.</span><span class="sxs-lookup"><span data-stu-id="b765d-117">When you manage groups in standalone EOP PowerShell, you might encounter throttling.</span></span> <span data-ttu-id="b765d-118">Les procédures PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.</span><span class="sxs-lookup"><span data-stu-id="b765d-118">The PowerShell procedures in this topic use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="b765d-119">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="b765d-119">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="b765d-120">Plus précisément, vous avez besoin du rôle groupes de distribution, qui est affecté aux groupes de rôles OrganizationManagement (administrateurs globaux) et RecipientManagement par défaut.</span><span class="sxs-lookup"><span data-stu-id="b765d-120">Specifically, you need the Distribution Groups role, which is assigned to the OrganizationManagement (global admins) and RecipientManagement role groups by default.</span></span> <span data-ttu-id="b765d-121">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="b765d-121">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="b765d-122">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="b765d-122">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="b765d-123">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="b765d-123">Having problems?</span></span> <span data-ttu-id="b765d-124">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="b765d-124">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-exchange-admin-center-to-manage-distribution-groups"></a><span data-ttu-id="b765d-125">Utiliser le centre d’administration Exchange pour gérer les groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="b765d-125">Use the Exchange admin center to manage distribution groups</span></span>

### <a name="use-the-eac-to-create-groups"></a><span data-ttu-id="b765d-126">Utiliser le centre d’administration Exchange pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-126">Use the EAC to create groups</span></span>

1. <span data-ttu-id="b765d-127">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b765d-127">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="b765d-128">Cliquez sur **nouvelle** ![ icône ](../../media/ITPro-EAC-AddIcon.png) , puis sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="b765d-128">Click **New** ![New icon](../../media/ITPro-EAC-AddIcon.png), and then select one of the following options:</span></span>

   - <span data-ttu-id="b765d-129">**Groupe de distribution**</span><span class="sxs-lookup"><span data-stu-id="b765d-129">**Distribution group**</span></span>

   - <span data-ttu-id="b765d-130">**Groupe de sécurité à extension messagerie**</span><span class="sxs-lookup"><span data-stu-id="b765d-130">**Mail-enabled security group**</span></span>

3. <span data-ttu-id="b765d-131">Dans la page nouveau groupe qui s’ouvre, configurez les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="b765d-131">In the new group page that opens, configure the following settings.</span></span> <span data-ttu-id="b765d-132">Les paramètres marqués par un <sup>\*</sup> sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="b765d-132">Settings marked with an <sup>\*</sup> are required.</span></span>

   - <span data-ttu-id="b765d-133"><sup>\*</sup>**Nom d’affichage**: ce nom s’affiche dans le carnet d’adresses de votre organisation, sur la ligne à : quand un message électronique est envoyé à ce groupe, et dans la liste **groupes** du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b765d-133"><sup>\*</sup>**Display name**: This name appears in your organization's address book, on the To: line when email is sent to this group, and in the **Groups** list in the EAC.</span></span> <span data-ttu-id="b765d-134">Le nom complet est obligatoire, doit être unique et doit être convivial afin que les utilisateurs puissent reconnaître ce qu’il est.</span><span class="sxs-lookup"><span data-stu-id="b765d-134">The display name is required, must be unique, and should be user-friendly so people recognize what it is.</span></span>

   - <span data-ttu-id="b765d-135"><sup>\*</sup>**Alias**: ce champ permet de taper le nom de l’alias du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-135"><sup>\*</sup>**Alias**: Use this box to type the name of the alias for the group.</span></span> <span data-ttu-id="b765d-136">L’alias ne peut pas dépasser 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="b765d-136">The alias can't exceed 64 characters and must be unique.</span></span> <span data-ttu-id="b765d-137">Lorsqu’un utilisateur tape l’alias dans la ligne à d’un message électronique, il est résolu en nom complet du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-137">When a user types the alias in the To line of an email message, it resolves to the group's display name.</span></span>

   - <span data-ttu-id="b765d-138"><sup>\*</sup>**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole arobase (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="b765d-138"><sup>\*</sup>**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="b765d-139">Par défaut, la valeur d' **alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="b765d-139">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="b765d-140">Pour la valeur Domain (domaine), cliquez sur le menu déroulant et sélectionnez le domaine accepté dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b765d-140">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

   - <span data-ttu-id="b765d-141">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet d’informations du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b765d-141">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

   - <span data-ttu-id="b765d-142"><sup>\*</sup>**Propriétaires**: un propriétaire de groupe peut gérer l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-142"><sup>\*</sup>**Owners**: A group owner can manage group membership.</span></span> <span data-ttu-id="b765d-143">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-143">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="b765d-144">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-144">All groups must have at least one owner.</span></span>

     <span data-ttu-id="b765d-145">Pour ajouter des propriétaires, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="b765d-145">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="b765d-146">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="b765d-146">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="b765d-147">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-147">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="b765d-148">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b765d-148">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="b765d-149">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b765d-149">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

   - <span data-ttu-id="b765d-150">**Membres**: ajouter et supprimer des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-150">**Members**: Add and remove group members.</span></span>

     <span data-ttu-id="b765d-151">Pour ajouter des membres, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="b765d-151">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="b765d-152">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="b765d-152">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="b765d-153">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-153">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="b765d-154">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b765d-154">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="b765d-155">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b765d-155">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

4. <span data-ttu-id="b765d-156">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="b765d-156">When you're finished, click **Save** to create the distribution group.</span></span>

### <a name="use-the-eac-to-modify-distribution-groups"></a><span data-ttu-id="b765d-157">Utiliser le centre d’administration Exchange pour modifier des groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="b765d-157">Use the EAC to modify distribution groups</span></span>

1. <span data-ttu-id="b765d-158">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b765d-158">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="b765d-159">Dans la liste des groupes, sélectionnez le groupe de distribution ou le groupe de sécurité à extension messagerie à modifier, puis cliquez sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="b765d-159">In the list of groups, select the distribution group or mail-enabled security group that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

3. <span data-ttu-id="b765d-160">Dans la page des propriétés du groupe de distribution qui s’ouvre, cliquez sur l’un des onglets suivants pour afficher ou modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="b765d-160">On the distribution group properties page that opens, click one of the following tabs to view or change properties.</span></span>

   <span data-ttu-id="b765d-161">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b765d-161">When you're finished, click **Save**.</span></span>

#### <a name="general"></a><span data-ttu-id="b765d-162">Général</span><span class="sxs-lookup"><span data-stu-id="b765d-162">General</span></span>

<span data-ttu-id="b765d-163">Utilisez cet onglet pour afficher ou modifier les informations de base relatives au groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-163">Use this tab to view or change basic information about the group.</span></span>

- <span data-ttu-id="b765d-164">**Nom d’affichage**: ce nom s’affiche dans le carnet d’adresses, sur la ligne à lorsque le courrier électronique est envoyé à ce groupe, et dans la **Liste groupes**.</span><span class="sxs-lookup"><span data-stu-id="b765d-164">**Display name**: This name appears in the address book, on the To line when email is sent to this group, and in the **Groups list**.</span></span> <span data-ttu-id="b765d-165">Le nom d'affichage est obligatoire et doit être convivial afin que les personnes identifient facilement de quoi il s'agit.</span><span class="sxs-lookup"><span data-stu-id="b765d-165">The display name is required and should be user-friendly so people recognize what it is.</span></span> <span data-ttu-id="b765d-166">Il doit également être unique dans votre domaine.</span><span class="sxs-lookup"><span data-stu-id="b765d-166">It also has to be unique in your domain.</span></span>

  <span data-ttu-id="b765d-167">Si vous avez implémenté une stratégie de noms de groupes, le nom d'affichage doit se conformer au format de nom défini par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b765d-167">If you've implemented a group naming policy, the display name has to conform to the naming format defined by the policy.</span></span>

- <span data-ttu-id="b765d-168">**Alias**: il s’agit de la partie de l’adresse de messagerie qui apparaît à gauche du symbole arobase (@).</span><span class="sxs-lookup"><span data-stu-id="b765d-168">**Alias**: This is the portion of the email address that appears to the left of the at (@) symbol.</span></span> <span data-ttu-id="b765d-169">Si vous modifiez l'alias, l'adresse SMTP principale du groupe est également modifiée et contient le nouvel alias.</span><span class="sxs-lookup"><span data-stu-id="b765d-169">If you change the alias, the primary SMTP address for the group will also be changed, and contain the new alias.</span></span> <span data-ttu-id="b765d-170">De plus, l'adresse de messagerie électronique qui comprend l'alias précédent est gardée en tant qu'adresse de proxy du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-170">Also, the email address with the previous alias will be kept as a proxy address for the group.</span></span>

- <span data-ttu-id="b765d-171">**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole arobase (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="b765d-171">**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="b765d-172">Par défaut, la valeur d' **alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="b765d-172">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="b765d-173">Pour la valeur Domain (domaine), cliquez sur le menu déroulant et sélectionnez le domaine accepté dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b765d-173">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

- <span data-ttu-id="b765d-174">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet d’informations du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b765d-174">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

#### <a name="ownership"></a><span data-ttu-id="b765d-175">Propriété</span><span class="sxs-lookup"><span data-stu-id="b765d-175">Ownership</span></span>

<span data-ttu-id="b765d-176">Utilisez cet onglet pour affecter des propriétaires de groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-176">Use this tab to assign group owners.</span></span> <span data-ttu-id="b765d-177">Un propriétaire de groupe peut gérer l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-177">A group owner can manage group membership.</span></span> <span data-ttu-id="b765d-178">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-178">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="b765d-179">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-179">All groups must have at least one owner.</span></span>

<span data-ttu-id="b765d-180">Pour ajouter des propriétaires, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="b765d-180">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="b765d-181">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="b765d-181">In the dialog that appears, find and select a recipient, and then click **add ->**.</span></span> <span data-ttu-id="b765d-182">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-182">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="b765d-183">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b765d-183">When you're finished, click **OK**.</span></span>

<span data-ttu-id="b765d-184">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b765d-184">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

#### <a name="membership"></a><span data-ttu-id="b765d-185">Appartenance</span><span class="sxs-lookup"><span data-stu-id="b765d-185">Membership</span></span>

<span data-ttu-id="b765d-186">Utilisez cet onglet pour ajouter ou supprimer des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-186">Use this tab to add or remove group members.</span></span> <span data-ttu-id="b765d-187">Les propriétaires de groupe n’ont pas besoin d’être membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-187">Group owners don't need to be members of the group.</span></span>

<span data-ttu-id="b765d-188">Pour ajouter des membres, cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="b765d-188">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="b765d-189">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="b765d-189">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="b765d-190">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b765d-190">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="b765d-191">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b765d-191">When you're finished, click **OK**.</span></span>

<span data-ttu-id="b765d-192">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b765d-192">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

### <a name="use-the-eac-to-remove-groups"></a><span data-ttu-id="b765d-193">Utiliser le centre d’administration Exchange pour supprimer des groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-193">Use the EAC to remove groups</span></span>

1. <span data-ttu-id="b765d-194">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b765d-194">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="b765d-195">Dans la liste des groupes, sélectionnez le groupe de distribution que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="b765d-195">In the list of groups, select the distribution group that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

## <a name="use-powershell-to-manage-groups"></a><span data-ttu-id="b765d-196">Utiliser PowerShell pour gérer les groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-196">Use PowerShell to manage groups</span></span>

### <a name="use-standalone-eop-powershell-to-view-groups"></a><span data-ttu-id="b765d-197">Utilisation d’EOP PowerShell autonome pour afficher des groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-197">Use standalone EOP PowerShell to view groups</span></span>

<span data-ttu-id="b765d-198">Pour renvoyer une liste récapitulative de tous les groupes de distribution et des groupes de sécurité à extension messagerie dans la version autonome d’EOP PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b765d-198">To return a summary list of all distribution groups and mail-enabled security groups in standalone EOP PowerShell, run the following command:</span></span>

```powershell
Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
```

<span data-ttu-id="b765d-199">Pour renvoyer la liste des membres du groupe, remplacez \< groupIdentity \> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b765d-199">To return the list of group members, replace \<GroupIdentity\> with the name, alias, or email address of the group, and run the following command:</span></span>

```powershell
Get-DistributionGroupMember -Identity <GroupIdentity>
```

<span data-ttu-id="b765d-200">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) et [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/get-distributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="b765d-200">For detailed syntax and parameter information, see [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) and [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/get-distributiongroupmember).</span></span>

### <a name="use-standalone-eop-powershell-to-create-groups"></a><span data-ttu-id="b765d-201">Utilisation d’EOP PowerShell autonome pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-201">Use standalone EOP PowerShell to create groups</span></span>

<span data-ttu-id="b765d-202">Pour créer des groupes de distribution ou des groupes de sécurité à extension messagerie dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b765d-202">To create distribution groups or mail-enabled security groups in standalone EOP PowerShell, use the following syntax:</span></span>

```PowerShell
New-EOPDistributionGroup -Name "<Unique Name>" -ManagedBy @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">) [-Alias <text>] [-DisplayName "<Descriptive Name>"] [-Members @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">)] [-Notes "<Optional Text>"] [-PrimarySmtpAddress <SmtpAddress>] [-Type <Distribution | Security>]
```

<span data-ttu-id="b765d-203">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="b765d-203">**Notes**:</span></span>

- <span data-ttu-id="b765d-204">Le paramètre _Name_ est obligatoire, sa longueur maximale est de 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="b765d-204">The _Name_ parameter is required, has a maximum length of 64 characters, and must be unique.</span></span> <span data-ttu-id="b765d-205">Si vous n’utilisez pas le paramètre _DisplayName_, la valeur du paramètre _Name_ est utilisée pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="b765d-205">If you don't use the _DisplayName_ parameter, the value of the _Name_ parameter is used for the display name.</span></span>

- <span data-ttu-id="b765d-206">Si vous n’utilisez pas le paramètre _alias_ , le paramètre _Name_ est utilisé pour la valeur alias.</span><span class="sxs-lookup"><span data-stu-id="b765d-206">If you don't use the _Alias_ parameter, the _Name_ parameter is used for the alias value.</span></span> <span data-ttu-id="b765d-207">Les espaces sont supprimés et les caractères non pris en charge sont convertis en points d’interrogation ( ?).</span><span class="sxs-lookup"><span data-stu-id="b765d-207">Spaces are removed and unsupported characters are converted to question marks (?).</span></span>

- <span data-ttu-id="b765d-208">Si vous n’utilisez pas le paramètre _PrimarySmtpAddress_ , la valeur d’alias est utilisée dans le paramètre _PrimarySmtpAddress_ .</span><span class="sxs-lookup"><span data-stu-id="b765d-208">If you don't use the _PrimarySmtpAddress_ parameter, the alias value is used in the _PrimarySmtpAddress_ parameter.</span></span>

- <span data-ttu-id="b765d-209">Si vous n’utilisez pas le paramètre _type_ , la valeur par défaut est distribution.</span><span class="sxs-lookup"><span data-stu-id="b765d-209">If you don't use the _Type_ parameter, the default value is Distribution.</span></span>

<span data-ttu-id="b765d-210">Cet exemple crée un groupe de distribution nommé administrateurs informatiques avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b765d-210">This example creates a distribution group named IT Administrators with the specified properties.</span></span>

```PowerShell
New-EOPDistributionGroup -Name "IT Administrators" -Alias itadmin -Members @("michelle@contoso.com","laura@contoso.com","julia@contoso.com") -ManagedBy "chris@contoso.com"
```

<span data-ttu-id="b765d-211">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/New-EOPDistributionGroup).</span><span class="sxs-lookup"><span data-stu-id="b765d-211">For detailed syntax and parameter information, see [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/New-EOPDistributionGroup).</span></span>

### <a name="use-standalone-eop-powershell-to-modify-groups"></a><span data-ttu-id="b765d-212">Utilisation d’EOP PowerShell autonome pour modifier des groupes</span><span class="sxs-lookup"><span data-stu-id="b765d-212">Use standalone EOP PowerShell to modify groups</span></span>

<span data-ttu-id="b765d-213">Pour modifier des groupes dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b765d-213">To modify groups in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
Set-EOPDistributionGroup -Identity <GroupIdentity> [-Alias <Text>] [-DisplayName <Text>] [-ManagedBy @("User1","User2",..."UserN")] [-PrimarySmtpAddress <SmtpAddress>]

```powershell
Update-EOPDistributionGroupMember -Identity <GroupIdentity> -Members @("User1","User2",..."UserN")
```

<span data-ttu-id="b765d-214">Cet exemple utilise la modification de l’adresse SMTP principale (également appelée adresse de réponse) pour le groupe Seattle Employees vers sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="b765d-214">This example uses changes the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span>

```PowerShell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"
```

<span data-ttu-id="b765d-215">Cet exemple remplace les membres actuels du groupe d’équipe de sécurité par Kitty Petersen et Tyson Fawcett.</span><span class="sxs-lookup"><span data-stu-id="b765d-215">This example replaces the current members of the Security Team group with Kitty Petersen and Tyson Fawcett.</span></span>

```powershell
Update-EOPDistributionGroupMember -Identity "Security Team" -Members @("Kitty Petersen","Tyson Fawcett")
```

<span data-ttu-id="b765d-216">Cet exemple ajoute un nouvel utilisateur appelé Tyson Fawcett au groupe nommé « équipe de sécurité » tout en conservant les membres actuels du groupe.</span><span class="sxs-lookup"><span data-stu-id="b765d-216">This example adds a new user named Tyson Fawcett to the group named Security Team while preserving the current members of the group.</span></span>

```powershell
$CurrentMemberObjects = Get-DistributionGroupMember "Security Team"
$CurrentMemberNames = $CurrentMemberObjects | % {$_.name}
$CurrentMemberNames += "Tyson Fawcett"
Update-EOPDistributionGroupMember -Identity "Security Team" -Members $CurrentMemberNames
```

<span data-ttu-id="b765d-217">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/set-eopdistributiongroup) et [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/update-eopdistributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="b765d-217">For detailed syntax and parameter information, see [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/set-eopdistributiongroup) and [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/update-eopdistributiongroupmember).</span></span>

### <a name="remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="b765d-218">Supprimer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="b765d-218">Remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="b765d-219">Cet exemple utilise le groupe de distribution nommé administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="b765d-219">This example uses removes the distribution group named IT Administrators.</span></span>

```PowerShell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

<span data-ttu-id="b765d-220">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/remove-eopdistributiongroup).</span><span class="sxs-lookup"><span data-stu-id="b765d-220">For detailed syntax and parameter information, see [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/remove-eopdistributiongroup).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="b765d-221">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="b765d-221">How do you know these procedures worked?</span></span>

<span data-ttu-id="b765d-222">Pour vérifier que vous avez bien créé, modifié ou supprimé un groupe de distribution ou un groupe de sécurité à extension messagerie, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b765d-222">To verify that you've successfully created, modified, or removed a distribution group or a mail-enabled security group, do any of the following steps:</span></span>

- <span data-ttu-id="b765d-223">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b765d-223">In the EAC, go to **Recipients** \> **Groups**.</span></span> <span data-ttu-id="b765d-224">Vérifiez que le groupe est affiché (ou non), puis vérifiez la valeur du **type de groupe** .</span><span class="sxs-lookup"><span data-stu-id="b765d-224">Verify that the group is listed (or not listed), and verify the **Group Type** value.</span></span> <span data-ttu-id="b765d-225">Sélectionnez le groupe et affichez les informations dans le volet d’informations, ou cliquez sur **modifier** ![ l’icône modifier ](../../media/ITPro-EAC-AddIcon.png) pour afficher les paramètres.</span><span class="sxs-lookup"><span data-stu-id="b765d-225">Select the group and view the information in the Details pane, or click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png) to view the settings.</span></span>

- <span data-ttu-id="b765d-226">Dans la version autonome d’EOP PowerShell, exécutez la commande suivante pour vérifier que le groupe est affiché (ou non) :</span><span class="sxs-lookup"><span data-stu-id="b765d-226">In standalone EOP PowerShell, run the following command to verify the group is listed (or isn't listed):</span></span>

  ```PowerShell
  Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
  ```

- <span data-ttu-id="b765d-227">Remplacez \< groupIdentity \> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="b765d-227">Replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command to verify the settings:</span></span>

  ```PowerShell
  Get-Recipient -Identity <GroupIdentity> | Format-List
  ```

- <span data-ttu-id="b765d-228">Pour afficher les membres du groupe, remplacez \< groupIdentity \> par le nom, l’alias ou l’adresse de messagerie du groupe, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b765d-228">To view the group members, replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command:</span></span>

  ```PowerShell
  Get-DistributionGroupMember -Identity "<GroupIdentity>"
  ```
