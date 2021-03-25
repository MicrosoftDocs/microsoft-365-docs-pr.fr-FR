---
title: Prendre des mesures sur les résultats de requête de recherche avancée dans la Protection Microsoft contre les menaces
description: Traiter rapidement les menaces et les ressources affectées dans vos résultats de requête de recherche avancée
keywords: repérage avancé, repérage de menace, repérage de cybermenace, mdatp, microsoft defender atp, recherche wdatp, requête, télémétrie, détections personnalisées, schéma, kusto, éviter le délai d’attente, lignes de commande, ID de processus
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
ms.openlocfilehash: 79d720a8b996f826548b79834e5d5c2048e28c2b
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067414"
---
# <a name="take-action-on-advanced-hunting-query-results"></a><span data-ttu-id="8639f-104">Prendre des mesures sur les résultats de requête de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="8639f-104">Take action on advanced hunting query results</span></span>

<span data-ttu-id="8639f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8639f-105">**Applies to:**</span></span>
- [<span data-ttu-id="8639f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8639f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

> <span data-ttu-id="8639f-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8639f-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="8639f-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8639f-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhuntingref-abovefoldlink)

<span data-ttu-id="8639f-109">Vous pouvez rapidement contenir des menaces ou [](advanced-hunting-overview.md) traiter les ressources compromises que vous trouvez dans le recherche avancée à l’aide d’options d’action puissantes et complètes.</span><span class="sxs-lookup"><span data-stu-id="8639f-109">You can quickly contain threats or address compromised assets that you find in [advanced hunting](advanced-hunting-overview.md) using powerful and comprehensive action options.</span></span> <span data-ttu-id="8639f-110">Avec ces options, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="8639f-110">With these options, you can:</span></span>

- <span data-ttu-id="8639f-111">Prendre différentes mesures sur les appareils</span><span class="sxs-lookup"><span data-stu-id="8639f-111">Take various actions on devices</span></span>
- <span data-ttu-id="8639f-112">Fichiers de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8639f-112">Quarantine files</span></span>

## <a name="required-permissions"></a><span data-ttu-id="8639f-113">Autorisations requises</span><span class="sxs-lookup"><span data-stu-id="8639f-113">Required permissions</span></span>

