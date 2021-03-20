---
title: Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS
f1.keywords:
- CSH
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
- MET150
- GEA150
ms.assetid: 0669bf14-414d-4f51-8231-6b710ce7980b
ROBOTS: NOINDEX
description: 'Apprenez à créer des enregistrements DNS pour Office 365 géré par 21Vianet lorsque vous gérez vos enregistrements DNS. '
monikerRange: o365-21vianet
ms.openlocfilehash: 1eaa2bcc7263eaa12e53131246abd591006b0536
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50914353"
---
# <a name="create-dns-records-for-office-365-when-you-manage-your-dns-records"></a><span data-ttu-id="71d2c-103">Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="71d2c-103">Create DNS records for Office 365 when you manage your DNS records</span></span>

<span data-ttu-id="71d2c-104">Pour obtenir des instructions détaillées sur la création d’enregistrements DNS pour Office 365 géré par 21Vianet, notamment l’enregistrement MX requis pour le routage du courrier, voir Créer des enregistrements DNS chez n’importe quel fournisseur d’hébergement [DNS pour Office 365.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="71d2c-104">For detailed instructions about how to create DNS records for Office 365 operated by 21Vianet, including the MX record required for mail routing, see [Create DNS records at any DNS hosting provider for Office 365](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span> 
  
  
<span data-ttu-id="71d2c-105">Autres options et éléments à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="71d2c-105">More options and some things to be aware of:</span></span>
      
-  <span data-ttu-id="71d2c-106">Si vous ne connaissez pas le fournisseur d'hébergement DNS ou le bureau d'enregistrement pour votre domaine, voir [Rechercher mon bureau d'enregistrement de domaines ou mon fournisseur d'hébergement DNS](../get-help-with-domains/find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="71d2c-106">If you don't know the DNS hosting provider or domain registrar for your domain, see [Find your domain registrar or DNS hosting provider](../get-help-with-domains/find-your-domain-registrar.md).</span></span> <span data-ttu-id="71d2c-107">Pour obtenir des descriptions de ce que font les enregistrements DNS, voir les informations de base [sur DNS.](../get-help-with-domains/dns-basics.md)</span><span class="sxs-lookup"><span data-stu-id="71d2c-107">For descriptions of what the DNS records do, see [DNS basics](../get-help-with-domains/dns-basics.md).</span></span>
    
-  <span data-ttu-id="71d2c-108">Certains fournisseurs d’hébergement DNS ne vous laissaient pas créer tous les types d’enregistrement requis, ce qui entraîne des limitations de service lorsque votre fournisseur d’hébergement ne prend pas en charge [SRV, CNAME, TXT](https://support.microsoft.com/office/dfbb03e3-08c1-4c4e-b2f0-891665b29b77)ou la redirection.</span><span class="sxs-lookup"><span data-stu-id="71d2c-108">Some DNS hosting providers don't let you create all the required record types, which causes [Service limitations when your hosting provider does not support SRV, CNAME, TXT, or redirection](https://support.microsoft.com/office/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span></span> <span data-ttu-id="71d2c-109">Si votre fournisseur ne prend pas en charge les enregistrements SRV, [](../get-help-with-domains/buy-a-domain-name.md) TXT ou CNAME, nous vous recommandons de transférer votre domaine vers un fournisseur qui prend en charge tous les types d’enregistrements [requis.](https://support.microsoft.com/office/dfbb03e3-08c1-4c4e-b2f0-891665b29b77)</span><span class="sxs-lookup"><span data-stu-id="71d2c-109">If your provider doesn't support SRV, TXT, or CNAME records, we recommend that you [transfer your domain](../get-help-with-domains/buy-a-domain-name.md) to a [provider that supports all required record types](https://support.microsoft.com/office/dfbb03e3-08c1-4c4e-b2f0-891665b29b77).</span></span> 
    
- <span data-ttu-id="71d2c-110">Pour voir quels enregistrements DNS sont requis et trouver les valeurs à utiliser pour chaque enregistrement, y compris l’enregistrement MX pour le courrier électronique, voir Recueillir les informations dont vous avez besoin pour créer des enregistrements [DNS Office 365.](../get-help-with-domains/information-for-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="71d2c-110">To see which DNS records are required and find the values to use for each record, including the MX record for email, see [Gather the information you need to create Office 365 DNS records](../get-help-with-domains/information-for-dns-records.md).</span></span> <span data-ttu-id="71d2c-111">Pour obtenir des descriptions de ce que font les enregistrements DNS, voir les informations de base [sur DNS.](../get-help-with-domains/dns-basics.md)</span><span class="sxs-lookup"><span data-stu-id="71d2c-111">For descriptions of what the DNS records do, see [DNS basics](../get-help-with-domains/dns-basics.md).</span></span>
