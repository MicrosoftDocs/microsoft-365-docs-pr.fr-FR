---
title: Créer des indicateurs pour les fichiers
ms.reviewer: ''
description: Créez des indicateurs pour un hachage de fichier qui définissent la détection, la prévention et l’exclusion des entités.
keywords: fichier, hachage, gérer, autorisé, bloqué, bloquer, nettoyer, malveillant, hachage de fichier, adresse IP, url, domaine
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
ms.openlocfilehash: b56a18e1b35b65629318ab29f2189ef1f73373f5
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53256914"
---
# <a name="create-indicators-for-files"></a><span data-ttu-id="31975-104">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="31975-104">Create indicators for files</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="31975-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="31975-105">**Applies to:**</span></span>
- [<span data-ttu-id="31975-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="31975-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="31975-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="31975-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="31975-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="31975-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="31975-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="31975-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)

<span data-ttu-id="31975-110">Empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="31975-110">Prevent further propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> <span data-ttu-id="31975-111">Si vous connaissez un fichier exécutable portable (PE) potentiellement malveillant, vous pouvez le bloquer.</span><span class="sxs-lookup"><span data-stu-id="31975-111">If you know a potentially malicious portable executable (PE) file, you can block it.</span></span> <span data-ttu-id="31975-112">Cette opération l’empêche d’être lue, écrite ou exécutée sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31975-112">This operation will prevent it from being read, written, or executed on devices in your organization.</span></span>

<span data-ttu-id="31975-113">Il existe trois façons de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="31975-113">There are three ways you can create indicators for files:</span></span>

