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
ms.openlocfilehash: 04027e78a2683c6c33954bb548c502497c5e8323
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029477"
---
# <a name="configuration-analyzer-for-protection-policies-in-eop-and-microsoft-defender-for-office-365"></a><span data-ttu-id="715d3-103">Analyseur de configuration des stratégies de protection dans EOP et Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="715d3-103">Configuration analyzer for protection policies in EOP and Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="715d3-104">L’analyseur de configuration dans le Centre de sécurité & conformité fournit un emplacement central pour rechercher et corriger [](preset-security-policies.md)les stratégies de sécurité où les paramètres se trouvent en dessous des paramètres de profil de protection standard et strict dans les stratégies de sécurité prédéfines.</span><span class="sxs-lookup"><span data-stu-id="715d3-104">Configuration analyzer in the Security & Compliance center provides a central location to find and fix security policies where the settings are below the Standard protection and Strict protection profile settings in [preset security policies](preset-security-policies.md).</span></span>

<span data-ttu-id="715d3-105">Les types de stratégies suivants sont analysés par l’analyseur de configuration :</span><span class="sxs-lookup"><span data-stu-id="715d3-105">The following types of policies are analyzed by the configuration analyzer:</span></span>

- <span data-ttu-id="715d3-106">**Stratégies Exchange Online Protection (EOP)**: cela inclut les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online et les organisations EOP autonomes sans boîtes aux lettres Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="715d3-106">**Exchange Online Protection (EOP) policies**: This includes Microsoft 365 organizations with Exchange Online mailboxes and standalone EOP organizations without Exchange Online mailboxes:</span></span>

  - <span data-ttu-id="715d3-107">[Stratégies anti-courrier indésirable.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="715d3-107">[Anti-spam policies](configure-your-spam-filter-policies.md).</span></span>
  - <span data-ttu-id="715d3-108">[Stratégies anti-programme malveillant.](configure-anti-malware-policies.md)</span><span class="sxs-lookup"><span data-stu-id="715d3-108">[Anti-malware policies](configure-anti-malware-policies.md).</span></span>
  - <span data-ttu-id="715d3-109">[Stratégies anti-hameçonnage EOP](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="715d3-109">[EOP Anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

- <span data-ttu-id="715d3-110">**Stratégies de Microsoft Defender pour Office 365**: cela inclut les organisations 365 E5 ou Defender pour les abonnements de modules office 365 :</span><span class="sxs-lookup"><span data-stu-id="715d3-110">**Microsoft Defender for Office 365 policies**: This includes organizations with Microsoft 365 E5 or Defender for Office 365 add-on subscriptions:</span></span>

  - <span data-ttu-id="715d3-111">Stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, qui incluent :</span><span class="sxs-lookup"><span data-stu-id="715d3-111">Anti-phishing policies in Microsoft Defender for Office 365, which include:</span></span>

    - <span data-ttu-id="715d3-112">Paramètres [d’usurpation disponibles](set-up-anti-phishing-policies.md#spoof-settings) dans les stratégies anti-hameçonnage EOP.</span><span class="sxs-lookup"><span data-stu-id="715d3-112">The same [spoof settings](set-up-anti-phishing-policies.md#spoof-settings) that are available in the EOP anti-phishing policies.</span></span>
    - [<span data-ttu-id="715d3-113">Paramètres d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="715d3-113">Impersonation settings</span></span>](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)
    - [<span data-ttu-id="715d3-114">Seuils de hameçonnage avancés</span><span class="sxs-lookup"><span data-stu-id="715d3-114">Advanced phishing thresholds</span></span>](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365)

  - <span data-ttu-id="715d3-115">[Stratégies de liens sécurisés](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="715d3-115">[Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>

  - <span data-ttu-id="715d3-116">[Stratégies de pièces jointes sécurisées](set-up-atp-safe-attachments-policies.md).</span><span class="sxs-lookup"><span data-stu-id="715d3-116">[Safe Attachments policies](set-up-atp-safe-attachments-policies.md).</span></span>

<span data-ttu-id="715d3-117">Les **valeurs de** paramètre de stratégie Standard et **Strict** utilisées comme lignes de base sont décrites dans les paramètres recommandés pour EOP et Microsoft Defender pour la sécurité [Office 365.](recommended-settings-for-eop-and-office365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="715d3-117">The **Standard** and **Strict** policy setting values that are used as baselines are described in [Recommended settings for EOP and Microsoft Defender for Office 365 security](recommended-settings-for-eop-and-office365-atp.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="715d3-118">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="715d3-118">What do you need to know before you begin?</span></span>

- <span data-ttu-id="715d3-119">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="715d3-119">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="715d3-120">Pour aller directement à la page de **l’analyseur de** configuration, utilisez <https://protection.office.com/configurationAnalyzer> .</span><span class="sxs-lookup"><span data-stu-id="715d3-120">To go directly to the **Configuration analyzer** page, use <https://protection.office.com/configurationAnalyzer>.</span></span>

- <span data-ttu-id="715d3-121">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="715d3-121">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="715d3-122">Des autorisations doivent vous avoir été attribuées dans le Centre de sécurité et de conformité pour que vous puissiez effectuer les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="715d3-122">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="715d3-123">Pour utiliser l’analyseur de configuration et mettre à jour les  stratégies de sécurité, vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité. </span><span class="sxs-lookup"><span data-stu-id="715d3-123">To use the configuration analyzer **and** make updates to security policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="715d3-124">Pour un accès en lecture seule à l’analyseur  de configuration, vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité. </span><span class="sxs-lookup"><span data-stu-id="715d3-124">For read-only access to the configuration analyzer, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="715d3-125">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="715d3-125">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  > [!NOTE]
  >  
  > - <span data-ttu-id="715d3-126">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="715d3-126">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="715d3-127">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="715d3-127">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  > 
  > - <span data-ttu-id="715d3-128">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="715d3-128">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-configuration-analyzer-in-the-security--compliance-center"></a><span data-ttu-id="715d3-129">Utiliser l’analyseur de configuration dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="715d3-129">Use the configuration analyzer in the Security & Compliance Center</span></span>

<span data-ttu-id="715d3-130">Dans le Centre de sécurité &  conformité, allez à l’analyseur de configuration des stratégies \>  \> **de gestion des menaces.**</span><span class="sxs-lookup"><span data-stu-id="715d3-130">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Configuration analyzer**.</span></span>

![Widget de l’analyseur de configuration dans la page Stratégie de gestion \> des menaces](../../media/configuration-analyzer-widget.png)

<span data-ttu-id="715d3-132">L’analyseur de configuration possède deux onglets principaux :</span><span class="sxs-lookup"><span data-stu-id="715d3-132">The configuration analyzer has two main tabs:</span></span>

- <span data-ttu-id="715d3-133">**Paramètres et recommandations**: vous choisissez Standard ou Strict et comparez ces paramètres à vos stratégies de sécurité existantes.</span><span class="sxs-lookup"><span data-stu-id="715d3-133">**Settings and recommendations**: You pick Standard or Strict and compare those settings to your existing security policies.</span></span> <span data-ttu-id="715d3-134">Dans les résultats, vous pouvez ajuster les valeurs de vos paramètres pour les faire monter au même niveau que Standard ou Strict.</span><span class="sxs-lookup"><span data-stu-id="715d3-134">In the results, you can adjust the values of your settings to bring them up to the same level as Standard or Strict.</span></span>

- <span data-ttu-id="715d3-135">**Analyse et historique de dérive de configuration**: cet affichage vous permet de suivre les modifications de stratégie au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="715d3-135">**Configuration drift analysis and history**: This view allows you to track policy changes over time.</span></span>

### <a name="setting-and-recommendations-tab-in-the-configuration-analyzer"></a><span data-ttu-id="715d3-136">Onglet Paramètres et recommandations dans l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="715d3-136">Setting and recommendations tab in the configuration analyzer</span></span>

<span data-ttu-id="715d3-137">Par défaut, l’onglet s’ouvre dans la comparaison au profil de protection standard.</span><span class="sxs-lookup"><span data-stu-id="715d3-137">By default, the tab opens on the comparison to the Standard protection profile.</span></span> <span data-ttu-id="715d3-138">Vous pouvez basculer vers la comparaison du profil De protection stricte en cliquant sur **Afficher les recommandations strictes.**</span><span class="sxs-lookup"><span data-stu-id="715d3-138">You can switch to the comparison of the Strict protection profile by clicking **View Strict recommendations**.</span></span> <span data-ttu-id="715d3-139">Pour revenir en arrière, **sélectionnez Afficher les recommandations standard.**</span><span class="sxs-lookup"><span data-stu-id="715d3-139">To switch back, select **View Standard recommendations**.</span></span>

![Affichage des paramètres et des recommandations dans l’analyseur de configuration](../../media/configuration-analyzer-settings-and-recommendations-view.png)

<span data-ttu-id="715d3-141">Par défaut, la colonne Nom du **groupe/paramètre** de stratégie contient une vue d’ensemble des différents types de stratégies de sécurité et du nombre de paramètres qui doivent être améliorés (le cas nécessaire).</span><span class="sxs-lookup"><span data-stu-id="715d3-141">By default, the **Policy group/setting name** column contains a collapsed view of the different types of security policies and the number of settings that need improvement (if any).</span></span> <span data-ttu-id="715d3-142">Les types de stratégies sont :</span><span class="sxs-lookup"><span data-stu-id="715d3-142">The types of policies are:</span></span>

- <span data-ttu-id="715d3-143">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="715d3-143">**Anti-spam**</span></span>
- <span data-ttu-id="715d3-144">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="715d3-144">**Anti-phishing**</span></span>
- <span data-ttu-id="715d3-145">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="715d3-145">**Anti-malware**</span></span>
- <span data-ttu-id="715d3-146">**Pièces jointes sécurisées ATP** (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="715d3-146">**ATP Safe Attachments** (if your subscription includes Microsoft Defender for Office 365)</span></span>
- <span data-ttu-id="715d3-147">**Liens sécurisés ATP** (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="715d3-147">**ATP Safe Links** (if your subscription includes Microsoft Defender for Office 365)</span></span>

<span data-ttu-id="715d3-148">Dans l’affichage par défaut, tout est réduire.</span><span class="sxs-lookup"><span data-stu-id="715d3-148">In the default view, everything is collapsed.</span></span> <span data-ttu-id="715d3-149">En regard de chaque stratégie, il existe un résumé des résultats de comparaison de vos stratégies (que vous pouvez modifier) et des paramètres dans les stratégies correspondantes pour les profils de protection Standard ou Strict (que vous ne pouvez pas modifier).</span><span class="sxs-lookup"><span data-stu-id="715d3-149">Next to each policy, there's a summary of comparison results from your policies (which you can modify) and the settings in the corresponding policies for the Standard or Strict protection profiles (which you can't modify).</span></span> <span data-ttu-id="715d3-150">Vous verrez les informations suivantes pour le profil de protection que vous comparez à :</span><span class="sxs-lookup"><span data-stu-id="715d3-150">You'll see the following information for the protection profile that you're comparing to:</span></span>

- <span data-ttu-id="715d3-151">**Vert**: tous les paramètres de toutes les stratégies existantes sont au moins aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="715d3-151">**Green**: All settings in all existing policies are at least as secure as the protection profile.</span></span>
- <span data-ttu-id="715d3-152">**Orange**: un petit nombre de paramètres dans les stratégies existantes ne sont pas aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="715d3-152">**Amber**: A small number of settings in the existing policies are not as secure as the protection profile.</span></span>
- <span data-ttu-id="715d3-153">**Rouge**: un nombre important de paramètres dans les stratégies existantes ne sont pas aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="715d3-153">**Red**: A significant number of settings in the existing policies are not as secure as the protection profile.</span></span> <span data-ttu-id="715d3-154">Il peut s’agit de quelques paramètres dans de nombreuses stratégies ou de nombreux paramètres dans une stratégie.</span><span class="sxs-lookup"><span data-stu-id="715d3-154">This could be a few settings in many policies or many settings in one policy.</span></span>

<span data-ttu-id="715d3-155">Pour des comparaisons favorables, vous verrez le texte : Tous les **paramètres suivent** \<**Standard** or **Strict**\> **les recommandations.**</span><span class="sxs-lookup"><span data-stu-id="715d3-155">For favorable comparisons, you'll see the text: **All settings follow** \<**Standard** or **Strict**\> **recommendations**.</span></span> <span data-ttu-id="715d3-156">Dans le cas contraire, vous verrez le nombre de paramètres recommandés à modifier.</span><span class="sxs-lookup"><span data-stu-id="715d3-156">Otherwise, you'll see the number of recommended settings to change.</span></span>

<span data-ttu-id="715d3-157">Si vous développez **le nom du groupe/paramètre** de stratégie, toutes les stratégies et les paramètres associés dans chaque stratégie spécifique nécessitant une attention particulière sont révélés.</span><span class="sxs-lookup"><span data-stu-id="715d3-157">If you expand **Policy group/setting name**, all of the policies and the associated settings in each specific policy that require attention are revealed.</span></span> <span data-ttu-id="715d3-158">Vous pouvez également développer un type spécifique de stratégie (par exemple, **anti-courrier** indésirable) pour voir uniquement ces paramètres dans les types de stratégies qui nécessitent votre attention.</span><span class="sxs-lookup"><span data-stu-id="715d3-158">Or, you can expand a specific type of policy (for example, **Anti-spam**) to see just those settings in those types of policies that require your attention.</span></span>

<span data-ttu-id="715d3-159">Si la comparaison n’a aucune recommandation d’amélioration (vert), l’extension de la stratégie ne révèle rien.</span><span class="sxs-lookup"><span data-stu-id="715d3-159">If the comparison has no recommendations for improvement (green), expanding the policy reveals nothing.</span></span> <span data-ttu-id="715d3-160">S’il existe un certain nombre de recommandations d’amélioration (orange ou rouge), les paramètres qui nécessitent une attention particulière sont révélés et les informations correspondantes sont révélées dans les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="715d3-160">If there are any number of recommendations for improvement (amber or red), the settings that require attention are revealed, and corresponding information is revealed in the following columns:</span></span>

- <span data-ttu-id="715d3-161">Nom du paramètre qui nécessite votre attention.</span><span class="sxs-lookup"><span data-stu-id="715d3-161">The name of the setting that requires your attention.</span></span> <span data-ttu-id="715d3-162">Par exemple, dans la capture d’écran précédente, il s’agit du seuil de courrier en masse **dans** une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="715d3-162">For example, in the previous screenshot, it's the **Bulk email threshold** in an anti-spam policy.</span></span>

- <span data-ttu-id="715d3-163">**Stratégie**: nom de la stratégie concernée qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="715d3-163">**Policy**: The name of the affected policy that contains the setting.</span></span>

- <span data-ttu-id="715d3-164">**Appliqué à**: nombre d’utilisateurs à qui les stratégies affectées sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="715d3-164">**Applied to**: The number of users that the affected policies are applied to.</span></span>

- <span data-ttu-id="715d3-165">**Configuration actuelle**: valeur actuelle du paramètre.</span><span class="sxs-lookup"><span data-stu-id="715d3-165">**Current configuration**: The current value of the setting.</span></span>

- <span data-ttu-id="715d3-166">**Dernière modification**: date de la dernière modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="715d3-166">**Last modified**: The date that the policy was last modified.</span></span>

- <span data-ttu-id="715d3-167">**Recommandations**: valeur du paramètre dans le profil de protection Standard ou Strict.</span><span class="sxs-lookup"><span data-stu-id="715d3-167">**Recommendations**: The value of the setting in the Standard or Strict protection profile.</span></span> <span data-ttu-id="715d3-168">Pour modifier la valeur du paramètre dans votre stratégie afin qu’elle corresponde à la valeur recommandée dans le profil de protection, cliquez sur **Adopter**.</span><span class="sxs-lookup"><span data-stu-id="715d3-168">To change the value of the setting in your policy to match the recommended value in the protection profile, click **Adopt**.</span></span> <span data-ttu-id="715d3-169">Si la modification réussit, vous verrez le message : **Recommandations correctement adoptées.**</span><span class="sxs-lookup"><span data-stu-id="715d3-169">If the change is successful, you'll see the message: **Recommendations successfully adopted**.</span></span> <span data-ttu-id="715d3-170">Cliquez **sur Actualiser** pour voir le nombre réduit de recommandations et la suppression de la ligne de paramètre/stratégie spécifique des résultats.</span><span class="sxs-lookup"><span data-stu-id="715d3-170">Click **Refresh** to see the reduced number of recommendations, and the removal of the specific setting/policy row from the results.</span></span>

### <a name="configuration-drift-analysis-and-history-tab-in-the-configuration-analyzer"></a><span data-ttu-id="715d3-171">Analyse de dérive de configuration et onglet Historique dans l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="715d3-171">Configuration drift analysis and history tab in the configuration analyzer</span></span>

<span data-ttu-id="715d3-172">Cet onglet vous permet de suivre les modifications que vous avez apportées à vos stratégies de sécurité personnalisées.</span><span class="sxs-lookup"><span data-stu-id="715d3-172">This tab allows you to track the changes that you've made to your custom security policies.</span></span> <span data-ttu-id="715d3-173">Par défaut, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="715d3-173">By default, the following information is displayed:</span></span>

- <span data-ttu-id="715d3-174">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="715d3-174">**Last modified**</span></span>
- <span data-ttu-id="715d3-175">**Modifié par**</span><span class="sxs-lookup"><span data-stu-id="715d3-175">**Modified by**</span></span>
- <span data-ttu-id="715d3-176">**Nom du paramètre**</span><span class="sxs-lookup"><span data-stu-id="715d3-176">**Setting Name**</span></span>
- <span data-ttu-id="715d3-177">**Policy**</span><span class="sxs-lookup"><span data-stu-id="715d3-177">**Policy**</span></span>
- <span data-ttu-id="715d3-178">**Type**</span><span class="sxs-lookup"><span data-stu-id="715d3-178">**Type**</span></span>

<span data-ttu-id="715d3-179">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="715d3-179">To filter the results, click **Filter**.</span></span> <span data-ttu-id="715d3-180">Dans le volant **Filtres** qui s’affiche, vous pouvez choisir parmi les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="715d3-180">In the **Filters** flyout that appears, you can select from the following filters:</span></span>

- <span data-ttu-id="715d3-181">**Heure de début** **et heure de fin** (date)</span><span class="sxs-lookup"><span data-stu-id="715d3-181">**Start time** and **End time** (date)</span></span>
- <span data-ttu-id="715d3-182">**Protection standard** ou **protection stricte**</span><span class="sxs-lookup"><span data-stu-id="715d3-182">**Standard protection** or **Strict protection**</span></span>

<span data-ttu-id="715d3-183">Pour exporter les résultats dans un fichier .csv, cliquez sur **Exporter.**</span><span class="sxs-lookup"><span data-stu-id="715d3-183">To export the results to a .csv file, click **Export**.</span></span>

![Analyse de dérive de configuration et affichage historique dans l’analyseur de configuration](../../media/configuration-analyzer-configuration-drift-analysis-view.png)
