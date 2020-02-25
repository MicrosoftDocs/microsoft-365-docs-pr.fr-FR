---
title: Créer des enregistrements DNS sur Dreamhost pour Office 365
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
ms.assetid: 9c0812e0-908b-4b41-a64b-77f0dbd3db7a
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Dreamhost pour Office 365.
ms.openlocfilehash: f3f52e97fefece72dd96d9370e75e24fc4cebedf
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42244705"
---
# <a name="create-dns-records-at-dreamhost-for-office-365"></a><span data-ttu-id="f6179-103">Créer des enregistrements DNS sur Dreamhost pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f6179-103">Create DNS records at Dreamhost for Office 365</span></span>

 <span data-ttu-id="f6179-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f6179-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f6179-105">Si DreamHost est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Lync, etc.</span><span class="sxs-lookup"><span data-stu-id="f6179-105">If DreamHost is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Lync, and so on.</span></span>
 
<span data-ttu-id="f6179-106">Une fois ces enregistrements ajoutés sur DreamHost, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6179-106">After you add these records at DreamHost, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="f6179-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6179-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f6179-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f6179-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f6179-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f6179-111">Add a TXT record for verification</span></span>
<span data-ttu-id="f6179-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="f6179-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="f6179-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="f6179-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f6179-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f6179-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f6179-117">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="f6179-117">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="f6179-118">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f6179-118">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="f6179-120">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="f6179-120">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="f6179-122">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f6179-122">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="f6179-124">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f6179-124">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f6179-125">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f6179-125">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="f6179-126">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f6179-126">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f6179-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6179-127">**Name**</span></span>|<span data-ttu-id="f6179-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="f6179-128">**Type**</span></span>|<span data-ttu-id="f6179-129">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f6179-129">**Value**</span></span>|<span data-ttu-id="f6179-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6179-130">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f6179-131">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f6179-131">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f6179-132">TXT</span><span class="sxs-lookup"><span data-stu-id="f6179-132">TXT</span></span>  <br/> |<span data-ttu-id="f6179-133">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f6179-133">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="f6179-134">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="f6179-134">**Note:** This is an example.</span></span> <span data-ttu-id="f6179-135">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6179-135">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="f6179-136">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f6179-136">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="f6179-137">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-137">(This field is optional.)</span></span>  <br/> |
   
   ![Dreamhost-BP-Verify-1-1](../media/ed4a7d43-eeeb-4ec8-849c-37f81315dc69.png)
  
5. <span data-ttu-id="f6179-139">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="f6179-139">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-Verify-1-2](../media/5b89c89b-3a8e-4624-895a-86f3cc4638f6.png)
  
6. <span data-ttu-id="f6179-141">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f6179-141">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f6179-142">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="f6179-142">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="f6179-143">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="f6179-143">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f6179-144">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="f6179-144">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="f6179-145">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f6179-145">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="f6179-146">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="f6179-146">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="f6179-147">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f6179-147">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="f6179-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f6179-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="f6179-151">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="f6179-151">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="f6179-152"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="f6179-152"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="f6179-153">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f6179-153">Follow the steps below.</span></span>
  
1. <span data-ttu-id="f6179-154">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="f6179-154">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="f6179-155">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f6179-155">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="f6179-157">Sur la page **tableau de bord** , sélectionnez **courrier**, puis **MX personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="f6179-157">On the **Dashboard** page, select **Mail**, and then **Custom MX**.</span></span>
    
    ![Dreamhost-BP-configure-2-1](../media/58478679-4018-49cc-9d83-371dc5fa4a22.png)
  
3. <span data-ttu-id="f6179-159">Dans la section **gérer la remise du courrier** , dans la colonne **actions** , sélectionnez **modifier** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f6179-159">In the **Manage Mail Delivery** section, in the **Actions** column, select **Edit** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-2-2](../media/6eed0be2-6477-4f49-9f90-39e190499a53.png)
  
4. <span data-ttu-id="f6179-161">Dans la section **enregistrement MX personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f6179-161">In the **Custom MX Record** section, in the boxes for the new record, type or copy and paste the following values from the following table.</span></span> 
    
    <span data-ttu-id="f6179-162">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f6179-162">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="f6179-163">(S’il existe d’autres enregistrements MX existants, marquez-les comme devant être supprimés.)</span><span class="sxs-lookup"><span data-stu-id="f6179-163">(If there are any other existing MX records, mark those records to be deleted.)</span></span>
    
    |<span data-ttu-id="f6179-164">**Enregistrement MX (obligatoire)**</span><span class="sxs-lookup"><span data-stu-id="f6179-164">**MX Record (required)**</span></span>|
    |:-----|
    |<span data-ttu-id="f6179-165">0  *\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-165">0  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="f6179-166">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-166">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="f6179-p108">La valeur 0 est la valeur de priorité Max. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par une espace.  </span><span class="sxs-lookup"><span data-stu-id="f6179-p108">The 0 is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="f6179-169">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6179-169">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="f6179-170">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f6179-170">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Dreamhost-BP-configure-2-3](../media/90da1816-e186-4016-ab22-7962f8b86add.png)
  
