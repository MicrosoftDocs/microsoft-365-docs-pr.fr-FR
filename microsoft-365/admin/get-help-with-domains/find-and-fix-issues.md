---
title: Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: 40398b0b-bdd0-4afd-ab5e-b5ae6b7990bf
description: Découvrez comment détecter les problèmes que vous rencontrez lors de la configuration d’un domaine personnalisé en vous assurant que les enregistrements DNS sont correctement configurés.
ms.openlocfilehash: a93318d54b950b908319fe50a0cfedefe8586036
ms.sourcegitcommit: 8edad75338cf74712ca1ab5d6631b9b52ff54410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43115971"
---
# <a name="find-and-fix-issues-after-adding-your-domain-or-dns-records-in-office-365"></a><span data-ttu-id="ddff3-103">Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ddff3-103">Find and fix issues after adding your domain or DNS records in Office 365</span></span>

 <span data-ttu-id="ddff3-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ddff3-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ddff3-p101">[] La configuration de votre domaine pour qu'il fonctionne avec Office 365 peut présenter des difficultés. Le système DNS est exigeant et la configuration DNS pour votre domaine a une incidence sur les activités professionnelles importantes, comme le courrier.</span><span class="sxs-lookup"><span data-stu-id="ddff3-p101">Getting your domain set up to work with Office 365 can be challenging. The DNS system is nitpicky to work with, and the DNS setup for your domain affects important business activities, like email!</span></span>

> [!NOTE]
> <span data-ttu-id="ddff3-107">Vous pouvez vérifier les problèmes liés à votre domaine en vérifiant son état.</span><span class="sxs-lookup"><span data-stu-id="ddff3-107">You can check for problems with your domain by checking its status.</span></span> <span data-ttu-id="ddff3-108">Accédez à **configurer** > les**domaines** et affichez les notifications dans la colonne **État** .</span><span class="sxs-lookup"><span data-stu-id="ddff3-108">Go to **Setup** > **Domains** and view the notifications in the **Status** column.</span></span> <span data-ttu-id="ddff3-109">Si vous voyez un problème, sélectionnez autres actions (trois points), puis sélectionnez **vérifier l’intégrité**.</span><span class="sxs-lookup"><span data-stu-id="ddff3-109">If you see an issue, select More actions (three dots), and then choose **Check health**.</span></span> <span data-ttu-id="ddff3-110">Le volet qui s’ouvre décrit tous les problèmes liés à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ddff3-110">The pane that opens will describe any issues occurring with your domain.</span></span>
  
## <a name="whats-going-on"></a><span data-ttu-id="ddff3-111">Que se passe-t-il ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-111">What's going on?</span></span>

