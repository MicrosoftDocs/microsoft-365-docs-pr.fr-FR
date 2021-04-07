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
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs d’organisations Exchange Online Protection (EOP) autonomes peuvent apprendre à créer, modifier et supprimer des groupes de distribution et des groupes de sécurité à messagerie dans le Centre d’administration Exchange (CAE) et dans Exchange Online Protection (EOP) autonome PowerShell.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: b9d83f2fb59ee8f8d2d3035045ed438d5ba45851
ms.sourcegitcommit: 7ee50882cb4ed37794a3cd82dac9b2f9e0a1f14a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "51599568"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="d7e56-103">Gestion des groupes dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="d7e56-103">Manage groups in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="d7e56-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d7e56-104">**Applies to**</span></span>
-  [<span data-ttu-id="d7e56-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="d7e56-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="d7e56-106">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez créer, modifier et supprimer les types de groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="d7e56-106">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can create, modify, and remove the following types of groups:</span></span>

- <span data-ttu-id="d7e56-107">**Groupes de distribution**: collection d’utilisateurs de messagerie ou d’autres groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="d7e56-107">**Distribution groups**: A collection of mail users or other distribution groups.</span></span> <span data-ttu-id="d7e56-108">Par exemple, les équipes ou d’autres groupes ad hoc qui doivent recevoir ou envoyer des messages électroniques dans un domaine commun d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="d7e56-108">For example, teams or other ad hoc groups who need to receive or send email in a common area of interest.</span></span> <span data-ttu-id="d7e56-109">Les groupes de distribution sont exclusivement dédiés à la distribution des messages électroniques et ne sont pas des principaux de sécurité (ils ne peuvent pas se voir attribuer d’autorisations).</span><span class="sxs-lookup"><span data-stu-id="d7e56-109">Distribution groups are exclusively for distributing email messages, and are not security principals (they can't have permissions assigned to them).</span></span>

- <span data-ttu-id="d7e56-110">**Groupes de sécurité à messagerie**: collection d’utilisateurs de messagerie et d’autres groupes de sécurité qui ont besoin d’autorisations d’accès pour les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d7e56-110">**Mail-enabled security groups**: A collection of mail users and other security groups who need access permissions for admin roles.</span></span> <span data-ttu-id="d7e56-111">Par exemple, vous souhaiterez peut-être accorder à un groupe spécifique d’utilisateurs des autorisations d’administration afin qu’ils configurent les paramètres anti-courrier indésirable et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="d7e56-111">For example, you might want to give specific group of users admin permissions so they can configure anti-spam and anti-malware settings.</span></span>

    > [!NOTE]
    >
    > - <span data-ttu-id="d7e56-112">Par défaut, les nouveaux groupes de sécurité à messagerie rejettent les messages provenant d’expéditeurs externes (non authentifiés).</span><span class="sxs-lookup"><span data-stu-id="d7e56-112">By default, new mail-enabled security groups reject messages from external (unauthenticated) senders.</span></span>
    >
    > - <span data-ttu-id="d7e56-113">N’ajoutez pas de groupes de distribution aux groupes de sécurité à messagerie.</span><span class="sxs-lookup"><span data-stu-id="d7e56-113">Don't add distribution groups to mail-enabled security groups.</span></span>

<span data-ttu-id="d7e56-114">Vous pouvez gérer des groupes dans le Centre d’administration Exchange (CAE) et dans EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="d7e56-114">You can manage groups in the Exchange admin center (EAC) and in standalone EOP PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d7e56-115">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d7e56-115">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d7e56-116">Pour ouvrir le Centre d’administration Exchange, consultez le [Centre d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="d7e56-116">To open the Exchange admin center, see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="d7e56-117">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="d7e56-117">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="d7e56-118">Lorsque vous gérez des groupes dans EOP PowerShell autonome, vous pouvez rencontrer une limitation.</span><span class="sxs-lookup"><span data-stu-id="d7e56-118">When you manage groups in standalone EOP PowerShell, you might encounter throttling.</span></span> <span data-ttu-id="d7e56-119">Les procédures PowerShell de cet article utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="d7e56-119">The PowerShell procedures in this article use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="d7e56-120">Des autorisations doivent vous être attribuées dans Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="d7e56-120">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="d7e56-121">Plus précisément, vous avez besoin du rôle  Groupes de **distribution,** qui est attribué aux groupes de rôles Gestion de l’organisation et **Gestion** des destinataires par défaut.</span><span class="sxs-lookup"><span data-stu-id="d7e56-121">Specifically, you need the **Distribution Groups** role, which is assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="d7e56-122">Pour plus d’informations, voir Autorisations dans [EOP](feature-permissions-in-eop.md) autonome et utiliser le CAE pour modifier la liste des membres des [groupes de rôles.](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)</span><span class="sxs-lookup"><span data-stu-id="d7e56-122">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="d7e56-123">Pour plus d’informations sur les raccourcis clavier qui peuvent s’appliquer aux procédures de cet article, voir raccourcis clavier pour le Centre d’administration [Exchange dans Exchange Online.](/Exchange/accessibility/keyboard-shortcuts-in-admin-center)</span><span class="sxs-lookup"><span data-stu-id="d7e56-123">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="d7e56-124">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="d7e56-124">Having problems?</span></span> <span data-ttu-id="d7e56-125">Demandez de l’aide dans le Forum [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) .</span><span class="sxs-lookup"><span data-stu-id="d7e56-125">Ask for help in the [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) forum.</span></span>

## <a name="use-the-exchange-admin-center-to-manage-distribution-groups"></a><span data-ttu-id="d7e56-126">Utiliser le Centre d’administration Exchange pour gérer les groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="d7e56-126">Use the Exchange admin center to manage distribution groups</span></span>

### <a name="use-the-eac-to-create-groups"></a><span data-ttu-id="d7e56-127">Utiliser le EAC pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-127">Use the EAC to create groups</span></span>

1. <span data-ttu-id="d7e56-128">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-128">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="d7e56-129">Cliquez **sur Nouvelle** ![ ](../../media/ITPro-EAC-AddIcon.png) icône, puis sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7e56-129">Click **New** ![New icon](../../media/ITPro-EAC-AddIcon.png), and then select one of the following options:</span></span>

   - <span data-ttu-id="d7e56-130">**Groupe de distribution**</span><span class="sxs-lookup"><span data-stu-id="d7e56-130">**Distribution group**</span></span>

   - <span data-ttu-id="d7e56-131">**Groupe de sécurité à extension messagerie**</span><span class="sxs-lookup"><span data-stu-id="d7e56-131">**Mail-enabled security group**</span></span>

3. <span data-ttu-id="d7e56-132">Dans la page de nouveau groupe qui s’ouvre, configurez les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="d7e56-132">In the new group page that opens, configure the following settings.</span></span> <span data-ttu-id="d7e56-133">Les paramètres marqués avec <sup>\*</sup> un paramètre sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="d7e56-133">Settings marked with an <sup>\*</sup> are required.</span></span>

   - <span data-ttu-id="d7e56-134"><sup>\*</sup>**Nom d’affichage**: ce nom apparaît dans le carnet d’adresses de votre organisation, sur la ligne À : lorsque le courrier électronique est envoyé à ce groupe, et dans la liste Groupes dans leAC. </span><span class="sxs-lookup"><span data-stu-id="d7e56-134"><sup>\*</sup>**Display name**: This name appears in your organization's address book, on the To: line when email is sent to this group, and in the **Groups** list in the EAC.</span></span> <span data-ttu-id="d7e56-135">Le nom d’affichage est obligatoire, doit être unique et convivial afin que les utilisateurs reconnaissent ce qu’il est.</span><span class="sxs-lookup"><span data-stu-id="d7e56-135">The display name is required, must be unique, and should be user-friendly so people recognize what it is.</span></span>

   - <span data-ttu-id="d7e56-136"><sup>\*</sup>**Alias**: utilisez cette zone pour taper le nom de l’alias du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-136"><sup>\*</sup>**Alias**: Use this box to type the name of the alias for the group.</span></span> <span data-ttu-id="d7e56-137">L’alias ne peut pas dépasser 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="d7e56-137">The alias can't exceed 64 characters and must be unique.</span></span> <span data-ttu-id="d7e56-138">Lorsqu’un utilisateur tape l’alias dans la ligne À d’un message électronique, il est résolu en nom complet du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-138">When a user types the alias in the To line of an email message, it resolves to the group's display name.</span></span>

   - <span data-ttu-id="d7e56-139"><sup>\*</sup>**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="d7e56-139"><sup>\*</sup>**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="d7e56-140">Par défaut, la valeur **d’Alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="d7e56-140">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="d7e56-141">Pour la valeur du domaine, cliquez sur la drop down et sélectionnez et acceptez le domaine dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d7e56-141">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

   - <span data-ttu-id="d7e56-142">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet Détails du EAC.</span><span class="sxs-lookup"><span data-stu-id="d7e56-142">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

   - <span data-ttu-id="d7e56-143"><sup>\*</sup>**Propriétaires**: un propriétaire de groupe peut gérer l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-143"><sup>\*</sup>**Owners**: A group owner can manage group membership.</span></span> <span data-ttu-id="d7e56-144">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-144">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="d7e56-145">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-145">All groups must have at least one owner.</span></span>

     <span data-ttu-id="d7e56-146">Pour ajouter des propriétaires, cliquez **sur Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="d7e56-146">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="d7e56-147">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-147">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="d7e56-148">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-148">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="d7e56-149">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-149">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="d7e56-150">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="d7e56-150">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

   - <span data-ttu-id="d7e56-151">**Membres :** ajoutez et supprimez des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-151">**Members**: Add and remove group members.</span></span>

     <span data-ttu-id="d7e56-152">Pour ajouter des membres, cliquez **sur Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="d7e56-152">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="d7e56-153">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-153">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="d7e56-154">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-154">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="d7e56-155">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-155">When you're finished, click **OK**.</span></span>

     <span data-ttu-id="d7e56-156">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="d7e56-156">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

4. <span data-ttu-id="d7e56-157">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="d7e56-157">When you're finished, click **Save** to create the distribution group.</span></span>

### <a name="use-the-eac-to-modify-distribution-groups"></a><span data-ttu-id="d7e56-158">Utiliser le CENTRE D’EAC pour modifier des groupes de distribution</span><span class="sxs-lookup"><span data-stu-id="d7e56-158">Use the EAC to modify distribution groups</span></span>

1. <span data-ttu-id="d7e56-159">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-159">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="d7e56-160">Dans la liste des groupes, sélectionnez le groupe de distribution ou le  groupe de sécurité à messagerie à modifier, puis cliquez sur Modifier ![ l’icône ](../../media/ITPro-EAC-AddIcon.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="d7e56-160">In the list of groups, select the distribution group or mail-enabled security group that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

3. <span data-ttu-id="d7e56-161">Dans la page des propriétés du groupe de distribution qui s’ouvre, cliquez sur l’un des onglets suivants pour afficher ou modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="d7e56-161">On the distribution group properties page that opens, click one of the following tabs to view or change properties.</span></span>

   <span data-ttu-id="d7e56-162">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-162">When you're finished, click **Save**.</span></span>

#### <a name="general"></a><span data-ttu-id="d7e56-163">Général</span><span class="sxs-lookup"><span data-stu-id="d7e56-163">General</span></span>

<span data-ttu-id="d7e56-164">Utilisez cet onglet pour afficher ou modifier les informations de base relatives au groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-164">Use this tab to view or change basic information about the group.</span></span>

- <span data-ttu-id="d7e56-165">**Nom complet**: ce nom apparaît dans le carnet d’adresses, sur la ligne À lorsque le courrier électronique est envoyé à ce groupe et dans la liste **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="d7e56-165">**Display name**: This name appears in the address book, on the To line when email is sent to this group, and in the **Groups list**.</span></span> <span data-ttu-id="d7e56-166">Le nom d'affichage est obligatoire et doit être convivial afin que les personnes identifient facilement de quoi il s'agit.</span><span class="sxs-lookup"><span data-stu-id="d7e56-166">The display name is required and should be user-friendly so people recognize what it is.</span></span> <span data-ttu-id="d7e56-167">Il doit également être unique dans votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d7e56-167">It also has to be unique in your domain.</span></span>

  <span data-ttu-id="d7e56-168">Si vous avez implémenté une stratégie de noms de groupes, le nom d'affichage doit se conformer au format de nom défini par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d7e56-168">If you've implemented a group naming policy, the display name has to conform to the naming format defined by the policy.</span></span>

- <span data-ttu-id="d7e56-169">**Alias**: il s’agit de la partie de l’adresse de messagerie qui apparaît à gauche du symbole @.</span><span class="sxs-lookup"><span data-stu-id="d7e56-169">**Alias**: This is the portion of the email address that appears to the left of the at (@) symbol.</span></span> <span data-ttu-id="d7e56-170">Si vous modifiez l'alias, l'adresse SMTP principale du groupe est également modifiée et contient le nouvel alias.</span><span class="sxs-lookup"><span data-stu-id="d7e56-170">If you change the alias, the primary SMTP address for the group will also be changed, and contain the new alias.</span></span> <span data-ttu-id="d7e56-171">De plus, l'adresse de messagerie électronique qui comprend l'alias précédent est gardée en tant qu'adresse de proxy du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-171">Also, the email address with the previous alias will be kept as a proxy address for the group.</span></span>

- <span data-ttu-id="d7e56-172">**Adresse de messagerie**: l’adresse de messagerie se compose de l’alias sur le côté gauche du symbole @, et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="d7e56-172">**Email address**: The email address consists of the alias on the left side of the at (@) symbol, and a domain on the right side.</span></span> <span data-ttu-id="d7e56-173">Par défaut, la valeur **d’Alias** est utilisée pour la valeur d’alias, mais vous pouvez la modifier.</span><span class="sxs-lookup"><span data-stu-id="d7e56-173">By default, the value of **Alias** is used for the alias value, but you can change it.</span></span> <span data-ttu-id="d7e56-174">Pour la valeur du domaine, cliquez sur la drop down et sélectionnez et acceptez le domaine dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d7e56-174">For the domain value, click the drop down and select and accepted domain in your organization.</span></span>

- <span data-ttu-id="d7e56-175">**Description**: cette description apparaît dans le carnet d’adresses et dans le volet Détails du EAC.</span><span class="sxs-lookup"><span data-stu-id="d7e56-175">**Description**: This description appears in the address book and in the Details pane in the EAC.</span></span>

#### <a name="ownership"></a><span data-ttu-id="d7e56-176">Propriété</span><span class="sxs-lookup"><span data-stu-id="d7e56-176">Ownership</span></span>

<span data-ttu-id="d7e56-177">Utilisez cet onglet pour attribuer des propriétaires de groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-177">Use this tab to assign group owners.</span></span> <span data-ttu-id="d7e56-178">Un propriétaire de groupe peut gérer l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-178">A group owner can manage group membership.</span></span> <span data-ttu-id="d7e56-179">Par défaut, la personne qui crée un groupe en est le propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-179">By default, the person who creates a group is the owner.</span></span> <span data-ttu-id="d7e56-180">Tous les groupes doivent avoir au moins un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-180">All groups must have at least one owner.</span></span>

<span data-ttu-id="d7e56-181">Pour ajouter des propriétaires, cliquez **sur Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="d7e56-181">To add owners, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="d7e56-182">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire, puis cliquez sur **ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-182">In the dialog that appears, find and select a recipient, and then click **add ->**.</span></span> <span data-ttu-id="d7e56-183">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-183">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="d7e56-184">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-184">When you're finished, click **OK**.</span></span>

<span data-ttu-id="d7e56-185">Pour supprimer un propriétaire, sélectionnez-le, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="d7e56-185">To remove an owner, select the owner, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

#### <a name="membership"></a><span data-ttu-id="d7e56-186">Appartenance</span><span class="sxs-lookup"><span data-stu-id="d7e56-186">Membership</span></span>

<span data-ttu-id="d7e56-187">Utilisez cet onglet pour ajouter ou supprimer des membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-187">Use this tab to add or remove group members.</span></span> <span data-ttu-id="d7e56-188">Les propriétaires de groupe n’ont pas besoin d’être membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-188">Group owners don't need to be members of the group.</span></span>

<span data-ttu-id="d7e56-189">Pour ajouter des membres, cliquez **sur Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="d7e56-189">To add members, click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="d7e56-190">Dans la boîte de dialogue qui s’affiche, recherchez et sélectionnez un destinataire ou un groupe, puis cliquez sur **Ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-190">In the dialog that appears, find and select a recipient or group, and then click **add ->**.</span></span> <span data-ttu-id="d7e56-191">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d7e56-191">Repeat this step as many times as necessary.</span></span> <span data-ttu-id="d7e56-192">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-192">When you're finished, click **OK**.</span></span>

<span data-ttu-id="d7e56-193">Pour supprimer un membre, sélectionnez-le, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="d7e56-193">To remove a member, select the member, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

### <a name="use-the-eac-to-remove-groups"></a><span data-ttu-id="d7e56-194">Utiliser le EAC pour supprimer des groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-194">Use the EAC to remove groups</span></span>

1. <span data-ttu-id="d7e56-195">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-195">In the EAC, go to **Recipients** \> **Groups**.</span></span>

2. <span data-ttu-id="d7e56-196">Dans la liste des groupes, sélectionnez le groupe de  distribution à supprimer, puis cliquez sur Supprimer ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="d7e56-196">In the list of groups, select the distribution group that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

## <a name="use-powershell-to-manage-groups"></a><span data-ttu-id="d7e56-197">Utiliser PowerShell pour gérer les groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-197">Use PowerShell to manage groups</span></span>

### <a name="use-standalone-eop-powershell-to-view-groups"></a><span data-ttu-id="d7e56-198">Utiliser EOP PowerShell autonome pour afficher des groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-198">Use standalone EOP PowerShell to view groups</span></span>

<span data-ttu-id="d7e56-199">Pour renvoyer une liste récapitulatif de tous les groupes de distribution et groupes de sécurité à messagerie dans EOP PowerShell autonome, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d7e56-199">To return a summary list of all distribution groups and mail-enabled security groups in standalone EOP PowerShell, run the following command:</span></span>

```powershell
Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
```

<span data-ttu-id="d7e56-200">Pour renvoyer la liste des membres du groupe, remplacez-la par le nom, l’alias ou l’adresse e-mail du groupe, puis \<GroupIdentity\> exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d7e56-200">To return the list of group members, replace \<GroupIdentity\> with the name, alias, or email address of the group, and run the following command:</span></span>

```powershell
Get-DistributionGroupMember -Identity <GroupIdentity>
```

<span data-ttu-id="d7e56-201">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-Recipient](/powershell/module/exchange/get-recipient) et [Get-DistributionGroupMember](/powershell/module/exchange/get-distributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="d7e56-201">For detailed syntax and parameter information, see [Get-Recipient](/powershell/module/exchange/get-recipient) and [Get-DistributionGroupMember](/powershell/module/exchange/get-distributiongroupmember).</span></span>

### <a name="use-standalone-eop-powershell-to-create-groups"></a><span data-ttu-id="d7e56-202">Utiliser EOP PowerShell autonome pour créer des groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-202">Use standalone EOP PowerShell to create groups</span></span>

<span data-ttu-id="d7e56-203">Pour créer des groupes de distribution ou des groupes de sécurité à messagerie dans EOP PowerShell autonome, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d7e56-203">To create distribution groups or mail-enabled security groups in standalone EOP PowerShell, use the following syntax:</span></span>

```PowerShell
New-EOPDistributionGroup -Name "<Unique Name>" -ManagedBy @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">) [-Alias <text>] [-DisplayName "<Descriptive Name>"] [-Members @("UserOrGroup1","UserOrGroup2",..."UserOrGroupN">)] [-Notes "<Optional Text>"] [-PrimarySmtpAddress <SmtpAddress>] [-Type <Distribution | Security>]
```

<span data-ttu-id="d7e56-204">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="d7e56-204">**Notes**:</span></span>

- <span data-ttu-id="d7e56-205">Le _paramètre Name_ est obligatoire, a une longueur maximale de 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="d7e56-205">The _Name_ parameter is required, has a maximum length of 64 characters, and must be unique.</span></span> <span data-ttu-id="d7e56-206">Si vous n’utilisez pas le paramètre _DisplayName_, la valeur du paramètre _Name_ est utilisée pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="d7e56-206">If you don't use the _DisplayName_ parameter, the value of the _Name_ parameter is used for the display name.</span></span>

- <span data-ttu-id="d7e56-207">Si vous n’utilisez pas le paramètre _Alias,_ le paramètre _Name_ est utilisé pour la valeur d’alias.</span><span class="sxs-lookup"><span data-stu-id="d7e56-207">If you don't use the _Alias_ parameter, the _Name_ parameter is used for the alias value.</span></span> <span data-ttu-id="d7e56-208">Les espaces sont supprimés et les caractères non pris en place sont convertis en points d’interrogation (?).</span><span class="sxs-lookup"><span data-stu-id="d7e56-208">Spaces are removed and unsupported characters are converted to question marks (?).</span></span>

- <span data-ttu-id="d7e56-209">Si vous n’utilisez pas le _paramètre PrimarySmtpAddress,_ la valeur d’alias est utilisée dans le _paramètre PrimarySmtpAddress._</span><span class="sxs-lookup"><span data-stu-id="d7e56-209">If you don't use the _PrimarySmtpAddress_ parameter, the alias value is used in the _PrimarySmtpAddress_ parameter.</span></span>

- <span data-ttu-id="d7e56-210">Si vous n’utilisez pas le _paramètre Type,_ la valeur par défaut est Distribution.</span><span class="sxs-lookup"><span data-stu-id="d7e56-210">If you don't use the _Type_ parameter, the default value is Distribution.</span></span>

<span data-ttu-id="d7e56-211">Cet exemple crée un groupe de distribution nommé Administrateurs informatiques avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d7e56-211">This example creates a distribution group named IT Administrators with the specified properties.</span></span>

```PowerShell
New-EOPDistributionGroup -Name "IT Administrators" -Alias itadmin -Members @("michelle@contoso.com","laura@contoso.com","julia@contoso.com") -ManagedBy "chris@contoso.com"
```

<span data-ttu-id="d7e56-212">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-EOPDistributionGroup](/powershell/module/exchange/New-EOPDistributionGroup).</span><span class="sxs-lookup"><span data-stu-id="d7e56-212">For detailed syntax and parameter information, see [New-EOPDistributionGroup](/powershell/module/exchange/New-EOPDistributionGroup).</span></span>

### <a name="use-standalone-eop-powershell-to-modify-groups"></a><span data-ttu-id="d7e56-213">Utiliser EOP PowerShell autonome pour modifier des groupes</span><span class="sxs-lookup"><span data-stu-id="d7e56-213">Use standalone EOP PowerShell to modify groups</span></span>

<span data-ttu-id="d7e56-214">Pour modifier des groupes dans EOP PowerShell autonome, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="d7e56-214">To modify groups in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
Set-EOPDistributionGroup -Identity <GroupIdentity> [-Alias <Text>] [-DisplayName <Text>] [-ManagedBy @("User1","User2",..."UserN")] [-PrimarySmtpAddress <SmtpAddress>]

```powershell
Update-EOPDistributionGroupMember -Identity <GroupIdentity> -Members @("User1","User2",..."UserN")
```

<span data-ttu-id="d7e56-215">Cet exemple utilise la modification de l’adresse SMTP principale (également appelée adresse de réponse) pour le groupe Seattle Employees sea.employees@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="d7e56-215">This example uses changes the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span>

```PowerShell
Set-EOPDistributionGroup "Seattle Employees" -PrimarySmtpAddress "sea.employees@contoso.com"
```

<span data-ttu-id="d7e56-216">Cet exemple remplace les membres actuels du groupe d’équipe de sécurité par Kitty Petersen et ContrôleSyrence.</span><span class="sxs-lookup"><span data-stu-id="d7e56-216">This example replaces the current members of the Security Team group with Kitty Petersen and Tyson Fawcett.</span></span>

```powershell
Update-EOPDistributionGroupMember -Identity "Security Team" -Members @("Kitty Petersen","Tyson Fawcett")
```

<span data-ttu-id="d7e56-217">Cet exemple ajoute un nouvel utilisateur nommé « Agitassett » au groupe nommé « Security Team » tout en conservant les membres actuels du groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-217">This example adds a new user named Tyson Fawcett to the group named Security Team while preserving the current members of the group.</span></span>

```powershell
$CurrentMemberObjects = Get-DistributionGroupMember "Security Team"
$CurrentMemberNames = $CurrentMemberObjects | % {$_.name}
$CurrentMemberNames += "Tyson Fawcett"
Update-EOPDistributionGroupMember -Identity "Security Team" -Members $CurrentMemberNames
```

<span data-ttu-id="d7e56-218">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-EOPDistributionGroup](/powershell/module/exchange/set-eopdistributiongroup) et [Update-EOPDistributionGroupMember](/powershell/module/exchange/update-eopdistributiongroupmember).</span><span class="sxs-lookup"><span data-stu-id="d7e56-218">For detailed syntax and parameter information, see [Set-EOPDistributionGroup](/powershell/module/exchange/set-eopdistributiongroup) and [Update-EOPDistributionGroupMember](/powershell/module/exchange/update-eopdistributiongroupmember).</span></span>

