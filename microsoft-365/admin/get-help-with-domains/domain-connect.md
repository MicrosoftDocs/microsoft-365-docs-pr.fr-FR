---
title: Utilisation de Domain Connect
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
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
ms.assetid: ec6f4bd8-5996-4505-ba68-afaf8a141fb9
description: Découvrez comment travailler avec des bureaux d’enregistrement activés pour Domain Connect et ajouter votre domaine à Microsoft 365.
ms.openlocfilehash: 109255d82100e636e3472242866a519ff64a9e54
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49655611"
---
# <a name="using-domain-connect"></a><span data-ttu-id="8f7c8-103">Utilisation de Domain Connect</span><span class="sxs-lookup"><span data-stu-id="8f7c8-103">Using Domain Connect</span></span>

 <span data-ttu-id="8f7c8-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="8f7c8-105">[Les bureaux ](https://www.domainconnect.org/) d’enregistrement activés pour Domain Connect vous permettent d’ajouter votre domaine à Microsoft 365 au cours d’un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-105">[Domain Connect ](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="8f7c8-106">Dans l’Assistant, nous allons simplement confirmer que vous êtes propriétaire du domaine, puis configurer automatiquement les enregistrements de votre domaine, afin que le courrier électronique soit envoyé à Microsoft 365 et à d’autres services Microsoft 365, tels que Teams, fonctionnent avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-106">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8f7c8-107">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-107">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
## <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="8f7c8-108">Intégration des bureaux d’enregistrement Domain Connect à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8f7c8-108">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="8f7c8-109">1 &amp; 1 IONOS</span><span class="sxs-lookup"><span data-stu-id="8f7c8-109">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="8f7c8-110">123Reg</span><span class="sxs-lookup"><span data-stu-id="8f7c8-110">123Reg</span></span>](https://www.123-reg.co.uk/)
- [<span data-ttu-id="8f7c8-111">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="8f7c8-111">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="8f7c8-112">WordPress</span><span class="sxs-lookup"><span data-stu-id="8f7c8-112">WordPress</span></span>](https://wordpress.com/)
- [<span data-ttu-id="8f7c8-113">Iquésk</span><span class="sxs-lookup"><span data-stu-id="8f7c8-113">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="8f7c8-114">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="8f7c8-114">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="8f7c8-115">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant l’hébergement DNS SecureServer)</span><span class="sxs-lookup"><span data-stu-id="8f7c8-115">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - [<span data-ttu-id="8f7c8-116">Domaines MadDog</span><span class="sxs-lookup"><span data-stu-id="8f7c8-116">MadDog Domains</span></span>](https://www.maddogdomains.com/)
    - [<span data-ttu-id="8f7c8-117">SondesNames</span><span class="sxs-lookup"><span data-stu-id="8f7c8-117">CheapNames</span></span>](https://www.cheapnames.com)

## <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="8f7c8-118">Qu’arrive-t-il à mon courrier électronique et mon site web ?</span><span class="sxs-lookup"><span data-stu-id="8f7c8-118">What happens to my email and website?</span></span>

<span data-ttu-id="8f7c8-119">Une fois que vous avez terminé l’installation, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les messages électroniques de votre domaine commenceront à arriver vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-119">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="8f7c8-120">Assurez-vous d’avoir ajouté des utilisateurs et de configurer des boîtes aux lettres dans Microsoft 365 pour toute personne qui reçoit du courrier électronique sur votre domaine !</span><span class="sxs-lookup"><span data-stu-id="8f7c8-120">Make sure you've added users and set up mailboxes in Microsoft 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="8f7c8-121">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-121">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="8f7c8-122">Les étapes de configuration de Domain Connect n’affectent pas votre site web.</span><span class="sxs-lookup"><span data-stu-id="8f7c8-122">The Domain Connect setup steps don't affect your website.</span></span>
