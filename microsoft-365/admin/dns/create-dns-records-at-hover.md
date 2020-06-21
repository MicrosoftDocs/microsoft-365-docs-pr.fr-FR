---
title: Créer des enregistrements DNS sur le point de suspension pour Microsoft
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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 46ab4b10-6857-44b1-b08d-d1b5f45a69c6
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online et d’autres services sur le point de contrôle de Microsoft.
ms.openlocfilehash: e51cb77831f4e29ac3a51602a1bb19f8b0c9e0e3
ms.sourcegitcommit: 659adf65d88ee44f643c471e6202396f1ffb6576
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "44780348"
---
# <a name="create-dns-records-at-hover-for-microsoft"></a><span data-ttu-id="15470-103">Créer des enregistrements DNS sur le point de suspension pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="15470-103">Create DNS records at Hover for Microsoft</span></span>

 <span data-ttu-id="15470-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="15470-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="15470-105">Si Hover est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="15470-105">If Hover is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
     
<span data-ttu-id="15470-106">Une fois ces enregistrements ajoutés sur pointage, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15470-106">After you add these records at Hover, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
>  <span data-ttu-id="15470-107">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="15470-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="15470-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="15470-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="15470-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="15470-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="15470-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="15470-110">Add a TXT record for verification</span></span>
<span data-ttu-id="15470-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="15470-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="15470-112">Before you use your domain with Microsoft, we have to make sure that you own it.</span><span class="sxs-lookup"><span data-stu-id="15470-112">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="15470-113">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span><span class="sxs-lookup"><span data-stu-id="15470-113">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="15470-114">This record is used only to verify that you own your domain; it doesn't affect anything else.</span><span class="sxs-lookup"><span data-stu-id="15470-114">This record is used only to verify that you own your domain; it doesn't affect anything else.</span></span> <span data-ttu-id="15470-115">You can delete it later, if you like.</span><span class="sxs-lookup"><span data-stu-id="15470-115">You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="15470-116">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2)</span><span class="sxs-lookup"><span data-stu-id="15470-116">Follow the steps below or [watch the video](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2).</span></span>
  
1. <span data-ttu-id="15470-117">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span><span class="sxs-lookup"><span data-stu-id="15470-117">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span></span> <span data-ttu-id="15470-118">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="15470-118">You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="15470-120">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="15470-120">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="15470-122">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="15470-122">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="15470-124">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15470-124">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="15470-126">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="15470-126">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    ||||
    |:-----|:-----|:-----|
    |<span data-ttu-id="15470-127">Hostname (Nom d'hôte)</span><span class="sxs-lookup"><span data-stu-id="15470-127">Hostname</span></span>  <br/> |<span data-ttu-id="15470-128">Type d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="15470-128">Record Type</span></span>  <br/> |<span data-ttu-id="15470-129">Value (Valeur)</span><span class="sxs-lookup"><span data-stu-id="15470-129">Value</span></span>  <br/> |
    |@  <br/> |<span data-ttu-id="15470-130">TXT</span><span class="sxs-lookup"><span data-stu-id="15470-130">TXT</span></span>  <br/> |<span data-ttu-id="15470-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="15470-131">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="15470-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="15470-132">**Note:** This is an example.</span></span> <span data-ttu-id="15470-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="15470-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="15470-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="15470-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/3b0d19f9-4138-47a7-aab2-137ad120ded6.png)
  
6. <span data-ttu-id="15470-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="15470-136">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/07dcf68e-34be-47dc-999e-0216de68cc9c.png)
  
7. <span data-ttu-id="15470-138">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="15470-138">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="15470-139">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Microsoft 365 et demandez à Microsoft 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="15470-139">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="15470-140">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="15470-140">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="15470-141">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="15470-141">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="15470-142">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="15470-142">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="15470-143">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="15470-143">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="15470-144">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="15470-144">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="15470-145">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="15470-145">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="15470-146">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="15470-146">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="15470-147">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="15470-147">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="15470-148">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="15470-148">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="15470-149"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="15470-149"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="15470-150">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2)</span><span class="sxs-lookup"><span data-stu-id="15470-150">Follow the steps below or [watch the video](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2).</span></span>
  
