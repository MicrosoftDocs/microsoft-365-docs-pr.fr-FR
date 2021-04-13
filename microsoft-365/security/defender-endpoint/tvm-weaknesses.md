---
title: 'Vulnérabilités dans mon organisation : gestion des menaces et des vulnérabilités'
description: Répertorie les vulnérabilités courantes et l'ID d'exposition (CVE) des faiblesses trouvées dans le logiciel en cours d'exécution dans votre organisation. Découverte par microsoft Defender pour la fonctionnalité de gestion des menaces et des vulnérabilités des points de terminaison.
keywords: menace mdatp & gestion des vulnérabilités, gestion des menaces et des vulnérabilités, page de faiblesses tvm mdatp, recherche de faiblesses par le biais de tvm, liste de vulnérabilités tvm, détails de vulnérabilité dans tvm
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
ms.openlocfilehash: 0f573b2425764876e877de44555691979a0e1fcf
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689400"
---
# <a name="vulnerabilities-in-my-organization---threat-and-vulnerability-management"></a><span data-ttu-id="85c9a-105">Vulnérabilités dans mon organisation : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="85c9a-105">Vulnerabilities in my organization - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="85c9a-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="85c9a-106">**Applies to:**</span></span>
- [<span data-ttu-id="85c9a-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="85c9a-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="85c9a-108">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="85c9a-108">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="85c9a-109">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="85c9a-109">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="85c9a-110">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="85c9a-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="85c9a-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="85c9a-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="85c9a-112">La gestion des menaces et des vulnérabilités utilise les mêmes signaux dans Defender pour la protection des points de terminaison pour analyser et détecter les vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="85c9a-112">Threat and vulnerability management uses the same signals in Defender for Endpoint's endpoint protection to scan and detect vulnerabilities.</span></span>

<span data-ttu-id="85c9a-113">La page **Faiblesses** répertorie les vulnérabilités logicielles que vos appareils sont exposés en répertoriant l'ID CVE (Common Vulnerabilities and Exposures).</span><span class="sxs-lookup"><span data-stu-id="85c9a-113">The **Weaknesses** page lists the software vulnerabilities your devices are exposed to by listing the Common Vulnerabilities and Exposures (CVE) ID.</span></span> <span data-ttu-id="85c9a-114">Vous pouvez également afficher la gravité, la notation des vulnérabilités courantes (CVSS), la prévalence dans votre organisation, la violation correspondante, les informations sur les menaces, etc.</span><span class="sxs-lookup"><span data-stu-id="85c9a-114">You can also view the severity, Common Vulnerability Scoring System (CVSS) rating, prevalence in your organization, corresponding breach, threat insights, and more.</span></span>

>[!NOTE]
><span data-ttu-id="85c9a-115">Si aucun ID CVE officiel n'est affecté à une vulnérabilité, le nom de la vulnérabilité est attribué par la gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="85c9a-115">If there is no official CVE-ID assigned to a vulnerability, the vulnerability name is assigned by threat and vulnerability management.</span></span>

>[!TIP]
><span data-ttu-id="85c9a-116">Pour obtenir des e-mails sur les nouveaux événements de vulnérabilité, voir Configurer les notifications par courrier électronique de vulnérabilité [dans Microsoft Defender pour le point de terminaison](configure-vulnerability-email-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="85c9a-116">To get emails about new vulnerability events, see [Configure vulnerability email notifications in Microsoft Defender for Endpoint](configure-vulnerability-email-notifications.md)</span></span>

## <a name="navigate-to-the-weaknesses-page"></a><span data-ttu-id="85c9a-117">Accéder à la page Faiblesses</span><span class="sxs-lookup"><span data-stu-id="85c9a-117">Navigate to the Weaknesses page</span></span>

<span data-ttu-id="85c9a-118">Accédez à la page Faiblesses de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="85c9a-118">Access the Weaknesses page a few different ways:</span></span>

- <span data-ttu-id="85c9a-119">Sélection des **faiblesses dans le** menu de navigation de gestion des menaces et des vulnérabilités dans le Centre de [sécurité Microsoft Defender](portal-overview.md)</span><span class="sxs-lookup"><span data-stu-id="85c9a-119">Selecting **Weaknesses** from the threat and vulnerability management navigation menu in the [Microsoft Defender Security Center](portal-overview.md)</span></span>
- <span data-ttu-id="85c9a-120">Recherche globale</span><span class="sxs-lookup"><span data-stu-id="85c9a-120">Global search</span></span>

### <a name="navigation-menu"></a><span data-ttu-id="85c9a-121">Menu de navigation</span><span class="sxs-lookup"><span data-stu-id="85c9a-121">Navigation menu</span></span>

<span data-ttu-id="85c9a-122">Go to the threat and vulnerability management navigation menu and select **Weaknesses** to open the list of CVEs.</span><span class="sxs-lookup"><span data-stu-id="85c9a-122">Go to the threat and vulnerability management navigation menu and select **Weaknesses** to open the list of CVEs.</span></span>

### <a name="vulnerabilities-in-global-search"></a><span data-ttu-id="85c9a-123">Vulnérabilités dans la recherche globale</span><span class="sxs-lookup"><span data-stu-id="85c9a-123">Vulnerabilities in global search</span></span>

1. <span data-ttu-id="85c9a-124">Go to the global search drop-down menu.</span><span class="sxs-lookup"><span data-stu-id="85c9a-124">Go to the global search drop-down menu.</span></span>
2. <span data-ttu-id="85c9a-125">Sélectionnez **Vulnérabilité et** clé dans l'ID CVE (Common Vulnerabilities and Exposures) que vous recherchez, puis sélectionnez l'icône de recherche.</span><span class="sxs-lookup"><span data-stu-id="85c9a-125">Select **Vulnerability** and key-in the Common Vulnerabilities and Exposures (CVE) ID that you're looking for, then select the search icon.</span></span> <span data-ttu-id="85c9a-126">La page **Faiblesses** s'ouvre avec les informations CVE que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="85c9a-126">The **Weaknesses** page opens with the CVE information that you're looking for.</span></span>
<span data-ttu-id="85c9a-127">![Zone de recherche globale avec l'option « vulnérabilité » sélectionnée et un exemple CVE.](images/tvm-vuln-globalsearch.png)</span><span class="sxs-lookup"><span data-stu-id="85c9a-127">![Global search box with the dropdown option "vulnerability" selected and an example CVE.](images/tvm-vuln-globalsearch.png)</span></span>
3. <span data-ttu-id="85c9a-128">Sélectionnez la CVE pour ouvrir un panneau volant avec plus d'informations, notamment la description de la vulnérabilité, les détails, les informations sur les menaces et les appareils exposés.</span><span class="sxs-lookup"><span data-stu-id="85c9a-128">Select the CVE to open a flyout panel with more information, including the vulnerability description, details, threat insights, and exposed devices.</span></span>

<span data-ttu-id="85c9a-129">Pour voir le reste des vulnérabilités dans la page **Faiblesses,** tapez CVE, puis sélectionnez rechercher.</span><span class="sxs-lookup"><span data-stu-id="85c9a-129">To see the rest of the vulnerabilities in the **Weaknesses** page, type CVE, then select search.</span></span>

## <a name="weaknesses-overview"></a><span data-ttu-id="85c9a-130">Vue d'ensemble des faiblesses</span><span class="sxs-lookup"><span data-stu-id="85c9a-130">Weaknesses overview</span></span>

<span data-ttu-id="85c9a-131">Corriger les vulnérabilités des appareils exposés afin de réduire les risques pour vos ressources et votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85c9a-131">Remediate the vulnerabilities in exposed devices to reduce the risk to your assets and organization.</span></span> <span data-ttu-id="85c9a-132">Si la **colonne Appareils** exposés affiche 0, cela signifie que vous n'êtes pas en danger.</span><span class="sxs-lookup"><span data-stu-id="85c9a-132">If the **Exposed Devices** column shows 0, that means you aren't at risk.</span></span>

![Page d'accueil des faiblesses.](images/tvm-weaknesses-overview.png)

### <a name="breach-and-threat-insights"></a><span data-ttu-id="85c9a-134">Informations sur les violations et les menaces</span><span class="sxs-lookup"><span data-stu-id="85c9a-134">Breach and threat insights</span></span>

<span data-ttu-id="85c9a-135">Affichez les informations sur les violations et menaces associées dans la colonne **Menace** lorsque les icônes sont colorées en rouge.</span><span class="sxs-lookup"><span data-stu-id="85c9a-135">View any related breach and threat insights in the **Threat** column when the icons are colored red.</span></span>

 >[!NOTE]
 > <span data-ttu-id="85c9a-136">Toujours hiérarchiser les recommandations associées aux menaces en cours.</span><span class="sxs-lookup"><span data-stu-id="85c9a-136">Always prioritize recommendations that are associated with ongoing threats.</span></span> <span data-ttu-id="85c9a-137">Ces recommandations sont marquées avec l'icône d'informations sur les menaces ![ Simple dessin d'un bogue rouge.](images/tvm_bug_icon.png)</span><span class="sxs-lookup"><span data-stu-id="85c9a-137">These recommendations are marked with the threat insight icon ![Simple drawing of a red bug.](images/tvm_bug_icon.png)</span></span> <span data-ttu-id="85c9a-138">et l'icône d'informations sur la violation, dessin ![ simple d'une flèche qui atteint une cible. ](images/tvm_alert_icon.png) .</span><span class="sxs-lookup"><span data-stu-id="85c9a-138">and breach insight icon ![Simple drawing of an arrow hitting a target.](images/tvm_alert_icon.png).</span></span>  

<span data-ttu-id="85c9a-139">L'icône Informations sur les violations est mise en surbrillant si une vulnérabilité est trouvée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85c9a-139">The breach insights icon is highlighted if there's a vulnerability found in your organization.</span></span>
<span data-ttu-id="85c9a-140">![Exemple de texte d'informations sur la violation qui pourrait s'afficher lorsque vous placez le pointage sur l'icône.</span><span class="sxs-lookup"><span data-stu-id="85c9a-140">![Example of a breach insights text that could show up when hovering over icon.</span></span> <span data-ttu-id="85c9a-141">Celle-ci indique « une alerte active possible est associée à cette recommandation.](images/tvm-breach-insights.png)</span><span class="sxs-lookup"><span data-stu-id="85c9a-141">This one says "possible active alert is associated with this recommendation.](images/tvm-breach-insights.png)</span></span>

<span data-ttu-id="85c9a-142">L'icône Informations sur les menaces est mise en évidence si la vulnérabilité trouvée dans votre organisation est associée à des exploits.</span><span class="sxs-lookup"><span data-stu-id="85c9a-142">The threat insights icon is highlighted if there are associated exploits in the vulnerability found in your organization.</span></span> <span data-ttu-id="85c9a-143">Le pointage sur l'icône indique si la menace fait partie d'un kit d'exploitation ou est connectée à des campagnes avancées persistantes ou à des groupes d'activités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="85c9a-143">Hovering over the icon shows whether the threat is a part of an exploit kit, or connected to specific advanced persistent campaigns or activity groups.</span></span> <span data-ttu-id="85c9a-144">Lorsqu'il est disponible, il existe un lien vers un rapport d'analyse des menaces avec les actualités sur l'exploitation zéro jour, les divulgations ou les conseils de sécurité associés.</span><span class="sxs-lookup"><span data-stu-id="85c9a-144">When available, there's a link to a Threat Analytics report with zero-day exploitation news, disclosures, or related security advisories.</span></span>  

![Texte d'informations sur les menaces qui peut s'afficher lorsque vous placez le pointage sur l'icône.](images/tvm-threat-insights.png)

### <a name="gain-vulnerability-insights"></a><span data-ttu-id="85c9a-147">Obtenir des informations sur les vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="85c9a-147">Gain vulnerability insights</span></span>

<span data-ttu-id="85c9a-148">Si vous sélectionnez un contrôle CVE, un panneau volant s'ouvre avec plus d'informations, telles que la description de la vulnérabilité, les détails, les informations sur les menaces et les appareils exposés.</span><span class="sxs-lookup"><span data-stu-id="85c9a-148">If you select a CVE, a flyout panel will open with more information such as the vulnerability description, details, threat insights, and exposed devices.</span></span>

- <span data-ttu-id="85c9a-149">La catégorie « Fonctionnalité du système d'exploitation » est affichée dans les scénarios pertinents</span><span class="sxs-lookup"><span data-stu-id="85c9a-149">The "OS Feature" category is shown in relevant scenarios</span></span>
- <span data-ttu-id="85c9a-150">Vous pouvez passer à la recommandation de sécurité associée pour chaque CVE avec appareil exposé</span><span class="sxs-lookup"><span data-stu-id="85c9a-150">You can go to the related security recommendation for every CVE with exposed device</span></span>

 ![Exemple de volant de faiblesse.](images/tvm-weakness-flyout400.png)

### <a name="software-that-isnt-supported"></a><span data-ttu-id="85c9a-152">Logiciel non pris en charge</span><span class="sxs-lookup"><span data-stu-id="85c9a-152">Software that isn't supported</span></span>

<span data-ttu-id="85c9a-153">Les VC pour les logiciels qui ne sont actuellement pas pris en charge par la gestion des menaces & des vulnérabilités sont toujours présents dans la page Faiblesses.</span><span class="sxs-lookup"><span data-stu-id="85c9a-153">CVEs for software that isn't currently supported by threat & vulnerability management is still present in the Weaknesses page.</span></span> <span data-ttu-id="85c9a-154">Étant donné que le logiciel n'est pas pris en charge, seules des données limitées seront disponibles.</span><span class="sxs-lookup"><span data-stu-id="85c9a-154">Because the software is not supported, only limited data will be available.</span></span>

<span data-ttu-id="85c9a-155">Les informations sur l'appareil exposé ne seront pas disponibles pour les VC avec des logiciels non pris en cas de non-gestion.</span><span class="sxs-lookup"><span data-stu-id="85c9a-155">Exposed device information will not be available for CVEs with unsupported software.</span></span> <span data-ttu-id="85c9a-156">Filtrez en sélectionnant l'option « Non disponible » dans la section « Appareils exposés ».</span><span class="sxs-lookup"><span data-stu-id="85c9a-156">Filter by unsupported software by selecting the "Not available" option in the "Exposed devices" section.</span></span>

 ![Filtre des appareils exposés.](images/tvm-exposed-devices-filter.png)

## <a name="view-common-vulnerabilities-and-exposures-cve-entries-in-other-places"></a><span data-ttu-id="85c9a-158">Afficher les entrées CVE (Common Vulnerabilities and Exposures) à d'autres endroits</span><span class="sxs-lookup"><span data-stu-id="85c9a-158">View Common Vulnerabilities and Exposures (CVE) entries in other places</span></span>

### <a name="top-vulnerable-software-in-the-dashboard"></a><span data-ttu-id="85c9a-159">Logiciels les plus vulnérables dans le tableau de bord</span><span class="sxs-lookup"><span data-stu-id="85c9a-159">Top vulnerable software in the dashboard</span></span>

1. <span data-ttu-id="85c9a-160">Go to the [threat and vulnerability management dashboard](tvm-dashboard-insights.md) and scroll down to the Top vulnerable **software** widget.</span><span class="sxs-lookup"><span data-stu-id="85c9a-160">Go to the [threat and vulnerability management dashboard](tvm-dashboard-insights.md) and scroll down to the **Top vulnerable software** widget.</span></span> <span data-ttu-id="85c9a-161">Vous verrez le nombre de vulnérabilités trouvées dans chaque logiciel, ainsi que des informations sur les menaces et une vue d'exposition de haut niveau de l'appareil au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="85c9a-161">You will see the number of vulnerabilities found in each software, along with threat information and a high-level view of device exposure over time.</span></span>

    ![Carte logicielle la plus vulnérable avec quatre colonnes : logiciels, faiblesses, menaces, appareils exposés.](images/tvm-top-vulnerable-software500.png)

2. <span data-ttu-id="85c9a-163">Sélectionnez le logiciel que vous souhaitez examiner pour aller à une page d'exercice.</span><span class="sxs-lookup"><span data-stu-id="85c9a-163">Select the software you want to investigate to go to a drilldown page.</span></span>
3. <span data-ttu-id="85c9a-164">Sélectionnez **l'onglet Vulnérabilités découvertes.**</span><span class="sxs-lookup"><span data-stu-id="85c9a-164">Select the **Discovered vulnerabilities** tab.</span></span>
4. <span data-ttu-id="85c9a-165">Sélectionnez la vulnérabilité que vous souhaitez examiner pour plus d'informations sur les détails de la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="85c9a-165">Select the vulnerability you want to investigate for more information on vulnerability details</span></span>

    ![Vue d'ensemble de l'exploitation de Windows Server 2019.](images/windows-server-drilldown.png)

### <a name="discover-vulnerabilities-in-the-device-page"></a><span data-ttu-id="85c9a-167">Découvrir les vulnérabilités dans la page d'appareil</span><span class="sxs-lookup"><span data-stu-id="85c9a-167">Discover vulnerabilities in the device page</span></span>

<span data-ttu-id="85c9a-168">Afficher les informations sur les faiblesses associées dans la page de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="85c9a-168">View related weaknesses information in the device page.</span></span>

1. <span data-ttu-id="85c9a-169">Go to the Microsoft Defender Security Center navigation menu bar, then select the device icon.</span><span class="sxs-lookup"><span data-stu-id="85c9a-169">Go to the Microsoft Defender Security Center navigation menu bar, then select the device icon.</span></span> <span data-ttu-id="85c9a-170">La page **Liste des périphériques** s'ouvre.</span><span class="sxs-lookup"><span data-stu-id="85c9a-170">The **Devices list** page opens.</span></span>
2. <span data-ttu-id="85c9a-171">Dans la page **Liste des** appareils, sélectionnez le nom de l'appareil que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="85c9a-171">In the **Devices list** page, select the device name that you want to investigate.</span></span>

    ![Liste des appareils avec l'appareil sélectionné à examiner.](images/tvm_machinetoinvestigate.png)

3. <span data-ttu-id="85c9a-173">La page de l'appareil s'ouvre avec des détails et des options de réponse pour l'appareil que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="85c9a-173">The device page will open with details and response options for the device you want to investigate.</span></span>
4. <span data-ttu-id="85c9a-174">Sélectionnez **vulnérabilités découvertes.**</span><span class="sxs-lookup"><span data-stu-id="85c9a-174">Select **Discovered vulnerabilities**.</span></span>

    ![Page Appareil avec détails et options de réponse.](images/tvm-discovered-vulnerabilities.png)

5. <span data-ttu-id="85c9a-176">Sélectionnez la vulnérabilité que vous souhaitez examiner pour ouvrir un panneau volant avec les détails CVE, tels que : description de la vulnérabilité, informations sur les menaces et logique de détection.</span><span class="sxs-lookup"><span data-stu-id="85c9a-176">Select the vulnerability that you want to investigate to open up a flyout panel with the CVE details, such as: vulnerability description, threat insights, and detection logic.</span></span>

#### <a name="cve-detection-logic"></a><span data-ttu-id="85c9a-177">Logique de détection CVE</span><span class="sxs-lookup"><span data-stu-id="85c9a-177">CVE Detection logic</span></span>

<span data-ttu-id="85c9a-178">Comme pour la preuve logicielle, nous montrons maintenant la logique de détection que nous avons appliquée sur un appareil afin de l'afficher comme vulnérable.</span><span class="sxs-lookup"><span data-stu-id="85c9a-178">Similar to the software evidence, we now show the detection logic we applied on a device in order to state that it's vulnerable.</span></span> <span data-ttu-id="85c9a-179">La nouvelle section est appelée « Logique de détection » (dans toute vulnérabilité détectée dans la page de l'appareil) et affiche la logique et la source de détection.</span><span class="sxs-lookup"><span data-stu-id="85c9a-179">The new section is called "Detection Logic" (in any discovered vulnerability in the device page) and shows the detection logic and source.</span></span>

<span data-ttu-id="85c9a-180">La catégorie « Fonctionnalité du système d'exploitation » est également affichée dans les scénarios pertinents.</span><span class="sxs-lookup"><span data-stu-id="85c9a-180">The "OS Feature" category is also shown in relevant scenarios.</span></span> <span data-ttu-id="85c9a-181">Une CVE affecterait les appareils qui exécutent un système d'exploitation vulnérable uniquement si un composant de système d'exploitation spécifique est activé.</span><span class="sxs-lookup"><span data-stu-id="85c9a-181">A CVE would affect devices that run a vulnerable OS only if a specific OS component is enabled.</span></span> <span data-ttu-id="85c9a-182">Supposons que Windows Server 2019 présente une vulnérabilité dans son composant DNS.</span><span class="sxs-lookup"><span data-stu-id="85c9a-182">Let's say Windows Server 2019 has vulnerability in its DNS component.</span></span> <span data-ttu-id="85c9a-183">Avec cette nouvelle fonctionnalité, nous attacherons uniquement cette CVE aux appareils Windows Server 2019 avec la fonctionnalité DNS activée dans leur système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="85c9a-183">With this new capability, we’ll only attach this CVE to the Windows Server 2019 devices with the DNS capability enabled in their OS.</span></span>

![Exemple de logique de détection qui répertorie les logiciels détectés sur l'appareil et les ko.](images/tvm-cve-detection-logic.png)

## <a name="report-inaccuracy"></a><span data-ttu-id="85c9a-185">Inaccuracy de rapport</span><span class="sxs-lookup"><span data-stu-id="85c9a-185">Report inaccuracy</span></span>

<span data-ttu-id="85c9a-186">Signalez un faux positif lorsque vous voyez des informations vagues, inexactes ou incomplètes.</span><span class="sxs-lookup"><span data-stu-id="85c9a-186">Report a false positive when you see any vague, inaccurate, or incomplete information.</span></span> <span data-ttu-id="85c9a-187">Vous pouvez également signaler les recommandations de sécurité qui ont déjà été corrigés.</span><span class="sxs-lookup"><span data-stu-id="85c9a-187">You can also report on security recommendations that have already been remediated.</span></span>

1. <span data-ttu-id="85c9a-188">Ouvrez la CVE sur la page Faiblesses.</span><span class="sxs-lookup"><span data-stu-id="85c9a-188">Open the CVE on the Weaknesses page.</span></span>
2. <span data-ttu-id="85c9a-189">Select **Report inaccuracy** and a flyout pane will open.</span><span class="sxs-lookup"><span data-stu-id="85c9a-189">Select **Report inaccuracy** and a flyout pane will open.</span></span>
3. <span data-ttu-id="85c9a-190">Sélectionnez la catégorie d'imprécision dans le menu déroulant et remplissez votre adresse e-mail et les détails d'imprécision.</span><span class="sxs-lookup"><span data-stu-id="85c9a-190">Select the inaccuracy category from the drop-down menu and fill in your email address and inaccuracy details.</span></span>
4. <span data-ttu-id="85c9a-191">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="85c9a-191">Select **Submit**.</span></span> <span data-ttu-id="85c9a-192">Vos commentaires sont immédiatement envoyés aux experts en gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="85c9a-192">Your feedback is immediately sent to the threat and vulnerability management experts.</span></span>

## <a name="related-articles"></a><span data-ttu-id="85c9a-193">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="85c9a-193">Related articles</span></span>

- [<span data-ttu-id="85c9a-194">Vue d'ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="85c9a-194">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="85c9a-195">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="85c9a-195">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="85c9a-196">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="85c9a-196">Software inventory</span></span>](tvm-software-inventory.md)
- [<span data-ttu-id="85c9a-197">Tableau de bord des informations</span><span class="sxs-lookup"><span data-stu-id="85c9a-197">Dashboard insights</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="85c9a-198">Afficher et organiser la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="85c9a-198">View and organize the Microsoft Defender for Endpoint Devices list</span></span>](machines-view-overview.md)
