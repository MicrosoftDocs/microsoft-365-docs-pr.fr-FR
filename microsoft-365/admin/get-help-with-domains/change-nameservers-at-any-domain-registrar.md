---
title: Modifier les serveurs de noms pour configurer Microsoft 365 auprès d’un bureau d’enregistrement de domaines
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
- Adm_TOC
- Adm_O365_Setup
ms.custom:
- okr_smb
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEU150
- GEA150
ms.assetid: a8b487a9-2a45-4581-9dc4-5d28a47010a2
description: Découvrez comment ajouter et configurer votre domaine dans Microsoft 365 afin que vos services tels que la messagerie électronique et Skype Entreprise Online utilisent votre propre nom de domaine.
ms.openlocfilehash: 9c26f9afcf17857c4b3b8f05b89253272cf20e56
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52924502"
---
# <a name="change-nameservers-to-set-up-microsoft-365-with-any-domain-registrar"></a><span data-ttu-id="5c0d6-103">Modifier les serveurs de noms pour configurer Microsoft 365 auprès d’un bureau d’enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="5c0d6-103">Change nameservers to set up Microsoft 365 with any domain registrar</span></span>

 <span data-ttu-id="5c0d6-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="5c0d6-105">Suivez ces instructions pour ajouter et configurer votre domaine dans Microsoft 365 afin que vos services tels que la messagerie Teams utilisent votre propre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-105">Follow these instructions to add and set up your domain in Microsoft 365 so your services like email and Teams will use your own domain name.</span></span> <span data-ttu-id="5c0d6-106">Pour ce faire, vous devez vérifier votre domaine, puis modifier les serveurs de noms de votre domaine en Microsoft 365 afin que les enregistrements DNS corrects soient mis en place pour vous.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-106">To do this, you'll verify your domain, and then change your domain's nameservers to Microsoft 365 so the correct DNS records can be set up for you.</span></span> <span data-ttu-id="5c0d6-107">Suivez ces étapes si les instructions suivantes décrivent votre situation :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-107">Follow these steps if the following statements describe your situation:</span></span>
  
- <span data-ttu-id="5c0d6-108">Vous avez votre propre domaine et souhaitez le configurer pour qu’il fonctionne avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-108">You have your own domain and want to set it up to work with Microsoft 365.</span></span>
    
- <span data-ttu-id="5c0d6-109">Vous souhaitez Microsoft 365 gérer vos enregistrements DNS à votre place.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-109">You want Microsoft 365 to manage your DNS records for you.</span></span> <span data-ttu-id="5c0d6-110">Si vous le souhaitez, vous pouvez [gérer vos propres enregistrements DNS](../setup/add-domain.md).</span><span class="sxs-lookup"><span data-stu-id="5c0d6-110">(If you prefer, you can [manage your own DNS records](../setup/add-domain.md).)</span></span>
    
## <a name="add-a-txt-or-mx-record-for-verification"></a><span data-ttu-id="5c0d6-111">Ajouter un enregistrement TXT ou MX à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="5c0d6-111">Add a TXT or MX record for verification</span></span>

> [!NOTE]
> <span data-ttu-id="5c0d6-p103">Vous ne devez créer qu'un seul des deux enregistrements. TXT est le type d'enregistrement préféré, mais certains fournisseurs d'hébergement DNS ne le prennent pas en charge, auquel cas vous pouvez créer un enregistrement MX à la place.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-p103">You will create only one or the other of these records. TXT is the preferred record type, but some DNS hosting providers don't support it, in which case you can create an MX record instead.</span></span> 
  
<span data-ttu-id="5c0d6-p104">Avant que vous puissiez utiliser votre domaine avec Microsoft 365, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft 365 que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-p104">Before you use your domain with Microsoft 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5c0d6-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
### <a name="find-the-area-on-your-dns-hosting-providers-website-where-you-can-create-a-new-record"></a><span data-ttu-id="5c0d6-118">Recherchez la zone sur le site web de votre fournisseur d’hébergement DNS où vous pouvez créer un nouvel enregistrement</span><span class="sxs-lookup"><span data-stu-id="5c0d6-118">Find the area on your DNS hosting provider's website where you can create a new record</span></span>

1. <span data-ttu-id="5c0d6-119">Connectez-vous sur le site web de votre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-119">Sign in to your DNS hosting provider's website.</span></span>
    
2. <span data-ttu-id="5c0d6-120">Choisissez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-120">Choose your domain.</span></span>
    
