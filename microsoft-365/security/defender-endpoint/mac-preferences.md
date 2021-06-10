---
title: Définir des préférences pour Microsoft Defender pour le point de terminaison sur Mac
description: Configurez MMicrosoft Defender pour endpoint sur Mac dans les organisations d’entreprise.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, mac, gestion, préférences, entreprise, intune, jamf, macos,pératin, mojave, high sierra
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
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: b706cb8dbd43d545768c1c573021b5ef401e3c09
ms.sourcegitcommit: 94e64afaf12f3d8813099d8ffa46baba65772763
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52346401"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="8a10e-104">Définir des préférences pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="8a10e-104">Set preferences for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="8a10e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8a10e-105">**Applies to:**</span></span>

- [<span data-ttu-id="8a10e-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="8a10e-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)

>[!IMPORTANT]
><span data-ttu-id="8a10e-107">Cet article contient des instructions sur la façon de définir des préférences pour Microsoft Defender pour Endpoint sur macOS dans les organisations d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8a10e-107">This article contains instructions for how to set preferences for Microsoft Defender for Endpoint on macOS in enterprise organizations.</span></span> <span data-ttu-id="8a10e-108">Pour configurer Microsoft Defender pour endpoint sur macOS à l’aide de l’interface de ligne de commande, voir [Resources](mac-resources.md#configuring-from-the-command-line).</span><span class="sxs-lookup"><span data-stu-id="8a10e-108">To configure Microsoft Defender for Endpoint on macOS using the command-line interface, see [Resources](mac-resources.md#configuring-from-the-command-line).</span></span>

## <a name="summary"></a><span data-ttu-id="8a10e-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="8a10e-109">Summary</span></span>

<span data-ttu-id="8a10e-110">Dans les organisations d’entreprise, Microsoft Defender pour Endpoint sur macOS peut être géré via un profil de configuration déployé à l’aide de l’un des outils de gestion.</span><span class="sxs-lookup"><span data-stu-id="8a10e-110">In enterprise organizations, Microsoft Defender for Endpoint on macOS can be managed through a configuration profile that is deployed by using one of several management tools.</span></span> <span data-ttu-id="8a10e-111">Les préférences gérées par votre équipe en charge des opérations de sécurité prévalent sur les préférences définies localement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8a10e-111">Preferences that are managed by your security operations team take precedence over preferences that are set locally on the device.</span></span> <span data-ttu-id="8a10e-112">La modification des préférences définies par le biais du profil de configuration nécessite des privilèges escalades et n’est pas disponible pour les utilisateurs sans autorisations administratives.</span><span class="sxs-lookup"><span data-stu-id="8a10e-112">Changing the preferences that are set through the configuration profile requires escalated privileges and is not available for users without administrative permissions.</span></span>

<span data-ttu-id="8a10e-113">Cet article décrit la structure du profil de configuration, inclut un profil recommandé que vous pouvez utiliser pour commencer et fournit des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="8a10e-113">This article describes the structure of the configuration profile, includes a recommended profile that you can use to get started, and provides instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="8a10e-114">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="8a10e-114">Configuration profile structure</span></span>

<span data-ttu-id="8a10e-115">Le profil de configuration est un fichier *.plist* qui se compose d’entrées identifiées par une clé (qui indique le nom de la préférence), suivi d’une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="8a10e-115">The configuration profile is a *.plist* file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="8a10e-116">Les valeurs peuvent être simples (par exemple, une valeur numérique) ou complexes, telles qu’une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="8a10e-116">Values can either be simple (such as a numerical value) or complex, such as a nested list of preferences.</span></span>

>[!CAUTION]
><span data-ttu-id="8a10e-117">La disposition du profil de configuration dépend de la console de gestion que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="8a10e-117">The layout of the configuration profile depends on the management console that you are using.</span></span> <span data-ttu-id="8a10e-118">Les sections suivantes contiennent des exemples de profils de configuration pour JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="8a10e-118">The following sections contain examples of configuration profiles for JAMF and Intune.</span></span>

<span data-ttu-id="8a10e-119">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l’échelle du produit pour les sous-catégories de Microsoft Defender pour le point de terminaison, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a10e-119">The top level of the configuration profile includes product-wide preferences and entries for subareas of Microsoft Defender for Endpoint, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="8a10e-120">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="8a10e-120">Antivirus engine preferences</span></span>

<span data-ttu-id="8a10e-121">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="8a10e-121">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of Microsoft Defender for Endpoint.</span></span>

|<span data-ttu-id="8a10e-122">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-122">Section</span></span>|<span data-ttu-id="8a10e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-123">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-124">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-124">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-125">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-125">**Key**</span></span> | <span data-ttu-id="8a10e-126">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="8a10e-126">antivirusEngine</span></span> |
| <span data-ttu-id="8a10e-127">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-127">**Data type**</span></span> | <span data-ttu-id="8a10e-128">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-128">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-129">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-129">**Comments**</span></span> | <span data-ttu-id="8a10e-130">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-130">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="8a10e-131">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="8a10e-131">Enable / disable real-time protection</span></span>

<span data-ttu-id="8a10e-132">Spécifiez s’il faut activer la protection en temps réel, qui analyse les fichiers à mesure qu’ils sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="8a10e-132">Specify whether to enable real-time protection, which scans files as they are accessed.</span></span>

|<span data-ttu-id="8a10e-133">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-133">Section</span></span>|<span data-ttu-id="8a10e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-134">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-135">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-135">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-136">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-136">**Key**</span></span> | <span data-ttu-id="8a10e-137">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="8a10e-137">enableRealTimeProtection</span></span> |
| <span data-ttu-id="8a10e-138">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-138">**Data type**</span></span> | <span data-ttu-id="8a10e-139">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-139">Boolean</span></span> |
| <span data-ttu-id="8a10e-140">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-140">**Possible values**</span></span> | <span data-ttu-id="8a10e-141">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-141">true (default)</span></span> <br/> <span data-ttu-id="8a10e-142">false</span><span class="sxs-lookup"><span data-stu-id="8a10e-142">false</span></span> |

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="8a10e-143">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="8a10e-143">Enable / disable passive mode</span></span>

<span data-ttu-id="8a10e-144">Spécifiez si le moteur antivirus s’exécute en mode passif.</span><span class="sxs-lookup"><span data-stu-id="8a10e-144">Specify whether the antivirus engine runs in passive mode.</span></span> <span data-ttu-id="8a10e-145">Le mode passif a les implications suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a10e-145">Passive mode has the following implications:</span></span> 
- <span data-ttu-id="8a10e-146">La protection en temps réel est désactivée</span><span class="sxs-lookup"><span data-stu-id="8a10e-146">Real-time protection is turned off</span></span>
- <span data-ttu-id="8a10e-147">L’analyse à la demande est désactivée</span><span class="sxs-lookup"><span data-stu-id="8a10e-147">On-demand scanning is turned on</span></span>
- <span data-ttu-id="8a10e-148">La correction automatique des menaces est désactivée</span><span class="sxs-lookup"><span data-stu-id="8a10e-148">Automatic threat remediation is turned off</span></span>
- <span data-ttu-id="8a10e-149">Les mises à jour de l’intelligence de la sécurité sont allumées</span><span class="sxs-lookup"><span data-stu-id="8a10e-149">Security intelligence updates are turned on</span></span>
- <span data-ttu-id="8a10e-150">L’icône du menu État est masquée</span><span class="sxs-lookup"><span data-stu-id="8a10e-150">Status menu icon is hidden</span></span>

|<span data-ttu-id="8a10e-151">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-151">Section</span></span>|<span data-ttu-id="8a10e-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-152">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-153">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-153">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-154">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-154">**Key**</span></span> | <span data-ttu-id="8a10e-155">passiveMode</span><span class="sxs-lookup"><span data-stu-id="8a10e-155">passiveMode</span></span> |
| <span data-ttu-id="8a10e-156">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-156">**Data type**</span></span> | <span data-ttu-id="8a10e-157">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-157">Boolean</span></span> |
| <span data-ttu-id="8a10e-158">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-158">**Possible values**</span></span> | <span data-ttu-id="8a10e-159">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-159">false (default)</span></span> <br/> <span data-ttu-id="8a10e-160">true</span><span class="sxs-lookup"><span data-stu-id="8a10e-160">true</span></span> |
| <span data-ttu-id="8a10e-161">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-161">**Comments**</span></span> | <span data-ttu-id="8a10e-162">Disponible dans Microsoft Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-162">Available in Microsoft Defender for Endpoint version 100.67.60 or higher.</span></span> |

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="8a10e-163">Stratégie de fusion d’exclusions</span><span class="sxs-lookup"><span data-stu-id="8a10e-163">Exclusion merge policy</span></span>

