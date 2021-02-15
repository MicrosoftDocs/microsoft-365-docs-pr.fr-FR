---
title: Rechercher et corriger des problèmes après avoir ajouté votre domaine ou des enregistrements DNS
f1.keywords:
- NOCSH
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
- Adm_TOC
- Adm_O365_Setup
ms.custom:
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 40398b0b-bdd0-4afd-ab5e-b5ae6b7990bf
description: Apprenez à suivre les problèmes que vous avez à résoudre lors de la configuration d’un domaine personnalisé en vous assurez que les enregistrements DNS sont correctement configurer.
ms.openlocfilehash: 786df75f3f8a514e9b3c2a7666d715c9abd082bd
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49926389"
---
# <a name="find-and-fix-issues-after-adding-your-domain-or-dns-records"></a><span data-ttu-id="bc0a1-103">Rechercher et corriger des problèmes après avoir ajouté votre domaine ou des enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="bc0a1-103">Find and fix issues after adding your domain or DNS records</span></span>

 <span data-ttu-id="bc0a1-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="bc0a1-105">La mise en place de votre domaine pour utiliser Microsoft 365 peut être difficile.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-105">Getting your domain set up to work with Microsoft 365 can be challenging.</span></span> <span data-ttu-id="bc0a1-106">Le système DNS est exigeant et la configuration DNS pour votre domaine a une incidence sur les activités professionnelles importantes, comme le courrier.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-106">The DNS system is nitpicky to work with, and the DNS setup for your domain affects important business activities, like email!</span></span>

> [!NOTE]
> <span data-ttu-id="bc0a1-107">Vous pouvez vérifier les problèmes liés à votre domaine en vérifiant son état.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-107">You can check for problems with your domain by checking its status.</span></span> <span data-ttu-id="bc0a1-108">Go to **Setup**  >  **Domains** and view the notifications in the **Status** column.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-108">Go to **Setup** > **Domains** and view the notifications in the **Status** column.</span></span> <span data-ttu-id="bc0a1-109">Si vous voyez un problème, sélectionnez Plus d’actions (trois points), puis **sélectionnez Vérifier l’état d’santé.**</span><span class="sxs-lookup"><span data-stu-id="bc0a1-109">If you see an issue, select More actions (three dots), and then choose **Check health**.</span></span> <span data-ttu-id="bc0a1-110">Le volet qui s’ouvre décrit les problèmes qui se produisent avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-110">The pane that opens will describe any issues occurring with your domain.</span></span>
  
## <a name="whats-going-on"></a><span data-ttu-id="bc0a1-111">Que se passe-t-il ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-111">What's going on?</span></span>

