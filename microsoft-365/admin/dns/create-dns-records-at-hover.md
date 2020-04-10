---
title: Créer des enregistrements DNS auprès de Hover pour Office 365
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
ms.assetid: 46ab4b10-6857-44b1-b08d-d1b5f45a69c6
description: Découvrez comment vérifier votre domaine et configurer des enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services à l’aide du pointage pour Office 365.
ms.openlocfilehash: 7884038dcd1ebc7b13bbed44d98f0d5172015cc1
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211702"
---
# <a name="create-dns-records-at-hover-for-office-365"></a><span data-ttu-id="46c5b-103">Créer des enregistrements DNS auprès de Hover pour Office 365</span><span class="sxs-lookup"><span data-stu-id="46c5b-103">Create DNS records at Hover for Office 365</span></span>

 <span data-ttu-id="46c5b-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="46c5b-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="46c5b-105">Si Hover est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="46c5b-105">If Hover is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
     
<span data-ttu-id="46c5b-106">Une fois ces enregistrements ajoutés sur Hover, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="46c5b-106">After you add these records at Hover, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="46c5b-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="46c5b-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="46c5b-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="46c5b-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="46c5b-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="46c5b-111">Add a TXT record for verification</span></span>
<span data-ttu-id="46c5b-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="46c5b-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="46c5b-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="46c5b-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="46c5b-117">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="46c5b-117">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="46c5b-p104">Pour commencer, accédez à la page de vos domaines sur Hover à l'aide de [ce lien](https://www.hover.com/domains). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p104">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains). You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="46c5b-121">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="46c5b-121">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="46c5b-123">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="46c5b-123">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="46c5b-125">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-125">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="46c5b-127">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="46c5b-127">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="46c5b-128">Hostname (Nom d'hôte)</span><span class="sxs-lookup"><span data-stu-id="46c5b-128">Hostname</span></span>  <br/> |<span data-ttu-id="46c5b-129">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="46c5b-129">Record Type</span></span>  <br/> |<span data-ttu-id="46c5b-130">Value (Valeur)</span><span class="sxs-lookup"><span data-stu-id="46c5b-130">Value</span></span>  <br/> |
    |@  <br/> |<span data-ttu-id="46c5b-131">TXT</span><span class="sxs-lookup"><span data-stu-id="46c5b-131">TXT</span></span>  <br/> |<span data-ttu-id="46c5b-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="46c5b-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="46c5b-133">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="46c5b-133">**Note:** This is an example.</span></span> <span data-ttu-id="46c5b-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="46c5b-134">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="46c5b-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="46c5b-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/3b0d19f9-4138-47a7-aab2-137ad120ded6.png)
  
6. <span data-ttu-id="46c5b-137">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-137">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/07dcf68e-34be-47dc-999e-0216de68cc9c.png)
  
7. <span data-ttu-id="46c5b-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="46c5b-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="46c5b-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="46c5b-140">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="46c5b-141">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="46c5b-141">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="46c5b-142">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="46c5b-142">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="46c5b-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="46c5b-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="46c5b-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-144">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="46c5b-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-145">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="46c5b-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="46c5b-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="46c5b-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="46c5b-149">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="46c5b-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="46c5b-150"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="46c5b-151">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="46c5b-151">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="46c5b-p107">Pour commencer, accédez à la page de vos domaines sur Hover à l'aide de [ce lien](https://www.hover.com/domains). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p107">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains). You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="46c5b-155">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="46c5b-155">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="46c5b-157">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="46c5b-157">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="46c5b-159">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-159">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="46c5b-161">Dans les zones du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **MX**, puis tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46c5b-161">In the boxes for the new record, select **MX** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="46c5b-162">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-162">**Hostname**</span></span>|<span data-ttu-id="46c5b-163">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-163">**Record Type**</span></span>|<span data-ttu-id="46c5b-164">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-164">**Priority**</span></span>|<span data-ttu-id="46c5b-165">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-165">**Hostname**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="46c5b-166">MX</span><span class="sxs-lookup"><span data-stu-id="46c5b-166">MX</span></span>  <br/> |<span data-ttu-id="46c5b-167">0</span><span class="sxs-lookup"><span data-stu-id="46c5b-167">0</span></span>  <br/> <span data-ttu-id="46c5b-168">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="46c5b-168">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> | <span data-ttu-id="46c5b-169">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-169">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="46c5b-170">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="46c5b-170">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="46c5b-171">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="46c5b-171">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/2c8915fa-04a8-4d2a-a8ae-a79de0c8ef99.png)
  
