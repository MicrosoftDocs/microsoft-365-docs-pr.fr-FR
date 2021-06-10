---
title: Détails et résultats d’une enquête automatisée
description: Afficher les résultats et les principales conclusions de l’examen automatisé dans Microsoft 365 Defender
keywords: automatisé, examen, résultats, analyse, détails, correction, autoair
search.appverid: met150
ms.prod: m365-security
ms.technology: m365d
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.openlocfilehash: ad774fc36f4f167cb7a4e695b9f572ceb55b968b
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274675"
---
# <a name="details-and-results-of-an-automated-investigation"></a><span data-ttu-id="f0a29-104">Détails et résultats d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="f0a29-104">Details and results of an automated investigation</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="f0a29-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f0a29-105">**Applies to:**</span></span>
- <span data-ttu-id="f0a29-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f0a29-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="f0a29-107">Avec Microsoft 365 Defender, lorsqu’une enquête automatisée s’exécute, des détails sur cet examen sont disponibles pendant et après le processus d’examen automatisé. [](m365d-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="f0a29-107">With Microsoft 365 Defender, when an [automated investigation](m365d-autoir.md) runs, details about that investigation are available both during and after the automated investigation process.</span></span> <span data-ttu-id="f0a29-108">Si vous disposez des [autorisations nécessaires](m365d-action-center.md#required-permissions-for-action-center-tasks), vous pouvez afficher ces détails dans une vue Détails de l'examen.</span><span class="sxs-lookup"><span data-stu-id="f0a29-108">If you have the [necessary permissions](m365d-action-center.md#required-permissions-for-action-center-tasks), you can view those details in an investigation details view.</span></span> <span data-ttu-id="f0a29-109">Cette vue vous fournit l’état à jour et la possibilité d’approuver les actions en attente.</span><span class="sxs-lookup"><span data-stu-id="f0a29-109">This view provides you with up-to-date status and the ability to approve any pending actions.</span></span> 

![Détails de l’examen](../../media/mtp-air-investdetails.png)

## <a name="new-unified-investigation-page"></a><span data-ttu-id="f0a29-111">(NOUVEAU!) Page Examen unifié</span><span class="sxs-lookup"><span data-stu-id="f0a29-111">(NEW!) Unified investigation page</span></span>

