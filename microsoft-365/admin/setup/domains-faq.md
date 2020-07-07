---
title: Forum aux questions sur les domaines
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
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 1272bad0-4bd4-4796-8005-67d6fb3afc5a
description: Pour en savoir plus sur les domaines, trouvez des réponses à vos questions fréquemment posées.
ms.openlocfilehash: 093125d1652355fbd9b624e1f15b5858fd586301
ms.sourcegitcommit: 7c1b34205746ff0690ffc774a74bdfd434256cf5
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "45049735"
---
# <a name="domains-faq"></a><span data-ttu-id="4f33f-103">Forum aux questions sur les domaines</span><span class="sxs-lookup"><span data-stu-id="4f33f-103">Domains FAQ</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="4f33f-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="4f33f-104">The admin center is changing.</span></span> <span data-ttu-id="4f33f-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="4f33f-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="4f33f-106">Cet article contient des réponses aux questions fréquemment posées à propos des domaines dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-106">This article contains answers to frequently asked questions about domains in Microsoft 365.</span></span>

<span data-ttu-id="4f33f-107">Si vous ne trouvez pas la réponse à votre question, laissez-nous un commentaire et nous l'ajouterons à la liste.</span><span class="sxs-lookup"><span data-stu-id="4f33f-107">If you can't find an answer to your question, let us know by leaving a comment and we'll add it to the list.</span></span>

<span data-ttu-id="4f33f-108">Contenu de cet article</span><span class="sxs-lookup"><span data-stu-id="4f33f-108">In this article</span></span>

