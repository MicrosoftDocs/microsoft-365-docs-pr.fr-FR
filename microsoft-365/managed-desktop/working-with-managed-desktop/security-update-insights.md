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
ms.sourcegitcommit: cebbdd393dcfd93ff43a1ab66ad70115853f83e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52739796"
---
# <a name="windows-security-update-insights"></a><span data-ttu-id="aa2dc-103">Perspectives sur la mise à jour de sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="aa2dc-103">Windows security update insights</span></span>
<span data-ttu-id="aa2dc-104">Cette vue fournit une vue d’ensemble de l’état des mises à jour de sécurité pour Bureau géré Microsoft appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-104">This view provides an overview of the status of security updates for your Microsoft Managed Desktop devices.</span></span> 

<span data-ttu-id="aa2dc-105">Pour afficher les données d’utilisation, sélectionnez <strong>l Windows onglet Mises à jour de sécurité.</strong></span><span class="sxs-lookup"><span data-stu-id="aa2dc-105">To view usage data, select the <strong>Windows security updates</strong> tab.</span></span>

![Volet des mises à jour de sécurité Windows : graphiques à barres de l’état de l’appareil et de la version de mise à jour dans la colonne de gauche, mise à jour de l’avancement du déploiement dans la colonne centrale et pourcentage d’appareils actifs par groupe de déploiement, ainsi que le nombre de jours pris pour atteindre la cible de déploiement de 95 % dans la colonne de droite.](../../media/update-insights.jpg)

## <a name="device-status"></a><span data-ttu-id="aa2dc-107">État de l’appareil</span><span class="sxs-lookup"><span data-stu-id="aa2dc-107">Device status</span></span>

<span data-ttu-id="aa2dc-108">Pour que les appareils soient mis à jour par Windows Update, ils doivent être connectés à Internet et ne pas mettre en veille prolongée pendant au moins six heures, dont deux doivent être en continu.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-108">For devices to be updated by Windows Update, they must be connected to the Internet and not hibernating for a minimum of six hours, two of which must be continuous.</span></span> <span data-ttu-id="aa2dc-109">Bien qu’il soit possible qu’un appareil qui ne réponde pas à ces exigences soit mis à jour, les appareils qui les répondent ont la plus grande probabilité d’être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-109">Although it's possible that a device that doesn't meet these requirements will be updated, devices that meet them have the highest likelihood of being updated.</span></span> 

<span data-ttu-id="aa2dc-110">Nous classons l’activité de l’appareil dans le contexte Windows mise à jour avec les termes ci-après :</span><span class="sxs-lookup"><span data-stu-id="aa2dc-110">We categorize device activity in the context of Windows Update with these terms:</span></span>

- <span data-ttu-id="aa2dc-111"><strong>Actif :</strong> Appareils qui ont satisfait aux critères d’activité minimale (six heures, deux en continu) pour la dernière version de mise à jour de sécurité et qui ont été enregistrés avec Microsoft Intune au moins tous les cinq jours</span><span class="sxs-lookup"><span data-stu-id="aa2dc-111"><strong>Active:</strong> Devices that have met the minimum activity criteria (six hours, two continuous) for the most recent security update release and have checked in with Microsoft Intune at least every five days</span></span>
- <span data-ttu-id="aa2dc-112"><strong>Synchronisé :</strong> Appareils qui ont été enregistrés avec Intune au cours des 28 derniers jours</span><span class="sxs-lookup"><span data-stu-id="aa2dc-112"><strong>Synced:</strong> Devices that have checked in with Intune within the last 28 days</span></span>
- <span data-ttu-id="aa2dc-113"><strong>Synchronisation non synchronisée :</strong> Appareils qui <i>n’ont</i> pas été enregistrés avec Intune au cours des 28 derniers jours</span><span class="sxs-lookup"><span data-stu-id="aa2dc-113"><strong>Out of sync:</strong> Devices that have <i>not</i> checked in with Intune in the last 28 days</span></span>




## <a name="update-version-status"></a><span data-ttu-id="aa2dc-114">Mettre à jour l’état de la version</span><span class="sxs-lookup"><span data-stu-id="aa2dc-114">Update version status</span></span>

<span data-ttu-id="aa2dc-115">Microsoft publie des mises à jour de sécurité tous les deux mardis du mois.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-115">Microsoft releases security updates every second Tuesday of the month.</span></span> <span data-ttu-id="aa2dc-116">Chaque version ajoute des mises à jour importantes pour les vulnérabilités de sécurité connues.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-116">Each release adds important updates for known security vulnerabilities.</span></span> <span data-ttu-id="aa2dc-117">Bureau géré Microsoft garantit que 95 % de ses appareils gérés sont mis à jour avec la dernière mise à jour de sécurité disponible tous les mois.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-117">Microsoft Managed Desktop ensures that 95% of its managed devices are updated with the latest available security update every month.</span></span> <span data-ttu-id="aa2dc-118">Les mises à jour de sécurité sont parfois publiées à d’autres moments pour répondre de manière urgente aux nouvelles menaces.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-118">Security updates are sometimes released at other times to urgently address new threats.</span></span> <span data-ttu-id="aa2dc-119">Bureau géré Microsoft déploie ces mises à jour de la même manière.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-119">Microsoft Managed Desktop deploys these updates in a similar fashion.</span></span>

<span data-ttu-id="aa2dc-120">Nous classons l’état des versions de mise à jour de sécurité avec les termes ci-après :</span><span class="sxs-lookup"><span data-stu-id="aa2dc-120">We categorize the status of security update versions with these terms:</span></span>

