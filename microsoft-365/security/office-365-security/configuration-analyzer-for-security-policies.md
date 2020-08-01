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
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à utiliser l’analyseur de configuration pour rechercher et corriger des stratégies de sécurité qui contiennent des paramètres inférieurs aux stratégies de sécurité standard protection prédéfinie protection et protection stricte.
ms.openlocfilehash: 259d498646ecf893a57a608a37e3b771083716cc
ms.sourcegitcommit: fab425ea4580d1924fb421e6db233d135f5b7d19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2020
ms.locfileid: "46533969"
---
# <a name="configuration-analyzer-for-protection-policies-in-eop-and-office-365-atp"></a><span data-ttu-id="280f8-103">Configuration Analyzer pour les stratégies de protection dans EOP et Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="280f8-103">Configuration analyzer for protection policies in EOP and Office 365 ATP</span></span>

> [!NOTE]
> <span data-ttu-id="280f8-104">Les fonctionnalités décrites dans cette rubrique sont en aperçu, ne sont pas disponibles dans toutes les organisations et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="280f8-104">The features described in this topic are in Preview, aren't available in all organizations, and are subject to change.</span></span>

<span data-ttu-id="280f8-105">Configuration Analyzer dans le centre de sécurité & conformité fournit un emplacement central pour rechercher et corriger toutes vos stratégies de sécurité qui contiennent des paramètres inférieurs aux paramètres de profil de protection standard et de profil de protection stricte dans les [stratégies de sécurité prédéfinies](preset-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-105">Configuration analyzer in the Security & Compliance center provides a central location to find and fix any of your security policies that contain settings that are below the Standard protection and Strict protection profile settings in [preset security policies](preset-security-policies.md).</span></span>

<span data-ttu-id="280f8-106">Les types de stratégies suivants sont analysés par l’analyseur de configuration :</span><span class="sxs-lookup"><span data-stu-id="280f8-106">The following types of policies are analyzed by the configuration analyzer:</span></span>

- <span data-ttu-id="280f8-107">**Stratégies Exchange Online Protection (EoP)**: cela inclut les organisations Microsoft 365 avec les boîtes aux lettres Exchange Online et les organisations EOP autonomes sans boîtes aux lettres Exchange Online :</span><span class="sxs-lookup"><span data-stu-id="280f8-107">**Exchange Online Protection (EOP) policies**: This includes Microsoft 365 organizations with Exchange Online mailboxes and standalone EOP organizations without Exchange Online mailboxes:</span></span>
  
  - <span data-ttu-id="280f8-108">[Stratégies de blocage du courrier indésirable](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-108">[Anti-spam policies](configure-your-spam-filter-policies.md).</span></span>
  - <span data-ttu-id="280f8-109">[Stratégies de protection contre les programmes malveillants](configure-anti-malware-policies.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-109">[Anti-malware policies](configure-anti-malware-policies.md).</span></span>
  - <span data-ttu-id="280f8-110">[Stratégies de hameçonnage d’EOP](set-up-anti-phishing-policies.md#spoof-settings).</span><span class="sxs-lookup"><span data-stu-id="280f8-110">[EOP Anti-phishing policies](set-up-anti-phishing-policies.md#spoof-settings).</span></span>

- <span data-ttu-id="280f8-111">**Stratégies Office 365 Advanced Threat Protection (ATP)**: cela inclut les organisations avec les abonnements complémentaires Microsoft 365 E5 ou Office 365 ATP :</span><span class="sxs-lookup"><span data-stu-id="280f8-111">**Office 365 Advanced Threat Protection (ATP) policies**: This includes organizations with Microsoft 365 E5 or Office 365 ATP add-on subscriptions:</span></span>

  - <span data-ttu-id="280f8-112">Stratégies anti-hameçonnage ATP, qui incluent :</span><span class="sxs-lookup"><span data-stu-id="280f8-112">ATP anti-phishing policies, which include:</span></span>

    - <span data-ttu-id="280f8-113">Les mêmes [paramètres d’usurpation](set-up-anti-phishing-policies.md#spoof-settings) qui sont disponibles dans les stratégies anti-hameçonnage EOP.</span><span class="sxs-lookup"><span data-stu-id="280f8-113">The same [spoof settings](set-up-anti-phishing-policies.md#spoof-settings) that are available in the EOP anti-phishing policies.</span></span>
    - [<span data-ttu-id="280f8-114">Paramètres d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="280f8-114">Impersonation settings</span></span>](set-up-anti-phishing-policies.md#impersonation-settings-in-atp-anti-phishing-policies)
    - [<span data-ttu-id="280f8-115">Seuils de hameçonnage avancés</span><span class="sxs-lookup"><span data-stu-id="280f8-115">Advanced phishing thresholds</span></span>](set-up-anti-phishing-policies.md#advanced-phishing-thresholds-in-atp-anti-phishing-policies)

  - <span data-ttu-id="280f8-116">[Stratégies de liens fiables](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings-in-custom-policies-for-specific-users).</span><span class="sxs-lookup"><span data-stu-id="280f8-116">[Safe Links policies](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings-in-custom-policies-for-specific-users).</span></span>

  - <span data-ttu-id="280f8-117">[Stratégies de pièces jointes approuvées](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-policy-settings-in-custom-policies-for-specific-users).</span><span class="sxs-lookup"><span data-stu-id="280f8-117">[Safe Attachments policies](recommended-settings-for-eop-and-office365-atp.md#safe-attachments-policy-settings-in-custom-policies-for-specific-users).</span></span>

<span data-ttu-id="280f8-118">Les valeurs de paramètres de stratégie **standard** et **strictes** utilisées comme configurations de référence sont décrites dans [paramètres recommandés pour la sécurité de l’ATP et d’Office 365](recommended-settings-for-eop-and-office365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-118">The **Standard** and **Strict** policy setting values that are used as baselines are described in [Recommended settings for EOP and Office 365 ATP security](recommended-settings-for-eop-and-office365-atp.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="280f8-119">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="280f8-119">What do you need to know before you begin?</span></span>

- <span data-ttu-id="280f8-120">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="280f8-120">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="280f8-121">Pour accéder directement à la page de l' **Analyseur de configuration** , utilisez <https://protection.office.com/configurationAnalyzer> .</span><span class="sxs-lookup"><span data-stu-id="280f8-121">To go directly to the **Configuration analyzer** page, use <https://protection.office.com/configurationAnalyzer>.</span></span>

- <span data-ttu-id="280f8-122">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="280f8-122">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="280f8-123">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="280f8-123">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="280f8-124">Pour utiliser l’analyseur de configuration **et** mettre à jour les stratégies de sécurité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="280f8-124">To use the configuration analyzer **and** make updates to security policies, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="280f8-125">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-125">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="280f8-126">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="280f8-126">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="280f8-127">Pour un accès en lecture seule à Configuration Analyzer, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="280f8-127">For read-only access to the configuration analyzer, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="280f8-128">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="280f8-128">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="280f8-129">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="280f8-129">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

## <a name="use-the-configuration-analyzer-in-the-security--compliance-center"></a><span data-ttu-id="280f8-130">Utiliser l’analyseur de configuration dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="280f8-130">Use the configuration analyzer in the Security & Compliance Center</span></span>

<span data-ttu-id="280f8-131">Dans le centre de sécurité & conformité, accédez à **Threat Management** \> **Policy** \> **Analyzer**.</span><span class="sxs-lookup"><span data-stu-id="280f8-131">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **Configuration analyzer**.</span></span>

![Widget Configuration Analyzer sur la page de stratégie de gestion des menaces \>](../../media/configuration-analyzer-widget.png)

<span data-ttu-id="280f8-133">L’analyseur de configuration comporte deux onglets principaux :</span><span class="sxs-lookup"><span data-stu-id="280f8-133">The configuration analyzer has two main tabs:</span></span>

- <span data-ttu-id="280f8-134">**Paramètres et recommandations**: sélectionnez standard ou strict et Comparez ces paramètres à vos stratégies de sécurité existantes.</span><span class="sxs-lookup"><span data-stu-id="280f8-134">**Settings and recommendations**: You pick Standard or Strict and compare those settings to your existing security policies.</span></span> <span data-ttu-id="280f8-135">Dans les résultats, vous pouvez ajuster les valeurs de vos paramètres pour les ramener au même niveau que standard ou strict.</span><span class="sxs-lookup"><span data-stu-id="280f8-135">In the results, you can adjust the values of your settings to bring them up to the same level as Standard or Strict.</span></span>

- <span data-ttu-id="280f8-136">**Analyse et historique de dérive de configuration**: cette vue permet de suivre les modifications que vous avez apportées à vos stratégies en fonction des résultats de l’analyseur de configuration au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="280f8-136">**Configuration drift analysis and history**: This view allows to track the changes that you've made to your policies based on the results of the configuration analyzer over time.</span></span>

### <a name="setting-and-recommendations-tab-in-the-configuration-analyzer"></a><span data-ttu-id="280f8-137">Onglet définition et recommandations de l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="280f8-137">Setting and recommendations tab in the configuration analyzer</span></span>

<span data-ttu-id="280f8-138">Par défaut, l’onglet s’ouvre sur la comparaison avec le profil de protection standard.</span><span class="sxs-lookup"><span data-stu-id="280f8-138">By default, the tab opens on the comparison to the Standard protection profile.</span></span> <span data-ttu-id="280f8-139">Vous pouvez passer à la comparaison du profil de protection strict en cliquant sur **Afficher rigoureuse Recommendations**.</span><span class="sxs-lookup"><span data-stu-id="280f8-139">You can switch to the comparison of the Strict protection profile by clicking **View Strict recommendations**.</span></span> <span data-ttu-id="280f8-140">Pour revenir en arrière, sélectionnez **afficher les recommandations standard**.</span><span class="sxs-lookup"><span data-stu-id="280f8-140">To switch back, select **View Standard recommendations**.</span></span>

![Vue paramètres et recommandations dans l’analyseur de configuration](../../media/configuration-analyzer-settings-and-recommendations-view.png)

<span data-ttu-id="280f8-142">Par défaut, la colonne **groupe de stratégies/nom du paramètre** contient une vue réduite des différents types de stratégies de sécurité et le nombre de paramètres dans ces stratégies qui doivent être améliorés (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="280f8-142">By default, the **Policy group/setting name** column contains a collapsed view of the different types of security polices and the number of settings in those policies that need improvement (if any).</span></span> <span data-ttu-id="280f8-143">Les types de stratégies sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="280f8-143">The types of policies are:</span></span>

- <span data-ttu-id="280f8-144">**Anti-spam**</span><span class="sxs-lookup"><span data-stu-id="280f8-144">**Anti-spam**</span></span>
- <span data-ttu-id="280f8-145">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="280f8-145">**Anti-phishing**</span></span>
- <span data-ttu-id="280f8-146">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="280f8-146">**Anti-malware**</span></span>
- <span data-ttu-id="280f8-147">**Pièces jointes sûres ATP** (si votre abonnement inclut ATP)</span><span class="sxs-lookup"><span data-stu-id="280f8-147">**ATP Safe Attachments** (if your subscription includes ATP)</span></span>
- <span data-ttu-id="280f8-148">**Liens fiables ATP** (si votre abonnement inclut ATP)</span><span class="sxs-lookup"><span data-stu-id="280f8-148">**ATP Safe Links** (if your subscription includes ATP)</span></span>

<span data-ttu-id="280f8-149">Dans l’affichage par défaut, tout est réduit.</span><span class="sxs-lookup"><span data-stu-id="280f8-149">In the default view, everything is collapsed.</span></span> <span data-ttu-id="280f8-150">En regard de chaque stratégie, un résumé des résultats de la comparaison de vos stratégies (que vous pouvez modifier) et les paramètres des stratégies correspondantes pour les profils de protection standard ou stricte (que vous ne pouvez pas modifier) s’affichent.</span><span class="sxs-lookup"><span data-stu-id="280f8-150">Next to each policy, a summary of comparison results from your policies (which you can modify) and the settings in the corresponding policies for the Standard or Strict protection profiles (which you can't modify) are displayed.</span></span> <span data-ttu-id="280f8-151">Les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="280f8-151">You'll see the following information:</span></span>

- <span data-ttu-id="280f8-152">**Vert**: tous les paramètres de toutes les stratégies existantes sont au moins aussi sécurisés que le profil de protection auquel vous effectuez une comparaison.</span><span class="sxs-lookup"><span data-stu-id="280f8-152">**Green**: All settings in all existing policies are at least as secure as the protection profile that you're comparing to.</span></span>
- <span data-ttu-id="280f8-153">**Orange**: un petit nombre de paramètres dans les stratégies existantes n’est pas aussi sécurisé que le profil de protection auquel vous effectuez une comparaison.</span><span class="sxs-lookup"><span data-stu-id="280f8-153">**Amber**: A small number of settings in the existing policies are not as secure as the protection profile that you're comparing to.</span></span>
- <span data-ttu-id="280f8-154">**Rouge**: un nombre significatif de paramètres dans les stratégies existantes n’est pas aussi sécurisé que le profil de protection auquel vous effectuez une comparaison.</span><span class="sxs-lookup"><span data-stu-id="280f8-154">**Red**: A significant number of settings in the existing policies are not as secure as the protection profile that you're comparing to.</span></span> <span data-ttu-id="280f8-155">Il peut s’agir de quelques paramètres dans de nombreuses stratégies ou de nombreux paramètres dans une stratégie.</span><span class="sxs-lookup"><span data-stu-id="280f8-155">This could be a few settings in many policies or many settings in one policy.</span></span>

<span data-ttu-id="280f8-156">Pour les comparaisons favorables, vous verrez le texte : **tous les paramètres suivent** les \<**Standard** or **Strict**\> **recommandations**.</span><span class="sxs-lookup"><span data-stu-id="280f8-156">For favorable comparisons, you'll see the text: **All settings follow** \<**Standard** or **Strict**\> **recommendations**.</span></span> <span data-ttu-id="280f8-157">Dans le cas contraire, vous verrez le nombre de paramètres recommandés à modifier.</span><span class="sxs-lookup"><span data-stu-id="280f8-157">Otherwise, you'll see the number of recommended settings to change.</span></span>

<span data-ttu-id="280f8-158">Si vous développez le **nom du groupe de stratégies/du paramètre**, toutes les stratégies et les paramètres associés dans chaque stratégie spécifique nécessitant une attention sont révélés.</span><span class="sxs-lookup"><span data-stu-id="280f8-158">If you expand **Policy group/setting name**, all of the policies and the associated settings in each specific policy that require attention are revealed.</span></span> <span data-ttu-id="280f8-159">Vous pouvez également développer un type spécifique de stratégie (par exemple, le **blocage du courrier indésirable**) pour afficher uniquement ces paramètres dans ces types de stratégies qui nécessitent votre attention.</span><span class="sxs-lookup"><span data-stu-id="280f8-159">Or, you can expand a specific type of policy (for example, **Anti-spam**) to see just those settings in those types of policies that require your attention.</span></span>

<span data-ttu-id="280f8-160">Si la comparaison n’a pas de recommandations d’amélioration (en vert), le développement de la stratégie n’indique rien.</span><span class="sxs-lookup"><span data-stu-id="280f8-160">If the comparison has no recommendations for improvement (green), expanding the policy reveals nothing.</span></span> <span data-ttu-id="280f8-161">S’il existe un nombre de recommandations pour l’amélioration (jaune ou rouge), les paramètres nécessitant une attention sont révélés, et les informations correspondantes sont révélées dans les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="280f8-161">If there are any number of recommendations for improvement (amber or red), the settings that require attention are revealed, and corresponding information is revealed in the following columns:</span></span>

- <span data-ttu-id="280f8-162">Nom du paramètre qui requiert votre attention.</span><span class="sxs-lookup"><span data-stu-id="280f8-162">The name of the setting that requires your attention.</span></span> <span data-ttu-id="280f8-163">Par exemple, dans la capture d’écran précédente, il s’agit du **seuil de courrier électronique en bloc** dans une stratégie de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="280f8-163">For example, in the previous screenshot, it's the **Bulk email threshold** in an anti-spam policy.</span></span>

- <span data-ttu-id="280f8-164">**Stratégie**: nom de la stratégie concernée qui contient le paramètre.</span><span class="sxs-lookup"><span data-stu-id="280f8-164">**Policy**: The name of the affected policy that contains the setting.</span></span>

- <span data-ttu-id="280f8-165">**Appliqué à**: le nombre d’utilisateurs auxquels les stratégies affectées sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="280f8-165">**Applied to**: The number of user that the affected policies are applied to.</span></span>

- <span data-ttu-id="280f8-166">**Configuration actuelle**: valeur actuelle du paramètre.</span><span class="sxs-lookup"><span data-stu-id="280f8-166">**Current configuration**: The current value of the setting.</span></span>

- <span data-ttu-id="280f8-167">**Dernière modification**: date de la dernière modification de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="280f8-167">**Last modified**: The date that the policy was last modified.</span></span>

- <span data-ttu-id="280f8-168">**Recommandations**: valeur du paramètre dans le profil de protection standard ou strict.</span><span class="sxs-lookup"><span data-stu-id="280f8-168">**Recommendations**: The value of the setting in the Standard or Strict protection profile.</span></span> <span data-ttu-id="280f8-169">Pour modifier la valeur du paramètre dans votre stratégie pour qu’elle corresponde à la valeur recommandée dans le profil de protection, cliquez sur **adopter**.</span><span class="sxs-lookup"><span data-stu-id="280f8-169">To change the value of the setting in your policy to match the recommended value in the protection profile, click **Adopt**.</span></span> <span data-ttu-id="280f8-170">Si la modification réussit, vous verrez le message suivant : **recommandations correctement adoptées**.</span><span class="sxs-lookup"><span data-stu-id="280f8-170">If the change is successful, you'll see the message: **Recommendations successfully adopted**.</span></span> <span data-ttu-id="280f8-171">Cliquez sur **Actualiser** pour afficher le nombre réduit de recommandations, ainsi que la suppression de la ligne de paramètre/stratégie spécifique des résultats.</span><span class="sxs-lookup"><span data-stu-id="280f8-171">Click **Refresh** to see the reduced number of recommendations, and the removal of the specific setting/policy row from the results.</span></span>

### <a name="configuration-drift-analysis-and-history-tab-in-the-configuration-analyzer"></a><span data-ttu-id="280f8-172">Onglet analyse de dérive et historique de configuration de l’analyseur de configuration</span><span class="sxs-lookup"><span data-stu-id="280f8-172">Configuration drift analysis and history tab in the configuration analyzer</span></span>

<span data-ttu-id="280f8-173">Cet onglet vous permet d’effectuer le suivi des modifications que vous avez apportées à vos stratégies de sécurité personnalisées en fonction des informations de l’analyseur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="280f8-173">This tab allows you to track the changes that you've made to your custom security policies based on the information in the security analyzer.</span></span> <span data-ttu-id="280f8-174">Par défaut, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="280f8-174">By default, the following information is displayed:</span></span>

- <span data-ttu-id="280f8-175">**Dernière modification**</span><span class="sxs-lookup"><span data-stu-id="280f8-175">**Last modified**</span></span>
- <span data-ttu-id="280f8-176">**Modifié par**</span><span class="sxs-lookup"><span data-stu-id="280f8-176">**Modified by**</span></span>
- <span data-ttu-id="280f8-177">**Nom du paramètre**</span><span class="sxs-lookup"><span data-stu-id="280f8-177">**Setting Name**</span></span>
- <span data-ttu-id="280f8-178">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="280f8-178">**Policy**</span></span>
- <span data-ttu-id="280f8-179">**Type**</span><span class="sxs-lookup"><span data-stu-id="280f8-179">**Type**</span></span>

<span data-ttu-id="280f8-180">Pour filtrer les résultats, cliquez sur **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="280f8-180">To filter the results, click **Filter**.</span></span> <span data-ttu-id="280f8-181">Dans le menu volant **filtres** qui s’affiche, vous pouvez sélectionner l’un des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="280f8-181">In the **Filters** flyout that appears, you can select from the following filters:</span></span>

- <span data-ttu-id="280f8-182">Heure de **début** et **heure de fin** (date)</span><span class="sxs-lookup"><span data-stu-id="280f8-182">**Start time** and **End time** (date)</span></span>
- <span data-ttu-id="280f8-183">**Protection standard** ou **protection stricte**</span><span class="sxs-lookup"><span data-stu-id="280f8-183">**Standard protection** or **Strict protection**</span></span>

<span data-ttu-id="280f8-184">Pour exporter les résultats dans un fichier. csv, cliquez sur **Exporter**.</span><span class="sxs-lookup"><span data-stu-id="280f8-184">To export the results to a .csv file, click **Export**.</span></span>

![Analyse de dérive de configuration et vue historique dans l’analyseur de configuration](../../media/configuration-analyzer-configuration-drift-analysis-view.png)
