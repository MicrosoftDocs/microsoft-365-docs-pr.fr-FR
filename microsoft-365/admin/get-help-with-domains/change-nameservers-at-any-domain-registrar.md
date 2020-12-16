---
title: Modifier les serveurs de noms pour configurer Microsoft 365 avec n’importe quel bureau d’enregistrement de domaines
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
description: Découvrez comment ajouter et configurer votre domaine dans Microsoft 365 afin que vos services de messagerie électronique et Skype entreprise Online utilisent votre propre nom de domaine.
ms.openlocfilehash: 492bc5d2a5f3fd9810f045e7effda1ea20fa15ed
ms.sourcegitcommit: 849b365bd3eaa9f3c3a9ef9f5973ef81af9156fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49688248"
---
# <a name="change-nameservers-to-set-up-microsoft-365-with-any-domain-registrar"></a><span data-ttu-id="3d982-103">Modifier les serveurs de noms pour configurer Microsoft 365 avec n’importe quel bureau d’enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="3d982-103">Change nameservers to set up Microsoft 365 with any domain registrar</span></span>

 <span data-ttu-id="3d982-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="3d982-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="3d982-105">Consultez [la rubrique Configurer votre domaine (instructions spécifiques à l’hôte)](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) pour savoir si nous avons des instructions pour votre serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="3d982-105">Check [Set up your domain (host-specific instructions)](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) first to see if we have instructions for your registrar.</span></span> 
  
<span data-ttu-id="3d982-106">Suivez ces instructions pour ajouter et configurer votre domaine dans Microsoft 365 afin que vos services, tels que le courrier électronique et les équipes, utilisent votre propre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-106">Follow these instructions to add and set up your domain in Microsoft 365 so your services like email and Teams will use your own domain name.</span></span> <span data-ttu-id="3d982-107">Pour ce faire, vous devez vérifier votre domaine, puis modifier les serveurs de noms de votre domaine en Microsoft 365 afin que les enregistrements DNS corrects puissent être configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="3d982-107">To do this, you'll verify your domain, and then change your domain's nameservers to Microsoft 365 so the correct DNS records can be set up for you.</span></span> <span data-ttu-id="3d982-108">Procédez comme suit si les instructions suivantes décrivent votre situation :</span><span class="sxs-lookup"><span data-stu-id="3d982-108">Follow these steps if the following statements describe your situation:</span></span>
  
- <span data-ttu-id="3d982-109">Vous disposez de votre propre domaine et souhaitez le configurer pour qu’il fonctionne avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d982-109">You have your own domain and want to set it up to work with Microsoft 365.</span></span>
    
- <span data-ttu-id="3d982-110">Vous souhaitez que Microsoft 365 gère vos enregistrements DNS pour vous.</span><span class="sxs-lookup"><span data-stu-id="3d982-110">You want Microsoft 365 to manage your DNS records for you.</span></span> <span data-ttu-id="3d982-111">Si vous le souhaitez, vous pouvez [gérer vos propres enregistrements DNS](../setup/add-domain.md).</span><span class="sxs-lookup"><span data-stu-id="3d982-111">(If you prefer, you can [manage your own DNS records](../setup/add-domain.md).)</span></span>
    
## <a name="add-a-txt-or-mx-record-for-verification"></a><span data-ttu-id="3d982-112">Ajouter un enregistrement TXT ou MX à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="3d982-112">Add a TXT or MX record for verification</span></span>
<span data-ttu-id="3d982-113"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="3d982-113"><a name="BKMK_verify"> </a></span></span>

> [!NOTE]
> <span data-ttu-id="3d982-p103">Vous ne devez créer qu'un seul des deux enregistrements. TXT est le type d'enregistrement préféré, mais certains fournisseurs d'hébergement DNS ne le prennent pas en charge, auquel cas vous pouvez créer un enregistrement MX à la place.</span><span class="sxs-lookup"><span data-stu-id="3d982-p103">You will create only one or the other of these records. TXT is the preferred record type, but some DNS hosting providers don't support it, in which case you can create an MX record instead.</span></span> 
  
<span data-ttu-id="3d982-p104">Avant que vous puissiez utiliser votre domaine avec Microsoft 365, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft 365 que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="3d982-p104">Before you use your domain with Microsoft 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3d982-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3d982-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
### <a name="find-the-area-on-your-dns-hosting-providers-website-where-you-can-create-a-new-record"></a><span data-ttu-id="3d982-120">Recherchez la zone sur le site Web de votre fournisseur d’hébergement DNS où vous pouvez créer un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3d982-120">Find the area on your DNS hosting provider's website where you can create a new record</span></span>

