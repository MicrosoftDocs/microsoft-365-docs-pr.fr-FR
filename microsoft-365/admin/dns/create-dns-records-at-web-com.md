---
title: Créer des enregistrements DNS web.com microsoft
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
- Adm_NonTOC
- Adm_O365_Setup
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 84acd4fc-6eec-4d00-8bed-568f036ae2af
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur web.com pour Microsoft.
ms.openlocfilehash: b667b2e69822fcd69babda7790a6468b640b073b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50909981"
---
# <a name="create-dns-records-at-webcom-for-microsoft"></a><span data-ttu-id="03aa9-103">Créer des enregistrements DNS web.com microsoft</span><span class="sxs-lookup"><span data-stu-id="03aa9-103">Create DNS records at web.com for Microsoft</span></span>

 <span data-ttu-id="03aa9-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="03aa9-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="03aa9-105">Si web.com est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="03aa9-105">If web.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="03aa9-106">Une fois ces enregistrements ajoutés web.com, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03aa9-106">After you add these records at web.com, your domain will be set up to work with Microsoft services.</span></span>

  
> [!NOTE]
>  <span data-ttu-id="03aa9-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="03aa9-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="03aa9-110">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="03aa9-110">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="03aa9-111"><a name="BKMK_Nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-111"><a name="BKMK_Nameservers"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="03aa9-112">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="03aa9-112">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="03aa9-113">Lorsque vous vous êtes inscrit à web.com, vous avez ajouté un domaine à l’aide du processus **web.com’installation.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-113">When you signed up for web.com, you added a domain by using the web.com **Setup** process.</span></span> 
  
<span data-ttu-id="03aa9-114">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Microsoft, vous devez d’abord modifier les serveurs de noms de votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms web.com.</span><span class="sxs-lookup"><span data-stu-id="03aa9-114">To verify and create DNS records for your domain in Microsoft, you first need to change the nameservers at your domain registrar so that they use web.com's nameservers.</span></span>
  
<span data-ttu-id="03aa9-115">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="03aa9-115">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="03aa9-116">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="03aa9-116">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="03aa9-117">Créez deux enregistrements de nameserver à l’aide des valeurs du tableau suivant, ou modifiez les enregistrements de nameserver existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="03aa9-117">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="03aa9-118">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="03aa9-118">First nameserver</span></span>  <br/> |<span data-ttu-id="03aa9-119">Utilisez la valeur de nameserver fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="03aa9-119">Use the nameserver value provided by web.com.</span></span>  <br/> |
    |<span data-ttu-id="03aa9-120">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="03aa9-120">Second nameserver</span></span>  <br/> |<span data-ttu-id="03aa9-121">Utilisez la valeur de nameserver fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="03aa9-121">Use the nameserver value provided by web.com.</span></span>  <br/> |
   
    > [!TIP]
    > <span data-ttu-id="03aa9-122">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="03aa9-122">You should use at least two name server records.</span></span> <span data-ttu-id="03aa9-123">Si d’autres serveurs de noms sont répertoriés, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="03aa9-123">If there are any other name servers listed, you should delete them.</span></span> 
  
3. <span data-ttu-id="03aa9-124">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="03aa9-124">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="03aa9-125">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="03aa9-125">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="03aa9-126">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="03aa9-126">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="03aa9-127">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="03aa9-127">Add a TXT record for verification</span></span>
<span data-ttu-id="03aa9-128"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-128"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="03aa9-p104">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="03aa9-p104">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="03aa9-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="03aa9-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="03aa9-133">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="03aa9-133">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="03aa9-134">Connectez-vous en premier.</span><span class="sxs-lookup"><span data-stu-id="03aa9-134">Log in first.</span></span>
  
2. <span data-ttu-id="03aa9-135">Dans la page **Gestionnaire de comptes,** sélectionnez **Mes noms de domaine.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-135">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="03aa9-136">Sous \*\*Gérer \*mon domaine\*\*\*, sélectionnez **Modifier les enregistrements DNS avancés.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-136">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="03aa9-137">Dans la page **Noms de** domaine, sous **Texte (Enregistrements TXT),** cliquez sur Modifier les enregistrements **TXT,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03aa9-137">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="03aa9-138">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-138">**Host**</span></span>|<span data-ttu-id="03aa9-139">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-139">**TTL**</span></span>|<span data-ttu-id="03aa9-140">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-140">**Text**</span></span>|
    |:-----|:-----|:----|
    |@  <br/> |<span data-ttu-id="03aa9-141">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-141">3600</span></span>  <br/> |<span data-ttu-id="03aa9-142">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="03aa9-142">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="03aa9-143">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="03aa9-143">**Note:** This is an example.</span></span> <span data-ttu-id="03aa9-144">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="03aa9-144">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="03aa9-145">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="03aa9-145">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
  
    
