---
title: Résolution des problèmes liés à AzCopy dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: troubleshooting
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Résoudre les erreurs liées à Azure AzCopy lors du chargement de données non Office 365 pour la correction d’erreur dans Advanced eDiscovery.
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: 4bf8461cb02ca3601707f248a64d8a8a9741efab
ms.sourcegitcommit: 9ce9001aa41172152458da27c1c52825355f426d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2020
ms.locfileid: "47357704"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a><span data-ttu-id="dd9cb-103">Résolution des problèmes liés à AzCopy dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="dd9cb-103">Troubleshoot AzCopy in Advanced eDiscovery</span></span>

<span data-ttu-id="dd9cb-104">Lors du chargement de données ou de documents non-Microsoft 365 pour la correction d’erreur dans Advanced eDiscovery, l’interface utilisateur fournit une commande AzCopy Azure qui contient les paramètres de l’emplacement où les fichiers que vous souhaitez télécharger sont stockés et l’emplacement de stockage Azure dans lequel les fichiers seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-104">When loading non-Microsoft 365 data or documents for error remediation in Advanced eDiscovery, the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="dd9cb-105">Pour télécharger vos documents, copiez cette commande, puis exécutez-la dans une invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-105">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="dd9cb-106">La capture d’écran suivante illustre un exemple de commande AzCopy :</span><span class="sxs-lookup"><span data-stu-id="dd9cb-106">The follow screenshot shows an example of an AzCopy command:</span></span>

![Télécharger des fichiers non-Microsoft 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="dd9cb-108">En règle générale, la commande fournie fonctionne lorsque vous l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-108">Usually the command that's provided works when you run it.</span></span> <span data-ttu-id="dd9cb-109">Toutefois, il peut arriver que la commande affichée ne s’exécute pas correctement.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-109">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="dd9cb-110">Voici quelques raisons possibles.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-110">Here's a few possible reasons.</span></span>

## <a name="the-supported-version-of-azcopy-isnt-installed-on-the-local-computer"></a><span data-ttu-id="dd9cb-111">La version prise en charge d’AzCopy n’est pas installée sur l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="dd9cb-111">The supported version of AzCopy isn't installed on the local computer</span></span>

<span data-ttu-id="dd9cb-112">Pour le moment, vous devez utiliser AzCopy v 8.1 pour charger des données non-Microsoft 365 dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-112">At this time, you must use AzCopy v8.1 to load non-Microsoft 365 data in Advanced eDiscovery.</span></span> <span data-ttu-id="dd9cb-113">La commande AzCopy affichée sur la page **Télécharger les fichiers** indiquée dans la capture d’écran précédente renvoie une erreur si vous n’utilisez pas AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-113">The AzCopy command that's displayed on the **Upload files** page shown in the previous screenshot returns an error if you're not using AzCopy v8.1.</span></span> <span data-ttu-id="dd9cb-114">Pour installer cette version, voir [transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="dd9cb-114">To install this version, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="dd9cb-115">AzCopy n’est pas installé sur l’ordinateur local ou il n’est pas installé à l’emplacement par défaut</span><span class="sxs-lookup"><span data-stu-id="dd9cb-115">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="dd9cb-116">Si AzCopy n’est pas installé ou s’il est installé à un emplacement autre que l’emplacement d’installation par défaut (c’est-à-dire `%ProgramFiles(x86)%` ), il se peut que vous receviez le message d’erreur suivant lorsque vous exécutez la commande AzCopy :</span><span class="sxs-lookup"><span data-stu-id="dd9cb-116">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

> <span data-ttu-id="dd9cb-117">Le système ne peut pas trouver le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-117">The system cannot find the path specified.</span></span>

<span data-ttu-id="dd9cb-118">Si AzCopy n’est pas installé sur l’ordinateur local, vous pouvez trouver des informations relatives à l’installation dans [le transfert de données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="dd9cb-118">If AzCopy isn't installed on the local computer, you can find installation information in [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="dd9cb-119">Veillez à l’installer à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-119">Be sure to install it in the default location.</span></span>

<span data-ttu-id="dd9cb-120">Si AzCopy est installé, mais qu’il est installé à un emplacement différent de l’emplacement par défaut, vous pouvez copier la commande, la coller dans un fichier texte, puis modifier le chemin d’accès à l’emplacement où AzCopy est installé.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-120">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is installed.</span></span> <span data-ttu-id="dd9cb-121">Par exemple, si Azcopy se trouve dans `%ProgramFiles%` , vous pouvez remplacer la première partie de la commande par `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` .</span><span class="sxs-lookup"><span data-stu-id="dd9cb-121">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="dd9cb-122">Une fois que vous avez effectué cette modification, copiez-la à partir du fichier texte, puis exécutez-la dans une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-122">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="dd9cb-123">Si AzCopy est installé à un emplacement autre que l’emplacement d’installation par défaut, envisagez de le désinstaller, puis de le réinstaller à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-123">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="dd9cb-124">Cela vous permettra d’éviter ce problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="dd9cb-124">This will help prevent this issue in the future.</span></span>
