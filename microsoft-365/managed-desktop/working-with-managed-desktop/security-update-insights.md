---
title: Perspectives sur la mise à jour de sécurité Windows
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: b3b1f43217b3be285f20925065bf9710a38f9606
ms.sourcegitcommit: 36795a6735cd3fc678c7d5db71ddc97fac3f6f8a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2020
ms.locfileid: "48941440"
---
# <a name="windows-security-update-insights"></a><span data-ttu-id="f2b65-103">Perspectives sur la mise à jour de sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="f2b65-103">Windows security update insights</span></span>
<span data-ttu-id="f2b65-104">Cet affichage fournit une vue d’ensemble de l’état des mises à jour de sécurité pour vos appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2b65-104">This view provides an overview of the status of security updates for your Microsoft Managed Desktop devices.</span></span> 

<span data-ttu-id="f2b65-105">Pour afficher les données d’utilisation, sélectionnez l’onglet <strong>mises à jour de sécurité Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="f2b65-105">To view usage data, select the <strong>Windows security updates</strong> tab.</span></span>

![Volet mises à jour de sécurité Windows : graphiques à barres de l’état du périphérique et de la version de mise à jour dans la colonne de gauche, mise à jour de l’avancement du déploiement dans le temps dans le centre et pourcentage d’appareils actifs par groupe de déploiement, ainsi que le nombre de jours pris pour atteindre la cible de déploiement de 95% dans la colonne de droite.](../../media/update-insights.jpg)

## <a name="device-status"></a><span data-ttu-id="f2b65-107">État de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f2b65-107">Device status</span></span>

<span data-ttu-id="f2b65-108">Pour que les appareils soient mis à jour par Windows Update, ils doivent être connectés à Internet et ne pas être mis en veille prolongée pendant une durée minimale de six heures, dont deux doivent être continus.</span><span class="sxs-lookup"><span data-stu-id="f2b65-108">For devices to be updated by Windows Update, they must be connected to the Internet and not hibernating for a minimum of six hours, two of which must be continuous.</span></span> <span data-ttu-id="f2b65-109">Bien qu’il soit possible qu’un appareil qui ne répond pas à ces exigences soit mis à jour, les appareils qui les satisfont ont la plus grande probabilité d’être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f2b65-109">Although it's possible that a device that doesn't meet these requirements will be updated, devices that meet them have the highest likelihood of being updated.</span></span> 

<span data-ttu-id="f2b65-110">Nous catégoriserons l’activité de l’appareil dans le contexte de Windows Update selon les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="f2b65-110">We categorize device activity in the context of Windows Update with these terms:</span></span>

- <span data-ttu-id="f2b65-111"><strong>Actif :</strong> Appareils ayant satisfait aux critères d’activité minimum (six heures, deux en continu) pour la dernière version de la mise à jour de sécurité et qui ont archivé avec Microsoft Intune au moins tous les cinq jours</span><span class="sxs-lookup"><span data-stu-id="f2b65-111"><strong>Active:</strong> Devices that have met the minimum activity criteria (six hours, two continuous) for the most recent security update release and have checked in with Microsoft Intune at least every five days</span></span>
- <span data-ttu-id="f2b65-112"><strong>Synchronisés :</strong> Appareils ayant archivé avec Intune au cours des 28 derniers jours</span><span class="sxs-lookup"><span data-stu-id="f2b65-112"><strong>Synced:</strong> Devices that have checked in with Intune within the last 28 days</span></span>
- <span data-ttu-id="f2b65-113"><strong>Désynchronisation :</strong> Appareils qui <i>n’ont pas</i> archivé avec Intune au cours des 28 derniers jours</span><span class="sxs-lookup"><span data-stu-id="f2b65-113"><strong>Out of sync:</strong> Devices that have <i>not</i> checked in with Intune in the last 28 days</span></span>




## <a name="update-version-status"></a><span data-ttu-id="f2b65-114">Mettre à jour l’état de version</span><span class="sxs-lookup"><span data-stu-id="f2b65-114">Update version status</span></span>

<span data-ttu-id="f2b65-115">Microsoft publie les mises à jour de sécurité chaque deuxième mardi du mois.</span><span class="sxs-lookup"><span data-stu-id="f2b65-115">Microsoft releases security updates every second Tuesday of the month.</span></span> <span data-ttu-id="f2b65-116">Chaque version ajoute des mises à jour importantes pour les failles de sécurité connues.</span><span class="sxs-lookup"><span data-stu-id="f2b65-116">Each release adds important updates for known security vulnerabilities.</span></span> <span data-ttu-id="f2b65-117">Microsoft Managed Desktop garantit que 95% de ses appareils gérés sont mis à jour avec la dernière mise à jour de sécurité disponible tous les mois.</span><span class="sxs-lookup"><span data-stu-id="f2b65-117">Microsoft Managed Desktop ensures that 95% of its managed devices are updated with the latest available security update every month.</span></span> <span data-ttu-id="f2b65-118">Les mises à jour de sécurité sont parfois publiées à d’autres moments pour résoudre les nouvelles menaces de façon urgente.</span><span class="sxs-lookup"><span data-stu-id="f2b65-118">Security updates are sometimes released at other times to urgently address new threats.</span></span> <span data-ttu-id="f2b65-119">Microsoft Managed Desktop déploie ces mises à jour de la même manière.</span><span class="sxs-lookup"><span data-stu-id="f2b65-119">Microsoft Managed Desktop deploys these updates in a similar fashion.</span></span>

<span data-ttu-id="f2b65-120">Nous catégoriserons l’état des versions de mise à jour de sécurité avec les termes suivants :</span><span class="sxs-lookup"><span data-stu-id="f2b65-120">We categorize the status of security update versions with these terms:</span></span>

