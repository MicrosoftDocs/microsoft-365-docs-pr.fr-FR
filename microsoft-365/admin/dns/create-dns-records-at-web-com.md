---
title: Créer des enregistrements DNS sur web.com pour Office 365
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
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 84acd4fc-6eec-4d00-8bed-568f036ae2af
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur web.com pour Office 365.
ms.openlocfilehash: eb231f85e568e81a5e229f0533d8176feb590f48
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42249454"
---
# <a name="create-dns-records-at-webcom-for-office-365"></a><span data-ttu-id="64022-103">Créer des enregistrements DNS sur web.com pour Office 365</span><span class="sxs-lookup"><span data-stu-id="64022-103">Create DNS records at web.com for Office 365</span></span>

 <span data-ttu-id="64022-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="64022-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="64022-105">Si web.com est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="64022-105">If web.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="64022-106">Une fois ces enregistrements ajoutés sur web.com, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="64022-106">After you add these records at web.com, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="64022-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="64022-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="64022-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="64022-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="64022-111">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="64022-111">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="64022-112"><a name="BKMK_Nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-112"><a name="BKMK_Nameservers"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="64022-113">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="64022-113">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="64022-114">Lorsque vous vous êtes inscrit à web.com, vous avez ajouté un domaine à l’aide du processus de **configuration** de Web.com.</span><span class="sxs-lookup"><span data-stu-id="64022-114">When you signed up for web.com, you added a domain by using the web.com **Setup** process.</span></span> 
  
<span data-ttu-id="64022-115">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Office 365, vous devez d’abord modifier les serveurs de noms dans votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms de Web. com.</span><span class="sxs-lookup"><span data-stu-id="64022-115">To verify and create DNS records for your domain in Office 365, you first need to change the nameservers at your domain registrar so that they use web.com's nameservers.</span></span>
  
<span data-ttu-id="64022-116">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="64022-116">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="64022-117">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="64022-117">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="64022-118">Créez deux enregistrements de serveur de noms à l’aide des valeurs indiquées dans le tableau suivant, ou modifiez les enregistrements de serveur de noms existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="64022-118">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="64022-119">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="64022-119">First nameserver</span></span>  <br/> |<span data-ttu-id="64022-120">Utilisez la valeur de serveur de noms fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="64022-120">Use the nameserver value provided by web.com.</span></span>  <br/> |
    |<span data-ttu-id="64022-121">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="64022-121">Second nameserver</span></span>  <br/> |<span data-ttu-id="64022-122">Utilisez la valeur de serveur de noms fournie par web.com.</span><span class="sxs-lookup"><span data-stu-id="64022-122">Use the nameserver value provided by web.com.</span></span>  <br/> |
   
    > [!TIP]
    > <span data-ttu-id="64022-123">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="64022-123">You should use at least two name server records.</span></span> <span data-ttu-id="64022-124">Si d’autres serveurs de noms sont répertoriés, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="64022-124">If there are any other name servers listed, you should delete them.</span></span> 
  
3. <span data-ttu-id="64022-125">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="64022-125">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="64022-p103">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="64022-p103">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="64022-128">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="64022-128">Add a TXT record for verification</span></span>
<span data-ttu-id="64022-129"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-129"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="64022-p104">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="64022-p104">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="64022-p105">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="64022-p105">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="64022-134">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="64022-134">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="64022-135">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="64022-135">Log in first.</span></span>
  
2. <span data-ttu-id="64022-136">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="64022-136">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="64022-137">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="64022-137">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="64022-138">Dans la page **noms de domaine** , sous **texte (enregistrements TXT)**, cliquez sur **modifier les enregistrements TXT**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64022-138">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="64022-139">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="64022-139">**Host**</span></span>|<span data-ttu-id="64022-140">**TTL**</span><span class="sxs-lookup"><span data-stu-id="64022-140">**TTL**</span></span>|<span data-ttu-id="64022-141">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="64022-141">**Text**</span></span>|
    |:-----|:-----|:----|
    |@  <br/> |<span data-ttu-id="64022-142">3600</span><span class="sxs-lookup"><span data-stu-id="64022-142">3600</span></span>  <br/> |<span data-ttu-id="64022-143">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="64022-143">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="64022-144">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="64022-144">**Note:** This is an example.</span></span> <span data-ttu-id="64022-145">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="64022-145">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="64022-146">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="64022-146">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
  
    
