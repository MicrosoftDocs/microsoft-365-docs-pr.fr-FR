---
title: Afficher les résultats d’une enquête automatisée dans Microsoft 365
keywords: AIR, autoIR, ATP, automatisé, examen, correction, actions
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Pendant et après un examen automatisé dans Microsoft 365, vous pouvez afficher les résultats et les résultats clés.
ms.date: 01/29/2021
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 8bf18a9fb80805581a1439b3965a664fd0868248
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065614"
---
# <a name="details-and-results-of-an-automated-investigation-in-microsoft-365"></a><span data-ttu-id="8f7da-104">Détails et résultats d’une enquête automatisée dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8f7da-104">Details and results of an automated investigation in Microsoft 365</span></span>

<span data-ttu-id="8f7da-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8f7da-105">**Applies to**</span></span>
- [<span data-ttu-id="8f7da-106">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="8f7da-106">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="8f7da-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8f7da-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="8f7da-108">[Lorsqu’une enquête automatisée](office-365-air.md) se produit dans Microsoft Defender pour [Office 365,](defender-for-office-365.md)des détails sur cette enquête sont disponibles pendant et après le processus d’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="8f7da-108">When an [automated investigation](office-365-air.md) occurs in [Microsoft Defender for Office 365](defender-for-office-365.md), details about that investigation are available during and after the automated investigation process.</span></span> <span data-ttu-id="8f7da-109">Si vous avez les autorisations nécessaires, vous pouvez afficher ces détails dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8f7da-109">If you have the necessary permissions, you can view those details in the Microsoft 365 security center.</span></span> <span data-ttu-id="8f7da-110">Les détails de l’examen vous fournissent l’état à jour et la possibilité d’approuver les actions en attente.</span><span class="sxs-lookup"><span data-stu-id="8f7da-110">Investigation details provide you with up-to-date status, and the ability to approve any pending actions.</span></span>

> [!TIP]
> <span data-ttu-id="8f7da-111">Consultez la nouvelle page d’examen unifié dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8f7da-111">Check out the new, unified investigation page in the Microsoft 365 security center.</span></span> <span data-ttu-id="8f7da-112">Pour en savoir plus, [voir (NOUVEAU!) Page d’examen unifié](../defender/m365d-autoir-results.md#new-unified-investigation-page).</span><span class="sxs-lookup"><span data-stu-id="8f7da-112">To learn more, see [(NEW!) Unified investigation page](../defender/m365d-autoir-results.md#new-unified-investigation-page).</span></span>

## <a name="investigation-status"></a><span data-ttu-id="8f7da-113">État de l’examen</span><span class="sxs-lookup"><span data-stu-id="8f7da-113">Investigation status</span></span>

<span data-ttu-id="8f7da-114">L’état de l’examen indique la progression de l’analyse et des actions.</span><span class="sxs-lookup"><span data-stu-id="8f7da-114">The investigation status indicates the progress of the analysis and actions.</span></span> <span data-ttu-id="8f7da-115">Au cours de l’examen, l’état change pour indiquer si des menaces ont été trouvées et si des actions ont été approuvées.</span><span class="sxs-lookup"><span data-stu-id="8f7da-115">As the investigation runs, status changes to indicate whether threats were found, and whether actions have been approved.</span></span>

|<span data-ttu-id="8f7da-116">Statut</span><span class="sxs-lookup"><span data-stu-id="8f7da-116">Status</span></span>|<span data-ttu-id="8f7da-117">Description</span><span class="sxs-lookup"><span data-stu-id="8f7da-117">Description</span></span>|
|:---|:---|
|<span data-ttu-id="8f7da-118">**Démarrage**</span><span class="sxs-lookup"><span data-stu-id="8f7da-118">**Starting**</span></span>|<span data-ttu-id="8f7da-119">L’enquête a été déclenchée et en attente de démarrage de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8f7da-119">The investigation has been triggered and waiting to start running.</span></span>|
|<span data-ttu-id="8f7da-120">**En cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="8f7da-120">**Running**</span></span>|<span data-ttu-id="8f7da-121">Le processus d’examen a démarré et est en cours.</span><span class="sxs-lookup"><span data-stu-id="8f7da-121">The investigation process has started and is underway.</span></span> <span data-ttu-id="8f7da-122">Cet état se produit également lorsque les [actions en attente sont](air-review-approve-pending-completed-actions.md#approve-or-reject-pending-actions) approuvées.</span><span class="sxs-lookup"><span data-stu-id="8f7da-122">This state also occurs when [pending actions](air-review-approve-pending-completed-actions.md#approve-or-reject-pending-actions) are approved.</span></span>|
|<span data-ttu-id="8f7da-123">**Aucune menace trouvée**</span><span class="sxs-lookup"><span data-stu-id="8f7da-123">**No Threats Found**</span></span>|<span data-ttu-id="8f7da-124">L’enquête est terminée et aucune menace (compte d’utilisateur, message électronique, URL ou fichier) n’a été identifiée.</span><span class="sxs-lookup"><span data-stu-id="8f7da-124">The investigation has finished and no threats (user account, email message, URL, or file) were identified.</span></span> <p> <span data-ttu-id="8f7da-125">**CONSEIL**: si vous pensez que quelque chose a été manqué (tel qu’un faux négatif), vous pouvez prendre des mesures à l’aide de [l’Explorateur de menaces.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="8f7da-125">**TIP**: If you suspect something was missed (such as a false negative), you can take action using [Threat Explorer](threat-explorer.md).</span></span>|
|<span data-ttu-id="8f7da-126">**Menaces détectées**</span><span class="sxs-lookup"><span data-stu-id="8f7da-126">**Threats Found**</span></span>|<span data-ttu-id="8f7da-127">L’examen automatisé a trouvé des problèmes, mais il n’existe aucune action de correction spécifique pour résoudre ces problèmes.</span><span class="sxs-lookup"><span data-stu-id="8f7da-127">The automated investigation found issues, but there are no specific remediation actions to resolve those issues.</span></span> <p> <span data-ttu-id="8f7da-128">**L’état Menaces** trouvées peut se produire lorsqu’un type d’activité utilisateur a été identifié, mais qu’aucune action de nettoyage n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="8f7da-128">The **Threats Found** status can occur when some type of user activity was identified but no cleanup actions are available.</span></span> <span data-ttu-id="8f7da-129">Voici quelques exemples d’activités utilisateur :</span><span class="sxs-lookup"><span data-stu-id="8f7da-129">Examples include any of the following user activities:</span></span> <br/><span data-ttu-id="8f7da-130">- Un événement [de protection contre la](../../compliance/data-loss-prevention-policies.md) perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="8f7da-130">- A [data loss prevention](../../compliance/data-loss-prevention-policies.md) (DLP) event</span></span><br/><span data-ttu-id="8f7da-131">- Une anomalie d’envoi de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="8f7da-131">- An email sending anomaly</span></span><br/><span data-ttu-id="8f7da-132">- Programmes malveillants envoyés</span><span class="sxs-lookup"><span data-stu-id="8f7da-132">- Sent malware</span></span><br/><span data-ttu-id="8f7da-133">- Hameçonnage envoyé</span><span class="sxs-lookup"><span data-stu-id="8f7da-133">- Sent phish</span></span> <p> <span data-ttu-id="8f7da-134">L’examen n’a trouvé aucune URL, aucun fichier ou message électronique malveillant à corriger, ni aucune activité de boîte aux lettres à corriger, telle que la non-remise des règles de forwarding ou de la délégation.</span><span class="sxs-lookup"><span data-stu-id="8f7da-134">The investigation found no malicious URLs, files, or email messages to remediate, and no mailbox activity to fix, such as turning off forwarding rules or delegation.</span></span> <p> <span data-ttu-id="8f7da-135">**CONSEIL**: si vous pensez que quelque chose a été manqué (tel qu’un faux négatif), vous pouvez examiner et prendre des mesures à l’aide de [l’Explorateur de menaces.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="8f7da-135">**TIP**: If you suspect something was missed (such as a false negative), you can investigate and take action using [Threat Explorer](threat-explorer.md).</span></span>|
|<span data-ttu-id="8f7da-136">**Terminated By System**</span><span class="sxs-lookup"><span data-stu-id="8f7da-136">**Terminated By System**</span></span>|<span data-ttu-id="8f7da-137">L’examen a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="8f7da-137">The investigation stopped.</span></span> <span data-ttu-id="8f7da-138">Une enquête peut s’arrêter pour plusieurs raisons :</span><span class="sxs-lookup"><span data-stu-id="8f7da-138">An investigation can stop for several reasons:</span></span> <br/><span data-ttu-id="8f7da-139">- Les actions en attente de l’examen ont expiré.</span><span class="sxs-lookup"><span data-stu-id="8f7da-139">- The investigation's pending actions expired.</span></span> <span data-ttu-id="8f7da-140">Le délai d’attente des actions en attente d’approbation est de 1 semaine.</span><span class="sxs-lookup"><span data-stu-id="8f7da-140">Pending actions time out after awaiting approval for one week.</span></span><br/><span data-ttu-id="8f7da-141">- Il y a trop d’actions.</span><span class="sxs-lookup"><span data-stu-id="8f7da-141">- There are too many actions.</span></span> <span data-ttu-id="8f7da-142">Par exemple, s’il y a trop d’utilisateurs qui cliquent sur des URL malveillantes, cela peut aller au-delà de la capacité de l’examen à exécuter tous les analyseurs, de sorte que l’enquête s’arrête.</span><span class="sxs-lookup"><span data-stu-id="8f7da-142">For example, if there are too many users clicking on malicious URLs, it can exceed the investigation's ability to run all the analyzers, so the investigation halts.</span></span><p> <span data-ttu-id="8f7da-143">**CONSEIL :** si un examen s’arrête avant que des mesures ne sont prises, essayez d’utiliser l’Explorateur de menaces [pour](threat-explorer.md) rechercher et résoudre les menaces.</span><span class="sxs-lookup"><span data-stu-id="8f7da-143">**TIP**: If an investigation halts before actions were taken, try using [Threat Explorer](threat-explorer.md) to find and address threats.</span></span>|
|<span data-ttu-id="8f7da-144">**Action en attente**</span><span class="sxs-lookup"><span data-stu-id="8f7da-144">**Pending Action**</span></span>|<span data-ttu-id="8f7da-145">L’enquête a trouvé une menace, telle qu’un e-mail malveillant, une URL malveillante ou un paramètre de boîte aux lettres à risque, et une action pour corriger cette menace est en attente [d’approbation.](air-review-approve-pending-completed-actions.md)</span><span class="sxs-lookup"><span data-stu-id="8f7da-145">The investigation has found a threat, such as a malicious email, a malicious URL, or a risky mailbox setting, and an action to remediate that threat is [awaiting approval](air-review-approve-pending-completed-actions.md).</span></span> <p> <span data-ttu-id="8f7da-146">**L’état Action en attente** est déclenché lorsqu’une menace avec une action correspondante est trouvée.</span><span class="sxs-lookup"><span data-stu-id="8f7da-146">The **Pending Action** state is triggered when any threat with a corresponding action is found.</span></span> <span data-ttu-id="8f7da-147">Toutefois, la liste des actions en attente peut augmenter au cours d’une enquête.</span><span class="sxs-lookup"><span data-stu-id="8f7da-147">However, the list of pending actions can increase as an investigation runs.</span></span> <span data-ttu-id="8f7da-148">Affichez les détails de l’examen pour voir si d’autres éléments sont en attente d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="8f7da-148">View investigation details to see if other items are still pending completion.</span></span>|
|<span data-ttu-id="8f7da-149">**Corrigé**</span><span class="sxs-lookup"><span data-stu-id="8f7da-149">**Remediated**</span></span>|<span data-ttu-id="8f7da-150">L’examen s’est terminé et toutes les actions de correction ont été approuvées (notées comme étant entièrement corrigés).</span><span class="sxs-lookup"><span data-stu-id="8f7da-150">The investigation finished and all remediation actions were approved (noted as fully remediated).</span></span> <p> <span data-ttu-id="8f7da-151">**REMARQUE**: les actions de correction approuvées peuvent avoir des erreurs qui empêchent les actions d’être prises.</span><span class="sxs-lookup"><span data-stu-id="8f7da-151">**NOTE**: Approved remediation actions can have errors that prevent the actions from being taken.</span></span> <span data-ttu-id="8f7da-152">Que les actions de correction soient effectuées avec succès ou non, l’état de l’examen ne change pas.</span><span class="sxs-lookup"><span data-stu-id="8f7da-152">Regardless of whether remediation actions are successfully completed, the investigation status does not change.</span></span> <span data-ttu-id="8f7da-153">Afficher les détails de l’examen.</span><span class="sxs-lookup"><span data-stu-id="8f7da-153">View investigation details.</span></span>|
|<span data-ttu-id="8f7da-154">**Correction partielle**</span><span class="sxs-lookup"><span data-stu-id="8f7da-154">**Partially Remediated**</span></span>|<span data-ttu-id="8f7da-155">L’examen a entraîné des actions de correction, dont certaines ont été approuvées et terminées.</span><span class="sxs-lookup"><span data-stu-id="8f7da-155">The investigation resulted in remediation actions, and some were approved and completed.</span></span> <span data-ttu-id="8f7da-156">D’autres actions sont [toujours en attente.](air-review-approve-pending-completed-actions.md)</span><span class="sxs-lookup"><span data-stu-id="8f7da-156">Other actions are still [pending](air-review-approve-pending-completed-actions.md).</span></span>|
|<span data-ttu-id="8f7da-157">**Échec**</span><span class="sxs-lookup"><span data-stu-id="8f7da-157">**Failed**</span></span>|<span data-ttu-id="8f7da-158">Au moins un analyseur d’examen a rencontré un problème dans lequel il n’a pas pu se terminer correctement.</span><span class="sxs-lookup"><span data-stu-id="8f7da-158">At least one investigation analyzer ran into a problem where it could not complete properly.</span></span> <p> <span data-ttu-id="8f7da-159">**REMARQUE**: si un examen échoue après l’approbation des actions de correction, les actions de correction ont peut-être encore réussi.</span><span class="sxs-lookup"><span data-stu-id="8f7da-159">**NOTE**: If an investigation fails after remediation actions were approved, the remediation actions might still have succeeded.</span></span> <span data-ttu-id="8f7da-160">Afficher les détails de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="8f7da-160">View the investigation details.</span></span> |
|<span data-ttu-id="8f7da-161">**Mis en file d’attente par limitation**</span><span class="sxs-lookup"><span data-stu-id="8f7da-161">**Queued By Throttling**</span></span>|<span data-ttu-id="8f7da-162">Un examen est placé dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8f7da-162">An investigation is being held in a queue.</span></span> <span data-ttu-id="8f7da-163">Lorsque d’autres enquêtes sont terminées, les enquêtes en file d’attente commencent.</span><span class="sxs-lookup"><span data-stu-id="8f7da-163">When other investigations complete, queued investigations begin.</span></span> <span data-ttu-id="8f7da-164">La limitation permet d’éviter des performances de service médiocres.</span><span class="sxs-lookup"><span data-stu-id="8f7da-164">Throttling helps avoid poor service performance.</span></span>  <p> <span data-ttu-id="8f7da-165">**CONSEIL**: les actions en attente peuvent limiter le nombre de nouvelles enquêtes qui peuvent s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="8f7da-165">**TIP**: Pending actions can limit how many new investigations can run.</span></span> <span data-ttu-id="8f7da-166">Veillez à [approuver (ou rejeter) les actions en attente.](air-review-approve-pending-completed-actions.md#approve-or-reject-pending-actions)</span><span class="sxs-lookup"><span data-stu-id="8f7da-166">Make sure to [approve (or reject) pending actions](air-review-approve-pending-completed-actions.md#approve-or-reject-pending-actions).</span></span>|
|<span data-ttu-id="8f7da-167">**Terminated By Throttling**</span><span class="sxs-lookup"><span data-stu-id="8f7da-167">**Terminated By Throttling**</span></span>|<span data-ttu-id="8f7da-168">Si un examen est mis trop longtemps dans la file d’attente, il s’arrête.</span><span class="sxs-lookup"><span data-stu-id="8f7da-168">If an investigation is held in the queue too long, it stops.</span></span> <p> <span data-ttu-id="8f7da-169">**CONSEIL**: vous pouvez [démarrer une enquête à partir de l’Explorateur de menaces.](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer)</span><span class="sxs-lookup"><span data-stu-id="8f7da-169">**TIP**: You can [start an investigation from Threat Explorer](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).</span></span>|
|

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="8f7da-170">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="8f7da-170">View details of an investigation</span></span>

1. <span data-ttu-id="8f7da-171">Go to the Microsoft 365 security center ( <https://security.microsoft.com> ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="8f7da-171">Go to the Microsoft 365 security center (<https://security.microsoft.com>) and sign in.</span></span>
2. <span data-ttu-id="8f7da-172">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="8f7da-172">In the navigation pane, select **Action center**.</span></span>
3. <span data-ttu-id="8f7da-173">Sous les onglets **En attente** **ou** Historique, sélectionnez une action.</span><span class="sxs-lookup"><span data-stu-id="8f7da-173">On either the **Pending** or **History** tabs, select an action.</span></span> <span data-ttu-id="8f7da-174">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8f7da-174">Its flyout pane opens.</span></span>
4. <span data-ttu-id="8f7da-175">Dans le volet volant, sélectionnez **Ouvrir la page Enquête.**</span><span class="sxs-lookup"><span data-stu-id="8f7da-175">In the flyout pane, select **Open investigation page**.</span></span> 
5. <span data-ttu-id="8f7da-176">Utilisez les différents onglets pour en savoir plus sur l’examen.</span><span class="sxs-lookup"><span data-stu-id="8f7da-176">Use the various tabs to learn more about the investigation.</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="8f7da-177">Afficher les détails d’une alerte liée à un examen</span><span class="sxs-lookup"><span data-stu-id="8f7da-177">View details about an alert related to an investigation</span></span>

<span data-ttu-id="8f7da-178">Certains types d’alerte déclenchent une enquête automatisée dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8f7da-178">Certain kinds of alerts trigger automated investigation in Microsoft 365.</span></span> <span data-ttu-id="8f7da-179">Pour en savoir plus, consultez les [stratégies d’alerte qui déclenchent des enquêtes automatisées.](office-365-air.md#which-alert-policies-trigger-automated-investigations)</span><span class="sxs-lookup"><span data-stu-id="8f7da-179">To learn more, see [alert policies that trigger automated investigations](office-365-air.md#which-alert-policies-trigger-automated-investigations).</span></span>

1. <span data-ttu-id="8f7da-180">Go to the Microsoft 365 security center ( <https://security.microsoft.com> ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="8f7da-180">Go to the Microsoft 365 security center (<https://security.microsoft.com>) and sign in.</span></span>
2. <span data-ttu-id="8f7da-181">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="8f7da-181">In the navigation pane, select **Action center**.</span></span>
3. <span data-ttu-id="8f7da-182">Sous les onglets **En attente** **ou** Historique, sélectionnez une action.</span><span class="sxs-lookup"><span data-stu-id="8f7da-182">On either the **Pending** or **History** tabs, select an action.</span></span> <span data-ttu-id="8f7da-183">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8f7da-183">Its flyout pane opens.</span></span>
4. <span data-ttu-id="8f7da-184">Dans le volet volant, sélectionnez **Ouvrir la page Enquête.**</span><span class="sxs-lookup"><span data-stu-id="8f7da-184">In the flyout pane, select **Open investigation page**.</span></span> 
5. <span data-ttu-id="8f7da-185">Sélectionnez **l’onglet Alertes** pour afficher la liste de toutes les alertes associées à cet examen.</span><span class="sxs-lookup"><span data-stu-id="8f7da-185">Select the **Alerts** tab to view a list of all of the alerts associated with that investigation.</span></span>
6. <span data-ttu-id="8f7da-186">Sélectionnez un élément dans la liste pour ouvrir son volet volant.</span><span class="sxs-lookup"><span data-stu-id="8f7da-186">Select an item in the list to open its flyout pane.</span></span> <span data-ttu-id="8f7da-187">Vous y pouvez afficher plus d’informations sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="8f7da-187">There, you can view more information about the alert.</span></span>

## <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="8f7da-188">Gardez les points suivants à l’esprit</span><span class="sxs-lookup"><span data-stu-id="8f7da-188">Keep the following points in mind</span></span>

- <span data-ttu-id="8f7da-189">Les nombres d’e-mails sont calculés au moment de l’enquête et certains sont recalculés lorsque vous ouvrez des volants d’enquête (sur la base d’une requête sous-jacente).</span><span class="sxs-lookup"><span data-stu-id="8f7da-189">Email counts are calculated at the time of the investigation, and some counts are recalculated when you open investigation flyouts (based on an underlying query).</span></span>

- <span data-ttu-id="8f7da-190">Les nombres de messages affichés  pour les clusters de messagerie sous l’onglet Courrier électronique et la valeur de quantité de courrier indiquée dans le flyout de cluster sont calculés au moment de l’examen et ne changent pas.</span><span class="sxs-lookup"><span data-stu-id="8f7da-190">The email counts shown for the email clusters on the **Email** tab and the email quantity value shown on cluster flyout are calculated at the time of investigation, and do not change.</span></span>

- <span data-ttu-id="8f7da-191">Le nombre de messages affichés en bas de l’onglet Courrier du flyout du cluster de messagerie et le nombre de messages électroniques affichés dans l’Explorateur reflètent les messages électroniques reçus après l’analyse initiale de l’enquête. </span><span class="sxs-lookup"><span data-stu-id="8f7da-191">The email count shown at the bottom of the **Email** tab of the email cluster flyout and the count of email messages shown in Explorer reflect email messages received after the investigation's initial analysis.</span></span>

  <span data-ttu-id="8f7da-192">Par conséquent, un cluster de messagerie qui affiche une quantité d’origine de 10 messages électroniques affiche un total de 15 messages électroniques lorsque cinq autres messages électroniques arrivent entre la phase d’analyse de l’examen et lorsque l’administrateur examine l’examen.</span><span class="sxs-lookup"><span data-stu-id="8f7da-192">Thus, an email cluster that shows an original quantity of 10 email messages would show an email list total of 15 when five more email messages arrive between the investigation analysis phase and when the admin reviews the investigation.</span></span> <span data-ttu-id="8f7da-193">De même, les anciennes enquêtes peuvent commencer à afficher des nombres plus élevés que les requêtes De l’Explorateur, car les données dans Microsoft Defender pour Office 365 Plan 2 expirent après sept jours pour les essais et après 30 jours pour les licences payantes.</span><span class="sxs-lookup"><span data-stu-id="8f7da-193">Likewise, old investigations might start showing higher counts than Explorer queries show, because data in Microsoft Defender for Office 365 Plan 2 expires after seven days for trials and after 30 days for paid licenses.</span></span>

  <span data-ttu-id="8f7da-194">L’affichage du nombre historique et du nombre actuel dans différents affichages est effectué pour indiquer l’impact de la messagerie au moment de l’examen et l’impact actuel jusqu’au moment où la correction est effectuée.</span><span class="sxs-lookup"><span data-stu-id="8f7da-194">Showing both count historical and current counts in different views is done to indicate the email impact at the time of investigation and the current impact up until the time that remediation is run.</span></span>

- <span data-ttu-id="8f7da-195">Dans le contexte du courrier électronique, vous pouvez voir une surface de menace d’anomalie de volume dans le cadre de l’examen.</span><span class="sxs-lookup"><span data-stu-id="8f7da-195">In the context of email, you might see a volume anomaly threat surface as part of the investigation.</span></span> <span data-ttu-id="8f7da-196">Une anomalie de volume indique un pic du nombre de messages électroniques similaires autour de la durée de l’événement d’investigation par rapport aux périodes antérieures.</span><span class="sxs-lookup"><span data-stu-id="8f7da-196">A volume anomaly indicates a spike in similar email messages around the investigation event time compared to earlier timeframes.</span></span> <span data-ttu-id="8f7da-197">Un pic du trafic de messagerie ainsi que certaines caractéristiques (par exemple, le domaine de l’objet et de l’expéditeur, la similarité du corps et l’adresse IP de l’expéditeur) est caractéristique du début des campagnes ou des attaques par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="8f7da-197">A spike in email traffic together with certain characteristics (for example, subject and sender domain, body similarity, and sender IP) is typical of the start of email campaigns or attacks.</span></span> <span data-ttu-id="8f7da-198">Toutefois, les campagnes de courrier en masse, de courrier indésirable et légitimes partagent généralement ces caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="8f7da-198">However, bulk, spam, and legitimate email campaigns commonly share these characteristics.</span></span>

- <span data-ttu-id="8f7da-199">Les anomalies de volume représentent une menace potentielle et, par conséquent, peuvent être moins graves que les programmes malveillants ou les menaces de hameçonnage identifiés à l’aide de moteurs antivirus, de détonation ou de réputation malveillante.</span><span class="sxs-lookup"><span data-stu-id="8f7da-199">Volume anomalies represent a potential threat, and accordingly could be less severe compared to malware or phish threats that are identified using anti-virus engines, detonation, or malicious reputation.</span></span>

- <span data-ttu-id="8f7da-200">Vous n’avez pas besoin d’approuver chaque action.</span><span class="sxs-lookup"><span data-stu-id="8f7da-200">You do not have to approve every action.</span></span> <span data-ttu-id="8f7da-201">Si vous n’êtes pas d’accord avec l’action recommandée ou si  votre organisation ne choisit pas certains types d’actions, vous pouvez choisir de rejeter les actions ou simplement de les ignorer et de ne pas prendre d’action.</span><span class="sxs-lookup"><span data-stu-id="8f7da-201">If you do not agree with the recommended action or your organization does not choose certain types of actions, then you can choose to **Reject** the actions or simply ignore them and take no action.</span></span>

- <span data-ttu-id="8f7da-202">L’approbation et/ou le rejet de toutes les actions permet à l’examen de se fermer complètement (l’état est corrigé), tout en laissant certaines actions incomplètes, l’état de l’examen passe à un état partiellement corrigé.</span><span class="sxs-lookup"><span data-stu-id="8f7da-202">Approving and/or rejecting all actions lets the investigation fully close (status becomes remediated), while leaving some actions incomplete results in the investigation status changing to a partially remediated state.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8f7da-203">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8f7da-203">Next steps</span></span>

- [<span data-ttu-id="8f7da-204">Examiner et approuver les actions en attente</span><span class="sxs-lookup"><span data-stu-id="8f7da-204">Review and approve pending actions</span></span>](air-review-approve-pending-completed-actions.md#approve-or-reject-pending-actions)