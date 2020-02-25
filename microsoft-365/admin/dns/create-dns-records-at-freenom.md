---
title: Créer des enregistrements DNS sur Freenom pour Office 365
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
ms.assetid: d8ff45a2-19e3-413d-aa64-a9982bd6633c
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Freenom pour Office 365.
ms.openlocfilehash: a1396964c7dc9c279589a6020e0c741fd0cb29d5
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42244771"
---
# <a name="create-dns-records-at-freenom-for-office-365"></a><span data-ttu-id="7fcbf-103">Créer des enregistrements DNS sur Freenom pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7fcbf-103">Create DNS records at Freenom for Office 365</span></span>

<span data-ttu-id="7fcbf-104">[Consultez le Forum aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-104">[Check the Domains FAQ ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="7fcbf-105">Le site Web Freenom ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype entreprise Online et d’Outlook Web App ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-105">The Freenom website doesn't support SRV records, which means that several Skype for Business Online and Outlook Web App features won't work.</span></span> <span data-ttu-id="7fcbf-106">Quelle que soit la planification d’Office 365 que vous utilisez, il existe des limitations de service importantes, et vous pouvez choisir d’utiliser un autre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-106">No matter which Office 365 plan you use, there are significant service limitations, and you may want to switch to a different DNS hosting provider.</span></span> 
  
<span data-ttu-id="7fcbf-107">Si malgré les limitations de service, vous choisissez de gérer vos propres enregistrements DNS Office 365 sur Freenom, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour la messagerie et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-107">If despite the service limitations, you choose to manage your own Office 365 DNS records at Freenom, follow the steps in this article to verify your domain and set up DNS records for email and other services.</span></span>
  
<span data-ttu-id="7fcbf-108">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-108">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="7fcbf-p102">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-p102">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="7fcbf-112">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="7fcbf-112">Add a TXT record for verification</span></span>
<span data-ttu-id="7fcbf-113"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="7fcbf-113"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="7fcbf-p103">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-p103">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7fcbf-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="7fcbf-118">Pour commencer, accédez à la page de vos domaines dans Freenom à l’aide de [ce lien](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-118">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="7fcbf-119">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-119">You'll be prompted to log in.</span></span>
    
    ![Connexion Freenom](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="7fcbf-121">Sélectionnez **services**, puis **My Domains**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-121">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom sélectionner les services et mes domaines](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="7fcbf-123">Pour le domaine que vous souhaitez modifier, sélectionnez **Manage Domain (gérer le domaine**).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-123">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom sélectionnez Manage Domain (gérer le domaine)](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="7fcbf-125">Sélectionnez **gérer le DNS Freenom**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-125">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom gérer le DNS Freenom](../media/9854a511-27e3-4658-8903-34b3d425096d.png)
  
5. <span data-ttu-id="7fcbf-127">Sous **Ajouter un enregistrement**, dans la colonne **type** , choisissez **txt** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-127">Under **Add Record**, in the **Type** column, choose **TXT** from the menu.</span></span> 
    
    ![Freenom ajouter un type d’enregistrement TXT](../media/7f0e85e7-844f-4962-815e-5d80d9e6efa0.png)
  
6. <span data-ttu-id="7fcbf-129">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-129">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="7fcbf-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-130">**Name**</span></span>|<span data-ttu-id="7fcbf-131">**Type**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-131">**Type**</span></span>|<span data-ttu-id="7fcbf-132">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-132">**TTL**</span></span>|<span data-ttu-id="7fcbf-133">**Target**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-133">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7fcbf-134">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-134">(leave blank)</span></span>  <br/> |<span data-ttu-id="7fcbf-135">TXT</span><span class="sxs-lookup"><span data-stu-id="7fcbf-135">TXT</span></span>  <br/> |<span data-ttu-id="7fcbf-136">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-136">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-137">MS = msXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="7fcbf-137">MS=msXXXXXXXX</span></span>  <br/> <span data-ttu-id="7fcbf-138">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-138">**Note:** This is an example.</span></span> <span data-ttu-id="7fcbf-139">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-139">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="7fcbf-140">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="7fcbf-140">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Valeurs TXT Freenom pour la vérification](../media/650098df-b3aa-47e5-9763-7fde24e34c3f.png)
  
7. <span data-ttu-id="7fcbf-142">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-142">Select **Save Changes**.</span></span>
    
    ![Enregistrement TXT Freenom enregistrer les modifications](../media/b1a63f9a-4578-491a-9554-c40f73b37e09.png)
  
8. <span data-ttu-id="7fcbf-144">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-144">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="7fcbf-145">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-145">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="7fcbf-146">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-146">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="7fcbf-147">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="7fcbf-147">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="7fcbf-148">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-148">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="7fcbf-149">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-149">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="7fcbf-150">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-150">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="7fcbf-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="7fcbf-154">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="7fcbf-154">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="7fcbf-155"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="7fcbf-155"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="7fcbf-156">Pour commencer, accédez à la page de vos domaines dans Freenom à l’aide de [ce lien](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-156">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="7fcbf-157">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-157">You'll be prompted to log in.</span></span>
    
    ![Connexion Freenom](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="7fcbf-159">Sélectionnez **services**, puis **My Domains**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-159">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom sélectionner les services et mes domaines](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="7fcbf-161">Pour le domaine que vous souhaitez modifier, sélectionnez **Manage Domain (gérer le domaine**).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-161">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom sélectionnez Manage Domain (gérer le domaine)](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="7fcbf-163">Définissez le nom pour votre domaine sur les serveurs de noms Freenom par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-163">Set the name serves for your domain to the default Freenom name servers.</span></span> <span data-ttu-id="7fcbf-164">Sélectionnez **outils de gestion**, puis serveurs de **noms**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-164">Select **Management Tools**, and then select **Nameservers**.</span></span>
    
    ![Paramètre de serveur de noms Freenom](../media/a6ae877a-c248-42b9-bae9-210a80cd01e7.png)
  
5. <span data-ttu-id="7fcbf-166">Assurez-vous que l’option utiliser les serveurs de **noms par défaut** est sélectionnée, puis sélectionnez Modifier les serveurs de **noms**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-166">Make sure **Use default nameservers** is selected, and then select **Change Nameservers**.</span></span>
    
    ![Modifier les serveurs de noms Freenom](../media/0ef90d84-c0a0-4ef9-9e4c-43ef0aac3a2e.png)
  
6. <span data-ttu-id="7fcbf-168">Sélectionnez **gérer le DNS Freenom**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-168">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom sélectionnez Manage Freenom DNS](../media/f55a8053-2411-45da-a357-776c6699f721.png)
  
7. <span data-ttu-id="7fcbf-170">Sous **Ajouter un enregistrement**, dans la colonne **type** , choisissez **MX** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-170">Under **Add Record**, in the **Type** column, choose **MX** from the menu.</span></span> 
    
    ![Freenom ajouter un type d’enregistrement MX](../media/c728c6ee-786c-4f6a-8ad5-1d9914a5bfcf.png)
  
8. <span data-ttu-id="7fcbf-172">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-172">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    |<span data-ttu-id="7fcbf-173">**Name**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-173">**Name**</span></span>|<span data-ttu-id="7fcbf-174">**Type**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-174">**Type**</span></span>|<span data-ttu-id="7fcbf-175">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-175">**TTL**</span></span>|<span data-ttu-id="7fcbf-176">**Target**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-176">**Target**</span></span>|<span data-ttu-id="7fcbf-177">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-177">**Priority**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7fcbf-178">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-178">(leave blank)</span></span>  <br/> |<span data-ttu-id="7fcbf-179">MX (Mail Exchanger) (MX - Serveur de courrier)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-179">MX (Mail Exchanger)</span></span>  <br/> |<span data-ttu-id="7fcbf-180">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-180">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-181">\<Key\>. mail.protection.Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7fcbf-181">\<domain-key\>.mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="7fcbf-182">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-182">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>   [<span data-ttu-id="7fcbf-183">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="7fcbf-183">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="7fcbf-184">10 </span><span class="sxs-lookup"><span data-stu-id="7fcbf-184">10</span></span>  <br/> <span data-ttu-id="7fcbf-185">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/17d415c1-067e-4974-84d5-aaeaf3a0c0a9).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-185">For more information about priority, see [What is MX priority?](https://support.office.com/article/17d415c1-067e-4974-84d5-aaeaf3a0c0a9)</span></span> <br/> |
   
   ![Enregistrement MX Freenom](../media/8896c4a9-b3dd-45ed-9916-f7da2715ba8c.png)
  
9. <span data-ttu-id="7fcbf-187">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-187">Select **Save Changes**.</span></span>
    
    ![Enregistrement MX Freenom enregistrer les modifications](../media/7aa0a464-d136-417f-be40-48d3f728eeb7.png)
  
10. <span data-ttu-id="7fcbf-189">S’il existe d’autres enregistrements MX, supprimez-les tous.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-189">If there are any other MX records, delete them all.</span></span> <span data-ttu-id="7fcbf-190">Pour chaque enregistrement, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-190">For each record, select **Delete**.</span></span> <span data-ttu-id="7fcbf-191">Lorsque le message voulez **-vous vraiment supprimer cette entrée ?** s’affiche, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-191">When the message **Do you really want to remove this entry?** appears, select **OK**.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="7fcbf-192">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7fcbf-192">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="7fcbf-193"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="7fcbf-193"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="7fcbf-194">Pour commencer, accédez à la page de vos domaines dans Freenom à l’aide de [ce lien](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-194">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="7fcbf-195">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-195">You'll be prompted to log in.</span></span>
    
    ![Connexion Freenom](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="7fcbf-197">Sélectionnez **services**, puis **My Domains**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-197">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom sélectionner les services et mes domaines](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="7fcbf-199">Pour le domaine que vous souhaitez modifier, sélectionnez **Manage Domain (gérer le domaine**).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-199">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom sélectionnez Manage Domain (gérer le domaine)](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="7fcbf-201">Sélectionnez **gérer le DNS Freenom**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-201">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom sélectionnez Manage Freenom DNS](../media/5e7bc3a7-0d5e-431b-bb27-da3b0f316d01.png)
  
5. <span data-ttu-id="7fcbf-203">Sous **Ajouter un enregistrement**, dans la colonne **type** , choisissez **CNAME** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-203">Under **Add Record**, in the **Type** column, choose **CNAME** from the menu.</span></span> 
    
    ![Freenom ajouter un type d’enregistrement CNAMe](../media/9b204755-ca2a-46d2-bce2-030d82fd1f9e.png)
  
6. <span data-ttu-id="7fcbf-205">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-205">Create the first CNAME record.</span></span> <span data-ttu-id="7fcbf-206">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-206">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    |<span data-ttu-id="7fcbf-207">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-207">**Name**</span></span>|<span data-ttu-id="7fcbf-208">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-208">**Record type**</span></span>|<span data-ttu-id="7fcbf-209">**TTL**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-209">**TTL**</span></span>|<span data-ttu-id="7fcbf-210">**Target**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-210">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7fcbf-211">autodiscover</span><span class="sxs-lookup"><span data-stu-id="7fcbf-211">autodiscover</span></span>  <br/> |<span data-ttu-id="7fcbf-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="7fcbf-212">CNAME</span></span>  <br/> |<span data-ttu-id="7fcbf-213">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-213">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-214">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="7fcbf-214">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="7fcbf-215">sip</span><span class="sxs-lookup"><span data-stu-id="7fcbf-215">sip</span></span>  <br/> |<span data-ttu-id="7fcbf-216">CNAME</span><span class="sxs-lookup"><span data-stu-id="7fcbf-216">CNAME</span></span>  <br/> |<span data-ttu-id="7fcbf-217">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-217">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-218">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7fcbf-218">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="7fcbf-219">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="7fcbf-219">lyncdiscover</span></span>  <br/> |<span data-ttu-id="7fcbf-220">CNAME</span><span class="sxs-lookup"><span data-stu-id="7fcbf-220">CNAME</span></span>  <br/> |<span data-ttu-id="7fcbf-221">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-221">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-222">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="7fcbf-222">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="7fcbf-223">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="7fcbf-223">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="7fcbf-224">CNAME</span><span class="sxs-lookup"><span data-stu-id="7fcbf-224">CNAME</span></span>  <br/> |<span data-ttu-id="7fcbf-225">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-225">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-226">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="7fcbf-226">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="7fcbf-227">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="7fcbf-227">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="7fcbf-228">CNAME</span><span class="sxs-lookup"><span data-stu-id="7fcbf-228">CNAME</span></span>  <br/> |<span data-ttu-id="7fcbf-229">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-229">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-230">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7fcbf-230">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Valeurs CNAMe Freenom](../media/752fc682-e3f2-4b9c-9253-bf1ba2d414e9.png)
  
7. <span data-ttu-id="7fcbf-232">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-232">Select **Save Changes**.</span></span>
    
    ![Freenom CNAMe enregistrer les modifications](../media/68103fd2-0f5f-4aac-a875-25157c6bbdd2.png)
  
8. <span data-ttu-id="7fcbf-234">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-234">Repeat the previous steps to create the other five CNAME records.</span></span> 
    
    <span data-ttu-id="7fcbf-235">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-235">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="7fcbf-236">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="7fcbf-236">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="7fcbf-237"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="7fcbf-237"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fcbf-238">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-238">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="7fcbf-239">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-239">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="7fcbf-240">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-240">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="7fcbf-241">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-241">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 

1. <span data-ttu-id="7fcbf-242">Pour commencer, accédez à la page de vos domaines dans Freenom à l’aide de [ce lien](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-242">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="7fcbf-243">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-243">You'll be prompted to log in.</span></span>
    
    ![Connexion Freenom](../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="7fcbf-245">Sélectionnez **services**, puis **My Domains**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-245">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom sélectionner les services et mes domaines](../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="7fcbf-247">Pour le domaine que vous souhaitez modifier, sélectionnez **Manage Domain (gérer le domaine**).</span><span class="sxs-lookup"><span data-stu-id="7fcbf-247">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom sélectionnez Manage Domain (gérer le domaine)](../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="7fcbf-249">Sélectionnez **gérer le DNS Freenom**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-249">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom sélectionnez Manage Freenom DNS](../media/94809955-0315-409c-a15d-703a2fe4c4ed.png)
  
5. <span data-ttu-id="7fcbf-251">Sous **Ajouter un enregistrement**, dans la colonne **type** , choisissez **txt** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-251">Under **Add Record**, in the **Type** column, choose **TXT** from the menu.</span></span> 
    
    ![Freenom ajouter un type d’enregistrement TXT](../media/d8854285-c4ae-416c-a072-72a11ba1cd9a.png)
  
6. <span data-ttu-id="7fcbf-253">In the boxes for the new record, type or copy and paste the following values.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-253">In the boxes for the new record, type or copy and paste the following values.</span></span> 
    
    |<span data-ttu-id="7fcbf-254">**Name**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-254">**Name**</span></span>|<span data-ttu-id="7fcbf-255">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-255">**Record type**</span></span>|<span data-ttu-id="7fcbf-256">**TTL**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-256">**TTL**</span></span>|<span data-ttu-id="7fcbf-257">**Target**</span><span class="sxs-lookup"><span data-stu-id="7fcbf-257">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="7fcbf-258">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-258">(leave blank)</span></span>  <br/> |<span data-ttu-id="7fcbf-259">TXT</span><span class="sxs-lookup"><span data-stu-id="7fcbf-259">TXT</span></span>  <br/> |<span data-ttu-id="7fcbf-260">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="7fcbf-260">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="7fcbf-261">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="7fcbf-261">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="7fcbf-262">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-262">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Valeurs TXT Freenom pour SPF](../media/1b3b1199-9104-4ca1-acdb-786d139c21ac.png)
  
7. <span data-ttu-id="7fcbf-264">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="7fcbf-264">Select **Save Changes**.</span></span>
    
    ![Enregistrement TXT Freenom pour les modifications d’enregistrement SPF](../media/e2fc52b1-0dcb-4595-9a4c-fca5e2ef9f97.png)
  

