---
title: Utiliser des enquêtes automatisées pour examiner et corriger les menaces
description: Comprendre le flux d’examen automatisé dans Microsoft Defender pour point de terminaison.
keywords: automatisé, examen, détection, Microsoft Defender pour point de terminaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.technology: mde
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: JoeDavies-MSFT
ms.author: josephd
ms.date: 02/02/2021
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: how-to
ms.reviewer: ramarom, evaldm, isco, mabraitm, chriggs
ms.custom: AIR
ms.openlocfilehash: e52471e1b3e9ee3a410de493b536f9d360d60624
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844441"
---
# <a name="overview-of-automated-investigations"></a><span data-ttu-id="1d18a-104">Vue d’ensemble des examens automatisés</span><span class="sxs-lookup"><span data-stu-id="1d18a-104">Overview of automated investigations</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1d18a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1d18a-105">**Applies to:**</span></span>
- [<span data-ttu-id="1d18a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d18a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1d18a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1d18a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


<span data-ttu-id="1d18a-108">Vous voulez voir comment cela fonctionne ?</span><span class="sxs-lookup"><span data-stu-id="1d18a-108">Want to see how it works?</span></span> <span data-ttu-id="1d18a-109">Regardez la vidéo suivante :</span><span class="sxs-lookup"><span data-stu-id="1d18a-109">Watch the following video:</span></span> <br/><br/>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4bOeh]

<span data-ttu-id="1d18a-110">La technologie utilisée dans les enquêtes automatisées utilise différents algorithmes d’inspection et repose sur des processus utilisés par les analystes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d18a-110">The technology in automated investigation uses various inspection algorithms and is based on processes that are used by security analysts.</span></span> <span data-ttu-id="1d18a-111">Les fonctionnalités AIR sont conçues pour examiner les alertes et prendre des mesures immédiates pour résoudre les violations.</span><span class="sxs-lookup"><span data-stu-id="1d18a-111">AIR capabilities are designed to examine alerts and take immediate action to resolve breaches.</span></span> <span data-ttu-id="1d18a-112">Les fonctionnalités AIR réduisent considérablement le volume d’alertes, ce qui permet aux opérations de sécurité de se concentrer sur des menaces plus sophistiquées et d’autres initiatives à valeur élevée.</span><span class="sxs-lookup"><span data-stu-id="1d18a-112">AIR capabilities significantly reduce alert volume, allowing security operations to focus on more sophisticated threats and other high-value initiatives.</span></span> <span data-ttu-id="1d18a-113">Toutes les actions de correction, en attente ou terminées, sont suivis dans le centre [de correction.](auto-investigation-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="1d18a-113">All remediation actions, whether pending or completed, are tracked in the [Action center](auto-investigation-action-center.md).</span></span> <span data-ttu-id="1d18a-114">Dans le centre de traitement des actions, les actions en attente sont approuvées (ou rejetées) et les actions terminées peuvent être annulées si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d18a-114">In the Action center, pending actions are approved (or rejected), and completed actions can be undone if needed.</span></span>

<span data-ttu-id="1d18a-115">Cet article fournit une vue d’ensemble d’AIR et inclut des liens vers les étapes suivantes et des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1d18a-115">This article provides an overview of AIR and includes links to next steps and additional resources.</span></span>

> [!TIP]
> <span data-ttu-id="1d18a-116">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1d18a-116">Want to experience Microsoft Defender for Endpoint?</span></span> <span data-ttu-id="1d18a-117">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-automated-investigations-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="1d18a-117">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-automated-investigations-abovefoldlink).</span></span>

## <a name="how-the-automated-investigation-starts"></a><span data-ttu-id="1d18a-118">Comment l’examen automatisé démarre</span><span class="sxs-lookup"><span data-stu-id="1d18a-118">How the automated investigation starts</span></span>

<span data-ttu-id="1d18a-119">Une enquête automatisée peut commencer lorsqu’une alerte est déclenchée ou lorsqu’un opérateur de sécurité lance l’enquête.</span><span class="sxs-lookup"><span data-stu-id="1d18a-119">An automated investigation can start when an alert is triggered or when a security operator initiates the investigation.</span></span>