<span data-ttu-id="8a10e-164">Spécifiez la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="8a10e-164">Specify the merge policy for exclusions.</span></span> <span data-ttu-id="8a10e-165">Il peut s’agit d’une combinaison d’exclusions définies par l’administrateur et d’exclusions définies par l’utilisateur ( ) ou uniquement `merge` d’exclusions définies par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="8a10e-165">This can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="8a10e-166">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="8a10e-166">This setting can be used to restrict local users from defining their own exclusions.</span></span>

|<span data-ttu-id="8a10e-167">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-167">Section</span></span>|<span data-ttu-id="8a10e-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-168">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-169">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-169">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-170">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-170">**Key**</span></span> | <span data-ttu-id="8a10e-171">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="8a10e-171">exclusionsMergePolicy</span></span> |
| <span data-ttu-id="8a10e-172">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-172">**Data type**</span></span> | <span data-ttu-id="8a10e-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-173">String</span></span> |
| <span data-ttu-id="8a10e-174">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-174">**Possible values**</span></span> | <span data-ttu-id="8a10e-175">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-175">merge (default)</span></span> <br/> <span data-ttu-id="8a10e-176">admin_only</span><span class="sxs-lookup"><span data-stu-id="8a10e-176">admin_only</span></span> |
| <span data-ttu-id="8a10e-177">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-177">**Comments**</span></span> | <span data-ttu-id="8a10e-178">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-178">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="scan-exclusions"></a><span data-ttu-id="8a10e-179">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="8a10e-179">Scan exclusions</span></span>

<span data-ttu-id="8a10e-180">Spécifiez les entités exclues de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a10e-180">Specify entities excluded from being scanned.</span></span> <span data-ttu-id="8a10e-181">Les exclusions peuvent être spécifiées par des chemins d’accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a10e-181">Exclusions can be specified by full paths, extensions, or file names.</span></span>
<span data-ttu-id="8a10e-182">(Les exclusions sont spécifiées en tant que tableau d’éléments, l’administrateur peut spécifier autant d’éléments que nécessaire, dans n’importe quel ordre.)</span><span class="sxs-lookup"><span data-stu-id="8a10e-182">(Exclusions are specified as an array of items, administrator can specify as many elements as necessary, in any order.)</span></span>

|<span data-ttu-id="8a10e-183">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-183">Section</span></span>|<span data-ttu-id="8a10e-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-184">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-185">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-185">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-186">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-186">**Key**</span></span> | <span data-ttu-id="8a10e-187">exclusions</span><span class="sxs-lookup"><span data-stu-id="8a10e-187">exclusions</span></span> |
| <span data-ttu-id="8a10e-188">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-188">**Data type**</span></span> | <span data-ttu-id="8a10e-189">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-189">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-190">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-190">**Comments**</span></span> | <span data-ttu-id="8a10e-191">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-191">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-exclusion"></a><span data-ttu-id="8a10e-192">Type d’exclusion</span><span class="sxs-lookup"><span data-stu-id="8a10e-192">Type of exclusion</span></span>

<span data-ttu-id="8a10e-193">Spécifiez le contenu exclu de l’analyse par type.</span><span class="sxs-lookup"><span data-stu-id="8a10e-193">Specify content excluded from being scanned by type.</span></span>

|<span data-ttu-id="8a10e-194">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-194">Section</span></span>|<span data-ttu-id="8a10e-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-195">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-196">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-196">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-197">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-197">**Key**</span></span> | <span data-ttu-id="8a10e-198">$type</span><span class="sxs-lookup"><span data-stu-id="8a10e-198">$type</span></span> |
| <span data-ttu-id="8a10e-199">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-199">**Data type**</span></span> | <span data-ttu-id="8a10e-200">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-200">String</span></span> |
| <span data-ttu-id="8a10e-201">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-201">**Possible values**</span></span> | <span data-ttu-id="8a10e-202">excludedPath</span><span class="sxs-lookup"><span data-stu-id="8a10e-202">excludedPath</span></span> <br/> <span data-ttu-id="8a10e-203">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="8a10e-203">excludedFileExtension</span></span> <br/> <span data-ttu-id="8a10e-204">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="8a10e-204">excludedFileName</span></span> |

##### <a name="path-to-excluded-content"></a><span data-ttu-id="8a10e-205">Chemin d’accès au contenu exclu</span><span class="sxs-lookup"><span data-stu-id="8a10e-205">Path to excluded content</span></span>

<span data-ttu-id="8a10e-206">Spécifiez le contenu exclu de l’analyse par le chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="8a10e-206">Specify content excluded from being scanned by full file path.</span></span>

|<span data-ttu-id="8a10e-207">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-207">Section</span></span>|<span data-ttu-id="8a10e-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-208">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-209">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-209">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-210">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-210">**Key**</span></span> | <span data-ttu-id="8a10e-211">chemin</span><span class="sxs-lookup"><span data-stu-id="8a10e-211">path</span></span> |
| <span data-ttu-id="8a10e-212">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-212">**Data type**</span></span> | <span data-ttu-id="8a10e-213">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-213">String</span></span> |
| <span data-ttu-id="8a10e-214">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-214">**Possible values**</span></span> | <span data-ttu-id="8a10e-215">chemins d’accès valides</span><span class="sxs-lookup"><span data-stu-id="8a10e-215">valid paths</span></span> |
| <span data-ttu-id="8a10e-216">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-216">**Comments**</span></span> | <span data-ttu-id="8a10e-217">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="8a10e-217">Applicable only if *$type* is *excludedPath*</span></span> |

## <a name="supported-exclusion-types"></a><span data-ttu-id="8a10e-218">Types d’exclusion pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a10e-218">Supported exclusion types</span></span>

<span data-ttu-id="8a10e-219">Le tableau suivant indique les types d’exclusion pris en charge par Defender pour Endpoint sur Mac.</span><span class="sxs-lookup"><span data-stu-id="8a10e-219">The follow table shows the exclusion types supported by Defender for Endpoint on Mac.</span></span>

<span data-ttu-id="8a10e-220">Exclusion</span><span class="sxs-lookup"><span data-stu-id="8a10e-220">Exclusion</span></span> | <span data-ttu-id="8a10e-221">Définition</span><span class="sxs-lookup"><span data-stu-id="8a10e-221">Definition</span></span> | <span data-ttu-id="8a10e-222">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a10e-222">Examples</span></span>
---|---|---
<span data-ttu-id="8a10e-223">Extension de fichier</span><span class="sxs-lookup"><span data-stu-id="8a10e-223">File extension</span></span> | <span data-ttu-id="8a10e-224">Tous les fichiers avec l’extension, n’importe où sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="8a10e-224">All files with the extension, anywhere on the device</span></span> | `.test`
<span data-ttu-id="8a10e-225">Fichier</span><span class="sxs-lookup"><span data-stu-id="8a10e-225">File</span></span> | <span data-ttu-id="8a10e-226">Un fichier spécifique identifié par le chemin d’accès complet</span><span class="sxs-lookup"><span data-stu-id="8a10e-226">A specific file identified by the full path</span></span> | `/var/log/test.log`<br/>`/var/log/*.log`<br/>`/var/log/install.?.log`
<span data-ttu-id="8a10e-227">Dossier</span><span class="sxs-lookup"><span data-stu-id="8a10e-227">Folder</span></span> | <span data-ttu-id="8a10e-228">Tous les fichiers sous le dossier spécifié (de manière récursive)</span><span class="sxs-lookup"><span data-stu-id="8a10e-228">All files under the specified folder (recursively)</span></span> | `/var/log/`<br/>`/var/*/`
<span data-ttu-id="8a10e-229">Processus</span><span class="sxs-lookup"><span data-stu-id="8a10e-229">Process</span></span> | <span data-ttu-id="8a10e-230">Un processus spécifique (spécifié par le chemin d’accès complet ou le nom de fichier) et tous les fichiers ouverts par celui-ci</span><span class="sxs-lookup"><span data-stu-id="8a10e-230">A specific process (specified either by the full path or file name) and all files opened by it</span></span> | `/bin/cat`<br/>`cat`<br/>`c?t`

