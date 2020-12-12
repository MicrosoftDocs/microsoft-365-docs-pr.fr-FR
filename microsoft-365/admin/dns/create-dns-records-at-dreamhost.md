---
title: Créer des enregistrements DNS sur Dreamhost pour Microsoft
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
ms.assetid: 9c0812e0-908b-4b41-a64b-77f0dbd3db7a
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Dreamhost pour Microsoft.
ms.openlocfilehash: 2faf7cae1fd9a0f9308e303c0588958e56b223e1
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49658122"
---
# <a name="create-dns-records-at-dreamhost-for-microsoft"></a><span data-ttu-id="718e7-103">Créer des enregistrements DNS sur Dreamhost pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="718e7-103">Create DNS records at Dreamhost for Microsoft</span></span>

 <span data-ttu-id="718e7-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="718e7-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="718e7-105">Si DreamHost est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Lync, etc.</span><span class="sxs-lookup"><span data-stu-id="718e7-105">If DreamHost is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Lync, and so on.</span></span>
 
<span data-ttu-id="718e7-106">Une fois ces enregistrements ajoutés sur DreamHost, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="718e7-106">After you add these records at DreamHost, your domain will be set up to work with Microsoft services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="718e7-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="718e7-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="718e7-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="718e7-110">Add a TXT record for verification</span></span>
<span data-ttu-id="718e7-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="718e7-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="718e7-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="718e7-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="718e7-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="718e7-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="718e7-116">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="718e7-116">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="718e7-117">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="718e7-117">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="718e7-119">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="718e7-119">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="718e7-121">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="718e7-121">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="718e7-123">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="718e7-123">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="718e7-124">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="718e7-124">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="718e7-125">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="718e7-125">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="718e7-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="718e7-126">**Name**</span></span>|<span data-ttu-id="718e7-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="718e7-127">**Type**</span></span>|<span data-ttu-id="718e7-128">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="718e7-128">**Value**</span></span>|<span data-ttu-id="718e7-129">**Comment**</span><span class="sxs-lookup"><span data-stu-id="718e7-129">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="718e7-130">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="718e7-130">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="718e7-131">TXT</span><span class="sxs-lookup"><span data-stu-id="718e7-131">TXT</span></span>  <br/> |<span data-ttu-id="718e7-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="718e7-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="718e7-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="718e7-133">**Note:** This is an example.</span></span> <span data-ttu-id="718e7-134">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="718e7-134">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="718e7-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="718e7-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="718e7-136">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-136">(This field is optional.)</span></span>  <br/> |
   
   ![Dreamhost-BP-Verify-1-1](../../media/ed4a7d43-eeeb-4ec8-849c-37f81315dc69.png)
  
5. <span data-ttu-id="718e7-138">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="718e7-138">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-Verify-1-2](../../media/5b89c89b-3a8e-4624-895a-86f3cc4638f6.png)
  
6. <span data-ttu-id="718e7-140">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="718e7-140">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="718e7-141">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="718e7-141">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="718e7-142">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="718e7-142">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="718e7-143">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="718e7-143">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="718e7-144">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="718e7-144">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="718e7-145">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="718e7-145">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="718e7-146">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="718e7-146">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="718e7-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="718e7-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="718e7-150">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="718e7-150">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="718e7-151"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="718e7-151"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="718e7-152">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="718e7-152">Follow the steps below.</span></span>
  
1. <span data-ttu-id="718e7-153">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="718e7-153">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="718e7-154">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="718e7-154">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="718e7-156">Sur la page **tableau de bord** , sélectionnez **courrier**, puis **MX personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="718e7-156">On the **Dashboard** page, select **Mail**, and then **Custom MX**.</span></span>
    
    ![Dreamhost-BP-configure-2-1](../../media/58478679-4018-49cc-9d83-371dc5fa4a22.png)
  
3. <span data-ttu-id="718e7-158">Dans la section **gérer la remise du courrier** , dans la colonne **actions** , sélectionnez **modifier** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="718e7-158">In the **Manage Mail Delivery** section, in the **Actions** column, select **Edit** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-2-2](../../media/6eed0be2-6477-4f49-9f90-39e190499a53.png)
  
4. <span data-ttu-id="718e7-160">Dans la section **enregistrement MX personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="718e7-160">In the **Custom MX Record** section, in the boxes for the new record, type or copy and paste the following values from the following table.</span></span> 
    
    <span data-ttu-id="718e7-161">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="718e7-161">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="718e7-162">(S’il existe d’autres enregistrements MX existants, marquez-les comme devant être supprimés.)</span><span class="sxs-lookup"><span data-stu-id="718e7-162">(If there are any other existing MX records, mark those records to be deleted.)</span></span>
    
    |<span data-ttu-id="718e7-163">**Enregistrement MX (obligatoire)**</span><span class="sxs-lookup"><span data-stu-id="718e7-163">**MX Record (required)**</span></span>|
    |:-----|
    |<span data-ttu-id="718e7-164">0  *\<domain-key\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-164">0  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="718e7-165">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-165">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="718e7-p108">La valeur 0 est la valeur de priorité Max. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par une espace.  </span><span class="sxs-lookup"><span data-stu-id="718e7-p108">The 0 is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="718e7-168">**Remarque :** Obtenir votre  *\<domain-key\>*  à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="718e7-168">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="718e7-169">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="718e7-169">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Dreamhost-BP-configure-2-3](../../media/90da1816-e186-4016-ab22-7962f8b86add.png)
  
