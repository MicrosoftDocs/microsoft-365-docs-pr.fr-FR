---
title: Créer des enregistrements DNS sur NetRegistry pour Microsoft
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
- BEA160
ms.assetid: 48e09394-2287-4b3c-9853-21eadf61277e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur NetRegistry pour Microsoft.
ms.openlocfilehash: ed3e3bae232dcbb3c8e4eea3d1a3bc4dd0a88799
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939154"
---
# <a name="create-dns-records-at-netregistry-for-microsoft"></a><span data-ttu-id="324ca-103">Créer des enregistrements DNS sur NetRegistry pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-103">Create DNS records at Netregistry for Microsoft</span></span>

<span data-ttu-id="324ca-104">[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="324ca-104">[Check the Domains FAQ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="324ca-105">Si NetRegistry est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="324ca-105">If Netregistry is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="324ca-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="324ca-106">These are the main records to add.</span></span>
  
- [<span data-ttu-id="324ca-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="324ca-107">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="324ca-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)

- [<span data-ttu-id="324ca-109">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-109">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="324ca-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="324ca-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="324ca-111">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="324ca-112">Une fois ces enregistrements ajoutés sur NetRegistry, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="324ca-112">After you add these records at Netregistry, your domain will be set up to work with Microsoft services.</span></span>
  
  
> [!NOTE]
> <span data-ttu-id="324ca-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="324ca-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="324ca-116">Add a TXT record for verification</span></span>
<span data-ttu-id="324ca-117"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="324ca-117"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="324ca-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="324ca-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="324ca-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="324ca-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="324ca-122">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="324ca-122">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="324ca-123">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="324ca-123">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../../media/ed3c785f-01c3-49e7-affd-c04637c0ffe9.png)
  
2. <span data-ttu-id="324ca-125">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="324ca-125">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../../media/64ad542a-5ec4-4148-96f8-d6e163449352.png)
  
3. <span data-ttu-id="324ca-127">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="324ca-127">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../../media/e18c32f9-c1e7-4aa2-9aa6-8dc9c5ea44af.png)
  
4. <span data-ttu-id="324ca-129">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement txt** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-129">Under **Add a zone record**, choose **TXT Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_TXT_select](../../media/eb1761e6-9deb-4631-8deb-bc5d09926722.png)
  
    > [!NOTE]
    > <span data-ttu-id="324ca-131">Vous devez utiliser des guillemets avant et après l’entrée dans la zone TXT.</span><span class="sxs-lookup"><span data-stu-id="324ca-131">You must use quotation marks before and after the entry in the TXT box.</span></span> 
  
    <span data-ttu-id="324ca-132">Dans le **nouveau formulaire d’enregistrement txt** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="324ca-132">In the **New TXT Record** form, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="324ca-133">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="324ca-133">**Name**</span></span>|<span data-ttu-id="324ca-134">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="324ca-134">**TTL (SEC)**</span></span>|<span data-ttu-id="324ca-135">**TXT (pointe vers l’adresse ou la valeur)**</span><span class="sxs-lookup"><span data-stu-id="324ca-135">**TXT (Points to address or value)**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="324ca-136">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="324ca-136">(leave blank)</span></span>  <br/> |<span data-ttu-id="324ca-137">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-137">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-138">« MS = msXXXXXXXX »</span><span class="sxs-lookup"><span data-stu-id="324ca-138">"MS=msXXXXXXXX"</span></span>  <br/> <span data-ttu-id="324ca-139">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="324ca-139">**Note:** This is an example.</span></span> <span data-ttu-id="324ca-140">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="324ca-140">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="324ca-141">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="324ca-141">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  |
       
    ![Netregistry_verificationTXTvalues](../../media/cfe8b05a-fa8b-4dba-9554-7a3466e6c012.png)
  
6. <span data-ttu-id="324ca-143">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-143">Select **Add record**.</span></span>
    
<span data-ttu-id="324ca-144">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="324ca-144">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="324ca-145">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="324ca-145">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="324ca-146">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="324ca-146">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="324ca-147">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="324ca-147">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="324ca-148">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="324ca-148">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="324ca-149">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="324ca-149">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="324ca-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="324ca-153">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-153">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="324ca-154"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="324ca-154"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="324ca-155">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="324ca-155">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="324ca-156">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="324ca-156">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../../media/80277b0e-547e-4635-aa6a-5d8ebe3fba85.png)
  
2. <span data-ttu-id="324ca-158">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="324ca-158">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../../media/96e2c6e4-21fd-4405-a4fe-b1188400b985.png)
  