6. <span data-ttu-id="46c5b-173">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-173">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/266c30a4-6703-48fb-a919-b510ed966193.png)
  
7. <span data-ttu-id="46c5b-175">S'il existe d'autres enregistrements MX, utilisez le processus en deux étapes suivant pour supprimer chacun d'eux :</span><span class="sxs-lookup"><span data-stu-id="46c5b-175">If there are any other MX records, use the following two-step process to remove each of them:</span></span>
    
    <span data-ttu-id="46c5b-176">Tout d’abord, en plaçant le pointeur de la souris sur un enregistrement que vous souhaitez supprimer, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-176">First, mousing over a record that you want to remove, select **Delete**.</span></span>
    
    ![Pointez avec la souris et sélectionnez Supprimer.](../../media/2ddf4902-8cd2-4969-a418-2cb592741e86.png)
  
    <span data-ttu-id="46c5b-178">Deuxièmement, sélectionnez **Oui** pour confirmer chaque suppression.</span><span class="sxs-lookup"><span data-stu-id="46c5b-178">Second, select **Yes** to confirm each deletion.</span></span> 
    
    ![Sélectionnez Oui pour confirmer la suppression](../../media/48756bd5-0205-4c4d-9803-9246795dbf4a.png)
  
    <span data-ttu-id="46c5b-180">Répétez cette procédure jusqu'à avoir supprimé tous les enregistrements MX à l'exception de celui que vous avez ajouté précédemment durant cette procédure.</span><span class="sxs-lookup"><span data-stu-id="46c5b-180">Repeat this process until you have deleted all MX records except for the one that you added earlier in this procedure.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="46c5b-181">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="46c5b-181">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="46c5b-182"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="46c5b-182"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="46c5b-183">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="46c5b-183">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="46c5b-p109">Pour commencer, accédez à la page de vos domaines sur Hover à l'aide de [ce lien](https://www.hover.com/domains). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p109">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains). You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="46c5b-187">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="46c5b-187">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="46c5b-189">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="46c5b-189">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="46c5b-191">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="46c5b-191">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="46c5b-192">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-192">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="46c5b-194">Dans les zones vides du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **CNAME**, puis tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46c5b-194">In the empty boxes for the new record, select **CNAME** for the **Record Type**, and then type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="46c5b-195">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-195">**Hostname**</span></span>|<span data-ttu-id="46c5b-196">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-196">**Record Type**</span></span>|<span data-ttu-id="46c5b-197">**Target Host (Hôte cible)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-197">**Target Host**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="46c5b-198">autodiscover</span><span class="sxs-lookup"><span data-stu-id="46c5b-198">autodiscover</span></span>  <br/> |<span data-ttu-id="46c5b-199">CNAME</span><span class="sxs-lookup"><span data-stu-id="46c5b-199">CNAME</span></span>  <br/> |<span data-ttu-id="46c5b-200">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-200">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="46c5b-201">sip</span><span class="sxs-lookup"><span data-stu-id="46c5b-201">sip</span></span>  <br/> |<span data-ttu-id="46c5b-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="46c5b-202">CNAME</span></span>  <br/> |<span data-ttu-id="46c5b-203">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-203">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="46c5b-204">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="46c5b-204">lyncdiscover</span></span>  <br/> |<span data-ttu-id="46c5b-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="46c5b-205">CNAME</span></span>  <br/> |<span data-ttu-id="46c5b-206">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-206">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="46c5b-207">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="46c5b-207">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="46c5b-208">CNAME</span><span class="sxs-lookup"><span data-stu-id="46c5b-208">CNAME</span></span>  <br/> |<span data-ttu-id="46c5b-209">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="46c5b-209">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="46c5b-210">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="46c5b-210">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="46c5b-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="46c5b-211">CNAME</span></span>  <br/> |<span data-ttu-id="46c5b-212">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-212">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/6ae607f8-d26e-47f0-a0f2-3487d37e8c7f.png)
  
6. <span data-ttu-id="46c5b-214">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-214">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/69aa3546-32de-4c17-a2e2-8c0cd133efaa.png)
  
