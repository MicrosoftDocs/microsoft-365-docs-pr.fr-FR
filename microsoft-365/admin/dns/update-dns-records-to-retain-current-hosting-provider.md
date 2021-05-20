---
title: Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 2c4cf347-b897-45c1-a71f-210bdc8f1061
description: Découvrez comment router le trafic vers un site web public existant hébergé en dehors de Microsoft, si vous avez demandé à Microsoft de gérer les enregistrements DNS pour votre domaine personnalisé.
ms.openlocfilehash: 2a1559bbb902375bbc363180cdb4f98ec2b3a939
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572140"
---
# <a name="update-dns-records-to-keep-your-website-with-your-current-hosting-provider"></a><span data-ttu-id="7b1cb-103">Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel</span><span class="sxs-lookup"><span data-stu-id="7b1cb-103">Update DNS records to keep your website with your current hosting provider</span></span>

 <span data-ttu-id="7b1cb-104">Si vous gérez les enregistrements Microsoft de votre domaine chez votre fournisseur d’hébergement **DNS,** vous n’avez pas à vous soucier des étapes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-104">**If you manage your domain's Microsoft records at your DNS hosting provider**, you don't have to worry about the steps in this topic.</span></span> <span data-ttu-id="7b1cb-105">Votre site web reste en place et les utilisateurs peuvent toujours y accéder.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-105">Your website stays where it is and people can still get to it.</span></span> 
  
 <span data-ttu-id="7b1cb-106">Si Microsoft gère vos enregistrements **DNS,** pour router le trafic vers un site web public existant hébergé en dehors de Microsoft, après avoir ajouté votre domaine à Microsoft, faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b1cb-106">**If Microsoft manages your DNS records**, to route traffic to an existing public website hosted outside of Microsoft, after you add your domain to Microsoft, do the following:</span></span> 
  
## <a name="update-dns-records-in-the-microsoft-365-admin-center"></a><span data-ttu-id="7b1cb-107">Mettre à jour les enregistrements DNS dans le centre Microsoft 365'administration</span><span class="sxs-lookup"><span data-stu-id="7b1cb-107">Update DNS records in the Microsoft 365 admin center</span></span>
1. <span data-ttu-id="7b1cb-108">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-108">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

1. <span data-ttu-id="7b1cb-109">Dans la page **Domaines,** sélectionnez le domaine, puis choisissez **Enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-109">On the **Domains** page, select the domain and then choose **DNS Records**.</span></span>

1. <span data-ttu-id="7b1cb-110">Sélectionnez **+ Ajouter un enregistrement,** puis entrez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7b1cb-110">Select **+ Add record** and enter the following:</span></span> 
    
   - <span data-ttu-id="7b1cb-111">For **type** enter: **A (Address)**</span><span class="sxs-lookup"><span data-stu-id="7b1cb-111">For **type** enter: **A (Address)**</span></span>
    
   - <span data-ttu-id="7b1cb-112">Pour **Nom d'hôte ou Alias**, tapez **@**.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-112">For **Host name or Alias**, type the following: **@**</span></span>
    
   - <span data-ttu-id="7b1cb-113">Pour **Adresse IP**, tapez l'adresse IP statique correspondant à l'hébergement actuel de votre site web (par exemple, 172.16.140.1).</span><span class="sxs-lookup"><span data-stu-id="7b1cb-113">For **IP Address**, type the static IP address for your website where it's currently hosted (for example, 172.16.140.1).</span></span> 
    
   <span data-ttu-id="7b1cb-p102">Il doit s'agir d'une adresse IP  *statique*  pour le site web (et non d'une adresse IP  *dynamique*  ). Vérifiez l'emplacement d'hébergement de votre site web pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-p102">This must be a  *static*  IP address for the website, not a  *dynamic*  IP address. Check with site where your website is hosted to make sure you can get a static IP address for your public website.</span></span> 
    
1. <span data-ttu-id="7b1cb-116">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-116">Select **Save**.</span></span> 
    
<span data-ttu-id="7b1cb-117">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-117">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1. <span data-ttu-id="7b1cb-118">Sélectionnez **+ Ajouter un enregistrement,** puis entrez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7b1cb-118">Select **+ Add record** and enter the following:</span></span> 
    
   - <span data-ttu-id="7b1cb-119">For **type** enter: **CNAME (Alias)**</span><span class="sxs-lookup"><span data-stu-id="7b1cb-119">For **type** enter: **CNAME (Alias)**</span></span>
    
   - <span data-ttu-id="7b1cb-120">Pour **Nom d'hôte ou Alias**, tapez **www**</span><span class="sxs-lookup"><span data-stu-id="7b1cb-120">For **Host name or Alias**, type the following: **www**</span></span>
    
   - <span data-ttu-id="7b1cb-121">Pour **Adresse de pointage**, tapez le nom de domaine complet (FQDN) de votre site web (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="7b1cb-121">For **Points to address**, type the fully qualified domain name (FQDN) for your website (for example, contoso.com).</span></span> 
    
2. <span data-ttu-id="7b1cb-122">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-122">Select **Save**.</span></span> 
    
<span data-ttu-id="7b1cb-123">Pour terminer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7b1cb-123">Finally, do the following:</span></span>
  
<span data-ttu-id="7b1cb-124">[Mettez à jour les enregistrements NS de votre](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) domaine pour qu’ils pointent vers Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-124">[Update your domain's NS records](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) to point to Microsoft.</span></span> 
  
<span data-ttu-id="7b1cb-125">Lorsque les enregistrements NS ont été mis à jour pour pointer vers Microsoft, votre domaine est tous mis en place.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-125">When the NS records have been updated to point to Microsoft, your domain is all set up.</span></span> <span data-ttu-id="7b1cb-126">Le courrier électronique est acheminé vers Microsoft et le trafic vers votre adresse de site web continue d’être acheminé vers l’hôte de votre site web actuel.</span><span class="sxs-lookup"><span data-stu-id="7b1cb-126">Email will be routed to Microsoft, and traffic to your website address will continue to go to your current website host.</span></span>
