---
title: Gérer les utilisateurs d’e-mail dans EOP autonome
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: Découvrez comment gérer les utilisateurs de messagerie dans Exchange Online Protection (EOP), notamment en utilisant la synchronisation d’annuaires, le CAE et PowerShell pour gérer les utilisateurs.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6a0dc1c0c343be77c6d6f713ee6b68a08a4fe5be
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289912"
---
# <a name="manage-mail-users-in-standalone-eop"></a><span data-ttu-id="1c443-103">Gérer les utilisateurs d’e-mail dans EOP autonome</span><span class="sxs-lookup"><span data-stu-id="1c443-103">Manage mail users in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1c443-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1c443-104">**Applies to**</span></span>
-  [<span data-ttu-id="1c443-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="1c443-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="1c443-106">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, les utilisateurs de messagerie représentent le type fondamental de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c443-106">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, mail users are the fundamental type of user account.</span></span> <span data-ttu-id="1c443-107">Un utilisateur de messagerie dispose d’informations d’identification de compte dans votre organisation EOP autonome et peut accéder aux ressources (avoir des autorisations affectées).</span><span class="sxs-lookup"><span data-stu-id="1c443-107">A mail user has account credentials in your standalone EOP organization, and can access resources (have permissions assigned).</span></span> <span data-ttu-id="1c443-108">L’adresse de messagerie d’un utilisateur de messagerie est externe (par exemple, dans votre environnement de messagerie local).</span><span class="sxs-lookup"><span data-stu-id="1c443-108">A mail user's email address is external (for example, in your on-premises email environment).</span></span>

> [!NOTE]
> <span data-ttu-id="1c443-109">Lorsque vous créez un utilisateur de messagerie, le compte d’utilisateur correspondant est disponible dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c443-109">When you create a mail user, the corresponding user account is available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="1c443-110">Lorsque vous créez un compte d’utilisateur dans le Centre d’administration Microsoft 365, vous ne pouvez pas l’utiliser pour créer un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c443-110">When you create a user account in the Microsoft 365 admin center, you can't use that account to create a mail user.</span></span>

<span data-ttu-id="1c443-111">La [méthode](#use-directory-synchronization-to-manage-mail-users) recommandée pour créer et gérer des utilisateurs de messagerie dans EOP autonome consiste à utiliser la synchronisation d’annuaires comme décrit dans la section Utiliser la synchronisation d’annuaires pour gérer les utilisateurs de messagerie plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1c443-111">The recommended method to create and manage mail users in standalone EOP is to use directory synchronization as described in the [Use directory synchronization to manage mail users](#use-directory-synchronization-to-manage-mail-users) section later in this article.</span></span>

<span data-ttu-id="1c443-112">Pour les organisations EOP autonomes avec un petit nombre d’utilisateurs, vous pouvez ajouter et gérer des utilisateurs de messagerie dans le Centre d’administration Exchange (CAE) ou dans EOP PowerShell autonome, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1c443-112">For standalone EOP organizations with a small number of users, you can add and manage mail users in the Exchange admin center (EAC) or in standalone EOP PowerShell as described in this article.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1c443-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1c443-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1c443-114">Pour ouvrir le Centre d’administration Exchange (CAE), consultez le Centre [d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="1c443-114">To open the Exchange admin center (EAC), see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="1c443-115">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="1c443-115">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="1c443-116">Lorsque vous créez des utilisateurs de messagerie dans EOP PowerShell, vous pouvez rencontrer une limitation.</span><span class="sxs-lookup"><span data-stu-id="1c443-116">When you create mail users in EOP PowerShell, you might encounter throttling.</span></span> <span data-ttu-id="1c443-117">En outre, les cmdlets EOP PowerShell utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes ne soient visibles.</span><span class="sxs-lookup"><span data-stu-id="1c443-117">Also, the EOP PowerShell cmdlets use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="1c443-118">Des autorisations doivent vous être attribuées dans Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="1c443-118">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="1c443-119">Plus précisément, vous avez besoin des **rôles** Création **(créer)** et Destinataires de messagerie (modifier),  qui sont affectés par défaut aux groupes de rôles Gestion de l’organisation **(administrateurs** globaux) et Gestion des destinataires.</span><span class="sxs-lookup"><span data-stu-id="1c443-119">Specifically, you need the **Mail Recipient Creation** (create) and **Mail Recipients** (modify) roles, which are assigned to the **Organization Management** (global admins) and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="1c443-120">Pour plus d’informations, voir Autorisations dans [EOP](feature-permissions-in-eop.md) autonome et utiliser le CAE pour modifier la liste des membres des [groupes de rôles.](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)</span><span class="sxs-lookup"><span data-stu-id="1c443-120">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="1c443-121">Pour plus d’informations sur les raccourcis clavier qui peuvent s’appliquer aux procédures de cet article, voir raccourcis clavier pour le Centre d’administration [Exchange dans Exchange Online.](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center)</span><span class="sxs-lookup"><span data-stu-id="1c443-121">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="1c443-122">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="1c443-122">Having problems?</span></span> <span data-ttu-id="1c443-123">Demandez de l’aide en participant aux forums Exchange.</span><span class="sxs-lookup"><span data-stu-id="1c443-123">Ask for help in the Exchange forums.</span></span> <span data-ttu-id="1c443-124">Visitez le forum [Exchange Online Protection.](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE)</span><span class="sxs-lookup"><span data-stu-id="1c443-124">Visit the [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) forum.</span></span>

## <a name="use-the-exchange-admin-center-to-manage-mail-users"></a><span data-ttu-id="1c443-125">Utiliser le Centre d’administration Exchange pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-125">Use the Exchange admin center to manage mail users</span></span>

### <a name="use-the-eac-to-create-mail-users"></a><span data-ttu-id="1c443-126">Utiliser le EAC pour créer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-126">Use the EAC to create mail users</span></span>

1. <span data-ttu-id="1c443-127">Dans le EAC, allez à **Contacts des** \> **destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c443-127">In the EAC, go to **Recipients** \> **Contacts**</span></span>

2. <span data-ttu-id="1c443-128">Cliquez **sur Nouvelle** ![ ](../../media/ITPro-EAC-AddIcon.png) icône.</span><span class="sxs-lookup"><span data-stu-id="1c443-128">Click **New** ![New icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="1c443-129">Dans la page **Nouvel utilisateur de messagerie** qui s’ouvre, configurez les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1c443-129">In the **New mail user** page that opens, configure the following settings.</span></span> <span data-ttu-id="1c443-130">Les paramètres marqués par un <sup>\*</sup> paramètre sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="1c443-130">Settings marked with an <sup>\*</sup> are required.</span></span>

   - <span data-ttu-id="1c443-131">**Prénom**</span><span class="sxs-lookup"><span data-stu-id="1c443-131">**First name**</span></span>

   - <span data-ttu-id="1c443-132">**Initiales :** initiale du deuxième milieu de la personne.</span><span class="sxs-lookup"><span data-stu-id="1c443-132">**Initials**: The person's middle initial.</span></span>

   - <span data-ttu-id="1c443-133">**Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="1c443-133">**Last name**</span></span>

   - <span data-ttu-id="1c443-134"><sup>\*</sup>**Nom d’affichage**: par défaut, cette zone affiche les **valeurs** des zones **Prénom,** Initiales **et** Nom.</span><span class="sxs-lookup"><span data-stu-id="1c443-134"><sup>\*</sup>**Display name**: By default, this box shows the values from the **First name**, **Initials**, and **Last name** boxes.</span></span> <span data-ttu-id="1c443-135">Vous pouvez accepter cette valeur ou la modifier.</span><span class="sxs-lookup"><span data-stu-id="1c443-135">You can accept this value or change it.</span></span> <span data-ttu-id="1c443-136">La valeur doit être unique et sa longueur maximale est de 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="1c443-136">The value should be unique, and has a maximum length of 64 characters.</span></span>

   - <span data-ttu-id="1c443-137"><sup>\*</sup>**Alias**: entrez un alias unique, en utilisant jusqu’à 64 caractères, pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c443-137"><sup>\*</sup>**Alias**: Enter a unique alias, using up to 64 characters, for the user</span></span>

   - <span data-ttu-id="1c443-138">**Adresse de messagerie externe**: entrez l’adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c443-138">**External email address**: Enter the user's email address.</span></span> <span data-ttu-id="1c443-139">Le domaine doit être externe à votre organisation informatique.</span><span class="sxs-lookup"><span data-stu-id="1c443-139">The domain should be external to your cloud-based organization.</span></span>

   - <span data-ttu-id="1c443-140"><sup>\*</sup>**ID d’utilisateur**: entrez le compte que la personne utilisera pour se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="1c443-140"><sup>\*</sup>**User ID**: Enter the account that the person will use to sign in to the service.</span></span> <span data-ttu-id="1c443-141">L’ID d’utilisateur se compose d’un nom d’utilisateur sur le côté gauche du symbole @) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="1c443-141">The user ID consists of a username on the left side of the at (@) symbol (@) and a domain on the right side.</span></span>

   - <span data-ttu-id="1c443-142"><sup>\*</sup>**Nouveau mot de passe** et confirmer le mot de passe : entrez et entrez de nouveau le mot de passe du <sup>\*</sup> compte.</span><span class="sxs-lookup"><span data-stu-id="1c443-142"><sup>\*</sup>**New password** and <sup>\*</sup>**Confirm password**: Enter and reenter the account password.</span></span> <span data-ttu-id="1c443-143">Vérifiez que le mot de passe est conforme aux exigences de longueur, de complexité et d’historique du mot de passe de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1c443-143">Verify that the password complies with the password length, complexity, and history requirements of your organization.</span></span>

3. <span data-ttu-id="1c443-144">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer l'utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c443-144">When you've finished, click **Save** to create the mail user.</span></span>

### <a name="use-the-eac-to-modify-mail-users"></a><span data-ttu-id="1c443-145">Utiliser le EAC pour modifier les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-145">Use the EAC to modify mail users</span></span>

1. <span data-ttu-id="1c443-146">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="1c443-146">In the EAC, go to **Recipients** \> **Contacts**.</span></span>

2. <span data-ttu-id="1c443-147">Sélectionnez l’utilisateur de messagerie à modifier, puis cliquez **sur** Modifier ![ l’icône ](../../media/ITPro-EAC-AddIcon.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="1c443-147">Select the mail user that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

3. <span data-ttu-id="1c443-148">Dans la page des propriétés de l’utilisateur de messagerie qui s’ouvre, cliquez sur l’un des onglets suivants pour afficher ou modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c443-148">On the mail user properties page that opens, click one of the following tabs to view or change properties.</span></span>

   <span data-ttu-id="1c443-149">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1c443-149">When you're finished, click **Save**.</span></span>

#### <a name="general"></a><span data-ttu-id="1c443-150">Général</span><span class="sxs-lookup"><span data-stu-id="1c443-150">General</span></span>

<span data-ttu-id="1c443-151">Utilisez **l’onglet Général** pour afficher ou modifier des informations de base sur l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c443-151">Use the **General** tab to view or change basic information about the mail user.</span></span>

- <span data-ttu-id="1c443-152">**Prénom**</span><span class="sxs-lookup"><span data-stu-id="1c443-152">**First name**</span></span>

- <span data-ttu-id="1c443-153">**Initiales**</span><span class="sxs-lookup"><span data-stu-id="1c443-153">**Initials**</span></span>

- <span data-ttu-id="1c443-154">**Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="1c443-154">**Last name**</span></span>

- <span data-ttu-id="1c443-155">**Nom d’affichage**: ce nom apparaît dans le carnet d’adresses de votre organisation, sur les lignes À : et De : du message électronique et dans la liste des contacts dans leAC.</span><span class="sxs-lookup"><span data-stu-id="1c443-155">**Display name**: This name appears in your organization's address book, on the To: and From: lines in email, and in the list of contacts in the EAC.</span></span> <span data-ttu-id="1c443-156">Ce nom ne peut pas contenir d'espaces vides avant ou après le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1c443-156">This name can't contain empty spaces before or after the display name.</span></span>

- <span data-ttu-id="1c443-157">**ID utilisateur**: il s’agit du compte de l’utilisateur dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c443-157">**User ID**: This is the user's account in Microsoft 365.</span></span> <span data-ttu-id="1c443-158">Vous ne pouvez pas modifier cette valeur ici.</span><span class="sxs-lookup"><span data-stu-id="1c443-158">You can't modify this value here.</span></span>

#### <a name="contact-information"></a><span data-ttu-id="1c443-159">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="1c443-159">Contact information</span></span>

<span data-ttu-id="1c443-160">Utilisez **l’onglet Informations de** contact pour afficher ou modifier les informations de contact de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c443-160">Use the **Contact information** tab to view or change the user's contact information.</span></span> <span data-ttu-id="1c443-161">L'information sur cette page s'affiche dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="1c443-161">The information on this page is displayed in the address book.</span></span>

- <span data-ttu-id="1c443-162">**Street**</span><span class="sxs-lookup"><span data-stu-id="1c443-162">**Street**</span></span>
- <span data-ttu-id="1c443-163">**Ville**</span><span class="sxs-lookup"><span data-stu-id="1c443-163">**City**</span></span>
- <span data-ttu-id="1c443-164">**État/Province**</span><span class="sxs-lookup"><span data-stu-id="1c443-164">**State/Province**</span></span>
- <span data-ttu-id="1c443-165">**Code postal**</span><span class="sxs-lookup"><span data-stu-id="1c443-165">**ZIP/Postal code**</span></span>
- <span data-ttu-id="1c443-166">**Pays**</span><span class="sxs-lookup"><span data-stu-id="1c443-166">**Country/Region**</span></span>
- <span data-ttu-id="1c443-167">**Téléphone de travail**</span><span class="sxs-lookup"><span data-stu-id="1c443-167">**Work phone**</span></span>
- <span data-ttu-id="1c443-168">**Téléphone portable**</span><span class="sxs-lookup"><span data-stu-id="1c443-168">**Mobile phone**</span></span>
- <span data-ttu-id="1c443-169">**Fax**</span><span class="sxs-lookup"><span data-stu-id="1c443-169">**Fax**</span></span>
- <span data-ttu-id="1c443-170">**Autres options**</span><span class="sxs-lookup"><span data-stu-id="1c443-170">**More options**</span></span>

  - <span data-ttu-id="1c443-171">**Bureau**</span><span class="sxs-lookup"><span data-stu-id="1c443-171">**Office**</span></span>
  - <span data-ttu-id="1c443-172">**Téléphone personnel**</span><span class="sxs-lookup"><span data-stu-id="1c443-172">**Home phone**</span></span>
  - <span data-ttu-id="1c443-173">**Page Web**</span><span class="sxs-lookup"><span data-stu-id="1c443-173">**Web page**</span></span>
  - <span data-ttu-id="1c443-174">**Notes**</span><span class="sxs-lookup"><span data-stu-id="1c443-174">**Notes**</span></span>

#### <a name="organization"></a><span data-ttu-id="1c443-175">Organisation</span><span class="sxs-lookup"><span data-stu-id="1c443-175">Organization</span></span>

<span data-ttu-id="1c443-176">Utilisez **l’onglet** Organisation pour enregistrer des informations détaillées sur le rôle de l’utilisateur dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1c443-176">Use the **Organization** tab to record detailed information about the user's role in the organization.</span></span>

- <span data-ttu-id="1c443-177">**Poste**</span><span class="sxs-lookup"><span data-stu-id="1c443-177">**Title**</span></span>
- <span data-ttu-id="1c443-178">**Service**</span><span class="sxs-lookup"><span data-stu-id="1c443-178">**Department**</span></span>
- <span data-ttu-id="1c443-179">**Entreprise**</span><span class="sxs-lookup"><span data-stu-id="1c443-179">**Company**</span></span>

### <a name="use-the-eac-to-remove-mail-users"></a><span data-ttu-id="1c443-180">Utiliser le EAC pour supprimer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-180">Use the EAC to remove mail users</span></span>

1. <span data-ttu-id="1c443-181">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="1c443-181">In the EAC, go to **Recipients** \> **Contacts**.</span></span>

2. <span data-ttu-id="1c443-182">Sélectionnez l’utilisateur de messagerie à supprimer, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="1c443-182">Select the mail user that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

## <a name="use-powershell-to-manage-mail-users"></a><span data-ttu-id="1c443-183">Utiliser PowerShell pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-183">Use PowerShell to manage mail users</span></span>

### <a name="use-standalone-eop-powershell-to-view-mail-users"></a><span data-ttu-id="1c443-184">Utiliser EOP PowerShell autonome pour afficher les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-184">Use standalone EOP PowerShell to view mail users</span></span>

<span data-ttu-id="1c443-185">Pour renvoyer une liste récapitulatif de tous les utilisateurs de messagerie dans EOP PowerShell autonome, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1c443-185">To return a summary list of all mail users in standalone EOP PowerShell, run the following command:</span></span>

```powershell
Get-Recipient -RecipientType MailUser -ResultSize unlimited
```

<span data-ttu-id="1c443-186">Pour afficher des informations détaillées sur un utilisateur de messagerie spécifique, remplacez-le par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez les \<MailUserIdentity\> commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c443-186">To view detailed information about a specific mail user, replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following commands:</span></span>

```powershell
Get-Recipient -Identity <MailUserIdentity> | Format-List
```

```powershell
Get-User -Identity <MailUserIdentity> | Format-List
```

<span data-ttu-id="1c443-187">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) et [Get-User.](https://docs.microsoft.com/powershell/module/exchange/get-user)</span><span class="sxs-lookup"><span data-stu-id="1c443-187">For detailed syntax and parameter information, see [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) and [Get-User](https://docs.microsoft.com/powershell/module/exchange/get-user).</span></span>

### <a name="use-standalone-eop-powershell-to-create-mail-users"></a><span data-ttu-id="1c443-188">Utiliser EOP PowerShell autonome pour créer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-188">Use standalone EOP PowerShell to create mail users</span></span>

<span data-ttu-id="1c443-189">Pour créer des utilisateurs de messagerie dans EOP PowerShell autonome, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1c443-189">To create mail users in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
New-EOPMailUser -Name "<UniqueName>" -MicrosoftOnlineServicesID <Account> -Password (ConvertTo-SecureString -String '<password>' -AsPlainText -Force) [-Alias <AliasValue>] [-DisplayName "<Display Name>"] [-ExternalEmailAddress <ExternalEmailAddress>] [-FirstName <Text>] [-Initials <Text>] [-LastName <Text>]
```

<span data-ttu-id="1c443-190">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="1c443-190">**Notes**:</span></span>

- <span data-ttu-id="1c443-191">Le _paramètre Name_ est obligatoire, a une longueur maximale de 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="1c443-191">The _Name_ parameter is required, has a maximum length of 64 characters, and must be unique.</span></span> <span data-ttu-id="1c443-192">Si vous n’utilisez pas le paramètre _DisplayName_, la valeur du paramètre _Name_ est utilisée pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="1c443-192">If you don't use the _DisplayName_ parameter, the value of the _Name_ parameter is used for the display name.</span></span>
- <span data-ttu-id="1c443-193">Si vous n’utilisez pas le paramètre _Alias,_ le côté gauche du paramètre _MicrosoftOnlineServicesID_ est utilisé pour l’alias.</span><span class="sxs-lookup"><span data-stu-id="1c443-193">If you don't use the _Alias_ parameter, the left side of the _MicrosoftOnlineServicesID_ parameter is used for the alias.</span></span>
- <span data-ttu-id="1c443-194">Si vous n’utilisez pas le _paramètre ExternalEmailAddress,_ la valeur _MicrosoftOnlineServicesID_ est utilisée pour l’adresse de messagerie externe.</span><span class="sxs-lookup"><span data-stu-id="1c443-194">If you don't use the _ExternalEmailAddress_ parameter, the _MicrosoftOnlineServicesID_ value is used for the external email address.</span></span>

<span data-ttu-id="1c443-195">Cet exemple crée un utilisateur de messagerie avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c443-195">This example creates a mail user with the following settings:</span></span>

- <span data-ttu-id="1c443-196">Le nom est JeffreyZeng et le nom complet est Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="1c443-196">The name is JeffreyZeng and the display name is Jeffrey Zeng.</span></span>
- <span data-ttu-id="1c443-197">Le prénom est Jeffrey et le nom est Zeng.</span><span class="sxs-lookup"><span data-stu-id="1c443-197">The first name is Jeffrey and the last name is Zeng.</span></span>
- <span data-ttu-id="1c443-198">L'alias est jeffreyz.</span><span class="sxs-lookup"><span data-stu-id="1c443-198">The alias is jeffreyz.</span></span>
- <span data-ttu-id="1c443-199">L'adresse de messagerie externe est jzeng@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="1c443-199">The external email address is jzeng@tailspintoys.com.</span></span>
- <span data-ttu-id="1c443-200">Le nom du compte est jeffreyz@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="1c443-200">The account name is jeffreyz@contoso.onmicrosoft.com.</span></span>
- <span data-ttu-id="1c443-201">Le mot de passe est Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="1c443-201">The password is Pa$$word1.</span></span>

```PowerShell
New-EOPMailUser -Name JeffreyZeng -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force) -ExternalEmailAddress jeffreyz@tailspintoys.com -DisplayName "Jeffrey Zeng" -Alias jeffreyz -FirstName Jeffrey -LastName Zeng
```

<span data-ttu-id="1c443-202">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/new-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="1c443-202">For detailed syntax and parameter information, see [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/new-eopmailuser).</span></span>

### <a name="use-standalone-eop-powershell-to-modify-mail-users"></a><span data-ttu-id="1c443-203">Utiliser EOP PowerShell autonome pour modifier les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-203">Use standalone EOP PowerShell to modify mail users</span></span>

<span data-ttu-id="1c443-204">Pour modifier les utilisateurs de messagerie existants dans EOP PowerShell autonome, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1c443-204">To modify existing mail users in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
Set-EOPMailUser -Identity <MailUserIdentity> [-Alias <Text>] [-DisplayName <Text>] [-EmailAddresses <ProxyAddressCollection>] [-MicrosoftOnlineServicesID <SmtpAddress>]
```

```powershell
Set-EOPUser -Identity <MailUserIdentity> [-City <Text>] [-Company <Text>] [-CountryOrRegion <CountryInfo>] [-Department <Text>] [-Fax <PhoneNumber>] [-FirstName <Text>] [-HomePhone <PhoneNumber>] [-Initials <Text>] [-LastName <Text>] [-MobilePhone <PhoneNumber>] [-Notes <Text>] [-Office <Text>] [-Phone <PhoneNumber>] [-PostalCode <String>] [-StateOrProvince <String>] [-StreetAddress <Tet>] [-Title <Text>] [-WebPage <Text>]
```

<span data-ttu-id="1c443-205">Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="1c443-205">This example sets the external email address for Pilar Pinilla.</span></span>

```PowerShell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="1c443-206">Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c443-206">This example sets the Company property for all mail users to Contoso.</span></span>

```PowerShell
$Recip = Get-Recipient -RecipientType MailUser -ResultSize unlimited
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```

<span data-ttu-id="1c443-207">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/set-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="1c443-207">For detailed syntax and parameter information, see [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/set-eopmailuser).</span></span>

### <a name="use-standalone-eop-powershell-to-remove-mail-users"></a><span data-ttu-id="1c443-208">Utiliser EOP PowerShell autonome pour supprimer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-208">Use standalone EOP PowerShell to remove mail users</span></span>

<span data-ttu-id="1c443-209">Pour supprimer des utilisateurs de messagerie dans EOP PowerShell autonome, remplacez-les par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez \<MailUserIdentity\> la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1c443-209">To remove mail users in standalone EOP PowerShell, replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following command:</span></span>

```PowerShell
Remove-EOPMailUser -Identity <MailUserIdentity\>
```

<span data-ttu-id="1c443-210">Cet exemple supprime l’utilisateur de messagerie pour Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="1c443-210">This example removes the mail user for Jeffrey Zeng.</span></span>

```PowerShell
Remove-EOPMailUser -Identity "Jeffrey Zeng"
```

<span data-ttu-id="1c443-211">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/remove-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="1c443-211">For detailed syntax and parameter information, see [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/remove-eopmailuser).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="1c443-212">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="1c443-212">How do you know these procedures worked?</span></span>

<span data-ttu-id="1c443-213">Pour vérifier que vous avez correctement créé, modifié ou supprimé des utilisateurs de messagerie dans EOP autonome, utilisez l’une des procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c443-213">To verify that you've successfully created, modified, or removed mail users in standalone EOP, use any of the following procedures:</span></span>

- <span data-ttu-id="1c443-214">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="1c443-214">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="1c443-215">Vérifiez que l’utilisateur de messagerie est répertorié (ou n’est pas répertorié).</span><span class="sxs-lookup"><span data-stu-id="1c443-215">Verify that the mail user is listed (or isn't listed).</span></span> <span data-ttu-id="1c443-216">Sélectionnez l’utilisateur de messagerie et affichez les  informations dans le volet Détails, ou cliquez sur Modifier l’icône ![ Modifier pour afficher les ](../../media/ITPro-EAC-AddIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="1c443-216">Select the mail user and view the information in the Details pane, or click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png) to view the settings.</span></span>

- <span data-ttu-id="1c443-217">Dans EOP PowerShell autonome, exécutez la commande suivante pour vérifier que l’utilisateur de messagerie est répertorié (ou n’est pas répertorié) :</span><span class="sxs-lookup"><span data-stu-id="1c443-217">In standalone EOP PowerShell, run the following command to verify the mail user is listed (or isn't listed):</span></span>

  ```powershell
  Get-Recipient -RecipientType MailUser -ResultSize unlimited
  ```

- <span data-ttu-id="1c443-218">Remplacez-le par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez les commandes \<MailUserIdentity\> suivantes pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="1c443-218">Replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following commands to verify the settings:</span></span>

  ```powershell
  Get-Recipient -Identity <MailUserIdentity> | Format-List
  ```

  ```powershell
  Get-User -Identity <MailUserIdentity> | Format-List
  ```

## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="1c443-219">Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c443-219">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="1c443-220">Dans EOP autonome, la synchronisation d’annuaires est disponible pour les clients avec Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="1c443-220">In standalone EOP, directory synchronization is available for customers with on-premises Active Directory.</span></span> <span data-ttu-id="1c443-221">Vous pouvez synchroniser ces comptes avec Azure Active Directory (Azure AD), où les copies des comptes sont stockées dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="1c443-221">You can synchronize those accounts to Azure Active Directory (Azure AD), where copies of the accounts are stored in the cloud.</span></span> <span data-ttu-id="1c443-222">Lorsque vous synchronisez vos comptes d’utilisateur existants avec Azure Active Directory, vous pouvez afficher ces utilisateurs dans le volet **Destinataires** du Centre d’administration Exchange (CAE) ou dans EOP PowerShell autonome.</span><span class="sxs-lookup"><span data-stu-id="1c443-222">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC) or in standalone EOP PowerShell.</span></span>

<span data-ttu-id="1c443-223">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="1c443-223">**Notes**:</span></span>

- <span data-ttu-id="1c443-224">Si vous utilisez la synchronisation d’annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le Centre d’administration Microsoft 365, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="1c443-224">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="1c443-225">En effet, la synchronisation d’annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage.</span><span class="sxs-lookup"><span data-stu-id="1c443-225">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span>

- <span data-ttu-id="1c443-226">Il est recommandé d’utiliser la synchronisation d’annuaires avec les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c443-226">Using directory synchronization is recommended for use with the following features:</span></span>

  - <span data-ttu-id="1c443-227">**Listes d’expéditeurs sûrs Outlook** et expéditeurs bloqués : lorsqu’elles sont synchronisées avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service.</span><span class="sxs-lookup"><span data-stu-id="1c443-227">**Outlook Safe Sender lists and Blocked Sender lists**: When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="1c443-228">Cela permet aux utilisateurs de gérer leurs propres listes d’expéditeurs sûrs et d’expéditeurs bloqués avec des entrées d’expéditeur et de domaine individuelles.</span><span class="sxs-lookup"><span data-stu-id="1c443-228">This lets users manage their own Safe Sender list and Blocked Sender list with individual sender and domain entries.</span></span> <span data-ttu-id="1c443-229">Pour plus d’informations, voir [Configurer les paramètres du courrier indésirable sur les boîtes aux lettres Exchange Online](configure-junk-email-settings-on-exo-mailboxes.md).</span><span class="sxs-lookup"><span data-stu-id="1c443-229">For more information, see [Configure junk email settings on Exchange Online mailboxes](configure-junk-email-settings-on-exo-mailboxes.md).</span></span>

  - <span data-ttu-id="1c443-230">Blocage du périphérie basé sur l’annuaire **(DBEB)**: pour plus d’informations sur DBEB, voir Utiliser le blocage de périphérie basé sur l’annuaire pour rejeter les messages envoyés à des [destinataires non valides.](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-directory-based-edge-blocking)</span><span class="sxs-lookup"><span data-stu-id="1c443-230">**Directory Based Edge Blocking (DBEB)**: For more information about DBEB, see [Use Directory Based Edge Blocking to reject messages sent to invalid recipients](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-directory-based-edge-blocking).</span></span>

  - <span data-ttu-id="1c443-231">**Accès des utilisateurs finaux** à la mise en quarantaine : pour accéder à leurs messages mis en quarantaine, les destinataires doivent avoir un ID d’utilisateur et un mot de passe valides dans le service.</span><span class="sxs-lookup"><span data-stu-id="1c443-231">**End user access to quarantine**: To access their quarantined messages, recipients must have a valid user ID and password in the service.</span></span> <span data-ttu-id="1c443-232">Pour plus d’informations sur la mise en quarantaine, voir Rechercher et libérer les messages mis en [quarantaine en tant qu’utilisateur.](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="1c443-232">For more information about quarantine, see [Find and release quarantined messages as a user](find-and-release-quarantined-messages-as-a-user.md).</span></span>

  - <span data-ttu-id="1c443-233">Règles de flux de messagerie (également appelées règles de **transport)**: lorsque vous utilisez la synchronisation d’annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement chargés dans le cloud, et vous pouvez ensuite créer des règles de flux de messagerie qui ciblent des utilisateurs et/ou des groupes spécifiques sans avoir à les ajouter manuellement dans le service.</span><span class="sxs-lookup"><span data-stu-id="1c443-233">**Mail flow rules (also known as transport rules)**: When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules that target specific users and/or groups without having to manually add them in the service.</span></span> <span data-ttu-id="1c443-234">Notez [que les groupes de distribution](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-dynamic-distribution-groups/manage-dynamic-distribution-groups) dynamique ne peuvent pas être synchronisés via la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="1c443-234">Note that [dynamic distribution groups](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-dynamic-distribution-groups/manage-dynamic-distribution-groups) can't be synchronized via directory synchronization.</span></span>

<span data-ttu-id="1c443-235">Obtenez les autorisations nécessaires et préparez-vous à la synchronisation d’annuaires, comme décrit dans qu’est-ce que l’identité [hybride avec Azure Active Directory ?](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-hybrid-identity)</span><span class="sxs-lookup"><span data-stu-id="1c443-235">Get the necessary permissions and prepare for directory synchronization, as described in [What is hybrid identity with Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-hybrid-identity).</span></span>

### <a name="synchronize-directories-with-azure-active-directory-connect-aad-connect"></a><span data-ttu-id="1c443-236">Synchroniser des répertoires avec Azure Active Directory Connect (AAD Connect)</span><span class="sxs-lookup"><span data-stu-id="1c443-236">Synchronize directories with Azure Active Directory Connect (AAD Connect)</span></span>

1. <span data-ttu-id="1c443-237">Activez la synchronisation d’annuaires comme décrit dans la synchronisation Azure AD Connect : comprendre [et personnaliser la synchronisation.](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis)</span><span class="sxs-lookup"><span data-stu-id="1c443-237">Activate directory synchronization as described in [Azure AD Connect sync: Understand and customize synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span></span>

2. <span data-ttu-id="1c443-238">Installez et configurez un ordinateur local pour exécuter AAD Connect, comme décrit dans les conditions [préalables pour Azure AD Connect.](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)</span><span class="sxs-lookup"><span data-stu-id="1c443-238">Install and configure an on-premises computer to run AAD Connect as described in [Prerequisites for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites).</span></span>

3. <span data-ttu-id="1c443-239">[Sélectionnez le type d’installation à utiliser pour Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation):</span><span class="sxs-lookup"><span data-stu-id="1c443-239">[Select which installation type to use for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation):</span></span>

   - [<span data-ttu-id="1c443-240">Express</span><span class="sxs-lookup"><span data-stu-id="1c443-240">Express</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)

   - [<span data-ttu-id="1c443-241">Custom</span><span class="sxs-lookup"><span data-stu-id="1c443-241">Custom</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)

   - [<span data-ttu-id="1c443-242">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="1c443-242">Pass-through authentication</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start)

> [!IMPORTANT]
> <span data-ttu-id="1c443-p121">Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site.</span><span class="sxs-lookup"><span data-stu-id="1c443-p121">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span>

<span data-ttu-id="1c443-246">Après avoir configuré votre synchronisation, vérifiez qu’AAD Connect se synchronise correctement.</span><span class="sxs-lookup"><span data-stu-id="1c443-246">After configuring your sync, be sure to verify that AAD Connect is synchronizing correctly.</span></span> <span data-ttu-id="1c443-247">Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="1c443-247">In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span>
