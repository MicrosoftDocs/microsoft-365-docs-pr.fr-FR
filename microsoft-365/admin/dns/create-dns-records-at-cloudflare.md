---
title: Créer des enregistrements DNS sur cloudflare pour Office 365
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
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur cloudflare pour Office 365.
ms.openlocfilehash: 8d64824f880bab9e6691ebf47c9508c555562fe4
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211810"
---
# <a name="create-dns-records-at-cloudflare-for-office-365"></a><span data-ttu-id="708c9-103">Créer des enregistrements DNS sur cloudflare pour Office 365</span><span class="sxs-lookup"><span data-stu-id="708c9-103">Create DNS records at Cloudflare for Office 365</span></span>

 <span data-ttu-id="708c9-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="708c9-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="708c9-105">Si cloudflare est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="708c9-105">If Cloudflare is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="708c9-106">Une fois ces enregistrements ajoutés sur cloudflare, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="708c9-106">After you add these records at Cloudflare, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="708c9-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="708c9-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="708c9-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="708c9-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="708c9-111">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="708c9-111">Change your domain's nameserver (NS) records</span></span>
<span data-ttu-id="708c9-112"><a name="BKMK_Nameservers"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-112"><a name="BKMK_Nameservers"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="708c9-113">Vous devez effectuer cette procédure au niveau du bureau d'enregistrement de domaines auprès duquel vous avez acheté et inscrit votre domaine.</span><span class="sxs-lookup"><span data-stu-id="708c9-113">You must perform this procedure at the domain registrar where you purchased and registered your domain.</span></span> 
  
<span data-ttu-id="708c9-114">Lorsque vous vous êtes inscrit à cloudflare, vous avez ajouté un domaine à l’aide du processus de **configuration** de cloudflare.</span><span class="sxs-lookup"><span data-stu-id="708c9-114">When you signed up for Cloudflare, you added a domain by using the Cloudflare **Setup** process.</span></span> 
  
<span data-ttu-id="708c9-115">Le domaine que vous avez ajouté a été acheté auprès d’un bureau d’enregistrement de domaines distinct ; Cloudflare n’offre pas de services d’inscription de domaine.</span><span class="sxs-lookup"><span data-stu-id="708c9-115">The domain that you added was purchased from a separate domain registrar; Cloudflare does not offer domain registration services.</span></span> <span data-ttu-id="708c9-116">Pour vérifier et créer des enregistrements DNS pour votre domaine dans Office 365, vous devez d’abord modifier les serveurs de noms au niveau de votre bureau d’enregistrement de domaines afin qu’ils utilisent les serveurs de noms cloudflare.</span><span class="sxs-lookup"><span data-stu-id="708c9-116">To verify and create DNS records for your domain in Office 365, you first need to change the nameservers at your domain registrar so that they use Cloudflare's nameservers.</span></span>
  
<span data-ttu-id="708c9-117">Pour modifier vous-même les serveurs de noms de votre domaine sur le site web de votre bureau d'enregistrement de domaines, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="708c9-117">To change your domain's name servers at your domain registrar's website yourself, follow these steps.</span></span>
  
1. <span data-ttu-id="708c9-118">Identifiez la zone sur le site web du bureau d'enregistrement de domaines dans laquelle vous pouvez modifier les serveurs de noms pour votre domaine.</span><span class="sxs-lookup"><span data-stu-id="708c9-118">Find the area on the domain registrar's website where you can edit the nameservers for your domain.</span></span>
    
