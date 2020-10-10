---
title: Effectuer des actions sur les résultats de la recherche avancée dans Microsoft Threat Protection
description: Résoudre rapidement les menaces et les ressources affectées dans vos résultats de recherche avancée de la chasse
keywords: chasse aux menaces, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, effectuer une action
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
ms.collection:
- M365-security-compliance
- m365-initiative-m365-defender
ms.topic: article
ms.openlocfilehash: 3d2df325198c420cb2444a74b6c3507657355012
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48412093"
---
# <a name="take-action-on-advanced-hunting-query-results"></a><span data-ttu-id="a58d0-104">Effectuer des actions sur les résultats de la recherche avancée de la chasse</span><span class="sxs-lookup"><span data-stu-id="a58d0-104">Take action on advanced hunting query results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a58d0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a58d0-105">**Applies to:**</span></span>
- <span data-ttu-id="a58d0-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a58d0-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="a58d0-107">Vous pouvez rapidement contenir des menaces ou des ressources d’adresses compromises que vous trouvez dans la recherche [avancée](advanced-hunting-overview.md) à l’aide d’actions puissantes et complètes.</span><span class="sxs-lookup"><span data-stu-id="a58d0-107">You can quickly contain threats or address compromised assets that you find in [advanced hunting](advanced-hunting-overview.md) using powerful and comprehensive action options.</span></span> <span data-ttu-id="a58d0-108">Avec ces options, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="a58d0-108">With these options, you can:</span></span>

- <span data-ttu-id="a58d0-109">Effectuer différentes actions sur les appareils</span><span class="sxs-lookup"><span data-stu-id="a58d0-109">Take various actions on devices</span></span>
- <span data-ttu-id="a58d0-110">Mettre en quarantaine les fichiers</span><span class="sxs-lookup"><span data-stu-id="a58d0-110">Quarantine files</span></span>