3. <span data-ttu-id="5c0d6-121">Recherchez la page dans laquelle vous pouvez modifier les enregistrements DNS pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-121">Find the page where you can edit DNS records for your domain.</span></span>
    
### <a name="create-the-record"></a><span data-ttu-id="5c0d6-122">Créer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5c0d6-122">Create the record</span></span>

<span data-ttu-id="5c0d6-123">Selon que vous créez un enregistrement TXT ou un enregistrement MX, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-123">Depending on whether you are creating a TXT record or an MX record, do one of the following:</span></span>
  
<span data-ttu-id="5c0d6-124">**Si vous créez un enregistrement TXT, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-124">**If you create a TXT record, use these values:**</span></span>
    

|<span data-ttu-id="5c0d6-125">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5c0d6-125">Record type</span></span><br/> |<span data-ttu-id="5c0d6-126">Alias ou nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="5c0d6-126">Alias or host name</span></span> <br/> |<span data-ttu-id="5c0d6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c0d6-127">Value</span></span> <br/> |<span data-ttu-id="5c0d6-128">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="5c0d6-128">TTL</span></span><br/> |
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c0d6-129">TXT</span><span class="sxs-lookup"><span data-stu-id="5c0d6-129">TXT</span></span>  <br/> |<span data-ttu-id="5c0d6-130">Effectuez l'une des opérations suivantes : Tapez **@**, laissez le champ vide ou entrez le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-130">Do one of the following: Type **@** or leave the field empty or type your domain name.</span></span>  <br/> <span data-ttu-id="5c0d6-131">> [!NOTE]> Les conditions requises pour ce champ ne sont pas identiques pour tous les hôtes DNS.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-131">> [!NOTE]> Different DNS hosts have different requirements for this field.</span></span>           
|<span data-ttu-id="5c0d6-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="5c0d6-132">MS=ms *XXXXXXXX*</span></span>  <br/><span data-ttu-id="5c0d6-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-133">**Note:** This is an example.</span></span> <span data-ttu-id="5c0d6-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-134">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="5c0d6-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="5c0d6-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="5c0d6-136">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-136">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span>  <br/> |
   
<span data-ttu-id="5c0d6-137">**Si vous créez un enregistrement MX, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-137">**If you create an MX record, use these values:**</span></span>
    
|<span data-ttu-id="5c0d6-138">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5c0d6-138">Record type</span></span>|<span data-ttu-id="5c0d6-139">Alias ou nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="5c0d6-139">Alias or host name</span></span>|<span data-ttu-id="5c0d6-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c0d6-140">Value</span></span>|<span data-ttu-id="5c0d6-141">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="5c0d6-141">Priority</span></span>|<span data-ttu-id="5c0d6-142">TTL (Durée de vie)</span><span class="sxs-lookup"><span data-stu-id="5c0d6-142">TTL</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5c0d6-143">MX</span><span class="sxs-lookup"><span data-stu-id="5c0d6-143">MX</span></span>|<span data-ttu-id="5c0d6-144">Entrez soit **@**, soit votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-144">Type either **@** or your domain name.</span></span> |<span data-ttu-id="5c0d6-145">MS=ms *XXXXXXXX* **Note : Il** s’agit d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-145">MS=ms *XXXXXXXX* **Note:** This is an example.</span></span> <span data-ttu-id="5c0d6-146">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-146">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="5c0d6-147">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="5c0d6-147">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="5c0d6-148">Pour **Priorité**, afin d’éviter les conflits avec l’enregistrement MX utilisé pour le flux de courrier électronique, utilisez une priorité plus basse que la priorité des enregistrements MX existants.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-148">For **Priority**, to avoid conflicts with the MX record used for mail flow, use a lower priority than the priority for any existing MX records.</span></span> <span data-ttu-id="5c0d6-149">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="5c0d6-149">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> |<span data-ttu-id="5c0d6-150">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-150">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span> |
   
### <a name="save-the-record"></a><span data-ttu-id="5c0d6-151">Enregistrer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5c0d6-151">Save the record</span></span>

<span data-ttu-id="5c0d6-152">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-152">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="5c0d6-153">Lorsque Microsoft 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-153">When Microsoft 365 finds the correct TXT record, your domain is verified.</span></span>
  

1. <span data-ttu-id="5c0d6-154">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-154">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="5c0d6-155">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-155">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
  
