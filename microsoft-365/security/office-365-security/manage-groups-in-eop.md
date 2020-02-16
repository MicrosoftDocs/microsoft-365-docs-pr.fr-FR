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
description: Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes.
ms.openlocfilehash: ad07066906f78703c568850afbfa5dfa8d8cc3c1
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42082889"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="ea1af-104">Gestion des groupes dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="ea1af-104">Manage groups in EOP</span></span>

 <span data-ttu-id="ea1af-p102">Vous pouvez utiliser Exchange Online Protection (EOP) pour créer des groupes à extension messagerie pour une organisation Exchange. Vous pouvez également utiliser EOP pour définir ou mettre à jour les propriétés de groupe qui indiquent l'appartenance, les adresses électroniques et d'autres aspects des groupes. Vous pouvez créer des groupes de distribution et des groupes de sécurité, en fonction de vos besoins. Ces groupes peuvent être créés à l'aide du Centre d'administration Exchange (CAE) ou via Windows PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="ea1af-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span>

## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="ea1af-109">Types de groupe à extension messagerie</span><span class="sxs-lookup"><span data-stu-id="ea1af-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="ea1af-110">Vous pouvez créer deux types de groupes pour votre organisation Exchange :</span><span class="sxs-lookup"><span data-stu-id="ea1af-110">You can create two types of groups for your Exchange organization:</span></span>

- <span data-ttu-id="ea1af-111">Les groupes de distribution sont des collections d’utilisateurs de messagerie, tels qu’une équipe ou un autre groupe ad hoc, qui doivent recevoir ou envoyer des courriers électroniques concernant un domaine d’intérêt commun.</span><span class="sxs-lookup"><span data-stu-id="ea1af-111">Distribution groups are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest.</span></span> <span data-ttu-id="ea1af-112">Les groupes de distribution sont exclusivement destinés à la distribution de messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="ea1af-112">Distribution groups are exclusively for distributing email messages.</span></span> <span data-ttu-id="ea1af-113">Dans EOP, un groupe de distribution fait référence à n'importe quel groupe à extension messagerie, qu'il dispose ou non d'un contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ea1af-113">In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>

- <span data-ttu-id="ea1af-114">Les groupes de sécurité sont des collections d’utilisateurs de messagerie qui ont besoin d’autorisations d’accès pour les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ea1af-114">Security groups are collections of email users who need access permissions for Admin roles.</span></span> <span data-ttu-id="ea1af-115">Par exemple, vous voudrez peut-être accorder à un groupe spécifique d'utilisateurs des autorisations de rôle d'administrateur afin qu'ils puissent configurer des paramètres de blocage du courrier indésirable et des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="ea1af-115">For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea1af-p105">Par défaut, tous les nouveaux groupes de sécurité à extension messagerie exigent que tous les expéditeurs soient identifiés. En procédant de la sorte, les expéditeurs externes ne peuvent pas envoyer de messages aux groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="ea1af-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ea1af-118">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="ea1af-118">Before you begin</span></span>

