---
title: Configurer des stratégies de pièces jointes sécurisées dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
ms.collection:
- M365-security-compliance
description: Découvrez comment définir des stratégies de pièces jointes sécurisées pour protéger votre organisation contre les fichiers malveillants dans le courrier électronique.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d48e373dc95aaa65d0f436f99208d926477aacd6
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918713"
---
# <a name="set-up-safe-attachments-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="408b7-103">Configurer des stratégies de pièces jointes sécurisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="408b7-103">Set up Safe Attachments policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="408b7-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="408b7-104">**Applies to**</span></span>
- [<span data-ttu-id="408b7-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="408b7-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="408b7-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="408b7-106">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

> [!IMPORTANT]
> <span data-ttu-id="408b7-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="408b7-107">This article is intended for business customers who have [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="408b7-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur l’analyse des pièces jointes dans Outlook, voir [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="408b7-108">If you're a home user looking for information about attachment scanning in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="408b7-109">La fonctionnalité Pièces jointes sécurisées de Microsoft Defender pour [Office 365](office-365-atp.md) utilise un environnement virtuel pour vérifier les pièces jointes dans les messages électroniques entrants une fois qu’elles ont été analysées par la protection anti-programme malveillant dans [Exchange Online Protection (EOP),](anti-malware-protection.md)mais avant leur remise aux destinataires.</span><span class="sxs-lookup"><span data-stu-id="408b7-109">Safe Attachments is a feature in [Microsoft Defender for Office 365](office-365-atp.md) that uses a virtual environment to check attachments in inbound email messages after they've been scanned by [anti-malware protection in Exchange Online Protection (EOP)](anti-malware-protection.md), but before delivery to recipients.</span></span> <span data-ttu-id="408b7-110">Pour plus d’informations, [voir Pièces jointes sécurisées dans Microsoft Defender pour Office 365.](atp-safe-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="408b7-110">For more information, see [Safe Attachments in Microsoft Defender for Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="408b7-111">Il n’existe aucune stratégie de pièces jointes sécurisées intégrée ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="408b7-111">There's no built-in or default Safe Attachments policy.</span></span> <span data-ttu-id="408b7-112">Pour obtenir l’analyse des pièces jointes des messages électroniques, vous devez créer une ou plusieurs stratégies de pièces jointes sécurisées, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="408b7-112">To get Safe Attachments scanning of email message attachments, you need to create one or more Safe Attachments policies as described in this article.</span></span>

<span data-ttu-id="408b7-113">Vous pouvez configurer des stratégies de pièces jointes sécurisées dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec des abonnements de modules add-on Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="408b7-113">You can configure Safe Attachments policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="408b7-114">Les éléments de base d’une stratégie de pièces jointes sécurisées sont :</span><span class="sxs-lookup"><span data-stu-id="408b7-114">The basic elements of a Safe Attachments policy are:</span></span>

- <span data-ttu-id="408b7-115">La stratégie de pièces jointes fiables : spécifie les actions pour les détections de programmes malveillants inconnus, s’il faut envoyer des messages avec des pièces jointes à une adresse e-mail spécifiée et s’il faut remettre des messages si l’analyse des pièces jointes fiables ne peut pas se terminer.</span><span class="sxs-lookup"><span data-stu-id="408b7-115">**The safe attachment policy**: Specifies the actions for unknown malware detections, whether to send messages with malware attachments to a specified email address, and whether to deliver messages if Safe Attachments scanning can't complete.</span></span>
- <span data-ttu-id="408b7-116">**La règle de pièce jointe sécurisée**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique).</span><span class="sxs-lookup"><span data-stu-id="408b7-116">**The safe attachment rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="408b7-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez les polices de pièces jointes sécurisées dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="408b7-117">The difference between these two elements isn't obvious when you manage Safe Attachments polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="408b7-118">Lorsque vous créez une stratégie de pièces jointes sécurisées, vous créez en fait une règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="408b7-118">When you create a Safe Attachments policy, you're actually creating a safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="408b7-119">Lorsque vous modifiez une stratégie de pièces jointes sécurisées, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle de pièce jointe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="408b7-119">When you modify a Safe Attachments policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe attachment rule.</span></span> <span data-ttu-id="408b7-120">Tous les autres paramètres modifient la stratégie de pièce jointe sécurisée associée.</span><span class="sxs-lookup"><span data-stu-id="408b7-120">All other settings modify the associated safe attachment policy.</span></span>
- <span data-ttu-id="408b7-121">Lorsque vous supprimez une stratégie de pièces jointes sécurisées, la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="408b7-121">When you remove a Safe Attachments policy, the safe attachment rule and the associated safe attachment policy are removed.</span></span>

<span data-ttu-id="408b7-122">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="408b7-122">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="408b7-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de pièces [jointes sécurisées](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="408b7-123">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="408b7-124">Dans la zone des paramètres globaux des paramètres de pièces jointes sécurisées, vous configurez les fonctionnalités qui ne dépendent pas des stratégies de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-124">In the global settings area of Safe Attachments settings, you configure features that are not dependent on Safe Attachments policies.</span></span> <span data-ttu-id="408b7-125">Pour obtenir des instructions, voir Activer les pièces [jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md) et les documents sécurisés dans Microsoft [365 E5.](safe-docs.md)</span><span class="sxs-lookup"><span data-stu-id="408b7-125">For instructions see [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md) and [Safe Documents in Microsoft 365 E5](safe-docs.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="408b7-126">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="408b7-126">What do you need to know before you begin?</span></span>

- <span data-ttu-id="408b7-127">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="408b7-127">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="408b7-128">Pour aller directement à la page **Pièces jointes sécurisées,** utilisez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="408b7-128">To go directly to the **Safe Attachments** page, use <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="408b7-129">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="408b7-129">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="408b7-130">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="408b7-130">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="408b7-131">Des autorisations doivent vous être attribuées avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="408b7-131">You need to be assigned permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="408b7-132">Pour créer, modifier et supprimer des stratégies de pièces  jointes sécurisées, vous devez être membre des groupes de  rôles Gestion de l’organisation ou Administrateur de la sécurité dans le Centre de sécurité & conformité et membre du groupe de rôles Gestion de l’organisation dans Exchange Online.  </span><span class="sxs-lookup"><span data-stu-id="408b7-132">To create, modify, and delete Safe Attachments policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center **and** a member of the **Organization Management** role group in Exchange Online.</span></span>
  - <span data-ttu-id="408b7-133">Pour accéder en lecture seule aux stratégies de pièces  jointes  sécurisées, vous devez être membre des groupes de rôles Lecteur général ou Lecteur sécurité dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="408b7-133">For read-only access to Safe Attachments policies, you need to be a member of the **Global Reader** or **Security Reader** role groups in the Security & Compliance Center.</span></span>

  <span data-ttu-id="408b7-134">Pour plus d’informations, [voir Autorisations](permissions-in-the-security-and-compliance-center.md) dans le Centre de sécurité & conformité et [autorisations dans Exchange Online.](/exchange/permissions-exo/permissions-exo)</span><span class="sxs-lookup"><span data-stu-id="408b7-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) and [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="408b7-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="408b7-135">**Notes**:</span></span>

  - <span data-ttu-id="408b7-136">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="408b7-136">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="408b7-137">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="408b7-137">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="408b7-138">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="408b7-138">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="408b7-139">Pour obtenir nos paramètres recommandés pour les stratégies de pièces jointes sécurisées, voir [Paramètres des pièces jointes sécurisées.](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings)</span><span class="sxs-lookup"><span data-stu-id="408b7-139">For our recommended settings for Safe Attachments policies, see [Safe Attachments settings](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span></span>

- <span data-ttu-id="408b7-140">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="408b7-140">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

## <a name="use-the-security--compliance-center-to-create-safe-attachments-policies"></a><span data-ttu-id="408b7-141">Utiliser le Centre de sécurité & conformité pour créer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-141">Use the Security & Compliance Center to create Safe Attachments policies</span></span>

<span data-ttu-id="408b7-142">La création d’une stratégie de pièces jointes sécurisées personnalisée dans le Centre de sécurité & conformité crée la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="408b7-142">Creating a custom Safe Attachments policy in the Security & Compliance Center creates the safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="408b7-143">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-143">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-144">Dans la page **Pièces jointes sécurisées,** cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="408b7-144">On the **Safe Attachments** page, click **Create**.</span></span>

3. <span data-ttu-id="408b7-145">**L’Assistant Nouvelle stratégie de pièces jointes sécurisées** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="408b7-145">The **New Safe Attachments policy** wizard opens.</span></span> <span data-ttu-id="408b7-146">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="408b7-146">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="408b7-147">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="408b7-147">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="408b7-148">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="408b7-148">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="408b7-149">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="408b7-149">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="408b7-150">Dans la page **Paramètres** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="408b7-150">On the **Settings** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="408b7-151">**Réponse aux programmes malveillants inconnus** pour les pièces jointes sécurisées : sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="408b7-151">**Safe Attachments unknown malware response**: Select one of the following values:</span></span>

     - <span data-ttu-id="408b7-152">**Off**: En règle générale, nous ne recommandons pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="408b7-152">**Off**: Typically, we don't recommend this value.</span></span>
     - <span data-ttu-id="408b7-153">**Moniteur**</span><span class="sxs-lookup"><span data-stu-id="408b7-153">**Monitor**</span></span>
     - <span data-ttu-id="408b7-154">**Bloc**: il s’agit de la valeur par défaut et de la valeur recommandée dans les stratégies de sécurité standard [et](preset-security-policies.md)stricte.</span><span class="sxs-lookup"><span data-stu-id="408b7-154">**Block**: This is the default value, and the recommended value in Standard and Strict [preset security policies](preset-security-policies.md).</span></span>
     - <span data-ttu-id="408b7-155">**Remplacer**</span><span class="sxs-lookup"><span data-stu-id="408b7-155">**Replace**</span></span>
     - <span data-ttu-id="408b7-156">**Remise dynamique (fonctionnalité d’aperçu)**</span><span class="sxs-lookup"><span data-stu-id="408b7-156">**Dynamic Delivery (Preview Feature)**</span></span>

     <span data-ttu-id="408b7-157">Ces valeurs sont expliquées dans les paramètres de stratégie [de pièces jointes sécurisées.](atp-safe-attachments.md#safe-attachments-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="408b7-157">These values are explained in [Safe Attachments policy settings](atp-safe-attachments.md#safe-attachments-policy-settings).</span></span>

   - <span data-ttu-id="408b7-158">Envoyez la pièce jointe à l’adresse de messagerie suivante : Pour les valeurs d’action **Bloquer,** Surveiller ou **Remplacer,** vous pouvez sélectionner Activer la **redirection** pour envoyer des messages contenant des pièces jointes contenant des programmes malveillants à l’adresse de messagerie interne ou externe spécifiée pour analyse et examen.</span><span class="sxs-lookup"><span data-stu-id="408b7-158">**Send the attachment to the following email address**: For the action values **Block**, **Monitor**, or **Replace**, you can select **Enable redirect** to send messages that contain malware attachments to the specified internal or external email address for analysis and investigation.</span></span>

     <span data-ttu-id="408b7-159">La recommandation pour les paramètres de stratégie Standard et Strict consiste à activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="408b7-159">The recommendation for Standard and Strict policy settings is to enable redirection.</span></span> <span data-ttu-id="408b7-160">Pour plus d’informations, [voir Paramètres des pièces jointes sécurisées.](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings)</span><span class="sxs-lookup"><span data-stu-id="408b7-160">For more information, see [Safe Attachments settings](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span></span>

   - <span data-ttu-id="408b7-161">Appliquez la sélection ci-dessus si l’analyse des programmes **malveillants** pour les pièces jointes arrive à arriver ou si une erreur se produit : l’action spécifiée par la réponse de programmes malveillants inconnus de pièces **jointes sécurisées** est appliquée aux messages même lorsque l’analyse des pièces jointes sécurisées ne peut pas se terminer.</span><span class="sxs-lookup"><span data-stu-id="408b7-161">**Apply the above selection if malware scanning for attachments times out or error occurs**: The action specified by **Safe Attachments unknown malware response** is taken on messages even when Safe Attachments scanning can't complete.</span></span> <span data-ttu-id="408b7-162">Si vous avez sélectionné cette option, sélectionnez toujours **Redirection activée.**</span><span class="sxs-lookup"><span data-stu-id="408b7-162">If you selected this option, always select **Enabled redirect**.</span></span> <span data-ttu-id="408b7-163">Dans le cas contraire, les messages peuvent être perdus.</span><span class="sxs-lookup"><span data-stu-id="408b7-163">Otherwise, messages might be lost.</span></span>

   <span data-ttu-id="408b7-164">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="408b7-164">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="408b7-165">Dans la page **Appliqué à** qui s’affiche, identifiez les destinataires internes à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="408b7-165">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="408b7-166">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="408b7-166">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="408b7-167">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="408b7-167">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="408b7-168">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="408b7-168">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="408b7-169">Cliquez **sur Ajouter une condition.**</span><span class="sxs-lookup"><span data-stu-id="408b7-169">Click **Add a condition**.</span></span> <span data-ttu-id="408b7-170">Dans ladown qui s’affiche, sélectionnez une condition sous **Applied si**:</span><span class="sxs-lookup"><span data-stu-id="408b7-170">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="408b7-171">**Le destinataire est**: Spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="408b7-171">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="408b7-172">**Le destinataire est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="408b7-172">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="408b7-173">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="408b7-173">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="408b7-174">Une fois que vous avez sélectionné la condition, une zone « Tout » apparaît dans la zone « **Tout le** monde ».</span><span class="sxs-lookup"><span data-stu-id="408b7-174">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="408b7-175">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="408b7-175">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="408b7-176">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="408b7-176">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="408b7-177">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="408b7-177">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="408b7-178">Pour supprimer des entrées individuelles, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="408b7-178">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="408b7-179">Pour supprimer la condition entière, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la condition.</span><span class="sxs-lookup"><span data-stu-id="408b7-179">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="408b7-180">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous Appliqué **si**.</span><span class="sxs-lookup"><span data-stu-id="408b7-180">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="408b7-181">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous Sauf **si**.</span><span class="sxs-lookup"><span data-stu-id="408b7-181">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="408b7-182">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="408b7-182">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="408b7-183">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="408b7-183">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="408b7-184">Dans la page **Examiner vos paramètres** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="408b7-184">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="408b7-185">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="408b7-185">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="408b7-186">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="408b7-186">When you're finished, click **Finish**.</span></span>

## <a name="use-the-security--compliance-center-to-view-safe-attachments-policies"></a><span data-ttu-id="408b7-187">Utiliser le Centre de sécurité & conformité pour afficher les stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-187">Use the Security & Compliance Center to view Safe Attachments policies</span></span>

1. <span data-ttu-id="408b7-188">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-188">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-189">Dans la page **Pièces jointes sécurisées,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="408b7-189">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

   <span data-ttu-id="408b7-190">Les détails de la stratégie apparaissent dans un volant</span><span class="sxs-lookup"><span data-stu-id="408b7-190">The policy details appear in a fly out</span></span>

## <a name="use-the-security--compliance-center-to-modify-safe-attachments-policies"></a><span data-ttu-id="408b7-191">Utiliser le Centre de sécurité & conformité pour modifier les stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-191">Use the Security & Compliance Center to modify Safe Attachments policies</span></span>

1. <span data-ttu-id="408b7-192">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-192">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-193">Dans la page **Pièces jointes sécurisées,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="408b7-193">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="408b7-194">Dans le volant des détails de stratégie qui s’affiche, cliquez **sur Modifier la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="408b7-194">In the policy details fly out that appears, click **Edit policy**.</span></span>

<span data-ttu-id="408b7-195">Les paramètres disponibles dans le volant qui s’affiche sont identiques à ceux décrits dans la section Utiliser le Centre de sécurité & conformité pour créer des stratégies de pièces [jointes sécurisées.](#use-the-security--compliance-center-to-create-safe-attachments-policies)</span><span class="sxs-lookup"><span data-stu-id="408b7-195">The available settings in the fly out that appears are identical to those described in the [Use the Security & Compliance Center to create Safe Attachments policies](#use-the-security--compliance-center-to-create-safe-attachments-policies) section.</span></span>

<span data-ttu-id="408b7-196">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="408b7-196">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-attachments-policies"></a><span data-ttu-id="408b7-197">Activer ou désactiver les stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-197">Enable or disable Safe Attachments policies</span></span>

1. <span data-ttu-id="408b7-198">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-198">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-199">Notez la valeur dans la **colonne État** :</span><span class="sxs-lookup"><span data-stu-id="408b7-199">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="408b7-200">Déplacer le basculement vers la gauche</span><span class="sxs-lookup"><span data-stu-id="408b7-200">Move the toggle to the left</span></span> ![Désactiver la stratégie](../../media/scc-toggle-off.png) <span data-ttu-id="408b7-202">pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="408b7-202">to disable the policy.</span></span>

   - <span data-ttu-id="408b7-203">Déplacer le basculement vers la droite</span><span class="sxs-lookup"><span data-stu-id="408b7-203">Move the toggle to the right</span></span> ![Activer la stratégie](../../media/scc-toggle-on.png) <span data-ttu-id="408b7-205">pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="408b7-205">to enable the policy.</span></span>

### <a name="set-the-priority-of-safe-attachments-policies"></a><span data-ttu-id="408b7-206">Définir la priorité des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-206">Set the priority of Safe Attachments policies</span></span>

<span data-ttu-id="408b7-207">Par défaut, les stratégies de pièces jointes sécurisées ont une priorité qui est basée sur l’ordre dans quoi elles ont été créées (les stratégies les plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="408b7-207">By default, Safe Attachments policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="408b7-208">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="408b7-208">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="408b7-209">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="408b7-209">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="408b7-210">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="408b7-210">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="408b7-211">Les stratégies de pièces jointes sécurisées sont affichées dans l’ordre de traitement (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="408b7-211">Safe Attachments policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

<span data-ttu-id="408b7-212">**Remarque**: dans le Centre de sécurité & conformité, vous ne pouvez modifier la priorité de la stratégie de pièces jointes sécurisées qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="408b7-212">**Note**: In the Security & Compliance Center, you can only change the priority of the Safe Attachments policy after you create it.</span></span> <span data-ttu-id="408b7-213">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle de pièce jointe sécurisée (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="408b7-213">In PowerShell, you can override the default priority when you create the safe attachment rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="408b7-214">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="408b7-214">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="408b7-215">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-215">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-216">Dans la page **Pièces jointes sécurisées,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="408b7-216">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="408b7-217">Dans le volant des détails de stratégie qui s’affiche, cliquez sur le bouton de priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="408b7-217">In the policy details fly out that appears, click the available priority button.</span></span>

   - <span data-ttu-id="408b7-218">La stratégie pièces jointes sécurisées avec la valeur **de** priorité **0** ne dispose que **du** bouton Diminuer la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="408b7-218">The Safe Attachments policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="408b7-219">La stratégie pièces jointes sécurisées dont la valeur **de** priorité est la plus faible **(par** exemple, 3 ) ne dispose que du bouton **Augmenter** la priorité.</span><span class="sxs-lookup"><span data-stu-id="408b7-219">The Safe Attachments policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="408b7-220">Si vous avez au moins trois stratégies de pièces jointes sécurisées,  les stratégies entre les valeurs de priorité les plus élevées et les plus faibles disposent des boutons Augmenter la priorité et Diminuer la priorité. </span><span class="sxs-lookup"><span data-stu-id="408b7-220">If you have three or more Safe Attachments policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="408b7-221">Cliquez **sur Augmenter la priorité** ou Diminuer la **priorité** pour modifier la **valeur** Priorité.</span><span class="sxs-lookup"><span data-stu-id="408b7-221">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="408b7-222">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="408b7-222">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-safe-attachments-policies"></a><span data-ttu-id="408b7-223">Utiliser le Centre de sécurité & conformité pour supprimer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-223">Use the Security & Compliance Center to remove Safe Attachments policies</span></span>

1. <span data-ttu-id="408b7-224">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-224">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="408b7-225">Dans la page **Pièces jointes sécurisées,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="408b7-225">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="408b7-226">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur Supprimer la **stratégie,** puis cliquez sur **Oui.**</span><span class="sxs-lookup"><span data-stu-id="408b7-226">In the policy details fly out that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies"></a><span data-ttu-id="408b7-227">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-227">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies</span></span>

<span data-ttu-id="408b7-228">Comme décrit précédemment, une stratégie de pièces jointes sécurisées se compose d’une stratégie de pièces jointes sécurisées et d’une règle de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-228">As previously described, a Safe Attachments policy consists of a safe attachment policy and a safe attachment rule.</span></span>

<span data-ttu-id="408b7-229">Dans PowerShell, la différence entre les stratégies de pièces jointes sécurisées et les règles de pièces jointes sécurisées est évidente.</span><span class="sxs-lookup"><span data-stu-id="408b7-229">In PowerShell, the difference between safe attachment policies and safe attachment rules is apparent.</span></span> <span data-ttu-id="408b7-230">Vous gérez les stratégies de pièces jointes sécurisées à l’aide des cmdlets **\* -SafeAttachmentPolicy** et vous gérez les règles de pièces jointes sécurisées à l’aide des cmdlets **\* -SafeAttachmentRule.**</span><span class="sxs-lookup"><span data-stu-id="408b7-230">You manage safe attachment policies by using the **\*-SafeAttachmentPolicy** cmdlets, and you manage safe attachment rules by using the **\*-SafeAttachmentRule** cmdlets.</span></span>

- <span data-ttu-id="408b7-231">Dans PowerShell, vous créez d’abord la stratégie de pièces jointes sécurisées, puis vous créez la règle de pièce jointe sécurisée qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="408b7-231">In PowerShell, you create the safe attachment policy first, then you create the safe attachment rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="408b7-232">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de pièces jointes sécurisées et de la règle de pièce jointe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="408b7-232">In PowerShell, you modify the settings in the safe attachment policy and the safe attachment rule separately.</span></span>
- <span data-ttu-id="408b7-233">Lorsque vous supprimez une stratégie de pièces jointes sécurisées de PowerShell, la règle de pièce jointe sécurisée correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="408b7-233">When you remove a safe attachment policy from PowerShell, the corresponding safe attachment rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-attachments-policies"></a><span data-ttu-id="408b7-234">Utiliser PowerShell pour créer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-234">Use PowerShell to create Safe Attachments policies</span></span>

<span data-ttu-id="408b7-235">La création d’une stratégie de pièces jointes sécurisées dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="408b7-235">Creating a Safe Attachments policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="408b7-236">Créez la stratégie de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-236">Create the safe attachment policy.</span></span>
2. <span data-ttu-id="408b7-237">Créez la règle de pièce jointe sécurisée qui spécifie la stratégie de pièces jointes sécurisées à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="408b7-237">Create the safe attachment rule that specifies the safe attachment policy that the rule applies to.</span></span>

 <span data-ttu-id="408b7-238">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="408b7-238">**Notes**:</span></span>

- <span data-ttu-id="408b7-239">Vous pouvez créer une règle de pièce jointe sécurisée et lui attribuer une stratégie de pièces jointes sécurisées existante non attachée.</span><span class="sxs-lookup"><span data-stu-id="408b7-239">You can create a new safe attachment rule and assign an existing, unassociated safe attachment policy to it.</span></span> <span data-ttu-id="408b7-240">Une règle de pièce jointe sécurisée ne peut pas être associée à plusieurs stratégies de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-240">A safe attachment rule can't be associated with more than one safe attachment policy.</span></span>

- <span data-ttu-id="408b7-241">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de pièces jointes sécurisées dans PowerShell qui ne sont pas disponibles dans le Centre de sécurité & conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="408b7-241">You can configure the following settings on new safe attachment policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>
  - <span data-ttu-id="408b7-242">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-SafeAttachmentRule).**</span><span class="sxs-lookup"><span data-stu-id="408b7-242">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeAttachmentRule** cmdlet).</span></span>
  - <span data-ttu-id="408b7-243">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-SafeAttachmentRule).**</span><span class="sxs-lookup"><span data-stu-id="408b7-243">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeAttachmentRule** cmdlet).</span></span>

- <span data-ttu-id="408b7-244">Une nouvelle stratégie de pièces jointes sécurisées que vous créez dans PowerShell n’est pas visible dans le Centre de sécurité & conformité tant que vous n’avez pas attribué la stratégie à une règle de pièce jointe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="408b7-244">A new safe attachment policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a safe attachment rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-attachment-policy"></a><span data-ttu-id="408b7-245">Étape 1 : Utiliser PowerShell pour créer une stratégie de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-245">Step 1: Use PowerShell to create a safe attachment policy</span></span>

<span data-ttu-id="408b7-246">Pour créer une stratégie de pièces jointes sécurisées, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-246">To create a safe attachment policy, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-Action <Allow | Block | Replace | DynamicDelivery>] [-Redirect <$true | $false>] [-RedirectAddress <SMTPEmailAddress>] [-ActionOnError <$true | $false>]
```

<span data-ttu-id="408b7-247">Cet exemple crée une stratégie de pièce jointe sécurisée nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="408b7-247">This example creates a safe attachment policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="408b7-248">Bloquer les messages qui contiennent des programmes malveillants par l’analyse des documents sécurisés (nous n’utilisons pas le paramètre _Action,_ et la valeur par défaut est `Block` ).</span><span class="sxs-lookup"><span data-stu-id="408b7-248">Block messages that are found to contain malware by Safe Documents scanning (we aren't using the _Action_ parameter, and the default value is `Block`).</span></span>
- <span data-ttu-id="408b7-249">La redirection est activée et les messages qui contiennent des programmes malveillants sont envoyés sec-ops@contoso.com pour analyse et examen.</span><span class="sxs-lookup"><span data-stu-id="408b7-249">Redirection is enabled, and messages that are found to contain malware are sent to sec-ops@contoso.com for analysis and investigation.</span></span>
- <span data-ttu-id="408b7-250">Si l’analyse des pièces jointes sécurisées n’est pas disponible ou rencontre des erreurs, ne remettre pas le message (nous n’utilisons pas le paramètre _ActionOnError_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="408b7-250">If Safe Attachments scanning isn't available or encounters errors, don't deliver the message (we aren't using the _ActionOnError_ parameter, and the default value is `$true`).</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "Contoso All" -Redirect $true -RedirectAddress sec-ops@contoso.com
```

<span data-ttu-id="408b7-251">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeAttachmentPolicy](/powershell/module/exchange/new-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="408b7-251">For detailed syntax and parameter information, see [New-SafeAttachmentPolicy](/powershell/module/exchange/new-safeattachmentpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-attachment-rule"></a><span data-ttu-id="408b7-252">Étape 2 : Utiliser PowerShell pour créer une règle de pièce jointe sécurisée</span><span class="sxs-lookup"><span data-stu-id="408b7-252">Step 2: Use PowerShell to create a safe attachment rule</span></span>

<span data-ttu-id="408b7-253">Pour créer une règle de pièce jointe sécurisée, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-253">To create a safe attachment rule, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentRule -Name "<RuleName>" -SafeAttachmentPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="408b7-254">Cet exemple crée une règle de pièce jointe sécurisée nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="408b7-254">This example creates a safe attachment rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="408b7-255">La règle est associée à la stratégie de pièces jointes sécurisée nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="408b7-255">The rule is associated with the safe attachment policy named Contoso All.</span></span>
- <span data-ttu-id="408b7-256">La règle s’applique à tous les destinataires du contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="408b7-256">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="408b7-257">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="408b7-257">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="408b7-258">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="408b7-258">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeAttachmentRule -Name "Contoso All" -SafeAttachmentPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="408b7-259">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeAttachmentRule](/powershell/module/exchange/new-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-259">For detailed syntax and parameter information, see [New-SafeAttachmentRule](/powershell/module/exchange/new-safeattachmentrule).</span></span>

### <a name="use-powershell-to-view-safe-attachment-policies"></a><span data-ttu-id="408b7-260">Utiliser PowerShell pour afficher les stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-260">Use PowerShell to view safe attachment policies</span></span>

<span data-ttu-id="408b7-261">Pour afficher les stratégies de pièces jointes sécurisées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-261">To view existing safe attachment policies, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="408b7-262">Cet exemple renvoie une liste récapitulatif de toutes les stratégies de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-262">This example returns a summary list of all safe attachment policies.</span></span>

```PowerShell
Get-SafeAttachmentPolicy
```

<span data-ttu-id="408b7-263">Cet exemple renvoie des informations détaillées sur la stratégie de pièces jointes sécurisée nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="408b7-263">This example returns detailed information for the safe attachment policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentPolicy -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="408b7-264">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SafeAttachmentPolicy](/powershell/module/exchange/get-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="408b7-264">For detailed syntax and parameter information, see [Get-SafeAttachmentPolicy](/powershell/module/exchange/get-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-view-safe-attachment-rules"></a><span data-ttu-id="408b7-265">Utiliser PowerShell pour afficher les règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-265">Use PowerShell to view safe attachment rules</span></span>

<span data-ttu-id="408b7-266">Pour afficher les règles de pièces jointes sécurisées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-266">To view existing safe attachment rules, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled>] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="408b7-267">Cet exemple renvoie une liste récapitulatif de toutes les règles de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="408b7-267">This example returns a summary list of all safe attachment rules.</span></span>

```PowerShell
Get-SafeAttachmentRule
```

<span data-ttu-id="408b7-268">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="408b7-268">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeAttachmentRule -State Disabled
```

```PowerShell
Get-SafeAttachmentRule -State Enabled
```

<span data-ttu-id="408b7-269">Cet exemple renvoie des informations détaillées sur la règle de pièce jointe sécurisée nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="408b7-269">This example returns detailed information for the safe attachment rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="408b7-270">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SafeAttachmentRule](/powershell/module/exchange/get-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-270">For detailed syntax and parameter information, see [Get-SafeAttachmentRule](/powershell/module/exchange/get-safeattachmentrule).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-policies"></a><span data-ttu-id="408b7-271">Utiliser PowerShell pour modifier des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-271">Use PowerShell to modify safe attachment policies</span></span>

<span data-ttu-id="408b7-272">Vous ne pouvez pas renommer une stratégie de pièces jointes sécurisées dans PowerShell (la cmdlet **Set-SafeAttachmentPolicy** n’a pas de _paramètre_ Name).</span><span class="sxs-lookup"><span data-stu-id="408b7-272">You can't rename a safe attachment policy in PowerShell (the **Set-SafeAttachmentPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="408b7-273">Lorsque vous renommez une stratégie de pièces jointes sécurisées dans le Centre de sécurité & conformité, vous renommez uniquement la règle de pièces jointes _sécurisées._</span><span class="sxs-lookup"><span data-stu-id="408b7-273">When you rename a Safe Attachments policy in the Security & Compliance Center, you're only renaming the safe attachment _rule_.</span></span>

<span data-ttu-id="408b7-274">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de pièces jointes sécurisées, comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-a-safe-attachment-policy) pour créer une section sur la stratégie de pièces jointes sécurisées plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="408b7-274">Otherwise, the same settings are available when you create a safe attachment policy as described in the [Step 1: Use PowerShell to create a safe attachment policy](#step-1-use-powershell-to-create-a-safe-attachment-policy) section earlier in this article.</span></span>

<span data-ttu-id="408b7-275">Pour modifier une stratégie de pièces jointes sécurisées, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-275">To modify a safe attachment policy, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="408b7-276">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentPolicy](/powershell/module/exchange/set-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="408b7-276">For detailed syntax and parameter information, see [Set-SafeAttachmentPolicy](/powershell/module/exchange/set-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-rules"></a><span data-ttu-id="408b7-277">Utiliser PowerShell pour modifier des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-277">Use PowerShell to modify safe attachment rules</span></span>

<span data-ttu-id="408b7-278">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de pièce jointe sécurisée dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="408b7-278">The only setting that's not available when you modify a safe attachment rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="408b7-279">Pour activer ou désactiver des règles de pièces jointes sécurisées existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="408b7-279">To enable or disable existing safe attachment rules, see the next section.</span></span>

<span data-ttu-id="408b7-280">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-a-safe-attachment-rule) pour créer une section de règle de pièce jointe sécurisée plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="408b7-280">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe attachment rule](#step-2-use-powershell-to-create-a-safe-attachment-rule) section earlier in this article.</span></span>

<span data-ttu-id="408b7-281">Pour modifier une règle de pièce jointe sécurisée, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-281">To modify a safe attachment rule, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="408b7-282">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-282">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-attachment-rules"></a><span data-ttu-id="408b7-283">Utiliser PowerShell pour activer ou désactiver les règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-283">Use PowerShell to enable or disable safe attachment rules</span></span>

<span data-ttu-id="408b7-284">L’activation ou la désactivation d’une règle de pièce jointe sécurisée dans PowerShell active ou désactive l’ensemble de la stratégie de pièces jointes sécurisées (la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées affectée).</span><span class="sxs-lookup"><span data-stu-id="408b7-284">Enabling or disabling a safe attachment rule in PowerShell enables or disables the whole Safe Attachments policy (the safe attachment rule and the assigned safe attachment policy).</span></span>

<span data-ttu-id="408b7-285">Pour activer ou désactiver une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-285">To enable or disable a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeAttachmentRule | Disable-SafeAttachmentRule> -Identity "<RuleName>"
```

<span data-ttu-id="408b7-286">Cet exemple désactive la règle de pièce jointe sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="408b7-286">This example disables the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="408b7-287">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="408b7-287">This example enables same rule.</span></span>

```PowerShell
Enable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="408b7-288">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-SafeAttachmentRule](/powershell/module/exchange/enable-safeattachmentrule) et [Disable-SafeAttachmentRule](/powershell/module/exchange/disable-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-288">For detailed syntax and parameter information, see [Enable-SafeAttachmentRule](/powershell/module/exchange/enable-safeattachmentrule) and [Disable-SafeAttachmentRule](/powershell/module/exchange/disable-safeattachmentrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-attachment-rules"></a><span data-ttu-id="408b7-289">Utiliser PowerShell pour définir la priorité des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-289">Use PowerShell to set the priority of safe attachment rules</span></span>

<span data-ttu-id="408b7-290">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="408b7-290">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="408b7-291">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="408b7-291">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="408b7-292">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="408b7-292">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="408b7-293">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="408b7-293">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="408b7-294">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="408b7-294">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="408b7-295">Pour définir la priorité d’une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-295">To set the priority of a safe attachment rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="408b7-p124">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="408b7-p124">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="408b7-298">**Remarque**: pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-SafeAttachmentRule.**</span><span class="sxs-lookup"><span data-stu-id="408b7-298">**Note**: To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeAttachmentRule** cmdlet instead.</span></span>

<span data-ttu-id="408b7-299">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-299">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-policies"></a><span data-ttu-id="408b7-300">Utiliser PowerShell pour supprimer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-300">Use PowerShell to remove safe attachment policies</span></span>

<span data-ttu-id="408b7-301">Lorsque vous utilisez PowerShell pour supprimer une stratégie de pièces jointes sécurisées, la règle de pièce jointe sécurisée correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="408b7-301">When you use PowerShell to remove a safe attachment policy, the corresponding safe attachment rule isn't removed.</span></span>

<span data-ttu-id="408b7-302">Pour supprimer une stratégie de pièces jointes sécurisées dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-302">To remove a safe attachment policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="408b7-303">Cet exemple supprime la stratégie de pièces jointes sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="408b7-303">This example removes the safe attachment policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "Marketing Department"
```

<span data-ttu-id="408b7-304">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeAttachmentPolicy](/powershell/module/exchange/remove-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="408b7-304">For detailed syntax and parameter information, see [Remove-SafeAttachmentPolicy](/powershell/module/exchange/remove-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-rules"></a><span data-ttu-id="408b7-305">Utiliser PowerShell pour supprimer des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="408b7-305">Use PowerShell to remove safe attachment rules</span></span>

<span data-ttu-id="408b7-306">Lorsque vous utilisez PowerShell pour supprimer une règle de pièce jointe sécurisée, la stratégie de pièces jointes sécurisées correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="408b7-306">When you use PowerShell to remove a safe attachment rule, the corresponding safe attachment policy isn't removed.</span></span>

<span data-ttu-id="408b7-307">Pour supprimer une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="408b7-307">To remove a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "<PolicyName>"
```

<span data-ttu-id="408b7-308">Cet exemple supprime la règle de pièce jointe sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="408b7-308">This example removes the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="408b7-309">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeAttachmentRule](/powershell/module/exchange/remove-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="408b7-309">For detailed syntax and parameter information, see [Remove-SafeAttachmentRule](/powershell/module/exchange/remove-safeattachmentrule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="408b7-310">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="408b7-310">How do you know these procedures worked?</span></span>

<span data-ttu-id="408b7-311">Pour vérifier que vous avez correctement créé, modifié ou supprimé des stratégies de pièces jointes sécurisées, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="408b7-311">To verify that you've successfully created, modified, or removed Safe Attachments policies, do any of the following steps:</span></span>

- <span data-ttu-id="408b7-312">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span><span class="sxs-lookup"><span data-stu-id="408b7-312">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span> <span data-ttu-id="408b7-313">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="408b7-313">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="408b7-314">Pour afficher plus de détails, sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="408b7-314">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="408b7-315">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez \<Name\> les paramètres :</span><span class="sxs-lookup"><span data-stu-id="408b7-315">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeAttachmentPolicy -Identity "<Name>" | Format-List
  ```

  ```PowerShell
  Get-SafeAttachmentRule -Identity "<Name>" | Format-List
  ```

<span data-ttu-id="408b7-316">Pour vérifier que les pièces jointes sécurisées analysent les messages, consultez les rapports Defender pour Office 365 disponibles.</span><span class="sxs-lookup"><span data-stu-id="408b7-316">To verify that Safe Attachments is scanning messages, check the available Defender for Office 365 reports.</span></span> <span data-ttu-id="408b7-317">Pour plus d’informations, voir Afficher les rapports pour Defender pour [Office 365](view-reports-for-atp.md) et Utiliser l’Explorateur dans le Centre de sécurité [& conformité.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="408b7-317">For more information, see [View reports for Defender for Office 365](view-reports-for-atp.md) and [Use Explorer in the Security & Compliance Center](threat-explorer.md).</span></span>