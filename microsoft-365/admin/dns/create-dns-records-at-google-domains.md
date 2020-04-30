---
title: Créer des enregistrements DNS auprès de Google Domains pour Microsoft
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
ms.assetid: 0db29490-2612-48bc-9b77-1862e7a41a8c
description: Découvrez comment vérifier votre domaine et configurer des enregistrements DNS pour la messagerie, Lync et d’autres services de Google Domains pour Microsoft.
ms.openlocfilehash: baa406f61346dc052ab90a1b1c1271ab585d92c7
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939202"
---
# <a name="create-dns-records-at-google-domains-for-microsoft"></a><span data-ttu-id="6534a-103">Créer des enregistrements DNS auprès de Google Domains pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6534a-103">Create DNS records at Google Domains for Microsoft</span></span>

 <span data-ttu-id="6534a-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="6534a-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="6534a-105">Si Google Domains est votre fournisseur d'hébergement DNS, procédez de la manière décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Lync, etc.</span><span class="sxs-lookup"><span data-stu-id="6534a-105">If Google Domains is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Lync, and so on.</span></span>
  
<span data-ttu-id="6534a-106">Après avoir ajouté ces enregistrements à Google Domains, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6534a-106">After you add these records at Google Domains, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="6534a-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="6534a-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="6534a-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="6534a-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="6534a-109">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Microsoft](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6534a-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Microsoft](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="6534a-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="6534a-110">Add a TXT record for verification</span></span>
<span data-ttu-id="6534a-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="6534a-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="6534a-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="6534a-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6534a-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6534a-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="6534a-p104">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="6534a-p104">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
1. <span data-ttu-id="6534a-119">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-119">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="6534a-120">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="6534a-120">Enter your login credentials, and then again select **Sign In**.</span></span>
    
2. <span data-ttu-id="6534a-121">Sur la page **Mes domaines** , recherchez le domaine que vous souhaitez utiliser avec Microsoft, puis sélectionnez le lien **gérer** en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6534a-121">On the **My domains** page, find the domain you want to use with Microsoft, and select the **MANAGE** link next to it.</span></span> <span data-ttu-id="6534a-122">Dans le volet de navigation de gauche, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="6534a-122">In the left navigation, select **DNS**.</span></span>
    
3. <span data-ttu-id="6534a-123">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="6534a-123">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="6534a-124">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="6534a-124">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="6534a-125">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="6534a-125">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6534a-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="6534a-126">**Name**</span></span> <br/> |<span data-ttu-id="6534a-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="6534a-127">**Type**</span></span> <br/> |<span data-ttu-id="6534a-128">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6534a-128">**TTL**</span></span> <br/> |<span data-ttu-id="6534a-129">**Données**</span><span class="sxs-lookup"><span data-stu-id="6534a-129">**Data**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="6534a-130">TXT</span><span class="sxs-lookup"><span data-stu-id="6534a-130">TXT</span></span>  <br/> |<span data-ttu-id="6534a-131">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-131">1H</span></span>  <br/> |<span data-ttu-id="6534a-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="6534a-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="6534a-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="6534a-133">**Note:** This is an example.</span></span> <span data-ttu-id="6534a-134">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="6534a-134">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="6534a-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6534a-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
4. <span data-ttu-id="6534a-136">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-136">Select **Add**.</span></span>
    
5. <span data-ttu-id="6534a-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6534a-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="6534a-138">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6534a-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="6534a-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="6534a-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="6534a-140">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="6534a-140">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="6534a-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="6534a-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="6534a-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="6534a-142">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="6534a-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="6534a-143">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6534a-144">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="6534a-144">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="6534a-145">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="6534a-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="6534a-146">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6534a-146">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="6534a-147">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="6534a-147">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="6534a-148"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="6534a-148"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="6534a-p108">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="6534a-p108">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
2. <span data-ttu-id="6534a-152">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-152">Select **Sign In**.</span></span>
    
3. <span data-ttu-id="6534a-153">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="6534a-153">Enter your login credentials, and then again select **Sign In**.</span></span>
4. <span data-ttu-id="6534a-154">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="6534a-154">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="6534a-155">Si vous avez un compte de courrier G Suite, vous devez commencer par supprimer les enregistrements MX qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="6534a-155">If you have a G Suite email account, you must first delete the MX records associated with that account.</span></span> <span data-ttu-id="6534a-156">Les enregistrements MX de la suite G vous empêchent d’ajouter d’autres enregistrements MX, y compris ceux requis pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6534a-156">The G Suite MX records prevent you from adding any other MX records, including those required for Microsoft.</span></span> <span data-ttu-id="6534a-157">Notez que la suppression d'enregistrements G Suite ne supprime pas votre compte G Suite.</span><span class="sxs-lookup"><span data-stu-id="6534a-157">Note that deleting the G Suite records does not delete your G Suite account.</span></span> <span data-ttu-id="6534a-158">Pour supprimer les enregistrements MX G Suite, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6534a-158">To delete your G Suite MX records, use the following steps.</span></span> 
  
