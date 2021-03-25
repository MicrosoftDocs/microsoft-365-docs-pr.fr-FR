---
title: Gérer les alertes microsoft Defender pour les points de terminaison
description: Modifiez l’état des alertes, créez des règles de suppression pour masquer les alertes, envoyez des commentaires et examinez l’historique des changements pour les alertes individuelles à l’intérieur du menu Gérer les alertes.
keywords: gérer les alertes, gérer, alertes, état, nouveau, en cours, résolu, résoudre les alertes, supprimer, supprimer, règles, contexte, historique, commentaires, modifications
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f03c2209b369e6fb9e001452c53073daeb5fe1c6
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187000"
---
# <a name="manage-microsoft-defender-for-endpoint-alerts"></a><span data-ttu-id="1fce4-104">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-104">Manage Microsoft Defender for Endpoint alerts</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1fce4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1fce4-105">**Applies to:**</span></span>
- [<span data-ttu-id="1fce4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1fce4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1fce4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="1fce4-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="1fce4-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1fce4-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1fce4-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-managealerts-abovefoldlink)

<span data-ttu-id="1fce4-110">Defender pour le point de terminaison vous avertit des événements malveillants, attributs et informations contextuelles possibles par le biais d’alertes.</span><span class="sxs-lookup"><span data-stu-id="1fce4-110">Defender for Endpoint notifies you of possible malicious events, attributes, and contextual information through alerts.</span></span> <span data-ttu-id="1fce4-111">Un résumé des nouvelles alertes s’affiche dans le tableau de bord Opérations de sécurité **et** vous pouvez accéder à toutes les alertes dans la file **d’attente des alertes.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-111">A summary of new alerts is displayed in the **Security operations dashboard**, and you can access all alerts in the **Alerts queue**.</span></span>

<span data-ttu-id="1fce4-112">Vous pouvez gérer les alertes en sélectionnant une alerte dans la file d’attente des **alertes** ou l’onglet **Alertes** de la page Appareil pour un appareil individuel.</span><span class="sxs-lookup"><span data-stu-id="1fce4-112">You can manage alerts by selecting an alert in the **Alerts queue**, or the **Alerts** tab of the Device page for an individual device.</span></span>

<span data-ttu-id="1fce4-113">La sélection d’une alerte dans l’un de ces lieux fait monter le volet **de gestion des alertes.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-113">Selecting an alert in either of those places brings up the **Alert management pane**.</span></span>

![Image du volet de gestion des alertes et de la file d’attente des alertes](images/atp-alerts-selected.png)

## <a name="link-to-another-incident"></a><span data-ttu-id="1fce4-115">Lien vers un autre incident</span><span class="sxs-lookup"><span data-stu-id="1fce4-115">Link to another incident</span></span>
<span data-ttu-id="1fce4-116">Vous pouvez créer un incident à partir de l’alerte ou d’un lien vers un incident existant.</span><span class="sxs-lookup"><span data-stu-id="1fce4-116">You can create a new incident from the alert or link to an existing incident.</span></span> 

## <a name="assign-alerts"></a><span data-ttu-id="1fce4-117">Affecter des alertes</span><span class="sxs-lookup"><span data-stu-id="1fce4-117">Assign alerts</span></span>
<span data-ttu-id="1fce4-118">Si une alerte n’est pas encore attribuée, vous pouvez sélectionner Affecter à moi **pour** vous attribuer l’alerte.</span><span class="sxs-lookup"><span data-stu-id="1fce4-118">If an alert is not yet assigned, you can select **Assign to me** to assign the alert to yourself.</span></span>


## <a name="suppress-alerts"></a><span data-ttu-id="1fce4-119">Supprimer des alertes</span><span class="sxs-lookup"><span data-stu-id="1fce4-119">Suppress alerts</span></span>
<span data-ttu-id="1fce4-120">Dans certains scénarios, vous devrez peut-être supprimer l’apparition d’alertes dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="1fce4-120">There might be scenarios where you need to suppress alerts from appearing in Microsoft Defender Security Center.</span></span> <span data-ttu-id="1fce4-121">Defender pour le point de terminaison vous permet de créer des règles de suppression pour des alertes spécifiques qui sont connues comme étant superflues, telles que des outils ou des processus connus dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1fce4-121">Defender for Endpoint lets you create suppression rules for specific alerts that are known to be innocuous such as known tools or processes in your organization.</span></span>

<span data-ttu-id="1fce4-122">Les règles de suppression peuvent être créées à partir d’une alerte existante.</span><span class="sxs-lookup"><span data-stu-id="1fce4-122">Suppression rules can be created from an existing alert.</span></span> <span data-ttu-id="1fce4-123">Elles peuvent être désactivées et réactivées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1fce4-123">They can be disabled and reenabled if needed.</span></span>

<span data-ttu-id="1fce4-124">Lorsqu’une règle de suppression est créée, elle prend effet à partir du moment où la règle est créée.</span><span class="sxs-lookup"><span data-stu-id="1fce4-124">When a suppression rule is created, it will take effect from the point when the rule is created.</span></span> <span data-ttu-id="1fce4-125">La règle n’affecte pas les alertes existantes déjà dans la file d’attente, avant la création de la règle.</span><span class="sxs-lookup"><span data-stu-id="1fce4-125">The rule will not affect existing alerts already in the queue, prior to the rule creation.</span></span> <span data-ttu-id="1fce4-126">La règle sera appliquée uniquement aux alertes qui répondent aux conditions définies après la création de la règle.</span><span class="sxs-lookup"><span data-stu-id="1fce4-126">The rule will only be applied on alerts that satisfy the conditions set after the rule is created.</span></span>

<span data-ttu-id="1fce4-127">Vous pouvez choisir parmi deux contextes pour une règle de suppression :</span><span class="sxs-lookup"><span data-stu-id="1fce4-127">There are two contexts for a suppression rule that you can choose from:</span></span>

- <span data-ttu-id="1fce4-128">**Supprimer l’alerte sur cet appareil**</span><span class="sxs-lookup"><span data-stu-id="1fce4-128">**Suppress alert on this device**</span></span>
- <span data-ttu-id="1fce4-129">**Supprimer une alerte dans mon organisation**</span><span class="sxs-lookup"><span data-stu-id="1fce4-129">**Suppress alert in my organization**</span></span>

<span data-ttu-id="1fce4-130">Le contexte de la règle vous permet d’adapter ce qui est mis en avant dans le portail et de vous assurer que seules les alertes de sécurité réelles sont sur le portail.</span><span class="sxs-lookup"><span data-stu-id="1fce4-130">The context of the rule lets you tailor what gets surfaced into the portal and ensure that only real security alerts are surfaced into the portal.</span></span>

<span data-ttu-id="1fce4-131">Vous pouvez utiliser les exemples du tableau suivant pour vous aider à choisir le contexte d’une règle de suppression :</span><span class="sxs-lookup"><span data-stu-id="1fce4-131">You can use the examples in the following table to help you choose the context for a suppression rule:</span></span>

| <span data-ttu-id="1fce4-132">**Context**</span><span class="sxs-lookup"><span data-stu-id="1fce4-132">**Context**</span></span>                           | <span data-ttu-id="1fce4-133">**Définition**</span><span class="sxs-lookup"><span data-stu-id="1fce4-133">**Definition**</span></span>                                                                                                                                              | <span data-ttu-id="1fce4-134">**Exemples de scénarios**</span><span class="sxs-lookup"><span data-stu-id="1fce4-134">**Example scenarios**</span></span>                                                                                                                                                                                                  |
|:--------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fce4-135">**Supprimer l’alerte sur cet appareil**</span><span class="sxs-lookup"><span data-stu-id="1fce4-135">**Suppress alert on this device**</span></span>    | <span data-ttu-id="1fce4-136">Les alertes avec le même titre d’alerte et sur cet appareil spécifique seront supprimées uniquement.</span><span class="sxs-lookup"><span data-stu-id="1fce4-136">Alerts with the same alert title and on that specific device only will be suppressed.</span></span> <br /><br /><span data-ttu-id="1fce4-137">Toutes les autres alertes de cet appareil ne seront pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="1fce4-137">All other alerts on that device will not be suppressed.</span></span> | <ul><li><span data-ttu-id="1fce4-138">Un chercheur en sécurité examine un script malveillant qui a été utilisé pour attaquer d’autres appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1fce4-138">A security researcher is investigating a malicious script that has been used to attack other devices in your organization.</span></span></li><li><span data-ttu-id="1fce4-139">Un développeur crée régulièrement des scripts PowerShell pour son équipe.</span><span class="sxs-lookup"><span data-stu-id="1fce4-139">A developer regularly creates PowerShell scripts for their team.</span></span></li></ul> |
| <span data-ttu-id="1fce4-140">**Supprimer une alerte dans mon organisation**</span><span class="sxs-lookup"><span data-stu-id="1fce4-140">**Suppress alert in my organization**</span></span> | <span data-ttu-id="1fce4-141">Les alertes avec le même titre d’alerte sur n’importe quel appareil seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="1fce4-141">Alerts with the same alert title on any device will be suppressed.</span></span>                                                                                         | <ul><li><span data-ttu-id="1fce4-142">Un outil d’administration anodin est utilisé par tous les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1fce4-142">A benign administrative tool is used by everyone in your organization.</span></span></li></ul>                                                                                                                               |

### <a name="suppress-an-alert-and-create-a-new-suppression-rule"></a><span data-ttu-id="1fce4-143">Supprimez une alerte et créez une règle de suppression :</span><span class="sxs-lookup"><span data-stu-id="1fce4-143">Suppress an alert and create a new suppression rule:</span></span>
<span data-ttu-id="1fce4-144">Créez des règles personnalisées pour contrôler quand les alertes sont supprimées ou résolues.</span><span class="sxs-lookup"><span data-stu-id="1fce4-144">Create custom rules to control when alerts are suppressed, or resolved.</span></span> <span data-ttu-id="1fce4-145">Vous pouvez contrôler le contexte de suppression d’une alerte en spécifiant le titre de l’alerte, l’indicateur de compromis et les conditions.</span><span class="sxs-lookup"><span data-stu-id="1fce4-145">You can control the context for when an alert is suppressed by specifying the alert title, Indicator of compromise, and the conditions.</span></span> <span data-ttu-id="1fce4-146">Après avoir spécifié le contexte, vous pourrez configurer l’action et l’étendue de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="1fce4-146">After specifying the context, you’ll be able to configure the action and scope on the alert.</span></span> 

1. <span data-ttu-id="1fce4-147">Sélectionnez l’alerte que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="1fce4-147">Select the alert you'd like to suppress.</span></span> <span data-ttu-id="1fce4-148">Le volet gestion  des alertes s’en charge.</span><span class="sxs-lookup"><span data-stu-id="1fce4-148">This brings up the **Alert management** pane.</span></span>

2.  <span data-ttu-id="1fce4-149">Sélectionnez **Créer une règle de suppression.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-149">Select **Create a suppression rule**.</span></span>

    <span data-ttu-id="1fce4-150">Vous pouvez créer une condition de suppression à l’aide de ces attributs.</span><span class="sxs-lookup"><span data-stu-id="1fce4-150">You can create a suppression condition using these attributes.</span></span> <span data-ttu-id="1fce4-151">Un opérateur AND est appliqué entre chaque condition, de sorte que la suppression se produit uniquement si toutes les conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="1fce4-151">An AND operator is applied between each condition, so suppression occurs only if all conditions are met.</span></span>
    
    * <span data-ttu-id="1fce4-152">Fichier SHA1</span><span class="sxs-lookup"><span data-stu-id="1fce4-152">File SHA1</span></span>
    * <span data-ttu-id="1fce4-153">Nom de fichier : caractère générique pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fce4-153">File name - wildcard supported</span></span>
    * <span data-ttu-id="1fce4-154">Chemin d’accès du dossier - caractère générique pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fce4-154">Folder path - wildcard supported</span></span>
    * <span data-ttu-id="1fce4-155">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="1fce4-155">IP address</span></span>
    * <span data-ttu-id="1fce4-156">URL : caractère générique pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fce4-156">URL - wildcard supported</span></span>
    * <span data-ttu-id="1fce4-157">Ligne de commande : caractère générique pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fce4-157">Command line - wildcard supported</span></span>

3. <span data-ttu-id="1fce4-158">Sélectionnez **l’IOC déclenchant l’événement.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-158">Select the **Triggering IOC**.</span></span>
    
4. <span data-ttu-id="1fce4-159">Spécifiez l’action et l’étendue de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="1fce4-159">Specify the action and scope on the alert.</span></span> <br>
   <span data-ttu-id="1fce4-160">Vous pouvez résoudre automatiquement une alerte ou la masquer sur le portail.</span><span class="sxs-lookup"><span data-stu-id="1fce4-160">You can automatically resolve an alert or hide it from the portal.</span></span> <span data-ttu-id="1fce4-161">Les alertes qui sont automatiquement résolues apparaissent dans la section résolue de la file d’attente, de la page d’alertes et de la chronologie de l’appareil, et apparaissent comme résolues dans les API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="1fce4-161">Alerts that are automatically resolved will appear in the resolved section of the alerts queue, alert page, and device timeline and will appear as resolved across Defender for Endpoint APIs.</span></span> <br><br> <span data-ttu-id="1fce4-162">Les alertes marquées comme masquées seront supprimées de l’ensemble du système, à la fois sur les alertes associées de l’appareil et à partir du tableau de bord et ne seront pas diffusées dans les API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="1fce4-162">Alerts that are marked as hidden will be suppressed from the entire system, both on the device's associated alerts and from the dashboard and will not be streamed across Defender for Endpoint APIs.</span></span>


5. <span data-ttu-id="1fce4-163">Entrez un nom de règle et un commentaire.</span><span class="sxs-lookup"><span data-stu-id="1fce4-163">Enter a rule name and a comment.</span></span>

6. <span data-ttu-id="1fce4-164">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1fce4-164">Click **Save**.</span></span>

#### <a name="view-the-list-of-suppression-rules"></a><span data-ttu-id="1fce4-165">Afficher la liste des règles de suppression</span><span class="sxs-lookup"><span data-stu-id="1fce4-165">View the list of suppression rules</span></span>

1. <span data-ttu-id="1fce4-166">Dans le volet de navigation, sélectionnez **Suppression de l’alerte**  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-166">In the navigation pane, select **Settings** > **Alert suppression**.</span></span>

2. <span data-ttu-id="1fce4-167">La liste des règles de suppression affiche toutes les règles créées par les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1fce4-167">The list of suppression rules shows all the rules that users in your organization have created.</span></span>

<span data-ttu-id="1fce4-168">Pour plus d’informations sur la gestion des règles de suppression, voir [Gérer les règles de suppression](manage-suppression-rules.md)</span><span class="sxs-lookup"><span data-stu-id="1fce4-168">For more information on managing suppression rules, see [Manage suppression rules](manage-suppression-rules.md)</span></span>

## <a name="change-the-status-of-an-alert"></a><span data-ttu-id="1fce4-169">Modifier l’état d’une alerte</span><span class="sxs-lookup"><span data-stu-id="1fce4-169">Change the status of an alert</span></span>

<span data-ttu-id="1fce4-170">Vous pouvez catégoriser les alertes **(comme Nouveau,** **En cours** ou **Résolu)** en modifiant leur état au fur et à mesure de l’avancement de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="1fce4-170">You can categorize alerts (as **New**, **In Progress**, or **Resolved**) by changing their status as your investigation progresses.</span></span> <span data-ttu-id="1fce4-171">Cela vous permet d’organiser et de gérer la façon dont votre équipe peut répondre aux alertes.</span><span class="sxs-lookup"><span data-stu-id="1fce4-171">This helps you organize and manage how your team can respond to alerts.</span></span>

<span data-ttu-id="1fce4-172">Par exemple, un responsable  d’équipe peut passer en revue  toutes les nouvelles alertes et décider de les affecter à la file d’attente En cours pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="1fce4-172">For example, a team leader can review all **New** alerts, and decide to assign them to the **In Progress** queue for further analysis.</span></span>

<span data-ttu-id="1fce4-173">Le responsable de l’équipe peut  également affecter l’alerte à la file d’attente résolue s’il sait que l’alerte est anodin, provenant d’un appareil non pertinent (par exemple, un appareil appartenant à un administrateur de sécurité) ou traité par le biais d’une alerte antérieure.</span><span class="sxs-lookup"><span data-stu-id="1fce4-173">Alternatively, the team leader might assign the alert to the **Resolved** queue if they know the alert is benign, coming from a device that is irrelevant (such as one belonging to a security administrator), or is being dealt with through an earlier alert.</span></span>



## <a name="alert-classification"></a><span data-ttu-id="1fce4-174">Classification des alertes</span><span class="sxs-lookup"><span data-stu-id="1fce4-174">Alert classification</span></span>
<span data-ttu-id="1fce4-175">Vous pouvez choisir de ne pas définir de classification ou de spécifier si une alerte est une alerte vraie ou une fausse alerte.</span><span class="sxs-lookup"><span data-stu-id="1fce4-175">You can choose not to set a classification, or specify whether an alert is a true alert or a false alert.</span></span> <span data-ttu-id="1fce4-176">Il est important de fournir la classification du vrai positif/faux positif.</span><span class="sxs-lookup"><span data-stu-id="1fce4-176">It's important to provide the classification of true positive/false positive.</span></span> <span data-ttu-id="1fce4-177">Cette classification permet de surveiller la qualité des alertes et d’améliorer la précision des alertes.</span><span class="sxs-lookup"><span data-stu-id="1fce4-177">This classification is used to monitor alert quality, and make alerts more accurate.</span></span> <span data-ttu-id="1fce4-178">Le champ « détermination » définit une fidélité supplémentaire pour une classification « vrai positif ».</span><span class="sxs-lookup"><span data-stu-id="1fce4-178">The "determination" field defines additional fidelity for a "true positive" classification.</span></span> 

## <a name="add-comments-and-view-the-history-of-an-alert"></a><span data-ttu-id="1fce4-179">Ajouter des commentaires et afficher l’historique d’une alerte</span><span class="sxs-lookup"><span data-stu-id="1fce4-179">Add comments and view the history of an alert</span></span>
<span data-ttu-id="1fce4-180">Vous pouvez ajouter des commentaires et afficher des événements historiques sur une alerte pour voir les modifications précédentes apportées à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="1fce4-180">You can add comments and view historical events about an alert to see previous changes made to the alert.</span></span>

<span data-ttu-id="1fce4-181">Chaque fois qu’une modification ou un commentaire est apporté à une alerte, il est enregistré dans la section Commentaires et **historique.**</span><span class="sxs-lookup"><span data-stu-id="1fce4-181">Whenever a change or comment is made to an alert, it is recorded in the **Comments and history** section.</span></span>

<span data-ttu-id="1fce4-182">Les commentaires ajoutés apparaissent instantanément dans le volet.</span><span class="sxs-lookup"><span data-stu-id="1fce4-182">Added comments instantly appear on the pane.</span></span>


## <a name="related-topics"></a><span data-ttu-id="1fce4-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fce4-183">Related topics</span></span>
- [<span data-ttu-id="1fce4-184">Gérer les règles de suppression</span><span class="sxs-lookup"><span data-stu-id="1fce4-184">Manage suppression rules</span></span>](manage-suppression-rules.md)
- [<span data-ttu-id="1fce4-185">Afficher et organiser la file d’attente des alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-185">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="1fce4-186">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-186">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="1fce4-187">Examiner un fichier associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-187">Investigate a file associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="1fce4-188">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-188">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="1fce4-189">Examiner une adresse IP associée à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-189">Investigate an IP address associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="1fce4-190">Examiner un domaine associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-190">Investigate a domain associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-domain.md)
- [<span data-ttu-id="1fce4-191">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1fce4-191">Investigate a user account in Microsoft Defender for Endpoint</span></span>](investigate-user.md)
