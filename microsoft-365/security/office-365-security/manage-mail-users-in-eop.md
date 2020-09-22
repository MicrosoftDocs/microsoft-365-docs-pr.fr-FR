---
title: Gérer les utilisateurs de courrier dans une version autonome de EOP
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
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: Découvrez comment gérer les utilisateurs de messagerie dans Exchange Online Protection (EOP), notamment à l’aide de la synchronisation d’annuaires, du centre d’administration Exchange et de PowerShell pour gérer les utilisateurs.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 56e6f8955b5993fb4b5064aa92cdde80a4c67ffe
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201782"
---
# <a name="manage-mail-users-in-standalone-eop"></a><span data-ttu-id="6175f-103">Gérer les utilisateurs de courrier dans une version autonome de EOP</span><span class="sxs-lookup"><span data-stu-id="6175f-103">Manage mail users in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="6175f-104">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, les utilisateurs de messagerie constituent le type de compte d’utilisateur fondamental.</span><span class="sxs-lookup"><span data-stu-id="6175f-104">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, mail users are the fundamental type of user account.</span></span> <span data-ttu-id="6175f-105">Un utilisateur de messagerie dispose d’informations d’identification de compte dans votre organisation EOP autonome et peut accéder aux ressources (auxquelles des autorisations sont attribuées).</span><span class="sxs-lookup"><span data-stu-id="6175f-105">A mail user has account credentials in your standalone EOP organization, and can access resources (have permissions assigned).</span></span> <span data-ttu-id="6175f-106">L’adresse de messagerie d’un utilisateur de messagerie est externe (par exemple, dans votre environnement de messagerie local).</span><span class="sxs-lookup"><span data-stu-id="6175f-106">A mail user's email address is external (for example, in your on-premises email environment).</span></span>

> [!NOTE]
> <span data-ttu-id="6175f-107">Lorsque vous créez un utilisateur de messagerie, le compte d’utilisateur correspondant est disponible dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6175f-107">When you create a mail user, the corresponding user account is available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="6175f-108">Lorsque vous créez un compte d’utilisateur dans le centre d’administration 365 de Microsoft, vous ne pouvez pas utiliser ce compte pour créer un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6175f-108">When you create a user account in the Microsoft 365 admin center, you can't use that account to create a mail user.</span></span>