1. <span data-ttu-id="3d982-121">Connectez-vous sur le site web de votre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="3d982-121">Sign in to your DNS hosting provider's website.</span></span>
    
2. <span data-ttu-id="3d982-122">Choisissez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-122">Choose your domain.</span></span>
    
3. <span data-ttu-id="3d982-123">Recherchez la page dans laquelle vous pouvez modifier les enregistrements DNS pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-123">Find the page where you can edit DNS records for your domain.</span></span>
    
### <a name="create-the-record"></a><span data-ttu-id="3d982-124">Créer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="3d982-124">Create the record</span></span>

<span data-ttu-id="3d982-125">Selon que vous créez un enregistrement TXT ou un enregistrement MX, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d982-125">Depending on whether you are creating a TXT record or an MX record, do one of the following:</span></span>
  
<span data-ttu-id="3d982-126">**Si vous créez un enregistrement TXT, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="3d982-126">**If you create a TXT record, use these values:**</span></span>
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3d982-127">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="3d982-127">**Record Type**</span></span> <br/> |<span data-ttu-id="3d982-128">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="3d982-128">**Alias** or **Host Name**</span></span> <br/> |<span data-ttu-id="3d982-129">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3d982-129">**Value**</span></span> <br/> |<span data-ttu-id="3d982-130">**TTL**</span><span class="sxs-lookup"><span data-stu-id="3d982-130">**TTL**</span></span> <br/> |
|<span data-ttu-id="3d982-131">TXT</span><span class="sxs-lookup"><span data-stu-id="3d982-131">TXT</span></span>  <br/> |<span data-ttu-id="3d982-132">Effectuez l'une des opérations suivantes : Tapez **@**, laissez le champ vide ou entrez le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-132">Do one of the following: Type **@** or leave the field empty or type your domain name.</span></span>  <br/> <span data-ttu-id="3d982-133">> [!NOTE]> Les conditions requises pour ce champ ne sont pas identiques pour tous les hôtes DNS.</span><span class="sxs-lookup"><span data-stu-id="3d982-133">> [!NOTE]> Different DNS hosts have different requirements for this field.</span></span>           
|<span data-ttu-id="3d982-134">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="3d982-134">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="3d982-135">> [!NOTE]> Il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="3d982-135">> [!NOTE]> This is an example.</span></span> <span data-ttu-id="3d982-136">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d982-136">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="3d982-137">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="3d982-137">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="3d982-138">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="3d982-138">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span>  <br/> |
   
<span data-ttu-id="3d982-139">**Si vous créez un enregistrement MX, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="3d982-139">**If you create an MX record, use these values:**</span></span>
    