|<span data-ttu-id="1d18a-120">Situation</span><span class="sxs-lookup"><span data-stu-id="1d18a-120">Situation</span></span>  |<span data-ttu-id="1d18a-121">Action exécutée</span><span class="sxs-lookup"><span data-stu-id="1d18a-121">What happens</span></span>  |
|---------|---------|
|<span data-ttu-id="1d18a-122">Une alerte est déclenchée</span><span class="sxs-lookup"><span data-stu-id="1d18a-122">An alert is triggered</span></span>     | <span data-ttu-id="1d18a-123">En règle générale, une enquête automatisée démarre [lorsqu’une](review-alerts.md) alerte est déclenchée et qu’un [incident](view-incidents-queue.md) est créé.</span><span class="sxs-lookup"><span data-stu-id="1d18a-123">In general, an automated investigation starts when an [alert](review-alerts.md) is triggered, and an [incident](view-incidents-queue.md) is created.</span></span> <span data-ttu-id="1d18a-124">Par exemple, supposons qu’un fichier malveillant réside sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="1d18a-124">For example, suppose a malicious file resides on a device.</span></span> <span data-ttu-id="1d18a-125">Lorsque ce fichier est détecté, une alerte est déclenchée et un incident est créé.</span><span class="sxs-lookup"><span data-stu-id="1d18a-125">When that file is detected, an alert is triggered, and incident is created.</span></span> <span data-ttu-id="1d18a-126">Un processus d’examen automatisé commence sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1d18a-126">An automated investigation process begins on the device.</span></span> <span data-ttu-id="1d18a-127">Comme d’autres alertes sont générées en raison du même fichier sur d’autres appareils, elles sont ajoutées à l’incident associé et à l’examen automatisé.</span><span class="sxs-lookup"><span data-stu-id="1d18a-127">As other alerts are generated because of the same file on other devices, they are added to the associated incident and to the automated investigation.</span></span>         |
|<span data-ttu-id="1d18a-128">Une enquête est démarrée manuellement</span><span class="sxs-lookup"><span data-stu-id="1d18a-128">An investigation is started manually</span></span>     | <span data-ttu-id="1d18a-129">Une enquête automatisée peut être lancée manuellement par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d18a-129">An automated investigation can be started manually by your security operations team.</span></span> <span data-ttu-id="1d18a-130">Par exemple, supposons qu’un opérateur de sécurité examine une liste d’appareils et remarque qu’un appareil présente un niveau de risque élevé.</span><span class="sxs-lookup"><span data-stu-id="1d18a-130">For example, suppose a security operator is reviewing a list of devices and notices that a device has a high risk level.</span></span> <span data-ttu-id="1d18a-131">L’opérateur de sécurité peut sélectionner l’appareil dans la liste pour ouvrir son volant, puis sélectionner **Lancer une enquête automatisée.**</span><span class="sxs-lookup"><span data-stu-id="1d18a-131">The security operator can select the device in the list to open its flyout, and then select **Initiate Automated Investigation**.</span></span> |

## <a name="how-an-automated-investigation-expands-its-scope"></a><span data-ttu-id="1d18a-132">Comment un examen automatisé étend son étendue</span><span class="sxs-lookup"><span data-stu-id="1d18a-132">How an automated investigation expands its scope</span></span>

<span data-ttu-id="1d18a-133">Pendant l’exécution d’un examen, toutes les autres alertes générées à partir de l’appareil sont ajoutées à un examen automatisé en cours jusqu’à ce que l’enquête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="1d18a-133">While an investigation is running, any other alerts generated from the device are added to an ongoing automated investigation until that investigation is completed.</span></span> <span data-ttu-id="1d18a-134">En outre, si la même menace est vue sur d’autres appareils, ces appareils sont ajoutés à l’examen.</span><span class="sxs-lookup"><span data-stu-id="1d18a-134">In addition, if the same threat is seen on other devices, those devices are added to the investigation.</span></span>

<span data-ttu-id="1d18a-135">Si une entité incriminée est vue dans un autre appareil, le processus d’examen automatisé étend son étendue pour inclure cet appareil, et un manuel de sécurité général démarre sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="1d18a-135">If an incriminated entity is seen in another device, the automated investigation process expands its scope to include that device, and a general security playbook starts on that device.</span></span> <span data-ttu-id="1d18a-136">Si au moins 10 appareils sont trouvés au cours de ce processus d’expansion à partir de la même entité, cette action d’expansion nécessite une approbation et est visible sous l’onglet **Actions** en attente.</span><span class="sxs-lookup"><span data-stu-id="1d18a-136">If 10 or more devices are found during this expansion process from the same entity, then that expansion action requires an approval, and is visible on the **Pending actions** tab.</span></span>

