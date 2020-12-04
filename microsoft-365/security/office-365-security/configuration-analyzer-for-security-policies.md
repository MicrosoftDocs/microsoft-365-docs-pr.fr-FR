---
title: Configuration Analyzer pour les stratégies de sécurité
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: ''
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser l’analyseur de configuration pour rechercher et corriger des stratégies de sécurité qui sont inférieures aux stratégies de sécurité standard protection et protection stricte.
ms.openlocfilehash: 7d02a6f83ceb06eb56039b449890fd90712c76e5
ms.sourcegitcommit: d81c7cea85af6ad5fef81d3c930514a51464368c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2020
ms.locfileid: "49572536"
---
# <a name="configuration-analyzer-for-protection-policies-in-eop-and-microsoft-defender-for-office-365"></a><span data-ttu-id="35c00-103">Configuration Analyzer pour les stratégies de protection dans EOP et Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="35c00-103">Configuration analyzer for protection policies in EOP and Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> <span data-ttu-id="35c00-104">Les fonctionnalités décrites dans cette rubrique sont en aperçu, ne sont pas disponibles dans toutes les organisations et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="35c00-104">The features described in this topic are in Preview, aren't available in all organizations, and are subject to change.</span></span> <span data-ttu-id="35c00-105">Pour plus d’informations sur le calendrier des publications, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=config%2Canalyzer).</span><span class="sxs-lookup"><span data-stu-id="35c00-105">For information about the release schedule, check out the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=config%2Canalyzer).</span></span>