3. <span data-ttu-id="5c0d6-156">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-156">On the **Setup** page, select **Start setup**.</span></span>
 
  
4. <span data-ttu-id="5c0d6-157">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-157">On the **Verify domain** page, select **Verify**.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="5c0d6-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="5c0d6-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="5c0d6-161">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="5c0d6-161">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="5c0d6-162">Lorsque vous arrivez à la dernière étape de l’Assistant Configuration des domaines Microsoft 365, il vous reste une tâche.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-162">When you get to the last step of the domains setup wizard in Microsoft 365, you have one task remaining.</span></span> <span data-ttu-id="5c0d6-163">Pour configurer votre domaine avec des services Microsoft 365, tels que le courrier électronique, vous modifiez les enregistrements de serveur de noms (ou NS) de votre domaine auprès de votre bureau d’enregistrement de domaines pour qu’ils pointent vers les serveurs de noms principal et secondaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-163">To set up your domain with Microsoft 365 services, like email, you change your domain's nameserver (or NS) records at your domain registrar to point to the Microsoft 365 primary and secondary nameservers.</span></span> <span data-ttu-id="5c0d6-164">Ensuite, comme Microsoft 365 héberge votre DNS, les enregistrements DNS requis pour vos services sont automatiquement mis en place pour vous.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-164">Then, because Microsoft 365 hosts your DNS, the required DNS records for your services are set up automatically for you.</span></span> <span data-ttu-id="5c0d6-165">Vous pouvez mettre à jour les enregistrements de serveur de noms vous-même en suivant les étapes fournies éventuellement par votre bureau d'enregistrement de domaines dans l'aide disponible sur son site web.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-165">You can update the nameserver records yourself by following the steps your domain registrar may provide in the help content at their website.</span></span> <span data-ttu-id="5c0d6-166">Si vous n'êtes pas familiarisé avec DNS, contactez le support du bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-166">If you're not familiar with DNS, contact support at the domain registrar.</span></span>

::: moniker range="o365-worldwide"
  
<span data-ttu-id="5c0d6-167">Pour changer vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-167">To change your domain's nameservers at your domain registrar's website yourself, follow these steps:</span></span>
  
1. <span data-ttu-id="5c0d6-168">Recherchez la zone sur le site web du bureau d’enregistrement de domaines où vous pouvez modifier les serveurs de noms de votre domaine ou une zone dans laquelle vous pouvez utiliser des serveurs de noms personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-168">Find the area on the domain registrar's website where you can change the nameservers for your domain or an area where you can use custom nameservers.</span></span>
    
2. <span data-ttu-id="5c0d6-169">Créez des enregistrements de nameserver ou modifiez les enregistrements de nameserver existants pour qu’ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-169">Create nameserver records, or edit the existing nameserver records to match the following values:</span></span>

    - <span data-ttu-id="5c0d6-170">Premier nameserver : ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="5c0d6-170">First nameserver: ns1.bdm.microsoftonline.com</span></span>
    - <span data-ttu-id="5c0d6-171">Second nameserver: ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="5c0d6-171">Second nameserver: ns2.bdm.microsoftonline.com</span></span>
    - <span data-ttu-id="5c0d6-172">Troisième nameserver : ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="5c0d6-172">Third nameserver: ns3.bdm.microsoftonline.com</span></span>
    - <span data-ttu-id="5c0d6-173">Quatrième nameserver : ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="5c0d6-173">Fourth nameserver: ns4.bdm.microsoftonline.com</span></span>
      
   
   > [!TIP]
   > <span data-ttu-id="5c0d6-174">Il est préférable d’ajouter les quatre enregistrements, mais si votre bureau d’enregistrement ne prend en charge que deux enregistrements, **ajoutez ns1.bdm.microsoftonline.com** et **ns2.bdm.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-174">It's best to add all four records, but if your registrar only supports two, add **ns1.bdm.microsoftonline.com** and **ns2.bdm.microsoftonline.com**.</span></span> 
  
3. <span data-ttu-id="5c0d6-175">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-175">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="5c0d6-176">Lorsque vous modifiez les enregistrements NS de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft 365, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-176">When you change your domain's NS records to point to the Microsoft 365 nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="5c0d6-177">Si vous avez ignoré des étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour des blogs, des paniers ou d’autres services, d’autres étapes sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-177">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="5c0d6-178">Dans le cas contraire, cette modification risque d’entraîner un temps d’arrêt du service, par exemple l’absence d’accès à la messagerie ou l’in inaccessible de votre site web actuel.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-178">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"
  
