---
title: Visitez le centre de mise en œuvre pour voir les actions de correction
description: Utiliser le centre de gestion des actions pour afficher les détails et les résultats à la suite d’un examen automatisé
keywords: action, centre, autoir, automatisé, examen, réponse, correction
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: JoeDavies-MSFT
ms.author: josephd
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
ms.openlocfilehash: cc806678bbb5ac19f7c4e035efb52b6ba7d1edb1
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844909"
---
# <a name="visit-the-action-center-to-see-remediation-actions"></a><span data-ttu-id="5618a-104">Visitez le centre de mise en œuvre pour voir les actions de correction</span><span class="sxs-lookup"><span data-stu-id="5618a-104">Visit the Action center to see remediation actions</span></span>

<span data-ttu-id="5618a-105">Pendant et après un examen automatisé, les actions de correction des détections de menaces sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="5618a-105">During and after an automated investigation, remediation actions for threat detections are identified.</span></span> <span data-ttu-id="5618a-106">Selon la menace particulière et la façon dont [Microsoft Defender pour le](/windows/security/threat-protection) point de terminaison est configuré pour votre organisation, certaines actions de correction sont prises automatiquement et d’autres nécessitent une approbation.</span><span class="sxs-lookup"><span data-stu-id="5618a-106">Depending on the particular threat and how [Microsoft Defender for Endpoint](/windows/security/threat-protection) is configured for your organization, some remediation actions are taken automatically, and others require approval.</span></span> <span data-ttu-id="5618a-107">Si vous faites partie de l’équipe des opérations de sécurité de votre organisation, vous pouvez afficher les [actions](manage-auto-investigation.md#remediation-actions) de correction en attente et terminées dans le centre **de actions.**</span><span class="sxs-lookup"><span data-stu-id="5618a-107">If you're part of your organization's security operations team, you can view pending and completed [remediation actions](manage-auto-investigation.md#remediation-actions) in the **Action center**.</span></span> 


<span data-ttu-id="5618a-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5618a-108">**Applies to:**</span></span>
- [<span data-ttu-id="5618a-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5618a-109">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5618a-110">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5618a-110">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

## <a name="new-a-unified-action-center"></a><span data-ttu-id="5618a-111">(NOUVEAU!) Un centre de l’action unifié</span><span class="sxs-lookup"><span data-stu-id="5618a-111">(NEW!) A unified Action center</span></span>


<span data-ttu-id="5618a-112">Nous sommes heureux d’annoncer un nouveau centre de travail unifié ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) )!</span><span class="sxs-lookup"><span data-stu-id="5618a-112">We are pleased to announce a new, unified Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center))!</span></span>

:::image type="content" source="images/mde-action-center-unified.png" alt-text="Centre de Microsoft 365 de sécurité":::

<span data-ttu-id="5618a-114">Le tableau suivant compare le nouveau centre de l’action unifié au centre de l’action précédent.</span><span class="sxs-lookup"><span data-stu-id="5618a-114">The following table compares the new, unified Action center to the previous Action center.</span></span>