3. <span data-ttu-id="324ca-160">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="324ca-160">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../../media/914021f6-dff3-4640-84d6-b83cf8f61cf1.png)
  
4. <span data-ttu-id="324ca-162">Sous **enregistrements de la zone actuelle**, supprimez les enregistrements MX par défaut en sélectionnant **supprimer** en regard de chaque enregistrement MX de la liste.</span><span class="sxs-lookup"><span data-stu-id="324ca-162">Under **Current zone records**, remove the default MX records by selecting **Remove** next to each MX record in the list.</span></span> 
    
    ![Netregistry_MX_remove](../../media/494670a9-8b8d-46e5-8136-05e82212a115.png)
  
5. <span data-ttu-id="324ca-164">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement MX** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-164">Under **Add a zone record**, choose **MX Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_MX_select](../../media/29b60eb9-6c40-490f-9669-e65b65962f37.png)
  
6. <span data-ttu-id="324ca-166">Dans le **nouveau formulaire d’enregistrement MX** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="324ca-166">In the **New MX Record** form, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="324ca-167">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="324ca-167">**Name**</span></span>|<span data-ttu-id="324ca-168">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="324ca-168">**TTL (SEC)**</span></span>|<span data-ttu-id="324ca-169">**Exchange (pointe vers l’adresse ou la valeur)**</span><span class="sxs-lookup"><span data-stu-id="324ca-169">**Exchange (Points to address or value)**</span></span>|<span data-ttu-id="324ca-170">**L’hôte est-il entièrement qualifié ?**</span><span class="sxs-lookup"><span data-stu-id="324ca-170">**Is host fully qualified?**</span></span>|<span data-ttu-id="324ca-171">**Préférence (priorité)**</span><span class="sxs-lookup"><span data-stu-id="324ca-171">**Preference (Priority)**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="324ca-172">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="324ca-172">(leave blank)</span></span>  <br/> |<span data-ttu-id="324ca-173">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-173">3600 (seconds)</span></span>  <br/> | <span data-ttu-id="324ca-174">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="324ca-174">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="324ca-175">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="324ca-175">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="324ca-176">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="324ca-176">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)      |<span data-ttu-id="324ca-177">(cochez la case)</span><span class="sxs-lookup"><span data-stu-id="324ca-177">(select the checkbox)</span></span>  <br/> |<span data-ttu-id="324ca-178">10 </span><span class="sxs-lookup"><span data-stu-id="324ca-178">10</span></span>  <br/> <span data-ttu-id="324ca-179">For more information about priority, see What is MX priority?</span><span class="sxs-lookup"><span data-stu-id="324ca-179">For more information about priority, see What is MX priority?</span></span>  <br/> |
       
    ![Netregistry_MX_values](../../media/518b3da6-4055-4e2d-b5ce-44a0fee25419.png)
  
7. <span data-ttu-id="324ca-181">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-181">Select **Add Record**.</span></span>
    
    ![Netregistry_MX_values_AddRecord](../../media/8194cb38-afa0-48ac-831c-fd34b6ad652e.png)
  
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="324ca-183">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-183">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="324ca-184"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="324ca-184"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="324ca-185">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="324ca-185">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="324ca-186">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="324ca-186">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../../media/cbf83dce-86d2-4008-9400-56def4b6fcd7.png)
  
2. <span data-ttu-id="324ca-188">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="324ca-188">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../../media/7bee4b0f-2c1d-43ca-b1bb-9b889ca0c5e4.png)
  
3. <span data-ttu-id="324ca-190">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="324ca-190">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../../media/58384add-0a9d-472b-a5d0-51ec8155fd41.png)
  
4. <span data-ttu-id="324ca-192">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement CNAME** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-192">Under  **Add a zone record**, choose **CNAME Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_CNAME_CreateNewRecord](../../media/7b4f133f-45da-48da-93c0-62f57c786165.png)
  