<span data-ttu-id="f0a29-112">La page d’examen a récemment été mise à jour pour inclure des informations sur vos appareils, votre courrier électronique et le contenu de collaboration.</span><span class="sxs-lookup"><span data-stu-id="f0a29-112">The investigation page has recently been updated to include information across your devices, email, and collaboration content.</span></span> <span data-ttu-id="f0a29-113">La nouvelle page d’enquête unifiée définit un langage commun et fournit une expérience unifiée pour les examens automatiques dans Microsoft Defender pour [Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) et [Microsoft Defender pour Office 365](../office-365-security/defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="f0a29-113">The new, unified investigation page defines a common language and provides a unified experience for automatic investigations across [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) and [Microsoft Defender for Office 365](../office-365-security/defender-for-office-365.md).</span></span> <span data-ttu-id="f0a29-114">Pour accéder à la page d’enquête unifiée, sélectionnez le lien dans la bannière jaune qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="f0a29-114">To access the unified investigation page, select the link in the yellow banner you'll see on:</span></span>

- <span data-ttu-id="f0a29-115">N’importe quelle page d’enquête dans Office 365 centre de sécurité & conformité ( [https://protection.office.com](https://protection.office.com) )</span><span class="sxs-lookup"><span data-stu-id="f0a29-115">Any investigation page in the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com))</span></span>
- <span data-ttu-id="f0a29-116">N’importe quelle page d’enquête dans le Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) )</span><span class="sxs-lookup"><span data-stu-id="f0a29-116">Any investigation page in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com))</span></span>
- <span data-ttu-id="f0a29-117">Toute expérience d’incident ou de centre de Microsoft 365 centre de sécurité ( [https://security.microsoft.com](https://security.microsoft.com) )</span><span class="sxs-lookup"><span data-stu-id="f0a29-117">Any incident or Action center experience in the Microsoft 365 security center ([https://security.microsoft.com](https://security.microsoft.com))</span></span>

## <a name="open-the-investigation-details-view"></a><span data-ttu-id="f0a29-118">Ouvrir la vue Détails de l’examen</span><span class="sxs-lookup"><span data-stu-id="f0a29-118">Open the investigation details view</span></span>

<span data-ttu-id="f0a29-119">Vous pouvez ouvrir une vue Détails de l’examen avant impression comme suit :</span><span class="sxs-lookup"><span data-stu-id="f0a29-119">You can open the investigation details view by using one of the following methods:</span></span>

- [<span data-ttu-id="f0a29-120">Sélectionnez un élément dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="f0a29-120">Select an item in the Action center</span></span>](#select-an-item-in-the-action-center)
- [<span data-ttu-id="f0a29-121">Sélectionnez un examen dans une page de détails d’incident</span><span class="sxs-lookup"><span data-stu-id="f0a29-121">Select an investigation from an incident details page</span></span>](#open-an-investigation-from-an-incident-details-page)

### <a name="select-an-item-in-the-action-center"></a><span data-ttu-id="f0a29-122">Sélectionnez un élément dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="f0a29-122">Select an item in the Action center</span></span>

<span data-ttu-id="f0a29-123">Le centre de [mesures](m365d-action-center.md) amélioré regroupe les actions de correction sur vos appareils, la messagerie & le contenu [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) de collaboration et les identités. [](m365d-remediation-actions.md)</span><span class="sxs-lookup"><span data-stu-id="f0a29-123">The improved [Action center](m365d-action-center.md) ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) brings together [remediation actions](m365d-remediation-actions.md) across your devices, email & collaboration content, and identities.</span></span> <span data-ttu-id="f0a29-124">Les actions répertoriées incluent des actions de correction qui ont été prises automatiquement ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="f0a29-124">Listed actions include remediation actions that were taken automatically or manually.</span></span> <span data-ttu-id="f0a29-125">Dans le centre de actions, vous pouvez afficher les actions en attente d’approbation et les actions qui ont déjà été approuvées ou terminées.</span><span class="sxs-lookup"><span data-stu-id="f0a29-125">In the Action center, you can view actions that are awaiting approval and actions that were already approved or completed.</span></span> <span data-ttu-id="f0a29-126">Vous pouvez également accéder à d’autres détails, tels qu’une page d’enquête.</span><span class="sxs-lookup"><span data-stu-id="f0a29-126">You can also navigate to more details, such as an investigation page.</span></span>

> [!TIP]
> <span data-ttu-id="f0a29-127">Vous devez avoir [certaines autorisations pour](m365d-action-center.md#required-permissions-for-action-center-tasks) approuver, rejeter ou annuler des actions.</span><span class="sxs-lookup"><span data-stu-id="f0a29-127">You must have [certain permissions](m365d-action-center.md#required-permissions-for-action-center-tasks) to approve, reject, or undo actions.</span></span>

1. <span data-ttu-id="f0a29-128">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f0a29-128">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="f0a29-129">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="f0a29-129">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="f0a29-130">Sous l’onglet **En attente** ou **Historique**, sélectionnez un élément.</span><span class="sxs-lookup"><span data-stu-id="f0a29-130">On either the **Pending** or **History** tab, select an item.</span></span> <span data-ttu-id="f0a29-131">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f0a29-131">Its flyout pane opens.</span></span>

4. <span data-ttu-id="f0a29-132">Examinez les informations dans le volet volant, puis prenez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0a29-132">Review the information in the flyout pane, and then take one of the following steps:</span></span>
   - <span data-ttu-id="f0a29-133">Sélectionnez **Ouvrir la page Examen** pour afficher plus de détails sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="f0a29-133">Select **Open investigation page** to view more details about the investigation.</span></span>
   - <span data-ttu-id="f0a29-134">Sélectionnez **Approuver** pour lancer une action en attente.</span><span class="sxs-lookup"><span data-stu-id="f0a29-134">Select **Approve** to initiate a pending action.</span></span>
   - <span data-ttu-id="f0a29-135">Sélectionnez **Rejeter** pour empêcher une action en attente d’être prise.</span><span class="sxs-lookup"><span data-stu-id="f0a29-135">Select **Reject** to prevent a pending action from being taken.</span></span>
   - <span data-ttu-id="f0a29-136">Sélectionnez **Go hunt** (Aller à la recherche) pour aller [dans le recherche avancée](advanced-hunting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0a29-136">Select **Go hunt** to go into [Advanced hunting](advanced-hunting-overview.md).</span></span>

### <a name="open-an-investigation-from-an-incident-details-page"></a><span data-ttu-id="f0a29-137">Ouvrez un examen dans une page de détails d’incident</span><span class="sxs-lookup"><span data-stu-id="f0a29-137">Open an investigation from an incident details page</span></span>

<span data-ttu-id="f0a29-138">La page Détails de l’incident permet d’afficher des informations détaillées sur un incident, notamment des alertes qui ont déclenché des informations sur les appareils, les comptes utilisateurs ou les boîtes aux lettres concernés.</span><span class="sxs-lookup"><span data-stu-id="f0a29-138">Use an incident details page to view detailed information about an incident, including alerts that were triggered information about any affected devices, user accounts, or mailboxes.</span></span>

1. <span data-ttu-id="f0a29-139">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f0a29-139">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="f0a29-140">Dans le volet de navigation, sélectionnez **Incidents &**  >  **alertes Incidents**.</span><span class="sxs-lookup"><span data-stu-id="f0a29-140">In the navigation pane, choose **Incidents & alerts** > **Incidents**.</span></span> 

3. <span data-ttu-id="f0a29-141">Sélectionnez un élément dans la liste, puis choisissez **Ouvrir la page Incident.**</span><span class="sxs-lookup"><span data-stu-id="f0a29-141">Select an item in the list, and then choose **Open incident page**.</span></span>

4. <span data-ttu-id="f0a29-142">Sélectionnez **l’onglet** Examens, puis un examen dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f0a29-142">Select the **Investigations** tab, and then select an investigation in the list.</span></span> <span data-ttu-id="f0a29-143">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f0a29-143">Its flyout pane opens.</span></span>

5. <span data-ttu-id="f0a29-144">Sélectionnez **Ouvrir la page Examen.**</span><span class="sxs-lookup"><span data-stu-id="f0a29-144">Select **Open investigation page**.</span></span> 

<span data-ttu-id="f0a29-145">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="f0a29-145">Here's an example.</span></span>

![Détails de l’incident](../../media/mtp-incidentdetails-tabs.png)

## <a name="investigation-details"></a><span data-ttu-id="f0a29-147">Détails de l’examen</span><span class="sxs-lookup"><span data-stu-id="f0a29-147">Investigation details</span></span>

<span data-ttu-id="f0a29-148">Utilisez la vue Détails de l’examen pour afficher les activités passées, actuelles et en attente relatives à un examen.</span><span class="sxs-lookup"><span data-stu-id="f0a29-148">Use the investigation details view to see past, current, and pending activity pertaining to an investigation.</span></span> <span data-ttu-id="f0a29-149">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="f0a29-149">Here's an example.</span></span>

![Détails de l’examen](../../media/mtp-air-investdetails.png)

<span data-ttu-id="f0a29-151">Dans la vue Détails de l’examen, vous pouvez consulter des informations sur les onglets **Graphique de l'examen**, **Alertes**, **Appareils**, **Identités**, **Principales conclusions**, **Entités**, **Journal** et **Actions en attente**, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f0a29-151">In the Investigation details view, you can see information on the **Investigation graph**, **Alerts**, **Devices**, **Identities**, **Key findings**, **Entities**, **Log**, and **Pending actions** tabs, described in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="f0a29-152">Les onglets spécifiques que vous voyez dans une page de détails d’enquête dépendent de ce que comprend votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0a29-152">The specific tabs you see in an investigation details page depends on what your subscription includes.</span></span> <span data-ttu-id="f0a29-153">Par exemple, si votre abonnement n’inclut pas Microsoft Defender pour Office 365 Plan 2, vous ne verrez pas d’onglet **Boîtes aux** lettres.</span><span class="sxs-lookup"><span data-stu-id="f0a29-153">For example, if your subscription does not include Microsoft Defender for Office 365 Plan 2, you won't see a **Mailboxes** tab.</span></span>

| <span data-ttu-id="f0a29-154">Tab</span><span class="sxs-lookup"><span data-stu-id="f0a29-154">Tab</span></span> | <span data-ttu-id="f0a29-155">Description</span><span class="sxs-lookup"><span data-stu-id="f0a29-155">Description</span></span> |
|:--------|:--------|
| <span data-ttu-id="f0a29-156">**Graphique de l'examen**</span><span class="sxs-lookup"><span data-stu-id="f0a29-156">**Investigation graph**</span></span>   | <span data-ttu-id="f0a29-157">Fournit une représentation visuelle de l’examen.</span><span class="sxs-lookup"><span data-stu-id="f0a29-157">Provides a visual representation of the investigation.</span></span> <span data-ttu-id="f0a29-158">Décrit les entités et répertorie de menaces détectées, ainsi que les alertes et l’attente d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="f0a29-158">Depicts entities and lists threats found, along with alerts and whether any actions are awaiting approval.</span></span><br/><span data-ttu-id="f0a29-159">Vous pouvez sélectionner un élément sur le graphique pour afficher plus de détails.</span><span class="sxs-lookup"><span data-stu-id="f0a29-159">You can select an item on the graph to view more details.</span></span> <span data-ttu-id="f0a29-160">Par exemple, la sélection de l’icône **Preuve** vous permet d’utiliser l’onglet Preuves, où vous pouvez voir les entités détectées et leurs verdicts. </span><span class="sxs-lookup"><span data-stu-id="f0a29-160">For example, selecting the **Evidence** icon takes you to the **Evidence** tab, where you can see detected entities and their verdicts.</span></span> |
| <span data-ttu-id="f0a29-161">**Alertes**</span><span class="sxs-lookup"><span data-stu-id="f0a29-161">**Alerts**</span></span>    | <span data-ttu-id="f0a29-162">Répertorie les alertes associées à l’examen.</span><span class="sxs-lookup"><span data-stu-id="f0a29-162">Lists alerts associated with the investigation.</span></span> <span data-ttu-id="f0a29-163">Les alertes peuvent être le fait de fonctionnalités de protection contre les menaces sur l’appareil d’un utilisateur, dans Office applications, Microsoft Cloud App Security et d’autres fonctionnalités Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="f0a29-163">Alerts can come from threat protection features on a user's device, in Office apps, Microsoft Cloud App Security, and other Microsoft 365 Defender features.</span></span>|
| <span data-ttu-id="f0a29-164">**Appareils**</span><span class="sxs-lookup"><span data-stu-id="f0a29-164">**Devices**</span></span> | <span data-ttu-id="f0a29-165">Répertorie les appareils inclus dans l’examen, ainsi que leur niveau de correction.</span><span class="sxs-lookup"><span data-stu-id="f0a29-165">Lists devices included in the investigation along with their remediation level.</span></span> <span data-ttu-id="f0a29-166">(Les niveaux de correction correspondent [au niveau d’automatisation des groupes d’appareils.)](m365d-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups)</span><span class="sxs-lookup"><span data-stu-id="f0a29-166">(Remediation levels correspond to [the automation level for device groups](m365d-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups).)</span></span> |
| <span data-ttu-id="f0a29-167">**Boîtes aux lettres**</span><span class="sxs-lookup"><span data-stu-id="f0a29-167">**Mailboxes**</span></span> |<span data-ttu-id="f0a29-168">Répertorie les boîtes aux lettres qui sont touchées par les menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="f0a29-168">Lists mailboxes that are impacted by detected threats.</span></span>  |
| <span data-ttu-id="f0a29-169">**Utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="f0a29-169">**Users**</span></span>  | <span data-ttu-id="f0a29-170">Répertorie les comptes d’utilisateurs qui sont touchés par les menaces détectées.</span><span class="sxs-lookup"><span data-stu-id="f0a29-170">Lists user accounts that are impacted by detected threats.</span></span> |
| <span data-ttu-id="f0a29-171">**Preuve**</span><span class="sxs-lookup"><span data-stu-id="f0a29-171">**Evidence**</span></span> | <span data-ttu-id="f0a29-172">Répertorie les éléments de preuve élevés par des alertes ou des enquêtes.</span><span class="sxs-lookup"><span data-stu-id="f0a29-172">Lists pieces of evidence raised by alerts or investigations.</span></span> <span data-ttu-id="f0a29-173">Inclut les verdicts (*malveillant,* *suspect,* *inconnu* ou aucune menace *trouvée)* et l’état de correction.</span><span class="sxs-lookup"><span data-stu-id="f0a29-173">Includes verdicts (*Malicious*, *Suspicious*, *Unknown*, or *No threats found*) and remediation status.</span></span> |
| <span data-ttu-id="f0a29-174">**Entities**</span><span class="sxs-lookup"><span data-stu-id="f0a29-174">**Entities**</span></span>  | <span data-ttu-id="f0a29-175">Fournit des détails sur chaque entité analysée, y compris un verdict pour chaque type d’entité *(* *malveillant,* suspect ou aucune *menace trouvée).*</span><span class="sxs-lookup"><span data-stu-id="f0a29-175">Provides details about each analyzed entity, including a verdict for each entity type (*Malicious*, *Suspicious*, or *No threats found*).</span></span>|
|<span data-ttu-id="f0a29-176">**Log**</span><span class="sxs-lookup"><span data-stu-id="f0a29-176">**Log**</span></span>    | <span data-ttu-id="f0a29-177">Fournit une vue chronologique et détaillée de toutes les actions d’investigation entreprises après le déclenchement d’une alerte.</span><span class="sxs-lookup"><span data-stu-id="f0a29-177">Provides a chronological, detailed view of all the investigation actions taken after an alert was triggered.</span></span>|
| <span data-ttu-id="f0a29-178">**Historique des actions en attente**</span><span class="sxs-lookup"><span data-stu-id="f0a29-178">**Pending actions history**</span></span> | <span data-ttu-id="f0a29-179">Répertorie les éléments qui nécessitent une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="f0a29-179">Lists items that require approval to proceed.</span></span> <span data-ttu-id="f0a29-180">Go to the Action center ( [https://security.microsoft.com/action-center](https://security.microsoft.com/action-center) ) to approve pending actions.</span><span class="sxs-lookup"><span data-stu-id="f0a29-180">Go to the Action center ([https://security.microsoft.com/action-center](https://security.microsoft.com/action-center)) to approve pending actions.</span></span> |

## <a name="next-steps"></a><span data-ttu-id="f0a29-181">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="f0a29-181">Next steps</span></span>

- [<span data-ttu-id="f0a29-182">Afficher et gérer les actions de correction</span><span class="sxs-lookup"><span data-stu-id="f0a29-182">View and manage remediation actions</span></span>](m365d-autoir-actions.md)
- [<span data-ttu-id="f0a29-183">En savoir plus sur les actions de correction</span><span class="sxs-lookup"><span data-stu-id="f0a29-183">Learn more about remediation actions</span></span>](m365d-remediation-actions.md)
