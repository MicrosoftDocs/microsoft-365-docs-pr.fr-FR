---
title: À quoi sert l'enregistrement CNAME Office 365 pour MSOID ?
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.collection:
- Adm_O365
- Adm_NonTOC
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- BCS160
- MET150
- MOE150
ROBOTS: NOINDEX
description: Pour plus d’informations sur l’enregistrement CNAMe « MSOID » dans Office 365 qui vous dirige vers le meilleur serveur pour les processus d’authentification, vous allez obtenir une réponse plus rapide.
monikerRange: o365-21vianet
ms.openlocfilehash: f5369b8a723c60691da0e73f2bd8cc32233abbcd
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43212220"
---
# <a name="whats-the-purpose-of-the-office-365-cname-record-for-msoid"></a><span data-ttu-id="a3d75-103">À quoi sert l'enregistrement CNAME Office 365 pour MSOID ?</span><span class="sxs-lookup"><span data-stu-id="a3d75-103">What's the purpose of the Office 365 CNAME record for MSOID?</span></span>

 <span data-ttu-id="a3d75-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a3d75-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
> [!NOTE]
> <span data-ttu-id="a3d75-105">Le code suivant s’applique uniquement à \* \* Office 365 géré par 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="a3d75-105">The following only Applies to \*\*Office 365 operated by 21Vianet.</span></span>
  
<span data-ttu-id="a3d75-p101">Vous vous demandez peut-être pourquoi vous devez ajouter l'enregistrement CNAME « MSOID » dans Office 365. Cet enregistrement doit être ajouté pour tous les domaines personnalisés, quel que soit l'abonnement que vous utilisez. Pourquoi en avez-vous besoin ? Il s'agit d'un aspect un peu technique. Grosso modo, cet enregistrement vous permet d'être redirigé vers le meilleur serveur pour certains processus d'authentification, afin de recevoir une réponse plus rapide.</span><span class="sxs-lookup"><span data-stu-id="a3d75-p101">You may wonder why you need to add the "MSOID" CNAME record in Office 365. This is a record that has to be added for all custom domains, no matter which subscription you use. Why do you need it? It's a little technical, but essentially, it's so that you'll be directed to the best server for certain authentication processes, so you'll get faster response.</span></span>
  
<span data-ttu-id="a3d75-p102">Informations techniques : lorsque vous exécutez une application cliente compatible avec Office 365, telle que Skype Entreprise Online, Outlook, Windows PowerShell ou l'outil de synchronisation Microsoft Azure Azure Active Directory, vos informations d'identification doivent être authentifiées. Office 365 utilise un enregistrement CNAME pour pointer vers le point de terminaison d'authentification correct pour votre emplacement, ce qui garantit des temps de réponse d'authentification rapides.</span><span class="sxs-lookup"><span data-stu-id="a3d75-p102">Technical details: When you run a client application that works with Office 365 such as Skype for Business Online, Outlook, Windows PowerShell or Microsoft Azure Active Directory Sync tool, your credentials must be authenticated. Office 365 uses a CNAME record to point to the correct authentication endpoint for your location, which ensures rapid authentication response times.</span></span>
  
<span data-ttu-id="a3d75-p103">Si cet enregistrement CNAME est manquant pour votre domaine, ces applications utiliseront un point de terminaison d'authentification par défaut aux États-Unis, ce qui peut ralentir le processus d'authentification. Si cet enregistrement CNAME n'est pas correctement configuré (par exemple, si la valeur **Adresse de pointage** inclut une coquille), ces applications ne pourront pas s'authentifier.</span><span class="sxs-lookup"><span data-stu-id="a3d75-p103">If this CNAME record is missing for your domain, these applications will use a default authentication endpoint in the United States, which means authentication might be slower. If this CNAME record isn't configured properly—for example, if you have a typo in the **Points to address**—these applications won't be able to authenticate.</span></span>
  
 <span data-ttu-id="a3d75-114">**Si Office 365 gère les enregistrements DNS de votre domaine,** Office 365 configure cet enregistrement CNAMe pour vous.</span><span class="sxs-lookup"><span data-stu-id="a3d75-114">**If Office 365 manages your domain's DNS records,** Office 365 sets up this CNAME record for you.</span></span> 
  
 <span data-ttu-id="a3d75-115">**Si vous gérez des enregistrements DNS pour votre domaine au niveau de votre hôte DNS,** vous pouvez créer cet enregistrement vous-même en [suivant les instructions de votre hôte DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23.aspx).</span><span class="sxs-lookup"><span data-stu-id="a3d75-115">**If you are managing DNS records for your domain at your DNS host,** you create this record yourself by [following the instructions for your DNS host](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23.aspx).</span></span>
  
<span data-ttu-id="a3d75-116">Si vous planifiez un déploiement d’Office 365 et que vous souhaitez en savoir plus sur tous les enregistrements DNS que vous aurez peut-être besoin d’ajouter ou de mettre à jour, lisez les informations à ce sujet dans la [référence : enregistrements DNS externes pour Office 365](https://go.microsoft.com/fwlink/?LinkId=579013).</span><span class="sxs-lookup"><span data-stu-id="a3d75-116">If you're planning an Office 365 deployment and want to learn more about all the DNS records that you may need to add or update, read about them in [Reference: External Domain Name System records for Office 365](https://go.microsoft.com/fwlink/?LinkId=579013).</span></span>
  