- <span data-ttu-id="ea1af-p106">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Groupes de distribution et groupes de sécurité » dans la rubrique [Autorisations des fonctionnalités dans EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="ea1af-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span>

- <span data-ttu-id="ea1af-121">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="ea1af-121">To open the Exchange admin center, see [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="ea1af-122">N’oubliez pas que lors de la création et de la gestion des groupes à l’aide des cmdlets PowerShell d’Exchange Online Protection, vous pouvez rencontrer des limitations.</span><span class="sxs-lookup"><span data-stu-id="ea1af-122">Be aware that when creating and managing groups by using Exchange Online Protection PowerShell cmdlets, you may encounter throttling.</span></span>

- <span data-ttu-id="ea1af-123">Les procédures PowerShell de cette rubrique utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.</span><span class="sxs-lookup"><span data-stu-id="ea1af-123">The PowerShell procedures in this topic use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="ea1af-124">Pour apprendre à utiliser Windows PowerShell afin d’établir une connexion à Exchange Online Protection, voir [Connexion à Exchange Online Protection à l’aide de Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="ea1af-124">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="ea1af-125">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="ea1af-125">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="ea1af-126">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="ea1af-126">Having problems?</span></span> <span data-ttu-id="ea1af-127">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="ea1af-127">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="ea1af-128">Créer un groupe dans le CAE</span><span class="sxs-lookup"><span data-stu-id="ea1af-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="ea1af-129">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="ea1af-129">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="ea1af-130">Cliquez sur **nouvelle** ![icône](../../media/ITPro-EAC-AddIcon.gif)ajouter, puis sur **groupe de distribution** ou groupe de **sécurité**, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ea1af-130">Click **New** ![Add Icon](../../media/ITPro-EAC-AddIcon.gif), and then click **Distribution group** or **Security group**, depending on your needs.</span></span>

3. <span data-ttu-id="ea1af-131">Sur la page **nouveau groupe de distribution** ou **nouveau groupe de sécurité** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea1af-131">On the **New distribution group** or **New security group** page, configure the following settings:</span></span>

   - <span data-ttu-id="ea1af-132">**Nom d’affichage**: tapez un nom d’affichage propre à votre organisation et pertinent pour les utilisateurs EOP.</span><span class="sxs-lookup"><span data-stu-id="ea1af-132">**Display name**: Type a display name that's unique to your organization and meaningful to EOP users.</span></span> <span data-ttu-id="ea1af-133">Le nom complet est requis.</span><span class="sxs-lookup"><span data-stu-id="ea1af-133">The display name is required.</span></span>

   - <span data-ttu-id="ea1af-134">**Alias**: tapez un alias de groupe de jusqu’à 64 caractères qui sont propres à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ea1af-134">**Alias**: Type a group alias of up to 64 characters that's unique to your organization.</span></span> <span data-ttu-id="ea1af-135">Les utilisateurs EOP tapent l’alias dans la ligne à : des messages électroniques et l’alias est résolu en nom complet du groupe.</span><span class="sxs-lookup"><span data-stu-id="ea1af-135">EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name.</span></span> <span data-ttu-id="ea1af-136">Si vous modifiez l’alias, l’adresse SMTP principale du groupe est également modifiée et contiendra le nouvel alias.</span><span class="sxs-lookup"><span data-stu-id="ea1af-136">If you change the alias, the primary SMTP address for the group also changes and will contain the new alias.</span></span> <span data-ttu-id="ea1af-137">L'alias est un champ obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ea1af-137">The alias is required.</span></span>

   - <span data-ttu-id="ea1af-138">**Description**: tapez une description du groupe afin que les utilisateurs connaissent l’objectif du groupe.</span><span class="sxs-lookup"><span data-stu-id="ea1af-138">**Description**: Type a description of the group so that people will know the purpose of the group.</span></span>

   - <span data-ttu-id="ea1af-139">**Propriétaires**: par défaut, la personne qui crée le groupe est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ea1af-139">**Owners**: By default, the person who creates the group is the owner.</span></span> <span data-ttu-id="ea1af-140">Vous pouvez ajouter un propriétaire en sélectionnant **Ajouter** ![une](../../media/ITPro-EAC-AddIcon.gif)icône Ajouter.</span><span class="sxs-lookup"><span data-stu-id="ea1af-140">You can add an owner by choosing **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.gif).</span></span> <span data-ttu-id="ea1af-141">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ea1af-141">All groups must have at least one owner.</span></span>

     > [!NOTE]
     > <span data-ttu-id="ea1af-142">Les propriétaires des groupes ne doivent pas nécessairement en être membres.</span><span class="sxs-lookup"><span data-stu-id="ea1af-142">Owners don't have to be members of the group.</span></span>

   - <span data-ttu-id="ea1af-143">**Membres**: utilisez cette section pour ajouter des membres du groupe et pour spécifier si une approbation est requise pour que des personnes puissent rejoindre ou quitter le groupe.</span><span class="sxs-lookup"><span data-stu-id="ea1af-143">**Members**: Use this section to add group members and to specify whether approval is required for people to join or leave the group.</span></span> <span data-ttu-id="ea1af-144">Pour ajouter des membres au groupe, cliquez sur **Ajouter** ![une](../../media/ITPro-EAC-AddIcon.gif)icône Ajouter.</span><span class="sxs-lookup"><span data-stu-id="ea1af-144">To add members to the group, click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.gif).</span></span>

4. <span data-ttu-id="ea1af-145">Cliquez sur **OK** pour revenir à la page d'origine.</span><span class="sxs-lookup"><span data-stu-id="ea1af-145">Click **OK** to return to the original page.</span></span>

5. <span data-ttu-id="ea1af-p112">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe. Le nouveau groupe doit apparaître dans la liste des groupes.</span><span class="sxs-lookup"><span data-stu-id="ea1af-p112">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span>

## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="ea1af-148">Modifier ou supprimer un groupe dans le CAE</span><span class="sxs-lookup"><span data-stu-id="ea1af-148">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="ea1af-149">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="ea1af-149">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="ea1af-150">Effectuez l'une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea1af-150">Do one of the following steps:</span></span>

   - <span data-ttu-id="ea1af-151">Pour modifier un groupe : dans la liste des groupes, cliquez sur le groupe que vous souhaitez afficher ou modifier, puis cliquez sur **modifier** ![l’icône](../../media/ITPro-EAC-EditIcon.gif)modifier.</span><span class="sxs-lookup"><span data-stu-id="ea1af-151">To edit a group: In the list of groups, click the group that you want to view or change, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.gif).</span></span> <span data-ttu-id="ea1af-152">Vous pouvez mettre à jour les paramètres généraux, ajouter ou supprimer des propriétaires de groupes, et ajouter ou supprimer des membres du groupe selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ea1af-152">You can update general settings, add or remove group owners, and add or remove group members as needed.</span></span>

   - <span data-ttu-id="ea1af-153">Pour supprimer un groupe : sélectionnez le groupe, puis \*\*\*\* ![cliquez sur supprimer](../../media/ITPro-EAC-RemoveIcon.gif)l’icône Supprimer.</span><span class="sxs-lookup"><span data-stu-id="ea1af-153">To remove a group: Select the group and click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

3. <span data-ttu-id="ea1af-154">Après avoir effectué toutes les modifications voulues, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ea1af-154">When you're finished making your changes, click **Save**.</span></span>

## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="ea1af-155">Créer, modifier ou supprimer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="ea1af-155">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="ea1af-156">Cette section fournit des informations sur la création de groupes et la modification de leurs propriétés dans Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea1af-156">This section provides information about creating groups and changing their properties in Exchange Online Protection PowerShell.</span></span> <span data-ttu-id="ea1af-157">Elle explique également comment supprimer un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="ea1af-157">It also shows how to remove an existing group.</span></span>

### <a name="create-a-group-using-remote-windows-powershell"></a><span data-ttu-id="ea1af-158">Créer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="ea1af-158">Create a group using remote Windows PowerShell</span></span>

<span data-ttu-id="ea1af-p115">Cet exemple utilise la cmdlet [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/New-EOPDistributionGroup) pour créer un groupe de distribution avec l'alias itadmin et le nom IT Administrators. Il ajoute également des utilisateurs en tant que membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="ea1af-p115">This example uses the [New-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/New-EOPDistributionGroup) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span>

```PowerShell
New-EOPDistributionGroup -Type Distribution -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy Member1
```

<span data-ttu-id="ea1af-161">**Remarque**: pour créer un groupe de sécurité au lieu d’un groupe de distribution, `Security` utilisez la valeur pour le paramètre *type* .</span><span class="sxs-lookup"><span data-stu-id="ea1af-161">**Note**: To create a security group instead of a distribution group, use the value `Security` for the *Type* parameter.</span></span>

<span data-ttu-id="ea1af-162">Pour vérifier que vous avez bien créé le groupe administrateurs informatiques, exécutez la commande suivante pour afficher les informations sur le nouveau groupe :</span><span class="sxs-lookup"><span data-stu-id="ea1af-162">To verify that you've successfully created the IT Administrators group, run the following command to display information about the new group:</span></span>

```PowerShell
Get-Recipient "IT Administrators" | Format-List
```

<span data-ttu-id="ea1af-163">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient).</span><span class="sxs-lookup"><span data-stu-id="ea1af-163">For detailed syntax and parameter information, see [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient).</span></span>