1. <span data-ttu-id="5c0d6-179">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-179">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="5c0d6-180">Créez deux enregistrements de serveur de noms, ou modifiez les enregistrements existants pour qu'ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-180">Create two nameserver records, or edit the existing nameserver records to match the following values:</span></span>

   - <span data-ttu-id="5c0d6-181">Premier nameserver : ns1.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="5c0d6-181">First nameserver: ns1.dns.partner.microsoftonline.cn</span></span>
   - <span data-ttu-id="5c0d6-182">Second nameserver: ns2.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="5c0d6-182">Second nameserver: ns2.dns.partner.microsoftonline.cn</span></span>
    
   > [!TIP]
   > <span data-ttu-id="5c0d6-183">Vous devez utiliser au moins deux enregistrements de nameserver.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-183">You should use at least two nameserver records.</span></span> <span data-ttu-id="5c0d6-184">Si d’autres serveurs de noms sont répertoriés, vous pouvez les supprimer ou les remplacer par **ns3.dns.partner.microsoftonline.cn** et **ns4.dns.partner.microsoftonline.cn**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-184">If there are any other nameservers listed, you can either delete them, or change them to **ns3.dns.partner.microsoftonline.cn** and **ns4.dns.partner.microsoftonline.cn**.</span></span> 
  
3. <span data-ttu-id="5c0d6-185">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-185">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="5c0d6-186">Lorsque vous modifiez les enregistrements NS de votre domaine pour qu’ils pointent vers le Office 365 géré par les serveurs de noms 21Vianet, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-186">When you change your domain's NS records to point to the Office 365 operated by 21Vianet nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="5c0d6-187">Si vous avez ignoré des étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour des blogs, des paniers ou d’autres services, d’autres étapes sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-187">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="5c0d6-188">Dans le cas contraire, cette modification risque d’entraîner un temps d’arrêt du service, par exemple l’absence d’accès à la messagerie ou l’in inaccessible de votre site web actuel.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-188">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end
  
<span data-ttu-id="5c0d6-189">Voici, par exemple, quelques étapes supplémentaires qui peuvent être nécessaires pour le courrier et l'hébergement du site web :</span><span class="sxs-lookup"><span data-stu-id="5c0d6-189">For example, here are some additional steps that might be required for email and website hosting:</span></span>
  
- <span data-ttu-id="5c0d6-190">Déplacez toutes les adresses de messagerie qui utilisent votre domaine Microsoft 365 avant de modifier vos enregistrements NS.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-190">Move all email addresses that use your domain to Microsoft 365 before you change your NS records.</span></span>
    
- <span data-ttu-id="5c0d6-191">Vous souhaitez ajouter un domaine actuellement utilisé avec une adresse de site web, comme www.fourthcoffee.com ?</span><span class="sxs-lookup"><span data-stu-id="5c0d6-191">Want to add a domain that's currently used with a website address, like www.fourthcoffee.com?</span></span> <span data-ttu-id="5c0d6-192">Vous pouvez suivre les étapes ci-dessous pendant que vous ajoutez le domaine pour que son site web reste hébergé là où le site est hébergé maintenant afin que les personnes continuent d’y avoir accès après avoir changé les enregistrements NS du domaine pour qu’ils pointent vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-192">You can take below steps while you add the domain to keep its website hosted where the site is hosted now so people can still get to the website after you change the domain's NS records to point to Microsoft 365.</span></span>

1. <span data-ttu-id="5c0d6-193">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-193">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="5c0d6-194">Dans la page **Domaines**, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-194">On the **Domains** page, select a domain.</span></span>

3. <span data-ttu-id="5c0d6-195">Dans la page des détails du domaine, sélectionnez l’onglet **Enregistrements DNS.**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-195">On the domain details page, select the **DNS records** tab.</span></span>
 
4. <span data-ttu-id="5c0d6-196">Sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-196">Select **Add record**.</span></span>

5. <span data-ttu-id="5c0d6-197">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **A (Address)**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-197">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **A (Address)**.</span></span>

6. <span data-ttu-id="5c0d6-198">Dans la **zone Nom d’hôte ou Alias,** tapez **@** .</span><span class="sxs-lookup"><span data-stu-id="5c0d6-198">In the **Host name or Alias** box, type **@**.</span></span>

7. <span data-ttu-id="5c0d6-199">Dans la zone **Adresse IP,** tapez l’adresse IP statique du site web où elle est actuellement hébergée.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-199">In the **IP Address** box, type the static IP address for the website where it's currently hosted.</span></span> <span data-ttu-id="5c0d6-200">Par exemple, 172.16.140.1.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-200">For example, 172.16.140.1.</span></span>
    
