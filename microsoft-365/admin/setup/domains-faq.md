---
title: Foire aux questions domaines
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
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 1272bad0-4bd4-4796-8005-67d6fb3afc5a
description: Pour plus d’informations sur les domaines dans Office 365, recherchez les réponses à vos questions dans FAQ.
ms.custom: okr_smb
ms.openlocfilehash: f3c72f1ce772e3021d79aa4568dbfdb700400803
ms.sourcegitcommit: 93e6bf1b541e22129f8c443051375d0ef1374150
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/13/2020
ms.locfileid: "42633182"
---
# <a name="domains-faq"></a><span data-ttu-id="81c6e-103">Foire aux questions domaines</span><span class="sxs-lookup"><span data-stu-id="81c6e-103">Domains FAQ</span></span>

<span data-ttu-id="81c6e-104">Cet article contient des réponses aux questions fréquemment posées à propos des domaines dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-104">This article contains answers to Frequently Asked Questions about domains in Office 365.</span></span>

<span data-ttu-id="81c6e-105">Si vous ne trouvez pas la réponse à votre question, laissez-nous un commentaire et nous l'ajouterons à la liste.</span><span class="sxs-lookup"><span data-stu-id="81c6e-105">If you can't find an answer to your question, let us know by leaving a comment and we'll add it to the list.</span></span>
    
## <a name="what-is-mx-priority"></a><span data-ttu-id="81c6e-106">Quelle est la priorité MX ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-106">What is MX priority?</span></span>

<span data-ttu-id="81c6e-107">Le courrier électronique est remis au serveur Exchange de messagerie avec le numéro de préférence le plus bas (priorité la plus élevée), de sorte que l’enregistrement MX que vous utilisez pour le routage du courrier doit avoir le numéro de préférence le plus bas, généralement 0 ou *une priorité élevée* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-107">Mail is delivered to the mail exchange server with the lowest preference number (highest priority), so the MX record you use for mail routing should have the lowest preference number, typically 0 or  *High*  priority.</span></span> 
  
- <span data-ttu-id="81c6e-108">Lorsque vous créez un enregistrement MX, la plupart des fournisseurs d’hébergement DNS exigent que vous définiez le numéro de préférence.</span><span class="sxs-lookup"><span data-stu-id="81c6e-108">When you create an MX record, most DNS hosting providers require you to set the preference number.</span></span>
    
- <span data-ttu-id="81c6e-109">Une étiquette la *préférence* de zone, et une étiquette la *priorité* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-109">Some label the box  *preference*  , and some label it  *priority*  .</span></span> 
    
- <span data-ttu-id="81c6e-110">Certains nécessitent un numéro et d’autres vous demandent de sélectionner *faible* , *moyen* ou *élevé* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-110">Some require a number, and some ask you to select  *Low*  ,  *Medium*  , or  *High*  .</span></span> 
    
- <span data-ttu-id="81c6e-111">Si vous n’avez qu’un seul enregistrement MX, la valeur de Priority ou preference est correcte.</span><span class="sxs-lookup"><span data-stu-id="81c6e-111">If you only have one MX record, any value is fine for priority or preference.</span></span>
    
- <span data-ttu-id="81c6e-112">Si vous en avez plusieurs, assurez-vous que l’enregistrement MX pour le routage du courrier est de priorité supérieure à celle utilisée pour valider le fait que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-112">If you have more than one, make sure the MX record for mail routing is higher priority than the one used for validating that you own the domain.</span></span>
    
## <a name="how-can-i-validate-spf-records-for-my-domain"></a><span data-ttu-id="81c6e-113">Comment puis-je valider des enregistrements SPF pour mon domaine ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-113">How can I validate SPF records for my domain?</span></span>

<span data-ttu-id="81c6e-114">Il est important de disposer ou de créer **un seul enregistrement txt pour SPF**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-114">It's important that you have or create **only one TXT record for SPF**.</span></span> <span data-ttu-id="81c6e-115">Si vous disposez déjà d’un enregistrement SPF, vous devez ajouter les nouvelles valeurs Office 365 au lieu d’en créer un.</span><span class="sxs-lookup"><span data-stu-id="81c6e-115">If you already have an SPF record, you should append the new Office 365 values to it, rather than create a new one.</span></span> <span data-ttu-id="81c6e-116">Une fois que vous avez ajouté ou mis à jour votre enregistrement SPF pour le courrier électronique Office 365, vous devez vérifier que la syntaxe est correcte avec l’un des outils suivants :</span><span class="sxs-lookup"><span data-stu-id="81c6e-116">After you've added or updated your SPF record for Office 365 email, you should check to make sure that the syntax is correct with one of these tools:</span></span> 
  
