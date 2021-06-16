---
title: Configurer des stratégies de liens sécurisés dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: how-to
ms.date: ''
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir comment afficher, créer, modifier et supprimer des stratégies de liens sécurisés et des paramètres globaux de liens sécurisés dans Microsoft Defender pour Office 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: fb157792f0f9e80e4a974b59aebaa2e1991c5d0b
ms.sourcegitcommit: ac3e9ccb7b43a42e600af8f44e6f30019533faeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "52933118"
---
# <a name="set-up-safe-links-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="6f670-103">Configurer des stratégies de liens sécurisés dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6f670-103">Set up Safe Links policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="6f670-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6f670-104">**Applies to**</span></span>
- [<span data-ttu-id="6f670-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="6f670-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="6f670-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f670-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!IMPORTANT]
> <span data-ttu-id="6f670-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="6f670-107">This article is intended for business customers who have [Microsoft Defender for Office 365](defender-for-office-365.md).</span></span> <span data-ttu-id="6f670-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur les liens sécurisés dans Outlook, voir [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="6f670-108">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="6f670-109">La technologie Liens sécurisés dans [Microsoft Defender pour Office 365](defender-for-office-365.md) permet d’analyser les URL des messages électroniques entrants dans le flux de messagerie, ainsi que l’heure de vérification des URL et des liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="6f670-109">Safe Links in [Microsoft Defender for Office 365](defender-for-office-365.md) provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="6f670-110">Pour plus d’informations, [voir Liens sécurisés dans Microsoft Defender pour Office 365](safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="6f670-110">For more information, see [Safe Links in Microsoft Defender for Office 365](safe-links.md).</span></span>

<span data-ttu-id="6f670-111">Il n’existe aucune stratégie de liens sécurisés intégrée ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="6f670-111">There's no built-in or default Safe Links policy.</span></span> <span data-ttu-id="6f670-112">Pour obtenir l’analyse des URL par des liens sécurisés, vous devez créer une ou plusieurs stratégies de liens sécurisés, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-112">To get Safe Links scanning of URLs, you need to create one or more Safe Links policies as described in this article.</span></span>

> [!NOTE]
>
> <span data-ttu-id="6f670-113">Vous configurez les paramètres globaux pour la **protection** des liens sécurisés en dehors des stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-113">You configure the global settings for Safe Links protection **outside** of Safe Links policies.</span></span> <span data-ttu-id="6f670-114">Pour obtenir des instructions, voir [Configurer les paramètres globaux](configure-global-settings-for-safe-links.md)des liens sécurisés dans Microsoft Defender pour Office 365 .</span><span class="sxs-lookup"><span data-stu-id="6f670-114">For instructions, see [Configure global settings for Safe Links in Microsoft Defender for Office 365](configure-global-settings-for-safe-links.md).</span></span>
>
> <span data-ttu-id="6f670-115">Les administrateurs doivent prendre en compte les différents paramètres de configuration pour les liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-115">Admins should consider the different configuration settings for Safe Links.</span></span> <span data-ttu-id="6f670-116">L’une des options disponibles consiste à inclure des informations d’identification utilisateur dans les liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-116">One of the available options is to include user identifiable information in Safe Links.</span></span> <span data-ttu-id="6f670-117">Cette fonctionnalité permet aux équipes *d’opérations* de sécurité d’examiner la compromission potentielle de l’utilisateur, de prendre des mesures correctives et de limiter les violations coûteuses.</span><span class="sxs-lookup"><span data-stu-id="6f670-117">This feature enables *Security Ops teams* to investigate potential user compromise, take corrective action, and limit costly breaches.</span></span>

<span data-ttu-id="6f670-118">Vous pouvez configurer des stratégies de liens sécurisés dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec Microsoft Defender pour les abonnements de modules supplémentaires Office 365).</span><span class="sxs-lookup"><span data-stu-id="6f670-118">You can configure Safe Links policies in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Microsoft Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="6f670-119">Les éléments de base d’une stratégie de liens sécurisés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6f670-119">The basic elements of a Safe Links policy are:</span></span>

- <span data-ttu-id="6f670-120">La stratégie de liens sécurisés : activer la protection contre les liens sécurisés, activer l’analyse des URL en temps réel, spécifier s’il faut attendre la fin de l’analyse en temps réel avant de remettre le message, activer l’analyse des messages internes, spécifier s’il faut suivre les clics des utilisateurs sur les URL et spécifier s’il faut autoriser les utilisateurs à cliquer sur l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="6f670-120">**The safe links policy**: Turn on Safe Links protection, turn on real-time URL scanning, specify whether to wait for real-time scanning to complete before delivering the message, turn on scanning for internal messages, specify whether to track user clicks on URLs, and specify whether to allow users to click trough to the original URL.</span></span>
- <span data-ttu-id="6f670-121">**La règle de liens sécurisés**: spécifie la priorité et les filtres de destinataires (à qui s’applique la stratégie).</span><span class="sxs-lookup"><span data-stu-id="6f670-121">**The safe links rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="6f670-122">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des polices de liens sécurisés dans le portail Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="6f670-122">The difference between these two elements isn't obvious when you manage Safe Links polices in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="6f670-123">Lorsque vous créez une stratégie de liens sécurisés, vous créez en même temps une règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="6f670-123">When you create a Safe Links policy, you're actually creating a safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="6f670-124">Lorsque vous modifiez une stratégie de liens sécurisés, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-124">When you modify a Safe Links policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe links rule.</span></span> <span data-ttu-id="6f670-125">Tous les autres paramètres modifient la stratégie de liens sécurisés associée.</span><span class="sxs-lookup"><span data-stu-id="6f670-125">All other settings modify the associated safe links policy.</span></span>
- <span data-ttu-id="6f670-126">Lorsque vous supprimez une stratégie de liens sécurisés, la règle de liens sécurisés et la stratégie de liens sécurisés associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="6f670-126">When you remove a Safe Links policy, the safe links rule and the associated safe links policy are removed.</span></span>

<span data-ttu-id="6f670-127">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="6f670-127">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="6f670-128">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou [EOP PowerShell](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) autonome pour configurer des stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-128">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) section later in this article.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6f670-129">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6f670-129">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6f670-130">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="6f670-130">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="6f670-131">Pour aller directement à la page **Liens sécurisés,** utilisez <https://security.microsoft.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="6f670-131">To go directly to the **Safe Links** page, use <https://security.microsoft.com/safelinksv2>.</span></span>

- <span data-ttu-id="6f670-132">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="6f670-132">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="6f670-133">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="6f670-133">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="6f670-134">Des autorisations doivent vous être attribuées avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="6f670-134">You need to be assigned permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="6f670-135">Pour créer, modifier et supprimer des stratégies de liens  sécurisés, vous devez être membre des  groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité dans le portail Microsoft 365 Defender et membre du groupe de rôles Gestion de l’organisation dans Exchange Online.  </span><span class="sxs-lookup"><span data-stu-id="6f670-135">To create, modify, and delete Safe Links policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Microsoft 365 Defender portal **and** a member of the **Organization Management** role group in Exchange Online.</span></span>
  - <span data-ttu-id="6f670-136">Pour accéder en lecture seule aux stratégies de liens  sécurisés, vous devez être membre des groupes de rôles Lecteur global ou Lecteur **de** sécurité.</span><span class="sxs-lookup"><span data-stu-id="6f670-136">For read-only access to Safe Links policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="6f670-137">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender](permissions-in-the-security-and-compliance-center.md) et [autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="6f670-137">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md) and [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  >
  > - <span data-ttu-id="6f670-138">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne  aux utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6f670-138">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="6f670-139">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6f670-139">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  <span data-ttu-id="6f670-140">.</span><span class="sxs-lookup"><span data-stu-id="6f670-140">.</span></span> <span data-ttu-id="6f670-141">- Le **groupe de rôles** Gestion de l’organisation en affichage seul dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6f670-141">- The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="6f670-142">Pour obtenir nos paramètres recommandés pour les stratégies de liens sécurisés, consultez les [paramètres de stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="6f670-142">For our recommended settings for Safe Links policies, see [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).</span></span>

- <span data-ttu-id="6f670-143">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="6f670-143">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="6f670-144">[De nouvelles fonctionnalités sont continuellement ajoutées à Microsoft Defender pour Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="6f670-144">[New features are continually being added to Microsoft Defender for Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="6f670-145">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements à vos stratégies de liens sécurisés existantes.</span><span class="sxs-lookup"><span data-stu-id="6f670-145">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-safe-links-policies"></a><span data-ttu-id="6f670-146">Utiliser le portail Microsoft 365 Defender pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-146">Use the Microsoft 365 Defender portal to create Safe Links policies</span></span>

<span data-ttu-id="6f670-147">La création d’une stratégie de liens sécurisés personnalisée dans le portail Microsoft 365 Defender crée la règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="6f670-147">Creating a custom Safe Links policy in the Microsoft 365 Defender portal creates the safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="6f670-148">Dans le portail Microsoft 365 Defender, go to **Policies & rules** Threat \> **Policies** section \>  Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-148">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-149">Dans la page **Liens sécurisés,** cliquez sur ![ Créer une icône ](../../media/m365-cc-sc-create-icon.png) **Créer.**</span><span class="sxs-lookup"><span data-stu-id="6f670-149">On the **Safe Links** page, click ![Create icon](../../media/m365-cc-sc-create-icon.png) **Create**.</span></span>

3. <span data-ttu-id="6f670-150">**L’Assistant Nouvelle stratégie de liens sécurisés** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="6f670-150">The **New Safe Links policy** wizard opens.</span></span> <span data-ttu-id="6f670-151">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f670-151">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="6f670-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6f670-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>
   - <span data-ttu-id="6f670-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6f670-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="6f670-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f670-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="6f670-155">Dans la page **Utilisateurs** et domaines qui s’affiche, identifiez les destinataires internes à qui la stratégie s’applique (conditions de destinataire) :</span><span class="sxs-lookup"><span data-stu-id="6f670-155">On the **Users and domains** page that appears, identify the internal recipients that the policy applies to (recipient conditions):</span></span>
   - <span data-ttu-id="6f670-156">**Utilisateurs** : boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6f670-156">**Users**: The specified mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="6f670-157">**Groupes** : groupes de distribution, groupes de sécurité à extension messagerie ou groupes Microsoft 365 spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6f670-157">**Groups**: The specified distribution groups, mail-enabled security groups, or Microsoft 365 Groups in your organization.</span></span>
   - <span data-ttu-id="6f670-158">**Domaines** : tous les destinataires des [domaines acceptés](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) spécifiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6f670-158">**Domains**: All recipients in the specified [accepted domains](/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) in your organization.</span></span>

   <span data-ttu-id="6f670-159">Cliquez dans la zone appropriée, commencez à taper une valeur et sélectionnez la valeur souhaitée dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="6f670-159">Click in the appropriate box, start typing a value, and select the value that you want from the results.</span></span> <span data-ttu-id="6f670-160">Répétez cette opération autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6f670-160">Repeat this process as many times as necessary.</span></span> <span data-ttu-id="6f670-161">Pour supprimer une valeur existante, cliquez sur Supprimer</span><span class="sxs-lookup"><span data-stu-id="6f670-161">To remove an existing value, click remove</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="6f670-163">en regard de la valeur.</span><span class="sxs-lookup"><span data-stu-id="6f670-163">next to the value.</span></span>

   <span data-ttu-id="6f670-164">Pour les utilisateurs ou les groupes, vous pouvez utiliser la plupart des identificateurs (nom, nom d’affichage, alias, adresse e-mail, nom de compte, etc.), mais le nom d'affichage correspondant apparaît dans les résultats.</span><span class="sxs-lookup"><span data-stu-id="6f670-164">For users or groups, you can use most identifiers (name, display name, alias, email address, account name, etc.), but the corresponding display name is shown in the results.</span></span> <span data-ttu-id="6f670-165">Pour les utilisateurs, entrez un astérisque (\*) seul pour afficher toutes les valeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="6f670-165">For users, enter an asterisk (\*) by itself to see all available values.</span></span>

   <span data-ttu-id="6f670-166">Plusieurs valeurs dans la même condition utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="6f670-166">Multiple values in the same condition use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="6f670-167">Des conditions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="6f670-167">Different conditions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   - <span data-ttu-id="6f670-168">**Exclure ces utilisateurs, groupes et domaines** : pour ajouter des exceptions pour les destinataires internes auxquels la stratégie s’applique (exceptions pour les destinataires), sélectionnez cette option et configurez les exceptions.</span><span class="sxs-lookup"><span data-stu-id="6f670-168">**Exclude these users, groups, and domains**: To add exceptions for the internal recipients that the policy applies to (recpient exceptions), select this option and configure the exceptions.</span></span> <span data-ttu-id="6f670-169">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="6f670-169">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="6f670-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f670-170">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="6f670-171">Dans la page **Paramètres de protection** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6f670-171">On the **Protection settings** page that appears, configure the following settings:</span></span>
   - <span data-ttu-id="6f670-172">**Sélectionnez l’action pour les URL potentiellement malveillantes inconnues** dans les messages : sélectionnez **Activé** pour activer la protection des liens vers des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="6f670-172">**Select the action for unknown potentially malicious URLs in messages**: Select **On** to enable Safe Links protection for links in email messages.</span></span> <span data-ttu-id="6f670-173">Si vous allumez ce paramètre, les paramètres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="6f670-173">If you turn this setting on, the following settings are available:</span></span>
     - <span data-ttu-id="6f670-174">**Appliquer l’analyse d’URL** en temps réel pour les liens suspects et les liens pointant vers des fichiers : sélectionnez cette option pour activer l’analyse en temps réel des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="6f670-174">**Apply real-time URL scanning for suspicious links and links that point to files**: Select this option to enable real-time scanning of links in email messages.</span></span> <span data-ttu-id="6f670-175">Si vous activer ce paramètre, le paramètre suivant est disponible :</span><span class="sxs-lookup"><span data-stu-id="6f670-175">If you turn this setting on the following setting is available:</span></span>
       - <span data-ttu-id="6f670-176">**Attendez que l’analyse des URL** se termine avant de remettre le message : sélectionnez cette option pour attendre la fin de l’analyse de l’URL en temps réel avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="6f670-176">**Wait for URL scanning to complete before delivering the message**: Select this option to wait for real-time URL scanning to complete before delivering the message.</span></span>
     - <span data-ttu-id="6f670-177">**Appliquer des liens sûrs aux messages** électroniques envoyés au sein de l’organisation : sélectionnez cette option pour appliquer la stratégie de liens sécurisés aux messages entre les expéditeurs internes et les destinataires internes.</span><span class="sxs-lookup"><span data-stu-id="6f670-177">**Apply Safe Links to email messages sent within the organization**: Select this option to apply the Safe Links policy to messages between internal senders and internal recipients.</span></span>
   - <span data-ttu-id="6f670-178">**Sélectionnez l’action** pour les URL inconnues ou  potentiellement malveillantes dans Microsoft Teams : sélectionnez Activé pour activer la protection des liens sécurisés pour les liens Teams.</span><span class="sxs-lookup"><span data-stu-id="6f670-178">**Select the action for unknown or potentially malicious URLs within Microsoft Teams**: Select **On** to enable Safe Links protection for links in Teams.</span></span>
   - <span data-ttu-id="6f670-179">**Ne pas suivre les clics** de l’utilisateur : laissez ce paramètre désélectionnés pour activer les clics de l’utilisateur de suivi sur les URL des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="6f670-179">**Do not track user clicks**: Leave this setting unselected to enable the tracking user clicks on URLs in email messages.</span></span>
   - <span data-ttu-id="6f670-180">**N’autorisez pas** les utilisateurs à cliquer sur l’URL d’origine : sélectionnez cette option pour empêcher les utilisateurs de cliquer jusqu’à l’URL d’origine dans les [pages d’avertissement.](safe-links.md#warning-pages-from-safe-links)</span><span class="sxs-lookup"><span data-stu-id="6f670-180">**Do not allow users to click through to original URL**: Select this option to block users from clicking through to the original URL in [warning pages](safe-links.md#warning-pages-from-safe-links).</span></span>
   - <span data-ttu-id="6f670-181">**Ne réécrivez pas les** URL suivantes : permet d’accéder aux URL spécifiées qui seraient autrement bloquées par les liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-181">**Do not rewrite the following URLs**: Allows access the specified URLs that would otherwise be blocked by Safe Links.</span></span>

     <span data-ttu-id="6f670-182">Dans la zone, tapez l’URL ou la valeur que vous souhaitez, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="6f670-182">In the box, type the URL or value that you want, and then click **Add**.</span></span> <span data-ttu-id="6f670-183">Répétez cette étape autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6f670-183">Repeat this step as many times as necessary.</span></span>

     <span data-ttu-id="6f670-184">Pour supprimer une entrée existante, cliquez sur</span><span class="sxs-lookup"><span data-stu-id="6f670-184">To remove an existing entry, click</span></span> ![Icône Suppression](../../media/m365-cc-sc-remove-selection-icon.png) <span data-ttu-id="6f670-186">à côté de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f670-186">next to the entry.</span></span>

     <span data-ttu-id="6f670-187">Pour la syntaxe d’entrée, voir [syntaxe d’entrée pour la](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="6f670-187">For entry syntax, see [Entry syntax for the "Do not rewrite the following URLs" list](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>

   <span data-ttu-id="6f670-188">Pour plus d’informations sur ces paramètres, consultez la liste des paramètres de liens [sécurisés](safe-links.md#safe-links-settings-for-email-messages) pour les messages électroniques et les [paramètres](safe-links.md#safe-links-settings-for-microsoft-teams)de liens Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="6f670-188">For detailed information about these settings, see [Safe Links settings for email messages](safe-links.md#safe-links-settings-for-email-messages) and [Safe Links settings for Microsoft Teams](safe-links.md#safe-links-settings-for-microsoft-teams).</span></span>

   <span data-ttu-id="6f670-189">Pour plus d’informations sur les valeurs recommandées pour les paramètres de stratégie Standard et Strict, voir Paramètres de [stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="6f670-189">For more the recommended values for Standard and Strict policy settings, see [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).</span></span>

   <span data-ttu-id="6f670-190">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f670-190">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="6f670-191">Dans la page **notification** qui s’affiche, sélectionnez l’une des valeurs suivantes pour avertir **vos utilisateurs :**</span><span class="sxs-lookup"><span data-stu-id="6f670-191">On the **Notification** page that appears, select one of the following values for **How would you like to notify your users?**:</span></span>
   - <span data-ttu-id="6f670-192">**Utiliser le texte de notification par défaut**</span><span class="sxs-lookup"><span data-stu-id="6f670-192">**Use the default notification text**</span></span>
   - <span data-ttu-id="6f670-193">**Utilisez un texte de notification personnalisé**: si vous sélectionnez cette valeur, les paramètres suivants s’affichent :</span><span class="sxs-lookup"><span data-stu-id="6f670-193">**Use custom notification text**: If you select this value, the following settings appear:</span></span>
     - <span data-ttu-id="6f670-194">**Utiliser Microsoft Traducteur pour la localisation automatique**</span><span class="sxs-lookup"><span data-stu-id="6f670-194">**Use Microsoft Translator for automatic localization**</span></span>
     - <span data-ttu-id="6f670-195">**Texte de notification personnalisé**: entrez le texte de notification personnalisé dans cette zone.</span><span class="sxs-lookup"><span data-stu-id="6f670-195">**Custom notification text**: Enter the custom notification text in this box.</span></span>

   <span data-ttu-id="6f670-196">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6f670-196">When you're finished, click **Next**.</span></span>

7. <span data-ttu-id="6f670-197">Dans la page **Révision** qui s’affiche, passez en revue vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="6f670-197">On the **Review** page that appears, review your settings.</span></span> <span data-ttu-id="6f670-198">Vous pouvez sélectionner **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="6f670-198">You can select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="6f670-199">Vous pouvez également cliquer sur **Précédent** ou sélectionner la page spécifique dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="6f670-199">Or you can click **Back** or select the specific page in the wizard.</span></span>

   <span data-ttu-id="6f670-200">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="6f670-200">When you're finished, click **Submit**.</span></span>

8. <span data-ttu-id="6f670-201">Dans la page de confirmation qui s’affiche, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="6f670-201">On the confirmation page that appears, click **Done**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-safe-links-policies"></a><span data-ttu-id="6f670-202">Utiliser le portail Microsoft 365 Defender pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-202">Use the Microsoft 365 Defender portal to view Safe Links policies</span></span>

1. <span data-ttu-id="6f670-203">Dans le portail Microsoft 365 Defender, go to **Policies & rules** Threat \> **Policies** section \>  Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-203">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-204">Dans la page **Liens sécurisés,** les propriétés suivantes sont affichées dans la liste des stratégies de liens sécurisés :</span><span class="sxs-lookup"><span data-stu-id="6f670-204">On the **Safe Links** page, the following properties are displayed in the list of Safe Links policies:</span></span>
   - <span data-ttu-id="6f670-205">**Name**</span><span class="sxs-lookup"><span data-stu-id="6f670-205">**Name**</span></span>
   - <span data-ttu-id="6f670-206">**État**</span><span class="sxs-lookup"><span data-stu-id="6f670-206">**Status**</span></span>
   - <span data-ttu-id="6f670-207">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6f670-207">**Priority**</span></span>

3. <span data-ttu-id="6f670-208">Lorsque vous sélectionnez une stratégie en cliquant sur le nom, les paramètres de stratégie s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="6f670-208">When you select a policy by clicking on the name, the policy settings are displayed in a flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-safe-links-policies"></a><span data-ttu-id="6f670-209">Utiliser le portail Microsoft 365 Defender pour modifier les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-209">Use the Microsoft 365 Defender portal to modify Safe Links policies</span></span>

1. <span data-ttu-id="6f670-210">Dans le portail Microsoft 365 Defender, go to **Policies & rules** Threat \> **Policies** section \>  Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-210">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-211">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="6f670-211">On the **Safe Links** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="6f670-212">Dans le menu volant des détails de stratégie qui s’affiche, sélectionnez **Modifier** dans chaque section pour modifier les paramètres de la section.</span><span class="sxs-lookup"><span data-stu-id="6f670-212">In the policy details flyout that appears, select **Edit** in each section to modify the settings within the section.</span></span> <span data-ttu-id="6f670-213">Pour plus d’informations sur les paramètres, voir la section précédente Utiliser le portail [Microsoft 365 Defender](#use-the-microsoft-365-defender-portal-to-create-safe-links-policies) pour créer des stratégies de liens sécurisés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-213">For more information about the settings, see the previous [Use the Microsoft 365 Defender portal to create Safe Links policies](#use-the-microsoft-365-defender-portal-to-create-safe-links-policies) section in this article.</span></span>  

<span data-ttu-id="6f670-214">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f670-214">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-links-policies"></a><span data-ttu-id="6f670-215">Activer ou désactiver les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-215">Enable or disable Safe Links policies</span></span>

1. <span data-ttu-id="6f670-216">Dans le portail Microsoft 365 Defender, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-216">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-217">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="6f670-217">On the **Safe Links** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="6f670-218">En haut du menu volant des détails de stratégie qui s’affiche, vous verrez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f670-218">At the top of the policy details flyout that appears, you'll see one of the following values:</span></span>
   - <span data-ttu-id="6f670-219">**Stratégie désactivée** : pour activer la stratégie, cliquez sur ![Icône Activer](../../media/m365-cc-sc-turn-on-off-icon.png) **Activer**.</span><span class="sxs-lookup"><span data-stu-id="6f670-219">**Policy off**: To turn on the policy, click ![Turn on icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn on** .</span></span>
   - <span data-ttu-id="6f670-220">**Stratégie activée** : pour activer la stratégie, cliquez sur ![Icône Désactiver](../../media/m365-cc-sc-turn-on-off-icon.png) **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="6f670-220">**Policy on**: To turn off the policy, click ![Turn off icon](../../media/m365-cc-sc-turn-on-off-icon.png) **Turn off**.</span></span>

4. <span data-ttu-id="6f670-221">Dans la boîte de dialogue de confirmation qui s’affiche, cliquez sur **Activer** ou **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="6f670-221">In the confirmation dialog that appears, click **Turn on** or **Turn off**.</span></span>

5. <span data-ttu-id="6f670-222">Cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6f670-222">Click **Close** in the policy details flyout.</span></span>

<span data-ttu-id="6f670-223">De retour sur la page principale de la stratégie, la valeur **État** de la stratégie sera **Activée** ou **Désactivée**.</span><span class="sxs-lookup"><span data-stu-id="6f670-223">Back on the main policy page, the **Status** value of the policy will be **On** or **Off**.</span></span>

### <a name="set-the-priority-of-safe-links-policies"></a><span data-ttu-id="6f670-224">Définir la priorité des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-224">Set the priority of Safe Links policies</span></span>

<span data-ttu-id="6f670-225">Par défaut, les liens sécurisés ont une priorité qui est basée sur l’ordre de leur création (les stratégies les plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="6f670-225">By default, Safe Links are given a priority that's based on the order they were created in (newer policies are lower priority than older policies).</span></span> <span data-ttu-id="6f670-226">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="6f670-226">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="6f670-227">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="6f670-227">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="6f670-228">Pour modifier la priorité d’une stratégie, cliquez sur **Augmenter la priorité** ou **Diminuer la priorité** dans les propriétés de la stratégie (vous ne pouvez pas modifier directement le numéro **Priorité** dans le Portail Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="6f670-228">To change the priority of a policy, you click **Increase priority** or **Decrease priority** in the properties of the policy (you can't directly modify the **Priority** number in the Microsoft 365 Defender portal).</span></span> <span data-ttu-id="6f670-229">La modification de la priorité d’une stratégie n’a de sens que si vous avez plusieurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="6f670-229">Changing the priority of a policy only makes sense if you have multiple policies.</span></span>

<span data-ttu-id="6f670-230">**Remarque** :</span><span class="sxs-lookup"><span data-stu-id="6f670-230">**Note**:</span></span>

- <span data-ttu-id="6f670-231">Dans le Microsoft 365 Defender, vous ne pouvez modifier la priorité de la stratégie de liens sécurisés qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="6f670-231">In the Microsoft 365 Defender portal, you can only change the priority of the Safe Links policy after you create it.</span></span> <span data-ttu-id="6f670-232">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle de liens sécurisés (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="6f670-232">In PowerShell, you can override the default priority when you create the safe links rule (which can affect the priority of existing rules).</span></span>
- <span data-ttu-id="6f670-233">Les stratégies de liens sécurisés sont traitées dans l’ordre d’affichage (la première stratégie a la valeur Priorité 0). </span><span class="sxs-lookup"><span data-stu-id="6f670-233">Safe Links policies are processed in the order that they're displayed (the first policy has the **Priority** value 0).</span></span> <span data-ttu-id="6f670-234">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="6f670-234">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

1. <span data-ttu-id="6f670-235">Dans le portail Microsoft 365 Defender, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-235">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-236">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="6f670-236">On the **Safe Links** page, select a policy from the list by clicking on the name.</span></span>

3. <span data-ttu-id="6f670-237">En haut du menu volant détails de la stratégie qui s’affiche, vous verrez **Augmenter la priorité** ou **Diminuer la priorité** en fonction de la valeur de priorité actuelle et du nombre de stratégies personnalisées :</span><span class="sxs-lookup"><span data-stu-id="6f670-237">At the top of the policy details flyout that appears, you'll see **Increase priority** or **Decrease priority** based on the current priority value and the number of custom policies:</span></span>
   - <span data-ttu-id="6f670-238">La stratégie dont la valeur **de** priorité **est 0** ne dispose que de l’option Diminuer **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="6f670-238">The policy with the **Priority** value **0** has only the **Decrease priority** option available.</span></span>
   - <span data-ttu-id="6f670-239">La stratégie dont la valeur **de** priorité est la plus faible (par exemple, **3**) n’a que l’option Augmenter **la** priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="6f670-239">The policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** option available.</span></span>
   - <span data-ttu-id="6f670-240">Si vous avez au moins trois stratégies, les stratégies  entre les valeurs de priorité les plus élevées et les plus faibles ont les options Augmenter la priorité et Diminuer **la** priorité disponibles.</span><span class="sxs-lookup"><span data-stu-id="6f670-240">If you have three or more policies, the policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** options available.</span></span>

   <span data-ttu-id="6f670-241">Cliquez sur l’![Icône Augmenter la priorité](../../media/m365-cc-sc-increase-icon.png) **Augmenter la priorité** ou ![Icône Diminuer la priorité](../../media/m365-cc-sc-decrease-icon.png) **Diminuer la priorité** pour modifier la valeur **Priorité**.</span><span class="sxs-lookup"><span data-stu-id="6f670-241">Click ![Increase priority icon](../../media/m365-cc-sc-increase-icon.png) **Increase priority** or ![Decrease priority icon](../../media/m365-cc-sc-decrease-icon.png) **Decrease priority** to change the **Priority** value.</span></span>

4. <span data-ttu-id="6f670-242">Lorsque vous avez terminé, cliquez sur **Fermer** dans le menu volant des détails de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6f670-242">When you're finished, click **Close** in the policy details flyout.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-safe-links-policies"></a><span data-ttu-id="6f670-243">Utiliser le portail Microsoft 365 Defender pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-243">Use the Microsoft 365 Defender portal to remove Safe Links policies</span></span>

1. <span data-ttu-id="6f670-244">Dans le portail Microsoft 365 Defender, go to **Email & Collaboration** Policies & \> **Rules** Threat \>  \> **policies** section \> **Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-244">In the Microsoft 365 Defender portal, go to **Email & Collaboration** \> **Policies & Rules** \> **Threat policies** \> **Policies** section \> **Safe Links**.</span></span>

2. <span data-ttu-id="6f670-245">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste en cliquant sur le nom.</span><span class="sxs-lookup"><span data-stu-id="6f670-245">On the **Safe Links** page, select a policy from the list by clicking on the name.</span></span> <span data-ttu-id="6f670-246">En haut du menu volant Détails de la stratégie qui s’affiche, cliquez sur l’![Icône Autres actions](../../media/m365-cc-sc-more-actions-icon.png) **Autres actions** \> ![Icône Supprimer la stratégie](../../media/m365-cc-sc-delete-icon.png) **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="6f670-246">At the top of the policy details flyout that appears, click ![More actions icon](../../media/m365-cc-sc-more-actions-icon.png) **More actions** \> ![Delete policy icon](../../media/m365-cc-sc-delete-icon.png) **Delete policy**.</span></span>

3. <span data-ttu-id="6f670-247">Dans la boîte de dialogue de confirmation qui s'affiche, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="6f670-247">In the confirmation dialog that appears, click **Yes**.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies"></a><span data-ttu-id="6f670-248">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-248">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies</span></span>

<span data-ttu-id="6f670-249">Comme décrit précédemment, une stratégie de liens sécurisés se compose d’une stratégie de liens sécurisés et d’une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-249">As previously described, a Safe Links policy consists of a safe links policy and a safe links rule.</span></span>

<span data-ttu-id="6f670-250">Dans PowerShell, la différence entre les stratégies de liens sécurisés et les règles de liens sécurisés est évidente.</span><span class="sxs-lookup"><span data-stu-id="6f670-250">In PowerShell, the difference between safe links policies and safe links rules is apparent.</span></span> <span data-ttu-id="6f670-251">Vous gérez les stratégies de liens sécurisés à l’aide des cmdlets **\* -SafeLinksPolicy** et vous gérez les règles de liens sécurisés à l’aide des cmdlets **\* -SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="6f670-251">You manage safe links policies by using the **\*-SafeLinksPolicy** cmdlets, and you manage safe links rules by using the **\*-SafeLinksRule** cmdlets.</span></span>

- <span data-ttu-id="6f670-252">Dans PowerShell, vous créez d’abord la stratégie de liens sécurisés, puis vous créez la règle de liens sécurisés qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="6f670-252">In PowerShell, you create the safe links policy first, then you create the safe links rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="6f670-253">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de liens sécurisés et de la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-253">In PowerShell, you modify the settings in the safe links policy and the safe links rule separately.</span></span>
- <span data-ttu-id="6f670-254">Lorsque vous supprimez une stratégie de liens sécurisés de PowerShell, la règle de liens sécurisés correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="6f670-254">When you remove a safe links policy from PowerShell, the corresponding safe links rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-links-policies"></a><span data-ttu-id="6f670-255">Utiliser PowerShell pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-255">Use PowerShell to create Safe Links policies</span></span>

<span data-ttu-id="6f670-256">La création d’une stratégie de liens sécurisés dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="6f670-256">Creating a Safe Links policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="6f670-257">Créez la stratégie de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-257">Create the safe links policy.</span></span>
2. <span data-ttu-id="6f670-258">Créez la règle de liens sécurisés qui spécifie la stratégie de liens sécurisés à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="6f670-258">Create the safe links rule that specifies the safe links policy that the rule applies to.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="6f670-259">Vous pouvez créer une règle de liens sécurisés et lui attribuer une stratégie de liens sécurisés non associés existante.</span><span class="sxs-lookup"><span data-stu-id="6f670-259">You can create a new safe links rule and assign an existing, unassociated safe links policy to it.</span></span> <span data-ttu-id="6f670-260">Une règle de liens sécurisés ne peut pas être associée à plusieurs stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-260">A safe links rule can't be associated with more than one safe links policy.</span></span>
>
> - <span data-ttu-id="6f670-261">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de liens sécurisés dans PowerShell qui ne sont pas disponibles dans le portail Microsoft 365 Defender tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="6f670-261">You can configure the following settings on new safe links policies in PowerShell that aren't available in the Microsoft 365 Defender portal until after you create the policy:</span></span>
>   - <span data-ttu-id="6f670-262">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="6f670-262">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeLinksRule** cmdlet).</span></span>
>   - <span data-ttu-id="6f670-263">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="6f670-263">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeLinksRule** cmdlet).</span></span>
>
> - <span data-ttu-id="6f670-264">Une nouvelle stratégie de liens sécurisés que vous créez dans PowerShell n’est pas visible dans le portail Microsoft 365 Defender tant que vous n’avez pas attribué la stratégie à une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-264">A new safe links policy that you create in PowerShell isn't visible in the Microsoft 365 Defender portal until you assign the policy to a safe links rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-links-policy"></a><span data-ttu-id="6f670-265">Étape 1 : Utiliser PowerShell pour créer une stratégie de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-265">Step 1: Use PowerShell to create a safe links policy</span></span>

<span data-ttu-id="6f670-266">Pour créer une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-266">To create a safe links policy, use this syntax:</span></span>

```PowerShell
New-SafeLinksPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-IsEnabled <$true | $false>] [-EnableSafeLinksForTeams <$true | $false>] [-ScanUrls <$true | $false>] [-DeliverMessageAfterScan <$true | $false>] [-EnableForInternalSenders <$true | $false>] [-DoNotAllowClickThrough <$true | $false>] [-DoNotTrackUserClicks <$true | $false>] [-DoNotRewriteUrls "Entry1","Entry2",..."EntryN"]
```

> [!NOTE]
>
> - <span data-ttu-id="6f670-267">Pour plus d’informations sur la syntaxe d’entrée à utiliser pour le paramètre _DoNotRewriteUrls,_ voir la [syntaxe d’entrée](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)pour la liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="6f670-267">For details about the entry syntax to use for the _DoNotRewriteUrls_ parameter, see [Entry syntax for the "Do not rewrite the following URLs" list](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>
>
> - <span data-ttu-id="6f670-268">Pour obtenir une syntaxe supplémentaire que vous pouvez utiliser pour le paramètre _DoNotRewriteUrls_ lorsque vous modifiez des stratégies de liens sécurisés existantes à l’aide de la cmdlet **Set-SafeLinksPolicy,** consultez la section Utiliser [PowerShell](#use-powershell-to-modify-safe-links-policies) pour modifier les stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-268">For additional syntax that you can use for the _DoNotRewriteUrls_ parameter when you modify existing safe links policies by using the **Set-SafeLinksPolicy** cmdlet, see the [Use PowerShell to modify safe links policies](#use-powershell-to-modify-safe-links-policies) section later in this article.</span></span>

<span data-ttu-id="6f670-269">Cet exemple crée une stratégie de liens sécurisés nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f670-269">This example creates a safe links policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="6f670-270">Activer l’analyse et la réécriture d’URL dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="6f670-270">Turn on URL scanning and rewriting in email messages.</span></span>
- <span data-ttu-id="6f670-271">Activer l’analyse des URL dans Teams (aperçu tap uniquement).</span><span class="sxs-lookup"><span data-stu-id="6f670-271">Turn on URL scanning in Teams (TAP Preview only).</span></span>
- <span data-ttu-id="6f670-272">Activer l’analyse en temps réel des URL sur lesquelles vous avez cliqué, y compris les liens qui pointent vers des fichiers.</span><span class="sxs-lookup"><span data-stu-id="6f670-272">Turn on real-time scanning of clicked URLs, including clicked links that point to files.</span></span>
- <span data-ttu-id="6f670-273">Attendez la fin de l’analyse de l’URL avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="6f670-273">Wait for URL scanning to complete before delivering the message.</span></span>
- <span data-ttu-id="6f670-274">Activer l’analyse et la réécriture d’URL pour les messages internes.</span><span class="sxs-lookup"><span data-stu-id="6f670-274">Turn on URL scanning and rewriting for internal messages.</span></span>
- <span data-ttu-id="6f670-275">Suivez les clics des utilisateurs liés à la protection contre les liens sécurisés (nous n’utilisons pas le paramètre _DoNotTrackUserClicks_ et la valeur par défaut est $false, ce qui signifie que les clics utilisateur sont suivis).</span><span class="sxs-lookup"><span data-stu-id="6f670-275">Track user clicks related to Safe Links protection (we aren't using the _DoNotTrackUserClicks_ parameter, and the default value is $false, which means user clicks are tracked).</span></span>
- <span data-ttu-id="6f670-276">N’autorisez pas les utilisateurs à accéder à l’URL d’origine en cliquant.</span><span class="sxs-lookup"><span data-stu-id="6f670-276">Do not allow users to click through to the original URL.</span></span>

```PowerShell
New-SafeLinksPolicy -Name "Contoso All" -IsEnabled $true -EnableSafeLinksForTeams $true -ScanUrls $true -DeliverMessageAfterScan $true -EnableForInternalSenders $true -DoNotAllowClickThrough $true
```

<span data-ttu-id="6f670-277">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksPolicy.](/powershell/module/exchange/new-safelinkspolicy)</span><span class="sxs-lookup"><span data-stu-id="6f670-277">For detailed syntax and parameter information, see [New-SafeLinksPolicy](/powershell/module/exchange/new-safelinkspolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-links-rule"></a><span data-ttu-id="6f670-278">Étape 2 : Utiliser PowerShell pour créer une règle de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-278">Step 2: Use PowerShell to create a safe links rule</span></span>

<span data-ttu-id="6f670-279">Pour créer une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-279">To create a safe links rule, use this syntax:</span></span>

```PowerShell
New-SafeLinksRule -Name "<RuleName>" -SafeLinksPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="6f670-280">Cet exemple crée une règle de liens sécurisés nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f670-280">This example creates a safe links rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="6f670-281">La règle est associée à la stratégie de liens sécurisés nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="6f670-281">The rule is associated with the safe links policy named Contoso All.</span></span>
- <span data-ttu-id="6f670-282">La règle s’applique à tous les destinataires du contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="6f670-282">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="6f670-283">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6f670-283">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="6f670-284">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="6f670-284">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeLinksRule -Name "Contoso All" -SafeLinksPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="6f670-285">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksRule](/powershell/module/exchange/new-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-285">For detailed syntax and parameter information, see [New-SafeLinksRule](/powershell/module/exchange/new-safelinksrule).</span></span>

### <a name="use-powershell-to-view-safe-links-policies"></a><span data-ttu-id="6f670-286">Utiliser PowerShell pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-286">Use PowerShell to view safe links policies</span></span>

<span data-ttu-id="6f670-287">Pour afficher les stratégies de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-287">To view existing safe links policies, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="6f670-288">Cet exemple renvoie une liste récapitulatif de toutes les stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-288">This example returns a summary list of all safe links policies.</span></span>

```PowerShell
Get-SafeLinksPolicy | Format-Table Name
```

<span data-ttu-id="6f670-289">Cet exemple renvoie des informations détaillées sur la stratégie de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="6f670-289">This example returns detailed information for the safe links policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksPolicy -Identity "Contoso Executives"
```

<span data-ttu-id="6f670-290">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksPolicy](/powershell/module/exchange/get-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="6f670-290">For detailed syntax and parameter information, see [Get-SafeLinksPolicy](/powershell/module/exchange/get-safelinkspolicy).</span></span>

### <a name="use-powershell-to-view-safe-links-rules"></a><span data-ttu-id="6f670-291">Utiliser PowerShell pour afficher les règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-291">Use PowerShell to view safe links rules</span></span>

<span data-ttu-id="6f670-292">Pour afficher les règles de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-292">To view existing safe links rules, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="6f670-293">Cet exemple renvoie une liste récapitulatif de toutes les règles de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="6f670-293">This example returns a summary list of all safe links rules.</span></span>

```PowerShell
Get-SafeLinksRule | Format-Table Name,State
```

<span data-ttu-id="6f670-294">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f670-294">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeLinksRule -State Disabled
```

```PowerShell
Get-SafeLinksRule -State Enabled
```

<span data-ttu-id="6f670-295">Cet exemple renvoie des informations détaillées sur la règle de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="6f670-295">This example returns detailed information for the safe links rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksRule -Identity "Contoso Executives"
```

<span data-ttu-id="6f670-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksRule](/powershell/module/exchange/get-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-296">For detailed syntax and parameter information, see [Get-SafeLinksRule](/powershell/module/exchange/get-safelinksrule).</span></span>

### <a name="use-powershell-to-modify-safe-links-policies"></a><span data-ttu-id="6f670-297">Utiliser PowerShell pour modifier des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-297">Use PowerShell to modify safe links policies</span></span>

<span data-ttu-id="6f670-298">Vous ne pouvez pas renommer une stratégie de liens sécurisés dans PowerShell (la cmdlet **Set-SafeLinksPolicy** n’a pas _de paramètre_ Name).</span><span class="sxs-lookup"><span data-stu-id="6f670-298">You can't rename a safe links policy in PowerShell (the **Set-SafeLinksPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="6f670-299">Lorsque vous renommez une stratégie de liens sécurisés dans le portail Microsoft 365 Defender, vous renommez uniquement la règle de liens _sécurisés._</span><span class="sxs-lookup"><span data-stu-id="6f670-299">When you rename a Safe Links policy in the Microsoft 365 Defender portal, you're only renaming the safe links _rule_.</span></span>

<span data-ttu-id="6f670-300">La seule considération supplémentaire pour modifier les stratégies de liens sécurisés dans PowerShell est la syntaxe disponible pour le paramètre _DoNotRewriteUrls_ (la liste « Ne pas réécrire les URL [suivantes](safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)» ) :</span><span class="sxs-lookup"><span data-stu-id="6f670-300">The only additional consideration for modifying safe links policies in PowerShell is the available syntax for the _DoNotRewriteUrls_ parameter (the ["Do not rewrite the following URLs" list](safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)):</span></span>

- <span data-ttu-id="6f670-301">Pour ajouter des valeurs qui remplaceront les entrées existantes, utilisez la syntaxe suivante `"Entry1","Entry2,..."EntryN"` :</span><span class="sxs-lookup"><span data-stu-id="6f670-301">To add values that will replace any existing entries, use the following syntax: `"Entry1","Entry2,..."EntryN"`.</span></span>
- <span data-ttu-id="6f670-302">Pour ajouter ou supprimer des valeurs sans affecter les autres entrées existantes, utilisez la syntaxe suivante : `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span><span class="sxs-lookup"><span data-stu-id="6f670-302">To add or remove values without affecting other existing entries, use the following syntax: `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span></span>

<span data-ttu-id="6f670-303">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de liens sécurisés, comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-a-safe-links-policy) pour créer une section de stratégie de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-303">Otherwise, the same settings are available when you create a safe links policy as described in the [Step 1: Use PowerShell to create a safe links policy](#step-1-use-powershell-to-create-a-safe-links-policy) section earlier in this article.</span></span>

<span data-ttu-id="6f670-304">Pour modifier une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-304">To modify a safe links policy, use this syntax:</span></span>

```PowerShell
Set-SafeLinksPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="6f670-305">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksPolicy](/powershell/module/exchange/set-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="6f670-305">For detailed syntax and parameter information, see [Set-SafeLinksPolicy](/powershell/module/exchange/set-safelinkspolicy).</span></span>

### <a name="use-powershell-to-modify-safe-links-rules"></a><span data-ttu-id="6f670-306">Utiliser PowerShell pour modifier des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-306">Use PowerShell to modify safe links rules</span></span>

<span data-ttu-id="6f670-307">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de liens sécurisés dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="6f670-307">The only setting that's not available when you modify a safe links rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="6f670-308">Pour activer ou désactiver des règles de liens sécurisés existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="6f670-308">To enable or disable existing safe links rules, see the next section.</span></span>

<span data-ttu-id="6f670-309">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-a-safe-links-rule) pour créer une section de règle de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6f670-309">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe links rule](#step-2-use-powershell-to-create-a-safe-links-rule) section earlier in this article.</span></span>

<span data-ttu-id="6f670-310">Pour modifier une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-310">To modify a safe links rule, use this syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="6f670-311">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-311">For detailed syntax and parameter information, see [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-links-rules"></a><span data-ttu-id="6f670-312">Utiliser PowerShell pour activer ou désactiver des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-312">Use PowerShell to enable or disable safe links rules</span></span>

<span data-ttu-id="6f670-313">L’activation ou la désactivation d’une règle de liens sécurisés dans PowerShell active ou désactive l’ensemble de la stratégie de liens sécurisés (la règle de liens sécurisés et la stratégie de liens sécurisés affectée).</span><span class="sxs-lookup"><span data-stu-id="6f670-313">Enabling or disabling a safe links rule in PowerShell enables or disables the whole Safe Links policy (the safe links rule and the assigned safe links policy).</span></span>

<span data-ttu-id="6f670-314">Pour activer ou désactiver une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-314">To enable or disable a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeLinksRule | Disable-SafeLinksRule> -Identity "<RuleName>"
```

<span data-ttu-id="6f670-315">Cet exemple désactive la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="6f670-315">This example disables the safe links rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="6f670-316">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="6f670-316">This example enables same rule.</span></span>

```PowerShell
Enable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="6f670-317">Pour obtenir des informations détaillées sur la syntaxe et les [paramètres, voir Enable-SafeLinksRule](/powershell/module/exchange/enable-safelinksrule) et [Disable-SafeLinksRule](/powershell/module/exchange/disable-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-317">For detailed syntax and parameter information, see [Enable-SafeLinksRule](/powershell/module/exchange/enable-safelinksrule) and [Disable-SafeLinksRule](/powershell/module/exchange/disable-safelinksrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-links-rules"></a><span data-ttu-id="6f670-318">Utiliser PowerShell pour définir la priorité des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-318">Use PowerShell to set the priority of safe links rules</span></span>

<span data-ttu-id="6f670-p131">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle. La valeur la plus basse que vous pouvez définir dépend du nombre de règles. Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4. Tout changement de priorité d'une règle existante peut avoir un effet en cascade sur les autres règles. Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="6f670-p131">The highest priority value you can set on a rule is 0. The lowest value you can set depends on the number of rules. For example, if you have five rules, you can use the priority values 0 through 4. Changing the priority of an existing rule can have a cascading effect on other rules. For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="6f670-324">Pour définir la priorité d’une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-324">To set the priority of a safe links rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="6f670-p132">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="6f670-p132">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeLinksRule -Identity "Marketing Department" -Priority 2
```

> [!NOTE]
> <span data-ttu-id="6f670-327">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="6f670-327">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeLinksRule** cmdlet instead.</span></span>

<span data-ttu-id="6f670-328">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-328">For detailed syntax and parameter information, see [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-remove-safe-links-policies"></a><span data-ttu-id="6f670-329">Utiliser PowerShell pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-329">Use PowerShell to remove safe links policies</span></span>

<span data-ttu-id="6f670-330">Lorsque vous utilisez PowerShell pour supprimer une stratégie de liens sécurisés, la règle de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="6f670-330">When you use PowerShell to remove a safe links policy, the corresponding safe links rule isn't removed.</span></span>

<span data-ttu-id="6f670-331">Pour supprimer une stratégie de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-331">To remove a safe links policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="6f670-332">Cet exemple supprime la stratégie de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="6f670-332">This example removes the safe links policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "Marketing Department"
```

<span data-ttu-id="6f670-333">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksPolicy](/powershell/module/exchange/remove-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="6f670-333">For detailed syntax and parameter information, see [Remove-SafeLinksPolicy](/powershell/module/exchange/remove-safelinkspolicy).</span></span>

### <a name="use-powershell-to-remove-safe-links-rules"></a><span data-ttu-id="6f670-334">Utiliser PowerShell pour supprimer des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="6f670-334">Use PowerShell to remove safe links rules</span></span>

<span data-ttu-id="6f670-335">Lorsque vous utilisez PowerShell pour supprimer une règle de liens sécurisés, la stratégie de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="6f670-335">When you use PowerShell to remove a safe links rule, the corresponding safe links policy isn't removed.</span></span>

<span data-ttu-id="6f670-336">Pour supprimer une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f670-336">To remove a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "<PolicyName>"
```

<span data-ttu-id="6f670-337">Cet exemple supprime la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="6f670-337">This example removes the safe links rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="6f670-338">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksRule](/powershell/module/exchange/remove-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="6f670-338">For detailed syntax and parameter information, see [Remove-SafeLinksRule](/powershell/module/exchange/remove-safelinksrule).</span></span>

<span data-ttu-id="6f670-339">Pour vérifier que la sécurité est en cours d’analyse des messages, vérifiez que Microsoft Defender est disponible Office 365 rapports.</span><span class="sxs-lookup"><span data-stu-id="6f670-339">To verify that Safe Links is scanning messages, check the available Microsoft Defender for Office 365 reports.</span></span> <span data-ttu-id="6f670-340">Pour plus d’informations, voir Afficher les [rapports de Defender pour Office 365](view-reports-for-mdo.md) et Utiliser l’Explorateur dans le portail Microsoft 365 [Defender.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="6f670-340">For more information, see [View reports for Defender for Office 365](view-reports-for-mdo.md) and [Use Explorer in the Microsoft 365 Defender portal](threat-explorer.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="6f670-341">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="6f670-341">How do you know these procedures worked?</span></span>

<span data-ttu-id="6f670-342">Pour vérifier que vous avez correctement créé, modifié ou supprimé des stratégies de liens sécurisés, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f670-342">To verify that you've successfully created, modified, or removed Safe Links policies, do any of the following steps:</span></span>

- <span data-ttu-id="6f670-343">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="6f670-343">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Safe Links**.</span></span> <span data-ttu-id="6f670-344">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="6f670-344">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="6f670-345">Pour afficher plus de détails, sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="6f670-345">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="6f670-346">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les \<Name\> paramètres :</span><span class="sxs-lookup"><span data-stu-id="6f670-346">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeLinksPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-SafeLinksRule -Identity "<Name>"
  ```
