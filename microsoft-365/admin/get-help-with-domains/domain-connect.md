---
title: Utilisation de la connexion au domaine
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
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
description: Découvrez comment travailler avec les bureaux d’accès de Domain Connect activés et ajouter votre domaine à Microsoft 365.
ms.openlocfilehash: 70a30201d4b795c7458959b6b2eee14c9b3c7186
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399955"
---
# <a name="using-domain-connect"></a><span data-ttu-id="5bcf1-103">Utilisation de la connexion au domaine</span><span class="sxs-lookup"><span data-stu-id="5bcf1-103">Using Domain Connect</span></span>

 <span data-ttu-id="5bcf1-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="5bcf1-105">Les bureaux d’accès activés pour la [connexion au domaine](https://www.domainconnect.org/) vous permettent d’ajouter votre domaine à Microsoft 365 dans un processus en trois étapes qui prend quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-105">[Domain Connect ](https://www.domainconnect.org/) enabled registrars let you add your domain to Microsoft 365 in a three-step process that takes minutes.</span></span> 
  
<span data-ttu-id="5bcf1-106">Dans l’Assistant, nous confirmons que vous êtes propriétaire du domaine, puis vous configurez automatiquement les enregistrements de votre domaine, de sorte que le courrier électronique est envoyé à Microsoft 365 et d’autres services Microsoft 365, comme Teams, travaillez avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-106">In the wizard, we'll just confirm that you own the domain, and then automatically set up your domain's records, so email comes to Microsoft 365 and other Microsoft 365 services, like Teams, work with your domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5bcf1-107">Veillez à désactiver les bloqueurs de fenêtres contextuelles dans votre navigateur avant de démarrer l'Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-107">Make sure you disable any popup blockers in your browser before you start the setup wizard.</span></span>
  
## <a name="domain-connect-registrars-integrating-with-microsoft-365"></a><span data-ttu-id="5bcf1-108">Bureaux de connexion au domaine intégration à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5bcf1-108">Domain Connect registrars integrating with Microsoft 365</span></span>

- [<span data-ttu-id="5bcf1-109">1 &amp; 1 Ionos</span><span class="sxs-lookup"><span data-stu-id="5bcf1-109">1&amp;1 IONOS</span></span>](https://www.1and1.com/)
- [<span data-ttu-id="5bcf1-110">123Reg</span><span class="sxs-lookup"><span data-stu-id="5bcf1-110">123Reg</span></span>](https://www.123-reg.co.uk/)
- [<span data-ttu-id="5bcf1-111">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="5bcf1-111">GoDaddy</span></span>](https://www.godaddy.com/)
- [<span data-ttu-id="5bcf1-112">WordPress</span><span class="sxs-lookup"><span data-stu-id="5bcf1-112">WordPress</span></span>](https://wordpress.com/)
- [<span data-ttu-id="5bcf1-113">Plesk</span><span class="sxs-lookup"><span data-stu-id="5bcf1-113">Plesk</span></span>](https://www.plesk.com/)
- [<span data-ttu-id="5bcf1-114">MediaTemple</span><span class="sxs-lookup"><span data-stu-id="5bcf1-114">MediaTemple</span></span>](https://mediatemple.net/)
- <span data-ttu-id="5bcf1-115">SecureServer ou WildWestDomains (revendeurs GoDaddy utilisant SecureServer hébergement DNS)</span><span class="sxs-lookup"><span data-stu-id="5bcf1-115">SecureServer or WildWestDomains (GoDaddy resellers using SecureServer DNS hosting)</span></span>
    - [<span data-ttu-id="5bcf1-116">Domaines MadDog</span><span class="sxs-lookup"><span data-stu-id="5bcf1-116">MadDog Domains</span></span>](https://www.maddogdomains.com/)
    - [<span data-ttu-id="5bcf1-117">CheapNames</span><span class="sxs-lookup"><span data-stu-id="5bcf1-117">CheapNames</span></span>](https://www.cheapnames.com)

## <a name="what-happens-to-my-email-and-website"></a><span data-ttu-id="5bcf1-118">Qu’arrive-t-il à mon courrier électronique et à mon site Web ?</span><span class="sxs-lookup"><span data-stu-id="5bcf1-118">What happens to my email and website?</span></span>

<span data-ttu-id="5bcf1-119">Une fois que vous avez terminé l’installation, l’enregistrement MX de votre domaine est mis à jour pour pointer vers Microsoft 365 et tous les messages électroniques pour votre domaine vont débuter vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-119">After you finish setup, the MX record for your domain is updated to point to Microsoft 365 and all email for your domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="5bcf1-120">Vérifiez que vous avez ajouté les utilisateurs et configuré les boîtes aux lettres dans Office 365 de toutes les personnes qui reçoivent du courrier électronique sur votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-120">Make sure you've added users and set up mailboxes in Office 365 for everyone who gets email on your domain!</span></span>
  
<span data-ttu-id="5bcf1-121">Si vous avez un site web que vous utilisez dans le cadre de votre activité, il continuera à fonctionner là où il se trouve.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-121">If you have a website that you use with your business, it will keep working where it is.</span></span> <span data-ttu-id="5bcf1-122">Les étapes de configuration de la connexion au domaine n’affectent pas votre site Web.</span><span class="sxs-lookup"><span data-stu-id="5bcf1-122">The Domain Connect setup steps don't affect your website.</span></span>
