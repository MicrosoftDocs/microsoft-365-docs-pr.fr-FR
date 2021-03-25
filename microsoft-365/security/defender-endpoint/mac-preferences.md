---
title: Définir des préférences pour Microsoft Defender ATP pour Mac
description: Configurez Microsoft Defender ATP pour Mac dans les organisations d’entreprise.
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
ms.openlocfilehash: 578830d44a9a69c3ccafd78ceaf59ddfe100e43f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51068894"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-for-mac"></a><span data-ttu-id="394e6-104">Définir des préférences pour Microsoft Defender pour endpoint pour Mac</span><span class="sxs-lookup"><span data-stu-id="394e6-104">Set preferences for Microsoft Defender for Endpoint for Mac</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="394e6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="394e6-105">**Applies to:**</span></span>

- [<span data-ttu-id="394e6-106">Microsoft Defender pour point de terminaison pour Mac</span><span class="sxs-lookup"><span data-stu-id="394e6-106">Microsoft Defender for Endpoint for Mac</span></span>](microsoft-defender-endpoint-mac.md)

>[!IMPORTANT]
><span data-ttu-id="394e6-107">Cet article contient des instructions sur la façon de définir des préférences pour Microsoft Defender pour Endpoint pour Mac dans les organisations d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="394e6-107">This article contains instructions for how to set preferences for Microsoft Defender for Endpoint for Mac in enterprise organizations.</span></span> <span data-ttu-id="394e6-108">Pour configurer Microsoft Defender pour endpoint pour Mac à l’aide de l’interface de ligne de commande, voir [Resources](mac-resources.md#configuring-from-the-command-line).</span><span class="sxs-lookup"><span data-stu-id="394e6-108">To configure Microsoft Defender for Endpoint for Mac using the command-line interface, see [Resources](mac-resources.md#configuring-from-the-command-line).</span></span>

## <a name="summary"></a><span data-ttu-id="394e6-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="394e6-109">Summary</span></span>

<span data-ttu-id="394e6-110">Dans les organisations d’entreprise, Microsoft Defender pour Endpoint pour Mac peut être géré par le biais d’un profil de configuration déployé à l’aide de l’un des outils de gestion.</span><span class="sxs-lookup"><span data-stu-id="394e6-110">In enterprise organizations, Microsoft Defender for Endpoint for Mac can be managed through a configuration profile that is deployed by using one of several management tools.</span></span> <span data-ttu-id="394e6-111">Les préférences gérées par votre équipe en charge des opérations de sécurité prévalent sur les préférences définies localement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="394e6-111">Preferences that are managed by your security operations team take precedence over preferences that are set locally on the device.</span></span> <span data-ttu-id="394e6-112">La modification des préférences définies par le biais du profil de configuration nécessite des privilèges escalades et n’est pas disponible pour les utilisateurs sans autorisations administratives.</span><span class="sxs-lookup"><span data-stu-id="394e6-112">Changing the preferences that are set through the configuration profile requires escalated privileges and is not available for users without administrative permissions.</span></span>

<span data-ttu-id="394e6-113">Cet article décrit la structure du profil de configuration, inclut un profil recommandé que vous pouvez utiliser pour commencer et fournit des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="394e6-113">This article describes the structure of the configuration profile, includes a recommended profile that you can use to get started, and provides instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="394e6-114">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="394e6-114">Configuration profile structure</span></span>

<span data-ttu-id="394e6-115">Le profil de configuration est un fichier *.plist* qui se compose d’entrées identifiées par une clé (qui indique le nom de la préférence), suivi d’une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="394e6-115">The configuration profile is a *.plist* file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="394e6-116">Les valeurs peuvent être simples (par exemple, une valeur numérique) ou complexes, telles qu’une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="394e6-116">Values can either be simple (such as a numerical value) or complex, such as a nested list of preferences.</span></span>

>[!CAUTION]
><span data-ttu-id="394e6-117">La disposition du profil de configuration dépend de la console de gestion que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="394e6-117">The layout of the configuration profile depends on the management console that you are using.</span></span> <span data-ttu-id="394e6-118">Les sections suivantes contiennent des exemples de profils de configuration pour JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="394e6-118">The following sections contain examples of configuration profiles for JAMF and Intune.</span></span>

<span data-ttu-id="394e6-119">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l’échelle du produit pour les sous-catégories de Microsoft Defender pour le point de terminaison, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="394e6-119">The top level of the configuration profile includes product-wide preferences and entries for subareas of Microsoft Defender for Endpoint, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="394e6-120">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="394e6-120">Antivirus engine preferences</span></span>

<span data-ttu-id="394e6-121">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="394e6-121">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of Microsoft Defender for Endpoint.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-122">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-122">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-123">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-123">**Key**</span></span> | <span data-ttu-id="394e6-124">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="394e6-124">antivirusEngine</span></span> |
| <span data-ttu-id="394e6-125">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-125">**Data type**</span></span> | <span data-ttu-id="394e6-126">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-126">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-127">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-127">**Comments**</span></span> | <span data-ttu-id="394e6-128">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-128">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="394e6-129">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="394e6-129">Enable / disable real-time protection</span></span>

<span data-ttu-id="394e6-130">Spécifiez s’il faut activer la protection en temps réel, qui analyse les fichiers à mesure qu’ils sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="394e6-130">Specify whether to enable real-time protection, which scans files as they are accessed.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-131">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-131">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-132">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-132">**Key**</span></span> | <span data-ttu-id="394e6-133">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="394e6-133">enableRealTimeProtection</span></span> |
| <span data-ttu-id="394e6-134">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-134">**Data type**</span></span> | <span data-ttu-id="394e6-135">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-135">Boolean</span></span> |
| <span data-ttu-id="394e6-136">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-136">**Possible values**</span></span> | <span data-ttu-id="394e6-137">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-137">true (default)</span></span> <br/> <span data-ttu-id="394e6-138">false</span><span class="sxs-lookup"><span data-stu-id="394e6-138">false</span></span> |

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="394e6-139">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="394e6-139">Enable / disable passive mode</span></span>

<span data-ttu-id="394e6-140">Spécifiez si le moteur antivirus s’exécute en mode passif.</span><span class="sxs-lookup"><span data-stu-id="394e6-140">Specify whether the antivirus engine runs in passive mode.</span></span> <span data-ttu-id="394e6-141">Le mode passif a les implications suivantes :</span><span class="sxs-lookup"><span data-stu-id="394e6-141">Passive mode has the following implications:</span></span> 
- <span data-ttu-id="394e6-142">La protection en temps réel est désactivée</span><span class="sxs-lookup"><span data-stu-id="394e6-142">Real-time protection is turned off</span></span>
- <span data-ttu-id="394e6-143">L’analyse à la demande est désactivée</span><span class="sxs-lookup"><span data-stu-id="394e6-143">On-demand scanning is turned on</span></span>
- <span data-ttu-id="394e6-144">La correction automatique des menaces est désactivée</span><span class="sxs-lookup"><span data-stu-id="394e6-144">Automatic threat remediation is turned off</span></span>
- <span data-ttu-id="394e6-145">Les mises à jour de l’intelligence de la sécurité sont allumées</span><span class="sxs-lookup"><span data-stu-id="394e6-145">Security intelligence updates are turned on</span></span>
- <span data-ttu-id="394e6-146">L’icône du menu État est masquée</span><span class="sxs-lookup"><span data-stu-id="394e6-146">Status menu icon is hidden</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-147">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-147">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-148">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-148">**Key**</span></span> | <span data-ttu-id="394e6-149">passiveMode</span><span class="sxs-lookup"><span data-stu-id="394e6-149">passiveMode</span></span> |
| <span data-ttu-id="394e6-150">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-150">**Data type**</span></span> | <span data-ttu-id="394e6-151">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-151">Boolean</span></span> |
| <span data-ttu-id="394e6-152">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-152">**Possible values**</span></span> | <span data-ttu-id="394e6-153">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-153">false (default)</span></span> <br/> <span data-ttu-id="394e6-154">true</span><span class="sxs-lookup"><span data-stu-id="394e6-154">true</span></span> |
| <span data-ttu-id="394e6-155">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-155">**Comments**</span></span> | <span data-ttu-id="394e6-156">Disponible dans Microsoft Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-156">Available in Microsoft Defender for Endpoint version 100.67.60 or higher.</span></span> |

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="394e6-157">Stratégie de fusion d’exclusions</span><span class="sxs-lookup"><span data-stu-id="394e6-157">Exclusion merge policy</span></span>

<span data-ttu-id="394e6-158">Spécifiez la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="394e6-158">Specify the merge policy for exclusions.</span></span> <span data-ttu-id="394e6-159">Il peut s’agit d’une combinaison d’exclusions définies par l’administrateur et d’exclusions définies par l’utilisateur ( ) ou uniquement `merge` d’exclusions définies par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="394e6-159">This can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="394e6-160">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="394e6-160">This setting can be used to restrict local users from defining their own exclusions.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-161">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-161">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-162">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-162">**Key**</span></span> | <span data-ttu-id="394e6-163">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="394e6-163">exclusionsMergePolicy</span></span> |
| <span data-ttu-id="394e6-164">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-164">**Data type**</span></span> | <span data-ttu-id="394e6-165">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-165">String</span></span> |
| <span data-ttu-id="394e6-166">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-166">**Possible values**</span></span> | <span data-ttu-id="394e6-167">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-167">merge (default)</span></span> <br/> <span data-ttu-id="394e6-168">admin_only</span><span class="sxs-lookup"><span data-stu-id="394e6-168">admin_only</span></span> |
| <span data-ttu-id="394e6-169">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-169">**Comments**</span></span> | <span data-ttu-id="394e6-170">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-170">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="scan-exclusions"></a><span data-ttu-id="394e6-171">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="394e6-171">Scan exclusions</span></span>

<span data-ttu-id="394e6-172">Spécifiez les entités exclues de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="394e6-172">Specify entities excluded from being scanned.</span></span> <span data-ttu-id="394e6-173">Les exclusions peuvent être spécifiées par des chemins d’accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="394e6-173">Exclusions can be specified by full paths, extensions, or file names.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-174">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-174">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-175">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-175">**Key**</span></span> | <span data-ttu-id="394e6-176">exclusions</span><span class="sxs-lookup"><span data-stu-id="394e6-176">exclusions</span></span> |
| <span data-ttu-id="394e6-177">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-177">**Data type**</span></span> | <span data-ttu-id="394e6-178">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-178">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-179">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-179">**Comments**</span></span> | <span data-ttu-id="394e6-180">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-180">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-exclusion"></a><span data-ttu-id="394e6-181">Type d’exclusion</span><span class="sxs-lookup"><span data-stu-id="394e6-181">Type of exclusion</span></span>

<span data-ttu-id="394e6-182">Spécifiez le contenu exclu de l’analyse par type.</span><span class="sxs-lookup"><span data-stu-id="394e6-182">Specify content excluded from being scanned by type.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-183">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-183">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-184">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-184">**Key**</span></span> | <span data-ttu-id="394e6-185">$type</span><span class="sxs-lookup"><span data-stu-id="394e6-185">$type</span></span> |
| <span data-ttu-id="394e6-186">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-186">**Data type**</span></span> | <span data-ttu-id="394e6-187">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-187">String</span></span> |
| <span data-ttu-id="394e6-188">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-188">**Possible values**</span></span> | <span data-ttu-id="394e6-189">excludedPath</span><span class="sxs-lookup"><span data-stu-id="394e6-189">excludedPath</span></span> <br/> <span data-ttu-id="394e6-190">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="394e6-190">excludedFileExtension</span></span> <br/> <span data-ttu-id="394e6-191">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="394e6-191">excludedFileName</span></span> |

##### <a name="path-to-excluded-content"></a><span data-ttu-id="394e6-192">Chemin d’accès au contenu exclu</span><span class="sxs-lookup"><span data-stu-id="394e6-192">Path to excluded content</span></span>

<span data-ttu-id="394e6-193">Spécifiez le contenu exclu de l’analyse par le chemin d’accès complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="394e6-193">Specify content excluded from being scanned by full file path.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-194">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-194">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-195">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-195">**Key**</span></span> | <span data-ttu-id="394e6-196">chemin</span><span class="sxs-lookup"><span data-stu-id="394e6-196">path</span></span> |
| <span data-ttu-id="394e6-197">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-197">**Data type**</span></span> | <span data-ttu-id="394e6-198">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-198">String</span></span> |
| <span data-ttu-id="394e6-199">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-199">**Possible values**</span></span> | <span data-ttu-id="394e6-200">chemins d’accès valides</span><span class="sxs-lookup"><span data-stu-id="394e6-200">valid paths</span></span> |
| <span data-ttu-id="394e6-201">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-201">**Comments**</span></span> | <span data-ttu-id="394e6-202">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="394e6-202">Applicable only if *$type* is *excludedPath*</span></span> |

##### <a name="path-type-file--directory"></a><span data-ttu-id="394e6-203">Type de chemin d’accès (fichier/répertoire)</span><span class="sxs-lookup"><span data-stu-id="394e6-203">Path type (file / directory)</span></span>

<span data-ttu-id="394e6-204">Indiquez si la *propriété du* chemin d’accès fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="394e6-204">Indicate if the *path* property refers to a file or directory.</span></span> 

|||
|:---|:---|
| <span data-ttu-id="394e6-205">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-205">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-206">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-206">**Key**</span></span> | <span data-ttu-id="394e6-207">isDirectory</span><span class="sxs-lookup"><span data-stu-id="394e6-207">isDirectory</span></span> |
| <span data-ttu-id="394e6-208">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-208">**Data type**</span></span> | <span data-ttu-id="394e6-209">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-209">Boolean</span></span> |
| <span data-ttu-id="394e6-210">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-210">**Possible values**</span></span> | <span data-ttu-id="394e6-211">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-211">false (default)</span></span> <br/> <span data-ttu-id="394e6-212">true</span><span class="sxs-lookup"><span data-stu-id="394e6-212">true</span></span> |
| <span data-ttu-id="394e6-213">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-213">**Comments**</span></span> | <span data-ttu-id="394e6-214">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="394e6-214">Applicable only if *$type* is *excludedPath*</span></span> |

##### <a name="file-extension-excluded-from-the-scan"></a><span data-ttu-id="394e6-215">Extension de fichier exclue de l’analyse</span><span class="sxs-lookup"><span data-stu-id="394e6-215">File extension excluded from the scan</span></span>

<span data-ttu-id="394e6-216">Spécifiez le contenu exclu de l’analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="394e6-216">Specify content excluded from being scanned by file extension.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-217">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-217">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-218">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-218">**Key**</span></span> | <span data-ttu-id="394e6-219">extension</span><span class="sxs-lookup"><span data-stu-id="394e6-219">extension</span></span> |
| <span data-ttu-id="394e6-220">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-220">**Data type**</span></span> | <span data-ttu-id="394e6-221">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-221">String</span></span> |
| <span data-ttu-id="394e6-222">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-222">**Possible values**</span></span> | <span data-ttu-id="394e6-223">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="394e6-223">valid file extensions</span></span> |
| <span data-ttu-id="394e6-224">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-224">**Comments**</span></span> | <span data-ttu-id="394e6-225">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="394e6-225">Applicable only if *$type* is *excludedFileExtension*</span></span> |

##### <a name="process-excluded-from-the-scan"></a><span data-ttu-id="394e6-226">Processus exclu de l’analyse</span><span class="sxs-lookup"><span data-stu-id="394e6-226">Process excluded from the scan</span></span>

<span data-ttu-id="394e6-227">Spécifiez un processus pour lequel toute l’activité de fichier est exclue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="394e6-227">Specify a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="394e6-228">Le processus peut être spécifié par son nom (par exemple) ou son chemin d’accès complet `cat` (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="394e6-228">The process can be specified either by its name (e.g. `cat`) or full path (e.g. `/bin/cat`).</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-229">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-229">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-230">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-230">**Key**</span></span> | <span data-ttu-id="394e6-231">nom</span><span class="sxs-lookup"><span data-stu-id="394e6-231">name</span></span> |
| <span data-ttu-id="394e6-232">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-232">**Data type**</span></span> | <span data-ttu-id="394e6-233">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-233">String</span></span> |
| <span data-ttu-id="394e6-234">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-234">**Possible values**</span></span> | <span data-ttu-id="394e6-235">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-235">any string</span></span> |
| <span data-ttu-id="394e6-236">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-236">**Comments**</span></span> | <span data-ttu-id="394e6-237">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="394e6-237">Applicable only if *$type* is *excludedFileName*</span></span> |

#### <a name="allowed-threats"></a><span data-ttu-id="394e6-238">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="394e6-238">Allowed threats</span></span>

<span data-ttu-id="394e6-239">Spécifiez les menaces par nom qui ne sont pas bloquées par Defender pour endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-239">Specify threats by name that are not blocked by Defender for Endpoint for Mac.</span></span> <span data-ttu-id="394e6-240">Ces menaces seront autorisées à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="394e6-240">These threats will be allowed to run.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-241">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-241">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-242">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-242">**Key**</span></span> | <span data-ttu-id="394e6-243">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="394e6-243">allowedThreats</span></span> |
| <span data-ttu-id="394e6-244">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-244">**Data type**</span></span> | <span data-ttu-id="394e6-245">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="394e6-245">Array of strings</span></span> |

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="394e6-246">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="394e6-246">Disallowed threat actions</span></span>

<span data-ttu-id="394e6-247">Limite les actions que l’utilisateur local d’un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="394e6-247">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="394e6-248">Les actions incluses dans cette liste ne sont pas affichées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="394e6-248">The actions included in this list are not displayed in the user interface.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-249">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-249">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-250">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-250">**Key**</span></span> | <span data-ttu-id="394e6-251">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="394e6-251">disallowedThreatActions</span></span> |
| <span data-ttu-id="394e6-252">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-252">**Data type**</span></span> | <span data-ttu-id="394e6-253">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="394e6-253">Array of strings</span></span> |
| <span data-ttu-id="394e6-254">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-254">**Possible values**</span></span> | <span data-ttu-id="394e6-255">autoriser (empêche les utilisateurs d’autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="394e6-255">allow (restricts users from allowing threats)</span></span> <br/> <span data-ttu-id="394e6-256">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="394e6-256">restore (restricts users from restoring threats from the quarantine)</span></span> |
| <span data-ttu-id="394e6-257">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-257">**Comments**</span></span> | <span data-ttu-id="394e6-258">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-258">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="threat-type-settings"></a><span data-ttu-id="394e6-259">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="394e6-259">Threat type settings</span></span>

<span data-ttu-id="394e6-260">Spécifiez comment certains types de menaces sont gérés par Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-260">Specify how certain threat types are handled by Microsoft Defender for Endpoint for Mac.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-261">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-261">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-262">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-262">**Key**</span></span> | <span data-ttu-id="394e6-263">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="394e6-263">threatTypeSettings</span></span> |
| <span data-ttu-id="394e6-264">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-264">**Data type**</span></span> | <span data-ttu-id="394e6-265">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-265">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-266">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-266">**Comments**</span></span> | <span data-ttu-id="394e6-267">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-267">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="threat-type"></a><span data-ttu-id="394e6-268">Type de menace</span><span class="sxs-lookup"><span data-stu-id="394e6-268">Threat type</span></span>

<span data-ttu-id="394e6-269">Spécifiez les types de menaces.</span><span class="sxs-lookup"><span data-stu-id="394e6-269">Specify threat types.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-270">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-270">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-271">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-271">**Key**</span></span> | <span data-ttu-id="394e6-272">clé</span><span class="sxs-lookup"><span data-stu-id="394e6-272">key</span></span> |
| <span data-ttu-id="394e6-273">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-273">**Data type**</span></span> | <span data-ttu-id="394e6-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-274">String</span></span> |
| <span data-ttu-id="394e6-275">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-275">**Possible values**</span></span> | <span data-ttu-id="394e6-276">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="394e6-276">potentially_unwanted_application</span></span> <br/> <span data-ttu-id="394e6-277">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="394e6-277">archive_bomb</span></span> |

##### <a name="action-to-take"></a><span data-ttu-id="394e6-278">Mesures à prendre</span><span class="sxs-lookup"><span data-stu-id="394e6-278">Action to take</span></span>

<span data-ttu-id="394e6-279">Spécifiez l’action à prendre lorsqu’une menace du type spécifié dans la section précédente est détectée.</span><span class="sxs-lookup"><span data-stu-id="394e6-279">Specify what action to take when a threat of the type specified in the preceding section is detected.</span></span> <span data-ttu-id="394e6-280">Choisissez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="394e6-280">Choose from the following options:</span></span>

- <span data-ttu-id="394e6-281">**Audit**: votre appareil n’est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="394e6-281">**Audit**: your device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="394e6-282">**Bloquer**: votre appareil est protégé contre ce type de menace et vous êtes averti dans l’interface utilisateur et la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="394e6-282">**Block**: your device is protected against this type of threat and you are notified in the user interface and the security console.</span></span>
- <span data-ttu-id="394e6-283">**Off**: votre appareil n’est pas protégé contre ce type de menace et rien n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="394e6-283">**Off**: your device is not protected against this type of threat and nothing is logged.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-284">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-284">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-285">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-285">**Key**</span></span> | <span data-ttu-id="394e6-286">valeur</span><span class="sxs-lookup"><span data-stu-id="394e6-286">value</span></span> |
| <span data-ttu-id="394e6-287">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-287">**Data type**</span></span> | <span data-ttu-id="394e6-288">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-288">String</span></span> |
| <span data-ttu-id="394e6-289">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-289">**Possible values**</span></span> | <span data-ttu-id="394e6-290">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-290">audit (default)</span></span> <br/> <span data-ttu-id="394e6-291">block</span><span class="sxs-lookup"><span data-stu-id="394e6-291">block</span></span> <br/> <span data-ttu-id="394e6-292">off</span><span class="sxs-lookup"><span data-stu-id="394e6-292">off</span></span> |

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="394e6-293">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="394e6-293">Threat type settings merge policy</span></span>

<span data-ttu-id="394e6-294">Spécifiez la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="394e6-294">Specify the merge policy for threat type settings.</span></span> <span data-ttu-id="394e6-295">Il peut s’agit d’une combinaison de paramètres définis par l’administrateur et de paramètres définis par l’utilisateur ( ) ou uniquement de `merge` paramètres définis par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="394e6-295">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="394e6-296">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="394e6-296">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-297">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-297">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-298">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-298">**Key**</span></span> | <span data-ttu-id="394e6-299">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="394e6-299">threatTypeSettingsMergePolicy</span></span> |
| <span data-ttu-id="394e6-300">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-300">**Data type**</span></span> | <span data-ttu-id="394e6-301">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-301">String</span></span> |
| <span data-ttu-id="394e6-302">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-302">**Possible values**</span></span> | <span data-ttu-id="394e6-303">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-303">merge (default)</span></span> <br/> <span data-ttu-id="394e6-304">admin_only</span><span class="sxs-lookup"><span data-stu-id="394e6-304">admin_only</span></span> |
| <span data-ttu-id="394e6-305">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-305">**Comments**</span></span> | <span data-ttu-id="394e6-306">Disponible dans Microsoft Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-306">Available in Microsoft Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="394e6-307">Conservation de l’historique d’analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="394e6-307">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="394e6-308">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l’historique d’analyse sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="394e6-308">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="394e6-309">Les anciens résultats d’analyse sont supprimés de l’historique.</span><span class="sxs-lookup"><span data-stu-id="394e6-309">Old scan results are removed from the history.</span></span> <span data-ttu-id="394e6-310">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="394e6-310">Old quarantined files that are also removed from the disk.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-311">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-311">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-312">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-312">**Key**</span></span> | <span data-ttu-id="394e6-313">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="394e6-313">scanResultsRetentionDays</span></span> |
| <span data-ttu-id="394e6-314">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-314">**Data type**</span></span> | <span data-ttu-id="394e6-315">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-315">String</span></span> |
| <span data-ttu-id="394e6-316">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-316">**Possible values**</span></span> | <span data-ttu-id="394e6-317">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="394e6-317">90 (default).</span></span> <span data-ttu-id="394e6-318">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="394e6-318">Allowed values are from 1 day to 180 days.</span></span> |
| <span data-ttu-id="394e6-319">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-319">**Comments**</span></span> | <span data-ttu-id="394e6-320">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-320">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="394e6-321">Nombre maximal d’éléments dans l’historique d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="394e6-321">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="394e6-322">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="394e6-322">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="394e6-323">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="394e6-323">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-324">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-324">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-325">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-325">**Key**</span></span> | <span data-ttu-id="394e6-326">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="394e6-326">scanHistoryMaximumItems</span></span> |
| <span data-ttu-id="394e6-327">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-327">**Data type**</span></span> | <span data-ttu-id="394e6-328">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-328">String</span></span> |
| <span data-ttu-id="394e6-329">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-329">**Possible values**</span></span> | <span data-ttu-id="394e6-330">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="394e6-330">10000 (default).</span></span> <span data-ttu-id="394e6-331">Les valeurs autorisées sont de 5 000 à 1 5 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="394e6-331">Allowed values are from 5000 items to 15000 items.</span></span> |
| <span data-ttu-id="394e6-332">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-332">**Comments**</span></span> | <span data-ttu-id="394e6-333">Disponible dans Microsoft Defender pour Endpoint version 101.07.23 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-333">Available in Microsoft Defender for Endpoint version 101.07.23 or higher.</span></span> |

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="394e6-334">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="394e6-334">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="394e6-335">Configurez les fonctionnalités de protection informatique de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-335">Configure the cloud-driven protection features of Microsoft Defender for Endpoint for Mac.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-336">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-336">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-337">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-337">**Key**</span></span> | <span data-ttu-id="394e6-338">cloudService</span><span class="sxs-lookup"><span data-stu-id="394e6-338">cloudService</span></span> |
| <span data-ttu-id="394e6-339">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-339">**Data type**</span></span> | <span data-ttu-id="394e6-340">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-340">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-341">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-341">**Comments**</span></span> | <span data-ttu-id="394e6-342">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-342">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="394e6-343">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="394e6-343">Enable / disable cloud-delivered protection</span></span>

<span data-ttu-id="394e6-344">Spécifiez s’il faut activer ou non la protection de l’appareil livrée par le cloud.</span><span class="sxs-lookup"><span data-stu-id="394e6-344">Specify whether to enable cloud-delivered protection the device or not.</span></span> <span data-ttu-id="394e6-345">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="394e6-345">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-346">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-346">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-347">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-347">**Key**</span></span> | <span data-ttu-id="394e6-348">activé</span><span class="sxs-lookup"><span data-stu-id="394e6-348">enabled</span></span> |
| <span data-ttu-id="394e6-349">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-349">**Data type**</span></span> | <span data-ttu-id="394e6-350">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-350">Boolean</span></span> |
| <span data-ttu-id="394e6-351">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-351">**Possible values**</span></span> | <span data-ttu-id="394e6-352">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-352">true (default)</span></span> <br/> <span data-ttu-id="394e6-353">false</span><span class="sxs-lookup"><span data-stu-id="394e6-353">false</span></span> |

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="394e6-354">Niveau de collection de diagnostics</span><span class="sxs-lookup"><span data-stu-id="394e6-354">Diagnostic collection level</span></span>

<span data-ttu-id="394e6-355">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Microsoft Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="394e6-355">Diagnostic data is used to keep Microsoft Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="394e6-356">Ce paramètre détermine le niveau de diagnostics envoyés par Microsoft Defender pour endpoint à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="394e6-356">This setting determines the level of diagnostics sent by Microsoft Defender for Endpoint to Microsoft.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-357">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-357">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-358">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-358">**Key**</span></span> | <span data-ttu-id="394e6-359">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="394e6-359">diagnosticLevel</span></span> |
| <span data-ttu-id="394e6-360">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-360">**Data type**</span></span> | <span data-ttu-id="394e6-361">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-361">String</span></span> |
| <span data-ttu-id="394e6-362">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-362">**Possible values**</span></span> | <span data-ttu-id="394e6-363">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-363">optional (default)</span></span> <br/> <span data-ttu-id="394e6-364">obligatoire</span><span class="sxs-lookup"><span data-stu-id="394e6-364">required</span></span> |

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="394e6-365">Activer/désactiver les envois automatiques d’échantillons</span><span class="sxs-lookup"><span data-stu-id="394e6-365">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="394e6-366">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="394e6-366">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="394e6-367">Vous êtes invité à savoir si le fichier envoyé est susceptible de contenir des informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="394e6-367">You are prompted if the submitted file is likely to contain personal information.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-368">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-368">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-369">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-369">**Key**</span></span> | <span data-ttu-id="394e6-370">automaticSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="394e6-370">automaticSampleSubmission</span></span> |
| <span data-ttu-id="394e6-371">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-371">**Data type**</span></span> | <span data-ttu-id="394e6-372">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-372">Boolean</span></span> |
| <span data-ttu-id="394e6-373">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-373">**Possible values**</span></span> | <span data-ttu-id="394e6-374">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-374">true (default)</span></span> <br/> <span data-ttu-id="394e6-375">false</span><span class="sxs-lookup"><span data-stu-id="394e6-375">false</span></span> |

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="394e6-376">Activer/désactiver les mises à jour automatiques de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="394e6-376">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="394e6-377">Détermine si les mises à jour d’informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="394e6-377">Determines whether security intelligence updates are installed automatically:</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-378">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-378">**Key**</span></span> | <span data-ttu-id="394e6-379">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="394e6-379">automaticDefinitionUpdateEnabled</span></span> |
| <span data-ttu-id="394e6-380">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-380">**Data type**</span></span> | <span data-ttu-id="394e6-381">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-381">Boolean</span></span> |
| <span data-ttu-id="394e6-382">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-382">**Possible values**</span></span> | <span data-ttu-id="394e6-383">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-383">true (default)</span></span> <br/> <span data-ttu-id="394e6-384">false</span><span class="sxs-lookup"><span data-stu-id="394e6-384">false</span></span> |

### <a name="user-interface-preferences"></a><span data-ttu-id="394e6-385">Préférences de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="394e6-385">User interface preferences</span></span>

<span data-ttu-id="394e6-386">Gérez les préférences pour l’interface utilisateur de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-386">Manage the preferences for the user interface of Microsoft Defender for Endpoint for Mac.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-387">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-387">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-388">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-388">**Key**</span></span> | <span data-ttu-id="394e6-389">userInterface</span><span class="sxs-lookup"><span data-stu-id="394e6-389">userInterface</span></span> |
| <span data-ttu-id="394e6-390">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-390">**Data type**</span></span> | <span data-ttu-id="394e6-391">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-391">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-392">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-392">**Comments**</span></span> | <span data-ttu-id="394e6-393">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-393">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="show--hide-status-menu-icon"></a><span data-ttu-id="394e6-394">Afficher/masquer l’icône du menu État</span><span class="sxs-lookup"><span data-stu-id="394e6-394">Show / hide status menu icon</span></span>

<span data-ttu-id="394e6-395">Spécifiez s’il faut afficher ou masquer l’icône du menu d’état dans le coin supérieur droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="394e6-395">Specify whether to show or hide the status menu icon in the top-right corner of the screen.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-396">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-396">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-397">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-397">**Key**</span></span> | <span data-ttu-id="394e6-398">hideStatusMenuIcon</span><span class="sxs-lookup"><span data-stu-id="394e6-398">hideStatusMenuIcon</span></span> |
| <span data-ttu-id="394e6-399">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-399">**Data type**</span></span> | <span data-ttu-id="394e6-400">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="394e6-400">Boolean</span></span> |
| <span data-ttu-id="394e6-401">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-401">**Possible values**</span></span> | <span data-ttu-id="394e6-402">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-402">false (default)</span></span> <br/> <span data-ttu-id="394e6-403">true</span><span class="sxs-lookup"><span data-stu-id="394e6-403">true</span></span> |

#### <a name="show--hide-option-to-send-feedback"></a><span data-ttu-id="394e6-404">Afficher /masquer l’option d’envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="394e6-404">Show / hide option to send feedback</span></span>

<span data-ttu-id="394e6-405">Spécifiez si les utilisateurs peuvent envoyer des commentaires à Microsoft en allant à `Help`  >  `Send Feedback` .</span><span class="sxs-lookup"><span data-stu-id="394e6-405">Specify whether users can submit feedback to Microsoft by going to `Help` > `Send Feedback`.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-406">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-406">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-407">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-407">**Key**</span></span> | <span data-ttu-id="394e6-408">userInitiatedFeedback</span><span class="sxs-lookup"><span data-stu-id="394e6-408">userInitiatedFeedback</span></span> |
| <span data-ttu-id="394e6-409">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-409">**Data type**</span></span> | <span data-ttu-id="394e6-410">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-410">String</span></span> |
| <span data-ttu-id="394e6-411">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-411">**Possible values**</span></span> | <span data-ttu-id="394e6-412">activé (par défaut)</span><span class="sxs-lookup"><span data-stu-id="394e6-412">enabled (default)</span></span> <br/> <span data-ttu-id="394e6-413">désactivé</span><span class="sxs-lookup"><span data-stu-id="394e6-413">disabled</span></span> |
| <span data-ttu-id="394e6-414">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-414">**Comments**</span></span> | <span data-ttu-id="394e6-415">Disponible dans Microsoft Defender pour Endpoint version 101.19.61 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="394e6-415">Available in Microsoft Defender for Endpoint version 101.19.61 or higher.</span></span> |

### <a name="endpoint-detection-and-response-preferences"></a><span data-ttu-id="394e6-416">Préférences de détection et de réponse des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="394e6-416">Endpoint detection and response preferences</span></span>

<span data-ttu-id="394e6-417">Gérez les préférences du composant EDR (Endpoint Detection and Response) de Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-417">Manage the preferences of the endpoint detection and response (EDR) component of Microsoft Defender for Endpoint for Mac.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-418">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-418">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-419">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-419">**Key**</span></span> | <span data-ttu-id="394e6-420">edr</span><span class="sxs-lookup"><span data-stu-id="394e6-420">edr</span></span> |
| <span data-ttu-id="394e6-421">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-421">**Data type**</span></span> | <span data-ttu-id="394e6-422">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-422">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-423">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-423">**Comments**</span></span> | <span data-ttu-id="394e6-424">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-424">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="device-tags"></a><span data-ttu-id="394e6-425">Balises d’appareil</span><span class="sxs-lookup"><span data-stu-id="394e6-425">Device tags</span></span>

<span data-ttu-id="394e6-426">Spécifiez un nom de balise et sa valeur.</span><span class="sxs-lookup"><span data-stu-id="394e6-426">Specify a tag name and its value.</span></span> 

- <span data-ttu-id="394e6-427">La balise GROUP balise l’appareil avec la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="394e6-427">The GROUP tag, tags the device with the specified value.</span></span> <span data-ttu-id="394e6-428">La balise est reflétée dans le portail sous la page de l’appareil et peut être utilisée pour le filtrage et le regroupement des appareils.</span><span class="sxs-lookup"><span data-stu-id="394e6-428">The tag is reflected in the portal under the device page and can be used for filtering and grouping devices.</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-429">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-429">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-430">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-430">**Key**</span></span> | <span data-ttu-id="394e6-431">étiquettes</span><span class="sxs-lookup"><span data-stu-id="394e6-431">tags</span></span> |
| <span data-ttu-id="394e6-432">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-432">**Data type**</span></span> | <span data-ttu-id="394e6-433">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="394e6-433">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="394e6-434">**Comments**</span><span class="sxs-lookup"><span data-stu-id="394e6-434">**Comments**</span></span> | <span data-ttu-id="394e6-435">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="394e6-435">See the following sections for a description of the dictionary contents.</span></span> |

##### <a name="type-of-tag"></a><span data-ttu-id="394e6-436">Type de balise</span><span class="sxs-lookup"><span data-stu-id="394e6-436">Type of tag</span></span>

<span data-ttu-id="394e6-437">Spécifie le type de balise</span><span class="sxs-lookup"><span data-stu-id="394e6-437">Specifies the type of tag</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-438">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-438">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-439">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-439">**Key**</span></span> | <span data-ttu-id="394e6-440">clé</span><span class="sxs-lookup"><span data-stu-id="394e6-440">key</span></span> |
| <span data-ttu-id="394e6-441">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-441">**Data type**</span></span> | <span data-ttu-id="394e6-442">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-442">String</span></span> |
| <span data-ttu-id="394e6-443">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-443">**Possible values**</span></span> | `GROUP` |

##### <a name="value-of-tag"></a><span data-ttu-id="394e6-444">Valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="394e6-444">Value of tag</span></span>

<span data-ttu-id="394e6-445">Spécifie la valeur de la balise</span><span class="sxs-lookup"><span data-stu-id="394e6-445">Specifies the value of tag</span></span>

|||
|:---|:---|
| <span data-ttu-id="394e6-446">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="394e6-446">**Domain**</span></span> | `com.microsoft.wdav` |
| <span data-ttu-id="394e6-447">**Clé**</span><span class="sxs-lookup"><span data-stu-id="394e6-447">**Key**</span></span> | <span data-ttu-id="394e6-448">valeur</span><span class="sxs-lookup"><span data-stu-id="394e6-448">value</span></span> |
| <span data-ttu-id="394e6-449">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="394e6-449">**Data type**</span></span> | <span data-ttu-id="394e6-450">Chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-450">String</span></span> |
| <span data-ttu-id="394e6-451">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="394e6-451">**Possible values**</span></span> | <span data-ttu-id="394e6-452">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="394e6-452">any string</span></span> |

> [!IMPORTANT]  
> - <span data-ttu-id="394e6-453">Une seule valeur par type de balise peut être définie.</span><span class="sxs-lookup"><span data-stu-id="394e6-453">Only one value per tag type can be set.</span></span>
> - <span data-ttu-id="394e6-454">Le type de balises est unique et ne doit pas être répété dans le même profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="394e6-454">Type of tags are unique, and should not be repeated in the same configuration profile.</span></span>

## <a name="recommended-configuration-profile"></a><span data-ttu-id="394e6-455">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="394e6-455">Recommended configuration profile</span></span>

<span data-ttu-id="394e6-456">Pour commencer, nous recommandons la configuration suivante pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Microsoft Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="394e6-456">To get started, we recommend the following configuration for your enterprise to take advantage of all protection features that Microsoft Defender for Endpoint provides.</span></span>

<span data-ttu-id="394e6-457">Le profil de configuration suivant (ou, dans le cas de JAMF, une liste de propriétés qui peut être téléchargée dans le profil de configuration des paramètres personnalisés) sera :</span><span class="sxs-lookup"><span data-stu-id="394e6-457">The following configuration profile (or, in case of JAMF, a property list that could be uploaded into the custom settings configuration profile) will:</span></span>
- <span data-ttu-id="394e6-458">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="394e6-458">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="394e6-459">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="394e6-459">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="394e6-460">**Les applications potentiellement indésirables (PUA) sont** bloquées</span><span class="sxs-lookup"><span data-stu-id="394e6-460">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="394e6-461">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans Microsoft Defender pour les journaux de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="394e6-461">**Archive bombs** (file with a high compression rate) are audited to Microsoft Defender for Endpoint logs</span></span>
- <span data-ttu-id="394e6-462">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="394e6-462">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="394e6-463">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="394e6-463">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="394e6-464">Activer l’envoi automatique d’échantillons</span><span class="sxs-lookup"><span data-stu-id="394e6-464">Enable automatic sample submission</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="394e6-465">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="394e6-465">Property list for JAMF configuration profile</span></span>

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

### <a name="intune-profile"></a><span data-ttu-id="394e6-466">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="394e6-466">Intune profile</span></span>

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

## <a name="full-configuration-profile-example"></a><span data-ttu-id="394e6-467">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="394e6-467">Full configuration profile example</span></span>

<span data-ttu-id="394e6-468">Les modèles suivants contiennent des entrées pour tous les paramètres décrits dans ce document et peuvent être utilisés pour des scénarios plus avancés dans lequel vous souhaitez mieux contrôler Microsoft Defender pour Endpoint pour Mac.</span><span class="sxs-lookup"><span data-stu-id="394e6-468">The following templates contain entries for all settings described in this document and can be used for more advanced scenarios where you want more control over Microsoft Defender for Endpoint for Mac.</span></span>

### <a name="property-list-for-jamf-configuration-profile"></a><span data-ttu-id="394e6-469">Liste de propriétés pour le profil de configuration JAMF</span><span class="sxs-lookup"><span data-stu-id="394e6-469">Property list for JAMF configuration profile</span></span>

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

### <a name="intune-profile"></a><span data-ttu-id="394e6-470">Profil Intune</span><span class="sxs-lookup"><span data-stu-id="394e6-470">Intune profile</span></span>

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

## <a name="property-list-validation"></a><span data-ttu-id="394e6-471">Validation de liste de propriétés</span><span class="sxs-lookup"><span data-stu-id="394e6-471">Property list validation</span></span>

<span data-ttu-id="394e6-472">La liste des propriétés doit être un fichier *.plist* valide.</span><span class="sxs-lookup"><span data-stu-id="394e6-472">The property list must be a valid *.plist* file.</span></span> <span data-ttu-id="394e6-473">Pour ce faire, exécutez :</span><span class="sxs-lookup"><span data-stu-id="394e6-473">This can be checked by executing:</span></span>

```bash
plutil -lint com.microsoft.wdav.plist
```
```Output
com.microsoft.wdav.plist: OK
```

<span data-ttu-id="394e6-474">Si le fichier est bien formé, la commande ci-dessus produit `OK` et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="394e6-474">If the file is well-formed, the above command outputs `OK` and returns an exit code of `0`.</span></span> <span data-ttu-id="394e6-475">Sinon, une erreur qui décrit le problème s’affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="394e6-475">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="394e6-476">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="394e6-476">Configuration profile deployment</span></span>

<span data-ttu-id="394e6-477">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via la console de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="394e6-477">Once you've built the configuration profile for your enterprise, you can deploy it through the management console that your enterprise is using.</span></span> <span data-ttu-id="394e6-478">Les sections suivantes fournissent des instructions sur la façon de déployer ce profil à l’aide de JAMF et Intune.</span><span class="sxs-lookup"><span data-stu-id="394e6-478">The following sections provide instructions on how to deploy this profile using JAMF and Intune.</span></span>

### <a name="jamf-deployment"></a><span data-ttu-id="394e6-479">Déploiement JAMF</span><span class="sxs-lookup"><span data-stu-id="394e6-479">JAMF deployment</span></span>

<span data-ttu-id="394e6-480">À partir de la console JAMF, **ouvrez** profils de configuration ordinateurs, accédez au profil de configuration que vous souhaitez utiliser, puis sélectionnez  >   **Paramètres personnalisés.**</span><span class="sxs-lookup"><span data-stu-id="394e6-480">From the JAMF console, open **Computers** > **Configuration Profiles**, navigate to the configuration profile you'd like to use, then select **Custom Settings**.</span></span> <span data-ttu-id="394e6-481">Créez une entrée avec `com.microsoft.wdav` comme domaine de préférence et téléchargez le *.plist* produit précédemment.</span><span class="sxs-lookup"><span data-stu-id="394e6-481">Create an entry with `com.microsoft.wdav` as the preference domain and upload the *.plist* produced earlier.</span></span>

>[!CAUTION]
><span data-ttu-id="394e6-482">Vous devez entrer le domaine de préférence correct ( ) ; sinon, les préférences ne seront pas reconnues par `com.microsoft.wdav` Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="394e6-482">You must enter the correct preference domain (`com.microsoft.wdav`); otherwise, the preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

### <a name="intune-deployment"></a><span data-ttu-id="394e6-483">Déploiement d’Intune</span><span class="sxs-lookup"><span data-stu-id="394e6-483">Intune deployment</span></span>

1. <span data-ttu-id="394e6-484">Ouvrez **Gérer**  >  **la configuration de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="394e6-484">Open **Manage** > **Device configuration**.</span></span> <span data-ttu-id="394e6-485">Sélectionnez **Gérer**  >  **les profils**  >  **créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="394e6-485">Select **Manage** > **Profiles** > **Create Profile**.</span></span>

2. <span data-ttu-id="394e6-486">Choisissez un nom pour le profil.</span><span class="sxs-lookup"><span data-stu-id="394e6-486">Choose a name for the profile.</span></span> <span data-ttu-id="394e6-487">Change **Platform=macOS** to **Profile type=Custom**.</span><span class="sxs-lookup"><span data-stu-id="394e6-487">Change **Platform=macOS** to **Profile type=Custom**.</span></span> <span data-ttu-id="394e6-488">Sélectionnez Configurer.</span><span class="sxs-lookup"><span data-stu-id="394e6-488">Select Configure.</span></span>

3. <span data-ttu-id="394e6-489">Enregistrez le .plist produit précédemment sous `com.microsoft.wdav.xml` .</span><span class="sxs-lookup"><span data-stu-id="394e6-489">Save the .plist produced earlier as `com.microsoft.wdav.xml`.</span></span>

4. <span data-ttu-id="394e6-490">Entrez `com.microsoft.wdav` comme nom de profil de configuration **personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="394e6-490">Enter `com.microsoft.wdav` as the **custom configuration profile name**.</span></span>

5. <span data-ttu-id="394e6-491">Ouvrez le profil de configuration et téléchargez le `com.microsoft.wdav.xml` fichier.</span><span class="sxs-lookup"><span data-stu-id="394e6-491">Open the configuration profile and upload the `com.microsoft.wdav.xml` file.</span></span> <span data-ttu-id="394e6-492">(Ce fichier a été créé à l’étape 3.)</span><span class="sxs-lookup"><span data-stu-id="394e6-492">(This file was created in step 3.)</span></span>

6. <span data-ttu-id="394e6-493">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="394e6-493">Select **OK**.</span></span>

7. <span data-ttu-id="394e6-494">Sélectionnez   >  **Gérer les affectations.**</span><span class="sxs-lookup"><span data-stu-id="394e6-494">Select **Manage** > **Assignments**.</span></span> <span data-ttu-id="394e6-495">Dans **l’onglet** Inclure, sélectionnez Affecter à tous **les utilisateurs & tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="394e6-495">In the **Include** tab, select **Assign to All Users & All devices**.</span></span>

>[!CAUTION]
><span data-ttu-id="394e6-496">Vous devez entrer le nom de profil de configuration personnalisé correct . Dans le cas contraire, ces préférences ne seront pas reconnues par Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="394e6-496">You must enter the correct custom configuration profile name; otherwise, these preferences will not be recognized by Microsoft Defender for Endpoint.</span></span>

## <a name="resources"></a><span data-ttu-id="394e6-497">Ressources</span><span class="sxs-lookup"><span data-stu-id="394e6-497">Resources</span></span>

- [<span data-ttu-id="394e6-498">Référence du profil de configuration (documentation Apple pour les développeurs)</span><span class="sxs-lookup"><span data-stu-id="394e6-498">Configuration Profile Reference (Apple developer documentation)</span></span>](https://developer.apple.com/business/documentation/Configuration-Profile-Reference.pdf)
