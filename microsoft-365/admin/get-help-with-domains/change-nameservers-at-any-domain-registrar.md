---
title: Modifier les serveurs de noms de manière à configurer Office 365 avec n'importe quel bureau d'enregistrement de domaines
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
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
- GEU150
- GEA150
ms.assetid: a8b487a9-2a45-4581-9dc4-5d28a47010a2
description: Découvrez comment ajouter et configurer votre domaine dans Office 365 de sorte que vos services de messagerie électronique et Skype entreprise Online utilisent votre propre nom de domaine.
ms.custom: okr_smb
ms.openlocfilehash: 838025002443ec35787ea91775c60d3829545af4
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43210491"
---
# <a name="change-nameservers-to-set-up-office-365-with-any-domain-registrar"></a><span data-ttu-id="ee9bf-103">Modifier les serveurs de noms de manière à configurer Office 365 avec n'importe quel bureau d'enregistrement de domaines</span><span class="sxs-lookup"><span data-stu-id="ee9bf-103">Change nameservers to set up Office 365 with any domain registrar</span></span>

 <span data-ttu-id="ee9bf-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="ee9bf-105">Consultez [la rubrique Configurer votre domaine (instructions spécifiques à l’hôte)](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) pour savoir si nous avons des instructions pour votre serveur d’inscriptions.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-105">Check [Set up your domain (host-specific instructions)](../get-help-with-domains/set-up-your-domain-host-specific-instructions.md) first to see if we have instructions for your registrar.</span></span> 
  
<span data-ttu-id="ee9bf-106">Suivez ces instructions pour ajouter et configurer votre domaine dans Office 365 afin que vos services tels que le courrier électronique et Skype Entreprise Online utilisent le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-106">Follow these instructions to add and set up your domain in Office 365 so your services like email and Skype for Business Online will use your own domain name.</span></span> <span data-ttu-id="ee9bf-107">Pour ce faire, vous devez vérifier votre domaine et modifier les serveurs de noms de votre domaine afin qu'ils utilisent Office 365 et que les enregistrements DNS corrects puissent être configurés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-107">To do this, you'll verify your domain, and then change your domain's nameservers to Office 365 so the correct DNS records can be set up for you.</span></span> <span data-ttu-id="ee9bf-108">Procédez comme suit si les instructions suivantes décrivent votre situation :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-108">Follow these steps if the following statements describe your situation:</span></span>
  
- <span data-ttu-id="ee9bf-109">Vous disposez de votre propre domaine et souhaitez le configurer pour qu'il fonctionne avec Office 365.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-109">You have your own domain and want to set it up to work with Office 365.</span></span>
    
- <span data-ttu-id="ee9bf-p102">Vous voulez qu'Office 365 gère vos enregistrements DNS pour vous (vous pouvez naturellement [gérer vos propres enregistrements DNS](../setup/add-domain.md)).</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p102">You want Office 365 to manage your DNS records for you. (If you prefer, you can [manage your own DNS records](../setup/add-domain.md).)</span></span>
    
## <a name="add-a-txt-or-mx-record-for-verification"></a><span data-ttu-id="ee9bf-112">Ajouter un enregistrement TXT ou MX à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="ee9bf-112">Add a TXT or MX record for verification</span></span>
<span data-ttu-id="ee9bf-113"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="ee9bf-113"><a name="BKMK_verify"> </a></span></span>

> [!NOTE]
> <span data-ttu-id="ee9bf-p103">Vous ne devez créer qu'un seul des deux enregistrements. TXT est le type d'enregistrement préféré, mais certains fournisseurs d'hébergement DNS ne le prennent pas en charge, auquel cas vous pouvez créer un enregistrement MX à la place.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p103">You will create only one or the other of these records. TXT is the preferred record type, but some DNS hosting providers don't support it, in which case you can create an MX record instead.</span></span> 
  
<span data-ttu-id="ee9bf-p104">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p104">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee9bf-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
### <a name="find-the-area-on-your-dns-hosting-providers-website-where-you-can-create-a-new-record"></a><span data-ttu-id="ee9bf-120">Recherchez la zone sur le site Web de votre fournisseur d’hébergement DNS où vous pouvez créer un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-120">Find the area on your DNS hosting provider's website where you can create a new record</span></span>

1. <span data-ttu-id="ee9bf-121">Connectez-vous sur le site web de votre fournisseur d'hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-121">Sign in to your DNS hosting provider's website.</span></span>
    
