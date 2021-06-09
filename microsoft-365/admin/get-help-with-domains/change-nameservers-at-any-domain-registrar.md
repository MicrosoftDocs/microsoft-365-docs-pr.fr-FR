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
ms.openlocfilehash: 7f1ade6cb3013126fb011fe9232b3b4c2e9a82d4
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683126"
---
# <a name="change-nameservers-to-set-up-microsoft-365-with-any-domain-registrar"></a><span data-ttu-id="ebaaa-103">Modifier les serveurs de noms pour configurer Microsoft 365 auprès d’un bureau d’enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="ebaaa-103">Change nameservers to set up Microsoft 365 with any domain registrar</span></span>

 <span data-ttu-id="ebaaa-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ebaaa-105">Suivez ces instructions pour ajouter et configurer votre domaine dans Microsoft 365 afin que vos services tels que le courrier électronique et Teams utilisent votre propre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-105">Follow these instructions to add and set up your domain in Microsoft 365 so your services like email and Teams will use your own domain name.</span></span> <span data-ttu-id="ebaaa-106">Pour ce faire, vous devez vérifier votre domaine, puis modifier les serveurs de noms de votre domaine en Microsoft 365 afin que les enregistrements DNS corrects soient mis en place pour vous.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-106">To do this, you'll verify your domain, and then change your domain's nameservers to Microsoft 365 so the correct DNS records can be set up for you.</span></span> <span data-ttu-id="ebaaa-107">Suivez ces étapes si les instructions suivantes décrivent votre situation :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-107">Follow these steps if the following statements describe your situation:</span></span>
  
- <span data-ttu-id="ebaaa-108">Vous avez votre propre domaine et souhaitez le configurer pour qu’il fonctionne avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-108">You have your own domain and want to set it up to work with Microsoft 365.</span></span>
    
- <span data-ttu-id="ebaaa-109">Vous souhaitez Microsoft 365 gérer vos enregistrements DNS à votre place.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-109">You want Microsoft 365 to manage your DNS records for you.</span></span> <span data-ttu-id="ebaaa-110">Si vous le souhaitez, vous pouvez [gérer vos propres enregistrements DNS](../setup/add-domain.md).</span><span class="sxs-lookup"><span data-stu-id="ebaaa-110">(If you prefer, you can [manage your own DNS records](../setup/add-domain.md).)</span></span>
    
## <a name="add-a-txt-or-mx-record-for-verification"></a><span data-ttu-id="ebaaa-111">Ajouter un enregistrement TXT ou MX à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ebaaa-111">Add a TXT or MX record for verification</span></span>

> [!NOTE]
> <span data-ttu-id="ebaaa-p103">Vous ne devez créer qu'un seul des deux enregistrements. TXT est le type d'enregistrement préféré, mais certains fournisseurs d'hébergement DNS ne le prennent pas en charge, auquel cas vous pouvez créer un enregistrement MX à la place.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-p103">You will create only one or the other of these records. TXT is the preferred record type, but some DNS hosting providers don't support it, in which case you can create an MX record instead.</span></span> 
  
<span data-ttu-id="ebaaa-p104">Avant que vous puissiez utiliser votre domaine avec Microsoft 365, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft 365 que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-p104">Before you use your domain with Microsoft 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ebaaa-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
### <a name="find-the-area-on-your-dns-hosting-providers-website-where-you-can-create-a-new-record"></a><span data-ttu-id="ebaaa-118">Recherchez la zone sur le site web de votre fournisseur d’hébergement DNS où vous pouvez créer un nouvel enregistrement</span><span class="sxs-lookup"><span data-stu-id="ebaaa-118">Find the area on your DNS hosting provider's website where you can create a new record</span></span>

1. <span data-ttu-id="ebaaa-119">Connectez-vous sur le site web de votre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-119">Sign in to your DNS hosting provider's website.</span></span>
    
2. <span data-ttu-id="ebaaa-120">Choisissez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-120">Choose your domain.</span></span>
    
3. <span data-ttu-id="ebaaa-121">Recherchez la page dans laquelle vous pouvez modifier les enregistrements DNS pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-121">Find the page where you can edit DNS records for your domain.</span></span>
    
### <a name="create-the-record"></a><span data-ttu-id="ebaaa-122">Créer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ebaaa-122">Create the record</span></span>