5. <span data-ttu-id="6534a-159">Dans la section **rapports synthétiques** , dans la zone **G suite** , sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6534a-159">In the **Synthetic records** section, in the **G Suite** area, select **Delete**.</span></span>
    
    <span data-ttu-id="6534a-160">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="6534a-160">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Supprimer dans la section enregistrements synthétiques.](../../media/bd276b5d-5667-4bb1-a233-2dc5194e7ace.png)
  
6. <span data-ttu-id="6534a-162">Sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6534a-162">Select **Delete**.</span></span>
    
    ![Sélectionnez supprimer](../../media/4413a45a-5b82-4ec6-82c6-0091f5be9696.png)
  
7. <span data-ttu-id="6534a-164">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="6534a-164">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="6534a-165">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="6534a-165">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="6534a-166">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="6534a-166">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="6534a-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="6534a-167">**Name**</span></span>|<span data-ttu-id="6534a-168">**Type**</span><span class="sxs-lookup"><span data-stu-id="6534a-168">**Type**</span></span>|<span data-ttu-id="6534a-169">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6534a-169">**TTL**</span></span>|<span data-ttu-id="6534a-170">**Données**</span><span class="sxs-lookup"><span data-stu-id="6534a-170">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="6534a-171">MX</span><span class="sxs-lookup"><span data-stu-id="6534a-171">MX</span></span>  <br/> |<span data-ttu-id="6534a-172">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-172">1H</span></span>  <br/> |<span data-ttu-id="6534a-173">0  *\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-173">0  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="6534a-174">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-174">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="6534a-p110">La valeur **0** représente la valeur de priorité MX. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par un espace.  </span><span class="sxs-lookup"><span data-stu-id="6534a-p110">The **0** is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="6534a-177">**Remarque :** Obtenez votre \<*clé de domaine*\> à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6534a-177">**Note:** Get your \<*domain-key*\> from your Microsoft account.</span></span>  [<span data-ttu-id="6534a-178">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6534a-178">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          <span data-ttu-id="6534a-179">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="6534a-179">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../../media/b660ca9e-984d-449f-ae59-a65fe4e2c6bd.png)
  
5. <span data-ttu-id="6534a-181">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-181">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/32f8f23c-0b80-48da-b08e-4e04052971af.png)
  
6. <span data-ttu-id="6534a-183">Si d'autres enregistrements MX personnalisés sont répertoriés, supprimez-les.</span><span class="sxs-lookup"><span data-stu-id="6534a-183">If there are any other Custom MX records, remove them.</span></span>
    
1. <span data-ttu-id="6534a-184">Sélectionnez **modifier** dans la ligne enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="6534a-184">Select **Edit** in the MX record row.</span></span> 
    
    ![Sélectionnez Modifier dans la ligne enregistrement MX.](../../media/acc53ae9-3b8a-421d-8d11-d4a4108b2353.png)
  
2. <span data-ttu-id="6534a-186">Pour chacun des autres enregistrements MX personnalisés, sélectionnez l’entrée dans la zone **données** , puis appuyez sur la touche **Suppr** de votre clavier pour supprimer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6534a-186">For each of the other Custom MX records, select the entry in the **Data** box and then press the **Delete** key on your keyboard to delete that record.</span></span> 
    
    <span data-ttu-id="6534a-187">Continuez jusqu'à ce que vous ayez supprimé l'entrée **Data (Données)** de chacun des autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="6534a-187">Continue until you have deleted the **Data** entry for each of the other MX records.</span></span> 
    
    ![Delete entries in the Data box](../../media/28192089-7b38-4d2e-9d52-9b83422c27d5.png)
  
7. <span data-ttu-id="6534a-189">Une fois que vous avez supprimé l’entrée de **données** pour chacun des autres enregistrements MX, sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="6534a-189">When you have deleted the **Data** entry for each of the other MX records, select **Save** to save your changes.</span></span> 
    
    ![Sélectionnez Enregistrer.](../../media/bf496d01-ccbe-4800-95f4-7b2283f2e5f6.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="6534a-191">Ajouter les cinq enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6534a-191">Add the five CNAME records that are required for Microsoft</span></span>

1. <span data-ttu-id="6534a-192">Pour commencer, accédez à la page [Google Domains] (https://domains.google.com/registrar) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="6534a-192">To get started, go to your [Google Domains page] (https://domains.google.com/registrar) and sign in.</span></span>
    
2. <span data-ttu-id="6534a-193">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="6534a-193">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="6534a-194">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="6534a-194">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="6534a-195">Dans la section **Custom resource records (Enregistrements de ressource personnalisés)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6534a-195">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from first row of the following table.</span></span> 
    
    <span data-ttu-id="6534a-196">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="6534a-196">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="6534a-197">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="6534a-197">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="6534a-198">**Name**</span><span class="sxs-lookup"><span data-stu-id="6534a-198">**Name**</span></span>|<span data-ttu-id="6534a-199">**Type**</span><span class="sxs-lookup"><span data-stu-id="6534a-199">**Type**</span></span>|<span data-ttu-id="6534a-200">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6534a-200">**TTL**</span></span>|<span data-ttu-id="6534a-201">**Données**</span><span class="sxs-lookup"><span data-stu-id="6534a-201">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6534a-202">autodiscover</span><span class="sxs-lookup"><span data-stu-id="6534a-202">autodiscover</span></span>  <br/> |<span data-ttu-id="6534a-203">CNAME</span><span class="sxs-lookup"><span data-stu-id="6534a-203">CNAME</span></span>  <br/> |<span data-ttu-id="6534a-204">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-204">1H</span></span>  <br/> |<span data-ttu-id="6534a-205">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-205">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="6534a-206">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-206">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="6534a-207">sip</span><span class="sxs-lookup"><span data-stu-id="6534a-207">sip</span></span>  <br/> |<span data-ttu-id="6534a-208">CNAME</span><span class="sxs-lookup"><span data-stu-id="6534a-208">CNAME</span></span>  <br/> |<span data-ttu-id="6534a-209">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-209">1H</span></span>  <br/> |<span data-ttu-id="6534a-210">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-210">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="6534a-211">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-211">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="6534a-212">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="6534a-212">lyncdiscover</span></span>  <br/> |<span data-ttu-id="6534a-213">CNAME</span><span class="sxs-lookup"><span data-stu-id="6534a-213">CNAME</span></span>  <br/> |<span data-ttu-id="6534a-214">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-214">1H</span></span>  <br/> |<span data-ttu-id="6534a-215">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-215">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="6534a-216">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-216">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="6534a-217">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="6534a-217">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="6534a-218">CNAME</span><span class="sxs-lookup"><span data-stu-id="6534a-218">CNAME</span></span>  <br/> |<span data-ttu-id="6534a-219">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-219">1H</span></span>  <br/> |<span data-ttu-id="6534a-220">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="6534a-220">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="6534a-221">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-221">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="6534a-222">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="6534a-222">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="6534a-223">CNAME</span><span class="sxs-lookup"><span data-stu-id="6534a-223">CNAME</span></span>  <br/> |<span data-ttu-id="6534a-224">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-224">1H</span></span>  <br/> |<span data-ttu-id="6534a-225">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-225">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="6534a-226">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-226">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../../media/cff9832a-6d57-421f-a183-55320974ed87.png)
  
4. <span data-ttu-id="6534a-228">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-228">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/4a78080a-e0b2-4582-9696-3fe4fea41e91.png)
  
5. <span data-ttu-id="6534a-230">Ajoutez les quatre autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="6534a-230">Add the other four CNAME records.</span></span>
    
    <span data-ttu-id="6534a-231">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Add (Ajouter** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6534a-231">In the **Custom resource records** section, create a record by using the values from the next row in the table, and then again select **Add** to complete that record.</span></span> 
    
    <span data-ttu-id="6534a-232">Répétez cette procédure jusqu’à ce que vous ayez créé tous les enregistrements CNAMe requis.</span><span class="sxs-lookup"><span data-stu-id="6534a-232">Repeat this process until you have created all of the required CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="6534a-233">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="6534a-233">Add a TXT record for SPF to help prevent email spam</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6534a-234">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="6534a-234">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="6534a-235">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="6534a-235">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="6534a-236">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6534a-236">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="6534a-237">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir qu’un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="6534a-237">Instead, add the required Microsoft values to the current record so that you have a single SPF record that includes both sets of values.</span></span> <span data-ttu-id="6534a-238">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="6534a-238">Need examples?</span></span> <span data-ttu-id="6534a-239">Consultez ces [Enregistrements DNS externes pour Microsoft](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="6534a-239">Check out these [External Domain Name System records for Microsoft](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span></span> <span data-ttu-id="6534a-240">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="6534a-240">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="6534a-p113">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="6534a-p113">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
1. <span data-ttu-id="6534a-244">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-244">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="6534a-245">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="6534a-245">Enter your login credentials, and then again select **Sign In**.</span></span>
    
3. <span data-ttu-id="6534a-246">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="6534a-246">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="6534a-247">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), sur la ligne de l’enregistrement txt, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="6534a-247">In the **Custom resource records** section, on the TXT record row, select **Edit**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6534a-p114">Google Domains stocke les enregistrements TXT en tant qu'ensemble pouvant contenir plusieurs enregistrements. Lorsque vous avez au moins un autre enregistrement TXT, par exemple, l'enregistrement TXT que vous avez utilisé pour vérifier votre domaine, vous devez ajouter de nouveaux enregistrements TXT à ce jeu d'enregistrements. Toute tentative de saisie d'enregistrements TXT supplémentaires sous forme d'entrées distinctes entraîne un message d'erreur **Enregistrement en double**.</span><span class="sxs-lookup"><span data-stu-id="6534a-p114">Google Domains stores TXT records as a set that may contain multiple records. When you have at least one other TXT record, such as the TXT record you used to verify your domain, you must add TXT new records to that record set. Any attempt to enter additional TXT records as separate entries will result in a **Duplicate record** error message.</span></span> 
  
    ![Sélectionnez Modifier dans la ligne enregistrement TXT.](../../media/eae14850-8d0c-4f29-8587-df8b36129d5f.png)
  
5. <span data-ttu-id="6534a-252">Sélectionnez le contrôle **(+)** .</span><span class="sxs-lookup"><span data-stu-id="6534a-252">Select the **(+)** control.</span></span> 
    
    ![Sélectionner le contrôle plus](../../media/628604cc-d2b2-42a5-bb5b-13c327b85d9f.png)
  
6. <span data-ttu-id="6534a-254">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6534a-254">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="6534a-255">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="6534a-255">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="6534a-256">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="6534a-256">**Data**</span></span>|
    |:-----|
    |<span data-ttu-id="6534a-257">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="6534a-257">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> 

    > [!NOTE]
    > <span data-ttu-id="6534a-258">Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6534a-258">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           
   
   ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../../media/4645cc4f-9fcc-4626-9674-072ed6fa34c2.png)
  
7. <span data-ttu-id="6534a-260">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6534a-260">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/20c4c926-f062-4048-9265-bf752be54e0c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="6534a-262">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="6534a-262">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="6534a-263"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="6534a-263"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="6534a-p115">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="6534a-p115">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
2. <span data-ttu-id="6534a-267">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-267">Select **Sign In**.</span></span>
    
3. <span data-ttu-id="6534a-268">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="6534a-268">Enter your login credentials, and then again select **Sign In**.</span></span>
    
4. <span data-ttu-id="6534a-269">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="6534a-269">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
5. <span data-ttu-id="6534a-270">Ajouter le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="6534a-270">Add the first SRV record.</span></span>
    
    <span data-ttu-id="6534a-271">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="6534a-271">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="6534a-272">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="6534a-272">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="6534a-273">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="6534a-273">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="6534a-274">**Name**</span><span class="sxs-lookup"><span data-stu-id="6534a-274">**Name**</span></span>|<span data-ttu-id="6534a-275">**Type**</span><span class="sxs-lookup"><span data-stu-id="6534a-275">**Type**</span></span>|<span data-ttu-id="6534a-276">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6534a-276">**TTL**</span></span>|<span data-ttu-id="6534a-277">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="6534a-277">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6534a-278">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="6534a-278">_sip._tls</span></span>|<span data-ttu-id="6534a-279">SRV</span><span class="sxs-lookup"><span data-stu-id="6534a-279">SRV</span></span>|<span data-ttu-id="6534a-280">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-280">1H</span></span>|<span data-ttu-id="6534a-281">100 1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-281">100 1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="6534a-282">**Cette valeur doit se terminer par un point (.)** **Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6534a-282">**This value MUST end with a period (.)** **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="6534a-283">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="6534a-283">_sipfederationtls._tcp</span></span>|<span data-ttu-id="6534a-284">SRV</span><span class="sxs-lookup"><span data-stu-id="6534a-284">SRV</span></span>|<span data-ttu-id="6534a-285">Premier</span><span class="sxs-lookup"><span data-stu-id="6534a-285">1H</span></span>|<span data-ttu-id="6534a-286">100 1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="6534a-286">100 1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="6534a-287">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="6534a-287">**This value MUST end with a period (.)**</span></span>

    <span data-ttu-id="6534a-288">Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6534a-288">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>       
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../../media/429d06a9-c0af-4961-b7d2-7a8dea6db37e.png)
  
6. <span data-ttu-id="6534a-290">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6534a-290">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../../media/89df6efd-e641-4441-baa2-d9a890424569.png)
  
7. <span data-ttu-id="6534a-292">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="6534a-292">Add the other SRV record.</span></span>
    
    <span data-ttu-id="6534a-293">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Add (Ajouter** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6534a-293">In the **Custom resource records** section, create a record by using the values from the second row in the table, and then again select **Add** to complete that record.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6534a-294">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="6534a-294">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="6534a-295">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="6534a-295">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="6534a-296">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6534a-296">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