2. <span data-ttu-id="708c9-119">Créez deux enregistrements de serveur de noms à l’aide des valeurs indiquées dans le tableau suivant, ou modifiez les enregistrements de serveur de noms existants afin qu’ils correspondent à ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="708c9-119">Either create two nameserver records by using the values in the following table, or edit the existing nameserver records so that they match these values.</span></span>
    
    |||
    |:-----|:-----|
    |<span data-ttu-id="708c9-120">Premier serveur de noms</span><span class="sxs-lookup"><span data-stu-id="708c9-120">First nameserver</span></span>  <br/> |<span data-ttu-id="708c9-121">Utilisez la valeur de serveur de noms fournie par cloudflare.</span><span class="sxs-lookup"><span data-stu-id="708c9-121">Use the nameserver value provided by Cloudflare.</span></span>  <br/> |
    |<span data-ttu-id="708c9-122">Deuxième serveur de noms</span><span class="sxs-lookup"><span data-stu-id="708c9-122">Second nameserver</span></span>  <br/> |<span data-ttu-id="708c9-123">Utilisez la valeur de serveur de noms fournie par cloudflare.</span><span class="sxs-lookup"><span data-stu-id="708c9-123">Use the nameserver value provided by Cloudflare.</span></span>  <br/> |
   
    > [!TIP]
    > <span data-ttu-id="708c9-124">You should use at least two name server records.</span><span class="sxs-lookup"><span data-stu-id="708c9-124">You should use at least two name server records.</span></span> <span data-ttu-id="708c9-125">Si d’autres serveurs de noms sont répertoriés, vous devez les supprimer.</span><span class="sxs-lookup"><span data-stu-id="708c9-125">If there are any other name servers listed, you should delete them.</span></span> 
  
3. <span data-ttu-id="708c9-126">Enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="708c9-126">Save your changes.</span></span>
    
> [!NOTE]
> <span data-ttu-id="708c9-p104">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="708c9-p104">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="708c9-129">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="708c9-129">Add a TXT record for verification</span></span>
<span data-ttu-id="708c9-130"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-130"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="708c9-p105">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="708c9-p105">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="708c9-p106">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="708c9-p106">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="708c9-135">Pour commencer, accédez à la page de vos domaines sur cloudflare à l’aide de [ce lien](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="708c9-135">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="708c9-136">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="708c9-136">You'll be prompted to log in first.</span></span>
  
2. <span data-ttu-id="708c9-137">Sur la page d' **Accueil** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="708c9-137">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="708c9-138">Sur la page de **vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="708c9-138">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="708c9-139">Dans la page **gestion du DNS** , cliquez sur Ajouter un **enregistrement**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="708c9-139">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="708c9-140">**Type**</span><span class="sxs-lookup"><span data-stu-id="708c9-140">**Type**</span></span>|<span data-ttu-id="708c9-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="708c9-141">**Name**</span></span>|<span data-ttu-id="708c9-142">**TTL automatique**</span><span class="sxs-lookup"><span data-stu-id="708c9-142">**Automatic TTL**</span></span>|<span data-ttu-id="708c9-143">**Content (Contenu)**</span><span class="sxs-lookup"><span data-stu-id="708c9-143">**Content**</span></span>|
    |:-----|:-----|:-----|:----|
    |<span data-ttu-id="708c9-144">TXT</span><span class="sxs-lookup"><span data-stu-id="708c9-144">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="708c9-145">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-145">30 minutes</span></span>  <br/> |<span data-ttu-id="708c9-146">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="708c9-146">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="708c9-147">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="708c9-147">**Note:** This is an example.</span></span> <span data-ttu-id="708c9-148">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="708c9-148">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="708c9-149">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="708c9-149">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)    |
  
    
5. <span data-ttu-id="708c9-150">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="708c9-150">Select **Save**.</span></span>
  
  
9. <span data-ttu-id="708c9-151">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="708c9-151">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="708c9-152">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="708c9-152">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="708c9-153">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="708c9-153">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="708c9-154">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="708c9-154">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="708c9-155">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="708c9-155">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="708c9-156">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="708c9-156">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="708c9-157">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="708c9-157">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="708c9-p109">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="708c9-p109">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="708c9-161">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="708c9-161">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="708c9-162"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-162"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="708c9-163">Pour commencer, accédez à la page de vos domaines sur cloudflare à l’aide de [ce lien](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="708c9-163">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="708c9-164">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="708c9-164">You'll be prompted to log in first.</span></span>
  
