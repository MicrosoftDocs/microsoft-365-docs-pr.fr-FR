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
ms.openlocfilehash: 43324b0f3a0d5d351d7164bb05415899bf7d181c
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51062449"
---
# <a name="whats-new-in-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="8c541-104">Nouveautés de Microsoft Defender pour Endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="8c541-104">What's new in Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

## <a name="1011853"></a><span data-ttu-id="8c541-105">101.18.53</span><span class="sxs-lookup"><span data-stu-id="8c541-105">101.18.53</span></span>

- <span data-ttu-id="8c541-106">EDR pour Linux est désormais [généralement disponible](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span><span class="sxs-lookup"><span data-stu-id="8c541-106">EDR for Linux is now [generally available](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/edr-for-linux-is-now-is-generally-available/ba-p/2048539)</span></span>
- <span data-ttu-id="8c541-107">Ajout d’un nouveau commutateur de ligne de commande ( ) pour ignorer les exclusions av lors `--ignore-exclusions` des analyses personnalisées ( `mdatp scan custom` )</span><span class="sxs-lookup"><span data-stu-id="8c541-107">Added a new command-line switch (`--ignore-exclusions`) to ignore AV exclusions during custom scans (`mdatp scan custom`)</span></span>
- <span data-ttu-id="8c541-108">Étendu avec un nouveau paramètre ( ) qui permet d’enregistrer les journaux de diagnostic dans `mdatp diagnostic create` `--path [directory]` un autre répertoire</span><span class="sxs-lookup"><span data-stu-id="8c541-108">Extended `mdatp diagnostic create` with a new parameter (`--path [directory]`) that allows the diagnostic logs to be saved to a different directory</span></span>
- <span data-ttu-id="8c541-109">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-109">Performance improvements & bug fixes</span></span>

## <a name="1011299"></a><span data-ttu-id="8c541-110">101.12.99</span><span class="sxs-lookup"><span data-stu-id="8c541-110">101.12.99</span></span>

- <span data-ttu-id="8c541-111">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-111">Performance improvements & bug fixes</span></span>

## <a name="1010476"></a><span data-ttu-id="8c541-112">101.04.76</span><span class="sxs-lookup"><span data-stu-id="8c541-112">101.04.76</span></span>

- <span data-ttu-id="8c541-113">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-113">Bug fixes</span></span>

## <a name="1010348"></a><span data-ttu-id="8c541-114">101.03.48</span><span class="sxs-lookup"><span data-stu-id="8c541-114">101.03.48</span></span>

- <span data-ttu-id="8c541-115">Résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-115">Bug fixes</span></span>

## <a name="1010255"></a><span data-ttu-id="8c541-116">101.02.55</span><span class="sxs-lookup"><span data-stu-id="8c541-116">101.02.55</span></span>

- <span data-ttu-id="8c541-117">Correction d’un problème dans lequel le produit ne démarre parfois pas après un redémarrage/mise à niveau</span><span class="sxs-lookup"><span data-stu-id="8c541-117">Fixed an issue where the product sometimes does not start following a reboot / upgrade</span></span>
- <span data-ttu-id="8c541-118">Correction d’un problème dans lequel les paramètres proxy ne sont pas persistants entre les mises à niveau de produits</span><span class="sxs-lookup"><span data-stu-id="8c541-118">Fixed an issue where proxy settings are not persisted across product upgrades</span></span>

## <a name="1010075"></a><span data-ttu-id="8c541-119">101.00.75</span><span class="sxs-lookup"><span data-stu-id="8c541-119">101.00.75</span></span>

- <span data-ttu-id="8c541-120">Ajout de la prise en charge des types de système de fichiers suivants `ecryptfs` : , , , , , , , `fuse` `fuseblk` `jfs` `nfs` `overlay` `ramfs` `reiserfs` `udf` et `vfat`</span><span class="sxs-lookup"><span data-stu-id="8c541-120">Added support for the following file system types: `ecryptfs`, `fuse`, `fuseblk`, `jfs`, `nfs`, `overlay`, `ramfs`, `reiserfs`, `udf`, and `vfat`</span></span>
- <span data-ttu-id="8c541-121">Nouvelle syntaxe pour [l’outil en ligne de commande.](linux-resources.md#configure-from-the-command-line)</span><span class="sxs-lookup"><span data-stu-id="8c541-121">New syntax for the [command-line tool](linux-resources.md#configure-from-the-command-line).</span></span>
- <span data-ttu-id="8c541-122">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-122">Performance improvements & bug fixes</span></span>

## <a name="1009070"></a><span data-ttu-id="8c541-123">100.90.70</span><span class="sxs-lookup"><span data-stu-id="8c541-123">100.90.70</span></span>

> [!WARNING]
> <span data-ttu-id="8c541-124">Lors de la mise à niveau du package installé à partir d’une version antérieure à la version 100.90.70, la mise à jour peut échouer sur les distributions Basées sur Red Hat et SLES.</span><span class="sxs-lookup"><span data-stu-id="8c541-124">When upgrading the installed package from a product version earlier than 100.90.70, the update may fail on Red Hat-based and SLES distributions.</span></span> <span data-ttu-id="8c541-125">Cela est dû à un changement majeur dans le chemin d’accès d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="8c541-125">This is because of a major change in a file path.</span></span> <span data-ttu-id="8c541-126">Une solution temporaire consiste à supprimer l’ancien package, puis à installer le nouveau.</span><span class="sxs-lookup"><span data-stu-id="8c541-126">A temporary solution is to remove the older package, and then install the newer one.</span></span> <span data-ttu-id="8c541-127">Ce problème n’existe pas dans les versions plus récentes.</span><span class="sxs-lookup"><span data-stu-id="8c541-127">This issue does not exist in newer versions.</span></span>

- <span data-ttu-id="8c541-128">Les [exclusions antivirus désormais prise en charge les caractères génériques](linux-exclusions.md#supported-exclusion-types)</span><span class="sxs-lookup"><span data-stu-id="8c541-128">Antivirus [exclusions now support wildcards](linux-exclusions.md#supported-exclusion-types)</span></span>
- <span data-ttu-id="8c541-129">Ajout de la possibilité de résoudre [les problèmes](linux-support-perf.md) de performances via l’outil en ligne `mdatp` de commande</span><span class="sxs-lookup"><span data-stu-id="8c541-129">Added the ability to [troubleshoot performance issues](linux-support-perf.md) through the `mdatp` command-line tool</span></span>
- <span data-ttu-id="8c541-130">Améliorations pour rendre l’installation du package plus robuste</span><span class="sxs-lookup"><span data-stu-id="8c541-130">Improvements to make the package installation more robust</span></span>
- <span data-ttu-id="8c541-131">Améliorations des performances & résolutions de bogues</span><span class="sxs-lookup"><span data-stu-id="8c541-131">Performance improvements & bug fixes</span></span>
