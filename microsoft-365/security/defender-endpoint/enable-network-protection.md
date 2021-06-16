---
title: Activer la protection du réseau
description: Activez la protection réseau avec la stratégie de groupe, PowerShell ou Gestion des périphériques mobiles et Configuration Manager.
keywords: Protection ANetwork, attaques, site web malveillant, ip, domaine, domaines, activer, activer
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
ms.topic: conceptual
author: dansimp
ms.author: dansimp
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: bde97638a39eef4561b898b2cf49e51bed6e77a5
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52926654"
---
# <a name="turn-on-network-protection"></a><span data-ttu-id="14dc9-104">Activer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-104">Turn on network protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="14dc9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="14dc9-105">**Applies to:**</span></span>
- [<span data-ttu-id="14dc9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="14dc9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="14dc9-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="14dc9-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="14dc9-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="14dc9-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="14dc9-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="14dc9-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="14dc9-110">[La protection du](network-protection.md) réseau permet d’empêcher les employés d’utiliser n’importe quelle application pour accéder à des domaines dangereux qui peuvent héberger des tentatives d’hameçonnage, des attaques et d’autres contenus malveillants sur Internet.</span><span class="sxs-lookup"><span data-stu-id="14dc9-110">[Network protection](network-protection.md) helps to prevent employees from using any application to access dangerous domains that may host phishing scams, exploits, and other malicious content on the internet.</span></span> <span data-ttu-id="14dc9-111">Vous pouvez [auditer la protection réseau](evaluate-network-protection.md) dans un environnement de test pour afficher les applications qui seraient bloquées avant de l’activer.</span><span class="sxs-lookup"><span data-stu-id="14dc9-111">You can [audit network protection](evaluate-network-protection.md) in a test environment to view which apps would be blocked before you enable it.</span></span>

[<span data-ttu-id="14dc9-112">En savoir plus sur les options de configuration du filtrage réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-112">Learn more about network filtering configuration options</span></span>](/mem/intune/protect/endpoint-protection-windows-10#network-filtering)

## <a name="check-if-network-protection-is-enabled"></a><span data-ttu-id="14dc9-113">Vérifier si la protection réseau est activée</span><span class="sxs-lookup"><span data-stu-id="14dc9-113">Check if network protection is enabled</span></span>

<span data-ttu-id="14dc9-114">Vérifiez si la protection réseau a été activée sur un appareil local à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="14dc9-114">Check if network protection has been enabled on a local device by using Registry editor.</span></span>

1. <span data-ttu-id="14dc9-115">Sélectionnez **le bouton** Démarrer dans la barre des tâches et tapez **regedit** pour ouvrir l’Éditeur du Registre</span><span class="sxs-lookup"><span data-stu-id="14dc9-115">Select the **Start** button in the task bar and type **regedit** to open Registry editor</span></span>

2. <span data-ttu-id="14dc9-116">Choisir **HKEY_LOCAL_MACHINE** dans le menu latéral</span><span class="sxs-lookup"><span data-stu-id="14dc9-116">Choose **HKEY_LOCAL_MACHINE** from the side menu</span></span>

3. <span data-ttu-id="14dc9-117">Naviguez dans les menus imbrmbrés jusqu’à **SOFTWARE**  >  **Microsoft**  >  **Windows Defender**  >  **Windows Defender Exploit Guard** Network  >  **Protection**</span><span class="sxs-lookup"><span data-stu-id="14dc9-117">Navigate through the nested menus to **SOFTWARE** > **Microsoft** > **Windows Defender** > **Windows Defender Exploit Guard** > **Network Protection**</span></span>

4. <span data-ttu-id="14dc9-118">Sélectionnez **EnableNetworkProtection pour** voir l’état actuel de la protection réseau sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="14dc9-118">Select **EnableNetworkProtection** to see the current state of network protection on the device</span></span>

    * <span data-ttu-id="14dc9-119">0 ou **Off**</span><span class="sxs-lookup"><span data-stu-id="14dc9-119">0, or **Off**</span></span>
    * <span data-ttu-id="14dc9-120">1 ou **Sur**</span><span class="sxs-lookup"><span data-stu-id="14dc9-120">1, or **On**</span></span>
    * <span data-ttu-id="14dc9-121">2 ou **mode Audit**</span><span class="sxs-lookup"><span data-stu-id="14dc9-121">2, or **Audit** mode</span></span>
    
    ![networkprotection](https://user-images.githubusercontent.com/3296790/95341270-b738b280-08d3-11eb-84a0-16abb140c9fd.PNG)

## <a name="enable-network-protection"></a><span data-ttu-id="14dc9-123">Activer la protection réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-123">Enable network protection</span></span>

<span data-ttu-id="14dc9-124">Activez la protection réseau à l’aide de l’une des méthodes ci-après :</span><span class="sxs-lookup"><span data-stu-id="14dc9-124">Enable network protection by using any of these methods:</span></span>

* [<span data-ttu-id="14dc9-125">PowerShell</span><span class="sxs-lookup"><span data-stu-id="14dc9-125">PowerShell</span></span>](#powershell)
* [<span data-ttu-id="14dc9-126">Gestion des périphériques mobiles (MDM)</span><span class="sxs-lookup"><span data-stu-id="14dc9-126">Mobile Device Management (MDM)</span></span>](#mobile-device-management-mdm)
* [<span data-ttu-id="14dc9-127">Microsoft Endpoint Manager / Intune</span><span class="sxs-lookup"><span data-stu-id="14dc9-127">Microsoft Endpoint Manager / Intune</span></span>](#microsoft-endpoint-manager-formerly-intune)
* [<span data-ttu-id="14dc9-128">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="14dc9-128">Group Policy</span></span>](#group-policy)

### <a name="powershell"></a><span data-ttu-id="14dc9-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="14dc9-129">PowerShell</span></span>

1. <span data-ttu-id="14dc9-130">Tapez **powershell** dans le menu Démarrer, cliquez avec le **bouton droit sur Windows PowerShell** puis **sélectionnez Exécuter en tant qu’administrateur**</span><span class="sxs-lookup"><span data-stu-id="14dc9-130">Type **powershell** in the Start menu, right-click **Windows PowerShell** and select **Run as administrator**</span></span>
2. <span data-ttu-id="14dc9-131">Entrez l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="14dc9-131">Enter the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -EnableNetworkProtection Enabled
    ```

3. <span data-ttu-id="14dc9-132">Facultatif : activez la fonctionnalité en mode audit à l’aide de l’cmdlet suivante :</span><span class="sxs-lookup"><span data-stu-id="14dc9-132">Optional: Enable the feature in audit mode using the following cmdlet:</span></span>

    ```PowerShell
    Set-MpPreference -EnableNetworkProtection AuditMode
    ```

    <span data-ttu-id="14dc9-133">À `Disabled` utiliser à la place ou pour désactiver la `AuditMode` `Enabled` fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="14dc9-133">Use `Disabled` instead of `AuditMode` or `Enabled` to turn off the feature.</span></span>

### <a name="mobile-device-management-mdm"></a><span data-ttu-id="14dc9-134">Gestion des périphériques mobiles (GPM)</span><span class="sxs-lookup"><span data-stu-id="14dc9-134">Mobile device management (MDM)</span></span>

<span data-ttu-id="14dc9-135">Utilisez le fournisseur de services de configuration [./Vendor/MSFT/Policy/Config/Defender/EnableNetworkProtection](/windows/client-management/mdm/policy-csp-defender) (CSP) pour activer ou désactiver la protection réseau ou activer le mode audit.</span><span class="sxs-lookup"><span data-stu-id="14dc9-135">Use the [./Vendor/MSFT/Policy/Config/Defender/EnableNetworkProtection](/windows/client-management/mdm/policy-csp-defender) configuration service provider (CSP) to enable or disable network protection or enable audit mode.</span></span>

### <a name="microsoft-endpoint-manager-formerly-intune"></a><span data-ttu-id="14dc9-136">Microsoft Endpoint Manager (anciennement Intune)</span><span class="sxs-lookup"><span data-stu-id="14dc9-136">Microsoft Endpoint Manager (formerly Intune)</span></span>

1. <span data-ttu-id="14dc9-137">Connectez-vous au Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="14dc9-137">Sign into the Microsoft Endpoint Manager admin center (https://endpoint.microsoft.com)</span></span>

2. <span data-ttu-id="14dc9-138">Créer ou modifier un profil [de configuration de la protection des points de terminaison](/mem/intune/protect/endpoint-protection-configure)</span><span class="sxs-lookup"><span data-stu-id="14dc9-138">Create or edit an [endpoint protection configuration profile](/mem/intune/protect/endpoint-protection-configure)</span></span>

3. <span data-ttu-id="14dc9-139">Sous **Configuration Paramètres** dans le flux de profil, Protection contre les attaques Microsoft Defender Protection réseau de filtrage réseau  >    >    >  **Activer** ou **Auditer uniquement**</span><span class="sxs-lookup"><span data-stu-id="14dc9-139">Under **Configuration Settings** in the profile flow, go to **Microsoft Defender Exploit Guard** > **Network filtering** > **Network protection** > **Enable** or **Audit only**</span></span>

### <a name="group-policy"></a><span data-ttu-id="14dc9-140">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="14dc9-140">Group Policy</span></span>

<span data-ttu-id="14dc9-141">Utilisez la procédure suivante pour activer la protection réseau sur des ordinateurs joints à un domaine ou sur un ordinateur autonome.</span><span class="sxs-lookup"><span data-stu-id="14dc9-141">Use the following procedure to enable network protection on domain-joined computers or on a standalone computer.</span></span>

1. <span data-ttu-id="14dc9-142">Sur un ordinateur autonome,  sélectionnez Démarrer, puis tapez et sélectionnez **Modifier la stratégie de groupe.**</span><span class="sxs-lookup"><span data-stu-id="14dc9-142">On a standalone computer, go to **Start** and then type and select **Edit group policy**.</span></span>

    <span data-ttu-id="14dc9-143">*-Or-*</span><span class="sxs-lookup"><span data-stu-id="14dc9-143">*-Or-*</span></span>

    <span data-ttu-id="14dc9-144">Sur un ordinateur de gestion de stratégie de groupe joint à un domaine, ouvrez la [Console](https://technet.microsoft.com/library/cc731212.aspx)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="14dc9-144">On a domain-joined Group Policy management computer, open the [Group Policy Management Console](https://technet.microsoft.com/library/cc731212.aspx), right-click the Group Policy Object you want to configure and select **Edit**.</span></span>

2. <span data-ttu-id="14dc9-145">Dans l’**Éditeur de gestion des stratégies de groupe**, accédez à **Configuration ordinateur**, puis sélectionnez **Modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="14dc9-145">In the **Group Policy Management Editor**, go to **Computer configuration** and select **Administrative templates**.</span></span>

3. <span data-ttu-id="14dc9-146">Développez l’arborescence **Windows composants**  >  **Antivirus Microsoft Defender**  >  **Windows Defender Exploit Guard** Network  >  **Protection**.</span><span class="sxs-lookup"><span data-stu-id="14dc9-146">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Windows Defender Exploit Guard** > **Network protection**.</span></span>

> [!NOTE]
> <span data-ttu-id="14dc9-147">Sur les versions antérieures Windows, le chemin d’accès de la stratégie de groupe peut dire « Antivirus Windows Defender » au lieu de « Antivirus Microsoft Defender ».</span><span class="sxs-lookup"><span data-stu-id="14dc9-147">On older versions of Windows, the group policy path may say "Windows Defender Antivirus" instead of "Microsoft Defender Antivirus."</span></span>

4. <span data-ttu-id="14dc9-148">Double-cliquez sur le paramètre Empêcher les utilisateurs **et les applications d’accéder** au paramètre sites web dangereux et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="14dc9-148">Double-click the **Prevent users and apps from accessing dangerous websites** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="14dc9-149">Dans la section Options, vous devez spécifier l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="14dc9-149">In the options section, you must specify one of the following options:</span></span>
    * <span data-ttu-id="14dc9-150">**Bloquer** : les utilisateurs ne peuvent pas accéder aux domaines et aux adresses IP malveillants</span><span class="sxs-lookup"><span data-stu-id="14dc9-150">**Block** - Users can't access malicious IP addresses and domains</span></span>
    * <span data-ttu-id="14dc9-151">**Désactiver (par défaut)** : la fonctionnalité de protection réseau ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="14dc9-151">**Disable (Default)** - The Network protection feature won't work.</span></span> <span data-ttu-id="14dc9-152">Les utilisateurs ne seront pas bloqués pour accéder aux domaines malveillants</span><span class="sxs-lookup"><span data-stu-id="14dc9-152">Users won't be blocked from accessing malicious domains</span></span>
    * <span data-ttu-id="14dc9-153">**Mode audit** : si un utilisateur visite une adresse IP ou un domaine malveillant, un événement est enregistré dans le journal Windows’événements malveillants.</span><span class="sxs-lookup"><span data-stu-id="14dc9-153">**Audit Mode** - If a user visits a malicious IP address or domain, an event will be recorded in the Windows event log.</span></span> <span data-ttu-id="14dc9-154">Toutefois, l’utilisateur ne sera pas empêché de visiter l’adresse.</span><span class="sxs-lookup"><span data-stu-id="14dc9-154">However, the user won't be blocked from visiting the address.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14dc9-155">Pour activer entièrement la protection réseau,  vous devez définir  l’option stratégie de groupe sur Activé et également sélectionner Bloquer dans le menu déroulant Options.</span><span class="sxs-lookup"><span data-stu-id="14dc9-155">To fully enable network protection, you must set the Group Policy option to **Enabled** and also select **Block** in the options drop-down menu.</span></span>

<span data-ttu-id="14dc9-156">Confirmez que la protection réseau est activée sur un ordinateur local à l’aide de l’éditeur du Registre :</span><span class="sxs-lookup"><span data-stu-id="14dc9-156">Confirm network protection is enabled on a local computer by using Registry editor:</span></span>

1. <span data-ttu-id="14dc9-157">Sélectionnez **Démarrer** et tapez **regedit** pour ouvrir **l’Éditeur du Registre.**</span><span class="sxs-lookup"><span data-stu-id="14dc9-157">Select **Start** and type **regedit** to open **Registry Editor**.</span></span>

2. <span data-ttu-id="14dc9-158">Accédez à **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Defender\Windows Defender Exploit Guard\Network Protection\EnableNetworkProtection**</span><span class="sxs-lookup"><span data-stu-id="14dc9-158">Navigate to **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Defender\Windows Defender Exploit Guard\Network Protection\EnableNetworkProtection**</span></span>

3. <span data-ttu-id="14dc9-159">Sélectionnez **EnableNetworkProtection et** confirmez la valeur :</span><span class="sxs-lookup"><span data-stu-id="14dc9-159">Select **EnableNetworkProtection** and confirm the value:</span></span>
   * <span data-ttu-id="14dc9-160">0=Off</span><span class="sxs-lookup"><span data-stu-id="14dc9-160">0=Off</span></span>
   * <span data-ttu-id="14dc9-161">1=Sur</span><span class="sxs-lookup"><span data-stu-id="14dc9-161">1=On</span></span>
   * <span data-ttu-id="14dc9-162">2=Audit</span><span class="sxs-lookup"><span data-stu-id="14dc9-162">2=Audit</span></span>

## <a name="see-also"></a><span data-ttu-id="14dc9-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14dc9-163">See also</span></span>

* [<span data-ttu-id="14dc9-164">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-164">Network protection</span></span>](network-protection.md)
* [<span data-ttu-id="14dc9-165">Évaluer la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-165">Evaluate network protection</span></span>](evaluate-network-protection.md)
* [<span data-ttu-id="14dc9-166">Résoudre les problèmes de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="14dc9-166">Troubleshoot network protection</span></span>](troubleshoot-np.md)
