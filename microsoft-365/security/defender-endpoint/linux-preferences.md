---
title: Définir des préférences pour Microsoft Defender ATP pour Linux
ms.reviewer: ''
description: Décrit comment configurer Microsoft Defender ATP pour Linux dans les entreprises.
keywords: microsoft, defender, atp, linux, installation, déployer, désinstallation, casque, ansible, linux, redhat, ubuntu, debian, sles, suse, centos
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
ms.openlocfilehash: 5206de55523c6f5a24fa85f29d48620b38be5bfa
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064558"
---
# <a name="set-preferences-for-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="b025d-104">Définir des préférences pour Microsoft Defender pour le point de terminaison pour Linux</span><span class="sxs-lookup"><span data-stu-id="b025d-104">Set preferences for Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b025d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b025d-105">**Applies to:**</span></span>
- [<span data-ttu-id="b025d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b025d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="b025d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b025d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b025d-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="b025d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="b025d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b025d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

>[!IMPORTANT]
><span data-ttu-id="b025d-110">Cette rubrique contient des instructions sur la façon de définir des préférences pour Defender pour Endpoint pour Linux dans les environnements d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b025d-110">This topic contains instructions for how to set preferences for Defender for Endpoint for Linux in enterprise environments.</span></span> <span data-ttu-id="b025d-111">Si vous souhaitez configurer le produit sur un appareil à partir de la ligne de commande, consultez [Ressources.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="b025d-111">If you are interested in configuring the product on a device from the command-line, see [Resources](linux-resources.md#configure-from-the-command-line).</span></span>

<span data-ttu-id="b025d-112">Dans les environnements d’entreprise, Defender pour Point de terminaison pour Linux peut être géré via un profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="b025d-112">In enterprise environments, Defender for Endpoint for Linux can be managed through a configuration profile.</span></span> <span data-ttu-id="b025d-113">Ce profil est déployé à partir de l’outil de gestion de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b025d-113">This profile is deployed from the management tool of your choice.</span></span> <span data-ttu-id="b025d-114">Les préférences gérées par l’entreprise prévalent sur les préférences définies localement sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b025d-114">Preferences managed by the enterprise take precedence over the ones set locally on the device.</span></span> <span data-ttu-id="b025d-115">En d’autres termes, les utilisateurs de votre entreprise ne peuvent pas modifier les préférences définies par le biais de ce profil de configuration.</span><span class="sxs-lookup"><span data-stu-id="b025d-115">In other words, users in your enterprise are not able to change preferences that are set through this configuration profile.</span></span>

<span data-ttu-id="b025d-116">Cet article décrit la structure de ce profil (y compris un profil recommandé que vous pouvez utiliser pour commencer) et des instructions sur la façon de déployer le profil.</span><span class="sxs-lookup"><span data-stu-id="b025d-116">This article describes the structure of this profile (including a recommended profile that you can use to get started) and instructions on how to deploy the profile.</span></span>

## <a name="configuration-profile-structure"></a><span data-ttu-id="b025d-117">Structure de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b025d-117">Configuration profile structure</span></span>

<span data-ttu-id="b025d-118">Le profil de configuration est un fichier .json qui se compose d’entrées identifiées par une clé (qui indique le nom de la préférence), suivi d’une valeur, qui dépend de la nature de la préférence.</span><span class="sxs-lookup"><span data-stu-id="b025d-118">The configuration profile is a .json file that consists of entries identified by a key (which denotes the name of the preference), followed by a value, which depends on the nature of the preference.</span></span> <span data-ttu-id="b025d-119">Les valeurs peuvent être simples, telles qu’une valeur numérique, ou complexes, telles qu’une liste imbriée de préférences.</span><span class="sxs-lookup"><span data-stu-id="b025d-119">Values can be simple, such as a numerical value, or complex, such as a nested list of preferences.</span></span>

<span data-ttu-id="b025d-120">En règle générale, vous utilisez un outil de gestion de la configuration pour pousser un fichier avec le nom ```mdatp_managed.json``` à l’emplacement ```/etc/opt/microsoft/mdatp/managed/``` .</span><span class="sxs-lookup"><span data-stu-id="b025d-120">Typically, you would use a configuration management tool to push a file with the name ```mdatp_managed.json``` at the location ```/etc/opt/microsoft/mdatp/managed/```.</span></span>

<span data-ttu-id="b025d-121">Le niveau supérieur du profil de configuration inclut les préférences et entrées à l’échelle du produit pour les sous-catégories du produit, qui sont expliquées plus en détail dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b025d-121">The top level of the configuration profile includes product-wide preferences and entries for subareas of the product, which are explained in more detail in the next sections.</span></span>

### <a name="antivirus-engine-preferences"></a><span data-ttu-id="b025d-122">Préférences du moteur antivirus</span><span class="sxs-lookup"><span data-stu-id="b025d-122">Antivirus engine preferences</span></span>

<span data-ttu-id="b025d-123">La *section antivirusEngine* du profil de configuration est utilisée pour gérer les préférences du composant antivirus du produit.</span><span class="sxs-lookup"><span data-stu-id="b025d-123">The *antivirusEngine* section of the configuration profile is used to manage the preferences of the antivirus component of the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-124">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-124">**Key**</span></span> | <span data-ttu-id="b025d-125">antivirusEngine</span><span class="sxs-lookup"><span data-stu-id="b025d-125">antivirusEngine</span></span> |
| <span data-ttu-id="b025d-126">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-126">**Data type**</span></span> | <span data-ttu-id="b025d-127">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b025d-127">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b025d-128">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-128">**Comments**</span></span> | <span data-ttu-id="b025d-129">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b025d-129">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-real-time-protection"></a><span data-ttu-id="b025d-130">Activer/désactiver la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="b025d-130">Enable / disable real-time protection</span></span>

<span data-ttu-id="b025d-131">Détermine si la protection en temps réel (analyser les fichiers à mesure qu’ils sont accessibles) est activée ou non.</span><span class="sxs-lookup"><span data-stu-id="b025d-131">Determines whether real-time protection (scan files as they are accessed) is enabled or not.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-132">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-132">**Key**</span></span> | <span data-ttu-id="b025d-133">enableRealTimeProtection</span><span class="sxs-lookup"><span data-stu-id="b025d-133">enableRealTimeProtection</span></span> |
| <span data-ttu-id="b025d-134">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-134">**Data type**</span></span> | <span data-ttu-id="b025d-135">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b025d-135">Boolean</span></span> |
| <span data-ttu-id="b025d-136">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-136">**Possible values**</span></span> | <span data-ttu-id="b025d-137">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-137">true (default)</span></span> <br/> <span data-ttu-id="b025d-138">false</span><span class="sxs-lookup"><span data-stu-id="b025d-138">false</span></span> |

#### <a name="enable--disable-passive-mode"></a><span data-ttu-id="b025d-139">Activer/désactiver le mode passif</span><span class="sxs-lookup"><span data-stu-id="b025d-139">Enable / disable passive mode</span></span>

<span data-ttu-id="b025d-140">Détermine si le moteur antivirus s’exécute en mode passif ou non.</span><span class="sxs-lookup"><span data-stu-id="b025d-140">Determines whether the antivirus engine runs in passive mode or not.</span></span> <span data-ttu-id="b025d-141">En mode passif :</span><span class="sxs-lookup"><span data-stu-id="b025d-141">In passive mode:</span></span>
- <span data-ttu-id="b025d-142">La protection en temps réel est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b025d-142">Real-time protection is turned off.</span></span>
- <span data-ttu-id="b025d-143">L’analyse à la demande est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b025d-143">On-demand scanning is turned on.</span></span>
- <span data-ttu-id="b025d-144">La correction automatique des menaces est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b025d-144">Automatic threat remediation is turned off.</span></span>
- <span data-ttu-id="b025d-145">Les mises à jour de l’intelligence de la sécurité sont allumées.</span><span class="sxs-lookup"><span data-stu-id="b025d-145">Security intelligence updates are turned on.</span></span>
- <span data-ttu-id="b025d-146">L’icône du menu État est masquée.</span><span class="sxs-lookup"><span data-stu-id="b025d-146">Status menu icon is hidden.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-147">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-147">**Key**</span></span> | <span data-ttu-id="b025d-148">passiveMode</span><span class="sxs-lookup"><span data-stu-id="b025d-148">passiveMode</span></span> |
| <span data-ttu-id="b025d-149">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-149">**Data type**</span></span> | <span data-ttu-id="b025d-150">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b025d-150">Boolean</span></span> |
| <span data-ttu-id="b025d-151">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-151">**Possible values**</span></span> | <span data-ttu-id="b025d-152">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-152">false (default)</span></span> <br/> <span data-ttu-id="b025d-153">true</span><span class="sxs-lookup"><span data-stu-id="b025d-153">true</span></span> |
| <span data-ttu-id="b025d-154">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-154">**Comments**</span></span> | <span data-ttu-id="b025d-155">Disponible dans Defender pour Endpoint version 100.67.60 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-155">Available in Defender for Endpoint version 100.67.60 or higher.</span></span> |

#### <a name="exclusion-merge-policy"></a><span data-ttu-id="b025d-156">Stratégie de fusion d’exclusions</span><span class="sxs-lookup"><span data-stu-id="b025d-156">Exclusion merge policy</span></span>

<span data-ttu-id="b025d-157">Spécifie la stratégie de fusion pour les exclusions.</span><span class="sxs-lookup"><span data-stu-id="b025d-157">Specifies the merge policy for exclusions.</span></span> <span data-ttu-id="b025d-158">Il peut s’agit d’une combinaison d’exclusions définies par l’administrateur et d’exclusions définies par l’utilisateur ( ) ou uniquement `merge` d’exclusions définies par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="b025d-158">It can be a combination of administrator-defined and user-defined exclusions (`merge`) or only administrator-defined exclusions (`admin_only`).</span></span> <span data-ttu-id="b025d-159">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres exclusions.</span><span class="sxs-lookup"><span data-stu-id="b025d-159">This setting can be used to restrict local users from defining their own exclusions.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-160">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-160">**Key**</span></span> | <span data-ttu-id="b025d-161">exclusionsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="b025d-161">exclusionsMergePolicy</span></span> |
| <span data-ttu-id="b025d-162">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-162">**Data type**</span></span> | <span data-ttu-id="b025d-163">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-163">String</span></span> |
| <span data-ttu-id="b025d-164">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-164">**Possible values**</span></span> | <span data-ttu-id="b025d-165">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-165">merge (default)</span></span> <br/> <span data-ttu-id="b025d-166">admin_only</span><span class="sxs-lookup"><span data-stu-id="b025d-166">admin_only</span></span> |
| <span data-ttu-id="b025d-167">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-167">**Comments**</span></span> | <span data-ttu-id="b025d-168">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-168">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="scan-exclusions"></a><span data-ttu-id="b025d-169">Analyser les exclusions</span><span class="sxs-lookup"><span data-stu-id="b025d-169">Scan exclusions</span></span>

<span data-ttu-id="b025d-170">Entités exclues de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b025d-170">Entities that have been excluded from the scan.</span></span> <span data-ttu-id="b025d-171">Les exclusions peuvent être spécifiées par des chemins d’accès complets, des extensions ou des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b025d-171">Exclusions can be specified by full paths, extensions, or file names.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-172">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-172">**Key**</span></span> | <span data-ttu-id="b025d-173">exclusions</span><span class="sxs-lookup"><span data-stu-id="b025d-173">exclusions</span></span> |
| <span data-ttu-id="b025d-174">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-174">**Data type**</span></span> | <span data-ttu-id="b025d-175">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b025d-175">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b025d-176">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-176">**Comments**</span></span> | <span data-ttu-id="b025d-177">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b025d-177">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="b025d-178">**Type d’exclusion**</span><span class="sxs-lookup"><span data-stu-id="b025d-178">**Type of exclusion**</span></span>

<span data-ttu-id="b025d-179">Spécifie le type de contenu exclu de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b025d-179">Specifies the type of content excluded from the scan.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-180">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-180">**Key**</span></span> | <span data-ttu-id="b025d-181">$type</span><span class="sxs-lookup"><span data-stu-id="b025d-181">$type</span></span> |
| <span data-ttu-id="b025d-182">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-182">**Data type**</span></span> | <span data-ttu-id="b025d-183">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-183">String</span></span> |
| <span data-ttu-id="b025d-184">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-184">**Possible values**</span></span> | <span data-ttu-id="b025d-185">excludedPath</span><span class="sxs-lookup"><span data-stu-id="b025d-185">excludedPath</span></span> <br/> <span data-ttu-id="b025d-186">excludedFileExtension</span><span class="sxs-lookup"><span data-stu-id="b025d-186">excludedFileExtension</span></span> <br/> <span data-ttu-id="b025d-187">excludedFileName</span><span class="sxs-lookup"><span data-stu-id="b025d-187">excludedFileName</span></span> |

<span data-ttu-id="b025d-188">**Chemin d’accès au contenu exclu**</span><span class="sxs-lookup"><span data-stu-id="b025d-188">**Path to excluded content**</span></span>

<span data-ttu-id="b025d-189">Utilisé pour exclure le contenu de l’analyse par chemin d’accès complet au fichier.</span><span class="sxs-lookup"><span data-stu-id="b025d-189">Used to exclude content from the scan by full file path.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-190">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-190">**Key**</span></span> | <span data-ttu-id="b025d-191">chemin</span><span class="sxs-lookup"><span data-stu-id="b025d-191">path</span></span> |
| <span data-ttu-id="b025d-192">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-192">**Data type**</span></span> | <span data-ttu-id="b025d-193">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-193">String</span></span> |
| <span data-ttu-id="b025d-194">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-194">**Possible values**</span></span> | <span data-ttu-id="b025d-195">chemins d’accès valides</span><span class="sxs-lookup"><span data-stu-id="b025d-195">valid paths</span></span> |
| <span data-ttu-id="b025d-196">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-196">**Comments**</span></span> | <span data-ttu-id="b025d-197">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="b025d-197">Applicable only if *$type* is *excludedPath*</span></span> |

<span data-ttu-id="b025d-198">**Type de chemin d’accès (fichier/répertoire)**</span><span class="sxs-lookup"><span data-stu-id="b025d-198">**Path type (file / directory)**</span></span>

<span data-ttu-id="b025d-199">Indique si la propriété *du chemin d’accès* fait référence à un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b025d-199">Indicates if the *path* property refers to a file or directory.</span></span> 

|||
|:---|:---|
| <span data-ttu-id="b025d-200">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-200">**Key**</span></span> | <span data-ttu-id="b025d-201">isDirectory</span><span class="sxs-lookup"><span data-stu-id="b025d-201">isDirectory</span></span> |
| <span data-ttu-id="b025d-202">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-202">**Data type**</span></span> | <span data-ttu-id="b025d-203">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b025d-203">Boolean</span></span> |
| <span data-ttu-id="b025d-204">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-204">**Possible values**</span></span> | <span data-ttu-id="b025d-205">false (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-205">false (default)</span></span> <br/> <span data-ttu-id="b025d-206">true</span><span class="sxs-lookup"><span data-stu-id="b025d-206">true</span></span> |
| <span data-ttu-id="b025d-207">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-207">**Comments**</span></span> | <span data-ttu-id="b025d-208">Applicable uniquement si *$type* est *excluPath*</span><span class="sxs-lookup"><span data-stu-id="b025d-208">Applicable only if *$type* is *excludedPath*</span></span> |

<span data-ttu-id="b025d-209">**Extension de fichier exclue de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="b025d-209">**File extension excluded from the scan**</span></span>

<span data-ttu-id="b025d-210">Utilisé pour exclure le contenu de l’analyse par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="b025d-210">Used to exclude content from the scan by file extension.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-211">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-211">**Key**</span></span> | <span data-ttu-id="b025d-212">extension</span><span class="sxs-lookup"><span data-stu-id="b025d-212">extension</span></span> |
| <span data-ttu-id="b025d-213">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-213">**Data type**</span></span> | <span data-ttu-id="b025d-214">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-214">String</span></span> |
| <span data-ttu-id="b025d-215">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-215">**Possible values**</span></span> | <span data-ttu-id="b025d-216">extensions de fichier valides</span><span class="sxs-lookup"><span data-stu-id="b025d-216">valid file extensions</span></span> |
| <span data-ttu-id="b025d-217">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-217">**Comments**</span></span> | <span data-ttu-id="b025d-218">Applicable uniquement si *$type* est *excluFileExtension*</span><span class="sxs-lookup"><span data-stu-id="b025d-218">Applicable only if *$type* is *excludedFileExtension*</span></span> |

<span data-ttu-id="b025d-219">**Processus exclu de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="b025d-219">**Process excluded from the scan**</span></span>

<span data-ttu-id="b025d-220">Spécifie un processus pour lequel toute l’activité de fichier est exclue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b025d-220">Specifies a process for which all file activity is excluded from scanning.</span></span> <span data-ttu-id="b025d-221">Le processus peut être spécifié par son nom (par exemple) ou son chemin `cat` d’accès complet (par exemple, `/bin/cat` ).</span><span class="sxs-lookup"><span data-stu-id="b025d-221">The process can be specified either by its name (for example, `cat`) or full path (for example, `/bin/cat`).</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-222">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-222">**Key**</span></span> | <span data-ttu-id="b025d-223">nom</span><span class="sxs-lookup"><span data-stu-id="b025d-223">name</span></span> |
| <span data-ttu-id="b025d-224">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-224">**Data type**</span></span> | <span data-ttu-id="b025d-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-225">String</span></span> |
| <span data-ttu-id="b025d-226">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-226">**Possible values**</span></span> | <span data-ttu-id="b025d-227">n’importe quelle chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-227">any string</span></span> |
| <span data-ttu-id="b025d-228">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-228">**Comments**</span></span> | <span data-ttu-id="b025d-229">Applicable uniquement *si $type* est *excluFileName*</span><span class="sxs-lookup"><span data-stu-id="b025d-229">Applicable only if *$type* is *excludedFileName*</span></span> |

#### <a name="allowed-threats"></a><span data-ttu-id="b025d-230">Menaces autorisées</span><span class="sxs-lookup"><span data-stu-id="b025d-230">Allowed threats</span></span>

<span data-ttu-id="b025d-231">Liste des menaces (identifiées par leur nom) qui ne sont pas bloquées par le produit et sont autorisées à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="b025d-231">List of threats (identified by their name) that are not blocked by the product and are instead allowed to run.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-232">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-232">**Key**</span></span> | <span data-ttu-id="b025d-233">allowedThreats</span><span class="sxs-lookup"><span data-stu-id="b025d-233">allowedThreats</span></span> |
| <span data-ttu-id="b025d-234">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-234">**Data type**</span></span> | <span data-ttu-id="b025d-235">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="b025d-235">Array of strings</span></span> |

#### <a name="disallowed-threat-actions"></a><span data-ttu-id="b025d-236">Actions contre les menaces nonallées</span><span class="sxs-lookup"><span data-stu-id="b025d-236">Disallowed threat actions</span></span>

<span data-ttu-id="b025d-237">Limite les actions que l’utilisateur local d’un appareil peut prendre lorsque des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="b025d-237">Restricts the actions that the local user of a device can take when threats are detected.</span></span> <span data-ttu-id="b025d-238">Les actions incluses dans cette liste ne sont pas affichées dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b025d-238">The actions included in this list are not displayed in the user interface.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-239">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-239">**Key**</span></span> | <span data-ttu-id="b025d-240">disallowedThreatActions</span><span class="sxs-lookup"><span data-stu-id="b025d-240">disallowedThreatActions</span></span> |
| <span data-ttu-id="b025d-241">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-241">**Data type**</span></span> | <span data-ttu-id="b025d-242">Tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="b025d-242">Array of strings</span></span> |
| <span data-ttu-id="b025d-243">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-243">**Possible values**</span></span> | <span data-ttu-id="b025d-244">autoriser (empêche les utilisateurs d’autoriser les menaces)</span><span class="sxs-lookup"><span data-stu-id="b025d-244">allow (restricts users from allowing threats)</span></span> <br/> <span data-ttu-id="b025d-245">restaurer (empêche les utilisateurs de restaurer les menaces de la quarantaine)</span><span class="sxs-lookup"><span data-stu-id="b025d-245">restore (restricts users from restoring threats from the quarantine)</span></span> |
| <span data-ttu-id="b025d-246">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-246">**Comments**</span></span> | <span data-ttu-id="b025d-247">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-247">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="threat-type-settings"></a><span data-ttu-id="b025d-248">Paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="b025d-248">Threat type settings</span></span>

<span data-ttu-id="b025d-249">La *préférence threatTypeSettings dans* le moteur antivirus est utilisée pour contrôler la façon dont certains types de menaces sont gérés par le produit.</span><span class="sxs-lookup"><span data-stu-id="b025d-249">The *threatTypeSettings* preference in the antivirus engine is used to control how certain threat types are handled by the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-250">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-250">**Key**</span></span> | <span data-ttu-id="b025d-251">threatTypeSettings</span><span class="sxs-lookup"><span data-stu-id="b025d-251">threatTypeSettings</span></span> |
| <span data-ttu-id="b025d-252">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-252">**Data type**</span></span> | <span data-ttu-id="b025d-253">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b025d-253">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b025d-254">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-254">**Comments**</span></span> | <span data-ttu-id="b025d-255">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b025d-255">See the following sections for a description of the dictionary contents.</span></span> |

<span data-ttu-id="b025d-256">**Type de menace**</span><span class="sxs-lookup"><span data-stu-id="b025d-256">**Threat type**</span></span>

<span data-ttu-id="b025d-257">Type de menace pour lequel le comportement est configuré.</span><span class="sxs-lookup"><span data-stu-id="b025d-257">Type of threat for which the behavior is configured.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-258">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-258">**Key**</span></span> | <span data-ttu-id="b025d-259">clé</span><span class="sxs-lookup"><span data-stu-id="b025d-259">key</span></span> |
| <span data-ttu-id="b025d-260">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-260">**Data type**</span></span> | <span data-ttu-id="b025d-261">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-261">String</span></span> |
| <span data-ttu-id="b025d-262">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-262">**Possible values**</span></span> | <span data-ttu-id="b025d-263">potentially_unwanted_application</span><span class="sxs-lookup"><span data-stu-id="b025d-263">potentially_unwanted_application</span></span> <br/> <span data-ttu-id="b025d-264">archive_bomb</span><span class="sxs-lookup"><span data-stu-id="b025d-264">archive_bomb</span></span> |

<span data-ttu-id="b025d-265">**Mesures à prendre**</span><span class="sxs-lookup"><span data-stu-id="b025d-265">**Action to take**</span></span>

<span data-ttu-id="b025d-266">Action à prendre en cas de menace du type spécifié dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="b025d-266">Action to take when coming across a threat of the type specified in the preceding section.</span></span> <span data-ttu-id="b025d-267">Peut être :</span><span class="sxs-lookup"><span data-stu-id="b025d-267">Can be:</span></span>

- <span data-ttu-id="b025d-268">**Audit**: l’appareil n’est pas protégé contre ce type de menace, mais une entrée sur la menace est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="b025d-268">**Audit**: The device is not protected against this type of threat, but an entry about the threat is logged.</span></span>
- <span data-ttu-id="b025d-269">**Bloc**: l’appareil est protégé contre ce type de menace et vous êtes averti dans la console de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b025d-269">**Block**: The device is protected against this type of threat and you are notified in the security console.</span></span>
- <span data-ttu-id="b025d-270">**Off**: l’appareil n’est pas protégé contre ce type de menace et rien n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="b025d-270">**Off**: The device is not protected against this type of threat and nothing is logged.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-271">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-271">**Key**</span></span> | <span data-ttu-id="b025d-272">valeur</span><span class="sxs-lookup"><span data-stu-id="b025d-272">value</span></span> |
| <span data-ttu-id="b025d-273">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-273">**Data type**</span></span> | <span data-ttu-id="b025d-274">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-274">String</span></span> |
| <span data-ttu-id="b025d-275">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-275">**Possible values**</span></span> | <span data-ttu-id="b025d-276">audit (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-276">audit (default)</span></span> <br/> <span data-ttu-id="b025d-277">block</span><span class="sxs-lookup"><span data-stu-id="b025d-277">block</span></span> <br/> <span data-ttu-id="b025d-278">off</span><span class="sxs-lookup"><span data-stu-id="b025d-278">off</span></span> |

#### <a name="threat-type-settings-merge-policy"></a><span data-ttu-id="b025d-279">Stratégie de fusion des paramètres du type de menace</span><span class="sxs-lookup"><span data-stu-id="b025d-279">Threat type settings merge policy</span></span>

<span data-ttu-id="b025d-280">Spécifie la stratégie de fusion pour les paramètres de type de menace.</span><span class="sxs-lookup"><span data-stu-id="b025d-280">Specifies the merge policy for threat type settings.</span></span> <span data-ttu-id="b025d-281">Il peut s’agit d’une combinaison de paramètres définis par l’administrateur et de paramètres définis par l’utilisateur ( ) ou uniquement de `merge` paramètres définis par l’administrateur ( `admin_only` ).</span><span class="sxs-lookup"><span data-stu-id="b025d-281">This can be a combination of administrator-defined and user-defined settings (`merge`) or only administrator-defined settings (`admin_only`).</span></span> <span data-ttu-id="b025d-282">Ce paramètre peut être utilisé pour empêcher les utilisateurs locaux de définir leurs propres paramètres pour différents types de menaces.</span><span class="sxs-lookup"><span data-stu-id="b025d-282">This setting can be used to restrict local users from defining their own settings for different threat types.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-283">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-283">**Key**</span></span> | <span data-ttu-id="b025d-284">threatTypeSettingsMergePolicy</span><span class="sxs-lookup"><span data-stu-id="b025d-284">threatTypeSettingsMergePolicy</span></span> |
| <span data-ttu-id="b025d-285">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-285">**Data type**</span></span> | <span data-ttu-id="b025d-286">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-286">String</span></span> |
| <span data-ttu-id="b025d-287">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-287">**Possible values**</span></span> | <span data-ttu-id="b025d-288">merge (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-288">merge (default)</span></span> <br/> <span data-ttu-id="b025d-289">admin_only</span><span class="sxs-lookup"><span data-stu-id="b025d-289">admin_only</span></span> |
| <span data-ttu-id="b025d-290">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-290">**Comments**</span></span> | <span data-ttu-id="b025d-291">Disponible dans Defender pour Endpoint version 100.83.73 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-291">Available in Defender for Endpoint version 100.83.73 or higher.</span></span> |

#### <a name="antivirus-scan-history-retention-in-days"></a><span data-ttu-id="b025d-292">Conservation de l’historique d’analyse antivirus (en jours)</span><span class="sxs-lookup"><span data-stu-id="b025d-292">Antivirus scan history retention (in days)</span></span>

<span data-ttu-id="b025d-293">Spécifiez le nombre de jours pendant combien de jours les résultats sont conservés dans l’historique d’analyse sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b025d-293">Specify the number of days that results are retained in the scan history on the device.</span></span> <span data-ttu-id="b025d-294">Les anciens résultats d’analyse sont supprimés de l’historique.</span><span class="sxs-lookup"><span data-stu-id="b025d-294">Old scan results are removed from the history.</span></span> <span data-ttu-id="b025d-295">Anciens fichiers mis en quarantaine qui sont également supprimés du disque.</span><span class="sxs-lookup"><span data-stu-id="b025d-295">Old quarantined files that are also removed from the disk.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-296">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-296">**Key**</span></span> | <span data-ttu-id="b025d-297">scanResultsRetentionDays</span><span class="sxs-lookup"><span data-stu-id="b025d-297">scanResultsRetentionDays</span></span> |
| <span data-ttu-id="b025d-298">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-298">**Data type**</span></span> | <span data-ttu-id="b025d-299">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-299">String</span></span> |
| <span data-ttu-id="b025d-300">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-300">**Possible values**</span></span> | <span data-ttu-id="b025d-301">90 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b025d-301">90 (default).</span></span> <span data-ttu-id="b025d-302">Les valeurs autorisées sont de 1 jour à 180 jours.</span><span class="sxs-lookup"><span data-stu-id="b025d-302">Allowed values are from 1 day to 180 days.</span></span> |
| <span data-ttu-id="b025d-303">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-303">**Comments**</span></span> | <span data-ttu-id="b025d-304">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-304">Available in Defender for Endpoint version 101.04.76 or higher.</span></span> |

#### <a name="maximum-number-of-items-in-the-antivirus-scan-history"></a><span data-ttu-id="b025d-305">Nombre maximal d’éléments dans l’historique d’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="b025d-305">Maximum number of items in the antivirus scan history</span></span>

<span data-ttu-id="b025d-306">Spécifiez le nombre maximal d’entrées à conserver dans l’historique d’analyse.</span><span class="sxs-lookup"><span data-stu-id="b025d-306">Specify the maximum number of entries to keep in the scan history.</span></span> <span data-ttu-id="b025d-307">Les entrées incluent toutes les analyses à la demande effectuées dans le passé et toutes les détections antivirus.</span><span class="sxs-lookup"><span data-stu-id="b025d-307">Entries include all on-demand scans performed in the past and all antivirus detections.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-308">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-308">**Key**</span></span> | <span data-ttu-id="b025d-309">scanHistoryMaximumItems</span><span class="sxs-lookup"><span data-stu-id="b025d-309">scanHistoryMaximumItems</span></span> |
| <span data-ttu-id="b025d-310">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-310">**Data type**</span></span> | <span data-ttu-id="b025d-311">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-311">String</span></span> |
| <span data-ttu-id="b025d-312">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-312">**Possible values**</span></span> | <span data-ttu-id="b025d-313">10000 (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b025d-313">10000 (default).</span></span> <span data-ttu-id="b025d-314">Les valeurs autorisées sont de 5 000 à 1 5 000 éléments.</span><span class="sxs-lookup"><span data-stu-id="b025d-314">Allowed values are from 5000 items to 15000 items.</span></span> |
| <span data-ttu-id="b025d-315">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-315">**Comments**</span></span> | <span data-ttu-id="b025d-316">Disponible dans Defender pour Endpoint version 101.04.76 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="b025d-316">Available in Defender for Endpoint version 101.04.76 or higher.</span></span> |

### <a name="cloud-delivered-protection-preferences"></a><span data-ttu-id="b025d-317">Préférences de protection dans le cloud</span><span class="sxs-lookup"><span data-stu-id="b025d-317">Cloud-delivered protection preferences</span></span>

<span data-ttu-id="b025d-318">*L’entrée cloudService* dans le profil de configuration est utilisée pour configurer la fonctionnalité de protection pilotée par le cloud du produit.</span><span class="sxs-lookup"><span data-stu-id="b025d-318">The *cloudService* entry in the configuration profile is used to configure the cloud-driven protection feature of the product.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-319">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-319">**Key**</span></span> | <span data-ttu-id="b025d-320">cloudService</span><span class="sxs-lookup"><span data-stu-id="b025d-320">cloudService</span></span> |
| <span data-ttu-id="b025d-321">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-321">**Data type**</span></span> | <span data-ttu-id="b025d-322">Dictionnaire (préférence imbriée)</span><span class="sxs-lookup"><span data-stu-id="b025d-322">Dictionary (nested preference)</span></span> |
| <span data-ttu-id="b025d-323">**Comments**</span><span class="sxs-lookup"><span data-stu-id="b025d-323">**Comments**</span></span> | <span data-ttu-id="b025d-324">Consultez les sections suivantes pour obtenir une description du contenu du dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="b025d-324">See the following sections for a description of the dictionary contents.</span></span> |

#### <a name="enable--disable-cloud-delivered-protection"></a><span data-ttu-id="b025d-325">Activer/désactiver la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b025d-325">Enable / disable cloud delivered protection</span></span>

<span data-ttu-id="b025d-326">Détermine si la protection cloud est activée ou non sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b025d-326">Determines whether cloud-delivered protection is enabled on the device or not.</span></span> <span data-ttu-id="b025d-327">Pour améliorer la sécurité de vos services, nous vous recommandons de maintenir cette fonctionnalité allumée.</span><span class="sxs-lookup"><span data-stu-id="b025d-327">To improve the security of your services, we recommend keeping this feature turned on.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-328">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-328">**Key**</span></span> | <span data-ttu-id="b025d-329">activé</span><span class="sxs-lookup"><span data-stu-id="b025d-329">enabled</span></span> |
| <span data-ttu-id="b025d-330">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-330">**Data type**</span></span> | <span data-ttu-id="b025d-331">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b025d-331">Boolean</span></span> |
| <span data-ttu-id="b025d-332">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-332">**Possible values**</span></span> | <span data-ttu-id="b025d-333">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-333">true (default)</span></span> <br/> <span data-ttu-id="b025d-334">false</span><span class="sxs-lookup"><span data-stu-id="b025d-334">false</span></span> |

#### <a name="diagnostic-collection-level"></a><span data-ttu-id="b025d-335">Niveau de collection de diagnostics</span><span class="sxs-lookup"><span data-stu-id="b025d-335">Diagnostic collection level</span></span>

<span data-ttu-id="b025d-336">Les données de diagnostic sont utilisées pour sécuriser et mettre à jour Defender for Endpoint, détecter, diagnostiquer et résoudre les problèmes, ainsi que pour améliorer les produits.</span><span class="sxs-lookup"><span data-stu-id="b025d-336">Diagnostic data is used to keep Defender for Endpoint secure and up-to-date, detect, diagnose and fix problems, and also make product improvements.</span></span> <span data-ttu-id="b025d-337">Ce paramètre détermine le niveau de diagnostics envoyés par le produit à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b025d-337">This setting determines the level of diagnostics sent by the product to Microsoft.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-338">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-338">**Key**</span></span> | <span data-ttu-id="b025d-339">diagnosticLevel</span><span class="sxs-lookup"><span data-stu-id="b025d-339">diagnosticLevel</span></span> |
| <span data-ttu-id="b025d-340">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-340">**Data type**</span></span> | <span data-ttu-id="b025d-341">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-341">String</span></span> |
| <span data-ttu-id="b025d-342">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-342">**Possible values**</span></span> | <span data-ttu-id="b025d-343">facultatif (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-343">optional (default)</span></span> <br/> <span data-ttu-id="b025d-344">obligatoire</span><span class="sxs-lookup"><span data-stu-id="b025d-344">required</span></span> |

#### <a name="enable--disable-automatic-sample-submissions"></a><span data-ttu-id="b025d-345">Activer/désactiver les envois automatiques d’échantillons</span><span class="sxs-lookup"><span data-stu-id="b025d-345">Enable / disable automatic sample submissions</span></span>

<span data-ttu-id="b025d-346">Détermine si des échantillons suspects (susceptibles de contenir des menaces) sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b025d-346">Determines whether suspicious samples (that are likely to contain threats) are sent to Microsoft.</span></span> <span data-ttu-id="b025d-347">Il existe trois niveaux pour contrôler l’envoi d’échantillons :</span><span class="sxs-lookup"><span data-stu-id="b025d-347">There are three levels for controlling sample submission:</span></span>

- <span data-ttu-id="b025d-348">**Aucun**: aucun échantillon suspect n’est envoyé à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b025d-348">**None**: no suspicious samples are submitted to Microsoft.</span></span>
- <span data-ttu-id="b025d-349">**Sécurisé**: seuls les échantillons suspects qui ne contiennent pas d’informations d’identification personnelle (PII) sont envoyés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b025d-349">**Safe**: only suspicious samples that do not contain personally identifiable information (PII) are submitted automatically.</span></span> <span data-ttu-id="b025d-350">Il s’agit de la valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b025d-350">This is the default value for this setting.</span></span>
- <span data-ttu-id="b025d-351">**Tous**: tous les échantillons suspects sont envoyés à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b025d-351">**All**: all suspicious samples are submitted to Microsoft.</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-352">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-352">**Key**</span></span> | <span data-ttu-id="b025d-353">automaticSampleSubmissionConsent</span><span class="sxs-lookup"><span data-stu-id="b025d-353">automaticSampleSubmissionConsent</span></span> |
| <span data-ttu-id="b025d-354">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-354">**Data type**</span></span> | <span data-ttu-id="b025d-355">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b025d-355">String</span></span> |
| <span data-ttu-id="b025d-356">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-356">**Possible values**</span></span> | <span data-ttu-id="b025d-357">aucune</span><span class="sxs-lookup"><span data-stu-id="b025d-357">none</span></span> <br/> <span data-ttu-id="b025d-358">safe (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-358">safe (default)</span></span> <br/> <span data-ttu-id="b025d-359">all</span><span class="sxs-lookup"><span data-stu-id="b025d-359">all</span></span> |

#### <a name="enable--disable-automatic-security-intelligence-updates"></a><span data-ttu-id="b025d-360">Activer/désactiver les mises à jour automatiques de l’intelligence de sécurité</span><span class="sxs-lookup"><span data-stu-id="b025d-360">Enable / disable automatic security intelligence updates</span></span>

<span data-ttu-id="b025d-361">Détermine si les mises à jour d’informations de sécurité sont installées automatiquement :</span><span class="sxs-lookup"><span data-stu-id="b025d-361">Determines whether security intelligence updates are installed automatically:</span></span>

|||
|:---|:---|
| <span data-ttu-id="b025d-362">**Clé**</span><span class="sxs-lookup"><span data-stu-id="b025d-362">**Key**</span></span> | <span data-ttu-id="b025d-363">automaticDefinitionUpdateEnabled</span><span class="sxs-lookup"><span data-stu-id="b025d-363">automaticDefinitionUpdateEnabled</span></span> |
| <span data-ttu-id="b025d-364">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b025d-364">**Data type**</span></span> | <span data-ttu-id="b025d-365">Valeur booléenne</span><span class="sxs-lookup"><span data-stu-id="b025d-365">Boolean</span></span> |
| <span data-ttu-id="b025d-366">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b025d-366">**Possible values**</span></span> | <span data-ttu-id="b025d-367">true (par défaut)</span><span class="sxs-lookup"><span data-stu-id="b025d-367">true (default)</span></span> <br/> <span data-ttu-id="b025d-368">false</span><span class="sxs-lookup"><span data-stu-id="b025d-368">false</span></span> |

## <a name="recommended-configuration-profile"></a><span data-ttu-id="b025d-369">Profil de configuration recommandé</span><span class="sxs-lookup"><span data-stu-id="b025d-369">Recommended configuration profile</span></span>

<span data-ttu-id="b025d-370">Pour commencer, nous recommandons le profil de configuration suivant pour votre entreprise afin de tirer parti de toutes les fonctionnalités de protection que Defender pour Endpoint fournit.</span><span class="sxs-lookup"><span data-stu-id="b025d-370">To get started, we recommend the following configuration profile for your enterprise to take advantage of all protection features that Defender for Endpoint provides.</span></span>

<span data-ttu-id="b025d-371">Le profil de configuration suivant :</span><span class="sxs-lookup"><span data-stu-id="b025d-371">The following configuration profile will:</span></span>

- <span data-ttu-id="b025d-372">Activer la protection en temps réel (RTP)</span><span class="sxs-lookup"><span data-stu-id="b025d-372">Enable real-time protection (RTP)</span></span>
- <span data-ttu-id="b025d-373">Spécifiez la façon dont les types de menaces suivants sont gérés :</span><span class="sxs-lookup"><span data-stu-id="b025d-373">Specify how the following threat types are handled:</span></span>
  - <span data-ttu-id="b025d-374">**Les applications potentiellement indésirables (PUA) sont** bloquées</span><span class="sxs-lookup"><span data-stu-id="b025d-374">**Potentially unwanted applications (PUA)** are blocked</span></span>
  - <span data-ttu-id="b025d-375">**Les archives** archivées (fichier avec un taux de compression élevé) sont auditées dans les journaux du produit</span><span class="sxs-lookup"><span data-stu-id="b025d-375">**Archive bombs** (file with a high compression rate) are audited to the product logs</span></span>
- <span data-ttu-id="b025d-376">Activer les mises à jour automatiques des informations de sécurité</span><span class="sxs-lookup"><span data-stu-id="b025d-376">Enable automatic security intelligence updates</span></span>
- <span data-ttu-id="b025d-377">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="b025d-377">Enable cloud-delivered protection</span></span>
- <span data-ttu-id="b025d-378">Activer l’envoi automatique d’échantillons au `safe` niveau</span><span class="sxs-lookup"><span data-stu-id="b025d-378">Enable automatic sample submission at `safe` level</span></span>

### <a name="sample-profile"></a><span data-ttu-id="b025d-379">Exemple de profil</span><span class="sxs-lookup"><span data-stu-id="b025d-379">Sample profile</span></span>

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
      "enabled":true
   }
}
```

## <a name="full-configuration-profile-example"></a><span data-ttu-id="b025d-380">Exemple de profil de configuration complète</span><span class="sxs-lookup"><span data-stu-id="b025d-380">Full configuration profile example</span></span>

<span data-ttu-id="b025d-381">Le profil de configuration suivant contient des entrées pour tous les paramètres décrits dans ce document et peut être utilisé pour des scénarios plus avancés où vous souhaitez contrôler davantage le produit.</span><span class="sxs-lookup"><span data-stu-id="b025d-381">The following configuration profile contains entries for all settings described in this document and can be used for more advanced scenarios where you want more control over the product.</span></span>

### <a name="full-profile"></a><span data-ttu-id="b025d-382">Profil complet</span><span class="sxs-lookup"><span data-stu-id="b025d-382">Full profile</span></span>

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
            "path":"/home"
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
      "automaticDefinitionUpdateEnabled":true
   }
}
```