## <a name="required-permissions"></a><span data-ttu-id="a58d0-111">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="a58d0-111">Required permissions</span></span>
<span data-ttu-id="a58d0-112">Pour pouvoir prendre des mesures par le biais de la chasse avancée, vous avez besoin d’un rôle dans Microsoft Defender ATP avec des [autorisations pour soumettre des actions de correction sur les appareils](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles#permission-options).</span><span class="sxs-lookup"><span data-stu-id="a58d0-112">To be able to take action through advanced hunting, you need a role in Microsoft Defender ATP with [permissions to submit remediation actions on devices](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles#permission-options).</span></span> <span data-ttu-id="a58d0-113">Si vous ne pouvez pas agir, contactez un administrateur général pour obtenir l’autorisation suivante :</span><span class="sxs-lookup"><span data-stu-id="a58d0-113">If you can't take action, contact a global administrator about getting the following permission:</span></span>

<span data-ttu-id="a58d0-114">*Actions de correction actives > gestion des menaces et des vulnérabilités-gestion des corrections*</span><span class="sxs-lookup"><span data-stu-id="a58d0-114">*Active remediation actions > Threat and vulnerability management - Remediation handling*</span></span>

## <a name="take-various-actions-on-devices"></a><span data-ttu-id="a58d0-115">Effectuer différentes actions sur les appareils</span><span class="sxs-lookup"><span data-stu-id="a58d0-115">Take various actions on devices</span></span>
<span data-ttu-id="a58d0-116">Vous pouvez effectuer les actions suivantes sur les appareils identifiés par la `DeviceId` colonne dans les résultats de la requête :</span><span class="sxs-lookup"><span data-stu-id="a58d0-116">You can take the following actions on devices identified by the `DeviceId` column in you query results:</span></span>

- <span data-ttu-id="a58d0-117">Isoler les appareils affectés pour contenir une infection ou empêcher les attaques de se déplacer plus tard</span><span class="sxs-lookup"><span data-stu-id="a58d0-117">Isolate affected devices to contain an infection or prevent attacks from moving laterally</span></span>
- <span data-ttu-id="a58d0-118">Collecter les packages d’enquête pour obtenir des informations plus légales</span><span class="sxs-lookup"><span data-stu-id="a58d0-118">Collect investigation package to obtain more forensic information</span></span>
- <span data-ttu-id="a58d0-119">Exécuter une analyse antivirus pour rechercher et supprimer les menaces à l’aide des dernières mises à jour de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="a58d0-119">Run an antivirus scan to find and remove threats using the latest security intelligence updates</span></span>
- <span data-ttu-id="a58d0-120">Lancer une enquête automatisée pour vérifier et corriger les menaces sur l’appareil et éventuellement sur d’autres appareils affectés</span><span class="sxs-lookup"><span data-stu-id="a58d0-120">Initiate an automated investigation to check and remediate threats on the device and possibly other affected devices</span></span>
- <span data-ttu-id="a58d0-121">Limiter l’exécution de l’application aux seuls fichiers exécutables signés par Microsoft, ce qui empêche les activités de menace ultérieures par des programmes malveillants ou d’autres fichiers exécutables non approuvés</span><span class="sxs-lookup"><span data-stu-id="a58d0-121">Restrict app execution to only Microsoft-signed executable files, preventing subsequent threat activity through malware or other untrusted executables</span></span>

<span data-ttu-id="a58d0-122">Pour plus d’informations sur l’exécution de ces actions de réponse via Microsoft Defender ATP, lisez la rubrique [about Response actions on Devices](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts).</span><span class="sxs-lookup"><span data-stu-id="a58d0-122">To learn more about how these response actions are performed through Microsoft Defender ATP, [read about response actions on devices](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts).</span></span>
   
## <a name="quarantine-files"></a><span data-ttu-id="a58d0-123">Mettre en quarantaine les fichiers</span><span class="sxs-lookup"><span data-stu-id="a58d0-123">Quarantine files</span></span>
<span data-ttu-id="a58d0-124">Vous pouvez déployer l’action de *mise en quarantaine* sur les fichiers afin qu’ils soient automatiquement mis en quarantaine lorsqu’ils sont détectés.</span><span class="sxs-lookup"><span data-stu-id="a58d0-124">You can deploy the *quarantine* action on files so that they are automatically quarantined when encountered.</span></span> <span data-ttu-id="a58d0-125">Lors de la sélection de cette action, vous pouvez choisir entre les colonnes suivantes pour identifier les fichiers de la requête à mettre en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a58d0-125">When selecting this action, you can choose between the following columns to identify which files in your query results to quarantine:</span></span>

- <span data-ttu-id="a58d0-126">`SHA1` — Dans la plupart des tableaux de la chasse avancée, il s’agit du SHA-1 du fichier qui a été affecté par l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="a58d0-126">`SHA1` — In most advanced hunting tables, this is the SHA-1 of the file that was affected by the recorded action.</span></span> <span data-ttu-id="a58d0-127">Par exemple, si un fichier a été copié, il s’agit du fichier copié.</span><span class="sxs-lookup"><span data-stu-id="a58d0-127">For example, if a file was copied, this would be the copied file.</span></span>
- <span data-ttu-id="a58d0-128">`InitiatingProcessSHA1` — Dans la plupart des tableaux de la chasse avancée, il s’agit du fichier responsable de l’initialisation de l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="a58d0-128">`InitiatingProcessSHA1` — In most advanced hunting tables, this is the file responsible for initiating the recorded action.</span></span> <span data-ttu-id="a58d0-129">Par exemple, si un processus enfant a été lancé, il s’agit du processus parent.</span><span class="sxs-lookup"><span data-stu-id="a58d0-129">For example, if a child process was launched, this would be the parent process.</span></span> 
- <span data-ttu-id="a58d0-130">`SHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `SHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="a58d0-130">`SHA256` — This is the SHA-256 equivalent of the file identified by the `SHA1` column.</span></span>
- <span data-ttu-id="a58d0-131">`InitiatingProcessSHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `InitiatingProcessSHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="a58d0-131">`InitiatingProcessSHA256` — This is the SHA-256 equivalent of the file identified by the `InitiatingProcessSHA1` column.</span></span>

<span data-ttu-id="a58d0-132">Pour en savoir plus sur la façon dont les actions de mise en quarantaine sont effectuées et sur la manière dont les fichiers peuvent être restaurés, consultez la rubrique [actions Response sur les fichiers](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-file-alerts).</span><span class="sxs-lookup"><span data-stu-id="a58d0-132">To learn more about how quarantine actions are taken and how files can be restored, [read about response actions on files](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-file-alerts).</span></span>

>[!NOTE]
><span data-ttu-id="a58d0-133">Pour localiser des fichiers et les mettre en quarantaine, les résultats de la requête doivent également inclure des `DeviceId` valeurs en tant qu’identificateurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="a58d0-133">To locate files and quarantine them, the query results should also include `DeviceId` values as device identifiers.</span></span>  

## <a name="take-action"></a><span data-ttu-id="a58d0-134">Effectuer une action</span><span class="sxs-lookup"><span data-stu-id="a58d0-134">Take action</span></span>
<span data-ttu-id="a58d0-135">Pour effectuer l’une des actions décrites, sélectionnez un ou plusieurs enregistrements dans les résultats de votre requête, puis sélectionnez **prendre les actions**.</span><span class="sxs-lookup"><span data-stu-id="a58d0-135">To take any of the described actions, select one or more records in your query results and then select **Take actions**.</span></span> <span data-ttu-id="a58d0-136">Un Assistant vous guide tout au long du processus de sélection et d’envoi de vos actions favorites.</span><span class="sxs-lookup"><span data-stu-id="a58d0-136">A wizard will guide you through the process of selecting and then submitting your preferred actions.</span></span>

![Image de l’enregistrement sélectionné avec le panneau pour inspecter l’enregistrement](../../media/mtp-ah/ah-take-actions.png)

## <a name="review-actions-taken"></a><span data-ttu-id="a58d0-138">Examiner les actions effectuées</span><span class="sxs-lookup"><span data-stu-id="a58d0-138">Review actions taken</span></span>
<span data-ttu-id="a58d0-139">Chaque action est enregistrée individuellement dans le [Centre de notifications](mtp-action-center.md) sous historique du **Centre de notifications**  >  **History** ([Security.Microsoft.com/Action-Center/History](https://security.microsoft.com/action-center/history)).</span><span class="sxs-lookup"><span data-stu-id="a58d0-139">Each action is individually recorded in the [action center](mtp-action-center.md) under **Action center** > **History** ([security.microsoft.com/action-center/history](https://security.microsoft.com/action-center/history)).</span></span> <span data-ttu-id="a58d0-140">Accédez au centre de notifications pour vérifier l’état de chaque action.</span><span class="sxs-lookup"><span data-stu-id="a58d0-140">Go to the action center to check the status of each action.</span></span>
 
## <a name="related-topics"></a><span data-ttu-id="a58d0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a58d0-141">Related topics</span></span>
- [<span data-ttu-id="a58d0-142">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a58d0-142">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a58d0-143">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a58d0-143">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="a58d0-144">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="a58d0-144">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="a58d0-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="a58d0-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="a58d0-146">Vue d’ensemble du centre de notifications</span><span class="sxs-lookup"><span data-stu-id="a58d0-146">Action center overview</span></span>](mtp-action-center.md)
