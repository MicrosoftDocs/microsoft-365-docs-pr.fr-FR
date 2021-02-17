---
title: Retirer les utilisateurs bloqués du portail des utilisateurs restreints
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
description: Les administrateurs peuvent découvrir comment supprimer des utilisateurs du portail des utilisateurs restreints dans Office 365. Les utilisateurs sont ajoutés au portail Utilisateurs restreints pour avoir envoyé du courrier indésirable sortant, généralement en raison de la compromission d’un compte.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 1ba5334689ad58c8a50864a3618c0972b61dfd7f
ms.sourcegitcommit: a9ac702c9efc9defded3bfa65618b94bac00c237
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/16/2021
ms.locfileid: "50261548"
---
# <a name="remove-blocked-users-from-the-restricted-users-portal-in-office-365"></a><span data-ttu-id="d9772-104">Retirer les utilisateurs bloqués du portail Utilisateurs restreints dans Office 365</span><span class="sxs-lookup"><span data-stu-id="d9772-104">Remove blocked users from the Restricted Users portal in Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="d9772-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d9772-105">**Applies to**</span></span>
- [<span data-ttu-id="d9772-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="d9772-106">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="d9772-107">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="d9772-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="d9772-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d9772-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="d9772-109">Si un utilisateur dépasse l’une des limites d’envoi sortant, comme spécifié dans [les limites de service](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) ou dans [les stratégies anti-courrier indésirable sortantes](configure-the-outbound-spam-policy.md), l’utilisateur ne peut pas envoyer d’e-mails, mais il peut continuer à en recevoir.</span><span class="sxs-lookup"><span data-stu-id="d9772-109">If a user exceeds one of the outbound sending limits as specified in [the service limits](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) or in [outbound spam policies](configure-the-outbound-spam-policy.md), the user is restricted from sending email, but they can still receive email.</span></span>

<span data-ttu-id="d9772-110">L’utilisateur est ajouté au portail Utilisateurs restreints dans le Centre de sécurité et conformité.</span><span class="sxs-lookup"><span data-stu-id="d9772-110">The user is added to the Restricted Users portal in the Security & Compliance Center.</span></span> <span data-ttu-id="d9772-111">Lorsqu’il essaie d’envoyer des e-mail, le message est renvoyé dans une notification d’échec de remise (ou notification de non-remise) avec le code d’erreur [5.1.8](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) et le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="d9772-111">When they try to send email, the message is returned in a non-delivery report (also known as an NDR or bounce messages) with the error code [5.1.8](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) and the following text:</span></span>

> <span data-ttu-id="d9772-112">«Votre message n’a pas pu être remis parce que vous n’avez pas été reconnu comme expéditeur valide.</span><span class="sxs-lookup"><span data-stu-id="d9772-112">"Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="d9772-113">Le plus souvent, il est possible que votre adresse de messagerie soit susceptible d’envoyer du courrier indésirable et qu’elle ne soit plus autorisée à envoyer du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="d9772-113">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send email.</span></span>  <span data-ttu-id="d9772-114">Contactez votre administrateur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="d9772-114">Contact  your email admin for assistance.</span></span> <span data-ttu-id="d9772-115">Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect».</span><span class="sxs-lookup"><span data-stu-id="d9772-115">Remote Server returned '550 5.1.8 Access denied, bad outbound sender."</span></span>

<span data-ttu-id="d9772-116">Les administrateurs peuvent supprimer des utilisateurs du portail Expéditeurs restreints dans le centre de sécurité et conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9772-116">Admins can remove users from the Restricted Senders portal in the Security & Compliance Center or in Exchange Online PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d9772-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d9772-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d9772-118">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="d9772-118">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="d9772-119">Pour accéder directement à la page **Utilisateurs restreints**, utilisez <https://protection.office.com/restrictedusers>.</span><span class="sxs-lookup"><span data-stu-id="d9772-119">To go directly to the **Restricted Users** page, use <https://protection.office.com/restrictedusers>.</span></span>

- <span data-ttu-id="d9772-120">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="d9772-120">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="d9772-121">Des autorisations doivent vous avoir été attribuées dans le Centre de sécurité et de conformité pour que vous puissiez effectuer les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d9772-121">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="d9772-122">Pour supprimer des utilisateurs du portail Utilisateurs restreints, vous devez être membre des groupes de rôles **Management de l’organisation** ou **Administrateur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="d9772-122">To remove users from the Restricted Users portal, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="d9772-123">Pour l’accès en lecture seule au portail Utilisateurs restreints, vous devez être membre du groupe de rôles **Lecteur global** ou **Lecteur de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="d9772-123">For read-only access to the Restricted Users portal, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="d9772-124">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d9772-124">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="d9772-125">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9772-125">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="d9772-126">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="d9772-126">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  >
  > - <span data-ttu-id="d9772-127">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d9772-127">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="d9772-128">Un expéditeur dépassant la limite du nombre de messages sortants est un indicateur de compte compromis.</span><span class="sxs-lookup"><span data-stu-id="d9772-128">A sender exceeding the outbound email limits is an indicator of a compromised account.</span></span> <span data-ttu-id="d9772-129">Avant de supprimer l’utilisateur du portail Utilisateurs restreints, veillez à suivre les étapes nécessaires pour reprendre le contrôle de son compte.</span><span class="sxs-lookup"><span data-stu-id="d9772-129">Before you remove the user from the Restricted Users portal, be sure to follow the required steps to regain control of their account.</span></span> <span data-ttu-id="d9772-130">Pour plus informations, voir [Réponse à un compte de messagerie compromis dans Office 365](responding-to-a-compromised-email-account.md).</span><span class="sxs-lookup"><span data-stu-id="d9772-130">For more information, see [Responding to a compromised email account in Office 365](responding-to-a-compromised-email-account.md).</span></span>

## <a name="use-the-security--compliance-center-to-remove-a-user-from-the-restricted-users-list"></a><span data-ttu-id="d9772-131">Utiliser le Centre de sécurité et conformité pour supprimer un utilisateur de la liste Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="d9772-131">Use the Security & Compliance Center to remove a user from the Restricted Users list</span></span>

1. <span data-ttu-id="d9772-132">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="d9772-132">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Restricted users**.</span></span>

2. <span data-ttu-id="d9772-133">Recherchez et sélectionnez l’utilisateur que vous souhaitez débloquer.</span><span class="sxs-lookup"><span data-stu-id="d9772-133">Find and select the user that you want to unblock.</span></span> <span data-ttu-id="d9772-134">Dans la colonne **Actions**, cliquez sur **Débloquer**.</span><span class="sxs-lookup"><span data-stu-id="d9772-134">In the **Actions** column, click **Unblock**.</span></span>

3. <span data-ttu-id="d9772-135">Une fenêtre permet d’accéder aux informations relatives au compte dont l’envoi est restreint.</span><span class="sxs-lookup"><span data-stu-id="d9772-135">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="d9772-136">Nous vous conseillons de suivre les recommandations afin de vous assurer que vous effectuez les actions appropriées au cas où le compte serait réellement compromis.</span><span class="sxs-lookup"><span data-stu-id="d9772-136">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="d9772-137">Sélectionnez **Suivant** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="d9772-137">Click **Next** when done.</span></span>

4. <span data-ttu-id="d9772-138">L’écran suivant comporte des recommandations pour empêcher toute compromission ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d9772-138">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="d9772-139">L’activation de l’authentification multifacteur (MFA) et la modification des mots de passe constituent une bonne défense.</span><span class="sxs-lookup"><span data-stu-id="d9772-139">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="d9772-140">Lorsque vous avez terminé, cliquez sur **débloquer l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="d9772-140">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="d9772-141">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="d9772-141">Click **Yes** to confirm the change.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d9772-142">La suppression de toutes les restrictions de l’utilisateur peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="d9772-142">It might take up to 24 hours for all restrictions to be removed from the user.</span></span>

## <a name="verify-the-alert-settings-for-restricted-users"></a><span data-ttu-id="d9772-143">Vérifier les paramètres d’alerte pour les utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="d9772-143">Verify the alert settings for restricted users</span></span>

<span data-ttu-id="d9772-144">La stratégie d’alerte par défaut nommée **Utilisateur pour lequel l’envoi de courrier est restreint** avertit automatiquement les administrateurs lorsque les utilisateurs ne peuvent pas envoyer de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="d9772-144">The default alert policy named **User restricted from sending email** will automatically notify admins when users are blocked from sending outbound mail.</span></span> <span data-ttu-id="d9772-145">Vous pouvez vérifier ces paramètres et ajouter des utilisateurs à avertir.</span><span class="sxs-lookup"><span data-stu-id="d9772-145">You can verify these settings and add additional users to notify.</span></span> <span data-ttu-id="d9772-146">Pour plus d’informations sur les stratégies d’alerte, accédez à [Stratégies d’alerte dans le centre de sécurité et conformité](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d9772-146">For more information about alert policies, see [Alert policies in the security and compliance center](../../compliance/alert-policies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9772-147">Pour que les alertes fonctionnent, la recherche dans le journal d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="d9772-147">For alerts to work, audit log search must to be turned on.</span></span> <span data-ttu-id="d9772-148">Pour plus d’informations, voir [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="d9772-148">For more information, see [Turn the audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

1. <span data-ttu-id="d9772-149">Dans le Centre de sécurité et conformité, accédez à **Alertes** \> **Stratégies d’alerte**.</span><span class="sxs-lookup"><span data-stu-id="d9772-149">In the Security & Compliance Center, go to **Alerts** \> **Alert policies**.</span></span>

2. <span data-ttu-id="d9772-150">Recherchez et sélectionnez l’alerte **Utilisateur pour lequel l’envoi de courrier est restreint**.</span><span class="sxs-lookup"><span data-stu-id="d9772-150">Find and select the **User restricted from sending email** alert.</span></span>

3. <span data-ttu-id="d9772-151">Dans le menu volant qui apparaît, vérifiez ou configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d9772-151">In the flyout that appears, verify or configure the following settings:</span></span>

   - <span data-ttu-id="d9772-152">**État** : vérifiez que l’alerte est activée ![Activer](../../media/scc-toggle-on.png).</span><span class="sxs-lookup"><span data-stu-id="d9772-152">**Status**: Verify the alert is turned on ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   - <span data-ttu-id="d9772-153">**Destinataires de courrier** : cliquez sur **Modifier** et vérifiez ou configurez les paramètres suivants dans le menu volant **Modifier les destinataires** qui apparaît :</span><span class="sxs-lookup"><span data-stu-id="d9772-153">**Email recipients**: Click **Edit** and verify or configure the following settings in the **Edit recipients** flyout that appears:</span></span>

     - <span data-ttu-id="d9772-154">**Envoyer des notifications par courrier** : vérifiez que la case est cochée (**Activé**).</span><span class="sxs-lookup"><span data-stu-id="d9772-154">**Send email notifications**: Verify the check box is selected (**On**).</span></span>

     - <span data-ttu-id="d9772-155">**Destinataires du courrier** : la valeur par défaut est **TenantAdmins** (c’est-à-dire membres de type **Administrateur général**).</span><span class="sxs-lookup"><span data-stu-id="d9772-155">**Email recipients**: The default value is **TenantAdmins** (meaning, **Global admin** members).</span></span> <span data-ttu-id="d9772-156">Pour ajouter des destinataires, cliquez sur une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="d9772-156">To add more recipients, click in a blank area of the box.</span></span> <span data-ttu-id="d9772-157">Une liste de destinataires apparaît, puis vous pouvez commencer à saisir un nom pour filtrer et sélectionner un destinataire.</span><span class="sxs-lookup"><span data-stu-id="d9772-157">A list of recipients will appear, and you can start typing a name to filter and select a recipient.</span></span> <span data-ttu-id="d9772-158">Vous pouvez supprimer un destinataire existant de la zone en cliquant sur ![Icône Supprimer](../../media/scc-remove-icon.png) en regard de son nom.</span><span class="sxs-lookup"><span data-stu-id="d9772-158">You can remove an existing recipient from the box by clicking ![Remove icon](../../media/scc-remove-icon.png) next to their name.</span></span>

     - <span data-ttu-id="d9772-159">**Limite quotidienne de notification** : la valeur par défaut est **Aucune limite**, mais vous pouvez sélectionner une limite pour le nombre maximal de notifications par jour.</span><span class="sxs-lookup"><span data-stu-id="d9772-159">**Daily notification limit**: The default value is **No limit** but you can select a limit for the maximum number of notifications per day.</span></span>

     <span data-ttu-id="d9772-160">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d9772-160">When you're finished, click **Save**.</span></span>

4. <span data-ttu-id="d9772-161">De retour dans le menu roulant **Utilisateur pour lequel l’envoi de courrier est restreint**, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d9772-161">Back on the **User restricted from sending email** flyout, click **Close**.</span></span>

## <a name="use-exchange-online-powershell-to-view-and-remove-users-from-the-restricted-users-list"></a><span data-ttu-id="d9772-162">Utiliser Exchange Online PowerShell pour afficher et supprimer des utilisateurs de la liste Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="d9772-162">Use Exchange Online PowerShell to view and remove users from the Restricted Users list</span></span>

<span data-ttu-id="d9772-163">Pour afficher cette liste d’utilisateurs pour lesquels l’envoi de courrier est restreint, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9772-163">To view this list of users that are restricted from sending email, run the following command:</span></span>

```powershell
Get-BlockedSenderAddress
```

<span data-ttu-id="d9772-164">Pour afficher les détails d’un utilisateur spécifique, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9772-164">To view details about a specific user, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Get-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="d9772-165">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Get-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/get-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="d9772-165">For detailed syntax and parameter information, see [Get-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/get-blockedsenderaddress).</span></span>

<span data-ttu-id="d9772-166">Pour supprimer un utilisateur de la liste Utilisateurs restreints, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9772-166">To remove a user from the Restricted Users list, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Remove-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="d9772-167">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Remove-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/remove-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="d9772-167">For detailed syntax and parameter information, see [Remove-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/remove-blockedsenderaddress).</span></span>
