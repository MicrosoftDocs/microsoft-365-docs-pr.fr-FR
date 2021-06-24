---
title: Supprimer les utilisateurs bloqués du portail Utilisateurs restreints
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à supprimer des utilisateurs de la page Utilisateurs restreints dans le portail Microsoft 365 Defender. Les utilisateurs sont ajoutés au portail Utilisateurs restreints pour avoir envoyé du courrier indésirable sortant, généralement en raison de la compromission d’un compte.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 924db948103a4d3b45c499f433961762a45931af
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53082851"
---
# <a name="remove-blocked-users-from-the-restricted-users-portal-in-microsoft-365"></a><span data-ttu-id="1c82b-104">Supprimer les utilisateurs bloqués du portail Utilisateurs restreints dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c82b-104">Remove blocked users from the Restricted users portal in Microsoft 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1c82b-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1c82b-105">**Applies to**</span></span>
- [<span data-ttu-id="1c82b-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="1c82b-106">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="1c82b-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="1c82b-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="1c82b-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1c82b-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="1c82b-109">Si un utilisateur dépasse l’une des limites d’envoi sortant, comme spécifié dans [les limites de service](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) ou dans [les stratégies anti-courrier indésirable sortantes](configure-the-outbound-spam-policy.md), l’utilisateur ne peut pas envoyer d’e-mails, mais il peut continuer à en recevoir.</span><span class="sxs-lookup"><span data-stu-id="1c82b-109">If a user exceeds one of the outbound sending limits as specified in [the service limits](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) or in [outbound spam policies](configure-the-outbound-spam-policy.md), the user is restricted from sending email, but they can still receive email.</span></span>

<span data-ttu-id="1c82b-110">L’utilisateur est ajouté à la page **Utilisateurs restreints** dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="1c82b-110">The user is added to the **Restricted users** page in the Microsoft 365 Defender portal.</span></span> <span data-ttu-id="1c82b-111">Lorsqu’il essaie d’envoyer des e-mail, le message est renvoyé dans une notification d’échec de remise (ou notification de non-remise) avec le code d’erreur [5.1.8](/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) et le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="1c82b-111">When they try to send email, the message is returned in a non-delivery report (also known as an NDR or bounce messages) with the error code [5.1.8](/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) and the following text:</span></span>

> <span data-ttu-id="1c82b-112">«Votre message n’a pas pu être remis parce que vous n’avez pas été reconnu comme expéditeur valide.</span><span class="sxs-lookup"><span data-stu-id="1c82b-112">"Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="1c82b-113">Le plus souvent, il est possible que votre adresse de messagerie soit susceptible d’envoyer du courrier indésirable et qu’elle ne soit plus autorisée à envoyer du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="1c82b-113">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send email.</span></span>  <span data-ttu-id="1c82b-114">Contactez votre administrateur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="1c82b-114">Contact  your email admin for assistance.</span></span> <span data-ttu-id="1c82b-115">Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect».</span><span class="sxs-lookup"><span data-stu-id="1c82b-115">Remote Server returned '550 5.1.8 Access denied, bad outbound sender."</span></span>

<span data-ttu-id="1c82b-116">Les administrateurs peuvent supprimer des utilisateurs de la page Utilisateurs restreints dans Microsoft 365 Defender ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c82b-116">Admins can remove users from the Restricted users page in the Microsoft 365 Defender or in Exchange Online PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1c82b-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1c82b-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1c82b-118">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="1c82b-118">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="1c82b-119">Pour accéder directement à la page **Utilisateurs restreints**, utilisez <https://security.microsoft.com/restrictedusers>.</span><span class="sxs-lookup"><span data-stu-id="1c82b-119">Too go directly to the **Restricted users** page, use <https://security.microsoft.com/restrictedusers>.</span></span>

- <span data-ttu-id="1c82b-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="1c82b-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="1c82b-121">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="1c82b-121">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="1c82b-122">Pour supprimer des utilisateurs du portail Utilisateurs restreints, vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-122">To remove users from the Restricted users portal, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="1c82b-123">Pour l’accès en lecture seule au portail Utilisateurs restreints, vous devez être membre du groupe de rôles **Lecteur global** ou **Lecteur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-123">For read-only access to the Restricted users portal, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="1c82b-124">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="1c82b-124">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="1c82b-125">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c82b-125">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1c82b-126">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1c82b-126">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="1c82b-127">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1c82b-127">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="1c82b-128">Un expéditeur dépassant la limite du nombre de messages sortants est un indicateur de compte compromis.</span><span class="sxs-lookup"><span data-stu-id="1c82b-128">A sender exceeding the outbound email limits is an indicator of a compromised account.</span></span> <span data-ttu-id="1c82b-129">Avant de supprimer l’utilisateur du portail Utilisateurs restreints, veillez à suivre les étapes nécessaires pour reprendre le contrôle de son compte.</span><span class="sxs-lookup"><span data-stu-id="1c82b-129">Before you remove the user from the Restricted users portal, be sure to follow the required steps to regain control of their account.</span></span> <span data-ttu-id="1c82b-130">Pour plus informations, voir [Réponse à un compte de messagerie compromis dans Office 365](responding-to-a-compromised-email-account.md).</span><span class="sxs-lookup"><span data-stu-id="1c82b-130">For more information, see [Responding to a compromised email account in Office 365](responding-to-a-compromised-email-account.md).</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-a-user-from-the-restricted-users-list"></a><span data-ttu-id="1c82b-131">Utiliser le portail Microsoft 365 Defender pour supprimer un utilisateur de la liste des Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="1c82b-131">Use the Microsoft 365 Defender portal to remove a user from the Restricted users list</span></span>

1. <span data-ttu-id="1c82b-132">Dans le portail Microsoft 365 Defender, accédez à **Courrier électronique et collaboration** > **Examiner** > **Utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-132">In the Microsoft 365 Defender portal, go to **Email & collaboration** > **Review** > **Restricted users**.</span></span>

2. <span data-ttu-id="1c82b-133">Dans la page **Utilisateurs restreints** , recherchez et sélectionnez l’utilisateur que vous souhaitez débloquer en cliquant sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c82b-133">On the **Restricted users** page, find and select the user that you want to unblock by clicking on the user.</span></span>

3. <span data-ttu-id="1c82b-134">Cliquez sur l’action **Débloquer** qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1c82b-134">Click the **Unblock** action that appears.</span></span>

4. <span data-ttu-id="1c82b-135">Dans le menu volant **Débloquer l’utilisateur** qui s’affiche, lisez les détails sur le compte restreint.</span><span class="sxs-lookup"><span data-stu-id="1c82b-135">In the **Unblock user** flyout that appears, read the details about the restricted account.</span></span> <span data-ttu-id="1c82b-136">Vous devez suivre les recommandations pour vous assurer que vous effectuez les actions appropriées au cas où le compte est compromis.</span><span class="sxs-lookup"><span data-stu-id="1c82b-136">You should go through the recommendations to ensure you're taking the proper actions in case the account is compromised.</span></span>

   <span data-ttu-id="1c82b-137">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-137">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="1c82b-138">L’écran suivant comporte des recommandations pour empêcher toute compromission ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1c82b-138">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="1c82b-139">L’activation de l’authentification multifacteur (MFA) et la réinitialisation du mot de passe constituent une bonne défense.</span><span class="sxs-lookup"><span data-stu-id="1c82b-139">Enabling multi-factor authentication (MFA) and resetting the password are a good defense.</span></span>

   <span data-ttu-id="1c82b-140">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-140">When you're finished, click **Submit**.</span></span>

6. <span data-ttu-id="1c82b-141">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="1c82b-141">Click **Yes** to confirm the change.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1c82b-142">La suppression de toutes les restrictions de l’utilisateur peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="1c82b-142">It might take up to 24 hours for all restrictions to be removed from the user.</span></span>

## <a name="verify-the-alert-settings-for-restricted-users"></a><span data-ttu-id="1c82b-143">Vérifier les paramètres d’alerte pour les utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="1c82b-143">Verify the alert settings for restricted users</span></span>

<span data-ttu-id="1c82b-144">La stratégie d’alerte par défaut nommée **Utilisateur pour lequel l’envoi de courrier est restreint** avertit automatiquement les administrateurs lorsque les utilisateurs ne peuvent pas envoyer de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="1c82b-144">The default alert policy named **User restricted from sending email** will automatically notify admins when users are blocked from sending outbound mail.</span></span> <span data-ttu-id="1c82b-145">Vous pouvez vérifier ces paramètres et ajouter des utilisateurs à avertir.</span><span class="sxs-lookup"><span data-stu-id="1c82b-145">You can verify these settings and add additional users to notify.</span></span> <span data-ttu-id="1c82b-146">Pour plus d'informations sur les stratégies d'alerte, voir Stratégies [d'alerte dans Microsoft 365](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1c82b-146">For more information about alert policies, see [Alert policies in Microsoft 365](../../compliance/alert-policies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c82b-147">Pour que les alertes fonctionnent, la recherche dans le journal d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="1c82b-147">For alerts to work, audit log search must to be turned on.</span></span> <span data-ttu-id="1c82b-148">Pour plus d’informations, voir [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="1c82b-148">For more information, see [Turn the audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

1. <span data-ttu-id="1c82b-149">Dans le portail Microsoft 365 Defender, accédez à **Courrier électronique et stratégies de collaboration** \> **Stratégies & règles** \> **Alerte**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-149">In the Microsoft 365 Defender portal, go to **Email & collaboration** \> **Policies & rules** \> **Alert policy**.</span></span>

2. <span data-ttu-id="1c82b-150">Dans la page **Stratégie d’alerte**, recherchez et sélectionnez l’alerte nommée **Utilisateur restreint pour l’envoi d’e-mail**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-150">On the **Alert policy** page, find and select the alert named **User restricted from sending email**.</span></span> <span data-ttu-id="1c82b-151">Vous pouvez trier les stratégies par nom ou utiliser la **Zone de recherche** pour rechercher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1c82b-151">You can sort the policies by name, or use the **Search box** to find the policy.</span></span>

3. <span data-ttu-id="1c82b-152">Dans le menu volant **Utilisateur restreint pour l’envoi d’e-mail** qui s’affiche, vérifiez ou configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c82b-152">In the **User restricted from sending email** flyout that appears, verify or configure the following settings:</span></span>
   - <span data-ttu-id="1c82b-153">**État** : vérifiez que l’alerte est activée ![Activer](../../media/scc-toggle-on.png).</span><span class="sxs-lookup"><span data-stu-id="1c82b-153">**Status**: Verify the alert is turned on ![Toggle on](../../media/scc-toggle-on.png).</span></span>
   - <span data-ttu-id="1c82b-154">**Destinataires de courrier** : cliquez sur **Modifier** et vérifiez ou configurez les paramètres suivants dans le menu volant **Modifier les destinataires** qui apparaît :</span><span class="sxs-lookup"><span data-stu-id="1c82b-154">**Email recipients**: Click **Edit** and verify or configure the following settings in the **Edit recipients** flyout that appears:</span></span>
     - <span data-ttu-id="1c82b-155">**Envoyer des notifications par e-mail**: vérifiez que cette option est sélectionnée (**Activé**).</span><span class="sxs-lookup"><span data-stu-id="1c82b-155">**Send email notifications**: Verify this is selected (**On**).</span></span>
     - <span data-ttu-id="1c82b-156">**Destinataires du courrier** : la valeur par défaut est **TenantAdmins** (c’est-à-dire membres de type **Administrateur général**).</span><span class="sxs-lookup"><span data-stu-id="1c82b-156">**Email recipients**: The default value is **TenantAdmins** (meaning, **Global admin** members).</span></span> <span data-ttu-id="1c82b-157">Pour ajouter des destinataires, cliquez sur une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="1c82b-157">To add more recipients, click in a blank area of the box.</span></span> <span data-ttu-id="1c82b-158">Une liste de destinataires apparaît, puis vous pouvez commencer à saisir un nom pour filtrer et sélectionner un destinataire.</span><span class="sxs-lookup"><span data-stu-id="1c82b-158">A list of recipients will appear, and you can start typing a name to filter and select a recipient.</span></span> <span data-ttu-id="1c82b-159">Vous pouvez supprimer un destinataire existant de la zone en cliquant sur ![Icône Supprimer](../../media/m365-cc-sc-remove-selection-icon.png) en regard de son nom.</span><span class="sxs-lookup"><span data-stu-id="1c82b-159">You can remove an existing recipient from the box by clicking ![Remove icon](../../media/m365-cc-sc-remove-selection-icon.png) next to their name.</span></span>
     - <span data-ttu-id="1c82b-160">**Limite quotidienne de notification** : la valeur par défaut est **Aucune limite**, mais vous pouvez sélectionner une limite pour le nombre maximal de notifications par jour.</span><span class="sxs-lookup"><span data-stu-id="1c82b-160">**Daily notification limit**: The default value is **No limit** but you can select a limit for the maximum number of notifications per day.</span></span>

     <span data-ttu-id="1c82b-161">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-161">When you're finished, click **Save**.</span></span>

4. <span data-ttu-id="1c82b-162">De retour dans le menu roulant **Utilisateur pour lequel l’envoi de courrier est restreint**, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1c82b-162">Back on the **User restricted from sending email** flyout, click **Close**.</span></span>

## <a name="use-exchange-online-powershell-to-view-and-remove-users-from-the-restricted-users-list"></a><span data-ttu-id="1c82b-163">Utiliser Exchange Online PowerShell pour afficher et supprimer des utilisateurs de la liste des Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="1c82b-163">Use Exchange Online PowerShell to view and remove users from the Restricted users list</span></span>

<span data-ttu-id="1c82b-164">Pour afficher cette liste d’utilisateurs pour lesquels l’envoi de courrier est restreint, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1c82b-164">To view this list of users that are restricted from sending email, run the following command:</span></span>

```powershell
Get-BlockedSenderAddress
```

<span data-ttu-id="1c82b-165">Pour afficher les détails d’un utilisateur spécifique, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1c82b-165">To view details about a specific user, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Get-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="1c82b-166">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Get-BlockedSenderAddress](/powershell/module/exchange/get-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="1c82b-166">For detailed syntax and parameter information, see [Get-BlockedSenderAddress](/powershell/module/exchange/get-blockedsenderaddress).</span></span>

<span data-ttu-id="1c82b-167">Pour supprimer un utilisateur de la liste Utilisateurs restreints, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1c82b-167">To remove a user from the Restricted users list, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Remove-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="1c82b-168">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Remove-BlockedSenderAddress](/powershell/module/exchange/remove-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="1c82b-168">For detailed syntax and parameter information, see [Remove-BlockedSenderAddress](/powershell/module/exchange/remove-blockedsenderaddress).</span></span>
