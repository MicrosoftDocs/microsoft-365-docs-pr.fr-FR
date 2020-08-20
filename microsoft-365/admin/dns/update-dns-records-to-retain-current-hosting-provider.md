---
title: Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
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
description: Découvrez comment acheminer le trafic vers un site Web public existant hébergé en dehors de Microsoft, si vous avez configuré Microsoft pour gérer les enregistrements DNS pour votre domaine personnalisé.
ms.openlocfilehash: 9a7090eef3ce7d1c67839e7320f31d7bd32aa6a7
ms.sourcegitcommit: 167c05cc6a776f62f0a0c2de5f3ffeb68c4a27ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "46814397"
---
# <a name="update-dns-records-to-keep-your-website-with-your-current-hosting-provider"></a><span data-ttu-id="9b7b2-103">Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel</span><span class="sxs-lookup"><span data-stu-id="9b7b2-103">Update DNS records to keep your website with your current hosting provider</span></span>

 <span data-ttu-id="9b7b2-104">**Si vous gérez les enregistrements Microsoft de votre domaine auprès de votre fournisseur d’hébergement DNS**, vous n’avez pas à vous soucier des étapes décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-104">**If you manage your domain's Microsoft records at your DNS hosting provider**, you don't have to worry about the steps in this topic.</span></span> <span data-ttu-id="9b7b2-105">Votre site web reste en place et les utilisateurs peuvent toujours y accéder.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-105">Your website stays where it is and people can still get to it.</span></span> 
  
 <span data-ttu-id="9b7b2-106">**Si Microsoft gère vos enregistrements DNS**, pour acheminer le trafic vers un site Web public existant hébergé en dehors de Microsoft, après avoir ajouté votre domaine à Microsoft, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9b7b2-106">**If Microsoft manages your DNS records**, to route traffic to an existing public website hosted outside of Microsoft, after you add your domain to Microsoft, do the following:</span></span> 
  
## <a name="update-dns-records-in-the-microsoft-365-admin-center"></a><span data-ttu-id="9b7b2-107">Mettre à jour les enregistrements DNS dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9b7b2-107">Update DNS records in the Microsoft 365 admin center</span></span>
1. <span data-ttu-id="9b7b2-108">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-108">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="9b7b2-109">Dans la page **domaines** , sélectionnez le domaine, puis sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-109">On the **Domains** page, select the domain and then choose **DNS Records**.</span></span>

3. <span data-ttu-id="9b7b2-110">Sous **paramètres DNS**, sélectionnez **enregistrements personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-110">Under **DNS settings**, select **Custom Records**.</span></span>

4. <span data-ttu-id="9b7b2-111">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b7b2-111">Select **+ New custom record** and enter the following:</span></span> 
    
   - <span data-ttu-id="9b7b2-112">Pour **Type de DNS** entrez : **A (Adresse)**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-112">For **DNS type** enter: **A (Address)**</span></span>
    
   - <span data-ttu-id="9b7b2-113">Pour **Nom d'hôte ou Alias**, tapez **@**.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-113">For **Host name or Alias**, type the following: **@**</span></span>
    
   - <span data-ttu-id="9b7b2-114">Pour **Adresse IP**, tapez l'adresse IP statique correspondant à l'hébergement actuel de votre site web (par exemple, 172.16.140.1).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-114">For **IP Address**, type the static IP address for your website where it's currently hosted (for example, 172.16.140.1).</span></span> 
    
   <span data-ttu-id="9b7b2-p102">Il doit s'agir d'une adresse IP  *statique*  pour le site web (et non d'une adresse IP  *dynamique*  ). Vérifiez l'emplacement d'hébergement de votre site web pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-p102">This must be a  *static*  IP address for the website, not a  *dynamic*  IP address. Check with site where your website is hosted to make sure you can get a static IP address for your public website.</span></span> 
    
5. <span data-ttu-id="9b7b2-117">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-117">Select **Save**.</span></span> 
    
<span data-ttu-id="9b7b2-118">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-118">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1. <span data-ttu-id="9b7b2-119">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9b7b2-119">Select **+ New custom record** and enter the following:</span></span> 
    
   - <span data-ttu-id="9b7b2-120">Pour **Type de DNS** entrez : **CNAME (Alias)**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-120">For **DNS type** enter: **CNAME (Alias)**</span></span>
    
   - <span data-ttu-id="9b7b2-121">Pour **Nom d'hôte ou Alias**, tapez **www**</span><span class="sxs-lookup"><span data-stu-id="9b7b2-121">For **Host name or Alias**, type the following: **www**</span></span>
    
   - <span data-ttu-id="9b7b2-122">Pour **Adresse de pointage**, tapez le nom de domaine complet (FQDN) de votre site web (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9b7b2-122">For **Points to address**, type the fully qualified domain name (FQDN) for your website (for example, contoso.com).</span></span> 
    
2. <span data-ttu-id="9b7b2-123">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-123">Select **Save**.</span></span> 
    
<span data-ttu-id="9b7b2-124">Pour terminer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9b7b2-124">Finally, do the following:</span></span>
  
<span data-ttu-id="9b7b2-125">[Mettez à jour les enregistrements NS de votre domaine](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions) pour qu’ils pointent vers Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-125">[Update your domain's NS records](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/set-up-your-domain-host-specific-instructions) to point to Microsoft.</span></span> 
  
<span data-ttu-id="9b7b2-126">Lorsque les enregistrements NS ont été mis à jour pour pointer vers Microsoft, votre domaine est configuré.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-126">When the NS records have been updated to point to Microsoft, your domain is all set up.</span></span> <span data-ttu-id="9b7b2-127">Le courrier électronique sera acheminé vers Microsoft, et le trafic vers votre adresse de site Web continuera à accéder à votre hôte de site Web actuel.</span><span class="sxs-lookup"><span data-stu-id="9b7b2-127">Email will be routed to Microsoft, and traffic to your website address will continue to go to your current website host.</span></span>
 
