---
title: Créer des indicateurs pour les fichiers
ms.reviewer: ''
description: Créez des indicateurs pour un hachage de fichier qui définit la détection, la prévention et l’exclusion des entités.
keywords: fichier, hachage, gérer, autorisé, bloqué, bloquer, nettoyer, malveillant, hachage de fichier, adresse IP, url, domaine
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 4edff7a9c7f541e31363519e4bafc2a21602e011
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067713"
---
# <a name="create-indicators-for-files"></a><span data-ttu-id="0bab0-104">Créer des indicateurs pour les fichiers</span><span class="sxs-lookup"><span data-stu-id="0bab0-104">Create indicators for files</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0bab0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0bab0-105">**Applies to:**</span></span>
- [<span data-ttu-id="0bab0-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0bab0-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="0bab0-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0bab0-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)



><span data-ttu-id="0bab0-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0bab0-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="0bab0-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0bab0-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-automationexclusionlist-abovefoldlink)

<span data-ttu-id="0bab0-110">Vous pouvez empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="0bab0-110">You can prevent further propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> <span data-ttu-id="0bab0-111">Si vous connaissez un fichier exécutable portable (PE) potentiellement malveillant, vous pouvez le bloquer.</span><span class="sxs-lookup"><span data-stu-id="0bab0-111">If you know a potentially malicious portable executable (PE) file, you can block it.</span></span> <span data-ttu-id="0bab0-112">Cette opération l’empêche d’être lue, écrite ou exécutée sur des ordinateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0bab0-112">This operation will prevent it from being read, written, or executed on machines in your organization.</span></span>

<span data-ttu-id="0bab0-113">Il existe deux façons de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="0bab0-113">There are two ways you can create indicators for files:</span></span>
- <span data-ttu-id="0bab0-114">En créant un indicateur via la page paramètres</span><span class="sxs-lookup"><span data-stu-id="0bab0-114">By creating an indicator through the settings page</span></span>
- <span data-ttu-id="0bab0-115">En créant un indicateur contextuel à l’aide du bouton Ajouter un indicateur à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="0bab0-115">By creating a contextual indicator using the add indicator button from the file details page</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="0bab0-116">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0bab0-116">Before you begin</span></span>
<span data-ttu-id="0bab0-117">Il est important de comprendre les conditions préalables suivantes avant de créer des indicateurs pour les fichiers :</span><span class="sxs-lookup"><span data-stu-id="0bab0-117">It's important to understand the following prerequisites prior to creating indicators for files:</span></span>

- <span data-ttu-id="0bab0-118">Cette fonctionnalité est disponible si votre organisation utilise Windows Defender antivirus et la protection basée sur le cloud est activée.</span><span class="sxs-lookup"><span data-stu-id="0bab0-118">This feature is available if your organization uses Windows Defender Antivirus and Cloud-based protection is enabled.</span></span> <span data-ttu-id="0bab0-119">Pour plus d’informations, voir Utiliser les technologies de nouvelle génération dans [l’Antivirus Microsoft Defender via](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/utilize-microsoft-cloud-protection-microsoft-defender-antivirus)la protection livrée par le cloud.</span><span class="sxs-lookup"><span data-stu-id="0bab0-119">For more information, see [Use next-generation technologies in Microsoft Defender Antivirus through cloud-delivered protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/utilize-microsoft-cloud-protection-microsoft-defender-antivirus).</span></span>
- <span data-ttu-id="0bab0-120">La version du client anti-programme malveillant doit être 4.18.1901.x ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0bab0-120">The Antimalware client version must be 4.18.1901.x or later.</span></span>
- <span data-ttu-id="0bab0-121">Pris en charge sur les ordinateurs sur Windows 10, version 1703 ou ultérieure, Windows Server 2016 et 2019.</span><span class="sxs-lookup"><span data-stu-id="0bab0-121">Supported on machines on Windows 10, version 1703 or later, Windows server 2016 and 2019.</span></span>
- <span data-ttu-id="0bab0-122">Pour commencer à bloquer les fichiers, vous devez d’abord activer la fonctionnalité Bloquer ou [autoriser dans  ](advanced-features.md) paramètres.</span><span class="sxs-lookup"><span data-stu-id="0bab0-122">To start blocking files, you first need to [turn the **Block or allow** feature on](advanced-features.md) in Settings.</span></span>
- <span data-ttu-id="0bab0-123">Cette fonctionnalité est conçue pour empêcher le téléchargement de programmes malveillants (ou de fichiers potentiellement malveillants) à partir du web.</span><span class="sxs-lookup"><span data-stu-id="0bab0-123">This feature is designed to prevent suspected malware (or potentially malicious files) from being downloaded from the web.</span></span> <span data-ttu-id="0bab0-124">Il prend actuellement en charge les fichiers exécutables portables (PE), y compris les fichiers _.exe_ et _.dll._</span><span class="sxs-lookup"><span data-stu-id="0bab0-124">It currently supports portable executable (PE) files, including _.exe_ and _.dll_ files.</span></span> <span data-ttu-id="0bab0-125">La couverture sera étendue au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="0bab0-125">The coverage will be extended over time.</span></span>

