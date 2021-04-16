---
title: Définir des préférences pour Microsoft Defender pour endpoint pour Mac
description: Configurez Microsoft Defender pour endpoint pour Mac dans les organisations d'entreprise.
keywords: microsoft, defender, atp, mac, management, preferences, enterprise, intune, jamf, macos,pé, mojave, high sierra
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
ms.openlocfilehash: d2bea469031e2c5932e859fbad7d442ebe4d34ed
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51860922"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-on-macos"></a><span data-ttu-id="f3583-104">Définir des préférences pour Microsoft Defender pour le point de terminaison sur macOS</span><span class="sxs-lookup"><span data-stu-id="f3583-104">Set preferences for Microsoft Defender for Endpoint on macOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f3583-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f3583-105">**Applies to:**</span></span>

- [<span data-ttu-id="f3583-106">Microsoft Defender pour point de terminaison macOS</span><span class="sxs-lookup"><span data-stu-id="f3583-106">Microsoft Defender for Endpoint on macOS</span></span>](microsoft-defender-endpoint-mac.md)

>[!IMPORTANT]
><span data-ttu-id="f3583-107">Cet article contient des instructions sur la façon de définir des préférences pour Microsoft Defender pour Endpoint sur macOS dans les organisations d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="f3583-107">This article contains instructions for how to set preferences for Microsoft Defender for Endpoint on macOS in enterprise organizations.</span></span> <span data-ttu-id="f3583-108">Pour configurer Microsoft Defender pour endpoint sur macOS à l'aide de l'interface de ligne de commande, voir [Resources](mac-resources.md#configuring-from-the-command-line).</span><span class="sxs-lookup"><span data-stu-id="f3583-108">To configure Microsoft Defender for Endpoint on macOS using the command-line interface, see [Resources](mac-resources.md#configuring-from-the-command-line).</span></span>

## <a name="summary"></a><span data-ttu-id="f3583-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="f3583-109">Summary</span></span>

<span data-ttu-id="f3583-110">Dans les organisations d'entreprise, Microsoft Defender pour endpoint sur macOS peut être géré via un profil de configuration déployé à l'aide de l'un des outils de gestion.</span><span class="sxs-lookup"><span data-stu-id="f3583-110">In enterprise organizations, Microsoft Defender for Endpoint on macOS can be managed through a configuration profile that is deployed by using one of several management tools.</span></span> <span data-ttu-id="f3583-111">Les préférences gérées par votre équipe en charge des opérations de sécurité prévalent sur les préférences définies localement sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="f3583-111">Preferences that are managed by your security operations team take precedence over preferences that are set locally on the device.</span></span> <span data-ttu-id="f3583-112">La modification des préférences définies par le biais du profil de configuration nécessite des privilèges escalades et n'est pas disponible pour les utilisateurs sans autorisations administratives.</span><span class="sxs-lookup"><span data-stu-id="f3583-112">Changing the preferences that are set through the configuration profile requires escalated privileges and is not available for users without administrative permissions.</span></span>

<span data-ttu-id="f3583-113">Cet article décrit la structure du profil de configuration, inclut un profil recommandé que vous pouvez utiliser pour commencer et fournit des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="f3583-113">This article describes the structure of the configuration profile, includes a recommended profile that you can use to get started, and provides instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="f3583-114">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="f3583-114">Configuration profile structure</span></span>

<span data-ttu-id="f3583-115">Le profil de configuration est un fichier *.plist* qui se compose d'entrées identifiées par une clé (qui indique le nom de la préférence), suivi d'une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="f3583-115">The configuration profile is a *.plist* file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="f3583-116">Les valeurs peuvent être simples (par exemple, une valeur numérique) ou complexes, telles qu'une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="f3583-116">Values can either be simple (such as a numerical value) or complex, such as a nested list of preferences.</span></span>

>[!CAUTION]
><span data-ttu-id="f3583-117">La disposition du profil de configuration dépend de la console de gestion que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="f3583-117">The layout of the configuration profile depends on the management console that you are using.</span></span> <span data-ttu-id="f3583-118">Les sections suivantes contiennent des exemples de profils de configuration pour JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="f3583-118">The following sections contain examples of configuration profiles for JAMF and Intune.</span></span>

<span data-ttu-id="f3583-119">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l'échelle du produit pour les sous-catégories de Microsoft Defender pour le point de terminaison, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3583-119">The top level of the configuration profile includes product-wide preferences and entries for subareas of Microsoft Defender for Endpoint, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="f3583-120">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="f3583-120">Antivirus engine preferences</span></span>

<span data-ttu-id="f3583-121">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="f3583-121">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of Microsoft Defender for Endpoint.</span></span>

|<span data-ttu-id="f3583-122">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-122">Section</span></span>|<span data-ttu-id="f3583-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-123">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-124">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-124">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-125">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-125">**Key**</span></span> | <span data-ttu-id="f3583-126">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="f3583-126">antivirusEngine</span></span> |
| <span data-ttu-id="f3583-127">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-127">**Data type**</span></span> | <span data-ttu-id="f3583-128">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-128">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-129">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-129">**Comments**</span></span> | <span data-ttu-id="f3583-130">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-130">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="f3583-131">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="f3583-131">Enable / disable real-time protection</span></span>

<span data-ttu-id="f3583-132">Spécifiez s'il faut activer la protection en temps réel, qui analyse les fichiers à mesure qu'ils sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="f3583-132">Specify whether to enable real-time protection, which scans files as they are accessed.</span></span>

|<span data-ttu-id="f3583-133">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-133">Section</span></span>|<span data-ttu-id="f3583-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-134">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-135">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-135">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-136">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-136">**Key**</span></span> | <span data-ttu-id="f3583-137">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="f3583-137">enableRealTimeProtection</span></span> |
| <span data-ttu-id="f3583-138">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-138">**Data type**</span></span> | <span data-ttu-id="f3583-139">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-139">Boolean</span></span> |
| <span data-ttu-id="f3583-140">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-140">**Possible values**</span></span> | <span data-ttu-id="f3583-141">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-141">true (default)</span></span> <br/> <span data-ttu-id="f3583-142">false</span><span class="sxs-lookup"><span data-stu-id="f3583-142">false</span></span> |

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="f3583-143">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="f3583-143">Enable / disable passive mode</span></span>

<span data-ttu-id="f3583-144">Spécifiez si le moteur antivirus s'exécute en mode passif.</span><span class="sxs-lookup"><span data-stu-id="f3583-144">Specify whether the antivirus engine runs in passive mode.</span></span> <span data-ttu-id="f3583-145">Le mode passif a les implications suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3583-145">Passive mode has the following implications:</span></span> 
- <span data-ttu-id="f3583-146">La protection en temps réel est désactivée</span><span class="sxs-lookup"><span data-stu-id="f3583-146">Real-time protection is turned off</span></span>
- <span data-ttu-id="f3583-147">L'analyse à la demande est désactivée</span><span class="sxs-lookup"><span data-stu-id="f3583-147">On-demand scanning is turned on</span></span>
- <span data-ttu-id="f3583-148">La correction automatique des menaces est désactivée</span><span class="sxs-lookup"><span data-stu-id="f3583-148">Automatic threat remediation is turned off</span></span>
- <span data-ttu-id="f3583-149">Les mises à jour de l'intelligence de la sécurité sont allumées</span><span class="sxs-lookup"><span data-stu-id="f3583-149">Security intelligence updates are turned on</span></span>
- <span data-ttu-id="f3583-150">L'icône du menu État est masquée</span><span class="sxs-lookup"><span data-stu-id="f3583-150">Status menu icon is hidden</span></span>

|<span data-ttu-id="f3583-151">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-151">Section</span></span>|<span data-ttu-id="f3583-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-152">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-153">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-153">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-154">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-154">**Key**</span></span> | <span data-ttu-id="f3583-155">passiveMode</span><span class="sxs-lookup"><span data-stu-id="f3583-155">passiveMode</span></span> |
| <span data-ttu-id="f3583-156">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-156">**Data type**</span></span> | <span data-ttu-id="f3583-157">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-157">Boolean</span></span> |
| <span data-ttu-id="f3583-158">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-158">**Possible values**</span></span> | <span data-ttu-id="f3583-159">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-159">false (default)</span></span> <br/> <span data-ttu-id="f3583-160">true</span><span class="sxs-lookup"><span data-stu-id="f3583-160">true</span></span> |
| <span data-ttu-id="f3583-161">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-161">**Comments**</span></span> | <span data-ttu-id="f3583-162">Disponible dans Microsoft Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-162">Available in Microsoft Defender for Endpoint version 100.67.60 or higher.</span></span> |

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="f3583-163">Stratégie de fusion d'exclusions</span><span class="sxs-lookup"><span data-stu-id="f3583-163">Exclusion merge policy</span></span>

<span data-ttu-id="f3583-164">Spécifiez la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="f3583-164">Specify the merge policy for exclusions.</span></span> <span data-ttu-id="f3583-165">Il peut s'agit d'une combinaison d'exclusions définies par l'administrateur et d'exclusions définies par l'utilisateur ( ) ou uniquement `merge` d'exclusions définies par l'administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="f3583-165">This can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="f3583-166">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="f3583-166">This setting can be used to restrict local users from defining their own exclusions.</span></span>

|<span data-ttu-id="f3583-167">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-167">Section</span></span>|<span data-ttu-id="f3583-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-168">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-169">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-169">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-170">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-170">**Key**</span></span> | <span data-ttu-id="f3583-171">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="f3583-171">exclusionsMergePolicy</span></span> |
| <span data-ttu-id="f3583-172">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-172">**Data type**</span></span> | <span data-ttu-id="f3583-173">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-173">String</span></span> |
| <span data-ttu-id="f3583-174">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-174">**Possible values**</span></span> | <span data-ttu-id="f3583-175">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-175">merge (default)</span></span> <br/> <span data-ttu-id="f3583-176">admin_only</span><span class="sxs-lookup"><span data-stu-id="f3583-176">admin_only</span></span> |
| <span data-ttu-id="f3583-177">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-177">**Comments**</span></span> | <span data-ttu-id="f3583-178">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-178">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="scan-exclusions"></a><span data-ttu-id="f3583-179">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="f3583-179">Scan exclusions</span></span>

<span data-ttu-id="f3583-180">Spécifiez les entités exclues de l'analyse.</span><span class="sxs-lookup"><span data-stu-id="f3583-180">Specify entities excluded from being scanned.</span></span> <span data-ttu-id="f3583-181">Les exclusions peuvent être spécifiées par des chemins d'accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f3583-181">Exclusions can be specified by full paths, extensions, or file names.</span></span>

|<span data-ttu-id="f3583-182">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-182">Section</span></span>|<span data-ttu-id="f3583-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-183">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-184">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-184">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-185">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-185">**Key**</span></span> | <span data-ttu-id="f3583-186">exclusions</span><span class="sxs-lookup"><span data-stu-id="f3583-186">exclusions</span></span> |
| <span data-ttu-id="f3583-187">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-187">**Data type**</span></span> | <span data-ttu-id="f3583-188">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-188">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-189">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-189">**Comments**</span></span> | <span data-ttu-id="f3583-190">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-190">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-exclusion"></a><span data-ttu-id="f3583-191">Type d'exclusion</span><span class="sxs-lookup"><span data-stu-id="f3583-191">Type of exclusion</span></span>

<span data-ttu-id="f3583-192">Spécifiez le contenu exclu de l'analyse par type.</span><span class="sxs-lookup"><span data-stu-id="f3583-192">Specify content excluded from being scanned by type.</span></span>

|<span data-ttu-id="f3583-193">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-193">Section</span></span>|<span data-ttu-id="f3583-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-194">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-195">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-195">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-196">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-196">**Key**</span></span> | <span data-ttu-id="f3583-197">$type</span><span class="sxs-lookup"><span data-stu-id="f3583-197">$type</span></span> |
| <span data-ttu-id="f3583-198">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-198">**Data type**</span></span> | <span data-ttu-id="f3583-199">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-199">String</span></span> |
| <span data-ttu-id="f3583-200">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-200">**Possible values**</span></span> | <span data-ttu-id="f3583-201">excludedPath</span><span class="sxs-lookup"><span data-stu-id="f3583-201">excludedPath</span></span> <br/> <span data-ttu-id="f3583-202">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="f3583-202">excludedFileExtension</span></span> <br/> <span data-ttu-id="f3583-203">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="f3583-203">excludedFileName</span></span> |

##### <a name="path-to-excluded-content"></a><span data-ttu-id="f3583-204">Chemin d'accès au contenu exclu</span><span class="sxs-lookup"><span data-stu-id="f3583-204">Path to excluded content</span></span>

<span data-ttu-id="f3583-205">Spécifiez le contenu exclu de l'analyse par le chemin d'accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="f3583-205">Specify content excluded from being scanned by full file path.</span></span>

|<span data-ttu-id="f3583-206">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-206">Section</span></span>|<span data-ttu-id="f3583-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-207">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-208">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-208">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-209">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-209">**Key**</span></span> | <span data-ttu-id="f3583-210">chemin</span><span class="sxs-lookup"><span data-stu-id="f3583-210">path</span></span> |
| <span data-ttu-id="f3583-211">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-211">**Data type**</span></span> | <span data-ttu-id="f3583-212">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-212">String</span></span> |
| <span data-ttu-id="f3583-213">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-213">**Possible values**</span></span> | <span data-ttu-id="f3583-214">chemins d'accès valides</span><span class="sxs-lookup"><span data-stu-id="f3583-214">valid paths</span></span> |
| <span data-ttu-id="f3583-215">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-215">**Comments**</span></span> | <span data-ttu-id="f3583-216">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="f3583-216">Applicable only if *$type* is *excludedPath*</span></span> |

##### <a name="path-type-file--directory"></a><span data-ttu-id="f3583-217">Type de chemin d'accès (fichier/répertoire)</span><span class="sxs-lookup"><span data-stu-id="f3583-217">Path type (file / directory)</span></span>

<span data-ttu-id="f3583-218">Indiquez si la *propriété du* chemin d'accès fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="f3583-218">Indicate if the *path* property refers to a file or directory.</span></span> 

|<span data-ttu-id="f3583-219">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-219">Section</span></span>|<span data-ttu-id="f3583-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-220">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-221">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-221">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-222">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-222">**Key**</span></span> | <span data-ttu-id="f3583-223">isDirectory</span><span class="sxs-lookup"><span data-stu-id="f3583-223">isDirectory</span></span> |
| <span data-ttu-id="f3583-224">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-224">**Data type**</span></span> | <span data-ttu-id="f3583-225">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-225">Boolean</span></span> |
| <span data-ttu-id="f3583-226">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-226">**Possible values**</span></span> | <span data-ttu-id="f3583-227">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-227">false (default)</span></span> <br/> <span data-ttu-id="f3583-228">true</span><span class="sxs-lookup"><span data-stu-id="f3583-228">true</span></span> |
| <span data-ttu-id="f3583-229">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-229">**Comments**</span></span> | <span data-ttu-id="f3583-230">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="f3583-230">Applicable only if *$type* is *excludedPath*</span></span> |

##### <a name="file-extension-excluded-from-the-scan"></a><span data-ttu-id="f3583-231">Extension de fichier exclue de l'analyse</span><span class="sxs-lookup"><span data-stu-id="f3583-231">File extension excluded from the scan</span></span>

<span data-ttu-id="f3583-232">Spécifiez le contenu exclu de l'analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="f3583-232">Specify content excluded from being scanned by file extension.</span></span>

|<span data-ttu-id="f3583-233">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-233">Section</span></span>|<span data-ttu-id="f3583-234">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-234">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-235">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-235">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-236">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-236">**Key**</span></span> | <span data-ttu-id="f3583-237">extension</span><span class="sxs-lookup"><span data-stu-id="f3583-237">extension</span></span> |
| <span data-ttu-id="f3583-238">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-238">**Data type**</span></span> | <span data-ttu-id="f3583-239">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-239">String</span></span> |
| <span data-ttu-id="f3583-240">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-240">**Possible values**</span></span> | <span data-ttu-id="f3583-241">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="f3583-241">valid file extensions</span></span> |
| <span data-ttu-id="f3583-242">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-242">**Comments**</span></span> | <span data-ttu-id="f3583-243">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="f3583-243">Applicable only if *$type* is *excludedFileExtension*</span></span> |

##### <a name="process-excluded-from-the-scan"></a><span data-ttu-id="f3583-244">Processus exclu de l'analyse</span><span class="sxs-lookup"><span data-stu-id="f3583-244">Process excluded from the scan</span></span>

<span data-ttu-id="f3583-245">Spécifiez un processus pour lequel toute l'activité de fichier est exclue de l'analyse.</span><span class="sxs-lookup"><span data-stu-id="f3583-245">Specify a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="f3583-246">Le processus peut être spécifié par son nom (par exemple) ou son chemin d'accès complet `cat` (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="f3583-246">The process can be specified either by its name (e.g. `cat`) or full path (e.g. `/bin/cat`).</span></span>

|<span data-ttu-id="f3583-247">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-247">Section</span></span>|<span data-ttu-id="f3583-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-248">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-249">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-249">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-250">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-250">**Key**</span></span> | <span data-ttu-id="f3583-251">nom</span><span class="sxs-lookup"><span data-stu-id="f3583-251">name</span></span> |
| <span data-ttu-id="f3583-252">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-252">**Data type**</span></span> | <span data-ttu-id="f3583-253">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-253">String</span></span> |
| <span data-ttu-id="f3583-254">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-254">**Possible values**</span></span> | <span data-ttu-id="f3583-255">n'importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-255">any string</span></span> |
| <span data-ttu-id="f3583-256">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-256">**Comments**</span></span> | <span data-ttu-id="f3583-257">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="f3583-257">Applicable only if *$type* is *excludedFileName*</span></span> |

#### <a name="allowed-threats"></a><span data-ttu-id="f3583-258">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="f3583-258">Allowed threats</span></span>

<span data-ttu-id="f3583-259">Spécifiez les menaces par nom qui ne sont pas bloquées par Defender pour endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="f3583-259">Specify threats by name that are not blocked by Defender for Endpoint for Mac.</span></span> <span data-ttu-id="f3583-260">Ces menaces seront autorisées à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="f3583-260">These threats will be allowed to run.</span></span>

|<span data-ttu-id="f3583-261">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-261">Section</span></span>|<span data-ttu-id="f3583-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-262">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-263">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-263">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-264">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-264">**Key**</span></span> | <span data-ttu-id="f3583-265">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="f3583-265">allowedThreats</span></span> |
| <span data-ttu-id="f3583-266">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-266">**Data type**</span></span> | <span data-ttu-id="f3583-267">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="f3583-267">Array of strings</span></span> |

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="f3583-268">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="f3583-268">Disallowed threat actions</span></span>

<span data-ttu-id="f3583-269">Limite les actions que l'utilisateur local d'un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="f3583-269">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="f3583-270">Les actions incluses dans cette liste ne sont pas affichées dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3583-270">The actions included in this list are not displayed in the user interface.</span></span>

|<span data-ttu-id="f3583-271">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-271">Section</span></span>|<span data-ttu-id="f3583-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-272">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-273">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-273">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-274">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-274">**Key**</span></span> | <span data-ttu-id="f3583-275">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="f3583-275">disallowedThreatActions</span></span> |
| <span data-ttu-id="f3583-276">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-276">**Data type**</span></span> | <span data-ttu-id="f3583-277">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="f3583-277">Array of strings</span></span> |
| <span data-ttu-id="f3583-278">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-278">**Possible values**</span></span> | <span data-ttu-id="f3583-279">autoriser (empêche les utilisateurs d'autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="f3583-279">allow (restricts users from allowing threats)</span></span> <br/> <span data-ttu-id="f3583-280">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="f3583-280">restore (restricts users from restoring threats from the quarantine)</span></span> |
| <span data-ttu-id="f3583-281">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-281">**Comments**</span></span> | <span data-ttu-id="f3583-282">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-282">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="threat-type-settings"></a><span data-ttu-id="f3583-283">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="f3583-283">Threat type settings</span></span>

<span data-ttu-id="f3583-284">Spécifiez comment certains types de menaces sont gérés par Microsoft Defender pour point de terminaison sur macOS.</span><span class="sxs-lookup"><span data-stu-id="f3583-284">Specify how certain threat types are handled by Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="f3583-285">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-285">Section</span></span>|<span data-ttu-id="f3583-286">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-286">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-287">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-287">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-288">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-288">**Key**</span></span> | <span data-ttu-id="f3583-289">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="f3583-289">threatTypeSettings</span></span> |
| <span data-ttu-id="f3583-290">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-290">**Data type**</span></span> | <span data-ttu-id="f3583-291">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-291">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-292">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-292">**Comments**</span></span> | <span data-ttu-id="f3583-293">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-293">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="threat-type"></a><span data-ttu-id="f3583-294">Type de menace</span><span class="sxs-lookup"><span data-stu-id="f3583-294">Threat type</span></span>

<span data-ttu-id="f3583-295">Spécifiez les types de menaces.</span><span class="sxs-lookup"><span data-stu-id="f3583-295">Specify threat types.</span></span>

|<span data-ttu-id="f3583-296">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-296">Section</span></span>|<span data-ttu-id="f3583-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-297">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-298">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-298">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-299">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-299">**Key**</span></span> | <span data-ttu-id="f3583-300">clé</span><span class="sxs-lookup"><span data-stu-id="f3583-300">key</span></span> |
| <span data-ttu-id="f3583-301">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-301">**Data type**</span></span> | <span data-ttu-id="f3583-302">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-302">String</span></span> |
| <span data-ttu-id="f3583-303">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-303">**Possible values**</span></span> | <span data-ttu-id="f3583-304">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="f3583-304">potentially_unwanted_application</span></span> <br/> <span data-ttu-id="f3583-305">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="f3583-305">archive_bomb</span></span> |

##### <a name="action-to-take"></a><span data-ttu-id="f3583-306">Mesures à prendre</span><span class="sxs-lookup"><span data-stu-id="f3583-306">Action to take</span></span>

<span data-ttu-id="f3583-307">Spécifiez l'action à prendre lorsqu'une menace du type spécifié dans la section précédente est détectée.</span><span class="sxs-lookup"><span data-stu-id="f3583-307">Specify what action to take when a threat of the type specified in the preceding section is detected.</span></span> <span data-ttu-id="f3583-308">Choisissez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3583-308">Choose from the following options:</span></span>

- <span data-ttu-id="f3583-309">**Audit**: votre appareil n'est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="f3583-309">**Audit**: your device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="f3583-310">**Bloquer**: votre appareil est protégé contre ce type de menace et vous êtes averti dans l'interface utilisateur et la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f3583-310">**Block**: your device is protected against this type of threat and you are notified in the user interface and the security console.</span></span>
- <span data-ttu-id="f3583-311">**Off**: votre appareil n'est pas protégé contre ce type de menace et rien n'est enregistré.</span><span class="sxs-lookup"><span data-stu-id="f3583-311">**Off**: your device is not protected against this type of threat and nothing is logged.</span></span>

|<span data-ttu-id="f3583-312">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-312">Section</span></span>|<span data-ttu-id="f3583-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-313">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-314">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-314">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-315">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-315">**Key**</span></span> | <span data-ttu-id="f3583-316">valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-316">value</span></span> |
| <span data-ttu-id="f3583-317">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-317">**Data type**</span></span> | <span data-ttu-id="f3583-318">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-318">String</span></span> |
| <span data-ttu-id="f3583-319">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-319">**Possible values**</span></span> | <span data-ttu-id="f3583-320">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-320">audit (default)</span></span> <br/> <span data-ttu-id="f3583-321">block</span><span class="sxs-lookup"><span data-stu-id="f3583-321">block</span></span> <br/> <span data-ttu-id="f3583-322">off</span><span class="sxs-lookup"><span data-stu-id="f3583-322">off</span></span> |

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="f3583-323">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="f3583-323">Threat type settings merge policy</span></span>

<span data-ttu-id="f3583-324">Spécifiez la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="f3583-324">Specify the merge policy for threat type settings.</span></span> <span data-ttu-id="f3583-325">Il peut s'agit d'une combinaison de paramètres définis par l'administrateur et de paramètres définis par l'utilisateur ( ) ou uniquement de `merge` paramètres définis par l'administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="f3583-325">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="f3583-326">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="f3583-326">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

|<span data-ttu-id="f3583-327">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-327">Section</span></span>|<span data-ttu-id="f3583-328">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-328">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-329">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-329">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-330">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-330">**Key**</span></span> | <span data-ttu-id="f3583-331">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="f3583-331">threatTypeSettingsMergePolicy</span></span> |
| <span data-ttu-id="f3583-332">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-332">**Data type**</span></span> | <span data-ttu-id="f3583-333">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-333">String</span></span> |
| <span data-ttu-id="f3583-334">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-334">**Possible values**</span></span> | <span data-ttu-id="f3583-335">merge (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-335">merge (default)</span></span> <br/> <span data-ttu-id="f3583-336">admin_only</span><span class="sxs-lookup"><span data-stu-id="f3583-336">admin_only</span></span> |
| <span data-ttu-id="f3583-337">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-337">**Comments**</span></span> | <span data-ttu-id="f3583-338">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-338">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="f3583-339">Conservation de l'historique d'analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="f3583-339">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="f3583-340">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l'historique d'analyse sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="f3583-340">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="f3583-341">Les anciens résultats d'analyse sont supprimés de l'historique.</span><span class="sxs-lookup"><span data-stu-id="f3583-341">Old scan results are removed from the history.</span></span> <span data-ttu-id="f3583-342">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="f3583-342">Old quarantined files that are also removed from the disk.</span></span>

|<span data-ttu-id="f3583-343">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-343">Section</span></span>|<span data-ttu-id="f3583-344">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-344">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-345">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-345">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-346">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-346">**Key**</span></span> | <span data-ttu-id="f3583-347">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="f3583-347">scanResultsRetentionDays</span></span> |
| <span data-ttu-id="f3583-348">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-348">**Data type**</span></span> | <span data-ttu-id="f3583-349">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-349">String</span></span> |
| <span data-ttu-id="f3583-350">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-350">**Possible values**</span></span> | <span data-ttu-id="f3583-351">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f3583-351">90 (default).</span></span> <span data-ttu-id="f3583-352">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="f3583-352">Allowed values are from 1 day to 180 days.</span></span> |
| <span data-ttu-id="f3583-353">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-353">**Comments**</span></span> | <span data-ttu-id="f3583-354">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-354">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="f3583-355">Nombre maximal d'éléments dans l'historique d'analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="f3583-355">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="f3583-356">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="f3583-356">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="f3583-357">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="f3583-357">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

|<span data-ttu-id="f3583-358">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-358">Section</span></span>|<span data-ttu-id="f3583-359">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-359">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-360">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-360">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-361">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-361">**Key**</span></span> | <span data-ttu-id="f3583-362">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="f3583-362">scanHistoryMaximumItems</span></span> |
| <span data-ttu-id="f3583-363">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-363">**Data type**</span></span> | <span data-ttu-id="f3583-364">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-364">String</span></span> |
| <span data-ttu-id="f3583-365">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-365">**Possible values**</span></span> | <span data-ttu-id="f3583-366">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f3583-366">10000 (default).</span></span> <span data-ttu-id="f3583-367">Les valeurs autorisées sont de 5 000 à 1 5 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="f3583-367">Allowed values are from 5000 items to 15000 items.</span></span> |
| <span data-ttu-id="f3583-368">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-368">**Comments**</span></span> | <span data-ttu-id="f3583-369">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-369">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="f3583-370">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="f3583-370">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="f3583-371">Configurez les fonctionnalités de protection informatique de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="f3583-371">Configure the cloud-driven protection features of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="f3583-372">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-372">Section</span></span>|<span data-ttu-id="f3583-373">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-373">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-374">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-374">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-375">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-375">**Key**</span></span> | <span data-ttu-id="f3583-376">cloudService</span><span class="sxs-lookup"><span data-stu-id="f3583-376">cloudService</span></span> |
| <span data-ttu-id="f3583-377">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-377">**Data type**</span></span> | <span data-ttu-id="f3583-378">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-378">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-379">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-379">**Comments**</span></span> | <span data-ttu-id="f3583-380">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-380">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="f3583-381">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="f3583-381">Enable / disable cloud-delivered protection</span></span>

<span data-ttu-id="f3583-382">Spécifiez s’il faut activer ou non la protection de l’appareil livrée par le cloud.</span><span class="sxs-lookup"><span data-stu-id="f3583-382">Specify whether to enable cloud-delivered protection the device or not.</span></span> <span data-ttu-id="f3583-383">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="f3583-383">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

|<span data-ttu-id="f3583-384">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-384">Section</span></span>|<span data-ttu-id="f3583-385">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-385">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-386">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-386">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-387">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-387">**Key**</span></span> | <span data-ttu-id="f3583-388">activé</span><span class="sxs-lookup"><span data-stu-id="f3583-388">enabled</span></span> |
| <span data-ttu-id="f3583-389">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-389">**Data type**</span></span> | <span data-ttu-id="f3583-390">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-390">Boolean</span></span> |
| <span data-ttu-id="f3583-391">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-391">**Possible values**</span></span> | <span data-ttu-id="f3583-392">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-392">true (default)</span></span> <br/> <span data-ttu-id="f3583-393">false</span><span class="sxs-lookup"><span data-stu-id="f3583-393">false</span></span> |

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="f3583-394">Niveau de collection de diagnostics</span><span class="sxs-lookup"><span data-stu-id="f3583-394">Diagnostic collection level</span></span>

<span data-ttu-id="f3583-395">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Microsoft Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="f3583-395">Diagnostic data is used to keep Microsoft Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="f3583-396">Ce paramètre détermine le niveau de diagnostics envoyés par Microsoft Defender pour endpoint à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3583-396">This setting determines the level of diagnostics sent by Microsoft Defender for Endpoint to Microsoft.</span></span>

|<span data-ttu-id="f3583-397">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-397">Section</span></span>|<span data-ttu-id="f3583-398">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-398">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-399">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-399">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-400">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-400">**Key**</span></span> | <span data-ttu-id="f3583-401">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="f3583-401">diagnosticLevel</span></span> |
| <span data-ttu-id="f3583-402">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-402">**Data type**</span></span> | <span data-ttu-id="f3583-403">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-403">String</span></span> |
| <span data-ttu-id="f3583-404">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-404">**Possible values**</span></span> | <span data-ttu-id="f3583-405">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-405">optional (default)</span></span> <br/> <span data-ttu-id="f3583-406">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f3583-406">required</span></span> |

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="f3583-407">Activer/désactiver les envois automatiques d'échantillons</span><span class="sxs-lookup"><span data-stu-id="f3583-407">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="f3583-408">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3583-408">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="f3583-409">Vous êtes invité à savoir si le fichier envoyé est susceptible de contenir des informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="f3583-409">You are prompted if the submitted file is likely to contain personal information.</span></span>

|<span data-ttu-id="f3583-410">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-410">Section</span></span>|<span data-ttu-id="f3583-411">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-411">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-412">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-412">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-413">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-413">**Key**</span></span> | <span data-ttu-id="f3583-414">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="f3583-414">automaticSampleSubmission</span></span> |
| <span data-ttu-id="f3583-415">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-415">**Data type**</span></span> | <span data-ttu-id="f3583-416">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-416">Boolean</span></span> |
| <span data-ttu-id="f3583-417">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-417">**Possible values**</span></span> | <span data-ttu-id="f3583-418">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-418">true (default)</span></span> <br/> <span data-ttu-id="f3583-419">false</span><span class="sxs-lookup"><span data-stu-id="f3583-419">false</span></span> |

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="f3583-420">Activer/désactiver les mises à jour automatiques de l'intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="f3583-420">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="f3583-421">Détermine si les mises à jour d'informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="f3583-421">Determines whether security intelligence updates are installed automatically:</span></span>

|<span data-ttu-id="f3583-422">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-422">Section</span></span>|<span data-ttu-id="f3583-423">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-423">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-424">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-424">**Key**</span></span> | <span data-ttu-id="f3583-425">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="f3583-425">automaticDefinitionUpdateEnabled</span></span> |
| <span data-ttu-id="f3583-426">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-426">**Data type**</span></span> | <span data-ttu-id="f3583-427">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-427">Boolean</span></span> |
| <span data-ttu-id="f3583-428">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-428">**Possible values**</span></span> | <span data-ttu-id="f3583-429">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-429">true (default)</span></span> <br/> <span data-ttu-id="f3583-430">false</span><span class="sxs-lookup"><span data-stu-id="f3583-430">false</span></span> |

### <a name="user-interface-preferences"></a><span data-ttu-id="f3583-431">Préférences de l'interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="f3583-431">User interface preferences</span></span>

<span data-ttu-id="f3583-432">Gérez les préférences pour l'interface utilisateur de Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="f3583-432">Manage the preferences for the user interface of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="f3583-433">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-433">Section</span></span>|<span data-ttu-id="f3583-434">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-434">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-435">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-435">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-436">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-436">**Key**</span></span> | <span data-ttu-id="f3583-437">userInterface</span><span class="sxs-lookup"><span data-stu-id="f3583-437">userInterface</span></span> |
| <span data-ttu-id="f3583-438">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-438">**Data type**</span></span> | <span data-ttu-id="f3583-439">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-439">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-440">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-440">**Comments**</span></span> | <span data-ttu-id="f3583-441">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-441">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="show--hide-status-menu-icon"></a><span data-ttu-id="f3583-442">Afficher/masquer l'icône du menu État</span><span class="sxs-lookup"><span data-stu-id="f3583-442">Show / hide status menu icon</span></span>

<span data-ttu-id="f3583-443">Spécifiez s'il faut afficher ou masquer l'icône du menu d'état dans le coin supérieur droit de l'écran.</span><span class="sxs-lookup"><span data-stu-id="f3583-443">Specify whether to show or hide the status menu icon in the top-right corner of the screen.</span></span>

|<span data-ttu-id="f3583-444">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-444">Section</span></span>|<span data-ttu-id="f3583-445">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-445">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-446">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-446">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-447">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-447">**Key**</span></span> | <span data-ttu-id="f3583-448">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="f3583-448">hideStatusMenuIcon</span></span> |
| <span data-ttu-id="f3583-449">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-449">**Data type**</span></span> | <span data-ttu-id="f3583-450">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="f3583-450">Boolean</span></span> |
| <span data-ttu-id="f3583-451">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-451">**Possible values**</span></span> | <span data-ttu-id="f3583-452">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-452">false (default)</span></span> <br/> <span data-ttu-id="f3583-453">true</span><span class="sxs-lookup"><span data-stu-id="f3583-453">true</span></span> |

#### <a name="show--hide-option-to-send-feedback"></a><span data-ttu-id="f3583-454">Afficher /masquer l'option d'envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="f3583-454">Show / hide option to send feedback</span></span>

<span data-ttu-id="f3583-455">Spécifiez si les utilisateurs peuvent envoyer des commentaires à Microsoft en allant à `Help`  >  `Send Feedback` .</span><span class="sxs-lookup"><span data-stu-id="f3583-455">Specify whether users can submit feedback to Microsoft by going to `Help` > `Send Feedback`.</span></span>

|<span data-ttu-id="f3583-456">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-456">Section</span></span>|<span data-ttu-id="f3583-457">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-457">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-458">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-458">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-459">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-459">**Key**</span></span> | <span data-ttu-id="f3583-460">userInitiatedFeedback</span><span class="sxs-lookup"><span data-stu-id="f3583-460">userInitiatedFeedback</span></span> |
| <span data-ttu-id="f3583-461">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-461">**Data type**</span></span> | <span data-ttu-id="f3583-462">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-462">String</span></span> |
| <span data-ttu-id="f3583-463">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-463">**Possible values**</span></span> | <span data-ttu-id="f3583-464">activé (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f3583-464">enabled (default)</span></span> <br/> <span data-ttu-id="f3583-465">désactivé</span><span class="sxs-lookup"><span data-stu-id="f3583-465">disabled</span></span> |
| <span data-ttu-id="f3583-466">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-466">**Comments**</span></span> | <span data-ttu-id="f3583-467">Disponible dans Microsoft Defender pour Endpoint version 101.19.61 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="f3583-467">Available in Microsoft Defender for Endpoint version 101.19.61 or higher.</span></span> |

### <a name="endpoint-detection-and-response-preferences"></a><span data-ttu-id="f3583-468">Préférences de détection et de réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="f3583-468">Endpoint detection and response preferences</span></span>

<span data-ttu-id="f3583-469">Gérez les préférences du composant EDR (Endpoint Detection and Response) de Microsoft Defender for Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="f3583-469">Manage the preferences of the endpoint detection and response (EDR) component of Microsoft Defender for Endpoint on macOS.</span></span>

|<span data-ttu-id="f3583-470">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-470">Section</span></span>|<span data-ttu-id="f3583-471">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-471">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-472">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-472">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-473">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-473">**Key**</span></span> | <span data-ttu-id="f3583-474">edr</span><span class="sxs-lookup"><span data-stu-id="f3583-474">edr</span></span> |
| <span data-ttu-id="f3583-475">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-475">**Data type**</span></span> | <span data-ttu-id="f3583-476">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-476">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-477">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-477">**Comments**</span></span> | <span data-ttu-id="f3583-478">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-478">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="device-tags"></a><span data-ttu-id="f3583-479">Balises d’appareil</span><span class="sxs-lookup"><span data-stu-id="f3583-479">Device tags</span></span>

<span data-ttu-id="f3583-480">Spécifiez un nom de balise et sa valeur.</span><span class="sxs-lookup"><span data-stu-id="f3583-480">Specify a tag name and its value.</span></span> 

- <span data-ttu-id="f3583-481">La balise GROUP balise l’appareil avec la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f3583-481">The GROUP tag, tags the device with the specified value.</span></span> <span data-ttu-id="f3583-482">La balise est reflétée dans le portail sous la page de l’appareil et peut être utilisée pour le filtrage et le regroupement des appareils.</span><span class="sxs-lookup"><span data-stu-id="f3583-482">The tag is reflected in the portal under the device page and can be used for filtering and grouping devices.</span></span>

|<span data-ttu-id="f3583-483">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-483">Section</span></span>|<span data-ttu-id="f3583-484">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-484">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-485">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-485">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-486">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-486">**Key**</span></span> | <span data-ttu-id="f3583-487">étiquettes</span><span class="sxs-lookup"><span data-stu-id="f3583-487">tags</span></span> |
| <span data-ttu-id="f3583-488">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-488">**Data type**</span></span> | <span data-ttu-id="f3583-489">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="f3583-489">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="f3583-490">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="f3583-490">**Comments**</span></span> | <span data-ttu-id="f3583-491">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f3583-491">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-tag"></a><span data-ttu-id="f3583-492">Type de balise</span><span class="sxs-lookup"><span data-stu-id="f3583-492">Type of tag</span></span>

<span data-ttu-id="f3583-493">Spécifie le type de balise</span><span class="sxs-lookup"><span data-stu-id="f3583-493">Specifies the type of tag</span></span>

|<span data-ttu-id="f3583-494">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-494">Section</span></span>|<span data-ttu-id="f3583-495">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-495">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-496">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-496">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-497">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-497">**Key**</span></span> | <span data-ttu-id="f3583-498">clé</span><span class="sxs-lookup"><span data-stu-id="f3583-498">key</span></span> |
| <span data-ttu-id="f3583-499">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-499">**Data type**</span></span> | <span data-ttu-id="f3583-500">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-500">String</span></span> |
| <span data-ttu-id="f3583-501">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-501">**Possible values**</span></span> | `GROUP` |

##### <a name="value-of-tag"></a><span data-ttu-id="f3583-502">Valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="f3583-502">Value of tag</span></span>

<span data-ttu-id="f3583-503">Spécifie la valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="f3583-503">Specifies the value of tag</span></span>

|<span data-ttu-id="f3583-504">Section</span><span class="sxs-lookup"><span data-stu-id="f3583-504">Section</span></span>|<span data-ttu-id="f3583-505">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-505">Value</span></span>|
|:---|:---|
| <span data-ttu-id="f3583-506">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="f3583-506">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="f3583-507">**Key**</span><span class="sxs-lookup"><span data-stu-id="f3583-507">**Key**</span></span> | <span data-ttu-id="f3583-508">valeur</span><span class="sxs-lookup"><span data-stu-id="f3583-508">value</span></span> |
| <span data-ttu-id="f3583-509">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f3583-509">**Data type**</span></span> | <span data-ttu-id="f3583-510">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-510">String</span></span> |
| <span data-ttu-id="f3583-511">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f3583-511">**Possible values**</span></span> | <span data-ttu-id="f3583-512">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="f3583-512">any string</span></span> |

> [!IMPORTANT]  
> - <span data-ttu-id="f3583-513">Une seule valeur par type de balise peut être définie.</span><span class="sxs-lookup"><span data-stu-id="f3583-513">Only one value per tag type can be set.</span></span>
> - <span data-ttu-id="f3583-514">Le type de balises est unique et ne doit pas être répété dans le même profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="f3583-514">Type of tags are unique, and should not be repeated in the same configuration profile.</span></span>

## <a name="recommended-configuration-profile"></a><span data-ttu-id="f3583-515">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="f3583-515">Recommended configuration profile</span></span>

<span data-ttu-id="f3583-516">Pour commencer, nous recommandons la configuration suivante pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Microsoft Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="f3583-516">To get started, we recommend the following configuration for your enterprise to take advantage of all protection features that Microsoft Defender for Endpoint provides.</span></span>

<span data-ttu-id="f3583-517">Le profil de configuration suivant (ou, dans le cas de JAMF, une liste de propriétés qui peut être téléchargée dans le profil de configuration des paramètres personnalisés) sera :</span><span class="sxs-lookup"><span data-stu-id="f3583-517">The following configuration profile (or, in case of JAMF, a property list that could be uploaded into the custom settings configuration profile) will:</span></span>
- <span data-ttu-id="f3583-518">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="f3583-518">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="f3583-519">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="f3583-519">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="f3583-520">**Les applications potentiellement indésirables (PUA) sont** bloquées</span><span class="sxs-lookup"><span data-stu-id="f3583-520">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="f3583-521">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans Microsoft Defender pour les journaux de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f3583-521">**Archive bombs** (file with a high compression rate) are audited to Microsoft Defender for Endpoint logs</span></span>
- <span data-ttu-id="f3583-522">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="f3583-522">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="f3583-523">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="f3583-523">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="f3583-524">Activer l'envoi automatique d'échantillons</span><span class="sxs-lookup"><span data-stu-id="f3583-524">Enable automatic sample submission</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="f3583-525">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="f3583-525">Property list for JAMF configuration profile</span></span>

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

### <a name="intune-profile"></a><span data-ttu-id="f3583-526">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="f3583-526">Intune profile</span></span>

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

## <a name="full-configuration-profile-example"></a><span data-ttu-id="f3583-527">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="f3583-527">Full configuration profile example</span></span>

<span data-ttu-id="f3583-528">Les modèles suivants contiennent des entrées pour tous les paramètres décrits dans ce document et peuvent être utilisés pour des scénarios plus avancés dans lequel vous souhaitez mieux contrôler Microsoft Defender pour Endpoint sur macOS.</span><span class="sxs-lookup"><span data-stu-id="f3583-528">The following templates contain entries for all settings described in this document and can be used for more advanced scenarios where you want more control over Microsoft Defender for Endpoint on macOS.</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="f3583-529">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="f3583-529">Property list for JAMF configuration profile</span></span>

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

### <a name="intune-profile"></a><span data-ttu-id="f3583-530">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="f3583-530">Intune profile</span></span>

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

## <a name="property-list-validation"></a><span data-ttu-id="f3583-531">Validation de liste de propriétés</span><span class="sxs-lookup"><span data-stu-id="f3583-531">Property list validation</span></span>

<span data-ttu-id="f3583-532">La liste des propriétés doit être un fichier *.plist* valide.</span><span class="sxs-lookup"><span data-stu-id="f3583-532">The property list must be a valid *.plist* file.</span></span> <span data-ttu-id="f3583-533">Pour ce faire, exécutez :</span><span class="sxs-lookup"><span data-stu-id="f3583-533">This can be checked by executing:</span></span>

```bash
plutil -lint com.microsoft.wdav.plist
```
```Output
com.microsoft.wdav.plist: OK
```

<span data-ttu-id="f3583-534">Si le fichier est bien formé, la commande ci-dessus produit `OK` et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="f3583-534">If the file is well-formed, the above command outputs `OK` and returns an exit code of `0`.</span></span> <span data-ttu-id="f3583-535">Sinon, une erreur qui décrit le problème s'affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="f3583-535">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="f3583-536">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="f3583-536">Configuration profile deployment</span></span>

<span data-ttu-id="f3583-537">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="f3583-537">Once you've built the configuration profile for your enterprise, you can deploy it through the management console that your enterprise is using.</span></span> <span data-ttu-id="f3583-538">Les sections suivantes fournissent des instructions sur la façon de déployer ce profil à l'aide de JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="f3583-538">The following sections provide instructions on how to deploy this profile using JAMF and Intune.</span></span>

### <a name="jamf-deployment"></a><span data-ttu-id="f3583-539">Déploiement JAMF</span><span class="sxs-lookup"><span data-stu-id="f3583-539">JAMF deployment</span></span>

<span data-ttu-id="f3583-540">À partir de la console JAMF, **ouvrez** profils de configuration ordinateurs, accédez au profil de configuration que vous souhaitez utiliser, puis sélectionnez  >   **Paramètres personnalisés.**</span><span class="sxs-lookup"><span data-stu-id="f3583-540">From the JAMF console, open **Computers** > **Configuration Profiles**, navigate to the configuration profile you'd like to use, then select **Custom Settings**.</span></span> <span data-ttu-id="f3583-541">Créez une entrée avec `com.microsoft.wdav` comme domaine de préférence et téléchargez le *.plist* produit précédemment.</span><span class="sxs-lookup"><span data-stu-id="f3583-541">Create an entry with `com.microsoft.wdav` as the preference domain and upload the *.plist* produced earlier.</span></span>

>[!CAUTION]
><span data-ttu-id="f3583-542">Vous devez entrer le domaine de préférence correct ( ) ; sinon, les préférences ne seront pas reconnues par `com.microsoft.wdav` Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f3583-542">You must enter the correct preference domain (`com.microsoft.wdav`); otherwise, the preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

### <a name="intune-deployment"></a><span data-ttu-id="f3583-543">Déploiement d'Intune</span><span class="sxs-lookup"><span data-stu-id="f3583-543">Intune deployment</span></span>

1. <span data-ttu-id="f3583-544">Ouvrez **Gérer**  >  **la configuration de l'appareil.**</span><span class="sxs-lookup"><span data-stu-id="f3583-544">Open **Manage** > **Device configuration**.</span></span> <span data-ttu-id="f3583-545">Sélectionnez **Gérer**  >  **les profils**  >  **créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="f3583-545">Select **Manage** > **Profiles** > **Create Profile**.</span></span>

2. <span data-ttu-id="f3583-546">Choisissez un nom pour le profil.</span><span class="sxs-lookup"><span data-stu-id="f3583-546">Choose a name for the profile.</span></span> <span data-ttu-id="f3583-547">Change **Platform=macOS** to **Profile type=Custom**.</span><span class="sxs-lookup"><span data-stu-id="f3583-547">Change **Platform=macOS** to **Profile type=Custom**.</span></span> <span data-ttu-id="f3583-548">Sélectionnez Configurer.</span><span class="sxs-lookup"><span data-stu-id="f3583-548">Select Configure.</span></span>

3. <span data-ttu-id="f3583-549">Enregistrez le .plist produit précédemment sous `com.microsoft.wdav.xml` .</span><span class="sxs-lookup"><span data-stu-id="f3583-549">Save the .plist produced earlier as `com.microsoft.wdav.xml`.</span></span>

4. <span data-ttu-id="f3583-550">Entrez `com.microsoft.wdav` comme nom de profil de configuration **personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="f3583-550">Enter `com.microsoft.wdav` as the **custom configuration profile name**.</span></span>

5. <span data-ttu-id="f3583-551">Ouvrez le profil de configuration et téléchargez le `com.microsoft.wdav.xml` fichier.</span><span class="sxs-lookup"><span data-stu-id="f3583-551">Open the configuration profile and upload the `com.microsoft.wdav.xml` file.</span></span> <span data-ttu-id="f3583-552">(Ce fichier a été créé à l'étape 3.)</span><span class="sxs-lookup"><span data-stu-id="f3583-552">(This file was created in step 3.)</span></span>

6. <span data-ttu-id="f3583-553">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3583-553">Select **OK**.</span></span>

7. <span data-ttu-id="f3583-554">Sélectionnez   >  **Gérer les affectations.**</span><span class="sxs-lookup"><span data-stu-id="f3583-554">Select **Manage** > **Assignments**.</span></span> <span data-ttu-id="f3583-555">Dans **l'onglet** Inclure, sélectionnez Affecter à tous **les utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="f3583-555">In the **Include** tab, select **Assign to All Users & All devices**.</span></span>

>[!CAUTION]
><span data-ttu-id="f3583-556">Vous devez entrer le nom de profil de configuration personnalisé correct . Dans le cas contraire, ces préférences ne seront pas reconnues par Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="f3583-556">You must enter the correct custom configuration profile name; otherwise, these preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

## <a name="resources"></a><span data-ttu-id="f3583-557">Ressources</span><span class="sxs-lookup"><span data-stu-id="f3583-557">Resources</span></span>

- [<span data-ttu-id="f3583-558">Référence du profil de configuration (documentation Apple pour les développeurs)</span><span class="sxs-lookup"><span data-stu-id="f3583-558">Configuration Profile Reference (Apple developer documentation)</span></span>](https://developer.apple.com/business/documentation/Configuration-Profile-Reference.pdf)
