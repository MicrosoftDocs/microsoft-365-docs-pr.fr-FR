---
title: Bloquer des applications potentiellement indésirables avec l’Antivirus Microsoft Defender
description: Activer la fonctionnalité antivirus de l’application de protection contre les applications potentiellement indésirables (PUA) pour bloquer des logiciels non souhaités tels qu’un logiciel de publicité.
keywords: applications potentiellement indésirables (pua), activer, logiciel non souhaité, applications indésirables, logiciel de publicité, barre d’outils du navigateur, détecter, bloquer, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: detect
ms.sitesec: library
localization_priority: Priority
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
audience: ITPro
ms.reviewer: mimilone, julih
manager: dansimp
ms.technology: mde
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: d7f411c81e839d3929d4aa1a52fda29399c59dca
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772376"
---
# <a name="detect-and-block-potentially-unwanted-applications"></a><span data-ttu-id="39083-104">Détecter et bloquer des applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="39083-104">Detect and block potentially unwanted applications</span></span>

<span data-ttu-id="39083-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="39083-105">**Applies to:**</span></span>

- [<span data-ttu-id="39083-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="39083-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- [<span data-ttu-id="39083-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="39083-107">Microsoft Edge</span></span>](/microsoft-edge/deploy/microsoft-edge)

<span data-ttu-id="39083-108">Les applications potentiellement indésirables (PUA) est une catégorie de logiciel qui peut amener votre ordinateur à fonctionner lentement, afficher des publicités inattendues ou, au pire, installer un autre programme pouvant être imprévu ou non souhaité.</span><span class="sxs-lookup"><span data-stu-id="39083-108">Potentially unwanted applications (PUA) are a category of software that can cause your machine to run slowly, display unexpected ads, or at worst, install other software that might be unexpected or unwanted.</span></span> <span data-ttu-id="39083-109">Les applications potentiellement indésirables (PUA) ne sont pas considérées comme des virus, des programmes malveillants ou d’autres types de menace, mais elles peuvent effectuer des actions sur les points de terminaison qui affectent négativement l’utilisation ou les performances des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="39083-109">PUA is not considered a virus, malware, or other type of threat, but it might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="39083-110">Le terme *PUA* peut également faire référence à une application ayant une réputation médiocre, tel qu’évalué par Microsoft Defender pour point de terminaison, en raison de types de comportement indésirables.</span><span class="sxs-lookup"><span data-stu-id="39083-110">The term *PUA* can also refer to an application that has a poor reputation, as assessed by Microsoft Defender for Endpoint, due to certain kinds of undesirable behavior.</span></span>

<span data-ttu-id="39083-111">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="39083-111">Here are some examples:</span></span>

- <span data-ttu-id="39083-112">**Logiciel de publicité** qui affiche des publicités ou des promotions, notamment le programme qui insert des publicités sur des pages web.</span><span class="sxs-lookup"><span data-stu-id="39083-112">**Advertising software** that displays advertisements or promotions, including software that inserts advertisements to webpages.</span></span>
- <span data-ttu-id="39083-113">**Logiciel de regroupement** qui propose d’installer un autre programme qui n’est pas signé numériquement par la même entité.</span><span class="sxs-lookup"><span data-stu-id="39083-113">**Bundling software** that offers to install other software that is not digitally signed by the same entity.</span></span> <span data-ttu-id="39083-114">En outre, un logiciel qui propose d’installer un autre programme qui est considéré comme application potentiellement indésirable.</span><span class="sxs-lookup"><span data-stu-id="39083-114">Also, software that offers to install other software that qualifies as PUA.</span></span>
- <span data-ttu-id="39083-115">**Logiciel type évasion** qui tente de manière active d’éviter la détection par les produits de sécurité, y compris le programme qui agit différemment en présence de produits de sécurité.</span><span class="sxs-lookup"><span data-stu-id="39083-115">**Evasion software** that actively tries to evade detection by security products, including software that behaves differently in the presence of security products.</span></span>

> [!TIP]
> <span data-ttu-id="39083-116">Pour d’autres exemples et une discussion sur les critères que nous utilisons pour étiqueter des applications auxquelles il convient que les fonctionnalités de sécurité accordent une attention particulière, voir [Comment Microsoft identifie les programmes malveillants et les applications potentiellement indésirables](/windows/security/threat-protection/intelligence/criteria).</span><span class="sxs-lookup"><span data-stu-id="39083-116">For more examples and a discussion of the criteria we use to label applications for special attention from security features, see [How Microsoft identifies malware and potentially unwanted applications](/windows/security/threat-protection/intelligence/criteria).</span></span>

<span data-ttu-id="39083-117">Les applications potentiellement indésirables peuvent augmenter le risque que votre réseau soit infecté par un vrai programme malveillant, rendre les infections de programme malveillant plus difficiles à détecter ou gaspiller des ressources informatiques pour les nettoyer.</span><span class="sxs-lookup"><span data-stu-id="39083-117">Potentially unwanted applications can increase the risk of your network being infected with actual malware, make malware infections harder to identify, or waste IT resources in cleaning them up.</span></span> <span data-ttu-id="39083-118">La protection contre les applications potentiellement indésirables est prise en charge sur Windows 10, Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="39083-118">PUA protection is supported on Windows 10, Windows Server 2019, and Windows Server 2016.</span></span> <span data-ttu-id="39083-119">Dans Windows 10 (version 2004 et ultérieure), l’Antivirus Microsoft Defender bloque les applications considérées par défaut comme applications potentiellement indésirables pour les appareils Entreprise (E5).</span><span class="sxs-lookup"><span data-stu-id="39083-119">In Windows 10 (version 2004 and later), Microsoft Defender Antivirus blocks apps that are considered PUA for Enterprise (E5) devices by default.</span></span>

## <a name="microsoft-edge"></a><span data-ttu-id="39083-120">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="39083-120">Microsoft Edge</span></span>

<span data-ttu-id="39083-121">Le [nouveau Microsoft Edge](https://support.microsoft.com/microsoft-edge/get-to-know-microsoft-edge-3f4bb0ff-58de-2188-55c0-f560b7e20bea), qui est basé sur Chromium, bloque les téléchargements d’applications potentiellement indésirables et les URL de ressources associées.</span><span class="sxs-lookup"><span data-stu-id="39083-121">The [new Microsoft Edge](https://support.microsoft.com/microsoft-edge/get-to-know-microsoft-edge-3f4bb0ff-58de-2188-55c0-f560b7e20bea), which is Chromium-based, blocks potentially unwanted application downloads and associated resource URLs.</span></span> <span data-ttu-id="39083-122">Cette fonctionnalité est proposée par [Microsoft Defender SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview).</span><span class="sxs-lookup"><span data-stu-id="39083-122">This feature is provided via [Microsoft Defender SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview).</span></span>

### <a name="enable-pua-protection-in-chromium-based-microsoft-edge"></a><span data-ttu-id="39083-123">Activer la protection contre les applications potentiellement indésirables dans Microsoft Edge basé sur Chromium</span><span class="sxs-lookup"><span data-stu-id="39083-123">Enable PUA protection in Chromium-based Microsoft Edge</span></span>

<span data-ttu-id="39083-124">Bien que la protection contre les applications potentiellement indésirables dans Microsoft Edge (basé sur Chromium, version 80.0.361.50) soit désactivée par défaut, vous pouvez facilement l’activer dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="39083-124">Although potentially unwanted application protection in Microsoft Edge (Chromium-based, version 80.0.361.50) is turned off by default, it can easily be turned on from within the browser.</span></span>

1. <span data-ttu-id="39083-125">Dans votre navigateur Microsoft Edge, sélectionnez les ellipses, puis choisissez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="39083-125">In your Edge browser, select the ellipses, and then choose **Settings**.</span></span>

2. <span data-ttu-id="39083-126">Sélectionnez **Confidentialité, recherche et services**.</span><span class="sxs-lookup"><span data-stu-id="39083-126">Select **Privacy, search, and services**.</span></span>

3. <span data-ttu-id="39083-127">Sous la section **Sécurité**, activez **Bloquer les applications potentiellement indésirables**.</span><span class="sxs-lookup"><span data-stu-id="39083-127">Under the **Security** section, turn on **Block potentially unwanted apps**.</span></span>

> [!TIP]
> <span data-ttu-id="39083-128">Si vous exécutez Microsoft Edge (basé sur Chromium), vous pouvez explorer en toute sécurité la fonctionnalité de blocage d’URL de la protection contre les applications potentiellement indésirables en la testant sur l’une de nos [pages de démonstration Microsoft Defender SmartScreen](https://demo.smartscreen.msft.net/).</span><span class="sxs-lookup"><span data-stu-id="39083-128">If you are running Microsoft Edge (Chromium-based), you can safely explore the URL-blocking feature of PUA protection by testing it out on one of our [Microsoft Defender SmartScreen demo pages](https://demo.smartscreen.msft.net/).</span></span>

### <a name="block-urls-with-microsoft-defender-smartscreen"></a><span data-ttu-id="39083-129">Bloquer les URL avec Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="39083-129">Block URLs with Microsoft Defender SmartScreen</span></span>

<span data-ttu-id="39083-130">Dans Microsoft Edge basé sur Chromium avec la protection contre les applications potentiellement indésirables activée, Microsoft Defender SmartScreen vous protège contre les URL associées aux applications potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="39083-130">In Chromium-based Edge with PUA protection turned on, Microsoft Defender SmartScreen protects you from PUA-associated URLs.</span></span>

<span data-ttu-id="39083-131">Les administrateurs de sécurité peuvent [configurer](/DeployEdge/configure-microsoft-edge) comment Microsoft Edge et Microsoft Defender SmartScreen travaillent ensemble pour protéger des groupes d’utilisateurs contre des URL associées aux applications potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="39083-131">Security admins can [configure](/DeployEdge/configure-microsoft-edge) how Microsoft Edge and Microsoft Defender SmartScreen work together to protect groups of users from PUA-associated URLs.</span></span> <span data-ttu-id="39083-132">Il existe plusieurs [paramètres de stratégie de groupe](/DeployEdge/microsoft-edge-policies#smartscreen-settings) explicitement disponibles pour Microsoft Defender SmartScreen, notamment [une bloquant les applications potentiellement indésirables](/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled).</span><span class="sxs-lookup"><span data-stu-id="39083-132">There are several [group policy settings](/DeployEdge/microsoft-edge-policies#smartscreen-settings) explicitly for Microsoft Defender SmartScreen available, including [one for blocking PUA](/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled).</span></span> <span data-ttu-id="39083-133">En outre, les administrateurs peuvent [configurer Microsoft Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen) dans son ensemble, en utilisant les paramètres de stratégie de groupe pour activer ou désactiver Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="39083-133">In addition, admins can [configure Microsoft Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen) as a whole, using group policy settings to turn Microsoft Defender SmartScreen on or off.</span></span>

<span data-ttu-id="39083-134">Bien que Microsoft Defender pour point de terminaison ait sa propre liste de blocage basée sur un jeu de données gérées par Microsoft, vous pouvez personnaliser cette liste en fonction de votre propre veille contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="39083-134">Although Microsoft Defender for Endpoint has its own blocklist based upon a data set managed by Microsoft, you can customize this list based on your own threat intelligence.</span></span> <span data-ttu-id="39083-135">Si vous [créez et gérez des indicateurs](manage-indicators.md) dans le portail Microsoft Defender pour point de terminaison, Microsoft Defender SmartScreen respecte les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="39083-135">If you [create and manage indicators](manage-indicators.md) in the Microsoft Defender for Endpoint portal, Microsoft Defender SmartScreen respects the new settings.</span></span>

## <a name="microsoft-defender-antivirus-and-pua-protection"></a><span data-ttu-id="39083-136">Antivirus Microsoft Defender et la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-136">Microsoft Defender Antivirus and PUA protection</span></span>

<span data-ttu-id="39083-137">La fonctionnalité de protection contre les applications potentiellement indésirables (PUA) dans l’Antivirus Microsoft Defender peut détecter et bloquer les applications potentiellement indésirables (PUA) sur les points de terminaison dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="39083-137">The potentially unwanted application (PUA) protection feature in Microsoft Defender Antivirus can detect and block PUA on endpoints in your network.</span></span>

> [!NOTE]
> <span data-ttu-id="39083-138">Cette fonctionnalité est disponible dans Windows 10, Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="39083-138">This feature is available in Windows 10, Windows Server 2019, and Windows Server 2016.</span></span>

<span data-ttu-id="39083-139">L’Antivirus Microsoft Defender bloque les fichiers détectés d’applications potentiellement indésirables (PUA) et toutes les tentatives pour les télécharger, déplacer, exécuter ou installer.</span><span class="sxs-lookup"><span data-stu-id="39083-139">Microsoft Defender Antivirus blocks detected PUA files and any attempts to download, move, run, or install them.</span></span> <span data-ttu-id="39083-140">Les fichiers d’applications potentiellement indésirables (PUA) sont ensuite déplacés vers la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="39083-140">Blocked PUA files are then moved to quarantine.</span></span> <span data-ttu-id="39083-141">Lorsqu’un fichier d’applications potentiellement indésirables (PUA) est détecté sur un point de terminaison, l’Antivirus Microsoft Defender envoie une notification à l’utilisateur ([sauf si les notifications sont désactivées](configure-notifications-microsoft-defender-antivirus.md)) dans le même format que les autres détections de menaces.</span><span class="sxs-lookup"><span data-stu-id="39083-141">When a PUA file is detected on an endpoint, Microsoft Defender Antivirus sends a notification to the user ([unless notifications have been disabled](configure-notifications-microsoft-defender-antivirus.md)) in the same format as other threat detections.</span></span> <span data-ttu-id="39083-142">La notification est précédée par `PUA:` pour indiquer son contenu.</span><span class="sxs-lookup"><span data-stu-id="39083-142">The notification is prefaced with `PUA:` to indicate its content.</span></span>

<span data-ttu-id="39083-143">La notification s’affiche dans [la liste de quarantaine dans l’application Sécurité Windows](microsoft-defender-security-center-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="39083-143">The notification appears in the usual [quarantine list within the Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>

## <a name="configure-pua-protection-in-microsoft-defender-antivirus"></a><span data-ttu-id="39083-144">Configurer la protection contre les applications potentiellement indésirables (PUA) dans l’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="39083-144">Configure PUA protection in Microsoft Defender Antivirus</span></span>

<span data-ttu-id="39083-145">Vous pouvez activer la protection contre les applications potentiellement indésirables (PUA) avec [Microsoft Intune](/mem/intune/protect/device-protect), [Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection), [la stratégie de groupe](/azure/active-directory-domain-services/manage-group-policy) ou via les [cmdlets PowerShell](/powershell/module/defender/?preserve-view=true&view=win10-ps).</span><span class="sxs-lookup"><span data-stu-id="39083-145">You can enable PUA protection with [Microsoft Intune](/mem/intune/protect/device-protect), [Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection), [Group Policy](/azure/active-directory-domain-services/manage-group-policy), or via [PowerShell cmdlets](/powershell/module/defender/?preserve-view=true&view=win10-ps).</span></span>

<span data-ttu-id="39083-146">Vous pouvez également utiliser la protection contre les applications potentiellement indésirables (PUA) dans le mode audit pour détecter les applications potentiellement indésirables (PUA) sans les bloquer.</span><span class="sxs-lookup"><span data-stu-id="39083-146">You can also use PUA protection in audit mode to detect potentially unwanted applications without blocking them.</span></span> <span data-ttu-id="39083-147">Les détections sont capturées dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="39083-147">The detections are captured in the Windows event log.</span></span>

> [!TIP]
> <span data-ttu-id="39083-148">Visitez le site web de démonstration Microsoft Defender pour point de terminaison sur [demo.wd.microsoft.com](https://demo.wd.microsoft.com/Page/UrlRep) pour vérifier que la fonctionnalité est opérationnelle et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="39083-148">Visit the Microsoft Defender for Endpoint demo website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com/Page/UrlRep) to confirm that the feature is working, and see it in action.</span></span>

<span data-ttu-id="39083-149">La protection contre les applications potentiellement indésirables (PUA) dans le mode audit est utile si votre entreprise effectue une vérification de la conformité en matière de sécurité d’un logiciel interne et vous voulez éviter tout faux positif.</span><span class="sxs-lookup"><span data-stu-id="39083-149">PUA protection in audit mode is useful if your company is conducting an internal software security compliance check and you'd like to avoid any false positives.</span></span>

### <a name="use-intune-to-configure-pua-protection"></a><span data-ttu-id="39083-150">Utiliser Intune pour configurer la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-150">Use Intune to configure PUA protection</span></span>

<span data-ttu-id="39083-151">Consultez [Configurer des paramètres de restriction d’appareils dans Microsoft Intune](/intune/device-restrictions-configure) et [Paramètres de restriction d’appareil de l’Antivirus Microsoft Defender pour Windows 10](/intune/device-restrictions-windows-10#microsoft-defender-antivirus) pour obtenir des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="39083-151">See [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure) and [Microsoft Defender Antivirus device restriction settings for Windows 10 in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus) for more details.</span></span>

### <a name="use-configuration-manager-to-configure-pua-protection"></a><span data-ttu-id="39083-152">Utiliser Configuration Manager pour configurer la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-152">Use Configuration Manager to configure PUA protection</span></span>

<span data-ttu-id="39083-153">La protection contre les applications potentiellement indésirables (PUA) est activée par défaut dans Microsoft Endpoint Manager (branche actuelle).</span><span class="sxs-lookup"><span data-stu-id="39083-153">PUA protection is enabled by default in the Microsoft Endpoint Manager (Current Branch).</span></span>

<span data-ttu-id="39083-154">Voir [Comment créer et déployer des stratégies de logiciel anti-programme malveillant : paramètres d’analyses planifiées](/configmgr/protect/deploy-use/endpoint-antimalware-policies#real-time-protection-settings) pour obtenir des détails sur la configuration de Microsoft Endpoint Manager (branche actuelle).</span><span class="sxs-lookup"><span data-stu-id="39083-154">See [How to create and deploy antimalware policies: Scheduled scans settings](/configmgr/protect/deploy-use/endpoint-antimalware-policies#real-time-protection-settings) for details on configuring Microsoft Endpoint Manager (Current Branch).</span></span>

<span data-ttu-id="39083-155">Pour System Center 2012 Configuration Manager, voir [Comment déployer la stratégie de protection contre les applications potentiellement indésirables (PUA) pour Endpoint protection dans Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#BKMK_PUA).</span><span class="sxs-lookup"><span data-stu-id="39083-155">For System Center 2012 Configuration Manager, see [How to Deploy Potentially Unwanted Application Protection Policy for Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#BKMK_PUA).</span></span>

> [!NOTE]
> <span data-ttu-id="39083-156">Les événements d’applications potentiellement indésirables (PUA) bloqués par l’Antivirus Microsoft Defender sont signalés dans l’Observateur d'événements Windows et non dans Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="39083-156">PUA events blocked by Microsoft Defender Antivirus are reported in the Windows Event Viewer and not in Microsoft Endpoint Configuration Manager.</span></span>

### <a name="use-group-policy-to-configure-pua-protection"></a><span data-ttu-id="39083-157">Utiliser la stratégie de groupe pour configurer la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-157">Use Group Policy to configure PUA protection</span></span>

1. <span data-ttu-id="39083-158">Télécharger et installer [Modèles d’administration (.admx) pour Windows 10, mise à jour d’octobre 2020 (20H2)](https://www.microsoft.com/download/details.aspx?id=102157).</span><span class="sxs-lookup"><span data-stu-id="39083-158">Download and install [Administrative Templates (.admx) for Windows 10 October 2020 Update (20H2)](https://www.microsoft.com/download/details.aspx?id=102157)</span></span>

2. <span data-ttu-id="39083-159">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la[Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="39083-159">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

3. <span data-ttu-id="39083-160">Sélectionnez l’objet de stratégie de groupe que vous souhaitez configurer, puis choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="39083-160">Select the Group Policy Object you want to configure, and then choose **Edit**.</span></span>

4. <span data-ttu-id="39083-161">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="39083-161">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

5. <span data-ttu-id="39083-162">Développez l’arborescence sur **Composants Windows** > **Antivirus Microsoft Defender**.</span><span class="sxs-lookup"><span data-stu-id="39083-162">Expand the tree to **Windows Components** > **Microsoft Defender Antivirus**.</span></span>

6. <span data-ttu-id="39083-163">Cliquez deux fois sur **Configurer la détection pour les applications potentiellement indésirables (PUA)**.</span><span class="sxs-lookup"><span data-stu-id="39083-163">Double-click **Configure detection for potentially unwanted applications**.</span></span>

7. <span data-ttu-id="39083-164">Sélectionnez **Activé** pour activer la protection contre les applications potentiellement indésirables (PUA).</span><span class="sxs-lookup"><span data-stu-id="39083-164">Select **Enabled** to enable PUA protection.</span></span>

8. <span data-ttu-id="39083-165">Dans **Options**, sélectionnez **Bloquer** pour bloquer les applications potentiellement indésirables ou **Mode Audit** pour tester le fonctionnement du setting dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="39083-165">In **Options**, select **Block** to block potentially unwanted applications, or select **Audit Mode** to test how the setting works in your environment.</span></span> <span data-ttu-id="39083-166">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="39083-166">Select **OK**.</span></span>

9. <span data-ttu-id="39083-167">Déployez votre objet de stratégie de groupe comme vous le faites habituellement.</span><span class="sxs-lookup"><span data-stu-id="39083-167">Deploy your Group Policy object as you usually do.</span></span>

### <a name="use-powershell-cmdlets-to-configure-pua-protection"></a><span data-ttu-id="39083-168">Utiliser les cmdlets PowerShell pour configurer la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-168">Use PowerShell cmdlets to configure PUA protection</span></span>

#### <a name="to-enable-pua-protection"></a><span data-ttu-id="39083-169">Pour activer la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-169">To enable PUA protection</span></span>

```PowerShell
Set-MpPreference -PUAProtection Enabled
```

<span data-ttu-id="39083-170">La configuration de la valeur de cette cmdlet sur `Enabled` active la fonctionnalité si elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="39083-170">Setting the value for this cmdlet to `Enabled` turns on the feature if it has been disabled.</span></span>

#### <a name="to-set-pua-protection-to-audit-mode"></a><span data-ttu-id="39083-171">Définir la protection contre les applications potentiellement indésirables (PUA) sur le mode audit</span><span class="sxs-lookup"><span data-stu-id="39083-171">To set PUA protection to audit mode</span></span>

```PowerShell
Set-MpPreference -PUAProtection AuditMode
```

<span data-ttu-id="39083-172">La définition de `AuditMode` détecte les applications potentiellement indésirables (PUA) sans les bloquer.</span><span class="sxs-lookup"><span data-stu-id="39083-172">Setting `AuditMode` detects PUAs without blocking them.</span></span>

#### <a name="to-disable-pua-protection"></a><span data-ttu-id="39083-173">Pour désactiver la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-173">To disable PUA protection</span></span>

<span data-ttu-id="39083-174">Nous vous recommandons de maintenir la protection contre les applications potentiellement indésirables (PUA) activé.</span><span class="sxs-lookup"><span data-stu-id="39083-174">We recommend keeping PUA protection turned on.</span></span> <span data-ttu-id="39083-175">Toutefois, vous pouvez la désactiver en utilisant la cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="39083-175">However, you can turn it off by using the following cmdlet:</span></span>

```PowerShell
Set-MpPreference -PUAProtection Disabled
```

<span data-ttu-id="39083-176">La configuration de la valeur de cette cmdlet sur `Disabled` désactive la fonctionnalité si elle a été activée.</span><span class="sxs-lookup"><span data-stu-id="39083-176">Setting the value for this cmdlet to `Disabled` turns off the feature if it has been enabled.</span></span>

<span data-ttu-id="39083-177">Pour plus d’informations, voir [Utiliser les cmdlets PowerShell pour configurer et gérer l'Antivirus Microsoft Defender](use-powershell-cmdlets-microsoft-defender-antivirus.md) et [Cmdlets Defender](/powershell/module/defender/index).</span><span class="sxs-lookup"><span data-stu-id="39083-177">For more information, see [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/index).</span></span>

## <a name="view-pua-events-using-powershell"></a><span data-ttu-id="39083-178">Afficher les événements d’applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-178">View PUA events using PowerShell</span></span>

<span data-ttu-id="39083-179">Les événements d’applications potentiellement indésirables (PUA) sont signalés dans l’Observateur d'événements Windows, mais pas dans Microsoft Endpoint Manager ou Intune.</span><span class="sxs-lookup"><span data-stu-id="39083-179">PUA events are reported in the Windows Event Viewer, but not in Microsoft Endpoint Manager or in Intune.</span></span> <span data-ttu-id="39083-180">Vous pouvez également utiliser la cmdlet `Get-MpThreat` pour afficher les menaces traitées par l’Antivirus Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="39083-180">You can also use the `Get-MpThreat` cmdlet to view threats that Microsoft Defender Antivirus handled.</span></span> <span data-ttu-id="39083-181">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="39083-181">Here's an example:</span></span>

```console
CategoryID       : 27
DidThreatExecute : False
IsActive         : False
Resources        : {webfile:_q:\Builds\Dalton_Download_Manager_3223905758.exe|http://d18yzm5yb8map8.cloudfront.net/
                    fo4yue@kxqdw/Dalton_Download_Manager.exe|pid:14196,ProcessStart:132378130057195714}
RollupStatus     : 33
SchemaVersion    : 1.0.0.0
SeverityID       : 1
ThreatID         : 213927
ThreatName       : PUA:Win32/InstallCore
TypeID           : 0
PSComputerName   :
```

## <a name="get-email-notifications-about-pua-detections"></a><span data-ttu-id="39083-182">Obtenir des notifications par courrier électronique à propos des détections de la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-182">Get email notifications about PUA detections</span></span>

<span data-ttu-id="39083-183">Vous pouvez activer les notifications par -email pour recevoir le courrier à propos de la détection des applications potentiellement indésirables (PUA).</span><span class="sxs-lookup"><span data-stu-id="39083-183">You can turn on email notifications to receive mail about PUA detections.</span></span>

<span data-ttu-id="39083-184">Consultez [Résoudre des problèmes relatifs aux ID d’événement](troubleshoot-microsoft-defender-antivirus.md) pour plus de détails sur l’affichage des événements de l’Antivirus Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="39083-184">See [Troubleshoot event IDs](troubleshoot-microsoft-defender-antivirus.md) for details on viewing Microsoft Defender Antivirus events.</span></span> <span data-ttu-id="39083-185">Les événements des applications potentiellement indésirables (PUA) sont enregistrés sous l’ID d’événement **1160**.</span><span class="sxs-lookup"><span data-stu-id="39083-185">PUA events are recorded under event ID **1160**.</span></span>

## <a name="view-pua-events-using-advanced-hunting"></a><span data-ttu-id="39083-186">Afficher les événements des applications potentiellement indésirables (PUA) à l’aide du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="39083-186">View PUA events using advanced hunting</span></span>

<span data-ttu-id="39083-187">Si vous utilisez [Microsoft Defender pour point de terminaison](microsoft-defender-endpoint.md), vous pouvez utiliser une requête de repérage avancé pour afficher les événements des applications potentiellement indésirables (PUA).</span><span class="sxs-lookup"><span data-stu-id="39083-187">If you're using [Microsoft Defender for Endpoint](microsoft-defender-endpoint.md), you can use an advanced hunting query to view PUA events.</span></span> <span data-ttu-id="39083-188">Voici une requête d’exemple :</span><span class="sxs-lookup"><span data-stu-id="39083-188">Here's an example query:</span></span>

```console
DeviceEvents
| where ActionType == "AntivirusDetection"
| extend x = parse_json(AdditionalFields)
| project Timestamp, DeviceName, FolderPath, FileName, SHA256, ThreatName = tostring(x.ThreatName), WasExecutingWhileDetected = tostring(x.WasExecutingWhileDetected), WasRemediated = tostring(x.WasRemediated)
| where ThreatName startswith_cs 'PUA:'
```

<span data-ttu-id="39083-189">Pour en savoir plus sur le repérage avancé, voir [Repérer de manière proactive les menaces grâce au repérage avancé](advanced-hunting-overview.md).</span><span class="sxs-lookup"><span data-stu-id="39083-189">To learn more about advanced hunting, see [Proactively hunt for threats with advanced hunting](advanced-hunting-overview.md).</span></span>

## <a name="exclude-files-from-pua-protection"></a><span data-ttu-id="39083-190">Exclure des fichiers de la protection contre les applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="39083-190">Exclude files from PUA protection</span></span>

<span data-ttu-id="39083-191">Un fichier est parfois bloqué par erreur par la protection contre les applications potentiellement indésirables (PUA) ou une fonctionnalité d’une application potentiellement indésirable (PUA) est nécessaire pour effectuer une tâche.</span><span class="sxs-lookup"><span data-stu-id="39083-191">Sometimes a file is erroneously blocked by PUA protection, or a feature of a PUA is required to complete a task.</span></span> <span data-ttu-id="39083-192">Dans ces cas, un fichier peut être ajouté à une liste d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="39083-192">In these cases, a file can be added to an exclusion list.</span></span>

<span data-ttu-id="39083-193">Pour plus d’informations, voir [Configurer et valider des exclusions en fonction de l’extension de fichier et de l’emplacement du dossier](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="39083-193">For more information, see [Configure and validate exclusions based on file extension and folder location](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="39083-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39083-194">See also</span></span>

- [<span data-ttu-id="39083-195">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="39083-195">Next-generation protection</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="39083-196">Configurer la protection comportementale, heuristique et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="39083-196">Configure behavioral, heuristic, and real-time protection</span></span>](configure-protection-features-microsoft-defender-antivirus.md)