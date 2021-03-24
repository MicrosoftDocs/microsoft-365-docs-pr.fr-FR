---
title: Examiner les fichiers Microsoft Defender pour les points de terminaison
description: Utilisez les options d’examen pour obtenir des détails sur les fichiers associés aux alertes, comportements ou événements.
keywords: examiner, examen, fichier, activité malveillante, motivation des attaques, analyse approfondie, rapport d’analyse approfondie
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: a801b6153cf3f273290721756440cfe974103e92
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064569"
---
# <a name="investigate-a-file-associated-with-a-microsoft-defender-for-endpoint-alert"></a><span data-ttu-id="c2269-104">Examiner un fichier associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-104">Investigate a file associated with a Microsoft Defender for Endpoint alert</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c2269-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c2269-105">**Applies to:**</span></span>
- [<span data-ttu-id="c2269-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="c2269-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c2269-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


><span data-ttu-id="c2269-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="c2269-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c2269-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c2269-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatefiles-abovefoldlink)

<span data-ttu-id="c2269-110">Examinez les détails d’un fichier associé à une alerte, un comportement ou un événement spécifique pour déterminer si le fichier présente des activités malveillantes, identifier la motivation de l’attaque et comprendre l’étendue potentielle de la violation.</span><span class="sxs-lookup"><span data-stu-id="c2269-110">Investigate the details of a file associated with a specific alert, behavior, or event to help determine if the file exhibits malicious activities, identify the attack motivation, and understand the potential scope of the breach.</span></span>

<span data-ttu-id="c2269-111">Il existe plusieurs façons d’accéder à la page de profil détaillée d’un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="c2269-111">There are many ways to access the detailed profile page of a specific file.</span></span> <span data-ttu-id="c2269-112">Par exemple, vous pouvez utiliser la fonctionnalité de recherche, cliquer sur un lien à partir de l’arborescence du processus d’alerte, du graphique **d’incident,** de la chronologie de l’artefact **ou** sélectionner un événement répertorié dans la chronologie de **l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="c2269-112">For example, you can  use the search feature, click on a link from the **Alert process tree**, **Incident graph**, **Artifact timeline**, or select an event listed in the **Device timeline**.</span></span>

<span data-ttu-id="c2269-113">Une fois sur la page de profil détaillée, vous pouvez basculer entre la nouvelle et l’ancienne mise en page en basant **la nouvelle page de fichier.**</span><span class="sxs-lookup"><span data-stu-id="c2269-113">Once on the detailed profile page, you can switch between the new and old page layouts by toggling **new File page**.</span></span> <span data-ttu-id="c2269-114">Le reste de cet article décrit la mise en page la plus nouvelle.</span><span class="sxs-lookup"><span data-stu-id="c2269-114">The rest of this article describes the newer page layout.</span></span>

<span data-ttu-id="c2269-115">Vous pouvez obtenir des informations à partir des sections suivantes dans l’affichage de fichier :</span><span class="sxs-lookup"><span data-stu-id="c2269-115">You can get information from the following sections in the file view:</span></span>

- <span data-ttu-id="c2269-116">Détails du fichier, détection des programmes malveillants, prévalence du fichier</span><span class="sxs-lookup"><span data-stu-id="c2269-116">File details, Malware detection, File prevalence</span></span>
- <span data-ttu-id="c2269-117">Analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="c2269-117">Deep analysis</span></span>
- <span data-ttu-id="c2269-118">Alertes</span><span class="sxs-lookup"><span data-stu-id="c2269-118">Alerts</span></span>
- <span data-ttu-id="c2269-119">Observé dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="c2269-119">Observed in organization</span></span>
- <span data-ttu-id="c2269-120">Analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="c2269-120">Deep analysis</span></span>
- <span data-ttu-id="c2269-121">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="c2269-121">File names</span></span>

<span data-ttu-id="c2269-122">Vous pouvez également agir sur un fichier à partir de cette page.</span><span class="sxs-lookup"><span data-stu-id="c2269-122">You can also take action on a file from this page.</span></span>

## <a name="file-actions"></a><span data-ttu-id="c2269-123">Actions de fichier</span><span class="sxs-lookup"><span data-stu-id="c2269-123">File actions</span></span>

<span data-ttu-id="c2269-124">En haut de la page de profil, au-dessus des cartes d’informations de fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-124">Along the top of the profile page, above the file information cards.</span></span> <span data-ttu-id="c2269-125">Les actions que vous pouvez effectuer ici sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2269-125">Actions you can perform here include:</span></span>