5. <span data-ttu-id="64022-147">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="64022-147">Select **Continue**.</span></span>
  
  
6. <span data-ttu-id="64022-148">Patientez quelques minutes avant de vérifier votre nouvel enregistrement TXT, afin que l’enregistrement que vous venez de créer puisse être mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="64022-148">Wait a few minutes before you verify your new TXT record, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="64022-149">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="64022-149">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="64022-150">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="64022-150">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="64022-151">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="64022-151">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="64022-152">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="64022-152">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="64022-153">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="64022-153">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="64022-154">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="64022-154">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="64022-p108">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="64022-p108">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="64022-158">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="64022-158">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="64022-159"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-159"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="64022-160">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="64022-160">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="64022-161">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="64022-161">Log in first.</span></span>
  
2. <span data-ttu-id="64022-162">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="64022-162">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="64022-163">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="64022-163">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="64022-164">Sous **serveurs de messagerie (enregistrements MX)**, cliquez sur **modifier les enregistrements MX**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64022-164">Under **Mail Servers (MX Records)**, click **Edit MX Records**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="64022-165">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="64022-165">**Priority**</span></span>|<span data-ttu-id="64022-166">**TTL**</span><span class="sxs-lookup"><span data-stu-id="64022-166">**TTL**</span></span>|<span data-ttu-id="64022-167">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="64022-167">**Mail server**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="64022-168">0,1</span><span class="sxs-lookup"><span data-stu-id="64022-168">1</span></span>  <br/> <span data-ttu-id="64022-169">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="64022-169">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="64022-170">3600</span><span class="sxs-lookup"><span data-stu-id="64022-170">3600</span></span>  <br/> |<span data-ttu-id="64022-171">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="64022-171">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="64022-172">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="64022-172">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="64022-173">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="64022-173">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |
   

5. <span data-ttu-id="64022-174">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="64022-174">Select **Save**.</span></span>
  
6. <span data-ttu-id="64022-175">Si d’autres enregistrements MX sont répertoriés dans la section **MX Records (enregistrements MX** ), activez la case à cocher en regard de l’enregistrement sous **Delete (supprimer**), puis sélectionnez Save ( **Enregistrer**).</span><span class="sxs-lookup"><span data-stu-id="64022-175">If there are any other MX records listed in the **MX Records** section, select the check box next to the record under **Delete**, and select **Save**.</span></span> 
  
7. <span data-ttu-id="64022-176">Dans l’écran de confirmation, sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="64022-176">On the confirmation screen, select **Save changes**.</span></span> 

  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="64022-177">Ajouter les six enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="64022-177">Add the Six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="64022-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-178"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="64022-179">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="64022-179">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="64022-180">You'll be prompted to log in first.</span><span class="sxs-lookup"><span data-stu-id="64022-180">You'll be prompted to log in first.</span></span>
     
2. <span data-ttu-id="64022-181">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="64022-181">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="64022-182">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="64022-182">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