### <a name="remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="d7e56-219">Supprimer un groupe à l’aide d’Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d7e56-219">Remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="d7e56-220">Cet exemple utilise la suppression du groupe de distribution nommé Administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="d7e56-220">This example uses removes the distribution group named IT Administrators.</span></span>

```PowerShell
Remove-EOPDistributionGroup -Identity "IT Administrators"
```

<span data-ttu-id="d7e56-221">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-EOPDistributionGroup](/powershell/module/exchange/remove-eopdistributiongroup).</span><span class="sxs-lookup"><span data-stu-id="d7e56-221">For detailed syntax and parameter information, see [Remove-EOPDistributionGroup](/powershell/module/exchange/remove-eopdistributiongroup).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="d7e56-222">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="d7e56-222">How do you know these procedures worked?</span></span>

<span data-ttu-id="d7e56-223">Pour vérifier que vous avez correctement créé, modifié ou supprimé un groupe de distribution ou un groupe de sécurité à messagerie, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7e56-223">To verify that you've successfully created, modified, or removed a distribution group or a mail-enabled security group, do any of the following steps:</span></span>

- <span data-ttu-id="d7e56-224">Dans le CAE, accédez à **Destinataires** \> **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="d7e56-224">In the EAC, go to **Recipients** \> **Groups**.</span></span> <span data-ttu-id="d7e56-225">Vérifiez que le groupe est répertorié (ou non répertorié) et vérifiez la valeur **type de** groupe.</span><span class="sxs-lookup"><span data-stu-id="d7e56-225">Verify that the group is listed (or not listed), and verify the **Group Type** value.</span></span> <span data-ttu-id="d7e56-226">Sélectionnez le groupe et affichez les informations  dans le volet d’informations, ou cliquez sur Modifier l’icône ![ Modifier pour afficher les ](../../media/ITPro-EAC-AddIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="d7e56-226">Select the group and view the information in the Details pane, or click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png) to view the settings.</span></span>