- <span data-ttu-id="31975-114">En créant un indicateur via la page paramètres</span><span class="sxs-lookup"><span data-stu-id="31975-114">By creating an indicator through the settings page</span></span>
- <span data-ttu-id="31975-115">En créant un indicateur contextuel à l’aide du bouton Ajouter un indicateur à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="31975-115">By creating a contextual indicator using the add indicator button from the file details page</span></span>
- <span data-ttu-id="31975-116">En créant un indicateur via [l’API d’indicateur](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="31975-116">By creating an indicator through the [Indicator API](ti-indicator.md)</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="31975-117">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="31975-117">Before you begin</span></span>

<span data-ttu-id="31975-118">Il est important de comprendre les conditions préalables suivantes avant de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="31975-118">It's important to understand the following prerequisites prior to creating indicators for files:</span></span>

- <span data-ttu-id="31975-119">Cette fonctionnalité est disponible si votre organisation utilise **Antivirus Microsoft Defender (en mode actif)** et si la protection basée sur **le cloud est activée.**</span><span class="sxs-lookup"><span data-stu-id="31975-119">This feature is available if your organization uses **Microsoft Defender Antivirus (in active mode)** and **Cloud-based protection is enabled**.</span></span> <span data-ttu-id="31975-120">Pour plus d’informations, [voir Gérer la protection basée sur le cloud.](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="31975-120">For more information, see [Manage cloud-based protection](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus).</span></span>

- <span data-ttu-id="31975-121">La version du client anti-programme malveillant doit être 4.18.1901.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="31975-121">The Antimalware client version must be 4.18.1901.x or later.</span></span> <span data-ttu-id="31975-122">Voir [les versions mensuelles de la plateforme et du moteur](manage-updates-baselines-microsoft-defender-antivirus.md#monthly-platform-and-engine-versions)</span><span class="sxs-lookup"><span data-stu-id="31975-122">See [Monthly platform and engine versions](manage-updates-baselines-microsoft-defender-antivirus.md#monthly-platform-and-engine-versions)</span></span>

- <span data-ttu-id="31975-123">Pris en charge sur les appareils Windows 10, version 1703 ou ultérieure, Windows Server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="31975-123">Supported on devices with Windows 10, version 1703 or later, Windows Server 2016 and 2019.</span></span>

- <span data-ttu-id="31975-124">Pour commencer à bloquer les fichiers, vous devez d’abord [activer](advanced-features.md) la fonctionnalité « bloquer ou autoriser » dans Paramètres.</span><span class="sxs-lookup"><span data-stu-id="31975-124">To start blocking files, you first need to [turn on the "block or allow" feature](advanced-features.md) in Settings.</span></span>

<span data-ttu-id="31975-125">Cette fonctionnalité est conçue pour empêcher le téléchargement de programmes malveillants (ou de fichiers potentiellement malveillants) à partir du web.</span><span class="sxs-lookup"><span data-stu-id="31975-125">This feature is designed to prevent suspected malware (or potentially malicious files) from being downloaded from the web.</span></span> <span data-ttu-id="31975-126">Il prend actuellement en charge les fichiers exécutables portables(PE), notamment les fichiers .exe et .dll portables.</span><span class="sxs-lookup"><span data-stu-id="31975-126">It currently supports portable executable (PE) files, including .exe and .dll files.</span></span> <span data-ttu-id="31975-127">La couverture sera étendue au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="31975-127">The coverage will be extended over time.</span></span>

## <a name="create-an-indicator-for-files-from-the-settings-page"></a><span data-ttu-id="31975-128">Créer un indicateur pour les fichiers à partir de la page paramètres</span><span class="sxs-lookup"><span data-stu-id="31975-128">Create an indicator for files from the settings page</span></span>

1. <span data-ttu-id="31975-129">Dans le volet de navigation, sélectionnez **Paramètres > indicateurs.**</span><span class="sxs-lookup"><span data-stu-id="31975-129">In the navigation pane, select **Settings > Indicators**.</span></span>

2. <span data-ttu-id="31975-130">Sélectionnez **l’onglet De hachage de**   fichier.</span><span class="sxs-lookup"><span data-stu-id="31975-130">Select the **File hash** tab.</span></span>

3. <span data-ttu-id="31975-131">Sélectionnez **Ajouter un indicateur**.</span><span class="sxs-lookup"><span data-stu-id="31975-131">Select **Add indicator**.</span></span>

4. <span data-ttu-id="31975-132">Spécifiez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="31975-132">Specify the following details:</span></span>
    - <span data-ttu-id="31975-133">Indicateur : spécifiez les détails de l’entité et définissez l’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="31975-133">Indicator - Specify the entity details and define the expiration of the indicator.</span></span>
    - <span data-ttu-id="31975-134">Action : spécifiez l’action à prendre et fournissez une description.</span><span class="sxs-lookup"><span data-stu-id="31975-134">Action - Specify the action to be taken and provide a description.</span></span>
    - <span data-ttu-id="31975-135">Étendue : définir l’étendue du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="31975-135">Scope - Define the scope of the device group.</span></span>

5. <span data-ttu-id="31975-136">Examinez les détails dans l’onglet Résumé, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="31975-136">Review the details in the Summary tab, then select **Save**.</span></span>

## <a name="create-a-contextual-indicator-from-the-file-details-page"></a><span data-ttu-id="31975-137">Créer un indicateur contextuel à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="31975-137">Create a contextual indicator from the file details page</span></span>

<span data-ttu-id="31975-138">L’une des options lorsque vous prenez des mesures de réponse sur un [fichier consiste](respond-file-alerts.md)à ajouter un indicateur pour le   fichier.</span><span class="sxs-lookup"><span data-stu-id="31975-138">One of the options when taking [response actions on a file](respond-file-alerts.md) is adding an indicator for the file.</span></span> <span data-ttu-id="31975-139">Lorsque vous ajoutez un hachage d’indicateur pour un fichier, vous pouvez choisir de lancer une alerte et de bloquer le fichier chaque fois qu’un appareil de votre organisation tente de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="31975-139">When you add an indicator hash for a file, you can choose to raise an alert and block the file whenever a device in your organization attempts to run it.</span></span>

<span data-ttu-id="31975-140">Les fichiers automatiquement bloqués par un indicateur ne s’afficheront pas dans le centre de l’action du fichier, mais les alertes resteront visibles dans la file d’attente des alertes.</span><span class="sxs-lookup"><span data-stu-id="31975-140">Files automatically blocked by an indicator won't show up in the file's Action center, but the alerts will still be visible in the Alerts queue.</span></span>

>[!IMPORTANT]
>- <span data-ttu-id="31975-141">En règle générale, les blocs de fichiers sont appliqués et supprimés en quelques minutes, mais peuvent prendre plus de 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="31975-141">Typically, file blocks are enforced and removed within a couple of minutes, but can take upwards of 30 minutes.</span></span>
> 
>- <span data-ttu-id="31975-142">S’il existe des stratégies IoC de fichier en conflit avec le même type d’application et la même cible, la stratégie de hachage le plus sécurisé est appliquée.</span><span class="sxs-lookup"><span data-stu-id="31975-142">If there are conflicting file IoC policies with the same enforcement type and target, the policy of the more secure hash will be applied.</span></span> <span data-ttu-id="31975-143">Une stratégie IoC de hachage de fichier SHA-256 l’emporte sur une stratégie IoC de hachage de fichier SHA-1, qui l’emporte sur une stratégie IoC de hachage de fichier MD5 si les types de hachage définissent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="31975-143">An SHA-256 file hash IoC policy will win over an SHA-1 file hash IoC policy, which will win over an MD5 file hash IoC policy if the hash types define the same file.</span></span> <span data-ttu-id="31975-144">Cela est toujours vrai quel que soit le groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="31975-144">This is always true regardless of the device group.</span></span> 
>   <span data-ttu-id="31975-145">Dans tous les autres cas, si des stratégies IoC de fichier en conflit avec la même cible d’application sont appliquées à tous les appareils et au groupe de l’appareil, pour un appareil, la stratégie dans le groupe d’appareils l’emporte.</span><span class="sxs-lookup"><span data-stu-id="31975-145">In all other cases, if conflicting file IoC policies with the same enforcement target are applied to all devices and to the device’s group, then for a device, the policy in the device group will win.</span></span> 
>   
>- <span data-ttu-id="31975-146">Si la stratégie de groupe EnableFileHashComputation est désactivée, la précision de blocage du fichier IoC est réduite.</span><span class="sxs-lookup"><span data-stu-id="31975-146">If the EnableFileHashComputation group policy is disabled, the blocking accuracy of the file IoC is reduced.</span></span> <span data-ttu-id="31975-147">Toutefois, `EnableFileHashComputation` l’activation peut avoir un impact sur les performances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31975-147">However, enabling `EnableFileHashComputation` may impact device performance.</span></span> <span data-ttu-id="31975-148">Par exemple, la copie de fichiers de grande taille à partir d’un partage réseau sur votre appareil local, en particulier sur une connexion VPN, peut avoir un impact sur les performances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31975-148">For example, copying large files from a network share onto your local device, especially over a VPN connection, might have an effect on device performance.</span></span>
>
>   <span data-ttu-id="31975-149">Pour plus d’informations sur la stratégie de groupe EnableFileHashComputation, voir [CSP Defender](/windows/client-management/mdm/defender-csp)</span><span class="sxs-lookup"><span data-stu-id="31975-149">For more information about the EnableFileHashComputation group policy, see [Defender CSP](/windows/client-management/mdm/defender-csp)</span></span>

## <a name="policy-conflict-handling"></a><span data-ttu-id="31975-150">Gestion des conflits de stratégie</span><span class="sxs-lookup"><span data-stu-id="31975-150">Policy conflict handling</span></span>  

<span data-ttu-id="31975-151">Le conflit de gestion des stratégies Cert et IoC de fichier suit l’ordre ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="31975-151">Cert and File IoC policy handling conflict will follow the below order:</span></span>

- <span data-ttu-id="31975-152">Si le fichier n’est pas autorisé par Windows Defender application Control et AppLocker appliquent des stratégies/stratégies de mode, **bloquez**</span><span class="sxs-lookup"><span data-stu-id="31975-152">If the file is not allowed by Windows Defender Application Control and AppLocker enforce mode policy/policies, then **Block**</span></span>

- <span data-ttu-id="31975-153">Sinon, si le fichier est autorisé par l’exclusion Antivirus Microsoft Defender, **autorisez**</span><span class="sxs-lookup"><span data-stu-id="31975-153">Else if the file is allowed by the Microsoft Defender Antivirus exclusion, then **Allow**</span></span>

- <span data-ttu-id="31975-154">Sinon, si le fichier est bloqué ou averti par un blocage ou un avertissement de fichier IoC, **puis Bloquer/Avertir**</span><span class="sxs-lookup"><span data-stu-id="31975-154">Else if the file is blocked or warned by a block or warn file IoC, then **Block/Warn**</span></span>

- <span data-ttu-id="31975-155">Sinon, si le fichier est autorisé par une stratégie IoC de fichier autorisé, **autorisez**</span><span class="sxs-lookup"><span data-stu-id="31975-155">Else if the file is allowed by an allow file IoC policy, then **Allow**</span></span>

- <span data-ttu-id="31975-156">Sinon si le fichier est bloqué par les règles de la asr, cfa, av, SmartScreen, puis **bloquer**</span><span class="sxs-lookup"><span data-stu-id="31975-156">Else if the file is blocked by ASR rules, CFA, AV, SmartScreen, then **Block**</span></span>  

- <span data-ttu-id="31975-157">Else **Allow** (passe Windows Defender Application Control & AppLocker, aucune règle IoC ne s’applique à elle)</span><span class="sxs-lookup"><span data-stu-id="31975-157">Else **Allow** (passes Windows Defender Application Control & AppLocker policy, no IoC rules apply to it)</span></span>

<span data-ttu-id="31975-158">S’il existe des stratégies IoC de fichier en conflit avec le même type d’application et la même cible, la stratégie de hachage le plus sécurisé (c’est-à-dire plus long) est appliquée.</span><span class="sxs-lookup"><span data-stu-id="31975-158">If there are conflicting file IoC policies with the same enforcement type and target, the policy of the more secure (meaning longer) hash will be applied.</span></span> <span data-ttu-id="31975-159">Par exemple, une stratégie IoC de hachage de fichier SHA-256 l’emporte sur une stratégie IoC de hachage de fichier MD5 si les deux types de hachage définissent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="31975-159">For example, an SHA-256 file hash IoC policy will win over an MD5 file hash IoC policy if both hash types define the same file.</span></span>

<span data-ttu-id="31975-160">Les fonctionnalités gestion des vulnérabilités d’application vulnérables aux menaces et aux menaces utilisent les IOC de fichier pour l’application et suivent l’ordre de gestion des conflits ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="31975-160">Threat and vulnerability management's block vulnerable application features uses the file IoCs for enforcement and will follow the above conflict handling order.</span></span>

### <a name="examples"></a><span data-ttu-id="31975-161">範例</span><span class="sxs-lookup"><span data-stu-id="31975-161">Examples</span></span>

|<span data-ttu-id="31975-162">Composant</span><span class="sxs-lookup"><span data-stu-id="31975-162">Component</span></span> |<span data-ttu-id="31975-163">Application des composants</span><span class="sxs-lookup"><span data-stu-id="31975-163">Component enforcement</span></span> |<span data-ttu-id="31975-164">Action de l’indicateur de fichier</span><span class="sxs-lookup"><span data-stu-id="31975-164">File indicator Action</span></span> |<span data-ttu-id="31975-165">Résultat</span><span class="sxs-lookup"><span data-stu-id="31975-165">Result</span></span>
|--|--|--|--|
|<span data-ttu-id="31975-166">Exclusion du chemin d’accès au fichier de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="31975-166">Attack surface reduction file path exclusion</span></span> |<span data-ttu-id="31975-167">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-167">Allow</span></span> |<span data-ttu-id="31975-168">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-168">Block</span></span> |<span data-ttu-id="31975-169">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-169">Block</span></span>
|<span data-ttu-id="31975-170">Règle de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="31975-170">Attack surface reduction rule</span></span> |<span data-ttu-id="31975-171">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-171">Block</span></span> |<span data-ttu-id="31975-172">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-172">Allow</span></span> |<span data-ttu-id="31975-173">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-173">Allow</span></span>
|<span data-ttu-id="31975-174">Windows Defender Application Control</span><span class="sxs-lookup"><span data-stu-id="31975-174">Windows Defender Application Control</span></span> |<span data-ttu-id="31975-175">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-175">Allow</span></span> |<span data-ttu-id="31975-176">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-176">Block</span></span> |<span data-ttu-id="31975-177">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-177">Allow</span></span> |
|<span data-ttu-id="31975-178">Windows Defender Application Control</span><span class="sxs-lookup"><span data-stu-id="31975-178">Windows Defender Application Control</span></span> |<span data-ttu-id="31975-179">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-179">Block</span></span> |<span data-ttu-id="31975-180">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-180">Allow</span></span> |<span data-ttu-id="31975-181">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-181">Block</span></span>
|<span data-ttu-id="31975-182">Antivirus Microsoft Defender exclusion</span><span class="sxs-lookup"><span data-stu-id="31975-182">Microsoft Defender Antivirus exclusion</span></span> |<span data-ttu-id="31975-183">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-183">Allow</span></span> |<span data-ttu-id="31975-184">Bloquer</span><span class="sxs-lookup"><span data-stu-id="31975-184">Block</span></span> |<span data-ttu-id="31975-185">Autoriser</span><span class="sxs-lookup"><span data-stu-id="31975-185">Allow</span></span>

## <a name="see-also"></a><span data-ttu-id="31975-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31975-186">See also</span></span>

- [<span data-ttu-id="31975-187">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="31975-187">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="31975-188">Créer des indicateurs pour les IP et URL/domaines</span><span class="sxs-lookup"><span data-stu-id="31975-188">Create indicators for IPs and URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="31975-189">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="31975-189">Create indicators based on certificates</span></span>](indicator-certificates.md)
- [<span data-ttu-id="31975-190">Gérer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="31975-190">Manage indicators</span></span>](indicator-manage.md)