- <span data-ttu-id="c2269-126">Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c2269-126">Stop and quarantine</span></span>
- <span data-ttu-id="c2269-127">Indicateur d’ajout/modification</span><span class="sxs-lookup"><span data-stu-id="c2269-127">Add/edit indicator</span></span>
- <span data-ttu-id="c2269-128">Télécharger un fichier</span><span class="sxs-lookup"><span data-stu-id="c2269-128">Download file</span></span>
- <span data-ttu-id="c2269-129">Consulter un expert en menaces</span><span class="sxs-lookup"><span data-stu-id="c2269-129">Consult a threat expert</span></span>
- <span data-ttu-id="c2269-130">Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="c2269-130">Action center</span></span>

<span data-ttu-id="c2269-131">Pour plus d’informations sur ces actions, voir [Action de réponse sur un fichier.](respond-file-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="c2269-131">For more information on these actions, see [Take response action on a file](respond-file-alerts.md).</span></span>

## <a name="file-details-malware-detection-and-file-prevalence"></a><span data-ttu-id="c2269-132">Détails du fichier, détection des programmes malveillants et prévalence du fichier</span><span class="sxs-lookup"><span data-stu-id="c2269-132">File details, Malware detection, and File prevalence</span></span>

<span data-ttu-id="c2269-133">Les détails du fichier, les incidents, la détection des programmes malveillants et les cartes de prévalence de fichier affichent différents attributs sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-133">The file details, incident, malware detection, and file prevalence cards display various attributes about the file.</span></span>

<span data-ttu-id="c2269-134">Vous verrez des détails tels que le MD5 du fichier, le taux de détection du nombre total de virus et la détection de l’antivirus Microsoft Defender, le cas besoin, ainsi que la prévalence du fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-134">You'll see details such as the file’s MD5, the Virus Total detection ratio, and Microsoft Defender AV detection if available, and the file’s prevalence.</span></span>

<span data-ttu-id="c2269-135">La carte de prévalence du fichier indique où le fichier a été vu sur les appareils de l’organisation et du monde entier.</span><span class="sxs-lookup"><span data-stu-id="c2269-135">The file prevalence card shows where the file was seen in devices in the organization and worldwide.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c2269-136">Différents utilisateurs peuvent voir des valeurs différentes dans les appareils de la *section* Organisation de la carte de prévalence du fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-136">Different users may see dissimilar values in the *devices in organization* section of the file prevalence card.</span></span> <span data-ttu-id="c2269-137">En effet, la carte affiche des informations en fonction de l’étendue RBAC dont dispose un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2269-137">This is because the card displays information based on the RBAC scope that a user has.</span></span> <span data-ttu-id="c2269-138">Cela signifie que si un utilisateur a obtenu une visibilité sur un ensemble spécifique d’appareils, il verra uniquement le fichier de prévalence organisationnelle sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="c2269-138">Meaning, if a user has been granted visibility on a specific set of devices, they will only see the file organizational prevalence on those devices.</span></span>

![Image des informations de fichier](images/atp-file-information.png)

## <a name="alerts"></a><span data-ttu-id="c2269-140">Alertes</span><span class="sxs-lookup"><span data-stu-id="c2269-140">Alerts</span></span>

<span data-ttu-id="c2269-141">**L’onglet Alertes** fournit une liste des alertes associées au fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-141">The **Alerts** tab provides a list of alerts that are associated with the file.</span></span> <span data-ttu-id="c2269-142">Cette liste couvre la plupart des informations de la file d’attente des alertes, à l’exception du groupe d’appareils, s’il y en a, à qui appartient l’appareil concerné.</span><span class="sxs-lookup"><span data-stu-id="c2269-142">This list covers much of the same information as the Alerts queue, except for the device group, if any, the affected device belongs to.</span></span> <span data-ttu-id="c2269-143">Vous pouvez choisir le type d’informations affiché en sélectionnant Personnaliser les colonnes dans la barre d’outils au-dessus des en-têtes de colonne. </span><span class="sxs-lookup"><span data-stu-id="c2269-143">You can choose what kind of information is shown by selecting **Customize columns** from the toolbar above the column headers.</span></span>

![Image des alertes associées à la section de fichier](images/atp-alerts-related-to-file.png)

## <a name="observed-in-organization"></a><span data-ttu-id="c2269-145">Observé dans l’organisation</span><span class="sxs-lookup"><span data-stu-id="c2269-145">Observed in organization</span></span>

<span data-ttu-id="c2269-146">L’onglet Observé **dans l’organisation** vous permet de spécifier une plage de dates pour voir quels appareils ont été observés avec le fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-146">The **Observed in organization** tab allows you to specify a date range to see which devices have been observed with the file.</span></span>

>[!NOTE]
><span data-ttu-id="c2269-147">Cet onglet affiche un nombre maximal de 100 appareils.</span><span class="sxs-lookup"><span data-stu-id="c2269-147">This tab will show a maximum number of 100 devices.</span></span> <span data-ttu-id="c2269-148">Pour voir tous _les_ appareils avec le fichier, exportez l’onglet dans un fichier CSV en sélectionnant **Exporter** à partir du menu Actions au-dessus des en-têtes de colonne de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="c2269-148">To see _all_ devices with the file, export the tab to a CSV file, by selecting **Export** from the action menu above the tab's column headers.</span></span>

![Image de l’appareil observé le plus récent avec le fichier](images/atp-observed-machines.png)

<span data-ttu-id="c2269-150">Utilisez le curseur ou le sélecteur de plage pour spécifier rapidement une période à vérifier pour les événements impliquant le fichier.</span><span class="sxs-lookup"><span data-stu-id="c2269-150">Use the slider or the range selector to quickly specify a time period that you want to check for events involving the file.</span></span> <span data-ttu-id="c2269-151">Vous pouvez spécifier une fenêtre de temps aussi petite qu’un seul jour.</span><span class="sxs-lookup"><span data-stu-id="c2269-151">You can specify a time window as small as a single day.</span></span> <span data-ttu-id="c2269-152">Cela vous permettra de voir uniquement les fichiers qui ont communiqué avec cette adresse IP à ce moment-là, ce qui réduit considérablement les recherches et les défilements inutiles.</span><span class="sxs-lookup"><span data-stu-id="c2269-152">This will allow you to see only files that communicated with that IP Address at that time, drastically reducing unnecessary scrolling and searching.</span></span>

## <a name="deep-analysis"></a><span data-ttu-id="c2269-153">Analyse approfondie</span><span class="sxs-lookup"><span data-stu-id="c2269-153">Deep analysis</span></span>

<span data-ttu-id="c2269-154">**L’onglet** Analyse approfondie vous permet d’envoyer le fichier pour analyse [approfondie,](respond-file-alerts.md#deep-analysis)de découvrir plus de détails sur le comportement du fichier, ainsi que l’effet qu’il a au sein de vos organisations.</span><span class="sxs-lookup"><span data-stu-id="c2269-154">The **Deep analysis** tab allows you to [submit the file for deep analysis](respond-file-alerts.md#deep-analysis), to uncover more details about the file's behavior, as well as the effect it is having within your organizations.</span></span> <span data-ttu-id="c2269-155">Une fois le fichier soumis, le rapport d’analyse approfondie s’affiche dans cet onglet une fois que les résultats sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c2269-155">After you submit the file, the deep analysis report will appear in this tab once results are available.</span></span> <span data-ttu-id="c2269-156">Si l’analyse approfondie n’a trouvé rien, le rapport est vide et l’espace de résultats reste vide.</span><span class="sxs-lookup"><span data-stu-id="c2269-156">If deep analysis did not find anything, the report will be empty and the results space will remain blank.</span></span>

![Image de l’onglet Analyse approfondie](images/submit-file.png)

## <a name="file-names"></a><span data-ttu-id="c2269-158">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="c2269-158">File names</span></span>

<span data-ttu-id="c2269-159">**L’onglet Noms** de fichiers répertorie tous les noms que le fichier a été observé pour utiliser, au sein de vos organisations.</span><span class="sxs-lookup"><span data-stu-id="c2269-159">The **File names** tab lists all names the file has been observed to use, within your organizations.</span></span>

![Image de l’onglet Noms de fichiers](images/atp-file-names.png)

## <a name="related-topics"></a><span data-ttu-id="c2269-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2269-161">Related topics</span></span>

- [<span data-ttu-id="c2269-162">Afficher et organiser la file d’attente de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-162">View and organize the Microsoft Defender for Endpoint queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="c2269-163">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-163">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="c2269-164">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-164">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="c2269-165">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-165">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="c2269-166">Examiner une adresse IP associée à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-166">Investigate an IP address associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="c2269-167">Examiner un domaine associé à une alerte Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-167">Investigate a domain associated with a Microsoft Defender for Endpoint alert</span></span>](investigate-domain.md)
- [<span data-ttu-id="c2269-168">Examiner un compte d’utilisateur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c2269-168">Investigate a user account in Microsoft Defender for Endpoint</span></span>](investigate-user.md)
- [<span data-ttu-id="c2269-169">Prendre des mesures de réponse sur un fichier</span><span class="sxs-lookup"><span data-stu-id="c2269-169">Take response actions on a file</span></span>](respond-file-alerts.md)