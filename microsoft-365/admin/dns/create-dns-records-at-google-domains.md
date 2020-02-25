---
title: Créer des enregistrements DNS via Google Domains pour Office 365
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
ms.assetid: 0db29490-2612-48bc-9b77-1862e7a41a8c
description: Découvrez comment vérifier votre domaine et configurer des enregistrements DNS pour la messagerie, Lync et d’autres services de Google Domains pour Office 365.
ms.openlocfilehash: c59a3d63797f20b0d3a42647eb68d7699ed63450
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42244818"
---
# <a name="create-dns-records-at-google-domains-for-office-365"></a><span data-ttu-id="45cd4-103">Créer des enregistrements DNS via Google Domains pour Office 365</span><span class="sxs-lookup"><span data-stu-id="45cd4-103">Create DNS records at Google Domains for Office 365</span></span>

 <span data-ttu-id="45cd4-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="45cd4-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="45cd4-105">Si Google Domains est votre fournisseur d'hébergement DNS, procédez de la manière décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Lync, etc.</span><span class="sxs-lookup"><span data-stu-id="45cd4-105">If Google Domains is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Lync, and so on.</span></span>
  
<span data-ttu-id="45cd4-106">Une fois ces enregistrements ajoutés sur Google Domains, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="45cd4-106">After you add these records at Google Domains, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="45cd4-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="45cd4-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
> <span data-ttu-id="45cd4-108">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="45cd4-108">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="45cd4-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="45cd4-109">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="45cd4-110">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="45cd4-110">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="45cd4-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="45cd4-111">Add a TXT record for verification</span></span>
<span data-ttu-id="45cd4-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="45cd4-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="45cd4-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="45cd4-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45cd4-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="45cd4-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="45cd4-p104">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="45cd4-p104">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
1. <span data-ttu-id="45cd4-120">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-120">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="45cd4-121">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-121">Enter your login credentials, and then again select **Sign In**.</span></span>
    
2. <span data-ttu-id="45cd4-122">Sur la page **Mes domaines** , recherchez le domaine que vous souhaitez utiliser avec Office 365, puis sélectionnez le lien **gérer** en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="45cd4-122">On the **My domains** page, find the domain you want to use with Office 365, and select the **MANAGE** link next to it.</span></span> <span data-ttu-id="45cd4-123">Dans le volet de navigation de gauche, sélectionnez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-123">In the left navigation, select **DNS**.</span></span>
    
3. <span data-ttu-id="45cd4-124">Dans la section \* \* Custom Resource Records \* \*, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45cd4-124">In the \*\* Custom resource records \*\* section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="45cd4-125">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-125">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="45cd4-126">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-126">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="45cd4-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cd4-127">**Name**</span></span> <br/> |<span data-ttu-id="45cd4-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="45cd4-128">**Type**</span></span> <br/> |<span data-ttu-id="45cd4-129">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-129">**TTL**</span></span> <br/> |<span data-ttu-id="45cd4-130">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-130">**Data**</span></span> <br/> |
    |@  <br/> |<span data-ttu-id="45cd4-131">TXT</span><span class="sxs-lookup"><span data-stu-id="45cd4-131">TXT</span></span>  <br/> |<span data-ttu-id="45cd4-132">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-132">1H</span></span>  <br/> |<span data-ttu-id="45cd4-133">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="45cd4-133">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="45cd4-134">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="45cd4-134">**Note:** This is an example.</span></span> <span data-ttu-id="45cd4-135">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="45cd4-135">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="45cd4-136">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="45cd4-136">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
4. <span data-ttu-id="45cd4-137">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-137">Select **Add**.</span></span>
    
5. <span data-ttu-id="45cd4-138">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="45cd4-138">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="45cd4-139">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="45cd4-139">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="45cd4-140">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="45cd4-140">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="45cd4-141">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="45cd4-141">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="45cd4-142">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="45cd4-142">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="45cd4-143">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-143">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="45cd4-144">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-144">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="45cd4-145">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="45cd4-145">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="45cd4-146">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="45cd4-146">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="45cd4-147">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="45cd4-147">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 

  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="45cd4-148">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="45cd4-148">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="45cd4-149"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="45cd4-149"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="45cd4-p108">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="45cd4-p108">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
