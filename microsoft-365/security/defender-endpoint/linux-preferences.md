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
ms.openlocfilehash: 7998e878ad03fdfb64c314dc8b7234ece46164ce
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289486"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="2a45b-104">Définir des préférences pour Microsoft Defender pour le point de terminaison sur Linux</span><span class="sxs-lookup"><span data-stu-id="2a45b-104">Set preferences for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="2a45b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2a45b-105">**Applies to:**</span></span>
- [<span data-ttu-id="2a45b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2a45b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2a45b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2a45b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2a45b-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2a45b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="2a45b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

> [!IMPORTANT]
> <span data-ttu-id="2a45b-110">Cette rubrique contient des instructions sur la façon de définir des préférences pour Defender pour Endpoint sur Linux dans les environnements d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2a45b-110">This topic contains instructions for how to set preferences for Defender for Endpoint on Linux in enterprise environments.</span></span> <span data-ttu-id="2a45b-111">Si vous souhaitez configurer le produit sur un appareil à partir de la ligne de commande, consultez [Ressources.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="2a45b-111">If you are interested in configuring the product on a device from the command-line, see [Resources](linux-resources.md#configure-from-the-command-line).</span></span>

<span data-ttu-id="2a45b-112">Dans les environnements d’entreprise, Defender pour Point de terminaison sur Linux peut être géré via un profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="2a45b-112">In enterprise environments, Defender for Endpoint on Linux can be managed through a configuration profile.</span></span> <span data-ttu-id="2a45b-113">Ce profil est déployé à partir de l’outil de gestion de votre choix.</span><span class="sxs-lookup"><span data-stu-id="2a45b-113">This profile is deployed from the management tool of your choice.</span></span> <span data-ttu-id="2a45b-114">Les préférences gérées par l’entreprise prévalent sur les préférences définies localement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a45b-114">Preferences managed by the enterprise take precedence over the ones set locally on the device.</span></span> <span data-ttu-id="2a45b-115">En d’autres termes, les utilisateurs de votre entreprise ne peuvent pas modifier les préférences définies par le biais de ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="2a45b-115">In other words, users in your enterprise are not able to change preferences that are set through this configuration profile.</span></span>

<span data-ttu-id="2a45b-116">Cet article décrit la structure de ce profil (y compris un profil recommandé que vous pouvez utiliser pour commencer) et des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="2a45b-116">This article describes the structure of this profile (including a recommended profile that you can use to get started) and instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="2a45b-117">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="2a45b-117">Configuration profile structure</span></span>

<span data-ttu-id="2a45b-118">Le profil de configuration est un fichier .json qui se compose d’entrées identifiées par une clé (qui indique le nom de la préférence), suivi d’une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="2a45b-118">The configuration profile is a .json file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="2a45b-119">Les valeurs peuvent être simples, telles qu’une valeur numérique, ou complexes, telles qu’une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="2a45b-119">Values can be simple, such as a numerical value, or complex, such as a nested list of preferences.</span></span>

<span data-ttu-id="2a45b-120">En règle générale, vous utilisez un outil de gestion de la configuration pour pousser un fichier avec le nom ```mdatp_managed.json``` à l’emplacement ```/etc/opt/microsoft/mdatp/managed/``` .</span><span class="sxs-lookup"><span data-stu-id="2a45b-120">Typically, you would use a configuration management tool to push a file with the name ```mdatp_managed.json``` at the location ```/etc/opt/microsoft/mdatp/managed/```.</span></span>

<span data-ttu-id="2a45b-121">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l’échelle du produit pour les sous-catégories du produit, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a45b-121">The top level of the configuration profile includes product-wide preferences and entries for subareas of the product, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="2a45b-122">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="2a45b-122">Antivirus engine preferences</span></span>

<span data-ttu-id="2a45b-123">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus du produit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-123">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of the product.</span></span>

<br>

****

|<span data-ttu-id="2a45b-124">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-124">Description</span></span>|<span data-ttu-id="2a45b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-125">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-126">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-126">**Key**</span></span>|<span data-ttu-id="2a45b-127">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="2a45b-127">antivirusEngine</span></span>|
|<span data-ttu-id="2a45b-128">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-128">**Data type**</span></span>|<span data-ttu-id="2a45b-129">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="2a45b-129">Dictionary (nested preference)</span></span>|
|<span data-ttu-id="2a45b-130">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-130">**Comments**</span></span>|<span data-ttu-id="2a45b-131">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="2a45b-131">See the following sections for a description of the dictionary contents.</span></span>|
|

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="2a45b-132">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="2a45b-132">Enable / disable real-time protection</span></span>

<span data-ttu-id="2a45b-133">Détermine si la protection en temps réel (analyser les fichiers à mesure qu’ils sont accessibles) est activée ou non.</span><span class="sxs-lookup"><span data-stu-id="2a45b-133">Determines whether real-time protection (scan files as they are accessed) is enabled or not.</span></span>

<br>

****

|<span data-ttu-id="2a45b-134">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-134">Description</span></span>|<span data-ttu-id="2a45b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-135">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-136">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-136">**Key**</span></span>|<span data-ttu-id="2a45b-137">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="2a45b-137">enableRealTimeProtection</span></span>|
|<span data-ttu-id="2a45b-138">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-138">**Data type**</span></span>|<span data-ttu-id="2a45b-139">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2a45b-139">Boolean</span></span>|
|<span data-ttu-id="2a45b-140">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-140">**Possible values**</span></span>|<span data-ttu-id="2a45b-141">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-141">true (default)</span></span> <p> <span data-ttu-id="2a45b-142">false</span><span class="sxs-lookup"><span data-stu-id="2a45b-142">false</span></span>|
|

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="2a45b-143">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="2a45b-143">Enable / disable passive mode</span></span>

<span data-ttu-id="2a45b-144">Détermine si le moteur antivirus s’exécute en mode passif ou non.</span><span class="sxs-lookup"><span data-stu-id="2a45b-144">Determines whether the antivirus engine runs in passive mode or not.</span></span> <span data-ttu-id="2a45b-145">En mode passif :</span><span class="sxs-lookup"><span data-stu-id="2a45b-145">In passive mode:</span></span>

- <span data-ttu-id="2a45b-146">La protection en temps réel est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-146">Real-time protection is turned off.</span></span>
- <span data-ttu-id="2a45b-147">L’analyse à la demande est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-147">On-demand scanning is turned on.</span></span>
- <span data-ttu-id="2a45b-148">La correction automatique des menaces est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-148">Automatic threat remediation is turned off.</span></span>
- <span data-ttu-id="2a45b-149">Les mises à jour de l’intelligence de la sécurité sont allumées.</span><span class="sxs-lookup"><span data-stu-id="2a45b-149">Security intelligence updates are turned on.</span></span>
- <span data-ttu-id="2a45b-150">L’icône du menu État est masquée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-150">Status menu icon is hidden.</span></span>

<br>

****

|<span data-ttu-id="2a45b-151">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-151">Description</span></span>|<span data-ttu-id="2a45b-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-152">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-153">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-153">**Key**</span></span>|<span data-ttu-id="2a45b-154">passiveMode</span><span class="sxs-lookup"><span data-stu-id="2a45b-154">passiveMode</span></span>|
|<span data-ttu-id="2a45b-155">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-155">**Data type**</span></span>|<span data-ttu-id="2a45b-156">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2a45b-156">Boolean</span></span>|
|<span data-ttu-id="2a45b-157">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-157">**Possible values**</span></span>|<span data-ttu-id="2a45b-158">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-158">false (default)</span></span> <p> <span data-ttu-id="2a45b-159">true</span><span class="sxs-lookup"><span data-stu-id="2a45b-159">true</span></span>|
|<span data-ttu-id="2a45b-160">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-160">**Comments**</span></span>|<span data-ttu-id="2a45b-161">Disponible dans Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-161">Available in Defender for Endpoint version 100.67.60 or higher.</span></span>|
|

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="2a45b-162">Stratégie de fusion d’exclusion</span><span class="sxs-lookup"><span data-stu-id="2a45b-162">Exclusion merge policy</span></span>

<span data-ttu-id="2a45b-163">Spécifie la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="2a45b-163">Specifies the merge policy for exclusions.</span></span> <span data-ttu-id="2a45b-164">Il peut s’agit d’une combinaison d’exclusions définies par l’administrateur et d’exclusions définies par l’utilisateur ( ) ou uniquement `merge` d’exclusions définies par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="2a45b-164">It can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="2a45b-165">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="2a45b-165">This setting can be used to restrict local users from defining their own exclusions.</span></span>

<br>

****

|<span data-ttu-id="2a45b-166">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-166">Description</span></span>|<span data-ttu-id="2a45b-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-167">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-168">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-168">**Key**</span></span>|<span data-ttu-id="2a45b-169">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="2a45b-169">exclusionsMergePolicy</span></span>|
|<span data-ttu-id="2a45b-170">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-170">**Data type**</span></span>|<span data-ttu-id="2a45b-171">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-171">String</span></span>|
|<span data-ttu-id="2a45b-172">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-172">**Possible values**</span></span>|<span data-ttu-id="2a45b-173">merge (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-173">merge (default)</span></span> <p> <span data-ttu-id="2a45b-174">admin_only</span><span class="sxs-lookup"><span data-stu-id="2a45b-174">admin_only</span></span>|
|<span data-ttu-id="2a45b-175">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-175">**Comments**</span></span>|<span data-ttu-id="2a45b-176">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-176">Available in Defender for Endpoint version 100.83.73 or higher.</span></span>|
|

#### <a name="scan-exclusions"></a><span data-ttu-id="2a45b-177">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="2a45b-177">Scan exclusions</span></span>

<span data-ttu-id="2a45b-178">Entités exclues de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a45b-178">Entities that have been excluded from the scan.</span></span> <span data-ttu-id="2a45b-179">Les exclusions peuvent être spécifiées par des chemins d’accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2a45b-179">Exclusions can be specified by full paths, extensions, or file names.</span></span>
<span data-ttu-id="2a45b-180">(Les exclusions sont spécifiées en tant que tableau d’éléments, l’administrateur peut spécifier autant d’éléments que nécessaire, dans n’importe quel ordre.)</span><span class="sxs-lookup"><span data-stu-id="2a45b-180">(Exclusions are specified as an array of items, administrator can specify as many elements as necessary, in any order.)</span></span>

<br>

****

|<span data-ttu-id="2a45b-181">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-181">Description</span></span>|<span data-ttu-id="2a45b-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-182">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-183">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-183">**Key**</span></span>|<span data-ttu-id="2a45b-184">exclusions</span><span class="sxs-lookup"><span data-stu-id="2a45b-184">exclusions</span></span>|
|<span data-ttu-id="2a45b-185">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-185">**Data type**</span></span>|<span data-ttu-id="2a45b-186">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="2a45b-186">Dictionary (nested preference)</span></span>|
|<span data-ttu-id="2a45b-187">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-187">**Comments**</span></span>|<span data-ttu-id="2a45b-188">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="2a45b-188">See the following sections for a description of the dictionary contents.</span></span>|
|

##### <a name="type-of-exclusion"></a><span data-ttu-id="2a45b-189">Type d’exclusion</span><span class="sxs-lookup"><span data-stu-id="2a45b-189">Type of exclusion</span></span>

<span data-ttu-id="2a45b-190">Spécifie le type de contenu exclu de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a45b-190">Specifies the type of content excluded from the scan.</span></span>

<br>

****

|<span data-ttu-id="2a45b-191">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-191">Description</span></span>|<span data-ttu-id="2a45b-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-192">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-193">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-193">**Key**</span></span>|<span data-ttu-id="2a45b-194">$type</span><span class="sxs-lookup"><span data-stu-id="2a45b-194">$type</span></span>|
|<span data-ttu-id="2a45b-195">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-195">**Data type**</span></span>|<span data-ttu-id="2a45b-196">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-196">String</span></span>|
|<span data-ttu-id="2a45b-197">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-197">**Possible values**</span></span>|<span data-ttu-id="2a45b-198">excludedPath</span><span class="sxs-lookup"><span data-stu-id="2a45b-198">excludedPath</span></span> <p> <span data-ttu-id="2a45b-199">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="2a45b-199">excludedFileExtension</span></span> <p> <span data-ttu-id="2a45b-200">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="2a45b-200">excludedFileName</span></span>|
|

##### <a name="path-to-excluded-content"></a><span data-ttu-id="2a45b-201">Chemin d’accès au contenu exclu</span><span class="sxs-lookup"><span data-stu-id="2a45b-201">Path to excluded content</span></span>

<span data-ttu-id="2a45b-202">Utilisé pour exclure le contenu de l’analyse par chemin d’accès complet au fichier.</span><span class="sxs-lookup"><span data-stu-id="2a45b-202">Used to exclude content from the scan by full file path.</span></span>

<br>

****

|<span data-ttu-id="2a45b-203">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-203">Description</span></span>|<span data-ttu-id="2a45b-204">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-204">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-205">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-205">**Key**</span></span>|<span data-ttu-id="2a45b-206">chemin</span><span class="sxs-lookup"><span data-stu-id="2a45b-206">path</span></span>|
|<span data-ttu-id="2a45b-207">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-207">**Data type**</span></span>|<span data-ttu-id="2a45b-208">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-208">String</span></span>|
|<span data-ttu-id="2a45b-209">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-209">**Possible values**</span></span>|<span data-ttu-id="2a45b-210">chemins d’accès valides</span><span class="sxs-lookup"><span data-stu-id="2a45b-210">valid paths</span></span>|
|<span data-ttu-id="2a45b-211">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-211">**Comments**</span></span>|<span data-ttu-id="2a45b-212">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="2a45b-212">Applicable only if *$type* is *excludedPath*</span></span>|
|

##### <a name="path-type-file--directory"></a><span data-ttu-id="2a45b-213">Type de chemin d’accès (fichier/répertoire)</span><span class="sxs-lookup"><span data-stu-id="2a45b-213">Path type (file / directory)</span></span>

<span data-ttu-id="2a45b-214">Indique si la propriété *de chemin d’accès* fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="2a45b-214">Indicates if the *path* property refers to a file or directory.</span></span>

<br>

****

|<span data-ttu-id="2a45b-215">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-215">Description</span></span>|<span data-ttu-id="2a45b-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-216">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-217">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-217">**Key**</span></span>|<span data-ttu-id="2a45b-218">isDirectory</span><span class="sxs-lookup"><span data-stu-id="2a45b-218">isDirectory</span></span>|
|<span data-ttu-id="2a45b-219">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-219">**Data type**</span></span>|<span data-ttu-id="2a45b-220">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2a45b-220">Boolean</span></span>|
|<span data-ttu-id="2a45b-221">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-221">**Possible values**</span></span>|<span data-ttu-id="2a45b-222">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-222">false (default)</span></span> <p> <span data-ttu-id="2a45b-223">true</span><span class="sxs-lookup"><span data-stu-id="2a45b-223">true</span></span>|
|<span data-ttu-id="2a45b-224">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-224">**Comments**</span></span>|<span data-ttu-id="2a45b-225">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="2a45b-225">Applicable only if *$type* is *excludedPath*</span></span>|
|

##### <a name="file-extension-excluded-from-the-scan"></a><span data-ttu-id="2a45b-226">Extension de fichier exclue de l’analyse</span><span class="sxs-lookup"><span data-stu-id="2a45b-226">File extension excluded from the scan</span></span>

<span data-ttu-id="2a45b-227">Utilisé pour exclure le contenu de l’analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="2a45b-227">Used to exclude content from the scan by file extension.</span></span>

<br>

****

|<span data-ttu-id="2a45b-228">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-228">Description</span></span>|<span data-ttu-id="2a45b-229">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-229">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-230">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-230">**Key**</span></span>|<span data-ttu-id="2a45b-231">extension</span><span class="sxs-lookup"><span data-stu-id="2a45b-231">extension</span></span>|
|<span data-ttu-id="2a45b-232">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-232">**Data type**</span></span>|<span data-ttu-id="2a45b-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-233">String</span></span>|
|<span data-ttu-id="2a45b-234">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-234">**Possible values**</span></span>|<span data-ttu-id="2a45b-235">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="2a45b-235">valid file extensions</span></span>|
|<span data-ttu-id="2a45b-236">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-236">**Comments**</span></span>|<span data-ttu-id="2a45b-237">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="2a45b-237">Applicable only if *$type* is *excludedFileExtension*</span></span>|
|

##### <a name="process-excluded-from-the-scan"></a><span data-ttu-id="2a45b-238">Processus exclu de l’analyse\*</span><span class="sxs-lookup"><span data-stu-id="2a45b-238">Process excluded from the scan\*</span></span>

<span data-ttu-id="2a45b-239">Spécifie un processus pour lequel toute l’activité de fichier est exclue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a45b-239">Specifies a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="2a45b-240">Le processus peut être spécifié par son nom (par exemple) ou son chemin `cat` d’accès complet (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="2a45b-240">The process can be specified either by its name (for example, `cat`) or full path (for example, `/bin/cat`).</span></span>

<br>

****

|<span data-ttu-id="2a45b-241">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-241">Description</span></span>|<span data-ttu-id="2a45b-242">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-242">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-243">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-243">**Key**</span></span>|<span data-ttu-id="2a45b-244">name</span><span class="sxs-lookup"><span data-stu-id="2a45b-244">name</span></span>|
|<span data-ttu-id="2a45b-245">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-245">**Data type**</span></span>|<span data-ttu-id="2a45b-246">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-246">String</span></span>|
|<span data-ttu-id="2a45b-247">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-247">**Possible values**</span></span>|<span data-ttu-id="2a45b-248">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-248">any string</span></span>|
|<span data-ttu-id="2a45b-249">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-249">**Comments**</span></span>|<span data-ttu-id="2a45b-250">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="2a45b-250">Applicable only if *$type* is *excludedFileName*</span></span>|
|

#### <a name="allowed-threats"></a><span data-ttu-id="2a45b-251">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="2a45b-251">Allowed threats</span></span>

<span data-ttu-id="2a45b-252">Liste des menaces (identifiées par leur nom) qui ne sont pas bloquées par le produit et sont autorisées à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2a45b-252">List of threats (identified by their name) that are not blocked by the product and are instead allowed to run.</span></span>

<br>

****

|<span data-ttu-id="2a45b-253">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-253">Description</span></span>|<span data-ttu-id="2a45b-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-254">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-255">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-255">**Key**</span></span>|<span data-ttu-id="2a45b-256">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="2a45b-256">allowedThreats</span></span>|
|<span data-ttu-id="2a45b-257">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-257">**Data type**</span></span>|<span data-ttu-id="2a45b-258">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="2a45b-258">Array of strings</span></span>|
|

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="2a45b-259">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="2a45b-259">Disallowed threat actions</span></span>

<span data-ttu-id="2a45b-260">Limite les actions que l’utilisateur local d’un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="2a45b-260">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="2a45b-261">Les actions incluses dans cette liste ne sont pas affichées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a45b-261">The actions included in this list are not displayed in the user interface.</span></span>

<br>

****

|<span data-ttu-id="2a45b-262">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-262">Description</span></span>|<span data-ttu-id="2a45b-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-263">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-264">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-264">**Key**</span></span>|<span data-ttu-id="2a45b-265">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="2a45b-265">disallowedThreatActions</span></span>|
|<span data-ttu-id="2a45b-266">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-266">**Data type**</span></span>|<span data-ttu-id="2a45b-267">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="2a45b-267">Array of strings</span></span>|
|<span data-ttu-id="2a45b-268">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-268">**Possible values**</span></span>|<span data-ttu-id="2a45b-269">autoriser (empêche les utilisateurs d’autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="2a45b-269">allow (restricts users from allowing threats)</span></span> <p> <span data-ttu-id="2a45b-270">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="2a45b-270">restore (restricts users from restoring threats from the quarantine)</span></span>|
|<span data-ttu-id="2a45b-271">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-271">**Comments**</span></span>|<span data-ttu-id="2a45b-272">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-272">Available in Defender for Endpoint version 100.83.73 or higher.</span></span>|
|

#### <a name="threat-type-settings"></a><span data-ttu-id="2a45b-273">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="2a45b-273">Threat type settings</span></span>

<span data-ttu-id="2a45b-274">La *préférence threatTypeSettings dans* le moteur antivirus est utilisée pour contrôler la façon dont certains types de menaces sont gérés par le produit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-274">The *threatTypeSettings* preference in the antivirus engine is used to control how certain threat types are handled by the product.</span></span>

<br>

****

|<span data-ttu-id="2a45b-275">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-275">Description</span></span>|<span data-ttu-id="2a45b-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-276">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-277">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-277">**Key**</span></span>|<span data-ttu-id="2a45b-278">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="2a45b-278">threatTypeSettings</span></span>|
|<span data-ttu-id="2a45b-279">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-279">**Data type**</span></span>|<span data-ttu-id="2a45b-280">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="2a45b-280">Dictionary (nested preference)</span></span>|
|<span data-ttu-id="2a45b-281">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-281">**Comments**</span></span>|<span data-ttu-id="2a45b-282">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="2a45b-282">See the following sections for a description of the dictionary contents.</span></span>|
|

##### <a name="threat-type"></a><span data-ttu-id="2a45b-283">Type de menace</span><span class="sxs-lookup"><span data-stu-id="2a45b-283">Threat type</span></span>

<span data-ttu-id="2a45b-284">Type de menace pour lequel le comportement est configuré.</span><span class="sxs-lookup"><span data-stu-id="2a45b-284">Type of threat for which the behavior is configured.</span></span>

<br>

****

|<span data-ttu-id="2a45b-285">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-285">Description</span></span>|<span data-ttu-id="2a45b-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-286">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-287">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-287">**Key**</span></span>|<span data-ttu-id="2a45b-288">clé</span><span class="sxs-lookup"><span data-stu-id="2a45b-288">key</span></span>|
|<span data-ttu-id="2a45b-289">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-289">**Data type**</span></span>|<span data-ttu-id="2a45b-290">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-290">String</span></span>|
|<span data-ttu-id="2a45b-291">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-291">**Possible values**</span></span>|<span data-ttu-id="2a45b-292">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="2a45b-292">potentially_unwanted_application</span></span> <p> <span data-ttu-id="2a45b-293">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="2a45b-293">archive_bomb</span></span>|
|

##### <a name="action-to-take"></a><span data-ttu-id="2a45b-294">Mesures à prendre</span><span class="sxs-lookup"><span data-stu-id="2a45b-294">Action to take</span></span>

<span data-ttu-id="2a45b-295">Action à prendre en cas de menace du type spécifié dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="2a45b-295">Action to take when coming across a threat of the type specified in the preceding section.</span></span> <span data-ttu-id="2a45b-296">Peut être :</span><span class="sxs-lookup"><span data-stu-id="2a45b-296">Can be:</span></span>

- <span data-ttu-id="2a45b-297">**Audit**: l’appareil n’est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-297">**Audit**: The device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="2a45b-298">**Bloquer**: l’appareil est protégé contre ce type de menace et vous êtes averti dans la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2a45b-298">**Block**: The device is protected against this type of threat and you are notified in the security console.</span></span>
- <span data-ttu-id="2a45b-299">**Off**: l’appareil n’est pas protégé contre ce type de menace et rien n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="2a45b-299">**Off**: The device is not protected against this type of threat and nothing is logged.</span></span>

<br>

****

|<span data-ttu-id="2a45b-300">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-300">Description</span></span>|<span data-ttu-id="2a45b-301">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-301">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-302">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-302">**Key**</span></span>|<span data-ttu-id="2a45b-303">valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-303">value</span></span>|
|<span data-ttu-id="2a45b-304">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-304">**Data type**</span></span>|<span data-ttu-id="2a45b-305">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-305">String</span></span>|
|<span data-ttu-id="2a45b-306">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-306">**Possible values**</span></span>|<span data-ttu-id="2a45b-307">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-307">audit (default)</span></span> <p> <span data-ttu-id="2a45b-308">block</span><span class="sxs-lookup"><span data-stu-id="2a45b-308">block</span></span> <p> <span data-ttu-id="2a45b-309">off</span><span class="sxs-lookup"><span data-stu-id="2a45b-309">off</span></span>|
|

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="2a45b-310">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="2a45b-310">Threat type settings merge policy</span></span>

<span data-ttu-id="2a45b-311">Spécifie la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="2a45b-311">Specifies the merge policy for threat type settings.</span></span> <span data-ttu-id="2a45b-312">Il peut s’agit d’une combinaison de paramètres définis par l’administrateur et de paramètres définis par l’utilisateur ( ) ou uniquement de `merge` paramètres définis par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="2a45b-312">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="2a45b-313">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="2a45b-313">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

<br>

****

|<span data-ttu-id="2a45b-314">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-314">Description</span></span>|<span data-ttu-id="2a45b-315">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-315">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-316">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-316">**Key**</span></span>|<span data-ttu-id="2a45b-317">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="2a45b-317">threatTypeSettingsMergePolicy</span></span>|
|<span data-ttu-id="2a45b-318">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-318">**Data type**</span></span>|<span data-ttu-id="2a45b-319">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-319">String</span></span>|
|<span data-ttu-id="2a45b-320">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-320">**Possible values**</span></span>|<span data-ttu-id="2a45b-321">merge (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-321">merge (default)</span></span> <p> <span data-ttu-id="2a45b-322">admin_only</span><span class="sxs-lookup"><span data-stu-id="2a45b-322">admin_only</span></span>|
|<span data-ttu-id="2a45b-323">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-323">**Comments**</span></span>|<span data-ttu-id="2a45b-324">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-324">Available in Defender for Endpoint version 100.83.73 or higher.</span></span>|
|

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="2a45b-325">Conservation de l’historique d’analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="2a45b-325">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="2a45b-326">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l’historique d’analyse sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a45b-326">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="2a45b-327">Les anciens résultats d’analyse sont supprimés de l’historique.</span><span class="sxs-lookup"><span data-stu-id="2a45b-327">Old scan results are removed from the history.</span></span> <span data-ttu-id="2a45b-328">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="2a45b-328">Old quarantined files that are also removed from the disk.</span></span>

<br>

****

|<span data-ttu-id="2a45b-329">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-329">Description</span></span>|<span data-ttu-id="2a45b-330">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-330">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-331">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-331">**Key**</span></span>|<span data-ttu-id="2a45b-332">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="2a45b-332">scanResultsRetentionDays</span></span>|
|<span data-ttu-id="2a45b-333">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-333">**Data type**</span></span>|<span data-ttu-id="2a45b-334">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-334">String</span></span>|
|<span data-ttu-id="2a45b-335">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-335">**Possible values**</span></span>|<span data-ttu-id="2a45b-336">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="2a45b-336">90 (default).</span></span> <span data-ttu-id="2a45b-337">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="2a45b-337">Allowed values are from 1 day to 180 days.</span></span>|
|<span data-ttu-id="2a45b-338">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-338">**Comments**</span></span>|<span data-ttu-id="2a45b-339">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-339">Available in Defender for Endpoint version 101.04.76 or higher.</span></span>|
|

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="2a45b-340">Nombre maximal d’éléments dans l’historique d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="2a45b-340">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="2a45b-341">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="2a45b-341">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="2a45b-342">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="2a45b-342">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

<br>

****

|<span data-ttu-id="2a45b-343">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-343">Description</span></span>|<span data-ttu-id="2a45b-344">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-344">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-345">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-345">**Key**</span></span>|<span data-ttu-id="2a45b-346">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="2a45b-346">scanHistoryMaximumItems</span></span>|
|<span data-ttu-id="2a45b-347">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-347">**Data type**</span></span>|<span data-ttu-id="2a45b-348">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-348">String</span></span>|
|<span data-ttu-id="2a45b-349">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-349">**Possible values**</span></span>|<span data-ttu-id="2a45b-350">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="2a45b-350">10000 (default).</span></span> <span data-ttu-id="2a45b-351">Les valeurs autorisées sont de 5 000 à 15 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="2a45b-351">Allowed values are from 5000 items to 15000 items.</span></span>|
|<span data-ttu-id="2a45b-352">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-352">**Comments**</span></span>|<span data-ttu-id="2a45b-353">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="2a45b-353">Available in Defender for Endpoint version 101.04.76 or higher.</span></span>|
|

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="2a45b-354">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="2a45b-354">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="2a45b-355">*L’entrée cloudService* dans le profil de configuration est utilisée pour configurer la fonctionnalité de protection pilotée par le cloud du produit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-355">The *cloudService* entry in the configuration profile is used to configure the cloud-driven protection feature of the product.</span></span>

<br>

****

|<span data-ttu-id="2a45b-356">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-356">Description</span></span>|<span data-ttu-id="2a45b-357">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-357">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-358">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-358">**Key**</span></span>|<span data-ttu-id="2a45b-359">cloudService</span><span class="sxs-lookup"><span data-stu-id="2a45b-359">cloudService</span></span>|
|<span data-ttu-id="2a45b-360">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-360">**Data type**</span></span>|<span data-ttu-id="2a45b-361">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="2a45b-361">Dictionary (nested preference)</span></span>|
|<span data-ttu-id="2a45b-362">**Comments**</span><span class="sxs-lookup"><span data-stu-id="2a45b-362">**Comments**</span></span>|<span data-ttu-id="2a45b-363">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="2a45b-363">See the following sections for a description of the dictionary contents.</span></span>|
|

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="2a45b-364">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="2a45b-364">Enable / disable cloud delivered protection</span></span>

<span data-ttu-id="2a45b-365">Détermine si la protection cloud est activée ou non sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a45b-365">Determines whether cloud-delivered protection is enabled on the device or not.</span></span> <span data-ttu-id="2a45b-366">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="2a45b-366">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

<br>

****

|<span data-ttu-id="2a45b-367">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-367">Description</span></span>|<span data-ttu-id="2a45b-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-368">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-369">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-369">**Key**</span></span>|<span data-ttu-id="2a45b-370">activé</span><span class="sxs-lookup"><span data-stu-id="2a45b-370">enabled</span></span>|
|<span data-ttu-id="2a45b-371">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-371">**Data type**</span></span>|<span data-ttu-id="2a45b-372">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2a45b-372">Boolean</span></span>|
|<span data-ttu-id="2a45b-373">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-373">**Possible values**</span></span>|<span data-ttu-id="2a45b-374">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-374">true (default)</span></span> <p> <span data-ttu-id="2a45b-375">false</span><span class="sxs-lookup"><span data-stu-id="2a45b-375">false</span></span>|
|

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="2a45b-376">Niveau de collecte de diagnostics</span><span class="sxs-lookup"><span data-stu-id="2a45b-376">Diagnostic collection level</span></span>

<span data-ttu-id="2a45b-377">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="2a45b-377">Diagnostic data is used to keep Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="2a45b-378">Ce paramètre détermine le niveau de diagnostics envoyés par le produit à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a45b-378">This setting determines the level of diagnostics sent by the product to Microsoft.</span></span>

<br>

****

|<span data-ttu-id="2a45b-379">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-379">Description</span></span>|<span data-ttu-id="2a45b-380">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-380">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-381">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-381">**Key**</span></span>|<span data-ttu-id="2a45b-382">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="2a45b-382">diagnosticLevel</span></span>|
|<span data-ttu-id="2a45b-383">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-383">**Data type**</span></span>|<span data-ttu-id="2a45b-384">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-384">String</span></span>|
|<span data-ttu-id="2a45b-385">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-385">**Possible values**</span></span>|<span data-ttu-id="2a45b-386">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-386">optional (default)</span></span> <p> <span data-ttu-id="2a45b-387">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2a45b-387">required</span></span>|
|

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="2a45b-388">Activer/désactiver les envois automatiques d’échantillons</span><span class="sxs-lookup"><span data-stu-id="2a45b-388">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="2a45b-389">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a45b-389">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="2a45b-390">Il existe trois niveaux pour contrôler l’envoi d’échantillons :</span><span class="sxs-lookup"><span data-stu-id="2a45b-390">There are three levels for controlling sample submission:</span></span>

- <span data-ttu-id="2a45b-391">**Aucun**: aucun échantillon suspect n’est envoyé à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a45b-391">**None**: no suspicious samples are submitted to Microsoft.</span></span>
- <span data-ttu-id="2a45b-392">**Coffre**: seuls les échantillons suspects qui ne contiennent pas d’informations d’identification personnelle (PII) sont envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2a45b-392">**Safe**: only suspicious samples that do not contain personally identifiable information (PII) are submitted automatically.</span></span> <span data-ttu-id="2a45b-393">Il s’agit de la valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="2a45b-393">This is the default value for this setting.</span></span>
- <span data-ttu-id="2a45b-394">**Tous**: tous les échantillons suspects sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a45b-394">**All**: all suspicious samples are submitted to Microsoft.</span></span>

<br>

****

|<span data-ttu-id="2a45b-395">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-395">Description</span></span>|<span data-ttu-id="2a45b-396">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-396">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-397">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-397">**Key**</span></span>|<span data-ttu-id="2a45b-398">automaticSampleSubmissionConsent</span><span class="sxs-lookup"><span data-stu-id="2a45b-398">automaticSampleSubmissionConsent</span></span>|
|<span data-ttu-id="2a45b-399">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-399">**Data type**</span></span>|<span data-ttu-id="2a45b-400">Chaîne</span><span class="sxs-lookup"><span data-stu-id="2a45b-400">String</span></span>|
|<span data-ttu-id="2a45b-401">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-401">**Possible values**</span></span>|<span data-ttu-id="2a45b-402">aucune</span><span class="sxs-lookup"><span data-stu-id="2a45b-402">none</span></span> <p> <span data-ttu-id="2a45b-403">safe (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-403">safe (default)</span></span> <p> <span data-ttu-id="2a45b-404">all</span><span class="sxs-lookup"><span data-stu-id="2a45b-404">all</span></span>|
|

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="2a45b-405">Activer/désactiver les mises à jour automatiques de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="2a45b-405">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="2a45b-406">Détermine si les mises à jour d’informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="2a45b-406">Determines whether security intelligence updates are installed automatically:</span></span>

<br>

****

|<span data-ttu-id="2a45b-407">Description</span><span class="sxs-lookup"><span data-stu-id="2a45b-407">Description</span></span>|<span data-ttu-id="2a45b-408">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a45b-408">Value</span></span>|
|---|---|
|<span data-ttu-id="2a45b-409">**Key**</span><span class="sxs-lookup"><span data-stu-id="2a45b-409">**Key**</span></span>|<span data-ttu-id="2a45b-410">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="2a45b-410">automaticDefinitionUpdateEnabled</span></span>|
|<span data-ttu-id="2a45b-411">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2a45b-411">**Data type**</span></span>|<span data-ttu-id="2a45b-412">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="2a45b-412">Boolean</span></span>|
|<span data-ttu-id="2a45b-413">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a45b-413">**Possible values**</span></span>|<span data-ttu-id="2a45b-414">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="2a45b-414">true (default)</span></span> <p> <span data-ttu-id="2a45b-415">false</span><span class="sxs-lookup"><span data-stu-id="2a45b-415">false</span></span>|
|

## <a name="recommended-configuration-profile"></a><span data-ttu-id="2a45b-416">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="2a45b-416">Recommended configuration profile</span></span>

<span data-ttu-id="2a45b-417">Pour commencer, nous recommandons le profil de configuration suivant pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-417">To get started, we recommend the following configuration profile for your enterprise to take advantage of all protection features that Defender for Endpoint provides.</span></span>

<span data-ttu-id="2a45b-418">Le profil de configuration suivant :</span><span class="sxs-lookup"><span data-stu-id="2a45b-418">The following configuration profile will:</span></span>

- <span data-ttu-id="2a45b-419">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="2a45b-419">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="2a45b-420">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="2a45b-420">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="2a45b-421">**Les applications potentiellement indésirables (PUA)** sont bloquées</span><span class="sxs-lookup"><span data-stu-id="2a45b-421">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="2a45b-422">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans les journaux du produit</span><span class="sxs-lookup"><span data-stu-id="2a45b-422">**Archive bombs** (file with a high compression rate) are audited to the product logs</span></span>
- <span data-ttu-id="2a45b-423">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="2a45b-423">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="2a45b-424">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="2a45b-424">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="2a45b-425">Activer l’envoi automatique d’échantillons au `safe` niveau</span><span class="sxs-lookup"><span data-stu-id="2a45b-425">Enable automatic sample submission at `safe` level</span></span>

### <a name="sample-profile"></a><span data-ttu-id="2a45b-426">Exemple de profil</span><span class="sxs-lookup"><span data-stu-id="2a45b-426">Sample profile</span></span>

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

## <a name="full-configuration-profile-example"></a><span data-ttu-id="2a45b-427">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="2a45b-427">Full configuration profile example</span></span>

<span data-ttu-id="2a45b-428">Le profil de configuration suivant contient des entrées pour tous les paramètres décrits dans ce document et peut être utilisé pour des scénarios plus avancés où vous souhaitez contrôler davantage le produit.</span><span class="sxs-lookup"><span data-stu-id="2a45b-428">The following configuration profile contains entries for all settings described in this document and can be used for more advanced scenarios where you want more control over the product.</span></span>

### <a name="full-profile"></a><span data-ttu-id="2a45b-429">Profil complet</span><span class="sxs-lookup"><span data-stu-id="2a45b-429">Full profile</span></span>

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
            "extension":".pdf"
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

## <a name="configuration-profile-validation"></a><span data-ttu-id="2a45b-430">Validation du profil de configuration</span><span class="sxs-lookup"><span data-stu-id="2a45b-430">Configuration profile validation</span></span>

<span data-ttu-id="2a45b-431">Le profil de configuration doit être un fichier au format JSON valide.</span><span class="sxs-lookup"><span data-stu-id="2a45b-431">The configuration profile must be a valid JSON-formatted file.</span></span> <span data-ttu-id="2a45b-432">Il existe un certain nombre d’outils qui peuvent être utilisés pour vérifier cela.</span><span class="sxs-lookup"><span data-stu-id="2a45b-432">There are a number of tools that can be used to verify this.</span></span> <span data-ttu-id="2a45b-433">Par exemple, si vous avez `python` installé sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="2a45b-433">For example, if you have `python` installed on your device:</span></span>

```bash
python -m json.tool mdatp_managed.json
```

<span data-ttu-id="2a45b-434">Si le JSON est bien formé, la commande ci-dessus le renvoie au Terminal et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="2a45b-434">If the JSON is well-formed, the above command outputs it back to the Terminal and returns an exit code of `0`.</span></span> <span data-ttu-id="2a45b-435">Sinon, une erreur qui décrit le problème s’affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="2a45b-435">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="verifying-that-the-mdatp_managedjson-file-is-working-as-expected"></a><span data-ttu-id="2a45b-436">Vérification du fonctionnement du mdatp_managed.jssur le fichier comme prévu</span><span class="sxs-lookup"><span data-stu-id="2a45b-436">Verifying that the mdatp_managed.json file is working as expected</span></span>

<span data-ttu-id="2a45b-437">Pour vérifier que votre /etc/opt/microsoft/mdatp/managed/mdatp_managed.jsfonctionne correctement, vous devez voir « [géré] » en regard de ces paramètres :</span><span class="sxs-lookup"><span data-stu-id="2a45b-437">To verify that your /etc/opt/microsoft/mdatp/managed/mdatp_managed.json is working properly, you should see "[managed]" next to these settings:</span></span>

- <span data-ttu-id="2a45b-438">cloud_enabled</span><span class="sxs-lookup"><span data-stu-id="2a45b-438">cloud_enabled</span></span>
- <span data-ttu-id="2a45b-439">cloud_automatic_sample_submission_consent</span><span class="sxs-lookup"><span data-stu-id="2a45b-439">cloud_automatic_sample_submission_consent</span></span>
- <span data-ttu-id="2a45b-440">passive_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="2a45b-440">passive_mode_enabled</span></span>
- <span data-ttu-id="2a45b-441">real_time_protection_enabled</span><span class="sxs-lookup"><span data-stu-id="2a45b-441">real_time_protection_enabled</span></span>
- <span data-ttu-id="2a45b-442">automatic_definition_update_enabled</span><span class="sxs-lookup"><span data-stu-id="2a45b-442">automatic_definition_update_enabled</span></span>

> [!NOTE]
> <span data-ttu-id="2a45b-443">Pour que mdatp_managed.jsprenne effet, aucun redémarrage du wdavdaemon n’est requis.</span><span class="sxs-lookup"><span data-stu-id="2a45b-443">For the mdatp_managed.json to take effect, no restart of the wdavdaemon is required.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="2a45b-444">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="2a45b-444">Configuration profile deployment</span></span>

<span data-ttu-id="2a45b-445">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via l’outil de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="2a45b-445">Once you've built the configuration profile for your enterprise, you can deploy it through the management tool that your enterprise is using.</span></span> <span data-ttu-id="2a45b-446">Defender for Endpoint sur Linux lit la configuration gérée à partir du *fichier /etc/opt/microsoft/mdatp/managed/mdatp_managed.json.*</span><span class="sxs-lookup"><span data-stu-id="2a45b-446">Defender for Endpoint on Linux reads the managed configuration from the */etc/opt/microsoft/mdatp/managed/mdatp_managed.json* file.</span></span>