> [!IMPORTANT]
> <span data-ttu-id="8a10e-231">Les chemins ci-dessus doivent être des liens durs, et non symboliques, pour être correctement exclus.</span><span class="sxs-lookup"><span data-stu-id="8a10e-231">The paths above must be hard links, not symbolic links, in order to be successfully excluded.</span></span> <span data-ttu-id="8a10e-232">Vous pouvez vérifier si un chemin d’accès est un lien symbolique en exécutant `file <path-name>` .</span><span class="sxs-lookup"><span data-stu-id="8a10e-232">You can check if a path is a symbolic link by running `file <path-name>`.</span></span>

<span data-ttu-id="8a10e-233">Les exclusions de fichiers, de dossiers et de processus prisent en charge les caractères génériques suivants :</span><span class="sxs-lookup"><span data-stu-id="8a10e-233">File, folder, and process exclusions support the following wildcards:</span></span>

<span data-ttu-id="8a10e-234">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="8a10e-234">Wildcard</span></span> | <span data-ttu-id="8a10e-235">Description</span><span class="sxs-lookup"><span data-stu-id="8a10e-235">Description</span></span> | <span data-ttu-id="8a10e-236">Exemple</span><span class="sxs-lookup"><span data-stu-id="8a10e-236">Example</span></span> | <span data-ttu-id="8a10e-237">Correspondances</span><span class="sxs-lookup"><span data-stu-id="8a10e-237">Matches</span></span> | <span data-ttu-id="8a10e-238">Ne correspond pas</span><span class="sxs-lookup"><span data-stu-id="8a10e-238">Does not match</span></span>
---|---|---|---|---
\* |    <span data-ttu-id="8a10e-239">Correspond à n’importe quel nombre de caractères, y compris aucun (notez que lorsque ce caractère générique est utilisé à l’intérieur d’un chemin d’accès, il ne remplace qu’un seul dossier)</span><span class="sxs-lookup"><span data-stu-id="8a10e-239">Matches any number of any characters including none (note that when this wildcard is used inside a path it will substitute only one folder)</span></span> | `/var/\*/\*.log` | `/var/log/system.log` | `/var/log/nested/system.log`
<span data-ttu-id="8a10e-240">?</span><span class="sxs-lookup"><span data-stu-id="8a10e-240">?</span></span> | <span data-ttu-id="8a10e-241">Correspond à n’importe quel caractère</span><span class="sxs-lookup"><span data-stu-id="8a10e-241">Matches any single character</span></span> | `file?.log` | `file1.log`<br/>`file2.log` | `file123.log`

##### <a name="path-type-file--directory"></a><span data-ttu-id="8a10e-242">Type de chemin d’accès (fichier/répertoire)</span><span class="sxs-lookup"><span data-stu-id="8a10e-242">Path type (file / directory)</span></span>

<span data-ttu-id="8a10e-243">Indiquez si la *propriété du* chemin d’accès fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-243">Indicate if the *path* property refers to a file or directory.</span></span> 

|<span data-ttu-id="8a10e-244">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-244">Section</span></span>|<span data-ttu-id="8a10e-245">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-245">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-246">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-246">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-247">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-247">**Key**</span></span> | <span data-ttu-id="8a10e-248">isDirectory</span><span class="sxs-lookup"><span data-stu-id="8a10e-248">isDirectory</span></span> |
| <span data-ttu-id="8a10e-249">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-249">**Data type**</span></span> | <span data-ttu-id="8a10e-250">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-250">Boolean</span></span> |
| <span data-ttu-id="8a10e-251">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-251">**Possible values**</span></span> | <span data-ttu-id="8a10e-252">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-252">false (default)</span></span> <br/> <span data-ttu-id="8a10e-253">true</span><span class="sxs-lookup"><span data-stu-id="8a10e-253">true</span></span> |
| <span data-ttu-id="8a10e-254">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-254">**Comments**</span></span> | <span data-ttu-id="8a10e-255">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="8a10e-255">Applicable only if *$type* is *excludedPath*</span></span> |

##### <a name="file-extension-excluded-from-the-scan"></a><span data-ttu-id="8a10e-256">Extension de fichier exclue de l’analyse</span><span class="sxs-lookup"><span data-stu-id="8a10e-256">File extension excluded from the scan</span></span>

<span data-ttu-id="8a10e-257">Spécifiez le contenu exclu de l’analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="8a10e-257">Specify content excluded from being scanned by file extension.</span></span>

|<span data-ttu-id="8a10e-258">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-258">Section</span></span>|<span data-ttu-id="8a10e-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-259">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-260">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-260">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-261">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-261">**Key**</span></span> | <span data-ttu-id="8a10e-262">extension</span><span class="sxs-lookup"><span data-stu-id="8a10e-262">extension</span></span> |
| <span data-ttu-id="8a10e-263">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-263">**Data type**</span></span> | <span data-ttu-id="8a10e-264">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-264">String</span></span> |
| <span data-ttu-id="8a10e-265">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-265">**Possible values**</span></span> | <span data-ttu-id="8a10e-266">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="8a10e-266">valid file extensions</span></span> |
| <span data-ttu-id="8a10e-267">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-267">**Comments**</span></span> | <span data-ttu-id="8a10e-268">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="8a10e-268">Applicable only if *$type* is *excludedFileExtension*</span></span> |

##### <a name="process-excluded-from-the-scan"></a><span data-ttu-id="8a10e-269">Processus exclu de l’analyse</span><span class="sxs-lookup"><span data-stu-id="8a10e-269">Process excluded from the scan</span></span>

<span data-ttu-id="8a10e-270">Spécifiez un processus pour lequel toute l’activité de fichier est exclue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a10e-270">Specify a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="8a10e-271">Le processus peut être spécifié par son nom (par exemple) ou son chemin d’accès complet `cat` (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="8a10e-271">The process can be specified either by its name (e.g. `cat`) or full path (e.g. `/bin/cat`).</span></span>

|<span data-ttu-id="8a10e-272">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-272">Section</span></span>|<span data-ttu-id="8a10e-273">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-273">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-274">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-274">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-275">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-275">**Key**</span></span> | <span data-ttu-id="8a10e-276">name</span><span class="sxs-lookup"><span data-stu-id="8a10e-276">name</span></span> |
| <span data-ttu-id="8a10e-277">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-277">**Data type**</span></span> | <span data-ttu-id="8a10e-278">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-278">String</span></span> |
| <span data-ttu-id="8a10e-279">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-279">**Possible values**</span></span> | <span data-ttu-id="8a10e-280">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-280">any string</span></span> |
| <span data-ttu-id="8a10e-281">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-281">**Comments**</span></span> | <span data-ttu-id="8a10e-282">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="8a10e-282">Applicable only if *$type* is *excludedFileName*</span></span> |

#### <a name="allowed-threats"></a><span data-ttu-id="8a10e-283">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="8a10e-283">Allowed threats</span></span>

<span data-ttu-id="8a10e-284">Spécifiez les menaces par nom qui ne sont pas bloquées par Defender pour endpoint sur Mac.</span><span class="sxs-lookup"><span data-stu-id="8a10e-284">Specify threats by name that are not blocked by Defender for Endpoint on Mac.</span></span> <span data-ttu-id="8a10e-285">Ces menaces seront autorisées à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="8a10e-285">These threats will be allowed to run.</span></span>

|<span data-ttu-id="8a10e-286">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-286">Section</span></span>|<span data-ttu-id="8a10e-287">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-287">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-288">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-288">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-289">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-289">**Key**</span></span> | <span data-ttu-id="8a10e-290">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="8a10e-290">allowedThreats</span></span> |
| <span data-ttu-id="8a10e-291">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-291">**Data type**</span></span> | <span data-ttu-id="8a10e-292">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8a10e-292">Array of strings</span></span> |

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="8a10e-293">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="8a10e-293">Disallowed threat actions</span></span>

<span data-ttu-id="8a10e-294">Limite les actions que l’utilisateur local d’un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="8a10e-294">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="8a10e-295">Les actions incluses dans cette liste ne sont pas affichées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a10e-295">The actions included in this list are not displayed in the user interface.</span></span>

