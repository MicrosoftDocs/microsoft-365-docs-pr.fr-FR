---
title: Rechercher votre bureau d’enregistrement de domaine
f1.keywords:
- CSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: b5b633ba-1e56-4a98-8ff5-2acaac63a5c8
description: Découvrez comment rechercher votre bureau d’enregistrement de domaines et votre fournisseur d’hébergement DNS à l’aide de la recherche InterNIC.
ms.openlocfilehash: 8fa75800125179f046f3af76eea490d760b9f6cd
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48645322"
---
# <a name="find-your-domain-registrar"></a><span data-ttu-id="97307-103">Rechercher votre bureau d’enregistrement de domaine</span><span class="sxs-lookup"><span data-stu-id="97307-103">Find your domain registrar</span></span>

 <span data-ttu-id="97307-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="97307-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
## <a name="domain-registrar"></a><span data-ttu-id="97307-105">Bureau d'enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="97307-105">Domain registrar</span></span>
  
### <a name="find-your-domain-name-registrar"></a><span data-ttu-id="97307-106">Rechercher votre bureau d’enregistrement de noms de domaine</span><span class="sxs-lookup"><span data-stu-id="97307-106">Find your domain name registrar</span></span>

>[!NOTE]
> <span data-ttu-id="97307-107">Seuls les domaines se terminant par *. COM*, *.NET*et *.EDU* sont compatibles avec cet outil.</span><span class="sxs-lookup"><span data-stu-id="97307-107">Only domains ending in *.COM*, *.NET*, and *.EDU* work with this tool.</span></span>
  
1. <span data-ttu-id="97307-108">Tapez votre domaine dans la [page de recherche InterNIC](https://go.microsoft.com/fwlink/p/?LinkId=402770), dans la zone **Whois Search**.</span><span class="sxs-lookup"><span data-stu-id="97307-108">On the [InterNIC search page](https://go.microsoft.com/fwlink/p/?LinkId=402770), in the **Whois Search** box, type your domain.</span></span> <span data-ttu-id="97307-109">Par exemple, *contoso.com*.</span><span class="sxs-lookup"><span data-stu-id="97307-109">For example,  *contoso.com.*</span></span> 
    
2. <span data-ttu-id="97307-110">Sélectionnez l'option **Domaine**, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="97307-110">Select the **Domain** option, and then select **Submit**.</span></span>
    
3. <span data-ttu-id="97307-111">Sur la page **Whois Search Results**, recherchez l'entrée **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="97307-111">On the **Whois Search Results** page, locate the **Registrar** entry.</span></span> <span data-ttu-id="97307-112">Cette entrée indique l'organisation qui fournit le service de bureau d'enregistrement pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="97307-112">This entry lists the organization that provides registrar service for your domain.</span></span> 
    
## <a name="dns-hosting-provider"></a><span data-ttu-id="97307-113">Fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="97307-113">DNS hosting provider</span></span>
  
### <a name="find-your-dns-hosting-provider"></a><span data-ttu-id="97307-114">Rechercher votre fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="97307-114">Find your DNS hosting provider</span></span>

>[!NOTE]
> <span data-ttu-id="97307-115">Seuls les domaines se terminant par *. COM*, *.NET*et *.EDU* sont compatibles avec cet outil.</span><span class="sxs-lookup"><span data-stu-id="97307-115">Only domains ending in *.COM*, *.NET*, and *.EDU* work with this tool.</span></span>
  
1. <span data-ttu-id="97307-116">Tapez votre domaine dans la [page de recherche InterNIC]( https://go.microsoft.com/fwlink/p/?LinkId=402770), dans la zone **Whois Search**.</span><span class="sxs-lookup"><span data-stu-id="97307-116">On the [InterNIC search page]( https://go.microsoft.com/fwlink/p/?LinkId=402770), in the **Whois Search** box, type your domain.</span></span> <span data-ttu-id="97307-117">Par exemple, contoso.com.</span><span class="sxs-lookup"><span data-stu-id="97307-117">For example, contoso.com.</span></span> 
    
2. <span data-ttu-id="97307-118">Sélectionnez l'option **Domaine**, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="97307-118">Select the **Domain** option, and then select **Submit**.</span></span>
    
3. <span data-ttu-id="97307-119">Sur la page **Whois Search Results**, localisez la première entrée **Name Server**.</span><span class="sxs-lookup"><span data-stu-id="97307-119">On the **Whois Search Results** page, locate the first **Name Server** entry.</span></span> 
    
4. <span data-ttu-id="97307-120">Copiez les informations sur le serveur de noms (NS) affichées après les deux-points (:), puis collez-les dans la zone **Search** en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="97307-120">Copy the name server (NS) information that appears after the colon (:), and then paste it into the **Search** box at the top of the page.</span></span> <span data-ttu-id="97307-121">Sélectionnez **Serveur de noms**, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="97307-121">Select **Nameserver**, and then select **Submit**.</span></span>
    
5. <span data-ttu-id="97307-p105">Sur la page **Whois Search Results**, recherchez l’entrée **Registrar**. Cette entrée indique votre fournisseur d’hébergement DNS, le fournisseur DNS qui est propriétaire du serveur de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="97307-p105">On the **Whois Search Results** page, locate the **Registrar** entry. This entry lists your DNS hosting provider, the DNS provider who owns the name server for your domain.</span></span> 
    
---