1. <span data-ttu-id="15470-151">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span><span class="sxs-lookup"><span data-stu-id="15470-151">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span></span> <span data-ttu-id="15470-152">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="15470-152">You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="15470-154">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="15470-154">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="15470-156">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="15470-156">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="15470-158">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15470-158">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="15470-160">Dans les zones du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **MX**, puis tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15470-160">In the boxes for the new record, select **MX** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="15470-161">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="15470-161">**Hostname**</span></span>|<span data-ttu-id="15470-162">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="15470-162">**Record Type**</span></span>|<span data-ttu-id="15470-163">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="15470-163">**Priority**</span></span>|<span data-ttu-id="15470-164">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="15470-164">**Hostname**</span></span>|
    |:-----|:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="15470-165">MX</span><span class="sxs-lookup"><span data-stu-id="15470-165">MX</span></span>  <br/> |<span data-ttu-id="15470-166">0</span><span class="sxs-lookup"><span data-stu-id="15470-166">0</span></span>  <br/> <span data-ttu-id="15470-167">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="15470-167">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> | <span data-ttu-id="15470-168">*\<domain-key\>*. mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="15470-168">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="15470-169">**Remarque :** Obtenir votre *\<domain-key\>* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15470-169">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="15470-170">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="15470-170">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/2c8915fa-04a8-4d2a-a8ae-a79de0c8ef99.png)
  
6. <span data-ttu-id="15470-172">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="15470-172">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/266c30a4-6703-48fb-a919-b510ed966193.png)
  
7. <span data-ttu-id="15470-174">S'il existe d'autres enregistrements MX, utilisez le processus en deux étapes suivant pour supprimer chacun d'eux :</span><span class="sxs-lookup"><span data-stu-id="15470-174">If there are any other MX records, use the following two-step process to remove each of them:</span></span>
    
    <span data-ttu-id="15470-175">Tout d’abord, en plaçant le pointeur de la souris sur un enregistrement que vous souhaitez supprimer, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="15470-175">First, mousing over a record that you want to remove, select **Delete**.</span></span>
    
    ![Pointez avec la souris et sélectionnez Supprimer.](../../media/2ddf4902-8cd2-4969-a418-2cb592741e86.png)
  
    <span data-ttu-id="15470-177">Deuxièmement, sélectionnez **Oui** pour confirmer chaque suppression.</span><span class="sxs-lookup"><span data-stu-id="15470-177">Second, select **Yes** to confirm each deletion.</span></span> 
    
    ![Sélectionnez Oui pour confirmer la suppression](../../media/48756bd5-0205-4c4d-9803-9246795dbf4a.png)
  
    <span data-ttu-id="15470-179">Répétez cette procédure jusqu'à avoir supprimé tous les enregistrements MX à l'exception de celui que vous avez ajouté précédemment durant cette procédure.</span><span class="sxs-lookup"><span data-stu-id="15470-179">Repeat this process until you have deleted all MX records except for the one that you added earlier in this procedure.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="15470-180">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="15470-180">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="15470-181"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="15470-181"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="15470-182">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2)</span><span class="sxs-lookup"><span data-stu-id="15470-182">Follow the steps below or [watch the video](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2).</span></span>
  
