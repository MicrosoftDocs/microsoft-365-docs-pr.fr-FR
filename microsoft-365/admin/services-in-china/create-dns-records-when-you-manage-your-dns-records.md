---
title: Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS
f1.keywords:
- CSH
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
- MET150
- GEA150
ms.assetid: 0669bf14-414d-4f51-8231-6b710ce7980b
ROBOTS: NOINDEX
description: 'Apprenez à créer des enregistrements DNS pour Office 365 géré par 21Vianet lors de la gestion de vos enregistrements DNS. '
monikerRange: o365-21vianet
ms.openlocfilehash: 478f3d48a8d94d0a42d6501df8f0c32efc41e902
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399073"
---
# <a name="create-dns-records-for-office-365-when-you-manage-your-dns-records"></a><span data-ttu-id="0a072-103">Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="0a072-103">Create DNS records for Office 365 when you manage your DNS records</span></span>

<span data-ttu-id="0a072-104">Pour obtenir des instructions détaillées sur la création d’enregistrements DNS pour Office 365 géré par 21Vianet, y compris l’enregistrement MX requis pour le routage du courrier, consultez la rubrique [créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0a072-104">For detailed instructions about how to create DNS records for Office 365 operated by 21Vianet, including the MX record required for mail routing, see [Create DNS records at any DNS hosting provider for Office 365](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span> 
  
  
<span data-ttu-id="0a072-105">Plus d’options et quelques éléments à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="0a072-105">More options and some things to be aware of:</span></span>
      
-  <span data-ttu-id="0a072-106">Si vous ne connaissez pas le fournisseur d'hébergement DNS ou le bureau d'enregistrement pour votre domaine, voir [Rechercher mon bureau d'enregistrement de domaines ou mon fournisseur d'hébergement DNS](../get-help-with-domains/find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="0a072-106">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span> <span data-ttu-id="0a072-107">Pour obtenir une description des enregistrements DNS, consultez la rubrique [DNS Basics](../get-help-with-domains/dns-basics.md).</span><span class="sxs-lookup"><span data-stu-id="0a072-107">For descriptions of what the DNS records do, see [DNS basics](../get-help-with-domains/dns-basics.md).</span></span>
    
-  <span data-ttu-id="0a072-108">Certains fournisseurs d’hébergement DNS ne vous permettent pas de créer tous les types d’enregistrements requis, ce qui entraîne des [limitations de service lorsque votre fournisseur d’hébergement ne prend pas en charge SRV, CNAME, txt ou la redirection](https://support.office.com/article/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span><span class="sxs-lookup"><span data-stu-id="0a072-108">Some DNS hosting providers don't let you create all the required record types, which causes [Service limitations when your hosting provider does not support SRV, CNAME, TXT, or redirection](https://support.office.com/article/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span></span> <span data-ttu-id="0a072-109">Si votre fournisseur ne prend pas en charge les enregistrements SRV, TXT ou CNAMe, nous vous recommandons de [transférer votre domaine](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/buy-a-domain-name) à un [fournisseur qui prend en charge tous les types d’enregistrements requis](https://support.office.com/article/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span><span class="sxs-lookup"><span data-stu-id="0a072-109">If your provider doesn't support SRV, TXT, or CNAME records, we recommend that you [transfer your domain](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/buy-a-domain-name) to a [provider that supports all required record types](https://support.office.com/article/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span></span> 
    
- <span data-ttu-id="0a072-110">Pour voir les enregistrements DNS requis et rechercher les valeurs à utiliser pour chaque enregistrement, y compris l’enregistrement MX pour le courrier électronique, consultez [la rubrique recueillir les informations nécessaires pour créer des enregistrements DNS Office 365](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/information-for-dns-records).</span><span class="sxs-lookup"><span data-stu-id="0a072-110">To see which DNS records are required and find the values to use for each record, including the MX record for email, see [Gather the information you need to create Office 365 DNS records](https://docs.microsoft.com/microsoft-365/admin/get-help-with-domains/information-for-dns-records).</span></span> <span data-ttu-id="0a072-111">Pour obtenir une description des enregistrements DNS, consultez la rubrique [DNS Basics](../get-help-with-domains/dns-basics.md).</span><span class="sxs-lookup"><span data-stu-id="0a072-111">For descriptions of what the DNS records do, see [DNS basics](../get-help-with-domains/dns-basics.md).</span></span>
    

