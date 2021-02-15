---
title: Créer des enregistrements DNS sur Freenom pour Microsoft
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
ms.assetid: d8ff45a2-19e3-413d-aa64-a9982bd6633c
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur Freenom pour Microsoft.
ms.openlocfilehash: b958a69d1dad9a0b56cf954d12cd42e40d6d4fea
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657874"
---
# <a name="create-dns-records-at-freenom-for-microsoft"></a><span data-ttu-id="4f3c3-103">Créer des enregistrements DNS sur Freenom pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="4f3c3-103">Create DNS records at Freenom for Microsoft</span></span>

<span data-ttu-id="4f3c3-104">[Consultez la FAQ sur ](../setup/domains-faq.yml) les domaines si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-104">[Check the Domains FAQ ](../setup/domains-faq.yml) if you don't find what you're looking for.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="4f3c3-105">Le site web Freenom ne prend pas en charge les enregistrements SRV, ce qui signifie que plusieurs fonctionnalités de Skype Entreprise Online et d’Outlook Web App ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-105">The Freenom website doesn't support SRV records, which means that several Skype for Business Online and Outlook Web App features won't work.</span></span> <span data-ttu-id="4f3c3-106">Quelle que soit l’offre Microsoft que vous utilisez, il existe des limitations de service importantes et vous pouvez basculer vers un autre fournisseur d’hébergement DNS.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-106">No matter which Microsoft plan you use, there are significant service limitations, and you may want to switch to a different DNS hosting provider.</span></span> 
  
<span data-ttu-id="4f3c3-107">Si, malgré les limitations de service, vous choisissez de gérer vos propres enregistrements DNS Microsoft sur Freenom, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique et d’autres services.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-107">If despite the service limitations, you choose to manage your own Microsoft DNS records at Freenom, follow the steps in this article to verify your domain and set up DNS records for email and other services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="4f3c3-p102">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-p102">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="4f3c3-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="4f3c3-111">Add a TXT record for verification</span></span>
<span data-ttu-id="4f3c3-112"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="4f3c3-112"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="4f3c3-p103">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-p103">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f3c3-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="4f3c3-117">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-117">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="4f3c3-118">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-118">You'll be prompted to log in.</span></span>
    
    ![Connexion freenom](../../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="4f3c3-120">Sélectionnez **Services,** puis **Mes domaines.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-120">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom select Services and My Domains](../../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="4f3c3-122">Pour le domaine à modifier, sélectionnez **Gérer le domaine.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-122">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom select Manage Domain](../../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="4f3c3-124">Select **Manage Freenom DNS**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-124">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom Manage Freenom DNS](../../media/9854a511-27e3-4658-8903-34b3d425096d.png)
  
5. <span data-ttu-id="4f3c3-126">Sous **Ajouter un enregistrement,** dans la colonne **Type,** choisissez **TXT** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-126">Under **Add Record**, in the **Type** column, choose **TXT** from the menu.</span></span> 
    
    ![Freenom Add Record type TXT](../../media/7f0e85e7-844f-4962-815e-5d80d9e6efa0.png)
  
6. <span data-ttu-id="4f3c3-128">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-128">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="4f3c3-129">**Name**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-129">**Name**</span></span>|<span data-ttu-id="4f3c3-130">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-130">**Type**</span></span>|<span data-ttu-id="4f3c3-131">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-131">**TTL**</span></span>|<span data-ttu-id="4f3c3-132">**Target**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-132">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="4f3c3-133">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-133">(leave blank)</span></span>  <br/> |<span data-ttu-id="4f3c3-134">TXT</span><span class="sxs-lookup"><span data-stu-id="4f3c3-134">TXT</span></span>  <br/> |<span data-ttu-id="4f3c3-135">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-135">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-136">MS=msXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="4f3c3-136">MS=msXXXXXXXX</span></span>  <br/> <span data-ttu-id="4f3c3-137">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-137">**Note:** This is an example.</span></span> <span data-ttu-id="4f3c3-138">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-138">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="4f3c3-139">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="4f3c3-139">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Freenom TXT values for verification](../../media/650098df-b3aa-47e5-9763-7fde24e34c3f.png)
  
