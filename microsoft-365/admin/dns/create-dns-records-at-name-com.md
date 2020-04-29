---
title: Créer des enregistrements DNS sur name.com pour Microsoft
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
ms.assetid: 9ddcc2fc-9433-4335-8192-6ffb1f541087
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur name.com pour Microsoft.
ms.openlocfilehash: 9183d27641ee22d9e49be2ca04832ab68bc20ace
ms.sourcegitcommit: 2399ee6f9bc955cf8f2a76c01fc84c19eb37ff42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2020
ms.locfileid: "43919735"
---
# <a name="create-dns-records-at-namecom-for-microsoft"></a><span data-ttu-id="1b863-103">Créer des enregistrements DNS sur name.com pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="1b863-103">Create DNS records at name.com for Microsoft</span></span>

 <span data-ttu-id="1b863-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="1b863-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="1b863-105">Si name.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="1b863-105">If name.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="1b863-106">Une fois ces enregistrements ajoutés sur name.com, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1b863-106">After you add these records at name.com, your domain will be set up to work with Microsoft services.</span></span>
  
<span data-ttu-id="1b863-107">Si vous souhaitez en savoir plus sur l’hébergement web et le DNS pour les sites web avec Microsoft, consultez la page [Utiliser un site web public avec Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="1b863-107">To learn about webhosting and DNS for websites with Microsoft, see [Use a public website with Microsoft](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b863-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1b863-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="1b863-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="1b863-111">Add a TXT record for verification</span></span>
<span data-ttu-id="1b863-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="1b863-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="1b863-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="1b863-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b863-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="1b863-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="1b863-p104">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1b863-p104">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="1b863-120">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b863-120">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="1b863-122">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="1b863-122">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="1b863-124">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b863-124">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="1b863-125">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="1b863-125">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="1b863-126">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="1b863-126">**Type**</span></span> <br/> |<span data-ttu-id="1b863-127">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="1b863-127">**Host**</span></span> <br/> |<span data-ttu-id="1b863-128">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="1b863-128">**Answer**</span></span> <br/> |<span data-ttu-id="1b863-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1b863-129">**TTL**</span></span> <br/> |
    |<span data-ttu-id="1b863-130">TXT</span><span class="sxs-lookup"><span data-stu-id="1b863-130">TXT</span></span>  <br/> |<span data-ttu-id="1b863-131">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="1b863-131">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="1b863-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="1b863-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="1b863-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="1b863-133">**Note:** This is an example.</span></span> <span data-ttu-id="1b863-134">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="1b863-134">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="1b863-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="1b863-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="1b863-136">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-136">Use the default value (300).</span></span>  <br/> |
   
    ![Nom-BP-Verify-1-1](../../media/0c352fd3-cf84-439f-a481-0705e225cc54.png)
  
5. <span data-ttu-id="1b863-138">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1b863-138">Select **Add Record**.</span></span>
    
    ![Name-BP-Verify-1-2](../../media/816fc60b-17ab-4982-8849-6c3fcf3ca3d6.png)
  
6. <span data-ttu-id="1b863-140">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="1b863-140">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="1b863-141">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1b863-141">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="1b863-142">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="1b863-142">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="1b863-143">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="1b863-143">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="1b863-144">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="1b863-144">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="1b863-145">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="1b863-145">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="1b863-146">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="1b863-146">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
> <span data-ttu-id="1b863-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1b863-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="1b863-150">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="1b863-150">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="1b863-151"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="1b863-151"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="1b863-p107">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1b863-p107">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="1b863-155">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b863-155">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="1b863-157">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="1b863-157">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="1b863-159">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b863-159">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="1b863-160">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="1b863-160">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="1b863-161">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="1b863-161">**Type**</span></span>|<span data-ttu-id="1b863-162">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="1b863-162">**Host**</span></span>|<span data-ttu-id="1b863-163">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="1b863-163">**Answer**</span></span>|<span data-ttu-id="1b863-164">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="1b863-164">**TTL**</span></span>|<span data-ttu-id="1b863-165">**Prio (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="1b863-165">**Prio**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="1b863-166">MX</span><span class="sxs-lookup"><span data-stu-id="1b863-166">MX</span></span>  <br/> |<span data-ttu-id="1b863-167">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="1b863-167">(Leave this field empty.)</span></span>  <br/> | <span data-ttu-id="1b863-168">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="1b863-168">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="1b863-169">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1b863-169">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="1b863-170">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="1b863-170">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="1b863-171">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-171">Use the default value (300).</span></span>  <br/> |<span data-ttu-id="1b863-172">0</span><span class="sxs-lookup"><span data-stu-id="1b863-172">0</span></span>  <br/> <span data-ttu-id="1b863-173">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="1b863-173">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
   
   ![Nom-BP-configure-2-1](../../media/11ba2160-fc8e-4196-bb15-2b7c6d49c8fc.png)
  
5. <span data-ttu-id="1b863-175">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1b863-175">Select **Add Record**.</span></span>
    
    ![Name-BP-Configuration-2-2](../../media/fd09f161-7cc4-4723-aec2-5fa801bd19e9.png)
  
6. <span data-ttu-id="1b863-177">S'il existe d'autres enregistrements MX, supprimez chacun d'eux à l'aide de la procédure en deux étapes suivante :</span><span class="sxs-lookup"><span data-stu-id="1b863-177">If there are any other MX records, delete each of them by using the following two-step procedure:</span></span>
    
    <span data-ttu-id="1b863-178">Pour chaque autre enregistrement MX, sélectionnez **supprimer** dans la colonne **actions** .</span><span class="sxs-lookup"><span data-stu-id="1b863-178">For each other MX record, select **Delete** in the **Actions** column.</span></span> 
    
    ![Name-BP-Configuration-2-3](../../media/16734a98-31c4-4023-a2a5-10b7c95bc58e.png)
  
    <span data-ttu-id="1b863-180">Pour confirmer chaque suppression, sélectionnez **supprimer** dans la colonne **actions** .</span><span class="sxs-lookup"><span data-stu-id="1b863-180">To confirm each deletion, select **Delete** in the **Actions** column again.</span></span> 
    
    ![Name-BP-Configure-2-4](../../media/409c21c5-51f4-4244-bb84-5d32084224b2.png)
  
    <span data-ttu-id="1b863-182">Répétez cette procédure en deux étapes jusqu'à avoir supprimé tous les autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="1b863-182">Repeat this two-step procedure until you have deleted each of the other MX records.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="1b863-183">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="1b863-183">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="1b863-184"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="1b863-184"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="1b863-p109">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1b863-p109">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="1b863-188">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b863-188">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="1b863-190">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="1b863-190">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="1b863-192">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="1b863-192">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="1b863-193">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b863-193">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="1b863-194">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="1b863-194">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="1b863-195">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="1b863-195">**Type**</span></span>|<span data-ttu-id="1b863-196">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="1b863-196">**Host**</span></span>|<span data-ttu-id="1b863-197">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="1b863-197">**Answer**</span></span>|<span data-ttu-id="1b863-198">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="1b863-198">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="1b863-199">CNAME</span><span class="sxs-lookup"><span data-stu-id="1b863-199">CNAME</span></span>  <br/> |<span data-ttu-id="1b863-200">autodiscover</span><span class="sxs-lookup"><span data-stu-id="1b863-200">autodiscover</span></span>  <br/> |<span data-ttu-id="1b863-201">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="1b863-201">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="1b863-202">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-202">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="1b863-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="1b863-203">CNAME</span></span>  <br/> |<span data-ttu-id="1b863-204">sip</span><span class="sxs-lookup"><span data-stu-id="1b863-204">sip</span></span>  <br/> |<span data-ttu-id="1b863-205">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1b863-205">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="1b863-206">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-206">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="1b863-207">CNAME</span><span class="sxs-lookup"><span data-stu-id="1b863-207">CNAME</span></span>  <br/> |<span data-ttu-id="1b863-208">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="1b863-208">lyncdiscover</span></span>  <br/> |<span data-ttu-id="1b863-209">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1b863-209">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="1b863-210">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-210">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="1b863-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="1b863-211">CNAME</span></span>  <br/> |<span data-ttu-id="1b863-212">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="1b863-212">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="1b863-213">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="1b863-213">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="1b863-214">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-214">Use the default value (300).</span></span>  <br/> |
    |<span data-ttu-id="1b863-215">CNAME</span><span class="sxs-lookup"><span data-stu-id="1b863-215">CNAME</span></span>  <br/> |<span data-ttu-id="1b863-216">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="1b863-216">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="1b863-217">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="1b863-217">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="1b863-218">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-218">Use the default value (300).</span></span>  <br/> |
   
   ![Nom-BP-configure-3-1](../../media/4e34caaf-b418-40ec-abfa-fe62175a87c2.png)
  
5. <span data-ttu-id="1b863-220">Sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1b863-220">Select **Add Record** to add the first record.</span></span> 
    
    ![Name-BP-Configure-3-2](../../media/1053c2a7-07c3-4c1b-b54a-1c02881fb0ec.png)
  
6. <span data-ttu-id="1b863-222">Ajoutez le deuxième enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="1b863-222">Add the second CNAME record.</span></span>
    
    <span data-ttu-id="1b863-223">Utilisez les valeurs de la deuxième ligne du tableau ci-dessus, puis sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1b863-223">Use the values from the second row of the table above, and then select **Add Record** to add the second record.</span></span> 
    
    <span data-ttu-id="1b863-224">Ajoutez les enregistrements restants de la même manière, en utilisant les valeurs des troisième, quatrième, cinquième et sixième lignes du tableau.</span><span class="sxs-lookup"><span data-stu-id="1b863-224">Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="1b863-225">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="1b863-225">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="1b863-226"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="1b863-226"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b863-227">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="1b863-227">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="1b863-228">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1b863-228">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="1b863-229">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1b863-229">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="1b863-230">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="1b863-230">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="1b863-p111">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1b863-p111">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="1b863-234">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b863-234">Under **My Domains**, select the name of the domain that you want to modify.</span></span>

    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="1b863-236">Dans la colonne **Détails** , sélectionnez **enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="1b863-236">In the **Details** column, select **DNS Records**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="1b863-238">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b863-238">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="1b863-239">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="1b863-239">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="1b863-240">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="1b863-240">**Type**</span></span>|<span data-ttu-id="1b863-241">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="1b863-241">**Host**</span></span>|<span data-ttu-id="1b863-242">**Answer (Réponse)**</span><span class="sxs-lookup"><span data-stu-id="1b863-242">**Answer**</span></span>|<span data-ttu-id="1b863-243">**TTL**</span><span class="sxs-lookup"><span data-stu-id="1b863-243">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="1b863-244">TXT</span><span class="sxs-lookup"><span data-stu-id="1b863-244">TXT</span></span>  <br/> |<span data-ttu-id="1b863-245">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="1b863-245">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="1b863-246">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="1b863-246">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="1b863-247">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="1b863-247">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="1b863-248">Use the default value (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-248">Use the default value (300).</span></span>  <br/> |
   
   ![Nom-BP-configure-4-1](../../media/cbbfc071-840a-4ffa-a59e-0dfce03063cc.png)
  
5. <span data-ttu-id="1b863-250">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1b863-250">Select **Add Record**.</span></span>
    
    ![Name-BP-Configure-4-2](../../media/db1e0e09-2b95-4fc1-88bd-e86da536921f.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="1b863-252">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="1b863-252">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="1b863-253"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="1b863-253"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="1b863-p112">Pour commencer, accédez à la page de vos domaines sur le site name.com en utilisant [ce lien](https://www.name.com/account/domain). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="1b863-p112">To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.</span></span>
    
    ![Name-BP-Configure-1-1](../../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. <span data-ttu-id="1b863-257">Sous **Mes domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b863-257">Under **My Domains**, select the name of the domain that you want to modify.</span></span>
    
    ![Name-BP-Configure-1-2](../../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. <span data-ttu-id="1b863-259">Dans la colonne **Détails** , sélectionnez **enregistrements DNS +**.</span><span class="sxs-lookup"><span data-stu-id="1b863-259">In the **Details** column, select **DNS Records+**.</span></span> 
    
    ![Name-BP-Configure-1-3](../../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. <span data-ttu-id="1b863-261">Ajoutez le premier enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="1b863-261">Add the first SRV record:</span></span>
    
    <span data-ttu-id="1b863-262">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1b863-262">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>
    
    <span data-ttu-id="1b863-263">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="1b863-263">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="1b863-264">**Type**</span><span class="sxs-lookup"><span data-stu-id="1b863-264">**Type**</span></span>|<span data-ttu-id="1b863-265">**Service**</span><span class="sxs-lookup"><span data-stu-id="1b863-265">**Service**</span></span>|<span data-ttu-id="1b863-266">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="1b863-266">**Weight**</span></span>|<span data-ttu-id="1b863-267">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="1b863-267">**TTL**</span></span>|<span data-ttu-id="1b863-268">**Prio (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="1b863-268">**Prio**</span></span>|<span data-ttu-id="1b863-269">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="1b863-269">**Protocol**</span></span>|<span data-ttu-id="1b863-270">**Port**</span><span class="sxs-lookup"><span data-stu-id="1b863-270">**Port**</span></span>|<span data-ttu-id="1b863-271">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="1b863-271">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="1b863-272">SRV</span><span class="sxs-lookup"><span data-stu-id="1b863-272">SRV</span></span>|<span data-ttu-id="1b863-273">sip</span><span class="sxs-lookup"><span data-stu-id="1b863-273">sip</span></span>|<span data-ttu-id="1b863-274">0,1</span><span class="sxs-lookup"><span data-stu-id="1b863-274">1</span></span>|<span data-ttu-id="1b863-275">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-275">Use the default value (300).</span></span>|<span data-ttu-id="1b863-276">100</span><span class="sxs-lookup"><span data-stu-id="1b863-276">100</span></span>|<span data-ttu-id="1b863-277">tls</span><span class="sxs-lookup"><span data-stu-id="1b863-277">tls</span></span>|<span data-ttu-id="1b863-278">443</span><span class="sxs-lookup"><span data-stu-id="1b863-278">443</span></span>|<span data-ttu-id="1b863-279">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1b863-279">sipdir.online.lync.com</span></span> <br> <span data-ttu-id="1b863-280">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="1b863-280">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="1b863-281">SRV</span><span class="sxs-lookup"><span data-stu-id="1b863-281">SRV</span></span>|<span data-ttu-id="1b863-282">sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="1b863-282">sipfederationtls</span></span>|<span data-ttu-id="1b863-283">0,1</span><span class="sxs-lookup"><span data-stu-id="1b863-283">1</span></span>|<span data-ttu-id="1b863-284">Utilisez la valeur par défaut (300).</span><span class="sxs-lookup"><span data-stu-id="1b863-284">Use the default value (300).</span></span>|<span data-ttu-id="1b863-285">100</span><span class="sxs-lookup"><span data-stu-id="1b863-285">100</span></span>|<span data-ttu-id="1b863-286">tcp</span><span class="sxs-lookup"><span data-stu-id="1b863-286">tcp</span></span>|<span data-ttu-id="1b863-287">5061</span><span class="sxs-lookup"><span data-stu-id="1b863-287">5061</span></span>|<span data-ttu-id="1b863-288">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="1b863-288">sipfed.online.lync.com</span></span> <br><span data-ttu-id="1b863-289">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="1b863-289">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
   ![Nom-BP-configure-5-1](../../media/d9a885fd-7300-45b6-ad4c-0b4bf1067560.png)
  
5. <span data-ttu-id="1b863-291">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1b863-291">Select **Add Record**.</span></span>

    ![Name-BP-Configure-5-2](../../media/a804d51d-8f57-4b0b-8bd6-a52eb1c87a97.png)
  
6. <span data-ttu-id="1b863-293">Ajoutez le deuxième enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="1b863-293">Add the second SRV record:</span></span>

<span data-ttu-id="1b863-294">Utilisez les valeurs de la ligne suivante du tableau ci-dessus, puis sélectionnez **Add record (ajouter un enregistrement** ) pour ajouter le deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1b863-294">Use the values from the next row of the table above, and then select **Add Record** to add the second record.</span></span>

>[!NOTE]
><span data-ttu-id="1b863-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="1b863-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>