>[!IMPORTANT]
>- <span data-ttu-id="0bab0-126">La fonction autoriser ou bloquer ne peut pas être effectuée sur les fichiers si la classification du fichier existe sur le cache de l’appareil avant l’action autoriser ou bloquer</span><span class="sxs-lookup"><span data-stu-id="0bab0-126">The allow or block function cannot be done on files if the file's classification exists on the device's cache prior to the allow or block action</span></span> 
>- <span data-ttu-id="0bab0-127">Les fichiers signés fiables seront traités différemment.</span><span class="sxs-lookup"><span data-stu-id="0bab0-127">Trusted signed files will be treated differently.</span></span> <span data-ttu-id="0bab0-128">Defender for Endpoint est optimisé pour gérer les fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="0bab0-128">Defender for Endpoint is optimized to handle malicious files.</span></span> <span data-ttu-id="0bab0-129">Dans certains cas, la tentative de blocage des fichiers signés de confiance peut avoir des conséquences sur les performances.</span><span class="sxs-lookup"><span data-stu-id="0bab0-129">Trying to block trusted signed files, in some cases, may have performance implications.</span></span>

 
>[!NOTE]
><span data-ttu-id="0bab0-130">En règle générale, les blocs de fichiers sont appliqués en quelques minutes, mais peuvent prendre jusqu’à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="0bab0-130">Typically, file blocks are enforced within a couple of minutes, but can take upwards of 30 minutes.</span></span>

### <a name="create-an-indicator-for-files-from-the-settings-page"></a><span data-ttu-id="0bab0-131">Créer un indicateur pour les fichiers à partir de la page paramètres</span><span class="sxs-lookup"><span data-stu-id="0bab0-131">Create an indicator for files from the settings page</span></span>

1. <span data-ttu-id="0bab0-132">Dans le volet de navigation, sélectionnez **Indicateurs**  >  **de paramètres.**</span><span class="sxs-lookup"><span data-stu-id="0bab0-132">In the navigation pane, select **Settings** > **Indicators**.</span></span>  

2. <span data-ttu-id="0bab0-133">Sélectionnez **l’onglet hachage fichier.**</span><span class="sxs-lookup"><span data-stu-id="0bab0-133">Select the **File hash** tab.</span></span>

3. <span data-ttu-id="0bab0-134">Sélectionnez **Ajouter un indicateur**.</span><span class="sxs-lookup"><span data-stu-id="0bab0-134">Select **Add indicator**.</span></span>

4. <span data-ttu-id="0bab0-135">Spécifiez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="0bab0-135">Specify the following details:</span></span>
   - <span data-ttu-id="0bab0-136">Indicateur : spécifiez les détails de l’entité et définissez l’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="0bab0-136">Indicator - Specify the entity details and define the expiration of the indicator.</span></span>
   - <span data-ttu-id="0bab0-137">Action : spécifiez l’action à prendre et fournissez une description.</span><span class="sxs-lookup"><span data-stu-id="0bab0-137">Action - Specify the action to be taken and provide a description.</span></span>
   - <span data-ttu-id="0bab0-138">Étendue : définir l’étendue du groupe d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="0bab0-138">Scope - Define the scope of the machine group.</span></span>

5. <span data-ttu-id="0bab0-139">Consultez les détails de l’onglet Résumé, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0bab0-139">Review the details in the Summary tab, then click **Save**.</span></span>

### <a name="create-a-contextual-indicator-from-the-file-details-page"></a><span data-ttu-id="0bab0-140">Créer un indicateur contextuel à partir de la page de détails du fichier</span><span class="sxs-lookup"><span data-stu-id="0bab0-140">Create a contextual indicator from the file details page</span></span>
<span data-ttu-id="0bab0-141">L’une des options lorsque vous prenez des mesures de réponse sur un [fichier consiste](respond-file-alerts.md) à ajouter un indicateur pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="0bab0-141">One of the options when taking [response actions on a file](respond-file-alerts.md) is adding an indicator for the file.</span></span> 

<span data-ttu-id="0bab0-142">Lorsque vous ajoutez un hachage d’indicateur pour un fichier, vous pouvez choisir de lancer une alerte et de bloquer le fichier chaque fois qu’un ordinateur de votre organisation tente de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0bab0-142">When you add an indicator hash for a file, you can choose to raise an alert and block the file whenever a machine in your organization attempts to run it.</span></span>

<span data-ttu-id="0bab0-143">Les fichiers automatiquement bloqués par un indicateur ne s’afficheront pas dans le centre de l’action du fichier, mais les alertes resteront visibles dans la file d’attente des alertes.</span><span class="sxs-lookup"><span data-stu-id="0bab0-143">Files automatically blocked by an indicator won't show up in the file's Action center, but the alerts will still be visible in the Alerts queue.</span></span>


## <a name="related-topics"></a><span data-ttu-id="0bab0-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bab0-144">Related topics</span></span>
- [<span data-ttu-id="0bab0-145">Créer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="0bab0-145">Create indicators</span></span>](manage-indicators.md)
- [<span data-ttu-id="0bab0-146">Créer des indicateurs pour les adresses IP et les URL/domaines</span><span class="sxs-lookup"><span data-stu-id="0bab0-146">Create indicators for IPs and URLs/domains</span></span>](indicator-ip-domain.md)
- [<span data-ttu-id="0bab0-147">Créer des indicateurs basés sur des certificats</span><span class="sxs-lookup"><span data-stu-id="0bab0-147">Create indicators based on certificates</span></span>](indicator-certificates.md)
- [<span data-ttu-id="0bab0-148">Gérer les indicateurs</span><span class="sxs-lookup"><span data-stu-id="0bab0-148">Manage indicators</span></span>](indicator-manage.md)