<span data-ttu-id="35c00-106">Configuration Analyzer dans le centre de sécurité & conformité fournit un emplacement central pour rechercher et corriger les stratégies de sécurité lorsque les paramètres sont sous les paramètres de protection standard et de profil de protection stricte dans les [stratégies de sécurité prédéfinies](preset-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-106">Configuration analyzer in the Security & Compliance center provides a central location to find and fix security policies where the settings are below the Standard protection and Strict protection profile settings in [preset security policies](preset-security-policies.md).</span></span>

<span data-ttu-id="35c00-107">Les types de stratégies suivants sont analysés par l’analyseur de configuration :</span><span class="sxs-lookup"><span data-stu-id="35c00-107">The following types of policies are analyzed by the configuration analyzer:</span></span>

- <span data-ttu-id="35c00-108">**Stratégies Exchange Online Protection (EoP)**: cela inclut les organisations Microsoft 365 avec les boîtes aux lettres Exchange Online et les organisations EOP autonomes sans boîtes aux lettres Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="35c00-108">**Exchange Online Protection (EOP) policies**: This includes Microsoft 365 organizations with Exchange Online mailboxes and standalone EOP organizations without Exchange Online mailboxes:</span></span>
  
  - <span data-ttu-id="35c00-109">[Stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-109">[Anti-spam policies](configure-your-spam-filter-policies.md).</span></span>
  - <span data-ttu-id="35c00-110">[Stratégies de protection contre les programmes malveillants](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-110">[Anti-malware policies](configure-anti-malware-policies.md).</span></span>
  - <span data-ttu-id="35c00-111">[Stratégies de hameçonnage d’EOP](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="35c00-111">[EOP Anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

- <span data-ttu-id="35c00-112">**Stratégies Microsoft Defender pour office 365**: cela inclut les organisations avec Microsoft 365 E5 ou Defender pour Office 365 abonnements complémentaires :</span><span class="sxs-lookup"><span data-stu-id="35c00-112">**Microsoft Defender for Office 365 policies**: This includes organizations with Microsoft 365 E5 or Defender for Office 365 add-on subscriptions:</span></span>

  - <span data-ttu-id="35c00-113">Les stratégies anti-hameçonnage dans Microsoft Defender pour Office 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="35c00-113">Anti-phishing policies in Microsoft Defender for Office 365, which include:</span></span>

    - <span data-ttu-id="35c00-114">Les mêmes [paramètres d’usurpation](set-up-anti-phishing-policies.md#spoof-settings) qui sont disponibles dans les stratégies anti-hameçonnage EOP.</span><span class="sxs-lookup"><span data-stu-id="35c00-114">The same [spoof settings](set-up-anti-phishing-policies.md#spoof-settings) that are available in the EOP anti-phishing policies.</span></span>
    - [<span data-ttu-id="35c00-115">Paramètres d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="35c00-115">Impersonation settings</span></span>](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)
    - [<span data-ttu-id="35c00-116">Seuils de hameçonnage avancés</span><span class="sxs-lookup"><span data-stu-id="35c00-116">Advanced phishing thresholds</span></span>](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-anti-phishing-policies-in-microsoft-defender-for-office-365)

  - <span data-ttu-id="35c00-117">[Stratégies de liens fiables](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-117">[Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>

  - <span data-ttu-id="35c00-118">[Stratégies de pièces jointes approuvées](set-up-atp-safe-attachments-policies.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-118">[Safe Attachments policies](set-up-atp-safe-attachments-policies.md).</span></span>

<span data-ttu-id="35c00-119">Les valeurs de paramètres de stratégie **standard** et **strictes** utilisées comme configurations de référence sont décrites dans [paramètres recommandés pour EOP et Microsoft Defender for Office 365 Security](recommended-settings-for-eop-and-office365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-119">The **Standard** and **Strict** policy setting values that are used as baselines are described in [Recommended settings for EOP and Microsoft Defender for Office 365 security](recommended-settings-for-eop-and-office365-atp.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="35c00-120">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="35c00-120">What do you need to know before you begin?</span></span>

- <span data-ttu-id="35c00-121">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="35c00-121">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="35c00-122">Pour accéder directement à la page de l' **Analyseur de configuration** , utilisez <https://protection.office.com/configurationAnalyzer> .</span><span class="sxs-lookup"><span data-stu-id="35c00-122">To go directly to the **Configuration analyzer** page, use <https://protection.office.com/configurationAnalyzer>.</span></span>

- <span data-ttu-id="35c00-123">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="35c00-123">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="35c00-124">Avant de pouvoir effectuer les procédures décrites dans cet article, vous devez disposer d’autorisations dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="35c00-124">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="35c00-125">Pour utiliser l’analyseur de configuration **et** mettre à jour les stratégies de sécurité, vous devez être membre des groupes de rôles de gestion de l' **organisation** ou d' **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="35c00-125">To use the configuration analyzer **and** make updates to security policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="35c00-126">Pour un accès en lecture seule à Configuration Analyzer, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="35c00-126">For read-only access to the configuration analyzer, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="35c00-127">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="35c00-127">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="35c00-128">**Remarques**:</span><span class="sxs-lookup"><span data-stu-id="35c00-128">**Notes**:</span></span>

  - <span data-ttu-id="35c00-129">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le centre d’administration 365 de Microsoft donne aux utilisateurs les autorisations requises dans le centre de sécurité & conformité _et_ des autorisations pour d’autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="35c00-129">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="35c00-130">Si vous souhaitez en savoir plus, veuillez consulter la page [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="35c00-130">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="35c00-131">Le groupe de rôles gestion de l' **Organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) offre également un accès en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="35c00-131">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

## <a name="use-the-configuration-analyzer-in-the-security--compliance-center"></a><span data-ttu-id="35c00-132">Utiliser l’analyseur de configuration dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="35c00-132">Use the configuration analyzer in the Security & Compliance Center</span></span>

<span data-ttu-id="35c00-133">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Policy** \> **Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="35c00-133">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Configuration analyzer**.</span></span>

![Widget Configuration Analyzer sur la page de stratégie de gestion des menaces \>](../../media/configuration-analyzer-widget.png)

<span data-ttu-id="35c00-135">L’analyseur de configuration comporte deux onglets principaux :</span><span class="sxs-lookup"><span data-stu-id="35c00-135">The configuration analyzer has two main tabs:</span></span>

- <span data-ttu-id="35c00-136">**Paramètres et recommandations**: sélectionnez standard ou strict et Comparez ces paramètres à vos stratégies de sécurité existantes.</span><span class="sxs-lookup"><span data-stu-id="35c00-136">**Settings and recommendations**: You pick Standard or Strict and compare those settings to your existing security policies.</span></span> <span data-ttu-id="35c00-137">Dans les résultats, vous pouvez ajuster les valeurs de vos paramètres pour les ramener au même niveau que standard ou strict.</span><span class="sxs-lookup"><span data-stu-id="35c00-137">In the results, you can adjust the values of your settings to bring them up to the same level as Standard or Strict.</span></span>

- <span data-ttu-id="35c00-138">**Analyse de la dérive de la configuration et historique**: cette vue vous permet d’effectuer le suivi des modifications de stratégie au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="35c00-138">**Configuration drift analysis and history**: This view allows you to track policy changes over time.</span></span>

### <a name="setting-and-recommendations-tab-in-the-configuration-analyzer"></a><span data-ttu-id="35c00-139">Onglet définition et recommandations de l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="35c00-139">Setting and recommendations tab in the configuration analyzer</span></span>

<span data-ttu-id="35c00-140">Par défaut, l’onglet s’ouvre sur la comparaison avec le profil de protection standard.</span><span class="sxs-lookup"><span data-stu-id="35c00-140">By default, the tab opens on the comparison to the Standard protection profile.</span></span> <span data-ttu-id="35c00-141">Vous pouvez passer à la comparaison du profil de protection strict en cliquant sur **Afficher rigoureuse Recommendations**.</span><span class="sxs-lookup"><span data-stu-id="35c00-141">You can switch to the comparison of the Strict protection profile by clicking **View Strict recommendations**.</span></span> <span data-ttu-id="35c00-142">Pour revenir en arrière, sélectionnez **afficher les recommandations standard**.</span><span class="sxs-lookup"><span data-stu-id="35c00-142">To switch back, select **View Standard recommendations**.</span></span>

![Vue paramètres et recommandations dans l’analyseur de configuration](../../media/configuration-analyzer-settings-and-recommendations-view.png)

<span data-ttu-id="35c00-144">Par défaut, la colonne **groupe de stratégies/nom du paramètre** contient une vue réduite des différents types de stratégies de sécurité et le nombre de paramètres qui doivent être améliorés (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="35c00-144">By default, the **Policy group/setting name** column contains a collapsed view of the different types of security policies and the number of settings that need improvement (if any).</span></span> <span data-ttu-id="35c00-145">Les types de stratégies sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="35c00-145">The types of policies are:</span></span>

- <span data-ttu-id="35c00-146">**Blocage du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="35c00-146">**Anti-spam**</span></span>
- <span data-ttu-id="35c00-147">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="35c00-147">**Anti-phishing**</span></span>
- <span data-ttu-id="35c00-148">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="35c00-148">**Anti-malware**</span></span>
- <span data-ttu-id="35c00-149">**Pièces jointes sécurisées** pour la protection avancée contre les menaces (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="35c00-149">**ATP Safe Attachments** (if your subscription includes Microsoft Defender for Office 365)</span></span>
- <span data-ttu-id="35c00-150">**Liens fiables ATP** (si votre abonnement inclut Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="35c00-150">**ATP Safe Links** (if your subscription includes Microsoft Defender for Office 365)</span></span>

<span data-ttu-id="35c00-151">Dans l’affichage par défaut, tout est réduit.</span><span class="sxs-lookup"><span data-stu-id="35c00-151">In the default view, everything is collapsed.</span></span> <span data-ttu-id="35c00-152">En regard de chaque stratégie, il existe un résumé des résultats de la comparaison de vos stratégies (que vous pouvez modifier) et les paramètres des stratégies correspondantes pour les profils de protection standard ou stricte (que vous ne pouvez pas modifier).</span><span class="sxs-lookup"><span data-stu-id="35c00-152">Next to each policy, there's a summary of comparison results from your policies (which you can modify) and the settings in the corresponding policies for the Standard or Strict protection profiles (which you can't modify).</span></span> <span data-ttu-id="35c00-153">Les informations suivantes s’affichent pour le profil de protection que vous comparez :</span><span class="sxs-lookup"><span data-stu-id="35c00-153">You'll see the following information for the protection profile that you're comparing to:</span></span>

- <span data-ttu-id="35c00-154">**Vert**: tous les paramètres de toutes les stratégies existantes sont au moins aussi sécurisés que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="35c00-154">**Green**: All settings in all existing policies are at least as secure as the protection profile.</span></span>
- <span data-ttu-id="35c00-155">**Orange**: un petit nombre de paramètres dans les stratégies existantes n’est pas aussi sécurisé que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="35c00-155">**Amber**: A small number of settings in the existing policies are not as secure as the protection profile.</span></span>
- <span data-ttu-id="35c00-156">**Rouge**: un nombre significatif de paramètres dans les stratégies existantes n’est pas aussi sécurisé que le profil de protection.</span><span class="sxs-lookup"><span data-stu-id="35c00-156">**Red**: A significant number of settings in the existing policies are not as secure as the protection profile.</span></span> <span data-ttu-id="35c00-157">Il peut s’agir de quelques paramètres dans de nombreuses stratégies ou de nombreux paramètres dans une stratégie.</span><span class="sxs-lookup"><span data-stu-id="35c00-157">This could be a few settings in many policies or many settings in one policy.</span></span>

<span data-ttu-id="35c00-158">Pour les comparaisons favorables, vous verrez le texte : **tous les paramètres suivent** les \<**Standard** or **Strict**\> **recommandations**.</span><span class="sxs-lookup"><span data-stu-id="35c00-158">For favorable comparisons, you'll see the text: **All settings follow** \<**Standard** or **Strict**\> **recommendations**.</span></span> <span data-ttu-id="35c00-159">Dans le cas contraire, vous verrez le nombre de paramètres recommandés à modifier.</span><span class="sxs-lookup"><span data-stu-id="35c00-159">Otherwise, you'll see the number of recommended settings to change.</span></span>

<span data-ttu-id="35c00-160">Si vous développez le **nom du groupe de stratégies/du paramètre**, toutes les stratégies et les paramètres associés dans chaque stratégie spécifique nécessitant une attention sont révélés.</span><span class="sxs-lookup"><span data-stu-id="35c00-160">If you expand **Policy group/setting name**, all of the policies and the associated settings in each specific policy that require attention are revealed.</span></span> <span data-ttu-id="35c00-161">Vous pouvez également développer un type spécifique de stratégie (par exemple, le **blocage du courrier indésirable**) pour afficher uniquement ces paramètres dans ces types de stratégies qui nécessitent votre attention.</span><span class="sxs-lookup"><span data-stu-id="35c00-161">Or, you can expand a specific type of policy (for example, **Anti-spam**) to see just those settings in those types of policies that require your attention.</span></span>

<span data-ttu-id="35c00-162">Si la comparaison n’a pas de recommandations d’amélioration (en vert), le développement de la stratégie n’indique rien.</span><span class="sxs-lookup"><span data-stu-id="35c00-162">If the comparison has no recommendations for improvement (green), expanding the policy reveals nothing.</span></span> <span data-ttu-id="35c00-163">S’il existe un nombre de recommandations pour l’amélioration (jaune ou rouge), les paramètres nécessitant une attention sont révélés, et les informations correspondantes sont révélées dans les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="35c00-163">If there are any number of recommendations for improvement (amber or red), the settings that require attention are revealed, and corresponding information is revealed in the following columns:</span></span>

- <span data-ttu-id="35c00-164">Nom du paramètre qui requiert votre attention.</span><span class="sxs-lookup"><span data-stu-id="35c00-164">The name of the setting that requires your attention.</span></span> <span data-ttu-id="35c00-165">Par exemple, dans la capture d’écran précédente, il s’agit du **seuil de courrier électronique en bloc** dans une stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="35c00-165">For example, in the previous screenshot, it's the **Bulk email threshold** in an anti-spam policy.</span></span>

- <span data-ttu-id="35c00-166">**Stratégie**: nom de la stratégie concernée qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="35c00-166">**Policy**: The name of the affected policy that contains the setting.</span></span>

- <span data-ttu-id="35c00-167">**Appliqué à**: nombre d’utilisateurs auxquels les stratégies affectées sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="35c00-167">**Applied to**: The number of users that the affected policies are applied to.</span></span>

- <span data-ttu-id="35c00-168">**Configuration actuelle**: valeur actuelle du paramètre.</span><span class="sxs-lookup"><span data-stu-id="35c00-168">**Current configuration**: The current value of the setting.</span></span>

- <span data-ttu-id="35c00-169">**Dernière modification**: date de la dernière modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="35c00-169">**Last modified**: The date that the policy was last modified.</span></span>

- <span data-ttu-id="35c00-170">**Recommandations**: valeur du paramètre dans le profil de protection standard ou strict.</span><span class="sxs-lookup"><span data-stu-id="35c00-170">**Recommendations**: The value of the setting in the Standard or Strict protection profile.</span></span> <span data-ttu-id="35c00-171">Pour modifier la valeur du paramètre dans votre stratégie pour qu’elle corresponde à la valeur recommandée dans le profil de protection, cliquez sur **adopter**.</span><span class="sxs-lookup"><span data-stu-id="35c00-171">To change the value of the setting in your policy to match the recommended value in the protection profile, click **Adopt**.</span></span> <span data-ttu-id="35c00-172">Si la modification réussit, vous verrez le message suivant : **recommandations correctement adoptées**.</span><span class="sxs-lookup"><span data-stu-id="35c00-172">If the change is successful, you'll see the message: **Recommendations successfully adopted**.</span></span> <span data-ttu-id="35c00-173">Cliquez sur **Actualiser** pour afficher le nombre réduit de recommandations, ainsi que la suppression de la ligne de paramètre/stratégie spécifique des résultats.</span><span class="sxs-lookup"><span data-stu-id="35c00-173">Click **Refresh** to see the reduced number of recommendations, and the removal of the specific setting/policy row from the results.</span></span>

### <a name="configuration-drift-analysis-and-history-tab-in-the-configuration-analyzer"></a><span data-ttu-id="35c00-174">Onglet analyse de dérive et historique de configuration de l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="35c00-174">Configuration drift analysis and history tab in the configuration analyzer</span></span>

<span data-ttu-id="35c00-175">Cet onglet vous permet de suivre les modifications que vous avez apportées à vos stratégies de sécurité personnalisées.</span><span class="sxs-lookup"><span data-stu-id="35c00-175">This tab allows you to track the changes that you've made to your custom security policies.</span></span> <span data-ttu-id="35c00-176">Par défaut, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="35c00-176">By default, the following information is displayed:</span></span>

- <span data-ttu-id="35c00-177">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="35c00-177">**Last modified**</span></span>
- <span data-ttu-id="35c00-178">**Modifié par**</span><span class="sxs-lookup"><span data-stu-id="35c00-178">**Modified by**</span></span>
- <span data-ttu-id="35c00-179">**Nom du paramètre**</span><span class="sxs-lookup"><span data-stu-id="35c00-179">**Setting Name**</span></span>
- <span data-ttu-id="35c00-180">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="35c00-180">**Policy**</span></span>
- <span data-ttu-id="35c00-181">**Type**</span><span class="sxs-lookup"><span data-stu-id="35c00-181">**Type**</span></span>

<span data-ttu-id="35c00-182">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="35c00-182">To filter the results, click **Filter**.</span></span> <span data-ttu-id="35c00-183">Dans le menu volant **filtres** qui s’affiche, vous pouvez sélectionner l’un des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="35c00-183">In the **Filters** flyout that appears, you can select from the following filters:</span></span>

- <span data-ttu-id="35c00-184">Heure de **début** et **heure de fin** (date)</span><span class="sxs-lookup"><span data-stu-id="35c00-184">**Start time** and **End time** (date)</span></span>
- <span data-ttu-id="35c00-185">**Protection standard** ou **protection stricte**</span><span class="sxs-lookup"><span data-stu-id="35c00-185">**Standard protection** or **Strict protection**</span></span>

<span data-ttu-id="35c00-186">Pour exporter les résultats dans un fichier. csv, cliquez sur **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="35c00-186">To export the results to a .csv file, click **Export**.</span></span>

![Analyse de dérive de configuration et vue historique dans l’analyseur de configuration](../../media/configuration-analyzer-configuration-drift-analysis-view.png)
