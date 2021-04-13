---
title: Bloquer les applications potentiellement indésirables avec l'Antivirus Microsoft Defender
description: Activez la fonctionnalité antivirus d'application potentiellement indésirable (PUA) pour bloquer les logiciels indésirables tels que les logiciels adware.
keywords: pua, activer, logiciels indésirables, applications indésirables, logiciels publicitaires, barre d'outils du navigateur, détecter, bloquer, Antivirus Microsoft Defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: detect
ms.sitesec: library
ms.localizationpriority: high
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
audience: ITPro
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: bee92dfa998596578c27bda579a86776bc77c07b
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690717"
---
# <a name="detect-and-block-potentially-unwanted-applications"></a><span data-ttu-id="41330-104">Détecter et bloquer les applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="41330-104">Detect and block potentially unwanted applications</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="41330-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="41330-105">**Applies to:**</span></span>

- [<span data-ttu-id="41330-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="41330-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- [<span data-ttu-id="41330-107">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41330-107">Microsoft Edge</span></span>](/microsoft-edge/deploy/microsoft-edge)

> [!NOTE]
> <span data-ttu-id="41330-108">Les applications potentiellement indésirables (PUA) sont une catégorie de logiciels qui peuvent ralentir votre ordinateur, afficher des publicités inattendues ou, au pire, installer d'autres logiciels qui peuvent être inattendus ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="41330-108">Potentially unwanted applications (PUA) are a category of software that can cause your machine to run slowly, display unexpected ads, or at worst, install other software which might be unexpected or unwanted.</span></span> <span data-ttu-id="41330-109">Par défaut dans Windows 10 (version 2004 et ultérieures), l'Antivirus Microsoft Defender bloque les applications considérées comme PUA pour les appareils d'entreprise (E5).</span><span class="sxs-lookup"><span data-stu-id="41330-109">By default in Windows 10 (version 2004 and later), Microsoft Defender Antivirus blocks apps that are considered PUA, for Enterprise (E5) devices.</span></span>

<span data-ttu-id="41330-110">Les applications potentiellement indésirables (PUA) ne sont pas considérées comme des virus, des programmes malveillants ou d'autres types de menaces, mais elles peuvent effectuer des actions sur les points de terminaison qui affectent négativement les performances ou l'utilisation des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="41330-110">Potentially unwanted applications (PUA) are not considered viruses, malware, or other types of threats, but they might perform actions on endpoints which adversely affect endpoint performance or use.</span></span> <span data-ttu-id="41330-111">_PuA_ peut également faire référence à une application dont la réputation est médiocre, tel qu'évalué par Microsoft Defender for Endpoint, en raison de certains types de comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="41330-111">_PUA_ can also refer to an application that has a poor reputation, as assessed by Microsoft Defender for Endpoint, due to certain kinds of undesirable behavior.</span></span>

<span data-ttu-id="41330-112">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="41330-112">Here are some examples:</span></span>

- <span data-ttu-id="41330-113">**Logiciels publicitaires** qui affichent des publicités ou des promotions, y compris les logiciels qui insère des publicités dans des pages web.</span><span class="sxs-lookup"><span data-stu-id="41330-113">**Advertising software** that displays advertisements or promotions, including software that inserts advertisements to webpages.</span></span>
- <span data-ttu-id="41330-114">**Regroupement de logiciels** qui offrent l'installation d'autres logiciels qui ne sont pas signés numériquement par la même entité.</span><span class="sxs-lookup"><span data-stu-id="41330-114">**Bundling software** that offers to install other software that is not digitally signed by the same entity.</span></span> <span data-ttu-id="41330-115">En outre, les logiciels qui offrent d'installer d'autres logiciels éligibles en tant que PUA.</span><span class="sxs-lookup"><span data-stu-id="41330-115">Also, software that offers to install other software that qualify as PUA.</span></span>
- <span data-ttu-id="41330-116">**Logiciels de production** qui tentent activement d'éviter la détection par les produits de sécurité, y compris les logiciels qui se comportent différemment en présence des produits de sécurité.</span><span class="sxs-lookup"><span data-stu-id="41330-116">**Evasion software** that actively tries to evade detection by security products, including software that behaves differently in the presence of security products.</span></span>

> [!TIP]
> <span data-ttu-id="41330-117">Pour obtenir plus d'exemples et une discussion sur les critères que nous utilisons pour étiqueter les applications pour attirer une attention particulière des fonctionnalités de sécurité, voir Comment Microsoft identifie les programmes malveillants et [les applications potentiellement indésirables.](/windows/security/threat-protection/intelligence/criteria)</span><span class="sxs-lookup"><span data-stu-id="41330-117">For more examples and a discussion of the criteria we use to label applications for special attention from security features, see [How Microsoft identifies malware and potentially unwanted applications](/windows/security/threat-protection/intelligence/criteria).</span></span>

<span data-ttu-id="41330-118">Les applications potentiellement indésirables peuvent augmenter le risque que votre réseau soit infecté par des programmes malveillants réels, rendre l'identification des programmes malveillants plus difficile à identifier ou perdre des ressources informatiques lors de leur nettoyage.</span><span class="sxs-lookup"><span data-stu-id="41330-118">Potentially unwanted applications can increase the risk of your network being infected with actual malware, make malware infections harder to identify, or waste IT resources in cleaning them up.</span></span> <span data-ttu-id="41330-119">La protection PUA est prise en charge sur Windows 10, Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41330-119">PUA protection is supported on Windows 10, Windows Server 2019, and Windows Server 2016.</span></span>

## <a name="microsoft-edge"></a><span data-ttu-id="41330-120">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41330-120">Microsoft Edge</span></span>

<span data-ttu-id="41330-121">Le [nouveau Microsoft Edge,](https://support.microsoft.com/microsoft-edge/get-to-know-microsoft-edge-3f4bb0ff-58de-2188-55c0-f560b7e20bea)basé sur Chromium, bloque les téléchargements d'applications potentiellement indésirables et les URL de ressources associées.</span><span class="sxs-lookup"><span data-stu-id="41330-121">The [new Microsoft Edge](https://support.microsoft.com/microsoft-edge/get-to-know-microsoft-edge-3f4bb0ff-58de-2188-55c0-f560b7e20bea), which is Chromium-based, blocks potentially unwanted application downloads and associated resource URLs.</span></span> <span data-ttu-id="41330-122">Cette fonctionnalité est fournie via [Microsoft Defender SmartScreen.](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview)</span><span class="sxs-lookup"><span data-stu-id="41330-122">This feature is provided via [Microsoft Defender SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview).</span></span>

### <a name="enable-pua-protection-in-chromium-based-microsoft-edge"></a><span data-ttu-id="41330-123">Activer la protection PUA dans Microsoft Edge basé sur Chromium</span><span class="sxs-lookup"><span data-stu-id="41330-123">Enable PUA protection in Chromium-based Microsoft Edge</span></span>

<span data-ttu-id="41330-124">Bien que la protection des applications potentiellement indésirables dans Microsoft Edge (basée sur Chromium, version 80.0.361.50) soit désactivée par défaut, elle peut facilement être désactivée à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="41330-124">Although potentially unwanted application protection in Microsoft Edge (Chromium-based, version 80.0.361.50) is turned off by default, it can easily be turned on from within the browser.</span></span>

1. <span data-ttu-id="41330-125">Sélectionnez les ellipses, puis choisissez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="41330-125">Select the ellipses, and then choose **Settings**.</span></span>
2. <span data-ttu-id="41330-126">Sélectionnez **Confidentialité, recherche et services.**</span><span class="sxs-lookup"><span data-stu-id="41330-126">Select **Privacy, search, and services**.</span></span>
3. <span data-ttu-id="41330-127">Sous la section **Sécurité,** activer bloquer **les applications potentiellement indésirables.**</span><span class="sxs-lookup"><span data-stu-id="41330-127">Under the **Security** section, turn on **Block potentially unwanted apps**.</span></span>

> [!TIP]
> <span data-ttu-id="41330-128">Si vous exécutez Microsoft Edge (basé sur Chromium), vous pouvez explorer en toute sécurité la fonctionnalité de blocage d'URL de la protection PUA en la testant sur l'une de nos pages de démonstration [Microsoft Defender SmartScreen.](https://demo.smartscreen.msft.net/)</span><span class="sxs-lookup"><span data-stu-id="41330-128">If you are running Microsoft Edge (Chromium-based), you can safely explore the URL-blocking feature of PUA protection by testing it out on one of our [Microsoft Defender SmartScreen demo pages](https://demo.smartscreen.msft.net/).</span></span>

### <a name="blocking-urls-with-microsoft-defender-smartscreen"></a><span data-ttu-id="41330-129">Blocage des URL avec Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="41330-129">Blocking URLs with Microsoft Defender SmartScreen</span></span>

<span data-ttu-id="41330-130">Dans edge basé sur Chromium avec une protection PUA désactivée, Microsoft Defender SmartScreen vous protège contre les URL associées à PUA.</span><span class="sxs-lookup"><span data-stu-id="41330-130">In Chromium-based Edge with PUA protection turned on, Microsoft Defender SmartScreen protects you from PUA-associated URLs.</span></span>

<span data-ttu-id="41330-131">Les administrateurs de [sécurité](/DeployEdge/configure-microsoft-edge) peuvent configurer la façon dont Microsoft Edge et Microsoft Defender SmartScreen fonctionnent ensemble pour protéger les groupes d'utilisateurs contre les URL associées à puA.</span><span class="sxs-lookup"><span data-stu-id="41330-131">Security admins can [configure](/DeployEdge/configure-microsoft-edge) how Microsoft Edge and Microsoft Defender SmartScreen work together to protect groups of users from PUA-associated URLs.</span></span> <span data-ttu-id="41330-132">Plusieurs [paramètres de stratégie de groupe](/DeployEdge/microsoft-edge-policies#smartscreen-settings) sont explicitement disponibles pour Microsoft Defender SmartScreen, y compris un pour bloquer [puA](/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled).</span><span class="sxs-lookup"><span data-stu-id="41330-132">There are several [group policy settings](/DeployEdge/microsoft-edge-policies#smartscreen-settings) explicitly for Microsoft Defender SmartScreen available, including [one for blocking PUA](/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled).</span></span> <span data-ttu-id="41330-133">En outre, les administrateurs peuvent configurer [Microsoft Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen) dans son ensemble, à l'aide des paramètres de stratégie de groupe pour activer ou désactiver Microsoft Defender SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="41330-133">In addition, admins can [configure Microsoft Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen) as a whole, using group policy settings to turn Microsoft Defender SmartScreen on or off.</span></span>

<span data-ttu-id="41330-134">Bien que Microsoft Defender pour point de terminaison dispose de sa propre liste d'blocs basée sur un jeu de données géré par Microsoft, vous pouvez personnaliser cette liste en fonction de vos propres renseignements sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="41330-134">Although Microsoft Defender for Endpoint has its own block list based upon a data set managed by Microsoft, you can customize this list based on your own threat intelligence.</span></span> <span data-ttu-id="41330-135">Si vous [créez et gérez des indicateurs](/microsoft-365/security/defender-endpoint/manage-indicators) dans le portail Microsoft Defender pour points de terminaison, Microsoft Defender SmartScreen respecte les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="41330-135">If you [create and manage indicators](/microsoft-365/security/defender-endpoint/manage-indicators) in the Microsoft Defender for Endpoint portal, Microsoft Defender SmartScreen respects the new settings.</span></span>

## <a name="microsoft-defender-antivirus"></a><span data-ttu-id="41330-136">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="41330-136">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="41330-137">La fonctionnalité de protection des applications potentiellement indésirables (PUA) de l'Antivirus Microsoft Defender peut détecter et bloquer les applications potentiellement indésirables sur les points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="41330-137">The potentially unwanted application (PUA) protection feature in Microsoft Defender Antivirus can detect and block PUAs on endpoints in your network.</span></span>

> [!NOTE]
> <span data-ttu-id="41330-138">Cette fonctionnalité est disponible dans Windows 10, Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41330-138">This feature is available in Windows 10, Windows Server 2019, and Windows Server 2016.</span></span>

<span data-ttu-id="41330-139">L'Antivirus Microsoft Defender bloque les fichiers PUA détectés et toute tentative de téléchargement, de déplacement, d'exécuter ou d'installation de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="41330-139">Microsoft Defender Antivirus blocks detected PUA files and any attempts to download, move, run, or install them.</span></span> <span data-ttu-id="41330-140">Les fichiers PUA bloqués sont ensuite mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="41330-140">Blocked PUA files are then moved to quarantine.</span></span> <span data-ttu-id="41330-141">Lorsqu'un fichier PUA est détecté sur un point de terminaison, l'Antivirus Microsoft Defender envoie une notification à l'utilisateur (sauf si les[notifications](configure-notifications-microsoft-defender-antivirus.md)ont été désactivées) dans le même format que les autres détections de menaces.</span><span class="sxs-lookup"><span data-stu-id="41330-141">When a PUA file is detected on an endpoint, Microsoft Defender Antivirus sends a notification to the user ([unless notifications have been disabled](configure-notifications-microsoft-defender-antivirus.md)) in the same format as other threat detections.</span></span> <span data-ttu-id="41330-142">La notification est précédée pour `PUA:` indiquer son contenu.</span><span class="sxs-lookup"><span data-stu-id="41330-142">The notification is prefaced with `PUA:` to indicate its content.</span></span>

<span data-ttu-id="41330-143">La notification apparaît dans la liste de mise en [quarantaine habituelle dans l'application Sécurité Windows.](microsoft-defender-security-center-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="41330-143">The notification appears in the usual [quarantine list within the Windows Security app](microsoft-defender-security-center-antivirus.md).</span></span>

### <a name="configure-pua-protection-in-microsoft-defender-antivirus"></a><span data-ttu-id="41330-144">Configurer la protection PUA dans l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="41330-144">Configure PUA protection in Microsoft Defender Antivirus</span></span>

<span data-ttu-id="41330-145">Vous pouvez activer la protection PUA avec [Microsoft Intune,](/mem/intune/protect/device-protect) [Microsoft Endpoint Configuration Manager,](/mem/configmgr/protect/deploy-use/endpoint-protection)la stratégie de groupe [ou](/azure/active-directory-domain-services/manage-group-policy)via des [cmdlets PowerShell.](/powershell/module/defender/?preserve-view=true&view=win10-ps)</span><span class="sxs-lookup"><span data-stu-id="41330-145">You can enable PUA protection with [Microsoft Intune](/mem/intune/protect/device-protect), [Microsoft Endpoint Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection), [Group Policy](/azure/active-directory-domain-services/manage-group-policy), or via [PowerShell cmdlets](/powershell/module/defender/?preserve-view=true&view=win10-ps).</span></span>

<span data-ttu-id="41330-146">Vous pouvez également utiliser la protection PUA en mode audit pour détecter les applications potentiellement indésirables sans les bloquer.</span><span class="sxs-lookup"><span data-stu-id="41330-146">You can also use PUA protection in audit mode to detect potentially unwanted applications without blocking them.</span></span> <span data-ttu-id="41330-147">Les détections sont capturées dans le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="41330-147">The detections are captured in the Windows event log.</span></span>

> [!TIP]
> <span data-ttu-id="41330-148">Visitez le site web de démonstration microsoft Defender pour points de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com/Page/UrlRep) pour vérifier que la fonctionnalité fonctionne et la voir en action.</span><span class="sxs-lookup"><span data-stu-id="41330-148">Visit the Microsoft Defender for Endpoint demo website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com/Page/UrlRep) to confirm that the feature is working, and see it in action.</span></span>

<span data-ttu-id="41330-149">La protection PUA en mode audit est utile si votre entreprise effectue une vérification interne de la conformité des logiciels et que vous souhaitez éviter les faux positifs.</span><span class="sxs-lookup"><span data-stu-id="41330-149">PUA protection in audit mode is useful if your company is conducting an internal software security compliance check and you'd like to avoid any false positives.</span></span>

#### <a name="use-intune-to-configure-pua-protection"></a><span data-ttu-id="41330-150">Utiliser Intune pour configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-150">Use Intune to configure PUA protection</span></span>

<span data-ttu-id="41330-151">Pour plus d'informations, voir Configurer les paramètres de restriction d'appareil dans [Microsoft Intune](/intune/device-restrictions-configure) et l'Antivirus Microsoft Defender pour [Windows 10 dans Intune.](/intune/device-restrictions-windows-10#microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="41330-151">See [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure) and [Microsoft Defender Antivirus device restriction settings for Windows 10 in Intune](/intune/device-restrictions-windows-10#microsoft-defender-antivirus) for more details.</span></span>

#### <a name="use-configuration-manager-to-configure-pua-protection"></a><span data-ttu-id="41330-152">Utiliser Configuration Manager pour configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-152">Use Configuration Manager to configure PUA protection</span></span>

<span data-ttu-id="41330-153">La protection PUA est activée par défaut dans Microsoft Endpoint Manager (Current Branch).</span><span class="sxs-lookup"><span data-stu-id="41330-153">PUA protection is enabled by default in the Microsoft Endpoint Manager (Current Branch).</span></span>

<span data-ttu-id="41330-154">Découvrez comment créer et déployer des stratégies [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#real-time-protection-settings) malveillant : paramètres d'analyse programmés pour plus d'informations sur la configuration de Microsoft Endpoint Manager (Current Branch).</span><span class="sxs-lookup"><span data-stu-id="41330-154">See [How to create and deploy antimalware policies: Scheduled scans settings](/configmgr/protect/deploy-use/endpoint-antimalware-policies#real-time-protection-settings) for details on configuring Microsoft Endpoint Manager (Current Branch).</span></span>

<span data-ttu-id="41330-155">For System Center 2012 Configuration Manager, see [How to Deploy Potentially Unwanted Application Protection Policy for Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#BKMK_PUA).</span><span class="sxs-lookup"><span data-stu-id="41330-155">For System Center 2012 Configuration Manager, see [How to Deploy Potentially Unwanted Application Protection Policy for Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#BKMK_PUA).</span></span>

> [!NOTE]
> <span data-ttu-id="41330-156">Les événements PUA bloqués par l'Antivirus Microsoft Defender sont signalés dans l'Observateur d'événements Windows et non dans Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="41330-156">PUA events blocked by Microsoft Defender Antivirus are reported in the Windows Event Viewer and not in Microsoft Endpoint Configuration Manager.</span></span>

#### <a name="use-group-policy-to-configure-pua-protection"></a><span data-ttu-id="41330-157">Utiliser une stratégie de groupe pour configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-157">Use Group Policy to configure PUA protection</span></span>

1. <span data-ttu-id="41330-158">Télécharger et installer des modèles d'administration (.admx) pour la mise à jour [d'octobre 2020 de Windows 10 (20H2)](https://www.microsoft.com/download/details.aspx?id=102157)</span><span class="sxs-lookup"><span data-stu-id="41330-158">Download and install [Administrative Templates (.admx) for Windows 10 October 2020 Update (20H2)](https://www.microsoft.com/download/details.aspx?id=102157)</span></span>

2. <span data-ttu-id="41330-159">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="41330-159">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

3. <span data-ttu-id="41330-160">Sélectionnez l'objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="41330-160">Select the Group Policy Object you want to configure, and then choose **Edit**.</span></span>

4. <span data-ttu-id="41330-161">Dans **l'Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur et sélectionnez **Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="41330-161">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

5. <span data-ttu-id="41330-162">Développez l'arborescence **des composants Windows**  >  **de l'Antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="41330-162">Expand the tree to **Windows Components** > **Microsoft Defender Antivirus**.</span></span>

6. <span data-ttu-id="41330-163">Double-cliquez **sur Configurer la détection pour les applications potentiellement indésirables.**</span><span class="sxs-lookup"><span data-stu-id="41330-163">Double-click **Configure detection for potentially unwanted applications**.</span></span>

7. <span data-ttu-id="41330-164">Sélectionnez **Activé pour** activer la protection PUA.</span><span class="sxs-lookup"><span data-stu-id="41330-164">Select **Enabled** to enable PUA protection.</span></span>

8. <span data-ttu-id="41330-165">Dans **Options,** **sélectionnez Bloquer** pour bloquer les applications potentiellement indésirables, ou sélectionnez **Mode Audit** pour tester le fonctionnement du paramètre dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="41330-165">In **Options**, select **Block** to block potentially unwanted applications, or select **Audit Mode** to test how the setting works in your environment.</span></span> <span data-ttu-id="41330-166">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="41330-166">Select **OK**.</span></span>

9. <span data-ttu-id="41330-167">Déployez votre objet de stratégie de groupe comme vous le faites généralement.</span><span class="sxs-lookup"><span data-stu-id="41330-167">Deploy your Group Policy object as you usually do.</span></span>

#### <a name="use-powershell-cmdlets-to-configure-pua-protection"></a><span data-ttu-id="41330-168">Utiliser les cmdlets PowerShell pour configurer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-168">Use PowerShell cmdlets to configure PUA protection</span></span>

##### <a name="to-enable-pua-protection"></a><span data-ttu-id="41330-169">Pour activer la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-169">To enable PUA protection</span></span>

```PowerShell
Set-MpPreference -PUAProtection Enabled
```

<span data-ttu-id="41330-170">Définir la valeur de cette cmdlet pour qu'elle allume la fonctionnalité si `Enabled` elle a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="41330-170">Setting the value for this cmdlet to `Enabled` turns the feature on if it has been disabled.</span></span>

##### <a name="to-set-pua-protection-to-audit-mode"></a><span data-ttu-id="41330-171">Pour définir la protection PUA en mode audit</span><span class="sxs-lookup"><span data-stu-id="41330-171">To set PUA protection to audit mode</span></span>

```PowerShell
Set-MpPreference -PUAProtection AuditMode
```

<span data-ttu-id="41330-172">Le `AuditMode` paramètre détecte les puAs sans les bloquer.</span><span class="sxs-lookup"><span data-stu-id="41330-172">Setting `AuditMode` detects PUAs without blocking them.</span></span>

##### <a name="to-disable-pua-protection"></a><span data-ttu-id="41330-173">Pour désactiver la protection PUA</span><span class="sxs-lookup"><span data-stu-id="41330-173">To disable PUA protection</span></span>

<span data-ttu-id="41330-174">Nous vous recommandons de maintenir la protection PUA allumée.</span><span class="sxs-lookup"><span data-stu-id="41330-174">We recommend keeping PUA protection turned on.</span></span> <span data-ttu-id="41330-175">Toutefois, vous pouvez la désactiver à l'aide de l'cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="41330-175">However, you can turn it off by using the following cmdlet:</span></span>

```PowerShell
Set-MpPreference -PUAProtection Disabled
```

<span data-ttu-id="41330-176">Définir la valeur de cette cmdlet pour que la fonctionnalité soit éteinte si `Disabled` elle a été activée.</span><span class="sxs-lookup"><span data-stu-id="41330-176">Setting the value for this cmdlet to `Disabled` turns the feature off if it has been enabled.</span></span>

<span data-ttu-id="41330-177">Pour [plus d'informations](use-powershell-cmdlets-microsoft-defender-antivirus.md) sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir les [cmdlets](/powershell/module/defender/index) Utiliser PowerShell pour configurer et exécuter l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="41330-177">See [Use PowerShell cmdlets to configure and run Microsoft Defender Antivirus](use-powershell-cmdlets-microsoft-defender-antivirus.md) and [Defender cmdlets](/powershell/module/defender/index) for more information on how to use PowerShell with Microsoft Defender Antivirus.</span></span>

## <a name="view-pua-events"></a><span data-ttu-id="41330-178">Afficher les événements PUA</span><span class="sxs-lookup"><span data-stu-id="41330-178">View PUA events</span></span>

<span data-ttu-id="41330-179">Les événements PUA sont signalés dans l'Observateur d'événements Windows, mais pas dans Microsoft Endpoint Manager ou dans Intune.</span><span class="sxs-lookup"><span data-stu-id="41330-179">PUA events are reported in the Windows Event Viewer, but not in Microsoft Endpoint Manager or in Intune.</span></span> <span data-ttu-id="41330-180">Vous pouvez également utiliser la cmdlet pour afficher les menaces gérées par `Get-MpThreat` l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="41330-180">You can also use the `Get-MpThreat` cmdlet to view threats that Microsoft Defender Antivirus handled.</span></span> <span data-ttu-id="41330-181">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="41330-181">Here's an example:</span></span>

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

<span data-ttu-id="41330-182">Vous pouvez activer les notifications par courrier électronique pour recevoir des messages sur les détections PUA.</span><span class="sxs-lookup"><span data-stu-id="41330-182">You can turn on email notifications to receive mail about PUA detections.</span></span>

<span data-ttu-id="41330-183">Pour [plus d'informations](troubleshoot-microsoft-defender-antivirus.md) sur l'affichage des événements de l'Antivirus Microsoft Defender, voir Les ID d'événement de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="41330-183">See [Troubleshoot event IDs](troubleshoot-microsoft-defender-antivirus.md) for details on viewing Microsoft Defender Antivirus events.</span></span> <span data-ttu-id="41330-184">Les événements PUA sont enregistrés sous l'ID **d'événement 1160**.</span><span class="sxs-lookup"><span data-stu-id="41330-184">PUA events are recorded under event ID **1160**.</span></span>

## <a name="excluding-files"></a><span data-ttu-id="41330-185">Exclusion de fichiers</span><span class="sxs-lookup"><span data-stu-id="41330-185">Excluding files</span></span>

<span data-ttu-id="41330-186">Parfois, un fichier est bloqué par erreur par la protection PUA ou une fonctionnalité d'une PUA est nécessaire pour effectuer une tâche.</span><span class="sxs-lookup"><span data-stu-id="41330-186">Sometimes a file is erroneously blocked by PUA protection, or a feature of a PUA is required to complete a task.</span></span> <span data-ttu-id="41330-187">Dans ce cas, un fichier peut être ajouté à une liste d'exclusions.</span><span class="sxs-lookup"><span data-stu-id="41330-187">In these cases, a file can be added to an exclusion list.</span></span>

<span data-ttu-id="41330-188">Pour plus d'informations, voir Configurer et valider des exclusions en fonction de [l'extension de fichier et de l'emplacement du dossier.](configure-extension-file-exclusions-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="41330-188">For more information, see [Configure and validate exclusions based on file extension and folder location](configure-extension-file-exclusions-microsoft-defender-antivirus.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="41330-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41330-189">See also</span></span>

- [<span data-ttu-id="41330-190">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="41330-190">Next-generation protection</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="41330-191">Configurer la protection comportementale, heuristique et en temps réel</span><span class="sxs-lookup"><span data-stu-id="41330-191">Configure behavioral, heuristic, and real-time protection</span></span>](configure-protection-features-microsoft-defender-antivirus.md)