---
title: Créer des enregistrements DNS sur web.com pour Microsoft
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
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 84acd4fc-6eec-4d00-8bed-568f036ae2af
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur web.com pour Microsoft.
ms.openlocfilehash: ec1d0168fb8a9dfb30d47412146777bc88f90a46
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629250"
---
# <a name="create-dns-records-at-webcom-for-microsoft"></a><span data-ttu-id="91e1d-103">Créer des enregistrements DNS sur web.com pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="91e1d-103">Create DNS records at web.com for Microsoft</span></span>

 <span data-ttu-id="91e1d-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="91e1d-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="91e1d-105">Si web.com est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="91e1d-105">If web.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="91e1d-106">Une fois ces enregistrements ajoutés sur web.com, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91e1d-106">After you add these records at web.com, your domain will be set up to work with Microsoft services.</span></span>
  
<span data-ttu-id="91e1d-107">Pour en savoir plus sur l’hébergement Web et le DNS pour les sites Web avec Microsoft, consultez [la rubrique utiliser un site Web public avec Microsoft](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="91e1d-107">To learn about webhosting and DNS for websites with Microsoft, see [Use a public website with Microsoft](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="91e1d-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="91e1d-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="91e1d-111">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="91e1d-111">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="91e1d-112"><a name="BKMK_Nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-112"><a name="BKMK_Nameservers"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="91e1d-113">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="91e1d-113">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="91e1d-114">Lorsque vous vous êtes inscrit à web.com, vous avez ajouté un domaine à l’aide du processus de **configuration** de Web.com.</span><span class="sxs-lookup"><span data-stu-id="91e1d-114">When you signed up for web.com, you added a domain by using the web.com **Setup** process.</span></span> 
  
<span data-ttu-id="91e1d-115">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Microsoft, vous devez d’abord modifier les serveurs de noms au niveau de votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms de Web. com.</span><span class="sxs-lookup"><span data-stu-id="91e1d-115">To verify and create DNS records for your domain in Microsoft, you first need to change the nameservers at your domain registrar so that they use web.com's nameservers.</span></span>
  
<span data-ttu-id="91e1d-116">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="91e1d-116">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="91e1d-117">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="91e1d-117">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="91e1d-118">Créez deux enregistrements de serveur de noms à l’aide des valeurs indiquées dans le tableau suivant, ou modifiez les enregistrements de serveur de noms existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="91e1d-118">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="91e1d-119">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="91e1d-119">First nameserver</span></span>  <br/> |<span data-ttu-id="91e1d-120">Utilisez la valeur de serveur de noms fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="91e1d-120">Use the nameserver value provided by web.com.</span></span>  <br/> |
    |<span data-ttu-id="91e1d-121">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="91e1d-121">Second nameserver</span></span>  <br/> |<span data-ttu-id="91e1d-122">Utilisez la valeur de serveur de noms fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="91e1d-122">Use the nameserver value provided by web.com.</span></span>  <br/> |
   
    > [!TIP]
    > <span data-ttu-id="91e1d-123">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="91e1d-123">You should use at least two name server records.</span></span> <span data-ttu-id="91e1d-124">Si d’autres serveurs de noms sont répertoriés, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="91e1d-124">If there are any other name servers listed, you should delete them.</span></span> 
  
3. <span data-ttu-id="91e1d-125">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="91e1d-125">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="91e1d-126">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="91e1d-126">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="91e1d-127">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="91e1d-127">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="91e1d-128">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="91e1d-128">Add a TXT record for verification</span></span>
<span data-ttu-id="91e1d-129"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-129"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="91e1d-130">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="91e1d-130">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="91e1d-131">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="91e1d-131">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="91e1d-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="91e1d-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="91e1d-134">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="91e1d-134">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="91e1d-135">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="91e1d-135">Log in first.</span></span>
  
2. <span data-ttu-id="91e1d-136">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-136">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="91e1d-137">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-137">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="91e1d-138">Dans la page **noms de domaine** , sous **texte (enregistrements TXT)**, cliquez sur **modifier les enregistrements TXT**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91e1d-138">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="91e1d-139">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-139">**Host**</span></span>|<span data-ttu-id="91e1d-140">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-140">**TTL**</span></span>|<span data-ttu-id="91e1d-141">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-141">**Text**</span></span>|
    |:-----|:-----|:----|
    |@  <br/> |<span data-ttu-id="91e1d-142">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-142">3600</span></span>  <br/> |<span data-ttu-id="91e1d-143">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="91e1d-143">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="91e1d-144">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="91e1d-144">**Note:** This is an example.</span></span> <span data-ttu-id="91e1d-145">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="91e1d-145">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="91e1d-146">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="91e1d-146">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
  
    
5. <span data-ttu-id="91e1d-147">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-147">Select **Continue**.</span></span>
  
  
6. <span data-ttu-id="91e1d-148">Patientez quelques minutes avant de vérifier votre nouvel enregistrement TXT, afin que l’enregistrement que vous venez de créer puisse être mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="91e1d-148">Wait a few minutes before you verify your new TXT record, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="91e1d-149">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez revenir à Microsoft et demander l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="91e1d-149">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="91e1d-150">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="91e1d-150">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="91e1d-151">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="91e1d-151">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="91e1d-152">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="91e1d-152">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="91e1d-153">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-153">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="91e1d-154">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-154">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="91e1d-p108">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="91e1d-p108">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="91e1d-158">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="91e1d-158">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="91e1d-159"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-159"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="91e1d-160">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="91e1d-160">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="91e1d-161">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="91e1d-161">Log in first.</span></span>
  
2. <span data-ttu-id="91e1d-162">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-162">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="91e1d-163">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-163">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="91e1d-164">Sous **serveurs de messagerie (enregistrements MX)**, cliquez sur **modifier les enregistrements MX**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91e1d-164">Under **Mail Servers (MX Records)**, click **Edit MX Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="91e1d-165">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="91e1d-165">**Priority**</span></span>|<span data-ttu-id="91e1d-166">**TTL**</span><span class="sxs-lookup"><span data-stu-id="91e1d-166">**TTL**</span></span>|<span data-ttu-id="91e1d-167">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-167">**Mail server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="91e1d-168">0,1</span><span class="sxs-lookup"><span data-stu-id="91e1d-168">1</span></span>  <br/> <span data-ttu-id="91e1d-169">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="91e1d-169">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="91e1d-170">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-170">3600</span></span>  <br/> |<span data-ttu-id="91e1d-171">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-171">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="91e1d-172">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91e1d-172">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="91e1d-173">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="91e1d-173">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |
   

5. <span data-ttu-id="91e1d-174">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-174">Select **Save**.</span></span>
  
6. <span data-ttu-id="91e1d-175">Si d’autres enregistrements MX sont répertoriés dans la section **MX Records (enregistrements MX** ), activez la case à cocher en regard de l’enregistrement sous **Delete (supprimer**), puis sélectionnez Save ( **Enregistrer**).</span><span class="sxs-lookup"><span data-stu-id="91e1d-175">If there are any other MX records listed in the **MX Records** section, select the check box next to the record under **Delete**, and select **Save**.</span></span> 
  
7. <span data-ttu-id="91e1d-176">Dans l’écran de confirmation, sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-176">On the confirmation screen, select **Save changes**.</span></span> 

  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="91e1d-177">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="91e1d-177">Add the Six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="91e1d-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-178"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="91e1d-179">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="91e1d-179">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="91e1d-180">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="91e1d-180">You'll be prompted to log in first.</span></span>
     
2. <span data-ttu-id="91e1d-181">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-181">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="91e1d-182">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-182">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="91e1d-183">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="91e1d-183">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="91e1d-184">Sous **alias d’hôte (enregistrements CNAME)**, cliquez sur **modifier les enregistrements CNAME**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91e1d-184">Under **Host Aliases (CNAME Records)**, click **Edit CNAME Records**, and then select the values from the following table.</span></span>
    
    
    |<span data-ttu-id="91e1d-185">**Alias (Alias)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-185">**Alias**</span></span>|<span data-ttu-id="91e1d-186">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-186">**TTL**</span></span>|<span data-ttu-id="91e1d-187">**Refers to Host Name (Fait référence au nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-187">**Refers to Host Name**</span></span>|<span data-ttu-id="91e1d-188">**Autre hôte**</span><span class="sxs-lookup"><span data-stu-id="91e1d-188">**Other Host**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="91e1d-189">autodiscover</span><span class="sxs-lookup"><span data-stu-id="91e1d-189">autodiscover</span></span>  <br/> |<span data-ttu-id="91e1d-190">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-190">3600</span></span>  <br/> |<span data-ttu-id="91e1d-191">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-191">@ (none)</span></span>  <br/> |<span data-ttu-id="91e1d-192">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-192">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="91e1d-193">sip</span><span class="sxs-lookup"><span data-stu-id="91e1d-193">sip</span></span>  <br/> |<span data-ttu-id="91e1d-194">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-194">3600</span></span>  <br/> |<span data-ttu-id="91e1d-195">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-195">@ (none)</span></span>  <br/> |<span data-ttu-id="91e1d-196">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-196">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="91e1d-197">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="91e1d-197">lyncdiscover</span></span>  <br/> |<span data-ttu-id="91e1d-198">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-198">3600</span></span>  <br/> |<span data-ttu-id="91e1d-199">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-199">@ (none)</span></span>  <br/> | <span data-ttu-id="91e1d-200">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-200">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="91e1d-201">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="91e1d-201">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="91e1d-202">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-202">3600</span></span>  <br/> |<span data-ttu-id="91e1d-203">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-203">@ (none)</span></span>  <br/> |<span data-ttu-id="91e1d-204">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="91e1d-204">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="91e1d-205">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="91e1d-205">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="91e1d-206">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-206">3600</span></span>  <br/> |<span data-ttu-id="91e1d-207">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-207">@ (none)</span></span>  <br/> |<span data-ttu-id="91e1d-208">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-208">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
    |<span data-ttu-id="91e1d-209">msoid</span><span class="sxs-lookup"><span data-stu-id="91e1d-209">msoid</span></span>  <br/> |<span data-ttu-id="91e1d-210">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-210">3600</span></span>  <br/> |<span data-ttu-id="91e1d-211">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="91e1d-211">@ (none)</span></span>  <br/> |<span data-ttu-id="91e1d-212">clientconfig.microsoftonline-p.net</span><span class="sxs-lookup"><span data-stu-id="91e1d-212">clientconfig.microsoftonline-p.net</span></span>  <br/> |
    
  
5. <span data-ttu-id="91e1d-213">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-213">Select **Continue**.</span></span>
  
6. <span data-ttu-id="91e1d-214">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="91e1d-214">Add each of the other five CNAME records.</span></span>

    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="91e1d-215">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="91e1d-215">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="91e1d-216"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-216"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="91e1d-217">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="91e1d-217">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="91e1d-218">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="91e1d-218">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="91e1d-219">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, n’en créez pas pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91e1d-219">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="91e1d-220">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="91e1d-220">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="91e1d-221">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="91e1d-221">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="91e1d-222">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="91e1d-222">Log in first.</span></span>
    
  
2. <span data-ttu-id="91e1d-223">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-223">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="91e1d-224">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-224">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="91e1d-225">Dans la page **noms de domaine** , sous **texte (enregistrements TXT)**, cliquez sur **modifier les enregistrements TXT**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91e1d-225">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span>   
    
    |<span data-ttu-id="91e1d-226">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-226">**Host**</span></span>|<span data-ttu-id="91e1d-227">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-227">**TTL**</span></span>|<span data-ttu-id="91e1d-228">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-228">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="91e1d-229">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-229">3600</span></span>  <br/> |<span data-ttu-id="91e1d-230">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="91e1d-230">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="91e1d-231">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="91e1d-231">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>   |

 
5. <span data-ttu-id="91e1d-232">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-232">Select **Continue**.</span></span>

6. <span data-ttu-id="91e1d-233">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-233">Select **Save changes**.</span></span>
    

  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="91e1d-234">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="91e1d-234">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="91e1d-235"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="91e1d-235"><a name="BKMK_add_SRV"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="91e1d-236">N’oubliez pas que web.com est responsable de la mise à disposition de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="91e1d-236">Please keep in mind that web.com is responsible for making this functionality available.</span></span> <span data-ttu-id="91e1d-237">Si vous constatez des incohérences entre les étapes ci-dessous et l’interface utilisateur graphique (GUI) web.com actuelle, utilisez la [communauté Web.com](https://community.web.com.com/).</span><span class="sxs-lookup"><span data-stu-id="91e1d-237">In case you see discrepancies between the steps below and the current web.com GUI(Graphical User Interface), please leverage the [web.com Community](https://community.web.com.com/).</span></span> 

1. <span data-ttu-id="91e1d-238">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="91e1d-238">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="91e1d-239">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="91e1d-239">Log in first.</span></span>
      
2. <span data-ttu-id="91e1d-240">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-240">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="91e1d-241">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-241">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>
  
4. <span data-ttu-id="91e1d-242">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="91e1d-242">Add the first of the two SRV records.</span></span>

    <span data-ttu-id="91e1d-243">Sous **service (enregistrements SRV)**, cliquez sur **modifier les enregistrements SRV**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91e1d-243">Under **Service (SRV Records)**, click **Edit SRV Records**, and then select the values from the following table.</span></span> 
        
    |<span data-ttu-id="91e1d-244">**Service**</span><span class="sxs-lookup"><span data-stu-id="91e1d-244">**Service**</span></span>|<span data-ttu-id="91e1d-245">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-245">**Protocol**</span></span>|<span data-ttu-id="91e1d-246">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-246">**TTL**</span></span>|<span data-ttu-id="91e1d-247">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-247">**Priority**</span></span>|<span data-ttu-id="91e1d-248">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-248">**Weight**</span></span>|<span data-ttu-id="91e1d-249">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-249">**Port**</span></span>|<span data-ttu-id="91e1d-250">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="91e1d-250">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="91e1d-251">_sip</span><span class="sxs-lookup"><span data-stu-id="91e1d-251">_sip</span></span> |<span data-ttu-id="91e1d-252">_tls</span><span class="sxs-lookup"><span data-stu-id="91e1d-252">_tls</span></span> |<span data-ttu-id="91e1d-253">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-253">3600</span></span> | <span data-ttu-id="91e1d-254">100</span><span class="sxs-lookup"><span data-stu-id="91e1d-254">100</span></span>|<span data-ttu-id="91e1d-255">0,1</span><span class="sxs-lookup"><span data-stu-id="91e1d-255">1</span></span> |<span data-ttu-id="91e1d-256">443</span><span class="sxs-lookup"><span data-stu-id="91e1d-256">443</span></span> |<span data-ttu-id="91e1d-257">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-257">sipfed.online.lync.com</span></span>  |
    |<span data-ttu-id="91e1d-258">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="91e1d-258">_sipfederationtls</span></span> |<span data-ttu-id="91e1d-259">_tcp</span><span class="sxs-lookup"><span data-stu-id="91e1d-259">_tcp</span></span> |<span data-ttu-id="91e1d-260">3600</span><span class="sxs-lookup"><span data-stu-id="91e1d-260">3600</span></span> |<span data-ttu-id="91e1d-261">100</span><span class="sxs-lookup"><span data-stu-id="91e1d-261">100</span></span> |<span data-ttu-id="91e1d-262">0,1</span><span class="sxs-lookup"><span data-stu-id="91e1d-262">1</span></span> |<span data-ttu-id="91e1d-263">5061</span><span class="sxs-lookup"><span data-stu-id="91e1d-263">5061</span></span> | <span data-ttu-id="91e1d-264">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="91e1d-264">sipfed.online.lync.com</span></span> |

  
5. <span data-ttu-id="91e1d-265">Ajoutez l’autre enregistrement SRV en choisissant les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="91e1d-265">Add the other SRV record by choosing the values from the second row of the table.</span></span> 
  
6. <span data-ttu-id="91e1d-266">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-266">Select **Continue**.</span></span>

7. <span data-ttu-id="91e1d-267">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="91e1d-267">Select **Save changes**.</span></span>

    
> [!NOTE]
>  <span data-ttu-id="91e1d-p116">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="91e1d-p116">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