7. <span data-ttu-id="4f3c3-141">Sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-141">Select **Save Changes**.</span></span>
    
    ![Freenom TXT record Save Changes](../../media/b1a63f9a-4578-491a-9554-c40f73b37e09.png)
  
8. <span data-ttu-id="4f3c3-143">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-143">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="4f3c3-144">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-144">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="4f3c3-145">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-145">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="4f3c3-146">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-146">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="4f3c3-147">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-147">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="4f3c3-148">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-148">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="4f3c3-149">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-149">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="4f3c3-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="4f3c3-153">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="4f3c3-153">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="4f3c3-154"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="4f3c3-154"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="4f3c3-155">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-155">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="4f3c3-156">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-156">You'll be prompted to log in.</span></span>
    
    ![Connexion freenom](../../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="4f3c3-158">Sélectionnez **Services,** puis **Mes domaines.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-158">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom select Services and My Domains](../../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="4f3c3-160">Pour le domaine à modifier, sélectionnez **Gérer le domaine.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-160">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom select Manage Domain](../../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="4f3c3-162">Définissez le nom de votre domaine sur les serveurs de noms freenom par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-162">Set the name serves for your domain to the default Freenom name servers.</span></span> <span data-ttu-id="4f3c3-163">Sélectionnez **Outils de** gestion, puis serveurs **de noms.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-163">Select **Management Tools**, and then select **Nameservers**.</span></span>
    
    ![Paramètre Freenom Nameservers](../../media/a6ae877a-c248-42b9-bae9-210a80cd01e7.png)
  
5. <span data-ttu-id="4f3c3-165">**Assurez-vous que l’option** Utiliser les serveurs de noms par défaut est sélectionnée, puis sélectionnez **Modifier les serveurs de noms.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-165">Make sure **Use default nameservers** is selected, and then select **Change Nameservers**.</span></span>
    
    ![Freenom Change Nameservers](../../media/0ef90d84-c0a0-4ef9-9e4c-43ef0aac3a2e.png)
  
6. <span data-ttu-id="4f3c3-167">Select **Manage Freenom DNS**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-167">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom select Manage Freenom DNS](../../media/f55a8053-2411-45da-a357-776c6699f721.png)
  
7. <span data-ttu-id="4f3c3-169">Sous **Ajouter un enregistrement,** dans la colonne **Type,** choisissez **MX** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-169">Under **Add Record**, in the **Type** column, choose **MX** from the menu.</span></span> 
    
    ![Freenom Add Record type MX](../../media/c728c6ee-786c-4f6a-8ad5-1d9914a5bfcf.png)
  
8. <span data-ttu-id="4f3c3-171">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-171">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    |<span data-ttu-id="4f3c3-172">**Name**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-172">**Name**</span></span>|<span data-ttu-id="4f3c3-173">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-173">**Type**</span></span>|<span data-ttu-id="4f3c3-174">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-174">**TTL**</span></span>|<span data-ttu-id="4f3c3-175">**Target**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-175">**Target**</span></span>|<span data-ttu-id="4f3c3-176">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-176">**Priority**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="4f3c3-177">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-177">(leave blank)</span></span>  <br/> |<span data-ttu-id="4f3c3-178">MX (Mail Exchanger) (MX - Serveur de courrier)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-178">MX (Mail Exchanger)</span></span>  <br/> |<span data-ttu-id="4f3c3-179">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-179">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-180">\<domain-key\>.mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="4f3c3-180">\<domain-key\>.mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="4f3c3-181">**Remarque :** Obtenez votre  *\<domain-key\>*  compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-181">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>   [<span data-ttu-id="4f3c3-182">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="4f3c3-182">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="4f3c3-183">10 </span><span class="sxs-lookup"><span data-stu-id="4f3c3-183">10</span></span>  <br/> <span data-ttu-id="4f3c3-184">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-184">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |
   
   ![Enregistrement MX Freenom](../../media/8896c4a9-b3dd-45ed-9916-f7da2715ba8c.png)
  
9. <span data-ttu-id="4f3c3-186">Sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-186">Select **Save Changes**.</span></span>
    
    ![Freenom MX record Save Changes](../../media/7aa0a464-d136-417f-be40-48d3f728eeb7.png)
  
10. <span data-ttu-id="4f3c3-188">S’il existe d’autres enregistrements MX, supprimez-les tous.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-188">If there are any other MX records, delete them all.</span></span> <span data-ttu-id="4f3c3-189">Pour chaque enregistrement, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-189">For each record, select **Delete**.</span></span> <span data-ttu-id="4f3c3-190">Lorsque le message **Voulez-vous vraiment supprimer cette entrée ?** s’affiche, sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-190">When the message **Do you really want to remove this entry?** appears, select **OK**.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="4f3c3-191">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="4f3c3-191">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="4f3c3-192"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="4f3c3-192"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="4f3c3-193">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-193">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="4f3c3-194">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-194">You'll be prompted to log in.</span></span>
    
    ![Connexion freenom](../../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="4f3c3-196">Sélectionnez **Services,** puis **Mes domaines.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-196">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom select Services and My Domains](../../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="4f3c3-198">Pour le domaine à modifier, sélectionnez **Gérer le domaine.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-198">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom select Manage Domain](../../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="4f3c3-200">Select **Manage Freenom DNS**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-200">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom select Manage Freenom DNS](../../media/5e7bc3a7-0d5e-431b-bb27-da3b0f316d01.png)
  
5. <span data-ttu-id="4f3c3-202">Sous **Ajouter un enregistrement,** dans la colonne **Type,** choisissez **CNAME** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-202">Under **Add Record**, in the **Type** column, choose **CNAME** from the menu.</span></span> 
    
    ![Freenom Add Record type CNAME](../../media/9b204755-ca2a-46d2-bce2-030d82fd1f9e.png)
  
6. <span data-ttu-id="4f3c3-204">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-204">Create the first CNAME record.</span></span> <span data-ttu-id="4f3c3-205">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-205">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    |<span data-ttu-id="4f3c3-206">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-206">**Name**</span></span>|<span data-ttu-id="4f3c3-207">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-207">**Record type**</span></span>|<span data-ttu-id="4f3c3-208">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-208">**TTL**</span></span>|<span data-ttu-id="4f3c3-209">**Target**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-209">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="4f3c3-210">autodiscover</span><span class="sxs-lookup"><span data-stu-id="4f3c3-210">autodiscover</span></span>  <br/> |<span data-ttu-id="4f3c3-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="4f3c3-211">CNAME</span></span>  <br/> |<span data-ttu-id="4f3c3-212">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-212">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-213">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="4f3c3-213">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="4f3c3-214">sip</span><span class="sxs-lookup"><span data-stu-id="4f3c3-214">sip</span></span>  <br/> |<span data-ttu-id="4f3c3-215">CNAME</span><span class="sxs-lookup"><span data-stu-id="4f3c3-215">CNAME</span></span>  <br/> |<span data-ttu-id="4f3c3-216">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-216">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-217">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="4f3c3-217">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="4f3c3-218">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="4f3c3-218">lyncdiscover</span></span>  <br/> |<span data-ttu-id="4f3c3-219">CNAME</span><span class="sxs-lookup"><span data-stu-id="4f3c3-219">CNAME</span></span>  <br/> |<span data-ttu-id="4f3c3-220">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-220">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-221">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="4f3c3-221">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="4f3c3-222">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="4f3c3-222">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="4f3c3-223">CNAME</span><span class="sxs-lookup"><span data-stu-id="4f3c3-223">CNAME</span></span>  <br/> |<span data-ttu-id="4f3c3-224">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-224">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-225">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="4f3c3-225">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="4f3c3-226">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="4f3c3-226">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="4f3c3-227">CNAME</span><span class="sxs-lookup"><span data-stu-id="4f3c3-227">CNAME</span></span>  <br/> |<span data-ttu-id="4f3c3-228">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-228">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-229">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="4f3c3-229">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Freenom CNAME values](../../media/752fc682-e3f2-4b9c-9253-bf1ba2d414e9.png)
  
7. <span data-ttu-id="4f3c3-231">Sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-231">Select **Save Changes**.</span></span>
    
    ![Freenom CNAME Save Changes](../../media/68103fd2-0f5f-4aac-a875-25157c6bbdd2.png)
  
8. <span data-ttu-id="4f3c3-233">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-233">Repeat the previous steps to create the other five CNAME records.</span></span> 
    
    <span data-ttu-id="4f3c3-234">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-234">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="4f3c3-235">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="4f3c3-235">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="4f3c3-236"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="4f3c3-236"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f3c3-237">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-237">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="4f3c3-238">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-238">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="4f3c3-239">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-239">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="4f3c3-240">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de n’avoir qu’un seul  *enregistrement*  SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-240">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 

1. <span data-ttu-id="4f3c3-241">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span><span class="sxs-lookup"><span data-stu-id="4f3c3-241">To get started, go to your domains page in Freenom by using [this link](https://my.freenom.com/).</span></span> <span data-ttu-id="4f3c3-242">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-242">You'll be prompted to log in.</span></span>
    
    ![Connexion freenom](../../media/90a32855-bfdd-4dfe-881c-b9a36b2f0582.png)
  
2. <span data-ttu-id="4f3c3-244">Sélectionnez **Services,** puis **Mes domaines.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-244">Select **Services**, and then select **My Domains**.</span></span>
    
    ![Freenom select Services and My Domains](../../media/1917ced2-e254-4aec-9096-46d339b84d9a.png)
  
3. <span data-ttu-id="4f3c3-246">Pour le domaine à modifier, sélectionnez **Gérer le domaine.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-246">For the domain that you want to edit, select **Manage Domain**.</span></span>
    
    ![Freenom select Manage Domain](../../media/67737b71-8b1b-42a6-abaf-62d776d3eb87.png)
  
4. <span data-ttu-id="4f3c3-248">Select **Manage Freenom DNS**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-248">Select **Manage Freenom DNS**.</span></span>
    
    ![Freenom select Manage Freenom DNS](../../media/94809955-0315-409c-a15d-703a2fe4c4ed.png)
  
5. <span data-ttu-id="4f3c3-250">Sous **Ajouter un enregistrement,** dans la colonne **Type,** choisissez **TXT** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-250">Under **Add Record**, in the **Type** column, choose **TXT** from the menu.</span></span> 
    
    ![Freenom Add Record type TXT](../../media/d8854285-c4ae-416c-a072-72a11ba1cd9a.png)
  
6. <span data-ttu-id="4f3c3-252">In the boxes for the new record, type or copy and paste the following values.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-252">In the boxes for the new record, type or copy and paste the following values.</span></span> 
    
    |<span data-ttu-id="4f3c3-253">**Name**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-253">**Name**</span></span>|<span data-ttu-id="4f3c3-254">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-254">**Record type**</span></span>|<span data-ttu-id="4f3c3-255">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-255">**TTL**</span></span>|<span data-ttu-id="4f3c3-256">**Target**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-256">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="4f3c3-257">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-257">(leave blank)</span></span>  <br/> |<span data-ttu-id="4f3c3-258">TXT</span><span class="sxs-lookup"><span data-stu-id="4f3c3-258">TXT</span></span>  <br/> |<span data-ttu-id="4f3c3-259">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="4f3c3-259">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="4f3c3-260">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="4f3c3-260">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="4f3c3-261">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-261">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Freenom TXT values for SPF](../../media/1b3b1199-9104-4ca1-acdb-786d139c21ac.png)
  
7. <span data-ttu-id="4f3c3-263">Sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-263">Select **Save Changes**.</span></span>
    
    ![Enregistrement TXT freenom pour les modifications d’enregistrement SPF](../../media/e2fc52b1-0dcb-4595-9a4c-fca5e2ef9f97.png)
  