<span data-ttu-id="ebaaa-123">Selon que vous créez un enregistrement TXT ou un enregistrement MX, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-123">Depending on whether you are creating a TXT record or an MX record, do one of the following:</span></span>
  
<span data-ttu-id="ebaaa-124">**Si vous créez un enregistrement TXT, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-124">**If you create a TXT record, use these values:**</span></span>
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ebaaa-125">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-125">**Record Type**</span></span> <br/> |<span data-ttu-id="ebaaa-126">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-126">**Alias** or **Host Name**</span></span> <br/> |<span data-ttu-id="ebaaa-127">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-127">**Value**</span></span> <br/> |<span data-ttu-id="ebaaa-128">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-128">**TTL**</span></span> <br/> |
|<span data-ttu-id="ebaaa-129">TXT</span><span class="sxs-lookup"><span data-stu-id="ebaaa-129">TXT</span></span>  <br/> |<span data-ttu-id="ebaaa-130">Effectuez l'une des opérations suivantes : Tapez **@**, laissez le champ vide ou entrez le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-130">Do one of the following: Type **@** or leave the field empty or type your domain name.</span></span>  <br/> <span data-ttu-id="ebaaa-131">> [!NOTE]> Les conditions requises pour ce champ ne sont pas identiques pour tous les hôtes DNS.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-131">> [!NOTE]> Different DNS hosts have different requirements for this field.</span></span>           
|<span data-ttu-id="ebaaa-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ebaaa-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ebaaa-133">> [!NOTE]> Il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-133">> [!NOTE]> This is an example.</span></span> <span data-ttu-id="ebaaa-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-134">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="ebaaa-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ebaaa-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="ebaaa-136">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-136">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span>  <br/> |
   
<span data-ttu-id="ebaaa-137">**Si vous créez un enregistrement MX, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-137">**If you create an MX record, use these values:**</span></span>
    
||||||
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ebaaa-138">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-138">**Record Type**</span></span>|<span data-ttu-id="ebaaa-139">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-139">**Alias** or **Host Name**</span></span>|<span data-ttu-id="ebaaa-140">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-140">**Value**</span></span>|<span data-ttu-id="ebaaa-141">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-141">**Priority**</span></span>|<span data-ttu-id="ebaaa-142">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-142">**TTL**</span></span>|
|<span data-ttu-id="ebaaa-143">MX</span><span class="sxs-lookup"><span data-stu-id="ebaaa-143">MX</span></span>|<span data-ttu-id="ebaaa-144">Entrez soit **@**, soit votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-144">Type either **@** or your domain name.</span></span> |<span data-ttu-id="ebaaa-145">MS=ms *XXXXXXXX* > [!NOTE]> Il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-145">MS=ms *XXXXXXXX* > [!NOTE]> This is an example.</span></span> <span data-ttu-id="ebaaa-146">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-146">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="ebaaa-147">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="ebaaa-147">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="ebaaa-148">Pour **Priorité**, afin d’éviter les conflits avec l’enregistrement MX utilisé pour le flux de courrier électronique, utilisez une priorité plus basse que la priorité des enregistrements MX existants.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-148">For **Priority**, to avoid conflicts with the MX record used for mail flow, use a lower priority than the priority for any existing MX records.</span></span> <span data-ttu-id="ebaaa-149">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="ebaaa-149">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> |<span data-ttu-id="ebaaa-150">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-150">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span> |
   
### <a name="save-the-record"></a><span data-ttu-id="ebaaa-151">Enregistrer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ebaaa-151">Save the record</span></span>

<span data-ttu-id="ebaaa-152">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-152">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="ebaaa-153">Lorsque Microsoft 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-153">When Microsoft 365 finds the correct TXT record, your domain is verified.</span></span>
  

1. <span data-ttu-id="ebaaa-154">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-154">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="ebaaa-155">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-155">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
  