5. <span data-ttu-id="03aa9-146">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-146">Select **Continue**.</span></span>
  
  
6. <span data-ttu-id="03aa9-147">Patientez quelques minutes avant de vérifier votre nouvel enregistrement TXT, afin que l’enregistrement que vous venons de créer puisse être mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="03aa9-147">Wait a few minutes before you verify your new TXT record, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="03aa9-148">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="03aa9-148">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="03aa9-149">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="03aa9-149">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="03aa9-150">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="03aa9-150">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="03aa9-151">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="03aa9-151">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="03aa9-152">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-152">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="03aa9-153">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-153">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="03aa9-p108">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="03aa9-p108">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="03aa9-157">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="03aa9-157">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="03aa9-158"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-158"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="03aa9-159">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="03aa9-159">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="03aa9-160">Connectez-vous en premier.</span><span class="sxs-lookup"><span data-stu-id="03aa9-160">Log in first.</span></span>
  
2. <span data-ttu-id="03aa9-161">Dans la page **Gestionnaire de comptes,** sélectionnez **Mes noms de domaine.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-161">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="03aa9-162">Sous \*\*Gérer \*mon domaine\*\*\*, sélectionnez **Modifier les enregistrements DNS avancés.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-162">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="03aa9-163">Sous **Serveurs de messagerie (enregistrements MX),** cliquez sur Modifier les enregistrements **MX,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03aa9-163">Under **Mail Servers (MX Records)**, click **Edit MX Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="03aa9-164">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="03aa9-164">**Priority**</span></span>|<span data-ttu-id="03aa9-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="03aa9-165">**TTL**</span></span>|<span data-ttu-id="03aa9-166">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-166">**Mail server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="03aa9-167">1</span><span class="sxs-lookup"><span data-stu-id="03aa9-167">1</span></span>  <br/> <span data-ttu-id="03aa9-168">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](../setup/domains-faq.yml).</span><span class="sxs-lookup"><span data-stu-id="03aa9-168">For more information about priority, see [What is MX priority?](../setup/domains-faq.yml)</span></span> <br/> |<span data-ttu-id="03aa9-169">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-169">3600</span></span>  <br/> |<span data-ttu-id="03aa9-170">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-170">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="03aa9-171">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03aa9-171">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="03aa9-172">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="03aa9-172">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |
   

5. <span data-ttu-id="03aa9-173">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-173">Select **Save**.</span></span>
  
6. <span data-ttu-id="03aa9-174">Si d’autres enregistrements MX sont répertoriés dans la section **Enregistrements MX,** cochez la case en regard de l’enregistrement sous **Supprimer,** puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-174">If there are any other MX records listed in the **MX Records** section, select the check box next to the record under **Delete**, and select **Save**.</span></span> 
  
7. <span data-ttu-id="03aa9-175">Dans l’écran de confirmation, sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-175">On the confirmation screen, select **Save changes**.</span></span> 

  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="03aa9-176">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="03aa9-176">Add the Six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="03aa9-177"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-177"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="03aa9-178">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="03aa9-178">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="03aa9-179">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="03aa9-179">You'll be prompted to log in first.</span></span>
     
