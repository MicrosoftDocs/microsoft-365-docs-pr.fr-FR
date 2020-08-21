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
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir comment supprimer des utilisateurs du portail des utilisateurs restreints dans Office 365. Les utilisateurs sont ajoutés au portail Utilisateurs restreints pour avoir envoyé du courrier indésirable sortant, généralement en raison de la compromission d’un compte.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 0d411cec48ff6704d737850974e832dbe07a3ad3
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46826528"
---
# <a name="remove-blocked-users-from-the-restricted-users-portal-in-office-365"></a><span data-ttu-id="2769a-104">Retirer les utilisateurs bloqués du portail Utilisateurs restreints dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2769a-104">Remove blocked users from the Restricted Users portal in Office 365</span></span>

<span data-ttu-id="2769a-105">Si un utilisateur dépasse l’une des limites d’envoi sortant, comme spécifié dans [les limites de service](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) ou dans [les stratégies anti-courrier indésirable sortantes](configure-the-outbound-spam-policy.md), l’utilisateur ne peut pas envoyer d’e-mails, mais il peut continuer à en recevoir.</span><span class="sxs-lookup"><span data-stu-id="2769a-105">If a user exceeds one of the outbound sending limits as specified in [the service limits](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits-across-office-365-options) or in [outbound spam policies](configure-the-outbound-spam-policy.md), the user is restricted from sending email, but they can still receive email.</span></span>