2. <span data-ttu-id="ee9bf-122">Choisissez votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-122">Choose your domain.</span></span>
    
3. <span data-ttu-id="ee9bf-123">Recherchez la page dans laquelle vous pouvez modifier les enregistrements DNS pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-123">Find the page where you can edit DNS records for your domain.</span></span>
    
### <a name="create-the-record"></a><span data-ttu-id="ee9bf-124">Créer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ee9bf-124">Create the record</span></span>

<span data-ttu-id="ee9bf-125">Selon que vous créez un enregistrement TXT ou un enregistrement MX, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-125">Depending on whether you are creating a TXT record or an MX record, do one of the following:</span></span>
  
<span data-ttu-id="ee9bf-126">**Si vous créez un enregistrement TXT, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-126">**If you create a TXT record, use these values:**</span></span>
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee9bf-127">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-127">**Record Type**</span></span> <br/> |<span data-ttu-id="ee9bf-128">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-128">**Alias** or **Host Name**</span></span> <br/> |<span data-ttu-id="ee9bf-129">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-129">**Value**</span></span> <br/> |<span data-ttu-id="ee9bf-130">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-130">**TTL**</span></span> <br/> |
|<span data-ttu-id="ee9bf-131">TXT</span><span class="sxs-lookup"><span data-stu-id="ee9bf-131">TXT</span></span>  <br/> |<span data-ttu-id="ee9bf-132">Effectuez l'une des opérations suivantes : Tapez **@**, laissez le champ vide ou entrez le nom de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-132">Do one of the following: Type **@** or leave the field empty or type your domain name.</span></span>  <br/> <span data-ttu-id="ee9bf-133">> [!NOTE]> Les conditions requises pour ce champ ne sont pas identiques pour tous les hôtes DNS.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-133">> [!NOTE]> Different DNS hosts have different requirements for this field.</span></span>           
|<span data-ttu-id="ee9bf-134">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="ee9bf-134">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="ee9bf-p106">> [!NOTE]> Il s'agit d'un exemple. Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.           [Comment trouver cette valeur ?](../get-help-with-domains/information-for-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p106">> [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)</span></span>          |<span data-ttu-id="ee9bf-138">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-138">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span>  <br/> |
   
<span data-ttu-id="ee9bf-139">**Si vous créez un enregistrement MX, utilisez les valeurs suivantes :**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-139">**If you create an MX record, use these values:**</span></span>
    
||||||
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee9bf-140">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-140">**Record Type**</span></span>|<span data-ttu-id="ee9bf-141">**Alias** ou **nom d’hôte**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-141">**Alias** or **Host Name**</span></span>|<span data-ttu-id="ee9bf-142">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-142">**Value**</span></span>|<span data-ttu-id="ee9bf-143">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-143">**Priority**</span></span>|<span data-ttu-id="ee9bf-144">**TTL**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-144">**TTL**</span></span>|
|<span data-ttu-id="ee9bf-145">MX</span><span class="sxs-lookup"><span data-stu-id="ee9bf-145">MX</span></span>|<span data-ttu-id="ee9bf-146">Entrez soit **@**, soit votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-146">Type either **@** or your domain name.</span></span> |<span data-ttu-id="ee9bf-p107">MS=ms *XXXXXXXX* > [!NOTE]> Il s'agit d'un exemple. Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.           [Comment trouver cette valeur ?](../get-help-with-domains/information-for-dns-records.md)</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p107">MS=ms *XXXXXXXX* > [!NOTE]> This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)</span></span>          |<span data-ttu-id="ee9bf-150">Pour **Priorité**, afin d’éviter les conflits avec l’enregistrement MX utilisé pour le flux de courrier électronique, utilisez une priorité plus basse que la priorité des enregistrements MX existants.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-150">For **Priority**, to avoid conflicts with the MX record used for mail flow, use a lower priority than the priority for any existing MX records.</span></span> <span data-ttu-id="ee9bf-151">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.md#what-is-mx-priority).</span><span class="sxs-lookup"><span data-stu-id="ee9bf-151">For more information about priority, see [What is MX priority?](../setup/domains-faq.md#what-is-mx-priority)</span></span> |<span data-ttu-id="ee9bf-152">Définissez cette valeur sur **1 heure** ou sur l'équivalent en minutes ( **60** ), en secondes ( **3600** ), etc.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-152">Set this value to **1 hour** or to the equivalent in minutes ( **60** ), seconds ( **3600** ), etc.</span></span> |
   