<span data-ttu-id="6175f-109">La méthode recommandée pour créer et gérer des utilisateurs de messagerie en mode autonome EOP consiste à utiliser la synchronisation d’annuaires comme décrit dans la section [utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie](#use-directory-synchronization-to-manage-mail-users) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6175f-109">The recommended method to create and manage mail users in standalone EOP is to use directory synchronization as described in the [Use directory synchronization to manage mail users](#use-directory-synchronization-to-manage-mail-users) section later in this topic.</span></span>

<span data-ttu-id="6175f-110">Pour les organisations EOP autonomes avec un petit nombre d’utilisateurs, vous pouvez ajouter et gérer des utilisateurs de messagerie dans le centre d’administration Exchange ou dans une version PowerShell d’EOP autonome comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6175f-110">For standalone EOP organizations with a small number of users, you can add and manage mail users in the Exchange admin center (EAC) or in standalone EOP PowerShell as described in this topic.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6175f-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6175f-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6175f-112">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="6175f-112">To open the Exchange admin center (EAC), see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="6175f-113">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="6175f-113">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="6175f-114">Lorsque vous créez des utilisateurs de messagerie dans EOP PowerShell, il se peut que vous rencontriez une limitation.</span><span class="sxs-lookup"><span data-stu-id="6175f-114">When you create mail users in EOP PowerShell, you might encounter throttling.</span></span> <span data-ttu-id="6175f-115">En outre, les cmdlets PowerShell d’EOP utilisent une méthode de traitement par lots qui entraîne un délai de propagation de quelques minutes avant que les résultats des commandes soient visibles.</span><span class="sxs-lookup"><span data-stu-id="6175f-115">Also, the EOP PowerShell cmdlets use a batch processing method that results in a propagation delay of a few minutes before the results of the commands are visible.</span></span>

- <span data-ttu-id="6175f-116">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="6175f-116">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="6175f-117">Plus précisément, vous avez besoin des rôles création du destinataire de messagerie (création) et destinataires (modifier), qui sont attribués aux groupes de rôles OrganizationManagement (administrateurs globaux) et RecipientManagement par défaut.</span><span class="sxs-lookup"><span data-stu-id="6175f-117">Specifically, you need the Mail Recipient Creation (create) and Mail Recipients (modify) roles, which are assigned to the OrganizationManagement (global admins) and RecipientManagement role groups by default.</span></span> <span data-ttu-id="6175f-118">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="6175f-118">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="6175f-119">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="6175f-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="6175f-120">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="6175f-120">Having problems?</span></span> <span data-ttu-id="6175f-121">Demandez de l’aide en participant aux forums Exchange.</span><span class="sxs-lookup"><span data-stu-id="6175f-121">Ask for help in the Exchange forums.</span></span> <span data-ttu-id="6175f-122">Visitez le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="6175f-122">Visit the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-exchange-admin-center-to-manage-mail-users"></a><span data-ttu-id="6175f-123">Utiliser le centre d’administration Exchange pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-123">Use the Exchange admin center to manage mail users</span></span>

### <a name="use-the-eac-to-create-mail-users"></a><span data-ttu-id="6175f-124">Utiliser le centre d’administration Exchange pour créer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-124">Use the EAC to create mail users</span></span>

1. <span data-ttu-id="6175f-125">Dans le centre d’administration Exchange, accédez à contacts des **destinataires** \> **Contacts**</span><span class="sxs-lookup"><span data-stu-id="6175f-125">In the EAC, go to **Recipients** \> **Contacts**</span></span>

2. <span data-ttu-id="6175f-126">Cliquez sur **nouvelle** ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="6175f-126">Click **New** ![New icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="6175f-127">Dans la page **nouvel utilisateur de messagerie** qui s’ouvre, configurez les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="6175f-127">In the **New mail user** page that opens, configure the following settings.</span></span> <span data-ttu-id="6175f-128">Les paramètres marqués par un <sup>\*</sup> sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="6175f-128">Settings marked with an <sup>\*</sup> are required.</span></span>

   - <span data-ttu-id="6175f-129">**Prénom**</span><span class="sxs-lookup"><span data-stu-id="6175f-129">**First name**</span></span>

   - <span data-ttu-id="6175f-130">**Initiales**: initiale du deuxième prénom de la personne.</span><span class="sxs-lookup"><span data-stu-id="6175f-130">**Initials**: The person's middle initial.</span></span>

   - <span data-ttu-id="6175f-131">**Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="6175f-131">**Last name**</span></span>

   - <span data-ttu-id="6175f-132"><sup>\*</sup>**Nom d’affichage**: par défaut, cette zone affiche les valeurs des **zones Prénom**, **initiales**et nom de **famille** .</span><span class="sxs-lookup"><span data-stu-id="6175f-132"><sup>\*</sup>**Display name**: By default, this box shows the values from the **First name**, **Initials**, and **Last name** boxes.</span></span> <span data-ttu-id="6175f-133">Vous pouvez accepter cette valeur ou la modifier.</span><span class="sxs-lookup"><span data-stu-id="6175f-133">You can accept this value or change it.</span></span> <span data-ttu-id="6175f-134">La valeur doit être unique et sa longueur maximale est de 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="6175f-134">The value should be unique, and has a maximum length of 64 characters.</span></span>

   - <span data-ttu-id="6175f-135"><sup>\*</sup>**Alias**: entrez un alias unique, en utilisant jusqu’à 64 caractères, pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6175f-135"><sup>\*</sup>**Alias**: Enter a unique alias, using up to 64 characters, for the user</span></span>

   - <span data-ttu-id="6175f-136">**Adresse de messagerie externe**: entrez l’adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6175f-136">**External email address**: Enter the user's email address.</span></span> <span data-ttu-id="6175f-137">Le domaine doit être externe à votre organisation en nuage.</span><span class="sxs-lookup"><span data-stu-id="6175f-137">The domain should be external to your cloud-based organization.</span></span>

   - <span data-ttu-id="6175f-138"><sup>\*</sup>**ID d’utilisateur**: entrez le compte que la personne utilisera pour se connecter au service.</span><span class="sxs-lookup"><span data-stu-id="6175f-138"><sup>\*</sup>**User ID**: Enter the account that the person will use to sign in to the service.</span></span> <span data-ttu-id="6175f-139">L’ID d’utilisateur est constitué d’un nom d’utilisateur à gauche du symbole arobas (@) et d’un domaine sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="6175f-139">The user ID consists of a username on the left side of the at (@) symbol (@) and a domain on the right side.</span></span>

   - <span data-ttu-id="6175f-140"><sup>\*</sup>**Nouveau mot de** passe et <sup>\*</sup> **confirmer le mot de passe**: entrez et entrez à nouveau le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="6175f-140"><sup>\*</sup>**New password** and <sup>\*</sup>**Confirm password**: Enter and reenter the account password.</span></span> <span data-ttu-id="6175f-141">Vérifiez que le mot de passe est conforme aux exigences de longueur, de complexité et d’historique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6175f-141">Verify that the password complies with the password length, complexity, and history requirements of your organization.</span></span>

3. <span data-ttu-id="6175f-142">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer l'utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6175f-142">When you've finished, click **Save** to create the mail user.</span></span>

### <a name="use-the-eac-to-modify-mail-users"></a><span data-ttu-id="6175f-143">Utiliser le centre d’administration Exchange pour modifier les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-143">Use the EAC to modify mail users</span></span>

1. <span data-ttu-id="6175f-144">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="6175f-144">In the EAC, go to **Recipients** \> **Contacts**.</span></span>

2. <span data-ttu-id="6175f-145">Sélectionnez l’utilisateur de messagerie à modifier, puis cliquez sur modifier l' **Edit** ![ icône modifier ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="6175f-145">Select the mail user that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

3. <span data-ttu-id="6175f-146">Sur la page Propriétés de l’utilisateur de messagerie qui s’ouvre, cliquez sur l’un des onglets suivants pour afficher ou modifier les propriétés.</span><span class="sxs-lookup"><span data-stu-id="6175f-146">On the mail user properties page that opens, click one of the following tabs to view or change properties.</span></span>

   <span data-ttu-id="6175f-147">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6175f-147">When you're finished, click **Save**.</span></span>

#### <a name="general"></a><span data-ttu-id="6175f-148">Général</span><span class="sxs-lookup"><span data-stu-id="6175f-148">General</span></span>

<span data-ttu-id="6175f-149">Utilisez l’onglet **général** pour afficher ou modifier des informations de base sur l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6175f-149">Use the **General** tab to view or change basic information about the mail user.</span></span>

- <span data-ttu-id="6175f-150">**Prénom**</span><span class="sxs-lookup"><span data-stu-id="6175f-150">**First name**</span></span>

- <span data-ttu-id="6175f-151">**Initiales**</span><span class="sxs-lookup"><span data-stu-id="6175f-151">**Initials**</span></span>

- <span data-ttu-id="6175f-152">**Nom de famille**</span><span class="sxs-lookup"><span data-stu-id="6175f-152">**Last name**</span></span>

- <span data-ttu-id="6175f-153">**Nom d’affichage**: ce nom s’affiche dans le carnet d’adresses de votre organisation, sur les lignes à : et de : dans le courrier électronique, et dans la liste des contacts du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="6175f-153">**Display name**: This name appears in your organization's address book, on the To: and From: lines in email, and in the list of contacts in the EAC.</span></span> <span data-ttu-id="6175f-154">Ce nom ne peut pas contenir d'espaces vides avant ou après le nom complet.</span><span class="sxs-lookup"><span data-stu-id="6175f-154">This name can't contain empty spaces before or after the display name.</span></span>

- <span data-ttu-id="6175f-155">**ID utilisateur**: il s’agit du compte de l’utilisateur dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6175f-155">**User ID**: This is the user's account in Microsoft 365.</span></span> <span data-ttu-id="6175f-156">Vous ne pouvez pas modifier cette valeur ici.</span><span class="sxs-lookup"><span data-stu-id="6175f-156">You can't modify this value here.</span></span>

#### <a name="contact-information"></a><span data-ttu-id="6175f-157">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="6175f-157">Contact information</span></span>

<span data-ttu-id="6175f-158">L’onglet **informations** sur le contact permet d’afficher ou de modifier les informations de contact de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6175f-158">Use the **Contact information** tab to view or change the user's contact information.</span></span> <span data-ttu-id="6175f-159">L'information sur cette page s'affiche dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="6175f-159">The information on this page is displayed in the address book.</span></span>

- <span data-ttu-id="6175f-160">**Street**</span><span class="sxs-lookup"><span data-stu-id="6175f-160">**Street**</span></span>
- <span data-ttu-id="6175f-161">**Ville**</span><span class="sxs-lookup"><span data-stu-id="6175f-161">**City**</span></span>
- <span data-ttu-id="6175f-162">**État/Province**</span><span class="sxs-lookup"><span data-stu-id="6175f-162">**State/Province**</span></span>
- <span data-ttu-id="6175f-163">**Code postal**</span><span class="sxs-lookup"><span data-stu-id="6175f-163">**ZIP/Postal code**</span></span>
- <span data-ttu-id="6175f-164">**Pays**</span><span class="sxs-lookup"><span data-stu-id="6175f-164">**Country/Region**</span></span>
- <span data-ttu-id="6175f-165">**Téléphone professionnel**</span><span class="sxs-lookup"><span data-stu-id="6175f-165">**Work phone**</span></span>
- <span data-ttu-id="6175f-166">\*\*Téléphone portable \*\*</span><span class="sxs-lookup"><span data-stu-id="6175f-166">**Mobile phone**</span></span>
- <span data-ttu-id="6175f-167">**Fax**</span><span class="sxs-lookup"><span data-stu-id="6175f-167">**Fax**</span></span>
- <span data-ttu-id="6175f-168">**Autres options**</span><span class="sxs-lookup"><span data-stu-id="6175f-168">**More options**</span></span>

  - <span data-ttu-id="6175f-169">**Bureau**</span><span class="sxs-lookup"><span data-stu-id="6175f-169">**Office**</span></span>
  - <span data-ttu-id="6175f-170">\*\*Téléphone personnel \*\*</span><span class="sxs-lookup"><span data-stu-id="6175f-170">**Home phone**</span></span>
  - <span data-ttu-id="6175f-171">**Page Web**</span><span class="sxs-lookup"><span data-stu-id="6175f-171">**Web page**</span></span>
  - <span data-ttu-id="6175f-172">**Notes**</span><span class="sxs-lookup"><span data-stu-id="6175f-172">**Notes**</span></span>

#### <a name="organization"></a><span data-ttu-id="6175f-173">Organisation</span><span class="sxs-lookup"><span data-stu-id="6175f-173">Organization</span></span>

<span data-ttu-id="6175f-174">L’onglet **organisation** permet d’enregistrer des informations détaillées sur le rôle de l’utilisateur dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6175f-174">Use the **Organization** tab to record detailed information about the user's role in the organization.</span></span>

- <span data-ttu-id="6175f-175">**Poste**</span><span class="sxs-lookup"><span data-stu-id="6175f-175">**Title**</span></span>
- <span data-ttu-id="6175f-176">**Service**</span><span class="sxs-lookup"><span data-stu-id="6175f-176">**Department**</span></span>
- <span data-ttu-id="6175f-177">**Entreprise**</span><span class="sxs-lookup"><span data-stu-id="6175f-177">**Company**</span></span>

### <a name="use-the-eac-to-remove-mail-users"></a><span data-ttu-id="6175f-178">Utiliser le centre d’administration Exchange pour supprimer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-178">Use the EAC to remove mail users</span></span>

1. <span data-ttu-id="6175f-179">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="6175f-179">In the EAC, go to **Recipients** \> **Contacts**.</span></span>

2. <span data-ttu-id="6175f-180">Sélectionnez l’utilisateur de messagerie à supprimer, puis cliquez sur supprimer l' **Remove** ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="6175f-180">Select the mail user that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

## <a name="use-powershell-to-manage-mail-users"></a><span data-ttu-id="6175f-181">Utiliser PowerShell pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-181">Use PowerShell to manage mail users</span></span>

### <a name="use-standalone-eop-powershell-to-view-mail-users"></a><span data-ttu-id="6175f-182">Utilisation d’EOP PowerShell autonome pour afficher les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-182">Use standalone EOP PowerShell to view mail users</span></span>

<span data-ttu-id="6175f-183">Pour renvoyer une liste récapitulative de tous les utilisateurs de messagerie dans une version autonome d’EOP PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6175f-183">To return a summary list of all mail users in standalone EOP PowerShell, run the following command:</span></span>

```powershell
Get-Recipient -RecipientType MailUser -ResultSize unlimited
```

<span data-ttu-id="6175f-184">Pour afficher des informations détaillées sur un utilisateur de messagerie spécifique, remplacez \<MailUserIdentity\> par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6175f-184">To view detailed information about a specific mail user, replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following commands:</span></span>

```powershell
Get-Recipient -Identity <MailUserIdentity> | Format-List
```

```powershell
Get-User -Identity <MailUserIdentity> | Format-List
```

<span data-ttu-id="6175f-185">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) et [Get-User](https://docs.microsoft.com/powershell/module/exchange/get-user).</span><span class="sxs-lookup"><span data-stu-id="6175f-185">For detailed syntax and parameter information, see [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/get-recipient) and [Get-User](https://docs.microsoft.com/powershell/module/exchange/get-user).</span></span>

### <a name="use-standalone-eop-powershell-to-create-mail-users"></a><span data-ttu-id="6175f-186">Utilisation d’EOP PowerShell autonome pour créer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-186">Use standalone EOP PowerShell to create mail users</span></span>

<span data-ttu-id="6175f-187">Pour créer des utilisateurs de messagerie dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6175f-187">To create mail users in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
New-EOPMailUser -Name "<UniqueName>" -MicrosoftOnlineServicesID <Account> -Password (ConvertTo-SecureString -String '<password>' -AsPlainText -Force) [-Alias <AliasValue>] [-DisplayName "<Display Name>"] [-ExternalEmailAddress <ExternalEmailAddress>] [-FirstName <Text>] [-Initials <Text>] [-LastName <Text>]
```

<span data-ttu-id="6175f-188">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="6175f-188">**Notes**:</span></span>

- <span data-ttu-id="6175f-189">Le paramètre _Name_ est obligatoire, sa longueur maximale est de 64 caractères et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="6175f-189">The _Name_ parameter is required, has a maximum length of 64 characters, and must be unique.</span></span> <span data-ttu-id="6175f-190">Si vous n’utilisez pas le paramètre _DisplayName_, la valeur du paramètre _Name_ est utilisée pour le nom complet.</span><span class="sxs-lookup"><span data-stu-id="6175f-190">If you don't use the _DisplayName_ parameter, the value of the _Name_ parameter is used for the display name.</span></span>
- <span data-ttu-id="6175f-191">Si vous n’utilisez pas le paramètre _alias_ , le côté gauche du paramètre _MicrosoftOnlineServicesID_ est utilisé pour l’alias.</span><span class="sxs-lookup"><span data-stu-id="6175f-191">If you don't use the _Alias_ parameter, the left side of the _MicrosoftOnlineServicesID_ parameter is used for the alias.</span></span>
- <span data-ttu-id="6175f-192">Si vous n’utilisez pas le paramètre _ExternalEmailAddress_ , la valeur _MicrosoftOnlineServicesID_ est utilisée pour l’adresse de messagerie externe.</span><span class="sxs-lookup"><span data-stu-id="6175f-192">If you don't use the _ExternalEmailAddress_ parameter, the _MicrosoftOnlineServicesID_ value is used for the external email address.</span></span>

<span data-ttu-id="6175f-193">Cet exemple crée un utilisateur de messagerie avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6175f-193">This example creates a mail user with the following settings:</span></span>

- <span data-ttu-id="6175f-194">Le nom est JeffreyZeng et le nom d’affichage est Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="6175f-194">The name is JeffreyZeng and the display name is Jeffrey Zeng.</span></span>
- <span data-ttu-id="6175f-195">Le prénom est Jeffrey et le nom est Zeng.</span><span class="sxs-lookup"><span data-stu-id="6175f-195">The first name is Jeffrey and the last name is Zeng.</span></span>
- <span data-ttu-id="6175f-196">L'alias est jeffreyz.</span><span class="sxs-lookup"><span data-stu-id="6175f-196">The alias is jeffreyz.</span></span>
- <span data-ttu-id="6175f-197">L'adresse de messagerie externe est jzeng@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="6175f-197">The external email address is jzeng@tailspintoys.com.</span></span>
- <span data-ttu-id="6175f-198">Le nom du compte est jeffreyz@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6175f-198">The account name is jeffreyz@contoso.onmicrosoft.com.</span></span>
- <span data-ttu-id="6175f-199">Le mot de passe est Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="6175f-199">The password is Pa$$word1.</span></span>

```PowerShell
New-EOPMailUser -Name JeffreyZeng -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force) -ExternalEmailAddress jeffreyz@tailspintoys.com -DisplayName "Jeffrey Zeng" -Alias jeffreyz -FirstName Jeffrey -LastName Zeng
```

<span data-ttu-id="6175f-200">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/new-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="6175f-200">For detailed syntax and parameter information, see [New-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/new-eopmailuser).</span></span>

### <a name="use-standalone-eop-powershell-to-modify-mail-users"></a><span data-ttu-id="6175f-201">Utilisation d’EOP PowerShell autonome pour modifier des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-201">Use standalone EOP PowerShell to modify mail users</span></span>

<span data-ttu-id="6175f-202">Pour modifier des utilisateurs de messagerie existants dans une version autonome d’EOP PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6175f-202">To modify existing mail users in standalone EOP PowerShell, use the following syntax:</span></span>

```powershell
Set-EOPMailUser -Identity <MailUserIdentity> [-Alias <Text>] [-DisplayName <Text>] [-EmailAddresses <ProxyAddressCollection>] [-MicrosoftOnlineServicesID <SmtpAddress>]
```

```powershell
Set-EOPUser -Identity <MailUserIdentity> [-City <Text>] [-Company <Text>] [-CountryOrRegion <CountryInfo>] [-Department <Text>] [-Fax <PhoneNumber>] [-FirstName <Text>] [-HomePhone <PhoneNumber>] [-Initials <Text>] [-LastName <Text>] [-MobilePhone <PhoneNumber>] [-Notes <Text>] [-Office <Text>] [-Phone <PhoneNumber>] [-PostalCode <String>] [-StateOrProvince <String>] [-StreetAddress <Tet>] [-Title <Text>] [-WebPage <Text>]
```

<span data-ttu-id="6175f-203">Cet exemple illustre la configuration de l'adresse de messagerie externe pour Pilar Pinilla.</span><span class="sxs-lookup"><span data-stu-id="6175f-203">This example sets the external email address for Pilar Pinilla.</span></span>

```PowerShell
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="6175f-204">Cet exemple illustre la définition de la propriété Company sur Contoso pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6175f-204">This example sets the Company property for all mail users to Contoso.</span></span>

```PowerShell
$Recip = Get-Recipient -RecipientType MailUser -ResultSize unlimited
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}
```

<span data-ttu-id="6175f-205">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/set-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="6175f-205">For detailed syntax and parameter information, see [Set-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/set-eopmailuser).</span></span>

### <a name="use-standalone-eop-powershell-to-remove-mail-users"></a><span data-ttu-id="6175f-206">Utilisation d’EOP PowerShell autonome pour supprimer des utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-206">Use standalone EOP PowerShell to remove mail users</span></span>

<span data-ttu-id="6175f-207">Pour supprimer des utilisateurs de messagerie dans une version autonome d’EOP PowerShell, remplacez \<MailUserIdentity\> par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6175f-207">To remove mail users in standalone EOP PowerShell, replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following command:</span></span>

```PowerShell
Remove-EOPMailUser -Identity <MailUserIdentity\>
```

<span data-ttu-id="6175f-208">Cet exemple supprime l’utilisateur de messagerie pour Jeffrey Zeng.</span><span class="sxs-lookup"><span data-stu-id="6175f-208">This example removes the mail user for Jeffrey Zeng.</span></span>

```PowerShell
Remove-EOPMailUser -Identity "Jeffrey Zeng"
```

<span data-ttu-id="6175f-209">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/remove-eopmailuser).</span><span class="sxs-lookup"><span data-stu-id="6175f-209">For detailed syntax and parameter information, see [Remove-EOPMailUser](https://docs.microsoft.com/powershell/module/exchange/remove-eopmailuser).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="6175f-210">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="6175f-210">How do you know these procedures worked?</span></span>

<span data-ttu-id="6175f-211">Pour vérifier que vous avez bien créé, modifié ou supprimé des utilisateurs de messagerie dans une version autonome d’EOP, utilisez l’une des procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="6175f-211">To verify that you've successfully created, modified, or removed mail users in standalone EOP, use any of the following procedures:</span></span>

- <span data-ttu-id="6175f-212">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="6175f-212">In the EAC, go to **Recipients** \> **Contacts**.</span></span> <span data-ttu-id="6175f-213">Vérifiez que l’utilisateur de messagerie est indiqué (ou non).</span><span class="sxs-lookup"><span data-stu-id="6175f-213">Verify that the mail user is listed (or isn't listed).</span></span> <span data-ttu-id="6175f-214">Sélectionnez l’utilisateur de messagerie et affichez les informations dans le volet d’informations, ou cliquez sur **modifier** ![ l’icône modifier ](../../media/ITPro-EAC-AddIcon.png) pour afficher les paramètres.</span><span class="sxs-lookup"><span data-stu-id="6175f-214">Select the mail user and view the information in the Details pane, or click **Edit** ![Edit icon](../../media/ITPro-EAC-AddIcon.png) to view the settings.</span></span>

- <span data-ttu-id="6175f-215">Dans la version autonome d’EOP PowerShell, exécutez la commande suivante pour vérifier que l’utilisateur de messagerie est indiqué (ou non) :</span><span class="sxs-lookup"><span data-stu-id="6175f-215">In standalone EOP PowerShell, run the following command to verify the mail user is listed (or isn't listed):</span></span>

  ```powershell
  Get-Recipient -RecipientType MailUser -ResultSize unlimited
  ```

- <span data-ttu-id="6175f-216">Remplacez \<MailUserIdentity\> par le nom, l’alias ou le nom de compte de l’utilisateur de messagerie, puis exécutez les commandes suivantes pour vérifier les paramètres :</span><span class="sxs-lookup"><span data-stu-id="6175f-216">Replace \<MailUserIdentity\> with the name, alias, or account name of the mail user, and run the following commands to verify the settings:</span></span>

  ```powershell
  Get-Recipient -Identity <MailUserIdentity> | Format-List
  ```

  ```powershell
  Get-User -Identity <MailUserIdentity> | Format-List
  ```

## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="6175f-217">Utilisation de la synchronisation d’annuaires pour gérer les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="6175f-217">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="6175f-218">Dans la version autonome d’EOP, la synchronisation d’annuaires est disponible pour les clients disposant d’Active Directory sur site.</span><span class="sxs-lookup"><span data-stu-id="6175f-218">In standalone EOP, directory synchronization is available for customers with on-premises Active Directory.</span></span> <span data-ttu-id="6175f-219">Vous pouvez synchroniser ces comptes avec Azure Active Directory (Azure AD), où les copies des comptes sont stockées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="6175f-219">You can synchronize those accounts to Azure Active Directory (Azure AD), where copies of the accounts are stored in the cloud.</span></span> <span data-ttu-id="6175f-220">Lorsque vous synchronisez vos comptes d’utilisateur existants avec Azure Active Directory, vous pouvez afficher ces utilisateurs dans le volet **destinataires** du centre d’administration Exchange ou dans un PowerShell d’EOP autonome.</span><span class="sxs-lookup"><span data-stu-id="6175f-220">When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC) or in standalone EOP PowerShell.</span></span>

<span data-ttu-id="6175f-221">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="6175f-221">**Notes**:</span></span>

- <span data-ttu-id="6175f-222">Si vous utilisez la synchronisation d’annuaires pour gérer vos destinataires, vous pouvez toujours ajouter et gérer des utilisateurs dans le centre d’administration 365 de Microsoft, mais ils ne seront pas synchronisés avec votre annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="6175f-222">If you use directory synchronization to manage your recipients, you can still add and manage users in the Microsoft 365 admin center, but they will not be synchronized with your on-premises Active Directory.</span></span> <span data-ttu-id="6175f-223">En effet, la synchronisation d’annuaires ne synchronise que les destinataires de votre annuaire Active Directory sur site vers le nuage.</span><span class="sxs-lookup"><span data-stu-id="6175f-223">This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span>

- <span data-ttu-id="6175f-224">Il est recommandé d’utiliser la synchronisation d’annuaires avec les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="6175f-224">Using directory synchronization is recommended for use with the following features:</span></span>

  - <span data-ttu-id="6175f-225">Listes **des expéditeurs approuvés Outlook et listes des expéditeurs bloqués**: lorsqu’ils sont synchronisés avec le service, ces listes prévalent sur le filtrage du courrier indésirable dans le service.</span><span class="sxs-lookup"><span data-stu-id="6175f-225">**Outlook Safe Sender lists and Blocked Sender lists**: When synchronized to the service, these lists will take precedence over spam filtering in the service.</span></span> <span data-ttu-id="6175f-226">Cela permet aux utilisateurs de gérer leur propre liste d’expéditeurs approuvés et la liste des expéditeurs bloqués avec des entrées individuelles de domaine et d’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="6175f-226">This lets users manage their own Safe Sender list and Blocked Sender list with individual sender and domain entries.</span></span> <span data-ttu-id="6175f-227">Pour plus d’informations, voir [Configurer les paramètres du courrier indésirable sur les boîtes aux lettres Exchange Online](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="6175f-227">For more information, see [Configure junk email settings on Exchange Online mailboxes](https://docs.microsoft.com/microsoft-365/security/office-365-security/configure-junk-email-settings-on-exo-mailboxes).</span></span>

  - <span data-ttu-id="6175f-228">**Blocage du périmètre basé sur l’annuaire (DBEB)**: pour plus d’informations sur DBEB, voir [use Directory based Edge Blocking to Reject messages sent to Invalid Recipients](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-directory-based-edge-blocking).</span><span class="sxs-lookup"><span data-stu-id="6175f-228">**Directory Based Edge Blocking (DBEB)**: For more information about DBEB, see [Use Directory Based Edge Blocking to reject messages sent to invalid recipients](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-directory-based-edge-blocking).</span></span>

  - <span data-ttu-id="6175f-229">**Accès de l’utilisateur final à la mise en quarantaine**: pour accéder à ses messages mis en quarantaine, les destinataires doivent disposer d’un ID d’utilisateur et d’un mot de passe valides dans le service.</span><span class="sxs-lookup"><span data-stu-id="6175f-229">**End user access to quarantine**: To access their quarantined messages, recipients must have a valid user ID and password in the service.</span></span> <span data-ttu-id="6175f-230">Pour plus d’informations sur la mise en quarantaine, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur](https://docs.microsoft.com/microsoft-365/security/office-365-security/find-and-release-quarantined-messages-as-a-user).</span><span class="sxs-lookup"><span data-stu-id="6175f-230">For more information about quarantine, see [Find and release quarantined messages as a user](https://docs.microsoft.com/microsoft-365/security/office-365-security/find-and-release-quarantined-messages-as-a-user).</span></span>

  - <span data-ttu-id="6175f-231">**Règles de flux de messagerie (également appelées règles de transport)**: lorsque vous utilisez la synchronisation d’annuaires, vos utilisateurs et groupes Active Directory existants sont automatiquement téléchargés dans le Cloud, et vous pouvez créer des règles de flux de messagerie qui ciblent des utilisateurs et/ou des groupes spécifiques sans avoir à les ajouter manuellement au service.</span><span class="sxs-lookup"><span data-stu-id="6175f-231">**Mail flow rules (also known as transport rules)**: When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules that target specific users and/or groups without having to manually add them in the service.</span></span> <span data-ttu-id="6175f-232">Notez que les [groupes de distribution dynamique](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-dynamic-distribution-groups/manage-dynamic-distribution-groups) ne peuvent pas être synchronisés via la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="6175f-232">Note that [dynamic distribution groups](https://docs.microsoft.com/Exchange/recipients-in-exchange-online/manage-dynamic-distribution-groups/manage-dynamic-distribution-groups) can't be synchronized via directory synchronization.</span></span>

<span data-ttu-id="6175f-233">Obtenir les autorisations nécessaires et préparer la synchronisation d’annuaires, comme décrit dans [What is Hybrid Identity with Azure Active Directory ?](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-hybrid-identity).</span><span class="sxs-lookup"><span data-stu-id="6175f-233">Get the necessary permissions and prepare for directory synchronization, as described in [What is hybrid identity with Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/hybrid/whatis-hybrid-identity).</span></span>

### <a name="synchronize-directories-with-azure-active-directory-connect-aad-connect"></a><span data-ttu-id="6175f-234">Synchroniser des annuaires avec Azure Active Directory Connect (AAD Connect)</span><span class="sxs-lookup"><span data-stu-id="6175f-234">Synchronize directories with Azure Active Directory Connect (AAD Connect)</span></span>

1. <span data-ttu-id="6175f-235">Activer la synchronisation d’annuaires, comme décrit dans [Azure ad Connect Sync : comprendre et personnaliser la synchronisation](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span><span class="sxs-lookup"><span data-stu-id="6175f-235">Activate directory synchronization as described in [Azure AD Connect sync: Understand and customize synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-whatis).</span></span>

2. <span data-ttu-id="6175f-236">Installez et configurez un ordinateur local pour exécuter AAD Connect comme décrit dans [Prerequisites for Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites).</span><span class="sxs-lookup"><span data-stu-id="6175f-236">Install and configure an on-premises computer to run AAD Connect as described in [Prerequisites for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites).</span></span>

3. <span data-ttu-id="6175f-237">[Sélectionnez le type d’installation à utiliser pour Azure ad Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation):</span><span class="sxs-lookup"><span data-stu-id="6175f-237">[Select which installation type to use for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation):</span></span>

   - [<span data-ttu-id="6175f-238">Express</span><span class="sxs-lookup"><span data-stu-id="6175f-238">Express</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)

   - [<span data-ttu-id="6175f-239">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="6175f-239">Custom</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)

   - [<span data-ttu-id="6175f-240">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="6175f-240">Pass-through authentication</span></span>](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-pta-quick-start)

> [!IMPORTANT]
> <span data-ttu-id="6175f-p121">Après exécution de l'Assistant Configuration de l'outil de synchronisation Azure Active Directory, le compte **MSOL_AD_SYNC** est créé dans votre forêt Active Directory. Ce compte permet de lire et de synchroniser vos informations Active Directory sur site. Pour que la synchronisation d'annuaires fonctionne correctement, assurez-vous que le port TCP 443 est ouvert sur votre serveur de synchronisation d'annuaires sur site.</span><span class="sxs-lookup"><span data-stu-id="6175f-p121">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span>

<span data-ttu-id="6175f-244">Après avoir configuré votre synchronisation, veillez à vérifier que la synchronisation AAD se synchronise correctement.</span><span class="sxs-lookup"><span data-stu-id="6175f-244">After configuring your sync, be sure to verify that AAD Connect is synchronizing correctly.</span></span> <span data-ttu-id="6175f-245">Dans le CAE, accédez à **Destinataires** \> **Contacts** et vérifiez que la liste des utilisateurs a été correctement synchronisée à partir de votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="6175f-245">In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span>