|<span data-ttu-id="8a10e-296">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-296">Section</span></span>|<span data-ttu-id="8a10e-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-297">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-298">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-298">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-299">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-299">**Key**</span></span> | <span data-ttu-id="8a10e-300">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="8a10e-300">disallowedThreatActions</span></span> |
| <span data-ttu-id="8a10e-301">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-301">**Data type**</span></span> | <span data-ttu-id="8a10e-302">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="8a10e-302">Array of strings</span></span> |
| <span data-ttu-id="8a10e-303">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-303">**Possible values**</span></span> | <span data-ttu-id="8a10e-304">autoriser (empêche les utilisateurs d’autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="8a10e-304">allow (restricts users from allowing threats)</span></span> <br/> <span data-ttu-id="8a10e-305">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="8a10e-305">restore (restricts users from restoring threats from the quarantine)</span></span> |
| <span data-ttu-id="8a10e-306">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-306">**Comments**</span></span> | <span data-ttu-id="8a10e-307">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-307">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="threat-type-settings"></a><span data-ttu-id="8a10e-308">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="8a10e-308">Threat type settings</span></span>

<span data-ttu-id="8a10e-309">Spécifiez comment certains types de menaces sont gérés par Microsoft Defender pour point de terminaison sur macOS.</span><span class="sxs-lookup"><span data-stu-id="8a10e-309">Specify how certain threat types are handled by Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="8a10e-310">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-310">Section</span></span>|<span data-ttu-id="8a10e-311">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-311">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-312">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-312">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-313">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-313">**Key**</span></span> | <span data-ttu-id="8a10e-314">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="8a10e-314">threatTypeSettings</span></span> |
| <span data-ttu-id="8a10e-315">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-315">**Data type**</span></span> | <span data-ttu-id="8a10e-316">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-316">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-317">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-317">**Comments**</span></span> | <span data-ttu-id="8a10e-318">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-318">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="threat-type"></a><span data-ttu-id="8a10e-319">Type de menace</span><span class="sxs-lookup"><span data-stu-id="8a10e-319">Threat type</span></span>

<span data-ttu-id="8a10e-320">Spécifiez les types de menaces.</span><span class="sxs-lookup"><span data-stu-id="8a10e-320">Specify threat types.</span></span>

|<span data-ttu-id="8a10e-321">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-321">Section</span></span>|<span data-ttu-id="8a10e-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-322">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-323">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-323">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-324">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-324">**Key**</span></span> | <span data-ttu-id="8a10e-325">clé</span><span class="sxs-lookup"><span data-stu-id="8a10e-325">key</span></span> |
| <span data-ttu-id="8a10e-326">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-326">**Data type**</span></span> | <span data-ttu-id="8a10e-327">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-327">String</span></span> |
| <span data-ttu-id="8a10e-328">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-328">**Possible values**</span></span> | <span data-ttu-id="8a10e-329">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="8a10e-329">potentially_unwanted_application</span></span> <br/> <span data-ttu-id="8a10e-330">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="8a10e-330">archive_bomb</span></span> |

##### <a name="action-to-take"></a><span data-ttu-id="8a10e-331">Mesures à prendre</span><span class="sxs-lookup"><span data-stu-id="8a10e-331">Action to take</span></span>

<span data-ttu-id="8a10e-332">Spécifiez l’action à prendre lorsqu’une menace du type spécifié dans la section précédente est détectée.</span><span class="sxs-lookup"><span data-stu-id="8a10e-332">Specify what action to take when a threat of the type specified in the preceding section is detected.</span></span> <span data-ttu-id="8a10e-333">Choisissez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a10e-333">Choose from the following options:</span></span>

- <span data-ttu-id="8a10e-334">**Audit**: votre appareil n’est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8a10e-334">**Audit**: your device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="8a10e-335">**Bloquer**: votre appareil est protégé contre ce type de menace et vous êtes averti dans l’interface utilisateur et la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a10e-335">**Block**: your device is protected against this type of threat and you are notified in the user interface and the security console.</span></span>
- <span data-ttu-id="8a10e-336">**Off**: votre appareil n’est pas protégé contre ce type de menace et rien n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="8a10e-336">**Off**: your device is not protected against this type of threat and nothing is logged.</span></span>

|<span data-ttu-id="8a10e-337">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-337">Section</span></span>|<span data-ttu-id="8a10e-338">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-338">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-339">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-339">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-340">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-340">**Key**</span></span> | <span data-ttu-id="8a10e-341">valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-341">value</span></span> |
| <span data-ttu-id="8a10e-342">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-342">**Data type**</span></span> | <span data-ttu-id="8a10e-343">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-343">String</span></span> |
| <span data-ttu-id="8a10e-344">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-344">**Possible values**</span></span> | <span data-ttu-id="8a10e-345">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-345">audit (default)</span></span> <br/> <span data-ttu-id="8a10e-346">block</span><span class="sxs-lookup"><span data-stu-id="8a10e-346">block</span></span> <br/> <span data-ttu-id="8a10e-347">off</span><span class="sxs-lookup"><span data-stu-id="8a10e-347">off</span></span> |

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="8a10e-348">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="8a10e-348">Threat type settings merge policy</span></span>

<span data-ttu-id="8a10e-349">Spécifiez la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="8a10e-349">Specify the merge policy for threat type settings.</span></span> <span data-ttu-id="8a10e-350">Il peut s’agit d’une combinaison de paramètres définis par l’administrateur et de paramètres définis par l’utilisateur ( ) ou uniquement de `merge` paramètres définis par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="8a10e-350">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="8a10e-351">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="8a10e-351">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

|<span data-ttu-id="8a10e-352">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-352">Section</span></span>|<span data-ttu-id="8a10e-353">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-353">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-354">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-354">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-355">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-355">**Key**</span></span> | <span data-ttu-id="8a10e-356">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="8a10e-356">threatTypeSettingsMergePolicy</span></span> |
| <span data-ttu-id="8a10e-357">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-357">**Data type**</span></span> | <span data-ttu-id="8a10e-358">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-358">String</span></span> |
| <span data-ttu-id="8a10e-359">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-359">**Possible values**</span></span> | <span data-ttu-id="8a10e-360">merge (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-360">merge (default)</span></span> <br/> <span data-ttu-id="8a10e-361">admin_only</span><span class="sxs-lookup"><span data-stu-id="8a10e-361">admin_only</span></span> |
| <span data-ttu-id="8a10e-362">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-362">**Comments**</span></span> | <span data-ttu-id="8a10e-363">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-363">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="8a10e-364">Conservation de l’historique d’analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="8a10e-364">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="8a10e-365">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l’historique d’analyse sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8a10e-365">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="8a10e-366">Les anciens résultats d’analyse sont supprimés de l’historique.</span><span class="sxs-lookup"><span data-stu-id="8a10e-366">Old scan results are removed from the history.</span></span> <span data-ttu-id="8a10e-367">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="8a10e-367">Old quarantined files that are also removed from the disk.</span></span>

|<span data-ttu-id="8a10e-368">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-368">Section</span></span>|<span data-ttu-id="8a10e-369">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-369">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-370">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-370">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-371">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-371">**Key**</span></span> | <span data-ttu-id="8a10e-372">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="8a10e-372">scanResultsRetentionDays</span></span> |
| <span data-ttu-id="8a10e-373">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-373">**Data type**</span></span> | <span data-ttu-id="8a10e-374">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-374">String</span></span> |
| <span data-ttu-id="8a10e-375">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-375">**Possible values**</span></span> | <span data-ttu-id="8a10e-376">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="8a10e-376">90 (default).</span></span> <span data-ttu-id="8a10e-377">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="8a10e-377">Allowed values are from 1 day to 180 days.</span></span> |
| <span data-ttu-id="8a10e-378">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-378">**Comments**</span></span> | <span data-ttu-id="8a10e-379">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-379">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="8a10e-380">Nombre maximal d’éléments dans l’historique d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="8a10e-380">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="8a10e-381">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a10e-381">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="8a10e-382">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="8a10e-382">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

