---
title: Configurer des stratégies de pièces jointes fiables dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 078eb946-819a-4e13-8673-fe0c0ad3a775
ms.collection:
- M365-security-compliance
description: Découvrez comment définir des stratégies de pièces jointes fiables afin de protéger votre organisation contre les fichiers malveillants par courrier électronique.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 9105e7ed9e9bc376b3d86cd846d8c1d6eae8deea
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49682905"
---
# <a name="set-up-safe-attachments-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="99e50-103">Configurer des stratégies de pièces jointes fiables dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="99e50-103">Set up Safe Attachments policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!IMPORTANT]
> <span data-ttu-id="99e50-104">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-104">This article is intended for business customers who have [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="99e50-105">Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur l’analyse des pièces jointes dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="99e50-105">If you're a home user looking for information about attachment scanning in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="99e50-106">La fonctionnalité pièces jointes fiables est une fonctionnalité de [Microsoft Defender pour Office 365](office-365-atp.md) qui utilise un environnement virtuel pour vérifier les pièces jointes dans les messages électroniques entrants après qu’ils ont été analysés par la protection contre les [programmes malveillants dans Exchange Online Protection (EoP)](anti-malware-protection.md), mais avant remise aux destinataires.</span><span class="sxs-lookup"><span data-stu-id="99e50-106">Safe Attachments is a feature in [Microsoft Defender for Office 365](office-365-atp.md) that uses a virtual environment to check attachments in inbound email messages after they've been scanned by [anti-malware protection in Exchange Online Protection (EOP)](anti-malware-protection.md), but before delivery to recipients.</span></span> <span data-ttu-id="99e50-107">Pour plus d’informations, consultez la rubrique [pièces jointes fiables dans Microsoft Defender pour Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-107">For more information, see [Safe Attachments in Microsoft Defender for Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="99e50-108">Il n’existe pas de stratégie de pièces jointes approuvées ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="99e50-108">There's no built-in or default Safe Attachments policy.</span></span> <span data-ttu-id="99e50-109">Pour obtenir des pièces jointes fiables sur l’analyse des pièces jointes des messages électroniques, vous devez créer une ou plusieurs stratégies de pièces jointes fiables, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="99e50-109">To get Safe Attachments scanning of email message attachments, you need to create one or more Safe Attachments policies as described in this article.</span></span>

<span data-ttu-id="99e50-110">Vous pouvez configurer des stratégies de pièces jointes fiables dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome EOP PowerShell pour les organisations sans boîtes aux lettres Exchange Online, mais avec les abonnements de compléments pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="99e50-110">You can configure Safe Attachments policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="99e50-111">Les éléments de base d’une stratégie de pièces jointes fiables sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="99e50-111">The basic elements of a Safe Attachments policy are:</span></span>

- <span data-ttu-id="99e50-112">**Stratégie de pièces jointes approuvées**: spécifie les actions pour les détections de programmes malveillants inconnues, l’envoi de messages avec des pièces jointes de programmes malveillants à une adresse e-mail spécifique et la remise des messages si l’analyse des pièces jointes fiables ne peut pas aboutir.</span><span class="sxs-lookup"><span data-stu-id="99e50-112">**The safe attachment policy**: Specifies the actions for unknown malware detections, whether to send messages with malware attachments to a specified email address, and whether to deliver messages if Safe Attachments scanning can't complete.</span></span>
- <span data-ttu-id="99e50-113">**La règle de pièce jointe fiable**: spécifie la priorité et les filtres de destinataire (auxquels la stratégie s’applique).</span><span class="sxs-lookup"><span data-stu-id="99e50-113">**The safe attachment rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="99e50-114">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de pièces jointes fiables dans le centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="99e50-114">The difference between these two elements isn't obvious when you manage Safe Attachments polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="99e50-115">Lorsque vous créez une stratégie de pièces jointes approuvées, vous créez en réalité une règle de pièces jointes fiables et la stratégie de pièces jointes fiables associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="99e50-115">When you create a Safe Attachments policy, you're actually creating a safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="99e50-116">Lorsque vous modifiez une stratégie de pièces jointes approuvées, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle de pièce jointe fiable.</span><span class="sxs-lookup"><span data-stu-id="99e50-116">When you modify a Safe Attachments policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe attachment rule.</span></span> <span data-ttu-id="99e50-117">Tous les autres paramètres modifient la stratégie de pièces jointes fiables associée.</span><span class="sxs-lookup"><span data-stu-id="99e50-117">All other settings modify the associated safe attachment policy.</span></span>
- <span data-ttu-id="99e50-118">Lorsque vous supprimez une stratégie de pièces jointes fiables, la règle de pièce jointe fiable et la stratégie de pièces jointes fiables associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="99e50-118">When you remove a Safe Attachments policy, the safe attachment rule and the associated safe attachment policy are removed.</span></span>

<span data-ttu-id="99e50-119">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="99e50-119">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="99e50-120">Pour plus d’informations, reportez-vous à la section [utiliser Exchange Online PowerShell or standalone EOP PowerShell pour configurer les stratégies de pièces jointes approuvées](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="99e50-120">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="99e50-121">Dans la zone Paramètres globaux des pièces jointes approuvées, vous configurez des fonctionnalités qui ne dépendent pas des stratégies de pièces jointes approuvées.</span><span class="sxs-lookup"><span data-stu-id="99e50-121">In the global settings area of Safe Attachments settings, you configure features that are not dependent on Safe Attachments policies.</span></span> <span data-ttu-id="99e50-122">Pour obtenir des instructions, voir Activer la protection avancée contre [les menaces pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md) et [documents approuvés dans Microsoft 365 E5](safe-docs.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-122">For instructions see [Turn on ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md) and [Safe Documents in Microsoft 365 E5](safe-docs.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="99e50-123">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="99e50-123">What do you need to know before you begin?</span></span>

- <span data-ttu-id="99e50-124">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="99e50-124">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="99e50-125">Pour accéder directement à la page **pièces jointes approuvées** , utilisez <https://protection.office.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="99e50-125">To go directly to the **Safe Attachments** page, use <https://protection.office.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="99e50-126">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="99e50-126">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="99e50-127">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="99e50-127">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="99e50-128">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="99e50-128">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="99e50-129">Pour créer, modifier et supprimer des stratégies de pièces jointes approuvées, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="99e50-129">To create, modify, and delete Safe Attachments policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="99e50-130">Pour un accès en lecture seule aux stratégies de pièces jointes approuvées, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="99e50-130">For read-only access to Safe Attachments policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="99e50-131">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-131">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="99e50-132">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="99e50-132">**Notes**:</span></span>

  - <span data-ttu-id="99e50-133">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99e50-133">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="99e50-134">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="99e50-134">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="99e50-135">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="99e50-135">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="99e50-136">Pour connaître les paramètres recommandés pour les stratégies de pièces jointes approuvées, consultez la rubrique [Safe Attachments Settings](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span><span class="sxs-lookup"><span data-stu-id="99e50-136">For our recommended settings for Safe Attachments policies, see [Safe Attachments settings](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span></span>

- <span data-ttu-id="99e50-137">Autoriser jusqu’à 30 minutes pour l’application d’une stratégie nouvelle ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="99e50-137">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

## <a name="use-the-security--compliance-center-to-create-safe-attachments-policies"></a><span data-ttu-id="99e50-138">Utiliser le centre de sécurité & conformité pour créer des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-138">Use the Security & Compliance Center to create Safe Attachments policies</span></span>

<span data-ttu-id="99e50-139">La création d’une stratégie de pièces jointes fiables personnalisée dans le centre de sécurité & conformité crée la règle de pièce jointe fiable et la stratégie de pièces jointes fiables associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="99e50-139">Creating a custom Safe Attachments policy in the Security & Compliance Center creates the safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="99e50-140">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-140">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-141">Dans la page **pièces jointes approuvées** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="99e50-141">On the **Safe Attachments** page, click **Create**.</span></span>

3. <span data-ttu-id="99e50-142">L’Assistant **nouvelle stratégie de pièces jointes fiables** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="99e50-142">The **New Safe Attachments policy** wizard opens.</span></span> <span data-ttu-id="99e50-143">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="99e50-143">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="99e50-144">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="99e50-144">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="99e50-145">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="99e50-145">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="99e50-146">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="99e50-146">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="99e50-147">Sur la page **paramètres** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="99e50-147">On the **Settings** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="99e50-148">**Pièces jointes approuvées réponse aux programmes malveillants inconnus**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e50-148">**Safe Attachments unknown malware response**: Select one of the following values:</span></span>

     - <span data-ttu-id="99e50-149">**Off**: en règle générale, nous ne recommandons pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="99e50-149">**Off**: Typically, we don't recommend this value.</span></span>
     - <span data-ttu-id="99e50-150">**Moniteur**</span><span class="sxs-lookup"><span data-stu-id="99e50-150">**Monitor**</span></span>
     - <span data-ttu-id="99e50-151">**Block**: il s’agit de la valeur par défaut et de la valeur recommandée dans les stratégies de sécurité standard et rigoureuses [prédéfinies](preset-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-151">**Block**: This is the default value, and the recommended value in Standard and Strict [preset security policies](preset-security-policies.md).</span></span>
     - <span data-ttu-id="99e50-152">**Replace**</span><span class="sxs-lookup"><span data-stu-id="99e50-152">**Replace**</span></span>
     - <span data-ttu-id="99e50-153">**Remise dynamique (fonctionnalité aperçu)**</span><span class="sxs-lookup"><span data-stu-id="99e50-153">**Dynamic Delivery (Preview Feature)**</span></span>

     <span data-ttu-id="99e50-154">Ces valeurs sont expliquées dans [paramètres de stratégie de pièces jointes approuvées](atp-safe-attachments.md#safe-attachments-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="99e50-154">These values are explained in [Safe Attachments policy settings](atp-safe-attachments.md#safe-attachments-policy-settings).</span></span>

   - <span data-ttu-id="99e50-155">**Envoyez la pièce jointe à l’adresse de messagerie suivante**: pour les valeurs d’action **bloquer**, **surveiller** ou **remplacer**, vous pouvez sélectionner **activer la redirection** pour envoyer des messages contenant des pièces jointes de programmes malveillants à l’adresse de messagerie interne ou externe spécifiée à des fins d’analyse et d’enquête.</span><span class="sxs-lookup"><span data-stu-id="99e50-155">**Send the attachment to the following email address**: For the action values **Block**, **Monitor**, or **Replace**, you can select **Enable redirect** to send messages that contain malware attachments to the specified internal or external email address for analysis and investigation.</span></span>

     <span data-ttu-id="99e50-156">La recommandation pour les paramètres de stratégie standard et strict est d’activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="99e50-156">The recommendation for Standard and Strict policy settings is to enable redirection.</span></span> <span data-ttu-id="99e50-157">Pour plus d’informations, consultez la rubrique [paramètres de pièces jointes fiables](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span><span class="sxs-lookup"><span data-stu-id="99e50-157">For more information, see [Safe Attachments settings](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-settings).</span></span>

   - <span data-ttu-id="99e50-158">**Appliquer la sélection ci-dessus si l’analyse anti-programme malveillant pour les pièces jointes expire ou si une erreur se produit**: l’action spécifiée par les **pièces jointes approuvées une réponse inconnue aux programmes malveillants** est prise sur les messages, même lorsque l’analyse</span><span class="sxs-lookup"><span data-stu-id="99e50-158">**Apply the above selection if malware scanning for attachments times out or error occurs**: The action specified by **Safe Attachments unknown malware response** is taken on messages even when Safe Attachments scanning can't complete.</span></span> <span data-ttu-id="99e50-159">Sélectionnez toujours cette option si vous sélectionnez **Rediriger activé**.</span><span class="sxs-lookup"><span data-stu-id="99e50-159">Always select this option if you select **Enabled redirect**.</span></span> <span data-ttu-id="99e50-160">Sinon, les messages peuvent être perdus.</span><span class="sxs-lookup"><span data-stu-id="99e50-160">Otherwise, messages might be lost.</span></span>

   <span data-ttu-id="99e50-161">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="99e50-161">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="99e50-162">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="99e50-162">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="99e50-163">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="99e50-163">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="99e50-164">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="99e50-164">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="99e50-165">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="99e50-165">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="99e50-166">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="99e50-166">Click **Add a condition**.</span></span> <span data-ttu-id="99e50-167">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="99e50-167">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="99e50-168">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="99e50-168">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="99e50-169">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="99e50-169">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="99e50-170">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="99e50-170">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="99e50-171">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="99e50-171">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="99e50-172">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="99e50-172">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="99e50-173">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="99e50-173">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="99e50-174">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="99e50-174">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="99e50-175">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="99e50-175">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="99e50-176">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="99e50-176">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="99e50-177">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="99e50-177">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="99e50-178">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="99e50-178">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="99e50-179">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="99e50-179">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="99e50-180">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="99e50-180">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="99e50-181">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="99e50-181">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="99e50-182">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="99e50-182">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="99e50-183">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="99e50-183">When you're finished, click **Finish**.</span></span>

## <a name="use-the-security--compliance-center-to-view-safe-attachments-policies"></a><span data-ttu-id="99e50-184">Utiliser le centre de sécurité & conformité pour afficher les stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-184">Use the Security & Compliance Center to view Safe Attachments policies</span></span>

1. <span data-ttu-id="99e50-185">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-185">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-186">Dans la page **pièces jointes approuvées** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="99e50-186">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

   <span data-ttu-id="99e50-187">Les détails de la stratégie apparaissent dans un survol</span><span class="sxs-lookup"><span data-stu-id="99e50-187">The policy details appear in a fly out</span></span>

## <a name="use-the-security--compliance-center-to-modify-safe-attachments-policies"></a><span data-ttu-id="99e50-188">Utiliser le centre de sécurité & conformité pour modifier les stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-188">Use the Security & Compliance Center to modify Safe Attachments policies</span></span>

1. <span data-ttu-id="99e50-189">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-189">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-190">Dans la page **pièces jointes approuvées** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="99e50-190">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="99e50-191">Dans le volet Détails de la stratégie, cliquez sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="99e50-191">In the policy details fly out that appears, click **Edit policy**.</span></span>

<span data-ttu-id="99e50-192">Les paramètres disponibles dans le survol qui s’affiche sont identiques à ceux décrits dans la section [utiliser le centre de sécurité & conformité pour créer des stratégies de pièces jointes approuvées](#use-the-security--compliance-center-to-create-safe-attachments-policies) .</span><span class="sxs-lookup"><span data-stu-id="99e50-192">The available settings in the fly out that appears are identical to those described in the [Use the Security & Compliance Center to create Safe Attachments policies](#use-the-security--compliance-center-to-create-safe-attachments-policies) section.</span></span>

<span data-ttu-id="99e50-193">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité des stratégies, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="99e50-193">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-attachments-policies"></a><span data-ttu-id="99e50-194">Activer ou désactiver les stratégies de pièces jointes approuvées</span><span class="sxs-lookup"><span data-stu-id="99e50-194">Enable or disable Safe Attachments policies</span></span>

1. <span data-ttu-id="99e50-195">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-195">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-196">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="99e50-196">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="99e50-197">Déplacer le bouton bascule vers la gauche</span><span class="sxs-lookup"><span data-stu-id="99e50-197">Move the toggle to the left</span></span> ![Désactiver la stratégie](../../media/scc-toggle-off.png) <span data-ttu-id="99e50-199">pour désactiver la stratégie.</span><span class="sxs-lookup"><span data-stu-id="99e50-199">to disable the policy.</span></span>

   - <span data-ttu-id="99e50-200">Déplacer le bouton bascule vers la droite</span><span class="sxs-lookup"><span data-stu-id="99e50-200">Move the toggle to the right</span></span> ![Activer la stratégie](../../media/scc-toggle-on.png) <span data-ttu-id="99e50-202">pour activer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="99e50-202">to enable the policy.</span></span>

### <a name="set-the-priority-of-safe-attachments-policies"></a><span data-ttu-id="99e50-203">Définir la priorité des stratégies de pièces jointes approuvées</span><span class="sxs-lookup"><span data-stu-id="99e50-203">Set the priority of Safe Attachments policies</span></span>

<span data-ttu-id="99e50-204">Par défaut, les stratégies de pièces jointes approuvées reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="99e50-204">By default, Safe Attachments policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="99e50-205">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="99e50-205">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="99e50-206">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="99e50-206">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="99e50-207">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-207">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="99e50-208">Les stratégies de pièces jointes approuvées sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="99e50-208">Safe Attachments policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

<span data-ttu-id="99e50-209">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie de pièces jointes fiables une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="99e50-209">**Note**: In the Security & Compliance Center, you can only change the priority of the Safe Attachments policy after you create it.</span></span> <span data-ttu-id="99e50-210">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle de pièce jointe fiable (ce qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="99e50-210">In PowerShell, you can override the default priority when you create the safe attachment rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="99e50-211">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="99e50-211">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="99e50-212">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-212">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-213">Dans la page **pièces jointes approuvées** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="99e50-213">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="99e50-214">Dans le volet Détails de la stratégie, cliquez sur le bouton priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="99e50-214">In the policy details fly out that appears, click the available priority button.</span></span>

   - <span data-ttu-id="99e50-215">La stratégie de pièces jointes approuvées avec la valeur de **priorité** **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="99e50-215">The Safe Attachments policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="99e50-216">La stratégie de pièces jointes approuvées avec la valeur de **priorité** la plus faible (par exemple, **3**) n’a que le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="99e50-216">The Safe Attachments policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="99e50-217">Si vous avez au moins trois stratégies de pièces jointes approuvées, les stratégies entre les valeurs de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="99e50-217">If you have three or more Safe Attachments policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="99e50-218">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="99e50-218">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="99e50-219">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="99e50-219">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-safe-attachments-policies"></a><span data-ttu-id="99e50-220">Utiliser le centre de sécurité & conformité pour supprimer des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-220">Use the Security & Compliance Center to remove Safe Attachments policies</span></span>

1. <span data-ttu-id="99e50-221">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-221">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span>

2. <span data-ttu-id="99e50-222">Dans la page **pièces jointes approuvées** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="99e50-222">On the **Safe Attachments** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="99e50-223">Dans la boîte de dialogue détails de la stratégie, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="99e50-223">In the policy details fly out that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies"></a><span data-ttu-id="99e50-224">Utiliser Exchange Online PowerShell ou l’environnement de ligne de commande Exchange EOP PowerShell autonome pour configurer des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-224">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies</span></span>

<span data-ttu-id="99e50-225">Comme décrit précédemment, une stratégie de pièces jointes fiables est constituée d’une stratégie de pièces jointes fiables et d’une règle de pièce jointe fiable.</span><span class="sxs-lookup"><span data-stu-id="99e50-225">As previously described, a Safe Attachments policy consists of a safe attachment policy and a safe attachment rule.</span></span>

<span data-ttu-id="99e50-226">Dans PowerShell, la différence entre les stratégies de pièces jointes fiables et les règles de pièces jointes fiables est apparente.</span><span class="sxs-lookup"><span data-stu-id="99e50-226">In PowerShell, the difference between safe attachment policies and safe attachment rules is apparent.</span></span> <span data-ttu-id="99e50-227">Vous pouvez gérer les stratégies de pièces jointes fiables à l’aide des cmdlets **\* -safeattachmentpolicy permet** et gérer les règles de pièces jointes fiables à l’aide des cmdlets **\* -safeattachmentrule permet** .</span><span class="sxs-lookup"><span data-stu-id="99e50-227">You manage safe attachment policies by using the **\*-SafeAttachmentPolicy** cmdlets, and you manage safe attachment rules by using the **\*-SafeAttachmentRule** cmdlets.</span></span>

- <span data-ttu-id="99e50-228">Dans PowerShell, vous devez d’abord créer la stratégie de pièces jointes fiables, puis créer la règle de pièce jointe fiable qui identifie la stratégie à laquelle s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="99e50-228">In PowerShell, you create the safe attachment policy first, then you create the safe attachment rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="99e50-229">Dans PowerShell, vous pouvez modifier séparément les paramètres de la stratégie de pièces jointes approuvées et de la règle de pièces jointes approuvées.</span><span class="sxs-lookup"><span data-stu-id="99e50-229">In PowerShell, you modify the settings in the safe attachment policy and the safe attachment rule separately.</span></span>
- <span data-ttu-id="99e50-230">Lorsque vous supprimez une stratégie de pièces jointes fiables à partir de PowerShell, la règle de pièce jointe fiable correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="99e50-230">When you remove a safe attachment policy from PowerShell, the corresponding safe attachment rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-attachments-policies"></a><span data-ttu-id="99e50-231">Utiliser PowerShell pour créer des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-231">Use PowerShell to create Safe Attachments policies</span></span>

<span data-ttu-id="99e50-232">La création d’une stratégie de pièces jointes fiables dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="99e50-232">Creating a Safe Attachments policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="99e50-233">Créez la stratégie de pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="99e50-233">Create the safe attachment policy.</span></span>
2. <span data-ttu-id="99e50-234">Créer la règle de pièce jointe fiable qui spécifie la stratégie de pièces jointes fiables à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="99e50-234">Create the safe attachment rule that specifies the safe attachment policy that the rule applies to.</span></span>

 <span data-ttu-id="99e50-235">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="99e50-235">**Notes**:</span></span>

- <span data-ttu-id="99e50-236">Vous pouvez créer une règle de pièce jointe fiable et lui affecter une stratégie de pièces jointes fiables existante non associée.</span><span class="sxs-lookup"><span data-stu-id="99e50-236">You can create a new safe attachment rule and assign an existing, unassociated safe attachment policy to it.</span></span> <span data-ttu-id="99e50-237">Une règle de pièce jointe fiable ne peut pas être associée à plusieurs stratégies de pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="99e50-237">A safe attachment rule can't be associated with more than one safe attachment policy.</span></span>

- <span data-ttu-id="99e50-238">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de pièces jointes fiables dans PowerShell qui ne sont pas disponibles dans le centre de sécurité & jusqu’à ce que vous ayez créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="99e50-238">You can configure the following settings on new safe attachment policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>
  - <span data-ttu-id="99e50-239">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-safeattachmentrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="99e50-239">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeAttachmentRule** cmdlet).</span></span>
  - <span data-ttu-id="99e50-240">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-safeattachmentrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="99e50-240">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeAttachmentRule** cmdlet).</span></span>

- <span data-ttu-id="99e50-241">Une nouvelle stratégie de pièces jointes approuvées que vous créez dans PowerShell n’est pas visible dans le centre de sécurité &, tant que vous n’avez pas affecté la stratégie à une règle de pièce jointe fiable.</span><span class="sxs-lookup"><span data-stu-id="99e50-241">A new safe attachment policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a safe attachment rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-attachment-policy"></a><span data-ttu-id="99e50-242">Étape 1 : utiliser PowerShell pour créer une stratégie de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-242">Step 1: Use PowerShell to create a safe attachment policy</span></span>

<span data-ttu-id="99e50-243">Pour créer une stratégie de pièces jointes fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-243">To create a safe attachment policy, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-Action <Allow | Block | Replace | DynamicDelivery>] [-Redirect <$true | $false>] [-RedirectAddress <SMTPEmailAddress>] [-ActionOnError <$true | $false>]
```

<span data-ttu-id="99e50-244">Cet exemple crée une stratégie de pièces jointes approuvées nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e50-244">This example creates a safe attachment policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="99e50-245">Bloquer les messages qui contiennent des programmes malveillants par analyse des documents approuvés (nous n’utilisons pas le paramètre _action_ , et la valeur par défaut est `Block` ).</span><span class="sxs-lookup"><span data-stu-id="99e50-245">Block messages that are found to contain malware by Safe Documents scanning (we aren't using the _Action_ parameter, and the default value is `Block`).</span></span>
- <span data-ttu-id="99e50-246">La redirection est activée et les messages qui contiennent des programmes malveillants sont envoyés à sec-ops@contoso.com à des fins d’analyse et d’enquête.</span><span class="sxs-lookup"><span data-stu-id="99e50-246">Redirection is enabled, and messages that are found to contain malware are sent to sec-ops@contoso.com for analysis and investigation.</span></span>
- <span data-ttu-id="99e50-247">Si l’analyse des pièces jointes fiables n’est pas disponible ou rencontre des erreurs, ne fournissez pas le message (nous n’utilisons pas le paramètre _ActionOnError_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="99e50-247">If Safe Attachments scanning isn't available or encounters errors, don't deliver the message (we aren't using the _ActionOnError_ parameter, and the default value is `$true`).</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "Contoso All" -Redirect $true -RedirectAddress sec-ops@contoso.com
```

<span data-ttu-id="99e50-248">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-safeattachmentpolicy permet](https://docs.microsoft.com/powershell/module/exchange/new-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="99e50-248">For detailed syntax and parameter information, see [New-SafeAttachmentPolicy](https://docs.microsoft.com/powershell/module/exchange/new-safeattachmentpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-attachment-rule"></a><span data-ttu-id="99e50-249">Étape 2 : utiliser PowerShell pour créer une règle de pièce jointe fiable</span><span class="sxs-lookup"><span data-stu-id="99e50-249">Step 2: Use PowerShell to create a safe attachment rule</span></span>

<span data-ttu-id="99e50-250">Pour créer une règle de pièce jointe fiable, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-250">To create a safe attachment rule, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentRule -Name "<RuleName>" -SafeAttachmentPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="99e50-251">Cet exemple crée une règle de pièce jointe fiable nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e50-251">This example creates a safe attachment rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="99e50-252">La règle est associée à la stratégie de pièces jointes approuvées nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="99e50-252">The rule is associated with the safe attachment policy named Contoso All.</span></span>
- <span data-ttu-id="99e50-253">La règle s’applique à tous les destinataires dans le domaine contoso.com.</span><span class="sxs-lookup"><span data-stu-id="99e50-253">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="99e50-254">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="99e50-254">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="99e50-255">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="99e50-255">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeAttachmentRule -Name "Contoso All" -SafeAttachmentPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="99e50-256">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/new-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-256">For detailed syntax and parameter information, see [New-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/new-safeattachmentrule).</span></span>

### <a name="use-powershell-to-view-safe-attachment-policies"></a><span data-ttu-id="99e50-257">Utiliser PowerShell pour afficher les stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-257">Use PowerShell to view safe attachment policies</span></span>

<span data-ttu-id="99e50-258">Pour afficher les stratégies de pièces jointes approuvées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-258">To view existing safe attachment policies, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="99e50-259">Cet exemple renvoie la liste récapitulative de toutes les stratégies de pièces jointes approuvées.</span><span class="sxs-lookup"><span data-stu-id="99e50-259">This example returns a summary list of all safe attachment policies.</span></span>

```PowerShell
Get-SafeAttachmentPolicy
```

<span data-ttu-id="99e50-260">Cet exemple renvoie des informations détaillées sur la stratégie de pièces jointes approuvées nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="99e50-260">This example returns detailed information for the safe attachment policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentPolicy -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="99e50-261">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-safeattachmentpolicy permet](https://docs.microsoft.com/powershell/module/exchange/get-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="99e50-261">For detailed syntax and parameter information, see [Get-SafeAttachmentPolicy](https://docs.microsoft.com/powershell/module/exchange/get-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-view-safe-attachment-rules"></a><span data-ttu-id="99e50-262">Utiliser PowerShell pour afficher les règles de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-262">Use PowerShell to view safe attachment rules</span></span>

<span data-ttu-id="99e50-263">Pour afficher les règles de pièces jointes approuvées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-263">To view existing safe attachment rules, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled>] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="99e50-264">Cet exemple renvoie la liste récapitulative de toutes les règles de pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="99e50-264">This example returns a summary list of all safe attachment rules.</span></span>

```PowerShell
Get-SafeAttachmentRule
```

<span data-ttu-id="99e50-265">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e50-265">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeAttachmentRule -State Disabled
```

```PowerShell
Get-SafeAttachmentRule -State Enabled
```

<span data-ttu-id="99e50-266">Cet exemple renvoie des informations détaillées sur la règle de pièces jointes approuvées nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="99e50-266">This example returns detailed information for the safe attachment rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="99e50-267">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/get-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-267">For detailed syntax and parameter information, see [Get-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/get-safeattachmentrule).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-policies"></a><span data-ttu-id="99e50-268">Utiliser PowerShell pour modifier des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-268">Use PowerShell to modify safe attachment policies</span></span>

<span data-ttu-id="99e50-269">Vous ne pouvez pas renommer une stratégie de pièces jointes fiables dans PowerShell (l’applet de commande **Set-safeattachmentpolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="99e50-269">You can't rename a safe attachment policy in PowerShell (the **Set-SafeAttachmentPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="99e50-270">Lorsque vous renommez une stratégie de pièces jointes fiables dans le centre de sécurité & conformité, vous renommez uniquement la _règle_ de pièce jointe fiable.</span><span class="sxs-lookup"><span data-stu-id="99e50-270">When you rename a Safe Attachments policy in the Security & Compliance Center, you're only renaming the safe attachment _rule_.</span></span>

<span data-ttu-id="99e50-271">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de pièces jointes fiables, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie de pièces jointes fiables](#step-1-use-powershell-to-create-a-safe-attachment-policy) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="99e50-271">Otherwise, the same settings are available when you create a safe attachment policy as described in the [Step 1: Use PowerShell to create a safe attachment policy](#step-1-use-powershell-to-create-a-safe-attachment-policy) section earlier in this article.</span></span>

<span data-ttu-id="99e50-272">Pour modifier une stratégie de pièces jointes fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-272">To modify a safe attachment policy, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="99e50-273">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safeattachmentpolicy permet](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="99e50-273">For detailed syntax and parameter information, see [Set-SafeAttachmentPolicy](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-rules"></a><span data-ttu-id="99e50-274">Utiliser PowerShell pour modifier les règles de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-274">Use PowerShell to modify safe attachment rules</span></span>

<span data-ttu-id="99e50-275">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de pièce jointe fiable dans PowerShell est le paramètre _activé_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="99e50-275">The only setting that's not available when you modify a safe attachment rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="99e50-276">Pour activer ou désactiver les règles de pièces jointes approuvées existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="99e50-276">To enable or disable existing safe attachment rules, see the next section.</span></span>

<span data-ttu-id="99e50-277">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle de pièce jointe fiable](#step-2-use-powershell-to-create-a-safe-attachment-rule) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="99e50-277">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe attachment rule](#step-2-use-powershell-to-create-a-safe-attachment-rule) section earlier in this article.</span></span>

<span data-ttu-id="99e50-278">Pour modifier une règle de pièce jointe fiable, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-278">To modify a safe attachment rule, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="99e50-279">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-279">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-attachment-rules"></a><span data-ttu-id="99e50-280">Utiliser PowerShell pour activer ou désactiver les règles de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-280">Use PowerShell to enable or disable safe attachment rules</span></span>

<span data-ttu-id="99e50-281">L’activation ou la désactivation d’une règle de pièce jointe fiable dans PowerShell active ou désactive la stratégie de pièces jointes approuvées (la règle de pièces jointes fiables et la stratégie de pièces jointes approuvées).</span><span class="sxs-lookup"><span data-stu-id="99e50-281">Enabling or disabling a safe attachment rule in PowerShell enables or disables the whole Safe Attachments policy (the safe attachment rule and the assigned safe attachment policy).</span></span>

<span data-ttu-id="99e50-282">Pour activer ou désactiver une règle de pièce jointe fiable dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-282">To enable or disable a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeAttachmentRule | Disable-SafeAttachmentRule> -Identity "<RuleName>"
```

<span data-ttu-id="99e50-283">Cet exemple désactive la règle de pièces jointes approuvées nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="99e50-283">This example disables the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="99e50-284">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="99e50-284">This example enables same rule.</span></span>

```PowerShell
Enable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="99e50-285">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/enable-safeattachmentrule) et [Disable-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/disable-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-285">For detailed syntax and parameter information, see [Enable-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/enable-safeattachmentrule) and [Disable-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/disable-safeattachmentrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-attachment-rules"></a><span data-ttu-id="99e50-286">Utiliser PowerShell pour définir la priorité des règles de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-286">Use PowerShell to set the priority of safe attachment rules</span></span>

<span data-ttu-id="99e50-287">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="99e50-287">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="99e50-288">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="99e50-288">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="99e50-289">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="99e50-289">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="99e50-290">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="99e50-290">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="99e50-291">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="99e50-291">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="99e50-292">Pour définir la priorité d’une règle de pièce jointe fiable dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-292">To set the priority of a safe attachment rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="99e50-p124">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="99e50-p124">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="99e50-295">**Remarque**: pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-safeattachmentrule permet** .</span><span class="sxs-lookup"><span data-stu-id="99e50-295">**Note**: To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeAttachmentRule** cmdlet instead.</span></span>

<span data-ttu-id="99e50-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-296">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-policies"></a><span data-ttu-id="99e50-297">Utiliser PowerShell pour supprimer des stratégies de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-297">Use PowerShell to remove safe attachment policies</span></span>

<span data-ttu-id="99e50-298">Lorsque vous utilisez PowerShell pour supprimer une stratégie de pièces jointes fiables, la règle de pièce jointe fiable correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="99e50-298">When you use PowerShell to remove a safe attachment policy, the corresponding safe attachment rule isn't removed.</span></span>

<span data-ttu-id="99e50-299">Pour supprimer une stratégie de pièces jointes fiables dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-299">To remove a safe attachment policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="99e50-300">Cet exemple supprime la stratégie de pièces jointes approuvées nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="99e50-300">This example removes the safe attachment policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "Marketing Department"
```

<span data-ttu-id="99e50-301">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-safeattachmentpolicy permet](https://docs.microsoft.com/powershell/module/exchange/remove-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="99e50-301">For detailed syntax and parameter information, see [Remove-SafeAttachmentPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-rules"></a><span data-ttu-id="99e50-302">Utiliser PowerShell pour supprimer des règles de pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="99e50-302">Use PowerShell to remove safe attachment rules</span></span>

<span data-ttu-id="99e50-303">Lorsque vous utilisez PowerShell pour supprimer une règle de pièce jointe fiable, la stratégie de pièces jointes fiables correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="99e50-303">When you use PowerShell to remove a safe attachment rule, the corresponding safe attachment policy isn't removed.</span></span>

<span data-ttu-id="99e50-304">Pour supprimer une règle de pièce jointe fiable dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99e50-304">To remove a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "<PolicyName>"
```

<span data-ttu-id="99e50-305">Cet exemple supprime la règle de pièce jointe fiable nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="99e50-305">This example removes the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="99e50-306">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-safeattachmentrule permet](https://docs.microsoft.com/powershell/module/exchange/remove-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="99e50-306">For detailed syntax and parameter information, see [Remove-SafeAttachmentRule](https://docs.microsoft.com/powershell/module/exchange/remove-safeattachmentrule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="99e50-307">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="99e50-307">How do you know these procedures worked?</span></span>

<span data-ttu-id="99e50-308">Pour vérifier que vous avez bien créé, modifié ou supprimé des stratégies de pièces jointes fiables, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="99e50-308">To verify that you've successfully created, modified, or removed Safe Attachments policies, do any of the following steps:</span></span>

- <span data-ttu-id="99e50-309">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **pièces jointes ATP**.</span><span class="sxs-lookup"><span data-stu-id="99e50-309">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Attachments**.</span></span> <span data-ttu-id="99e50-310">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="99e50-310">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="99e50-311">Pour afficher plus de détails, sélectionnez la stratégie dans la liste, puis affichez les détails dans le survol.</span><span class="sxs-lookup"><span data-stu-id="99e50-311">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="99e50-312">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez \<Name\> par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="99e50-312">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeAttachmentPolicy -Identity "<Name>" | Format-List
  ```

  ```PowerShell
  Get-SafeAttachmentRule -Identity "<Name>" | Format-List
  ```

<span data-ttu-id="99e50-313">Pour vérifier que les pièces jointes fiables analysent les messages, consultez les rapports de Defender pour Office 365 disponibles.</span><span class="sxs-lookup"><span data-stu-id="99e50-313">To verify that Safe Attachments is scanning messages, check the available Defender for Office 365 reports.</span></span> <span data-ttu-id="99e50-314">Pour plus d’informations, consultez la rubrique [afficher les rapports pour Defender pour Office 365](view-reports-for-atp.md) et [utiliser l’Explorateur dans le centre de sécurité & conformité](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="99e50-314">For more information, see [View reports for Defender for Office 365](view-reports-for-atp.md) and [Use Explorer in the Security & Compliance Center](threat-explorer.md).</span></span>
