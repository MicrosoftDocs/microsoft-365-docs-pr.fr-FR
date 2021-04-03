---
title: Nouveautés de Microsoft Defender pour Endpoint pour Linux
description: Liste des principales modifications apportées à Microsoft Defender ATP pour Linux.
keywords: microsoft, defender, atp, linux, whatsnew, release
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
ms.openlocfilehash: 02a446f47ce4292b214c868e773802c53f7e3353
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51581001"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="3f9cf-104">Nouveautés de Microsoft Defender pour Endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="3f9cf-104">What's new in Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

## <a name="1012563-30121022125630"></a><span data-ttu-id="3f9cf-105">101.25.63 (30.121022.12563.0)</span><span class="sxs-lookup"><span data-stu-id="3f9cf-105">101.25.63 (30.121022.12563.0)</span></span>

- <span data-ttu-id="3f9cf-106">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-106">Performance improvements & bug fixes</span></span>

## <a name="1012364-30121021123640"></a><span data-ttu-id="3f9cf-107">101.23.64 (30.121021.12364.0)</span><span class="sxs-lookup"><span data-stu-id="3f9cf-107">101.23.64 (30.121021.12364.0)</span></span>

- <span data-ttu-id="3f9cf-108">Amélioration des performances pour la situation où un point de montage entier est ajouté à la liste d’exclusion antivirus.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-108">Performance improvement for the situation where an entire mount point is added to the antivirus exclusion list.</span></span> <span data-ttu-id="3f9cf-109">Avant cette version, l’activité de fichier provenant du point de montage était toujours traitée par le produit.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-109">Prior to this version, file activity originating from the mount point was still processed by the product.</span></span> <span data-ttu-id="3f9cf-110">À partir de cette version, l’activité de fichier pour les points de montage exclus est supprimée, ce qui améliore les performances du produit</span><span class="sxs-lookup"><span data-stu-id="3f9cf-110">Starting with this version, file activity for excluded mount points is suppressed, leading to better product performance</span></span>
- <span data-ttu-id="3f9cf-111">Ajout d’une nouvelle option à l’outil en ligne de commande pour afficher les informations sur la dernière analyse à la demande.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-111">Added a new option to the command-line tool to view information about the last on-demand scan.</span></span> <span data-ttu-id="3f9cf-112">Pour afficher des informations sur la dernière analyse à la demande, exécutez `mdatp health --details antivirus`</span><span class="sxs-lookup"><span data-stu-id="3f9cf-112">To view information about the last on-demand scan, run `mdatp health --details antivirus`</span></span>
- <span data-ttu-id="3f9cf-113">Autres améliorations en matière de performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-113">Other performance improvements & bug fixes</span></span>

## <a name="1011853"></a><span data-ttu-id="3f9cf-114">101.18.53</span><span class="sxs-lookup"><span data-stu-id="3f9cf-114">101.18.53</span></span>

