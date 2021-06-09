---
title: Créer des indicateurs pour les fichiers
ms.reviewer: ''
description: Créez des indicateurs pour un hachage de fichier qui définit la détection, la prévention et l’exclusion des entités.
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
ms.openlocfilehash: 6d92cbacba72210c6accbbb1e5ecf25de660fc3c
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730533"
---
# <a name="create-indicators-for-files"></a><span data-ttu-id="8e427-104">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="8e427-104">Create indicators for files</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="8e427-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8e427-105">**Applies to:**</span></span>
- [<span data-ttu-id="8e427-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8e427-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="8e427-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e427-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="8e427-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="8e427-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="8e427-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="8e427-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)

<span data-ttu-id="8e427-110">Empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="8e427-110">Prevent further propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> <span data-ttu-id="8e427-111">Si vous connaissez un fichier exécutable portable (PE) potentiellement malveillant, vous pouvez le bloquer.</span><span class="sxs-lookup"><span data-stu-id="8e427-111">If you know a potentially malicious portable executable (PE) file, you can block it.</span></span> <span data-ttu-id="8e427-112">Cette opération l’empêche d’être lue, écrite ou exécutée sur les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e427-112">This operation will prevent it from being read, written, or executed on devices in your organization.</span></span>

<span data-ttu-id="8e427-113">Il existe trois façons de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="8e427-113">There are three ways you can create indicators for files:</span></span>

