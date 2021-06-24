---
title: Configurer des stratégies Coffre pièces jointes dans Microsoft Defender pour Office 365
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
description: Découvrez comment définir des stratégies Coffre pièces jointes pour protéger votre organisation contre les fichiers malveillants dans le courrier électronique.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: e516a16ff28c762e154fd908312df65ea48699bc
ms.sourcegitcommit: ebb1c3b4d94058a58344317beb9475c8a2eae9a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53108222"
---
# <a name="set-up-safe-attachments-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="94990-103">Configurer des stratégies Coffre pièces jointes dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="94990-103">Set up Safe Attachments policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="94990-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="94990-104">**Applies to**</span></span>
- [<span data-ttu-id="94990-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="94990-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="94990-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="94990-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!IMPORTANT]
> <span data-ttu-id="94990-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](whats-new-in-defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="94990-107">This article is intended for business customers who have [Microsoft Defender for Office 365](whats-new-in-defender-for-office-365.md).</span></span> <span data-ttu-id="94990-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur l’analyse des pièces jointes dans Outlook, voir [Advanced Outlook.com.](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2)</span><span class="sxs-lookup"><span data-stu-id="94990-108">If you're a home user looking for information about attachment scanning in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="94990-109">Coffre Les pièces jointes sont une fonctionnalité de [Microsoft Defender](whats-new-in-defender-for-office-365.md) pour Office 365 qui utilise un environnement virtuel pour vérifier les pièces jointes dans les messages électroniques entrants après qu’elles ont été analysées par la protection anti-programme malveillant dans [Exchange Online Protection (EOP),](anti-malware-protection.md)mais avant leur remise aux destinataires.</span><span class="sxs-lookup"><span data-stu-id="94990-109">Safe Attachments is a feature in [Microsoft Defender for Office 365](whats-new-in-defender-for-office-365.md) that uses a virtual environment to check attachments in inbound email messages after they've been scanned by [anti-malware protection in Exchange Online Protection (EOP)](anti-malware-protection.md), but before delivery to recipients.</span></span> <span data-ttu-id="94990-110">Pour plus d’informations, [Coffre pièces jointes dans Microsoft Defender pour Office 365](safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="94990-110">For more information, see [Safe Attachments in Microsoft Defender for Office 365](safe-attachments.md).</span></span>

<span data-ttu-id="94990-111">Il n’existe aucune stratégie de pièces jointes intégrée ou Coffre par défaut.</span><span class="sxs-lookup"><span data-stu-id="94990-111">There's no built-in or default Safe Attachments policy.</span></span> <span data-ttu-id="94990-112">Pour obtenir Coffre pièces jointes des pièces jointes des messages électroniques, vous devez créer une ou plusieurs stratégies Coffre pièces jointes, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="94990-112">To get Safe Attachments scanning of email message attachments, you need to create one or more Safe Attachments policies as described in this article.</span></span>

<span data-ttu-id="94990-113">Vous pouvez configurer des stratégies de pièces jointes Coffre dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec Defender pour les abonnements de modules Office 365).</span><span class="sxs-lookup"><span data-stu-id="94990-113">You can configure Safe Attachments policies in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="94990-114">Les éléments de base d’une stratégie Coffre pièces jointes sont :</span><span class="sxs-lookup"><span data-stu-id="94990-114">The basic elements of a Safe Attachments policy are:</span></span>

- <span data-ttu-id="94990-115">La stratégie de pièces jointes fiables : spécifie les actions pour les détections de programmes malveillants inconnus, s’il faut envoyer des messages avec des pièces jointes à une adresse e-mail spécifiée et s’il faut remettre des messages si l’analyse des pièces jointes Coffre ne peut pas se terminer.</span><span class="sxs-lookup"><span data-stu-id="94990-115">**The safe attachment policy**: Specifies the actions for unknown malware detections, whether to send messages with malware attachments to a specified email address, and whether to deliver messages if Safe Attachments scanning can't complete.</span></span>
- <span data-ttu-id="94990-116">**La règle de pièce jointe sécurisée**: spécifie la priorité et les filtres de destinataires (à qui la stratégie s’applique).</span><span class="sxs-lookup"><span data-stu-id="94990-116">**The safe attachment rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="94990-117">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez les stratégies Coffre pièces jointes dans le portail Microsoft 365 Defender:</span><span class="sxs-lookup"><span data-stu-id="94990-117">The difference between these two elements isn't obvious when you manage Safe Attachments policies in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="94990-118">Lorsque vous créez une stratégie de pièces jointes Coffre, vous créez en fait une règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="94990-118">When you create a Safe Attachments policy, you're actually creating a safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="94990-119">Lorsque vous modifiez une stratégie Coffre pièces jointes, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle de pièce jointe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="94990-119">When you modify a Safe Attachments policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe attachment rule.</span></span> <span data-ttu-id="94990-120">Tous les autres paramètres modifient la stratégie de pièce jointe sécurisée associée.</span><span class="sxs-lookup"><span data-stu-id="94990-120">All other settings modify the associated safe attachment policy.</span></span>
- <span data-ttu-id="94990-121">Lorsque vous supprimez une stratégie Coffre pièces jointes, la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="94990-121">When you remove a Safe Attachments policy, the safe attachment rule and the associated safe attachment policy are removed.</span></span>