2. <span data-ttu-id="03aa9-180">Dans la page **Gestionnaire de comptes,** sélectionnez **Mes noms de domaine.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-180">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="03aa9-181">Sous \*\*Gérer \*mon domaine\*\*\*, sélectionnez **Modifier les enregistrements DNS avancés.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-181">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="03aa9-182">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="03aa9-182">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="03aa9-183">Sous **Alias d’hôte (enregistrements CNAME),** cliquez sur Modifier les enregistrements **CNAME,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03aa9-183">Under **Host Aliases (CNAME Records)**, click **Edit CNAME Records**, and then select the values from the following table.</span></span>
    
    
    |<span data-ttu-id="03aa9-184">**Alias (Alias)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-184">**Alias**</span></span>|<span data-ttu-id="03aa9-185">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-185">**TTL**</span></span>|<span data-ttu-id="03aa9-186">**Refers to Host Name (Fait référence au nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-186">**Refers to Host Name**</span></span>|<span data-ttu-id="03aa9-187">**Autre hôte**</span><span class="sxs-lookup"><span data-stu-id="03aa9-187">**Other Host**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="03aa9-188">autodiscover</span><span class="sxs-lookup"><span data-stu-id="03aa9-188">autodiscover</span></span>  <br/> |<span data-ttu-id="03aa9-189">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-189">3600</span></span>  <br/> |<span data-ttu-id="03aa9-190">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-190">@ (none)</span></span>  <br/> |<span data-ttu-id="03aa9-191">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-191">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="03aa9-192">sip</span><span class="sxs-lookup"><span data-stu-id="03aa9-192">sip</span></span>  <br/> |<span data-ttu-id="03aa9-193">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-193">3600</span></span>  <br/> |<span data-ttu-id="03aa9-194">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-194">@ (none)</span></span>  <br/> |<span data-ttu-id="03aa9-195">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-195">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="03aa9-196">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="03aa9-196">lyncdiscover</span></span>  <br/> |<span data-ttu-id="03aa9-197">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-197">3600</span></span>  <br/> |<span data-ttu-id="03aa9-198">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-198">@ (none)</span></span>  <br/> | <span data-ttu-id="03aa9-199">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-199">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="03aa9-200">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="03aa9-200">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="03aa9-201">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-201">3600</span></span>  <br/> |<span data-ttu-id="03aa9-202">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-202">@ (none)</span></span>  <br/> |<span data-ttu-id="03aa9-203">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="03aa9-203">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="03aa9-204">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="03aa9-204">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="03aa9-205">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-205">3600</span></span>  <br/> |<span data-ttu-id="03aa9-206">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-206">@ (none)</span></span>  <br/> |<span data-ttu-id="03aa9-207">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-207">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
    |<span data-ttu-id="03aa9-208">msoid</span><span class="sxs-lookup"><span data-stu-id="03aa9-208">msoid</span></span>  <br/> |<span data-ttu-id="03aa9-209">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-209">3600</span></span>  <br/> |<span data-ttu-id="03aa9-210">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="03aa9-210">@ (none)</span></span>  <br/> |<span data-ttu-id="03aa9-211">clientconfig.microsoftonline-p.net</span><span class="sxs-lookup"><span data-stu-id="03aa9-211">clientconfig.microsoftonline-p.net</span></span>  <br/> |
    
  
5. <span data-ttu-id="03aa9-212">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-212">Select **Continue**.</span></span>
  
6. <span data-ttu-id="03aa9-213">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="03aa9-213">Add each of the other five CNAME records.</span></span>

    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="03aa9-214">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="03aa9-214">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="03aa9-215"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-215"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="03aa9-216">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="03aa9-216">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="03aa9-217">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="03aa9-217">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="03aa9-218">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03aa9-218">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="03aa9-219">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="03aa9-219">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="03aa9-220">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="03aa9-220">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="03aa9-221">Connectez-vous en premier.</span><span class="sxs-lookup"><span data-stu-id="03aa9-221">Log in first.</span></span>
    
  
2. <span data-ttu-id="03aa9-222">Dans la page **Gestionnaire de comptes,** sélectionnez **Mes noms de domaine.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-222">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="03aa9-223">Sous \*\*Gérer \*mon domaine\*\*\*, sélectionnez **Modifier les enregistrements DNS avancés.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-223">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="03aa9-224">Dans la page **Noms de** domaine, sous **Texte (Enregistrements TXT),** cliquez sur Modifier les enregistrements **TXT,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03aa9-224">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span>   
    
    |<span data-ttu-id="03aa9-225">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-225">**Host**</span></span>|<span data-ttu-id="03aa9-226">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-226">**TTL**</span></span>|<span data-ttu-id="03aa9-227">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-227">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="03aa9-228">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-228">3600</span></span>  <br/> |<span data-ttu-id="03aa9-229">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="03aa9-229">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="03aa9-230">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="03aa9-230">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>   |

 
5. <span data-ttu-id="03aa9-231">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-231">Select **Continue**.</span></span>

6. <span data-ttu-id="03aa9-232">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-232">Select **Save changes**.</span></span>
    

  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="03aa9-233">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="03aa9-233">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="03aa9-234"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="03aa9-234"><a name="BKMK_add_SRV"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="03aa9-235">N’oubliez pas que web.com est chargé de rendre cette fonctionnalité disponible.</span><span class="sxs-lookup"><span data-stu-id="03aa9-235">Please keep in mind that web.com is responsible for making this functionality available.</span></span> <span data-ttu-id="03aa9-236">Si vous constatez des différences entre les étapes ci-dessous et l’interface utilisateur graphique web.com (interface utilisateur graphique), tirez parti de [la communauté web.com.](https://community.web.com.com/)</span><span class="sxs-lookup"><span data-stu-id="03aa9-236">In case you see discrepancies between the steps below and the current web.com GUI(Graphical User Interface), please leverage the [web.com Community](https://community.web.com.com/).</span></span> 

1. <span data-ttu-id="03aa9-237">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="03aa9-237">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="03aa9-238">Connectez-vous en premier.</span><span class="sxs-lookup"><span data-stu-id="03aa9-238">Log in first.</span></span>
      
2. <span data-ttu-id="03aa9-239">Dans la page **Gestionnaire de comptes,** sélectionnez **Mes noms de domaine.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-239">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="03aa9-240">Sous \*\*Gérer \*mon domaine\*\*\*, sélectionnez **Modifier les enregistrements DNS avancés.**</span><span class="sxs-lookup"><span data-stu-id="03aa9-240">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>
  
4. <span data-ttu-id="03aa9-241">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="03aa9-241">Add the first of the two SRV records.</span></span>

    <span data-ttu-id="03aa9-242">Sous **Service (Enregistrements SRV),** cliquez sur Modifier les enregistrements **SRV,** puis sélectionnez les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03aa9-242">Under **Service (SRV Records)**, click **Edit SRV Records**, and then select the values from the following table.</span></span> 
        
    |<span data-ttu-id="03aa9-243">**Service**</span><span class="sxs-lookup"><span data-stu-id="03aa9-243">**Service**</span></span>|<span data-ttu-id="03aa9-244">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-244">**Protocol**</span></span>|<span data-ttu-id="03aa9-245">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-245">**TTL**</span></span>|<span data-ttu-id="03aa9-246">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-246">**Priority**</span></span>|<span data-ttu-id="03aa9-247">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-247">**Weight**</span></span>|<span data-ttu-id="03aa9-248">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-248">**Port**</span></span>|<span data-ttu-id="03aa9-249">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="03aa9-249">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="03aa9-250">_sip</span><span class="sxs-lookup"><span data-stu-id="03aa9-250">_sip</span></span> |<span data-ttu-id="03aa9-251">_tls</span><span class="sxs-lookup"><span data-stu-id="03aa9-251">_tls</span></span> |<span data-ttu-id="03aa9-252">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-252">3600</span></span> | <span data-ttu-id="03aa9-253">100</span><span class="sxs-lookup"><span data-stu-id="03aa9-253">100</span></span>|<span data-ttu-id="03aa9-254">1</span><span class="sxs-lookup"><span data-stu-id="03aa9-254">1</span></span> |<span data-ttu-id="03aa9-255">443</span><span class="sxs-lookup"><span data-stu-id="03aa9-255">443</span></span> |<span data-ttu-id="03aa9-256">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-256">sipfed.online.lync.com</span></span>  |
    |<span data-ttu-id="03aa9-257">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="03aa9-257">_sipfederationtls</span></span> |<span data-ttu-id="03aa9-258">_tcp</span><span class="sxs-lookup"><span data-stu-id="03aa9-258">_tcp</span></span> |<span data-ttu-id="03aa9-259">3600</span><span class="sxs-lookup"><span data-stu-id="03aa9-259">3600</span></span> |<span data-ttu-id="03aa9-260">100</span><span class="sxs-lookup"><span data-stu-id="03aa9-260">100</span></span> |<span data-ttu-id="03aa9-261">1</span><span class="sxs-lookup"><span data-stu-id="03aa9-261">1</span></span> |<span data-ttu-id="03aa9-262">5061</span><span class="sxs-lookup"><span data-stu-id="03aa9-262">5061</span></span> | <span data-ttu-id="03aa9-263">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="03aa9-263">sipfed.online.lync.com</span></span> |

  
5. <span data-ttu-id="03aa9-264">Ajoutez l’autre enregistrement SRV en choisissant les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="03aa9-264">Add the other SRV record by choosing the values from the second row of the table.</span></span> 
  
6. <span data-ttu-id="03aa9-265">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-265">Select **Continue**.</span></span>

7. <span data-ttu-id="03aa9-266">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="03aa9-266">Select **Save changes**.</span></span>

    
> [!NOTE]
>  <span data-ttu-id="03aa9-p116">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="03aa9-p116">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