### <a name="save-the-record"></a><span data-ttu-id="ee9bf-153">Enregistrer l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="ee9bf-153">Save the record</span></span>

<span data-ttu-id="ee9bf-154">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-154">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="ee9bf-155">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-155">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  

1. <span data-ttu-id="ee9bf-156">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-156">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="ee9bf-157">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-157">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
  
3. <span data-ttu-id="ee9bf-158">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-158">On the **Setup** page, select **Start setup**.</span></span>
 
    
  
4. <span data-ttu-id="ee9bf-159">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-159">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="ee9bf-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="ee9bf-163">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="ee9bf-163">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="ee9bf-164"><a name="BKMK_nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="ee9bf-164"><a name="BKMK_nameservers"> </a></span></span>

<span data-ttu-id="ee9bf-p110">À la dernière étape de l'Assistant de configuration de domaines dans Office 365, vous devez exécuter une dernière tâche. Pour configurer votre domaine avec les services Office 365 tels que le courrier, vous devez modifier les enregistrements de serveur de noms de votre domaine auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire d'Office 365. Comme Office 365 héberge votre DNS, les enregistrements DNS nécessaires pour vos services sont configurés automatiquement. Vous pouvez mettre à jour les enregistrements de serveur de noms vous-même en suivant les étapes fournies éventuellement par votre bureau d'enregistrement de domaines dans l'aide disponible sur son site web. Si vous n'êtes pas familiarisé avec DNS, contactez le support du bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p110">When you get to the last step of the domains setup wizard in Office 365, you have one task remaining. To set up your domain with Office 365 services, like email, you change your domain's nameserver (or NS) records at your domain registrar to point to the Office 365 primary and secondary nameservers. Then, because Office 365 hosts your DNS, the required DNS records for your services are set up automatically for you. You can update the nameserver records yourself by following the steps your domain registrar may provide in the help content at their website. If you're not familiar with DNS, contact support at the domain registrar.</span></span>

::: moniker range="o365-worldwide"
  
<span data-ttu-id="ee9bf-170">Pour changer vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-170">To change your domain's nameservers at your domain registrar's website yourself, follow these steps:</span></span>
  
1. <span data-ttu-id="ee9bf-171">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-171">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="ee9bf-172">Créez deux enregistrements de serveur de noms, ou modifiez les enregistrements existants pour qu'ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-172">Create two nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="ee9bf-173">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ee9bf-173">First nameserver</span></span>  <br/> |<span data-ttu-id="ee9bf-174">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ee9bf-174">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="ee9bf-175">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ee9bf-175">Second nameserver</span></span>  <br/> |<span data-ttu-id="ee9bf-176">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="ee9bf-176">ns2.bdm.microsoftonline.com</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="ee9bf-177">Vous devez utiliser au moins deux enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-177">You should use at least two nameserver records.</span></span> <span data-ttu-id="ee9bf-178">Si d’autres serveurs de noms sont répertoriés, vous pouvez les supprimer ou les remplacer par **NS3.BDM.microsoftonline.com** et **NS4.BDM.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-178">If there are any other nameservers listed, you can either delete them, or change them to **ns3.bdm.microsoftonline.com** and **ns4.bdm.microsoftonline.com**.</span></span> 
  
3. <span data-ttu-id="ee9bf-179">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-179">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="ee9bf-p112">Quand vous modifiez les enregistrements de serveur de noms de votre domaine afin qu'ils pointent vers les serveurs de noms d'Office 365, tous les services actuellement associés à votre domaine sont affectés. Si vous passez une étape de l'Assistant (par exemple, ajout des adresses de courrier) ou si vous utilisez votre domaine pour les blogs, les paniers ou d'autres services, des étapes supplémentaires sont nécessaires, sans quoi cette modification pourrait entraîner une interruption de service telle que la perte de l'accès au courrier ou le blocage de l'accès à votre site web.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p112">When you change your domain's NS records to point to the Office 365 nameservers, all the services that are currently associated with your domain are affected. If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required. Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"
  