- <span data-ttu-id="f2b65-121"><strong>Actuel :</strong> Appareils qui exécutent la mise à jour publiée dans le mois en cours</span><span class="sxs-lookup"><span data-stu-id="f2b65-121"><strong>Current:</strong> Devices that are running the update released in the current month</span></span>
- <span data-ttu-id="f2b65-122"><strong>Précédent :</strong> Appareils exécutant la mise à jour publiée au cours du mois précédent</span><span class="sxs-lookup"><span data-stu-id="f2b65-122"><strong>Previous:</strong> Devices running the update that was released in the previous month</span></span>
- <span data-ttu-id="f2b65-123"><strong>Plus ancien :</strong> Périphériques exécutant une mise à jour de sécurité publiée avant le mois précédent</span><span class="sxs-lookup"><span data-stu-id="f2b65-123"><strong>Older:</strong> Devices running any security update released prior to the previous month</span></span>

<span data-ttu-id="f2b65-124">Vous devriez voir peu de périphériques dans l' <strong>ancienne</strong> catégorie--un grand nombre ou une population croissante indique probablement un problème système que vous devez signaler à Microsoft Managed Desktop afin que nous puissions examiner.</span><span class="sxs-lookup"><span data-stu-id="f2b65-124">You should see few devices in the <strong>Older</strong> category--a large or growing population probably indicates a systemic problem that you should report to Microsoft Managed Desktop so we can investigate.</span></span>


## <a name="deployment-progress"></a><span data-ttu-id="f2b65-125">Progression du déploiement</span><span class="sxs-lookup"><span data-stu-id="f2b65-125">Deployment progress</span></span>

<span data-ttu-id="f2b65-126">Au début de chaque cycle de publication des mises à jour de sécurité, le bureau géré Microsoft prend un instantané de la population du périphérique et définit sa cible de déploiement à 95% de ce remplissage.</span><span class="sxs-lookup"><span data-stu-id="f2b65-126">At the beginning of each security update release cycle, Microsoft Managed Desktop takes a snapshot of the device population and sets its deployment target at 95% of that population.</span></span> <span data-ttu-id="f2b65-127">La zone de <strong>progression du déploiement</strong> affiche une tendance historique, mise à jour quotidiennement, qui effectue le suivi de la différence entre le déploiement de la mise à jour et la cible de cette cible pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="f2b65-127">The <strong>Deployment progress</strong> area shows a historical trend, updated daily, tracking how closely the update deployment meets this target for each release.</span></span> <span data-ttu-id="f2b65-128">Ce graphique affiche uniquement les appareils dont le statut est actif.</span><span class="sxs-lookup"><span data-stu-id="f2b65-128">This graph only shows devices with Active status.</span></span>

<span data-ttu-id="f2b65-129">Vous pouvez afficher ces données pour les cycles de mise à jour précédents à l’aide du menu déroulant dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="f2b65-129">You can view this data for previous update cycles by using the dropdown menu in the upper right.</span></span> <span data-ttu-id="f2b65-130">La période que vous sélectionnez dans ce menu s’applique à toutes les informations sur la page entière.</span><span class="sxs-lookup"><span data-stu-id="f2b65-130">The period you select in this menu applies to all of the information on the whole page.</span></span>

<span data-ttu-id="f2b65-131">La zone de <strong>groupe périphériques actifs mis à jour par le groupe de déploiement</strong> offre une vue différente en indiquant la progression de l’installation de la mise à jour pour chacun des groupes de déploiement de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2b65-131">The <strong>Updated active devices by deployment group</strong> area offers a different view by showing the progress of the update installation for each of the Microsoft Managed Desktop deployment groups.</span></span>

<span data-ttu-id="f2b65-132">La zone des <strong>jours pour atteindre la cible</strong> affiche le temps nécessaire pour 95% du nombre total d’appareils à mettre à jour avec la mise à jour de sécurité actuelle.</span><span class="sxs-lookup"><span data-stu-id="f2b65-132">The <strong>Days to reach target</strong> area displays how long it took for 95% of the total number of devices to be updated with the current security update.</span></span> <span data-ttu-id="f2b65-133">Lorsque le déploiement est en cours, cette zone affiche <strong>toujours la mise à jour</strong> jusqu’à ce que la cible 95% soit atteinte pour la mise à jour sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f2b65-133">While deployment is underway, this area displays <strong>Still updating</strong> until the 95% target is reached for the selected update.</span></span>

## <a name="device-details-area"></a><span data-ttu-id="f2b65-134">Zone Détails sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="f2b65-134">Device details area</span></span>

<span data-ttu-id="f2b65-135">Le bas du tableau de bord contient des informations détaillées sur vos appareils, dont l’état de l' [appareil](#device-status) et l’état de la [version de mise à jour](#update-version-status).</span><span class="sxs-lookup"><span data-stu-id="f2b65-135">The bottom of the dashboard is a table showing detailed information for your devices, including the [Device status](#device-status) and the [Update version status](#update-version-status).</span></span> <span data-ttu-id="f2b65-136">Vous pouvez effectuer une recherche dans cette liste ou la filtrer par n’importe quelle valeur répertoriée.</span><span class="sxs-lookup"><span data-stu-id="f2b65-136">You can search this list or filter it by any listed value.</span></span>


![Tableau détails de l’appareil avec des colonnes pour le nom de l’appareil, l’état de l’appareil affecté, l’état de la mise à jour, la version du système d’exploitation et la date de la dernière synchronisation de l’appareil.](../../media/security-update-insights-device-table-sterile.png)