<span data-ttu-id="2769a-106">L’utilisateur est ajouté au portail Utilisateurs restreints dans le Centre de sécurité et conformité.</span><span class="sxs-lookup"><span data-stu-id="2769a-106">The user is added to the Restricted Users portal in the Security & Compliance Center.</span></span> <span data-ttu-id="2769a-107">Lorsqu’il essaie d’envoyer des e-mail, le message est renvoyé dans une notification d’échec de remise (ou notification de non-remise) avec le code d’erreur [5.1.8](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) et le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="2769a-107">When they try to send email, the message is returned in a non-delivery report (also known as an NDR or bounce messages) with the error code [5.1.8](https://docs.microsoft.com/Exchange/mail-flow-best-practices/non-delivery-reports-in-exchange-online/fix-error-code-5-1-8-in-exchange-online) and the following text:</span></span>

> <span data-ttu-id="2769a-108">«Votre message n’a pas pu être remis parce que vous n’avez pas été reconnu comme expéditeur valide.</span><span class="sxs-lookup"><span data-stu-id="2769a-108">"Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="2769a-109">Le plus souvent, il est possible que votre adresse de messagerie soit susceptible d’envoyer du courrier indésirable et qu’elle ne soit plus autorisée à envoyer du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="2769a-109">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send email.</span></span>  <span data-ttu-id="2769a-110">Contactez votre administrateur pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="2769a-110">Contact  your email admin for assistance.</span></span> <span data-ttu-id="2769a-111">Le serveur distant a renvoyé' 550 5.1.8 accès refusé, expéditeur sortant incorrect».</span><span class="sxs-lookup"><span data-stu-id="2769a-111">Remote Server returned '550 5.1.8 Access denied, bad outbound sender."</span></span>

<span data-ttu-id="2769a-112">Les administrateurs peuvent supprimer des utilisateurs du portail Expéditeurs restreints dans le centre de sécurité et conformité ou dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2769a-112">Admins can remove users from the Restricted Senders portal in the Security & Compliance Center or in Exchange Online PowerShell.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="2769a-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2769a-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="2769a-114">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="2769a-114">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="2769a-115">Pour accéder directement à la page **Utilisateurs restreints**, utilisez <https://protection.office.com/restrictedusers>.</span><span class="sxs-lookup"><span data-stu-id="2769a-115">To go directly to the **Restricted Users** page, use <https://protection.office.com/restrictedusers>.</span></span>

- <span data-ttu-id="2769a-116">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="2769a-116">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="2769a-117">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="2769a-117">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="2769a-118">Pour supprimer des utilisateurs du portail Utilisateurs restreints, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="2769a-118">To remove users from the Restricted Users portal, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="2769a-119">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2769a-119">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="2769a-120">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="2769a-120">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="2769a-121">Pour un accès en lecture seule au portail Utilisateurs restreints, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="2769a-121">For read-only access to the Restricted Users portal, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="2769a-122">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2769a-122">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="2769a-123">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="2769a-123">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="2769a-124">Un expéditeur dépassant la limite du nombre de messages sortants est un indicateur de compte compromis.</span><span class="sxs-lookup"><span data-stu-id="2769a-124">A sender exceeding the outbound email limits is an indicator of a compromised account.</span></span> <span data-ttu-id="2769a-125">Avant de supprimer l’utilisateur du portail Utilisateurs restreints, veillez à suivre les étapes nécessaires pour reprendre le contrôle de son compte.</span><span class="sxs-lookup"><span data-stu-id="2769a-125">Before you remove the user from the Restricted Users portal, be sure to follow the required steps to regain control of their account.</span></span> <span data-ttu-id="2769a-126">Pour plus informations, voir [Réponse à un compte de messagerie compromis dans Office 365](responding-to-a-compromised-email-account.md).</span><span class="sxs-lookup"><span data-stu-id="2769a-126">For more information, see [Responding to a compromised email account in Office 365](responding-to-a-compromised-email-account.md).</span></span>

## <a name="use-the-security--compliance-center-to-remove-a-user-from-the-restricted-users-list"></a><span data-ttu-id="2769a-127">Utiliser le Centre de sécurité et conformité pour supprimer un utilisateur de la liste Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="2769a-127">Use the Security & Compliance Center to remove a user from the Restricted Users list</span></span>

1. <span data-ttu-id="2769a-128">Dans le Centre de sécurité et conformité, accédez à **Gestion des menaces** \> **Examiner** \> **Utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="2769a-128">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Restricted users**.</span></span>

2. <span data-ttu-id="2769a-129">Recherchez et sélectionnez l’utilisateur que vous souhaitez débloquer.</span><span class="sxs-lookup"><span data-stu-id="2769a-129">Find and select the user that you want to unblock.</span></span> <span data-ttu-id="2769a-130">Dans la colonne **Actions**, cliquez sur **Débloquer**.</span><span class="sxs-lookup"><span data-stu-id="2769a-130">In the **Actions** column, click **Unblock**.</span></span>

3. <span data-ttu-id="2769a-131">Une fenêtre permet d’accéder aux informations relatives au compte dont l’envoi est restreint.</span><span class="sxs-lookup"><span data-stu-id="2769a-131">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="2769a-132">Nous vous conseillons de suivre les recommandations afin de vous assurer que vous effectuez les actions appropriées au cas où le compte serait réellement compromis.</span><span class="sxs-lookup"><span data-stu-id="2769a-132">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="2769a-133">Sélectionnez **Suivant** lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="2769a-133">Click **Next** when done.</span></span>

4. <span data-ttu-id="2769a-134">L’écran suivant comporte des recommandations pour empêcher toute compromission ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2769a-134">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="2769a-135">L’activation de l’authentification multifacteur (MFA) et la modification des mots de passe constituent une bonne défense.</span><span class="sxs-lookup"><span data-stu-id="2769a-135">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="2769a-136">Lorsque vous avez terminé, cliquez sur **débloquer l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="2769a-136">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="2769a-137">Cliquez sur **Oui** pour confirmer la modification.</span><span class="sxs-lookup"><span data-stu-id="2769a-137">Click **Yes** to confirm the change.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2769a-138">L’opération peut prendre jusqu’à 30 minutes avant la suppression des restrictions.</span><span class="sxs-lookup"><span data-stu-id="2769a-138">It may take 30 minutes or more before restrictions are removed.</span></span>

## <a name="verify-the-alert-settings-for-restricted-users"></a><span data-ttu-id="2769a-139">Vérifier les paramètres d’alerte pour les utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="2769a-139">Verify the alert settings for restricted users</span></span>

<span data-ttu-id="2769a-140">La stratégie d’alerte par défaut nommée **Utilisateur pour lequel l’envoi de courrier est restreint** avertit automatiquement les administrateurs lorsque les utilisateurs ne peuvent pas envoyer de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="2769a-140">The default alert policy named **User restricted from sending email** will automatically notify admins when users are blocked from sending outbound mail.</span></span> <span data-ttu-id="2769a-141">Vous pouvez vérifier ces paramètres et ajouter des utilisateurs à avertir.</span><span class="sxs-lookup"><span data-stu-id="2769a-141">You can verify these settings and add additional users to notify.</span></span> <span data-ttu-id="2769a-142">Pour plus d’informations sur les stratégies d’alerte, accédez à [Stratégies d’alerte dans le centre de sécurité et conformité](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="2769a-142">For more information about alert policies, see [Alert policies in the security and compliance center](../../compliance/alert-policies.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2769a-143">Pour que les alertes fonctionnent, la recherche dans le journal d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="2769a-143">For alerts to work, audit log search must to be turned on.</span></span> <span data-ttu-id="2769a-144">Pour plus d’informations, voir [Activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="2769a-144">For more information, see [Turn the audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

1. <span data-ttu-id="2769a-145">Dans le Centre de sécurité et conformité, accédez à **Alertes** \> **Stratégies d’alerte**.</span><span class="sxs-lookup"><span data-stu-id="2769a-145">In the Security & Compliance Center, go to **Alerts** \> **Alert policies**.</span></span>

2. <span data-ttu-id="2769a-146">Recherchez et sélectionnez l’alerte **Utilisateur pour lequel l’envoi de courrier est restreint**.</span><span class="sxs-lookup"><span data-stu-id="2769a-146">Find an select the **User restricted from sending email** alert.</span></span>

3. <span data-ttu-id="2769a-147">Dans le menu volant qui apparaît, vérifiez ou configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="2769a-147">In the flyout that appears, verify or configure the following settings:</span></span>

   - <span data-ttu-id="2769a-148">**État** : vérifiez que l’alerte est activée ![Activer](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png).</span><span class="sxs-lookup"><span data-stu-id="2769a-148">**Status**: Verify the alert is turned on ![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png).</span></span>

   - <span data-ttu-id="2769a-149">**Destinataires de courrier** : cliquez sur **Modifier** et vérifiez ou configurez les paramètres suivants dans le menu volant **Modifier les destinataires** qui apparaît :</span><span class="sxs-lookup"><span data-stu-id="2769a-149">**Email recipients**: Click **Edit** and verify or configure the following settings in the **Edit recipients** flyout that appears:</span></span>

     - <span data-ttu-id="2769a-150">**Envoyer des notifications par courrier** : vérifiez que la case est cochée (**Activé**).</span><span class="sxs-lookup"><span data-stu-id="2769a-150">**Send email notifications**: Verify the check box is selected (**On**).</span></span>

     - <span data-ttu-id="2769a-151">**Destinataires du courrier** : la valeur par défaut est **TenantAdmins** (c’est-à-dire membres de type **Administrateur général**).</span><span class="sxs-lookup"><span data-stu-id="2769a-151">**Email recipients**: The default value is **TenantAdmins** (meaning, **Global admin** members).</span></span> <span data-ttu-id="2769a-152">Pour ajouter des destinataires, cliquez sur une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="2769a-152">To add more recipients, click in a blank area of the box.</span></span> <span data-ttu-id="2769a-153">Une liste de destinataires apparaît, puis vous pouvez commencer à saisir un nom pour filtrer et sélectionner un destinataire.</span><span class="sxs-lookup"><span data-stu-id="2769a-153">A list of recipients will appear, and you can start typing a name to filter and select a recipient.</span></span> <span data-ttu-id="2769a-154">Vous pouvez supprimer un destinataire existant de la zone en cliquant sur ![Icône Supprimer](../../media/scc-remove-icon.png) en regard de son nom.</span><span class="sxs-lookup"><span data-stu-id="2769a-154">You can remove an existing recipient from the box by clicking ![Remove icon](../../media/scc-remove-icon.png) next to their name.</span></span>

     - <span data-ttu-id="2769a-155">**Limite quotidienne de notification** : la valeur par défaut est **Aucune limite**, mais vous pouvez sélectionner une limite pour le nombre maximal de notifications par jour.</span><span class="sxs-lookup"><span data-stu-id="2769a-155">**Daily notification limit**: The default value is **No limit** but you can select a limit for the maximum number of notifications per day.</span></span>

     <span data-ttu-id="2769a-156">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2769a-156">When you're finished, click **Save**.</span></span>

4. <span data-ttu-id="2769a-157">De retour dans le menu roulant **Utilisateur pour lequel l’envoi de courrier est restreint**, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2769a-157">Back on the **User restricted from sending email** flyout, click **Close**.</span></span>

## <a name="use-exchange-online-powershell-to-view-and-remove-users-from-the-restricted-users-list"></a><span data-ttu-id="2769a-158">Utiliser Exchange Online PowerShell pour afficher et supprimer des utilisateurs de la liste Utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="2769a-158">Use Exchange Online PowerShell to view and remove users from the Restricted Users list</span></span>

<span data-ttu-id="2769a-159">Pour afficher cette liste d’utilisateurs pour lesquels l’envoi de courrier est restreint, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2769a-159">To view this list of users that are restricted from sending email, run the following command:</span></span>

```powershell
Get-BlockedSenderAddress
```

<span data-ttu-id="2769a-160">Pour afficher les détails d’un utilisateur spécifique, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2769a-160">To view details about a specific user, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Get-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="2769a-161">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Get-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/get-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="2769a-161">For detailed syntax and parameter information, see [Get-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/get-blockedsenderaddress).</span></span>

<span data-ttu-id="2769a-162">Pour supprimer un utilisateur de la liste Utilisateurs restreints, remplacez \<emailaddress\> par son adresse e-mail, puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2769a-162">To remove a user from the Restricted Users list, replace \<emailaddress\> with their email address and run the following command:</span></span>

```powershell
Remove-BlockedSenderAddress -SenderAddress <emailaddress>
```

<span data-ttu-id="2769a-163">Pour des informations détaillées sur la syntaxe et les paramètres, voir [Remove-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/remove-blockedsenderaddress).</span><span class="sxs-lookup"><span data-stu-id="2769a-163">For detailed syntax and parameter information, see [Remove-BlockedSenderAddress](https://docs.microsoft.com/powershell/module/exchange/remove-blockedsenderaddress).</span></span>