<span data-ttu-id="8639f-114">Pour être en mesure d’agir par le biais d’une recherche avancée, vous avez besoin d’un rôle dans Defender pour le point de terminaison avec des autorisations pour soumettre des actions de correction [sur les appareils.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/user-roles#permission-options)</span><span class="sxs-lookup"><span data-stu-id="8639f-114">To be able to take action through advanced hunting, you need a role in Defender for Endpoint with [permissions to submit remediation actions on devices](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/user-roles#permission-options).</span></span> <span data-ttu-id="8639f-115">Si vous ne pouvez pas agir, contactez un administrateur général pour obtenir l’autorisation suivante :</span><span class="sxs-lookup"><span data-stu-id="8639f-115">If you can't take action, contact a global administrator about getting the following permission:</span></span>

<span data-ttu-id="8639f-116">*Actions de correction actives > gestion des menaces et des vulnérabilités : gestion des corrections*</span><span class="sxs-lookup"><span data-stu-id="8639f-116">*Active remediation actions > Threat and vulnerability management - Remediation handling*</span></span>

## <a name="take-various-actions-on-devices"></a><span data-ttu-id="8639f-117">Prendre différentes mesures sur les appareils</span><span class="sxs-lookup"><span data-stu-id="8639f-117">Take various actions on devices</span></span>

<span data-ttu-id="8639f-118">Vous pouvez prendre les mesures suivantes sur les appareils identifiés par la `DeviceId` colonne dans les résultats de votre requête :</span><span class="sxs-lookup"><span data-stu-id="8639f-118">You can take the following actions on devices identified by the `DeviceId` column in your query results:</span></span>

- <span data-ttu-id="8639f-119">Isoler les appareils affectés pour contenir une infection ou empêcher les attaques de se déplacer ultérieurement</span><span class="sxs-lookup"><span data-stu-id="8639f-119">Isolate affected devices to contain an infection or prevent attacks from moving laterally</span></span>
- <span data-ttu-id="8639f-120">Collecter un package d’enquête pour obtenir plus d’informations d’investigation</span><span class="sxs-lookup"><span data-stu-id="8639f-120">Collect investigation package to obtain more forensic information</span></span>
- <span data-ttu-id="8639f-121">Exécuter une analyse antivirus pour rechercher et supprimer les menaces à l’aide des dernières mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8639f-121">Run an antivirus scan to find and remove threats using the latest security intelligence updates</span></span>
- <span data-ttu-id="8639f-122">Lancer une enquête automatisée pour vérifier et corriger les menaces sur l’appareil et éventuellement sur d’autres appareils concernés</span><span class="sxs-lookup"><span data-stu-id="8639f-122">Initiate an automated investigation to check and remediate threats on the device and possibly other affected devices</span></span>
- <span data-ttu-id="8639f-123">Restreindre l’exécution de l’application uniquement aux fichiers exécutables signés par Microsoft, ce qui empêche toute activité de menace ultérieure par le biais de programmes malveillants ou d’autres fichiers exécutables non signés</span><span class="sxs-lookup"><span data-stu-id="8639f-123">Restrict app execution to only Microsoft-signed executable files, preventing subsequent threat activity through malware or other untrusted executables</span></span>

<span data-ttu-id="8639f-124">Pour en savoir plus sur la façon dont ces actions de réponse sont effectuées via Defender pour le point de terminaison, lisez la suite sur les actions de [réponse sur les appareils.](respond-machine-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="8639f-124">To learn more about how these response actions are performed through Defender for Endpoint, [read about response actions on devices](respond-machine-alerts.md).</span></span>

## <a name="quarantine-files"></a><span data-ttu-id="8639f-125">Fichiers de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="8639f-125">Quarantine files</span></span>

<span data-ttu-id="8639f-126">Vous pouvez déployer l’action *de* mise en quarantaine sur les fichiers afin qu’ils soient automatiquement mis en quarantaine lorsqu’ils sont rencontrés.</span><span class="sxs-lookup"><span data-stu-id="8639f-126">You can deploy the *quarantine* action on files so that they are automatically quarantined when encountered.</span></span> <span data-ttu-id="8639f-127">Lorsque vous sélectionnez cette action, vous pouvez choisir entre les colonnes suivantes pour identifier les fichiers de votre requête qui sont mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="8639f-127">When selecting this action, you can choose between the following columns to identify which files in your query results to quarantine:</span></span>

- <span data-ttu-id="8639f-128">`SHA1` — Dans la plupart des tables de recherche avancées, il s’agit du SHA-1 du fichier affecté par l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8639f-128">`SHA1` — In most advanced hunting tables, this is the SHA-1 of the file that was affected by the recorded action.</span></span> <span data-ttu-id="8639f-129">Par exemple, si un fichier a été copié, il s’agit du fichier copié.</span><span class="sxs-lookup"><span data-stu-id="8639f-129">For example, if a file was copied, this would be the copied file.</span></span>
- <span data-ttu-id="8639f-130">`InitiatingProcessSHA1` — Dans la plupart des tables de recherche avancées, il s’agit du fichier responsable de l’initiative de l’action enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8639f-130">`InitiatingProcessSHA1` — In most advanced hunting tables, this is the file responsible for initiating the recorded action.</span></span> <span data-ttu-id="8639f-131">Par exemple, si un processus enfant a été lancé, il s’agit du processus parent.</span><span class="sxs-lookup"><span data-stu-id="8639f-131">For example, if a child process was launched, this would be the parent process.</span></span> 
- <span data-ttu-id="8639f-132">`SHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `SHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="8639f-132">`SHA256` — This is the SHA-256 equivalent of the file identified by the `SHA1` column.</span></span>
- <span data-ttu-id="8639f-133">`InitiatingProcessSHA256` — Il s’agit de l’équivalent SHA-256 du fichier identifié par la `InitiatingProcessSHA1` colonne.</span><span class="sxs-lookup"><span data-stu-id="8639f-133">`InitiatingProcessSHA256` — This is the SHA-256 equivalent of the file identified by the `InitiatingProcessSHA1` column.</span></span>

<span data-ttu-id="8639f-134">Pour en savoir plus sur la façon dont les actions de mise en quarantaine sont prises et sur la façon dont les fichiers peuvent être restaurés, consultez les actions de [réponse sur les fichiers.](respond-file-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="8639f-134">To learn more about how quarantine actions are taken and how files can be restored, [read about response actions on files](respond-file-alerts.md).</span></span>

>[!NOTE]
><span data-ttu-id="8639f-135">Pour localiser des fichiers et les mettre en quarantaine, les résultats de la requête doivent également inclure des valeurs en tant `DeviceId` qu’identificateurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="8639f-135">To locate files and quarantine them, the query results should also include `DeviceId` values as device identifiers.</span></span>  

## <a name="take-action"></a><span data-ttu-id="8639f-136">Prendre action</span><span class="sxs-lookup"><span data-stu-id="8639f-136">Take action</span></span>

<span data-ttu-id="8639f-137">Pour prendre l’une des actions décrites, sélectionnez un ou plusieurs enregistrements dans les résultats de votre requête, puis **sélectionnez Actions.**</span><span class="sxs-lookup"><span data-stu-id="8639f-137">To take any of the described actions, select one or more records in your query results and then select **Take actions**.</span></span> <span data-ttu-id="8639f-138">Un Assistant vous guide tout au long du processus de sélection, puis d’envoi de vos actions préférées.</span><span class="sxs-lookup"><span data-stu-id="8639f-138">A wizard will guide you through the process of selecting and then submitting your preferred actions.</span></span>

![Image de l’enregistrement sélectionné avec panneau pour l’inspection de l’enregistrement](images/ah-take-actions.png)

## <a name="review-actions-taken"></a><span data-ttu-id="8639f-140">Examiner les actions entreprises</span><span class="sxs-lookup"><span data-stu-id="8639f-140">Review actions taken</span></span>

<span data-ttu-id="8639f-141">Chaque action est enregistrée individuellement dans le centre de actions, sous Historique du **centre** de security.microsoft.com/action-center/history  >   ).[](https://security.microsoft.com/action-center/history)</span><span class="sxs-lookup"><span data-stu-id="8639f-141">Each action is individually recorded in the action center, under **Action center** > **History** ([security.microsoft.com/action-center/history](https://security.microsoft.com/action-center/history)).</span></span> <span data-ttu-id="8639f-142">Go to the action center to check the status of each action.</span><span class="sxs-lookup"><span data-stu-id="8639f-142">Go to the action center to check the status of each action.</span></span>
 
## <a name="related-topics"></a><span data-ttu-id="8639f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8639f-143">Related topics</span></span>

- [<span data-ttu-id="8639f-144">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8639f-144">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8639f-145">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="8639f-145">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="8639f-146">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8639f-146">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="8639f-147">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="8639f-147">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="8639f-148">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="8639f-148">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="8639f-149">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="8639f-149">Custom detections overview</span></span>](overview-custom-detections.md)