- <span data-ttu-id="d7e56-227">Dans EOP PowerShell autonome, exécutez la commande suivante pour vérifier que le groupe est répertorié (ou n’est pas répertorié) :</span><span class="sxs-lookup"><span data-stu-id="d7e56-227">In standalone EOP PowerShell, run the following command to verify the group is listed (or isn't listed):</span></span>

  ```PowerShell
  Get-Recipient -RecipientType MailUniversalDistributionGroup,MailUniversalSecurityGroup -ResultSize unlimited
  ```

- <span data-ttu-id="d7e56-228">Remplacez-le par le nom, l’alias ou l’adresse e-mail du groupe et exécutez la commande suivante \<GroupIdentity\> pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="d7e56-228">Replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command to verify the settings:</span></span>

  ```PowerShell
  Get-Recipient -Identity <GroupIdentity> | Format-List
  ```

- <span data-ttu-id="d7e56-229">Pour afficher les membres du groupe, remplacez-les par le nom, l’alias ou l’adresse e-mail du groupe \<GroupIdentity\> et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d7e56-229">To view the group members, replace \<GroupIdentity\> with the name, alias, or email address of the group and run the following command:</span></span>

  ```PowerShell
  Get-DistributionGroupMember -Identity "<GroupIdentity>"
  ```