## <a name="how-threats-are-remediated"></a><span data-ttu-id="1d18a-137">Comment les menaces sont-elles corrigés ?</span><span class="sxs-lookup"><span data-stu-id="1d18a-137">How threats are remediated</span></span>

<span data-ttu-id="1d18a-138">Lorsque des alertes sont déclenchées et qu’une enquête automatisée s’exécute, un verdict est généré pour chaque élément de preuve examiné.</span><span class="sxs-lookup"><span data-stu-id="1d18a-138">As alerts are triggered, and an automated investigation runs, a verdict is generated for each piece of evidence investigated.</span></span> <span data-ttu-id="1d18a-139">Les verdicts peuvent être</span><span class="sxs-lookup"><span data-stu-id="1d18a-139">Verdicts can be</span></span> 
- <span data-ttu-id="1d18a-140">*Malveillant*;</span><span class="sxs-lookup"><span data-stu-id="1d18a-140">*Malicious*;</span></span>
- <span data-ttu-id="1d18a-141">*Suspect*; ou</span><span class="sxs-lookup"><span data-stu-id="1d18a-141">*Suspicious*; or</span></span> 
- <span data-ttu-id="1d18a-142">*Aucune menace trouvée.*</span><span class="sxs-lookup"><span data-stu-id="1d18a-142">*No threats found*.</span></span> 

