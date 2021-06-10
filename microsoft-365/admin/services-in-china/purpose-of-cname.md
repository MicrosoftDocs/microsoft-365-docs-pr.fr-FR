---
title: À quoi sert l'enregistrement CNAME Office 365 pour MSOID ?
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.collection:
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- BCS160
- MET150
- MOE150
ROBOTS: NOINDEX
description: En savoir plus sur l’enregistrement CNAME « MSOID » dans Office 365 qui vous dirige vers le meilleur serveur pour les processus d’authentification, afin que vous receviez une réponse plus rapide.
monikerRange: o365-21vianet
ms.openlocfilehash: a1d587abc9db03c9a1f7c5f66711fde3648a0e96
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50914305"
---
# <a name="whats-the-purpose-of-the-office-365-cname-record-for-msoid"></a><span data-ttu-id="317ff-103">À quoi sert l'enregistrement CNAME Office 365 pour MSOID ?</span><span class="sxs-lookup"><span data-stu-id="317ff-103">What's the purpose of the Office 365 CNAME record for MSOID?</span></span>

 <span data-ttu-id="317ff-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="317ff-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
> [!NOTE]
> <span data-ttu-id="317ff-105">L’exemple suivant s’applique uniquement à \*\*Office 365 géré par 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="317ff-105">The following only Applies to \*\*Office 365 operated by 21Vianet.</span></span>
  
<span data-ttu-id="317ff-p101">Vous vous demandez peut-être pourquoi vous devez ajouter l'enregistrement CNAME « MSOID » dans Office 365. Cet enregistrement doit être ajouté pour tous les domaines personnalisés, quel que soit l'abonnement que vous utilisez. Pourquoi en avez-vous besoin ? Il s'agit d'un aspect un peu technique. Grosso modo, cet enregistrement vous permet d'être redirigé vers le meilleur serveur pour certains processus d'authentification, afin de recevoir une réponse plus rapide.</span><span class="sxs-lookup"><span data-stu-id="317ff-p101">You may wonder why you need to add the "MSOID" CNAME record in Office 365. This is a record that has to be added for all custom domains, no matter which subscription you use. Why do you need it? It's a little technical, but essentially, it's so that you'll be directed to the best server for certain authentication processes, so you'll get faster response.</span></span>
  
<span data-ttu-id="317ff-p102">Informations techniques : lorsque vous exécutez une application cliente compatible avec Office 365, telle que Skype Entreprise Online, Outlook, Windows PowerShell ou l'outil de synchronisation Microsoft Azure Azure Active Directory, vos informations d'identification doivent être authentifiées. Office 365 utilise un enregistrement CNAME pour pointer vers le point de terminaison d'authentification correct pour votre emplacement, ce qui garantit des temps de réponse d'authentification rapides.</span><span class="sxs-lookup"><span data-stu-id="317ff-p102">Technical details: When you run a client application that works with Office 365 such as Skype for Business Online, Outlook, Windows PowerShell or Microsoft Azure Active Directory Sync tool, your credentials must be authenticated. Office 365 uses a CNAME record to point to the correct authentication endpoint for your location, which ensures rapid authentication response times.</span></span>
  
<span data-ttu-id="317ff-p103">Si cet enregistrement CNAME est manquant pour votre domaine, ces applications utiliseront un point de terminaison d'authentification par défaut aux États-Unis, ce qui peut ralentir le processus d'authentification. Si cet enregistrement CNAME n'est pas correctement configuré (par exemple, si la valeur **Adresse de pointage** inclut une coquille), ces applications ne pourront pas s'authentifier.</span><span class="sxs-lookup"><span data-stu-id="317ff-p103">If this CNAME record is missing for your domain, these applications will use a default authentication endpoint in the United States, which means authentication might be slower. If this CNAME record isn't configured properly—for example, if you have a typo in the **Points to address**—these applications won't be able to authenticate.</span></span>
  
 <span data-ttu-id="317ff-114">Si Office 365 les enregistrements **DNS** de votre domaine, Office 365 cet enregistrement CNAME pour vous.</span><span class="sxs-lookup"><span data-stu-id="317ff-114">**If Office 365 manages your domain's DNS records,** Office 365 sets up this CNAME record for you.</span></span> 
  
 <span data-ttu-id="317ff-115">Si vous gérez des enregistrements DNS pour votre domaine sur votre hôte **DNS,** vous créez cet enregistrement vous-même en suivant les instructions pour votre hôte [DNS.](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md)</span><span class="sxs-lookup"><span data-stu-id="317ff-115">**If you are managing DNS records for your domain at your DNS host,** you create this record yourself by [following the instructions for your DNS host](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span>
  
<span data-ttu-id="317ff-116">Si vous planifiez un déploiement Office 365 et que vous souhaitez en savoir plus sur tous les enregistrements DNS que vous devrez peut-être ajouter ou mettre à jour, lisez-les dans Référence : Enregistrements du système de noms de domaine externe pour [Office 365](../../enterprise/external-domain-name-system-records.md).</span><span class="sxs-lookup"><span data-stu-id="317ff-116">If you're planning an Office 365 deployment and want to learn more about all the DNS records that you may need to add or update, read about them in [Reference: External Domain Name System records for Office 365](../../enterprise/external-domain-name-system-records.md).</span></span>