7. <span data-ttu-id="46c5b-216">En suivant les trois étapes précédentes et en utilisant les valeurs des cinq autres lignes du tableau, ajoutez les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="46c5b-216">Using the preceding three steps and the values from the other five rows in the table, add each of the other five CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="46c5b-217">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="46c5b-217">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="46c5b-218"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="46c5b-218"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="46c5b-219">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="46c5b-219">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="46c5b-220">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="46c5b-220">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="46c5b-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="46c5b-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="46c5b-222">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="46c5b-222">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
<span data-ttu-id="46c5b-223">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="46c5b-223">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="46c5b-p111">Pour commencer, accédez à la page de vos domaines sur Hover à l'aide de [ce lien](https://www.hover.com/domains). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p111">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains). You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="46c5b-227">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="46c5b-227">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="46c5b-229">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="46c5b-229">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="46c5b-231">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-231">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="46c5b-233">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="46c5b-233">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="46c5b-234">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-234">**Hostname**</span></span>|<span data-ttu-id="46c5b-235">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-235">**Record Type**</span></span>|<span data-ttu-id="46c5b-236">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-236">**Value**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="46c5b-237">TXT</span><span class="sxs-lookup"><span data-stu-id="46c5b-237">TXT</span></span>  <br/> |<span data-ttu-id="46c5b-238">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="46c5b-238">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="46c5b-239">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="46c5b-239">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/ed36b9e0-aaa9-45fb-804d-7d4e82ba0c7f.png)
  
6. <span data-ttu-id="46c5b-241">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-241">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/13a395b9-e0e8-4393-b568-5f99b2da39da.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="46c5b-243">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="46c5b-243">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="46c5b-244"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="46c5b-244"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="46c5b-245">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US)</span><span class="sxs-lookup"><span data-stu-id="46c5b-245">Follow the steps below or [watch the video](https://support.office.com/article/Video-Create-DNS-records-at-Hover-for-Office-365-182bd58e-8fe4-4717-9233-3a3546b72ad2?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="46c5b-p112">Pour commencer, accédez à la page de vos domaines sur Hover à l'aide de [ce lien](https://www.hover.com/domains). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="46c5b-p112">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains). You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="46c5b-249">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="46c5b-249">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="46c5b-251">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="46c5b-251">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="46c5b-253">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="46c5b-253">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="46c5b-254">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-254">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="46c5b-256">Dans les zones vides du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **SRV**, puis tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46c5b-256">In the empty boxes for the new record, select **SRV** for the **Record Type**, and then type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="46c5b-257">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-257">**Hostname**</span></span>|<span data-ttu-id="46c5b-258">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-258">**Record Type**</span></span>|<span data-ttu-id="46c5b-259">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-259">**Priority**</span></span>|<span data-ttu-id="46c5b-260">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-260">**Weight**</span></span>|<span data-ttu-id="46c5b-261">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-261">**Port**</span></span>|<span data-ttu-id="46c5b-262">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="46c5b-262">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="46c5b-263">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="46c5b-263">_sip._tls</span></span>  <br/> |<span data-ttu-id="46c5b-264">SRV</span><span class="sxs-lookup"><span data-stu-id="46c5b-264">SRV</span></span>  <br/> |<span data-ttu-id="46c5b-265">100</span><span class="sxs-lookup"><span data-stu-id="46c5b-265">100</span></span>  <br/> |<span data-ttu-id="46c5b-266">0,1</span><span class="sxs-lookup"><span data-stu-id="46c5b-266">1</span></span>  <br/> |<span data-ttu-id="46c5b-267">443</span><span class="sxs-lookup"><span data-stu-id="46c5b-267">443</span></span>  <br/> |<span data-ttu-id="46c5b-268">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-268">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="46c5b-269">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="46c5b-269">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="46c5b-270">SRV</span><span class="sxs-lookup"><span data-stu-id="46c5b-270">SRV</span></span>  <br/> |<span data-ttu-id="46c5b-271">100</span><span class="sxs-lookup"><span data-stu-id="46c5b-271">100</span></span>  <br/> |<span data-ttu-id="46c5b-272">0,1</span><span class="sxs-lookup"><span data-stu-id="46c5b-272">1</span></span>  <br/> |<span data-ttu-id="46c5b-273">5061</span><span class="sxs-lookup"><span data-stu-id="46c5b-273">5061</span></span>  <br/> |<span data-ttu-id="46c5b-274">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="46c5b-274">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/67562cd6-c598-4c37-af53-626f153c0197.png)
  
6. <span data-ttu-id="46c5b-276">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46c5b-276">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/0d7ec216-9277-4709-b637-e94c8662730f.png)
  
7. <span data-ttu-id="46c5b-278">À l'aide des trois étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="46c5b-278">Using the preceding three steps and the values from the second row in the table, add the other SRV record.</span></span>
    
> [!NOTE]
> <span data-ttu-id="46c5b-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="46c5b-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