- [<span data-ttu-id="bc0a1-112">Vous ne pouvez pas vérifier votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-112">Can't verify your domain?</span></span>](#cant-verify-your-domain)
    
- [<span data-ttu-id="bc0a1-113">Outlook ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-113">Outlook isn't working?</span></span>](#outlook-isnt-working)
    
- [<span data-ttu-id="bc0a1-114">Tout le monde a basculé vers Microsoft 365 et vous souhaitez que votre courrier électronique bascule uniquement ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-114">Everyone's email got switched to Microsoft 365 and you only wanted YOUR email to switch?</span></span>](#everyones-email-got-switched-to-microsoft-365-and-you-only-wanted-your-email-to-switch)

- [<span data-ttu-id="bc0a1-115">Vous ne pouvez pas confirmer l’état du compte scolaire ou à but non lucratif ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-115">Can't confirm non-profit or school account status?</span></span>](#cant-confirm-non-profit-or-school-account-status)

- [<span data-ttu-id="bc0a1-116">Les services ne fonctionnent pas avec votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-116">Services not working with your domain?</span></span>](#services-not-working-with-your-domain)
    
- [<span data-ttu-id="bc0a1-117">L’accès à votre site web ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-117">Accessing your website isn't working?</span></span>](#accessing-your-website-isnt-working)

## <a name="cant-verify-your-domain"></a><span data-ttu-id="bc0a1-118">Vous ne pouvez pas vérifier votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-118">Can't verify your domain?</span></span>
<span data-ttu-id="bc0a1-119"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-119"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="bc0a1-120">Plusieurs raisons fréquentes peuvent empêcher le fonctionnement correct de la vérification du domaine :</span><span class="sxs-lookup"><span data-stu-id="bc0a1-120">There are a couple of common reasons that domain verification doesn't work as it should:</span></span>
  
1. <span data-ttu-id="bc0a1-p103">**La valeur de l'enregistrement de vérification est incorrecte.** Vérifiez que vous avez copié et collé la valeur exacte dans l'enregistrement de vérification TXT configuré auprès de votre hôte DNS. Le problème vient souvent de l'omission de la portion « MS= » de l'enregistrement. Celle-ci est indispensable.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-p103">**The verification record value isn't quite correct.** Doublecheck that you've copied and pasted the exact value into the TXT verification record at your DNS host. One common issue is not including the "MS=" part of the record. We need that too!</span></span> 
    
2. <span data-ttu-id="bc0a1-125">**L'enregistrement n'a pas été sauvegardé.**</span><span class="sxs-lookup"><span data-stu-id="bc0a1-125">**The record hasn't been saved.**</span></span> <span data-ttu-id="bc0a1-126">Pour certains hôtes DNS, une étape supplémentaire est nécessaire pour enregistrer le fichier de zone (emplacement de stockage de l'enregistrement DNS) de façon à ce qu'il soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-126">At some DNS hosts, you have to take an extra step to save the zone file (where the DNS record is stored) so that it will update across the Internet.</span></span> <span data-ttu-id="bc0a1-127">Vérifiez que vous avez enregistré vos modifications afin que Microsoft 365 puisse voir et vérifier l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-127">Make sure you've saved your changes so Microsoft 365 can see and verify the record.</span></span> 
    
3. <span data-ttu-id="bc0a1-128">**L’enregistrement n’a pas été mis à jour sur Internet.**</span><span class="sxs-lookup"><span data-stu-id="bc0a1-128">**The record hasn't updated across the Internet.**</span></span> <span data-ttu-id="bc0a1-129">En règle générale, nous ne pouvons voir le nouvel enregistrement que quelques minutes, mais cela peut parfois prendre jusqu’à quelques heures.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-129">It typically only takes a few minutes for us to be able to see the new record, but occasionally it can take as long as a few hours.</span></span> 
    
## <a name="outlook-isnt-working"></a><span data-ttu-id="bc0a1-130">Outlook ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-130">Outlook isn't working?</span></span>
<span data-ttu-id="bc0a1-131"><a name="BKMK_OutlookBroken"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-131"><a name="BKMK_OutlookBroken"> </a></span></span>

<span data-ttu-id="bc0a1-132">Si vous avez défini votre enregistrement MX et les autres enregistrements DNS correctement pour votre domaine, mais que le courrier ne fonctionne pas, nous pouvons vous aider à [résoudre les problèmes liés à Outlook que vous rencontrez](https://docs.microsoft.com/exchange/troubleshoot/outlook-connectivity/outlook-connection-issues).</span><span class="sxs-lookup"><span data-stu-id="bc0a1-132">If you've set up your MX record and other DNS records correctly for your domain, but mail doesn't work, let us help you [fix your Outlook problems](https://docs.microsoft.com/exchange/troubleshoot/outlook-connectivity/outlook-connection-issues).</span></span>
  
## <a name="everyones-email-got-switched-to-microsoft-365-and-you-only-wanted-your-email-to-switch"></a><span data-ttu-id="bc0a1-133">Tout le monde a basculé vers Microsoft 365 et vous souhaitez que votre courrier électronique bascule uniquement ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-133">Everyone's email got switched to Microsoft 365 and you only wanted YOUR email to switch?</span></span>
<span data-ttu-id="bc0a1-134"><a name="BKMK_EmailSwitched"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-134"><a name="BKMK_EmailSwitched"> </a></span></span>

<span data-ttu-id="bc0a1-135">Lorsque vous ajoutez votre domaine à Microsoft 365, l’enregistrement MX de votre domaine est généralement mis à jour (par vous ou Microsoft 365) pour pointer vers Microsoft 365, et tous les messages envoyés à ce domaine commencent à arriver vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-135">When you add your domain to Microsoft 365, typically your domain's MX record is updated (by you or Microsoft 365) to point to Microsoft 365, and ALL email sent to that domain will start coming to Microsoft 365.</span></span> <span data-ttu-id="bc0a1-136">Assurez-vous que vous avez créé des boîtes aux lettres dans Microsoft 365 pour toutes les personnes qui ont des messages sur votre domaine avant de modifier l’enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-136">Make sure you've created mailboxes in Microsoft 365 for everyone who has email on your domain BEFORE you change the MX record.</span></span>
  
<span data-ttu-id="bc0a1-137">Que se passe-t-il si vous ne souhaitez pas déplacer le courrier électronique de tous les employés de votre domaine vers Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-137">What if you don't want to move email for everyone on your domain to Microsoft 365?</span></span> <span data-ttu-id="bc0a1-138">Vous pouvez prendre des mesures pour [piloter Microsoft 365 avec seulement quelques adresses de messagerie à la place.](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span><span class="sxs-lookup"><span data-stu-id="bc0a1-138">You can take steps to [pilot Microsoft 365 with just a few email addresses instead](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span></span>
  
## <a name="cant-confirm-non-profit-or-school-account-status"></a><span data-ttu-id="bc0a1-139">Vous ne pouvez pas confirmer l’état du compte scolaire ou à but non lucratif ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-139">Can't confirm non-profit or school account status?</span></span>
<span data-ttu-id="bc0a1-140"><a name="BKMK_validateAcct"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-140"><a name="BKMK_validateAcct"> </a></span></span>

<span data-ttu-id="bc0a1-141">Il existe quelques scénarios où vous devez simplement vérifier le domaine de votre organisation et ne pas configurer de services.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-141">There are a couple of scenarios when you just need to verify your organization's domain and not set up any services.</span></span> <span data-ttu-id="bc0a1-142">Par exemple, pour prouver à Microsoft 365 que votre organisation est éligible pour un abonnement scolaire.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-142">For example, to prove to Microsoft 365 that your organization qualifies for a school subscription.</span></span>
  
<span data-ttu-id="bc0a1-143">Consultez les instructions dans Vérifier votre domaine [Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq) pour prouver la propriété, l’état des organisations à but non lucratif ou de l’éducation, ou pour activer Yammer pour vous assurer que vous avez effectué toutes les étapes requises.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-143">Check out the guidance in [Verify your Microsoft 365 domain to prove ownership, nonprofit or education status, or to activate Yammer](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq) to make sure you've completed all the required steps.</span></span> <span data-ttu-id="bc0a1-144">Il est légèrement différent pour chaque situation.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-144">It's a little different for each situation.</span></span> 
  
## <a name="services-not-working-with-your-domain"></a><span data-ttu-id="bc0a1-145">Les services ne fonctionnent pas avec votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-145">Services not working with your domain?</span></span>
<span data-ttu-id="bc0a1-146"><a name="BKMK_Test"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-146"><a name="BKMK_Test"> </a></span></span>

<span data-ttu-id="bc0a1-147">Nous pouvons vous aider à identifier les problèmes liés à la configuration DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-147">We can help you track down issues with your domain's DNS setup.</span></span> <span data-ttu-id="bc0a1-148">L’dépannage des domaines dans Microsoft 365 vous montre tous les enregistrements qui doivent être corrigés et indique exactement ce que les enregistrements doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-148">The domains troubleshooter in Microsoft 365 will show you any records that need fixing, and exactly what the records need to be set to.</span></span> 

> [!TIP]
> <span data-ttu-id="bc0a1-149">Votre DNS est correctement configuré, mais le courrier électronique ne fonctionne pas dans Outlook sur votre ordinateur de bureau ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-149">Got your DNS set up correctly, but mail doesn't work in Outlook on your desktop?</span></span> <span data-ttu-id="bc0a1-150">Consultez les différents scénarios de flux de messagerie que vous pouvez avoir avec [Microsoft 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/mail-flow-best-practices) pour vous assurer que les choses sont correctement définies pour votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-150">Check out the [different mail flow scenarios you can have with Microsoft 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/mail-flow-best-practices) to make sure you've got things set up correctly for your business.</span></span> <span data-ttu-id="bc0a1-151">Vous pouvez également obtenir de l'aide concernant la résolution des problèmes liés à le courrier dans la page suivante : [Résoudre les problèmes liés à Outlook](https://docs.microsoft.com/exchange/troubleshoot/outlook-connectivity/outlook-connection-issues).</span><span class="sxs-lookup"><span data-stu-id="bc0a1-151">Or get more troubleshooting help with email here: [Fix Outlook problems](https://docs.microsoft.com/exchange/troubleshoot/outlook-connectivity/outlook-connection-issues).</span></span> 
  
## <a name="accessing-your-website-isnt-working"></a><span data-ttu-id="bc0a1-152">Vous ne parvenez pas à accéder à votre site web ?</span><span class="sxs-lookup"><span data-stu-id="bc0a1-152">Accessing your website isn't working?</span></span>
<span data-ttu-id="bc0a1-153"><a name="BKMK_Website"> </a></span><span class="sxs-lookup"><span data-stu-id="bc0a1-153"><a name="BKMK_Website"> </a></span></span>

<span data-ttu-id="bc0a1-154">Si vous avez corrigé tous les problèmes DNS et que vous rencontrez toujours des difficultés, essayez l'une des solutions suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc0a1-154">If you've fixed any DNS issues and you're still having trouble, try one of the following.</span></span>
  
- <span data-ttu-id="bc0a1-155">Les utilisateurs ne peuvent pas accéder à votre site web à l'adresse www.mondomaine.com : [Identifier les problèmes liés au site web](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain)</span><span class="sxs-lookup"><span data-stu-id="bc0a1-155">People can't get to your website at www.mydomain.com: [Track down website issues](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain)</span></span>
    
- <span data-ttu-id="bc0a1-156">Vous ne pouvez pas mettre à jour votre enregistrement A ou CNAME pour qu’il pointe vers votre site web : mettre à jour des enregistrements DNS personnalisés [dans Microsoft 365](../dns/add-or-edit-custom-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="bc0a1-156">You can't update your A record or CNAME record to point to your website: [Update custom DNS records in Microsoft 365](../dns/add-or-edit-custom-dns-records.md)</span></span>

## <a name="related-content"></a><span data-ttu-id="bc0a1-157">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="bc0a1-157">Related content</span></span>

[<span data-ttu-id="bc0a1-158">Résolution des problèmes : données d’audit sur la modification vérifiée du domaine</span><span class="sxs-lookup"><span data-stu-id="bc0a1-158">Troubleshoot: Audit data on verified domain change</span></span>](https://docs.microsoft.com/azure/active-directory/reports-monitoring/troubleshoot-audit-data-verified-domain)

    