- <span data-ttu-id="3f9cf-115">EDR pour Linux est désormais [généralement disponible](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span><span class="sxs-lookup"><span data-stu-id="3f9cf-115">EDR for Linux is now [generally available](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span></span>
- <span data-ttu-id="3f9cf-116">Ajout d’un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions antivirus lors des `--ignore-exclusions` analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="3f9cf-116">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="3f9cf-117">Étendu avec un nouveau paramètre ( ) qui permet d’enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="3f9cf-117">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="3f9cf-118">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-118">Performance improvements & bug fixes</span></span>

## <a name="1011299"></a><span data-ttu-id="3f9cf-119">101.12.99</span><span class="sxs-lookup"><span data-stu-id="3f9cf-119">101.12.99</span></span>

- <span data-ttu-id="3f9cf-120">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-120">Performance improvements & bug fixes</span></span>

## <a name="1010476"></a><span data-ttu-id="3f9cf-121">101.04.76</span><span class="sxs-lookup"><span data-stu-id="3f9cf-121">101.04.76</span></span>

- <span data-ttu-id="3f9cf-122">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-122">Bug fixes</span></span>

## <a name="1010348"></a><span data-ttu-id="3f9cf-123">101.03.48</span><span class="sxs-lookup"><span data-stu-id="3f9cf-123">101.03.48</span></span>

- <span data-ttu-id="3f9cf-124">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-124">Bug fixes</span></span>

## <a name="1010255"></a><span data-ttu-id="3f9cf-125">101.02.55</span><span class="sxs-lookup"><span data-stu-id="3f9cf-125">101.02.55</span></span>

- <span data-ttu-id="3f9cf-126">Correction d’un problème dans lequel le produit ne démarre parfois pas après un redémarrage/mise à niveau</span><span class="sxs-lookup"><span data-stu-id="3f9cf-126">Fixed an issue where the product sometimes does not start following a reboot / upgrade</span></span>
- <span data-ttu-id="3f9cf-127">Correction d’un problème dans lequel les paramètres proxy ne sont pas persistants entre les mises à niveau de produits</span><span class="sxs-lookup"><span data-stu-id="3f9cf-127">Fixed an issue where proxy settings are not persisted across product upgrades</span></span>

## <a name="1010075"></a><span data-ttu-id="3f9cf-128">101.00.75</span><span class="sxs-lookup"><span data-stu-id="3f9cf-128">101.00.75</span></span>

- <span data-ttu-id="3f9cf-129">Prise en charge supplémentaire pour les types de système de fichiers suivants `ecryptfs` : , , , , , , , `fuse` `fuseblk` `jfs` `nfs` `overlay` `ramfs` `reiserfs` `udf` et `vfat`</span><span class="sxs-lookup"><span data-stu-id="3f9cf-129">Added support for the following file system types: `ecryptfs`, `fuse`, `fuseblk`, `jfs`, `nfs`, `overlay`, `ramfs`, `reiserfs`, `udf`, and `vfat`</span></span>
- <span data-ttu-id="3f9cf-130">Nouvelle syntaxe de [l’outil en ligne de commande.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="3f9cf-130">New syntax for the [command-line tool](linux-resources.md#configure-from-the-command-line).</span></span>
- <span data-ttu-id="3f9cf-131">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-131">Performance improvements & bug fixes</span></span>

## <a name="1009070"></a><span data-ttu-id="3f9cf-132">100.90.70</span><span class="sxs-lookup"><span data-stu-id="3f9cf-132">100.90.70</span></span>

> [!WARNING]
> <span data-ttu-id="3f9cf-133">Lors de la mise à niveau du package installé à partir d’une version de produit antérieure à la version 100.90.70, la mise à jour peut échouer sur les distributions Basées sur Red Hat et SLES.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-133">When upgrading the installed package from a product version earlier than 100.90.70, the update may fail on Red Hat-based and SLES distributions.</span></span> <span data-ttu-id="3f9cf-134">Cela est dû à un changement majeur dans le chemin d’accès d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-134">This is because of a major change in a file path.</span></span> <span data-ttu-id="3f9cf-135">Une solution temporaire consiste à supprimer l’ancien package, puis à installer le nouveau.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-135">A temporary solution is to remove the older package, and then install the newer one.</span></span> <span data-ttu-id="3f9cf-136">Ce problème n’existe pas dans les versions plus récentes.</span><span class="sxs-lookup"><span data-stu-id="3f9cf-136">This issue does not exist in newer versions.</span></span>

- <span data-ttu-id="3f9cf-137">Les [exclusions antivirus désormais prise en charge les caractères génériques](linux-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="3f9cf-137">Antivirus [exclusions now support wildcards](linux-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="3f9cf-138">Ajout de la possibilité de résoudre [les problèmes](linux-support-perf.md) de performances via l’outil en ligne `mdatp` de commande</span><span class="sxs-lookup"><span data-stu-id="3f9cf-138">Added the ability to [troubleshoot performance issues](linux-support-perf.md) through the `mdatp` command-line tool</span></span>
- <span data-ttu-id="3f9cf-139">Améliorations pour rendre l’installation du package plus robuste</span><span class="sxs-lookup"><span data-stu-id="3f9cf-139">Improvements to make the package installation more robust</span></span>
- <span data-ttu-id="3f9cf-140">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="3f9cf-140">Performance improvements & bug fixes</span></span>
