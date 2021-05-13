---
title: Définir des préférences pour Microsoft Defender pour le point de terminaison sur Linux
ms.reviewer: ''
description: Décrit comment configurer Microsoft Defender pour endpoint sur Linux dans les entreprises.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, installation, déployer, désinstallation, préinstallation, ansible, linux, redhat, ubuntu, debian, sles, suse, centos
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 29505a6e975fdfa2283efe3391c615e40e678164
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52346377"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="b2447-104">Définir des préférences pour Microsoft Defender pour le point de terminaison sur Linux</span><span class="sxs-lookup"><span data-stu-id="b2447-104">Set preferences for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b2447-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b2447-105">**Applies to:**</span></span>
- [<span data-ttu-id="b2447-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b2447-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b2447-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b2447-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b2447-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b2447-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="b2447-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b2447-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

>[!IMPORTANT]
><span data-ttu-id="b2447-110">Cette rubrique contient des instructions sur la façon de définir des préférences pour Defender pour Endpoint sur Linux dans les environnements d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b2447-110">This topic contains instructions for how to set preferences for Defender for Endpoint on Linux in enterprise environments.</span></span> <span data-ttu-id="b2447-111">Si vous souhaitez configurer le produit sur un appareil à partir de la ligne de commande, consultez [Ressources.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="b2447-111">If you are interested in configuring the product on a device from the command-line, see [Resources](linux-resources.md#configure-from-the-command-line).</span></span>

<span data-ttu-id="b2447-112">Dans les environnements d’entreprise, Defender pour Point de terminaison sur Linux peut être géré via un profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="b2447-112">In enterprise environments, Defender for Endpoint on Linux can be managed through a configuration profile.</span></span> <span data-ttu-id="b2447-113">Ce profil est déployé à partir de l’outil de gestion de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b2447-113">This profile is deployed from the management tool of your choice.</span></span> <span data-ttu-id="b2447-114">Les préférences gérées par l’entreprise prévalent sur les préférences définies localement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2447-114">Preferences managed by the enterprise take precedence over the ones set locally on the device.</span></span> <span data-ttu-id="b2447-115">En d’autres termes, les utilisateurs de votre entreprise ne peuvent pas modifier les préférences définies par le biais de ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="b2447-115">In other words, users in your enterprise are not able to change preferences that are set through this configuration profile.</span></span>

<span data-ttu-id="b2447-116">Cet article décrit la structure de ce profil (y compris un profil recommandé que vous pouvez utiliser pour commencer) et des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="b2447-116">This article describes the structure of this profile (including a recommended profile that you can use to get started) and instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="b2447-117">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b2447-117">Configuration profile structure</span></span>

<span data-ttu-id="b2447-118">Le profil de configuration est un fichier .json qui se compose d’entrées identifiées par une clé (qui indique le nom de la préférence), suivi d’une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="b2447-118">The configuration profile is a .json file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="b2447-119">Les valeurs peuvent être simples, telles qu’une valeur numérique, ou complexes, telles qu’une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="b2447-119">Values can be simple, such as a numerical value, or complex, such as a nested list of preferences.</span></span>

<span data-ttu-id="b2447-120">En règle générale, vous utilisez un outil de gestion de la configuration pour pousser un fichier avec le nom ```mdatp_managed.json``` à l’emplacement ```/etc/opt/microsoft/mdatp/managed/``` .</span><span class="sxs-lookup"><span data-stu-id="b2447-120">Typically, you would use a configuration management tool to push a file with the name ```mdatp_managed.json``` at the location ```/etc/opt/microsoft/mdatp/managed/```.</span></span>

<span data-ttu-id="b2447-121">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l’échelle du produit pour les sous-catégories du produit, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2447-121">The top level of the configuration profile includes product-wide preferences and entries for subareas of the product, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="b2447-122">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="b2447-122">Antivirus engine preferences</span></span>

<span data-ttu-id="b2447-123">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus du produit.</span><span class="sxs-lookup"><span data-stu-id="b2447-123">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-124">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-124">**Key**</span></span> | <span data-ttu-id="b2447-125">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="b2447-125">antivirusEngine</span></span> |
| <span data-ttu-id="b2447-126">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-126">**Data type**</span></span> | <span data-ttu-id="b2447-127">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b2447-127">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b2447-128">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-128">**Comments**</span></span> | <span data-ttu-id="b2447-129">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b2447-129">See the following sections for a description of the dictionary contents.</span></span> |
|||

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="b2447-130">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="b2447-130">Enable / disable real-time protection</span></span>

<span data-ttu-id="b2447-131">Détermine si la protection en temps réel (analyser les fichiers à mesure qu’ils sont accessibles) est activée ou non.</span><span class="sxs-lookup"><span data-stu-id="b2447-131">Determines whether real-time protection (scan files as they are accessed) is enabled or not.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-132">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-132">**Key**</span></span> | <span data-ttu-id="b2447-133">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="b2447-133">enableRealTimeProtection</span></span> |
| <span data-ttu-id="b2447-134">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-134">**Data type**</span></span> | <span data-ttu-id="b2447-135">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b2447-135">Boolean</span></span> |
| <span data-ttu-id="b2447-136">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-136">**Possible values**</span></span> | <span data-ttu-id="b2447-137">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-137">true (default)</span></span> <br/> <span data-ttu-id="b2447-138">false</span><span class="sxs-lookup"><span data-stu-id="b2447-138">false</span></span> |
|||

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="b2447-139">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="b2447-139">Enable / disable passive mode</span></span>

<span data-ttu-id="b2447-140">Détermine si le moteur antivirus s’exécute en mode passif ou non.</span><span class="sxs-lookup"><span data-stu-id="b2447-140">Determines whether the antivirus engine runs in passive mode or not.</span></span> <span data-ttu-id="b2447-141">En mode passif :</span><span class="sxs-lookup"><span data-stu-id="b2447-141">In passive mode:</span></span>
- <span data-ttu-id="b2447-142">La protection en temps réel est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b2447-142">Real-time protection is turned off.</span></span>
- <span data-ttu-id="b2447-143">L’analyse à la demande est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b2447-143">On-demand scanning is turned on.</span></span>
- <span data-ttu-id="b2447-144">La correction automatique des menaces est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b2447-144">Automatic threat remediation is turned off.</span></span>
- <span data-ttu-id="b2447-145">Les mises à jour de l’intelligence de la sécurité sont allumées.</span><span class="sxs-lookup"><span data-stu-id="b2447-145">Security intelligence updates are turned on.</span></span>
- <span data-ttu-id="b2447-146">L’icône du menu État est masquée.</span><span class="sxs-lookup"><span data-stu-id="b2447-146">Status menu icon is hidden.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-147">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-147">**Key**</span></span> | <span data-ttu-id="b2447-148">passiveMode</span><span class="sxs-lookup"><span data-stu-id="b2447-148">passiveMode</span></span> |
| <span data-ttu-id="b2447-149">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-149">**Data type**</span></span> | <span data-ttu-id="b2447-150">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b2447-150">Boolean</span></span> |
| <span data-ttu-id="b2447-151">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-151">**Possible values**</span></span> | <span data-ttu-id="b2447-152">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-152">false (default)</span></span> <br/> <span data-ttu-id="b2447-153">true</span><span class="sxs-lookup"><span data-stu-id="b2447-153">true</span></span> |
| <span data-ttu-id="b2447-154">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-154">**Comments**</span></span> | <span data-ttu-id="b2447-155">Disponible dans Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-155">Available in Defender for Endpoint version 100.67.60 or higher.</span></span> |
|||

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="b2447-156">Stratégie de fusion d’exclusions</span><span class="sxs-lookup"><span data-stu-id="b2447-156">Exclusion merge policy</span></span>

<span data-ttu-id="b2447-157">Spécifie la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="b2447-157">Specifies the merge policy for exclusions.</span></span> <span data-ttu-id="b2447-158">Il peut s’agit d’une combinaison d’exclusions définies par l’administrateur et d’exclusions définies par l’utilisateur ( ) ou uniquement `merge` d’exclusions définies par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="b2447-158">It can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="b2447-159">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="b2447-159">This setting can be used to restrict local users from defining their own exclusions.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-160">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-160">**Key**</span></span> | <span data-ttu-id="b2447-161">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="b2447-161">exclusionsMergePolicy</span></span> |
| <span data-ttu-id="b2447-162">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-162">**Data type**</span></span> | <span data-ttu-id="b2447-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-163">String</span></span> |
| <span data-ttu-id="b2447-164">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-164">**Possible values**</span></span> | <span data-ttu-id="b2447-165">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-165">merge (default)</span></span> <br/> <span data-ttu-id="b2447-166">admin_only</span><span class="sxs-lookup"><span data-stu-id="b2447-166">admin_only</span></span> |
| <span data-ttu-id="b2447-167">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-167">**Comments**</span></span> | <span data-ttu-id="b2447-168">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-168">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |
|||

#### <a name="scan-exclusions"></a><span data-ttu-id="b2447-169">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="b2447-169">Scan exclusions</span></span>

<span data-ttu-id="b2447-170">Entités exclues de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b2447-170">Entities that have been excluded from the scan.</span></span> <span data-ttu-id="b2447-171">Les exclusions peuvent être spécifiées par des chemins d’accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b2447-171">Exclusions can be specified by full paths, extensions, or file names.</span></span>
<span data-ttu-id="b2447-172">(Les exclusions sont spécifiées en tant que tableau d’éléments, l’administrateur peut spécifier autant d’éléments que nécessaire, dans n’importe quel ordre.)</span><span class="sxs-lookup"><span data-stu-id="b2447-172">(Exclusions are specified as an array of items, administrator can specify as many elements as necessary, in any order.)</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-173">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-173">**Key**</span></span> | <span data-ttu-id="b2447-174">exclusions</span><span class="sxs-lookup"><span data-stu-id="b2447-174">exclusions</span></span> |
| <span data-ttu-id="b2447-175">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-175">**Data type**</span></span> | <span data-ttu-id="b2447-176">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b2447-176">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b2447-177">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-177">**Comments**</span></span> | <span data-ttu-id="b2447-178">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b2447-178">See the following sections for a description of the dictionary contents.</span></span> |
|||

<span data-ttu-id="b2447-179">**Type d’exclusion**</span><span class="sxs-lookup"><span data-stu-id="b2447-179">**Type of exclusion**</span></span>

<span data-ttu-id="b2447-180">Spécifie le type de contenu exclu de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b2447-180">Specifies the type of content excluded from the scan.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-181">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-181">**Key**</span></span> | <span data-ttu-id="b2447-182">$type</span><span class="sxs-lookup"><span data-stu-id="b2447-182">$type</span></span> |
| <span data-ttu-id="b2447-183">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-183">**Data type**</span></span> | <span data-ttu-id="b2447-184">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-184">String</span></span> |
| <span data-ttu-id="b2447-185">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-185">**Possible values**</span></span> | <span data-ttu-id="b2447-186">excludedPath</span><span class="sxs-lookup"><span data-stu-id="b2447-186">excludedPath</span></span> <br/> <span data-ttu-id="b2447-187">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="b2447-187">excludedFileExtension</span></span> <br/> <span data-ttu-id="b2447-188">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="b2447-188">excludedFileName</span></span> |
|||

<span data-ttu-id="b2447-189">**Chemin d’accès au contenu exclu**</span><span class="sxs-lookup"><span data-stu-id="b2447-189">**Path to excluded content**</span></span>

<span data-ttu-id="b2447-190">Utilisé pour exclure le contenu de l’analyse par chemin d’accès complet au fichier.</span><span class="sxs-lookup"><span data-stu-id="b2447-190">Used to exclude content from the scan by full file path.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-191">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-191">**Key**</span></span> | <span data-ttu-id="b2447-192">chemin</span><span class="sxs-lookup"><span data-stu-id="b2447-192">path</span></span> |
| <span data-ttu-id="b2447-193">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-193">**Data type**</span></span> | <span data-ttu-id="b2447-194">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-194">String</span></span> |
| <span data-ttu-id="b2447-195">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-195">**Possible values**</span></span> | <span data-ttu-id="b2447-196">chemins d’accès valides</span><span class="sxs-lookup"><span data-stu-id="b2447-196">valid paths</span></span> |
| <span data-ttu-id="b2447-197">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-197">**Comments**</span></span> | <span data-ttu-id="b2447-198">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="b2447-198">Applicable only if *$type* is *excludedPath*</span></span> |
|||

<span data-ttu-id="b2447-199">**Type de chemin d’accès (fichier/répertoire)**</span><span class="sxs-lookup"><span data-stu-id="b2447-199">**Path type (file / directory)**</span></span>

<span data-ttu-id="b2447-200">Indique si la propriété *du chemin d’accès* fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b2447-200">Indicates if the *path* property refers to a file or directory.</span></span> 

|||
|:---|:---|
| <span data-ttu-id="b2447-201">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-201">**Key**</span></span> | <span data-ttu-id="b2447-202">isDirectory</span><span class="sxs-lookup"><span data-stu-id="b2447-202">isDirectory</span></span> |
| <span data-ttu-id="b2447-203">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-203">**Data type**</span></span> | <span data-ttu-id="b2447-204">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b2447-204">Boolean</span></span> |
| <span data-ttu-id="b2447-205">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-205">**Possible values**</span></span> | <span data-ttu-id="b2447-206">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-206">false (default)</span></span> <br/> <span data-ttu-id="b2447-207">true</span><span class="sxs-lookup"><span data-stu-id="b2447-207">true</span></span> |
| <span data-ttu-id="b2447-208">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-208">**Comments**</span></span> | <span data-ttu-id="b2447-209">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="b2447-209">Applicable only if *$type* is *excludedPath*</span></span> |
|||

<span data-ttu-id="b2447-210">**Extension de fichier exclue de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="b2447-210">**File extension excluded from the scan**</span></span>

<span data-ttu-id="b2447-211">Utilisé pour exclure le contenu de l’analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="b2447-211">Used to exclude content from the scan by file extension.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-212">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-212">**Key**</span></span> | <span data-ttu-id="b2447-213">extension</span><span class="sxs-lookup"><span data-stu-id="b2447-213">extension</span></span> |
| <span data-ttu-id="b2447-214">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-214">**Data type**</span></span> | <span data-ttu-id="b2447-215">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-215">String</span></span> |
| <span data-ttu-id="b2447-216">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-216">**Possible values**</span></span> | <span data-ttu-id="b2447-217">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="b2447-217">valid file extensions</span></span> |
| <span data-ttu-id="b2447-218">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-218">**Comments**</span></span> | <span data-ttu-id="b2447-219">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="b2447-219">Applicable only if *$type* is *excludedFileExtension*</span></span> |
|||

<span data-ttu-id="b2447-220">**Processus exclu de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="b2447-220">**Process excluded from the scan**</span></span>

<span data-ttu-id="b2447-221">Spécifie un processus pour lequel toute l’activité de fichier est exclue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b2447-221">Specifies a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="b2447-222">Le processus peut être spécifié par son nom (par exemple) ou son chemin `cat` d’accès complet (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="b2447-222">The process can be specified either by its name (for example, `cat`) or full path (for example, `/bin/cat`).</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-223">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-223">**Key**</span></span> | <span data-ttu-id="b2447-224">name</span><span class="sxs-lookup"><span data-stu-id="b2447-224">name</span></span> |
| <span data-ttu-id="b2447-225">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-225">**Data type**</span></span> | <span data-ttu-id="b2447-226">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-226">String</span></span> |
| <span data-ttu-id="b2447-227">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-227">**Possible values**</span></span> | <span data-ttu-id="b2447-228">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-228">any string</span></span> |
| <span data-ttu-id="b2447-229">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-229">**Comments**</span></span> | <span data-ttu-id="b2447-230">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="b2447-230">Applicable only if *$type* is *excludedFileName*</span></span> |
|||

#### <a name="allowed-threats"></a><span data-ttu-id="b2447-231">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="b2447-231">Allowed threats</span></span>

<span data-ttu-id="b2447-232">Liste des menaces (identifiées par leur nom) qui ne sont pas bloquées par le produit et sont autorisées à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="b2447-232">List of threats (identified by their name) that are not blocked by the product and are instead allowed to run.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-233">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-233">**Key**</span></span> | <span data-ttu-id="b2447-234">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="b2447-234">allowedThreats</span></span> |
| <span data-ttu-id="b2447-235">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-235">**Data type**</span></span> | <span data-ttu-id="b2447-236">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="b2447-236">Array of strings</span></span> |
|||

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="b2447-237">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="b2447-237">Disallowed threat actions</span></span>

<span data-ttu-id="b2447-238">Limite les actions que l’utilisateur local d’un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="b2447-238">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="b2447-239">Les actions incluses dans cette liste ne sont pas affichées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2447-239">The actions included in this list are not displayed in the user interface.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-240">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-240">**Key**</span></span> | <span data-ttu-id="b2447-241">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="b2447-241">disallowedThreatActions</span></span> |
| <span data-ttu-id="b2447-242">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-242">**Data type**</span></span> | <span data-ttu-id="b2447-243">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="b2447-243">Array of strings</span></span> |
| <span data-ttu-id="b2447-244">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-244">**Possible values**</span></span> | <span data-ttu-id="b2447-245">autoriser (empêche les utilisateurs d’autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="b2447-245">allow (restricts users from allowing threats)</span></span> <br/> <span data-ttu-id="b2447-246">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="b2447-246">restore (restricts users from restoring threats from the quarantine)</span></span> |
| <span data-ttu-id="b2447-247">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-247">**Comments**</span></span> | <span data-ttu-id="b2447-248">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-248">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |
|||

#### <a name="threat-type-settings"></a><span data-ttu-id="b2447-249">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="b2447-249">Threat type settings</span></span>

<span data-ttu-id="b2447-250">La *préférence threatTypeSettings dans* le moteur antivirus est utilisée pour contrôler la façon dont certains types de menaces sont gérés par le produit.</span><span class="sxs-lookup"><span data-stu-id="b2447-250">The *threatTypeSettings* preference in the antivirus engine is used to control how certain threat types are handled by the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-251">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-251">**Key**</span></span> | <span data-ttu-id="b2447-252">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="b2447-252">threatTypeSettings</span></span> |
| <span data-ttu-id="b2447-253">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-253">**Data type**</span></span> | <span data-ttu-id="b2447-254">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b2447-254">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b2447-255">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-255">**Comments**</span></span> | <span data-ttu-id="b2447-256">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b2447-256">See the following sections for a description of the dictionary contents.</span></span> |
|||

<span data-ttu-id="b2447-257">**Type de menace**</span><span class="sxs-lookup"><span data-stu-id="b2447-257">**Threat type**</span></span>

<span data-ttu-id="b2447-258">Type de menace pour lequel le comportement est configuré.</span><span class="sxs-lookup"><span data-stu-id="b2447-258">Type of threat for which the behavior is configured.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-259">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-259">**Key**</span></span> | <span data-ttu-id="b2447-260">clé</span><span class="sxs-lookup"><span data-stu-id="b2447-260">key</span></span> |
| <span data-ttu-id="b2447-261">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-261">**Data type**</span></span> | <span data-ttu-id="b2447-262">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-262">String</span></span> |
| <span data-ttu-id="b2447-263">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-263">**Possible values**</span></span> | <span data-ttu-id="b2447-264">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="b2447-264">potentially_unwanted_application</span></span> <br/> <span data-ttu-id="b2447-265">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="b2447-265">archive_bomb</span></span> |
|||

<span data-ttu-id="b2447-266">**Mesures à prendre**</span><span class="sxs-lookup"><span data-stu-id="b2447-266">**Action to take**</span></span>

<span data-ttu-id="b2447-267">Action à prendre en cas de menace du type spécifié dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="b2447-267">Action to take when coming across a threat of the type specified in the preceding section.</span></span> <span data-ttu-id="b2447-268">Peut être :</span><span class="sxs-lookup"><span data-stu-id="b2447-268">Can be:</span></span>

- <span data-ttu-id="b2447-269">**Audit**: l’appareil n’est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="b2447-269">**Audit**: The device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="b2447-270">**Bloc**: l’appareil est protégé contre ce type de menace et vous êtes averti dans la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b2447-270">**Block**: The device is protected against this type of threat and you are notified in the security console.</span></span>
- <span data-ttu-id="b2447-271">**Off**: l’appareil n’est pas protégé contre ce type de menace et rien n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="b2447-271">**Off**: The device is not protected against this type of threat and nothing is logged.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-272">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-272">**Key**</span></span> | <span data-ttu-id="b2447-273">valeur</span><span class="sxs-lookup"><span data-stu-id="b2447-273">value</span></span> |
| <span data-ttu-id="b2447-274">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-274">**Data type**</span></span> | <span data-ttu-id="b2447-275">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-275">String</span></span> |
| <span data-ttu-id="b2447-276">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-276">**Possible values**</span></span> | <span data-ttu-id="b2447-277">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-277">audit (default)</span></span> <br/> <span data-ttu-id="b2447-278">block</span><span class="sxs-lookup"><span data-stu-id="b2447-278">block</span></span> <br/> <span data-ttu-id="b2447-279">off</span><span class="sxs-lookup"><span data-stu-id="b2447-279">off</span></span> |
|||

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="b2447-280">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="b2447-280">Threat type settings merge policy</span></span>

<span data-ttu-id="b2447-281">Spécifie la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="b2447-281">Specifies the merge policy for threat type settings.</span></span> <span data-ttu-id="b2447-282">Il peut s’agit d’une combinaison de paramètres définis par l’administrateur et de paramètres définis par l’utilisateur ( ) ou uniquement de `merge` paramètres définis par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="b2447-282">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="b2447-283">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="b2447-283">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-284">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-284">**Key**</span></span> | <span data-ttu-id="b2447-285">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="b2447-285">threatTypeSettingsMergePolicy</span></span> |
| <span data-ttu-id="b2447-286">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-286">**Data type**</span></span> | <span data-ttu-id="b2447-287">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-287">String</span></span> |
| <span data-ttu-id="b2447-288">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-288">**Possible values**</span></span> | <span data-ttu-id="b2447-289">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-289">merge (default)</span></span> <br/> <span data-ttu-id="b2447-290">admin_only</span><span class="sxs-lookup"><span data-stu-id="b2447-290">admin_only</span></span> |
| <span data-ttu-id="b2447-291">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-291">**Comments**</span></span> | <span data-ttu-id="b2447-292">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-292">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |
|||

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="b2447-293">Conservation de l’historique d’analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="b2447-293">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="b2447-294">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l’historique d’analyse sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2447-294">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="b2447-295">Les anciens résultats d’analyse sont supprimés de l’historique.</span><span class="sxs-lookup"><span data-stu-id="b2447-295">Old scan results are removed from the history.</span></span> <span data-ttu-id="b2447-296">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="b2447-296">Old quarantined files that are also removed from the disk.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-297">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-297">**Key**</span></span> | <span data-ttu-id="b2447-298">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="b2447-298">scanResultsRetentionDays</span></span> |
| <span data-ttu-id="b2447-299">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-299">**Data type**</span></span> | <span data-ttu-id="b2447-300">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-300">String</span></span> |
| <span data-ttu-id="b2447-301">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-301">**Possible values**</span></span> | <span data-ttu-id="b2447-302">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b2447-302">90 (default).</span></span> <span data-ttu-id="b2447-303">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="b2447-303">Allowed values are from 1 day to 180 days.</span></span> |
| <span data-ttu-id="b2447-304">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-304">**Comments**</span></span> | <span data-ttu-id="b2447-305">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-305">Available in Defender for Endpoint version 101.04.76 or higher.</span></span> |
|||

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="b2447-306">Nombre maximal d’éléments dans l’historique d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="b2447-306">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="b2447-307">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="b2447-307">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="b2447-308">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="b2447-308">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-309">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-309">**Key**</span></span> | <span data-ttu-id="b2447-310">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="b2447-310">scanHistoryMaximumItems</span></span> |
| <span data-ttu-id="b2447-311">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-311">**Data type**</span></span> | <span data-ttu-id="b2447-312">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-312">String</span></span> |
| <span data-ttu-id="b2447-313">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-313">**Possible values**</span></span> | <span data-ttu-id="b2447-314">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b2447-314">10000 (default).</span></span> <span data-ttu-id="b2447-315">Les valeurs autorisées sont de 5 000 à 1 5 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="b2447-315">Allowed values are from 5000 items to 15000 items.</span></span> |
| <span data-ttu-id="b2447-316">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-316">**Comments**</span></span> | <span data-ttu-id="b2447-317">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b2447-317">Available in Defender for Endpoint version 101.04.76 or higher.</span></span> |
|||

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="b2447-318">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="b2447-318">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="b2447-319">*L’entrée cloudService* dans le profil de configuration est utilisée pour configurer la fonctionnalité de protection pilotée par le cloud du produit.</span><span class="sxs-lookup"><span data-stu-id="b2447-319">The *cloudService* entry in the configuration profile is used to configure the cloud-driven protection feature of the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-320">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-320">**Key**</span></span> | <span data-ttu-id="b2447-321">cloudService</span><span class="sxs-lookup"><span data-stu-id="b2447-321">cloudService</span></span> |
| <span data-ttu-id="b2447-322">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-322">**Data type**</span></span> | <span data-ttu-id="b2447-323">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b2447-323">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b2447-324">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="b2447-324">**Comments**</span></span> | <span data-ttu-id="b2447-325">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b2447-325">See the following sections for a description of the dictionary contents.</span></span> |
|||

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="b2447-326">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b2447-326">Enable / disable cloud delivered protection</span></span>

<span data-ttu-id="b2447-327">Détermine si la protection cloud est activée ou non sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2447-327">Determines whether cloud-delivered protection is enabled on the device or not.</span></span> <span data-ttu-id="b2447-328">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="b2447-328">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-329">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-329">**Key**</span></span> | <span data-ttu-id="b2447-330">activé</span><span class="sxs-lookup"><span data-stu-id="b2447-330">enabled</span></span> |
| <span data-ttu-id="b2447-331">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-331">**Data type**</span></span> | <span data-ttu-id="b2447-332">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b2447-332">Boolean</span></span> |
| <span data-ttu-id="b2447-333">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-333">**Possible values**</span></span> | <span data-ttu-id="b2447-334">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-334">true (default)</span></span> <br/> <span data-ttu-id="b2447-335">false</span><span class="sxs-lookup"><span data-stu-id="b2447-335">false</span></span> |
|||

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="b2447-336">Niveau de collecte de diagnostics</span><span class="sxs-lookup"><span data-stu-id="b2447-336">Diagnostic collection level</span></span>

<span data-ttu-id="b2447-337">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="b2447-337">Diagnostic data is used to keep Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="b2447-338">Ce paramètre détermine le niveau de diagnostics envoyés par le produit à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2447-338">This setting determines the level of diagnostics sent by the product to Microsoft.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-339">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-339">**Key**</span></span> | <span data-ttu-id="b2447-340">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="b2447-340">diagnosticLevel</span></span> |
| <span data-ttu-id="b2447-341">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-341">**Data type**</span></span> | <span data-ttu-id="b2447-342">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-342">String</span></span> |
| <span data-ttu-id="b2447-343">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-343">**Possible values**</span></span> | <span data-ttu-id="b2447-344">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-344">optional (default)</span></span> <br/> <span data-ttu-id="b2447-345">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b2447-345">required</span></span> |
|||

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="b2447-346">Activer/désactiver les envois automatiques d’échantillons</span><span class="sxs-lookup"><span data-stu-id="b2447-346">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="b2447-347">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2447-347">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="b2447-348">Il existe trois niveaux pour contrôler l’envoi d’échantillons :</span><span class="sxs-lookup"><span data-stu-id="b2447-348">There are three levels for controlling sample submission:</span></span>

- <span data-ttu-id="b2447-349">**Aucun**: aucun échantillon suspect n’est envoyé à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2447-349">**None**: no suspicious samples are submitted to Microsoft.</span></span>
- <span data-ttu-id="b2447-350">**Sécurisé**: seuls les échantillons suspects qui ne contiennent pas d’informations d’identification personnelle (PII) sont envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b2447-350">**Safe**: only suspicious samples that do not contain personally identifiable information (PII) are submitted automatically.</span></span> <span data-ttu-id="b2447-351">Il s’agit de la valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b2447-351">This is the default value for this setting.</span></span>
- <span data-ttu-id="b2447-352">**Tous**: tous les échantillons suspects sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b2447-352">**All**: all suspicious samples are submitted to Microsoft.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-353">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-353">**Key**</span></span> | <span data-ttu-id="b2447-354">automaticSampleSubmissionConsent</span><span class="sxs-lookup"><span data-stu-id="b2447-354">automaticSampleSubmissionConsent</span></span> |
| <span data-ttu-id="b2447-355">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-355">**Data type**</span></span> | <span data-ttu-id="b2447-356">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b2447-356">String</span></span> |
| <span data-ttu-id="b2447-357">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-357">**Possible values**</span></span> | <span data-ttu-id="b2447-358">aucune</span><span class="sxs-lookup"><span data-stu-id="b2447-358">none</span></span> <br/> <span data-ttu-id="b2447-359">safe (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-359">safe (default)</span></span> <br/> <span data-ttu-id="b2447-360">all</span><span class="sxs-lookup"><span data-stu-id="b2447-360">all</span></span> |
|||

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="b2447-361">Activer/désactiver les mises à jour automatiques de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="b2447-361">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="b2447-362">Détermine si les mises à jour d’informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="b2447-362">Determines whether security intelligence updates are installed automatically:</span></span>

|||
|:---|:---|
| <span data-ttu-id="b2447-363">**Key**</span><span class="sxs-lookup"><span data-stu-id="b2447-363">**Key**</span></span> | <span data-ttu-id="b2447-364">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="b2447-364">automaticDefinitionUpdateEnabled</span></span> |
| <span data-ttu-id="b2447-365">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b2447-365">**Data type**</span></span> | <span data-ttu-id="b2447-366">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b2447-366">Boolean</span></span> |
| <span data-ttu-id="b2447-367">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b2447-367">**Possible values**</span></span> | <span data-ttu-id="b2447-368">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b2447-368">true (default)</span></span> <br/> <span data-ttu-id="b2447-369">false</span><span class="sxs-lookup"><span data-stu-id="b2447-369">false</span></span> |
|||

## <a name="recommended-configuration-profile"></a><span data-ttu-id="b2447-370">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="b2447-370">Recommended configuration profile</span></span>

<span data-ttu-id="b2447-371">Pour commencer, nous recommandons le profil de configuration suivant pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="b2447-371">To get started, we recommend the following configuration profile for your enterprise to take advantage of all protection features that Defender for Endpoint provides.</span></span>

<span data-ttu-id="b2447-372">Le profil de configuration suivant :</span><span class="sxs-lookup"><span data-stu-id="b2447-372">The following configuration profile will:</span></span>

- <span data-ttu-id="b2447-373">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="b2447-373">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="b2447-374">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="b2447-374">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="b2447-375">**Les applications potentiellement indésirables (PUA) sont** bloquées</span><span class="sxs-lookup"><span data-stu-id="b2447-375">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="b2447-376">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans les journaux du produit</span><span class="sxs-lookup"><span data-stu-id="b2447-376">**Archive bombs** (file with a high compression rate) are audited to the product logs</span></span>
- <span data-ttu-id="b2447-377">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="b2447-377">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="b2447-378">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="b2447-378">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="b2447-379">Activer l’envoi automatique d’échantillons au `safe` niveau</span><span class="sxs-lookup"><span data-stu-id="b2447-379">Enable automatic sample submission at `safe` level</span></span>

### <a name="sample-profile"></a><span data-ttu-id="b2447-380">Exemple de profil</span><span class="sxs-lookup"><span data-stu-id="b2447-380">Sample profile</span></span>

```JSON
{
   "antivirusEngine":{
      "enableRealTimeProtection":true,
      "threatTypeSettings":[
         {
            "key":"potentially_unwanted_application",
            "value":"block"
         },
         {
            "key":"archive_bomb",
            "value":"audit"
         }
      ]
   },
   "cloudService":{
      "automaticDefinitionUpdateEnabled":true,
      "automaticSampleSubmissionConsent":"safe",
      "enabled":true,
      "proxy":"http://proxy.server:port/"
   }
}
```

## <a name="full-configuration-profile-example"></a><span data-ttu-id="b2447-381">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="b2447-381">Full configuration profile example</span></span>

<span data-ttu-id="b2447-382">Le profil de configuration suivant contient des entrées pour tous les paramètres décrits dans ce document et peut être utilisé pour des scénarios plus avancés où vous souhaitez contrôler davantage le produit.</span><span class="sxs-lookup"><span data-stu-id="b2447-382">The following configuration profile contains entries for all settings described in this document and can be used for more advanced scenarios where you want more control over the product.</span></span>

### <a name="full-profile"></a><span data-ttu-id="b2447-383">Profil complet</span><span class="sxs-lookup"><span data-stu-id="b2447-383">Full profile</span></span>

```JSON
{
   "antivirusEngine":{
      "enableRealTimeProtection":true,
      "passiveMode":false,
      "exclusionsMergePolicy":"merge",
      "exclusions":[
         {
            "$type":"excludedPath",
            "isDirectory":false,
            "path":"/var/log/system.log"
         },
         {
            "$type":"excludedPath",
            "isDirectory":true,
            "path":"/run"
         },
         {
            "$type":"excludedPath",
            "isDirectory":true,
            "path":"/home/*/git"
         },
         {
            "$type":"excludedFileExtension",
            "extension":"pdf"
         },
         {
            "$type":"excludedFileName",
            "name":"cat"
         }
      ],
      "allowedThreats":[
         "EICAR-Test-File (not a virus)"
      ],
      "disallowedThreatActions":[
         "allow",
         "restore"
      ],
      "threatTypeSettingsMergePolicy":"merge",
      "threatTypeSettings":[
         {
            "key":"potentially_unwanted_application",
            "value":"block"
         },
         {
            "key":"archive_bomb",
            "value":"audit"
         }
      ]
   },
   "cloudService":{
      "enabled":true,
      "diagnosticLevel":"optional",
      "automaticSampleSubmissionConsent":"safe",
      "automaticDefinitionUpdateEnabled":true,
      "proxy": "http://proxy.server:port/"
   }
}
```

## <a name="configuration-profile-validation"></a><span data-ttu-id="b2447-384">Validation du profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b2447-384">Configuration profile validation</span></span>

<span data-ttu-id="b2447-385">Le profil de configuration doit être un fichier au format JSON valide.</span><span class="sxs-lookup"><span data-stu-id="b2447-385">The configuration profile must be a valid JSON-formatted file.</span></span> <span data-ttu-id="b2447-386">Il existe un certain nombre d’outils qui peuvent être utilisés pour vérifier cela.</span><span class="sxs-lookup"><span data-stu-id="b2447-386">There are a number of tools that can be used to verify this.</span></span> <span data-ttu-id="b2447-387">Par exemple, si vous avez `python` installé sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="b2447-387">For example, if you have `python` installed on your device:</span></span>

```bash
python -m json.tool mdatp_managed.json
```

<span data-ttu-id="b2447-388">Si le JSON est bien formé, la commande ci-dessus le renvoie au Terminal et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="b2447-388">If the JSON is well-formed, the above command outputs it back to the Terminal and returns an exit code of `0`.</span></span> <span data-ttu-id="b2447-389">Sinon, une erreur qui décrit le problème s’affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="b2447-389">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="verifying-that-the-mdatp_managedjson-file-is-working-as-expected"></a><span data-ttu-id="b2447-390">Vérification du fonctionnement du mdatp_managed.jssur le fichier comme prévu</span><span class="sxs-lookup"><span data-stu-id="b2447-390">Verifying that the mdatp_managed.json file is working as expected</span></span>
<span data-ttu-id="b2447-391">Pour vérifier que votre /etc/opt/microsoft/mdatp/managed/mdatp_managed.jsfonctionne correctement, vous devez voir « [géré] » en regard de ces paramètres :</span><span class="sxs-lookup"><span data-stu-id="b2447-391">To verify that your /etc/opt/microsoft/mdatp/managed/mdatp_managed.json is working properly, you should see "[managed]" next to these settings:</span></span>  
- <span data-ttu-id="b2447-392">cloud_enabled</span><span class="sxs-lookup"><span data-stu-id="b2447-392">cloud_enabled</span></span>
- <span data-ttu-id="b2447-393">cloud_automatic_sample_submission_consent</span><span class="sxs-lookup"><span data-stu-id="b2447-393">cloud_automatic_sample_submission_consent</span></span>
- <span data-ttu-id="b2447-394">passice_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="b2447-394">passice_mode_enabled</span></span>
- <span data-ttu-id="b2447-395">real_time_protection_enabled</span><span class="sxs-lookup"><span data-stu-id="b2447-395">real_time_protection_enabled</span></span>
- <span data-ttu-id="b2447-396">automatic_definition_update_enabled</span><span class="sxs-lookup"><span data-stu-id="b2447-396">automatic_definition_update_enabled</span></span>

> [!NOTE]
> <span data-ttu-id="b2447-397">Pour que mdatp_managed.jsprenne effet, aucun redémarrage du wdavdaemon n’est requis.</span><span class="sxs-lookup"><span data-stu-id="b2447-397">For the mdatp_managed.json to take effect, no restart of the wdavdaemon is required.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="b2447-398">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b2447-398">Configuration profile deployment</span></span>

<span data-ttu-id="b2447-399">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via l’outil de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="b2447-399">Once you've built the configuration profile for your enterprise, you can deploy it through the management tool that your enterprise is using.</span></span> <span data-ttu-id="b2447-400">Defender for Endpoint sur Linux lit la configuration gérée à partir du *fichier /etc/opt/microsoft/mdatp/managed/mdatp_managed.json.*</span><span class="sxs-lookup"><span data-stu-id="b2447-400">Defender for Endpoint on Linux reads the managed configuration from the */etc/opt/microsoft/mdatp/managed/mdatp_managed.json* file.</span></span>
