---
title: Créer et gérer des règles de détection personnalisées dans Microsoft Threat Protection
description: Découvrez comment créer et gérer des règles de détection personnalisées sur la base de requêtes de chasse avancées.
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, détections personnalisées, règles, schéma, Kusto, Microsoft 365, protection contre les menaces Microsoft, RBAC, autorisations, Microsoft Defender ATP
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: cdfc23f34d90c9d725ec6fb314728553a987c025
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034863"
---
# <a name="create-and-manage-custom-detections-rules"></a><span data-ttu-id="80b7a-104">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="80b7a-104">Create and manage custom detections rules</span></span>

<span data-ttu-id="80b7a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="80b7a-105">**Applies to:**</span></span>
- <span data-ttu-id="80b7a-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="80b7a-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="80b7a-107">Les règles de détection personnalisées générées à partir de requêtes de [chasse avancées](advanced-hunting-overview.md) vous permettent de surveiller de manière proactive différents événements et États du système, y compris l’activité de violation présumée et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="80b7a-107">Custom detection rules built from [Advanced hunting](advanced-hunting-overview.md) queries let you proactively monitor various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="80b7a-108">Vous pouvez les configurer pour qu’elles s’exécutent à intervalles réguliers, générant des alertes et en prenant des mesures de réponse chaque fois qu’il y a des correspondances.</span><span class="sxs-lookup"><span data-stu-id="80b7a-108">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

## <a name="required-permissions-for-managing-custom-detections"></a><span data-ttu-id="80b7a-109">Autorisations requises pour la gestion des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="80b7a-109">Required permissions for managing custom detections</span></span>

<span data-ttu-id="80b7a-110">Pour gérer les détections personnalisées, vous devez disposer de l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="80b7a-110">To manage custom detections, you need to be assigned one of these roles:</span></span>

- <span data-ttu-id="80b7a-111">**Administrateur de sécurité** — le rôle d’administrateur de sécurité ou d’administrateur de sécurité est un [rôle Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) pour la gestion de différents paramètres de sécurité dans le centre de sécurité Microsoft 365 et divers portails et services.</span><span class="sxs-lookup"><span data-stu-id="80b7a-111">**Security administrator** — the security administrator or security admin role is an [Azure Active Directory role](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) for managing various security settings in Microsoft 365 security center and various portals and services.</span></span>

- <span data-ttu-id="80b7a-112">**Opérateur de sécurité** : le rôle opérateur de sécurité est un [rôle Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) pour la gestion des alertes et dispose d’un accès global en lecture seule sur les fonctionnalités liées à la sécurité, y compris toutes les informations du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="80b7a-112">**Security operator** —  the security operator role is an [Azure Active Directory role](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) for managing alerts and has global read-only access on security-related features, including all information in Microsoft 365 security center.</span></span> <span data-ttu-id="80b7a-113">Ce rôle est suffisant pour la gestion des détections personnalisées uniquement si le contrôle d’accès basé sur un rôle (RBAC) est désactivé dans Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="80b7a-113">This role is sufficient for managing custom detections only if role-based access control (RBAC) is turned off in Microsoft Defender ATP.</span></span> <span data-ttu-id="80b7a-114">Si RBAC est configuré, vous avez également besoin de l’autorisation **gérer les paramètres de sécurité** pour Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="80b7a-114">If you have RBAC configured, you also need the **manage security settings** permission for Microsoft Defender ATP.</span></span>

<span data-ttu-id="80b7a-115">Pour gérer les autorisations requises, un **administrateur général** peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="80b7a-115">To manage required permissions, a **global administrator** can do the following:</span></span>

