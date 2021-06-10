---
title: Inventaire logiciel dans Gestion des menaces et des vulnérabilités
description: La page d’inventaire des logiciels du point de terminaison de Microsoft Defender Gestion des menaces et des vulnérabilités le nombre de faiblesses et de vulnérabilités détectées dans les logiciels.
keywords: Gestion des menaces et des vulnérabilités, Microsoft Defender pour le point de terminaison, Inventaire logiciel Microsoft Defender pour les points de terminaison, Microsoft Defender pour les & gestion des vulnérabilités de menaces de point de terminaison, Inventaire logiciel microsoft Defender pour les menaces de point de terminaison & gestion des vulnérabilités, inventaire logiciel tvm de Microsoft Defender pour endpoint, inventaire des logiciels tvm
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
ms.openlocfilehash: 0d270760cfed965c8190668afcdb1cc25223d2b1
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933720"
---
# <a name="software-inventory---threat-and-vulnerability-management"></a><span data-ttu-id="fc5ab-104">Inventaire logiciel : Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="fc5ab-104">Software inventory - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fc5ab-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fc5ab-105">**Applies to:**</span></span>
- [<span data-ttu-id="fc5ab-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fc5ab-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="fc5ab-107">Menaces et gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="fc5ab-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="fc5ab-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fc5ab-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="fc5ab-109">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="fc5ab-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="fc5ab-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="fc5ab-111">L’inventaire logiciel dans Gestion des menaces et des vulnérabilités liste des logiciels connus de votre organisation avec les [énumérations officielles de plateforme commune (CPE)](https://nvd.nist.gov/products/cpe).</span><span class="sxs-lookup"><span data-stu-id="fc5ab-111">The software inventory in threat and vulnerability management is a list of known software in your organization with official [Common Platform Enumerations (CPE)](https://nvd.nist.gov/products/cpe).</span></span> <span data-ttu-id="fc5ab-112">Les produits logiciels sans CPE officielles n'ont pas de vulnérabilités publiées.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-112">Software products without an official CPE don’t have vulnerabilities published.</span></span> <span data-ttu-id="fc5ab-113">Il inclut également des détails tels que le nom du fournisseur, le nombre de faiblesses, les menaces et le nombre d’appareils exposés.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-113">It also includes details such as the name of the vendor, number of weaknesses, threats, and number of exposed devices.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="fc5ab-114">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="fc5ab-114">How it works</span></span>

<span data-ttu-id="fc5ab-115">Dans le domaine de la découverte, nous tirent parti du même ensemble de signaux qui est responsable de l’évaluation de la détection et de la vulnérabilité dans Microsoft Defender pour les fonctionnalités de détection et de réponse des points de [terminaison.](overview-endpoint-detection-response.md)</span><span class="sxs-lookup"><span data-stu-id="fc5ab-115">In the field of discovery, we're leveraging the same set of signals that is responsible for detection and vulnerability assessment in [Microsoft Defender for Endpoint detection and response capabilities](overview-endpoint-detection-response.md).</span></span>

<span data-ttu-id="fc5ab-116">Dans la mesure où c’est en temps réel, en quelques minutes, vous verrez des informations de vulnérabilité au moment où elles sont découvertes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-116">Since it's real time, in a matter of minutes, you'll see vulnerability information as they get discovered.</span></span> <span data-ttu-id="fc5ab-117">Le moteur prend automatiquement des informations à partir de plusieurs flux de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-117">The engine automatically grabs information from multiple security feeds.</span></span> <span data-ttu-id="fc5ab-118">En fait, vous verrez si un logiciel particulier est connecté à une campagne contre les menaces en direct.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-118">In fact, you'll see if a particular software is connected to a live threat campaign.</span></span> <span data-ttu-id="fc5ab-119">Il fournit également un lien vers un rapport d’analyse des menaces dès qu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-119">It also provides a link to a Threat Analytics report soon as it's available.</span></span>

## <a name="navigate-to-the-software-inventory-page"></a><span data-ttu-id="fc5ab-120">Accéder à la page Inventaire logiciel</span><span class="sxs-lookup"><span data-stu-id="fc5ab-120">Navigate to the Software inventory page</span></span>

<span data-ttu-id="fc5ab-121">Accédez à la page  Inventaire logiciel en sélectionnant Inventaire logiciel dans Gestion des menaces et des vulnérabilités menu de navigation dans le [Centre de sécurité Microsoft Defender](portal-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fc5ab-121">Access the Software inventory page by selecting **Software inventory** from the threat and vulnerability management navigation menu in the [Microsoft Defender Security Center](portal-overview.md).</span></span>

<span data-ttu-id="fc5ab-122">Afficher les logiciels sur des appareils spécifiques dans les pages des appareils individuels à partir de la [liste des appareils.](machines-view-overview.md)</span><span class="sxs-lookup"><span data-stu-id="fc5ab-122">View software on specific devices in the individual devices pages from the [devices list](machines-view-overview.md).</span></span>

>[!NOTE]
><span data-ttu-id="fc5ab-123">Si vous recherchez des logiciels à l’aide de la recherche globale de Microsoft Defender for Endpoint, veillez à placer un trait de soulignement au lieu d’un espace.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-123">If you search for software using the Microsoft Defender for Endpoint global search, make sure to put an underscore instead of a space.</span></span> <span data-ttu-id="fc5ab-124">Par exemple, pour obtenir les meilleurs résultats de recherche, vous devez écrire « windows_10 » au lieu de « Windows 10 ».</span><span class="sxs-lookup"><span data-stu-id="fc5ab-124">For example, for the best search results you'd write "windows_10" instead of "Windows 10".</span></span>

## <a name="software-inventory-overview"></a><span data-ttu-id="fc5ab-125">Vue d’ensemble de l’inventaire logiciel</span><span class="sxs-lookup"><span data-stu-id="fc5ab-125">Software inventory overview</span></span>

<span data-ttu-id="fc5ab-126">La **page** Inventaire logiciel s’ouvre avec une liste des logiciels installés dans votre réseau, y compris le nom du fournisseur, les faiblesses trouvées, les menaces qui y sont associées, les appareils exposés, l’impact sur le score d’exposition et les balises.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-126">The **Software inventory** page opens with a list of software installed in your network, including the vendor name, weaknesses found, threats associated with them, exposed devices, impact to exposure score, and tags.</span></span>

<span data-ttu-id="fc5ab-127">Vous pouvez filtrer l’affichage liste en fonction des faiblesses trouvées dans le logiciel, des menaces qui lui sont associées et des balises telles que si le logiciel a atteint la fin de la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-127">You can filter the list view based on weaknesses found in the software, threats associated with them, and tags like whether the software has reached end-of-support.</span></span>

![Exemple de page d’accueil pour l’inventaire logiciel.](images/tvm-software-inventory.png)

<span data-ttu-id="fc5ab-129">Sélectionnez le logiciel que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-129">Select the software that you want to investigate.</span></span> <span data-ttu-id="fc5ab-130">Un panneau volant s’ouvre avec une vue plus compacte des informations sur la page.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-130">A flyout panel will open with a more compact view of the information on the page.</span></span> <span data-ttu-id="fc5ab-131">Vous pouvez soit approfondir l’examen et sélectionner la page Ouvrir **un** logiciel, soit signaler toute incohérence technique en sélectionnant **l’imprécision du rapport.**</span><span class="sxs-lookup"><span data-stu-id="fc5ab-131">You can either dive deeper into the investigation and select **Open software page**, or flag any technical inconsistencies by selecting **Report inaccuracy**.</span></span>

### <a name="software-that-isnt-supported"></a><span data-ttu-id="fc5ab-132">Logiciel non pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc5ab-132">Software that isn't supported</span></span>

<span data-ttu-id="fc5ab-133">Les logiciels qui ne sont actuellement pas pris en charge par les menaces & gestion des vulnérabilités peuvent être présents dans la page Inventaire logiciel.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-133">Software that isn't currently supported by threat & vulnerability management may be present in the Software inventory page.</span></span> <span data-ttu-id="fc5ab-134">Étant donné qu’il n’est pas pris en charge, seules des données limitées seront disponibles.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-134">Because it is not supported, only limited data will be available.</span></span> <span data-ttu-id="fc5ab-135">Filtrez selon les logiciels non pris en place avec l’option « Non disponible » dans la section « Faiblesse ».</span><span class="sxs-lookup"><span data-stu-id="fc5ab-135">Filter by unsupported software with the "Not available" option in the "Weakness" section.</span></span>

![Filtre logiciel non pris en temps et place.](images/tvm-unsupported-software-filter.png)

<span data-ttu-id="fc5ab-137">Ce qui suit indique qu’un logiciel n’est pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="fc5ab-137">The following indicates that a software is not supported:</span></span>

- <span data-ttu-id="fc5ab-138">Le champ Faiblesses indique « Non disponible »</span><span class="sxs-lookup"><span data-stu-id="fc5ab-138">Weaknesses field shows "Not available"</span></span>
- <span data-ttu-id="fc5ab-139">Le champ Appareils exposés affiche un tiret</span><span class="sxs-lookup"><span data-stu-id="fc5ab-139">Exposed devices field shows a dash</span></span>
- <span data-ttu-id="fc5ab-140">Texte d’information ajouté dans le panneau latéral et dans la page du logiciel</span><span class="sxs-lookup"><span data-stu-id="fc5ab-140">Informational text added in side panel and in software page</span></span>
- <span data-ttu-id="fc5ab-141">La page logicielle ne contient pas les recommandations de sécurité, les vulnérabilités découvertes ou les sections de chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="fc5ab-141">The software page won't have the security recommendations, discovered vulnerabilities, or event timeline sections</span></span>

<span data-ttu-id="fc5ab-142">Actuellement, les produits sans CPE ne sont pas affichés dans la page d’inventaire logiciel, uniquement dans l’inventaire logiciel au niveau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-142">Currently, products without a CPE are not shown in the software inventory page, only in the device level software inventory.</span></span>

## <a name="software-inventory-on-devices"></a><span data-ttu-id="fc5ab-143">Inventaire logiciel sur les appareils</span><span class="sxs-lookup"><span data-stu-id="fc5ab-143">Software inventory on devices</span></span>

<span data-ttu-id="fc5ab-144">Dans le Centre de sécurité Microsoft Defender de navigation, allez dans la liste **[Appareils.](machines-view-overview.md)**</span><span class="sxs-lookup"><span data-stu-id="fc5ab-144">From the Microsoft Defender Security Center navigation panel, go to the **[Devices list](machines-view-overview.md)**.</span></span> <span data-ttu-id="fc5ab-145">Sélectionnez le nom d’un appareil pour ouvrir la  page de l’appareil (tel que Computer1), puis sélectionnez l’onglet Inventaire logiciel pour voir la liste de tous les logiciels connus présents sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-145">Select the name of a device to open the device page (like Computer1), then select the **Software inventory** tab to see a list of all the known software present on the device.</span></span> <span data-ttu-id="fc5ab-146">Sélectionnez une entrée de logiciel spécifique pour ouvrir le volant avec plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-146">Select a specific software entry to open the flyout with more information.</span></span>

<span data-ttu-id="fc5ab-147">Le logiciel peut être visible au niveau de l’appareil même s’il n’est actuellement pas pris en charge par Gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-147">Software may be visible at the device level even if it is currently not supported by threat and vulnerability management.</span></span> <span data-ttu-id="fc5ab-148">Toutefois, seules des données limitées seront disponibles.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-148">However, only limited data will be available.</span></span> <span data-ttu-id="fc5ab-149">Vous savez si le logiciel n’est pas pris en compte, car il indique « Non disponible » dans la colonne « Faiblesse ».</span><span class="sxs-lookup"><span data-stu-id="fc5ab-149">You'll know if software is unsupported because it will say "Not available" in the "Weakness" column.</span></span>

<span data-ttu-id="fc5ab-150">Les logiciels sans CPE peuvent également s’afficher sous cet inventaire logiciel spécifique à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-150">Software with no CPE can also show up under this device specific software inventory.</span></span>

### <a name="software-evidence"></a><span data-ttu-id="fc5ab-151">Preuve logicielle</span><span class="sxs-lookup"><span data-stu-id="fc5ab-151">Software evidence</span></span>

<span data-ttu-id="fc5ab-152">Voir la preuve de l’endroit où nous avons détecté un logiciel spécifique sur un appareil à partir du Registre, du disque ou des deux. Vous pouvez le trouver sur n’importe quel appareil dans l’inventaire logiciel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-152">See evidence of where we detected a specific software on a device from the registry, disk, or both.You can find it on any device in the device software inventory.</span></span>

<span data-ttu-id="fc5ab-153">Sélectionnez un nom de logiciel pour ouvrir le volant et recherchez la section appelée « Preuve logicielle ».</span><span class="sxs-lookup"><span data-stu-id="fc5ab-153">Select a software name to open the flyout, and look for the section called "Software Evidence."</span></span>

![Exemple de preuve logicielle de Windows 10 de la liste des appareils, montrant le chemin d’accès au Registre des preuves logicielles.](images/tvm-software-evidence.png)

## <a name="software-pages"></a><span data-ttu-id="fc5ab-155">Pages logicielles</span><span class="sxs-lookup"><span data-stu-id="fc5ab-155">Software pages</span></span>

<span data-ttu-id="fc5ab-156">Vous pouvez afficher les pages logicielles de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="fc5ab-156">You can view software pages a few different ways:</span></span>

- <span data-ttu-id="fc5ab-157">Page d’inventaire > sélectionnez un nom de logiciel > **page** Sélectionner un logiciel ouvert dans le volant</span><span class="sxs-lookup"><span data-stu-id="fc5ab-157">Software inventory page > Select a software name > Select **Open software page** in the flyout</span></span>
- <span data-ttu-id="fc5ab-158">[Page Recommandations en matière](tvm-security-recommendation.md) de sécurité > sélectionner une recommandation > **page** Sélectionner un logiciel ouvert dans le volant</span><span class="sxs-lookup"><span data-stu-id="fc5ab-158">[Security recommendations page](tvm-security-recommendation.md) > Select a recommendation > Select **Open software page** in the flyout</span></span>
- <span data-ttu-id="fc5ab-159">Page chronologie des [événements](threat-and-vuln-mgt-event-timeline.md) > Sélectionnez un > Sélectionnez le nom du logiciel avec lien hypertexte (comme Visual Studio 2017) dans la section intitulée « Composant associé » dans le volant</span><span class="sxs-lookup"><span data-stu-id="fc5ab-159">[Event timeline page](threat-and-vuln-mgt-event-timeline.md) > Select an event > Select the hyperlinked software name (like Visual Studio 2017) in the section called "Related component" in the flyout</span></span>

 <span data-ttu-id="fc5ab-160">Une page complète s’affiche avec tous les détails d’un logiciel spécifique et les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc5ab-160">A full page will appear with all the details of a specific software and the following information:</span></span>

- <span data-ttu-id="fc5ab-161">Panneau latéral avec des informations sur le fournisseur, la prévalence du logiciel dans l’organisation (y compris le nombre d’appareils sur lesquels il est installé et les appareils exposés qui ne sont pas corrigés), si et exploit est disponible et impact sur votre score d’exposition.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-161">Side panel with vendor information, prevalence of the software in the organization (including number of devices it's installed on, and exposed devices that aren't patched), whether and exploit is available, and impact to your exposure score.</span></span>
- <span data-ttu-id="fc5ab-162">Visualisations de données montrant le nombre et la gravité des vulnérabilités et des mauvaises configurations.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-162">Data visualizations showing the number of, and severity of, vulnerabilities and misconfigurations.</span></span> <span data-ttu-id="fc5ab-163">En outre, les graphiques avec le nombre d’appareils exposés.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-163">Also, graphs with the number of exposed devices.</span></span>
- <span data-ttu-id="fc5ab-164">Onglets affichant des informations telles que :</span><span class="sxs-lookup"><span data-stu-id="fc5ab-164">Tabs showing information such as:</span></span>
    - <span data-ttu-id="fc5ab-165">Recommandations de sécurité correspondantes pour les faiblesses et vulnérabilités identifiées.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-165">Corresponding security recommendations for the weaknesses and vulnerabilities identified.</span></span>
    - <span data-ttu-id="fc5ab-166">Cv nommés des vulnérabilités découvertes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-166">Named CVEs of discovered vulnerabilities.</span></span>
    - <span data-ttu-id="fc5ab-167">Les appareils sur qui le logiciel est installé (ainsi que le nom de l’appareil, le domaine, le système d’exploitation, et bien plus encore).</span><span class="sxs-lookup"><span data-stu-id="fc5ab-167">Devices that have the software installed (along with device name, domain, OS, and more).</span></span>
    - <span data-ttu-id="fc5ab-168">Liste des versions des logiciels (y compris le nombre d’appareils sur lesquels la version est installée, le nombre de vulnérabilités découvertes et les noms des appareils installés).</span><span class="sxs-lookup"><span data-stu-id="fc5ab-168">Software version list (including number of devices the version is installed on, the number of discovered vulnerabilities, and the names of the installed devices).</span></span>

    ![Page d’exemples de logiciels Visual Studio 2017 avec les détails logiciels, les faiblesses, les appareils exposés, etc.](images/tvm-software-page-example.png)

## <a name="report-inaccuracy"></a><span data-ttu-id="fc5ab-170">Report inaccuracy</span><span class="sxs-lookup"><span data-stu-id="fc5ab-170">Report inaccuracy</span></span>

<span data-ttu-id="fc5ab-171">Signalez un faux positif lorsque vous voyez des informations vagues, inexactes ou incomplètes.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-171">Report a false positive when you see any vague, inaccurate, or incomplete information.</span></span> <span data-ttu-id="fc5ab-172">Vous pouvez également signaler les recommandations de sécurité qui ont déjà été corrigés.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-172">You can also report on security recommendations that have already been remediated.</span></span>

1. <span data-ttu-id="fc5ab-173">Ouvrez le programme volant sur la page Inventaire logiciel.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-173">Open the software flyout on the Software inventory page.</span></span>
2. <span data-ttu-id="fc5ab-174">Select **Report inaccuracy**.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-174">Select **Report inaccuracy**.</span></span>
3. <span data-ttu-id="fc5ab-175">Dans le volet de menu volant, sélectionnez la catégorie imprécise dans le menu déroulant, remplissez votre adresse e-mail et des détails sur l’imprécision.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-175">From the flyout pane, select the inaccuracy category from the drop-down menu, fill in your email address, and details about the inaccuracy.</span></span>
4. <span data-ttu-id="fc5ab-176">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-176">Select **Submit**.</span></span> <span data-ttu-id="fc5ab-177">Vos commentaires sont immédiatement envoyés aux experts Gestion des menaces et des vulnérabilités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fc5ab-177">Your feedback is immediately sent to the threat and vulnerability management experts.</span></span>

## <a name="related-articles"></a><span data-ttu-id="fc5ab-178">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="fc5ab-178">Related articles</span></span>

- [<span data-ttu-id="fc5ab-179">Vue d’ensemble gestion des vulnérabilités menaces et gestion des vulnérabilités menaces</span><span class="sxs-lookup"><span data-stu-id="fc5ab-179">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="fc5ab-180">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="fc5ab-180">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="fc5ab-181">Chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="fc5ab-181">Event timeline</span></span>](threat-and-vuln-mgt-event-timeline.md)
- [<span data-ttu-id="fc5ab-182">Afficher et organiser la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fc5ab-182">View and organize the Microsoft Defender for Endpoint Devices list</span></span>](machines-view-overview.md)
