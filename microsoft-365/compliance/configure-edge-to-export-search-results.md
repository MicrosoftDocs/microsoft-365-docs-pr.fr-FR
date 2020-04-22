---
title: Utiliser l’outil d’exportation de découverte électronique dans Microsoft Edge
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Vous devez activer la prise en charge de ClickOnce pour utiliser la dernière version de Microsoft Edge pour télécharger les résultats de recherche à partir de la recherche de contenu et eDiscovery dans le centre de sécurité et de conformité.
ms.openlocfilehash: c48e3fb04747306693364a2cdbc6f18047a0fd9e
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43632379"
---
# <a name="use-the-ediscovery-export-tool-in-microsoft-edge"></a><span data-ttu-id="d1f30-103">Utiliser l’outil d’exportation de découverte électronique dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1f30-103">Use the eDiscovery Export Tool in Microsoft Edge</span></span>

<span data-ttu-id="d1f30-104">En raison de modifications récentes apportées à la version la plus récente de Microsoft Edge, la prise en charge de ClickOnce n’est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1f30-104">As a result of recent changes to the newest version of Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="d1f30-105">Pour continuer à utiliser l’outil d’exportation de découverte électronique pour télécharger des résultats de recherche de contenu ou de recherche de découverte électronique, vous devez utiliser [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) ou activer la prise en charge ClickOnce dans la dernière version de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d1f30-105">To continue using the eDiscovery Export Tool to download Content Search or eDiscovery search results, you either need to use [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) or enable ClickOnce support in the newest version of Microsoft Edge.</span></span>

## <a name="enable-clickonce-support-in-microsoft-edge"></a><span data-ttu-id="d1f30-106">Activer la prise en charge ClickOnce dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1f30-106">Enable ClickOnce support in Microsoft Edge</span></span>

1. <span data-ttu-id="d1f30-107">Dans Microsoft Edge, accédez à **edge://flags/#edge-cliquez-une seule fois**.</span><span class="sxs-lookup"><span data-stu-id="d1f30-107">In Microsoft Edge, go to **edge://flags/#edge-click-once**.</span></span>

2. <span data-ttu-id="d1f30-108">Si la valeur existante est définie sur **default** ou **Disabled** dans la liste déroulante, remplacez-la par **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="d1f30-108">If the existing value is set to **Default** or **Disabled** in the dropdown list, change it to **Enabled**.</span></span>

   ![](../media/ClickOnceimage1.png)

3. <span data-ttu-id="d1f30-109">Faites défiler jusqu’au bas de la fenêtre du navigateur et cliquez sur **redémarrer** pour redémarrer le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="d1f30-109">Scroll down to the bottom of the browser window and click **Restart** to restart Edge.</span></span>

   ![](../media/ClickOnceimage2.png)

<span data-ttu-id="d1f30-110">**Remarque :** Les organisations peuvent utiliser la stratégie de groupe pour désactiver la prise en charge ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="d1f30-110">**Note:** Organizations can use Group Policy to disable ClickOnce support.</span></span> <span data-ttu-id="d1f30-111">Pour vérifier s’il existe une stratégie d’organisation pour la prise en charge de ClickOnce, accédez à **Edge://Policy**.</span><span class="sxs-lookup"><span data-stu-id="d1f30-111">To check if there is an organizational policy for ClickOnce support, go to **edge://policy**.</span></span> <span data-ttu-id="d1f30-112">La capture d’écran suivante montre que ClickOnce est activé dans l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d1f30-112">The following screenshot shows that ClickOnce is enabled across the entire organization.</span></span> <span data-ttu-id="d1f30-113">Si cette valeur de stratégie est définie sur **false**, vous devrez contacter un administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d1f30-113">If this policy value is set to **false**, you will need to contact an admin in your organization.</span></span>

![](../media/ClickOnceimage3.png)

## <a name="install-and-run-the-ediscovery-export-tool"></a><span data-ttu-id="d1f30-114">Installer et exécuter l’outil d’exportation eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d1f30-114">Install and run the eDiscovery Export Tool</span></span>

1. <span data-ttu-id="d1f30-115">Cliquez sur **Télécharger les résultats** sur la page de menu volant d’une recherche d’exportation dans le contenu ou de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="d1f30-115">Click **Download results** on the flyout page of an export in Content Search or an eDiscovery case.</span></span>

   ![Cliquez sur Télécharger les résultats sur la page de menu volant pour télécharger les résultats de la recherche.](../media/ClickOnceExport1.png)

2. <span data-ttu-id="d1f30-117">Vous serez invité à confirmer le lancement de l’outil, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="d1f30-117">You will be prompted with a confirmation to launch the tool, Click **Open**.</span></span>

   ![Cliquez sur Ouvrir pour lancer l’outil d’exportation de découverte électronique.](../media/ClickOnceimage4.png)

   <span data-ttu-id="d1f30-119">Si l’outil d’exportation de découverte électronique n’est pas installé, un message d’avertissement de sécurité s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d1f30-119">If the eDiscovery Export Tool isn't installed, you will be prompted with a Security Warning,</span></span> 

   ![Cliquez sur installer pour installer l’outil d’exportation de découverte électronique.](../media/ClickOnceimage5.png)

3. <span data-ttu-id="d1f30-121">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d1f30-121">Click **Install**.</span></span> <span data-ttu-id="d1f30-122">Une fois l’installation terminée, l’outil d’exportation se lance automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d1f30-122">After it's installed, the export tool will launch automatically.</span></span>

<span data-ttu-id="d1f30-123">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1f30-123">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d1f30-124">Exporter les résultats de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="d1f30-124">Export Content Search results</span></span>](export-search-results.md)

- [<span data-ttu-id="d1f30-125">Activation des indicateurs d’expérimentation dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1f30-125">How to enable experiment flags in Microsoft Edge</span></span>](https://microsoftedgesupport.microsoft.com/hc/articles/360034075294-How-to-enable-experiment-flags-in-Microsoft-Edge-Insider-channels)
