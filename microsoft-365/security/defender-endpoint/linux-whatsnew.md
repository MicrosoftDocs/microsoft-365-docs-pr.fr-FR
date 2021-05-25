---
title: Nouveautés de Microsoft Defender pour Endpoint sur Linux
description: Liste des principales modifications apportées à Microsoft Defender pour Endpoint sur Linux.
keywords: microsoft, defender, Microsoft Defender pour point de terminaison, linux, whatsnew, release
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: security
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
ms.openlocfilehash: 0adcecefc19c681ef68498a3e7c375913d85985d
ms.sourcegitcommit: 07e536f1a6e335f114da55048844e4a866fe731b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "52651127"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="aefc0-104">Nouveautés de Microsoft Defender pour Endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="aefc0-104">What's new in Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

## <a name="1012964-30121042129640"></a><span data-ttu-id="aefc0-105">101.29.64 (30.121042.12964.0)</span><span class="sxs-lookup"><span data-stu-id="aefc0-105">101.29.64 (30.121042.12964.0)</span></span>

- <span data-ttu-id="aefc0-106">À partir de cette version, les menaces détectées lors des analyses antivirus à la demande déclenchées via le client de ligne de commande sont automatiquement corrigés.</span><span class="sxs-lookup"><span data-stu-id="aefc0-106">Starting with this version, threats detected during on-demand antivirus scans triggered through the command-line client are automatically remediated.</span></span> <span data-ttu-id="aefc0-107">Les menaces détectées lors des analyses déclenchées via l’interface utilisateur nécessitent toujours une action manuelle.</span><span class="sxs-lookup"><span data-stu-id="aefc0-107">Threats detected during scans triggered through the user interface still require manual action.</span></span>
- <span data-ttu-id="aefc0-108">`mdatp diagnostic real-time-protection-statistics` prend désormais en charge deux commutateurs supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="aefc0-108">`mdatp diagnostic real-time-protection-statistics` now supports two additional switches:</span></span>
  - <span data-ttu-id="aefc0-109">`--sort`: trie la sortie décroit par nombre total de fichiers analysés</span><span class="sxs-lookup"><span data-stu-id="aefc0-109">`--sort`: sorts the output descending by total number of files scanned</span></span>
  - <span data-ttu-id="aefc0-110">`--top N`: affiche les N premiers résultats (fonctionne uniquement si `--sort` elle est également spécifiée)</span><span class="sxs-lookup"><span data-stu-id="aefc0-110">`--top N`: displays the top N results (only works if `--sort` is also specified)</span></span>
- <span data-ttu-id="aefc0-111">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-111">Performance improvements & bug fixes</span></span>

## <a name="1012572-30121022125630"></a><span data-ttu-id="aefc0-112">101.25.72 (30.121022.12563.0)</span><span class="sxs-lookup"><span data-stu-id="aefc0-112">101.25.72 (30.121022.12563.0)</span></span>

- <span data-ttu-id="aefc0-113">Microsoft Defender pour endpoint sur Linux est désormais disponible en prévisualisation pour les clients du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="aefc0-113">Microsoft Defender for Endpoint on Linux is now available in preview for US Government customers.</span></span> <span data-ttu-id="aefc0-114">Pour plus d’informations, [voir Microsoft Defender for Endpoint for US Government customers](gov.md).</span><span class="sxs-lookup"><span data-stu-id="aefc0-114">For more information, see [Microsoft Defender for Endpoint for US Government customers](gov.md).</span></span>
- <span data-ttu-id="aefc0-115">Nous avons résolu un problème dans lequel l’utilisation de Microsoft Defender pour endpoint sur Linux sur des systèmes avec des systèmes de fichiers LINUX a conduit à un arrêt du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="aefc0-115">Fixed an issue where usage of Microsoft Defender for Endpoint on Linux on systems with FUSE filesystems was leading to OS hang</span></span>
- <span data-ttu-id="aefc0-116">Améliorations des performances & d’autres résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-116">Performance improvements & other bug fixes</span></span>