3. <span data-ttu-id="ebaaa-156">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-156">On the **Setup** page, select **Start setup**.</span></span>
 
  
4. <span data-ttu-id="ebaaa-157">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-157">On the **Verify domain** page, select **Verify**.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="ebaaa-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ebaaa-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="ebaaa-161">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="ebaaa-161">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="ebaaa-162">Lorsque vous arrivez à la dernière étape de l’Assistant Configuration des domaines Microsoft 365, il vous reste une tâche.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-162">When you get to the last step of the domains setup wizard in Microsoft 365, you have one task remaining.</span></span> <span data-ttu-id="ebaaa-163">Pour configurer votre domaine avec des services Microsoft 365, tels que le courrier électronique, vous modifiez les enregistrements de serveur de noms (ou NS) de votre domaine auprès de votre bureau d’enregistrement de domaines pour qu’ils pointent vers les serveurs de noms principal et secondaire Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-163">To set up your domain with Microsoft 365 services, like email, you change your domain's nameserver (or NS) records at your domain registrar to point to the Microsoft 365 primary and secondary nameservers.</span></span> <span data-ttu-id="ebaaa-164">Ensuite, comme Microsoft 365 héberge votre DNS, les enregistrements DNS requis pour vos services sont automatiquement mis en place pour vous.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-164">Then, because Microsoft 365 hosts your DNS, the required DNS records for your services are set up automatically for you.</span></span> <span data-ttu-id="ebaaa-165">Vous pouvez mettre à jour les enregistrements de serveur de noms vous-même en suivant les étapes fournies éventuellement par votre bureau d'enregistrement de domaines dans l'aide disponible sur son site web.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-165">You can update the nameserver records yourself by following the steps your domain registrar may provide in the help content at their website.</span></span> <span data-ttu-id="ebaaa-166">Si vous n'êtes pas familiarisé avec DNS, contactez le support du bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-166">If you're not familiar with DNS, contact support at the domain registrar.</span></span>

::: moniker range="o365-worldwide"
  
<span data-ttu-id="ebaaa-167">Pour changer vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-167">To change your domain's nameservers at your domain registrar's website yourself, follow these steps:</span></span>
  
1. <span data-ttu-id="ebaaa-168">Recherchez la zone sur le site web du bureau d’enregistrement de domaines où vous pouvez modifier les serveurs de noms de votre domaine ou une zone dans laquelle vous pouvez utiliser des serveurs de noms personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-168">Find the area on the domain registrar's website where you can change the nameservers for your domain or an area where you can use custom nameservers.</span></span>
    
2. <span data-ttu-id="ebaaa-169">Créez des enregistrements de nameserver ou modifiez les enregistrements de nameserver existants pour qu’ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-169">Create nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="ebaaa-170">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-170">First nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-171">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ebaaa-171">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="ebaaa-172">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-172">Second nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-173">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ebaaa-173">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="ebaaa-174">Troisième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-174">Third nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-175">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ebaaa-175">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="ebaaa-176">Quatrième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-176">Fourth nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-177">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ebaaa-177">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="ebaaa-178">Il est préférable d’ajouter les quatre enregistrements, mais si votre bureau d’enregistrement ne prend en charge que deux enregistrements, **ajoutez ns1.bdm.microsoftonline.com** et **ns2.bdm.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-178">It's best to add all four records, but if your registrar only supports two, add **ns1.bdm.microsoftonline.com** and **ns2.bdm.microsoftonline.com**.</span></span> 
  
3. <span data-ttu-id="ebaaa-179">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-179">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="ebaaa-180">Lorsque vous modifiez les enregistrements NS de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft 365, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-180">When you change your domain's NS records to point to the Microsoft 365 nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="ebaaa-181">Si vous avez ignoré des étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour des blogs, des paniers ou d’autres services, des étapes supplémentaires sont requises.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-181">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="ebaaa-182">Dans le cas contraire, cette modification risque d’entraîner un temps d’arrêt du service, par exemple l’absence d’accès à la messagerie ou l’in inaccessible de votre site web actuel.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-182">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"
  
1. <span data-ttu-id="ebaaa-183">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-183">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="ebaaa-184">Créez deux enregistrements de serveur de noms, ou modifiez les enregistrements existants pour qu'ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-184">Create two nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="ebaaa-185">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-185">First nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-186">ns1.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="ebaaa-186">ns1.dns.partner.microsoftonline.cn</span></span>  <br/> |
|<span data-ttu-id="ebaaa-187">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ebaaa-187">Second nameserver</span></span>  <br/> |<span data-ttu-id="ebaaa-188">ns2.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="ebaaa-188">ns2.dns.partner.microsoftonline.cn</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="ebaaa-189">Vous devez utiliser au moins deux enregistrements de nameserver.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-189">You should use at least two nameserver records.</span></span> <span data-ttu-id="ebaaa-190">Si d’autres serveurs de noms sont répertoriés, vous pouvez les supprimer ou les remplacer par **ns3.dns.partner.microsoftonline.cn** et **ns4.dns.partner.microsoftonline.cn**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-190">If there are any other nameservers listed, you can either delete them, or change them to **ns3.dns.partner.microsoftonline.cn** and **ns4.dns.partner.microsoftonline.cn**.</span></span> 
  
