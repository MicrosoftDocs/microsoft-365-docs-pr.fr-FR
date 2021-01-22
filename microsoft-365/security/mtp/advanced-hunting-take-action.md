---
title: Prendre des mesures sur les résultats de requête de recherche avancée dans Microsoft 365 Defender
description: Traiter rapidement les menaces et les ressources affectées dans vos résultats de requête de recherche avancée
keywords: recherche avancée, recherche de menace, recherche de cybermenace, protection microsoft contre les menaces, microsoft 365, mtp, m365, recherche, requête, télémétrie, prendre des mesures
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 9e8ad544cfe17d0d8e5c895e208b42ec56555565
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932177"
---
# <a name="take-action-on-advanced-hunting-query-results"></a><span data-ttu-id="5c190-104">Prendre des mesures sur les résultats de requête de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="5c190-104">Take action on advanced hunting query results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="5c190-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5c190-105">**Applies to:**</span></span>
- <span data-ttu-id="5c190-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5c190-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="5c190-107">Vous pouvez rapidement contenir des menaces ou [](advanced-hunting-overview.md) traiter les ressources compromises que vous trouvez dans le recherche avancée à l’aide d’options d’action puissantes et complètes.</span><span class="sxs-lookup"><span data-stu-id="5c190-107">You can quickly contain threats or address compromised assets that you find in [advanced hunting](advanced-hunting-overview.md) using powerful and comprehensive action options.</span></span> <span data-ttu-id="5c190-108">Avec ces options, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5c190-108">With these options, you can:</span></span>

- <span data-ttu-id="5c190-109">Prendre différentes mesures sur les appareils</span><span class="sxs-lookup"><span data-stu-id="5c190-109">Take various actions on devices</span></span>
- <span data-ttu-id="5c190-110">Fichiers de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="5c190-110">Quarantine files</span></span>