2. <span data-ttu-id="45cd4-153">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-153">Select **Sign In**.</span></span>
    
3. <span data-ttu-id="45cd4-154">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-154">Enter your login credentials, and then again select **Sign In**.</span></span>
4. <span data-ttu-id="45cd4-155">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="45cd4-155">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="45cd4-p109">Si vous avez un compte de courrier G Suite, vous devez commencer par supprimer les enregistrements MX qui lui sont associés. Les enregistrements MX G Suite vous empêchent d'ajouter d'autres enregistrements MX, notamment ceux requis pour Office 365. Notez que la suppression d'enregistrements G Suite ne supprime pas votre compte G Suite. Pour supprimer les enregistrements MX G Suite, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="45cd4-p109">If you have a G Suite email account, you must first delete the MX records associated with that account. The G Suite MX records prevent you from adding any other MX records, including those required for Office 365. Note that deleting the G Suite records does not delete your G Suite account. To delete your G Suite MX records, use the following steps.</span></span> 
  
5. <span data-ttu-id="45cd4-160">Dans la section **rapports synthétiques** , dans la zone **G suite** , sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-160">In the **Synthetic records** section, in the **G Suite** area, select **Delete**.</span></span>
    
    <span data-ttu-id="45cd4-161">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-161">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez Supprimer dans la section enregistrements synthétiques.](../media/bd276b5d-5667-4bb1-a233-2dc5194e7ace.png)
  
6. <span data-ttu-id="45cd4-163">Sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-163">Select **Delete**.</span></span>
    
    ![Sélectionnez supprimer](../media/4413a45a-5b82-4ec6-82c6-0091f5be9696.png)
  
7. <span data-ttu-id="45cd4-165">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="45cd4-165">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="45cd4-166">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-166">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="45cd4-167">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-167">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="45cd4-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cd4-168">**Name**</span></span>|<span data-ttu-id="45cd4-169">**Type**</span><span class="sxs-lookup"><span data-stu-id="45cd4-169">**Type**</span></span>|<span data-ttu-id="45cd4-170">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-170">**TTL**</span></span>|<span data-ttu-id="45cd4-171">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-171">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="45cd4-172">MX</span><span class="sxs-lookup"><span data-stu-id="45cd4-172">MX</span></span>  <br/> |<span data-ttu-id="45cd4-173">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-173">1H</span></span>  <br/> |<span data-ttu-id="45cd4-174">0  *\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-174">0  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="45cd4-175">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-175">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="45cd4-p110">La valeur **0** représente la valeur de priorité MX. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par un espace.  </span><span class="sxs-lookup"><span data-stu-id="45cd4-p110">The **0** is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="45cd4-178">**Remarque :** Obtenez votre \< *clé* \> de domaine à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="45cd4-178">**Note:** Get your \<*domain-key*\> from your Office 365 account.</span></span>  [<span data-ttu-id="45cd4-179">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="45cd4-179">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          <span data-ttu-id="45cd4-180">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="45cd4-180">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../media/b660ca9e-984d-449f-ae59-a65fe4e2c6bd.png)
  
5. <span data-ttu-id="45cd4-182">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-182">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/32f8f23c-0b80-48da-b08e-4e04052971af.png)
  
6. <span data-ttu-id="45cd4-184">Si d'autres enregistrements MX personnalisés sont répertoriés, supprimez-les.</span><span class="sxs-lookup"><span data-stu-id="45cd4-184">If there are any other Custom MX records, remove them.</span></span>
    
1. <span data-ttu-id="45cd4-185">Sélectionnez **modifier** dans la ligne enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="45cd4-185">Select **Edit** in the MX record row.</span></span> 
    
    ![Sélectionnez Modifier dans la ligne enregistrement MX.](../media/acc53ae9-3b8a-421d-8d11-d4a4108b2353.png)
  
