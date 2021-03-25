---
title: Créer des indicateurs
ms.reviewer: ''
description: Créez des indicateurs pour un hachage de fichier, une adresse IP, des URL ou des domaines qui définissent la détection, la prévention et l’exclusion des entités.
keywords: gérer, autorisé, bloqué, bloquer, nettoyer, malveillant, hachage de fichier, adresse IP, url, domaine
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
ms.openlocfilehash: a04f3be1f13fb57cd76cda7115d014f2ba3aa8d6
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51198824"
---
# <a name="create-indicators"></a><span data-ttu-id="1ee1c-104">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="1ee1c-104">Create indicators</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1ee1c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1ee1c-105">**Applies to:**</span></span>
- [<span data-ttu-id="1ee1c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1ee1c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1ee1c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1ee1c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> [!TIP]
> <span data-ttu-id="1ee1c-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1ee1c-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1ee1c-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)

<span data-ttu-id="1ee1c-110">L’indicateur de compromission (IoCs) est une fonctionnalité essentielle dans chaque solution de protection des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-110">Indicator of compromise (IoCs) matching is an essential feature in every endpoint protection solution.</span></span> <span data-ttu-id="1ee1c-111">Cette fonctionnalité permet à SecOps de définir une liste d’indicateurs pour la détection et le blocage (prévention et réponse).</span><span class="sxs-lookup"><span data-stu-id="1ee1c-111">This capability gives SecOps the ability to set a list of indicators for detection and for blocking (prevention and response).</span></span>

<span data-ttu-id="1ee1c-112">Créez des indicateurs qui définissent la détection, la prévention et l’exclusion des entités.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-112">Create indicators that define the detection, prevention, and exclusion of entities.</span></span> <span data-ttu-id="1ee1c-113">Vous pouvez définir l’action à prendre, ainsi que la durée de l’application de l’action, ainsi que l’étendue du groupe d’appareils à appliquer.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-113">You can define the action to be taken as well as the duration for when to apply the action as well as the scope of the device group to apply it to.</span></span>

<span data-ttu-id="1ee1c-114">Les sources actuellement pris en charge sont le moteur de détection cloud de Defender pour Endpoint, le moteur d’examen et de correction automatisé et le moteur de prévention des points de terminaison (Antivirus Microsoft Defender).</span><span class="sxs-lookup"><span data-stu-id="1ee1c-114">Currently supported sources are the cloud detection engine of Defender for Endpoint, the automated investigation and remediation engine, and the endpoint prevention engine (Microsoft Defender Antivirus).</span></span>

<span data-ttu-id="1ee1c-115">**Moteur de détection cloud**</span><span class="sxs-lookup"><span data-stu-id="1ee1c-115">**Cloud detection engine**</span></span><br>
<span data-ttu-id="1ee1c-116">Le moteur de détection cloud de Defender for Endpoint analyse régulièrement les données collectées et tente de correspondre aux indicateurs que vous avez définies.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-116">The cloud detection engine of Defender for Endpoint regularly scans collected data and tries to match the indicators you set.</span></span> <span data-ttu-id="1ee1c-117">En cas de correspondance, une action est prise en fonction des paramètres que vous avez spécifiés pour l’IoC.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-117">When there is a match, action will be taken according to the settings you specified for the IoC.</span></span>

<span data-ttu-id="1ee1c-118">**Moteur de prévention des points de terminaison**</span><span class="sxs-lookup"><span data-stu-id="1ee1c-118">**Endpoint prevention engine**</span></span><br>
<span data-ttu-id="1ee1c-119">La même liste d’indicateurs est honorée par l’agent de prévention.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-119">The same list of indicators is honored by the prevention agent.</span></span> <span data-ttu-id="1ee1c-120">Autrement dit, si Microsoft Defender AV est le principal antivirus configuré, les indicateurs de correspondance seront traités en fonction des paramètres.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-120">Meaning, if Microsoft Defender AV is the primary AV configured, the matched indicators will be treated according to the settings.</span></span> <span data-ttu-id="1ee1c-121">Par exemple, si l’action est « Alerte et bloquer », Microsoft Defender AV empêche les exécutions de fichiers (bloquer et corriger) et une alerte correspondante est élevée.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-121">For example, if the action is "Alert and Block", Microsoft Defender AV will prevent file executions (block and remediate) and a corresponding alert will be raised.</span></span> <span data-ttu-id="1ee1c-122">En revanche, si l’action est définie sur « Autoriser », l’Antivirus Microsoft Defender ne détecte pas et ne bloque pas l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-122">On the other hand, if the Action is set to "Allow", Microsoft Defender AV will not detect nor block the file from being run.</span></span>

<span data-ttu-id="1ee1c-123">**Moteur d’examen et de correction automatisé**</span><span class="sxs-lookup"><span data-stu-id="1ee1c-123">**Automated investigation and remediation engine**</span></span><BR>
<span data-ttu-id="1ee1c-124">L’examen et la correction automatisés se comportent de la même manière.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-124">The automated investigation and remediation behave the same.</span></span> <span data-ttu-id="1ee1c-125">Si un indicateur est définie sur « Autoriser », l’examen et la correction automatisés ignorent un verdict « mauvais » pour lui.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-125">If an indicator is set to "Allow", Automated investigation and remediation will ignore a "bad" verdict for it.</span></span> <span data-ttu-id="1ee1c-126">S’il est définie sur « Bloquer », les examens et corrections automatisés le traitent comme « mauvais ».</span><span class="sxs-lookup"><span data-stu-id="1ee1c-126">If set to "Block", Automated investigation and remediation will treat it as "bad".</span></span>


<span data-ttu-id="1ee1c-127">Les actions actuellement prises en charge sont :</span><span class="sxs-lookup"><span data-stu-id="1ee1c-127">The current supported actions are:</span></span>
- <span data-ttu-id="1ee1c-128">Autoriser</span><span class="sxs-lookup"><span data-stu-id="1ee1c-128">Allow</span></span>
- <span data-ttu-id="1ee1c-129">Alerte uniquement</span><span class="sxs-lookup"><span data-stu-id="1ee1c-129">Alert only</span></span>
- <span data-ttu-id="1ee1c-130">Alerte et blocage</span><span class="sxs-lookup"><span data-stu-id="1ee1c-130">Alert and block</span></span>


<span data-ttu-id="1ee1c-131">Vous pouvez créer un indicateur pour :</span><span class="sxs-lookup"><span data-stu-id="1ee1c-131">You can create an indicator for:</span></span>
- [<span data-ttu-id="1ee1c-132">Files</span><span class="sxs-lookup"><span data-stu-id="1ee1c-132">Files</span></span>](indicator-file.md)
- [<span data-ttu-id="1ee1c-133">Adresses IP, URL/domaines</span><span class="sxs-lookup"><span data-stu-id="1ee1c-133">IP addresses, URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="1ee1c-134">Certificats</span><span class="sxs-lookup"><span data-stu-id="1ee1c-134">Certificates</span></span>](indicator-certificates.md)


> [!NOTE]
> <span data-ttu-id="1ee1c-135">Il existe une limite de 15 000 indicateurs par client.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-135">There is a limit of 15,000 indicators per tenant.</span></span> <span data-ttu-id="1ee1c-136">Les indicateurs de fichier et de certificat ne bloquent pas les [exclusions définies pour l’Antivirus Microsoft Defender.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-exclusions-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="1ee1c-136">File and certificate indicators do not block [exclusions defined for Microsoft Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-exclusions-microsoft-defender-antivirus).</span></span> <span data-ttu-id="1ee1c-137">Les indicateurs ne sont pas pris en charge dans l’Antivirus Microsoft Defender en mode passif.</span><span class="sxs-lookup"><span data-stu-id="1ee1c-137">Indicators are not supported in Microsoft Defender Antivirus is in passive mode.</span></span> 


## <a name="related-topics"></a><span data-ttu-id="1ee1c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ee1c-138">Related topics</span></span>

- [<span data-ttu-id="1ee1c-139">Créer un IoC contextuel</span><span class="sxs-lookup"><span data-stu-id="1ee1c-139">Create contextual IoC</span></span>](respond-file-alerts.md#add-indicator-to-block-or-allow-a-file)
- [<span data-ttu-id="1ee1c-140">Utiliser l’API d’indicateurs microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="1ee1c-140">Use the Microsoft Defender for Endpoint indicators API</span></span>](ti-indicator.md)
- [<span data-ttu-id="1ee1c-141">Utiliser des solutions intégrées par des partenaires</span><span class="sxs-lookup"><span data-stu-id="1ee1c-141">Use partner integrated solutions</span></span>](partner-applications.md)