## <a name="configuration-profile-validation"></a><span data-ttu-id="b025d-383">Validation du profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b025d-383">Configuration profile validation</span></span>

<span data-ttu-id="b025d-384">Le profil de configuration doit être un fichier au format JSON valide.</span><span class="sxs-lookup"><span data-stu-id="b025d-384">The configuration profile must be a valid JSON-formatted file.</span></span> <span data-ttu-id="b025d-385">Il existe un certain nombre d’outils qui peuvent être utilisés pour vérifier cela.</span><span class="sxs-lookup"><span data-stu-id="b025d-385">There are a number of tools that can be used to verify this.</span></span> <span data-ttu-id="b025d-386">Par exemple, si vous avez `python` installé sur votre appareil :</span><span class="sxs-lookup"><span data-stu-id="b025d-386">For example, if you have `python` installed on your device:</span></span>

```bash
python -m json.tool mdatp_managed.json
```

<span data-ttu-id="b025d-387">Si le JSON est bien formé, la commande ci-dessus le renvoie au Terminal et renvoie un code de sortie de `0` .</span><span class="sxs-lookup"><span data-stu-id="b025d-387">If the JSON is well-formed, the above command outputs it back to the Terminal and returns an exit code of `0`.</span></span> <span data-ttu-id="b025d-388">Sinon, une erreur qui décrit le problème s’affiche et la commande renvoie un code de sortie de `1` .</span><span class="sxs-lookup"><span data-stu-id="b025d-388">Otherwise, an error that describes the issue is displayed and the command returns an exit code of `1`.</span></span>

## <a name="configuration-profile-deployment"></a><span data-ttu-id="b025d-389">Déploiement de profil de configuration</span><span class="sxs-lookup"><span data-stu-id="b025d-389">Configuration profile deployment</span></span>

<span data-ttu-id="b025d-390">Une fois que vous avez créé le profil de configuration pour votre entreprise, vous pouvez le déployer via l’outil de gestion que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="b025d-390">Once you've built the configuration profile for your enterprise, you can deploy it through the management tool that your enterprise is using.</span></span> <span data-ttu-id="b025d-391">Defender pour le point de terminaison pour Linux lit la configuration gérée à partir du *fichier /etc/opt/microsoft/mdatp/managed/mdatp_managed.json.*</span><span class="sxs-lookup"><span data-stu-id="b025d-391">Defender for Endpoint for Linux reads the managed configuration from the */etc/opt/microsoft/mdatp/managed/mdatp_managed.json* file.</span></span>