<span data-ttu-id="1d18a-143">À mesure que les verdicts sont atteints, des enquêtes automatisées peuvent entraîner une ou plusieurs actions de correction.</span><span class="sxs-lookup"><span data-stu-id="1d18a-143">As verdicts are reached, automated investigations can result in one or more remediation actions.</span></span> <span data-ttu-id="1d18a-144">L’envoi d’un fichier en quarantaine, l’arrêt d’un service, la suppression d’une tâche programmée, etc. sont des exemples d’actions de correction.</span><span class="sxs-lookup"><span data-stu-id="1d18a-144">Examples of remediation actions include sending a file to quarantine, stopping a service, removing a scheduled task, and more.</span></span> <span data-ttu-id="1d18a-145">Pour plus d’informations, voir [Actions de correction.](manage-auto-investigation.md#remediation-actions)</span><span class="sxs-lookup"><span data-stu-id="1d18a-145">To learn more, see [Remediation actions](manage-auto-investigation.md#remediation-actions).</span></span>  

<span data-ttu-id="1d18a-146">Selon le niveau [d’automatisation](automation-levels.md) définie pour votre organisation, ainsi que d’autres paramètres de sécurité, des actions de correction peuvent se produire automatiquement ou uniquement après approbation par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d18a-146">Depending on the [level of automation](automation-levels.md) set for your organization, as well as other security settings, remediation actions can occur automatically or only upon approval by your security operations team.</span></span> <span data-ttu-id="1d18a-147">Les paramètres de sécurité supplémentaires pouvant affecter la correction automatique incluent la protection contre les [applications potentiellement](/windows/security/threat-protection/microsoft-defender-antivirus/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus) indésirables (PUA).</span><span class="sxs-lookup"><span data-stu-id="1d18a-147">Additional security settings that can affect automatic remediation include [protection from potentially unwanted applications](/windows/security/threat-protection/microsoft-defender-antivirus/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus) (PUA).</span></span> 

<span data-ttu-id="1d18a-148">Toutes les actions de correction, en attente ou terminées, sont suivis dans le centre [de correction.](auto-investigation-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="1d18a-148">All remediation actions, whether pending or completed, are tracked in the [Action center](auto-investigation-action-center.md).</span></span> <span data-ttu-id="1d18a-149">Si nécessaire, votre équipe des opérations de sécurité peut annuler une action de correction.</span><span class="sxs-lookup"><span data-stu-id="1d18a-149">If necessary, your security operations team can undo a remediation action.</span></span> <span data-ttu-id="1d18a-150">Pour plus d’informations, voir [Examiner et approuver les actions de correction à la suite d’un examen automatisé.](/microsoft-365/security/defender-endpoint/manage-auto-investigation)</span><span class="sxs-lookup"><span data-stu-id="1d18a-150">To learn more, see [Review and approve remediation actions following an automated investigation](/microsoft-365/security/defender-endpoint/manage-auto-investigation).</span></span>

> [!TIP]
> <span data-ttu-id="1d18a-151">Consultez la nouvelle page d’examen unifié dans le centre Microsoft 365 sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d18a-151">Check out the new, unified investigation page in the Microsoft 365 security center.</span></span> <span data-ttu-id="1d18a-152">Pour en savoir plus, [voir (NOUVEAU!) Page d’examen unifié](/microsoft-365/security/defender/m365d-autoir-results#new-unified-investigation-page).</span><span class="sxs-lookup"><span data-stu-id="1d18a-152">To learn more, see [(NEW!) Unified investigation page](/microsoft-365/security/defender/m365d-autoir-results#new-unified-investigation-page).</span></span>


## <a name="requirements-for-air"></a><span data-ttu-id="1d18a-153">Conditions requises pour AIR</span><span class="sxs-lookup"><span data-stu-id="1d18a-153">Requirements for AIR</span></span>

<span data-ttu-id="1d18a-154">Votre organisation doit avoir Defender pour le point de terminaison (voir [Minimum requirements for Microsoft Defender for Endpoint](minimum-requirements.md)).</span><span class="sxs-lookup"><span data-stu-id="1d18a-154">Your organization must have Defender for Endpoint (see [Minimum requirements for Microsoft Defender for Endpoint](minimum-requirements.md)).</span></span>

<span data-ttu-id="1d18a-155">Actuellement, AIR prend uniquement en charge les versions de système d’exploitation suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d18a-155">Currently, AIR only supports the following OS versions:</span></span>
- <span data-ttu-id="1d18a-156">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="1d18a-156">Windows Server 2019</span></span>
- <span data-ttu-id="1d18a-157">Windows 10, version 1709 (os Build 16299.1085 avec [KB4493441)](https://support.microsoft.com/help/4493441/windows-10-update-kb4493441)ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1d18a-157">Windows 10, version 1709 (OS Build 16299.1085 with [KB4493441](https://support.microsoft.com/help/4493441/windows-10-update-kb4493441)) or later</span></span>
- <span data-ttu-id="1d18a-158">Windows 10, version 1803 (os build 17134.704 avec [KB4493464)](https://support.microsoft.com/help/4493464/windows-10-update-kb4493464)ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1d18a-158">Windows 10, version 1803 (OS Build 17134.704 with [KB4493464](https://support.microsoft.com/help/4493464/windows-10-update-kb4493464)) or later</span></span>
- <span data-ttu-id="1d18a-159">Windows 10, version [1803 ou](/windows/release-information/status-windows-10-1809-and-windows-server-2019) ultérieure</span><span class="sxs-lookup"><span data-stu-id="1d18a-159">Windows 10, version [1803](/windows/release-information/status-windows-10-1809-and-windows-server-2019) or later</span></span>

## <a name="next-steps"></a><span data-ttu-id="1d18a-160">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="1d18a-160">Next steps</span></span>

- [<span data-ttu-id="1d18a-161">En savoir plus sur les niveaux d’automatisation</span><span class="sxs-lookup"><span data-stu-id="1d18a-161">Learn more about automation levels</span></span>](automation-levels.md)
- [<span data-ttu-id="1d18a-162">Consultez le guide interactif : Examiner et corriger les menaces avec Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="1d18a-162">See the interactive guide: Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
- [<span data-ttu-id="1d18a-163">Configurer les fonctionnalités automatisées d’examen et de correction dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d18a-163">Configure automated investigation and remediation capabilities in Microsoft Defender for Endpoint</span></span>](configure-automated-investigations-remediation.md)

## <a name="see-also"></a><span data-ttu-id="1d18a-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d18a-164">See also</span></span>

- [<span data-ttu-id="1d18a-165">Protection PUA</span><span class="sxs-lookup"><span data-stu-id="1d18a-165">PUA protection</span></span>](/windows/security/threat-protection/microsoft-defender-antivirus/detect-block-potentially-unwanted-apps-microsoft-defender-antivirus)
- [<span data-ttu-id="1d18a-166">Examen et réponse automatisés dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1d18a-166">Automated investigation and response in Microsoft Defender for Office 365</span></span>](/microsoft-365/security/office-365-security/office-365-air)
- [<span data-ttu-id="1d18a-167">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1d18a-167">Automated investigation and response in Microsoft 365 Defender</span></span>](/microsoft-365/security/defender/mtp-autoir)