|<span data-ttu-id="8a10e-383">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-383">Section</span></span>|<span data-ttu-id="8a10e-384">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-384">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-385">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-385">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-386">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-386">**Key**</span></span> | <span data-ttu-id="8a10e-387">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="8a10e-387">scanHistoryMaximumItems</span></span> |
| <span data-ttu-id="8a10e-388">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-388">**Data type**</span></span> | <span data-ttu-id="8a10e-389">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-389">String</span></span> |
| <span data-ttu-id="8a10e-390">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-390">**Possible values**</span></span> | <span data-ttu-id="8a10e-391">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="8a10e-391">10000 (default).</span></span> <span data-ttu-id="8a10e-392">Les valeurs autorisées sont de 5 000 à 15 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="8a10e-392">Allowed values are from 5000 items to 15000 items.</span></span> |
| <span data-ttu-id="8a10e-393">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-393">**Comments**</span></span> | <span data-ttu-id="8a10e-394">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-394">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="8a10e-395">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="8a10e-395">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="8a10e-396">Configurez les fonctionnalités de protection informatique de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="8a10e-396">Configure the cloud-driven protection features of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="8a10e-397">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-397">Section</span></span>|<span data-ttu-id="8a10e-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-398">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-399">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-399">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-400">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-400">**Key**</span></span> | <span data-ttu-id="8a10e-401">cloudService</span><span class="sxs-lookup"><span data-stu-id="8a10e-401">cloudService</span></span> |
| <span data-ttu-id="8a10e-402">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-402">**Data type**</span></span> | <span data-ttu-id="8a10e-403">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-403">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-404">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-404">**Comments**</span></span> | <span data-ttu-id="8a10e-405">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-405">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="8a10e-406">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="8a10e-406">Enable / disable cloud-delivered protection</span></span>

<span data-ttu-id="8a10e-407">Spécifiez s’il faut activer ou non la protection de l’appareil livrée par le cloud.</span><span class="sxs-lookup"><span data-stu-id="8a10e-407">Specify whether to enable cloud-delivered protection the device or not.</span></span> <span data-ttu-id="8a10e-408">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="8a10e-408">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

|<span data-ttu-id="8a10e-409">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-409">Section</span></span>|<span data-ttu-id="8a10e-410">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-410">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-411">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-411">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-412">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-412">**Key**</span></span> | <span data-ttu-id="8a10e-413">activé</span><span class="sxs-lookup"><span data-stu-id="8a10e-413">enabled</span></span> |
| <span data-ttu-id="8a10e-414">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-414">**Data type**</span></span> | <span data-ttu-id="8a10e-415">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-415">Boolean</span></span> |
| <span data-ttu-id="8a10e-416">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-416">**Possible values**</span></span> | <span data-ttu-id="8a10e-417">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-417">true (default)</span></span> <br/> <span data-ttu-id="8a10e-418">false</span><span class="sxs-lookup"><span data-stu-id="8a10e-418">false</span></span> |

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="8a10e-419">Niveau de collection de diagnostics</span><span class="sxs-lookup"><span data-stu-id="8a10e-419">Diagnostic collection level</span></span>

<span data-ttu-id="8a10e-420">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Microsoft Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="8a10e-420">Diagnostic data is used to keep Microsoft Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="8a10e-421">Ce paramètre détermine le niveau de diagnostics envoyés par Microsoft Defender pour endpoint à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a10e-421">This setting determines the level of diagnostics sent by Microsoft Defender for Endpoint to Microsoft.</span></span>

|<span data-ttu-id="8a10e-422">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-422">Section</span></span>|<span data-ttu-id="8a10e-423">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-423">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-424">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-424">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-425">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-425">**Key**</span></span> | <span data-ttu-id="8a10e-426">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="8a10e-426">diagnosticLevel</span></span> |
| <span data-ttu-id="8a10e-427">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-427">**Data type**</span></span> | <span data-ttu-id="8a10e-428">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-428">String</span></span> |
| <span data-ttu-id="8a10e-429">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-429">**Possible values**</span></span> | <span data-ttu-id="8a10e-430">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-430">optional (default)</span></span> <br/> <span data-ttu-id="8a10e-431">obligatoire</span><span class="sxs-lookup"><span data-stu-id="8a10e-431">required</span></span> |

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="8a10e-432">Activer/désactiver les envois automatiques d’échantillons</span><span class="sxs-lookup"><span data-stu-id="8a10e-432">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="8a10e-433">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a10e-433">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="8a10e-434">Vous êtes invité à vous demander si le fichier envoyé est susceptible de contenir des informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="8a10e-434">You are prompted if the submitted file is likely to contain personal information.</span></span>

|<span data-ttu-id="8a10e-435">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-435">Section</span></span>|<span data-ttu-id="8a10e-436">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-436">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-437">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-437">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-438">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-438">**Key**</span></span> | <span data-ttu-id="8a10e-439">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="8a10e-439">automaticSampleSubmission</span></span> |
| <span data-ttu-id="8a10e-440">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-440">**Data type**</span></span> | <span data-ttu-id="8a10e-441">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-441">Boolean</span></span> |
| <span data-ttu-id="8a10e-442">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-442">**Possible values**</span></span> | <span data-ttu-id="8a10e-443">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-443">true (default)</span></span> <br/> <span data-ttu-id="8a10e-444">false</span><span class="sxs-lookup"><span data-stu-id="8a10e-444">false</span></span> |

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="8a10e-445">Activer/désactiver les mises à jour automatiques de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="8a10e-445">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="8a10e-446">Détermine si les mises à jour d’informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="8a10e-446">Determines whether security intelligence updates are installed automatically:</span></span>

|<span data-ttu-id="8a10e-447">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-447">Section</span></span>|<span data-ttu-id="8a10e-448">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-448">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-449">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-449">**Key**</span></span> | <span data-ttu-id="8a10e-450">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="8a10e-450">automaticDefinitionUpdateEnabled</span></span> |
| <span data-ttu-id="8a10e-451">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-451">**Data type**</span></span> | <span data-ttu-id="8a10e-452">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-452">Boolean</span></span> |
| <span data-ttu-id="8a10e-453">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-453">**Possible values**</span></span> | <span data-ttu-id="8a10e-454">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-454">true (default)</span></span> <br/> <span data-ttu-id="8a10e-455">false</span><span class="sxs-lookup"><span data-stu-id="8a10e-455">false</span></span> |

### <a name="user-interface-preferences"></a><span data-ttu-id="8a10e-456">Préférences de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="8a10e-456">User interface preferences</span></span>

<span data-ttu-id="8a10e-457">Gérez les préférences pour l’interface utilisateur de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="8a10e-457">Manage the preferences for the user interface of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="8a10e-458">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-458">Section</span></span>|<span data-ttu-id="8a10e-459">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-459">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-460">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-460">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-461">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-461">**Key**</span></span> | <span data-ttu-id="8a10e-462">userInterface</span><span class="sxs-lookup"><span data-stu-id="8a10e-462">userInterface</span></span> |
| <span data-ttu-id="8a10e-463">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-463">**Data type**</span></span> | <span data-ttu-id="8a10e-464">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-464">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-465">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-465">**Comments**</span></span> | <span data-ttu-id="8a10e-466">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-466">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="show--hide-status-menu-icon"></a><span data-ttu-id="8a10e-467">Afficher/masquer l’icône du menu d’état</span><span class="sxs-lookup"><span data-stu-id="8a10e-467">Show / hide status menu icon</span></span>

<span data-ttu-id="8a10e-468">Spécifiez s’il faut afficher ou masquer l’icône du menu d’état dans le coin supérieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="8a10e-468">Specify whether to show or hide the status menu icon in the top-right corner of the screen.</span></span>

|<span data-ttu-id="8a10e-469">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-469">Section</span></span>|<span data-ttu-id="8a10e-470">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-470">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-471">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-471">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-472">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-472">**Key**</span></span> | <span data-ttu-id="8a10e-473">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="8a10e-473">hideStatusMenuIcon</span></span> |
| <span data-ttu-id="8a10e-474">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-474">**Data type**</span></span> | <span data-ttu-id="8a10e-475">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="8a10e-475">Boolean</span></span> |
| <span data-ttu-id="8a10e-476">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-476">**Possible values**</span></span> | <span data-ttu-id="8a10e-477">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-477">false (default)</span></span> <br/> <span data-ttu-id="8a10e-478">true</span><span class="sxs-lookup"><span data-stu-id="8a10e-478">true</span></span> |

#### <a name="show--hide-option-to-send-feedback"></a><span data-ttu-id="8a10e-479">Afficher /masquer l’option d’envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="8a10e-479">Show / hide option to send feedback</span></span>

<span data-ttu-id="8a10e-480">Spécifiez si les utilisateurs peuvent envoyer des commentaires à Microsoft en allant à `Help`  >  `Send Feedback` .</span><span class="sxs-lookup"><span data-stu-id="8a10e-480">Specify whether users can submit feedback to Microsoft by going to `Help` > `Send Feedback`.</span></span>

