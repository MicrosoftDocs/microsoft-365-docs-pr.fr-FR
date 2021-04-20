---
title: Collecter les journaux de support dans Microsoft Defender pour les points de terminaison à l'aide de la réponse en direct
description: Découvrez comment collecter des journaux à l'aide d'une réponse en direct pour résoudre les problèmes de Microsoft Defender pour les points de terminaison
keywords: support, journal, collecter, dépanner, réponse en direct, liveanalyzer, analyseur, en direct, réponse
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
ms.topic: troubleshooting
ms.technology: mde
ms.openlocfilehash: 07593fac6ed9a3fbc00d904718380b386f31dba3
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893412"
---
# <a name="collect-support-logs-in-microsoft-defender-for-endpoint-using-live-response"></a><span data-ttu-id="0a490-104">Collecter les journaux de support dans Microsoft Defender pour le point de terminaison à l'aide d'une réponse en direct</span><span class="sxs-lookup"><span data-stu-id="0a490-104">Collect support logs in Microsoft Defender for Endpoint using live response</span></span> 


<span data-ttu-id="0a490-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0a490-105">**Applies to:**</span></span>
- [<span data-ttu-id="0a490-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0a490-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="0a490-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0a490-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="0a490-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0a490-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="0a490-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0a490-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


<span data-ttu-id="0a490-110">Lorsque vous contactez le support technique, vous pouvez être invité à fournir le package de sortie de l'outil Microsoft Defender for Endpoint Client Analyzer.</span><span class="sxs-lookup"><span data-stu-id="0a490-110">When contacting support, you may be asked to provide the output package of the Microsoft Defender for Endpoint Client Analyzer tool.</span></span>

<span data-ttu-id="0a490-111">Cette rubrique fournit des instructions sur la façon d'exécuter l'outil via Live Response.</span><span class="sxs-lookup"><span data-stu-id="0a490-111">This topic provides instructions on how to run the tool via Live Response.</span></span>

1. <span data-ttu-id="0a490-112">Télécharger le script approprié</span><span class="sxs-lookup"><span data-stu-id="0a490-112">Download the appropriate script</span></span>
    * <span data-ttu-id="0a490-113">Journaux de capteur client Microsoft Defender pour point de terminaison uniquement : [LiveAnalyzer.ps1 script](https://aka.ms/MDELiveAnalyzer).</span><span class="sxs-lookup"><span data-stu-id="0a490-113">Microsoft Defender for Endpoint client sensor logs only: [LiveAnalyzer.ps1 script](https://aka.ms/MDELiveAnalyzer).</span></span>
      - <span data-ttu-id="0a490-114">Taille approximative du package de résultats : ~100Kb</span><span class="sxs-lookup"><span data-stu-id="0a490-114">Result package approximate size: ~100Kb</span></span> 
    *  <span data-ttu-id="0a490-115">Capteur client microsoft Defender pour point de terminaison et journaux antivirus : [LiveAnalyzer+MDAV.ps1 script](https://aka.ms/MDELiveAnalyzerAV).</span><span class="sxs-lookup"><span data-stu-id="0a490-115">Microsoft Defender for Endpoint client sensor and Antivirus logs: [LiveAnalyzer+MDAV.ps1 script](https://aka.ms/MDELiveAnalyzerAV).</span></span>
       - <span data-ttu-id="0a490-116">Taille approximative du package de résultats : ~10 Mo</span><span class="sxs-lookup"><span data-stu-id="0a490-116">Result package approximate size: ~10Mb</span></span> 
 
2.  <span data-ttu-id="0a490-117">Lancez [une session Live Response](live-response.md#initiate-a-live-response-session-on-a-device) sur l'ordinateur que vous devez examiner.</span><span class="sxs-lookup"><span data-stu-id="0a490-117">Initiate a [Live Response session](live-response.md#initiate-a-live-response-session-on-a-device) on the machine you need to investigate.</span></span>

3.  <span data-ttu-id="0a490-118">Sélectionnez **Télécharger le fichier dans la bibliothèque.**</span><span class="sxs-lookup"><span data-stu-id="0a490-118">Select **Upload file to library**.</span></span>

    ![Image du fichier de téléchargement](images/upload-file.png)

4. <span data-ttu-id="0a490-120">Sélectionnez **Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="0a490-120">Select **Choose file**.</span></span>

    ![Image du bouton Choisir un fichier1](images/choose-file.png)

5. <span data-ttu-id="0a490-122">Sélectionnez le fichier téléchargé nommé MDELiveAnalyzer.ps1 puis cliquez sur **Confirmer**</span><span class="sxs-lookup"><span data-stu-id="0a490-122">Select the downloaded file named MDELiveAnalyzer.ps1 and then click on **Confirm**</span></span>


   ![Image de choisir le bouton2 du fichier](images/analyzer-file.png)


6. <span data-ttu-id="0a490-124">Pendant la session LiveResponse, utilisez les commandes ci-dessous pour exécuter l'analyseur et collecter le fichier de résultats :</span><span class="sxs-lookup"><span data-stu-id="0a490-124">While still in the LiveResponse session, use the commands below to run the analyzer and collect the result file:</span></span>

    ```console
    Run MDELiveAnalyzer.ps1
    GetFile "C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\MDEClientAnalyzerResult.zip" -auto
    ```

    <span data-ttu-id="0a490-125">[![Image des commandes ](images/analyzer-commands.png)](images/analyzer-commands.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0a490-125">[ ![Image of commands](images/analyzer-commands.png) ](images/analyzer-commands.png#lightbox)</span></span>


>[!NOTE]
> - <span data-ttu-id="0a490-126">La dernière version d'aperçu de MDEClientAnalyzer peut être téléchargée ici [https://aka.ms/Betamdeanalyzer](https://aka.ms/Betamdeanalyzer) :</span><span class="sxs-lookup"><span data-stu-id="0a490-126">The latest preview version of MDEClientAnalyzer can be downloaded here: [https://aka.ms/Betamdeanalyzer](https://aka.ms/Betamdeanalyzer).</span></span>
> 
> - <span data-ttu-id="0a490-127">Le script LiveAnalyzer télécharge le package de dépannage sur l'ordinateur de destination à partir https://mdatpclientanalyzer.blob.core.windows.net de :</span><span class="sxs-lookup"><span data-stu-id="0a490-127">The LiveAnalyzer script downloads the troubleshooting package on the destination machine from: https://mdatpclientanalyzer.blob.core.windows.net.</span></span>
> 
>   <span data-ttu-id="0a490-128">Si vous ne pouvez pas autoriser l'ordinateur à atteindre l'URL ci-dessus, téléchargez MDEClientAnalyzerPreview.zip fichier dans la bibliothèque avant d'exécutez le script LiveAnalyzer :</span><span class="sxs-lookup"><span data-stu-id="0a490-128">If you cannot allow the machine to reach the above URL, then upload MDEClientAnalyzerPreview.zip file to the library before running the LiveAnalyzer script:</span></span>
>
>   ```console
>   PutFile MDEClientAnalyzerPreview.zip -overwrite
>   Run MDELiveAnalyzer.ps1
>   GetFile "C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection\Downloads\MDEClientAnalyzerResult.zip" -auto
>   ```
> 
> - <span data-ttu-id="0a490-129">Pour plus d'informations sur la collecte de données localement sur un ordinateur au cas où l'ordinateur ne communique pas avec Microsoft Defender pour les services cloud de point de terminaison ou n'apparaît pas dans le portail Microsoft Defender pour point de terminaison comme prévu, voir Vérifier la connectivité du client à [Microsoft Defender pour](configure-proxy-internet.md#verify-client-connectivity-to-microsoft-defender-for-endpoint-service-urls)les URL de service De point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0a490-129">For more information on gathering data locally on a machine in case the machine isn't communicating with Microsoft Defender for Endpoint cloud services, or does not appear in Microsoft Defender for Endpoint portal as expected, see [Verify client connectivity to Microsoft Defender for Endpoint service URLs](configure-proxy-internet.md#verify-client-connectivity-to-microsoft-defender-for-endpoint-service-urls).</span></span>