> [!IMPORTANT]
>  <span data-ttu-id="5c0d6-201">Il doit s’agit _d’une_ adresse IP statique pour le site web, et non _d’une adresse_ IP dynamique.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-201">This must be a _static_ IP address for the website, not a _dynamic_ IP address.</span></span> <span data-ttu-id="5c0d6-202">Pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public, vérifiez auprès du site qui héberge votre site web.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-202">To make sure you can get a static IP address for your public website, check with the site that hosts your website.</span></span>
   
8. <span data-ttu-id="5c0d6-203">Si vous souhaitez modifier le paramètre de durée de vie (TTL) de l’enregistrement, sélectionnez une nouvelle durée dans la liste de listes de listes de durée de **vie(TTL).**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-203">If you want to change the TTL setting for the record, select a new length of time from the **TTL** dropdown list.</span></span> <span data-ttu-id="5c0d6-204">Dans le cas contraire, continuez à l’étape 9.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-204">Otherwise, continue to step 9.</span></span>
    
9. <span data-ttu-id="5c0d6-205">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-205">Select **Save**.</span></span> 
    
<span data-ttu-id="5c0d6-206">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-206">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1.  <span data-ttu-id="5c0d6-207">Sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-207">Select **Add record**.</span></span>

3.  <span data-ttu-id="5c0d6-208">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **CNAME (Alias)**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-208">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **CNAME (Alias)**.</span></span>
4.  <span data-ttu-id="5c0d6-209">Dans la **zone Nom d’hôte ou Alias,** tapez **www**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-209">In the **Host name or Alias** box, type **www**.</span></span>
5.  <span data-ttu-id="5c0d6-210">Dans la **zone Points d’adresse,** tapez le nom de domaine complet (FQDN) de votre site web.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-210">In the **Points to address** box, type the fully qualified domain name (FQDN) for your website.</span></span> <span data-ttu-id="5c0d6-211">Par exemple, **contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-211">For example, **contoso.com**.</span></span>
6.  <span data-ttu-id="5c0d6-212">Si vous souhaitez modifier le paramètre de durée de vie (TTL) de l’enregistrement, sélectionnez une nouvelle durée dans la liste de listes de listes de durée de **vie(TTL).**</span><span class="sxs-lookup"><span data-stu-id="5c0d6-212">If you want to change the TTL setting for the record, select a new length of time from the **TTL** dropdown list.</span></span> <span data-ttu-id="5c0d6-213">Dans le cas contraire, continuez à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-213">Otherwise, continue to step 6.</span></span>
7.  <span data-ttu-id="5c0d6-214">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-214">Select **Save**.</span></span>

<span data-ttu-id="5c0d6-215">Une fois que les enregistrements de serveurs de noms ont été mis à jour pour pointer vers Microsoft, la configuration de votre domaine est terminée.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-215">After the nameserver records are updated to point to Microsoft, your domain setup is complete.</span></span> <span data-ttu-id="5c0d6-216">Le courrier électronique est acheminé vers Microsoft et le trafic vers votre adresse de site web continue d’être acheminé vers votre hôte de site web actuel.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-216">Email is routed to Microsoft, and traffic to your website address continues to go to your current website host.\`</span></span>
    
> [!NOTE]
> <span data-ttu-id="5c0d6-217">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-217">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="5c0d6-218">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="5c0d6-218">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="5c0d6-219">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="5c0d6-219">Related content</span></span>

<span data-ttu-id="5c0d6-220">[Ajouter des enregistrements DNS pour connecter votre domaine](create-dns-records-at-any-dns-hosting-provider.md) (article)</span><span class="sxs-lookup"><span data-stu-id="5c0d6-220">[Add DNS records to connect your domain](create-dns-records-at-any-dns-hosting-provider.md) (article)</span></span>\
<span data-ttu-id="5c0d6-221">[Rechercher et corriger les problèmes, y compris de messagerie, après avoir ajouté votre domaine ou des enregistrements DNS](find-and-fix-issues.md) (article)</span><span class="sxs-lookup"><span data-stu-id="5c0d6-221">[Find and fix issues after adding your domain or DNS records](find-and-fix-issues.md) (article)</span></span>\
<span data-ttu-id="5c0d6-222">[Gérer des domaines](index.yml) (page de lien)</span><span class="sxs-lookup"><span data-stu-id="5c0d6-222">[Manage domains](index.yml) (link page)</span></span>
