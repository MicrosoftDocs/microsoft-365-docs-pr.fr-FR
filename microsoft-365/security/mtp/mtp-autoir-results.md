---
title: Consulter les détails et les résultats d'un examen automatisé
description: Pendant et après un examen automatisé, vous pouvez afficher les résultats et les principales conclusions
keywords: automatisé, examen, résultats, analyse, détails, correction, autoair
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: d33844c1bd774f6b53dbbaa428762c4832fccb85
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40806983"
---
# <a name="view-the-details-and-results-of-an-automated-investigation"></a><span data-ttu-id="18627-104">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="18627-104">View the details and results of an automated investigation</span></span>

<span data-ttu-id="18627-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="18627-105">**Applies to:**</span></span>
- <span data-ttu-id="18627-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="18627-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="18627-107">Lorsqu'une enquête automatisée a lieu dans le Protection Microsoft contre les menaces, les détails concernant cet examen sont disponibles pendant et après le processus d'examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="18627-107">When an automated investigation occurs in Microsoft Threat Protection, details about that investigation are available during and after the automated investigation process.</span></span> <span data-ttu-id="18627-108">Si vous disposez des [autorisations nécessaires](mtp-action-center.md#required-permissions-for-action-center-tasks), vous pouvez afficher ces détails dans une vue Détails de l'examen.</span><span class="sxs-lookup"><span data-stu-id="18627-108">If you have the [necessary permissions](mtp-action-center.md#required-permissions-for-action-center-tasks), you can view those details in an investigation details view.</span></span> <span data-ttu-id="18627-109">La vue Détails de l’examen vous fournit l’État à jour et la possibilité d’approuver les actions en attente.</span><span class="sxs-lookup"><span data-stu-id="18627-109">The investigation details view provides you with up-to-date status and the ability to approve any pending actions.</span></span> 

![Détails de l’examen](../images/mtp-air-investdetails.png)

## <a name="open-the-investigation-details-view"></a><span data-ttu-id="18627-111">Ouvrir la vue Détails de l’examen</span><span class="sxs-lookup"><span data-stu-id="18627-111">Open the investigation details view</span></span>

<span data-ttu-id="18627-112">Vous pouvez ouvrir une vue Détails de l’examen avant impression comme suit :</span><span class="sxs-lookup"><span data-stu-id="18627-112">You can open the investigation details view by using one of the following methods:</span></span>
- [<span data-ttu-id="18627-113">Sélectionnez un élément dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="18627-113">Select an item in the Action center</span></span>](#select-an-item-in-the-action-center)
- [<span data-ttu-id="18627-114">Sélectionnez un examen dans une page de détails d’incident</span><span class="sxs-lookup"><span data-stu-id="18627-114">Select an investigation from an incident details page</span></span>](#open-an-investigation-from-an-incident-details-page)

### <a name="select-an-item-in-the-action-center"></a><span data-ttu-id="18627-115">Sélectionnez un élément dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="18627-115">Select an item in the Action center</span></span>

<span data-ttu-id="18627-116">Utilisez le centre de notifications pour afficher les actions en attente d’approbation (sous l’onglet **En attente**) ou qui ont déjà été approuvées (sous l’onglet **Historique**).</span><span class="sxs-lookup"><span data-stu-id="18627-116">Use the Action center to view actions that are either pending approval (on the **Pending** tab) or were already approved (on the **History** tab).</span></span> 

1. <span data-ttu-id="18627-117">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="18627-117">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="18627-118">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="18627-118">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="18627-119">Sous l’onglet **En attente** ou **Historique**, sélectionnez un élément.</span><span class="sxs-lookup"><span data-stu-id="18627-119">On either the **Pending** or **History** tab, select an item.</span></span> <span data-ttu-id="18627-120">Si vous disposez des [autorisations nécessaires](mtp-action-center.md#required-permissions-for-action-center-tasks), vous pouvez approuver (ou refuser) les actions en attente.</span><span class="sxs-lookup"><span data-stu-id="18627-120">If you have the [necessary permissions](mtp-action-center.md#required-permissions-for-action-center-tasks), you can approve (or reject) pending actions.</span></span>

### <a name="open-an-investigation-from-an-incident-details-page"></a><span data-ttu-id="18627-121">Ouvrez un examen dans une page de détails d’incident</span><span class="sxs-lookup"><span data-stu-id="18627-121">Open an investigation from an incident details page</span></span>

<span data-ttu-id="18627-122">La page Détails de l’incident permet d’afficher des informations détaillées sur un incident, notamment des alertes qui ont déclenché des informations sur les appareils, les comptes utilisateurs ou les boîtes aux lettres concernés.</span><span class="sxs-lookup"><span data-stu-id="18627-122">Use an incident details page to view detailed information about an incident, including alerts that were triggered information about any affected devices, user accounts, or mailboxes.</span></span>

1. <span data-ttu-id="18627-123">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="18627-123">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="18627-124">Dans le volet de navigation, choisissez **Incidents**.</span><span class="sxs-lookup"><span data-stu-id="18627-124">In the navigation pane, choose **Incidents**.</span></span> 

3. <span data-ttu-id="18627-125">Sélectionnez un élément dans la liste pour ouvrir la vue Détails de l’événement.</span><span class="sxs-lookup"><span data-stu-id="18627-125">Select an item in the list to open the incident details view.</span></span><br/>![Détails de l’incident](../images/mtp-incidentdetails-tabs.png)

4. <span data-ttu-id="18627-127">Sous l’onglet **Examen**, sélectionnez un examen dans la liste.</span><span class="sxs-lookup"><span data-stu-id="18627-127">On the **Investigations** tab, select an investigation in the list.</span></span>

## <a name="investigation-details"></a><span data-ttu-id="18627-128">Détails de l’examen</span><span class="sxs-lookup"><span data-stu-id="18627-128">Investigation details</span></span>

<span data-ttu-id="18627-129">Utilisez la vue Détails de l’examen pour afficher les activités passées, actuelles et en attente relatives à un examen.</span><span class="sxs-lookup"><span data-stu-id="18627-129">Use the investigation details view to see past, current, and pending activity pertaining to an investigation.</span></span> <span data-ttu-id="18627-130">La vue Détails de l’examen est semblable à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="18627-130">The investigation details view resembles the following image:</span></span>

![Détails de l’examen](../images/mtp-air-investdetails.png)

<span data-ttu-id="18627-132">Dans la vue Détails de l’examen, vous pouvez consulter des informations sur les onglets **Graphique de l'examen**, **Alertes**, **Appareils**, **Identités**, **Principales conclusions**, **Entités**, **Journal**et **Actions en attente**, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="18627-132">In the Investigation details view, you can see information on the **Investigation graph**, **Alerts**, **Devices**, **Identities**, **Key findings**, **Entities**, **Log**, and **Pending actions** tabs, described in the following table.</span></span>

|<span data-ttu-id="18627-133">Tab</span><span class="sxs-lookup"><span data-stu-id="18627-133">Tab</span></span>    |<span data-ttu-id="18627-134">Description</span><span class="sxs-lookup"><span data-stu-id="18627-134">Description</span></span> |
|--------|--------|
|<span data-ttu-id="18627-135">Graphique de l'examen</span><span class="sxs-lookup"><span data-stu-id="18627-135">Investigation graph</span></span>    |<span data-ttu-id="18627-136">Fournit une représentation visuelle de l’examen.</span><span class="sxs-lookup"><span data-stu-id="18627-136">Provides a visual representation of the investigation.</span></span> <span data-ttu-id="18627-137">Décrit les entités et répertorie de menaces détectées, ainsi que les alertes et l’attente d’une approbation.</span><span class="sxs-lookup"><span data-stu-id="18627-137">Depicts entities and lists threats found, along with alerts and whether any actions are awaiting approval.</span></span><br/><span data-ttu-id="18627-138">Vous pouvez cliquer sur un élément sur le graphique pour afficher plus de détails.</span><span class="sxs-lookup"><span data-stu-id="18627-138">You can click an item on the graph to view more details.</span></span> <span data-ttu-id="18627-139">Par exemple, en cliquant sur l’icône **Menaces détectées**, vous accédez à l'onglet **Principales conclusions**.</span><span class="sxs-lookup"><span data-stu-id="18627-139">For example, clicking the **Threats found** icon takes you to the **Key findings** tab.</span></span> |
|<span data-ttu-id="18627-140">Alertes</span><span class="sxs-lookup"><span data-stu-id="18627-140">Alerts</span></span> |<span data-ttu-id="18627-141">Répertorie les alertes associées à l’examen.</span><span class="sxs-lookup"><span data-stu-id="18627-141">Lists alerts associated with the investigation.</span></span> <span data-ttu-id="18627-142">Les alertes peuvent provenir de fonctionnalités de protection contre les menaces sur l’ordinateur d’un utilisateur, dans les applications Office, dans le Cloud App Security et d’autres fonctionnalités de Protection 365 Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="18627-142">Alerts can come from threat protection features on a user's machine, in Office apps, Cloud App Security, and other Microsoft 365 Threat Protection features.</span></span>|
|<span data-ttu-id="18627-143">Appareils</span><span class="sxs-lookup"><span data-stu-id="18627-143">Devices</span></span>|<span data-ttu-id="18627-144">Répertorie les ordinateurs inclus dans l’examen et le niveau de correction.</span><span class="sxs-lookup"><span data-stu-id="18627-144">Lists machines included in the investigation along with remediation level.</span></span>|
|<span data-ttu-id="18627-145">Principales conclusions</span><span class="sxs-lookup"><span data-stu-id="18627-145">Key findings</span></span>   |<span data-ttu-id="18627-146">Répertorie les résultats de l’examen, ainsi que l’État et les actions effectuées ou en attente.</span><span class="sxs-lookup"><span data-stu-id="18627-146">Lists results from the investigation along with status and actions taken or pending.</span></span> <span data-ttu-id="18627-147">Vous pouvez approuver les actions en attente pour les appareils et les identités dans sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="18627-147">You can approve pending actions for devices and identities in on this tab.</span></span>|
|<span data-ttu-id="18627-148">Entités</span><span class="sxs-lookup"><span data-stu-id="18627-148">Entities</span></span>   |<span data-ttu-id="18627-149">Répertorie les activités des utilisateurs, les fichiers, les processus, les services, les pilotes, les adresses IP et les méthodes de persistance associées à l’examen, ainsi que l’État et les actions prises.</span><span class="sxs-lookup"><span data-stu-id="18627-149">Lists user activities, files, processes, services, drivers, IP addresses, and persistence methods associated with the investigation, along with status and actions taken.</span></span>|
|<span data-ttu-id="18627-150">Journal</span><span class="sxs-lookup"><span data-stu-id="18627-150">Log</span></span>    |<span data-ttu-id="18627-151">Fournit une vue détaillée de toutes les étapes effectuées pendant l’examen, ainsi que de l’État.</span><span class="sxs-lookup"><span data-stu-id="18627-151">Provides a detailed view of all steps taken during the investigation, along with status.</span></span>|
|<span data-ttu-id="18627-152">Actions en attente</span><span class="sxs-lookup"><span data-stu-id="18627-152">Pending actions</span></span>    |<span data-ttu-id="18627-153">Répertorie les éléments qui nécessitent une approbation pour continuer.</span><span class="sxs-lookup"><span data-stu-id="18627-153">Lists items that require approval to proceed.</span></span>|

## <a name="remediation-actions-following-automated-investigation"></a><span data-ttu-id="18627-154">Correction des actions en attente suite à un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="18627-154">Remediation actions following automated investigation</span></span>

<span data-ttu-id="18627-155">Lorsqu’un examen automatisé se termine, un verdict est atteint pour chaque élément de preuve impliqué et des actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="18627-155">When an automated investigation completes, a verdict is reached for every piece of evidence involved, and remediation actions are identified.</span></span> <span data-ttu-id="18627-156">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="18627-156">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="18627-157">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="18627-157">The following table lists possible verdicts and outcomes:</span></span>

|<span data-ttu-id="18627-158">Verdict</span><span class="sxs-lookup"><span data-stu-id="18627-158">Verdict</span></span>    |<span data-ttu-id="18627-159">Domaine</span><span class="sxs-lookup"><span data-stu-id="18627-159">Area</span></span>   |<span data-ttu-id="18627-160">Résultats</span><span class="sxs-lookup"><span data-stu-id="18627-160">Outcomes</span></span>|
|------|------|------|
|<span data-ttu-id="18627-161">Malveillant</span><span class="sxs-lookup"><span data-stu-id="18627-161">Malicious</span></span>  |<span data-ttu-id="18627-162">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="18627-162">Devices (endpoints)</span></span>    |<span data-ttu-id="18627-163">Les actions d'assainissement prennent automatiquement effet</span><span class="sxs-lookup"><span data-stu-id="18627-163">Remediation actions are taken automatically</span></span>|
|<span data-ttu-id="18627-164">Malveillant</span><span class="sxs-lookup"><span data-stu-id="18627-164">Malicious</span></span>  |<span data-ttu-id="18627-165">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="18627-165">Email content (URLs or attachments)</span></span> | <span data-ttu-id="18627-166">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="18627-166">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="18627-167">Suspect</span><span class="sxs-lookup"><span data-stu-id="18627-167">Suspicious</span></span> |<span data-ttu-id="18627-168">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="18627-168">Devices or email content</span></span> |<span data-ttu-id="18627-169">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="18627-169">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="18627-170">Nettoyer</span><span class="sxs-lookup"><span data-stu-id="18627-170">Clean</span></span>  |<span data-ttu-id="18627-171">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="18627-171">Devices or email content</span></span>   |<span data-ttu-id="18627-172">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="18627-172">No remediation actions are needed</span></span>|

[<span data-ttu-id="18627-173">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="18627-173">Review a pending action in the Action center</span></span>](mtp-autoir-actions.md#review-a-pending-action-in-the-action-center)

## <a name="next-steps"></a><span data-ttu-id="18627-174">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="18627-174">Next steps</span></span>

- [<span data-ttu-id="18627-175">Obtenir une vue d’ensemble des autorisations du centre de notifications</span><span class="sxs-lookup"><span data-stu-id="18627-175">Get an overview of Action center permissions</span></span>](mtp-action-center.md#required-permissions-for-action-center-tasks)
- [<span data-ttu-id="18627-176">Approuver ou refuser les actions liées à un examen et réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="18627-176">Approve or reject actions related to automated investigation and response</span></span>](mtp-autoir-actions.md)