|<span data-ttu-id="8a10e-481">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-481">Section</span></span>|<span data-ttu-id="8a10e-482">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-482">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-483">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-483">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-484">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-484">**Key**</span></span> | <span data-ttu-id="8a10e-485">userInitiatedFeedback</span><span class="sxs-lookup"><span data-stu-id="8a10e-485">userInitiatedFeedback</span></span> |
| <span data-ttu-id="8a10e-486">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-486">**Data type**</span></span> | <span data-ttu-id="8a10e-487">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-487">String</span></span> |
| <span data-ttu-id="8a10e-488">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-488">**Possible values**</span></span> | <span data-ttu-id="8a10e-489">activé (par défaut)</span><span class="sxs-lookup"><span data-stu-id="8a10e-489">enabled (default)</span></span> <br/> <span data-ttu-id="8a10e-490">désactivé</span><span class="sxs-lookup"><span data-stu-id="8a10e-490">disabled</span></span> |
| <span data-ttu-id="8a10e-491">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-491">**Comments**</span></span> | <span data-ttu-id="8a10e-492">Disponible dans Microsoft Defender pour Endpoint version 101.19.61 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="8a10e-492">Available in Microsoft Defender for Endpoint version 101.19.61 or higher.</span></span> |

### <a name="endpoint-detection-and-response-preferences"></a><span data-ttu-id="8a10e-493">Préférences de détection et de réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8a10e-493">Endpoint detection and response preferences</span></span>

<span data-ttu-id="8a10e-494">Gérez les préférences du composant protection évolutive des points de terminaison (PEPT) de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="8a10e-494">Manage the preferences of the endpoint detection and response (EDR) component of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="8a10e-495">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-495">Section</span></span>|<span data-ttu-id="8a10e-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-496">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-497">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-497">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-498">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-498">**Key**</span></span> | <span data-ttu-id="8a10e-499">edr</span><span class="sxs-lookup"><span data-stu-id="8a10e-499">edr</span></span> |
| <span data-ttu-id="8a10e-500">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-500">**Data type**</span></span> | <span data-ttu-id="8a10e-501">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-501">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-502">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-502">**Comments**</span></span> | <span data-ttu-id="8a10e-503">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-503">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="device-tags"></a><span data-ttu-id="8a10e-504">Balises d’appareil</span><span class="sxs-lookup"><span data-stu-id="8a10e-504">Device tags</span></span>

<span data-ttu-id="8a10e-505">Spécifiez un nom de balise et sa valeur.</span><span class="sxs-lookup"><span data-stu-id="8a10e-505">Specify a tag name and its value.</span></span> 

- <span data-ttu-id="8a10e-506">La balise GROUP balise l’appareil avec la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8a10e-506">The GROUP tag, tags the device with the specified value.</span></span> <span data-ttu-id="8a10e-507">La balise est reflétée dans le portail sous la page de l’appareil et peut être utilisée pour le filtrage et le regroupement des appareils.</span><span class="sxs-lookup"><span data-stu-id="8a10e-507">The tag is reflected in the portal under the device page and can be used for filtering and grouping devices.</span></span>

|<span data-ttu-id="8a10e-508">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-508">Section</span></span>|<span data-ttu-id="8a10e-509">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-509">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-510">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-510">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-511">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-511">**Key**</span></span> | <span data-ttu-id="8a10e-512">étiquettes</span><span class="sxs-lookup"><span data-stu-id="8a10e-512">tags</span></span> |
| <span data-ttu-id="8a10e-513">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-513">**Data type**</span></span> | <span data-ttu-id="8a10e-514">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="8a10e-514">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="8a10e-515">**Comments**</span><span class="sxs-lookup"><span data-stu-id="8a10e-515">**Comments**</span></span> | <span data-ttu-id="8a10e-516">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="8a10e-516">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-tag"></a><span data-ttu-id="8a10e-517">Type de balise</span><span class="sxs-lookup"><span data-stu-id="8a10e-517">Type of tag</span></span>

<span data-ttu-id="8a10e-518">Spécifie le type de balise</span><span class="sxs-lookup"><span data-stu-id="8a10e-518">Specifies the type of tag</span></span>

|<span data-ttu-id="8a10e-519">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-519">Section</span></span>|<span data-ttu-id="8a10e-520">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-520">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-521">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-521">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-522">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-522">**Key**</span></span> | <span data-ttu-id="8a10e-523">clé</span><span class="sxs-lookup"><span data-stu-id="8a10e-523">key</span></span> |
| <span data-ttu-id="8a10e-524">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-524">**Data type**</span></span> | <span data-ttu-id="8a10e-525">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-525">String</span></span> |
| <span data-ttu-id="8a10e-526">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-526">**Possible values**</span></span> | `GROUP` |

##### <a name="value-of-tag"></a><span data-ttu-id="8a10e-527">Valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="8a10e-527">Value of tag</span></span>

<span data-ttu-id="8a10e-528">Spécifie la valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="8a10e-528">Specifies the value of tag</span></span>

|<span data-ttu-id="8a10e-529">Section</span><span class="sxs-lookup"><span data-stu-id="8a10e-529">Section</span></span>|<span data-ttu-id="8a10e-530">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-530">Value</span></span>|
|:---|:---|
| <span data-ttu-id="8a10e-531">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8a10e-531">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="8a10e-532">**Clé**</span><span class="sxs-lookup"><span data-stu-id="8a10e-532">**Key**</span></span> | <span data-ttu-id="8a10e-533">valeur</span><span class="sxs-lookup"><span data-stu-id="8a10e-533">value</span></span> |
| <span data-ttu-id="8a10e-534">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8a10e-534">**Data type**</span></span> | <span data-ttu-id="8a10e-535">Chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-535">String</span></span> |
| <span data-ttu-id="8a10e-536">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="8a10e-536">**Possible values**</span></span> | <span data-ttu-id="8a10e-537">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="8a10e-537">any string</span></span> |

> [!IMPORTANT]  
> - <span data-ttu-id="8a10e-538">Une seule valeur par type de balise peut être définie.</span><span class="sxs-lookup"><span data-stu-id="8a10e-538">Only one value per tag type can be set.</span></span>
> - <span data-ttu-id="8a10e-539">Le type de balises est unique et ne doit pas être répété dans le même profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="8a10e-539">Type of tags are unique, and should not be repeated in the same configuration profile.</span></span>

## <a name="recommended-configuration-profile"></a><span data-ttu-id="8a10e-540">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="8a10e-540">Recommended configuration profile</span></span>

<span data-ttu-id="8a10e-541">Pour commencer, nous recommandons la configuration suivante pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Microsoft Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="8a10e-541">To get started, we recommend the following configuration for your enterprise to take advantage of all protection features that Microsoft Defender for Endpoint provides.</span></span>

<span data-ttu-id="8a10e-542">Le profil de configuration suivant (ou, dans le cas de JAMF, une liste de propriétés qui peut être téléchargée dans le profil de configuration des paramètres personnalisés) sera :</span><span class="sxs-lookup"><span data-stu-id="8a10e-542">The following configuration profile (or, in case of JAMF, a property list that could be uploaded into the custom settings configuration profile) will:</span></span>
- <span data-ttu-id="8a10e-543">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="8a10e-543">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="8a10e-544">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="8a10e-544">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="8a10e-545">**Les applications potentiellement indésirables (PUA) sont** bloquées</span><span class="sxs-lookup"><span data-stu-id="8a10e-545">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="8a10e-546">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans Microsoft Defender pour les journaux de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8a10e-546">**Archive bombs** (file with a high compression rate) are audited to Microsoft Defender for Endpoint logs</span></span>
- <span data-ttu-id="8a10e-547">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="8a10e-547">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="8a10e-548">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="8a10e-548">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="8a10e-549">Activer l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="8a10e-549">Enable automatic sample submission</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="8a10e-550">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="8a10e-550">Property list for JAMF configuration profile</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>antivirusEngine</key>
    <dict>
        <key>enableRealTimeProtection</key>
        <true/>
        <key>threatTypeSettings</key>
        <array>
            <dict>
                <key>key</key>
                <string>potentially_unwanted_application</string>
                <key>value</key>
                <string>block</string>
            </dict>
            <dict>
                <key>key</key>
                <string>archive_bomb</string>
                <key>value</key>
                <string>audit</string>
            </dict>
        </array>
    </dict>
    <key>cloudService</key>
    <dict>
        <key>enabled</key>
        <true/>
        <key>automaticSampleSubmission</key>
        <true/>
        <key>automaticDefinitionUpdateEnabled</key>
        <true/>
    </dict>