<span data-ttu-id="ea1af-164">Pour obtenir la liste des membres du groupe, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ea1af-164">To get a list of members in the group, run the following command:</span></span>

```PowerShell
Get-DistributionGroupMember "IT Administrators"
```

<span data-ttu-id="ea1af-165">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-distributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="ea1af-165">For detailed syntax and parameter information, see [Get-DistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/get-distributiongroupmember).</span></span>

<span data-ttu-id="ea1af-166">Pour obtenir la liste complète de tous vos groupes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ea1af-166">To get a full list of all your groups, run the following command:</span></span>

```PowerShell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | Format-Table | more
```

### <a name="change-the-properties-of-a-group-using-remote-windows-powershell"></a><span data-ttu-id="ea1af-167">Modifier les propriétés d’un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="ea1af-167">Change the properties of a group using remote Windows PowerShell</span></span>

<span data-ttu-id="ea1af-168">L’utilisation de PowerShell au lieu du centre d’administration Exchange permet de modifier les propriétés de plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="ea1af-168">An advantage of using PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span>

<span data-ttu-id="ea1af-169">Voici quelques exemples d’utilisation d’Exchange Online Protection PowerShell pour modifier les propriétés d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="ea1af-169">Here are some examples of using Exchange Online Protection PowerShell to change group properties.</span></span>