1. <span data-ttu-id="15470-183">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span><span class="sxs-lookup"><span data-stu-id="15470-183">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span></span> <span data-ttu-id="15470-184">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="15470-184">You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="15470-186">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="15470-186">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="15470-188">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="15470-188">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="15470-190">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="15470-190">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="15470-191">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15470-191">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="15470-193">Dans les zones vides du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **CNAME**, puis tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15470-193">In the empty boxes for the new record, select **CNAME** for the **Record Type**, and then type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="15470-194">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="15470-194">**Hostname**</span></span>|<span data-ttu-id="15470-195">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="15470-195">**Record Type**</span></span>|<span data-ttu-id="15470-196">**Target Host (Hôte cible)**</span><span class="sxs-lookup"><span data-stu-id="15470-196">**Target Host**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="15470-197">autodiscover</span><span class="sxs-lookup"><span data-stu-id="15470-197">autodiscover</span></span>  <br/> |<span data-ttu-id="15470-198">CNAME</span><span class="sxs-lookup"><span data-stu-id="15470-198">CNAME</span></span>  <br/> |<span data-ttu-id="15470-199">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="15470-199">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="15470-200">sip</span><span class="sxs-lookup"><span data-stu-id="15470-200">sip</span></span>  <br/> |<span data-ttu-id="15470-201">CNAME</span><span class="sxs-lookup"><span data-stu-id="15470-201">CNAME</span></span>  <br/> |<span data-ttu-id="15470-202">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="15470-202">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="15470-203">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="15470-203">lyncdiscover</span></span>  <br/> |<span data-ttu-id="15470-204">CNAME</span><span class="sxs-lookup"><span data-stu-id="15470-204">CNAME</span></span>  <br/> |<span data-ttu-id="15470-205">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="15470-205">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="15470-206">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="15470-206">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="15470-207">CNAME</span><span class="sxs-lookup"><span data-stu-id="15470-207">CNAME</span></span>  <br/> |<span data-ttu-id="15470-208">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="15470-208">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="15470-209">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="15470-209">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="15470-210">CNAME</span><span class="sxs-lookup"><span data-stu-id="15470-210">CNAME</span></span>  <br/> |<span data-ttu-id="15470-211">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="15470-211">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/6ae607f8-d26e-47f0-a0f2-3487d37e8c7f.png)
  
6. <span data-ttu-id="15470-213">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="15470-213">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/69aa3546-32de-4c17-a2e2-8c0cd133efaa.png)
  
7. <span data-ttu-id="15470-215">En suivant les trois étapes précédentes et en utilisant les valeurs des cinq autres lignes du tableau, ajoutez les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="15470-215">Using the preceding three steps and the values from the other five rows in the table, add each of the other five CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="15470-216">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="15470-216">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="15470-217"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="15470-217"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="15470-218">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="15470-218">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="15470-219">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="15470-219">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="15470-220">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15470-220">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="15470-221">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="15470-221">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
<span data-ttu-id="15470-222">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2)</span><span class="sxs-lookup"><span data-stu-id="15470-222">Follow the steps below or [watch the video](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2).</span></span>
  
1. <span data-ttu-id="15470-223">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span><span class="sxs-lookup"><span data-stu-id="15470-223">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span></span> <span data-ttu-id="15470-224">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="15470-224">You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="15470-226">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="15470-226">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="15470-228">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="15470-228">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="15470-230">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15470-230">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="15470-232">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="15470-232">In the boxes for the new record, select **TXT** for the **Record Type**, and then type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="15470-233">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="15470-233">**Hostname**</span></span>|<span data-ttu-id="15470-234">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="15470-234">**Record Type**</span></span>|<span data-ttu-id="15470-235">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="15470-235">**Value**</span></span>|
    |:-----|:-----|:-----|
    |@  <br/> |<span data-ttu-id="15470-236">TXT</span><span class="sxs-lookup"><span data-stu-id="15470-236">TXT</span></span>  <br/> |<span data-ttu-id="15470-237">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="15470-237">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/><span data-ttu-id="15470-238">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="15470-238">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/ed36b9e0-aaa9-45fb-804d-7d4e82ba0c7f.png)
  