</dict>
</plist>
```

### <a name="intune-profile"></a><span data-ttu-id="8a10e-551">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="8a10e-551">Intune profile</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1">
    <dict>
        <key>PayloadUUID</key>
        <string>C4E6A782-0C8D-44AB-A025-EB893987A295</string>
        <key>PayloadType</key>
        <string>Configuration</string>
        <key>PayloadOrganization</key>
        <string>Microsoft</string>
        <key>PayloadIdentifier</key>
        <string>com.microsoft.wdav</string>
        <key>PayloadDisplayName</key>
        <string>Microsoft Defender for Endpoint settings</string>
        <key>PayloadDescription</key>
        <string>Microsoft Defender for Endpoint configuration settings</string>
        <key>PayloadVersion</key>
        <integer>1</integer>
        <key>PayloadEnabled</key>
        <true/>
        <key>PayloadRemovalDisallowed</key>
        <true/>
        <key>PayloadScope</key>
        <string>System</string>
        <key>PayloadContent</key>
        <array>
            <dict>
                <key>PayloadUUID</key>
                <string>99DBC2BC-3B3A-46A2-A413-C8F9BB9A7295</string>
                <key>PayloadType</key>
                <string>com.microsoft.wdav</string>
                <key>PayloadOrganization</key>
                <string>Microsoft</string>
                <key>PayloadIdentifier</key>
                <string>com.microsoft.wdav</string>
                <key>PayloadDisplayName</key>
                <string>Microsoft Defender for Endpoint configuration settings</string>
                <key>PayloadDescription</key>
                <string/>
                <key>PayloadVersion</key>
                <integer>1</integer>
                <key>PayloadEnabled</key>
                <true/>
                <key>antivirusEngine</key>
                <dict>
                    <key>enableRealTimeProtection</key>
                    <true/>
                    <key>threatTypeSettings</key>
                    <array>
                        <dict>
                            <key>key</key>
                            <string>potentially_unwanted_application</string>
                            <key>value</key>
                            <string>block</string>
                        </dict>
                        <dict>
                            <key>key</key>
                            <string>archive_bomb</string>
                            <key>value</key>
                            <string>audit</string>
                        </dict>
                    </array>
                </dict>
                <key>cloudService</key>
                <dict>
                    <key>enabled</key>
                    <true/>
                    <key>automaticSampleSubmission</key>
                    <true/>
                    <key>automaticDefinitionUpdateEnabled</key>
                    <true/>
                </dict>
            </dict>
        </array>
    </dict>
</plist>
```

## <a name="full-configuration-profile-example"></a><span data-ttu-id="8a10e-552">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="8a10e-552">Full configuration profile example</span></span>

<span data-ttu-id="8a10e-553">Les modèles suivants contiennent des entrées pour tous les paramètres décrits dans ce document et peuvent être utilisés pour des scénarios plus avancés dans lequel vous souhaitez mieux contrôler Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="8a10e-553">The following templates contain entries for all settings described in this document and can be used for more advanced scenarios where you want more control over Microsoft Defender for Endpoint on macOS.</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="8a10e-554">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="8a10e-554">Property list for JAMF configuration profile</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>antivirusEngine</key>
    <dict>
        <key>enableRealTimeProtection</key>
        <true/>
        <key>passiveMode</key>
        <false/>
        <key>exclusions</key>
        <array>
            <dict>
                <key>$type</key>
                <string>excludedPath</string>
                <key>isDirectory</key>
                <false/>
                <key>path</key>
                <string>/var/log/system.log</string>
            </dict>
            <dict>
                <key>$type</key>
                <string>excludedPath</string>
                <key>isDirectory</key>
                <true/>
                <key>path</key>
                <string>/home</string>
            </dict>
            <dict>
                <key>$type</key>
                <string>excludedPath</string>
                <key>isDirectory</key>
                <true/>
                <key>path</key>
                <string>/Users/*/git</string>
            </dict>
            <dict>
                <key>$type</key>
                <string>excludedFileExtension</string>
                <key>extension</key>
                <string>pdf</string>
            </dict>
            <dict>
                <key>$type</key>
                <string>excludedFileName</string>
                <key>name</key>
                <string>cat</string>
            </dict>
        </array>
        <key>exclusionsMergePolicy</key>
        <string>merge</string>
        <key>allowedThreats</key>
        <array>
            <string>EICAR-Test-File (not a virus)</string>
        </array>
        <key>disallowedThreatActions</key>
        <array>
            <string>allow</string>
            <string>restore</string>
        </array>
        <key>threatTypeSettings</key>
        <array>
            <dict>
                <key>key</key>
                <string>potentially_unwanted_application</string>
                <key>value</key>
                <string>block</string>
            </dict>
            <dict>
                <key>key</key>
                <string>archive_bomb</string>
                <key>value</key>
                <string>audit</string>
            </dict>
        </array>
        <key>threatTypeSettingsMergePolicy</key>
        <string>merge</string>
    </dict>
    <key>cloudService</key>
    <dict>
        <key>enabled</key>
        <true/>
        <key>diagnosticLevel</key>
        <string>optional</string>
        <key>automaticSampleSubmission</key>
        <true/>
        <key>automaticDefinitionUpdateEnabled</key>
        <true/>
    </dict>
    <key>edr</key>
    <dict>
        <key>tags</key>
        <array>
            <dict>
                <key>key</key>
                <string>GROUP</string>
                <key>value</key>
                <string>ExampleTag</string>
            </dict>
        </array>
    </dict>
    <key>userInterface</key>
    <dict>
        <key>hideStatusMenuIcon</key>
        <false/>
        <key>userInitiatedFeedback</key>
        <string>enabled</string>
    </dict>
</dict>
</plist>
```

### <a name="intune-profile"></a><span data-ttu-id="8a10e-555">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="8a10e-555">Intune profile</span></span>

```XML
        <key>PayloadUUID</key>
        <string>C4E6A782-0C8D-44AB-A025-EB893987A295</string>
        <key>PayloadType</key>
        <string>Configuration</string>
        <key>PayloadOrganization</key>
        <string>Microsoft</string>
        <key>PayloadIdentifier</key>
        <string>C4E6A782-0C8D-44AB-A025-EB893987A295</string>
        <key>PayloadDisplayName</key>
        <string>Microsoft Defender for Endpoint settings</string>
        <key>PayloadDescription</key>
        <string>Microsoft Defender for Endpoint configuration settings</string>
        <key>PayloadVersion</key>
        <integer>1</integer>
        <key>PayloadEnabled</key>
        <true/>
        <key>PayloadRemovalDisallowed</key>
        <true/>
        <key>PayloadScope</key>
        <string>System</string>
        <key>PayloadContent</key>
        <array>
            <dict>
                <key>PayloadUUID</key>
                <string>99DBC2BC-3B3A-46A2-A413-C8F9BB9A7295</string>
                <key>PayloadType</key>
                <string>com.microsoft.wdav</string>
                <key>PayloadOrganization</key>
                <string>Microsoft</string>
                <key>PayloadIdentifier</key>
                <string>99DBC2BC-3B3A-46A2-A413-C8F9BB9A7295</string>
                <key>PayloadDisplayName</key>
                <string>Microsoft Defender for Endpoint configuration settings</string>
                <key>PayloadDescription</key>
                <string/>
                <key>PayloadVersion</key>
                <integer>1</integer>
                <key>PayloadEnabled</key>
                <true/>
                <key>antivirusEngine</key>
                <dict>
                    <key>enableRealTimeProtection</key>
                    <true/>
                    <key>passiveMode</key>
                    <false/>
                    <key>exclusions</key>
                    <array>
                        <dict>
                            <key>$type</key>
                            <string>excludedPath</string>
                            <key>isDirectory</key>
                            <false/>
                            <key>path</key>
                            <string>/var/log/system.log</string>
                        </dict>
                        <dict>
                            <key>$type</key>
                            <string>excludedPath</string>
                            <key>isDirectory</key>
                            <true/>
                            <key>path</key>
                            <string>/home</string>
                        </dict>
                        <dict>
                            <key>$type</key>
                            <string>excludedPath</string>
                            <key>isDirectory</key>
                            <true/>
                            <key>path</key>
                            <string>/Users/*/git</string>
                        </dict>
                        <dict>
                            <key>$type</key>
                            <string>excludedFileExtension</string>
                            <key>extension</key>
                            <string>pdf</string>
                        </dict>
                        <dict>
                            <key>$type</key>
                            <string>excludedFileName</string>
                            <key>name</key>
                            <string>cat</string>
                        </dict>
                    </array>
                    <key>exclusionsMergePolicy</key>
                    <string>merge</string>
                    <key>allowedThreats</key>
                    <array>
                        <string>EICAR-Test-File (not a virus)</string>
                    </array>
                    <key>disallowedThreatActions</key>
                    <array>
                        <string>allow</string>
                        <string>restore</string>
                    </array>
                    <key>threatTypeSettings</key>
                    <array>
                        <dict>
                            <key>key</key>
                            <string>potentially_unwanted_application</string>
                            <key>value</key>
                            <string>block</string>
                        </dict>
                        <dict>
                            <key>key</key>
                            <string>archive_bomb</string>
                            <key>value</key>
                            <string>audit</string>
                        </dict>
                    </array>
                    <key>threatTypeSettingsMergePolicy</key>
                    <string>merge</string>
                </dict>
                <key>cloudService</key>
                <dict>
                    <key>enabled</key>
                    <true/>
                    <key>diagnosticLevel</key>
                    <string>optional</string>
                    <key>automaticSampleSubmission</key>
                    <true/>
                    <key>automaticDefinitionUpdateEnabled</key>
                    <true/>
                </dict>
                <key>edr</key>
                <dict>
                    <key>tags</key>
                    <array>
                        <dict>
                            <key>key</key>
                            <string>GROUP</string>
                            <key>value</key>
                            <string>ExampleTag</string>
                        </dict>
                    </array>
                </dict>
                <key>userInterface</key>
                <dict>
                    <key>hideStatusMenuIcon</key>
                    <false/>
                    <key>userInitiatedFeedback</key>
                    <string>enabled</string>
                </dict>
            </dict>
        </array>
