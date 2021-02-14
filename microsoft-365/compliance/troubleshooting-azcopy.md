---
title: Résoudre les problèmes d’AzCopy dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Résolution des erreurs pour Azure AzCopy lors du chargement de données autres qu’Office 365 pour la correction des erreurs dans Advanced eDiscovery.
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: 4a4499bb9790ffeaec6a2be36b5eaff030afc010
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546454"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a><span data-ttu-id="2a81e-103">Résoudre les problèmes d’AzCopy dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2a81e-103">Troubleshoot AzCopy in Advanced eDiscovery</span></span>

<span data-ttu-id="2a81e-104">Lors du chargement de données ou de documents non-Microsoft 365 pour la correction des erreurs dans Advanced eDiscovery, l’interface utilisateur fournit une commande Azure AzCopy qui contient des paramètres avec l’emplacement de stockage des fichiers que vous souhaitez télécharger et l’emplacement de stockage Azure vers lequel les fichiers seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="2a81e-104">When loading non-Microsoft 365 data or documents for error remediation in Advanced eDiscovery, the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="2a81e-105">Pour télécharger vos documents, copiez cette commande, puis exécutez-la dans une invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2a81e-105">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="2a81e-106">La capture d’écran ci-dessous montre un exemple de commande AzCopy :</span><span class="sxs-lookup"><span data-stu-id="2a81e-106">The follow screenshot shows an example of an AzCopy command:</span></span>

![Télécharger des fichiers autres que Microsoft 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="2a81e-108">En règle générale, la commande fournie fonctionne lorsque vous l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="2a81e-108">Usually the command that's provided works when you run it.</span></span> <span data-ttu-id="2a81e-109">Toutefois, dans certains cas, la commande affichée ne s’exécute pas correctement.</span><span class="sxs-lookup"><span data-stu-id="2a81e-109">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="2a81e-110">Voici quelques raisons possibles.</span><span class="sxs-lookup"><span data-stu-id="2a81e-110">Here's a few possible reasons.</span></span>

## <a name="the-supported-version-of-azcopy-isnt-installed-on-the-local-computer"></a><span data-ttu-id="2a81e-111">La version prise en charge d’AzCopy n’est pas installée sur l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="2a81e-111">The supported version of AzCopy isn't installed on the local computer</span></span>

<span data-ttu-id="2a81e-112">Pour l’instant, vous devez utiliser AzCopy v8.1 pour charger des données autres que Microsoft 365 dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="2a81e-112">At this time, you must use AzCopy v8.1 to load non-Microsoft 365 data in Advanced eDiscovery.</span></span> <span data-ttu-id="2a81e-113">La commande AzCopy qui s’affiche sur la **page** Télécharger les fichiers de la capture d’écran précédente renvoie une erreur si vous n’utilisez pas AzCopy v8.1.</span><span class="sxs-lookup"><span data-stu-id="2a81e-113">The AzCopy command that's displayed on the **Upload files** page shown in the previous screenshot returns an error if you're not using AzCopy v8.1.</span></span> <span data-ttu-id="2a81e-114">Pour installer cette version, voir Transférer des données [avec AzCopy v8.1 sur Windows.](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)</span><span class="sxs-lookup"><span data-stu-id="2a81e-114">To install this version, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="2a81e-115">AzCopy n’est pas installé sur l’ordinateur local ou n’est pas installé à l’emplacement par défaut</span><span class="sxs-lookup"><span data-stu-id="2a81e-115">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="2a81e-116">Si AzCopy n’est pas installé ou s’il est installé à un emplacement autre que l’emplacement d’installation par défaut (autrement dit), vous pouvez recevoir l’erreur suivante lorsque vous exécutez la commande `%ProgramFiles(x86)%` AzCopy :</span><span class="sxs-lookup"><span data-stu-id="2a81e-116">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

> <span data-ttu-id="2a81e-117">Le système ne peut pas trouver le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="2a81e-117">The system cannot find the path specified.</span></span>

<span data-ttu-id="2a81e-118">Si AzCopy n’est pas installé sur l’ordinateur local, vous pouvez trouver des informations d’installation dans Transférer des données avec [AzCopy v8.1 sur Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="2a81e-118">If AzCopy isn't installed on the local computer, you can find installation information in [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="2a81e-119">Assurez-vous de l’installer à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a81e-119">Be sure to install it in the default location.</span></span>

<span data-ttu-id="2a81e-120">Si AzCopy est installé, mais qu’il est installé à un emplacement différent de l’emplacement par défaut, vous pouvez copier la commande, la coller dans un fichier texte, puis modifier le chemin d’accès à l’emplacement où AzCopy est installé.</span><span class="sxs-lookup"><span data-stu-id="2a81e-120">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is installed.</span></span> <span data-ttu-id="2a81e-121">Par exemple, si Azcopy se trouve dans , vous pouvez modifier la première partie de la `%ProgramFiles%` commande de `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` .</span><span class="sxs-lookup"><span data-stu-id="2a81e-121">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="2a81e-122">Après avoir fait cette modification, copiez-la à partir du fichier texte, puis exécutez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="2a81e-122">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="2a81e-123">Si AzCopy est installé à un autre emplacement que l’emplacement d’installation par défaut, envisagez de le désinstaller, puis de le réinstaller à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a81e-123">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="2a81e-124">Cela permettra d’éviter ce problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="2a81e-124">This will help prevent this issue in the future.</span></span>