2. <span data-ttu-id="45cd4-187">Pour chacun des autres enregistrements MX personnalisés, sélectionnez l’entrée dans la zone **données** , puis appuyez sur la touche **Suppr** de votre clavier pour supprimer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="45cd4-187">For each of the other Custom MX records, select the entry in the **Data** box and then press the **Delete** key on your keyboard to delete that record.</span></span> 
    
    <span data-ttu-id="45cd4-188">Continuez jusqu'à ce que vous ayez supprimé l'entrée **Data (Données)** de chacun des autres enregistrements MX.</span><span class="sxs-lookup"><span data-stu-id="45cd4-188">Continue until you have deleted the **Data** entry for each of the other MX records.</span></span> 
    
    ![Delete entries in the Data box](../media/28192089-7b38-4d2e-9d52-9b83422c27d5.png)
  
7. <span data-ttu-id="45cd4-190">Une fois que vous avez supprimé l’entrée de **données** pour chacun des autres enregistrements MX, sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="45cd4-190">When you have deleted the **Data** entry for each of the other MX records, select **Save** to save your changes.</span></span> 
    
    ![Sélectionnez Enregistrer.](../media/bf496d01-ccbe-4800-95f4-7b2283f2e5f6.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="45cd4-192">Ajouter les cinq enregistrements CNAMe requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="45cd4-192">Add the five CNAME records that are required for Office 365</span></span>

1. <span data-ttu-id="45cd4-193">Pour commencer, accédez à la page [Google Domains] (https://domains.google.com/registrar) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="45cd4-193">To get started, go to your [Google Domains page] (https://domains.google.com/registrar) and sign in.</span></span>
    
2. <span data-ttu-id="45cd4-194">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="45cd4-194">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="45cd4-195">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="45cd4-195">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="45cd4-196">Dans la section **Custom resource records (Enregistrements de ressource personnalisés)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45cd4-196">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from first row of the following table.</span></span> 
    
    <span data-ttu-id="45cd4-197">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-197">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="45cd4-198">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-198">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="45cd4-199">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cd4-199">**Name**</span></span>|<span data-ttu-id="45cd4-200">**Type**</span><span class="sxs-lookup"><span data-stu-id="45cd4-200">**Type**</span></span>|<span data-ttu-id="45cd4-201">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-201">**TTL**</span></span>|<span data-ttu-id="45cd4-202">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-202">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="45cd4-203">autodiscover</span><span class="sxs-lookup"><span data-stu-id="45cd4-203">autodiscover</span></span>  <br/> |<span data-ttu-id="45cd4-204">CNAME</span><span class="sxs-lookup"><span data-stu-id="45cd4-204">CNAME</span></span>  <br/> |<span data-ttu-id="45cd4-205">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-205">1H</span></span>  <br/> |<span data-ttu-id="45cd4-206">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-206">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="45cd4-207">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-207">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="45cd4-208">sip</span><span class="sxs-lookup"><span data-stu-id="45cd4-208">sip</span></span>  <br/> |<span data-ttu-id="45cd4-209">CNAME</span><span class="sxs-lookup"><span data-stu-id="45cd4-209">CNAME</span></span>  <br/> |<span data-ttu-id="45cd4-210">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-210">1H</span></span>  <br/> |<span data-ttu-id="45cd4-211">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-211">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="45cd4-212">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-212">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="45cd4-213">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="45cd4-213">lyncdiscover</span></span>  <br/> |<span data-ttu-id="45cd4-214">CNAME</span><span class="sxs-lookup"><span data-stu-id="45cd4-214">CNAME</span></span>  <br/> |<span data-ttu-id="45cd4-215">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-215">1H</span></span>  <br/> |<span data-ttu-id="45cd4-216">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-216">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="45cd4-217">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-217">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="45cd4-218">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="45cd4-218">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="45cd4-219">CNAME</span><span class="sxs-lookup"><span data-stu-id="45cd4-219">CNAME</span></span>  <br/> |<span data-ttu-id="45cd4-220">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-220">1H</span></span>  <br/> |<span data-ttu-id="45cd4-221">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="45cd4-221">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="45cd4-222">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-222">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="45cd4-223">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="45cd4-223">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="45cd4-224">CNAME</span><span class="sxs-lookup"><span data-stu-id="45cd4-224">CNAME</span></span>  <br/> |<span data-ttu-id="45cd4-225">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-225">1H</span></span>  <br/> |<span data-ttu-id="45cd4-226">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-226">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="45cd4-227">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-227">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../media/cff9832a-6d57-421f-a183-55320974ed87.png)
  
4. <span data-ttu-id="45cd4-229">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-229">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/4a78080a-e0b2-4582-9696-3fe4fea41e91.png)
  
5. <span data-ttu-id="45cd4-231">Ajoutez les quatre autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="45cd4-231">Add the other four CNAME records.</span></span>
    
    <span data-ttu-id="45cd4-232">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Add (Ajouter** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="45cd4-232">In the **Custom resource records** section, create a record by using the values from the next row in the table, and then again select **Add** to complete that record.</span></span> 
    
    <span data-ttu-id="45cd4-233">Répétez cette procédure jusqu’à ce que vous ayez créé tous les enregistrements CNAMe requis.</span><span class="sxs-lookup"><span data-stu-id="45cd4-233">Repeat this process until you have created all of the required CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="45cd4-234">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="45cd4-234">Add a TXT record for SPF to help prevent email spam</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45cd4-235">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="45cd4-235">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="45cd4-236">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="45cd4-236">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="45cd4-237">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="45cd4-237">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="45cd4-238">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un seul enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="45cd4-238">Instead, add the required Office 365 values to the current record so that you have a single SPF record that includes both sets of values.</span></span> <span data-ttu-id="45cd4-239">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="45cd4-239">Need examples?</span></span> <span data-ttu-id="45cd4-240">Consultez ces [enregistrements DNS externes pour Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span><span class="sxs-lookup"><span data-stu-id="45cd4-240">Check out these [External Domain Name System records for Office 365](https://support.office.com/article/c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0#bkmk_spfrecords).</span></span> <span data-ttu-id="45cd4-241">Pour valider votre enregistrement SPF, vous pouvez utiliser l'un des outils de [validation SPF suivants](../setup/domains-faq.md).</span><span class="sxs-lookup"><span data-stu-id="45cd4-241">To validate your SPF record, you can use one of these [SPF validation tools](../setup/domains-faq.md).</span></span> 
  
1. <span data-ttu-id="45cd4-p113">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="45cd4-p113">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
1. <span data-ttu-id="45cd4-245">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-245">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="45cd4-246">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-246">Enter your login credentials, and then again select **Sign In**.</span></span>
    
3. <span data-ttu-id="45cd4-247">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="45cd4-247">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="45cd4-248">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), sur la ligne de l’enregistrement txt, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-248">In the **Custom resource records** section, on the TXT record row, select **Edit**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="45cd4-p114">Google Domains stocke les enregistrements TXT en tant qu'ensemble pouvant contenir plusieurs enregistrements. Lorsque vous avez au moins un autre enregistrement TXT, par exemple, l'enregistrement TXT que vous avez utilisé pour vérifier votre domaine, vous devez ajouter de nouveaux enregistrements TXT à ce jeu d'enregistrements. Toute tentative de saisie d'enregistrements TXT supplémentaires sous forme d'entrées distinctes entraîne un message d'erreur **Enregistrement en double**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-p114">Google Domains stores TXT records as a set that may contain multiple records. When you have at least one other TXT record, such as the TXT record you used to verify your domain, you must add TXT new records to that record set. Any attempt to enter additional TXT records as separate entries will result in a **Duplicate record** error message.</span></span> 
  
    ![Sélectionnez Modifier dans la ligne enregistrement TXT.](../media/eae14850-8d0c-4f29-8587-df8b36129d5f.png)
  
5. <span data-ttu-id="45cd4-253">Sélectionnez le contrôle **(+)** .</span><span class="sxs-lookup"><span data-stu-id="45cd4-253">Select the **(+)** control.</span></span> 
    
    ![Sélectionner le contrôle plus](../media/628604cc-d2b2-42a5-bb5b-13c327b85d9f.png)
  
6. <span data-ttu-id="45cd4-255">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45cd4-255">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    <span data-ttu-id="45cd4-256">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-256">(You may have to scroll down.)</span></span>
    
    |<span data-ttu-id="45cd4-257">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-257">**Data**</span></span>|
    |:-----|
    |<span data-ttu-id="45cd4-258">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="45cd4-258">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> 

    > [!NOTE]
    > <span data-ttu-id="45cd4-259">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span><span class="sxs-lookup"><span data-stu-id="45cd4-259">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           
   
   ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../media/4645cc4f-9fcc-4626-9674-072ed6fa34c2.png)
  
7. <span data-ttu-id="45cd4-261">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-261">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../media/20c4c926-f062-4048-9265-bf752be54e0c.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="45cd4-263">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="45cd4-263">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="45cd4-264"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="45cd4-264"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="45cd4-p115">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="45cd4-p115">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
2. <span data-ttu-id="45cd4-268">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-268">Select **Sign In**.</span></span>
    
3. <span data-ttu-id="45cd4-269">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-269">Enter your login credentials, and then again select **Sign In**.</span></span>
    
4. <span data-ttu-id="45cd4-270">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="45cd4-270">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
5. <span data-ttu-id="45cd4-271">Ajouter le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="45cd4-271">Add the first SRV record.</span></span>
    
    <span data-ttu-id="45cd4-272">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="45cd4-272">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="45cd4-273">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-273">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="45cd4-274">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="45cd4-274">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="45cd4-275">**Name**</span><span class="sxs-lookup"><span data-stu-id="45cd4-275">**Name**</span></span>|<span data-ttu-id="45cd4-276">**Type**</span><span class="sxs-lookup"><span data-stu-id="45cd4-276">**Type**</span></span>|<span data-ttu-id="45cd4-277">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-277">**TTL**</span></span>|<span data-ttu-id="45cd4-278">**Données**</span><span class="sxs-lookup"><span data-stu-id="45cd4-278">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="45cd4-279">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="45cd4-279">_sip._tls</span></span>|<span data-ttu-id="45cd4-280">SRV</span><span class="sxs-lookup"><span data-stu-id="45cd4-280">SRV</span></span>|<span data-ttu-id="45cd4-281">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-281">1H</span></span>|<span data-ttu-id="45cd4-282">100 1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-282">100 1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="45cd4-283">**Cette valeur doit se terminer par un point (.)** **Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="45cd4-283">**This value MUST end with a period (.)** **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="45cd4-284">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="45cd4-284">_sipfederationtls._tcp</span></span>|<span data-ttu-id="45cd4-285">SRV</span><span class="sxs-lookup"><span data-stu-id="45cd4-285">SRV</span></span>|<span data-ttu-id="45cd4-286">Premier</span><span class="sxs-lookup"><span data-stu-id="45cd4-286">1H</span></span>|<span data-ttu-id="45cd4-287">100 1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="45cd4-287">100 1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="45cd4-288">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="45cd4-288">**This value MUST end with a period (.)**</span></span>

    <span data-ttu-id="45cd4-289">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span><span class="sxs-lookup"><span data-stu-id="45cd4-289">We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>       
   
    ![Taper ou coller des valeurs dans la section Custom Resource Records (enregistrements de ressources personnalisés)](../media/429d06a9-c0af-4961-b7d2-7a8dea6db37e.png)
  
6. <span data-ttu-id="45cd4-291">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="45cd4-291">Select **Add**.</span></span>
    
    ![Sélectionnez Ajouter](../media/89df6efd-e641-4441-baa2-d9a890424569.png)
  
7. <span data-ttu-id="45cd4-293">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="45cd4-293">Add the other SRV record.</span></span>
    
    <span data-ttu-id="45cd4-294">Dans la section **Custom Resource Records (enregistrements de ressources personnalisés** ), créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Add (Ajouter** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="45cd4-294">In the **Custom resource records** section, create a record by using the values from the second row in the table, and then again select **Add** to complete that record.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="45cd4-295">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="45cd4-295">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="45cd4-296">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="45cd4-296">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="45cd4-297">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="45cd4-297">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