5. <span data-ttu-id="f6179-172">Sélectionnez **modifier ce domaine pour utiliser des enregistrements MX personnalisés maintenant !**</span><span class="sxs-lookup"><span data-stu-id="f6179-172">Select **Change this domain to use custom MX records now!**</span></span>
    
    ![Dreamhost-BP-configure-2-4](../media/3221c767-83d3-4f30-9d08-dc998772d2a3.png)
  
6. <span data-ttu-id="f6179-174">S’il existe d’autres enregistrements MX, supprimez chaque enregistrement en sélectionnant l’entrée et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="f6179-174">If there are any other existing MX records, delete each record by selecting the entry and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Dreamhost-BP-configure-2-5](../media/1827733c-3609-4b0f-bba1-531ab090da91.png)
  
7. <span data-ttu-id="f6179-176">Si vous avez supprimé des enregistrements, sélectionnez **mettre à jour vos enregistrements MX personnalisés maintenant !**</span><span class="sxs-lookup"><span data-stu-id="f6179-176">If you have deleted any records, select **Update your custom MX records now!**</span></span>
    
    ![Dreamhost-BP-configure-2-6](../media/177462be-0686-47b7-a389-025dfc8d6526.png)

  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="f6179-178">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f6179-178">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="f6179-179"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="f6179-179"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="f6179-180">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f6179-180">Follow the steps below.</span></span>
  
1. <span data-ttu-id="f6179-181">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="f6179-181">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="f6179-182">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f6179-182">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="f6179-184">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="f6179-184">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="f6179-186">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f6179-186">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="f6179-188">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f6179-188">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="f6179-189">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f6179-189">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="f6179-190">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f6179-190">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f6179-191">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6179-191">**Name**</span></span>|<span data-ttu-id="f6179-192">**Type**</span><span class="sxs-lookup"><span data-stu-id="f6179-192">**Type**</span></span>|<span data-ttu-id="f6179-193">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f6179-193">**Value**</span></span>|<span data-ttu-id="f6179-194">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6179-194">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f6179-195">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f6179-195">autodiscover</span></span>  <br/> |<span data-ttu-id="f6179-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="f6179-196">CNAME</span></span>  <br/> |<span data-ttu-id="f6179-197">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-197">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="f6179-198">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-198">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-199">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-199">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="f6179-200">sip</span><span class="sxs-lookup"><span data-stu-id="f6179-200">sip</span></span>  <br/> |<span data-ttu-id="f6179-201">CNAME</span><span class="sxs-lookup"><span data-stu-id="f6179-201">CNAME</span></span>  <br/> |<span data-ttu-id="f6179-202">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-202">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="f6179-203">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-203">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-204">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-204">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="f6179-205">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f6179-205">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f6179-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="f6179-206">CNAME</span></span>  <br/> |<span data-ttu-id="f6179-207">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-207">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="f6179-208">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-208">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-209">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-209">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="f6179-210">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f6179-210">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f6179-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="f6179-211">CNAME</span></span>  <br/> |<span data-ttu-id="f6179-212">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f6179-212">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="f6179-213">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-213">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-214">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-214">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="f6179-215">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f6179-215">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f6179-216">CNAME</span><span class="sxs-lookup"><span data-stu-id="f6179-216">CNAME</span></span>  <br/> |<span data-ttu-id="f6179-217">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-217">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="f6179-218">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-218">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-219">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-219">(This field is optional.)</span></span>  <br/> |
   
    ![Dreamhost-BP-configure-3-1](../media/0c4cc587-ea24-47f2-8dc6-a35735b250e6.png)
  
5. <span data-ttu-id="f6179-221">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="f6179-221">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-configure-3-2](../media/b5d4f939-de6d-4d1f-a20a-4eb5fe715281.png)
  
6. <span data-ttu-id="f6179-223">À l’aide des deux étapes précédentes et des valeurs des cinq autres lignes du tableau, ajoutez chacun des cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="f6179-223">Using the preceding two steps and the values from the other five rows in the table, add each of the other five CNAME records.</span></span>

  
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f6179-224">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f6179-224">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f6179-225"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="f6179-225"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6179-226">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="f6179-226">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f6179-227">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="f6179-227">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f6179-228">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6179-228">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="f6179-229">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f6179-229">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
<span data-ttu-id="f6179-230">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f6179-230">Follow the steps below.</span></span>
  
1. <span data-ttu-id="f6179-231">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="f6179-231">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="f6179-232">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f6179-232">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="f6179-234">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="f6179-234">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="f6179-236">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f6179-236">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="f6179-238">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f6179-238">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="f6179-239">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f6179-239">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="f6179-240">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f6179-240">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f6179-241">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6179-241">**Name**</span></span>|<span data-ttu-id="f6179-242">**Type**</span><span class="sxs-lookup"><span data-stu-id="f6179-242">**Type**</span></span>|<span data-ttu-id="f6179-243">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f6179-243">**Value**</span></span>|<span data-ttu-id="f6179-244">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6179-244">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f6179-245">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="f6179-245">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="f6179-246">TXT</span><span class="sxs-lookup"><span data-stu-id="f6179-246">TXT</span></span>  <br/> |<span data-ttu-id="f6179-247">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f6179-247">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f6179-248">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f6179-248">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="f6179-249">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-249">(This field is optional.)</span></span>  <br/> |
   
   ![Dreamhost-BP-configure-4-1](../media/cbc4bbca-bdbc-4dc9-b1b7-b55491eb1e53.png)
  
