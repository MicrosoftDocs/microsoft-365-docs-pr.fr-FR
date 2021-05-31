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
ms.openlocfilehash: af883f53c8c45aee2594b0f5b8b9da57e5717f9e
ms.sourcegitcommit: a05f61a291eb4595fa9313757a3815b7f217681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2021
ms.locfileid: "52706393"
---
# <a name="find-your-domain-registrar"></a><span data-ttu-id="a7f82-103">Rechercher votre bureau d’enregistrement de domaine</span><span class="sxs-lookup"><span data-stu-id="a7f82-103">Find your domain registrar</span></span>

 <span data-ttu-id="a7f82-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a7f82-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
## <a name="domain-registrar"></a><span data-ttu-id="a7f82-105">Bureau d'enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="a7f82-105">Domain registrar</span></span>
  
### <a name="find-your-domain-name-registrar"></a><span data-ttu-id="a7f82-106">Rechercher votre bureau d’enregistrement de noms de domaine</span><span class="sxs-lookup"><span data-stu-id="a7f82-106">Find your domain name registrar</span></span>

>[!NOTE]
> <span data-ttu-id="a7f82-107">Seuls les domaines se terminant par *. COM*, *.NET* et *.EDU* sont compatibles avec cet outil.</span><span class="sxs-lookup"><span data-stu-id="a7f82-107">Only domains ending in *.COM*, *.NET*, and *.EDU* work with this tool.</span></span>
  
1. <span data-ttu-id="a7f82-p101">Sur la [page de recherche InterNIC](https://go.microsoft.com/fwlink/p/?LinkId=402770), dans la zone **Whois Search**, tapez votre domaine (par exemple,  *contoso.com).*</span><span class="sxs-lookup"><span data-stu-id="a7f82-p101">On the [InterNIC search page](https://go.microsoft.com/fwlink/p/?LinkId=402770), in the **Whois Search** box, type your domain. For example,  *contoso.com.*</span></span> 
    
2. <span data-ttu-id="a7f82-110">Sélectionnez l'option **Domaine**, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a7f82-110">Select the **Domain** option, and then select **Submit**.</span></span>
    
3. <span data-ttu-id="a7f82-p102">Sur la page **Whois Search Results**, recherchez l’entrée **Registrar**. Cette entrée indique l’organisation qui fournit le service de bureau d’enregistrement pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a7f82-p102">On the **Whois Search Results** page, locate the **Registrar** entry. This entry lists the organization that provides registrar service for your domain.</span></span> 
    
## <a name="dns-hosting-provider"></a><span data-ttu-id="a7f82-113">Fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="a7f82-113">DNS hosting provider</span></span>
  
### <a name="find-your-dns-hosting-provider"></a><span data-ttu-id="a7f82-114">Rechercher votre fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="a7f82-114">Find your DNS hosting provider</span></span>

>[!NOTE]
> <span data-ttu-id="a7f82-115">Seuls les domaines se terminant par *. COM*, *.NET* et *.EDU* sont compatibles avec cet outil.</span><span class="sxs-lookup"><span data-stu-id="a7f82-115">Only domains ending in *.COM*, *.NET*, and *.EDU* work with this tool.</span></span>
  
1. <span data-ttu-id="a7f82-p103">Sur la [page de recherche InterNIC]( https://go.microsoft.com/fwlink/p/?LinkId=402770), dans la zone **Whois Search**, tapez votre domaine (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a7f82-p103">On the [InterNIC search page]( https://go.microsoft.com/fwlink/p/?LinkId=402770), in the **Whois Search** box, type your domain. For example, contoso.com.</span></span> 
    
2. <span data-ttu-id="a7f82-118">Sélectionnez l'option **Domaine**, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a7f82-118">Select the **Domain** option, and then select **Submit**.</span></span>
    
3. <span data-ttu-id="a7f82-119">Sur la page **Whois Search Results**, localisez la première entrée **Name Server**.</span><span class="sxs-lookup"><span data-stu-id="a7f82-119">On the **Whois Search Results** page, locate the first **Name Server** entry.</span></span> 
    
4. <span data-ttu-id="a7f82-p104">Copiez les informations sur le serveur de noms (NS) affichées après les deux-points (:), puis collez-les dans la zone **Search** en haut de la page. Sélectionnez **Nameserver**, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="a7f82-p104">Copy the name server (NS) information that appears after the colon (:), and then paste it into the **Search** box at the top of the page. Select **Nameserver**, and then select **Submit**.</span></span>
    
5. <span data-ttu-id="a7f82-p105">Sur la page **Whois Search Results**, recherchez l’entrée **Registrar**. Cette entrée indique votre fournisseur d’hébergement DNS, le fournisseur DNS qui est propriétaire du serveur de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a7f82-p105">On the **Whois Search Results** page, locate the **Registrar** entry. This entry lists your DNS hosting provider, the DNS provider who owns the name server for your domain.</span></span> 
    
---

