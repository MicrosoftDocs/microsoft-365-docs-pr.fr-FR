---
title: Optimisation des performances Exchange Online
ms.author: krowley
author: tracyp
manager: laurawi
ms.date: 12/14/2017
audience: Admin
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom: Adm_O365
ms.assetid: 026e83cb-a945-4543-97b0-a8af6e80ac61
description: Cet article contient des conseils généraux et des liens vers d’autres ressources qui vous indiquent comment améliorer les performances d’Exchange Online.
ms.openlocfilehash: a7d3268f9f3cf1922319b03cf69d3f044272b27f
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909441"
---
# <a name="tune-exchange-online-performance"></a><span data-ttu-id="9fd58-103">Optimisation des performances Exchange Online</span><span class="sxs-lookup"><span data-stu-id="9fd58-103">Tune Exchange Online performance</span></span>

<span data-ttu-id="9fd58-104">Cet article contient des conseils généraux et des liens vers d’autres ressources qui vous indiquent comment améliorer les performances d’Exchange Online, en particulier avant une migration.</span><span class="sxs-lookup"><span data-stu-id="9fd58-104">This article contains general tips and links to other resources that tell you how to improve performance of Exchange Online, particularly in front of a migration.</span></span> <span data-ttu-id="9fd58-105">Cet article fait partie de la planification réseau et de l’optimisation des performances pour le projet [Office 365.](./network-planning-and-performance.md)</span><span class="sxs-lookup"><span data-stu-id="9fd58-105">This article is part of the [Network planning and performance tuning for Office 365](./network-planning-and-performance.md) project.</span></span>
   
## <a name="things-to-consider-in-order-to-improve-exchange-online-performance"></a><span data-ttu-id="9fd58-106">Éléments à prendre en compte pour améliorer les performances d’Exchange Online</span><span class="sxs-lookup"><span data-stu-id="9fd58-106">Things to consider in order to improve Exchange Online performance</span></span>

<span data-ttu-id="9fd58-107">Pour améliorer la vitesse de migration et réduire les contraintes de bande passante de votre organisation pour Exchange Online, prenons en compte les considérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fd58-107">To improve the speed of migration and reduce your organization's bandwidth constraints for Exchange Online, consider the following:</span></span>
  
- <span data-ttu-id="9fd58-108">**Réduisez la taille des boîtes aux lettres.**</span><span class="sxs-lookup"><span data-stu-id="9fd58-108">**Reduce mailbox sizes.**</span></span> <span data-ttu-id="9fd58-109">Une taille de boîte aux lettres plus petite améliore la vitesse de migration.</span><span class="sxs-lookup"><span data-stu-id="9fd58-109">Smaller mailbox size improves migration speed.</span></span> 
    
- <span data-ttu-id="9fd58-110">**Utilisez les fonctionnalités de déplacement de boîtes aux lettres avec un déploiement hybride Exchange.**</span><span class="sxs-lookup"><span data-stu-id="9fd58-110">**Use the mailbox move capabilities with an Exchange hybrid deployment.**</span></span> <span data-ttu-id="9fd58-111">Avec un déploiement hybride Exchange, la messagerie hors connexion (sous la forme . Fichiers OST) ne nécessite pas de re-téléchargement lors de la migration vers Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9fd58-111">With an Exchange hybrid deployment, offline mail (in the form of .OST files) does not require re-download when migrating to Exchange Online.</span></span> <span data-ttu-id="9fd58-112">Cela réduit considérablement vos besoins en bande passante de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="9fd58-112">This significantly reduces your download bandwidth requirements.</span></span> 
    
- <span data-ttu-id="9fd58-113">**Planifier les déplacements de boîtes aux lettres pendant les périodes de faible trafic Internet et d’utilisation d’Exchange sur site faible.**</span><span class="sxs-lookup"><span data-stu-id="9fd58-113">**Schedule mailbox moves to occur during periods of low Internet traffic and low on-premises Exchange use.**</span></span> <span data-ttu-id="9fd58-114">Lors de la planification des déplacements, les demandes de migration sont envoyées au proxy de réplication de boîte aux lettres et peuvent ne pas avoir lieu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="9fd58-114">When scheduling moves, migration requests are submitted to the mailbox replication proxy and may not take place immediately.</span></span> 
    
- <span data-ttu-id="9fd58-115">**Utilisez des fenêtres pop-out légères pour Outlook sur le web.**</span><span class="sxs-lookup"><span data-stu-id="9fd58-115">**Use lean popouts for Outlook on the web.**</span></span> <span data-ttu-id="9fd58-116">Les fenêtres pop-out allégées fournissent des versions plus petites et moins intensives en mémoire de certains messages électroniques dans Microsoft Edge ou Internet Explorer en rendant certains composants sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9fd58-116">Lean popouts provide smaller, less memory-intensive versions of certain email messages in Microsoft Edge or Internet Explorer by rendering some components on the server.</span></span> <span data-ttu-id="9fd58-117">Pour plus d’informations, voir [Utiliser des fenêtres publicitaires légères](https://support.office.com/article/a6d6ba01-2562-4c3d-a8f1-78748dd506cf)pour réduire la mémoire utilisée lors de la lecture des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="9fd58-117">For more information, see [Use lean popouts to reduce memory used when reading mail messages](https://support.office.com/article/a6d6ba01-2562-4c3d-a8f1-78748dd506cf).</span></span>


## <a name="general-advice"></a><span data-ttu-id="9fd58-118">Conseils généraux</span><span class="sxs-lookup"><span data-stu-id="9fd58-118">General advice</span></span>

- <span data-ttu-id="9fd58-119">Assurez-vous que la recherche DNS pour outlook.office.com le centre de données MS à un emplacement d’entrée logique pour votre emplacement.</span><span class="sxs-lookup"><span data-stu-id="9fd58-119">Make certain that DNS lookup for outlook.office.com enters the MS-datacenter at a logical entry location for your location.</span></span>

- <span data-ttu-id="9fd58-120">Mise en cache de boîte aux lettres de recherche et choix des options appropriées (re.</span><span class="sxs-lookup"><span data-stu-id="9fd58-120">Research mailbox caching and choose the appropriate options (re.</span></span> <span data-ttu-id="9fd58-121">période de mise en cache, mise en cache de boîtes aux lettres partagées, et courrier électronique).</span><span class="sxs-lookup"><span data-stu-id="9fd58-121">caching period, shared mailbox caching, et cetera).</span></span>

- <span data-ttu-id="9fd58-122">Veillez à ce que vos données Outlook ne passent pas de connexions VPN (à un bureau central) avant qu’elles ne passent par Internet.</span><span class="sxs-lookup"><span data-stu-id="9fd58-122">Keep your Outlook data from passing over VPN connections (to a central office) before it goes over the Internet.</span></span>

- <span data-ttu-id="9fd58-123">Assurez-vous que vos données de boîte aux lettres respectent les limites imposées aux montants des dossiers et des éléments.</span><span class="sxs-lookup"><span data-stu-id="9fd58-123">Be sure your mailbox data adheres to the limitations on folder, and item, amounts.</span></span>
    
<span data-ttu-id="9fd58-124">Pour plus d’informations sur les performances de migration Exchange, consultez les meilleures pratiques et performances de [migration d’Office 365.](https://support.office.com/article/d9acb371-fd6c-4c14-aa8e-db5cbe39aa57)</span><span class="sxs-lookup"><span data-stu-id="9fd58-124">For more information about Exchange migration performance, see [Office 365 migration performance and best practices](https://support.office.com/article/d9acb371-fd6c-4c14-aa8e-db5cbe39aa57).</span></span>