2. <span data-ttu-id="708c9-165">Sur la page d' **Accueil** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="708c9-165">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="708c9-166">Sur la page de **vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="708c9-166">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="708c9-167">Dans la page **gestion du DNS** , cliquez sur Ajouter un **enregistrement**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="708c9-167">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span> 
    
    |<span data-ttu-id="708c9-168">**Type**</span><span class="sxs-lookup"><span data-stu-id="708c9-168">**Type**</span></span>|<span data-ttu-id="708c9-169">**Nom**</span><span class="sxs-lookup"><span data-stu-id="708c9-169">**Name**</span></span>|<span data-ttu-id="708c9-170">**Mail Server (Serveur de courrier)**</span><span class="sxs-lookup"><span data-stu-id="708c9-170">**Mail server**</span></span>|<span data-ttu-id="708c9-171">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="708c9-171">**Priority**</span></span>|<span data-ttu-id="708c9-172">**TTL**</span><span class="sxs-lookup"><span data-stu-id="708c9-172">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="708c9-173">MX</span><span class="sxs-lookup"><span data-stu-id="708c9-173">MX</span></span>  <br/> |@  <br/> |<span data-ttu-id="708c9-174">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="708c9-174">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="708c9-175">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="708c9-175">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="708c9-176">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="708c9-176">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) |<span data-ttu-id="708c9-177">0,1</span><span class="sxs-lookup"><span data-stu-id="708c9-177">1</span></span>  <br/> <span data-ttu-id="708c9-178">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="708c9-178">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/>|<span data-ttu-id="708c9-179">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-179">30 minutes</span></span>  <br/> |
   

  
5. <span data-ttu-id="708c9-180">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="708c9-180">Select **Save**.</span></span>
  
9. <span data-ttu-id="708c9-181">Si d’autres enregistrements MX sont répertoriés dans la section **MX Records (enregistrements MX** ), supprimez-les en sélectionnant l’icône **Delete (X)** .</span><span class="sxs-lookup"><span data-stu-id="708c9-181">If there are any other MX records listed in the **MX Records** section, delete them by selecting the **Delete (X)** icon.</span></span> 
  
10. <span data-ttu-id="708c9-182">Dans la boîte de dialogue de confirmation, sélectionnez **supprimer** pour confirmer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="708c9-182">In the confirmation dialog box, select **Delete** to confirm your changes.</span></span> 

  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="708c9-183">Ajouter les six enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="708c9-183">Add the Six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="708c9-184"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-184"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="708c9-185">Pour commencer, accédez à la page de vos domaines sur cloudflare à l’aide de [ce lien](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="708c9-185">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="708c9-186">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="708c9-186">You'll be prompted to log in first.</span></span>
    
  
2. <span data-ttu-id="708c9-187">Sur la page d' **Accueil** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="708c9-187">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="708c9-188">Sur la page de **vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="708c9-188">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="708c9-189">Ajoutez le premier des cinq enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="708c9-189">Add the first of the five CNAME records.</span></span>
    
    <span data-ttu-id="708c9-190">Dans la page **gestion du DNS** , cliquez sur Ajouter un **enregistrement**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="708c9-190">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span>
    
    
    |<span data-ttu-id="708c9-191">**Type**</span><span class="sxs-lookup"><span data-stu-id="708c9-191">**Type**</span></span>|<span data-ttu-id="708c9-192">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="708c9-192">**Name**</span></span>|<span data-ttu-id="708c9-193">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="708c9-193">**Target**</span></span>|<span data-ttu-id="708c9-194">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="708c9-194">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="708c9-195">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-195">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-196">autodiscover</span><span class="sxs-lookup"><span data-stu-id="708c9-196">autodiscover</span></span>  <br/> |<span data-ttu-id="708c9-197">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="708c9-197">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="708c9-198">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-198">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="708c9-199">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-199">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-200">sip</span><span class="sxs-lookup"><span data-stu-id="708c9-200">sip</span></span>  <br/> |<span data-ttu-id="708c9-201">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="708c9-201">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="708c9-202">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-202">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="708c9-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-203">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-204">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="708c9-204">lyncdiscover</span></span>  <br/> |<span data-ttu-id="708c9-205">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="708c9-205">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="708c9-206">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-206">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="708c9-207">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-207">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-208">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="708c9-208">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="708c9-209">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="708c9-209">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="708c9-210">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-210">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="708c9-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-211">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-212">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="708c9-212">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="708c9-213">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="708c9-213">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="708c9-214">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-214">30 minutes</span></span>  <br/> |
    |<span data-ttu-id="708c9-215">CNAME</span><span class="sxs-lookup"><span data-stu-id="708c9-215">CNAME</span></span>  <br/> |<span data-ttu-id="708c9-216">msoid</span><span class="sxs-lookup"><span data-stu-id="708c9-216">msoid</span></span>  <br/> |<span data-ttu-id="708c9-217">clientconfig.microsoftonline-p.net</span><span class="sxs-lookup"><span data-stu-id="708c9-217">clientconfig.microsoftonline-p.net</span></span>  <br/> |<span data-ttu-id="708c9-218">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-218">30 minutes</span></span>  <br/> |
    
  