1. <span data-ttu-id="ee9bf-183">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-183">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="ee9bf-184">Créez deux enregistrements de serveur de noms, ou modifiez les enregistrements existants pour qu'ils correspondent aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-184">Create two nameserver records, or edit the existing nameserver records to match the following values:</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="ee9bf-185">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ee9bf-185">First nameserver</span></span>  <br/> |<span data-ttu-id="ee9bf-186">ns1.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="ee9bf-186">ns1.dns.partner.microsoftonline.cn</span></span>  <br/> |
|<span data-ttu-id="ee9bf-187">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="ee9bf-187">Second nameserver</span></span>  <br/> |<span data-ttu-id="ee9bf-188">ns2.dns.partner.microsoftonline.cn</span><span class="sxs-lookup"><span data-stu-id="ee9bf-188">ns2.dns.partner.microsoftonline.cn</span></span>  <br/> |
   
   > [!TIP]
   > <span data-ttu-id="ee9bf-189">Vous devez utiliser au moins deux enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-189">You should use at least two nameserver records.</span></span> <span data-ttu-id="ee9bf-190">Si d’autres serveurs de noms sont répertoriés, vous pouvez les supprimer ou les remplacer par **NS3.DNS.Partner.microsoftonline.CN** et **NS4.DNS.Partner.microsoftonline.CN**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-190">If there are any other nameservers listed, you can either delete them, or change them to **ns3.dns.partner.microsoftonline.cn** and **ns4.dns.partner.microsoftonline.cn**.</span></span> 
  
3. <span data-ttu-id="ee9bf-191">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-191">Save your changes.</span></span>
    
> [!CAUTION]
> <span data-ttu-id="ee9bf-192">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers l’Office 365 géré par les serveurs de noms 21Vianet, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-192">When you change your domain's NS records to point to the Office 365 operated by 21Vianet nameservers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="ee9bf-193">Si vous avez ignoré les étapes de l’Assistant, telles que l’ajout d’adresses de messagerie, ou si vous utilisez votre domaine pour les blogs, les paniers d’achat ou d’autres services, des étapes supplémentaires sont requises.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-193">If you skipped any steps of the wizard, such as adding email addresses, or if you're using your domain for blogs, shopping carts, or other services, there are additional steps that are required.</span></span> <span data-ttu-id="ee9bf-194">Dans le cas contraire, cette modification pourrait entraîner un temps d’arrêt du service, tel qu’un manque d’accès à la messagerie ou votre site Web actuel inaccessible.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-194">Otherwise this change could result in service downtime, such as lack of email access or your current website being inaccessible.</span></span> 

::: moniker-end
  
<span data-ttu-id="ee9bf-195">Voici, par exemple, quelques étapes supplémentaires qui peuvent être nécessaires pour le courrier et l'hébergement du site web :</span><span class="sxs-lookup"><span data-stu-id="ee9bf-195">For example, here are some additional steps that might be required for email and website hosting:</span></span>
  
- <span data-ttu-id="ee9bf-196">Déplacez toutes les adresses de courrier qui utilisent votre domaine vers Office 365 avant de modifier vos enregistrements NS.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-196">Move all email addresses that use your domain to Office 365 before you change your NS records.</span></span>
    
- <span data-ttu-id="ee9bf-197">Vous souhaitez ajouter un domaine actuellement utilisé avec une adresse de site Web, par exemple www.fourthcoffee.com ?</span><span class="sxs-lookup"><span data-stu-id="ee9bf-197">Want to add a domain that's currently used with a website address, like www.fourthcoffee.com?</span></span> <span data-ttu-id="ee9bf-198">Vous pouvez suivre les étapes ci-dessous pendant que vous ajoutez le domaine pour conserver son site Web hébergé sur lequel le site est hébergé maintenant afin que les utilisateurs puissent toujours accéder au site Web une fois que vous avez modifié les enregistrements de serveur de noms de domaine pour qu’ils pointent vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-198">You can take below steps while you add the domain to keep its website hosted where the site is hosted now so people can still get to the website after you change the domain's NS records to point to Office 365.</span></span>

1. <span data-ttu-id="ee9bf-199">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-199">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

3. <span data-ttu-id="ee9bf-200">Dans la page Domaines, sélectionnez un domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-200">On the Domains page, select a domain.</span></span>

4. <span data-ttu-id="ee9bf-201">Sous **paramètres DNS**, sélectionnez **enregistrements personnalisés**, puis **nouvel enregistrement personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-201">Under **DNS settings**, select **Custom Records**, and then choose **New custom record**.</span></span>

5. <span data-ttu-id="ee9bf-202">Sélectionnez le type d’enregistrement DNS que vous souhaitez ajouter, puis tapez les informations pour le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-202">Select the type of DNS record you want to add, and type the information for the new record.</span></span>

6. <span data-ttu-id="ee9bf-203">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-203">Select **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="ee9bf-p116">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-p116">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  