4. <span data-ttu-id="64022-183">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="64022-183">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="64022-184">Sous **alias d’hôte (enregistrements CNAME)**, cliquez sur **modifier les enregistrements CNAME**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64022-184">Under **Host Aliases (CNAME Records)**, click **Edit CNAME Records**, and then select the values from the following table.</span></span>
    
    
    |<span data-ttu-id="64022-185">**Alias (Alias)**</span><span class="sxs-lookup"><span data-stu-id="64022-185">**Alias**</span></span>|<span data-ttu-id="64022-186">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="64022-186">**TTL**</span></span>|<span data-ttu-id="64022-187">**Refers to Host Name (Fait référence au nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="64022-187">**Refers to Host Name**</span></span>|<span data-ttu-id="64022-188">**Autre hôte**</span><span class="sxs-lookup"><span data-stu-id="64022-188">**Other Host**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="64022-189">autodiscover</span><span class="sxs-lookup"><span data-stu-id="64022-189">autodiscover</span></span>  <br/> |<span data-ttu-id="64022-190">3600</span><span class="sxs-lookup"><span data-stu-id="64022-190">3600</span></span>  <br/> |<span data-ttu-id="64022-191">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-191">@ (none)</span></span>  <br/> |<span data-ttu-id="64022-192">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="64022-192">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="64022-193">sip</span><span class="sxs-lookup"><span data-stu-id="64022-193">sip</span></span>  <br/> |<span data-ttu-id="64022-194">3600</span><span class="sxs-lookup"><span data-stu-id="64022-194">3600</span></span>  <br/> |<span data-ttu-id="64022-195">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-195">@ (none)</span></span>  <br/> |<span data-ttu-id="64022-196">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="64022-196">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="64022-197">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="64022-197">lyncdiscover</span></span>  <br/> |<span data-ttu-id="64022-198">3600</span><span class="sxs-lookup"><span data-stu-id="64022-198">3600</span></span>  <br/> |<span data-ttu-id="64022-199">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-199">@ (none)</span></span>  <br/> | <span data-ttu-id="64022-200">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="64022-200">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="64022-201">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="64022-201">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="64022-202">3600</span><span class="sxs-lookup"><span data-stu-id="64022-202">3600</span></span>  <br/> |<span data-ttu-id="64022-203">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-203">@ (none)</span></span>  <br/> |<span data-ttu-id="64022-204">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="64022-204">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="64022-205">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="64022-205">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="64022-206">3600</span><span class="sxs-lookup"><span data-stu-id="64022-206">3600</span></span>  <br/> |<span data-ttu-id="64022-207">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-207">@ (none)</span></span>  <br/> |<span data-ttu-id="64022-208">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="64022-208">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
    |<span data-ttu-id="64022-209">msoid</span><span class="sxs-lookup"><span data-stu-id="64022-209">msoid</span></span>  <br/> |<span data-ttu-id="64022-210">3600</span><span class="sxs-lookup"><span data-stu-id="64022-210">3600</span></span>  <br/> |<span data-ttu-id="64022-211">@ (aucun)</span><span class="sxs-lookup"><span data-stu-id="64022-211">@ (none)</span></span>  <br/> |<span data-ttu-id="64022-212">clientconfig.microsoftonline-p.net</span><span class="sxs-lookup"><span data-stu-id="64022-212">clientconfig.microsoftonline-p.net</span></span>  <br/> |
    
  
5. <span data-ttu-id="64022-213">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="64022-213">Select **Continue**.</span></span>
  
6. <span data-ttu-id="64022-214">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="64022-214">Add each of the other five CNAME records.</span></span>

    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="64022-215">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="64022-215">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="64022-216"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-216"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="64022-217">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="64022-217">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="64022-218">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="64022-218">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="64022-219">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="64022-219">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="64022-220">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="64022-220">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="64022-221">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="64022-221">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="64022-222">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="64022-222">Log in first.</span></span>
    
  
2. <span data-ttu-id="64022-223">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="64022-223">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="64022-224">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="64022-224">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>

  
4. <span data-ttu-id="64022-225">Dans la page **noms de domaine** , sous **texte (enregistrements TXT)**, cliquez sur **modifier les enregistrements TXT**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64022-225">On the **Domain Names** page, under **Text (TXT Records)**, click **Edit TXT Records**, and then select the values from the following table.</span></span>   
    
    |<span data-ttu-id="64022-226">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="64022-226">**Host**</span></span>|<span data-ttu-id="64022-227">**TTL**</span><span class="sxs-lookup"><span data-stu-id="64022-227">**TTL**</span></span>|<span data-ttu-id="64022-228">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="64022-228">**Text**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="64022-229">3600</span><span class="sxs-lookup"><span data-stu-id="64022-229">3600</span></span>  <br/> |<span data-ttu-id="64022-230">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="64022-230">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="64022-231">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="64022-231">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>   |

 
5. <span data-ttu-id="64022-232">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="64022-232">Select **Continue**.</span></span>

6. <span data-ttu-id="64022-233">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="64022-233">Select **Save changes**.</span></span>
    

  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="64022-234">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="64022-234">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="64022-235"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="64022-235"><a name="BKMK_add_SRV"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="64022-236">N’oubliez pas que web.com est responsable de la mise à disposition de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="64022-236">Please keep in mind that web.com is responsible for making this functionality available.</span></span> <span data-ttu-id="64022-237">Si vous constatez des incohérences entre les étapes ci-dessous et l’interface utilisateur graphique (GUI) web.com actuelle, utilisez la [communauté Web.com](https://community.web.com.com/).</span><span class="sxs-lookup"><span data-stu-id="64022-237">In case you see discrepancies between the steps below and the current web.com GUI(Graphical User Interface), please leverage the [web.com Community](https://community.web.com.com/).</span></span> 

1. <span data-ttu-id="64022-238">Pour commencer, accédez à la page de vos domaines sur web.com à l’aide de [ce lien](https://checkout.web.com/manage-it/index.jsp).</span><span class="sxs-lookup"><span data-stu-id="64022-238">To get started, go to your domains page at web.com by using [this link](https://checkout.web.com/manage-it/index.jsp).</span></span> <span data-ttu-id="64022-239">Connectez-vous d’abord.</span><span class="sxs-lookup"><span data-stu-id="64022-239">Log in first.</span></span>
      
2. <span data-ttu-id="64022-240">Sur la page **Gestionnaire de comptes** , sélectionnez **mes noms de domaine**.</span><span class="sxs-lookup"><span data-stu-id="64022-240">On the **Account Manager** page, select **My Domain Names**.</span></span> 
  
3. <span data-ttu-id="64022-241">Sous \* \* Manage \* my Domain \* \* \*, sélectionnez **modifier les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="64022-241">Under \*\*Manage \*my domain\*\*\*, select **Edit Advanced DNS Records**.</span></span>
  
4. <span data-ttu-id="64022-242">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="64022-242">Add the first of the two SRV records.</span></span>

    <span data-ttu-id="64022-243">Sous **service (enregistrements SRV)**, cliquez sur **modifier les enregistrements SRV**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64022-243">Under **Service (SRV Records)**, click **Edit SRV Records**, and then select the values from the following table.</span></span> 
        
    |<span data-ttu-id="64022-244">**Service**</span><span class="sxs-lookup"><span data-stu-id="64022-244">**Service**</span></span>|<span data-ttu-id="64022-245">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="64022-245">**Protocol**</span></span>|<span data-ttu-id="64022-246">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="64022-246">**TTL**</span></span>|<span data-ttu-id="64022-247">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="64022-247">**Priority**</span></span>|<span data-ttu-id="64022-248">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="64022-248">**Weight**</span></span>|<span data-ttu-id="64022-249">**Port**</span><span class="sxs-lookup"><span data-stu-id="64022-249">**Port**</span></span>|<span data-ttu-id="64022-250">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="64022-250">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="64022-251">_sip</span><span class="sxs-lookup"><span data-stu-id="64022-251">_sip</span></span> |<span data-ttu-id="64022-252">_tls</span><span class="sxs-lookup"><span data-stu-id="64022-252">_tls</span></span> |<span data-ttu-id="64022-253">3600</span><span class="sxs-lookup"><span data-stu-id="64022-253">3600</span></span> | <span data-ttu-id="64022-254">100</span><span class="sxs-lookup"><span data-stu-id="64022-254">100</span></span>|<span data-ttu-id="64022-255">0,1</span><span class="sxs-lookup"><span data-stu-id="64022-255">1</span></span> |<span data-ttu-id="64022-256">443</span><span class="sxs-lookup"><span data-stu-id="64022-256">443</span></span> |<span data-ttu-id="64022-257">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="64022-257">sipfed.online.lync.com</span></span>  |
    |<span data-ttu-id="64022-258">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="64022-258">_sipfederationtls</span></span> |<span data-ttu-id="64022-259">_tcp</span><span class="sxs-lookup"><span data-stu-id="64022-259">_tcp</span></span> |<span data-ttu-id="64022-260">3600</span><span class="sxs-lookup"><span data-stu-id="64022-260">3600</span></span> |<span data-ttu-id="64022-261">100</span><span class="sxs-lookup"><span data-stu-id="64022-261">100</span></span> |<span data-ttu-id="64022-262">0,1</span><span class="sxs-lookup"><span data-stu-id="64022-262">1</span></span> |<span data-ttu-id="64022-263">5061</span><span class="sxs-lookup"><span data-stu-id="64022-263">5061</span></span> | <span data-ttu-id="64022-264">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="64022-264">sipfed.online.lync.com</span></span> |

  
5. <span data-ttu-id="64022-265">Ajoutez l’autre enregistrement SRV en choisissant les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="64022-265">Add the other SRV record by choosing the values from the second row of the table.</span></span> 
  
6. <span data-ttu-id="64022-266">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="64022-266">Select **Continue**.</span></span>

7. <span data-ttu-id="64022-267">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="64022-267">Select **Save changes**.</span></span>

    
> [!NOTE]
>  <span data-ttu-id="64022-p116">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="64022-p116">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