```

## <a name="property-list-validation"></a><span data-ttu-id="8a10e-556">Validation de liste de propriétés</span><span class="sxs-lookup"><span data-stu-id="8a10e-556">Property list validation</span></span>

<span data-ttu-id="8a10e-557">La liste des propriétés doit être un fichier *.plist* valide.</span><span class="sxs-lookup"><span data-stu-id="8a10e-557">The property list must be a valid *.plist* file.</span></span> <span data-ttu-id="8a10e-558">Pour ce faire, exécutez :</span><span class="sxs-lookup"><span data-stu-id="8a10e-558">This can be checked by executing:</span></span>

```bash
plutil -lint com.microsoft.wdav.plist
```
```Output
com.microsoft.wdav.plist: OK
```

<span data-ttu-id="8a10e-559">Si le fichier est bien formé, la commande ci-dessus produit `OK` et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="8a10e-559">If the file is well-formed, the above command outputs `OK` and returns an exit code of `0`.</span></span> <span data-ttu-id="8a10e-560">Sinon, une erreur qui décrit le problème s’affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="8a10e-560">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="8a10e-561">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="8a10e-561">Configuration profile deployment</span></span>

<span data-ttu-id="8a10e-562">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="8a10e-562">Once you've built the configuration profile for your enterprise, you can deploy it through the management console that your enterprise is using.</span></span> <span data-ttu-id="8a10e-563">Les sections suivantes fournissent des instructions sur la façon de déployer ce profil à l’aide de JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="8a10e-563">The following sections provide instructions on how to deploy this profile using JAMF and Intune.</span></span>

### <a name="jamf-deployment"></a><span data-ttu-id="8a10e-564">Déploiement JAMF</span><span class="sxs-lookup"><span data-stu-id="8a10e-564">JAMF deployment</span></span>

<span data-ttu-id="8a10e-565">À partir de la console JAMF, **ouvrez** profils de configuration ordinateurs, accédez au profil de configuration que vous souhaitez utiliser, puis sélectionnez Custom  >   **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="8a10e-565">From the JAMF console, open **Computers** > **Configuration Profiles**, navigate to the configuration profile you'd like to use, then select **Custom Settings**.</span></span> <span data-ttu-id="8a10e-566">Créez une entrée avec comme domaine de préférence `com.microsoft.wdav` et téléchargez *le .plist* produit précédemment.</span><span class="sxs-lookup"><span data-stu-id="8a10e-566">Create an entry with `com.microsoft.wdav` as the preference domain and upload the *.plist* produced earlier.</span></span>

>[!CAUTION]
><span data-ttu-id="8a10e-567">Vous devez entrer le domaine de préférence correct ( ) ; sinon, les préférences ne seront pas reconnues par `com.microsoft.wdav` Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="8a10e-567">You must enter the correct preference domain (`com.microsoft.wdav`); otherwise, the preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

### <a name="intune-deployment"></a><span data-ttu-id="8a10e-568">Déploiement d’Intune</span><span class="sxs-lookup"><span data-stu-id="8a10e-568">Intune deployment</span></span>

1. <span data-ttu-id="8a10e-569">Ouvrez **Gérer**  >  **la configuration de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="8a10e-569">Open **Manage** > **Device configuration**.</span></span> <span data-ttu-id="8a10e-570">Sélectionnez **Gérer**  >  **les profils**  >  **créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="8a10e-570">Select **Manage** > **Profiles** > **Create Profile**.</span></span>

2. <span data-ttu-id="8a10e-571">Choisissez un nom pour le profil.</span><span class="sxs-lookup"><span data-stu-id="8a10e-571">Choose a name for the profile.</span></span> <span data-ttu-id="8a10e-572">Change **Platform=macOS** to **Profile type=Custom**.</span><span class="sxs-lookup"><span data-stu-id="8a10e-572">Change **Platform=macOS** to **Profile type=Custom**.</span></span> <span data-ttu-id="8a10e-573">Sélectionnez Configurer.</span><span class="sxs-lookup"><span data-stu-id="8a10e-573">Select Configure.</span></span>

3. <span data-ttu-id="8a10e-574">Enregistrez le .plist produit précédemment sous `com.microsoft.wdav.xml` .</span><span class="sxs-lookup"><span data-stu-id="8a10e-574">Save the .plist produced earlier as `com.microsoft.wdav.xml`.</span></span>

4. <span data-ttu-id="8a10e-575">Entrez `com.microsoft.wdav` comme nom de profil de configuration **personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="8a10e-575">Enter `com.microsoft.wdav` as the **custom configuration profile name**.</span></span>

5. <span data-ttu-id="8a10e-576">Ouvrez le profil de configuration et téléchargez le `com.microsoft.wdav.xml` fichier.</span><span class="sxs-lookup"><span data-stu-id="8a10e-576">Open the configuration profile and upload the `com.microsoft.wdav.xml` file.</span></span> <span data-ttu-id="8a10e-577">(Ce fichier a été créé à l’étape 3.)</span><span class="sxs-lookup"><span data-stu-id="8a10e-577">(This file was created in step 3.)</span></span>

6. <span data-ttu-id="8a10e-578">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a10e-578">Select **OK**.</span></span>

7. <span data-ttu-id="8a10e-579">Sélectionnez   >  **Gérer les affectations.**</span><span class="sxs-lookup"><span data-stu-id="8a10e-579">Select **Manage** > **Assignments**.</span></span> <span data-ttu-id="8a10e-580">Dans **l’onglet** Inclure, sélectionnez Affecter à tous **les utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="8a10e-580">In the **Include** tab, select **Assign to All Users & All devices**.</span></span>

>[!CAUTION]
><span data-ttu-id="8a10e-581">Vous devez entrer le nom de profil de configuration personnalisé correct . Dans le cas contraire, ces préférences ne seront pas reconnues par Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="8a10e-581">You must enter the correct custom configuration profile name; otherwise, these preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

## <a name="resources"></a><span data-ttu-id="8a10e-582">Ressources</span><span class="sxs-lookup"><span data-stu-id="8a10e-582">Resources</span></span>

- [<span data-ttu-id="8a10e-583">Référence du profil de configuration (documentation Apple pour les développeurs)</span><span class="sxs-lookup"><span data-stu-id="8a10e-583">Configuration Profile Reference (Apple developer documentation)</span></span>](https://developer.apple.com/business/documentation/Configuration-Profile-Reference.pdf)
