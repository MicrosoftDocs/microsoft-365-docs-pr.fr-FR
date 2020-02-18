---
title: Résolution des problèmes liés à AzCopy dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3153fc92cfae6e2feba122cc895e787c9b573ef7
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42080895"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a><span data-ttu-id="43c85-102">Résolution des problèmes liés à AzCopy dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="43c85-102">Troubleshoot AzCopy in Advanced eDiscovery</span></span>

<span data-ttu-id="43c85-103">Lors du chargement de données ou de documents autres que Office 365 pour la correction d’erreur dans Advanced eDiscovery, l’interface utilisateur fournit une commande AzCopy Azure qui contient les paramètres de l’emplacement où les fichiers que vous souhaitez télécharger sont stockés et le stockage Azure emplacement vers lequel les fichiers seront téléchargés.</span><span class="sxs-lookup"><span data-stu-id="43c85-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery, the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="43c85-104">Pour télécharger vos documents, copiez cette commande, puis exécutez-la dans une invite de commandes sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="43c85-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="43c85-105">La capture d’écran suivante illustre un exemple de commande AzCopy :</span><span class="sxs-lookup"><span data-stu-id="43c85-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Télécharger des fichiers non-Office 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="43c85-107">En règle générale, la commande fournie fonctionne lorsque vous l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="43c85-107">Usually the command that's provided works when you run it.</span></span> <span data-ttu-id="43c85-108">Toutefois, il peut arriver que la commande affichée ne s’exécute pas correctement.</span><span class="sxs-lookup"><span data-stu-id="43c85-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="43c85-109">Voici quelques raisons possibles.</span><span class="sxs-lookup"><span data-stu-id="43c85-109">Here's a few possible reasons.</span></span>

## <a name="the-supported-version-of-azcopy-isnt-installed-on-the-local-computer"></a><span data-ttu-id="43c85-110">La version prise en charge d’AzCopy n’est pas installée sur l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="43c85-110">The supported version of AzCopy isn't installed on the local computer</span></span>

<span data-ttu-id="43c85-111">Pour le moment, vous devez utiliser AzCopy v 8.1 pour charger des données autres que Office 365 dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="43c85-111">At this time, you must use AzCopy v8.1 to load non-Office 365 data in Advanced eDiscovery.</span></span> <span data-ttu-id="43c85-112">La commande AzCopy affichée sur la page **Télécharger les fichiers** indiquée dans la capture d’écran précédente renvoie une erreur si vous n’utilisez pas AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="43c85-112">The AzCopy command that's displayed on the **Upload files** page shown in the previous screenshot returns an error if you're not using AzCopy v8.1.</span></span> <span data-ttu-id="43c85-113">Pour installer cette version, voir [transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="43c85-113">To install this version, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="43c85-114">AzCopy n’est pas installé sur l’ordinateur local ou il n’est pas installé à l’emplacement par défaut</span><span class="sxs-lookup"><span data-stu-id="43c85-114">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="43c85-115">Si AzCopy n’est pas installé ou s’il est installé à un emplacement autre que l’emplacement d’installation `%ProgramFiles(x86)%`par défaut (c’est-à-dire), il se peut que vous receviez le message d’erreur suivant lorsque vous exécutez la commande AzCopy :</span><span class="sxs-lookup"><span data-stu-id="43c85-115">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="43c85-116">Si AzCopy n’est pas installé sur l’ordinateur local, vous pouvez procéder à l’installation à partir de [ici](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="43c85-116">If AzCopy isn't installed on the local computer, you can install from [here](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="43c85-117">Veillez à l’installer à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="43c85-117">Be sure to install it in the default location.</span></span>

<span data-ttu-id="43c85-118">Si AzCopy est installé, mais qu’il est installé à un emplacement différent de l’emplacement par défaut, vous pouvez copier la commande, la coller dans un fichier texte, puis modifier le chemin d’accès à l’emplacement où AzCopy est installé.</span><span class="sxs-lookup"><span data-stu-id="43c85-118">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is installed.</span></span> <span data-ttu-id="43c85-119">Par exemple, si Azcopy se trouve dans `%ProgramFiles%`, vous pouvez remplacer la première partie de la commande `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` par. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`</span><span class="sxs-lookup"><span data-stu-id="43c85-119">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="43c85-120">Une fois que vous avez effectué cette modification, copiez-la à partir du fichier texte, puis exécutez-la dans une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="43c85-120">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="43c85-121">Si AzCopy est installé à un emplacement autre que l’emplacement d’installation par défaut, envisagez de le désinstaller, puis de le réinstaller à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="43c85-121">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="43c85-122">Cela vous permettra d’éviter ce problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="43c85-122">This will help prevent this issue in the future.</span></span>
