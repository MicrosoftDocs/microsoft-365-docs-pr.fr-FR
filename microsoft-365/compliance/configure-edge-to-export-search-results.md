---
title: Utiliser l’outil d’exportation eDiscovery dans Microsoft Edge
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Vous devez activer la prise en charge ClickOnce pour utiliser la dernière version de Microsoft Edge afin de télécharger les résultats de recherche à partir de la recherche de contenu et de la découverte électronique dans le centre de sécurité et conformité.
ms.openlocfilehash: 60f42d2884c56aaff40bc0a6a979e99698a3cd2e
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47546818"
---
# <a name="use-the-ediscovery-export-tool-in-microsoft-edge"></a><span data-ttu-id="d4568-103">Utiliser l’outil d’exportation eDiscovery dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4568-103">Use the eDiscovery Export Tool in Microsoft Edge</span></span>

<span data-ttu-id="d4568-104">Suite aux modifications récentes apportées à la dernière version de Microsoft Edge, la prise en charge ClickOnce’est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4568-104">As a result of recent changes to the newest version of Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="d4568-105">Pour continuer à utiliser l’outil d’exportation eDiscovery pour télécharger les résultats de recherche de contenu ou de découverte électronique, vous devez utiliser [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) ou activer la prise en charge de ClickOnce dans la dernière version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d4568-105">To continue using the eDiscovery Export Tool to download Content Search or eDiscovery search results, you either need to use [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) or enable ClickOnce support in the newest version of Microsoft Edge.</span></span>

## <a name="enable-clickonce-support-in-microsoft-edge"></a><span data-ttu-id="d4568-106">Activer ClickOnce prise en charge dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4568-106">Enable ClickOnce support in Microsoft Edge</span></span>

1. <span data-ttu-id="d4568-107">Dans Microsoft Edge, allez à **edge://flags/#edge-click-once**.</span><span class="sxs-lookup"><span data-stu-id="d4568-107">In Microsoft Edge, go to **edge://flags/#edge-click-once**.</span></span>

2. <span data-ttu-id="d4568-108">Si la valeur existante est définie sur **Default** ou **Disabled** dans la liste liste, changez-la **en Activé.**</span><span class="sxs-lookup"><span data-stu-id="d4568-108">If the existing value is set to **Default** or **Disabled** in the dropdown list, change it to **Enabled**.</span></span>

   ![Select Enabled from dropdown list](../media/ClickOnceimage1.png)

3. <span data-ttu-id="d4568-110">Faites défiler vers le bas jusqu’au bas de la fenêtre du navigateur, puis cliquez sur **Redémarrer** pour redémarrer Edge.</span><span class="sxs-lookup"><span data-stu-id="d4568-110">Scroll down to the bottom of the browser window and click **Restart** to restart Edge.</span></span>

   ![Cliquez sur Redémarrer](../media/ClickOnceimage2.png)

<span data-ttu-id="d4568-112">**Remarque :** Les organisations peuvent utiliser la stratégie de groupe pour désactiver ClickOnce prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d4568-112">**Note:** Organizations can use Group Policy to disable ClickOnce support.</span></span> <span data-ttu-id="d4568-113">Pour vérifier s’il existe une stratégie d’organisation ClickOnce prise en charge, edge://policy **.**</span><span class="sxs-lookup"><span data-stu-id="d4568-113">To check if there is an organizational policy for ClickOnce support, go to **edge://policy**.</span></span> <span data-ttu-id="d4568-114">La capture d’écran suivante montre que ClickOnce est activé dans toute l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d4568-114">The following screenshot shows that ClickOnce is enabled across the entire organization.</span></span> <span data-ttu-id="d4568-115">Si cette valeur de stratégie est définie sur **False,** vous devez contacter un administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d4568-115">If this policy value is set to **false**, you will need to contact an admin in your organization.</span></span>

![Liste des stratégies d’organisation Edge](../media/ClickOnceimage3.png)

## <a name="install-and-run-the-ediscovery-export-tool"></a><span data-ttu-id="d4568-117">Installer et exécuter l’outil d’exportation eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d4568-117">Install and run the eDiscovery Export Tool</span></span>

1. <span data-ttu-id="d4568-118">Cliquez **sur Télécharger les résultats** sur la page volante d’une exportation dans la recherche de contenu ou un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d4568-118">Click **Download results** on the flyout page of an export in Content Search or an eDiscovery case.</span></span>

   ![Cliquez sur Télécharger les résultats sur la page volante pour télécharger les résultats de la recherche](../media/ClickOnceExport1.png)

2. <span data-ttu-id="d4568-120">Vous serez invité à confirmer le lancement de l’outil, cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="d4568-120">You will be prompted with a confirmation to launch the tool, Click **Open**.</span></span>

   ![Cliquez sur Ouvrir pour lancer l’outil d’exportation eDiscovery](../media/ClickOnceimage4.png)

   <span data-ttu-id="d4568-122">Si l’outil d’exportation eDiscovery n’est pas installé, un avertissement de sécurité vous est demandé.</span><span class="sxs-lookup"><span data-stu-id="d4568-122">If the eDiscovery Export Tool isn't installed, you will be prompted with a Security Warning,</span></span> 

   ![Cliquez sur Installer pour installer l’outil d’exportation eDiscovery](../media/ClickOnceimage5.png)

3. <span data-ttu-id="d4568-124">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d4568-124">Click **Install**.</span></span> <span data-ttu-id="d4568-125">Une fois installé, l’outil d’exportation se lance automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d4568-125">After it's installed, the export tool will launch automatically.</span></span>

<span data-ttu-id="d4568-126">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4568-126">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d4568-127">Exporter les résultats de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="d4568-127">Export Content Search results</span></span>](export-search-results.md)

- [<span data-ttu-id="d4568-128">Comment activer les indicateurs d’expérience dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d4568-128">How to enable experiment flags in Microsoft Edge</span></span>](https://microsoftedgesupport.microsoft.com/hc/articles/360034075294-How-to-enable-experiment-flags-in-Microsoft-Edge-Insider-channels)