5. <span data-ttu-id="f6179-251">Sélectionnez **Ajouter un enregistrement maintenant.**</span><span class="sxs-lookup"><span data-stu-id="f6179-251">Select **Add Record Now!**</span></span>
    
    ![Dreamhost-BP-configure-4-2](../media/2bd7cae8-1fbc-4407-8dfa-06ce37c586c0.png)
  
6. <span data-ttu-id="f6179-253">À l’aide des deux étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f6179-253">Using the preceding two steps and the values from the second row in the table, add the other SRV record.</span></span>
    
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="f6179-254">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="f6179-254">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="f6179-255"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="f6179-255"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="f6179-256">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f6179-256">Follow the steps below.</span></span>
  
1. <span data-ttu-id="f6179-257">Pour commencer, accédez à la page de vos domaines sur DreamHost à l’aide de [ce lien](https://panel.dreamhost.com/).</span><span class="sxs-lookup"><span data-stu-id="f6179-257">To get started, go to your domains page at DreamHost by using [this link](https://panel.dreamhost.com/).</span></span> <span data-ttu-id="f6179-258">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f6179-258">You'll be prompted to Sign in.</span></span>
    
    ![Dreamhost-BP-configure-1-1](../media/1919b810-b6ba-4e29-a774-de1e7c67d078.png)
  
2. <span data-ttu-id="f6179-260">Sur la page **tableau de bord** , sélectionnez **domaines**, puis gérer les **domaines**.</span><span class="sxs-lookup"><span data-stu-id="f6179-260">On the **Dashboard** page, select **Domains**, and then **Manage Domains**.</span></span>
    
    ![Dreamhost-BP-configure-1-2](../media/ab05c16a-79f6-491f-ad07-9a2e6674671d.png)
  
3. <span data-ttu-id="f6179-262">Dans la page **gérer les domaines** , dans la section **domaine** , sélectionnez **DNS** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f6179-262">On the **Manage Domains** page, in the **Domain** section, select **DNS** for the domain that you want to edit.</span></span> 
    
    ![Dreamhost-BP-configure-1-3](../media/1a8723a0-54bc-40ff-bc30-5fc3e8cd219b.png)
  
4. <span data-ttu-id="f6179-264">Dans la section **Ajouter un enregistrement DNS personnalisé** , dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f6179-264">In the **Add a custom DNS record** section, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="f6179-265">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="f6179-265">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="f6179-266">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="f6179-266">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="f6179-267">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6179-267">**Name**</span></span>|<span data-ttu-id="f6179-268">**Type**</span><span class="sxs-lookup"><span data-stu-id="f6179-268">**Type**</span></span>|<span data-ttu-id="f6179-269">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f6179-269">**Value**</span></span>|<span data-ttu-id="f6179-270">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f6179-270">**Comment**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f6179-271">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="f6179-271">_sip._tls</span></span>  <br/> |<span data-ttu-id="f6179-272">SRV</span><span class="sxs-lookup"><span data-stu-id="f6179-272">SRV</span></span>  <br/> |<span data-ttu-id="f6179-273">100 1 443</span><span class="sxs-lookup"><span data-stu-id="f6179-273">100 1 443</span></span>  <br/> <span data-ttu-id="f6179-274">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-274">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="f6179-275">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-275">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-276">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-276">(This field is optional.)</span></span>  <br/> |
    |<span data-ttu-id="f6179-277">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="f6179-277">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="f6179-278">SRV</span><span class="sxs-lookup"><span data-stu-id="f6179-278">SRV</span></span>  <br/> |<span data-ttu-id="f6179-279">100 1 5061</span><span class="sxs-lookup"><span data-stu-id="f6179-279">100 1 5061</span></span>  <br/> <span data-ttu-id="f6179-280">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f6179-280">sipfed.online.lync.com.</span></span>  <br/> <span data-ttu-id="f6179-281">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f6179-281">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="f6179-282">(Ce champ est facultatif.)</span><span class="sxs-lookup"><span data-stu-id="f6179-282">(This field is optional.)</span></span>  <br/> |
   
    ![Dreamhost-BP-configure-5-1](../media/934eb79f-3617-4b72-802c-c42c7d165283.png)
  
5. <span data-ttu-id="f6179-284">Sélectionnez **Ajouter un enregistrement maintenant**.</span><span class="sxs-lookup"><span data-stu-id="f6179-284">Select **Add Record Now!**.</span></span>
    
    ![Dreamhost-BP-configure-5-2](../media/015bc73c-8f88-49ce-87f9-e5a6ea3e10a8.png)
  
6. <span data-ttu-id="f6179-286">À l’aide des deux étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f6179-286">Using the preceding two steps and the values from the second row in the table, add the other SRV record.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="f6179-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f6179-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