- <span data-ttu-id="8e427-114">En créant un indicateur via la page paramètres</span><span class="sxs-lookup"><span data-stu-id="8e427-114">By creating an indicator through the settings page</span></span>
- <span data-ttu-id="8e427-115">En créant un indicateur contextuel à l’aide du bouton Ajouter un indicateur à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="8e427-115">By creating a contextual indicator using the add indicator button from the file details page</span></span>
- <span data-ttu-id="8e427-116">En créant un indicateur via [l’API d’indicateur](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="8e427-116">By creating an indicator through the [Indicator API](ti-indicator.md)</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="8e427-117">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8e427-117">Before you begin</span></span>

<span data-ttu-id="8e427-118">Il est important de comprendre les conditions préalables suivantes avant de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="8e427-118">It's important to understand the following prerequisites prior to creating indicators for files:</span></span>

- <span data-ttu-id="8e427-119">Cette fonctionnalité est disponible si votre organisation utilise **Antivirus Microsoft Defender (en mode actif)** et si la protection basée sur **le cloud est activée.**</span><span class="sxs-lookup"><span data-stu-id="8e427-119">This feature is available if your organization uses **Microsoft Defender Antivirus (in active mode)** and **Cloud-based protection is enabled**.</span></span> <span data-ttu-id="8e427-120">Pour plus d’informations, [voir Gérer la protection basée sur le cloud.](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="8e427-120">For more information, see [Manage cloud-based protection](/windows/security/threat-protection/microsoft-defender-antivirus/deploy-manage-report-microsoft-defender-antivirus).</span></span>

- <span data-ttu-id="8e427-121">La version du client anti-programme malveillant doit être 4.18.1901.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8e427-121">The Antimalware client version must be 4.18.1901.x or later.</span></span> <span data-ttu-id="8e427-122">Voir [les versions mensuelles de la plateforme et du moteur](manage-updates-baselines-microsoft-defender-antivirus.md#monthly-platform-and-engine-versions)</span><span class="sxs-lookup"><span data-stu-id="8e427-122">See [Monthly platform and engine versions](manage-updates-baselines-microsoft-defender-antivirus.md#monthly-platform-and-engine-versions)</span></span>

- <span data-ttu-id="8e427-123">Pris en charge sur les appareils Windows 10, version 1703 ou ultérieure, Windows Server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="8e427-123">Supported on devices with Windows 10, version 1703 or later, Windows Server 2016 and 2019.</span></span>

- <span data-ttu-id="8e427-124">Pour commencer à bloquer les fichiers, vous devez d’abord [activer](advanced-features.md) la fonctionnalité « bloquer ou autoriser » dans Paramètres.</span><span class="sxs-lookup"><span data-stu-id="8e427-124">To start blocking files, you first need to [turn on the "block or allow" feature](advanced-features.md) in Settings.</span></span>

<span data-ttu-id="8e427-125">Cette fonctionnalité est conçue pour empêcher le téléchargement de programmes malveillants (ou de fichiers potentiellement malveillants) à partir du web.</span><span class="sxs-lookup"><span data-stu-id="8e427-125">This feature is designed to prevent suspected malware (or potentially malicious files) from being downloaded from the web.</span></span> <span data-ttu-id="8e427-126">Il prend actuellement en charge les fichiers exécutables portables(PE), notamment les fichiers .exe et .dll portables.</span><span class="sxs-lookup"><span data-stu-id="8e427-126">It currently supports portable executable (PE) files, including .exe and .dll files.</span></span> <span data-ttu-id="8e427-127">La couverture sera étendue au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="8e427-127">The coverage will be extended over time.</span></span>

## <a name="create-an-indicator-for-files-from-the-settings-page"></a><span data-ttu-id="8e427-128">Créer un indicateur pour les fichiers à partir de la page paramètres</span><span class="sxs-lookup"><span data-stu-id="8e427-128">Create an indicator for files from the settings page</span></span>

1. <span data-ttu-id="8e427-129">Dans le volet de navigation, sélectionnez **Paramètres > indicateurs.**</span><span class="sxs-lookup"><span data-stu-id="8e427-129">In the navigation pane, select **Settings > Indicators**.</span></span>

2. <span data-ttu-id="8e427-130">Sélectionnez **l’onglet De hachage de**   fichier.</span><span class="sxs-lookup"><span data-stu-id="8e427-130">Select the **File hash** tab.</span></span>

3. <span data-ttu-id="8e427-131">Sélectionnez **Ajouter un indicateur**.</span><span class="sxs-lookup"><span data-stu-id="8e427-131">Select **Add indicator**.</span></span>

4. <span data-ttu-id="8e427-132">Spécifiez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="8e427-132">Specify the following details:</span></span>
    - <span data-ttu-id="8e427-133">Indicateur : spécifiez les détails de l’entité et définissez l’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="8e427-133">Indicator - Specify the entity details and define the expiration of the indicator.</span></span>
    - <span data-ttu-id="8e427-134">Action : spécifiez l’action à prendre et fournissez une description.</span><span class="sxs-lookup"><span data-stu-id="8e427-134">Action - Specify the action to be taken and provide a description.</span></span>
    - <span data-ttu-id="8e427-135">Étendue : définir l’étendue du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="8e427-135">Scope - Define the scope of the device group.</span></span>

5. <span data-ttu-id="8e427-136">Examinez les détails dans l’onglet Résumé, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="8e427-136">Review the details in the Summary tab, then select **Save**.</span></span>

## <a name="create-a-contextual-indicator-from-the-file-details-page"></a><span data-ttu-id="8e427-137">Créer un indicateur contextuel à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="8e427-137">Create a contextual indicator from the file details page</span></span>

<span data-ttu-id="8e427-138">L’une des options lorsque vous prenez des mesures de réponse sur un [fichier consiste](respond-file-alerts.md)à ajouter un indicateur pour le   fichier.</span><span class="sxs-lookup"><span data-stu-id="8e427-138">One of the options when taking [response actions on a file](respond-file-alerts.md) is adding an indicator for the file.</span></span> <span data-ttu-id="8e427-139">Lorsque vous ajoutez un hachage d’indicateur pour un fichier, vous pouvez choisir de lancer une alerte et de bloquer le fichier chaque fois qu’un appareil de votre organisation tente de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="8e427-139">When you add an indicator hash for a file, you can choose to raise an alert and block the file whenever a device in your organization attempts to run it.</span></span>

<span data-ttu-id="8e427-140">Les fichiers automatiquement bloqués par un indicateur ne s’afficheront pas dans le centre de l’action du fichier, mais les alertes resteront visibles dans la file d’attente des alertes.</span><span class="sxs-lookup"><span data-stu-id="8e427-140">Files automatically blocked by an indicator won't show up in the file's Action center, but the alerts will still be visible in the Alerts queue.</span></span>

>[!IMPORTANT]
>- <span data-ttu-id="8e427-141">En règle générale, les blocs de fichiers sont appliqués et supprimés en quelques minutes, mais peuvent prendre plus de 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="8e427-141">Typically, file blocks are enforced and removed within a couple of minutes, but can take upwards of 30 minutes.</span></span>
>- <span data-ttu-id="8e427-142">S’il existe des stratégies d’indicateur de fichier en conflit, la stratégie d’application de la stratégie la plus sécurisée est appliquée.</span><span class="sxs-lookup"><span data-stu-id="8e427-142">If there are conflicting file indicator policies, the enforcement policy of the more secure policy is applied.</span></span> <span data-ttu-id="8e427-143">Par exemple, une stratégie d’indicateur de hachage de fichier SHA-256 est prioritaire sur une stratégie d’indicateur de hachage de fichier MD5 si les deux types de hachage définissent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="8e427-143">For example, a SHA-256 file hash indicator policy takes precedence over an MD5 file hash indicator policy if both hash types define the same file.</span></span>
>- <span data-ttu-id="8e427-144">Si la stratégie de groupe EnableFileHashComputation est désactivée, la précision de blocage du fichier IoC est réduite.</span><span class="sxs-lookup"><span data-stu-id="8e427-144">If EnableFileHashComputation group policy is disabled, the blocking accuracy of the file IoC is reduced.</span></span> <span data-ttu-id="8e427-145">Toutefois, l’activation de EnableFileHashComputation peut avoir un impact sur les performances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8e427-145">However, enabling EnableFileHashComputation may impact device performance.</span></span>
>    - <span data-ttu-id="8e427-146">Par exemple, la copie de fichiers de grande taille à partir d’un partage réseau sur votre appareil local, en particulier sur une connexion VPN, peut avoir un impact sur les performances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8e427-146">For example, copying large files from a network share onto your local device, especially over a VPN connection, may have an effect on device performance.</span></span>
>    - <span data-ttu-id="8e427-147">Pour plus d’informations sur la stratégie de groupe EnableFileHashComputation, voir [CSP Defender](/windows/client-management/mdm/defender-csp)</span><span class="sxs-lookup"><span data-stu-id="8e427-147">For more information about the EnableFileHashComputation group policy, see [Defender CSP](/windows/client-management/mdm/defender-csp)</span></span>

## <a name="policy-conflict-handling"></a><span data-ttu-id="8e427-148">Gestion des conflits de stratégie</span><span class="sxs-lookup"><span data-stu-id="8e427-148">Policy conflict handling</span></span>  

<span data-ttu-id="8e427-149">Le conflit de gestion des stratégies Cert et IoC de fichier suit l’ordre ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="8e427-149">Cert and File IoC policy handling conflict will follow the below order:</span></span>

- <span data-ttu-id="8e427-150">Si le fichier n’est pas autorisé par Windows Defender application Control et AppLocker appliquent des stratégies/stratégies de mode, **bloquez**</span><span class="sxs-lookup"><span data-stu-id="8e427-150">If the file is not allowed by Windows Defender Application Control and AppLocker enforce mode policy/policies, then **Block**</span></span>

- <span data-ttu-id="8e427-151">Sinon, si le fichier est autorisé par l’exclusion Antivirus Microsoft Defender, **autorisez**</span><span class="sxs-lookup"><span data-stu-id="8e427-151">Else if the file is allowed by the Microsoft Defender Antivirus exclusion, then **Allow**</span></span>

- <span data-ttu-id="8e427-152">Sinon, si le fichier est bloqué ou averti par un blocage ou un avertissement de fichier IoC, **puis Bloquer/Avertir**</span><span class="sxs-lookup"><span data-stu-id="8e427-152">Else if the file is blocked or warned by a block or warn file IoC, then **Block/Warn**</span></span>

- <span data-ttu-id="8e427-153">Sinon, si le fichier est autorisé par une stratégie IoC de fichier autorisé, **autorisez**</span><span class="sxs-lookup"><span data-stu-id="8e427-153">Else if the file is allowed by an allow file IoC policy, then **Allow**</span></span>

- <span data-ttu-id="8e427-154">Sinon, si le fichier est bloqué par les règles de la asr, LFA, AV, SmartScreen, puis **Bloquer**</span><span class="sxs-lookup"><span data-stu-id="8e427-154">Else if the file is blocked by ASR rules, CFA, AV, SmartScreen, then **Block**</span></span>  

- <span data-ttu-id="8e427-155">Else **Allow** (passe Windows Defender Application Control & AppLocker policy, no IoC rules apply to it)</span><span class="sxs-lookup"><span data-stu-id="8e427-155">Else **Allow** (passes Windows Defender Application Control & AppLocker policy, no IoC rules apply to it)</span></span>

<span data-ttu-id="8e427-156">S’il existe des stratégies IoC de fichier en conflit avec le même type d’application et la même cible, la stratégie de hachage le plus sécurisé (c’est-à-dire plus long) est appliquée.</span><span class="sxs-lookup"><span data-stu-id="8e427-156">If there are conflicting file IoC policies with the same enforcement type and target, the policy of the more secure (meaning longer) hash will be applied.</span></span> <span data-ttu-id="8e427-157">Par exemple, une stratégie IoC de hachage de fichier SHA-256 l’emporte sur une stratégie IoC de hachage de fichier MD5 si les deux types de hachage définissent le même fichier.</span><span class="sxs-lookup"><span data-stu-id="8e427-157">For example, a SHA-256 file hash IoC policy will win over a MD5 file hash IoC policy if both hash types define the same file.</span></span>

<span data-ttu-id="8e427-158">Notez que Gestion des menaces et des vulnérabilités’application de blocage vulnérable utilise les IOC de fichier pour l’application et suit l’ordre de gestion des conflits ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="8e427-158">Note that threat and vulnerability management's block vulnerable application features uses the file IoCs for enforcement and will follow the above conflict handling order.</span></span>

### <a name="examples"></a><span data-ttu-id="8e427-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="8e427-159">Examples</span></span>

|<span data-ttu-id="8e427-160">Composant</span><span class="sxs-lookup"><span data-stu-id="8e427-160">Component</span></span> |<span data-ttu-id="8e427-161">Application des composants</span><span class="sxs-lookup"><span data-stu-id="8e427-161">Component enforcement</span></span> |<span data-ttu-id="8e427-162">Action de l’indicateur de fichier</span><span class="sxs-lookup"><span data-stu-id="8e427-162">File indicator Action</span></span> |<span data-ttu-id="8e427-163">Résultat</span><span class="sxs-lookup"><span data-stu-id="8e427-163">Result</span></span>
|--|--|--|--|
|<span data-ttu-id="8e427-164">Exclusion du chemin d’accès au fichier de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="8e427-164">Attack surface reduction file path exclusion</span></span> |<span data-ttu-id="8e427-165">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-165">Allow</span></span> |<span data-ttu-id="8e427-166">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-166">Block</span></span> |<span data-ttu-id="8e427-167">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-167">Block</span></span>
|<span data-ttu-id="8e427-168">Règle de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="8e427-168">Attack surface reduction rule</span></span> |<span data-ttu-id="8e427-169">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-169">Block</span></span> |<span data-ttu-id="8e427-170">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-170">Allow</span></span> |<span data-ttu-id="8e427-171">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-171">Allow</span></span>
|<span data-ttu-id="8e427-172">Windows Defender Application Control</span><span class="sxs-lookup"><span data-stu-id="8e427-172">Windows Defender Application Control</span></span> |<span data-ttu-id="8e427-173">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-173">Allow</span></span> |<span data-ttu-id="8e427-174">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-174">Block</span></span> |<span data-ttu-id="8e427-175">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-175">Allow</span></span> |
|<span data-ttu-id="8e427-176">Windows Defender Application Control</span><span class="sxs-lookup"><span data-stu-id="8e427-176">Windows Defender Application Control</span></span> |<span data-ttu-id="8e427-177">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-177">Block</span></span> |<span data-ttu-id="8e427-178">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-178">Allow</span></span> |<span data-ttu-id="8e427-179">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-179">Block</span></span>
|<span data-ttu-id="8e427-180">Antivirus Microsoft Defender exclusion</span><span class="sxs-lookup"><span data-stu-id="8e427-180">Microsoft Defender Antivirus exclusion</span></span> |<span data-ttu-id="8e427-181">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-181">Allow</span></span> |<span data-ttu-id="8e427-182">Bloquer</span><span class="sxs-lookup"><span data-stu-id="8e427-182">Block</span></span> |<span data-ttu-id="8e427-183">Autoriser</span><span class="sxs-lookup"><span data-stu-id="8e427-183">Allow</span></span>

## <a name="see-also"></a><span data-ttu-id="8e427-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e427-184">See also</span></span>

- [<span data-ttu-id="8e427-185">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="8e427-185">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="8e427-186">Créer des indicateurs pour les IP et URL/domaines</span><span class="sxs-lookup"><span data-stu-id="8e427-186">Create indicators for IPs and URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="8e427-187">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="8e427-187">Create indicators based on certificates</span></span>](indicator-certificates.md)
- [<span data-ttu-id="8e427-188">Gérer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="8e427-188">Manage indicators</span></span>](indicator-manage.md)
