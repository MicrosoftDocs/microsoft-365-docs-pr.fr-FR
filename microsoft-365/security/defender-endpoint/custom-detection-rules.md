---
title: Créer des règles de détection personnalisées dans Microsoft Defender ATP
ms.reviewer: ''
description: Découvrez comment créer des règles de détection personnalisées basées sur des requêtes de repérage avancé
keywords: détections personnalisées, créer, gérer, alertes, modifier, exécuter à la demande, fréquence, intervalle, règles de détection, repérage avancé, recherche, requête, actions de réponse, mdatp, microsoft defender atp
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 09/20/2020
ms.technology: mde
ms.openlocfilehash: 48b1f1bf9506acc8491887fca49295d5e4ccbd69
ms.sourcegitcommit: ef98b8a18d275e5b5961e63d2b0743d046321737
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51382708"
---
# <a name="create-custom-detection-rules"></a><span data-ttu-id="6f837-104">Créer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="6f837-104">Create custom detection rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6f837-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6f837-105">**Applies to:**</span></span>
- [<span data-ttu-id="6f837-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6f837-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6f837-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6f837-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="6f837-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6f837-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6f837-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6f837-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="6f837-110">Les règles de [](advanced-hunting-overview.md) détection personnalisées conçues à partir de requêtes de repérage avancées vous permet de surveiller de manière proactive différents événements et états système, y compris les activités suspectées de violation et les appareils mal configurés.</span><span class="sxs-lookup"><span data-stu-id="6f837-110">Custom detection rules built from [advanced hunting](advanced-hunting-overview.md) queries let you proactively monitor various events and system states, including suspected breach activity and misconfigured devices.</span></span> <span data-ttu-id="6f837-111">Vous pouvez les configurer pour qu’ils s’exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu’il existe des correspondances.</span><span class="sxs-lookup"><span data-stu-id="6f837-111">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="6f837-112">Lisez cet article pour apprendre à créer des règles de détection personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6f837-112">Read this article to learn how to create new custom detection rules.</span></span> <span data-ttu-id="6f837-113">Vous pouvez [également consulter l’affichage et la gestion des règles existantes.](custom-detections-manage.md)</span><span class="sxs-lookup"><span data-stu-id="6f837-113">Or [see viewing and managing existing rules](custom-detections-manage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6f837-114">Pour créer ou gérer des détections personnalisées, [votre rôle](user-roles.md#create-roles-and-assign-the-role-to-an-azure-active-directory-group) doit avoir l’autorisation gérer les **paramètres de** sécurité.</span><span class="sxs-lookup"><span data-stu-id="6f837-114">To create or manage custom detections, [your role](user-roles.md#create-roles-and-assign-the-role-to-an-azure-active-directory-group) needs to have the **manage security settings** permission.</span></span>

## <a name="1-prepare-the-query"></a><span data-ttu-id="6f837-115">1. Préparez la requête.</span><span class="sxs-lookup"><span data-stu-id="6f837-115">1. Prepare the query.</span></span>

<span data-ttu-id="6f837-116">Dans le Centre de sécurité Microsoft Defender, allez à **la** recherche avancée et sélectionnez une requête existante ou créez une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="6f837-116">In Microsoft Defender Security Center, go to **Advanced hunting** and select an existing query or create a new query.</span></span> <span data-ttu-id="6f837-117">Lorsque vous utilisez une nouvelle requête, exécutez la requête pour identifier les erreurs et comprendre les résultats possibles.</span><span class="sxs-lookup"><span data-stu-id="6f837-117">When using a new query, run the query to identify errors and understand possible results.</span></span>

>[!IMPORTANT]
><span data-ttu-id="6f837-118">Pour empêcher le service de renvoyer trop d’alertes, chaque règle est limitée à générer seulement 100 alertes chaque fois qu’elle s’exécute.</span><span class="sxs-lookup"><span data-stu-id="6f837-118">To prevent the service from returning too many alerts, each rule is limited to generating only 100 alerts whenever it runs.</span></span> <span data-ttu-id="6f837-119">Avant de créer une règle, modifiez votre requête afin d’éviter les alertes pour une activité normale au quotidien.</span><span class="sxs-lookup"><span data-stu-id="6f837-119">Before creating a rule, tweak your query to avoid alerting for normal, day-to-day activity.</span></span>

### <a name="required-columns-in-the-query-results"></a><span data-ttu-id="6f837-120">Colonnes requises dans les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="6f837-120">Required columns in the query results</span></span>

<span data-ttu-id="6f837-121">Pour utiliser une requête pour une règle de détection personnalisée, la requête doit renvoyer les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f837-121">To use a query for a custom detection rule, the query must return the following columns:</span></span>

- `Timestamp`
- `DeviceId`
- `ReportId`

<span data-ttu-id="6f837-122">Les requêtes simples, telles que celles qui n’utilisent pas l’opérateur ou l’opérateur pour personnaliser ou agréger des résultats, retournent généralement `project` `summarize` ces colonnes courantes.</span><span class="sxs-lookup"><span data-stu-id="6f837-122">Simple queries, such as those that don't use the `project` or `summarize` operator to customize or aggregate results, typically return these common columns.</span></span>

<span data-ttu-id="6f837-123">Il existe plusieurs façons de s’assurer que les requêtes plus complexes retournent ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="6f837-123">There are various ways to ensure more complex queries return these columns.</span></span> <span data-ttu-id="6f837-124">Par exemple, si vous préférez agréger et compter par , vous pouvez toujours retourner et en les obtenant à partir de l’événement le plus récent `DeviceId` `Timestamp` impliquant chaque `ReportId` appareil.</span><span class="sxs-lookup"><span data-stu-id="6f837-124">For example, if you prefer to aggregate and count by `DeviceId`, you can still return `Timestamp` and `ReportId` by getting them from the most recent event involving each device.</span></span>

<span data-ttu-id="6f837-125">L’exemple de requête ci-dessous compte le nombre d’appareils uniques ( ) avec détections antivirus et l’utilise pour rechercher uniquement les appareils avec plus de `DeviceId` cinq détections.</span><span class="sxs-lookup"><span data-stu-id="6f837-125">The sample query below counts the number of unique devices (`DeviceId`) with antivirus detections and uses this to find only those devices with more than five detections.</span></span> <span data-ttu-id="6f837-126">Pour renvoyer la dernière `Timestamp` et la `ReportId` correspondante, elle utilise l’opérateur `summarize` avec la `arg_max` fonction.</span><span class="sxs-lookup"><span data-stu-id="6f837-126">To return the latest `Timestamp` and the corresponding `ReportId`, it uses the `summarize` operator with the `arg_max` function.</span></span>

```kusto
DeviceEvents
| where Timestamp > ago(7d)
| where ActionType == "AntivirusDetection"
| summarize (Timestamp, ReportId)=arg_max(Timestamp, ReportId), count() by DeviceId
| where count_ > 5
```

> [!TIP]
> <span data-ttu-id="6f837-127">Pour de meilleures performances de requête, définissez un filtre d’heure qui correspond à la fréquence d’exécution prévue pour la règle.</span><span class="sxs-lookup"><span data-stu-id="6f837-127">For better query performance, set a time filter that matches your intended run frequency for the rule.</span></span> <span data-ttu-id="6f837-128">Étant donné que l’utilisation la moins fréquente est toutes les 24 heures, le filtrage de la journée passée couvrira toutes les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="6f837-128">Since the least frequent run is every 24 hours, filtering for the past day will cover all new data.</span></span>

## <a name="2-create-a-new-rule-and-provide-alert-details"></a><span data-ttu-id="6f837-129">2. Créez une règle et fournissez des détails sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="6f837-129">2. Create a new rule and provide alert details.</span></span>

<span data-ttu-id="6f837-130">Avec la requête dans l’éditeur  de requête, sélectionnez Créer une règle de détection et spécifiez les détails d’alerte suivants :</span><span class="sxs-lookup"><span data-stu-id="6f837-130">With the query in the query editor, select **Create detection rule** and specify the following alert details:</span></span>

- <span data-ttu-id="6f837-131">**Nom de la détection**: nom de la règle de détection</span><span class="sxs-lookup"><span data-stu-id="6f837-131">**Detection name**—name of the detection rule</span></span>
- <span data-ttu-id="6f837-132">**Fréquence**: intervalle d’exécution de la requête et d’action.</span><span class="sxs-lookup"><span data-stu-id="6f837-132">**Frequency**—interval for running the query and taking action.</span></span> [<span data-ttu-id="6f837-133">Voir les conseils supplémentaires ci-dessous</span><span class="sxs-lookup"><span data-stu-id="6f837-133">See additional guidance below</span></span>](#rule-frequency)
- <span data-ttu-id="6f837-134">**Titre de l’alerte**: titre affiché avec les alertes déclenchées par la règle</span><span class="sxs-lookup"><span data-stu-id="6f837-134">**Alert title**—title displayed with alerts triggered by the rule</span></span>
- <span data-ttu-id="6f837-135">**Gravité :** risque potentiel du composant ou de l’activité identifié par la règle.</span><span class="sxs-lookup"><span data-stu-id="6f837-135">**Severity**—potential risk of the component or activity identified by the rule.</span></span> [<span data-ttu-id="6f837-136">En savoir plus sur les gravités des alertes</span><span class="sxs-lookup"><span data-stu-id="6f837-136">Read about alert severities</span></span>](alerts-queue.md#severity)
- <span data-ttu-id="6f837-137">**Catégorie**: type de composant ou d’activité de menace, le cas caser.</span><span class="sxs-lookup"><span data-stu-id="6f837-137">**Category**—type of threat component or activity, if any.</span></span> [<span data-ttu-id="6f837-138">En savoir plus sur les catégories d’alerte</span><span class="sxs-lookup"><span data-stu-id="6f837-138">Read about alert categories</span></span>](alerts-queue.md#understanding-alert-categories)
- <span data-ttu-id="6f837-139">**MITRE ATT&techniques CK**: une ou plusieurs techniques d’attaque identifiées par la règle, comme documenté dans l’infrastructure MITRE ATT&CK.</span><span class="sxs-lookup"><span data-stu-id="6f837-139">**MITRE ATT&CK techniques**—one or more attack techniques identified by the rule as documented in the MITRE ATT&CK framework.</span></span> <span data-ttu-id="6f837-140">Cette section n’est pas disponible avec certaines catégories d’alertes, telles que les programmes malveillants, les ransomware, les activités suspectes et les logiciels indésirables</span><span class="sxs-lookup"><span data-stu-id="6f837-140">This section is not available with certain alert categories, such as malware, ransomware, suspicious activity, and unwanted software</span></span>
- <span data-ttu-id="6f837-141">**Description**: plus d’informations sur le composant ou l’activité identifié par la règle</span><span class="sxs-lookup"><span data-stu-id="6f837-141">**Description**—more information about the component or activity identified by the rule</span></span> 
- <span data-ttu-id="6f837-142">**Actions recommandées**: actions supplémentaires que les répondeurs peuvent prendre en réponse à une alerte</span><span class="sxs-lookup"><span data-stu-id="6f837-142">**Recommended actions**—additional actions that responders might take in response to an alert</span></span>

<span data-ttu-id="6f837-143">Pour plus d’informations sur l’affichage des détails de l’alerte, consultez [la file d’attente des alertes.](alerts-queue.md)</span><span class="sxs-lookup"><span data-stu-id="6f837-143">For more information about how alert details are displayed, [read about the alert queue](alerts-queue.md).</span></span>

### <a name="rule-frequency"></a><span data-ttu-id="6f837-144">Fréquence des règles</span><span class="sxs-lookup"><span data-stu-id="6f837-144">Rule frequency</span></span>

<span data-ttu-id="6f837-145">Une fois enregistrée, une nouvelle règle de détection personnalisée s’exécute immédiatement et recherche les correspondances des 30 derniers jours de données.</span><span class="sxs-lookup"><span data-stu-id="6f837-145">When saved, a new custom detection rule immediately runs and checks for matches from the past 30 days of data.</span></span> <span data-ttu-id="6f837-146">La règle s’exécute ensuite à intervalles fixes et durées de recherche en fonction de la fréquence que vous choisissez :</span><span class="sxs-lookup"><span data-stu-id="6f837-146">The rule then runs again at fixed intervals and lookback durations based on the frequency you choose:</span></span>

- <span data-ttu-id="6f837-147">**Toutes les 24 heures**: s’exécute toutes les 24 heures, en vérifiant les données des 30 derniers jours</span><span class="sxs-lookup"><span data-stu-id="6f837-147">**Every 24 hours**—runs every 24 hours, checking data from the past 30 days</span></span>
- <span data-ttu-id="6f837-148">**Toutes les 12 heures**: s’exécute toutes les 12 heures, en vérifiant les données des dernières 24 heures</span><span class="sxs-lookup"><span data-stu-id="6f837-148">**Every 12 hours**—runs every 12 hours, checking data from the past 24 hours</span></span>
- <span data-ttu-id="6f837-149">**Toutes les 3 heures :** s’exécute toutes les 3 heures, en vérifiant les données des 6 dernières heures</span><span class="sxs-lookup"><span data-stu-id="6f837-149">**Every 3 hours**—runs every 3 hours, checking data from the past 6 hours</span></span>
- <span data-ttu-id="6f837-150">**Toutes les heures**: s’exécute toutes les heures, en vérifiant les données des dernières 2 heures</span><span class="sxs-lookup"><span data-stu-id="6f837-150">**Every hour**—runs hourly, checking data from the past 2 hours</span></span>

<span data-ttu-id="6f837-151">Lorsque vous modifiez une règle, elle s’exécute avec les modifications appliquées lors de la prochaine utilisation prévue en fonction de la fréquence que vous avez définie.</span><span class="sxs-lookup"><span data-stu-id="6f837-151">When you edit a rule, it will run with the applied changes in the next run time scheduled according to the frequency you set.</span></span>


> [!TIP]
> <span data-ttu-id="6f837-152">Faire correspondre les filtres d’heure de votre requête à la durée de la recherche.</span><span class="sxs-lookup"><span data-stu-id="6f837-152">Match the time filters in your query with the lookback duration.</span></span> <span data-ttu-id="6f837-153">Les résultats en dehors de la durée de la recherche sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6f837-153">Results outside of the lookback duration are ignored.</span></span>

<span data-ttu-id="6f837-154">Sélectionnez la fréquence qui correspond à la fréquence à laquelle vous souhaitez surveiller les détections et prenez en compte la capacité de votre organisation à répondre aux alertes.</span><span class="sxs-lookup"><span data-stu-id="6f837-154">Select the frequency that matches how closely you want to monitor detections, and consider your organization's capacity to respond to the alerts.</span></span>

## <a name="3-choose-the-impacted-entities"></a><span data-ttu-id="6f837-155">3. Choisissez les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="6f837-155">3. Choose the impacted entities.</span></span>

<span data-ttu-id="6f837-156">Identifiez les colonnes dans les résultats de votre requête où vous vous attendez à trouver l’entité principale affectée ou concernée.</span><span class="sxs-lookup"><span data-stu-id="6f837-156">Identify the columns in your query results where you expect to find the main affected or impacted entity.</span></span> <span data-ttu-id="6f837-157">Par exemple, une requête peut renvoyer des ID d’appareil et d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f837-157">For example, a query might return both device and user IDs.</span></span> <span data-ttu-id="6f837-158">L’identification de l’une de ces colonnes représentant la principale entité concernée permet au service d’agréger les alertes pertinentes, de corréler les incidents et les actions de réponse cible.</span><span class="sxs-lookup"><span data-stu-id="6f837-158">Identifying which of these columns represent the main impacted entity helps the service aggregate relevant alerts, correlate incidents, and target response actions.</span></span>

<span data-ttu-id="6f837-159">Vous ne pouvez sélectionner qu’une seule colonne pour chaque type d’entité.</span><span class="sxs-lookup"><span data-stu-id="6f837-159">You can select only one column for each entity type.</span></span> <span data-ttu-id="6f837-160">Les colonnes qui ne sont pas renvoyées par votre requête ne peuvent pas être sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="6f837-160">Columns that are not returned by your query can't be selected.</span></span>

## <a name="4-specify-actions"></a><span data-ttu-id="6f837-161">4. Spécifiez les actions.</span><span class="sxs-lookup"><span data-stu-id="6f837-161">4. Specify actions.</span></span>

<span data-ttu-id="6f837-162">Votre règle de détection personnalisée peut automatiquement prendre des mesures sur des fichiers ou des appareils renvoyés par la requête.</span><span class="sxs-lookup"><span data-stu-id="6f837-162">Your custom detection rule can automatically take actions on files or devices that are returned by the query.</span></span>

### <a name="actions-on-devices"></a><span data-ttu-id="6f837-163">Actions sur les appareils</span><span class="sxs-lookup"><span data-stu-id="6f837-163">Actions on devices</span></span>

<span data-ttu-id="6f837-164">Ces actions sont appliquées aux appareils dans la `DeviceId` colonne des résultats de la requête :</span><span class="sxs-lookup"><span data-stu-id="6f837-164">These actions are applied to devices in the `DeviceId` column of the query results:</span></span>

- <span data-ttu-id="6f837-165">**Isoler l’appareil**: applique une isolation complète du réseau, ce qui empêche l’appareil de se connecter à n’importe quelle application ou service, à l’exception du service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="6f837-165">**Isolate device**—applies full network isolation, preventing the device from connecting to any application or service, except for the Defender for Endpoint service.</span></span> [<span data-ttu-id="6f837-166">En savoir plus sur l’isolation des appareils</span><span class="sxs-lookup"><span data-stu-id="6f837-166">Learn more about device isolation</span></span>](respond-machine-alerts.md#isolate-devices-from-the-network)
- <span data-ttu-id="6f837-167">**Collecter un package d’examen**: collecte des informations sur l’appareil dans un fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="6f837-167">**Collect investigation package**—collects device information in a ZIP file.</span></span> [<span data-ttu-id="6f837-168">En savoir plus sur le package d’examen</span><span class="sxs-lookup"><span data-stu-id="6f837-168">Learn more about the investigation package</span></span>](respond-machine-alerts.md#collect-investigation-package-from-devices)
- <span data-ttu-id="6f837-169">**Exécuter une analyse antivirus**: effectue une analyse complète de l’Antivirus Microsoft Defender sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="6f837-169">**Run antivirus scan**—performs a full Microsoft Defender Antivirus scan on the device</span></span>
- <span data-ttu-id="6f837-170">**Lancer une enquête**: lance une [enquête automatisée](automated-investigations.md) sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="6f837-170">**Initiate investigation**—starts an [automated investigation](automated-investigations.md) on the device</span></span>
- <span data-ttu-id="6f837-171">**Restreindre l’exécution de** l’application : définit des restrictions sur l’appareil pour autoriser uniquement l’exécution des fichiers signés avec un certificat émis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f837-171">**Restrict app execution**—sets restrictions on the device to allow only files that are signed with a Microsoft-issued certificate to run.</span></span> [<span data-ttu-id="6f837-172">En savoir plus sur la restriction de l’exécution de l’application</span><span class="sxs-lookup"><span data-stu-id="6f837-172">Learn more about restricting app execution</span></span>](respond-machine-alerts.md#restrict-app-execution)

### <a name="actions-on-files"></a><span data-ttu-id="6f837-173">Actions sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="6f837-173">Actions on files</span></span>

<span data-ttu-id="6f837-174">Ces actions sont appliquées aux fichiers dans la ou `SHA1` la colonne des résultats de la requête `InitiatingProcessSHA1` :</span><span class="sxs-lookup"><span data-stu-id="6f837-174">These actions are applied to files in the `SHA1` or the `InitiatingProcessSHA1` column of the query results:</span></span>

- <span data-ttu-id="6f837-175">**Autoriser/Bloquer**: ajoute automatiquement le [](manage-indicators.md) fichier à votre liste d’indicateurs personnalisés afin qu’il soit toujours autorisé à s’exécuter ou qu’il ne soit pas autorisé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="6f837-175">**Allow/Block**—automatically adds the file to your [custom indicator list](manage-indicators.md) so that it is always allowed to run or blocked from running.</span></span> <span data-ttu-id="6f837-176">Vous pouvez définir l’étendue de cette action afin qu’elle soit prise uniquement sur les groupes d’appareils sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="6f837-176">You can set the scope of this action so that it is taken only on selected device groups.</span></span> <span data-ttu-id="6f837-177">Cette étendue est indépendante de l’étendue de la règle.</span><span class="sxs-lookup"><span data-stu-id="6f837-177">This scope is independent of the scope of the rule.</span></span>
- <span data-ttu-id="6f837-178">**Fichier de mise en** quarantaine : supprime le fichier de son emplacement actuel et place une copie en quarantaine</span><span class="sxs-lookup"><span data-stu-id="6f837-178">**Quarantine file**—deletes the file from its current location and places a copy in quarantine</span></span>

### <a name="actions-on-users"></a><span data-ttu-id="6f837-179">Actions sur les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6f837-179">Actions on users</span></span>

- <span data-ttu-id="6f837-180">**Marquez l’utilisateur comme** compromis : définit le niveau de risque de l’utilisateur sur « élevé » dans Azure Active Directory, déclenchant les stratégies de protection des [identités correspondantes.](https://docs.microsoft.com/azure/active-directory/identity-protection/overview-identity-protection#risk-levels)</span><span class="sxs-lookup"><span data-stu-id="6f837-180">**Mark user as compromised**—sets the user's risk level to "high" in Azure Active Directory, triggering the corresponding [identity protection policies](https://docs.microsoft.com/azure/active-directory/identity-protection/overview-identity-protection#risk-levels).</span></span>

## <a name="5-set-the-rule-scope"></a><span data-ttu-id="6f837-181">5. Définissez l’étendue de la règle.</span><span class="sxs-lookup"><span data-stu-id="6f837-181">5. Set the rule scope.</span></span>

<span data-ttu-id="6f837-182">Définissez l’étendue pour spécifier les appareils couverts par la règle :</span><span class="sxs-lookup"><span data-stu-id="6f837-182">Set the scope to specify which devices are covered by the rule:</span></span>

- <span data-ttu-id="6f837-183">Tous les appareils</span><span class="sxs-lookup"><span data-stu-id="6f837-183">All devices</span></span>
- <span data-ttu-id="6f837-184">Groupes d’appareils spécifiques</span><span class="sxs-lookup"><span data-stu-id="6f837-184">Specific device groups</span></span>

<span data-ttu-id="6f837-185">Seules les données des appareils dans l’étendue seront interrogés.</span><span class="sxs-lookup"><span data-stu-id="6f837-185">Only data from devices in scope will be queried.</span></span> <span data-ttu-id="6f837-186">En outre, des actions seront prises uniquement sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="6f837-186">Also, actions will be taken only on those devices.</span></span>

## <a name="6-review-and-turn-on-the-rule"></a><span data-ttu-id="6f837-187">6. Examinez et allumez la règle.</span><span class="sxs-lookup"><span data-stu-id="6f837-187">6. Review and turn on the rule.</span></span>

<span data-ttu-id="6f837-188">Après avoir passé en revue la règle, **sélectionnez Créer** pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="6f837-188">After reviewing the rule, select **Create** to save it.</span></span> <span data-ttu-id="6f837-189">La règle de détection personnalisée s’exécute immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6f837-189">The custom detection rule immediately runs.</span></span> <span data-ttu-id="6f837-190">Il s’exécute à nouveau en fonction de la fréquence configurée pour vérifier les correspondances, générer des alertes et prendre des mesures de réponse.</span><span class="sxs-lookup"><span data-stu-id="6f837-190">It runs again based on configured frequency to check for matches, generate alerts, and take response actions.</span></span>

<span data-ttu-id="6f837-191">Vous pouvez [afficher et gérer des règles de détection](custom-detections-manage.md)personnalisées, vérifier leurs précédentes séries et passer en revue les alertes qu’elles ont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="6f837-191">You can [view and manage custom detection rules](custom-detections-manage.md), check their previous runs, and review the alerts they have triggered.</span></span> <span data-ttu-id="6f837-192">Vous pouvez également exécuter une règle à la demande et la modifier.</span><span class="sxs-lookup"><span data-stu-id="6f837-192">You can also run a rule on demand and modify it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f837-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f837-193">Related topics</span></span>

- [<span data-ttu-id="6f837-194">Afficher et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="6f837-194">View and manage custom detection rules</span></span>](custom-detections-manage.md)
- [<span data-ttu-id="6f837-195">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="6f837-195">Custom detections overview</span></span>](overview-custom-detections.md)
- [<span data-ttu-id="6f837-196">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="6f837-196">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="6f837-197">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="6f837-197">Learn the advanced hunting query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="6f837-198">Afficher et organiser les alertes</span><span class="sxs-lookup"><span data-stu-id="6f837-198">View and organize alerts</span></span>](alerts-queue.md)