<span data-ttu-id="94990-122">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="94990-122">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="94990-123">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou [EOP PowerShell](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) autonome pour configurer des stratégies Coffre pièces jointes plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="94990-123">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="94990-124">Dans la zone paramètres globaux des paramètres Coffre pièces jointes, vous configurez les fonctionnalités qui ne dépendent pas des stratégies Coffre pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="94990-124">In the global settings area of Safe Attachments settings, you configure features that are not dependent on Safe Attachments policies.</span></span> <span data-ttu-id="94990-125">Pour obtenir des instructions, voir Activer Coffre pièces jointes pour [SharePoint, OneDrive et](turn-on-mdo-for-spo-odb-and-teams.md) Microsoft Teams et Coffre documents dans [Microsoft 365 E5](safe-docs.md).</span><span class="sxs-lookup"><span data-stu-id="94990-125">For instructions see [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-mdo-for-spo-odb-and-teams.md) and [Safe Documents in Microsoft 365 E5](safe-docs.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="94990-126">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="94990-126">What do you need to know before you begin?</span></span>

- <span data-ttu-id="94990-127">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="94990-127">You open the Microsoft 365 Defender portal at <https://security.microsoft.com>.</span></span> <span data-ttu-id="94990-128">Pour aller directement à la page **Coffre pièces jointes,** utilisez <https://security.microsoft.com/safeattachmentv2> .</span><span class="sxs-lookup"><span data-stu-id="94990-128">To go directly to the **Safe Attachments** page, use <https://security.microsoft.com/safeattachmentv2>.</span></span>

- <span data-ttu-id="94990-129">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="94990-129">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="94990-130">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="94990-130">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="94990-131">Vous avez besoin d’autorisations avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="94990-131">You need permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="94990-132">Pour créer, modifier et supprimer des stratégies de pièces jointes  Coffre,  vous devez être membre des  groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité dans le portail Microsoft 365 Defender et membre du groupe de rôles Gestion de l’organisation dans Exchange Online. </span><span class="sxs-lookup"><span data-stu-id="94990-132">To create, modify, and delete Safe Attachments policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Microsoft 365 Defender portal **and** a member of the **Organization Management** role group in Exchange Online.</span></span>
  - <span data-ttu-id="94990-133">Pour accéder en lecture seule aux stratégies Coffre pièces jointes,  vous  devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité dans le portail Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="94990-133">For read-only access to Safe Attachments policies, you need to be a member of the **Global Reader** or **Security Reader** role groups in the Microsoft 365 Defender portal.</span></span>

  <span data-ttu-id="94990-134">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender et](permissions-microsoft-365-security-center.md) [autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="94990-134">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md) and [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="94990-135">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="94990-135">**Notes**:</span></span>

  - <span data-ttu-id="94990-136">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365. </span><span class="sxs-lookup"><span data-stu-id="94990-136">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="94990-137">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="94990-137">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="94990-138">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="94990-138">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="94990-139">Pour obtenir les paramètres recommandés pour les stratégies Coffre pièces jointes, voir Coffre [paramètres de pièces jointes.](recommended-settings-for-eop-and-office365.md#safe-attachments-settings)</span><span class="sxs-lookup"><span data-stu-id="94990-139">For our recommended settings for Safe Attachments policies, see [Safe Attachments settings](recommended-settings-for-eop-and-office365.md#safe-attachments-settings).</span></span>

- <span data-ttu-id="94990-140">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="94990-140">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-safe-attachments-policies"></a><span data-ttu-id="94990-141">Utiliser le portail Microsoft 365 Defender pour créer des stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-141">Use the Microsoft 365 Defender portal to create Safe Attachments policies</span></span>

<span data-ttu-id="94990-142">La création d’une stratégie Coffre pièces jointes personnalisée dans le portail Microsoft 365 Defender crée la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="94990-142">Creating a custom Safe Attachments policy in the Microsoft 365 Defender portal creates the safe attachment rule and the associated safe attachment policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="94990-143">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-143">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-144">Dans la page **Coffre pièces jointes,** cliquez sur ![ Créer une icône ](../../media/m365-cc-sc-create-icon.png) **Créer.**</span><span class="sxs-lookup"><span data-stu-id="94990-144">On the **Safe Attachments** page, click ![Create icon](../../media/m365-cc-sc-create-icon.png) **Create**.</span></span>

3. <span data-ttu-id="94990-145">L’assistant d'application de stratégies s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="94990-145">The policy wizard opens.</span></span> <span data-ttu-id="94990-146">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="94990-146">On the **Name your policy** page, configure the following settings:</span></span>
   - <span data-ttu-id="94990-147">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="94990-147">**Name**: Enter a unique, descriptive name for the policy.</span></span>
   - <span data-ttu-id="94990-148">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="94990-148">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="94990-149">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="94990-149">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="94990-150">Dans la page **Utilisateurs** et domaines qui s’affiche, identifiez les destinataires internes à qui la stratégie s’applique (conditions de destinataire) :</span><span class="sxs-lookup"><span data-stu-id="94990-150">On the **Users and domains** page that appears, identify the internal recipients that the policy applies to (recipient conditions):</span></span>
   - <span data-ttu-id="94990-151">**Utilisateurs** : boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94990-151">**Users**: The specified mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="94990-152">**Groupes** : groupes de distribution, groupes de sécurité à extension messagerie ou groupes Microsoft 365 spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94990-152">**Groups**: The specified distribution groups, mail-enabled security groups, or Microsoft 365 Groups in your organization.</span></span>
   - <span data-ttu-id="94990-153">**Domaines** : tous les destinataires des [domaines acceptés](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="94990-153">**Domains**: All recipients in the specified [accepted domains](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) in your organization.</span></span>

   <span data-ttu-id="94990-154">Cliquez dans la zone appropriée, commencez à taper une valeur et sélectionnez la valeur souhaitée dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="94990-154">Click in the appropriate box, start typing a value, and select the value that you want from the results.</span></span> <span data-ttu-id="94990-155">Répétez cette opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="94990-155">Repeat this process as many times as necessary.</span></span> <span data-ttu-id="94990-156">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="94990-156">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="94990-158">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="94990-158">next to the value.</span></span>

   <span data-ttu-id="94990-159">Pour les utilisateurs ou les groupes, vous pouvez utiliser la plupart des identificateurs (nom, nom d’affichage, alias, adresse e-mail, nom de compte, etc.), mais le nom d'affichage correspondant apparaît dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="94990-159">For users or groups, you can use most identifiers (name, display name, alias, email address, account name, etc.), but the corresponding display name is shown in the results.</span></span> <span data-ttu-id="94990-160">Pour les utilisateurs, entrez un astérisque (\*) seul pour afficher toutes les valeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="94990-160">For users, enter an asterisk (\*) by itself to see all available values.</span></span>

   <span data-ttu-id="94990-161">Plusieurs valeurs dans la même condition utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="94990-161">Multiple values in the same condition use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="94990-162">Des conditions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="94990-162">Different conditions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   - <span data-ttu-id="94990-163">**Exclure ces utilisateurs, groupes et domaines** : pour ajouter des exceptions pour les destinataires internes auxquels la stratégie s’applique (exceptions pour les destinataires), sélectionnez cette option et configurez les exceptions.</span><span class="sxs-lookup"><span data-stu-id="94990-163">**Exclude these users, groups, and domains**: To add exceptions for the internal recipients that the policy applies to (recpient exceptions), select this option and configure the exceptions.</span></span> <span data-ttu-id="94990-164">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="94990-164">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="94990-165">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="94990-165">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="94990-166">Sur la **Paramètres** page, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="94990-166">On the **Settings** page, configure the following settings:</span></span>

   - <span data-ttu-id="94990-167">**Coffre de programmes malveillants inconnus attachments**: sélectionnez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-167">**Safe Attachments unknown malware response**: Select one of the following values:</span></span>
     - <span data-ttu-id="94990-168">**Off**: En règle générale, nous ne recommandons pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="94990-168">**Off**: Typically, we don't recommend this value.</span></span>
     - <span data-ttu-id="94990-169">**Moniteur**</span><span class="sxs-lookup"><span data-stu-id="94990-169">**Monitor**</span></span>
     - <span data-ttu-id="94990-170">**Bloc**: il s’agit de la valeur par défaut et de la valeur recommandée dans les stratégies de sécurité standard [et](preset-security-policies.md)stricte.</span><span class="sxs-lookup"><span data-stu-id="94990-170">**Block**: This is the default value, and the recommended value in Standard and Strict [preset security policies](preset-security-policies.md).</span></span>
     - <span data-ttu-id="94990-171">**Replace**</span><span class="sxs-lookup"><span data-stu-id="94990-171">**Replace**</span></span>
     - <span data-ttu-id="94990-172">**Remise dynamique (fonctionnalité d’aperçu)**</span><span class="sxs-lookup"><span data-stu-id="94990-172">**Dynamic Delivery (Preview Feature)**</span></span>

     <span data-ttu-id="94990-173">Ces valeurs sont expliquées dans les [paramètres Coffre pièces jointes.](safe-attachments.md#safe-attachments-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="94990-173">These values are explained in [Safe Attachments policy settings](safe-attachments.md#safe-attachments-policy-settings).</span></span>

   - <span data-ttu-id="94990-174">Rediriger les messages contenant des pièces **jointes détectées**: si vous sélectionnez Activer la **redirection,** vous pouvez spécifier une adresse de messagerie dans les messages d’envoi qui contiennent des pièces **jointes bloquées, surveillées** ou remplacées dans la zone d’adresse de messagerie spécifiée pour envoyer des messages contenant des pièces jointes contenant des programmes malveillants à des besoins d’analyse et d’examen.</span><span class="sxs-lookup"><span data-stu-id="94990-174">**Redirect messages with detected attachments**: If you select **Enable redirect**, you can specify an email address in the **Send messages that contain blocked, monitored, or replaced attachments to the specified email address** box to send messages that contain malware attachments for analysis and investigation.</span></span>

     <span data-ttu-id="94990-175">La recommandation pour les paramètres de stratégie Standard et Strict consiste à activer la redirection.</span><span class="sxs-lookup"><span data-stu-id="94990-175">The recommendation for Standard and Strict policy settings is to enable redirection.</span></span> <span data-ttu-id="94990-176">Pour plus d’informations, [voir Coffre Paramètres des pièces jointes.](recommended-settings-for-eop-and-office365.md#safe-attachments-settings)</span><span class="sxs-lookup"><span data-stu-id="94990-176">For more information, see [Safe Attachments settings](recommended-settings-for-eop-and-office365.md#safe-attachments-settings).</span></span>

   - <span data-ttu-id="94990-177">Appliquez la réponse de détection des pièces jointes Coffre si l’analyse ne peut pas se terminer (délai ou **erreurs) : l’action** spécifiée par Coffre La réponse anti-programme malveillant inconnue pièces **jointes** est appliquée aux messages même lorsque l’analyse des pièces jointes Coffre ne peut pas se terminer.</span><span class="sxs-lookup"><span data-stu-id="94990-177">**Apply the Safe Attachments detection response if scanning can't complete (timeout or errors)**: The action specified by **Safe Attachments unknown malware response** is taken on messages even when Safe Attachments scanning can't complete.</span></span> <span data-ttu-id="94990-178">Si vous avez sélectionné cette option, sélectionnez toujours Activer la **redirection** et spécifiez une adresse de messagerie pour envoyer des messages contenant des pièces jointes contenant des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="94990-178">If you selected this option, always select **Enable redirect** and specify an email address to send messages that contain malware attachments.</span></span> <span data-ttu-id="94990-179">Dans le cas contraire, les messages peuvent être perdus.</span><span class="sxs-lookup"><span data-stu-id="94990-179">Otherwise, messages might be lost.</span></span>

   <span data-ttu-id="94990-180">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="94990-180">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="94990-181">Dans la page **Révision** qui s’affiche, passez en revue vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="94990-181">On the **Review** page that appears, review your settings.</span></span> <span data-ttu-id="94990-182">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="94990-182">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="94990-183">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="94990-183">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="94990-184">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="94990-184">When you're finished, click **Submit**.</span></span>

7. <span data-ttu-id="94990-185">Dans la page de confirmation qui s’affiche, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="94990-185">On the confirmation page that appears, click **Done**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-safe-attachments-policies"></a><span data-ttu-id="94990-186">Utiliser le portail Microsoft 365 Defender pour afficher les stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-186">Use the Microsoft 365 Defender portal to view Safe Attachments policies</span></span>

1. <span data-ttu-id="94990-187">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-187">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-188">Dans la page **Coffre pièces jointes, les propriétés suivantes** sont affichées dans la liste des stratégies :</span><span class="sxs-lookup"><span data-stu-id="94990-188">On the **Safe Attachments** page, the following properties are displayed in the list of policies:</span></span>
   - <span data-ttu-id="94990-189">**Name**</span><span class="sxs-lookup"><span data-stu-id="94990-189">**Name**</span></span>
   - <span data-ttu-id="94990-190">**État**</span><span class="sxs-lookup"><span data-stu-id="94990-190">**Status**</span></span>
   - <span data-ttu-id="94990-191">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="94990-191">**Priority**</span></span>

3. <span data-ttu-id="94990-192">Lorsque vous sélectionnez une stratégie en cliquant sur le nom, les paramètres de stratégie s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="94990-192">When you select a policy by clicking on the name, the policy settings are displayed in a flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-safe-attachments-policies"></a><span data-ttu-id="94990-193">Utiliser le portail Microsoft 365 Defender pour modifier les stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-193">Use the Microsoft 365 Defender portal to modify Safe Attachments policies</span></span>

1. <span data-ttu-id="94990-194">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-194">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-195">Dans la page **Coffre pièces jointes,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="94990-195">On the **Safe Attachments** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="94990-196">Dans le menu volant des détails de stratégie qui s’affiche, sélectionnez **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="94990-196">In the policy details flyout that appears, select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="94990-197">Pour plus d’informations sur les paramètres, voir la section Utiliser le portail Microsoft 365 Defender pour créer des stratégies Coffre [pièces jointes](#use-the-microsoft-365-defender-portal-to-create-safe-attachments-policies) plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="94990-197">For more information about the settings, see the [Use the Microsoft 365 Defender portal to create Safe Attachments policies](#use-the-microsoft-365-defender-portal-to-create-safe-attachments-policies) section earlier in this article.</span></span>  

<span data-ttu-id="94990-198">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="94990-198">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-attachments-policies"></a><span data-ttu-id="94990-199">Activer ou désactiver les stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-199">Enable or disable Safe Attachments policies</span></span>

1. <span data-ttu-id="94990-200">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-200">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-201">Dans la page **Coffre pièces jointes,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="94990-201">On the **Safe Attachments** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="94990-202">En haut du menu volant des détails de stratégie qui s’affiche, vous verrez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-202">At the top of the policy details flyout that appears, you'll see one of the following values:</span></span>
   - <span data-ttu-id="94990-203">**Stratégie désactivée** : pour activer la stratégie, cliquez sur ![Icône Activer](../../media/m365-cc-sc-turn-on-off-icon.png) **Activer**.</span><span class="sxs-lookup"><span data-stu-id="94990-203">**Policy off**: To turn on the policy, click ![Turn on icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn on** .</span></span>
   - <span data-ttu-id="94990-204">**Stratégie activée** : pour activer la stratégie, cliquez sur ![Icône Désactiver](../../media/m365-cc-sc-turn-on-off-icon.png) **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="94990-204">**Policy on**: To turn off the policy, click ![Turn off icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn off**.</span></span>

4. <span data-ttu-id="94990-205">Dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Activer** ou **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="94990-205">In the confirmation dialog that appears, click **Turn on** or **Turn off**.</span></span>

5. <span data-ttu-id="94990-206">Cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="94990-206">Click **Close** in the policy details flyout.</span></span>

<span data-ttu-id="94990-207">De retour sur la page principale de la stratégie, la valeur **État** de la stratégie sera **Activée** ou **Désactivée**.</span><span class="sxs-lookup"><span data-stu-id="94990-207">Back on the main policy page, the **Status** value of the policy will be **On** or **Off**.</span></span>

### <a name="set-the-priority-of-safe-attachments-policies"></a><span data-ttu-id="94990-208">Définir la priorité des stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-208">Set the priority of Safe Attachments policies</span></span>

<span data-ttu-id="94990-209">Par défaut, Coffre les stratégies de pièces jointes ont une priorité basée sur l’ordre de leur création (les stratégies les plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="94990-209">By default, Safe Attachments policies are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="94990-210">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="94990-210">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="94990-211">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="94990-211">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="94990-212">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="94990-212">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="94990-213">Coffre Les stratégies de pièces jointes sont affichées dans l’ordre de traitement (la première stratégie a la **valeur** priority 0).</span><span class="sxs-lookup"><span data-stu-id="94990-213">Safe Attachments policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

<span data-ttu-id="94990-214">**Remarque**: dans le portail Microsoft 365 Defender, vous pouvez uniquement modifier la priorité de la stratégie Coffre pièces jointes une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="94990-214">**Note**: In the Microsoft 365 Defender portal, you can only change the priority of the Safe Attachments policy after you create it.</span></span> <span data-ttu-id="94990-215">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle de pièce jointe sécurisée (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="94990-215">In PowerShell, you can override the default priority when you create the safe attachment rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="94990-216">Pour modifier la priorité d’une stratégie, cliquez sur **Augmenter la priorité** ou **Diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro **Priorité** dans le Portail Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="94990-216">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Microsoft 365 Defender portal).</span></span> <span data-ttu-id="94990-217">La modification de la priorité d’une stratégie n’a de sens que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="94990-217">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

1. <span data-ttu-id="94990-218">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-218">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-219">Dans la page **Coffre pièces jointes,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="94990-219">On the **Safe Attachments** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="94990-220">En haut du volant des détails de stratégie  qui s’affiche, vous verrez Augmenter la priorité ou Diminuer la priorité en fonction de la valeur de priorité actuelle et du nombre de stratégies : </span><span class="sxs-lookup"><span data-stu-id="94990-220">At the top of the policy details flyout that appears, you'll see **Increase priority** or **Decrease priority** based on the current priority value and the number of policies:</span></span>
   - <span data-ttu-id="94990-221">La stratégie dont la valeur **de** priorité **est 0** ne dispose que de l’option Diminuer **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="94990-221">The policy with the **Priority** value **0** has only the **Decrease priority** option available.</span></span>
   - <span data-ttu-id="94990-222">La stratégie dont la valeur **de** priorité est la plus faible (par exemple, **3**) n’a que l’option Augmenter **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="94990-222">The policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** option available.</span></span>
   - <span data-ttu-id="94990-223">Si vous avez au moins trois stratégies, les stratégies  entre les valeurs de priorité les plus élevées et les plus faibles ont les options Augmenter la priorité et Diminuer **la** priorité disponibles.</span><span class="sxs-lookup"><span data-stu-id="94990-223">If you have three or more policies, the policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** options available.</span></span>

   <span data-ttu-id="94990-224">Cliquez sur l’![Icône Augmenter la priorité](../../media/m365-cc-sc-increase-icon.png) **Augmenter la priorité** ou ![Icône Diminuer la priorité](../../media/m365-cc-sc-decrease-icon.png) **Diminuer la priorité** pour modifier la valeur **Priorité**.</span><span class="sxs-lookup"><span data-stu-id="94990-224">Click ![Increase priority icon](../../media/m365-cc-sc-increase-icon.png) **Increase priority** or ![Decrease priority icon](../../media/m365-cc-sc-decrease-icon.png) **Decrease priority** to change the **Priority** value.</span></span>

4. <span data-ttu-id="94990-225">Lorsque vous avez terminé, cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="94990-225">When you're finished, click **Close** in the policy details flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-safe-attachments-policies"></a><span data-ttu-id="94990-226">Utiliser le portail Microsoft 365 Defender pour supprimer les stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-226">Use the Microsoft 365 Defender portal to remove Safe Attachments policies</span></span>

1. <span data-ttu-id="94990-227">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-227">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span>

2. <span data-ttu-id="94990-228">Dans la page **Coffre pièces jointes,** sélectionnez une stratégie personnalisée dans la liste en cliquant sur le nom de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="94990-228">On the **Safe Attachments** page, select a custom policy from the list by clicking on the name of the policy.</span></span>

3. <span data-ttu-id="94990-229">En haut du menu volant Détails de la stratégie qui s’affiche, cliquez sur l’![Icône Autres actions](../../media/m365-cc-sc-more-actions-icon.png) **Autres actions** \> ![Icône Supprimer la stratégie](../../media/m365-cc-sc-delete-icon.png) **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="94990-229">At the top of the policy details flyout that appears, click ![More actions icon](../../media/m365-cc-sc-more-actions-icon.png) **More actions** \> ![Delete policy icon](../../media/m365-cc-sc-delete-icon.png) **Delete policy**.</span></span>

4. <span data-ttu-id="94990-230">Dans la boîte de dialogue de confirmation qui s'affiche, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="94990-230">In the confirmation dialog that appears, click **Yes**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-attachments-policies"></a><span data-ttu-id="94990-231">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-231">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Attachments policies</span></span>

<span data-ttu-id="94990-232">Comme décrit précédemment, une stratégie Coffre pièces jointes se compose d’une stratégie de pièces jointes sécurisées et d’une règle de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-232">As previously described, a Safe Attachments policy consists of a safe attachment policy and a safe attachment rule.</span></span>

<span data-ttu-id="94990-233">Dans PowerShell, la différence entre les stratégies de pièces jointes sécurisées et les règles de pièces jointes sécurisées est évidente.</span><span class="sxs-lookup"><span data-stu-id="94990-233">In PowerShell, the difference between safe attachment policies and safe attachment rules is apparent.</span></span> <span data-ttu-id="94990-234">Vous gérez les stratégies de pièces jointes sécurisées à l’aide des cmdlets **\* -SafeAttachmentPolicy** et vous gérez les règles de pièces jointes sécurisées à l’aide des cmdlets **\* -SafeAttachmentRule.**</span><span class="sxs-lookup"><span data-stu-id="94990-234">You manage safe attachment policies by using the **\*-SafeAttachmentPolicy** cmdlets, and you manage safe attachment rules by using the **\*-SafeAttachmentRule** cmdlets.</span></span>

- <span data-ttu-id="94990-235">Dans PowerShell, vous créez d’abord la stratégie de pièces jointes sécurisées, puis vous créez la règle de pièce jointe sécurisée qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="94990-235">In PowerShell, you create the safe attachment policy first, then you create the safe attachment rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="94990-236">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de pièces jointes sécurisées et la règle de pièce jointe sécurisée.</span><span class="sxs-lookup"><span data-stu-id="94990-236">In PowerShell, you modify the settings in the safe attachment policy and the safe attachment rule separately.</span></span>
- <span data-ttu-id="94990-237">Lorsque vous supprimez une stratégie de pièces jointes sécurisées de PowerShell, la règle de pièce jointe sécurisée correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="94990-237">When you remove a safe attachment policy from PowerShell, the corresponding safe attachment rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-attachments-policies"></a><span data-ttu-id="94990-238">Utiliser PowerShell pour créer des stratégies Coffre pièces jointes</span><span class="sxs-lookup"><span data-stu-id="94990-238">Use PowerShell to create Safe Attachments policies</span></span>

<span data-ttu-id="94990-239">La création d Coffre de pièces jointes dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="94990-239">Creating a Safe Attachments policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="94990-240">Créez la stratégie de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-240">Create the safe attachment policy.</span></span>
2. <span data-ttu-id="94990-241">Créez la règle de pièce jointe sécurisée qui spécifie la stratégie de pièces jointes sécurisées à l’application de la règle.</span><span class="sxs-lookup"><span data-stu-id="94990-241">Create the safe attachment rule that specifies the safe attachment policy that the rule applies to.</span></span>

 <span data-ttu-id="94990-242">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="94990-242">**Notes**:</span></span>

- <span data-ttu-id="94990-243">Vous pouvez créer une règle de pièce jointe sécurisée et lui attribuer une stratégie de pièces jointes sécurisées existante et non attachée.</span><span class="sxs-lookup"><span data-stu-id="94990-243">You can create a new safe attachment rule and assign an existing, unassociated safe attachment policy to it.</span></span> <span data-ttu-id="94990-244">Une règle de pièce jointe sécurisée ne peut pas être associée à plusieurs stratégies de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-244">A safe attachment rule can't be associated with more than one safe attachment policy.</span></span>

- <span data-ttu-id="94990-245">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de pièces jointes sécurisées dans PowerShell qui ne sont pas disponibles dans le portail Microsoft 365 Defender tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="94990-245">You can configure the following settings on new safe attachment policies in PowerShell that aren't available in the Microsoft 365 Defender portal until after you create the policy:</span></span>
  - <span data-ttu-id="94990-246">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-SafeAttachmentRule).**</span><span class="sxs-lookup"><span data-stu-id="94990-246">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeAttachmentRule** cmdlet).</span></span>
  - <span data-ttu-id="94990-247">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-SafeAttachmentRule).**</span><span class="sxs-lookup"><span data-stu-id="94990-247">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeAttachmentRule** cmdlet).</span></span>

- <span data-ttu-id="94990-248">Une nouvelle stratégie de pièces jointes sécurisées que vous créez dans PowerShell n’est pas visible dans le portail Microsoft 365 Defender tant que vous n’avez pas attribué la stratégie à une règle de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-248">A new safe attachment policy that you create in PowerShell isn't visible in the Microsoft 365 Defender portal until you assign the policy to a safe attachment rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-attachment-policy"></a><span data-ttu-id="94990-249">Étape 1 : Utiliser PowerShell pour créer une stratégie de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-249">Step 1: Use PowerShell to create a safe attachment policy</span></span>

<span data-ttu-id="94990-250">Pour créer une stratégie de pièces jointes sécurisées, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-250">To create a safe attachment policy, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-Action <Allow | Block | Replace | DynamicDelivery>] [-Redirect <$true | $false>] [-RedirectAddress <SMTPEmailAddress>] [-ActionOnError <$true | $false>]
```

<span data-ttu-id="94990-251">Cet exemple crée une stratégie de pièce jointe sécurisée nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-251">This example creates a safe attachment policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="94990-252">Bloquez les messages qui contiennent des programmes malveillants par l’analyse Coffre documents (nous n’utilisons pas le paramètre _Action_ et la valeur par défaut est `Block` ).</span><span class="sxs-lookup"><span data-stu-id="94990-252">Block messages that are found to contain malware by Safe Documents scanning (we aren't using the _Action_ parameter, and the default value is `Block`).</span></span>
- <span data-ttu-id="94990-253">La redirection est activée et les messages qui contiennent des programmes malveillants sont envoyés sec-ops@contoso.com pour analyse et examen.</span><span class="sxs-lookup"><span data-stu-id="94990-253">Redirection is enabled, and messages that are found to contain malware are sent to sec-ops@contoso.com for analysis and investigation.</span></span>
- <span data-ttu-id="94990-254">Si Coffre’analyse des pièces jointes n’est pas disponible ou rencontre des erreurs, ne remettre pas le message (nous n’utilisons pas le paramètre _ActionOnError_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="94990-254">If Safe Attachments scanning isn't available or encounters errors, don't deliver the message (we aren't using the _ActionOnError_ parameter, and the default value is `$true`).</span></span>

```PowerShell
New-SafeAttachmentPolicy -Name "Contoso All" -Redirect $true -RedirectAddress sec-ops@contoso.com
```

<span data-ttu-id="94990-255">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeAttachmentPolicy](/powershell/module/exchange/new-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="94990-255">For detailed syntax and parameter information, see [New-SafeAttachmentPolicy](/powershell/module/exchange/new-safeattachmentpolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-attachment-rule"></a><span data-ttu-id="94990-256">Étape 2 : Utiliser PowerShell pour créer une règle de pièce jointe sécurisée</span><span class="sxs-lookup"><span data-stu-id="94990-256">Step 2: Use PowerShell to create a safe attachment rule</span></span>

<span data-ttu-id="94990-257">Pour créer une règle de pièce jointe sécurisée, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-257">To create a safe attachment rule, use this syntax:</span></span>

```PowerShell
New-SafeAttachmentRule -Name "<RuleName>" -SafeAttachmentPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="94990-258">Cet exemple crée une règle de pièce jointe sécurisée nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-258">This example creates a safe attachment rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="94990-259">La règle est associée à la stratégie de pièces jointes sécurisée nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="94990-259">The rule is associated with the safe attachment policy named Contoso All.</span></span>
- <span data-ttu-id="94990-260">La règle s’applique à tous les destinataires du contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="94990-260">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="94990-261">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="94990-261">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="94990-262">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="94990-262">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeAttachmentRule -Name "Contoso All" -SafeAttachmentPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="94990-263">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeAttachmentRule](/powershell/module/exchange/new-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-263">For detailed syntax and parameter information, see [New-SafeAttachmentRule](/powershell/module/exchange/new-safeattachmentrule).</span></span>

### <a name="use-powershell-to-view-safe-attachment-policies"></a><span data-ttu-id="94990-264">Utiliser PowerShell pour afficher les stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-264">Use PowerShell to view safe attachment policies</span></span>

<span data-ttu-id="94990-265">Pour afficher les stratégies de pièces jointes sécurisées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-265">To view existing safe attachment policies, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="94990-266">Cet exemple renvoie une liste récapitulatif de toutes les stratégies de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-266">This example returns a summary list of all safe attachment policies.</span></span>

```PowerShell
Get-SafeAttachmentPolicy
```

<span data-ttu-id="94990-267">Cet exemple renvoie des informations détaillées sur la stratégie de pièces jointes sécurisée nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="94990-267">This example returns detailed information for the safe attachment policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentPolicy -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="94990-268">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SafeAttachmentPolicy](/powershell/module/exchange/get-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="94990-268">For detailed syntax and parameter information, see [Get-SafeAttachmentPolicy](/powershell/module/exchange/get-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-view-safe-attachment-rules"></a><span data-ttu-id="94990-269">Utiliser PowerShell pour afficher les règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-269">Use PowerShell to view safe attachment rules</span></span>

<span data-ttu-id="94990-270">Pour afficher les règles de pièces jointes sécurisées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-270">To view existing safe attachment rules, use the following syntax:</span></span>

```PowerShell
Get-SafeAttachmentRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled>] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="94990-271">Cet exemple renvoie une liste récapitulatif de toutes les règles de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="94990-271">This example returns a summary list of all safe attachment rules.</span></span>

```PowerShell
Get-SafeAttachmentRule
```

<span data-ttu-id="94990-272">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-272">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeAttachmentRule -State Disabled
```

```PowerShell
Get-SafeAttachmentRule -State Enabled
```

<span data-ttu-id="94990-273">Cet exemple renvoie des informations détaillées sur la règle de pièce jointe sécurisée nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="94990-273">This example returns detailed information for the safe attachment rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeAttachmentRule -Identity "Contoso Executives" | Format-List
```

<span data-ttu-id="94990-274">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-SafeAttachmentRule](/powershell/module/exchange/get-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-274">For detailed syntax and parameter information, see [Get-SafeAttachmentRule](/powershell/module/exchange/get-safeattachmentrule).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-policies"></a><span data-ttu-id="94990-275">Utiliser PowerShell pour modifier des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-275">Use PowerShell to modify safe attachment policies</span></span>

<span data-ttu-id="94990-276">Vous ne pouvez pas renommer une stratégie de pièces jointes sécurisées dans PowerShell (la cmdlet **Set-SafeAttachmentPolicy** n’a pas de _paramètre_ Name).</span><span class="sxs-lookup"><span data-stu-id="94990-276">You can't rename a safe attachment policy in PowerShell (the **Set-SafeAttachmentPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="94990-277">Lorsque vous renommez une stratégie Coffre pièces jointes dans le portail Microsoft 365 Defender, vous renommez uniquement la règle de pièces jointes _sécurisées._</span><span class="sxs-lookup"><span data-stu-id="94990-277">When you rename a Safe Attachments policy in the Microsoft 365 Defender portal, you're only renaming the safe attachment _rule_.</span></span>

<span data-ttu-id="94990-278">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de pièces jointes sécurisées, comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-a-safe-attachment-policy) pour créer une section sur la stratégie de pièces jointes sécurisées plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="94990-278">Otherwise, the same settings are available when you create a safe attachment policy as described in the [Step 1: Use PowerShell to create a safe attachment policy](#step-1-use-powershell-to-create-a-safe-attachment-policy) section earlier in this article.</span></span>

<span data-ttu-id="94990-279">Pour modifier une stratégie de pièces jointes sécurisées, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-279">To modify a safe attachment policy, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="94990-280">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentPolicy](/powershell/module/exchange/set-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="94990-280">For detailed syntax and parameter information, see [Set-SafeAttachmentPolicy](/powershell/module/exchange/set-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-modify-safe-attachment-rules"></a><span data-ttu-id="94990-281">Utiliser PowerShell pour modifier des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-281">Use PowerShell to modify safe attachment rules</span></span>

<span data-ttu-id="94990-282">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de pièce jointe sécurisée dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="94990-282">The only setting that's not available when you modify a safe attachment rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="94990-283">Pour activer ou désactiver des règles de pièces jointes sécurisées existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="94990-283">To enable or disable existing safe attachment rules, see the next section.</span></span>

<span data-ttu-id="94990-284">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-a-safe-attachment-rule) pour créer une section de règle de pièce jointe sécurisée plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="94990-284">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe attachment rule](#step-2-use-powershell-to-create-a-safe-attachment-rule) section earlier in this article.</span></span>

<span data-ttu-id="94990-285">Pour modifier une règle de pièce jointe sécurisée, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-285">To modify a safe attachment rule, use this syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="94990-286">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-286">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-attachment-rules"></a><span data-ttu-id="94990-287">Utiliser PowerShell pour activer ou désactiver des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-287">Use PowerShell to enable or disable safe attachment rules</span></span>

<span data-ttu-id="94990-288">L’activation ou la désactivation d’une règle de pièce jointe sécurisée dans PowerShell active ou désactive l’ensemble de la stratégie de pièces jointes Coffre (la règle de pièces jointes sécurisées et la stratégie de pièces jointes sécurisées affectée).</span><span class="sxs-lookup"><span data-stu-id="94990-288">Enabling or disabling a safe attachment rule in PowerShell enables or disables the whole Safe Attachments policy (the safe attachment rule and the assigned safe attachment policy).</span></span>

<span data-ttu-id="94990-289">Pour activer ou désactiver une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-289">To enable or disable a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeAttachmentRule | Disable-SafeAttachmentRule> -Identity "<RuleName>"
```

<span data-ttu-id="94990-290">Cet exemple désactive la règle de pièce jointe sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="94990-290">This example disables the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="94990-291">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="94990-291">This example enables same rule.</span></span>

```PowerShell
Enable-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="94990-292">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-SafeAttachmentRule](/powershell/module/exchange/enable-safeattachmentrule) et [Disable-SafeAttachmentRule](/powershell/module/exchange/disable-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-292">For detailed syntax and parameter information, see [Enable-SafeAttachmentRule](/powershell/module/exchange/enable-safeattachmentrule) and [Disable-SafeAttachmentRule](/powershell/module/exchange/disable-safeattachmentrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-attachment-rules"></a><span data-ttu-id="94990-293">Utiliser PowerShell pour définir la priorité des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-293">Use PowerShell to set the priority of safe attachment rules</span></span>

<span data-ttu-id="94990-p126">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle. La valeur la plus basse que vous pouvez définir dépend du nombre de règles. Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4. Tout changement de priorité d'une règle existante peut avoir un effet en cascade sur les autres règles. Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="94990-p126">The highest priority value you can set on a rule is 0. The lowest value you can set depends on the number of rules. For example, if you have five rules, you can use the priority values 0 through 4. Changing the priority of an existing rule can have a cascading effect on other rules. For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="94990-299">Pour définir la priorité d’une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-299">To set the priority of a safe attachment rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="94990-p127">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="94990-p127">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeAttachmentRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="94990-302">**Remarque**: pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-SafeAttachmentRule.**</span><span class="sxs-lookup"><span data-stu-id="94990-302">**Note**: To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeAttachmentRule** cmdlet instead.</span></span>

<span data-ttu-id="94990-303">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-303">For detailed syntax and parameter information, see [Set-SafeAttachmentRule](/powershell/module/exchange/set-safeattachmentrule).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-policies"></a><span data-ttu-id="94990-304">Utiliser PowerShell pour supprimer des stratégies de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-304">Use PowerShell to remove safe attachment policies</span></span>

<span data-ttu-id="94990-305">Lorsque vous utilisez PowerShell pour supprimer une stratégie de pièces jointes sécurisées, la règle de pièce jointe sécurisée correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="94990-305">When you use PowerShell to remove a safe attachment policy, the corresponding safe attachment rule isn't removed.</span></span>

<span data-ttu-id="94990-306">Pour supprimer une stratégie de pièces jointes sécurisées dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-306">To remove a safe attachment policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="94990-307">Cet exemple supprime la stratégie de pièces jointes sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="94990-307">This example removes the safe attachment policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentPolicy -Identity "Marketing Department"
```

<span data-ttu-id="94990-308">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeAttachmentPolicy](/powershell/module/exchange/remove-safeattachmentpolicy).</span><span class="sxs-lookup"><span data-stu-id="94990-308">For detailed syntax and parameter information, see [Remove-SafeAttachmentPolicy](/powershell/module/exchange/remove-safeattachmentpolicy).</span></span>

### <a name="use-powershell-to-remove-safe-attachment-rules"></a><span data-ttu-id="94990-309">Utiliser PowerShell pour supprimer des règles de pièces jointes sécurisées</span><span class="sxs-lookup"><span data-stu-id="94990-309">Use PowerShell to remove safe attachment rules</span></span>

<span data-ttu-id="94990-310">Lorsque vous utilisez PowerShell pour supprimer une règle de pièce jointe sécurisée, la stratégie de pièces jointes sécurisées correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="94990-310">When you use PowerShell to remove a safe attachment rule, the corresponding safe attachment policy isn't removed.</span></span>

<span data-ttu-id="94990-311">Pour supprimer une règle de pièce jointe sécurisée dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="94990-311">To remove a safe attachment rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "<PolicyName>"
```

<span data-ttu-id="94990-312">Cet exemple supprime la règle de pièce jointe sécurisée nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="94990-312">This example removes the safe attachment rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeAttachmentRule -Identity "Marketing Department"
```

<span data-ttu-id="94990-313">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeAttachmentRule](/powershell/module/exchange/remove-safeattachmentrule).</span><span class="sxs-lookup"><span data-stu-id="94990-313">For detailed syntax and parameter information, see [Remove-SafeAttachmentRule](/powershell/module/exchange/remove-safeattachmentrule).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="94990-314">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="94990-314">How do you know these procedures worked?</span></span>

<span data-ttu-id="94990-315">Pour vérifier que vous avez correctement créé, modifié ou supprimé des stratégies Coffre pièces jointes, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="94990-315">To verify that you've successfully created, modified, or removed Safe Attachments policies, do any of the following steps:</span></span>

- <span data-ttu-id="94990-316">In the Microsoft 365 Defender portal, go to **Email & Collaboration** Policies & \> **Rules** Threat \> **policies** page \> **Policies** section \> **Coffre Attachments**.</span><span class="sxs-lookup"><span data-stu-id="94990-316">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** page \> **Policies** section \> **Safe Attachments**.</span></span> <span data-ttu-id="94990-317">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="94990-317">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="94990-318">Pour afficher plus de détails, sélectionnez la stratégie dans la liste en cliquant sur le nom, puis affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="94990-318">To view more details, select the policy from the list by clicking on the name, and view the details in the fly out.</span></span>

- <span data-ttu-id="94990-319">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les \<Name\> paramètres :</span><span class="sxs-lookup"><span data-stu-id="94990-319">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeAttachmentPolicy -Identity "<Name>" | Format-List
  ```

  ```PowerShell
  Get-SafeAttachmentRule -Identity "<Name>" | Format-List
  ```

<span data-ttu-id="94990-320">Pour vérifier que la Coffre pièces jointes analyse les messages, recherchez les rapports de Office 365 defender disponibles.</span><span class="sxs-lookup"><span data-stu-id="94990-320">To verify that Safe Attachments is scanning messages, check the available Defender for Office 365 reports.</span></span> <span data-ttu-id="94990-321">Pour plus d’informations, voir [Afficher les rapports pour Defender pour Office 365](view-reports-for-mdo.md) et Utiliser l’Explorateur dans le portail [Microsoft 365 Defender.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="94990-321">For more information, see [View reports for Defender for Office 365](view-reports-for-mdo.md) and [Use Explorer in the Microsoft 365 Defender portal](threat-explorer.md).</span></span>