- [<span data-ttu-id="81c6e-117">Outils de test de l’enregistrement SPF</span><span class="sxs-lookup"><span data-stu-id="81c6e-117">SPF Record Testing Tools</span></span>](http://www.kitterman.com/spf/validate.html)
    
- [<span data-ttu-id="81c6e-118">Enquêteur SPF</span><span class="sxs-lookup"><span data-stu-id="81c6e-118">SPF Surveyor</span></span>](https://dmarcian.com/spf-survey/)
    
- [<span data-ttu-id="81c6e-119">Explorer l’interface Web</span><span class="sxs-lookup"><span data-stu-id="81c6e-119">Dig web interface</span></span>](http://digwebinterface.com/)
    
## <a name="how-does-office-365-manage-my-dns-records"></a><span data-ttu-id="81c6e-120">Comment Office 365 gère-t-il mes enregistrements DNS ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-120">How does Office 365 manage my DNS records?</span></span>

<span data-ttu-id="81c6e-121">Il existe deux options pour la gestion du DNS avec Office 365 :</span><span class="sxs-lookup"><span data-stu-id="81c6e-121">There are two options for DNS management with Office 365:</span></span>
  
1. <span data-ttu-id="81c6e-122">Vous modifiez vos enregistrements de serveur de noms (NS), puis Office 365 prend en charge tous les enregistrements spécifiques aux services, comme la configuration de votre enregistrement MX pour le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="81c6e-122">You change your nameserver (NS) records, and then Office 365 takes care of all the service-specific records, like setting up your MX record for email.</span></span> <span data-ttu-id="81c6e-123">**Recommandation**</span><span class="sxs-lookup"><span data-stu-id="81c6e-123">**(Recommended)**</span></span>
    
2. <span data-ttu-id="81c6e-124">Vous ajoutez vous-même des enregistrements DNS pour le courrier électronique et d’autres services Office 365 au niveau de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-124">You add DNS records for email and other Office 365 services at your DNS host yourself.</span></span> <span data-ttu-id="81c6e-125">**(Experts uniquement)**</span><span class="sxs-lookup"><span data-stu-id="81c6e-125">**(Experts only)**</span></span>
    
### <a name="office-365-creates-and-hosts-the-dns-records"></a><span data-ttu-id="81c6e-126">Office 365 crée et héberge les enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="81c6e-126">Office 365 creates and hosts the DNS records</span></span> 
<span data-ttu-id="81c6e-127">**Avantages**</span><span class="sxs-lookup"><span data-stu-id="81c6e-127">**Advantages**</span></span> 
- <span data-ttu-id="81c6e-128">Vous n’avez pas à vous soucier des erreurs dans les valeurs que vous entrez pour les enregistrements DNS pour les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-128">You don't have to worry about making mistakes in the values you enter for the DNS records for Office 365 services.</span></span>  
- <span data-ttu-id="81c6e-129">Vous bénéficiez d’une plus grande flexibilité dans votre choix de bureau d’enregistrement de domaines et d’hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-129">You have more flexibility in your choice of domain registrar and DNS host.</span></span> 
- <span data-ttu-id="81c6e-130">Tout fournisseur qui vous permet de modifier vos enregistrements de serveur de noms fonctionnera, même si le fournisseur ne prend pas en charge tous les types d’enregistrements requis.</span><span class="sxs-lookup"><span data-stu-id="81c6e-130">Any provider that lets you change your nameserver records will work, even if the provider doesn't support all the required record types.</span></span>   
- <span data-ttu-id="81c6e-131">Lorsque Office 365 ajoute de nouveaux enregistrements DNS, il n’est pas nécessaire d’effectuer des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="81c6e-131">When Office 365 adds new DNS records, you don't have to make updates.</span></span>  

#### <a name="disadvantages"></a><span data-ttu-id="81c6e-132">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="81c6e-132">Disadvantages</span></span> 
- <span data-ttu-id="81c6e-133">Vous ne pouvez pas modifier vos enregistrements DNS pour héberger le courrier électronique en dehors d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-133">You can't change your DNS records to host email outside of Office 365.</span></span> 
- <span data-ttu-id="81c6e-134">Si vous utilisez déjà un site Web public avec votre domaine pour son adresse, par exemple www.fourthcoffee.com, vous devez rediriger les personnes vers cette adresse à partir d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-134">If you already use a public website with your domain for its address, like www.fourthcoffee.com, you must redirect people to that address from Office 365.</span></span> 
- <span data-ttu-id="81c6e-135">La configuration de la redirection nécessite une adresse IP statique, qui n’est pas toujours facilement disponible pour les sites Web publics.</span><span class="sxs-lookup"><span data-stu-id="81c6e-135">Setting up redirection requires a static IP address, which is not always easily available for public websites.</span></span> <span data-ttu-id="81c6e-136">-Si votre bureau d’enregistrement de domaines actuel ne vous permet pas de modifier les enregistrements de serveur de noms de votre domaine, vous devez passer à un autre serveur d’inscriptions pour utiliser cette option de gestion DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-136">- If your current domain registrar doesn't allow you to change your domain's nameserver records, you have to switch to a different registrar to use this DNS management option.</span></span>  

 ### <a name="you-manage-the-dns-records-yourself"></a><span data-ttu-id="81c6e-137">Vous gérez les enregistrements DNS vous-même</span><span class="sxs-lookup"><span data-stu-id="81c6e-137">You manage the DNS records yourself</span></span> 
 #### <a name="advantages"></a><span data-ttu-id="81c6e-138">Avantages</span><span class="sxs-lookup"><span data-stu-id="81c6e-138">Advantages</span></span>
- <span data-ttu-id="81c6e-139">Vous contrôlez les enregistrements DNS pour les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-139">You control the DNS records for Office 365 services.</span></span>   
- <span data-ttu-id="81c6e-140">Si vous disposez d’un site Web public avec votre domaine pour son adresse, par exemple www.fourthcoffee.com, vous n’avez pas à vous soucier de l’utilisation de la redirection afin de vous assurer que les utilisateurs peuvent toujours accéder à votre site Web après avoir configuré votre domaine dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-140">If you have a public website with your domain for its address, like www.fourthcoffee.com, you don't have to worry about using redirection to make sure people can still get to your website after you set up your domain in Office 365.</span></span>    
- <span data-ttu-id="81c6e-141">Vous avez la possibilité d’héberger des messages ailleurs, par exemple avec un serveur Exchange local.</span><span class="sxs-lookup"><span data-stu-id="81c6e-141">You have the flexibility to host email somewhere else, such as with an on-premises Exchange server.</span></span>  
 
#### <a name="disadvantages"></a><span data-ttu-id="81c6e-142">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="81c6e-142">Disadvantages</span></span>
<span data-ttu-id="81c6e-143">Vous devez configurer les enregistrements DNS pour les services Office 365 vous-même (sauf si vous disposez d’un domaine GoDaddy).</span><span class="sxs-lookup"><span data-stu-id="81c6e-143">You have to set up the DNS records for Office 365 services yourself (unless you have a GoDaddy domain).</span></span> 
-  <span data-ttu-id="81c6e-144">Si votre hôte DNS actuel ne prend pas en charge tous les types d’enregistrements requis pour Office 365, certaines fonctionnalités Office 365 ne seront pas disponibles et vous devrez peut-être basculer vers un autre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-144">If your current DNS host doesn't support all of the required record types for Office 365, some Office 365 features won't be available and you might need to switch to a different DNS host.</span></span> 
- <span data-ttu-id="81c6e-145">Lorsque Office 365 modifie les conditions requises pour les enregistrements DNS, ou ajoute de nouveaux services, vous devez effectuer des mises à jour vous-même auprès de votre hôte DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-145">When Office 365 changes requirements for DNS records, or adds new services, you have to make updates yourself at your DNS host.</span></span> 
   
## <a name="what-is-a-domain-name"></a><span data-ttu-id="81c6e-146">Qu’est-ce qu’un nom de domaine ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-146">What is a domain name?</span></span>


<span data-ttu-id="81c6e-147">[] Un domaine est un nom unique qui apparaît après le signe **@** dans les adresses de messagerie et après **www.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-147">A domain is a unique name that appears after the **@** sign in email addresses, and after **www.**</span></span> <span data-ttu-id="81c6e-148">dans les adresses web.</span><span class="sxs-lookup"><span data-stu-id="81c6e-148">in web addresses.</span></span> <span data-ttu-id="81c6e-149">Il prend généralement la forme du nom de votre organisation et d’un suffixe Internet standard, tel que *yourbusiness.com* ou *stateuniversity.edu.*</span><span class="sxs-lookup"><span data-stu-id="81c6e-149">It typically takes the form of your organization's name and a standard Internet suffix, such as  *yourbusiness.com*  or  *stateuniversity.edu.*</span></span> 
  
<span data-ttu-id="81c6e-150">L’utilisation d’un domaine personnalisé comme «**rob\@contoso.com**» avec Office 365 peut vous aider à créer une crédibilité et une reconnaissance pour votre marque.</span><span class="sxs-lookup"><span data-stu-id="81c6e-150">Using a custom domain like "**rob\@contoso.com**" with Office 365 can help build credibility and recognition for your brand.</span></span> 
  
<span data-ttu-id="81c6e-151">Vous pouvez [acheter un domaine dans Office 365 et nous allons le configurer automatiquement](../get-help-with-domains/buy-a-domain-name.md), ou vous pouvez acheter ou en disposer un dont vous êtes déjà propriétaire auprès d’un bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="81c6e-151">You can [buy a domain in Office 365 and we'll set it up automatically](../get-help-with-domains/buy-a-domain-name.md), or you can buy or bring one you already own from a domain registrar.</span></span>
  
## <a name="can-i-transfer-a-domain-i-purchased-from-microsoft-to-another-provider"></a><span data-ttu-id="81c6e-152">Puis-je transférer un domaine que j’ai acheté de Microsoft à un autre fournisseur ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-152">Can I transfer a domain I purchased from Microsoft to another provider?</span></span>

<span data-ttu-id="81c6e-153">Oui, mais vous ne pouvez pas transférer un domaine Office 365 vers un autre bureau d’enregistrement jusqu’à 60 jours après l’avoir acheté avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-153">Yes, but you can't transfer an Office 365 domain to another registrar until 60 days after you purchased it with Office 365.</span></span>

<span data-ttu-id="81c6e-154">Veuillez noter qu’une requête *Whois* affiche un bureau d’enregistrement de domaines Office 365 acheté comme sauvage West Domains LLC.</span><span class="sxs-lookup"><span data-stu-id="81c6e-154">Please note that a *Whois* query will show an Office 365 purchased domain registrar as Wild West Domains LLC.</span></span> <span data-ttu-id="81c6e-155">Toutefois, seul Office 365 doit être contacté concernant votre domaine acheté Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-155">However, only Office 365 should be contacted regarding your Office 365 purchased domain.</span></span>
  
<span data-ttu-id="81c6e-156">Suivez les étapes ci-dessous pour obtenir le code sur Office 365, puis accédez au site Web du Bureau d’enregistrement de domaine pour configurer le transfert de votre nom de domaine vers ce serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="81c6e-156">Follow the steps below to get the code at Office 365, and then go to the other domain registrar's website to set up transferring your domain name to that registrar.</span></span>
  
1. <span data-ttu-id="81c6e-157">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="81c6e-157">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="81c6e-158">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-158">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="81c6e-159">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-159">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="81c6e-160">Sur la page **domaines** , sélectionnez le domaine Office 365 que vous souhaitez transférer vers un autre bureau d’enregistrement de domaines, puis sélectionnez **transfert** > de domaine activé pour le transfert de**domaine**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-160">On the **Domains** page, select the Office 365 domain that you want to transfer to another domain registrar, and then select **Domain Transfer** > **Enable domain transfer**.</span></span>
       
4. <span data-ttu-id="81c6e-161">Suivez les étapes pour préparer le transfert de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-161">Follow the steps to prepare for transferring your domain.</span></span>
    
5. <span data-ttu-id="81c6e-162">Une fois le code obtenu, accédez au site Web du Bureau d’enregistrement de domaines dans lequel vous souhaitez gérer le nom de votre domaine et suivre leur orientation pour le transfert d’un domaine (recherchez de l’aide sur son site Web).</span><span class="sxs-lookup"><span data-stu-id="81c6e-162">After you get the code, go to the website of the domain registrar where you want to manage your domain name going forward and follow their directions for transferring a domain (search for help on their website).</span></span>
    
6. <span data-ttu-id="81c6e-163">Si vous avez besoin de nouveau de voir le code, dans la page **paramètres du domaine** dans Office 365, sélectionnez **afficher le code d’autorisation pour le transfert de domaine**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-163">If you need to see the code again, on the **Domain settings** page in Office 365, select **View authorization code for domain transfer**.</span></span>
    
7. <span data-ttu-id="81c6e-164">Une fois le transfert terminé, vous allez renouveler votre domaine au niveau du nouveau bureau d’enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="81c6e-164">After the transfer is complete, you'll renew your domain at the new domain registrar.</span></span>
    
8. <span data-ttu-id="81c6e-165">Pour terminer le processus, revenez à la page **domaines** du centre d’administration et sélectionnez **effectuer un transfert de domaine complet**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-165">To finish the process, go back to the admin center **Domains** page and select **Complete Domain Transfer**.</span></span> 

<span data-ttu-id="81c6e-166">*Remarque : Notez que les domaines achetés par Office 365 ne sont pas éligibles pour les modifications de serveur de noms ou transférant le domaine entre les locataires Office 365.  Si l’une ou l’autre de ces valeurs est requise, l’inscription de domaine doit être transférée vers un autre serveur d’inscriptions.*</span><span class="sxs-lookup"><span data-stu-id="81c6e-166">*Note: Please note that Office 365 purchased domains are not eligible for Name Server changes or transferring the domain between Office 365 Tenants.  If either of these are required, the domain registration will need to be transferred to another registrar.*</span></span>
    
## <a name="how-do-i-change-how-my-dns-records-are-managed-in-office-365"></a><span data-ttu-id="81c6e-167">Comment puis-je modifier la façon dont mes enregistrements DNS sont gérés dans Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-167">How do I change how my DNS records are managed in Office 365?</span></span>

### <a name="change-dns-management-to-a-dns-host-outside-office-365"></a><span data-ttu-id="81c6e-168">Modifier la gestion du DNS en hôte DNS en dehors d’Office 365</span><span class="sxs-lookup"><span data-stu-id="81c6e-168">Change DNS management to a DNS host outside Office 365</span></span>
   
1. <span data-ttu-id="81c6e-169">Connectez-vous au bureau d’enregistrement de domaines de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-169">Sign in to the domain registrar for your domain.</span></span>
    
2. <span data-ttu-id="81c6e-170">Recherchez la zone sur le site Web du serveur d’inscriptions où vous mettez à jour les enregistrements de serveur de noms et mettez à jour les serveurs de noms pour qu’ils pointent vers l’hôte DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-170">Find the area on the registrar's website where you update nameserver records, and update the nameservers to point to your domain's DNS host.</span></span> <span data-ttu-id="81c6e-171">(L’hôte DNS est souvent le Bureau d’enregistrement de domaines.)</span><span class="sxs-lookup"><span data-stu-id="81c6e-171">(The DNS host is often the domain registrar.)</span></span>
    
3. <span data-ttu-id="81c6e-172">Suivez un lien pour accéder à l’Assistant Configuration des domaines :</span><span class="sxs-lookup"><span data-stu-id="81c6e-172">Follow a link to go to the domains setup wizard:</span></span>
    
4. <span data-ttu-id="81c6e-173">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="81c6e-173">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="81c6e-174">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-174">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="81c6e-175">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-175">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
5. <span data-ttu-id="81c6e-176">Dans la page **domaines** , sélectionnez le domaine que vous changez, puis sélectionnez **gestion DNS**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-176">On the **Domains** page, select the domain you're switching, and select **DNS management**.</span></span>
    
6. <span data-ttu-id="81c6e-177">Dans l’Assistant Configuration des domaines, dans la page **configurer vos services en ligne** , sélectionnez **je vais gérer mes propres enregistrements DNS**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-177">In the domains setup wizard, on the **Set up your online services** page, select **I'll manage my own DNS records**, and then select **Next**.</span></span>
    
7. <span data-ttu-id="81c6e-178">Ajoutez les enregistrements DNS suggérés par l’Assistant sur la page **mettre à jour les paramètres DNS** sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-178">Add the DNS records suggested by the wizard on the **Update DNS settings** page to your registrar's website.</span></span> 
    
8. <span data-ttu-id="81c6e-179">Une fois que vous avez ajouté les enregistrements, revenez à Office 365 et sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-179">After you've added the records, come back to Office 365 and select **Verify**.</span></span>
    

### <a name="change-dns-management-to-office-365"></a><span data-ttu-id="81c6e-180">Modifier la gestion du DNS vers Office 365</span><span class="sxs-lookup"><span data-stu-id="81c6e-180">Change DNS management to Office 365</span></span>
  
1. <span data-ttu-id="81c6e-181">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="81c6e-181">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="81c6e-182">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-182">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="81c6e-183">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-183">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="81c6e-184">Dans la page **domaines** , sélectionnez le domaine que vous changez, puis sélectionnez **gestion DNS**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-184">On the **Domains** page, select the domain you're switching, and select **DNS Management**.</span></span>
    
3. <span data-ttu-id="81c6e-185">Dans l’Assistant Configuration des domaines, dans la page **configurer vos services en ligne** , sélectionnez **configurer mes services en ligne pour moi. (Recommandé)**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-185">In the domains setup wizard, on the **Set up your online services** page, select **Set up my online services for me. (Recommended)**, and then select **Next**.</span></span>
    
4. <span data-ttu-id="81c6e-186">Si vous n’avez pas encore vérifié le domaine, suivez la procédure décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="81c6e-186">If you haven't verified the domain yet, follow the steps to do that first.</span></span>
    
5. <span data-ttu-id="81c6e-187">Sur la page **mettre à jour les paramètres DNS** , nous répertorions les serveurs de noms pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-187">On the **Update DNS settings** page, we list the nameservers for Office 365.</span></span> <span data-ttu-id="81c6e-188">Accédez au bureau d’enregistrement de domaines de votre domaine et mettez à jour les serveurs de noms sur les serveurs de noms Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-188">Go to the domain registrar for your domain, and update the nameservers to the Office 365 nameservers.</span></span> 
    
4. <span data-ttu-id="81c6e-189">Une fois que vous avez mis à jour les serveurs de noms, **Patientez au moins une heure**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-189">After you've updated the nameservers, **wait at least an hour**.</span></span> <span data-ttu-id="81c6e-190">Ensuite, dans l’Assistant dans Office 365, sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-190">Then, back in the wizard in Office 365, select **Verify**.</span></span>
    
## <a name="what-happens-if-my-dns-provider-doesnt-support-certain-record-types"></a><span data-ttu-id="81c6e-191">Que se passe-t-il si mon fournisseur DNS ne prend pas en charge certains types d’enregistrements ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-191">What happens if my DNS provider doesn't support certain record types?</span></span>

<span data-ttu-id="81c6e-192">Si vous gérez vos propres enregistrements DNS et que votre hôte DNS ne prend pas en charge tous les enregistrements DNS dont Office 365 a besoin, certaines fonctionnalités Office 365 ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="81c6e-192">If you manage your own DNS records and your DNS host does not support all the DNS records that Office 365 needs, some Office 365 features won't work.</span></span> <span data-ttu-id="81c6e-193">Nous vous recommandons de transférer votre domaine vers un serveur d’inscriptions qui prend en charge tous les enregistrements DNS requis.</span><span class="sxs-lookup"><span data-stu-id="81c6e-193">We recommend that you transfer your domain to a registrar that supports all required DNS records.</span></span>
  
<span data-ttu-id="81c6e-194">Fournisseurs qui prennent en charge tous les enregistrements DNS requis :</span><span class="sxs-lookup"><span data-stu-id="81c6e-194">Providers that support all required DNS records:</span></span>
  
- <span data-ttu-id="81c6e-195">Dynadot</span><span class="sxs-lookup"><span data-stu-id="81c6e-195">Dynadot</span></span>
    
- <span data-ttu-id="81c6e-196">Auprès enomcentral</span><span class="sxs-lookup"><span data-stu-id="81c6e-196">eNomCentral</span></span>
    
- <span data-ttu-id="81c6e-197">Europe Registry</span><span class="sxs-lookup"><span data-stu-id="81c6e-197">Europe Registry</span></span>
    
- <span data-ttu-id="81c6e-198">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="81c6e-198">GoDaddy</span></span>
    
- <span data-ttu-id="81c6e-199">Sensitiv</span><span class="sxs-lookup"><span data-stu-id="81c6e-199">Hover</span></span>
    
- <span data-ttu-id="81c6e-200">MyHosting.com</span><span class="sxs-lookup"><span data-stu-id="81c6e-200">MyHosting.com</span></span>
    
- <span data-ttu-id="81c6e-201">Name.com</span><span class="sxs-lookup"><span data-stu-id="81c6e-201">Name.com</span></span>
    
- <span data-ttu-id="81c6e-202">Voix presque gratuite</span><span class="sxs-lookup"><span data-stu-id="81c6e-202">Nearly Free Speech</span></span>
    
- <span data-ttu-id="81c6e-203">Nettica</span><span class="sxs-lookup"><span data-stu-id="81c6e-203">Nettica</span></span>
    
- <span data-ttu-id="81c6e-204">Network Information Center (NIC)</span><span class="sxs-lookup"><span data-stu-id="81c6e-204">Network Information Center (NIC)</span></span>
    
- <span data-ttu-id="81c6e-205">Network Solutions</span><span class="sxs-lookup"><span data-stu-id="81c6e-205">Network Solutions</span></span>
    
- <span data-ttu-id="81c6e-206">Register.com</span><span class="sxs-lookup"><span data-stu-id="81c6e-206">Register.com</span></span>
    
 <span data-ttu-id="81c6e-207">**Si les enregistrements SRV ne sont pas pris en charge**, les fonctionnalités Office 365 suivantes ne sont pas disponibles :</span><span class="sxs-lookup"><span data-stu-id="81c6e-207">**If SRV records are not supported**, the following Office 365 features are not available:</span></span> 
  
- <span data-ttu-id="81c6e-208">Intégration de la messagerie instantanée et de la présence Skype entreprise Online à Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="81c6e-208">Skype for Business Online IM and presence integration with Outlook Web App</span></span>
    
- <span data-ttu-id="81c6e-209">Communication externe (Fédération) avec des utilisateurs de Skype entreprise Online dans d’autres organisations.</span><span class="sxs-lookup"><span data-stu-id="81c6e-209">External communication (federation) with Skype for Business Online users in other organizations.</span></span>
    
- <span data-ttu-id="81c6e-210">Connectivité Internet publique (PIC) avec des utilisateurs de Skype entreprise Online connectés à l’aide d’un compte Microsoft (anciennement appelé Windows Live ID).</span><span class="sxs-lookup"><span data-stu-id="81c6e-210">Public Internet Connectivity (PIC) with Skype for Business Online users signed in with a Microsoft account (formerly known as a Windows Live ID).</span></span>
    
 <span data-ttu-id="81c6e-211">**Si plusieurs enregistrements CNAME ne sont pas pris en charge,** vous devez choisir entre les fonctionnalités suivantes pour Skype entreprise Online :</span><span class="sxs-lookup"><span data-stu-id="81c6e-211">**If multiple CNAME records are not supported,** you have to choose between the following features for Skype for Business Online:</span></span> 
  
- <span data-ttu-id="81c6e-212">Les clients de bureau et les clients mobiles de messagerie peuvent utiliser la découverte automatique pour trouver automatiquement le service Exchange Online afin que les utilisateurs puissent se connecter sans avoir à entrer un nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="81c6e-212">Email desktop clients and mobile clients can use Autodiscover to automatically find the Exchange Online service so that users can sign in without having to enter a server name.</span></span>
    
- <span data-ttu-id="81c6e-213">Les clients de bureau Skype entreprise Online peuvent utiliser la découverte automatique pour trouver automatiquement le service Skype entreprise Online afin que les utilisateurs puissent se connecter sans avoir à entrer un nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="81c6e-213">Skype for Business Online desktop clients can use Autodiscover to automatically find the Skype for Business Online service so that users can sign in without having to enter a server name.</span></span>
    
- <span data-ttu-id="81c6e-214">Les clients mobiles Skype entreprise Online peuvent utiliser la découverte automatique pour trouver automatiquement le service Skype entreprise Online afin que les utilisateurs puissent se connecter sans avoir à entrer un nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="81c6e-214">Skype for Business Online mobile clients can use Autodiscover to automatically find the Skype for Business Online service so that users can sign in without having to enter a server name.</span></span>
    
 <span data-ttu-id="81c6e-215">**Si les enregistrements SPF/txt ne sont pas pris en charge**, d’autres personnes peuvent être en mesure d’utiliser votre domaine pour envoyer du courrier indésirable ou d’autres messages malveillants.</span><span class="sxs-lookup"><span data-stu-id="81c6e-215">**If SPF/TXT records are not supported**, other people may be able to use your domain to send spam or other malicious email.</span></span> <span data-ttu-id="81c6e-216">Les enregistrements SPF fonctionnent en identifiant les serveurs qui sont autorisés à envoyer des messages électroniques à partir de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-216">SPF records work by identifying the servers that are authorized to send email from your domain.</span></span> 
  
## <a name="how-do-i-set-or-change-the-default-domain-in-office-365"></a><span data-ttu-id="81c6e-217">Comment définir ou modifier le domaine par défaut dans Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-217">How do I set or change the default domain in Office 365?</span></span>

<span data-ttu-id="81c6e-218">Vous devez avoir au moins un domaine personnalisé que vous avez ajouté à Office 365 avant de pouvoir choisir un domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="81c6e-218">You must have at least one custom domain that you've added to Office 365 before you can choose a default domain.</span></span>
  
1. <span data-ttu-id="81c6e-219">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="81c6e-219">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
    <span data-ttu-id="81c6e-220">Si vous utilisez Office 365 Germany, accédez à la page de ces <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-220">If you're using Office 365 Germany, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span> 
    
    <span data-ttu-id="81c6e-221">Si vous utilisez Office 365 géré par 21Vianet, accédez à la page de ce <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">domaine</a> .</span><span class="sxs-lookup"><span data-stu-id="81c6e-221">If you're using Office 365 operated by 21Vianet, go to this <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="81c6e-222">Dans la page **domaines** , sélectionnez le domaine que vous souhaitez définir par défaut pour les nouvelles adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81c6e-222">On the **Domains** page, select the domain you want to set as the default for new email addresses.</span></span> 
    
3. <span data-ttu-id="81c6e-223">Sélectionnez **définir par défaut**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-223">Select **Set as default**.</span></span>
    
::: moniker range="o365-worldwide"

<span data-ttu-id="81c6e-224">Vous ne pouvez pas modifier le nom de votre domaine initial *. onmicrosoft.com* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-224">You cannot change the name of your initial  *.onmicrosoft.com*  domain.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="81c6e-225">Vous ne pouvez pas modifier le nom de votre domaine initial *. onmicrosoft.de* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-225">You cannot change the name of your initial  *.onmicrosoft.de*  domain.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="81c6e-226">Vous ne pouvez pas modifier le nom de votre domaine initial *. Partner.onmschina.CN* .</span><span class="sxs-lookup"><span data-stu-id="81c6e-226">You cannot change the name of your initial  *.partner.onmschina.cn*  domain.</span></span> 

::: moniker-end

## <a name="can-i-add-custom-subdomains-or-multiple-domains-to-office-365"></a><span data-ttu-id="81c6e-227">Puis-je ajouter des sous-domaines personnalisés ou plusieurs domaines à Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-227">Can I add custom subdomains or multiple domains to Office 365?</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="81c6e-228">OK!</span><span class="sxs-lookup"><span data-stu-id="81c6e-228">Yes!</span></span> <span data-ttu-id="81c6e-229">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-229">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="81c6e-230">Si vous autorisez Microsoft à gérer vos paramètres DNS avec des enregistrements NS, ou si vous avez acheté le domaine auprès de Microsoft, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="81c6e-230">If you are letting Microsoft manage your DNS settings with NS records, or if you bought the domain from Microsoft, you can't add subdomains.</span></span>

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="81c6e-231">OK!</span><span class="sxs-lookup"><span data-stu-id="81c6e-231">Yes!</span></span> <span data-ttu-id="81c6e-232">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-232">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="81c6e-233">Si vous autorisez Microsoft à gérer vos paramètres DNS avec des enregistrements NS, ou si vous avez acheté le domaine auprès de Microsoft, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="81c6e-233">If you are letting Microsoft manage your DNS settings with NS records, or if you bought the domain from Microsoft, you can't add subdomains.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="81c6e-234">OK!</span><span class="sxs-lookup"><span data-stu-id="81c6e-234">Yes!</span></span> <span data-ttu-id="81c6e-235">Pour ajouter des sous-domaines, vous devez gérer vos propres paramètres DNS sur le site Web de votre registraire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-235">To add subdomains, you must manage your own DNS settings at your registrar's website.</span></span> <span data-ttu-id="81c6e-236">Si vous laissez 21Vianet gérer vos paramètres DNS avec des enregistrements NS, vous ne pouvez pas ajouter de sous-domaines.</span><span class="sxs-lookup"><span data-stu-id="81c6e-236">If you are letting 21Vianet manage your DNS settings with NS records, you can't add subdomains.</span></span>

::: moniker-end

<span data-ttu-id="81c6e-237">En règle générale, vous pouvez ajouter jusqu’à 900 domaines à votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-237">Typically, you can add up to 900 domains to your Office 365 subscription.</span></span>
  
<span data-ttu-id="81c6e-238">Par exemple, vous pouvez ajouter les domaines contoso.com et contosomarketing.com, puis ajouter les sous-domaines www.contoso.com, www.partners.contoso.com, www.partners.marketing.contoso.com, etc.</span><span class="sxs-lookup"><span data-stu-id="81c6e-238">For example, you could add the domains contoso.com and contosomarketing.com, and then add the subdomains www.contoso.com, www.partners.contoso.com, www.partners.marketing.contoso.com, and so on.</span></span>
  
<span data-ttu-id="81c6e-239">Lorsque vous ajoutez un sous-domaine, il est automatiquement vérifié en fonction du domaine parent en cours de vérification.</span><span class="sxs-lookup"><span data-stu-id="81c6e-239">When you add a subdomain, it is automatically verified based on the parent domain that is being verified.</span></span>
  
<span data-ttu-id="81c6e-240">Lorsque vous ajoutez plusieurs domaines à Office 365, vous pouvez héberger des services (par exemple, des courriers électroniques) sur n’importe quel domaine que vous avez ajouté.</span><span class="sxs-lookup"><span data-stu-id="81c6e-240">When you add multiple domains to Office 365, you can host any of the services (like email) on any of the domains you've added.</span></span>  <span data-ttu-id="81c6e-241">*Lorsque vous modifiez votre courrier électronique en Office 365, en mettant à jour l’enregistrement MX d’un domaine, tous les messages envoyés à ce domaine débuteront dans Office 365.*</span><span class="sxs-lookup"><span data-stu-id="81c6e-241">*When you change your email to Office 365, by updating a domain's MX record, ALL email sent to that domain will start coming to Office 365.*</span></span> 
 
::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="81c6e-242">Si vous avez déjà ajouté un domaine contoso.com à un client Office 365, vous pouvez également ajouter le sous-domaine xyz.contoso.com à un autre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-242">If you have already added a contoso.com domain to an Office 365 tenant, you can also add the subdomain xyz.contoso.com to another Office 365 tenant.</span></span> <span data-ttu-id="81c6e-243">Lors de l’ajout du sous-domaine, vous serez invité à ajouter un enregistrement TXT dans le fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-243">When adding the subdomain, you will be prompted to add a TXT record in the DNS hosting provider.</span></span>

## <a name="why-do-i-have-an-onmicrosoftcom-domain"></a><span data-ttu-id="81c6e-244">Pourquoi ai-je un domaine « onmicrosoft.com » ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-244">Why do I have an "onmicrosoft.com" domain?</span></span>

<span data-ttu-id="81c6e-245">Office 365 crée un domaine pour vous, comme *contoso.onmicrosoft.com*, lorsque vous vous inscrivez auprès du service.</span><span class="sxs-lookup"><span data-stu-id="81c6e-245">Office 365 creates a domain for you, like *contoso.onmicrosoft.com*, when you sign up with the service.</span></span> <span data-ttu-id="81c6e-246">Le nom d’utilisateur que vous créez lors de votre inscription comprend le domaine, par exemple *Alan@contoso.onmicrosoft.com*.</span><span class="sxs-lookup"><span data-stu-id="81c6e-246">The user ID that you create when you sign up includes the domain, like *alan@contoso.onmicrosoft.com*.</span></span> 
  
 <span data-ttu-id="81c6e-247">**Si vous voulez faire ressembler votre courrier *électronique\@Alan contoso.com*:** [acheter le domaine](../get-help-with-domains/buy-a-domain-name.md) ou simplement suivre les étapes de la procédure [ajouter vos utilisateurs et votre domaine à Office 365](add-domain.md) si vous en êtes déjà propriétaire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-247">**If you want to have your email look like *alan\@contoso.com*:** [buy the domain](../get-help-with-domains/buy-a-domain-name.md) or just follow the steps in [Add your users and domain to Office 365](add-domain.md) if you own it already.</span></span> 
  
- <span data-ttu-id="81c6e-248">**Vous ne pouvez pas renommer le domaine onmicrosoft après l’inscription.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-248">**You can't rename the onmicrosoft domain after sign-up.**</span></span> <span data-ttu-id="81c6e-249">Par exemple, si le domaine initial que vous avez choisi était fourthcoffee.onmicrosoft.com, vous ne pouvez pas le modifier pour qu’il soit fabrikam.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="81c6e-249">For example, if the initial domain you chose was fourthcoffee.onmicrosoft.com, you can't change it to be fabrikam.onmicrosoft.com.</span></span> <span data-ttu-id="81c6e-250">Pour utiliser un autre domaine onmicrosoft.com, vous devez démarrer un nouvel abonnement avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-250">To use a different onmicrosoft.com domain, you'd have to start a new subscription with Office 365.</span></span> 
    
- <span data-ttu-id="81c6e-251">**Vous ne pouvez pas renommer l’URL de votre site d’équipe.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-251">**You can't rename your team site URL.**</span></span> <span data-ttu-id="81c6e-252">L’URL de votre site d’équipe est basée sur le nom de votre domaine onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="81c6e-252">Your team site URL is based on your onmicrosoft.com domain name.</span></span> <span data-ttu-id="81c6e-253">Malheureusement, en raison de la façon dont fonctionne l’architecture SharePoint Online, vous ne pouvez pas renommer le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="81c6e-253">Unfortunately, because of the way SharePoint Online architecture works, you can't rename the team site.</span></span> 
    
- <span data-ttu-id="81c6e-254">**Vous ne pouvez pas supprimer votre domaine onmicrosoft.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-254">**You can't remove your onmicrosoft domain.**</span></span> <span data-ttu-id="81c6e-255">Office 365 doit le conserver, car il est utilisé en arrière-plan pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="81c6e-255">Office 365 needs to keep it around because it's used behind the scenes for your subscription.</span></span> <span data-ttu-id="81c6e-256">Toutefois, vous n’êtes pas obligé d’utiliser le domaine vous-même après avoir ajouté un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="81c6e-256">But you don't have to use the domain yourself after you've added a custom domain.</span></span> 
    
<span data-ttu-id="81c6e-257">Vous pouvez continuer à utiliser le domaine onmicrosoft.com initial même après avoir ajouté votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-257">You can keep using the initial onmicrosoft.com domain even after you add your domain.</span></span> <span data-ttu-id="81c6e-258">Il fonctionne toujours pour le courrier électronique et d’autres services, c’est donc votre choix.</span><span class="sxs-lookup"><span data-stu-id="81c6e-258">It still works for email and other services, so it's your choice.</span></span>
  
::: moniker-end

::: moniker range="o365-germany"
## <a name="why-do-i-have-an-onmicrosoftde-domain"></a><span data-ttu-id="81c6e-259">Pourquoi ai-je un domaine « onmicrosoft.de » ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-259">Why do I have an "onmicrosoft.de" domain?</span></span>

<span data-ttu-id="81c6e-260">Office 365 crée un domaine pour vous, comme *contoso.onmicrosoft.de*, lorsque vous vous inscrivez auprès du service.</span><span class="sxs-lookup"><span data-stu-id="81c6e-260">Office 365 creates a domain for you, like *contoso.onmicrosoft.de*, when you sign up with the service.</span></span> <span data-ttu-id="81c6e-261">Le nom d’utilisateur que vous créez lors de votre inscription comprend le domaine, par exemple *Alan@contoso.onmicrosoft.de*.</span><span class="sxs-lookup"><span data-stu-id="81c6e-261">The user ID that you create when you sign up includes the domain, like *alan@contoso.onmicrosoft.de*.</span></span> 
  
 <span data-ttu-id="81c6e-262">**Si vous souhaitez que votre courrier électronique ressemble à *Alan@contoso.de*:** [achetez le domaine](../get-help-with-domains/buy-a-domain-name.md) ou suivez simplement les étapes de la procédure [ajouter vos utilisateurs et votre domaine à Office 365](add-domain.md) si vous en êtes déjà propriétaire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-262">**If you want to have your email look like *alan@contoso.de*:** [buy the domain](../get-help-with-domains/buy-a-domain-name.md) or just follow the steps in [Add your users and domain to Office 365](add-domain.md) if you own it already.</span></span> 
  
- <span data-ttu-id="81c6e-263">**Vous ne pouvez pas renommer le domaine onmicrosoft après l’inscription.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-263">**You can't rename the onmicrosoft domain after sign-up.**</span></span> <span data-ttu-id="81c6e-264">Par exemple, si le domaine initial que vous avez choisi était fourthcoffee.onmicrosoft.de, vous ne pouvez pas le modifier pour qu’il soit fabrikam.onmicrosoft.de.</span><span class="sxs-lookup"><span data-stu-id="81c6e-264">For example, if the initial domain you chose was fourthcoffee.onmicrosoft.de, you can't change it to be fabrikam.onmicrosoft.de.</span></span> <span data-ttu-id="81c6e-265">Pour utiliser un autre domaine onmicrosoft.de, vous devez démarrer un nouvel abonnement avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-265">To use a different onmicrosoft.de domain, you'd have to start a new subscription with Office 365.</span></span> 
    
- <span data-ttu-id="81c6e-266">**Vous ne pouvez pas renommer l’URL de votre site d’équipe.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-266">**You can't rename your team site URL.**</span></span> <span data-ttu-id="81c6e-267">L’URL de votre site d’équipe est basée sur le nom de votre domaine onmicrosoft.de. Malheureusement, en raison de la façon dont fonctionne l’architecture SharePoint Online, vous ne pouvez pas renommer le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="81c6e-267">Your team site URL is based on your onmicrosoft.de domain name.Unfortunately, because of the way SharePoint Online architecture works, you can't rename the team site.</span></span> 
    
- <span data-ttu-id="81c6e-268">**Vous ne pouvez pas supprimer votre domaine onmicrosoft.**</span><span class="sxs-lookup"><span data-stu-id="81c6e-268">**You can't remove your onmicrosoft domain.**</span></span> <span data-ttu-id="81c6e-269">Office 365 doit le conserver, car il est utilisé en arrière-plan pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="81c6e-269">Office 365 needs to keep it around because it's used behind the scenes for your subscription.</span></span> <span data-ttu-id="81c6e-270">Toutefois, vous n’êtes pas obligé d’utiliser le domaine vous-même après avoir ajouté un domaine personnalisé.</span><span class="sxs-lookup"><span data-stu-id="81c6e-270">But you don't have to use the domain yourself after you've added a custom domain.</span></span> 
    
<span data-ttu-id="81c6e-271">Vous pouvez continuer à utiliser le domaine onmicrosoft.de initial même après avoir ajouté votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-271">You can keep using the initial onmicrosoft.de domain even after you add your domain.</span></span> <span data-ttu-id="81c6e-272">Il fonctionne toujours pour le courrier électronique et d’autres services, c’est donc votre choix.</span><span class="sxs-lookup"><span data-stu-id="81c6e-272">It still works for email and other services, so it's your choice.</span></span>
  
::: moniker-end

## <a name="how-do-i-verify-my-nonprofit-or-education-status"></a><span data-ttu-id="81c6e-273">Comment puis-je vérifier mon statut de l’organisme ou de l’éducation ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-273">How do I verify my nonprofit or education status?</span></span>

1. <span data-ttu-id="81c6e-274">Sélectionnez **configuration** dans le [Centre d’administration](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791.aspx) pour démarrer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="81c6e-274">Select **Setup** in the [admin center](https://support.office.com/article/17d3ff3f-3601-466e-b5a1-482b31cfb791.aspx) to start the wizard.</span></span> <span data-ttu-id="81c6e-275">(Veillez à vous connecter d’abord à Office 365.)</span><span class="sxs-lookup"><span data-stu-id="81c6e-275">(Be sure to sign in to Office 365 first.)</span></span> 
    
2. <span data-ttu-id="81c6e-276">Pour devenir l’administrateur de votre école, sélectionnez l’option **devenir administrateur** dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-276">To become the admin for your school, select the **Become an admin** option in Office 365.</span></span> 
    
3. <span data-ttu-id="81c6e-277">Vous serez invité à ajouter un enregistrement TXT DNS sur le site Web hôte DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-277">You'll be prompted to add a TXT DNS record at the DNS host website for your domain.</span></span> <span data-ttu-id="81c6e-278">Pourquoi ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-278">Why?</span></span> <span data-ttu-id="81c6e-279">Étant donné qu’en se connectant au niveau de l’hôte DNS et en ajoutant un enregistrement pour votre domaine, vous prouvez à Office 365 que vous êtes propriétaire du nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-279">Because by signing in at the DNS host and adding a record for your domain, you prove to Office 365 that you own the domain name.</span></span>
    
4. <span data-ttu-id="81c6e-280">Après avoir ajouté l’enregistrement, revenez au portail Office 365 et confirmez que vous l’avez ajouté, de sorte que Office 365 puisse vérifier.</span><span class="sxs-lookup"><span data-stu-id="81c6e-280">After you add the record, you'll go back to the Office 365 portal and confirm that you've added it, so Office 365 can check.</span></span>
    
<span data-ttu-id="81c6e-281">Disposez-vous d’une offre caritative et souhaitez obtenir Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-281">Have a nonprofit and want to get Office 365?</span></span> <span data-ttu-id="81c6e-282">Assurez-vous que [votre organisation est qualifiée](https://www.microsoft.com/en-us/nonprofits/eligibility) et inscrivez-vous au service.</span><span class="sxs-lookup"><span data-stu-id="81c6e-282">[Make sure your organization qualifies](https://www.microsoft.com/en-us/nonprofits/eligibility) and then sign up for the service.</span></span> 
  
<span data-ttu-id="81c6e-283">Vous souhaitez en savoir plus sur le devenir administrateur de votre école ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-283">Want to know more about becoming the admin for your school?</span></span> <span data-ttu-id="81c6e-284">[Pour en savoir plus, consultez la rubrique](https://docs.microsoft.com/microsoft-365/education/deploy/becoming-an-admin-in-office-365-education
).</span><span class="sxs-lookup"><span data-stu-id="81c6e-284">[Learn all about it](https://docs.microsoft.com/microsoft-365/education/deploy/becoming-an-admin-in-office-365-education
).</span></span>
  
## <a name="can-i-pilot-office-365-with-just-a-few-email-addresses-from-my-custom-domain"></a><span data-ttu-id="81c6e-285">Puis-je piloter Office 365 avec seulement quelques adresses de messagerie à partir de mon domaine personnalisé ?</span><span class="sxs-lookup"><span data-stu-id="81c6e-285">Can I pilot Office 365 with just a few email addresses from my custom domain?</span></span>

<span data-ttu-id="81c6e-286">Vous pouvez, mais il existe des limitations :</span><span class="sxs-lookup"><span data-stu-id="81c6e-286">You can, but there are limitations:</span></span>
  
- <span data-ttu-id="81c6e-287">Votre fournisseur de messagerie actuel doit fournir le transfert du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="81c6e-287">Your current email provider must provide email forwarding.</span></span>
    
- <span data-ttu-id="81c6e-288">Vous devez gérer vos enregistrements DNS Office 365 auprès de votre fournisseur d’hébergement DNS, au lieu de faire en sorte que Office 365 gère ces enregistrements pour vous.</span><span class="sxs-lookup"><span data-stu-id="81c6e-288">You need to manage your Office 365-related DNS records at your DNS hosting provider, rather than having Office 365 manage these records for you.</span></span> <span data-ttu-id="81c6e-289">Pour en savoir plus, consultez la rubrique ajouter votre domaine à Office 365 lorsque vous voulez gérer vos propres enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-289">To learn what this entails, see Add your domain to Office 365 when you want to manage your own DNS records.</span></span>
    
- <span data-ttu-id="81c6e-290">Certaines fonctionnalités Office 365 ne seront pas disponibles :</span><span class="sxs-lookup"><span data-stu-id="81c6e-290">Some Office 365 features won't be available:</span></span>
- <span data-ttu-id="81c6e-291">Les utilisateurs ne peuvent pas voir les informations de disponibilité pour les utilisateurs qui se trouvent sur l’autre fournisseur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81c6e-291">Users won't be able to see free/busy information for the users who are on the other email provider.</span></span>
- <span data-ttu-id="81c6e-292">Les administrateurs ne pourront pas administrer les comptes de tous les utilisateurs à partir d’un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="81c6e-292">Admins won't be able to administer everyone's accounts from one place.</span></span>
- <span data-ttu-id="81c6e-293">Les utilisateurs peuvent ne pas être en mesure d’utiliser le filtrage du courrier indésirable Office 365</span><span class="sxs-lookup"><span data-stu-id="81c6e-293">Users may not be able to use Office 365 spam filtering</span></span>

### <a name="how-to-set-up-an-office-365-pilot"></a><span data-ttu-id="81c6e-294">Procédure de configuration d’un pilote Office 365</span><span class="sxs-lookup"><span data-stu-id="81c6e-294">How to set up an Office 365 pilot</span></span>
    
1. <span data-ttu-id="81c6e-295">Se connecter au centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81c6e-295">Sign in to the Microsoft 365 admin center</span></span>
    
    1. <span data-ttu-id="81c6e-296">Connectez-vous à Office 365 avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="81c6e-296">Sign in to Office 365 with your work or school account.</span></span>
        
    2. <span data-ttu-id="81c6e-297">Accédez à **paramètres** \> **Domains**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-297">Go to **Settings** \> **Domains**.</span></span> 
    
2. <span data-ttu-id="81c6e-298">Vérifier que vous êtes propriétaire du domaine que vous souhaitez utiliser</span><span class="sxs-lookup"><span data-stu-id="81c6e-298">Verify that you own the domain you want to use</span></span>
    
    1. <span data-ttu-id="81c6e-299">Dans la page **domaines** , sélectionnez **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-299">On the **Domains** page, select **Add domain**.</span></span> 
        
    2. <span data-ttu-id="81c6e-300">Dans le panneau, tapez le domaine, dans cet exemple cohowinery.com, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-300">In the panel, type the domain, in this example cohowinery.com, and then select **Next**.</span></span> 
        
    3. <span data-ttu-id="81c6e-301">Sur la page **vérifier** le domaine, suivez les instructions pas à pas.</span><span class="sxs-lookup"><span data-stu-id="81c6e-301">On the **Verify** domain page, follow the step-by-step instructions.</span></span> 
        
    4. <span data-ttu-id="81c6e-302">Dans la liste déroulante, sélectionnez votre fournisseur d’hébergement DNS et suivez les instructions pour montrer que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-302">In the drop-down list, select your DNS hosting provider, and follow the instructions to show that you own the domain.</span></span>
        
    5. <span data-ttu-id="81c6e-303">Sélectionnez **Verify (vérifier**).</span><span class="sxs-lookup"><span data-stu-id="81c6e-303">Select **Verify**.</span></span> <span data-ttu-id="81c6e-304">Les modifications DNS prennent effet entre quelques minutes et 72 heures.</span><span class="sxs-lookup"><span data-stu-id="81c6e-304">It takes between a few minutes and 72 hours for DNS changes to take effect.</span></span> 
        
    6. <span data-ttu-id="81c6e-305">Une fois la vérification réussie, vous serez invité à modifier vos enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="81c6e-305">When verification is successful, you'll be asked to modify your DNS records.</span></span>
    
3. <span data-ttu-id="81c6e-306">Marquer le domaine comme étant partagé dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="81c6e-306">Mark the domain as shared in Exchange Online</span></span>
    
    1. <span data-ttu-id="81c6e-307">Accédez au **Centre d’administration Exchange** .</span><span class="sxs-lookup"><span data-stu-id="81c6e-307">Go to the **Exchange admin center** (EAC).</span></span> 
        
    2. <span data-ttu-id="81c6e-308">Dans la section **flux de messagerie** , sélectionnez **domaines acceptés**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-308">In the **Mail flow** section, select **Accepted domains**.</span></span> 
        
    3. <span data-ttu-id="81c6e-309">Double-cliquez sur le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="81c6e-309">Double-click the domain you want to modify.</span></span>
        
    4. <span data-ttu-id="81c6e-310">Dans la fenêtre qui s’ouvre, sélectionnez **relais interne**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-310">In the window that opens, select **Internal Relay**.</span></span> 
        
    5. <span data-ttu-id="81c6e-311">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-311">Select **Save**.</span></span> <span data-ttu-id="81c6e-312">Ce paramètre peut nécessiter quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="81c6e-312">This setting may require a few minutes to take effect.</span></span> 
    
4. <span data-ttu-id="81c6e-313">Si vous le souhaitez, débloquez le serveur de messagerie existant.</span><span class="sxs-lookup"><span data-stu-id="81c6e-313">Optionally, unblock the existing email server</span></span>
    
    1. <span data-ttu-id="81c6e-314">Office 365 utilise Exchange Online Protection (EOP) pour la protection contre le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81c6e-314">Office 365 uses Exchange Online Protection (EOP) for spam protection.</span></span> <span data-ttu-id="81c6e-315">Si EOP détecte un volume élevé de courrier indésirable transféré par votre serveur de messagerie actuel, il peut le bloquer, ce qui empêche le transfert de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="81c6e-315">If EOP detects a high volume of spam being forwarded by your current mail server, it may block it, which would prevent forwarding from working.</span></span> <span data-ttu-id="81c6e-316">Si vous êtes sûr de la protection anti-courrier indésirable que votre autre fournisseur de messagerie utilise, vous pouvez autoriser son serveur dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-316">If you are confident with the spam protection your other email provider uses, you can whitelist their server in Office 365.</span></span> <span data-ttu-id="81c6e-317">Toutefois, cela permettra également aux courriers indésirables qui transitent par votre serveur d’origine d’être transmis aux boîtes aux lettres Office 365 et vous ne pourrez pas évaluer la manière dont Office 365 empêche le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="81c6e-317">However, this will also allow any spam that arrives through your original server to come through to the Office 365 mailboxes, and you won't be able to evaluate how well Office 365 prevents spam.</span></span>
    
    2. <span data-ttu-id="81c6e-318">Accédez au centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="81c6e-318">Go to Exchange admin center (EAC).</span></span>
        
    3. <span data-ttu-id="81c6e-319">Dans le centre d’administration Exchange, sélectionnez **protection**, puis **filtre de connexion**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-319">In EAC, select **Protection**, and then select **Connection filter**.</span></span> 
        
    4. <span data-ttu-id="81c6e-320">Dans la **liste**d’adresses IP autorisées **+**, sélectionnez et ajoutez l’adresse IP du serveur de messagerie que vous pouvez obtenir de votre fournisseur de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="81c6e-320">In the **IP Allow list**, select **+**, and add the mail server IP address that you can get from your current email provider.</span></span> 
    
5. <span data-ttu-id="81c6e-321">Créer des comptes d’utilisateurs et définir l’adresse principale (de réponse)</span><span class="sxs-lookup"><span data-stu-id="81c6e-321">Create user accounts and set the primary (reply-to) address</span></span>
    
    1. <span data-ttu-id="81c6e-322">Aller au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-322">Go to the Microsoft 365 admin center.</span></span>
        
    2. <span data-ttu-id="81c6e-323">Dans la barre de navigation de gauche **, sélectionnez** \> utilisateurs **actifs**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-323">On the left navigation bar, select **Users** \> **Active Users**.</span></span> 
        
    3. <span data-ttu-id="81c6e-324">Créez les comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81c6e-324">Create the user accounts.</span></span>
        
    4. <span data-ttu-id="81c6e-325">Pour chaque compte, sélectionnez **+ (nouveau)**, puis renseignez les informations requises.</span><span class="sxs-lookup"><span data-stu-id="81c6e-325">For each account select **+ (New)**, and fill out the required information.</span></span> 
        
    5. <span data-ttu-id="81c6e-326">Pour conserver le courrier électronique de l’utilisateur comme il le fait, le champ **nom d’utilisateur** doit être identique à l’adresse de messagerie existante de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81c6e-326">To keep user's email the same as it is currently, the **User name** field should be exactly the same as the user's existing email address.</span></span> 
        
    6. <span data-ttu-id="81c6e-327">En regard de nom d’utilisateur, sélectionnez votre nom de domaine personnalisé dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="81c6e-327">Next to User name, select your custom domain name from the drop-down list.</span></span>
        
    7. <span data-ttu-id="81c6e-328">Sélectionnez **créer** \> une **fermeture**.</span><span class="sxs-lookup"><span data-stu-id="81c6e-328">Select **Create** \> **Close**.</span></span> 
        
6. <span data-ttu-id="81c6e-329">Mettre à jour les enregistrements DNS au niveau de votre fournisseur d’hébergement DNS</span><span class="sxs-lookup"><span data-stu-id="81c6e-329">Update DNS records at your DNS hosting provider</span></span>
    
    1. <span data-ttu-id="81c6e-330">Connectez-vous au site Web de votre fournisseur d’hébergement DNS et suivez les [étapes créer des enregistrements DNS auprès d’un fournisseur d’hébergement DNS pour Office 365](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span><span class="sxs-lookup"><span data-stu-id="81c6e-330">Sign in to your DNS hosting provider's website, and follow the [Create DNS records at any DNS hosting provider for Office 365 steps](../get-help-with-domains/create-dns-records-at-any-dns-hosting-provider.md).</span></span> <span data-ttu-id="81c6e-331">**Faites les exceptions suivantes :**</span><span class="sxs-lookup"><span data-stu-id="81c6e-331">**Make the following exceptions:**</span></span>
    
        1. <span data-ttu-id="81c6e-332">Ne créez pas de nouvel enregistrement MX ou ne modifiez pas votre enregistrement MX existant.</span><span class="sxs-lookup"><span data-stu-id="81c6e-332">Do not create a new MX record or change your existing MX record.</span></span>
            
        2. <span data-ttu-id="81c6e-333">Si vous disposez déjà d’un enregistrement SPF (Sender Policy Framework) pour votre fournisseur de messagerie précédent, au lieu de créer un nouvel enregistrement SPF (TXT) pour Exchange Online, ajoutez simplement « inclure include. protection. Outlook. com » à l’enregistrement TXT actuel.</span><span class="sxs-lookup"><span data-stu-id="81c6e-333">If you already have a Sender Policy Framework (SPF) record for your previous email provider, instead of creating a new SPF (TXT) record for Exchange Online, just add "include:spf.protection.outlook.com" to the current TXT record.</span></span> <span data-ttu-id="81c6e-334">Par exemple, « v = spf1 mx include :adatum. com include include. protection. Outlook. com ~ All ».</span><span class="sxs-lookup"><span data-stu-id="81c6e-334">For example, "v=spf1 mx include:adatum.com include:spf.protection.outlook.com ~all".</span></span>
            
        3. <span data-ttu-id="81c6e-335">Si vous n’avez pas encore d’enregistrement SPF, modifiez celui recommandé par Office 365 pour inclure le domaine de votre fournisseur de messagerie actuel, plus spf.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="81c6e-335">If you don't have an SPF record yet, modify the one recommended by Office 365 to include the domain for your current email provider, plus spf.protection.outlook.com.</span></span> <span data-ttu-id="81c6e-336">Autorise les messages sortants des deux systèmes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81c6e-336">This authorizes outgoing messages from both email systems.</span></span>
            
7. <span data-ttu-id="81c6e-337">Configurer le transfert du courrier électronique auprès de votre fournisseur actuel</span><span class="sxs-lookup"><span data-stu-id="81c6e-337">Set up email forwarding at your current provider</span></span>
    
    1. <span data-ttu-id="81c6e-338">Auprès de votre fournisseur de messagerie actuel, configurez le transfert pour vos comptes de messagerie des utilisateurs vers votre domaine onmicrosoft.com :</span><span class="sxs-lookup"><span data-stu-id="81c6e-338">At your current email provider, set up forwarding for your users email accounts to your onmicrosoft.com domain:</span></span>
        
    2. <span data-ttu-id="81c6e-339">La boîte aux lettres de l’utilisateur A doit transférer vers usera@yourcompany.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="81c6e-339">User A's mailbox should forward to usera@yourcompany.onmicrosoft.com</span></span>
        
    3. <span data-ttu-id="81c6e-340">La boîte aux lettres de l’utilisateur B doit transférer vers userb@yourcompany.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="81c6e-340">User B's mailbox should forward to userb@yourcompany.onmicrosoft.com</span></span>
        
    4. <span data-ttu-id="81c6e-341">Lorsque vous effectuez cette étape :</span><span class="sxs-lookup"><span data-stu-id="81c6e-341">When you complete this step:</span></span>
        
    5. <span data-ttu-id="81c6e-342">Tous les messages envoyés à usera@yourcompany.com et userb@yourcompany.com seront disponibles dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="81c6e-342">All mail sent to usera@yourcompany.com and userb@yourcompany.com will be available in Office 365.</span></span>
    
    6. <span data-ttu-id="81c6e-343">Remarques :</span><span class="sxs-lookup"><span data-stu-id="81c6e-343">Notes:</span></span>
        
        - <span data-ttu-id="81c6e-344">Contactez votre fournisseur de messagerie actuel pour obtenir les étapes exactes de configuration du transfert.</span><span class="sxs-lookup"><span data-stu-id="81c6e-344">Contact your current email provider for the exact steps for setting up forwarding.</span></span>
            
        - <span data-ttu-id="81c6e-345">Vous n’avez pas besoin de conserver une copie des messages au niveau du fournisseur de messagerie actuel.</span><span class="sxs-lookup"><span data-stu-id="81c6e-345">You don't need to keep a copy of messages at the current email provider.</span></span>
            
        - <span data-ttu-id="81c6e-346">La plupart des fournisseurs transfèrent le courrier électronique en laissant l’adresse de réponse de l’expéditeur intacte, de sorte que les réponses soient envoyées à l’expéditeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-346">Most providers forward email leaving the Reply-to address of the sender intact, so that replies go to the original sender.</span></span>
    
8. <span data-ttu-id="81c6e-347">Tester le flux de courrier</span><span class="sxs-lookup"><span data-stu-id="81c6e-347">Test mail flow</span></span>
    
    1. <span data-ttu-id="81c6e-348">Connectez-vous à Outlook Web App en utilisant les informations d’identification de l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="81c6e-348">Sign in to Outlook Web App using User A's credentials.</span></span>
        
    2. <span data-ttu-id="81c6e-349">Effectuez les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="81c6e-349">Perform the following tests:</span></span>
        
    3. <span data-ttu-id="81c6e-350">Testez le courrier électronique 365 Office local.</span><span class="sxs-lookup"><span data-stu-id="81c6e-350">Test local Office 365 email.</span></span> <span data-ttu-id="81c6e-351">Par exemple, envoyez un message électronique à l’utilisateur B. Ce message électronique doit être remis immédiatement.</span><span class="sxs-lookup"><span data-stu-id="81c6e-351">For example, send an email to User B. This email should be delivered immediately.</span></span> <span data-ttu-id="81c6e-352">Dans ce scénario, le message n’est pas acheminé vers la boîte aux lettres de l’utilisateur B sur votre serveur d’origine car Office 365 voit la boîte aux lettres comme étant locale.</span><span class="sxs-lookup"><span data-stu-id="81c6e-352">In this scenario, the message will not be routed to User B's mailbox on your original server because Office 365 sees the mailbox as being local.</span></span>
        
    4. <span data-ttu-id="81c6e-353">Testez le courrier électronique à une personne qui se trouve sur l’autre système de courrier.</span><span class="sxs-lookup"><span data-stu-id="81c6e-353">Test email to someone who's on the other email system.</span></span> <span data-ttu-id="81c6e-354">Par exemple, envoyez un message électronique à l’utilisateur C. Ce message électronique doit être remis à la boîte aux lettres de l’utilisateur C sur votre serveur de messagerie d’origine.</span><span class="sxs-lookup"><span data-stu-id="81c6e-354">For example, send an email to User C. This email should be delivered to User C's mailbox on your original mail server.</span></span>
        
    5. <span data-ttu-id="81c6e-355">À partir d’un compte extérieur ou du compte de messagerie d’un employé sur l’autre système de courrier, vérifiez que le transfert est correctement configuré sur l’autre système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="81c6e-355">From an outside account, or from an employee's email account on the other email system, verify that forwarding is set up properly on the other email system.</span></span> <span data-ttu-id="81c6e-356">Par exemple, à partir du compte de serveur origninal de l’utilisateur C ou d’un compte Hotmail, envoyez un courrier électronique à l’utilisateur et vérifiez qu’il arrive dans la boîte aux lettres Office 365 de l’utilisateur A.</span><span class="sxs-lookup"><span data-stu-id="81c6e-356">For example, from User C's origninal server account or a Hotmail account, send User A an email and verify that it arrives in User A's Office 365 mailbox.</span></span>
        
9. <span data-ttu-id="81c6e-357">Déplacer le contenu de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="81c6e-357">Move mailbox contents</span></span>
    
    1. <span data-ttu-id="81c6e-358">Étant donné que deux utilisateurs seulement peuvent être déplacés, et comme l’utilisateur A et l’utilisateur B utilisent tous deux Outlook, le message peut être déplacé en ouvrant l’ancien. PST dans le nouveau profil Outlook et en copiant les messages, les éléments de calendrier, les contacts, etc., comme indiqué dans importer des éléments Outlook à partir d’un fichier de données Outlook (. pst).</span><span class="sxs-lookup"><span data-stu-id="81c6e-358">Since there are only two users to move, and since User A and User B are both using Outlook already, the email can be moved by opening the old .PST file in the new Outlook profile and copying the messages, calendar items, contacts, etc. as shown in Import Outlook items from an Outlook Data File (.pst).</span></span> <span data-ttu-id="81c6e-359">Une fois organisés aux emplacements appropriés dans la boîte aux lettres Office 365, les éléments sont accessibles à partir de n’importe quel appareil, où qu’ils soient.</span><span class="sxs-lookup"><span data-stu-id="81c6e-359">Once organized in the proper locations in the Office 365 mailbox, the items can all be accessed from any device, anywhere.</span></span>
        
    2. <span data-ttu-id="81c6e-360">Lorsque d’autres boîtes aux lettres sont impliquées, ou si les employés n’utilisent pas encore Outlook, vous pouvez utiliser les outils de migration disponibles dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="81c6e-360">When more mailboxes are involved, or if the employees are not already using Outlook, you can use the migration tools available in the Exchange admin center.</span></span> <span data-ttu-id="81c6e-361">Pour commencer, accédez au centre d’administration Exchange et suivez les instructions de la migration du courrier électronique à partir d’un serveur IMAP vers des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="81c6e-361">To get started, go to Exchange admin center and follow the directions in Migrate Email from an IMAP Server to Exchange Online Mailboxes.</span></span>
    