- <span data-ttu-id="80b7a-116">Attribuez le rôle **administrateur** de sécurité ou **opérateur de sécurité** dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/) sous **rôles** > de l’administrateur de la**sécurité**.</span><span class="sxs-lookup"><span data-stu-id="80b7a-116">Assign the **security administrator** or **security operator** role in [Microsoft 365 admin center](https://admin.microsoft.com/) under **Roles** > **Security admin**.</span></span>
- <span data-ttu-id="80b7a-117">Vérifiez les paramètres RBAC pour Microsoft Defender ATP dans le [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/) **sous** > **Permissions** > **rôles**des autorisations.</span><span class="sxs-lookup"><span data-stu-id="80b7a-117">Check RBAC settings for Microsoft Defender ATP in [Microsoft Defender Security Center](https://securitycenter.windows.com/) under **Settings** > **Permissions** > **Roles**.</span></span> <span data-ttu-id="80b7a-118">Sélectionnez le rôle correspondant pour attribuer l’autorisation **gérer les paramètres de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="80b7a-118">Select the corresponding role to assign the **manage security settings** permission.</span></span>

> [!NOTE]
> <span data-ttu-id="80b7a-119">Pour gérer les détections personnalisées, les **opérateurs de sécurité** doivent disposer de l’autorisation **gérer les paramètres de sécurité** dans Microsoft Defender ATP si le RBAC est activé.</span><span class="sxs-lookup"><span data-stu-id="80b7a-119">To manage custom detections, **security operators** will need the **manage security settings** permission in Microsoft Defender ATP if RBAC is turned on.</span></span>

## <a name="create-a-custom-detection-rule"></a><span data-ttu-id="80b7a-120">Créer une règle de détection personnalisée</span><span class="sxs-lookup"><span data-stu-id="80b7a-120">Create a custom detection rule</span></span>
### <a name="1-prepare-the-query"></a><span data-ttu-id="80b7a-121">1. Préparez la requête.</span><span class="sxs-lookup"><span data-stu-id="80b7a-121">1. Prepare the query.</span></span>

<span data-ttu-id="80b7a-122">Dans le centre de sécurité Microsoft 365, accédez à la **chasse avancée** et sélectionnez une requête existante ou créez une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="80b7a-122">In Microsoft 365 security center, go to **Advanced hunting** and select an existing query or create a new query.</span></span> <span data-ttu-id="80b7a-123">Lors de l’utilisation d’une nouvelle requête, exécutez la requête pour identifier les erreurs et comprendre les résultats possibles.</span><span class="sxs-lookup"><span data-stu-id="80b7a-123">When using a new query, run the query to identify errors and understand possible results.</span></span>

#### <a name="required-columns-in-the-query-results"></a><span data-ttu-id="80b7a-124">Colonnes requises dans les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="80b7a-124">Required columns in the query results</span></span>
<span data-ttu-id="80b7a-125">Pour créer une règle de détection personnalisée, la requête doit renvoyer les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="80b7a-125">To create a custom detection rule, the query must return the following columns:</span></span>

- `Timestamp`
- <span data-ttu-id="80b7a-126">Une des colonnes suivantes de l’appareil, de l’utilisateur ou de la boîte aux lettres :</span><span class="sxs-lookup"><span data-stu-id="80b7a-126">One of the following device, user, or mailbox columns:</span></span>
    - `DeviceId`
    - `DeviceName`
    - `RemoteDeviceName`
    - `RecipientEmailAddress`
    - <span data-ttu-id="80b7a-127">`SenderFromAddress`(adresse d’expéditeur ou de chemin d’accès de retour)</span><span class="sxs-lookup"><span data-stu-id="80b7a-127">`SenderFromAddress` (envelope sender or Return-Path address)</span></span>
    - <span data-ttu-id="80b7a-128">`SenderMailFromAddress`(adresse de l’expéditeur affichée par le client de messagerie)</span><span class="sxs-lookup"><span data-stu-id="80b7a-128">`SenderMailFromAddress` (sender address displayed by email client)</span></span>
    - `RecipientObjectId`
    - `AccountSid`
    - `InitiatingProcessAccountSid`
    - `InitiatingProcessAccountUpn`
    - `InitiatingProcessAccountObjectId`
>[!NOTE]
><span data-ttu-id="80b7a-129">Une prise en charge des entités supplémentaires sera ajoutée au fur et à mesure que de nouvelles tables seront ajoutées au [schéma de chasse avancé](advanced-hunting-schema-tables.md).</span><span class="sxs-lookup"><span data-stu-id="80b7a-129">Support for additional entities will be added as new tables are added to the [advanced hunting schema](advanced-hunting-schema-tables.md).</span></span>

<span data-ttu-id="80b7a-130">Les requêtes simples, telles que celles qui n’utilisent `project` pas `summarize` l’opérateur ou pour personnaliser ou agréger des résultats, renvoient généralement ces colonnes communes.</span><span class="sxs-lookup"><span data-stu-id="80b7a-130">Simple queries, such as those that don't use the `project` or `summarize` operator to customize or aggregate results, typically return these common columns.</span></span>

<span data-ttu-id="80b7a-131">Il existe plusieurs façons de s’assurer que les requêtes plus complexes renvoient ces colonnes.</span><span class="sxs-lookup"><span data-stu-id="80b7a-131">There are various ways to ensure more complex queries return these columns.</span></span> <span data-ttu-id="80b7a-132">Par exemple, si vous préférez agréger et dénombrer par entité sous une colonne telle `DeviceId`que, vous pouvez toujours `Timestamp` renvoyer en récupérant l’événement le plus récent impliquant chaque `DeviceId`.</span><span class="sxs-lookup"><span data-stu-id="80b7a-132">For example, if you prefer to aggregate and count by entity under a column such as `DeviceId`, you can still return `Timestamp` by getting it from the most recent event involving each unique `DeviceId`.</span></span>

<span data-ttu-id="80b7a-133">La requête d’exemple ci-dessous compte le nombre d'`DeviceId`ordinateurs uniques () avec des détections d’antivirus et utilise ce nombre pour rechercher uniquement les ordinateurs avec plus de cinq détections.</span><span class="sxs-lookup"><span data-stu-id="80b7a-133">The sample query below counts the number of unique machines (`DeviceId`) with antivirus detections and uses this count to find only the machines with more than five detections.</span></span> <span data-ttu-id="80b7a-134">Pour renvoyer le dernier `Timestamp`, il utilise l' `summarize` opérateur avec la `arg_max` fonction.</span><span class="sxs-lookup"><span data-stu-id="80b7a-134">To return the latest `Timestamp`, it uses the `summarize` operator with the `arg_max` function.</span></span>

```kusto
DeviceEvents
| where Timestamp > ago(7d)
| where ActionType == "AntivirusDetection"
| summarize Timestamp = max(Timestamp), count() by DeviceId
| where count_ > 5
```
### <a name="2-create-new-rule-and-provide-alert-details"></a><span data-ttu-id="80b7a-135">2. créer une règle et fournir des détails d’alerte.</span><span class="sxs-lookup"><span data-stu-id="80b7a-135">2. Create new rule and provide alert details.</span></span>

<span data-ttu-id="80b7a-136">À l’aide de la requête dans l’éditeur de requête, sélectionnez **créer une règle de détection** et spécifiez les détails d’alerte suivants :</span><span class="sxs-lookup"><span data-stu-id="80b7a-136">With the query in the query editor, select **Create detection rule** and specify the following alert details:</span></span>

- <span data-ttu-id="80b7a-137">**Nom** de la détection : nom de la règle de détection</span><span class="sxs-lookup"><span data-stu-id="80b7a-137">**Detection name** — name of the detection rule</span></span>
- <span data-ttu-id="80b7a-138">**Fréquence** : intervalle d’exécution de la requête et d’exécution de l’action.</span><span class="sxs-lookup"><span data-stu-id="80b7a-138">**Frequency** — interval for running the query and taking action.</span></span> [<span data-ttu-id="80b7a-139">Consultez les conseils supplémentaires ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="80b7a-139">See additional guidance below</span></span>](#rule-frequency)
- <span data-ttu-id="80b7a-140">**Titre** de l’alerte — titre affiché avec des alertes déclenchées par la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-140">**Alert title** — title displayed with alerts triggered by the rule</span></span>
- <span data-ttu-id="80b7a-141">**Gravité** — risque potentiel de l’activité ou du composant identifié par la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-141">**Severity** — potential risk of the component or activity identified by the rule</span></span>
- <span data-ttu-id="80b7a-142">**Catégorie** — composant de menace ou activité identifiée par la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-142">**Category** — threat component or activity identified by the rule</span></span>
- <span data-ttu-id="80b7a-143">**Mitre att&CK techniques** : une ou plusieurs techniques d’attaque identifiées par la règle comme indiqué dans la [Mitre att&CK Framework](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="80b7a-143">**MITRE ATT&CK techniques** — one or more attack techniques identified by the rule as documented in the [MITRE ATT&CK framework](https://attack.mitre.org/)</span></span>
- <span data-ttu-id="80b7a-144">**Description** : plus d’informations sur le composant ou l’activité identifié par la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-144">**Description** — more information about the component or activity identified by the rule</span></span> 
- <span data-ttu-id="80b7a-145">**Actions recommandées** : actions supplémentaires que les répondeurs peuvent entreprendre en réponse à une alerte</span><span class="sxs-lookup"><span data-stu-id="80b7a-145">**Recommended actions** — additional actions that responders might take in response to an alert</span></span>

#### <a name="rule-frequency"></a><span data-ttu-id="80b7a-146">Fréquence de la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-146">Rule frequency</span></span>
<span data-ttu-id="80b7a-147">Une fois enregistrée, une règle de détection personnalisée nouvelle ou modifiée s’exécute et recherche des correspondances des données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="80b7a-147">When saved, a new or edited custom detection rule immediately runs and checks for matches from  the past 30 days of data.</span></span> <span data-ttu-id="80b7a-148">La règle s’exécute à nouveau à intervalles fixes et lookback durées en fonction de la fréquence choisie :</span><span class="sxs-lookup"><span data-stu-id="80b7a-148">The rule then runs again at fixed intervals and lookback durations based on the frequency you choose:</span></span>

- <span data-ttu-id="80b7a-149">**Toutes les 24 heures** – s’exécute toutes les 24 heures, vérification des données des 30 derniers jours</span><span class="sxs-lookup"><span data-stu-id="80b7a-149">**Every 24 hours** — runs every 24 hours, checking data from the past 30 days</span></span>
- <span data-ttu-id="80b7a-150">**Toutes les 12 heures** — s’exécute toutes les 12 heures, en vérifiant les données des 24 dernières heures</span><span class="sxs-lookup"><span data-stu-id="80b7a-150">**Every 12 hours** — runs every 12 hours, checking data from the past 24 hours</span></span>
- <span data-ttu-id="80b7a-151">**Toutes les 3 heures** — s’exécute toutes les 3 heures, en vérifiant les données des 6 dernières heures</span><span class="sxs-lookup"><span data-stu-id="80b7a-151">**Every 3 hours** — runs every 3 hours, checking data from the past 6 hours</span></span>
- <span data-ttu-id="80b7a-152">**Toutes les heures** — s’exécute toutes les heures, en vérifiant les données des 2 dernières heures</span><span class="sxs-lookup"><span data-stu-id="80b7a-152">**Every hour** — runs hourly, checking data from the past 2 hours</span></span>

<span data-ttu-id="80b7a-153">Sélectionnez la fréquence correspondant à la fréquence à laquelle vous souhaitez surveiller les détections et tenez compte de la capacité de votre organisation à répondre aux alertes.</span><span class="sxs-lookup"><span data-stu-id="80b7a-153">Select the frequency that matches how closely you want to monitor detections, and consider your organization's capacity to respond to the alerts.</span></span>

### <a name="3-choose-the-impacted-entities"></a><span data-ttu-id="80b7a-154">3. Choisissez les entités concernées.</span><span class="sxs-lookup"><span data-stu-id="80b7a-154">3. Choose the impacted entities.</span></span>
<span data-ttu-id="80b7a-155">Identifiez les colonnes de vos résultats de requête où vous vous attendez à trouver l’entité principale affectée ou concernée.</span><span class="sxs-lookup"><span data-stu-id="80b7a-155">Identify the columns in your query results where you expect to find the main affected or impacted entity.</span></span> <span data-ttu-id="80b7a-156">Par exemple, une requête peut renvoyer des adresses d'`SenderFromAddress` expéditeur `SenderMailFromAddress`(ou) et`RecipientEmailAddress`de destinataire ().</span><span class="sxs-lookup"><span data-stu-id="80b7a-156">For example, a query might return sender (`SenderFromAddress` or `SenderMailFromAddress`) and recipient (`RecipientEmailAddress`) addresses.</span></span> <span data-ttu-id="80b7a-157">L’identification de l’une de ces colonnes qui représente l’entité affectée principale aide le service à agréger les alertes appropriées, à corréler les incidents et à cibler les actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="80b7a-157">Identifying which of these columns represent the main impacted entity helps the service aggregate relevant alerts, correlate incidents, and target response actions.</span></span>

<span data-ttu-id="80b7a-158">Vous pouvez sélectionner une seule colonne pour chaque type d’entité (boîte aux lettres, utilisateur ou appareil).</span><span class="sxs-lookup"><span data-stu-id="80b7a-158">You can select only one column for each entity type (mailbox, user, or device).</span></span> <span data-ttu-id="80b7a-159">Les colonnes qui ne sont pas renvoyées par votre requête ne peuvent pas être sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="80b7a-159">Columns that are not returned by your query can't be selected.</span></span>

### <a name="4-specify-actions-on-files-or-machines"></a><span data-ttu-id="80b7a-160">4. spécifiez des actions sur des fichiers ou des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="80b7a-160">4. Specify actions on files or machines.</span></span>
<span data-ttu-id="80b7a-161">Votre règle de détection personnalisée peut effectuer automatiquement des actions sur les fichiers ou les ordinateurs qui sont renvoyés par la requête.</span><span class="sxs-lookup"><span data-stu-id="80b7a-161">Your custom detection rule can automatically take actions on files or machines that are returned by the query.</span></span>

#### <a name="actions-on-machines"></a><span data-ttu-id="80b7a-162">Actions sur les ordinateurs</span><span class="sxs-lookup"><span data-stu-id="80b7a-162">Actions on machines</span></span>
<span data-ttu-id="80b7a-163">Ces actions sont appliquées aux machines dans la `DeviceId` colonne des résultats de la requête :</span><span class="sxs-lookup"><span data-stu-id="80b7a-163">These actions are applied to machines in the `DeviceId` column of the query results:</span></span>
- <span data-ttu-id="80b7a-164">**Isoler l’ordinateur** : utilise Microsoft Defender ATP pour appliquer l’isolement réseau complet, ce qui empêche l’ordinateur de se connecter à une application ou à un service.</span><span class="sxs-lookup"><span data-stu-id="80b7a-164">**Isolate machine** — uses Microsoft Defender ATP to apply full network isolation, preventing the machine from connecting to any application or service.</span></span> [<span data-ttu-id="80b7a-165">En savoir plus sur l’isolation de l’ordinateur Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="80b7a-165">Learn more about Microsoft Defender ATP machine isolation</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#isolate-machines-from-the-network)
- <span data-ttu-id="80b7a-166">**Package d’enquête de collecte** — recueille les informations de l’ordinateur dans un fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="80b7a-166">**Collect investigation package** — collects machine information in a ZIP file.</span></span> [<span data-ttu-id="80b7a-167">En savoir plus sur le package d’enquête Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="80b7a-167">Learn more about the Microsoft Defender ATP investigation package</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#collect-investigation-package-from-machines)
- <span data-ttu-id="80b7a-168">**Exécuter l’analyse antivirus** : effectue une analyse complète de l’antivirus Windows Defender sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="80b7a-168">**Run antivirus scan** — performs a full Windows Defender Antivirus scan on the machine</span></span>
- <span data-ttu-id="80b7a-169">**Lancer une enquête** : lance une [enquête automatisée](mtp-autoir.md) sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="80b7a-169">**Initiate investigation** — initiates an [automated investigation](mtp-autoir.md) on the machine</span></span>

#### <a name="actions-on-files"></a><span data-ttu-id="80b7a-170">Actions sur les fichiers</span><span class="sxs-lookup"><span data-stu-id="80b7a-170">Actions on files</span></span>
<span data-ttu-id="80b7a-171">Lorsque cette option est sélectionnée, l’action du **fichier de quarantaine** est effectuée `SHA1`sur `InitiatingProcessSHA1`les `SHA256`fichiers dans `InitiatingProcessSHA256` la colonne,, ou des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="80b7a-171">When selected, the **Quarantine file** action is taken on files in the `SHA1`, `InitiatingProcessSHA1`, `SHA256`, or `InitiatingProcessSHA256` column of the query results.</span></span> <span data-ttu-id="80b7a-172">Cette action supprime le fichier de son emplacement actuel et place une copie en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="80b7a-172">This action deletes the file from its current location and places a copy in quarantine.</span></span>

> [!NOTE]
> <span data-ttu-id="80b7a-173">L’action autoriser ou bloquer pour les règles de détection personnalisées n’est pas prise en charge actuellement sur la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80b7a-173">The allow or block action for custom detection rules is currently not supported on Microsoft Threat Protection.</span></span>

### <a name="5-set-the-rule-scope"></a><span data-ttu-id="80b7a-174">5. définir l’étendue de la règle.</span><span class="sxs-lookup"><span data-stu-id="80b7a-174">5. Set the rule scope.</span></span>
<span data-ttu-id="80b7a-175">Définissez l’étendue pour spécifier les appareils couverts par la règle.</span><span class="sxs-lookup"><span data-stu-id="80b7a-175">Set the scope to specify which devices are covered by the rule.</span></span> <span data-ttu-id="80b7a-176">L’étendue influe sur les règles qui vérifient les périphériques et n’affecte pas les règles qui vérifient uniquement les boîtes aux lettres et les comptes d’utilisateur ou les identités.</span><span class="sxs-lookup"><span data-stu-id="80b7a-176">The scope influences rules that check devices and doesn't affect rules that check only mailboxes and user accounts or identities.</span></span>

<span data-ttu-id="80b7a-177">Lors de la définition de l’étendue, vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="80b7a-177">When setting the scope, you can select:</span></span>

- <span data-ttu-id="80b7a-178">Tous les appareils</span><span class="sxs-lookup"><span data-stu-id="80b7a-178">All devices</span></span>
- <span data-ttu-id="80b7a-179">Groupes d’appareils spécifiques</span><span class="sxs-lookup"><span data-stu-id="80b7a-179">Specific device groups</span></span>

<span data-ttu-id="80b7a-180">Seules les données provenant d’appareils dans l’étendue seront interrogées.</span><span class="sxs-lookup"><span data-stu-id="80b7a-180">Only data from devices in scope will be queried.</span></span> <span data-ttu-id="80b7a-181">En outre, les actions ne seront effectuées que sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="80b7a-181">Also, actions will be taken only on those devices.</span></span>

### <a name="6-review-and-turn-on-the-rule"></a><span data-ttu-id="80b7a-182">6. Vérifiez et activez la règle.</span><span class="sxs-lookup"><span data-stu-id="80b7a-182">6. Review and turn on the rule.</span></span>
<span data-ttu-id="80b7a-183">Après avoir examiné la règle, cliquez sur **créer** pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="80b7a-183">After reviewing the rule, click **Create** to save it.</span></span> <span data-ttu-id="80b7a-184">La règle de détection personnalisée s’exécute immédiatement.</span><span class="sxs-lookup"><span data-stu-id="80b7a-184">The custom detection rule immediately runs.</span></span> <span data-ttu-id="80b7a-185">Il s’exécute à nouveau en fonction de la fréquence configurée pour vérifier les correspondances, générer des alertes et prendre des mesures de réponse.</span><span class="sxs-lookup"><span data-stu-id="80b7a-185">It runs again based on configured frequency to check for matches, generate alerts, and take response actions.</span></span>

## <a name="manage-existing-custom-detection-rules"></a><span data-ttu-id="80b7a-186">Gérer les règles de détection personnalisées existantes</span><span class="sxs-lookup"><span data-stu-id="80b7a-186">Manage existing custom detection rules</span></span>
<span data-ttu-id="80b7a-187">Vous pouvez afficher la liste des règles de détection personnalisées existantes, vérifier leurs exécutions précédentes et examiner les alertes qu’elles ont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="80b7a-187">You can view the list of existing custom detection rules, check their previous runs, and review the alerts they have triggered.</span></span> <span data-ttu-id="80b7a-188">Vous pouvez également exécuter une règle à la demande et la modifier.</span><span class="sxs-lookup"><span data-stu-id="80b7a-188">You can also run a rule on demand and modify it.</span></span>

### <a name="view-existing-rules"></a><span data-ttu-id="80b7a-189">Afficher les règles existantes</span><span class="sxs-lookup"><span data-stu-id="80b7a-189">View existing rules</span></span>

<span data-ttu-id="80b7a-190">Pour afficher toutes les règles de détection personnalisées existantes, **accédez à recherche** > **personnalisée**pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="80b7a-190">To view all existing custom detection rules, navigate to **Hunting** > **Custom detections**.</span></span> <span data-ttu-id="80b7a-191">La page répertorie toutes les règles avec les informations d’exécution suivantes :</span><span class="sxs-lookup"><span data-stu-id="80b7a-191">The page lists all the rules with the following run information:</span></span>

- <span data-ttu-id="80b7a-192">**Dernière exécution** : lors de la dernière exécution d’une règle pour rechercher les correspondances des requêtes et générer des alertes</span><span class="sxs-lookup"><span data-stu-id="80b7a-192">**Last run** — when a rule was last run to check for query matches and generate alerts</span></span>
- <span data-ttu-id="80b7a-193">**État de la dernière exécution** : indique si une règle a été exécutée avec succès</span><span class="sxs-lookup"><span data-stu-id="80b7a-193">**Last run status** — whether a rule ran successfully</span></span>
- <span data-ttu-id="80b7a-194">**Exécution suivante** : exécution planifiée suivante</span><span class="sxs-lookup"><span data-stu-id="80b7a-194">**Next run** — the next scheduled run</span></span>
- <span data-ttu-id="80b7a-195">**État** : indique si une règle a été activée ou désactivée</span><span class="sxs-lookup"><span data-stu-id="80b7a-195">**Status** — whether a rule has been turned on or off</span></span>

### <a name="view-rule-details-modify-rule-and-run-rule"></a><span data-ttu-id="80b7a-196">Afficher les détails de la règle, modifier la règle et exécuter la règle</span><span class="sxs-lookup"><span data-stu-id="80b7a-196">View rule details, modify rule, and run rule</span></span>

<span data-ttu-id="80b7a-197">Pour afficher des informations détaillées sur une règle de détection personnalisée, sélectionnez le nom de la **règle dans la** > liste des règles de recherche**personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="80b7a-197">To view comprehensive information about a custom detection rule, select the name of rule from the list of rules in **Hunting** > **Custom detections**.</span></span> <span data-ttu-id="80b7a-198">Cette opération ouvre une page sur la règle de détection personnalisée avec des informations générales sur la règle, notamment les détails de l’alerte, l’état d’exécution et l’étendue.</span><span class="sxs-lookup"><span data-stu-id="80b7a-198">This opens a page about the custom detection rule with general information about the rule, including the details of the alert, run status, and scope.</span></span> <span data-ttu-id="80b7a-199">Il fournit également la liste des alertes déclenchées et des actions déclenchées.</span><span class="sxs-lookup"><span data-stu-id="80b7a-199">It also provides the list of triggered alerts and triggered actions.</span></span>

<span data-ttu-id="80b7a-200">![Page des détails de la règle de détection personnalisée](../../media/custom-detection-details.png)</span><span class="sxs-lookup"><span data-stu-id="80b7a-200">![Custom detection rule details page](../../media/custom-detection-details.png)</span></span><br>
<span data-ttu-id="80b7a-201">*Détails de la règle de détection personnalisée*</span><span class="sxs-lookup"><span data-stu-id="80b7a-201">*Custom detection rule details*</span></span>

<span data-ttu-id="80b7a-202">Vous pouvez également effectuer les actions suivantes sur la règle à partir de cette page :</span><span class="sxs-lookup"><span data-stu-id="80b7a-202">You can also take the following actions on the rule from this page:</span></span>

- <span data-ttu-id="80b7a-203">**Exécuter** : exécuter la règle immédiatement.</span><span class="sxs-lookup"><span data-stu-id="80b7a-203">**Run** — run the rule immediately.</span></span> <span data-ttu-id="80b7a-204">Cela réinitialise également l’intervalle de la prochaine exécution.</span><span class="sxs-lookup"><span data-stu-id="80b7a-204">This also resets the interval for the next run.</span></span>
- <span data-ttu-id="80b7a-205">**Modifier** : modifier la règle sans modifier la requête</span><span class="sxs-lookup"><span data-stu-id="80b7a-205">**Edit** — modify the rule without changing the query</span></span>
- <span data-ttu-id="80b7a-206">**Requête modifier** : modifier la requête dans la recherche avancée</span><span class="sxs-lookup"><span data-stu-id="80b7a-206">**Modify query** — edit the query in advanced hunting</span></span>
- <span data-ttu-id="80b7a-207">**Activer**la fonctionnalité désactiver : activer la règle ou l’arrêter de s’exécuter.**Turn off**  / </span><span class="sxs-lookup"><span data-stu-id="80b7a-207">**Turn on** / **Turn off** — enable the rule or stop it from running</span></span>
- <span data-ttu-id="80b7a-208">**Supprimer** : désactiver la règle et la supprimer</span><span class="sxs-lookup"><span data-stu-id="80b7a-208">**Delete** — turn off the rule and remove it</span></span>

### <a name="view-and-manage-triggered-alerts"></a><span data-ttu-id="80b7a-209">Afficher et gérer les alertes déclenchées</span><span class="sxs-lookup"><span data-stu-id="80b7a-209">View and manage triggered alerts</span></span>

<span data-ttu-id="80b7a-210">Dans l’écran détails de la**règle (** > **recherche personnalisée** > de recherche **[nom de la règle]**), accédez à **alertes déclenchées** pour afficher la liste des alertes générées par correspondance à la règle.</span><span class="sxs-lookup"><span data-stu-id="80b7a-210">In the rule details screen (**Hunting** > **Custom detections** > **[Rule name]**), go to **Triggered alerts** to view the list of alerts generated by matches to the rule.</span></span> <span data-ttu-id="80b7a-211">Sélectionnez une alerte pour afficher des informations détaillées sur cette alerte et effectuez les actions suivantes sur cette alerte :</span><span class="sxs-lookup"><span data-stu-id="80b7a-211">Select an alert to view detailed information about that alert and take the following actions on that alert:</span></span>

- <span data-ttu-id="80b7a-212">Gérer l’alerte en définissant son état et sa classification (alerte true ou false)</span><span class="sxs-lookup"><span data-stu-id="80b7a-212">Manage the alert by setting its status and classification (true or false alert)</span></span>
- <span data-ttu-id="80b7a-213">Liaison de l’alerte à un incident</span><span class="sxs-lookup"><span data-stu-id="80b7a-213">Link the alert to an incident</span></span>
- <span data-ttu-id="80b7a-214">Exécuter la requête qui a déclenché l’alerte sur la chasse avancée</span><span class="sxs-lookup"><span data-stu-id="80b7a-214">Run the query that triggered the alert on advanced hunting</span></span>

### <a name="review-actions"></a><span data-ttu-id="80b7a-215">Examiner les actions</span><span class="sxs-lookup"><span data-stu-id="80b7a-215">Review actions</span></span>
<span data-ttu-id="80b7a-216">Dans l’écran**Détails de la règle (** > **recherche personnalisée** > de recherche **[nom de la règle]**), accédez à **actions déclenchées** pour afficher la liste des actions effectuées en fonction des correspondances avec la règle.</span><span class="sxs-lookup"><span data-stu-id="80b7a-216">In the rule details screen (**Hunting** > **Custom detections** > **[Rule name]**), go to **Triggered actions** to view the list of actions taken based on matches to the rule.</span></span>

>[!TIP]
><span data-ttu-id="80b7a-217">Pour afficher rapidement des informations et agir sur un élément d’un tableau, utilisez la colonne de sélection [&#10003;] à gauche du tableau.</span><span class="sxs-lookup"><span data-stu-id="80b7a-217">To quickly view information and take action on an item in a table, use the selection column [&#10003;] at the left of the table.</span></span>

## <a name="related-topic"></a><span data-ttu-id="80b7a-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b7a-218">Related topic</span></span>
- [<span data-ttu-id="80b7a-219">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="80b7a-219">Custom detections overview</span></span>](custom-detections-overview.md)
- [<span data-ttu-id="80b7a-220">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="80b7a-220">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="80b7a-221">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="80b7a-221">Learn the advanced hunting query language</span></span>](advanced-hunting-query-language.md)