5. <span data-ttu-id="324ca-194">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="324ca-194">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="324ca-195">**Name**</span><span class="sxs-lookup"><span data-stu-id="324ca-195">**Name**</span></span>|<span data-ttu-id="324ca-196">**Type**</span><span class="sxs-lookup"><span data-stu-id="324ca-196">**Type**</span></span>|<span data-ttu-id="324ca-197">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="324ca-197">**TTL**</span></span>|<span data-ttu-id="324ca-198">**HÔTE (pointe vers ou adresse)**</span><span class="sxs-lookup"><span data-stu-id="324ca-198">**HOST (Points to or address value)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="324ca-199">autodiscover</span><span class="sxs-lookup"><span data-stu-id="324ca-199">autodiscover</span></span>  <br/> |<span data-ttu-id="324ca-200">CNAME</span><span class="sxs-lookup"><span data-stu-id="324ca-200">CNAME</span></span>  <br/> |<span data-ttu-id="324ca-201">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-201">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-202">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="324ca-202">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="324ca-203">sip</span><span class="sxs-lookup"><span data-stu-id="324ca-203">sip</span></span>  <br/> |<span data-ttu-id="324ca-204">CNAME</span><span class="sxs-lookup"><span data-stu-id="324ca-204">CNAME</span></span>  <br/> |<span data-ttu-id="324ca-205">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-205">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-206">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="324ca-206">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="324ca-207">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="324ca-207">lyncdiscover</span></span>  <br/> |<span data-ttu-id="324ca-208">CNAME</span><span class="sxs-lookup"><span data-stu-id="324ca-208">CNAME</span></span>  <br/> |<span data-ttu-id="324ca-209">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-209">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-210">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="324ca-210">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="324ca-211">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="324ca-211">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="324ca-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="324ca-212">CNAME</span></span>  <br/> |<span data-ttu-id="324ca-213">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-213">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-214">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="324ca-214">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="324ca-215">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="324ca-215">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="324ca-216">CNAME</span><span class="sxs-lookup"><span data-stu-id="324ca-216">CNAME</span></span>  <br/> |<span data-ttu-id="324ca-217">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-217">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-218">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="324ca-218">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
       
    ![Netregistry_CNAME_values](../../media/93c479f0-3ce2-491a-9113-6dde1cd7131b.png)
      
6. <span data-ttu-id="324ca-220">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-220">Select **Add record**.</span></span>
    
    ![Netregistry_CNAME_values_AddRecord](../../media/046c8c64-ea71-4530-9fc6-69f0c70993b6.png)
  
7. <span data-ttu-id="324ca-222">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="324ca-222">Repeat the previous steps to create the other five CNAME records.</span></span>
    
    <span data-ttu-id="324ca-223">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="324ca-223">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="324ca-224">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="324ca-224">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="324ca-225"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="324ca-225"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="324ca-226">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="324ca-226">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="324ca-227">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="324ca-227">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="324ca-228">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="324ca-228">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="324ca-229">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="324ca-229">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="324ca-230">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="324ca-230">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="324ca-231">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="324ca-231">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../../media/a841f11f-1c0f-4926-acea-a2b8bb083984.png)
  
2. <span data-ttu-id="324ca-233">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="324ca-233">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../../media/4245bbbb-4e2d-49e7-a89c-679949aa3d18.png)
  
3. <span data-ttu-id="324ca-235">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="324ca-235">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../../media/372e5918-b6dc-4268-8f9a-0aa71d65deef.png)
  
4. <span data-ttu-id="324ca-237">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement txt** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-237">Under **Add a zone record**, choose **TXT Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_TXT_select](../../media/a2930d03-853a-4f1e-9205-d00f25bed35f.png)
  
5. <span data-ttu-id="324ca-239">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="324ca-239">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="324ca-240">Vous devez utiliser des guillemets avant et après l’entrée dans la zone TXT.</span><span class="sxs-lookup"><span data-stu-id="324ca-240">You must use quotation marks before and after the entry in the TXT box.</span></span> 
  
    |<span data-ttu-id="324ca-241">**Name**</span><span class="sxs-lookup"><span data-stu-id="324ca-241">**Name**</span></span>|<span data-ttu-id="324ca-242">**Type**</span><span class="sxs-lookup"><span data-stu-id="324ca-242">**Type**</span></span>|<span data-ttu-id="324ca-243">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="324ca-243">**TTL**</span></span>|<span data-ttu-id="324ca-244">**Données TXT (cible)**</span><span class="sxs-lookup"><span data-stu-id="324ca-244">**TXT Data (Target)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="324ca-245">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="324ca-245">(leave blank)</span></span>  <br/> |<span data-ttu-id="324ca-246">TXT</span><span class="sxs-lookup"><span data-stu-id="324ca-246">TXT</span></span>  <br/> |<span data-ttu-id="324ca-247">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-247">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-248">"v = spf1 include include. protection. Outlook. com-All"</span><span class="sxs-lookup"><span data-stu-id="324ca-248">"v=spf1 include:spf.protection.outlook.com -all"</span></span>  <br/> <span data-ttu-id="324ca-249">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="324ca-249">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Netregistry_SPF-TXTvalues](../../media/a369345a-d774-48bc-8160-b628ab8247f9.png)
  
