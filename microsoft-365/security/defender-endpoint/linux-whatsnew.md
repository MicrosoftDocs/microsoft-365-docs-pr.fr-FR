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
ms.openlocfilehash: 6aaf370ef0222c6c4a7f920a2a5ed8951f988839
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933564"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="d1862-104">Nouveautés de Microsoft Defender pour Endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="d1862-104">What's new in Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

## <a name="1012572-30121022125630"></a><span data-ttu-id="d1862-105">101.25.72 (30.121022.12563.0)</span><span class="sxs-lookup"><span data-stu-id="d1862-105">101.25.72 (30.121022.12563.0)</span></span>

- <span data-ttu-id="d1862-106">Microsoft Defender pour endpoint sur Linux est désormais disponible en prévisualisation pour les clients du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="d1862-106">Microsoft Defender for Endpoint on Linux is now available in preview for US Government customers.</span></span> <span data-ttu-id="d1862-107">Pour plus d'informations, [voir Microsoft Defender for Endpoint for US Government customers](gov.md).</span><span class="sxs-lookup"><span data-stu-id="d1862-107">For more information, see [Microsoft Defender for Endpoint for US Government customers](gov.md).</span></span>
- <span data-ttu-id="d1862-108">Nous avons résolu un problème dans lequel l'utilisation de Microsoft Defender pour endpoint sur Linux sur des systèmes avec des systèmes de fichiers LINUX a conduit à un arrêt du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="d1862-108">Fixed an issue where usage of Microsoft Defender for Endpoint on Linux on systems with FUSE filesystems was leading to OS hang</span></span>
- <span data-ttu-id="d1862-109">Améliorations des performances & d'autres résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-109">Performance improvements & other bug fixes</span></span>

## <a name="1012563-30121022125630"></a><span data-ttu-id="d1862-110">101.25.63 (30.121022.12563.0)</span><span class="sxs-lookup"><span data-stu-id="d1862-110">101.25.63 (30.121022.12563.0)</span></span>

- <span data-ttu-id="d1862-111">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-111">Performance improvements & bug fixes</span></span>

## <a name="1012364-30121021123640"></a><span data-ttu-id="d1862-112">101.23.64 (30.121021.12364.0)</span><span class="sxs-lookup"><span data-stu-id="d1862-112">101.23.64 (30.121021.12364.0)</span></span>

- <span data-ttu-id="d1862-113">Amélioration des performances pour la situation où un point de montage entier est ajouté à la liste d'exclusion antivirus.</span><span class="sxs-lookup"><span data-stu-id="d1862-113">Performance improvement for the situation where an entire mount point is added to the antivirus exclusion list.</span></span> <span data-ttu-id="d1862-114">Avant cette version, l'activité de fichier provenant du point de montage était toujours traitée par le produit.</span><span class="sxs-lookup"><span data-stu-id="d1862-114">Prior to this version, file activity originating from the mount point was still processed by the product.</span></span> <span data-ttu-id="d1862-115">À partir de cette version, l'activité de fichier pour les points de montage exclus est supprimée, ce qui améliore les performances du produit</span><span class="sxs-lookup"><span data-stu-id="d1862-115">Starting with this version, file activity for excluded mount points is suppressed, leading to better product performance</span></span>
- <span data-ttu-id="d1862-116">Ajout d'une nouvelle option à l'outil en ligne de commande pour afficher les informations sur la dernière analyse à la demande.</span><span class="sxs-lookup"><span data-stu-id="d1862-116">Added a new option to the command-line tool to view information about the last on-demand scan.</span></span> <span data-ttu-id="d1862-117">Pour afficher des informations sur la dernière analyse à la demande, exécutez `mdatp health --details antivirus`</span><span class="sxs-lookup"><span data-stu-id="d1862-117">To view information about the last on-demand scan, run `mdatp health --details antivirus`</span></span>
- <span data-ttu-id="d1862-118">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-118">Other performance improvements & bug fixes</span></span>

## <a name="1011853"></a><span data-ttu-id="d1862-119">101.18.53</span><span class="sxs-lookup"><span data-stu-id="d1862-119">101.18.53</span></span>