- <span data-ttu-id="aa2dc-121"><strong>Actuel :</strong> Appareils exécutant la mise à jour publiée au cours du mois en cours</span><span class="sxs-lookup"><span data-stu-id="aa2dc-121"><strong>Current:</strong> Devices that are running the update released in the current month</span></span>
- <span data-ttu-id="aa2dc-122"><strong>Précédent :</strong> Appareils exécutant la mise à jour publiée le mois précédent</span><span class="sxs-lookup"><span data-stu-id="aa2dc-122"><strong>Previous:</strong> Devices running the update that was released in the previous month</span></span>
- <span data-ttu-id="aa2dc-123"><strong>Plus ancien :</strong> Appareils exécutant une mise à jour de sécurité publiée avant le mois précédent</span><span class="sxs-lookup"><span data-stu-id="aa2dc-123"><strong>Older:</strong> Devices running any security update released prior to the previous month</span></span>

<span data-ttu-id="aa2dc-124">Vous devriez voir peu <strong></strong> d’appareils dans la catégorie Plus ancienne , une population importante ou croissante indique probablement un problème d’ampleur que vous devez signaler à Bureau géré Microsoft afin que nous pouvons l’examiner.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-124">You should see few devices in the <strong>Older</strong> category--a large or growing population probably indicates a systemic problem that you should report to Microsoft Managed Desktop so we can investigate.</span></span>


## <a name="deployment-progress"></a><span data-ttu-id="aa2dc-125">Progression du déploiement</span><span class="sxs-lookup"><span data-stu-id="aa2dc-125">Deployment progress</span></span>

<span data-ttu-id="aa2dc-126">Au début de chaque cycle de publication des mises à jour de sécurité, Bureau géré Microsoft prend un instantané de la population d’appareils et définit sa cible de déploiement à 95 % de cette population.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-126">At the beginning of each security update release cycle, Microsoft Managed Desktop takes a snapshot of the device population and sets its deployment target at 95% of that population.</span></span> <span data-ttu-id="aa2dc-127">La <strong>zone d’avancement</strong> du déploiement présente une tendance historique, mise à jour quotidiennement, qui suit la proximité du déploiement de mise à jour avec cette cible pour chaque version.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-127">The <strong>Deployment progress</strong> area shows a historical trend, updated daily, tracking how closely the update deployment meets this target for each release.</span></span> <span data-ttu-id="aa2dc-128">Ce graphique affiche uniquement les appareils dont l’état est actif.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-128">This graph only shows devices with Active status.</span></span>

<span data-ttu-id="aa2dc-129">Vous pouvez afficher ces données pour les cycles de mise à jour précédents à l’aide du menu déroulant dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-129">You can view this data for previous update cycles by using the dropdown menu in the upper right.</span></span> <span data-ttu-id="aa2dc-130">La période que vous sélectionnez dans ce menu s’applique à toutes les informations de la page entière.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-130">The period you select in this menu applies to all of the information on the whole page.</span></span>

<span data-ttu-id="aa2dc-131">Les <strong>appareils actifs mis</strong> à jour par zone de groupe de déploiement offrent une vue différente en affichant la progression de l’installation de la mise à jour pour chacun des groupes Bureau géré Microsoft déploiement.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-131">The <strong>Updated active devices by deployment group</strong> area offers a different view by showing the progress of the update installation for each of the Microsoft Managed Desktop deployment groups.</span></span>

<span data-ttu-id="aa2dc-132">Le <strong>nombre de jours pour atteindre</strong> la zone cible affiche le temps qu’il a fallu pour que 95 % du nombre total d’appareils soient mis à jour avec la mise à jour de sécurité actuelle.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-132">The <strong>Days to reach target</strong> area displays how long it took for 95% of the total number of devices to be updated with the current security update.</span></span> <span data-ttu-id="aa2dc-133">Pendant le déploiement, cette zone <strong></strong> affiche Toujours la mise à jour jusqu’à ce que la cible de 95 % soit atteinte pour la mise à jour sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-133">While deployment is underway, this area displays <strong>Still updating</strong> until the 95% target is reached for the selected update.</span></span>

## <a name="device-details-area"></a><span data-ttu-id="aa2dc-134">Zone de détails de l’appareil</span><span class="sxs-lookup"><span data-stu-id="aa2dc-134">Device details area</span></span>

<span data-ttu-id="aa2dc-135">Le bas du tableau de bord est un tableau [](#device-status) affichant des informations détaillées sur vos appareils, notamment l’état de l’appareil et l’état de la version de mise [à jour.](#update-version-status)</span><span class="sxs-lookup"><span data-stu-id="aa2dc-135">The bottom of the dashboard is a table showing detailed information for your devices, including the [Device status](#device-status) and the [Update version status](#update-version-status).</span></span> <span data-ttu-id="aa2dc-136">Vous pouvez effectuer une recherche dans cette liste ou la filtrer selon n’importe quelle valeur répertoriée.</span><span class="sxs-lookup"><span data-stu-id="aa2dc-136">You can search this list or filter it by any listed value.</span></span>


![Tableau des détails de l’appareil montrant les colonnes pour le nom de l’appareil, l’utilisateur affecté, l’état de l’appareil, la version de mise à jour, la version du système d’exploitation et la date de la dernière synchronisation de l’appareil.](../../media/security-update-insights-device-table-sterile.png)