- [<span data-ttu-id="ddff3-112">Vous ne pouvez pas vérifier votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-112">Can't verify your domain?</span></span>](#cant-verify-your-domain)
    
- [<span data-ttu-id="ddff3-113">Outlook ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-113">Outlook isn't working?</span></span>](#outlook-isnt-working)
    
- [<span data-ttu-id="ddff3-114">Le courrier de tous les utilisateurs a été basculé vers Office 365 et vous n’avez besoin que de votre courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-114">Everyone's email got switched to Office 365 and you only wanted YOUR email to switch?</span></span>](#everyones-email-got-switched-to-office-365-and-you-only-wanted-your-email-to-switch)

- [<span data-ttu-id="ddff3-115">Vous ne pouvez pas confirmer l’état des comptes scolaires ou scolaires ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-115">Can't confirm non-profit or school account status?</span></span>](#cant-confirm-non-profit-or-school-account-status)

- [<span data-ttu-id="ddff3-116">Les services ne fonctionnent-ils pas avec votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-116">Services not working with your domain?</span></span>](#services-not-working-with-your-domain)
    
- [<span data-ttu-id="ddff3-117">L’accès à votre site Web ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-117">Accessing your website isn't working?</span></span>](#accessing-your-website-isnt-working)

## <a name="cant-verify-your-domain"></a><span data-ttu-id="ddff3-118">Vous ne pouvez pas vérifier votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-118">Can't verify your domain?</span></span>
<span data-ttu-id="ddff3-119"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-119"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="ddff3-120">Plusieurs raisons fréquentes peuvent empêcher le fonctionnement correct de la vérification du domaine :</span><span class="sxs-lookup"><span data-stu-id="ddff3-120">There are a couple of common reasons that domain verification doesn't work as it should:</span></span>
  
1. <span data-ttu-id="ddff3-p103">**La valeur de l'enregistrement de vérification est incorrecte.** Vérifiez que vous avez copié et collé la valeur exacte dans l'enregistrement de vérification TXT configuré auprès de votre hôte DNS. Le problème vient souvent de l'omission de la portion « MS= » de l'enregistrement. Celle-ci est indispensable.</span><span class="sxs-lookup"><span data-stu-id="ddff3-p103">**The verification record value isn't quite correct.** Doublecheck that you've copied and pasted the exact value into the TXT verification record at your DNS host. One common issue is not including the "MS=" part of the record. We need that too!</span></span> 
    
2. <span data-ttu-id="ddff3-p104">**L'enregistrement n'a pas été sauvegardé.** Pour certains hôtes DNS, une étape supplémentaire est nécessaire pour enregistrer le fichier de zone (emplacement de stockage de l'enregistrement DNS) de façon à ce qu'il soit mis à jour sur Internet. Vérifiez que vous avez enregistré vos modifications, pour permettre à Office 365 de consulter et vérifier l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ddff3-p104">**The record hasn't been saved.** At some DNS hosts, you have to take an extra step to save the zone file (where the DNS record is stored) so that it will update across the Internet. Make sure you've saved your changes so Office 365 can see and verify the record.</span></span> 
    
3. <span data-ttu-id="ddff3-128">**L’enregistrement n’a pas été mis à jour sur Internet.**</span><span class="sxs-lookup"><span data-stu-id="ddff3-128">**The record hasn't updated across the Internet.**</span></span> <span data-ttu-id="ddff3-129">En règle générale, il ne prend que quelques minutes pour pouvoir voir le nouvel enregistrement, mais il peut arriver que quelques heures se soient nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ddff3-129">It typically only takes a few minutes for us to be able to see the new record, but occasionally it can take as long as a few hours.</span></span> 
    
## <a name="outlook-isnt-working"></a><span data-ttu-id="ddff3-130">Outlook ne fonctionne pas ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-130">Outlook isn't working?</span></span>
<span data-ttu-id="ddff3-131"><a name="BKMK_OutlookBroken"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-131"><a name="BKMK_OutlookBroken"> </a></span></span>

<span data-ttu-id="ddff3-132">Si vous avez défini votre enregistrement MX et les autres enregistrements DNS correctement pour votre domaine, mais que le courrier ne fonctionne pas, nous pouvons vous aider à [résoudre les problèmes liés à Outlook que vous rencontrez](https://support.office.com/article/b3e740b9-171d-4179-bcd1-e279a363fa75.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddff3-132">If you've set up your MX record and other DNS records correctly for your domain, but mail doesn't work, let us help you [fix your Outlook problems](https://support.office.com/article/b3e740b9-171d-4179-bcd1-e279a363fa75.aspx).</span></span>
  
## <a name="everyones-email-got-switched-to-office-365-and-you-only-wanted-your-email-to-switch"></a><span data-ttu-id="ddff3-133">Le courrier de tous les utilisateurs a été basculé vers Office 365 et vous n’avez besoin que de votre courrier électronique ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-133">Everyone's email got switched to Office 365 and you only wanted YOUR email to switch?</span></span>
<span data-ttu-id="ddff3-134"><a name="BKMK_EmailSwitched"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-134"><a name="BKMK_EmailSwitched"> </a></span></span>

<span data-ttu-id="ddff3-135">Lorsque vous ajoutez votre domaine à Office 365, l’enregistrement MX de votre domaine est généralement mis à jour (par vous-même ou par Office 365) pour pointer vers Office 365 et tous les messages envoyés à ce domaine débuteront dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="ddff3-135">When you add your domain to Office 365, typically your domain's MX record is updated (by you or Office 365) to point to Office 365, and ALL email sent to that domain will start coming to Office 365.</span></span> <span data-ttu-id="ddff3-136">Assurez-vous que vous avez créé des boîtes aux lettres dans Office 365 pour tous les utilisateurs qui disposent d’un courrier électronique sur votre domaine avant de modifier l’enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="ddff3-136">Make sure you've created mailboxes in Office 365 for everyone who has email on your domain BEFORE you change the MX record.</span></span>
  
<span data-ttu-id="ddff3-137">Que faire si vous ne souhaitez pas déplacer le courrier électronique de tous les membres de votre domaine vers Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-137">What if you don't want to move email for everyone on your domain to Office 365?</span></span> <span data-ttu-id="ddff3-138">Vous pouvez prendre des mesures pour [tester Office 365 avec seulement quelques adresses de courrier](https://support.office.com/article/39cee536-6a03-40cf-b9c1-f301bb6001d7.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddff3-138">You can take steps to [pilot Office 365 with just a few email addresses instead](https://support.office.com/article/39cee536-6a03-40cf-b9c1-f301bb6001d7.aspx).</span></span>
  
## <a name="cant-confirm-non-profit-or-school-account-status"></a><span data-ttu-id="ddff3-139">Vous ne pouvez pas confirmer l’état des comptes scolaires ou scolaires ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-139">Can't confirm non-profit or school account status?</span></span>
<span data-ttu-id="ddff3-140"><a name="BKMK_validateAcct"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-140"><a name="BKMK_validateAcct"> </a></span></span>

<span data-ttu-id="ddff3-141">Il existe deux scénarios pour vérifier que le domaine de votre organisation n’a pas été configuré.</span><span class="sxs-lookup"><span data-stu-id="ddff3-141">There are a couple of scenarios when you just need to verify your organization's domain and not set up any services.</span></span> <span data-ttu-id="ddff3-142">Par exemple, pour prouver à Office 365 que votre organisation est qualifiée pour un abonnement scolaire.</span><span class="sxs-lookup"><span data-stu-id="ddff3-142">For example, to prove to Office 365 that your organization qualifies for a school subscription.</span></span>
  
<span data-ttu-id="ddff3-143">Consultez les conseils fournis dans la partie [vérification de votre domaine Office 365 pour prouver le propriétaire, l’organisme ou l’état de l’éducation, ou pour activer Yammer](https://support.office.com/article/87d1844e-aa47-4dc0-a61b-1b773fd4e590) afin de vous assurer que vous avez effectué toutes les étapes requises.</span><span class="sxs-lookup"><span data-stu-id="ddff3-143">Check out the guidance in [Verify your Office 365 domain to prove ownership, nonprofit or education status, or to activate Yammer](https://support.office.com/article/87d1844e-aa47-4dc0-a61b-1b773fd4e590) to make sure you've completed all the required steps.</span></span> <span data-ttu-id="ddff3-144">Il s’agit d’un peu différent pour chaque situation.</span><span class="sxs-lookup"><span data-stu-id="ddff3-144">It's a little different for each situation.</span></span> 
  
## <a name="services-not-working-with-your-domain"></a><span data-ttu-id="ddff3-145">Les services ne fonctionnent pas avec votre domaine ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-145">Services not working with your domain?</span></span>
<span data-ttu-id="ddff3-146"><a name="BKMK_Test"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-146"><a name="BKMK_Test"> </a></span></span>

<span data-ttu-id="ddff3-147">Nous pouvons vous aider à identifier les problèmes liés à la configuration DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ddff3-147">We can help you track down issues with your domain's DNS setup.</span></span> <span data-ttu-id="ddff3-148">L'utilitaire de résolution des problèmes liés aux domaines dans Office 365 vous montre tous les enregistrements nécessitant une résolution et les valeurs devant être affectées aux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="ddff3-148">The domains troubleshooter in Office 365 will show you any records that need fixing, and exactly what the records need to be set to.</span></span> 

> [!TIP]
> <span data-ttu-id="ddff3-p111">Votre DNS est correctement configuré, mais le courrier électronique ne fonctionne pas dans Outlook sur votre ordinateur de bureau ? Découvrez les [différents scénarios de flux de courrier que vous pouvez rencontrer dans Office 365](https://go.microsoft.com/fwlink/?LinkId=787530) pour confirmer que vous avez configuré correctement votre environnement au sein de votre entreprise. Vous pouvez également obtenir de l'aide concernant la résolution des problèmes liés à le courrier dans la page suivante : [Résoudre les problèmes liés à Outlook](https://support.office.com/article/b3e740b9-171d-4179-bcd1-e279a363fa75.aspx).</span><span class="sxs-lookup"><span data-stu-id="ddff3-p111">Got your DNS set up correctly, but mail doesn't work in Outlook on your desktop? Check out the [different mail flow scenarios you can have with Office 365](https://go.microsoft.com/fwlink/?LinkId=787530) to make sure you've got things set up correctly for your business. Or get more troubleshooting help with email here: [Fix Outlook problems](https://support.office.com/article/b3e740b9-171d-4179-bcd1-e279a363fa75.aspx).</span></span> 
  
## <a name="accessing-your-website-isnt-working"></a><span data-ttu-id="ddff3-152">Vous ne parvenez pas à accéder à votre site web ?</span><span class="sxs-lookup"><span data-stu-id="ddff3-152">Accessing your website isn't working?</span></span>
<span data-ttu-id="ddff3-153"><a name="BKMK_Website"> </a></span><span class="sxs-lookup"><span data-stu-id="ddff3-153"><a name="BKMK_Website"> </a></span></span>

<span data-ttu-id="ddff3-154">Si vous avez corrigé tous les problèmes DNS et que vous rencontrez toujours des difficultés, essayez l'une des solutions suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddff3-154">If you've fixed any DNS issues and you're still having trouble, try one of the following.</span></span>
  
- <span data-ttu-id="ddff3-155">Les utilisateurs ne peuvent pas accéder à votre site web à l'adresse www.mondomaine.com : [Identifier les problèmes liés au site web](https://support.office.com/article/61f34ca1-ca7f-4a65-9348-def20db09ddf.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddff3-155">People can't get to your website at www.mydomain.com: [Track down website issues](https://support.office.com/article/61f34ca1-ca7f-4a65-9348-def20db09ddf.aspx)</span></span>
    
- <span data-ttu-id="ddff3-156">Vous ne pouvez pas mettre à jour votre enregistrement A ou CNAME de façon à ce qu'il pointe vers votre site web : [Mettre à jour les enregistrements DNS personnalisés dans Office 365](../dns/add-or-edit-custom-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="ddff3-156">You can't update your A record or CNAME record to point to your website: [Update custom DNS records in Office 365](../dns/add-or-edit-custom-dns-records.md)</span></span>
    
