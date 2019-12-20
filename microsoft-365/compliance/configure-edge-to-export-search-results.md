---
title: Utiliser l’outil d’exportation eDiscovery d’Office 365 dans Microsoft Edge
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: Vous devez activer la prise en charge de ClickOnce pour utiliser Microsoft Edge pour exporter les résultats de recherche de la recherche de contenu et eDiscovery dans le centre de sécurité et de conformité.
ms.openlocfilehash: f3e0442fe349aa3364594e07873b229f3205fb5e
ms.sourcegitcommit: d656fd58e5491cfb7fee16b55dc7a58904ed128d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2019
ms.locfileid: "39891125"
---
# <a name="use-the-office-365-ediscovery-export-tool-in-microsoft-edge"></a><span data-ttu-id="c9d05-103">Utiliser l’outil d’exportation eDiscovery d’Office 365 dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c9d05-103">Use the Office 365 eDiscovery Export Tool in Microsoft Edge</span></span>

<span data-ttu-id="c9d05-104">Suite à des modifications récentes apportées à Microsoft Edge, la prise en charge de ClickOnce n’est plus activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9d05-104">As a result of recent changes to Microsoft Edge, ClickOnce support is no longer enabled by default.</span></span> <span data-ttu-id="c9d05-105">Pour continuer à utiliser l’outil d’exportation de découverte électronique Microsoft Office 365 pour télécharger des résultats de recherche de contenu ou de découverte électronique, vous devez utiliser [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) ou activer la prise en charge ClickOnce dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9d05-105">To continue using the Microsoft Office 365 eDiscovery Export Tool to download Content Search or eDiscovery search results, you either need to use [Microsoft Internet Explorer](https://support.microsoft.com/help/17621/internet-explorer-downloads) or enable ClickOnce support in Microsoft Edge.</span></span>

## <a name="how-to-enable-clickonce-support-in-microsoft-edge"></a><span data-ttu-id="c9d05-106">Activation de la prise en charge de ClickOnce dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c9d05-106">How to enable ClickOnce support in Microsoft Edge</span></span>

1. <span data-ttu-id="c9d05-107">Dans Microsoft Edge, accédez à **edge://flags/#edge-cliquez-une seule fois**.</span><span class="sxs-lookup"><span data-stu-id="c9d05-107">In Microsoft Edge, navigate to **edge://flags/#edge-click-once**.</span></span>

2. <span data-ttu-id="c9d05-108">Si la valeur existante est définie sur **default** ou **Disabled** dans la liste déroulante, remplacez-la par **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="c9d05-108">If the existing value is set to **Default** or **Disabled** in the dropdown list, change it to **Enabled**.</span></span>
    
   ![](media/ClickOnceimage1.png)

3. <span data-ttu-id="c9d05-109">Faites défiler jusqu’au bas de la fenêtre du navigateur et cliquez sur **redémarrer** pour redémarrer le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="c9d05-109">Scroll down to the bottom of the browser window and click **Restart** to restart Edge.</span></span>

   ![](media/ClickOnceimage2.png)

<span data-ttu-id="c9d05-110">**Remarque :** Les organisations peuvent utiliser la stratégie de groupe pour désactiver la prise en charge ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="c9d05-110">**Note:** Organizations can use Group Policy to disable ClickOnce support.</span></span> <span data-ttu-id="c9d05-111">Pour vérifier s’il existe une stratégie d’organisation pour la prise en charge de ClickOnce, accédez à **Edge://Policy**.</span><span class="sxs-lookup"><span data-stu-id="c9d05-111">To check if there is an organizational policy for ClickOnce support, navigate to **edge://policy**.</span></span> <span data-ttu-id="c9d05-112">La capture d’écran suivante montre que ClickOnce est activé dans l’ensemble de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c9d05-112">The following screenshot shows that ClickOnce is enabled across the entire organization.</span></span> <span data-ttu-id="c9d05-113">Si cette valeur de stratégie est définie sur **false**, vous devrez contacter un administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c9d05-113">If this policy value is set to **false**, you will need to contact an admin in your organization.</span></span>

![](media/ClickOnceimage3.png)

## <a name="install-and-run-the-office-365-ediscovery-export-tool"></a><span data-ttu-id="c9d05-114">Installer et exécuter l’outil d’exportation eDiscovery d’Office 365</span><span class="sxs-lookup"><span data-stu-id="c9d05-114">Install and run the Office 365 eDiscovery Export Tool</span></span>

1. <span data-ttu-id="c9d05-115">Cliquez sur **Télécharger les résultats** sur la page de menu volant d’une recherche d’exportation dans le contenu ou de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="c9d05-115">Click **Download results** on the flyout page of an export in Content Search or an eDiscovery case.</span></span>

   ![Cliquez sur Télécharger les résultats sur la page de menu volant pour télécharger les résultats de la recherche.](media/ClickOnceExport1.png)

2. <span data-ttu-id="c9d05-117">Vous serez invité à confirmer le lancement de l’outil, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="c9d05-117">You will be prompted with a confirmation to launch the tool, Click **Open**.</span></span>

   ![Cliquez sur Ouvrir pour lancer l’outil d’exportation de découverte électronique.](media/ClickOnceimage4.png)

   <span data-ttu-id="c9d05-119">Si l’outil d’exportation de découverte électronique Microsoft Office 365 n’est pas installé, vous serez invité à indiquer un avertissement de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c9d05-119">If the Microsoft Office 365 eDiscovery Export Tool isn't installed, you will be prompted with a Security Warning,</span></span> 

   ![Cliquez sur installer pour installer l’outil d’exportation de découverte électronique.](media/ClickOnceimage5.png)

3. <span data-ttu-id="c9d05-121">Cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="c9d05-121">Click **Install**.</span></span> <span data-ttu-id="c9d05-122">Une fois l’installation terminée, l’outil d’exportation se lance automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c9d05-122">After it's installed, the export tool will launch automatically.</span></span>

<span data-ttu-id="c9d05-123">Pour plus d’informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9d05-123">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c9d05-124">Exporter les résultats de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="c9d05-124">Export Content Search results</span></span>](export-search-results.md)

- [<span data-ttu-id="c9d05-125">Activation des indicateurs d’expérimentation dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c9d05-125">How to enable experiment flags in Microsoft Edge</span></span>](https://microsoftedgesupport.microsoft.com/hc/articles/360034075294-How-to-enable-experiment-flags-in-Microsoft-Edge-Insider-channels)
