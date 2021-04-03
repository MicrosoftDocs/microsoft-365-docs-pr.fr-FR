---
title: Recommandations en matière de sécurité par gestion des menaces et des vulnérabilités
description: Obtenez des recommandations de sécurité actionnables prioritaires par menace, probabilité de violation et valeur dans la gestion des menaces et des vulnérabilités.
keywords: gestion des menaces et des vulnérabilités, recommandation sur la sécurité tvm mdatp, recommandation en matière de cybersécurité, recommandation de sécurité actionnable
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 97d496271c1ef7185419f7d39956da0429f070aa
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500490"
---
# <a name="security-recommendations---threat-and-vulnerability-management"></a><span data-ttu-id="737e9-104">Recommandations en matière de sécurité : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="737e9-104">Security recommendations - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="737e9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="737e9-105">**Applies to:**</span></span>

- [<span data-ttu-id="737e9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="737e9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="737e9-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="737e9-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="737e9-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="737e9-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="737e9-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="737e9-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="737e9-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="737e9-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="737e9-111">Les faiblesses de cybersécurité identifiées dans votre organisation sont mappées à des recommandations de sécurité actionnables et hiérarchisées par leur impact.</span><span class="sxs-lookup"><span data-stu-id="737e9-111">Cybersecurity weaknesses identified in your organization are mapped to actionable security recommendations and prioritized by their impact.</span></span> <span data-ttu-id="737e9-112">Les recommandations hiérarchisées permettent de raccourcir le temps d’atténuation ou de correction des vulnérabilités et de stimuler la conformité.</span><span class="sxs-lookup"><span data-stu-id="737e9-112">Prioritized recommendations help shorten the time to mitigate or remediate vulnerabilities and drive compliance.</span></span>

<span data-ttu-id="737e9-113">Chaque recommandation de sécurité inclut des étapes de correction actionnables.</span><span class="sxs-lookup"><span data-stu-id="737e9-113">Each security recommendation includes actionable remediation steps.</span></span> <span data-ttu-id="737e9-114">Pour faciliter la gestion des tâches, vous pouvez également envoyer la recommandation à l’aide de Microsoft Intune et de Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="737e9-114">To help with task management, the recommendation can also be sent using Microsoft Intune and Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="737e9-115">Lorsque le paysage des menaces change, la recommandation change également lorsqu’elle collecte en permanence des informations à partir de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="737e9-115">When the threat landscape changes, the recommendation also changes as it continuously collects information from your environment.</span></span>

>[!TIP]
><span data-ttu-id="737e9-116">Pour obtenir des e-mails sur les nouveaux événements de vulnérabilité, voir Configurer les notifications par courrier électronique de vulnérabilité [dans Microsoft Defender pour le point de terminaison](configure-vulnerability-email-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="737e9-116">To get emails about new vulnerability events, see [Configure vulnerability email notifications in Microsoft Defender for Endpoint](configure-vulnerability-email-notifications.md)</span></span>

## <a name="how-it-works"></a><span data-ttu-id="737e9-117">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="737e9-117">How it works</span></span>

<span data-ttu-id="737e9-118">Chaque appareil de l’organisation est marqué en fonction de trois facteurs importants pour aider les clients à se concentrer sur les bonnes choses au bon moment.</span><span class="sxs-lookup"><span data-stu-id="737e9-118">Each device in the organization is scored based on three important factors to help customers to focus on the right things at the right time.</span></span>

- <span data-ttu-id="737e9-119">**Menace** : caractéristiques des vulnérabilités et des exploits dans les appareils et l’historique des violations de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="737e9-119">**Threat** - Characteristics of the vulnerabilities and exploits in your organizations' devices and breach history.</span></span> <span data-ttu-id="737e9-120">En fonction de ces facteurs, les recommandations de sécurité indiquent les liens correspondants vers les alertes actives, les campagnes contre les menaces en cours et leurs rapports analytiques sur les menaces correspondants.</span><span class="sxs-lookup"><span data-stu-id="737e9-120">Based on these factors, the security recommendations show the corresponding links to active alerts, ongoing threat campaigns, and their corresponding threat analytic reports.</span></span>

- <span data-ttu-id="737e9-121">**Probabilité de violation** : posture de sécurité et résilience de votre organisation contre les menaces</span><span class="sxs-lookup"><span data-stu-id="737e9-121">**Breach likelihood** - Your organization's security posture and resilience against threats</span></span>

- <span data-ttu-id="737e9-122">**Valeur commerciale** : ressources de votre organisation, processus critiques et propriétés intellectuelles</span><span class="sxs-lookup"><span data-stu-id="737e9-122">**Business value** - Your organization's assets, critical processes, and intellectual properties</span></span>

## <a name="navigate-to-the-security-recommendations-page"></a><span data-ttu-id="737e9-123">Accéder à la page Recommandations en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="737e9-123">Navigate to the Security recommendations page</span></span>

<span data-ttu-id="737e9-124">Accédez à la page Recommandations de sécurité de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="737e9-124">Access the Security recommendations page a few different ways:</span></span>

- <span data-ttu-id="737e9-125">Menu de navigation de gestion des menaces et des vulnérabilités dans le [Centre de sécurité Microsoft Defender](portal-overview.md)</span><span class="sxs-lookup"><span data-stu-id="737e9-125">Threat and vulnerability management navigation menu in the [Microsoft Defender Security Center](portal-overview.md)</span></span>
- <span data-ttu-id="737e9-126">Principales recommandations en matière de sécurité dans le tableau de bord de gestion des [menaces et des vulnérabilités](tvm-dashboard-insights.md)</span><span class="sxs-lookup"><span data-stu-id="737e9-126">Top security recommendations in the [threat and vulnerability management dashboard](tvm-dashboard-insights.md)</span></span>

<span data-ttu-id="737e9-127">Affichez les recommandations de sécurité associées aux endroits suivants :</span><span class="sxs-lookup"><span data-stu-id="737e9-127">View related security recommendations in the following places:</span></span>

- <span data-ttu-id="737e9-128">Page de logiciels</span><span class="sxs-lookup"><span data-stu-id="737e9-128">Software page</span></span>
- <span data-ttu-id="737e9-129">Page Appareil</span><span class="sxs-lookup"><span data-stu-id="737e9-129">Device page</span></span>

### <a name="navigation-menu"></a><span data-ttu-id="737e9-130">Menu de navigation</span><span class="sxs-lookup"><span data-stu-id="737e9-130">Navigation menu</span></span>

<span data-ttu-id="737e9-131">Go to the threat and vulnerability management navigation menu and select **Security recommendations**.</span><span class="sxs-lookup"><span data-stu-id="737e9-131">Go to the threat and vulnerability management navigation menu and select **Security recommendations**.</span></span> <span data-ttu-id="737e9-132">La page contient une liste de recommandations de sécurité pour les menaces et les vulnérabilités trouvées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="737e9-132">The page contains a list of security recommendations for the threats and vulnerabilities found in your organization.</span></span>

### <a name="top-security-recommendations-in-the-threat-and-vulnerability-management-dashboard"></a><span data-ttu-id="737e9-133">Principales recommandations en matière de sécurité dans le tableau de bord de gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="737e9-133">Top security recommendations in the threat and vulnerability management dashboard</span></span>

<span data-ttu-id="737e9-134">Dans un jour donné en tant qu’administrateur [](tvm-dashboard-insights.md) de la sécurité, vous pouvez consulter le tableau de bord de gestion des menaces et des vulnérabilités pour voir votre [score](tvm-exposure-score.md) d’exposition côte à côte avec votre degré de sécurisation Microsoft pour les [appareils.](tvm-microsoft-secure-score-devices.md)</span><span class="sxs-lookup"><span data-stu-id="737e9-134">In a given day as a Security Administrator, you can take a look at the [threat and vulnerability management dashboard](tvm-dashboard-insights.md) to see your [exposure score](tvm-exposure-score.md) side by side with your [Microsoft Secure Score for Devices](tvm-microsoft-secure-score-devices.md).</span></span> <span data-ttu-id="737e9-135">L’objectif est **de** réduire l’exposition  de votre organisation contre les vulnérabilités et d’augmenter la sécurité des appareils de votre organisation afin d’être plus résiliente contre les attaques contre les menaces de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="737e9-135">The goal is to **lower** your organization's exposure from vulnerabilities, and **increase** your organization's device security to be more resilient against cybersecurity threat attacks.</span></span> <span data-ttu-id="737e9-136">La liste des recommandations de sécurité les plus importantes peut vous aider à atteindre cet objectif.</span><span class="sxs-lookup"><span data-stu-id="737e9-136">The top security recommendations list can help you achieve that goal.</span></span>

![Exemple de carte recommandations de sécurité principales, avec quatre recommandations de sécurité.](images/top-security-recommendations350.png)

<span data-ttu-id="737e9-138">Les principales recommandations en matière de sécurité présentent les opportunités d’amélioration prioritaires en fonction des facteurs importants mentionnés dans la section précédente : menace, probabilité de violation et valeur.</span><span class="sxs-lookup"><span data-stu-id="737e9-138">The top security recommendations list the improvement opportunities prioritized based on the important factors mentioned in the previous section - threat, likelihood to be breached, and value.</span></span> <span data-ttu-id="737e9-139">La sélection d’une recommandation vous permet d’accès à la page recommandations de sécurité avec plus de détails.</span><span class="sxs-lookup"><span data-stu-id="737e9-139">Selecting a recommendation will take you to the security recommendations page with more details.</span></span>

## <a name="security-recommendations-overview"></a><span data-ttu-id="737e9-140">Vue d’ensemble des recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="737e9-140">Security recommendations overview</span></span>

<span data-ttu-id="737e9-141">Afficher les recommandations, le nombre de faiblesses trouvées, les composants associés, les informations sur les menaces, le nombre d’appareils exposés, l’état, le type de correction, les activités de correction, l’impact sur votre score d’exposition et le score de sécurité Microsoft pour les appareils, ainsi que les balises associées.</span><span class="sxs-lookup"><span data-stu-id="737e9-141">View recommendations, the number of weaknesses found, related components, threat insights, number of exposed devices, status, remediation type, remediation activities, impact to your exposure score and Microsoft Secure Score for Devices, and associated tags.</span></span>

<span data-ttu-id="737e9-142">La couleur du graphique **des appareils exposés** change à mesure que la tendance change.</span><span class="sxs-lookup"><span data-stu-id="737e9-142">The color of the **Exposed devices** graph changes as the trend changes.</span></span> <span data-ttu-id="737e9-143">Si le nombre d’appareils exposés augmente, la couleur passe en rouge.</span><span class="sxs-lookup"><span data-stu-id="737e9-143">If the number of exposed devices is on the rise, the color changes into red.</span></span> <span data-ttu-id="737e9-144">En cas de diminution du nombre d’appareils exposés, la couleur du graphique change en vert.</span><span class="sxs-lookup"><span data-stu-id="737e9-144">If there's a decrease in the number of exposed devices, the color of the graph will change into green.</span></span>

>[!NOTE]
><span data-ttu-id="737e9-145">La gestion des menaces et des vulnérabilités affiche les appareils qui étaient utilisés il y a **30** jours.</span><span class="sxs-lookup"><span data-stu-id="737e9-145">Threat and vulnerability management shows devices that were in use up to **30 days** ago.</span></span> <span data-ttu-id="737e9-146">Ceci est différent du reste de Microsoft Defender pour point de terminaison, où si un appareil n’a pas été utilisé pendant plus de 7 jours, il présente l’état « Inactif ».</span><span class="sxs-lookup"><span data-stu-id="737e9-146">This is different from the rest of Microsoft Defender for Endpoint, where if a device has not been in use for more than 7 days it has in an ‘Inactive’ status.</span></span>

![Exemple de page d’accueil pour les recommandations de sécurité.](images/tvmsecrec-updated.png)

### <a name="icons"></a><span data-ttu-id="737e9-148">Icônes</span><span class="sxs-lookup"><span data-stu-id="737e9-148">Icons</span></span>

<span data-ttu-id="737e9-149">Les icônes utiles peuvent également attirer rapidement votre attention sur :</span><span class="sxs-lookup"><span data-stu-id="737e9-149">Useful icons also quickly call your attention to:</span></span>
- ![flèche tapant une cible](images/tvm_alert_icon.png) <span data-ttu-id="737e9-151">alertes actives possibles</span><span class="sxs-lookup"><span data-stu-id="737e9-151">possible active alerts</span></span>
- ![bogue rouge](images/tvm_bug_icon.png) <span data-ttu-id="737e9-153">exploits publics associés</span><span class="sxs-lookup"><span data-stu-id="737e9-153">associated public exploits</span></span>
- ![light light light](images/tvm_insight_icon.png) <span data-ttu-id="737e9-155">informations sur les recommandations</span><span class="sxs-lookup"><span data-stu-id="737e9-155">recommendation insights</span></span>

### <a name="explore-security-recommendation-options"></a><span data-ttu-id="737e9-156">Explorer les options de recommandation de sécurité</span><span class="sxs-lookup"><span data-stu-id="737e9-156">Explore security recommendation options</span></span>

<span data-ttu-id="737e9-157">Sélectionnez la recommandation de sécurité que vous souhaitez examiner ou traiter.</span><span class="sxs-lookup"><span data-stu-id="737e9-157">Select the security recommendation that you want to investigate or process.</span></span>

![Exemple de page de recommandation de sécurité.](images/secrec-flyouteolsw.png)

<span data-ttu-id="737e9-159">Dans le volant, vous pouvez choisir l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="737e9-159">From the flyout, you can choose any of the following options:</span></span>

- <span data-ttu-id="737e9-160">**Page Ouvrir un logiciel** : ouvrez la page du logiciel pour obtenir plus de contexte sur le logiciel et la façon dont il est distribué.</span><span class="sxs-lookup"><span data-stu-id="737e9-160">**Open software page** - Open the software page to get more context on the software and how it's distributed.</span></span> <span data-ttu-id="737e9-161">Les informations peuvent inclure le contexte des menaces, les recommandations associées, les faiblesses découvertes, le nombre d’appareils exposés, les vulnérabilités découvertes, les noms et les détails des appareils sur lequel le logiciel est installé et la distribution des versions.</span><span class="sxs-lookup"><span data-stu-id="737e9-161">The information can include threat context, associated recommendations, weaknesses discovered, number of exposed devices, discovered vulnerabilities, names and detailed of devices with the software installed, and version distribution.</span></span>

- <span data-ttu-id="737e9-162">[**Options de**](tvm-remediation.md) correction : envoyez une demande de correction pour ouvrir un ticket dans Microsoft Intune pour que votre administrateur informatique le sélectionne et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="737e9-162">[**Remediation options**](tvm-remediation.md) - Submit a remediation request to open a ticket in Microsoft Intune for your IT administrator to pick up and address.</span></span> <span data-ttu-id="737e9-163">Suivre l’activité de correction dans la page Correction.</span><span class="sxs-lookup"><span data-stu-id="737e9-163">Track the remediation activity in the Remediation page.</span></span>

- <span data-ttu-id="737e9-164">[**Options d’exception**](tvm-exception.md) : soumettre une exception, fournir une justification et définir la durée de l’exception si vous ne pouvez pas encore résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="737e9-164">[**Exception options**](tvm-exception.md) - Submit an exception, provide justification, and set exception duration if you can't remediate the issue yet.</span></span>

>[!NOTE]
><span data-ttu-id="737e9-165">Lorsqu’une modification logicielle est réalisée sur un appareil, il faut généralement 2 heures pour que les données soient reflétées dans le portail de sécurité.</span><span class="sxs-lookup"><span data-stu-id="737e9-165">When a software change is made on a device, it typically takes 2 hours for the data to be reflected in the security portal.</span></span> <span data-ttu-id="737e9-166">Toutefois, cela peut parfois prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="737e9-166">However, it may sometimes take longer.</span></span> <span data-ttu-id="737e9-167">Les modifications de configuration peuvent prendre entre 4 et 24 heures.</span><span class="sxs-lookup"><span data-stu-id="737e9-167">Configuration changes can take anywhere from 4 to 24 hours.</span></span>

### <a name="investigate-changes-in-device-exposure-or-impact"></a><span data-ttu-id="737e9-168">Examiner les modifications apportées à l’exposition ou à l’impact de l’appareil</span><span class="sxs-lookup"><span data-stu-id="737e9-168">Investigate changes in device exposure or impact</span></span>

<span data-ttu-id="737e9-169">S’il y a une augmentation importante du nombre d’appareils exposés ou une forte augmentation de l’impact sur le score d’exposition de votre organisation et le score de sécurité Microsoft pour les appareils, cette recommandation de sécurité vaut la peine d’être étudier.</span><span class="sxs-lookup"><span data-stu-id="737e9-169">If there is a large jump in the number of exposed devices, or a sharp increase in the impact on your organization exposure score and Microsoft Secure Score for Devices, then that security recommendation is worth investigating.</span></span>

1. <span data-ttu-id="737e9-170">Sélectionnez la page Recommandation **et Ouvrir le logiciel**</span><span class="sxs-lookup"><span data-stu-id="737e9-170">Select the recommendation and **Open software page**</span></span>
2. <span data-ttu-id="737e9-171">Sélectionnez **l’onglet Chronologie** des événements pour afficher tous les événements qui ont un impact sur ce logiciel, tels que les nouvelles vulnérabilités ou les nouvelles exploitations publiques.</span><span class="sxs-lookup"><span data-stu-id="737e9-171">Select the **Event timeline** tab to view all the impactful events related to that software, such as new vulnerabilities or new public exploits.</span></span> [<span data-ttu-id="737e9-172">En savoir plus sur la chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="737e9-172">Learn more about event timeline</span></span>](threat-and-vuln-mgt-event-timeline.md)
3. <span data-ttu-id="737e9-173">Décider comment faire face à l’augmentation ou à l’exposition de votre organisation, par exemple envoyer une demande de correction</span><span class="sxs-lookup"><span data-stu-id="737e9-173">Decide how to address the increase or your organization's exposure, such as submitting a remediation request</span></span>

## <a name="request-remediation"></a><span data-ttu-id="737e9-174">Demander la correction</span><span class="sxs-lookup"><span data-stu-id="737e9-174">Request remediation</span></span>

<span data-ttu-id="737e9-175">La fonctionnalité de correction de la gestion des menaces et des vulnérabilités relie les administrateurs informatiques et de sécurité par le biais du flux de travail de demande de correction.</span><span class="sxs-lookup"><span data-stu-id="737e9-175">The threat and vulnerability management remediation capability bridges the gap between Security and IT administrators through the remediation request workflow.</span></span> <span data-ttu-id="737e9-176">Les administrateurs de sécurité comme vous pouvez demander à l’administrateur informatique de corriger une vulnérabilité à partir de la **page** recommandations de sécurité vers Intune.</span><span class="sxs-lookup"><span data-stu-id="737e9-176">Security admins like you can request for the IT Administrator to remediate a vulnerability from the **Security recommendation** page to Intune.</span></span> [<span data-ttu-id="737e9-177">En savoir plus sur les options de correction</span><span class="sxs-lookup"><span data-stu-id="737e9-177">Learn more about remediation options</span></span>](tvm-remediation.md)

### <a name="how-to-request-remediation"></a><span data-ttu-id="737e9-178">Comment demander des corrections</span><span class="sxs-lookup"><span data-stu-id="737e9-178">How to request remediation</span></span>

<span data-ttu-id="737e9-179">Sélectionnez une recommandation de sécurité pour qui vous souhaitez demander des corrections, puis sélectionnez **Options de correction.**</span><span class="sxs-lookup"><span data-stu-id="737e9-179">Select a security recommendation you would like to request remediation for, and then select **Remediation options**.</span></span> <span data-ttu-id="737e9-180">Remplissez le formulaire et sélectionnez **Envoyer la demande.**</span><span class="sxs-lookup"><span data-stu-id="737e9-180">Fill out the form and select **Submit request**.</span></span> <span data-ttu-id="737e9-181">Go to the [**Remediation**](tvm-remediation.md) page to view the status of your remediation request.</span><span class="sxs-lookup"><span data-stu-id="737e9-181">Go to the [**Remediation**](tvm-remediation.md) page to view the status of your remediation request.</span></span> [<span data-ttu-id="737e9-182">En savoir plus sur la demande de correction</span><span class="sxs-lookup"><span data-stu-id="737e9-182">Learn more about how to request remediation</span></span>](tvm-remediation.md#request-remediation)

## <a name="file-for-exception"></a><span data-ttu-id="737e9-183">Fichier d’exception</span><span class="sxs-lookup"><span data-stu-id="737e9-183">File for exception</span></span>

<span data-ttu-id="737e9-184">En remplacement d’une demande de correction lorsqu’une recommandation n’est pas pertinente pour le moment, vous pouvez créer des exceptions pour les recommandations.</span><span class="sxs-lookup"><span data-stu-id="737e9-184">As an alternative to a remediation request when a recommendation is not relevant at the moment, you can create exceptions for recommendations.</span></span> [<span data-ttu-id="737e9-185">En savoir plus sur les exceptions</span><span class="sxs-lookup"><span data-stu-id="737e9-185">Learn more about exceptions</span></span>](tvm-exception.md)

<span data-ttu-id="737e9-186">Seuls les utilisateurs ayant des autorisations de « gestion des exceptions » peuvent ajouter des exceptions.</span><span class="sxs-lookup"><span data-stu-id="737e9-186">Only users with “exceptions handling” permissions can add exception.</span></span> <span data-ttu-id="737e9-187">[En savoir plus sur les rôles RBAC.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="737e9-187">[Learn more about RBAC roles](user-roles.md).</span></span>

<span data-ttu-id="737e9-188">Lorsqu’une exception est créée pour une recommandation, elle n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="737e9-188">When an exception is created for a recommendation, the recommendation is no longer active.</span></span> <span data-ttu-id="737e9-189">L’état de recommandation change en **Exception complète ou** Exception **partielle** (par groupe d’appareils).</span><span class="sxs-lookup"><span data-stu-id="737e9-189">The recommendation state will change to **Full exception** or **Partial exception** (by device group).</span></span>

### <a name="how-to-create-an-exception"></a><span data-ttu-id="737e9-190">Comment créer une exception</span><span class="sxs-lookup"><span data-stu-id="737e9-190">How to create an exception</span></span>

<span data-ttu-id="737e9-191">Sélectionnez une recommandation de sécurité pour la création d’une exception, puis sélectionnez **Options d’exception.**</span><span class="sxs-lookup"><span data-stu-id="737e9-191">Select a security recommendation you would like create an exception for, and then select **Exception options**.</span></span>  

![Affichage de l’emplacement du bouton « options d’exception » dans un volant de recommandations de sécurité.](images/tvm-exception-options.png)

<span data-ttu-id="737e9-193">Remplissez le formulaire et soumettez-le.</span><span class="sxs-lookup"><span data-stu-id="737e9-193">Fill out the form and submit.</span></span> <span data-ttu-id="737e9-194">Pour afficher toutes vos exceptions (actuelles et passées), accédez à la [page](tvm-remediation.md) Correction sous le menu Gestion des vulnérabilités des menaces **&** et sélectionnez l’onglet **Exceptions.** En savoir plus sur la création d’une [exception](tvm-exception.md#create-an-exception)</span><span class="sxs-lookup"><span data-stu-id="737e9-194">To view all your exceptions (current and past), navigate to the [Remediation](tvm-remediation.md) page under the **Threat & Vulnerability Management** menu and select the **Exceptions** tab. [Learn more about how to create an exception](tvm-exception.md#create-an-exception)</span></span>

## <a name="report-inaccuracy"></a><span data-ttu-id="737e9-195">Report inaccuracy</span><span class="sxs-lookup"><span data-stu-id="737e9-195">Report inaccuracy</span></span>

<span data-ttu-id="737e9-196">Vous pouvez signaler un faux positif lorsque vous voyez des informations de recommandation de sécurité vagues, inexactes, incomplètes ou déjà corrigés.</span><span class="sxs-lookup"><span data-stu-id="737e9-196">You can report a false positive when you see any vague, inaccurate, incomplete, or already remediated security recommendation information.</span></span>

1. <span data-ttu-id="737e9-197">Ouvrez la recommandation sécurité.</span><span class="sxs-lookup"><span data-stu-id="737e9-197">Open the Security recommendation.</span></span>

2. <span data-ttu-id="737e9-198">Sélectionnez les trois points en dehors de la recommandation de sécurité que vous souhaitez signaler, puis sélectionnez **L’imprécision du rapport.**</span><span class="sxs-lookup"><span data-stu-id="737e9-198">Select the three dots beside the security recommendation that you want to report,  then select **Report inaccuracy**.</span></span>

    ![Affichage de l’endroit où le bouton « Signaler l’imprécision » se trouve dans un volant de recommandations de sécurité.](images/report-inaccuracy500.png)

3. <span data-ttu-id="737e9-200">Dans le volet de menu volant, sélectionnez la catégorie d’imprécision dans le menu déroulant, remplissez votre adresse e-mail et les détails concernant l’imprécision.</span><span class="sxs-lookup"><span data-stu-id="737e9-200">From the flyout pane, select the inaccuracy category from the drop-down menu, fill in your email address, and details regarding the inaccuracy.</span></span>

4. <span data-ttu-id="737e9-201">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="737e9-201">Select **Submit**.</span></span> <span data-ttu-id="737e9-202">Vos commentaires sont immédiatement envoyés aux experts en gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="737e9-202">Your feedback is immediately sent to the threat and vulnerability management experts.</span></span>

## <a name="related-articles"></a><span data-ttu-id="737e9-203">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="737e9-203">Related articles</span></span>

- [<span data-ttu-id="737e9-204">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="737e9-204">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="737e9-205">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="737e9-205">Dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="737e9-206">Score d'exposition</span><span class="sxs-lookup"><span data-stu-id="737e9-206">Exposure score</span></span>](tvm-exposure-score.md)
- [<span data-ttu-id="737e9-207">Niveau de sécurité Microsoft pour les appareils</span><span class="sxs-lookup"><span data-stu-id="737e9-207">Microsoft Secure Score for Devices</span></span>](tvm-microsoft-secure-score-devices.md)
- [<span data-ttu-id="737e9-208">Corriger des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="737e9-208">Remediate vulnerabilities</span></span>](tvm-remediation.md)
- [<span data-ttu-id="737e9-209">Créer et afficher des exceptions pour les recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="737e9-209">Create and view exceptions for security recommendations</span></span>](tvm-exception.md)
- [<span data-ttu-id="737e9-210">Chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="737e9-210">Event timeline</span></span>](threat-and-vuln-mgt-event-timeline.md)
