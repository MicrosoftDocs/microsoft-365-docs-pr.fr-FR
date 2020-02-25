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
description: Découvrez comment router le trafic vers un site Web public existant hébergé en dehors d’Office 365, si vous avez configuré Office 365 pour gérer les enregistrements DNS pour votre domaine personnalisé.
ms.openlocfilehash: de95818eea729cb11972faf986c9be40bb6e76da
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42253120"
---
# <a name="update-dns-records-to-keep-your-website-with-your-current-hosting-provider"></a><span data-ttu-id="f3e80-103">Mettre à jour les enregistrements DNS pour conserver votre site web chez votre fournisseur d'hébergement actuel</span><span class="sxs-lookup"><span data-stu-id="f3e80-103">Update DNS records to keep your website with your current hosting provider</span></span>

 <span data-ttu-id="f3e80-p101">[] **Si vous gérez les enregistrements Office 365 de votre domaine au niveau de votre fournisseur d'hébergement DNS**, vous n'avez pas à vous soucier des étapes de cette rubrique. Votre site web reste en place et les utilisateurs peuvent toujours y accéder.</span><span class="sxs-lookup"><span data-stu-id="f3e80-p101">**If you manage your domain's Office 365 records at your DNS hosting provider**, you don't have to worry about the steps in this topic. Your website stays where it is and people can still get to it.</span></span> 
  
 <span data-ttu-id="f3e80-106">**Si Office 365 gère vos enregistrements DNS**, procédez comme suit pour router le trafic vers un site web public existant hébergé à l'extérieur d'Office 365, après avoir ajouté votre domaine à Office 365 :</span><span class="sxs-lookup"><span data-stu-id="f3e80-106">**If Office 365 manages your DNS records**, to route traffic to an existing public website hosted outside of Office 365, after you add your domain to Office 365, do the following:</span></span> 
  
## <a name="update-dns-records-in-the-microsoft-365-admin-center"></a><span data-ttu-id="f3e80-107">Mettre à jour les enregistrements DNS dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f3e80-107">Update DNS records in the Microsoft 365 admin center</span></span>
1. <span data-ttu-id="f3e80-108">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="f3e80-108">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="f3e80-109">Sur la page **Domaines**, dans la liste de domaines, cliquez sur celui que vous utilisez pour votre site web, puis sélectionnez **Paramètres DNS** dans le volet de gestion.</span><span class="sxs-lookup"><span data-stu-id="f3e80-109">On the **Domains** page, in the list of domains, select the domain you're using for your website, and then select **DNS settings** in the management pane.</span></span> 
    
3. <span data-ttu-id="f3e80-110">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f3e80-110">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="f3e80-111">Pour **Type de DNS** entrez : **A (Adresse)**</span><span class="sxs-lookup"><span data-stu-id="f3e80-111">For **DNS type** enter: **A (Address)**</span></span>
    
  - <span data-ttu-id="f3e80-112">Pour **Nom d'hôte ou Alias**, tapez **@**.</span><span class="sxs-lookup"><span data-stu-id="f3e80-112">For **Host name or Alias**, type the following: **@**</span></span>
    
  - <span data-ttu-id="f3e80-113">Pour **Adresse IP**, tapez l'adresse IP statique correspondant à l'hébergement actuel de votre site web (par exemple, 172.16.140.1).</span><span class="sxs-lookup"><span data-stu-id="f3e80-113">For **IP Address**, type the static IP address for your website where it's currently hosted (for example, 172.16.140.1).</span></span> 
    
    <span data-ttu-id="f3e80-p102">Il doit s'agir d'une adresse IP  *statique*  pour le site web (et non d'une adresse IP  *dynamique*  ). Vérifiez l'emplacement d'hébergement de votre site web pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public.</span><span class="sxs-lookup"><span data-stu-id="f3e80-p102">This must be a  *static*  IP address for the website, not a  *dynamic*  IP address. Check with site where your website is hosted to make sure you can get a static IP address for your public website.</span></span> 
    
3. <span data-ttu-id="f3e80-116">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f3e80-116">Select **Save**.</span></span> 
    
<span data-ttu-id="f3e80-117">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="f3e80-117">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1. <span data-ttu-id="f3e80-118">Sélectionnez **+Nouvel enregistrement personnalisé** et entrez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f3e80-118">Select **+ New custom record** and enter the following:</span></span> 
    
  - <span data-ttu-id="f3e80-119">Pour **Type de DNS** entrez : **CNAME (Alias)**</span><span class="sxs-lookup"><span data-stu-id="f3e80-119">For **DNS type** enter: **CNAME (Alias)**</span></span>
    
  - <span data-ttu-id="f3e80-120">Pour **Nom d'hôte ou Alias**, tapez **www**</span><span class="sxs-lookup"><span data-stu-id="f3e80-120">For **Host name or Alias**, type the following: **www**</span></span>
    
  - <span data-ttu-id="f3e80-121">Pour **Adresse de pointage**, tapez le nom de domaine complet (FQDN) de votre site web (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="f3e80-121">For **Points to address**, type the fully qualified domain name (FQDN) for your website (for example, contoso.com).</span></span> 
    
2. <span data-ttu-id="f3e80-122">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f3e80-122">Select **Save**.</span></span> 
    
<span data-ttu-id="f3e80-123">Pour terminer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f3e80-123">Finally, do the following:</span></span>
  
<span data-ttu-id="f3e80-124">[Mettez à jour les enregistrements de serveur de noms de votre domaine](https://support.office.com/article/a46bec33-2c78-4f45-a96c-b64b2a5bae22.aspx) pour qu'ils pointent vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="f3e80-124">[Update your domain's NS records](https://support.office.com/article/a46bec33-2c78-4f45-a96c-b64b2a5bae22.aspx) to point to Office 365.</span></span> 
  
<span data-ttu-id="f3e80-p103">Quand les enregistrements de serveur de noms ont été mis à jour de façon à pointer vers Office 365, votre domaine est configuré. Les messages électroniques sont acheminés vers Office 365 et le trafic vers l'adresse de votre site web continue d'être acheminé vers votre fournisseur d'hébergement actuel.</span><span class="sxs-lookup"><span data-stu-id="f3e80-p103">When the NS records have been updated to point to Office 365, your domain is all set up. Email will be routed to Office 365, and traffic to your website address will continue to go to your current website host.</span></span>
 