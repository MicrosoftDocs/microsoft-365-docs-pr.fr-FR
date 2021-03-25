---
title: Visitez le centre de mise en œuvre pour voir les actions de correction
description: Utiliser le centre de gestion des actions pour afficher les détails et les résultats à la suite d’un examen automatisé
keywords: action, centre, autoir, automatisé, examen, réponse, correction
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: how-to
ms.reviewer: ramarom, evaldm, isco, mabraitm, chriggs
ms.date: 01/28/2021
ms.technology: mde
ms.openlocfilehash: 6caa1cfe08a20aa824d85966c104a25988b8be53
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165356"
---
# <a name="visit-the-action-center-to-see-remediation-actions"></a><span data-ttu-id="d78d8-104">Visitez le centre de mise en œuvre pour voir les actions de correction</span><span class="sxs-lookup"><span data-stu-id="d78d8-104">Visit the Action center to see remediation actions</span></span>

<span data-ttu-id="d78d8-105">Pendant et après un examen automatisé, les actions de correction des détections de menaces sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="d78d8-105">During and after an automated investigation, remediation actions for threat detections are identified.</span></span> <span data-ttu-id="d78d8-106">Selon la menace particulière et la façon dont [Microsoft Defender pour le](https://docs.microsoft.com/windows/security/threat-protection) point de terminaison est configuré pour votre organisation, certaines actions de correction sont prises automatiquement et d’autres nécessitent une approbation.</span><span class="sxs-lookup"><span data-stu-id="d78d8-106">Depending on the particular threat and how [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection) is configured for your organization, some remediation actions are taken automatically, and others require approval.</span></span> <span data-ttu-id="d78d8-107">Si vous faites partie de l’équipe des opérations de sécurité de votre organisation, vous pouvez afficher les [actions](manage-auto-investigation.md#remediation-actions) de correction en attente et terminées dans le centre **de actions.**</span><span class="sxs-lookup"><span data-stu-id="d78d8-107">If you're part of your organization's security operations team, you can view pending and completed [remediation actions](manage-auto-investigation.md#remediation-actions) in the **Action center**.</span></span> 


<span data-ttu-id="d78d8-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d78d8-108">**Applies to:**</span></span>
- [<span data-ttu-id="d78d8-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d78d8-109">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d78d8-110">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d78d8-110">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

## <a name="new-a-unified-action-center"></a><span data-ttu-id="d78d8-111">(NOUVEAU!) Un centre de l’action unifié</span><span class="sxs-lookup"><span data-stu-id="d78d8-111">(NEW!) A unified Action center</span></span>


<span data-ttu-id="d78d8-112">Nous sommes heureux d’annoncer un nouveau centre de travail unifié ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) )!</span><span class="sxs-lookup"><span data-stu-id="d78d8-112">We are pleased to announce a new, unified Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center))!</span></span>

:::image type="content" source="images/mde-action-center-unified.png" alt-text="Centre de sécurité Microsoft 365":::

<span data-ttu-id="d78d8-114">Le tableau suivant compare le nouveau centre de l’action unifié au centre de l’action précédent.</span><span class="sxs-lookup"><span data-stu-id="d78d8-114">The following table compares the new, unified Action center to the previous Action center.</span></span>

