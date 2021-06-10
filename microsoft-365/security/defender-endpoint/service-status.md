---
title: Vérifier l’état du service Point de terminaison Microsoft Defender
description: Vérifiez l’état du service Point de terminaison dans Microsoft Defender, vérifiez si le service rencontre des problèmes et examinez les problèmes précédents qui ont été résolus.
keywords: tableau de bord, service, problèmes, état du service, état actuel, historique des statuts, résumé de l’impact, cause racine préliminaire, résolution, temps de résolution, temps de résolution attendu
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
ms.openlocfilehash: 1b4545daace5df1a1a9c6e827f7d8f1b522a690c
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51687624"
---
# <a name="check-the-microsoft-defender-for-endpoint-service-health"></a><span data-ttu-id="31b8e-104">Vérifier l’état du service Point de terminaison Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="31b8e-104">Check the Microsoft Defender for Endpoint service health</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="31b8e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="31b8e-105">**Applies to:**</span></span>
- [<span data-ttu-id="31b8e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="31b8e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)



><span data-ttu-id="31b8e-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="31b8e-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="31b8e-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="31b8e-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-servicestatus-abovefoldlink)

<span data-ttu-id="31b8e-109">**L’état** du service fournit des informations sur l’état actuel du service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="31b8e-109">**Service health** provides information on the current status of the Defender for Endpoint service.</span></span> <span data-ttu-id="31b8e-110">Vous serez en mesure de vérifier que l’état du service est sain ou s’il existe des problèmes actuels.</span><span class="sxs-lookup"><span data-stu-id="31b8e-110">You'll be able to verify that the service health is healthy or if there are current issues.</span></span> <span data-ttu-id="31b8e-111">S’il existe des problèmes, vous verrez des informations telles que le moment où le problème a été détecté, la cause racine préliminaire et le temps de résolution attendu.</span><span class="sxs-lookup"><span data-stu-id="31b8e-111">If there are issues, you'll see information such as when the issue was detected, what the preliminary root cause is, and the expected resolution time.</span></span>

<span data-ttu-id="31b8e-112">Vous verrez également des informations sur les problèmes historiques qui ont été résolus et des détails tels que la date et l’heure de résolution du problème.</span><span class="sxs-lookup"><span data-stu-id="31b8e-112">You'll also see information on historical issues that have been resolved and details such as the date and time when the issue was resolved.</span></span> <span data-ttu-id="31b8e-113">Lorsqu’il n’y a aucun problème sur le service, vous voyez un état sain.</span><span class="sxs-lookup"><span data-stu-id="31b8e-113">When there are no issues on the service, you'll see a healthy status.</span></span>

<span data-ttu-id="31b8e-114">Vous pouvez afficher des détails sur l’état  du service en cliquant sur la vignette à partir du tableau de bord Opérations de sécurité ou en sélectionnant le menu d’état du **service** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="31b8e-114">You can view details on the service health by clicking the tile from the **Security operations dashboard** or selecting the **Service health** menu from the navigation pane.</span></span>

<span data-ttu-id="31b8e-115">La page **Détails de l’état** du service possède les onglets suivants :</span><span class="sxs-lookup"><span data-stu-id="31b8e-115">The **Service health** details page has the following tabs:</span></span>

- <span data-ttu-id="31b8e-116">**État actuel**</span><span class="sxs-lookup"><span data-stu-id="31b8e-116">**Current status**</span></span>
- <span data-ttu-id="31b8e-117">**Historique des statuts**</span><span class="sxs-lookup"><span data-stu-id="31b8e-117">**Status history**</span></span>

## <a name="current-status"></a><span data-ttu-id="31b8e-118">État actuel</span><span class="sxs-lookup"><span data-stu-id="31b8e-118">Current status</span></span>
<span data-ttu-id="31b8e-119">**L’onglet État** actuel affiche l’état actuel du service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="31b8e-119">The **Current status** tab shows the current state of the Defender for Endpoint service.</span></span> <span data-ttu-id="31b8e-120">Lorsque le service s’exécute sans problème, l’état d’un service sain s’affiche.</span><span class="sxs-lookup"><span data-stu-id="31b8e-120">When the service is running smoothly a healthy service health is shown.</span></span> <span data-ttu-id="31b8e-121">S’il existe des problèmes, les détails de service suivants sont affichés pour vous aider à mieux comprendre le problème :</span><span class="sxs-lookup"><span data-stu-id="31b8e-121">If there are issues seen, the following service details are shown to help you gain better insight about the issue:</span></span>

- <span data-ttu-id="31b8e-122">Date et heure de détection du problème</span><span class="sxs-lookup"><span data-stu-id="31b8e-122">Date and time for when the issue was detected</span></span>
- <span data-ttu-id="31b8e-123">Brève description du problème</span><span class="sxs-lookup"><span data-stu-id="31b8e-123">A short description of the issue</span></span>
- <span data-ttu-id="31b8e-124">Heure de mise à jour</span><span class="sxs-lookup"><span data-stu-id="31b8e-124">Update time</span></span>
- <span data-ttu-id="31b8e-125">Résumé de l’impact</span><span class="sxs-lookup"><span data-stu-id="31b8e-125">Summary of impact</span></span>
- <span data-ttu-id="31b8e-126">Cause première préliminaire</span><span class="sxs-lookup"><span data-stu-id="31b8e-126">Preliminary root cause</span></span>
- <span data-ttu-id="31b8e-127">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="31b8e-127">Next steps</span></span>
- <span data-ttu-id="31b8e-128">Temps de résolution attendu</span><span class="sxs-lookup"><span data-stu-id="31b8e-128">Expected resolution time</span></span>

<span data-ttu-id="31b8e-129">Les mises à jour de la progression d’un problème sont reflétées sur la page à mesure que le problème est résolu.</span><span class="sxs-lookup"><span data-stu-id="31b8e-129">Updates on the progress of an issue are reflected on the page as the issue gets resolved.</span></span> <span data-ttu-id="31b8e-130">Vous verrez des mises à jour sur des informations telles qu’une estimation du temps de résolution mise à jour ou les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="31b8e-130">You'll see updates on information such as an updated estimate resolution time or next steps.</span></span>

<span data-ttu-id="31b8e-131">Lorsqu’un problème est résolu, il est enregistré dans l’onglet Historique **des** états.</span><span class="sxs-lookup"><span data-stu-id="31b8e-131">When an issue is resolved, it gets recorded in the **Status history** tab.</span></span>

## <a name="status-history"></a><span data-ttu-id="31b8e-132">Historique des statuts</span><span class="sxs-lookup"><span data-stu-id="31b8e-132">Status history</span></span>
<span data-ttu-id="31b8e-133">**L’onglet Historique** des états reflète tous les problèmes historiques qui ont été vus et résolus.</span><span class="sxs-lookup"><span data-stu-id="31b8e-133">The **Status history** tab reflects all the historical issues that were seen and resolved.</span></span> <span data-ttu-id="31b8e-134">Vous verrez des détails sur les problèmes résolus, ainsi que les autres informations incluses pendant leur résolution.</span><span class="sxs-lookup"><span data-stu-id="31b8e-134">You'll see details of the resolved issues along with the other information that were included while it was being resolved.</span></span>

### <a name="related-topic"></a><span data-ttu-id="31b8e-135">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="31b8e-135">Related topic</span></span>
- [<span data-ttu-id="31b8e-136">Afficher le tableau de bord Opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="31b8e-136">View the Security operations dashboard</span></span>](security-operations-dashboard.md)