- <span data-ttu-id="d1862-120">EDR pour Linux est désormais [généralement disponible](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span><span class="sxs-lookup"><span data-stu-id="d1862-120">EDR for Linux is now [generally available](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span></span>
- <span data-ttu-id="d1862-121">Ajout d'un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions antivirus lors des `--ignore-exclusions` analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="d1862-121">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="d1862-122">Étendu avec un nouveau paramètre ( ) qui permet d'enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="d1862-122">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="d1862-123">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-123">Performance improvements & bug fixes</span></span>

## <a name="1011299"></a><span data-ttu-id="d1862-124">101.12.99</span><span class="sxs-lookup"><span data-stu-id="d1862-124">101.12.99</span></span>

- <span data-ttu-id="d1862-125">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-125">Performance improvements & bug fixes</span></span>

## <a name="1010476"></a><span data-ttu-id="d1862-126">101.04.76</span><span class="sxs-lookup"><span data-stu-id="d1862-126">101.04.76</span></span>

- <span data-ttu-id="d1862-127">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-127">Bug fixes</span></span>

## <a name="1010348"></a><span data-ttu-id="d1862-128">101.03.48</span><span class="sxs-lookup"><span data-stu-id="d1862-128">101.03.48</span></span>

- <span data-ttu-id="d1862-129">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-129">Bug fixes</span></span>

## <a name="1010255"></a><span data-ttu-id="d1862-130">101.02.55</span><span class="sxs-lookup"><span data-stu-id="d1862-130">101.02.55</span></span>

- <span data-ttu-id="d1862-131">Correction d'un problème dans lequel le produit ne démarre parfois pas après un redémarrage/mise à niveau</span><span class="sxs-lookup"><span data-stu-id="d1862-131">Fixed an issue where the product sometimes does not start following a reboot / upgrade</span></span>
- <span data-ttu-id="d1862-132">Correction d'un problème dans lequel les paramètres proxy ne sont pas persistants entre les mises à niveau de produits</span><span class="sxs-lookup"><span data-stu-id="d1862-132">Fixed an issue where proxy settings are not persisted across product upgrades</span></span>

## <a name="1010075"></a><span data-ttu-id="d1862-133">101.00.75</span><span class="sxs-lookup"><span data-stu-id="d1862-133">101.00.75</span></span>

- <span data-ttu-id="d1862-134">Prise en charge supplémentaire pour les types de système de fichiers suivants `ecryptfs` : , , , , , , , `fuse` `fuseblk` `jfs` `nfs` `overlay` `ramfs` `reiserfs` `udf` et `vfat`</span><span class="sxs-lookup"><span data-stu-id="d1862-134">Added support for the following file system types: `ecryptfs`, `fuse`, `fuseblk`, `jfs`, `nfs`, `overlay`, `ramfs`, `reiserfs`, `udf`, and `vfat`</span></span>
- <span data-ttu-id="d1862-135">Nouvelle syntaxe de [l'outil en ligne de commande.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="d1862-135">New syntax for the [command-line tool](linux-resources.md#configure-from-the-command-line).</span></span>
- <span data-ttu-id="d1862-136">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-136">Performance improvements & bug fixes</span></span>

## <a name="1009070"></a><span data-ttu-id="d1862-137">100.90.70</span><span class="sxs-lookup"><span data-stu-id="d1862-137">100.90.70</span></span>

> [!WARNING]
> <span data-ttu-id="d1862-138">Lors de la mise à niveau du package installé à partir d'une version de produit antérieure à la version 100.90.70, la mise à jour peut échouer sur les distributions Basées sur Red Hat et SLES.</span><span class="sxs-lookup"><span data-stu-id="d1862-138">When upgrading the installed package from a product version earlier than 100.90.70, the update may fail on Red Hat-based and SLES distributions.</span></span> <span data-ttu-id="d1862-139">Cela est dû à un changement majeur dans le chemin d'accès d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="d1862-139">This is because of a major change in a file path.</span></span> <span data-ttu-id="d1862-140">Une solution temporaire consiste à supprimer l'ancien package, puis à installer le nouveau.</span><span class="sxs-lookup"><span data-stu-id="d1862-140">A temporary solution is to remove the older package, and then install the newer one.</span></span> <span data-ttu-id="d1862-141">Ce problème n'existe pas dans les versions plus récentes.</span><span class="sxs-lookup"><span data-stu-id="d1862-141">This issue does not exist in newer versions.</span></span>

- <span data-ttu-id="d1862-142">Les [exclusions antivirus désormais prise en charge les caractères génériques](linux-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="d1862-142">Antivirus [exclusions now support wildcards](linux-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="d1862-143">Ajout de la possibilité de résoudre [les problèmes](linux-support-perf.md) de performances via l'outil en ligne `mdatp` de commande</span><span class="sxs-lookup"><span data-stu-id="d1862-143">Added the ability to [troubleshoot performance issues](linux-support-perf.md) through the `mdatp` command-line tool</span></span>
- <span data-ttu-id="d1862-144">Améliorations pour rendre l'installation du package plus robuste</span><span class="sxs-lookup"><span data-stu-id="d1862-144">Improvements to make the package installation more robust</span></span>
- <span data-ttu-id="d1862-145">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="d1862-145">Performance improvements & bug fixes</span></span>