## <a name="1012563-30121022125630"></a><span data-ttu-id="aefc0-117">101.25.63 (30.121022.12563.0)</span><span class="sxs-lookup"><span data-stu-id="aefc0-117">101.25.63 (30.121022.12563.0)</span></span>

- <span data-ttu-id="aefc0-118">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-118">Performance improvements & bug fixes</span></span>

## <a name="1012364-30121021123640"></a><span data-ttu-id="aefc0-119">101.23.64 (30.121021.12364.0)</span><span class="sxs-lookup"><span data-stu-id="aefc0-119">101.23.64 (30.121021.12364.0)</span></span>

- <span data-ttu-id="aefc0-120">Amélioration des performances pour la situation où un point de montage entier est ajouté à la liste d’exclusion antivirus.</span><span class="sxs-lookup"><span data-stu-id="aefc0-120">Performance improvement for the situation where an entire mount point is added to the antivirus exclusion list.</span></span> <span data-ttu-id="aefc0-121">Avant cette version, l’activité de fichier provenant du point de montage était toujours traitée par le produit.</span><span class="sxs-lookup"><span data-stu-id="aefc0-121">Prior to this version, file activity originating from the mount point was still processed by the product.</span></span> <span data-ttu-id="aefc0-122">À partir de cette version, l’activité de fichier pour les points de montage exclus est supprimée, ce qui améliore les performances du produit</span><span class="sxs-lookup"><span data-stu-id="aefc0-122">Starting with this version, file activity for excluded mount points is suppressed, leading to better product performance</span></span>
- <span data-ttu-id="aefc0-123">Ajout d’une nouvelle option à l’outil en ligne de commande pour afficher les informations sur la dernière analyse à la demande.</span><span class="sxs-lookup"><span data-stu-id="aefc0-123">Added a new option to the command-line tool to view information about the last on-demand scan.</span></span> <span data-ttu-id="aefc0-124">Pour afficher des informations sur la dernière analyse à la demande, exécutez `mdatp health --details antivirus`</span><span class="sxs-lookup"><span data-stu-id="aefc0-124">To view information about the last on-demand scan, run `mdatp health --details antivirus`</span></span>
- <span data-ttu-id="aefc0-125">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-125">Other performance improvements & bug fixes</span></span>

## <a name="1011853"></a><span data-ttu-id="aefc0-126">101.18.53</span><span class="sxs-lookup"><span data-stu-id="aefc0-126">101.18.53</span></span>