6. <span data-ttu-id="15470-240">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="15470-240">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/13a395b9-e0e8-4393-b568-5f99b2da39da.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="15470-242">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="15470-242">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="15470-243"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="15470-243"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="15470-244">Suivez les étapes ci-dessous ou [regardez la vidéo](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2)</span><span class="sxs-lookup"><span data-stu-id="15470-244">Follow the steps below or [watch the video](https://support.microsoft.com/office/182bd58e-8fe4-4717-9233-3a3546b72ad2).</span></span>
  
1. <span data-ttu-id="15470-245">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span><span class="sxs-lookup"><span data-stu-id="15470-245">To get started, go to your domains page at Hover by using [this link](https://www.hover.com/domains).</span></span> <span data-ttu-id="15470-246">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="15470-246">You'll be prompted to sign in.</span></span>
    
    ![Connexion](../../media/f608cfaa-4962-46a1-a469-89010494e4be.png)
  
2. <span data-ttu-id="15470-248">Sous **gérer vos domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="15470-248">Under **Manage Your Domains**, select the name of the domain that you want to edit.</span></span>
    
    ![Sélectionner un domaine](../../media/ae7c1c46-7ad5-467a-b41c-077c90018989.png)
  
3. <span data-ttu-id="15470-250">Sélectionnez l’onglet **DNS** .</span><span class="sxs-lookup"><span data-stu-id="15470-250">Select the **DNS** tab.</span></span> 
    
    ![Sélectionnez l’onglet DNS](../../media/bd727fb4-0b06-426d-9387-42a160aead42.png)
  
4. <span data-ttu-id="15470-252">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="15470-252">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="15470-253">Sélectionnez **Ajouter un nouveau**.</span><span class="sxs-lookup"><span data-stu-id="15470-253">Select **Add New**.</span></span>
    
    ![Sélectionnez Ajouter un nouveau](../../media/66d6b2c9-741e-40e0-a096-6e7e204d655d.png)
  
5. <span data-ttu-id="15470-255">Dans les zones vides du nouvel enregistrement, sélectionnez le **Type d'enregistrement** **SRV**, puis tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="15470-255">In the empty boxes for the new record, select **SRV** for the **Record Type**, and then type or copy and paste the values from the first row in the following table.</span></span>
    
    |<span data-ttu-id="15470-256">**Hostname (Nom d'hôte)**</span><span class="sxs-lookup"><span data-stu-id="15470-256">**Hostname**</span></span>|<span data-ttu-id="15470-257">**Record Type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="15470-257">**Record Type**</span></span>|<span data-ttu-id="15470-258">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="15470-258">**Priority**</span></span>|<span data-ttu-id="15470-259">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="15470-259">**Weight**</span></span>|<span data-ttu-id="15470-260">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="15470-260">**Port**</span></span>|<span data-ttu-id="15470-261">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="15470-261">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="15470-262">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="15470-262">_sip._tls</span></span>  <br/> |<span data-ttu-id="15470-263">SRV</span><span class="sxs-lookup"><span data-stu-id="15470-263">SRV</span></span>  <br/> |<span data-ttu-id="15470-264">100</span><span class="sxs-lookup"><span data-stu-id="15470-264">100</span></span>  <br/> |<span data-ttu-id="15470-265">1 </span><span class="sxs-lookup"><span data-stu-id="15470-265">1</span></span>  <br/> |<span data-ttu-id="15470-266">443</span><span class="sxs-lookup"><span data-stu-id="15470-266">443</span></span>  <br/> |<span data-ttu-id="15470-267">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="15470-267">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="15470-268">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="15470-268">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="15470-269">SRV</span><span class="sxs-lookup"><span data-stu-id="15470-269">SRV</span></span>  <br/> |<span data-ttu-id="15470-270">100</span><span class="sxs-lookup"><span data-stu-id="15470-270">100</span></span>  <br/> |<span data-ttu-id="15470-271">1 </span><span class="sxs-lookup"><span data-stu-id="15470-271">1</span></span>  <br/> |<span data-ttu-id="15470-272">5061</span><span class="sxs-lookup"><span data-stu-id="15470-272">5061</span></span>  <br/> |<span data-ttu-id="15470-273">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="15470-273">sipfed.online.lync.com</span></span>  <br/> |
   
    ![Tapez ou copiez-collez les valeurs DNS](../../media/67562cd6-c598-4c37-af53-626f153c0197.png)
  
6. <span data-ttu-id="15470-275">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="15470-275">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer.](../../media/0d7ec216-9277-4709-b637-e94c8662730f.png)
  
7. <span data-ttu-id="15470-277">À l'aide des trois étapes précédentes et des valeurs de la deuxième ligne du tableau, ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="15470-277">Using the preceding three steps and the values from the second row in the table, add the other SRV record.</span></span>
    
> [!NOTE]
> <span data-ttu-id="15470-278">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="15470-278">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="15470-279">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="15470-279">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="15470-280">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="15470-280">If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
