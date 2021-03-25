---
title: Déploiement avec un autre système de gestion des périphériques mobiles (MDM) pour Microsoft Defender ATP pour Mac
description: Installez Microsoft Defender ATP pour Mac sur d’autres solutions de gestion.
keywords: microsoft, defender, atp, mac, installation, deploy, macos,pérron, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: mavel
author: maximvelichko
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: e3a20f0a356a32eddc05b3792c0c04c23197a7b0
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185694"
---
# <a name="deployment-with-a-different-mobile-device-management-mdm-system-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="e7efd-104">Déploiement avec un autre système de gestion des périphériques mobiles (MDM) pour Microsoft Defender pour Endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="e7efd-104">Deployment with a different Mobile Device Management (MDM) system for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="e7efd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e7efd-105">**Applies to:**</span></span>
- [<span data-ttu-id="e7efd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e7efd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="e7efd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e7efd-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="e7efd-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="e7efd-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="e7efd-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e7efd-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)
 
## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="e7efd-110">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="e7efd-110">Prerequisites and system requirements</span></span>

<span data-ttu-id="e7efd-111">Avant de commencer, consultez la page principale de [Microsoft Defender pour Endpoint pour Mac](microsoft-defender-endpoint-mac.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7efd-111">Before you get started, see [the main Microsoft Defender for Endpoint for Mac page](microsoft-defender-endpoint-mac.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="approach"></a><span data-ttu-id="e7efd-112">Approche</span><span class="sxs-lookup"><span data-stu-id="e7efd-112">Approach</span></span>

> [!CAUTION]
> <span data-ttu-id="e7efd-113">Actuellement, Microsoft prend uniquement en charge Intune et JAMF pour le déploiement et la gestion de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="e7efd-113">Currently, Microsoft oficially supports only Intune and JAMF for the deployment and management of Microsoft Defender for Endpoint for Mac.</span></span> <span data-ttu-id="e7efd-114">Microsoft n’offre aucune garantie, expressément ou implicite, en ce qui concerne les informations fournies ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e7efd-114">Microsoft makes no warranties, express or implied, with respect to the information provided below.</span></span>

<span data-ttu-id="e7efd-115">Si votre organisation utilise une solution de gestion des périphériques mobiles (MDM) qui n’est pas officiellement prise en charge, cela ne signifie pas que vous ne pouvez pas déployer ou exécuter Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="e7efd-115">If your organization uses a Mobile Device Management (MDM) solution that is not officially supported, this does not mean you are unable to deploy or run Microsoft Defender for Endpoint for Mac.</span></span>

<span data-ttu-id="e7efd-116">Microsoft Defender pour point de terminaison pour Mac ne dépend d’aucune fonctionnalité propre au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e7efd-116">Microsoft Defender for Endpoint for Mac does not depend on any vendor-specific features.</span></span> <span data-ttu-id="e7efd-117">Il peut être utilisé avec n’importe quelle solution MDM qui prend en charge les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7efd-117">It can be used with any MDM solution that supports the following features:</span></span>

- <span data-ttu-id="e7efd-118">Déployez un .pkg macOS sur des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="e7efd-118">Deploy a macOS .pkg to managed devices.</span></span>
- <span data-ttu-id="e7efd-119">Déployez les profils de configuration système macOS sur les appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="e7efd-119">Deploy macOS system configuration profiles to managed devices.</span></span>
- <span data-ttu-id="e7efd-120">Exécutez un outil/script arbitraire configuré par l’administrateur sur des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="e7efd-120">Run an arbitrary admin-configured tool/script on managed devices.</span></span>

<span data-ttu-id="e7efd-121">La plupart des solutions mdm modernes incluent ces fonctionnalités, mais elles peuvent les appeler différemment.</span><span class="sxs-lookup"><span data-stu-id="e7efd-121">Most modern MDM solutions include these features, however, they may call them differently.</span></span>

<span data-ttu-id="e7efd-122">Toutefois, vous pouvez déployer Defender sans la dernière condition requise de la liste précédente :</span><span class="sxs-lookup"><span data-stu-id="e7efd-122">You can deploy Defender without the last requirement from the preceding list, however:</span></span>

- <span data-ttu-id="e7efd-123">Vous ne pourrez pas collecter l’état de manière centralisée</span><span class="sxs-lookup"><span data-stu-id="e7efd-123">You will not be able to collect status in a centralized way</span></span>
- <span data-ttu-id="e7efd-124">Si vous décidez de désinstaller Defender, vous devez vous connecter localement à l’appareil client en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e7efd-124">If you decide to uninstall Defender, you will need to log on to the client device locally as an administrator</span></span>

## <a name="deployment"></a><span data-ttu-id="e7efd-125">Déploiement</span><span class="sxs-lookup"><span data-stu-id="e7efd-125">Deployment</span></span>

<span data-ttu-id="e7efd-126">La plupart des solutions MDM utilisent le même modèle pour la gestion des appareils macOS, avec une terminologie similaire.</span><span class="sxs-lookup"><span data-stu-id="e7efd-126">Most MDM solutions use the same model for managing macOS devices, with similar terminology.</span></span> <span data-ttu-id="e7efd-127">Utilisez [un déploiement basé sur JAMF](mac-install-with-jamf.md) comme modèle.</span><span class="sxs-lookup"><span data-stu-id="e7efd-127">Use [JAMF-based deployment](mac-install-with-jamf.md) as a template.</span></span>

### <a name="package"></a><span data-ttu-id="e7efd-128">Package</span><span class="sxs-lookup"><span data-stu-id="e7efd-128">Package</span></span>

<span data-ttu-id="e7efd-129">Configurez le déploiement d’un [package d’application](mac-install-with-jamf.md)requis, avec le package d’installation (wdav.pkg) téléchargé à partir du Centre de sécurité [Microsoft Defender.](mac-install-with-jamf.md)</span><span class="sxs-lookup"><span data-stu-id="e7efd-129">Configure deployment of a [required application package](mac-install-with-jamf.md), with the installation package (wdav.pkg) downloaded from [Microsoft Defender Security Center](mac-install-with-jamf.md).</span></span>

<span data-ttu-id="e7efd-130">Pour déployer le package dans votre entreprise, utilisez les instructions associées à votre solution MDM.</span><span class="sxs-lookup"><span data-stu-id="e7efd-130">In order to deploy the package to your enterprise, use the instructions associated with your MDM solution.</span></span>

### <a name="license-settings"></a><span data-ttu-id="e7efd-131">Paramètres de licence</span><span class="sxs-lookup"><span data-stu-id="e7efd-131">License settings</span></span>

<span data-ttu-id="e7efd-132">Configurer un [profil de configuration système.](mac-install-with-jamf.md)</span><span class="sxs-lookup"><span data-stu-id="e7efd-132">Set up [a system configuration profile](mac-install-with-jamf.md).</span></span> <span data-ttu-id="e7efd-133">Votre solution MDM peut l’appeler « Profil de paramètres personnalisés », car Microsoft Defender pour Endpoint pour Mac ne fait pas partie de macOS.</span><span class="sxs-lookup"><span data-stu-id="e7efd-133">Your MDM solution may call it something like "Custom Settings Profile", as Microsoft Defender for Endpoint for Mac is not part of macOS.</span></span>

<span data-ttu-id="e7efd-134">Utilisez la liste des propriétés, jamf/WindowsDefenderATPOnboarding.plist, qui peut être extraite d’un package d’intégration téléchargé à partir du Centre de sécurité [Microsoft Defender.](mac-install-with-jamf.md)</span><span class="sxs-lookup"><span data-stu-id="e7efd-134">Use the property list, jamf/WindowsDefenderATPOnboarding.plist, which can be extracted from an onboarding package downloaded from [Microsoft Defender Security Center](mac-install-with-jamf.md).</span></span>
<span data-ttu-id="e7efd-135">Votre système peut prendre en charge une liste de propriétés arbitraire au format XML.</span><span class="sxs-lookup"><span data-stu-id="e7efd-135">Your system may support an arbitrary property list in XML format.</span></span> <span data-ttu-id="e7efd-136">Vous pouvez télécharger le fichier jamf/WindowsDefenderATPOnboarding.plist tel qu’il est dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="e7efd-136">You can upload the jamf/WindowsDefenderATPOnboarding.plist file as-is in that case.</span></span>
<span data-ttu-id="e7efd-137">Vous pouvez également avoir besoin de convertir d’abord la liste des propriétés dans un autre format.</span><span class="sxs-lookup"><span data-stu-id="e7efd-137">Alternatively, it may require you to convert the property list to a different format first.</span></span>

<span data-ttu-id="e7efd-138">En règle générale, votre profil personnalisé possède un ID, un nom ou un attribut de domaine.</span><span class="sxs-lookup"><span data-stu-id="e7efd-138">Typically, your custom profile has an ID, name, or domain attribute.</span></span> <span data-ttu-id="e7efd-139">Vous devez utiliser exactement « com.microsoft.wdav.atp » pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e7efd-139">You must use exactly "com.microsoft.wdav.atp" for this value.</span></span>
<span data-ttu-id="e7efd-140">GDM l’utilise pour déployer le fichier de paramètres dans **/Library/Managed Preferences/com.microsoft.wdav.atp.plist** sur un appareil client, et Defender utilise ce fichier pour charger les informations d’intégration.</span><span class="sxs-lookup"><span data-stu-id="e7efd-140">MDM uses it to deploy the settings file to **/Library/Managed Preferences/com.microsoft.wdav.atp.plist** on a client device, and Defender uses this file for loading the onboarding information.</span></span>

### <a name="kernel-extension-policy"></a><span data-ttu-id="e7efd-141">Stratégie d’extension du noyau</span><span class="sxs-lookup"><span data-stu-id="e7efd-141">Kernel extension policy</span></span>

<span data-ttu-id="e7efd-142">Configurer une stratégie KEXT ou d’extension de noyau.</span><span class="sxs-lookup"><span data-stu-id="e7efd-142">Set up a KEXT or kernel extension policy.</span></span> <span data-ttu-id="e7efd-143">Utilisez **l’identificateur d’équipe UBF8T346G9** pour autoriser les extensions de noyau fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e7efd-143">Use team identifier **UBF8T346G9** to allow kernel extensions provided by Microsoft.</span></span>

### <a name="system-extension-policy"></a><span data-ttu-id="e7efd-144">Stratégie d’extension système</span><span class="sxs-lookup"><span data-stu-id="e7efd-144">System extension policy</span></span>

<span data-ttu-id="e7efd-145">Configurer une stratégie d’extension système.</span><span class="sxs-lookup"><span data-stu-id="e7efd-145">Set up a system extension policy.</span></span> <span data-ttu-id="e7efd-146">Utilisez **l’identificateur d’équipe UBF8T346G9** et approuvez les identificateurs d’ensemble suivants :</span><span class="sxs-lookup"><span data-stu-id="e7efd-146">Use team identifier **UBF8T346G9** and approve the following bundle identifiers:</span></span>

- <span data-ttu-id="e7efd-147">com.microsoft.wdav.epsext</span><span class="sxs-lookup"><span data-stu-id="e7efd-147">com.microsoft.wdav.epsext</span></span>
- <span data-ttu-id="e7efd-148">com.microsoft.wdav.netext</span><span class="sxs-lookup"><span data-stu-id="e7efd-148">com.microsoft.wdav.netext</span></span>

### <a name="full-disk-access-policy"></a><span data-ttu-id="e7efd-149">Stratégie d’accès disque complet</span><span class="sxs-lookup"><span data-stu-id="e7efd-149">Full disk access policy</span></span>

<span data-ttu-id="e7efd-150">Accordez un accès disque total aux composants suivants :</span><span class="sxs-lookup"><span data-stu-id="e7efd-150">Grant Full Disk Access to the following components:</span></span>

- <span data-ttu-id="e7efd-151">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e7efd-151">Microsoft Defender for Endpoint</span></span>
    - <span data-ttu-id="e7efd-152">Identificateur : `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="e7efd-152">Identifier: `com.microsoft.wdav`</span></span>
    - <span data-ttu-id="e7efd-153">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="e7efd-153">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="e7efd-154">Conditions requises pour le code : `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="e7efd-154">Code Requirement: `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>

- <span data-ttu-id="e7efd-155">Microsoft Defender pour l’extension de sécurité de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e7efd-155">Microsoft Defender for Endpoint Security Extension</span></span>
    - <span data-ttu-id="e7efd-156">Identificateur : `com.microsoft.wdav.epsext`</span><span class="sxs-lookup"><span data-stu-id="e7efd-156">Identifier: `com.microsoft.wdav.epsext`</span></span>
    - <span data-ttu-id="e7efd-157">Type d’identificateur : ID d’offre groupée</span><span class="sxs-lookup"><span data-stu-id="e7efd-157">Identifier Type: Bundle ID</span></span>
    - <span data-ttu-id="e7efd-158">Conditions requises pour le code : `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="e7efd-158">Code Requirement: `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>

### <a name="network-extension-policy"></a><span data-ttu-id="e7efd-159">Stratégie d’extension réseau</span><span class="sxs-lookup"><span data-stu-id="e7efd-159">Network extension policy</span></span>

<span data-ttu-id="e7efd-160">Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender pour Endpoint pour Mac inspecte le trafic de socket et signale ces informations au portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e7efd-160">As part of the Endpoint Detection and Response capabilities, Microsoft Defender for Endpoint for Mac inspects socket traffic and reports this information to the Microsoft Defender Security Center portal.</span></span> <span data-ttu-id="e7efd-161">La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e7efd-161">The following policy allows the network extension to perform this functionality.</span></span>

- <span data-ttu-id="e7efd-162">Type de filtre : Plug-in</span><span class="sxs-lookup"><span data-stu-id="e7efd-162">Filter type: Plugin</span></span>
- <span data-ttu-id="e7efd-163">Identificateur de l’ensemble de plug-ins : `com.microsoft.wdav`</span><span class="sxs-lookup"><span data-stu-id="e7efd-163">Plugin bundle identifier: `com.microsoft.wdav`</span></span>
- <span data-ttu-id="e7efd-164">Identificateur d’ensemble du fournisseur de données de filtre : `com.microsoft.wdav.netext`</span><span class="sxs-lookup"><span data-stu-id="e7efd-164">Filter data provider bundle identifier: `com.microsoft.wdav.netext`</span></span>
- <span data-ttu-id="e7efd-165">Exigence désignée par le fournisseur de données de filtre : `identifier "com.microsoft.wdav.tunnelext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span><span class="sxs-lookup"><span data-stu-id="e7efd-165">Filter data provider designated requirement: `identifier "com.microsoft.wdav.tunnelext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`</span></span>
- <span data-ttu-id="e7efd-166">Filtrer les sockets : `true`</span><span class="sxs-lookup"><span data-stu-id="e7efd-166">Filter sockets: `true`</span></span>

## <a name="check-installation-status"></a><span data-ttu-id="e7efd-167">Vérifier l’état de l’installation</span><span class="sxs-lookup"><span data-stu-id="e7efd-167">Check installation status</span></span>

<span data-ttu-id="e7efd-168">Exécutez [Microsoft Defender pour le point de terminaison](mac-install-with-jamf.md) sur un appareil client pour vérifier l’état d’intégration.</span><span class="sxs-lookup"><span data-stu-id="e7efd-168">Run [Microsoft Defender for Endpoint](mac-install-with-jamf.md) on a client device to check the onboarding status.</span></span>