3. <span data-ttu-id="ebaaa-191">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-191">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="ebaaa-192">Lorsque vous modifiez les enregistrements NS de votre domaine pour qu’ils pointent vers le Office 365 géré par les serveurs de noms 21Vianet, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-192">When you change your domain's NS records to point to the Office 365 operated by 21Vianet nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="ebaaa-193">Si vous avez ignoré des étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour des blogs, des paniers ou d’autres services, des étapes supplémentaires sont requises.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-193">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="ebaaa-194">Dans le cas contraire, cette modification risque d’entraîner un temps d’arrêt du service, par exemple l’absence d’accès à la messagerie ou l’in inaccessible de votre site web actuel.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-194">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end
  
<span data-ttu-id="ebaaa-195">Voici, par exemple, quelques étapes supplémentaires qui peuvent être nécessaires pour le courrier et l'hébergement du site web :</span><span class="sxs-lookup"><span data-stu-id="ebaaa-195">For example, here are some additional steps that might be required for email and website hosting:</span></span>
  
- <span data-ttu-id="ebaaa-196">Déplacez toutes les adresses de messagerie qui utilisent votre domaine Microsoft 365 avant de modifier vos enregistrements NS.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-196">Move all email addresses that use your domain to Microsoft 365 before you change your NS records.</span></span>
    
- <span data-ttu-id="ebaaa-197">Vous souhaitez ajouter un domaine actuellement utilisé avec une adresse de site web, comme www.fourthcoffee.com ?</span><span class="sxs-lookup"><span data-stu-id="ebaaa-197">Want to add a domain that's currently used with a website address, like www.fourthcoffee.com?</span></span> <span data-ttu-id="ebaaa-198">Vous pouvez suivre les étapes ci-dessous pendant que vous ajoutez le domaine pour que son site web reste hébergé là où le site est hébergé maintenant afin que les personnes continuent d’y avoir accès après avoir changé les enregistrements NS du domaine pour qu’ils pointent vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-198">You can take below steps while you add the domain to keep its website hosted where the site is hosted now so people can still get to the website after you change the domain's NS records to point to Microsoft 365.</span></span>

1. <span data-ttu-id="ebaaa-199">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-199">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="ebaaa-200">Dans la page **Domaines**, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-200">On the **Domains** page, select a domain.</span></span>

3. <span data-ttu-id="ebaaa-201">Dans la page des détails du domaine, sélectionnez l’onglet **Enregistrements DNS.**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-201">On the domain details page, select the **DNS records** tab.</span></span>
 
4. <span data-ttu-id="ebaaa-202">Sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-202">Select **Add record**.</span></span>

5. <span data-ttu-id="ebaaa-203">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **A (Address)**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-203">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **A (Address)**.</span></span>

6. <span data-ttu-id="ebaaa-204">Dans la **zone Nom d’hôte ou Alias,** tapez **@** .</span><span class="sxs-lookup"><span data-stu-id="ebaaa-204">In the **Host name or Alias** box, type **@**.</span></span>

7. <span data-ttu-id="ebaaa-205">Dans la zone **Adresse IP,** tapez l’adresse IP statique du site web où elle est actuellement hébergée.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-205">In the **IP Address** box, type the static IP address for the website where it's currently hosted.</span></span> <span data-ttu-id="ebaaa-206">Par exemple, 172.16.140.1.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-206">For example, 172.16.140.1.</span></span>
    
> [!IMPORTANT]
>  <span data-ttu-id="ebaaa-207">Il doit s’agit _d’une_ adresse IP statique pour le site web, et non _d’une adresse_ IP dynamique.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-207">This must be a _static_ IP address for the website, not a _dynamic_ IP address.</span></span> <span data-ttu-id="ebaaa-208">Pour vous assurer que vous pouvez obtenir une adresse IP statique pour votre site web public, vérifiez auprès du site qui héberge votre site web.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-208">To make sure you can get a static IP address for your public website, check with the site that hosts your website.</span></span>
   