5. <span data-ttu-id="718e7-171">Sélectionnez **modifier ce domaine pour utiliser des enregistrements MX personnalisés maintenant !**</span><span class="sxs-lookup"><span data-stu-id="718e7-171">Select **Change this domain to use custom MX records now!**</span></span>
    
    ![Dreamhost-BP-configure-2-4](../../media/3221c767-83d3-4f30-9d08-dc998772d2a3.png)
  
6. <span data-ttu-id="718e7-173">S’il existe d’autres enregistrements MX, supprimez chaque enregistrement en sélectionnant l’entrée et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="718e7-173">If there are any other existing MX records, delete each record by selecting the entry and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Dreamhost-BP-configure-2-5](../../media/1827733c-3609-4b0f-bba1-531ab090da91.png)
  
7. <span data-ttu-id="718e7-175">Si vous avez supprimé des enregistrements, sélectionnez **mettre à jour vos enregistrements MX personnalisés maintenant !**</span><span class="sxs-lookup"><span data-stu-id="718e7-175">If you have deleted any records, select **Update your custom MX records now!**</span></span>
    
    ![Dreamhost-BP-configure-2-6](../../media/177462be-0686-47b7-a389-025dfc8d6526.png)

  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="718e7-177">Ajouter les six enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="718e7-177">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="718e7-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="718e7-178"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="718e7-179">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="718e7-179">Follow the steps below.</span></span>
  
1. <span data-ttu-id="718e7-180">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="718e7-180">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="718e7-181">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="718e7-181">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="718e7-183">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="718e7-183">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="718e7-185">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="718e7-185">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="718e7-187">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="718e7-187">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="718e7-188">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="718e7-188">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="718e7-189">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="718e7-189">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="718e7-190">**Name**</span><span class="sxs-lookup"><span data-stu-id="718e7-190">**Name**</span></span>|<span data-ttu-id="718e7-191">**Type**</span><span class="sxs-lookup"><span data-stu-id="718e7-191">**Type**</span></span>|<span data-ttu-id="718e7-192">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="718e7-192">**Value**</span></span>|<span data-ttu-id="718e7-193">**Comment**</span><span class="sxs-lookup"><span data-stu-id="718e7-193">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="718e7-194">autodiscover</span><span class="sxs-lookup"><span data-stu-id="718e7-194">autodiscover</span></span>  <br/> |<span data-ttu-id="718e7-195">CNAME</span><span class="sxs-lookup"><span data-stu-id="718e7-195">CNAME</span></span>  <br/> |<span data-ttu-id="718e7-196">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-196">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="718e7-197">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-197">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-198">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-198">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="718e7-199">sip</span><span class="sxs-lookup"><span data-stu-id="718e7-199">sip</span></span>  <br/> |<span data-ttu-id="718e7-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="718e7-200">CNAME</span></span>  <br/> |<span data-ttu-id="718e7-201">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-201">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="718e7-202">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-202">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-203">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-203">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="718e7-204">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="718e7-204">lyncdiscover</span></span>  <br/> |<span data-ttu-id="718e7-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="718e7-205">CNAME</span></span>  <br/> |<span data-ttu-id="718e7-206">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-206">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="718e7-207">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-207">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-208">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-208">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="718e7-209">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="718e7-209">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="718e7-210">CNAME</span><span class="sxs-lookup"><span data-stu-id="718e7-210">CNAME</span></span>  <br/> |<span data-ttu-id="718e7-211">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="718e7-211">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="718e7-212">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-212">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-213">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-213">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="718e7-214">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="718e7-214">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="718e7-215">CNAME</span><span class="sxs-lookup"><span data-stu-id="718e7-215">CNAME</span></span>  <br/> |<span data-ttu-id="718e7-216">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-216">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="718e7-217">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-217">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-218">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-218">(This field is optional.)</span></span>  <br/> |
   
    ![Dreamhost-BP-configure-3-1](../../media/0c4cc587-ea24-47f2-8dc6-a35735b250e6.png)
  
5. <span data-ttu-id="718e7-220">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="718e7-220">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-configure-3-2](../../media/b5d4f939-de6d-4d1f-a20a-4eb5fe715281.png)
  