<span data-ttu-id="ea1af-170">Cet exemple utilise la modification de l’adresse SMTP principale (également appelée adresse de réponse) pour le groupe Seattle Employees vers sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ea1af-170">This example uses changes the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span>

```PowerShell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"
```

<span data-ttu-id="ea1af-171">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopdistributiongroup).</span><span class="sxs-lookup"><span data-stu-id="ea1af-171">For detailed syntax and parameter information, see [Set-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/set-eopdistributiongroup).</span></span>

<span data-ttu-id="ea1af-172">Pour vérifier que vous avez bien modifié les propriétés du groupe, exécutez la commande suivante pour vérifier la nouvelle valeur :</span><span class="sxs-lookup"><span data-stu-id="ea1af-172">To verify that you've successfully changed the properties for the group, run the following command to verify the new value:</span></span>

```PowerShell
Get-Recipient "Seattle Employees" | Format-List "PrimarySmtpAddress"
```

<span data-ttu-id="ea1af-173">Cet exemple met à jour tous les membres du groupe Seattle Employees.</span><span class="sxs-lookup"><span data-stu-id="ea1af-173">This example updates all the members of the Seattle Employees group.</span></span> <span data-ttu-id="ea1af-174">Utilisez des virgules pour séparer tous les membres.</span><span class="sxs-lookup"><span data-stu-id="ea1af-174">Use a comma to separate all members.</span></span>

```PowerShell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")
```

<span data-ttu-id="ea1af-175">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/update-eopdistributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="ea1af-175">For detailed syntax and parameter information, see [Update-EOPDistributionGroupMember](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/update-eopdistributiongroupmember).</span></span>

<span data-ttu-id="ea1af-176">Pour obtenir la liste de tous les membres du groupe Seattle Employees, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ea1af-176">To get the list of all the members in the group Seattle Employees, run the following command:</span></span>

```PowerShell
Get-DistributionGroupMember "Seattle Employees"
```

### <a name="remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="ea1af-177">Supprimer un groupe à l’aide de Windows PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="ea1af-177">Remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="ea1af-178">Cet exemple utilise le groupe de distribution nommé administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="ea1af-178">This example uses removes the distribution group named IT Administrators.</span></span>

```PowerShell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

<span data-ttu-id="ea1af-179">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/remove-eopdistributiongroup).</span><span class="sxs-lookup"><span data-stu-id="ea1af-179">For detailed syntax and parameter information, see [Remove-EOPDistributionGroup](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/remove-eopdistributiongroup).</span></span>

<span data-ttu-id="ea1af-180">Pour vérifier que le groupe a été supprimé, exécutez la commande suivante et assurez-vous que le groupe (dans ce cas administrateurs informatiques) a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ea1af-180">To verify that the group was removed, run the following command, and confirm that the group (in this case "It Administrators") was deleted.</span></span>

```PowerShell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"
```