8. <span data-ttu-id="ebaaa-209">Si vous souhaitez modifier le paramètre de durée de vie (TTL) de l’enregistrement, sélectionnez une nouvelle durée dans la liste de listes de listes de durée de **vie(TTL).**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-209">If you want to change the TTL setting for the record, select a new length of time from the **TTL** dropdown list.</span></span> <span data-ttu-id="ebaaa-210">Dans le cas contraire, continuez à l’étape 9.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-210">Otherwise, continue to step 9.</span></span>
    
9. <span data-ttu-id="ebaaa-211">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-211">Select **Save**.</span></span> 
    
<span data-ttu-id="ebaaa-212">De plus, vous pouvez créer un enregistrement CNAME pour aider les clients à trouver votre site web.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-212">In addition, you can create a CNAME record to help customers find your website.</span></span>
  
1.  <span data-ttu-id="ebaaa-213">Sélectionnez **Ajouter un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-213">Select **Add record**.</span></span>

3.  <span data-ttu-id="ebaaa-214">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **CNAME (Alias)**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-214">In the **Add a custom DNS record** pane, from the **Type** dropdown list, select **CNAME (Alias)**.</span></span>
4.  <span data-ttu-id="ebaaa-215">Dans la **zone Nom d’hôte ou Alias,** tapez **www**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-215">In the **Host name or Alias** box, type **www**.</span></span>
5.  <span data-ttu-id="ebaaa-216">Dans la **zone Points d’adresse,** tapez le nom de domaine complet (FQDN) de votre site web.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-216">In the **Points to address** box, type the fully qualified domain name (FQDN) for your website.</span></span> <span data-ttu-id="ebaaa-217">Par exemple, **contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-217">For example, **contoso.com**.</span></span>
6.  <span data-ttu-id="ebaaa-218">Si vous souhaitez modifier le paramètre de durée de vie (TTL) de l’enregistrement, sélectionnez une nouvelle durée dans la liste de listes de listes de durée de **vie(TTL).**</span><span class="sxs-lookup"><span data-stu-id="ebaaa-218">If you want to change the TTL setting for the record, select a new length of time from the **TTL** dropdown list.</span></span> <span data-ttu-id="ebaaa-219">Dans le cas contraire, continuez à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-219">Otherwise, continue to step 6.</span></span>
7.  <span data-ttu-id="ebaaa-220">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-220">Select **Save**.</span></span>

<span data-ttu-id="ebaaa-221">Une fois que les enregistrements de serveurs de noms ont été mis à jour pour pointer vers Microsoft, la configuration de votre domaine est terminée.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-221">After the nameserver records are updated to point to Microsoft, your domain setup is complete.</span></span> <span data-ttu-id="ebaaa-222">Le courrier électronique est acheminé vers Microsoft et le trafic vers votre adresse de site web continue d’être acheminé vers votre hôte de site web actuel.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-222">Email is routed to Microsoft, and traffic to your website address continues to go to your current website host.\`</span></span>
    
> [!NOTE]
> <span data-ttu-id="ebaaa-223">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-223">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="ebaaa-224">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ebaaa-224">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="ebaaa-225">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="ebaaa-225">Related content</span></span>

<span data-ttu-id="ebaaa-226">[Ajouter des enregistrements DNS pour connecter votre domaine](create-dns-records-at-any-dns-hosting-provider.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ebaaa-226">[Add DNS records to connect your domain](create-dns-records-at-any-dns-hosting-provider.md) (article)</span></span>\
<span data-ttu-id="ebaaa-227">[Rechercher et corriger les problèmes, y compris de messagerie, après avoir ajouté votre domaine ou des enregistrements DNS](find-and-fix-issues.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ebaaa-227">[Find and fix issues after adding your domain or DNS records](find-and-fix-issues.md) (article)</span></span>\
<span data-ttu-id="ebaaa-228">[Gérer des domaines](index.yml) (page de lien)</span><span class="sxs-lookup"><span data-stu-id="ebaaa-228">[Manage domains](index.yml) (link page)</span></span>