## <a name="required-permissions"></a><span data-ttu-id="5c190-111">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="5c190-111">Required permissions</span></span>
<span data-ttu-id="5c190-112">Pour être en mesure d’agir par le biais d’une recherche avancée, vous avez besoin d’un rôle dans Microsoft Defender pour le point de terminaison avec des autorisations pour soumettre des actions de correction [sur les appareils.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles#permission-options)</span><span class="sxs-lookup"><span data-stu-id="5c190-112">To be able to take action through advanced hunting, you need a role in Microsoft Defender for Endpoint with [permissions to submit remediation actions on devices](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles#permission-options).</span></span> <span data-ttu-id="5c190-113">Si vous ne pouvez pas agir, contactez un administrateur général pour obtenir l’autorisation suivante :</span><span class="sxs-lookup"><span data-stu-id="5c190-113">If you can't take action, contact a global administrator about getting the following permission:</span></span>

<span data-ttu-id="5c190-114">*Actions de correction actives > gestion des menaces et des vulnérabilités : gestion des corrections*</span><span class="sxs-lookup"><span data-stu-id="5c190-114">*Active remediation actions > Threat and vulnerability management - Remediation handling*</span></span>

## <a name="take-various-actions-on-devices"></a><span data-ttu-id="5c190-115">Prendre différentes mesures sur les appareils</span><span class="sxs-lookup"><span data-stu-id="5c190-115">Take various actions on devices</span></span>
<span data-ttu-id="5c190-116">Vous pouvez prendre les mesures suivantes sur les appareils identifiés par la `DeviceId` colonne dans les résultats de la requête :</span><span class="sxs-lookup"><span data-stu-id="5c190-116">You can take the following actions on devices identified by the `DeviceId` column in you query results:</span></span>

- <span data-ttu-id="5c190-117">Isoler les appareils affectés pour contenir une infection ou empêcher les attaques de se déplacer ultérieurement</span><span class="sxs-lookup"><span data-stu-id="5c190-117">Isolate affected devices to contain an infection or prevent attacks from moving laterally</span></span>
- <span data-ttu-id="5c190-118">Collecter un package d’enquête pour obtenir plus d’informations d’investigation</span><span class="sxs-lookup"><span data-stu-id="5c190-118">Collect investigation package to obtain more forensic information</span></span>
- <span data-ttu-id="5c190-119">Exécuter une analyse antivirus pour rechercher et supprimer les menaces à l’aide des dernières mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="5c190-119">Run an antivirus scan to find and remove threats using the latest security intelligence updates</span></span>
- <span data-ttu-id="5c190-120">Lancer un examen automatisé pour vérifier et corriger les menaces sur l’appareil et éventuellement sur d’autres appareils concernés</span><span class="sxs-lookup"><span data-stu-id="5c190-120">Initiate an automated investigation to check and remediate threats on the device and possibly other affected devices</span></span>
- <span data-ttu-id="5c190-121">Restreindre l’exécution de l’application uniquement aux fichiers exécutables signés par Microsoft, ce qui empêche toute activité de menace ultérieure par le biais de programmes malveillants ou d’autres fichiers exécutables non signés</span><span class="sxs-lookup"><span data-stu-id="5c190-121">Restrict app execution to only Microsoft-signed executable files, preventing subsequent threat activity through malware or other untrusted executables</span></span>

<span data-ttu-id="5c190-122">Pour en savoir plus sur la façon dont ces actions de réponse sont effectuées via Microsoft Defender pour le point de terminaison, consultez les actions de [réponse sur les appareils.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts)</span><span class="sxs-lookup"><span data-stu-id="5c190-122">To learn more about how these response actions are performed through Microsoft Defender for Endpoint, [read about response actions on devices](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts).</span></span>
   
## <a name="quarantine-files"></a><span data-ttu-id="5c190-123">Fichiers de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="5c190-123">Quarantine files</span></span>
<span data-ttu-id="5c190-124">Vous pouvez déployer l’action *de* mise en quarantaine sur les fichiers afin qu’ils soient automatiquement mis en quarantaine lorsqu’ils sont rencontrés.</span><span class="sxs-lookup"><span data-stu-id="5c190-124">You can deploy the *quarantine* action on files so that they are automatically quarantined when encountered.</span></span> <span data-ttu-id="5c190-125">Lorsque vous sélectionnez cette action, vous pouvez choisir entre les colonnes suivantes pour identifier les fichiers de votre requête qui sont mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="5c190-125">When selecting this action, you can choose between the following columns to identify which files in your query results to quarantine:</span></span>

- <span data-ttu-id="5c190-126">`SHA1` — Dans la plupart des tables de recherche avancées, il s’agit du SHA-1 du fichier affecté par l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="5c190-126">`SHA1` — In most advanced hunting tables, this is the SHA-1 of the file that was affected by the recorded action.</span></span> <span data-ttu-id="5c190-127">Par exemple, si un fichier a été copié, il s’agit du fichier copié.</span><span class="sxs-lookup"><span data-stu-id="5c190-127">For example, if a file was copied, this would be the copied file.</span></span>
- <span data-ttu-id="5c190-128">`InitiatingProcessSHA1` — Dans la plupart des tables de recherche avancées, il s’agit du fichier responsable de l’initiative de l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="5c190-128">`InitiatingProcessSHA1` — In most advanced hunting tables, this is the file responsible for initiating the recorded action.</span></span> <span data-ttu-id="5c190-129">Par exemple, si un processus enfant a été lancé, il s’agit du processus parent.</span><span class="sxs-lookup"><span data-stu-id="5c190-129">For example, if a child process was launched, this would be the parent process.</span></span> 
- <span data-ttu-id="5c190-130">`SHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `SHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="5c190-130">`SHA256` — This is the SHA-256 equivalent of the file identified by the `SHA1` column.</span></span>
- <span data-ttu-id="5c190-131">`InitiatingProcessSHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `InitiatingProcessSHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="5c190-131">`InitiatingProcessSHA256` — This is the SHA-256 equivalent of the file identified by the `InitiatingProcessSHA1` column.</span></span>

<span data-ttu-id="5c190-132">Pour en savoir plus sur la façon dont les actions de mise en quarantaine sont prises et sur la façon dont les fichiers peuvent être restaurés, consultez les actions de [réponse sur les fichiers.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-file-alerts)</span><span class="sxs-lookup"><span data-stu-id="5c190-132">To learn more about how quarantine actions are taken and how files can be restored, [read about response actions on files](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-file-alerts).</span></span>

>[!NOTE]
><span data-ttu-id="5c190-133">Pour localiser des fichiers et les mettre en quarantaine, les résultats de la requête doivent également inclure des valeurs en tant `DeviceId` qu’identificateurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="5c190-133">To locate files and quarantine them, the query results should also include `DeviceId` values as device identifiers.</span></span>  

## <a name="take-action"></a><span data-ttu-id="5c190-134">Prendre des mesures</span><span class="sxs-lookup"><span data-stu-id="5c190-134">Take action</span></span>
<span data-ttu-id="5c190-135">Pour prendre l’une des actions décrites, sélectionnez un ou plusieurs enregistrements dans les résultats de votre requête, puis **sélectionnez Actions.**</span><span class="sxs-lookup"><span data-stu-id="5c190-135">To take any of the described actions, select one or more records in your query results and then select **Take actions**.</span></span> <span data-ttu-id="5c190-136">Un Assistant vous guide tout au long du processus de sélection, puis d’envoi de vos actions préférées.</span><span class="sxs-lookup"><span data-stu-id="5c190-136">A wizard will guide you through the process of selecting and then submitting your preferred actions.</span></span>

![Image de l’enregistrement sélectionné avec panneau pour l’inspection de l’enregistrement](../../media/mtp-ah/ah-take-actions.png)

## <a name="review-actions-taken"></a><span data-ttu-id="5c190-138">Examiner les actions entreprises</span><span class="sxs-lookup"><span data-stu-id="5c190-138">Review actions taken</span></span>
<span data-ttu-id="5c190-139">Chaque action est enregistrée individuellement dans le centre de [l’action](mtp-action-center.md) sous **Historique** du centre de security.microsoft.com/action-center/history  >   ).[](https://security.microsoft.com/action-center/history)</span><span class="sxs-lookup"><span data-stu-id="5c190-139">Each action is individually recorded in the [action center](mtp-action-center.md) under **Action center** > **History** ([security.microsoft.com/action-center/history](https://security.microsoft.com/action-center/history)).</span></span> <span data-ttu-id="5c190-140">Go to the action center to check the status of each action.</span><span class="sxs-lookup"><span data-stu-id="5c190-140">Go to the action center to check the status of each action.</span></span>
 
## <a name="related-topics"></a><span data-ttu-id="5c190-141">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="5c190-141">Related topics</span></span>
- [<span data-ttu-id="5c190-142">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5c190-142">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5c190-143">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="5c190-143">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="5c190-144">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="5c190-144">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="5c190-145">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="5c190-145">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="5c190-146">Vue d’ensemble du centre de données</span><span class="sxs-lookup"><span data-stu-id="5c190-146">Action center overview</span></span>](mtp-action-center.md)