5. <span data-ttu-id="708c9-219">Sélectionnez l’icône du **trafic DNS** (Cloud orange) pour contourner les serveurs cloudflare.</span><span class="sxs-lookup"><span data-stu-id="708c9-219">Select the **DNS Traffic** icon (orange cloud) to bypass the Cloudflare servers.</span></span>
  
6. <span data-ttu-id="708c9-220">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="708c9-220">Select **Save**.</span></span>
  
7. <span data-ttu-id="708c9-221">Ajoutez successivement les 5 autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="708c9-221">Add each of the other five CNAME records.</span></span>

    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="708c9-222">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="708c9-222">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="708c9-223"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-223"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="708c9-224">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="708c9-224">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="708c9-225">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="708c9-225">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="708c9-226">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="708c9-226">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="708c9-227">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="708c9-227">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="708c9-228">Pour commencer, accédez à la page de vos domaines sur cloudflare à l’aide de [ce lien](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="708c9-228">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="708c9-229">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="708c9-229">You'll be prompted to log in first.</span></span>
    
  
2. <span data-ttu-id="708c9-230">Sur la page d' **Accueil** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="708c9-230">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="708c9-231">Sur la page de **vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="708c9-231">On the **Overview** page for your domain, select **DNS**.</span></span>

  
4. <span data-ttu-id="708c9-232">Dans la page **gestion du DNS** , cliquez sur Ajouter un **enregistrement**, puis sélectionnez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="708c9-232">On the **DNS management** page, click **Add record**, and then select the values from the following table.</span></span>  
    
    |<span data-ttu-id="708c9-233">**Type**</span><span class="sxs-lookup"><span data-stu-id="708c9-233">**Type**</span></span>|<span data-ttu-id="708c9-234">**Nom**</span><span class="sxs-lookup"><span data-stu-id="708c9-234">**Name**</span></span>|<span data-ttu-id="708c9-235">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="708c9-235">**TTL**</span></span>|<span data-ttu-id="708c9-236">**Content (Contenu)**</span><span class="sxs-lookup"><span data-stu-id="708c9-236">**Content**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="708c9-237">TXT</span><span class="sxs-lookup"><span data-stu-id="708c9-237">TXT</span></span>  <br/> |@  <br/> |<span data-ttu-id="708c9-238">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-238">30 minutes</span></span>  <br/> |<span data-ttu-id="708c9-239">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="708c9-239">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="708c9-240">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="708c9-240">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>   |

 