<span data-ttu-id="4f33f-109">[Qu’est-ce que la priorité MX ?](#what-is-mx-priority) 
 [Comment puis-je valider des enregistrements SPF pour mon domaine ?](#how-can-i-validate-spf-records-for-my-domain) 
 [Qu’est-ce qu’un nom de domaine ?](#what-is-a-domain-name) 
 [Que se passe-t-il si mon fournisseur DNS ne prend pas en charge certains types d’enregistrements ?](#what-happens-if-my-dns-provider-doesnt-support-certain-record-types) 
 [Comment définir ou modifier le domaine par défaut dans Microsoft 365 ?](#how-do-i-set-or-change-the-default-domain-in-microsoft-365) 
 [Puis-je ajouter des sous-domaines personnalisés ou plusieurs domaines à Microsoft 365 ?](#can-i-add-custom-subdomains-or-multiple-domains-to-microsoft-365) 
 [Pourquoi ai-je un domaine « onmicrosoft.com » ?](#why-do-i-have-an-onmicrosoftcom-domain) 
 [Pourquoi ai-je un domaine « onmicrosoft.de » ?](#why-do-i-have-an-onmicrosoftde-domain) 
 [Comment puis-je vérifier mon statut de l’organisme ou de l’éducation ?](#how-do-i-verify-my-nonprofit-or-education-status)</span><span class="sxs-lookup"><span data-stu-id="4f33f-109">[What is MX priority?](#what-is-mx-priority)
[How can I validate SPF records for my domain?](#how-can-i-validate-spf-records-for-my-domain)
[What is a domain name?](#what-is-a-domain-name)
[What happens if my DNS provider doesn't support certain record types?](#what-happens-if-my-dns-provider-doesnt-support-certain-record-types)
[How do I set or change the default domain in Microsoft 365?](#how-do-i-set-or-change-the-default-domain-in-microsoft-365)
[Can I add custom subdomains or multiple domains to Microsoft 365?](#can-i-add-custom-subdomains-or-multiple-domains-to-microsoft-365)
[Why do I have an "onmicrosoft.com" domain?](#why-do-i-have-an-onmicrosoftcom-domain)
[Why do I have an "onmicrosoft.de" domain?](#why-do-i-have-an-onmicrosoftde-domain)
[How do I verify my nonprofit or education status?](#how-do-i-verify-my-nonprofit-or-education-status)</span></span>
    
## <a name="what-is-mx-priority"></a><span data-ttu-id="4f33f-110">Quelle est la priorité MX ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-110">What is MX priority?</span></span>

<span data-ttu-id="4f33f-111">Le courrier électronique est remis au serveur Exchange de messagerie avec le numéro de préférence le plus bas (priorité la plus élevée), de sorte que l’enregistrement MX que vous utilisez pour le routage du courrier doit avoir le numéro de préférence le plus bas, généralement 0 ou *une priorité élevée* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-111">Mail is delivered to the mail exchange server with the lowest preference number (highest priority), so the MX record you use for mail routing should have the lowest preference number, typically 0 or  *High*  priority.</span></span> 
  
- <span data-ttu-id="4f33f-112">Lorsque vous créez un enregistrement MX, la plupart des fournisseurs d’hébergement DNS exigent que vous définiez le numéro de préférence.</span><span class="sxs-lookup"><span data-stu-id="4f33f-112">When you create an MX record, most DNS hosting providers require you to set the preference number.</span></span>
    
- <span data-ttu-id="4f33f-113">Une étiquette la *préférence* de zone, et une étiquette la *priorité* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-113">Some label the box  *preference*  , and some label it  *priority*  .</span></span> 
    
- <span data-ttu-id="4f33f-114">Certains nécessitent un numéro et d’autres vous demandent de sélectionner *faible* , *moyen* ou *élevé* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-114">Some require a number, and some ask you to select  *Low*  ,  *Medium*  , or  *High*  .</span></span> 
    
- <span data-ttu-id="4f33f-115">Si vous n’avez qu’un seul enregistrement MX, la valeur de Priority ou preference est correcte.</span><span class="sxs-lookup"><span data-stu-id="4f33f-115">If you only have one MX record, any value is fine for priority or preference.</span></span>
    
- <span data-ttu-id="4f33f-116">Si vous en avez plusieurs, assurez-vous que l’enregistrement MX pour le routage du courrier est de priorité supérieure à celle utilisée pour valider le fait que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="4f33f-116">If you have more than one, make sure the MX record for mail routing is higher priority than the one used for validating that you own the domain.</span></span>
    
## <a name="how-can-i-validate-spf-records-for-my-domain"></a><span data-ttu-id="4f33f-117">Comment puis-je valider des enregistrements SPF pour mon domaine ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-117">How can I validate SPF records for my domain?</span></span>

<span data-ttu-id="4f33f-118">Il est important de disposer ou de créer **un seul enregistrement txt pour SPF**.</span><span class="sxs-lookup"><span data-stu-id="4f33f-118">It's important that you have or create  **only one TXT record for SPF**.</span></span> <span data-ttu-id="4f33f-119">Si vous disposez déjà d’un enregistrement SPF, vous devez ajouter les nouvelles valeurs Microsoft 365 à ce dernier, plutôt que d’en créer un.</span><span class="sxs-lookup"><span data-stu-id="4f33f-119">If you already have an SPF record, you should append the new Microsoft 365 values to it, rather than create a new one.</span></span> <span data-ttu-id="4f33f-120">Une fois que vous avez ajouté ou mis à jour votre enregistrement SPF pour le courrier électronique Microsoft, vous devez vérifier que la syntaxe est correcte avec l’un des outils suivants :</span><span class="sxs-lookup"><span data-stu-id="4f33f-120">After you've added or updated your SPF record for Microsoft email, you should check to make sure that the syntax is correct with one of these tools:</span></span> 
  
- [<span data-ttu-id="4f33f-121">Outils de test de l’enregistrement SPF</span><span class="sxs-lookup"><span data-stu-id="4f33f-121">SPF Record Testing Tools</span></span>](http://www.kitterman.com/spf/validate.html)
    
- [<span data-ttu-id="4f33f-122">Enquêteur SPF</span><span class="sxs-lookup"><span data-stu-id="4f33f-122">SPF Surveyor</span></span>](https://dmarcian.com/spf-survey/)
    
- [<span data-ttu-id="4f33f-123">Explorer l’interface Web</span><span class="sxs-lookup"><span data-stu-id="4f33f-123">Dig web interface</span></span>](http://digwebinterface.com/)

## <a name="what-is-a-domain-name"></a><span data-ttu-id="4f33f-124">Qu’est-ce qu’un nom de domaine ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-124">What is a domain name?</span></span>

<span data-ttu-id="4f33f-125">[] Un domaine est un nom unique qui apparaît après le signe **@** dans les adresses de messagerie et après **www.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-125">A domain is a unique name that appears after the **@** sign in email addresses, and after **www.**</span></span> <span data-ttu-id="4f33f-126">dans les adresses web.</span><span class="sxs-lookup"><span data-stu-id="4f33f-126">in web addresses.</span></span> <span data-ttu-id="4f33f-127">Il prend généralement la forme du nom de votre organisation et d’un suffixe Internet standard, tel que *yourbusiness.com* ou *stateuniversity.edu.*</span><span class="sxs-lookup"><span data-stu-id="4f33f-127">It typically takes the form of your organization's name and a standard Internet suffix, such as  *yourbusiness.com*  or  *stateuniversity.edu.*</span></span> 
  
<span data-ttu-id="4f33f-128">L’utilisation d’un domaine personnalisé comme «**rob \@ contoso.com**» avec Microsoft 365 peut vous aider à créer une crédibilité et une reconnaissance pour votre marque.</span><span class="sxs-lookup"><span data-stu-id="4f33f-128">Using a custom domain like "**rob\@contoso.com**" with Microsoft 365 can help build credibility and recognition for your brand.</span></span> 
  
<span data-ttu-id="4f33f-129">Vous pouvez [acheter un domaine dans Microsoft 365 et nous allons le configurer automatiquement](../get-help-with-domains/buy-a-domain-name.md), ou vous pouvez acheter ou en disposer un dont vous êtes déjà propriétaire auprès d’un bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="4f33f-129">You can [buy a domain in Microsoft 365 and we'll set it up automatically](../get-help-with-domains/buy-a-domain-name.md), or you can buy or bring one you already own from a domain registrar.</span></span>
    
## <a name="what-happens-if-my-dns-provider-doesnt-support-certain-record-types"></a><span data-ttu-id="4f33f-130">Que se passe-t-il si mon fournisseur DNS ne prend pas en charge certains types d’enregistrements ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-130">What happens if my DNS provider doesn't support certain record types?</span></span>

<span data-ttu-id="4f33f-131">Si vous gérez vos propres enregistrements DNS et que votre hôte DNS ne prend pas en charge tous les enregistrements DNS dont Microsoft 365 a besoin, certaines fonctionnalités de Microsoft 365 ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="4f33f-131">If you manage your own DNS records and your DNS host does not support all the DNS records that Microsoft 365 needs, some Microsoft 365 features won't work.</span></span> <span data-ttu-id="4f33f-132">Nous vous recommandons de transférer votre domaine vers un serveur d’inscriptions qui prend en charge tous les enregistrements DNS requis.</span><span class="sxs-lookup"><span data-stu-id="4f33f-132">We recommend that you transfer your domain to a registrar that supports all required DNS records.</span></span>
  
<span data-ttu-id="4f33f-133">Fournisseurs qui prennent en charge tous les enregistrements DNS requis :</span><span class="sxs-lookup"><span data-stu-id="4f33f-133">Providers that support all required DNS records:</span></span>
  
- <span data-ttu-id="4f33f-134">Dynadot</span><span class="sxs-lookup"><span data-stu-id="4f33f-134">Dynadot</span></span>
    
- <span data-ttu-id="4f33f-135">Auprès enomcentral</span><span class="sxs-lookup"><span data-stu-id="4f33f-135">eNomCentral</span></span>
    
- <span data-ttu-id="4f33f-136">Europe Registry</span><span class="sxs-lookup"><span data-stu-id="4f33f-136">Europe Registry</span></span>
    
- <span data-ttu-id="4f33f-137">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="4f33f-137">GoDaddy</span></span>
    
- <span data-ttu-id="4f33f-138">Sensitiv</span><span class="sxs-lookup"><span data-stu-id="4f33f-138">Hover</span></span>
    
- <span data-ttu-id="4f33f-139">MyHosting.com</span><span class="sxs-lookup"><span data-stu-id="4f33f-139">MyHosting.com</span></span>
    
- <span data-ttu-id="4f33f-140">Name.com</span><span class="sxs-lookup"><span data-stu-id="4f33f-140">Name.com</span></span>
    
- <span data-ttu-id="4f33f-141">Voix presque gratuite</span><span class="sxs-lookup"><span data-stu-id="4f33f-141">Nearly Free Speech</span></span>
    
- <span data-ttu-id="4f33f-142">Nettica</span><span class="sxs-lookup"><span data-stu-id="4f33f-142">Nettica</span></span>
    
- <span data-ttu-id="4f33f-143">Network Information Center (NIC)</span><span class="sxs-lookup"><span data-stu-id="4f33f-143">Network Information Center (NIC)</span></span>
    
- <span data-ttu-id="4f33f-144">Network Solutions</span><span class="sxs-lookup"><span data-stu-id="4f33f-144">Network Solutions</span></span>
    
- <span data-ttu-id="4f33f-145">Register.com</span><span class="sxs-lookup"><span data-stu-id="4f33f-145">Register.com</span></span>
  
## <a name="how-do-i-set-or-change-the-default-domain-in-microsoft-365"></a><span data-ttu-id="4f33f-146">Comment définir ou modifier le domaine par défaut dans Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-146">How do I set or change the default domain in Microsoft 365?</span></span>

<span data-ttu-id="4f33f-147">Vous devez avoir au moins un domaine personnalisé que vous avez ajouté à Microsoft 365 avant de pouvoir choisir un domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f33f-147">You must have at least one custom domain that you've added to Microsoft 365 before you can choose a default domain.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4f33f-148">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="4f33f-148">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4f33f-149">Dans le centre d’administration, accédez à la page **Paramètres** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="4f33f-149">In the admin center, go to the **Settings** > <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4f33f-150">Dans le centre d’administration, accédez à la page **Paramètres** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="4f33f-150">In the admin center, go to the **Settings** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
    
2. <span data-ttu-id="4f33f-151">Dans la page **domaines** , sélectionnez le domaine que vous souhaitez définir par défaut pour les nouvelles adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4f33f-151">On the **Domains** page, select the domain you want to set as the default for new email addresses.</span></span> 
    
3. <span data-ttu-id="4f33f-152">Sélectionnez **Définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="4f33f-152">Select **Set as default**.</span></span>
    
::: moniker range="o365-worldwide"

<span data-ttu-id="4f33f-153">Vous ne pouvez pas modifier le nom de votre domaine initial *. onmicrosoft.com* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-153">You cannot change the name of your initial  *.onmicrosoft.com*  domain.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="4f33f-154">Vous ne pouvez pas modifier le nom de votre domaine initial *. onmicrosoft.de* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-154">You cannot change the name of your initial  *.onmicrosoft.de*  domain.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="4f33f-155">Vous ne pouvez pas modifier le nom de votre domaine initial *. Partner.onmschina.CN* .</span><span class="sxs-lookup"><span data-stu-id="4f33f-155">You cannot change the name of your initial  *.partner.onmschina.cn*  domain.</span></span> 

::: moniker-end

## <a name="can-i-add-custom-subdomains-or-multiple-domains-to-microsoft-365"></a><span data-ttu-id="4f33f-156">Puis-je ajouter des sous-domaines personnalisés ou plusieurs domaines à Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-156">Can I add custom subdomains or multiple domains to Microsoft 365?</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="4f33f-157">Oui.</span><span class="sxs-lookup"><span data-stu-id="4f33f-157">Yes.</span></span> <span data-ttu-id="4f33f-158">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="4f33f-158">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="4f33f-159">Si vous autorisez Microsoft à gérer vos paramètres DNS avec des enregistrements NS, ou si vous avez acheté le domaine auprès de Microsoft, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="4f33f-159">If you are letting Microsoft manage your DNS settings with NS records, or if you bought the domain from Microsoft, you can't add subdomains.</span></span>

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="4f33f-160">OK!</span><span class="sxs-lookup"><span data-stu-id="4f33f-160">Yes!</span></span> <span data-ttu-id="4f33f-161">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="4f33f-161">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="4f33f-162">Si vous autorisez Microsoft à gérer vos paramètres DNS avec des enregistrements NS, ou si vous avez acheté le domaine auprès de Microsoft, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="4f33f-162">If you are letting Microsoft manage your DNS settings with NS records, or if you bought the domain from Microsoft, you can't add subdomains.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="4f33f-163">OK!</span><span class="sxs-lookup"><span data-stu-id="4f33f-163">Yes!</span></span> <span data-ttu-id="4f33f-164">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="4f33f-164">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="4f33f-165">Si vous laissez 21Vianet gérer vos paramètres DNS avec des enregistrements NS, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="4f33f-165">If you are letting 21Vianet manage your DNS settings with NS records, you can't add subdomains.</span></span>

::: moniker-end

<span data-ttu-id="4f33f-166">En règle générale, vous pouvez ajouter jusqu’à 900 domaines à votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-166">Typically, you can add up to 900 domains to your Microsoft 365 subscription.</span></span>
  
<span data-ttu-id="4f33f-167">Par exemple, vous pouvez ajouter les domaines contoso.com et contosomarketing.com, puis ajouter les sous-domaines www.contoso.com, www.partners.contoso.com, www.partners.marketing.contoso.com, etc.</span><span class="sxs-lookup"><span data-stu-id="4f33f-167">For example, you could add the domains contoso.com and contosomarketing.com, and then add the subdomains www.contoso.com, www.partners.contoso.com, www.partners.marketing.contoso.com, and so on.</span></span>
  
<span data-ttu-id="4f33f-168">Lorsque vous ajoutez un sous-domaine, il est automatiquement vérifié en fonction du domaine parent en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="4f33f-168">When you add a subdomain, it is automatically verified based on the parent domain that is being verified.</span></span>
  
<span data-ttu-id="4f33f-169">Lorsque vous ajoutez plusieurs domaines à Microsoft 365, vous pouvez héberger des services (par exemple, des courriers électroniques) sur n’importe quel domaine que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="4f33f-169">When you add multiple domains to Microsoft 365, you can host any of the services (like email) on any of the domains you've added.</span></span>  <span data-ttu-id="4f33f-170">*Lorsque vous modifiez votre courrier électronique en Microsoft 365, en mettant à jour l’enregistrement MX d’un domaine, tous les messages envoyés à ce domaine débuteront à Microsoft 365.*</span><span class="sxs-lookup"><span data-stu-id="4f33f-170">*When you change your email to Microsoft 365, by updating a domain's MX record, ALL email sent to that domain will start coming to Microsoft 365.*</span></span> 
 
::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="4f33f-171">Si vous avez ajouté un domaine contoso.com à un abonnement Microsoft 365, vous pouvez également ajouter le sous-domaine xyz.contoso.com à une autre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-171">If you added a contoso.com domain to a Microsoft 365 subscription, you can also add the subdomain xyz.contoso.com to another Microsoft 365 organization.</span></span> <span data-ttu-id="4f33f-172">Lors de l’ajout du sous-domaine, vous êtes invité à ajouter un enregistrement TXT dans le fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="4f33f-172">When adding the subdomain, you are prompted to add a TXT record in the DNS hosting provider.</span></span>

## <a name="why-do-i-have-an-onmicrosoftcom-domain"></a><span data-ttu-id="4f33f-173">Pourquoi ai-je un domaine « onmicrosoft.com » ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-173">Why do I have an "onmicrosoft.com" domain?</span></span>

<span data-ttu-id="4f33f-174">Microsoft 365 crée un domaine pour vous, comme *contoso.onmicrosoft.com*, lorsque vous vous inscrivez auprès du service.</span><span class="sxs-lookup"><span data-stu-id="4f33f-174">Microsoft 365 creates a domain for you, like *contoso.onmicrosoft.com*, when you sign up with the service.</span></span> <span data-ttu-id="4f33f-175">Le nom d’utilisateur que vous créez lors de votre inscription comprend le domaine, par exemple *Alan@contoso.onmicrosoft.com*.</span><span class="sxs-lookup"><span data-stu-id="4f33f-175">The user ID that you create when you sign up includes the domain, like *alan@contoso.onmicrosoft.com*.</span></span> 
  
 <span data-ttu-id="4f33f-176">**Si vous voulez faire ressembler votre courrier électronique *Alan \@ contoso.com*:** [acheter le domaine](../get-help-with-domains/buy-a-domain-name.md) ou simplement suivre les étapes de la procédure [ajouter vos utilisateurs et votre domaine à Microsoft 365](add-domain.md) si vous en êtes déjà propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4f33f-176">**If you want to have your email look like *alan\@contoso.com*:** [buy the domain](../get-help-with-domains/buy-a-domain-name.md) or just follow the steps in [Add your users and domain to Microsoft 365](add-domain.md) if you own it already.</span></span> 
  
- <span data-ttu-id="4f33f-177">**Vous ne pouvez pas renommer le domaine onmicrosoft après l’inscription.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-177">**You can't rename the onmicrosoft domain after sign-up.**</span></span> <span data-ttu-id="4f33f-178">Par exemple, si le domaine initial que vous avez choisi était fourthcoffee.onmicrosoft.com, vous ne pouvez pas le modifier pour qu’il soit fabrikam.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="4f33f-178">For example, if the initial domain you chose was fourthcoffee.onmicrosoft.com, you can't change it to be fabrikam.onmicrosoft.com.</span></span> <span data-ttu-id="4f33f-179">Pour utiliser un autre domaine onmicrosoft.com, vous devez démarrer un nouvel abonnement avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-179">To use a different onmicrosoft.com domain, you'd have to start a new subscription with Microsoft 365.</span></span> 
    
- <span data-ttu-id="4f33f-180">**Vous ne pouvez pas renommer l’URL de votre site d’équipe.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-180">**You can't rename your team site URL.**</span></span> <span data-ttu-id="4f33f-181">L’URL de votre site d’équipe est basée sur le nom de votre domaine onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="4f33f-181">Your team site URL is based on your onmicrosoft.com domain name.</span></span> <span data-ttu-id="4f33f-182">Malheureusement, en raison de la façon dont fonctionne l’architecture SharePoint Online, vous ne pouvez pas renommer le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="4f33f-182">Unfortunately, because of the way SharePoint Online architecture works, you can't rename the team site.</span></span> 
    
- <span data-ttu-id="4f33f-183">**Vous ne pouvez pas supprimer votre domaine onmicrosoft.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-183">**You can't remove your onmicrosoft domain.**</span></span> <span data-ttu-id="4f33f-184">Microsoft 365 doit la conserver car elle est utilisée en arrière-plan pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f33f-184">Microsoft 365 needs to keep it around because it's used behind the scenes for your subscription.</span></span> <span data-ttu-id="4f33f-185">Toutefois, vous n’êtes pas obligé d’utiliser le domaine vous-même après avoir ajouté un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4f33f-185">But you don't have to use the domain yourself after you've added a custom domain.</span></span> 
    
<span data-ttu-id="4f33f-186">Vous pouvez continuer à utiliser le domaine onmicrosoft.com initial même après avoir ajouté votre domaine.</span><span class="sxs-lookup"><span data-stu-id="4f33f-186">You can keep using the initial onmicrosoft.com domain even after you add your domain.</span></span> <span data-ttu-id="4f33f-187">Il fonctionne toujours pour le courrier électronique et d’autres services, c’est donc votre choix.</span><span class="sxs-lookup"><span data-stu-id="4f33f-187">It still works for email and other services, so it's your choice.</span></span>
  
::: moniker-end

::: moniker range="o365-germany"
## <a name="why-do-i-have-an-onmicrosoftde-domain"></a><span data-ttu-id="4f33f-188">Pourquoi ai-je un domaine « onmicrosoft.de » ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-188">Why do I have an "onmicrosoft.de" domain?</span></span>

<span data-ttu-id="4f33f-189">Microsoft 365 crée un domaine pour vous, comme *contoso.onmicrosoft.de*, lorsque vous vous inscrivez auprès du service.</span><span class="sxs-lookup"><span data-stu-id="4f33f-189">Microsoft 365 creates a domain for you, like *contoso.onmicrosoft.de*, when you sign up with the service.</span></span> <span data-ttu-id="4f33f-190">Le nom d’utilisateur que vous créez lors de votre inscription comprend le domaine, par exemple *Alan@contoso.onmicrosoft.de*.</span><span class="sxs-lookup"><span data-stu-id="4f33f-190">The user ID that you create when you sign up includes the domain, like *alan@contoso.onmicrosoft.de*.</span></span> 
  
 <span data-ttu-id="4f33f-191">**Si vous souhaitez que votre courrier électronique ressemble à *Alan@contoso.de*:** [achetez le domaine](../get-help-with-domains/buy-a-domain-name.md) ou suivez simplement les étapes de la procédure [ajouter vos utilisateurs et votre domaine à Microsoft 365](add-domain.md) si vous en êtes déjà propriétaire.</span><span class="sxs-lookup"><span data-stu-id="4f33f-191">**If you want to have your email look like *alan@contoso.de*:** [buy the domain](../get-help-with-domains/buy-a-domain-name.md) or just follow the steps in [Add your users and domain to Microsoft 365](add-domain.md) if you own it already.</span></span> 
  
- <span data-ttu-id="4f33f-192">**Vous ne pouvez pas renommer le domaine onmicrosoft après l’inscription.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-192">**You can't rename the onmicrosoft domain after sign-up.**</span></span> <span data-ttu-id="4f33f-193">Par exemple, si le domaine initial que vous avez choisi était fourthcoffee.onmicrosoft.de, vous ne pouvez pas le modifier pour qu’il soit fabrikam.onmicrosoft.de.</span><span class="sxs-lookup"><span data-stu-id="4f33f-193">For example, if the initial domain you chose was fourthcoffee.onmicrosoft.de, you can't change it to be fabrikam.onmicrosoft.de.</span></span> <span data-ttu-id="4f33f-194">Pour utiliser un autre domaine onmicrosoft.de, vous devez démarrer un nouvel abonnement avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-194">To use a different onmicrosoft.de domain, you'd have to start a new subscription with Microsoft 365.</span></span> 
    
- <span data-ttu-id="4f33f-195">**Vous ne pouvez pas renommer l’URL de votre site d’équipe.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-195">**You can't rename your team site URL.**</span></span> <span data-ttu-id="4f33f-196">L’URL de votre site d’équipe est basée sur le nom de votre domaine onmicrosoft.de. Malheureusement, en raison de la façon dont fonctionne l’architecture SharePoint Online, vous ne pouvez pas renommer le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="4f33f-196">Your team site URL is based on your onmicrosoft.de domain name.Unfortunately, because of the way SharePoint Online architecture works, you can't rename the team site.</span></span> 
    
- <span data-ttu-id="4f33f-197">**Vous ne pouvez pas supprimer votre domaine onmicrosoft.**</span><span class="sxs-lookup"><span data-stu-id="4f33f-197">**You can't remove your onmicrosoft domain.**</span></span> <span data-ttu-id="4f33f-198">Microsoft 365 doit la conserver car elle est utilisée en arrière-plan pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f33f-198">Microsoft 365 needs to keep it around because it's used behind the scenes for your subscription.</span></span> <span data-ttu-id="4f33f-199">Toutefois, vous n’êtes pas obligé d’utiliser le domaine vous-même après avoir ajouté un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4f33f-199">But you don't have to use the domain yourself after you've added a custom domain.</span></span> 
    
<span data-ttu-id="4f33f-200">Vous pouvez continuer à utiliser le domaine onmicrosoft.de initial même après avoir ajouté votre domaine.</span><span class="sxs-lookup"><span data-stu-id="4f33f-200">You can keep using the initial onmicrosoft.de domain even after you add your domain.</span></span> <span data-ttu-id="4f33f-201">Il fonctionne toujours pour le courrier électronique et d’autres services, c’est donc votre choix.</span><span class="sxs-lookup"><span data-stu-id="4f33f-201">It still works for email and other services, so it's your choice.</span></span>
  
::: moniker-end

## <a name="how-do-i-verify-my-nonprofit-or-education-status"></a><span data-ttu-id="4f33f-202">Comment puis-je vérifier mon statut de l’organisme ou de l’éducation ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-202">How do I verify my nonprofit or education status?</span></span>

1. <span data-ttu-id="4f33f-203">Sélectionnez **configuration** dans le [Centre d’administration](https://docs.microsoft.com/microsoft-365/admin/admin-home) pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="4f33f-203">Select **Setup** in the [admin center](https://docs.microsoft.com/microsoft-365/admin/admin-home) to start the wizard.</span></span> <span data-ttu-id="4f33f-204">(Veillez à vous connecter d’abord à Microsoft 365.)</span><span class="sxs-lookup"><span data-stu-id="4f33f-204">(Be sure to sign in to Microsoft 365 first.)</span></span> 
    
2. <span data-ttu-id="4f33f-205">Pour devenir l’administrateur de votre école, sélectionnez l’option **devenir administrateur** dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4f33f-205">To become the admin for your school, select the  **Become an admin** option in Microsoft 365.</span></span> 
    
3. <span data-ttu-id="4f33f-206">Vous serez invité à ajouter un enregistrement TXT DNS sur le site Web hôte DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="4f33f-206">You'll be prompted to add a TXT DNS record at the DNS host website for your domain.</span></span> <span data-ttu-id="4f33f-207">Pourquoi ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-207">Why?</span></span> <span data-ttu-id="4f33f-208">Étant donné qu’en se connectant au niveau de l’hôte DNS et en ajoutant un enregistrement pour votre domaine, vous prouvez à Microsoft 365 que vous êtes propriétaire du nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="4f33f-208">Because by signing in at the DNS host and adding a record for your domain, you prove to Microsoft 365 that you own the domain name.</span></span>
    
4. <span data-ttu-id="4f33f-209">Après avoir ajouté l’enregistrement, revenez au portail Microsoft 365 et confirmez que vous l’avez ajouté, afin que Microsoft 365 puisse vérifier.</span><span class="sxs-lookup"><span data-stu-id="4f33f-209">After you add the record, you'll go back to the Microsoft 365 portal and confirm that you've added it, so Microsoft 365 can check.</span></span>
    
<span data-ttu-id="4f33f-210">Disposez-vous d’une offre caritative et souhaitez-vous obtenir Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-210">Have a nonprofit and want to get Microsoft 365?</span></span> <span data-ttu-id="4f33f-211">Assurez-vous que [votre organisation est qualifiée](https://www.microsoft.com/en-us/nonprofits/eligibility) et inscrivez-vous au service.</span><span class="sxs-lookup"><span data-stu-id="4f33f-211">[Make sure your organization qualifies](https://www.microsoft.com/en-us/nonprofits/eligibility) and then sign up for the service.</span></span> 
  
<span data-ttu-id="4f33f-212">Vous souhaitez en savoir plus sur le devenir administrateur de votre école ?</span><span class="sxs-lookup"><span data-stu-id="4f33f-212">Want to know more about becoming the admin for your school?</span></span> <span data-ttu-id="4f33f-213">[Pour en savoir plus, consultez la rubrique](https://docs.microsoft.com/microsoft-365/education/deploy/becoming-an-admin-in-office-365-education
).</span><span class="sxs-lookup"><span data-stu-id="4f33f-213">[Learn all about it](https://docs.microsoft.com/microsoft-365/education/deploy/becoming-an-admin-in-office-365-education
).</span></span>