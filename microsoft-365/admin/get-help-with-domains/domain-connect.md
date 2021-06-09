---
title: Utilisation du domaine Connecter
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
description: Découvrez comment travailler avec les bureaux d’Connecter bureaux d’enregistrement activés et ajouter votre domaine à Microsoft 365.
ms.openlocfilehash: 5dec69f70273e6a9430ce5926ed07888e197adcd
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51860654"
---
# <a name="using-domain-connect"></a><span data-ttu-id="af990-103">Utilisation du domaine Connecter</span><span class="sxs-lookup"><span data-stu-id="af990-103">Using Domain Connect</span></span>

 <span data-ttu-id="af990-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="af990-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="af990-105">[Les Connecter](https://www.domainconnect.org/) bureaux d’enregistrement activés vous permettent d’ajouter votre domaine à Microsoft 365 dans un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="af990-105">[Domain Connect ](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="af990-106">Dans l’Assistant, nous allons simplement confirmer que vous êtes propriétaire du domaine, puis configurer automatiquement les enregistrements de votre domaine, afin que le courrier électronique soit envoyé à Microsoft 365 et d’autres services Microsoft 365, tels que Teams, fonctionnent avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="af990-106">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="af990-107">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="af990-107">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
## <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="af990-108">Intégration Connecter bureaux d’enregistrement de domaines Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="af990-108">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="af990-109">1 &amp; 1 IONOS</span><span class="sxs-lookup"><span data-stu-id="af990-109">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="af990-110">123Reg</span><span class="sxs-lookup"><span data-stu-id="af990-110">123Reg</span></span>](https://www.123-reg.co.uk/)
- [<span data-ttu-id="af990-111">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="af990-111">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="af990-112">WordPress</span><span class="sxs-lookup"><span data-stu-id="af990-112">WordPress</span></span>](https://wordpress.com/)
- [<span data-ttu-id="af990-113">Iquésk</span><span class="sxs-lookup"><span data-stu-id="af990-113">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="af990-114">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="af990-114">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="af990-115">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant l’hébergement DNS SecureServer)</span><span class="sxs-lookup"><span data-stu-id="af990-115">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - [<span data-ttu-id="af990-116">Hébergement web MadDog</span><span class="sxs-lookup"><span data-stu-id="af990-116">MadDog Web Hosting</span></span>](https://maddogwebhosting.com/domains/)
    - [<span data-ttu-id="af990-117">SondesNames</span><span class="sxs-lookup"><span data-stu-id="af990-117">CheapNames</span></span>](https://www.cheapnames.com)

## <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="af990-118">Qu’arrive-t-il à mon courrier électronique et mon site web ?</span><span class="sxs-lookup"><span data-stu-id="af990-118">What happens to my email and website?</span></span>

<span data-ttu-id="af990-119">Une fois l’installation terminé, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les e-mails de votre domaine commenceront à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="af990-119">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="af990-120">Assurez-vous d’avoir ajouté des utilisateurs et de configurer des boîtes aux lettres dans Microsoft 365 pour toutes les personnes qui reçoit du courrier électronique sur votre domaine !</span><span class="sxs-lookup"><span data-stu-id="af990-120">Make sure you've added users and set up mailboxes in Microsoft 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="af990-121">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="af990-121">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="af990-122">Les étapes de Connecter domaine n’affectent pas votre site web.</span><span class="sxs-lookup"><span data-stu-id="af990-122">The Domain Connect setup steps don't affect your website.</span></span>
