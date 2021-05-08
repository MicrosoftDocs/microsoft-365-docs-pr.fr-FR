---
title: Collecter des données de diagnostic pour la conformité des mises à jour et les Windows Defender Antivirus Microsoft Defender
description: Utiliser un outil pour collecter des données afin de résoudre les problèmes de conformité des mises à jour lors de l’utilisation du Antivirus Microsoft Defender’évaluation
keywords: résoudre les problèmes, erreur, corriger, mettre à jour la conformité, oms, surveiller, signaler, Microsoft Defender AV
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 2aaf3d1c650713a7f6cfb7b9abb9f2232013d6db
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274795"
---
# <a name="collect-update-compliance-diagnostic-data-for-microsoft-defender-av-assessment"></a><span data-ttu-id="f5f64-104">Collecter les données de diagnostic de conformité des mises à jour pour l’évaluation de Microsoft Defender AV</span><span class="sxs-lookup"><span data-stu-id="f5f64-104">Collect Update Compliance diagnostic data for Microsoft Defender AV Assessment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f5f64-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f5f64-105">**Applies to:**</span></span>

- [<span data-ttu-id="f5f64-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f5f64-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="f5f64-107">Cet article explique comment collecter des données de diagnostic qui peuvent être utilisées par le support microsoft et les équipes d’ingénierie pour vous aider à résoudre les problèmes que vous pouvez rencontrer lors de l’utilisation de la section Évaluation de l’Antivirus Microsoft Defender dans le module de conformité des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f5f64-107">This article describes how to collect diagnostic data that can be used by Microsoft support and engineering teams to help troubleshoot issues you may encounter when using the Microsoft Defender AV Assessment section in the Update Compliance add-in.</span></span>

<span data-ttu-id="f5f64-108">Avant d’essayer ce processus, assurez-vous que vous avez lu résolution des problèmes Antivirus Microsoft Defender [rapports,](troubleshoot-reporting.md)satisfait à toutes les conditions préalables requises et pris les autres suggestions de procédures de dépannage.</span><span class="sxs-lookup"><span data-stu-id="f5f64-108">Before attempting this process, ensure you have read [Troubleshoot Microsoft Defender Antivirus reporting](troubleshoot-reporting.md), met all require prerequisites, and taken any other suggested troubleshooting steps.</span></span>

<span data-ttu-id="f5f64-109">Sur au moins deux appareils qui ne sont pas signalés ou qui s’affichent dans Update Compliance, obtenez le fichier de diagnostic .cab en suivant les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="f5f64-109">On at least two devices that are not reporting or showing up in Update Compliance, obtain the .cab diagnostic file by taking the following steps:</span></span>

1. <span data-ttu-id="f5f64-110">Ouvrez une version de niveau administrateur de l’invite de commandes comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5f64-110">Open an administrator-level version of the command prompt as follows:</span></span>
        
    <span data-ttu-id="f5f64-111">a.</span><span class="sxs-lookup"><span data-stu-id="f5f64-111">a.</span></span> <span data-ttu-id="f5f64-112">Ouvrez **le** menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="f5f64-112">Open the **Start** menu.</span></span>

    <span data-ttu-id="f5f64-113">b.</span><span class="sxs-lookup"><span data-stu-id="f5f64-113">b.</span></span> <span data-ttu-id="f5f64-114">Tapez **cmd**.</span><span class="sxs-lookup"><span data-stu-id="f5f64-114">Type **cmd**.</span></span> <span data-ttu-id="f5f64-115">Cliquez avec le bouton droit sur **l’invite de commandes,** puis cliquez **sur Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="f5f64-115">Right-click on **Command Prompt** and click **Run as administrator**.</span></span>

    <span data-ttu-id="f5f64-116">c.</span><span class="sxs-lookup"><span data-stu-id="f5f64-116">c.</span></span> <span data-ttu-id="f5f64-117">Entrez les informations d’identification de l’administrateur ou approuvez l’invite.</span><span class="sxs-lookup"><span data-stu-id="f5f64-117">Enter administrator credentials or approve the prompt.</span></span>
        
2. <span data-ttu-id="f5f64-118">Accédez au répertoire Windows Defender’annuaire.</span><span class="sxs-lookup"><span data-stu-id="f5f64-118">Navigate to the Windows Defender directory.</span></span> <span data-ttu-id="f5f64-119">Par défaut, cette valeur est `C:\Program Files\Windows Defender`.</span><span class="sxs-lookup"><span data-stu-id="f5f64-119">By default, this is `C:\Program Files\Windows Defender`.</span></span>

3. <span data-ttu-id="f5f64-120">Tapez la commande suivante, puis appuyez sur **Entrée**</span><span class="sxs-lookup"><span data-stu-id="f5f64-120">Type the following command, and then press **Enter**</span></span>
        
    ```Dos
    mpcmdrun -getfiles
    ```
    
4. <span data-ttu-id="f5f64-121">Un .cab de diagnostic qui contient divers journaux de diagnostic est généré.</span><span class="sxs-lookup"><span data-stu-id="f5f64-121">A .cab file will be generated that contains various diagnostic logs.</span></span> <span data-ttu-id="f5f64-122">L’emplacement du fichier est spécifié dans la sortie de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="f5f64-122">The location of the file will be specified in the output in the command prompt.</span></span> <span data-ttu-id="f5f64-123">Par défaut, l’emplacement est `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab` .</span><span class="sxs-lookup"><span data-stu-id="f5f64-123">By default, the location is `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab`.</span></span>

5. <span data-ttu-id="f5f64-124">Copiez ces .cab vers un emplacement accessible par le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5f64-124">Copy these .cab files to a location that can be accessed by Microsoft support.</span></span> <span data-ttu-id="f5f64-125">Par exemple, il peut s’agit d’un dossier OneDrive protégé par mot de passe que vous pouvez partager avec nous.</span><span class="sxs-lookup"><span data-stu-id="f5f64-125">An example could be a password-protected OneDrive folder that you can share with us.</span></span>

6. <span data-ttu-id="f5f64-126">Envoyez un courrier <a href="mailto:ucsupport@microsoft.com?subject=WDAV assessment issue&body=I%20am%20encountering%20the%20following%20issue%20when%20using%20Windows%20Defender%20AV%20in%20Update%20Compliance%3a%20%0d%0aI%20have%20provided%20at%20least%202%20support%20.cab%20files%20at%20the%20following%20location%3a%20%3Caccessible%20share%2c%20including%20access%20details%20such%20as%20password%3E%0d%0aMy%20OMS%20workspace%20ID%20is%3a%20%0d%0aPlease%20contact%20me%20at%3a"></a>électronique à l’aide du modèle de courrier électronique de prise en charge de la conformité des mises à jour et remplissez le modèle avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5f64-126">Send an email using the <a href="mailto:ucsupport@microsoft.com?subject=WDAV assessment issue&body=I%20am%20encountering%20the%20following%20issue%20when%20using%20Windows%20Defender%20AV%20in%20Update%20Compliance%3a%20%0d%0aI%20have%20provided%20at%20least%202%20support%20.cab%20files%20at%20the%20following%20location%3a%20%3Caccessible%20share%2c%20including%20access%20details%20such%20as%20password%3E%0d%0aMy%20OMS%20workspace%20ID%20is%3a%20%0d%0aPlease%20contact%20me%20at%3a">Update Compliance support email template</a>, and fill out the template with the following information:</span></span>
  
    ```
    I am encountering the following issue when using Microsoft Defender Antivirus in Update Compliance:
    
    I have provided at least 2 support .cab files at the following location: <accessible share, including access details such as password>

    My OMS workspace ID is:

    Please contact me at:
    ```

## <a name="see-also"></a><span data-ttu-id="f5f64-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5f64-127">See also</span></span>

- [<span data-ttu-id="f5f64-128">Résoudre les problèmes de Windows Defender Antivirus Microsoft Defender rapports</span><span class="sxs-lookup"><span data-stu-id="f5f64-128">Troubleshoot Windows Defender Microsoft Defender Antivirus reporting</span></span>](troubleshoot-reporting.md)