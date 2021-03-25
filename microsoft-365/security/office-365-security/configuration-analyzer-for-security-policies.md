---
title: Analyseur de configuration pour les stratégies de sécurité
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: ''
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser l’analyseur de configuration pour rechercher et corriger les stratégies de sécurité qui se trouvent en dessous des stratégies de sécurité prédéfines Protection standard et Protection stricte.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 65fd67c93711dc847a25be485b4b016af55e4a31
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51203995"
---
# <a name="configuration-analyzer-for-protection-policies-in-eop-and-microsoft-defender-for-office-365"></a><span data-ttu-id="9519d-103">Analyseur de configuration des stratégies de protection dans EOP et Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9519d-103">Configuration analyzer for protection policies in EOP and Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="9519d-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9519d-104">**Applies to**</span></span>
- [<span data-ttu-id="9519d-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="9519d-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="9519d-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="9519d-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="9519d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9519d-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="9519d-108">L’analyseur de configuration dans le Centre de sécurité & conformité fournit un emplacement central pour rechercher et corriger [](preset-security-policies.md)les stratégies de sécurité où les paramètres se trouvent sous les paramètres de profil protection standard et strict dans les stratégies de sécurité prédéfines.</span><span class="sxs-lookup"><span data-stu-id="9519d-108">Configuration analyzer in the Security & Compliance center provides a central location to find and fix security policies where the settings are below the Standard protection and Strict protection profile settings in [preset security policies](preset-security-policies.md).</span></span>

<span data-ttu-id="9519d-109">Les types de stratégies suivants sont analysés par l’analyseur de configuration :</span><span class="sxs-lookup"><span data-stu-id="9519d-109">The following types of policies are analyzed by the configuration analyzer:</span></span>

- <span data-ttu-id="9519d-110">**Stratégies Exchange Online Protection (EOP)**: cela inclut les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online et les organisations EOP autonomes sans boîtes aux lettres Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="9519d-110">**Exchange Online Protection (EOP) policies**: This includes Microsoft 365 organizations with Exchange Online mailboxes and standalone EOP organizations without Exchange Online mailboxes:</span></span>

  - <span data-ttu-id="9519d-111">[Stratégies anti-courrier indésirable.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="9519d-111">[Anti-spam policies](configure-your-spam-filter-policies.md).</span></span>
  - <span data-ttu-id="9519d-112">[Stratégies anti-programme malveillant.](configure-anti-malware-policies.md)</span><span class="sxs-lookup"><span data-stu-id="9519d-112">[Anti-malware policies](configure-anti-malware-policies.md).</span></span>
  - <span data-ttu-id="9519d-113">[Stratégies anti-hameçonnage EOP](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="9519d-113">[EOP Anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

- <span data-ttu-id="9519d-114">**Stratégies de Microsoft Defender pour Office 365**: cela inclut les organisations 365 E5 ou Defender pour les abonnements de modules office 365 :</span><span class="sxs-lookup"><span data-stu-id="9519d-114">**Microsoft Defender for Office 365 policies**: This includes organizations with Microsoft 365 E5 or Defender for Office 365 add-on subscriptions:</span></span>

  - <span data-ttu-id="9519d-115">Stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, qui incluent :</span><span class="sxs-lookup"><span data-stu-id="9519d-115">Anti-phishing policies in Microsoft Defender for Office 365, which include:</span></span>

    - <span data-ttu-id="9519d-116">Paramètres [d’usurpation disponibles](set-up-anti-phishing-policies.md#spoof-settings) dans les stratégies anti-hameçonnage EOP.</span><span class="sxs-lookup"><span data-stu-id="9519d-116">The same [spoof settings](set-up-anti-phishing-policies.md#spoof-settings) that are available in the EOP anti-phishing policies.</span></span>
    - [<span data-ttu-id="9519d-117">Paramètres d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="9519d-117">Impersonation settings</span></span>](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)
    - [<span data-ttu-id="9519d-118">Seuils de hameçonnage avancés</span><span class="sxs-lookup"><span data-stu-id="9519d-118">Advanced phishing thresholds</span></span>](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365)

  - <span data-ttu-id="9519d-119">[Stratégies de liens sécurisés](set-up-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9519d-119">[Safe Links policies](set-up-safe-links-policies.md).</span></span>

  - <span data-ttu-id="9519d-120">[Stratégies de pièces jointes sécurisées](set-up-safe-attachments-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9519d-120">[Safe Attachments policies](set-up-safe-attachments-policies.md).</span></span>

<span data-ttu-id="9519d-121">Les **valeurs de** paramètre de stratégie Standard et **Strict** utilisées comme lignes de base sont décrites dans les paramètres recommandés pour EOP et Microsoft Defender pour la sécurité [Office 365.](recommended-settings-for-eop-and-office365.md)</span><span class="sxs-lookup"><span data-stu-id="9519d-121">The **Standard** and **Strict** policy setting values that are used as baselines are described in [Recommended settings for EOP and Microsoft Defender for Office 365 security](recommended-settings-for-eop-and-office365.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9519d-122">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9519d-122">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9519d-123">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="9519d-123">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="9519d-124">Pour aller directement à la page de **l’analyseur de configuration,** utilisez <https://protection.office.com/configurationAnalyzer> .</span><span class="sxs-lookup"><span data-stu-id="9519d-124">To go directly to the **Configuration analyzer** page, use <https://protection.office.com/configurationAnalyzer>.</span></span>

- <span data-ttu-id="9519d-125">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="9519d-125">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="9519d-126">Des autorisations doivent vous avoir été attribuées dans le Centre de sécurité et de conformité pour que vous puissiez effectuer les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9519d-126">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="9519d-127">Pour utiliser l’analyseur de configuration et mettre à jour les  stratégies de sécurité, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="9519d-127">To use the configuration analyzer **and** make updates to security policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="9519d-128">Pour un accès en lecture seule à l’analyseur  de configuration, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="9519d-128">For read-only access to the configuration analyzer, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="9519d-129">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9519d-129">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  > [!NOTE]
  >  
  > - <span data-ttu-id="9519d-130">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9519d-130">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="9519d-131">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9519d-131">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  >
  > - <span data-ttu-id="9519d-132">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9519d-132">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-configuration-analyzer-in-the-security--compliance-center"></a><span data-ttu-id="9519d-133">Utiliser l’analyseur de configuration dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="9519d-133">Use the configuration analyzer in the Security & Compliance Center</span></span>

<span data-ttu-id="9519d-134">Dans le Centre de sécurité &  conformité, allez à l’analyseur de configuration des stratégies \>  \> **de gestion des menaces.**</span><span class="sxs-lookup"><span data-stu-id="9519d-134">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Configuration analyzer**.</span></span>

![Widget de l’analyseur de configuration dans la page Stratégie de gestion \> des menaces](../../media/configuration-analyzer-widget.png)

<span data-ttu-id="9519d-136">L’analyseur de configuration possède deux onglets principaux :</span><span class="sxs-lookup"><span data-stu-id="9519d-136">The configuration analyzer has two main tabs:</span></span>

- <span data-ttu-id="9519d-137">**Paramètres et recommandations**: vous choisissez Standard ou Strict et comparez ces paramètres à vos stratégies de sécurité existantes.</span><span class="sxs-lookup"><span data-stu-id="9519d-137">**Settings and recommendations**: You pick Standard or Strict and compare those settings to your existing security policies.</span></span> <span data-ttu-id="9519d-138">Dans les résultats, vous pouvez ajuster les valeurs de vos paramètres pour les faire monter au même niveau que Standard ou Strict.</span><span class="sxs-lookup"><span data-stu-id="9519d-138">In the results, you can adjust the values of your settings to bring them up to the same level as Standard or Strict.</span></span>

- <span data-ttu-id="9519d-139">**Analyse et historique de dérive de configuration**: cet affichage vous permet de suivre les modifications de stratégie au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9519d-139">**Configuration drift analysis and history**: This view allows you to track policy changes over time.</span></span>

### <a name="setting-and-recommendations-tab-in-the-configuration-analyzer"></a><span data-ttu-id="9519d-140">Onglet Paramètres et recommandations dans l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="9519d-140">Setting and recommendations tab in the configuration analyzer</span></span>

<span data-ttu-id="9519d-141">Par défaut, l’onglet s’ouvre dans la comparaison au profil de protection standard.</span><span class="sxs-lookup"><span data-stu-id="9519d-141">By default, the tab opens on the comparison to the Standard protection profile.</span></span> <span data-ttu-id="9519d-142">Vous pouvez basculer vers la comparaison du profil De protection stricte en cliquant sur **Afficher les recommandations strictes.**</span><span class="sxs-lookup"><span data-stu-id="9519d-142">You can switch to the comparison of the Strict protection profile by clicking **View Strict recommendations**.</span></span> <span data-ttu-id="9519d-143">Pour revenir en arrière, **sélectionnez Afficher les recommandations standard.**</span><span class="sxs-lookup"><span data-stu-id="9519d-143">To switch back, select **View Standard recommendations**.</span></span>

![Affichage des paramètres et des recommandations dans l’analyseur de configuration](../../media/configuration-analyzer-settings-and-recommendations-view.png)

<span data-ttu-id="9519d-145">Par défaut, la colonne Nom de **groupe/paramètre** de stratégie contient une vue d’ensemble des différents types de stratégies de sécurité et du nombre de paramètres qui doivent être améliorés (le cas nécessaire).</span><span class="sxs-lookup"><span data-stu-id="9519d-145">By default, the **Policy group/setting name** column contains a collapsed view of the different types of security policies and the number of settings that need improvement (if any).</span></span> <span data-ttu-id="9519d-146">Les types de stratégies sont :</span><span class="sxs-lookup"><span data-stu-id="9519d-146">The types of policies are:</span></span>

- <span data-ttu-id="9519d-147">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="9519d-147">**Anti-spam**</span></span>
- <span data-ttu-id="9519d-148">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="9519d-148">**Anti-phishing**</span></span>
- <span data-ttu-id="9519d-149">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="9519d-149">**Anti-malware**</span></span>
- <span data-ttu-id="9519d-150">**Pièces jointes sécurisées ATP** (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="9519d-150">**ATP Safe Attachments** (if your subscription includes Microsoft Defender for Office 365)</span></span>
- <span data-ttu-id="9519d-151">**Liens sécurisés ATP** (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="9519d-151">**ATP Safe Links** (if your subscription includes Microsoft Defender for Office 365)</span></span>

<span data-ttu-id="9519d-152">Dans l’affichage par défaut, tout est réduire.</span><span class="sxs-lookup"><span data-stu-id="9519d-152">In the default view, everything is collapsed.</span></span> <span data-ttu-id="9519d-153">En regard de chaque stratégie, il existe un résumé des résultats de comparaison de vos stratégies (que vous pouvez modifier) et des paramètres dans les stratégies correspondantes pour les profils de protection Standard ou Strict (que vous ne pouvez pas modifier).</span><span class="sxs-lookup"><span data-stu-id="9519d-153">Next to each policy, there's a summary of comparison results from your policies (which you can modify) and the settings in the corresponding policies for the Standard or Strict protection profiles (which you can't modify).</span></span> <span data-ttu-id="9519d-154">Vous verrez les informations suivantes pour le profil de protection que vous comparez :</span><span class="sxs-lookup"><span data-stu-id="9519d-154">You'll see the following information for the protection profile that you're comparing to:</span></span>

- <span data-ttu-id="9519d-155">**Vert**: tous les paramètres de toutes les stratégies existantes sont au moins aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="9519d-155">**Green**: All settings in all existing policies are at least as secure as the protection profile.</span></span>
- <span data-ttu-id="9519d-156">**Orange**: un petit nombre de paramètres dans les stratégies existantes ne sont pas aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="9519d-156">**Amber**: A small number of settings in the existing policies are not as secure as the protection profile.</span></span>
- <span data-ttu-id="9519d-157">**Rouge**: un nombre important de paramètres dans les stratégies existantes ne sont pas aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="9519d-157">**Red**: A significant number of settings in the existing policies are not as secure as the protection profile.</span></span> <span data-ttu-id="9519d-158">Il peut s’agit de quelques paramètres dans de nombreuses stratégies ou de nombreux paramètres dans une stratégie.</span><span class="sxs-lookup"><span data-stu-id="9519d-158">This could be a few settings in many policies or many settings in one policy.</span></span>

<span data-ttu-id="9519d-159">Pour des comparaisons favorables, vous verrez le texte : Tous les **paramètres suivent** \<**Standard** or **Strict**\> **les recommandations.**</span><span class="sxs-lookup"><span data-stu-id="9519d-159">For favorable comparisons, you'll see the text: **All settings follow** \<**Standard** or **Strict**\> **recommendations**.</span></span> <span data-ttu-id="9519d-160">Dans le cas contraire, vous verrez le nombre de paramètres recommandés à modifier.</span><span class="sxs-lookup"><span data-stu-id="9519d-160">Otherwise, you'll see the number of recommended settings to change.</span></span>

<span data-ttu-id="9519d-161">Si vous développez **le nom du groupe/paramètre** de stratégie, toutes les stratégies et les paramètres associés dans chaque stratégie spécifique nécessitant une attention particulière sont révélés.</span><span class="sxs-lookup"><span data-stu-id="9519d-161">If you expand **Policy group/setting name**, all of the policies and the associated settings in each specific policy that require attention are revealed.</span></span> <span data-ttu-id="9519d-162">Vous pouvez également développer un type spécifique de stratégie (par exemple, **anti-courrier** indésirable) pour voir uniquement ces paramètres dans les types de stratégies qui nécessitent votre attention.</span><span class="sxs-lookup"><span data-stu-id="9519d-162">Or, you can expand a specific type of policy (for example, **Anti-spam**) to see just those settings in those types of policies that require your attention.</span></span>

<span data-ttu-id="9519d-163">Si la comparaison n’a aucune recommandation d’amélioration (vert), l’extension de la stratégie ne révèle rien.</span><span class="sxs-lookup"><span data-stu-id="9519d-163">If the comparison has no recommendations for improvement (green), expanding the policy reveals nothing.</span></span> <span data-ttu-id="9519d-164">S’il existe un certain nombre de recommandations d’amélioration (orange ou rouge), les paramètres qui nécessitent une attention particulière sont révélés et les informations correspondantes sont révélées dans les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9519d-164">If there are any number of recommendations for improvement (amber or red), the settings that require attention are revealed, and corresponding information is revealed in the following columns:</span></span>

- <span data-ttu-id="9519d-165">Nom du paramètre qui nécessite votre attention.</span><span class="sxs-lookup"><span data-stu-id="9519d-165">The name of the setting that requires your attention.</span></span> <span data-ttu-id="9519d-166">Par exemple, dans la capture d’écran précédente, il s’agit du seuil de courrier en masse **dans** une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="9519d-166">For example, in the previous screenshot, it's the **Bulk email threshold** in an anti-spam policy.</span></span>

- <span data-ttu-id="9519d-167">**Stratégie**: nom de la stratégie concernée qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="9519d-167">**Policy**: The name of the affected policy that contains the setting.</span></span>

- <span data-ttu-id="9519d-168">**Appliqué à**: nombre d’utilisateurs à qui les stratégies affectées sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="9519d-168">**Applied to**: The number of users that the affected policies are applied to.</span></span>

- <span data-ttu-id="9519d-169">**Configuration actuelle**: valeur actuelle du paramètre.</span><span class="sxs-lookup"><span data-stu-id="9519d-169">**Current configuration**: The current value of the setting.</span></span>

- <span data-ttu-id="9519d-170">**Dernière modification**: date de la dernière modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9519d-170">**Last modified**: The date that the policy was last modified.</span></span>

- <span data-ttu-id="9519d-171">**Recommandations**: valeur du paramètre dans le profil de protection Standard ou Strict.</span><span class="sxs-lookup"><span data-stu-id="9519d-171">**Recommendations**: The value of the setting in the Standard or Strict protection profile.</span></span> <span data-ttu-id="9519d-172">Pour modifier la valeur du paramètre dans votre stratégie afin qu’elle corresponde à la valeur recommandée dans le profil de protection, cliquez sur **Adopter**.</span><span class="sxs-lookup"><span data-stu-id="9519d-172">To change the value of the setting in your policy to match the recommended value in the protection profile, click **Adopt**.</span></span> <span data-ttu-id="9519d-173">Si la modification réussit, vous verrez le message : **Recommandations correctement adoptées.**</span><span class="sxs-lookup"><span data-stu-id="9519d-173">If the change is successful, you'll see the message: **Recommendations successfully adopted**.</span></span> <span data-ttu-id="9519d-174">Cliquez **sur Actualiser** pour voir le nombre réduit de recommandations et la suppression de la ligne de paramètre/stratégie spécifique des résultats.</span><span class="sxs-lookup"><span data-stu-id="9519d-174">Click **Refresh** to see the reduced number of recommendations, and the removal of the specific setting/policy row from the results.</span></span>

### <a name="configuration-drift-analysis-and-history-tab-in-the-configuration-analyzer"></a><span data-ttu-id="9519d-175">Analyse de dérive de configuration et onglet Historique dans l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="9519d-175">Configuration drift analysis and history tab in the configuration analyzer</span></span>

<span data-ttu-id="9519d-176">Cet onglet vous permet de suivre les modifications que vous avez apportées à vos stratégies de sécurité personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9519d-176">This tab allows you to track the changes that you've made to your custom security policies.</span></span> <span data-ttu-id="9519d-177">Par défaut, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="9519d-177">By default, the following information is displayed:</span></span>

- <span data-ttu-id="9519d-178">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="9519d-178">**Last modified**</span></span>
- <span data-ttu-id="9519d-179">**Modifié par**</span><span class="sxs-lookup"><span data-stu-id="9519d-179">**Modified by**</span></span>
- <span data-ttu-id="9519d-180">**Nom du paramètre**</span><span class="sxs-lookup"><span data-stu-id="9519d-180">**Setting Name**</span></span>
- <span data-ttu-id="9519d-181">**Policy**</span><span class="sxs-lookup"><span data-stu-id="9519d-181">**Policy**</span></span>
- <span data-ttu-id="9519d-182">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="9519d-182">**Type**</span></span>

<span data-ttu-id="9519d-183">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="9519d-183">To filter the results, click **Filter**.</span></span> <span data-ttu-id="9519d-184">Dans le volant **Filtres** qui s’affiche, vous pouvez choisir parmi les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9519d-184">In the **Filters** flyout that appears, you can select from the following filters:</span></span>

- <span data-ttu-id="9519d-185">**Heure de début** **et heure de fin** (date)</span><span class="sxs-lookup"><span data-stu-id="9519d-185">**Start time** and **End time** (date)</span></span>
- <span data-ttu-id="9519d-186">**Protection standard** ou **protection stricte**</span><span class="sxs-lookup"><span data-stu-id="9519d-186">**Standard protection** or **Strict protection**</span></span>

<span data-ttu-id="9519d-187">Pour exporter les résultats dans un fichier .csv, cliquez sur **Exporter.**</span><span class="sxs-lookup"><span data-stu-id="9519d-187">To export the results to a .csv file, click **Export**.</span></span>

![Analyse de dérive de configuration et affichage historique dans l’analyseur de configuration](../../media/configuration-analyzer-configuration-drift-analysis-view.png)