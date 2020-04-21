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
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 2c4cf347-b897-45c1-a71f-210bdc8f1061
description: Découvrez comment acheminer le trafic vers un site Web public existant hébergé en dehors de Microsoft, si vous avez configuré Microsoft pour gérer les enregistrements DNS pour votre domaine personnalisé.
ms.openlocfilehash: 08a4e505f4e2a50b3e92cae00b62415e6d02551f
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629118"
---
# <a name="update-dns-records-to-keep-your-website-with-your-current-hosting-provider"></a><span data-ttu-id="8b2c3-103">Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel</span><span class="sxs-lookup"><span data-stu-id="8b2c3-103">Update DNS records to keep your website with your current hosting provider</span></span>

 <span data-ttu-id="8b2c3-104">**Si vous gérez les enregistrements Microsoft de votre domaine auprès de votre fournisseur d’hébergement DNS**, vous n’avez pas à vous soucier des étapes décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-104">**If you manage your domain's Microsoft records at your DNS hosting provider**, you don't have to worry about the steps in this topic.</span></span> <span data-ttu-id="8b2c3-105">Votre site web reste en place et les utilisateurs peuvent toujours y accéder.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-105">Your website stays where it is and people can still get to it.</span></span> 
  
 <span data-ttu-id="8b2c3-106">**Si Microsoft gère vos enregistrements DNS**, pour acheminer le trafic vers un site Web public existant hébergé en dehors de Microsoft, après avoir ajouté votre domaine à Microsoft, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8b2c3-106">**If Microsoft manages your DNS records**, to route traffic to an existing public website hosted outside of Microsoft, after you add your domain to Microsoft, do the following:</span></span> 
  
## <a name="update-dns-records-in-the-microsoft-365-admin-center"></a><span data-ttu-id="8b2c3-107">Mettre à jour les enregistrements DNS dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8b2c3-107">Update DNS records in the Microsoft 365 admin center</span></span>
1. <span data-ttu-id="8b2c3-108">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-108">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="8b2c3-109">Sur la page **Domaines**, dans la liste de domaines, cliquez sur celui que vous utilisez pour votre site web, puis sélectionnez **Paramètres DNS** dans le volet de gestion.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-109">On the **Domains** page, in the list of domains, select the domain you're using for your website, and then select **DNS settings** in the management pane.</span></span> 
    
3. <span data-ttu-id="8b2c3-110">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8b2c3-110">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="8b2c3-111">Pour **Type de DNS** entrez : **A (Adresse)**</span><span class="sxs-lookup"><span data-stu-id="8b2c3-111">For **DNS type** enter: **A (Address)**</span></span>
    
  - <span data-ttu-id="8b2c3-112">Pour **Nom d'hôte ou Alias**, tapez **@**.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-112">For **Host name or Alias**, type the following: **@**</span></span>
    
  - <span data-ttu-id="8b2c3-113">Pour **Adresse IP**, tapez l'adresse IP statique correspondant à l'hébergement actuel de votre site web (par exemple, 172.16.140.1).</span><span class="sxs-lookup"><span data-stu-id="8b2c3-113">For **IP Address**, type the static IP address for your website where it's currently hosted (for example, 172.16.140.1).</span></span> 
    
    <span data-ttu-id="8b2c3-p102">Il doit s'agir d'une adresse IP  *statique*  pour le site web (et non d'une adresse IP  *dynamique*  ). Vérifiez l'emplacement d'hébergement de votre site web pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-p102">This must be a  *static*  IP address for the website, not a  *dynamic*  IP address. Check with site where your website is hosted to make sure you can get a static IP address for your public website.</span></span> 
    
3. <span data-ttu-id="8b2c3-116">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-116">Select **Save**.</span></span> 
    
<span data-ttu-id="8b2c3-117">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-117">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1. <span data-ttu-id="8b2c3-118">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8b2c3-118">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="8b2c3-119">Pour **Type de DNS** entrez : **CNAME (Alias)**</span><span class="sxs-lookup"><span data-stu-id="8b2c3-119">For **DNS type** enter: **CNAME (Alias)**</span></span>
    
  - <span data-ttu-id="8b2c3-120">Pour **Nom d'hôte ou Alias**, tapez **www**</span><span class="sxs-lookup"><span data-stu-id="8b2c3-120">For **Host name or Alias**, type the following: **www**</span></span>
    
  - <span data-ttu-id="8b2c3-121">Pour **Adresse de pointage**, tapez le nom de domaine complet (FQDN) de votre site web (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8b2c3-121">For **Points to address**, type the fully qualified domain name (FQDN) for your website (for example, contoso.com).</span></span> 
    
2. <span data-ttu-id="8b2c3-122">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-122">Select **Save**.</span></span> 
    
<span data-ttu-id="8b2c3-123">Pour terminer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8b2c3-123">Finally, do the following:</span></span>
  
<span data-ttu-id="8b2c3-124">[Mettez à jour les enregistrements NS de votre domaine](https://support.office.com/article/a46bec33-2c78-4f45-a96c-b64b2a5bae22.aspx) pour qu’ils pointent vers Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-124">[Update your domain's NS records](https://support.office.com/article/a46bec33-2c78-4f45-a96c-b64b2a5bae22.aspx) to point to Microsoft.</span></span> 
  
<span data-ttu-id="8b2c3-125">Lorsque les enregistrements NS ont été mis à jour pour pointer vers Microsoft, votre domaine est configuré.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-125">When the NS records have been updated to point to Microsoft, your domain is all set up.</span></span> <span data-ttu-id="8b2c3-126">Le courrier électronique sera acheminé vers Microsoft, et le trafic vers votre adresse de site Web continuera à accéder à votre hôte de site Web actuel.</span><span class="sxs-lookup"><span data-stu-id="8b2c3-126">Email will be routed to Microsoft, and traffic to your website address will continue to go to your current website host.</span></span>
 