5. <span data-ttu-id="708c9-241">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="708c9-241">Select **Save**.</span></span>
    

  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="708c9-242">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="708c9-242">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="708c9-243"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="708c9-243"><a name="BKMK_add_SRV"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="708c9-244">N’oubliez pas que cloudflare est responsable de la mise à disposition de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="708c9-244">Please keep in mind that Cloudflare is responsible for making this functionality available.</span></span> <span data-ttu-id="708c9-245">Si vous constatez des incohérences entre les étapes ci-dessous et l’interface utilisateur graphique (GUI) cloudflare actuelle, utilisez la [communauté cloudflare](https://community.cloudflare.com/).</span><span class="sxs-lookup"><span data-stu-id="708c9-245">In case you see discrepancies between the steps below and the current Cloudflare GUI(Graphical User Interface), please leverage the [Cloudflare Community](https://community.cloudflare.com/).</span></span> 

1. <span data-ttu-id="708c9-246">Pour commencer, accédez à la page de vos domaines sur cloudflare à l’aide de [ce lien](https://www.cloudflare.com/a/login).</span><span class="sxs-lookup"><span data-stu-id="708c9-246">To get started, go to your domains page at Cloudflare by using [this link](https://www.cloudflare.com/a/login).</span></span> <span data-ttu-id="708c9-247">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="708c9-247">You'll be prompted to log in first.</span></span>
      
2. <span data-ttu-id="708c9-248">Sur la page d' **Accueil** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="708c9-248">On the **Home** page, select the domain that you want to update.</span></span> 
  
3. <span data-ttu-id="708c9-249">Sur la page de **vue d’ensemble** de votre domaine, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="708c9-249">On the **Overview** page for your domain, select **DNS**.</span></span>
  
4. <span data-ttu-id="708c9-250">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="708c9-250">Add the first of the two SRV records.</span></span>

    <span data-ttu-id="708c9-251">Dans la page **gestion du DNS** , cliquez sur Ajouter un **enregistrement**, puis sélectionnez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="708c9-251">On the **DNS management** page, click **Add record**, and then select the values from the first row of the following table.</span></span>
        
    |<span data-ttu-id="708c9-252">**Type**</span><span class="sxs-lookup"><span data-stu-id="708c9-252">**Type**</span></span>|<span data-ttu-id="708c9-253">**Service**</span><span class="sxs-lookup"><span data-stu-id="708c9-253">**Service**</span></span>|<span data-ttu-id="708c9-254">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="708c9-254">**Protocol**</span></span>|<span data-ttu-id="708c9-255">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="708c9-255">**Name**</span></span>|<span data-ttu-id="708c9-256">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="708c9-256">**TTL**</span></span>|<span data-ttu-id="708c9-257">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="708c9-257">**Priority**</span></span>|<span data-ttu-id="708c9-258">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="708c9-258">**Weight**</span></span>|<span data-ttu-id="708c9-259">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="708c9-259">**Port**</span></span>|<span data-ttu-id="708c9-260">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="708c9-260">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="708c9-261">SRV</span><span class="sxs-lookup"><span data-stu-id="708c9-261">SRV</span></span>|<span data-ttu-id="708c9-262">_sip</span><span class="sxs-lookup"><span data-stu-id="708c9-262">_sip</span></span> |<span data-ttu-id="708c9-263">TLS</span><span class="sxs-lookup"><span data-stu-id="708c9-263">TLS</span></span> |<span data-ttu-id="708c9-264">Utiliser votre *domain_name*; par exemple, contoso.com</span><span class="sxs-lookup"><span data-stu-id="708c9-264">Use your *domain_name*; for example, contoso.com</span></span>  |<span data-ttu-id="708c9-265">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-265">30 minutes</span></span> | <span data-ttu-id="708c9-266">100</span><span class="sxs-lookup"><span data-stu-id="708c9-266">100</span></span>|<span data-ttu-id="708c9-267">0,1</span><span class="sxs-lookup"><span data-stu-id="708c9-267">1</span></span> |<span data-ttu-id="708c9-268">443</span><span class="sxs-lookup"><span data-stu-id="708c9-268">443</span></span> |<span data-ttu-id="708c9-269">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="708c9-269">sipfed.online.lync.com</span></span>  |
    |<span data-ttu-id="708c9-270">SRV</span><span class="sxs-lookup"><span data-stu-id="708c9-270">SRV</span></span>|<span data-ttu-id="708c9-271">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="708c9-271">_sipfederationtls</span></span> | <span data-ttu-id="708c9-272">TCP</span><span class="sxs-lookup"><span data-stu-id="708c9-272">TCP</span></span>|<span data-ttu-id="708c9-273">Utiliser votre *domain_name*; par exemple, contoso.com</span><span class="sxs-lookup"><span data-stu-id="708c9-273">Use your *domain_name*; for example, contoso.com</span></span>   |<span data-ttu-id="708c9-274">30 minutes</span><span class="sxs-lookup"><span data-stu-id="708c9-274">30 minutes</span></span> |<span data-ttu-id="708c9-275">100</span><span class="sxs-lookup"><span data-stu-id="708c9-275">100</span></span> |<span data-ttu-id="708c9-276">0,1</span><span class="sxs-lookup"><span data-stu-id="708c9-276">1</span></span> |<span data-ttu-id="708c9-277">5061</span><span class="sxs-lookup"><span data-stu-id="708c9-277">5061</span></span> | <span data-ttu-id="708c9-278">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="708c9-278">sipfed.online.lync.com</span></span> |

  
5. <span data-ttu-id="708c9-279">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="708c9-279">Select **Save**.</span></span>

  
6. <span data-ttu-id="708c9-280">Ajoutez l’autre enregistrement SRV en choisissant les valeurs de la deuxième ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="708c9-280">Add the other SRV record by choosing the values from the second row of the table.</span></span> 

    
> [!NOTE]
>  <span data-ttu-id="708c9-p117">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="708c9-p117">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