||||||
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3d982-140">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="3d982-140">**Record Type**</span></span>|<span data-ttu-id="3d982-141">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="3d982-141">**Alias** or **Host Name**</span></span>|<span data-ttu-id="3d982-142">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3d982-142">**Value**</span></span>|<span data-ttu-id="3d982-143">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="3d982-143">**Priority**</span></span>|<span data-ttu-id="3d982-144">**TTL**</span><span class="sxs-lookup"><span data-stu-id="3d982-144">**TTL**</span></span>|
|<span data-ttu-id="3d982-145">MX</span><span class="sxs-lookup"><span data-stu-id="3d982-145">MX</span></span>|<span data-ttu-id="3d982-146">Entrez soit **@**, soit votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-146">Type either **@** or your domain name.</span></span> |<span data-ttu-id="3d982-147">MS=ms *XXXXXXXX* > [!NOTE]> Il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="3d982-147">MS=ms *XXXXXXXX* > [!NOTE]> This is an example.</span></span> <span data-ttu-id="3d982-148">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d982-148">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span>           [<span data-ttu-id="3d982-149">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="3d982-149">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="3d982-150">Pour **Priorité**, afin d’éviter les conflits avec l’enregistrement MX utilisé pour le flux de courrier électronique, utilisez une priorité plus basse que la priorité des enregistrements MX existants.</span><span class="sxs-lookup"><span data-stu-id="3d982-150">For **Priority**, to avoid conflicts with the MX record used for mail flow, use a lower priority than the priority for any existing MX records.</span></span> <span data-ttu-id="3d982-151">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="3d982-151">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> |<span data-ttu-id="3d982-152">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="3d982-152">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span> |
   
### <a name="save-the-record"></a><span data-ttu-id="3d982-153">Enregistrer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="3d982-153">Save the record</span></span>

<span data-ttu-id="3d982-154">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3d982-154">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="3d982-155">Lorsque Microsoft 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="3d982-155">When Microsoft 365 finds the correct TXT record, your domain is verified.</span></span>
  

1. <span data-ttu-id="3d982-156">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="3d982-156">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="3d982-157">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="3d982-157">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
  
3. <span data-ttu-id="3d982-158">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="3d982-158">On the **Setup** page, select **Start setup**.</span></span>
 
    
  
4. <span data-ttu-id="3d982-159">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="3d982-159">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="3d982-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="3d982-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="3d982-163">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="3d982-163">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="3d982-164"><a name="BKMK_nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="3d982-164"><a name="BKMK_nameservers"> </a></span></span>

<span data-ttu-id="3d982-165">Lorsque vous accédez à la dernière étape de l’Assistant Configuration des domaines dans Microsoft 365, vous disposez d’une tâche restante.</span><span class="sxs-lookup"><span data-stu-id="3d982-165">When you get to the last step of the domains setup wizard in Microsoft 365, you have one task remaining.</span></span> <span data-ttu-id="3d982-166">Pour configurer votre domaine avec les services Microsoft 365, tels que le courrier électronique, vous devez modifier les enregistrements nameserver (ou NS) de votre domaine au niveau de votre bureau d’enregistrement de domaines afin de pointer vers les serveurs de noms principaux et secondaires de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d982-166">To set up your domain with Microsoft 365 services, like email, you change your domain's nameserver (or NS) records at your domain registrar to point to the Microsoft 365 primary and secondary nameservers.</span></span> <span data-ttu-id="3d982-167">Ensuite, étant donné que Microsoft 365 héberge votre DNS, les enregistrements DNS requis pour vos services sont configurés automatiquement pour vous.</span><span class="sxs-lookup"><span data-stu-id="3d982-167">Then, because Microsoft 365 hosts your DNS, the required DNS records for your services are set up automatically for you.</span></span> <span data-ttu-id="3d982-168">Vous pouvez mettre à jour les enregistrements de serveur de noms vous-même en suivant les étapes fournies éventuellement par votre bureau d'enregistrement de domaines dans l'aide disponible sur son site web.</span><span class="sxs-lookup"><span data-stu-id="3d982-168">You can update the nameserver records yourself by following the steps your domain registrar may provide in the help content at their website.</span></span> <span data-ttu-id="3d982-169">Si vous n'êtes pas familiarisé avec DNS, contactez le support du bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="3d982-169">If you're not familiar with DNS, contact support at the domain registrar.</span></span>

::: moniker range="o365-worldwide"
  
<span data-ttu-id="3d982-170">Pour changer vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3d982-170">To change your domain's nameservers at your domain registrar's website yourself, follow these steps:</span></span>
  
1. <span data-ttu-id="3d982-171">Recherchez la zone sur le site Web du Bureau d’enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms de votre domaine ou une zone dans laquelle vous pouvez utiliser des serveurs de noms personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3d982-171">Find the area on the domain registrar's website where you can change the nameservers for your domain or an area where you can use custom nameservers.</span></span>
    
2. <span data-ttu-id="3d982-172">Créez des enregistrements de serveur de noms ou modifiez les enregistrements de serveur de noms existants pour qu’ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d982-172">Create nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="3d982-173">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-173">First nameserver</span></span>  <br/> |<span data-ttu-id="3d982-174">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3d982-174">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3d982-175">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-175">Second nameserver</span></span>  <br/> |<span data-ttu-id="3d982-176">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3d982-176">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3d982-177">Troisième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-177">Third nameserver</span></span>  <br/> |<span data-ttu-id="3d982-178">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3d982-178">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3d982-179">Quatrième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-179">Fourth nameserver</span></span>  <br/> |<span data-ttu-id="3d982-180">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3d982-180">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="3d982-181">Il est préférable d’ajouter les quatre enregistrements, mais si votre serveur d’inscriptions ne prend en charge que deux, ajoutez **NS1.BDM.microsoftonline.com** et **ns2.BDM.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="3d982-181">It's best to add all four records, but if your registrar only supports two, add **ns1.bdm.microsoftonline.com** and **ns2.bdm.microsoftonline.com**.</span></span> 
  
3. <span data-ttu-id="3d982-182">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="3d982-182">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="3d982-183">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft 365, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="3d982-183">When you change your domain's NS records to point to the Microsoft 365 nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="3d982-184">Si vous avez ignoré les étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour les blogs, les paniers d’achat ou d’autres services, des étapes supplémentaires sont requises.</span><span class="sxs-lookup"><span data-stu-id="3d982-184">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="3d982-185">Dans le cas contraire, cette modification pourrait entraîner un temps d’arrêt du service, tel qu’un manque d’accès à la messagerie ou votre site Web actuel inaccessible.</span><span class="sxs-lookup"><span data-stu-id="3d982-185">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"
  
1. <span data-ttu-id="3d982-186">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-186">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="3d982-187">Créez deux enregistrements de serveur de noms, ou modifiez les enregistrements existants pour qu'ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d982-187">Create two nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="3d982-188">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-188">First nameserver</span></span>  <br/> |<span data-ttu-id="3d982-189">ns1.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="3d982-189">ns1.dns.partner.microsoftonline.cn</span></span>  <br/> |
|<span data-ttu-id="3d982-190">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="3d982-190">Second nameserver</span></span>  <br/> |<span data-ttu-id="3d982-191">ns2.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="3d982-191">ns2.dns.partner.microsoftonline.cn</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="3d982-192">Vous devez utiliser au moins deux enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="3d982-192">You should use at least two nameserver records.</span></span> <span data-ttu-id="3d982-193">Si d’autres serveurs de noms sont répertoriés, vous pouvez les supprimer ou les remplacer par **NS3.DNS.Partner.microsoftonline.CN** et **NS4.DNS.Partner.microsoftonline.CN**.</span><span class="sxs-lookup"><span data-stu-id="3d982-193">If there are any other nameservers listed, you can either delete them, or change them to **ns3.dns.partner.microsoftonline.cn** and **ns4.dns.partner.microsoftonline.cn**.</span></span> 
  
3. <span data-ttu-id="3d982-194">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="3d982-194">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="3d982-195">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers l’Office 365 géré par les serveurs de noms 21Vianet, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="3d982-195">When you change your domain's NS records to point to the Office 365 operated by 21Vianet nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="3d982-196">Si vous avez ignoré les étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour les blogs, les paniers d’achat ou d’autres services, des étapes supplémentaires sont requises.</span><span class="sxs-lookup"><span data-stu-id="3d982-196">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="3d982-197">Dans le cas contraire, cette modification pourrait entraîner un temps d’arrêt du service, tel qu’un manque d’accès à la messagerie ou votre site Web actuel inaccessible.</span><span class="sxs-lookup"><span data-stu-id="3d982-197">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end
  
<span data-ttu-id="3d982-198">Voici, par exemple, quelques étapes supplémentaires qui peuvent être nécessaires pour le courrier et l'hébergement du site web :</span><span class="sxs-lookup"><span data-stu-id="3d982-198">For example, here are some additional steps that might be required for email and website hosting:</span></span>
  
- <span data-ttu-id="3d982-199">Déplacez toutes les adresses de messagerie qui utilisent votre domaine vers Microsoft 365 avant de modifier vos enregistrements NS.</span><span class="sxs-lookup"><span data-stu-id="3d982-199">Move all email addresses that use your domain to Microsoft 365 before you change your NS records.</span></span>
    
- <span data-ttu-id="3d982-200">Vous souhaitez ajouter un domaine actuellement utilisé avec une adresse de site Web, par exemple www.fourthcoffee.com ?</span><span class="sxs-lookup"><span data-stu-id="3d982-200">Want to add a domain that's currently used with a website address, like www.fourthcoffee.com?</span></span> <span data-ttu-id="3d982-201">Vous pouvez suivre les étapes ci-dessous pendant que vous ajoutez le domaine pour conserver son site Web hébergé sur lequel le site est hébergé maintenant afin que les utilisateurs puissent toujours accéder au site Web une fois que vous avez modifié les enregistrements de serveur de noms de domaine de manière à pointer vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3d982-201">You can take below steps while you add the domain to keep its website hosted where the site is hosted now so people can still get to the website after you change the domain's NS records to point to Microsoft 365.</span></span>

1. <span data-ttu-id="3d982-202">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="3d982-202">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

2. <span data-ttu-id="3d982-203">Dans la page **domaines** , sélectionnez le domaine, puis sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="3d982-203">On the **Domains** page, select the domain and then choose **DNS Records**.</span></span>

3. <span data-ttu-id="3d982-204">Sous **gérer le DNS**, sélectionnez **enregistrements personnalisés**, puis **nouvel enregistrement personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="3d982-204">Under **Manage DNS**, select **Custom Records**, and then choose **New custom record**.</span></span>

4. <span data-ttu-id="3d982-205">Sélectionnez le type d’enregistrement DNS que vous souhaitez ajouter, puis tapez les informations pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3d982-205">Select the type of DNS record you want to add, and type the information for the new record.</span></span>

5. <span data-ttu-id="3d982-206">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3d982-206">Select **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3d982-207">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="3d982-207">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="3d982-208">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3d982-208">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