|<span data-ttu-id="5618a-115">Nouveau centre de l’action unifié</span><span class="sxs-lookup"><span data-stu-id="5618a-115">The new, unified Action center</span></span>  |<span data-ttu-id="5618a-116">Centre de l’action précédent</span><span class="sxs-lookup"><span data-stu-id="5618a-116">The previous Action center</span></span>  |
|---------|---------|
|<span data-ttu-id="5618a-117">Répertorie les actions en attente et terminées pour les appareils et le courrier électronique dans un seul emplacement</span><span class="sxs-lookup"><span data-stu-id="5618a-117">Lists pending and completed actions for devices and email in one location</span></span> <br/><span data-ttu-id="5618a-118">([Microsoft Defender pour point de terminaison](microsoft-defender-endpoint.md) plus Microsoft Defender pour [Office 365](/microsoft-365/security/office-365-security/office-365-atp))</span><span class="sxs-lookup"><span data-stu-id="5618a-118">([Microsoft Defender for Endpoint](microsoft-defender-endpoint.md) plus [Microsoft Defender for Office 365](/microsoft-365/security/office-365-security/office-365-atp))</span></span>|<span data-ttu-id="5618a-119">Répertorie les actions en attente et terminées pour les appareils</span><span class="sxs-lookup"><span data-stu-id="5618a-119">Lists pending and completed actions for devices</span></span> <br/> <span data-ttu-id="5618a-120">([Microsoft Defender pour point de terminaison](microsoft-defender-endpoint.md) uniquement)</span><span class="sxs-lookup"><span data-stu-id="5618a-120">([Microsoft Defender for Endpoint](microsoft-defender-endpoint.md) only)</span></span>   |
|<span data-ttu-id="5618a-121">Se trouve à l’emplacement :</span><span class="sxs-lookup"><span data-stu-id="5618a-121">Is located at:</span></span><br/>[https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)         |<span data-ttu-id="5618a-122">Se trouve à l’emplacement :</span><span class="sxs-lookup"><span data-stu-id="5618a-122">Is located at:</span></span><br/>[https://securitycenter.windows.com/action-center](https://securitycenter.windows.com/action-center)     |
| <span data-ttu-id="5618a-123">Dans le centre Microsoft 365 de sécurité, sélectionnez **Centre de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="5618a-123">In the Microsoft 365 security center, choose **Action center**.</span></span> <p>:::image type="content" source="images/action-center-nav-new.png" alt-text="Navigation vers le centre de sécurité dans le centre de Microsoft 365 de sécurité"::: | <span data-ttu-id="5618a-125">In the Centre de sécurité Microsoft Defender, choose **Automated investigations** Action  >  **center**.</span><span class="sxs-lookup"><span data-stu-id="5618a-125">In the Microsoft Defender Security Center, choose **Automated investigations** > **Action center**.</span></span> <p>:::image type="content" source="images/action-center-nav-old.png" alt-text="Navigation vers le centre de l’action à partir du Centre de sécurité Microsoft Defender":::  |

<span data-ttu-id="5618a-127">Le centre de mise en œuvre unifié regroupe les actions de correction dans Defender pour Endpoint et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="5618a-127">The unified Action center brings together remediation actions across Defender for Endpoint and Defender for Office 365.</span></span> <span data-ttu-id="5618a-128">Il définit un langage commun pour toutes les actions de correction et fournit une expérience d’examen unifiée.</span><span class="sxs-lookup"><span data-stu-id="5618a-128">It defines a common language for all remediation actions, and provides a unified investigation experience.</span></span> 

<span data-ttu-id="5618a-129">Vous pouvez utiliser le centre de l’action unifiée si vous avez les autorisations appropriées et un ou plusieurs des abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="5618a-129">You can use the unified Action center if you have appropriate permissions and one or more of the following subscriptions:</span></span>
- [<span data-ttu-id="5618a-130">Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5618a-130">Defender for Endpoint</span></span>](microsoft-defender-endpoint.md)
- [<span data-ttu-id="5618a-131">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="5618a-131">Defender for Office 365</span></span>](/microsoft-365/security/office-365-security/office-365-atp)
- [<span data-ttu-id="5618a-132">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5618a-132">Microsoft 365 Defender</span></span>](/microsoft-365/security/mtp/microsoft-threat-protection) 

> [!TIP]
> <span data-ttu-id="5618a-133">Pour plus d’informations, voir [Requirements](/microsoft-365/security/mtp/prerequisites).</span><span class="sxs-lookup"><span data-stu-id="5618a-133">To learn more, see [Requirements](/microsoft-365/security/mtp/prerequisites).</span></span>

## <a name="using-the-action-center"></a><span data-ttu-id="5618a-134">Utilisation du centre de l’action</span><span class="sxs-lookup"><span data-stu-id="5618a-134">Using the Action center</span></span>

<span data-ttu-id="5618a-135">Pour obtenir le centre de l’action unifiée dans le centre de sécurité Microsoft 365 amélioré :</span><span class="sxs-lookup"><span data-stu-id="5618a-135">To get to the unified Action center in the improved Microsoft 365 security center:</span></span>
1. <span data-ttu-id="5618a-136">Go to the Microsoft 365 security center ( [https://security.microsoft.com](https://security.microsoft.com) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="5618a-136">Go to the Microsoft 365 security center ([https://security.microsoft.com](https://security.microsoft.com)) and sign in.</span></span>
2. <span data-ttu-id="5618a-137">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="5618a-137">In the navigation pane, select **Action center**.</span></span> 

<span data-ttu-id="5618a-138">Lorsque vous visitez le centre de l’action, vous voyez deux onglets : **Actions en attente et** **Historique.**</span><span class="sxs-lookup"><span data-stu-id="5618a-138">When you visit the Action center, you see two tabs: **Pending actions** and **History**.</span></span> <span data-ttu-id="5618a-139">Le tableau suivant récapitule ce que vous verrez sur chaque onglet :</span><span class="sxs-lookup"><span data-stu-id="5618a-139">The following table summarizes what you'll see on each tab:</span></span>

|<span data-ttu-id="5618a-140">Tab</span><span class="sxs-lookup"><span data-stu-id="5618a-140">Tab</span></span>  |<span data-ttu-id="5618a-141">Description</span><span class="sxs-lookup"><span data-stu-id="5618a-141">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="5618a-142">**Pending**</span><span class="sxs-lookup"><span data-stu-id="5618a-142">**Pending**</span></span>     | <span data-ttu-id="5618a-143">Affiche une liste d’actions qui nécessitent une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="5618a-143">Displays a list of actions that require attention.</span></span> <span data-ttu-id="5618a-144">Vous pouvez approuver ou rejeter des actions une par une, ou sélectionner plusieurs actions si elles ont le même type d’action (telles que le fichier **de mise en quarantaine).**</span><span class="sxs-lookup"><span data-stu-id="5618a-144">You can approve or reject actions one at a time, or select multiple actions if they have the same type of action (such as **Quarantine file**).</span></span> <br/><span data-ttu-id="5618a-145">**CONSEIL**: veillez à examiner et à approuver [(ou rejeter)](manage-auto-investigation.md) les actions en attente dès que possible afin que vos enquêtes automatisées se terminent en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="5618a-145">**TIP**: Make sure to [review and approve (or reject) pending actions](manage-auto-investigation.md) as soon as possible so that your automated investigations can complete in a timely manner.</span></span> |
|<span data-ttu-id="5618a-146">**Historique**</span><span class="sxs-lookup"><span data-stu-id="5618a-146">**History**</span></span>     | <span data-ttu-id="5618a-147">Sert de journal d’audit pour les actions qui ont été entreprises, telles que :</span><span class="sxs-lookup"><span data-stu-id="5618a-147">Serves as an audit log for actions that were taken, such as:</span></span> <br/><span data-ttu-id="5618a-148">- Mesures correctives prises suite à des enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="5618a-148">- Remediation actions that were taken as a result of automated investigations</span></span> <br><span data-ttu-id="5618a-149">- Actions de correction approuvées par votre équipe des opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="5618a-149">- Remediation actions that were approved by your security operations team</span></span>  <br/><span data-ttu-id="5618a-150">- Commandes qui ont été exécutés et actions de correction appliquées pendant les sessions Live Response</span><span class="sxs-lookup"><span data-stu-id="5618a-150">- Commands that were run and remediation actions that were applied during Live Response sessions</span></span>  <br/><span data-ttu-id="5618a-151">- Mesures correctives prises par les fonctionnalités de protection contre les menaces dans Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="5618a-151">- Remediation actions that were taken by threat protection features in Microsoft Defender Antivirus</span></span>  <p><span data-ttu-id="5618a-152">Fournit un moyen d’annuler certaines actions (voir [Annuler les actions terminées).](manage-auto-investigation.md#undo-completed-actions)</span><span class="sxs-lookup"><span data-stu-id="5618a-152">Provides a way to undo certain actions (see [Undo completed actions](manage-auto-investigation.md#undo-completed-actions)).</span></span>       |

<span data-ttu-id="5618a-153">Vous pouvez personnaliser, trier, filtrer et exporter des données dans le centre de gestion de l’action.</span><span class="sxs-lookup"><span data-stu-id="5618a-153">You can customize, sort, filter, and export data in the Action center.</span></span>

:::image type="content" source="images/new-action-center-columnsfilters.png" alt-text="Colonnes et filtres dans le centre de l’action":::

- <span data-ttu-id="5618a-155">Sélectionnez un en-tête de colonne pour trier les éléments par ordre croissant ou décroit.</span><span class="sxs-lookup"><span data-stu-id="5618a-155">Select a column heading to sort items in ascending or descending order.</span></span>
- <span data-ttu-id="5618a-156">Utilisez le filtre de période pour afficher les données du jour, de la semaine, des 30 ou 6 derniers mois.</span><span class="sxs-lookup"><span data-stu-id="5618a-156">Use the time period filter to view data for the past day, week, 30 days, or 6 months.</span></span>
- <span data-ttu-id="5618a-157">Choisissez les colonnes que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="5618a-157">Choose the columns that you want to view.</span></span>
- <span data-ttu-id="5618a-158">Spécifiez le nombre d’éléments à inclure sur chaque page de données.</span><span class="sxs-lookup"><span data-stu-id="5618a-158">Specify how many items to include on each page of data.</span></span>
- <span data-ttu-id="5618a-159">Utilisez des filtres pour afficher uniquement les éléments que vous souhaitez voir.</span><span class="sxs-lookup"><span data-stu-id="5618a-159">Use filters to view just the items you want to see.</span></span>
- <span data-ttu-id="5618a-160">Sélectionnez **Exporter** pour exporter les résultats vers .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="5618a-160">Select **Export** to export results to a .csv file.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="5618a-161">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="5618a-161">Next steps</span></span>

- [<span data-ttu-id="5618a-162">Afficher et approuver des actions de correction</span><span class="sxs-lookup"><span data-stu-id="5618a-162">View and approve remediation actions</span></span>](manage-auto-investigation.md)
- [<span data-ttu-id="5618a-163">Consultez le guide interactif : Examiner et corriger les menaces avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5618a-163">See the interactive guide: Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
 
## <a name="see-also"></a><span data-ttu-id="5618a-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5618a-164">See also</span></span>

- [<span data-ttu-id="5618a-165">Résoudre des faux négatifs/positifs dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5618a-165">Address false positives/negatives in Microsoft Defender for Endpoint</span></span>](defender-endpoint-false-positives-negatives.md)