6. <span data-ttu-id="324ca-251">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-251">Select **Add Record**.</span></span>
    
    ![Netregistry_SPF-TXTvalues_AddRecord](../../media/063bfbaf-940a-489f-970f-29c026b4b312.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="324ca-253">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="324ca-253">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="324ca-254"><a name="bkmk_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="324ca-254"><a name="bkmk_srv"> </a></span></span>

1. <span data-ttu-id="324ca-255">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="324ca-255">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="324ca-256">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="324ca-256">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../../media/accf6584-e5f4-4d68-a641-0f8847f8370f.png)
  
2. <span data-ttu-id="324ca-258">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="324ca-258">Next to the domain you want to manage, select  **Manage**.</span></span>
    
    ![Netregistry_Manage](../../media/e0ddc79e-0123-4e24-8380-9645bdb41aac.png)
  
3. <span data-ttu-id="324ca-260">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="324ca-260">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../../media/f122888b-3cc5-40ec-adac-0ede04799d9a.png)
  
4. <span data-ttu-id="324ca-262">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement SRV** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-262">Under  **Add a zone record**, choose **SRV Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_SRV_select](../../media/e5dab850-acd1-48b8-8b4a-e3b9777cf508.png)
  
5. <span data-ttu-id="324ca-264">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="324ca-264">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="324ca-265">Le champ nom est une combinaison du service (par exemple, _sip) et protocole (par exemple, _tls).</span><span class="sxs-lookup"><span data-stu-id="324ca-265">The Name field is a combination of the service (for example, _sip) and protocol (for example, _tls).</span></span> 
  
    |<span data-ttu-id="324ca-266">**Type**</span><span class="sxs-lookup"><span data-stu-id="324ca-266">**Type**</span></span>|<span data-ttu-id="324ca-267">**Nom**</span><span class="sxs-lookup"><span data-stu-id="324ca-267">**Name**</span></span>|<span data-ttu-id="324ca-268">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="324ca-268">**TTL (SEC)**</span></span>|<span data-ttu-id="324ca-269">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="324ca-269">**Priority**</span></span>|<span data-ttu-id="324ca-270">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="324ca-270">**Weight**</span></span>|<span data-ttu-id="324ca-271">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="324ca-271">**Port**</span></span>|<span data-ttu-id="324ca-272">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="324ca-272">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="324ca-273">SRV (service)</span><span class="sxs-lookup"><span data-stu-id="324ca-273">SRV (service)</span></span>  <br/> |<span data-ttu-id="324ca-274">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="324ca-274">_sip._tls</span></span>  <br/> |<span data-ttu-id="324ca-275">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-275">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-276">100</span><span class="sxs-lookup"><span data-stu-id="324ca-276">100</span></span>  <br/> |<span data-ttu-id="324ca-277">0,1</span><span class="sxs-lookup"><span data-stu-id="324ca-277">1</span></span>  <br/> |<span data-ttu-id="324ca-278">443</span><span class="sxs-lookup"><span data-stu-id="324ca-278">443</span></span>  <br/> |<span data-ttu-id="324ca-279">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="324ca-279">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="324ca-280">SRV (service)</span><span class="sxs-lookup"><span data-stu-id="324ca-280">SRV (service)</span></span>  <br/> |<span data-ttu-id="324ca-281">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="324ca-281">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="324ca-282">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="324ca-282">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="324ca-283">100</span><span class="sxs-lookup"><span data-stu-id="324ca-283">100</span></span>  <br/> |<span data-ttu-id="324ca-284">0,1</span><span class="sxs-lookup"><span data-stu-id="324ca-284">1</span></span>  <br/> |<span data-ttu-id="324ca-285">5061</span><span class="sxs-lookup"><span data-stu-id="324ca-285">5061</span></span>  <br/> |<span data-ttu-id="324ca-286">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="324ca-286">sipfed.online.lync.com</span></span>  <br/> |
       
    ![Netregistry_SRV_values](../../media/49292846-1598-4b8c-9940-db6e10675753.png)
  
6. <span data-ttu-id="324ca-288">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="324ca-288">Select **Add Record**.</span></span>
    
    ![Netregistry_SRV_values_AddRecord](../../media/abc82061-939f-4757-87e4-0e8f9e43ebcb.png)
  
7. <span data-ttu-id="324ca-290">Répétez les étapes précédentes pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="324ca-290">Repeat the previous steps to create the other SRV record.</span></span>
    
    <span data-ttu-id="324ca-291">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="324ca-291">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
> [!NOTE]
> <span data-ttu-id="324ca-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