- <span data-ttu-id="aefc0-127">PEPT linux est désormais [généralement disponible](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span><span class="sxs-lookup"><span data-stu-id="aefc0-127">EDR for Linux is now [generally available](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span></span>
- <span data-ttu-id="aefc0-128">Ajout d’un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions antivirus lors des `--ignore-exclusions` analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="aefc0-128">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="aefc0-129">Étendu avec un nouveau paramètre ( ) qui permet d’enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="aefc0-129">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="aefc0-130">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-130">Performance improvements & bug fixes</span></span>

## <a name="1011299"></a><span data-ttu-id="aefc0-131">101.12.99</span><span class="sxs-lookup"><span data-stu-id="aefc0-131">101.12.99</span></span>

- <span data-ttu-id="aefc0-132">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-132">Performance improvements & bug fixes</span></span>

## <a name="1010476"></a><span data-ttu-id="aefc0-133">101.04.76</span><span class="sxs-lookup"><span data-stu-id="aefc0-133">101.04.76</span></span>

- <span data-ttu-id="aefc0-134">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-134">Bug fixes</span></span>

## <a name="1010348"></a><span data-ttu-id="aefc0-135">101.03.48</span><span class="sxs-lookup"><span data-stu-id="aefc0-135">101.03.48</span></span>

- <span data-ttu-id="aefc0-136">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-136">Bug fixes</span></span>

## <a name="1010255"></a><span data-ttu-id="aefc0-137">101.02.55</span><span class="sxs-lookup"><span data-stu-id="aefc0-137">101.02.55</span></span>

- <span data-ttu-id="aefc0-138">Correction d’un problème dans lequel le produit ne démarre parfois pas après un redémarrage/mise à niveau</span><span class="sxs-lookup"><span data-stu-id="aefc0-138">Fixed an issue where the product sometimes does not start following a reboot / upgrade</span></span>
- <span data-ttu-id="aefc0-139">Correction d’un problème dans lequel les paramètres proxy ne sont pas persistants entre les mises à niveau de produits</span><span class="sxs-lookup"><span data-stu-id="aefc0-139">Fixed an issue where proxy settings are not persisted across product upgrades</span></span>

## <a name="1010075"></a><span data-ttu-id="aefc0-140">101.00.75</span><span class="sxs-lookup"><span data-stu-id="aefc0-140">101.00.75</span></span>

- <span data-ttu-id="aefc0-141">Prise en charge supplémentaire pour les types de système de fichiers suivants `ecryptfs` : , , , , , , , `fuse` `fuseblk` `jfs` `nfs` `overlay` `ramfs` `reiserfs` `udf` et `vfat`</span><span class="sxs-lookup"><span data-stu-id="aefc0-141">Added support for the following file system types: `ecryptfs`, `fuse`, `fuseblk`, `jfs`, `nfs`, `overlay`, `ramfs`, `reiserfs`, `udf`, and `vfat`</span></span>
- <span data-ttu-id="aefc0-142">Nouvelle syntaxe de [l’outil en ligne de commande.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="aefc0-142">New syntax for the [command-line tool](linux-resources.md#configure-from-the-command-line).</span></span>
- <span data-ttu-id="aefc0-143">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-143">Performance improvements & bug fixes</span></span>

## <a name="1009070"></a><span data-ttu-id="aefc0-144">100.90.70</span><span class="sxs-lookup"><span data-stu-id="aefc0-144">100.90.70</span></span>

> [!WARNING]
> <span data-ttu-id="aefc0-145">Lors de la mise à niveau du package installé à partir d’une version de produit antérieure à la version 100.90.70, la mise à jour peut échouer sur les distributions Basées sur Red Hat et SLES.</span><span class="sxs-lookup"><span data-stu-id="aefc0-145">When upgrading the installed package from a product version earlier than 100.90.70, the update may fail on Red Hat-based and SLES distributions.</span></span> <span data-ttu-id="aefc0-146">Cela est dû à un changement majeur dans le chemin d’accès d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="aefc0-146">This is because of a major change in a file path.</span></span> <span data-ttu-id="aefc0-147">Une solution temporaire consiste à supprimer l’ancien package, puis à installer le nouveau.</span><span class="sxs-lookup"><span data-stu-id="aefc0-147">A temporary solution is to remove the older package, and then install the newer one.</span></span> <span data-ttu-id="aefc0-148">Ce problème n’existe pas dans les versions plus récentes.</span><span class="sxs-lookup"><span data-stu-id="aefc0-148">This issue does not exist in newer versions.</span></span>

- <span data-ttu-id="aefc0-149">Les [exclusions antivirus désormais prise en charge les caractères génériques](linux-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="aefc0-149">Antivirus [exclusions now support wildcards](linux-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="aefc0-150">Ajout de la possibilité de résoudre [les problèmes](linux-support-perf.md) de performances via l’outil en ligne `mdatp` de commande</span><span class="sxs-lookup"><span data-stu-id="aefc0-150">Added the ability to [troubleshoot performance issues](linux-support-perf.md) through the `mdatp` command-line tool</span></span>
- <span data-ttu-id="aefc0-151">Améliorations pour rendre l’installation du package plus robuste</span><span class="sxs-lookup"><span data-stu-id="aefc0-151">Improvements to make the package installation more robust</span></span>
- <span data-ttu-id="aefc0-152">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="aefc0-152">Performance improvements & bug fixes</span></span>