|<span data-ttu-id="d78d8-115">Nouveau centre de l’action unifié</span><span class="sxs-lookup"><span data-stu-id="d78d8-115">The new, unified Action center</span></span>  |<span data-ttu-id="d78d8-116">Centre de l’action précédent</span><span class="sxs-lookup"><span data-stu-id="d78d8-116">The previous Action center</span></span>  |
|---------|---------|
|<span data-ttu-id="d78d8-117">Répertorie les actions en attente et terminées pour les appareils et le courrier électronique dans un seul emplacement</span><span class="sxs-lookup"><span data-stu-id="d78d8-117">Lists pending and completed actions for devices and email in one location</span></span> <br/><span data-ttu-id="d78d8-118">([Microsoft Defender pour point de terminaison](microsoft-defender-advanced-threat-protection.md) plus Microsoft Defender pour Office [365](https://docs.microsoft.com/microsoft-365/security/defender-365-security/office-365-atp))</span><span class="sxs-lookup"><span data-stu-id="d78d8-118">([Microsoft Defender for Endpoint](microsoft-defender-advanced-threat-protection.md) plus [Microsoft Defender for Office 365](https://docs.microsoft.com/microsoft-365/security/defender-365-security/office-365-atp))</span></span>|<span data-ttu-id="d78d8-119">Répertorie les actions en attente et terminées pour les appareils</span><span class="sxs-lookup"><span data-stu-id="d78d8-119">Lists pending and completed actions for devices</span></span> <br/> <span data-ttu-id="d78d8-120">([Microsoft Defender pour point de terminaison](microsoft-defender-advanced-threat-protection.md) uniquement)</span><span class="sxs-lookup"><span data-stu-id="d78d8-120">([Microsoft Defender for Endpoint](microsoft-defender-advanced-threat-protection.md) only)</span></span>   |
|<span data-ttu-id="d78d8-121">Se trouve à l’emplacement :</span><span class="sxs-lookup"><span data-stu-id="d78d8-121">Is located at:</span></span><br/>[https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)         |<span data-ttu-id="d78d8-122">Se trouve à l’emplacement :</span><span class="sxs-lookup"><span data-stu-id="d78d8-122">Is located at:</span></span><br/>[https://securitycenter.windows.com/action-center](https://securitycenter.windows.com/action-center)     |
| <span data-ttu-id="d78d8-123">Dans le Centre de sécurité Microsoft 365, choisissez **Centre de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="d78d8-123">In the Microsoft 365 security center, choose **Action center**.</span></span> <p>:::image type="content" source="images/action-center-nav-new.png" alt-text="Accès au Centre de sécurité Dans le Centre de sécurité Microsoft 365"::: | <span data-ttu-id="d78d8-125">Dans le Centre de sécurité Microsoft Defender, choisissez **Centre d’action**  >  **enquêtes automatisées.**</span><span class="sxs-lookup"><span data-stu-id="d78d8-125">In the Microsoft Defender Security Center, choose **Automated investigations** > **Action center**.</span></span> <p>:::image type="content" source="images/action-center-nav-old.png" alt-text="Navigation vers le centre de sécurité à partir du Centre de sécurité Microsoft Defender":::  |

<span data-ttu-id="d78d8-127">Le centre de mise en œuvre unifié regroupe les actions de correction dans Defender pour Endpoint et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="d78d8-127">The unified Action center brings together remediation actions across Defender for Endpoint and Defender for Office 365.</span></span> <span data-ttu-id="d78d8-128">Il définit un langage commun pour toutes les actions de correction et fournit une expérience d’examen unifiée.</span><span class="sxs-lookup"><span data-stu-id="d78d8-128">It defines a common language for all remediation actions, and provides a unified investigation experience.</span></span> 

<span data-ttu-id="d78d8-129">Vous pouvez utiliser le centre de l’action unifiée si vous avez les autorisations appropriées et un ou plusieurs des abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="d78d8-129">You can use the unified Action center if you have appropriate permissions and one or more of the following subscriptions:</span></span>
- [<span data-ttu-id="d78d8-130">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d78d8-130">Defender for Endpoint</span></span>](microsoft-defender-advanced-threat-protection.md)
- [<span data-ttu-id="d78d8-131">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="d78d8-131">Defender for Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-365-security/office-365-atp)
- [<span data-ttu-id="d78d8-132">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d78d8-132">Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/microsoft-threat-protection) 

> [!TIP]
> <span data-ttu-id="d78d8-133">Pour en savoir plus, consultez [La réglementation requise.](https://docs.microsoft.com/microsoft-365/security/mtp/prerequisites)</span><span class="sxs-lookup"><span data-stu-id="d78d8-133">To learn more, see [Requirements](https://docs.microsoft.com/microsoft-365/security/mtp/prerequisites).</span></span>

## <a name="using-the-action-center"></a><span data-ttu-id="d78d8-134">Utilisation du centre de l’action</span><span class="sxs-lookup"><span data-stu-id="d78d8-134">Using the Action center</span></span>

<span data-ttu-id="d78d8-135">Pour obtenir le centre de l’action unifiée dans le Centre de sécurité Microsoft 365 amélioré :</span><span class="sxs-lookup"><span data-stu-id="d78d8-135">To get to the unified Action center in the improved Microsoft 365 security center:</span></span>
1. <span data-ttu-id="d78d8-136">Go to the Microsoft 365 security center ( [https://security.microsoft.com](https://security.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="d78d8-136">Go to the Microsoft 365 security center ([https://security.microsoft.com](https://security.microsoft.com)) and sign in.</span></span>
2. <span data-ttu-id="d78d8-137">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="d78d8-137">In the navigation pane, select **Action center**.</span></span> 

<span data-ttu-id="d78d8-138">Lorsque vous visitez le centre de actions, vous voyez deux onglets : **Actions en attente et** **Historique.**</span><span class="sxs-lookup"><span data-stu-id="d78d8-138">When you visit the Action center, you see two tabs: **Pending actions** and **History**.</span></span> <span data-ttu-id="d78d8-139">Le tableau suivant récapitule ce que vous verrez sur chaque onglet :</span><span class="sxs-lookup"><span data-stu-id="d78d8-139">The following table summarizes what you'll see on each tab:</span></span>

|<span data-ttu-id="d78d8-140">Tab</span><span class="sxs-lookup"><span data-stu-id="d78d8-140">Tab</span></span>  |<span data-ttu-id="d78d8-141">Description</span><span class="sxs-lookup"><span data-stu-id="d78d8-141">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="d78d8-142">**Pending**</span><span class="sxs-lookup"><span data-stu-id="d78d8-142">**Pending**</span></span>     | <span data-ttu-id="d78d8-143">Affiche une liste d’actions qui nécessitent une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="d78d8-143">Displays a list of actions that require attention.</span></span> <span data-ttu-id="d78d8-144">Vous pouvez approuver ou rejeter des actions une par une, ou sélectionner plusieurs actions si elles ont le même type d’action (telles que le fichier **de mise en quarantaine).**</span><span class="sxs-lookup"><span data-stu-id="d78d8-144">You can approve or reject actions one at a time, or select multiple actions if they have the same type of action (such as **Quarantine file**).</span></span> <br/><span data-ttu-id="d78d8-145">**CONSEIL**: veillez à examiner et à approuver [(ou rejeter)](manage-auto-investigation.md) les actions en attente dès que possible afin que vos enquêtes automatisées se terminent en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="d78d8-145">**TIP**: Make sure to [review and approve (or reject) pending actions](manage-auto-investigation.md) as soon as possible so that your automated investigations can complete in a timely manner.</span></span> |
|<span data-ttu-id="d78d8-146">**Historique**</span><span class="sxs-lookup"><span data-stu-id="d78d8-146">**History**</span></span>     | <span data-ttu-id="d78d8-147">Sert de journal d’audit pour les actions qui ont été entreprises, telles que :</span><span class="sxs-lookup"><span data-stu-id="d78d8-147">Serves as an audit log for actions that were taken, such as:</span></span> <br/><span data-ttu-id="d78d8-148">- Mesures correctives prises à la suite d’enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="d78d8-148">- Remediation actions that were taken as a result of automated investigations</span></span> <br><span data-ttu-id="d78d8-149">- Actions de correction approuvées par votre équipe des opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="d78d8-149">- Remediation actions that were approved by your security operations team</span></span>  <br/><span data-ttu-id="d78d8-150">- Commandes qui ont été exécutés et actions de correction appliquées pendant les sessions Live Response</span><span class="sxs-lookup"><span data-stu-id="d78d8-150">- Commands that were run and remediation actions that were applied during Live Response sessions</span></span>  <br/><span data-ttu-id="d78d8-151">- Mesures correctives prises par les fonctionnalités de protection contre les menaces dans l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="d78d8-151">- Remediation actions that were taken by threat protection features in Microsoft Defender Antivirus</span></span>  <p><span data-ttu-id="d78d8-152">Fournit un moyen d’annuler certaines actions (voir [Annuler les actions terminées).](manage-auto-investigation.md#undo-completed-actions)</span><span class="sxs-lookup"><span data-stu-id="d78d8-152">Provides a way to undo certain actions (see [Undo completed actions](manage-auto-investigation.md#undo-completed-actions)).</span></span>       |

<span data-ttu-id="d78d8-153">Vous pouvez personnaliser, trier, filtrer et exporter des données dans le centre de gestion de l’action.</span><span class="sxs-lookup"><span data-stu-id="d78d8-153">You can customize, sort, filter, and export data in the Action center.</span></span>

:::image type="content" source="images/new-action-center-columnsfilters.png" alt-text="Colonnes et filtres dans le centre de l’action":::

- <span data-ttu-id="d78d8-155">Sélectionnez un en-tête de colonne pour trier les éléments par ordre croissant ou décroit.</span><span class="sxs-lookup"><span data-stu-id="d78d8-155">Select a column heading to sort items in ascending or descending order.</span></span>
- <span data-ttu-id="d78d8-156">Utilisez le filtre de période pour afficher les données du jour, de la semaine, des 30 ou 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="d78d8-156">Use the time period filter to view data for the past day, week, 30 days, or 6 months.</span></span>
- <span data-ttu-id="d78d8-157">Choisissez les colonnes que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="d78d8-157">Choose the columns that you want to view.</span></span>
- <span data-ttu-id="d78d8-158">Spécifiez le nombre d’éléments à inclure sur chaque page de données.</span><span class="sxs-lookup"><span data-stu-id="d78d8-158">Specify how many items to include on each page of data.</span></span>
- <span data-ttu-id="d78d8-159">Utilisez des filtres pour afficher uniquement les éléments que vous souhaitez voir.</span><span class="sxs-lookup"><span data-stu-id="d78d8-159">Use filters to view just the items you want to see.</span></span>
- <span data-ttu-id="d78d8-160">Sélectionnez **Exporter** pour exporter les résultats vers un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="d78d8-160">Select **Export** to export results to a .csv file.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="d78d8-161">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d78d8-161">Next steps</span></span>

- [<span data-ttu-id="d78d8-162">Afficher et approuver les actions de correction</span><span class="sxs-lookup"><span data-stu-id="d78d8-162">View and approve remediation actions</span></span>](manage-auto-investigation.md)
- [<span data-ttu-id="d78d8-163">Consultez le guide interactif : Examiner et corriger les menaces avec Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d78d8-163">See the interactive guide: Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
 
## <a name="see-also"></a><span data-ttu-id="d78d8-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d78d8-164">See also</span></span>

- [<span data-ttu-id="d78d8-165">Corriger les faux positifs/négatifs dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d78d8-165">Address false positives/negatives in Microsoft Defender for Endpoint</span></span>](defender-endpoint-false-positives-negatives.md)