6. <span data-ttu-id="718e7-222">À l’aide des deux étapes précédentes et des valeurs des cinq autres lignes du tableau, ajoutez chacun des cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="718e7-222">Using the preceding two steps and the values from the other five rows in the table, add each of the other five CNAME records.</span></span>

  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="718e7-223">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="718e7-223">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="718e7-224"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="718e7-224"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="718e7-225">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="718e7-225">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="718e7-226">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="718e7-226">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="718e7-227">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="718e7-227">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="718e7-228">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="718e7-228">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
<span data-ttu-id="718e7-229">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="718e7-229">Follow the steps below.</span></span>
  
1. <span data-ttu-id="718e7-230">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="718e7-230">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="718e7-231">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="718e7-231">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="718e7-233">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="718e7-233">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="718e7-235">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="718e7-235">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="718e7-237">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="718e7-237">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="718e7-238">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="718e7-238">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="718e7-239">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="718e7-239">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="718e7-240">**Name**</span><span class="sxs-lookup"><span data-stu-id="718e7-240">**Name**</span></span>|<span data-ttu-id="718e7-241">**Type**</span><span class="sxs-lookup"><span data-stu-id="718e7-241">**Type**</span></span>|<span data-ttu-id="718e7-242">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="718e7-242">**Value**</span></span>|<span data-ttu-id="718e7-243">**Comment**</span><span class="sxs-lookup"><span data-stu-id="718e7-243">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="718e7-244">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="718e7-244">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="718e7-245">TXT</span><span class="sxs-lookup"><span data-stu-id="718e7-245">TXT</span></span>  <br/> |<span data-ttu-id="718e7-246">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="718e7-246">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="718e7-247">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="718e7-247">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="718e7-248">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-248">(This field is optional.)</span></span>  <br/> |
   
   ![Dreamhost-BP-configure-4-1](../../media/cbc4bbca-bdbc-4dc9-b1b7-b55491eb1e53.png)
  
5. <span data-ttu-id="718e7-250">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="718e7-250">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-configure-4-2](../../media/2bd7cae8-1fbc-4407-8dfa-06ce37c586c0.png)
  
6. <span data-ttu-id="718e7-252">À l’aide des deux étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="718e7-252">Using the preceding two steps and the values from the second row in the table, add the other SRV record.</span></span>
    
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="718e7-253">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="718e7-253">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="718e7-254"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="718e7-254"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="718e7-255">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="718e7-255">Follow the steps below.</span></span>
  
1. <span data-ttu-id="718e7-256">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="718e7-256">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="718e7-257">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="718e7-257">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="718e7-259">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="718e7-259">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="718e7-261">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="718e7-261">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="718e7-263">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="718e7-263">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="718e7-264">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="718e7-264">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="718e7-265">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="718e7-265">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="718e7-266">**Name**</span><span class="sxs-lookup"><span data-stu-id="718e7-266">**Name**</span></span>|<span data-ttu-id="718e7-267">**Type**</span><span class="sxs-lookup"><span data-stu-id="718e7-267">**Type**</span></span>|<span data-ttu-id="718e7-268">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="718e7-268">**Value**</span></span>|<span data-ttu-id="718e7-269">**Comment**</span><span class="sxs-lookup"><span data-stu-id="718e7-269">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="718e7-270">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="718e7-270">_sip._tls</span></span>  <br/> |<span data-ttu-id="718e7-271">SRV</span><span class="sxs-lookup"><span data-stu-id="718e7-271">SRV</span></span>  <br/> |<span data-ttu-id="718e7-272">100 1 443</span><span class="sxs-lookup"><span data-stu-id="718e7-272">100 1 443</span></span>  <br/> <span data-ttu-id="718e7-273">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-273">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="718e7-274">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-274">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-275">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-275">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="718e7-276">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="718e7-276">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="718e7-277">SRV</span><span class="sxs-lookup"><span data-stu-id="718e7-277">SRV</span></span>  <br/> |<span data-ttu-id="718e7-278">100 1 5061</span><span class="sxs-lookup"><span data-stu-id="718e7-278">100 1 5061</span></span>  <br/> <span data-ttu-id="718e7-279">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="718e7-279">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="718e7-280">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="718e7-280">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="718e7-281">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="718e7-281">(This field is optional.)</span></span>  <br/> |
   
    ![Dreamhost-BP-configure-5-1](../../media/934eb79f-3617-4b72-802c-c42c7d165283.png)
  
5. <span data-ttu-id="718e7-283">Sélectionnez **Ajouter un enregistrement maintenant**.</span><span class="sxs-lookup"><span data-stu-id="718e7-283">Select **Add Record Now!**.</span></span>
    
    ![Dreamhost-BP-configure-5-2](../../media/015bc73c-8f88-49ce-87f9-e5a6ea3e10a8.png)
  
6. <span data-ttu-id="718e7-285">À l’aide des deux étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="718e7-285">Using the preceding two steps and the values from the second row in the table, add the other SRV record.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="718e7-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="718e7-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
