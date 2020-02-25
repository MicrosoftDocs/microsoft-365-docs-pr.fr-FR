---
title: Créer des enregistrements DNS dans NetRegistry pour Office 365
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
- BEA160
ms.assetid: 48e09394-2287-4b3c-9853-21eadf61277e
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur NetRegistry pour Office 365.
ms.openlocfilehash: de4e16fa20f950edef8d30b4c6d02214e3753b9c
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42252610"
---
# <a name="create-dns-records-at-netregistry-for-office-365"></a><span data-ttu-id="9f59e-103">Créer des enregistrements DNS dans NetRegistry pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-103">Create DNS records at Netregistry for Office 365</span></span>

<span data-ttu-id="9f59e-104">[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="9f59e-104">[Check the Domains FAQ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="9f59e-105">Si NetRegistry est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="9f59e-105">If Netregistry is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="9f59e-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="9f59e-106">These are the main records to add.</span></span>
  
- [<span data-ttu-id="9f59e-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="9f59e-107">Add a TXT record for verification</span></span>](#add-a-txt-record-for-verification)
    
- [<span data-ttu-id="9f59e-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-108">Add an MX record so email for your domain will come to Office 365</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)

- [<span data-ttu-id="9f59e-109">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-109">Add the CNAME records that are required for Office 365</span></span>](#add-the-cname-records-that-are-required-for-office-365)
    
- [<span data-ttu-id="9f59e-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="9f59e-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="9f59e-111">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-111">Add the two SRV records that are required for Office 365</span></span>](#add-the-two-srv-records-that-are-required-for-office-365)
    
<span data-ttu-id="9f59e-112">Une fois ces enregistrements ajoutés sur NetRegistry, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f59e-112">After you add these records at Netregistry, your domain will be set up to work with Office 365 services.</span></span>
  
<span data-ttu-id="9f59e-113">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f59e-113">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f59e-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="9f59e-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="9f59e-117">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="9f59e-117">Add a TXT record for verification</span></span>
<span data-ttu-id="9f59e-118"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="9f59e-118"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="9f59e-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="9f59e-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f59e-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9f59e-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="9f59e-123">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="9f59e-123">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="9f59e-124">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="9f59e-124">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../media/ed3c785f-01c3-49e7-affd-c04637c0ffe9.png)
  
2. <span data-ttu-id="9f59e-126">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-126">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../media/64ad542a-5ec4-4148-96f8-d6e163449352.png)
  
3. <span data-ttu-id="9f59e-128">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-128">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../media/e18c32f9-c1e7-4aa2-9aa6-8dc9c5ea44af.png)
  
4. <span data-ttu-id="9f59e-130">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement txt** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-130">Under **Add a zone record**, choose **TXT Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_TXT_select](../media/eb1761e6-9deb-4631-8deb-bc5d09926722.png)
  
    > [!NOTE]
    > <span data-ttu-id="9f59e-132">Vous devez utiliser des guillemets avant et après l’entrée dans la zone TXT.</span><span class="sxs-lookup"><span data-stu-id="9f59e-132">You must use quotation marks before and after the entry in the TXT box.</span></span> 
  
    <span data-ttu-id="9f59e-133">Dans le **nouveau formulaire d’enregistrement txt** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f59e-133">In the **New TXT Record** form, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="9f59e-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f59e-134">**Name**</span></span>|<span data-ttu-id="9f59e-135">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-135">**TTL (SEC)**</span></span>|<span data-ttu-id="9f59e-136">**TXT (pointe vers l’adresse ou la valeur)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-136">**TXT (Points to address or value)**</span></span>|
    |:-----|:-----|:-----|
    |<span data-ttu-id="9f59e-137">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="9f59e-137">(leave blank)</span></span>  <br/> |<span data-ttu-id="9f59e-138">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-138">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-139">« MS = msXXXXXXXX »</span><span class="sxs-lookup"><span data-stu-id="9f59e-139">"MS=msXXXXXXXX"</span></span>  <br/> <span data-ttu-id="9f59e-140">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9f59e-140">**Note:** This is an example.</span></span> <span data-ttu-id="9f59e-141">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f59e-141">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="9f59e-142">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="9f59e-142">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  |
       
    ![Netregistry_verificationTXTvalues](../media/cfe8b05a-fa8b-4dba-9554-7a3466e6c012.png)
  
6. <span data-ttu-id="9f59e-144">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-144">Select **Add record**.</span></span>
    
<span data-ttu-id="9f59e-145">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="9f59e-145">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="9f59e-146">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="9f59e-146">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="9f59e-147">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="9f59e-147">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="9f59e-148">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="9f59e-148">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="9f59e-149">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-149">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="9f59e-150">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-150">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="9f59e-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="9f59e-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="9f59e-154">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-154">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="9f59e-155"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="9f59e-155"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="9f59e-156">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="9f59e-156">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="9f59e-157">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="9f59e-157">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../media/80277b0e-547e-4635-aa6a-5d8ebe3fba85.png)
  
2. <span data-ttu-id="9f59e-159">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-159">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../media/96e2c6e4-21fd-4405-a4fe-b1188400b985.png)
  
3. <span data-ttu-id="9f59e-161">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-161">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../media/914021f6-dff3-4640-84d6-b83cf8f61cf1.png)
  
4. <span data-ttu-id="9f59e-163">Sous **enregistrements de la zone actuelle**, supprimez les enregistrements MX par défaut en sélectionnant **supprimer** en regard de chaque enregistrement MX de la liste.</span><span class="sxs-lookup"><span data-stu-id="9f59e-163">Under **Current zone records**, remove the default MX records by selecting **Remove** next to each MX record in the list.</span></span> 
    
    ![Netregistry_MX_remove](../media/494670a9-8b8d-46e5-8136-05e82212a115.png)
  
5. <span data-ttu-id="9f59e-165">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement MX** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-165">Under **Add a zone record**, choose **MX Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_MX_select](../media/29b60eb9-6c40-490f-9669-e65b65962f37.png)
  
6. <span data-ttu-id="9f59e-167">Dans le **nouveau formulaire d’enregistrement MX** , tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f59e-167">In the **New MX Record** form, type or copy and paste the values from the following table.</span></span> 
    
    |<span data-ttu-id="9f59e-168">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f59e-168">**Name**</span></span>|<span data-ttu-id="9f59e-169">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-169">**TTL (SEC)**</span></span>|<span data-ttu-id="9f59e-170">**Exchange (pointe vers l’adresse ou la valeur)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-170">**Exchange (Points to address or value)**</span></span>|<span data-ttu-id="9f59e-171">**L’hôte est-il entièrement qualifié ?**</span><span class="sxs-lookup"><span data-stu-id="9f59e-171">**Is host fully qualified?**</span></span>|<span data-ttu-id="9f59e-172">**Préférence (priorité)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-172">**Preference (Priority)**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="9f59e-173">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="9f59e-173">(leave blank)</span></span>  <br/> |<span data-ttu-id="9f59e-174">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-174">3600 (seconds)</span></span>  <br/> | <span data-ttu-id="9f59e-175">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-175">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="9f59e-176">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f59e-176">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>  [<span data-ttu-id="9f59e-177">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="9f59e-177">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)      |<span data-ttu-id="9f59e-178">(cochez la case)</span><span class="sxs-lookup"><span data-stu-id="9f59e-178">(select the checkbox)</span></span>  <br/> |<span data-ttu-id="9f59e-179">10 </span><span class="sxs-lookup"><span data-stu-id="9f59e-179">10</span></span>  <br/> <span data-ttu-id="9f59e-180">For more information about priority, see What is MX priority?</span><span class="sxs-lookup"><span data-stu-id="9f59e-180">For more information about priority, see What is MX priority?</span></span>  <br/> |
       
    ![Netregistry_MX_values](../media/518b3da6-4055-4e2d-b5ce-44a0fee25419.png)
  
7. <span data-ttu-id="9f59e-182">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-182">Select **Add Record**.</span></span>
    
    ![Netregistry_MX_values_AddRecord](../media/8194cb38-afa0-48ac-831c-fd34b6ad652e.png)
  
## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="9f59e-184">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-184">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="9f59e-185"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="9f59e-185"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="9f59e-186">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="9f59e-186">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="9f59e-187">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="9f59e-187">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../media/cbf83dce-86d2-4008-9400-56def4b6fcd7.png)
  
2. <span data-ttu-id="9f59e-189">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-189">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../media/7bee4b0f-2c1d-43ca-b1bb-9b889ca0c5e4.png)
  
3. <span data-ttu-id="9f59e-191">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-191">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../media/58384add-0a9d-472b-a5d0-51ec8155fd41.png)
  
4. <span data-ttu-id="9f59e-193">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement CNAME** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-193">Under  **Add a zone record**, choose **CNAME Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_CNAME_CreateNewRecord](../media/7b4f133f-45da-48da-93c0-62f57c786165.png)
  
5. <span data-ttu-id="9f59e-195">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="9f59e-195">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    |<span data-ttu-id="9f59e-196">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f59e-196">**Name**</span></span>|<span data-ttu-id="9f59e-197">**Type**</span><span class="sxs-lookup"><span data-stu-id="9f59e-197">**Type**</span></span>|<span data-ttu-id="9f59e-198">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-198">**TTL**</span></span>|<span data-ttu-id="9f59e-199">**HÔTE (pointe vers ou adresse)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-199">**HOST (Points to or address value)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="9f59e-200">autodiscover</span><span class="sxs-lookup"><span data-stu-id="9f59e-200">autodiscover</span></span>  <br/> |<span data-ttu-id="9f59e-201">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f59e-201">CNAME</span></span>  <br/> |<span data-ttu-id="9f59e-202">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-202">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-203">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-203">autodiscover.outlook.com</span></span>  <br/> |
    |<span data-ttu-id="9f59e-204">sip</span><span class="sxs-lookup"><span data-stu-id="9f59e-204">sip</span></span>  <br/> |<span data-ttu-id="9f59e-205">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f59e-205">CNAME</span></span>  <br/> |<span data-ttu-id="9f59e-206">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-206">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-207">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-207">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="9f59e-208">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="9f59e-208">lyncdiscover</span></span>  <br/> |<span data-ttu-id="9f59e-209">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f59e-209">CNAME</span></span>  <br/> |<span data-ttu-id="9f59e-210">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-210">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-211">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-211">webdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="9f59e-212">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="9f59e-212">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="9f59e-213">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f59e-213">CNAME</span></span>  <br/> |<span data-ttu-id="9f59e-214">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-214">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-215">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="9f59e-215">enterpriseregistration.windows.net</span></span>  <br/> |
    |<span data-ttu-id="9f59e-216">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="9f59e-216">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="9f59e-217">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f59e-217">CNAME</span></span>  <br/> |<span data-ttu-id="9f59e-218">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-218">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-219">enterpriseenrollment-s.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-219">enterpriseenrollment-s.manage.microsoft.com</span></span>  <br/> |
       
    ![Netregistry_CNAME_values](../media/93c479f0-3ce2-491a-9113-6dde1cd7131b.png)
      
6. <span data-ttu-id="9f59e-221">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-221">Select **Add record**.</span></span>
    
    ![Netregistry_CNAME_values_AddRecord](../media/046c8c64-ea71-4530-9fc6-69f0c70993b6.png)
  
7. <span data-ttu-id="9f59e-223">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="9f59e-223">Repeat the previous steps to create the other five CNAME records.</span></span>
    
    <span data-ttu-id="9f59e-224">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9f59e-224">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="9f59e-225">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="9f59e-225">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="9f59e-226"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="9f59e-226"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f59e-227">You cannot have more than one TXT record for SPF for a domain.</span><span class="sxs-lookup"><span data-stu-id="9f59e-227">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="9f59e-228">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span><span class="sxs-lookup"><span data-stu-id="9f59e-228">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="9f59e-229">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f59e-229">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="9f59e-230">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9f59e-230">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="9f59e-231">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="9f59e-231">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="9f59e-232">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="9f59e-232">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../media/a841f11f-1c0f-4926-acea-a2b8bb083984.png)
  
2. <span data-ttu-id="9f59e-234">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-234">Next to the domain you want to manage, select **Manage**.</span></span>
    
    ![Netregistry_Manage](../media/4245bbbb-4e2d-49e7-a89c-679949aa3d18.png)
  
3. <span data-ttu-id="9f59e-236">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-236">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../media/372e5918-b6dc-4268-8f9a-0aa71d65deef.png)
  
4. <span data-ttu-id="9f59e-238">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement txt** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-238">Under **Add a zone record**, choose **TXT Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_TXT_select](../media/a2930d03-853a-4f1e-9205-d00f25bed35f.png)
  
5. <span data-ttu-id="9f59e-240">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="9f59e-240">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9f59e-241">Vous devez utiliser des guillemets avant et après l’entrée dans la zone TXT.</span><span class="sxs-lookup"><span data-stu-id="9f59e-241">You must use quotation marks before and after the entry in the TXT box.</span></span> 
  
    |<span data-ttu-id="9f59e-242">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f59e-242">**Name**</span></span>|<span data-ttu-id="9f59e-243">**Type**</span><span class="sxs-lookup"><span data-stu-id="9f59e-243">**Type**</span></span>|<span data-ttu-id="9f59e-244">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-244">**TTL**</span></span>|<span data-ttu-id="9f59e-245">**Données TXT (cible)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-245">**TXT Data (Target)**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="9f59e-246">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="9f59e-246">(leave blank)</span></span>  <br/> |<span data-ttu-id="9f59e-247">TXT</span><span class="sxs-lookup"><span data-stu-id="9f59e-247">TXT</span></span>  <br/> |<span data-ttu-id="9f59e-248">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-248">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-249">"v = spf1 include include. protection. Outlook. com-All"</span><span class="sxs-lookup"><span data-stu-id="9f59e-249">"v=spf1 include:spf.protection.outlook.com -all"</span></span>  <br/> <span data-ttu-id="9f59e-250">**Remarque :** Nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="9f59e-250">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Netregistry_SPF-TXTvalues](../media/a369345a-d774-48bc-8160-b628ab8247f9.png)
  
6. <span data-ttu-id="9f59e-252">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-252">Select **Add Record**.</span></span>
    
    ![Netregistry_SPF-TXTvalues_AddRecord](../media/063bfbaf-940a-489f-970f-29c026b4b312.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="9f59e-254">Ajouter les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9f59e-254">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="9f59e-255"><a name="bkmk_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="9f59e-255"><a name="bkmk_srv"> </a></span></span>

1. <span data-ttu-id="9f59e-256">Pour commencer, accédez à la page de vos domaines dans NetRegistry en utilisant [ce lien](https://theconsole.netregistry.com.au/).</span><span class="sxs-lookup"><span data-stu-id="9f59e-256">To get started, go to your domains page in Netregistry by using [this link](https://theconsole.netregistry.com.au/).</span></span> <span data-ttu-id="9f59e-257">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="9f59e-257">You'll be prompted to log in.</span></span>
    
    ![Netregistry_login](../media/accf6584-e5f4-4d68-a641-0f8847f8370f.png)
  
2. <span data-ttu-id="9f59e-259">En regard du domaine que vous souhaitez gérer, sélectionnez **gérer**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-259">Next to the domain you want to manage, select  **Manage**.</span></span>
    
    ![Netregistry_Manage](../media/e0ddc79e-0123-4e24-8380-9645bdb41aac.png)
  
3. <span data-ttu-id="9f59e-261">Sélectionnez **Gestionnaire de zones**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-261">Select **Zone Manager**.</span></span>
    
    ![Netregistry_selectZoneManager](../media/f122888b-3cc5-40ec-adac-0ede04799d9a.png)
  
4. <span data-ttu-id="9f59e-263">Sous **Ajouter un enregistrement de zone**, choisissez **enregistrement SRV** dans la liste, puis sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-263">Under  **Add a zone record**, choose **SRV Record** from the list, and then select **Create new record**.</span></span>
    
    ![Netregistry_SRV_select](../media/e5dab850-acd1-48b8-8b4a-e3b9777cf508.png)
  
5. <span data-ttu-id="9f59e-265">In the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="9f59e-265">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9f59e-266">Le champ nom est une combinaison du service (par exemple, _sip) et protocole (par exemple, _tls).</span><span class="sxs-lookup"><span data-stu-id="9f59e-266">The Name field is a combination of the service (for example, _sip) and protocol (for example, _tls).</span></span> 
  
    |<span data-ttu-id="9f59e-267">**Type**</span><span class="sxs-lookup"><span data-stu-id="9f59e-267">**Type**</span></span>|<span data-ttu-id="9f59e-268">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9f59e-268">**Name**</span></span>|<span data-ttu-id="9f59e-269">**DURÉE DE VIE (S)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-269">**TTL (SEC)**</span></span>|<span data-ttu-id="9f59e-270">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-270">**Priority**</span></span>|<span data-ttu-id="9f59e-271">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-271">**Weight**</span></span>|<span data-ttu-id="9f59e-272">**Port**</span><span class="sxs-lookup"><span data-stu-id="9f59e-272">**Port**</span></span>|<span data-ttu-id="9f59e-273">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="9f59e-273">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="9f59e-274">SRV (service)</span><span class="sxs-lookup"><span data-stu-id="9f59e-274">SRV (service)</span></span>  <br/> |<span data-ttu-id="9f59e-275">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="9f59e-275">_sip._tls</span></span>  <br/> |<span data-ttu-id="9f59e-276">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-276">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-277">100</span><span class="sxs-lookup"><span data-stu-id="9f59e-277">100</span></span>  <br/> |<span data-ttu-id="9f59e-278">0,1</span><span class="sxs-lookup"><span data-stu-id="9f59e-278">1</span></span>  <br/> |<span data-ttu-id="9f59e-279">443</span><span class="sxs-lookup"><span data-stu-id="9f59e-279">443</span></span>  <br/> |<span data-ttu-id="9f59e-280">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-280">sipdir.online.lync.com</span></span>  <br/> |
    |<span data-ttu-id="9f59e-281">SRV (service)</span><span class="sxs-lookup"><span data-stu-id="9f59e-281">SRV (service)</span></span>  <br/> |<span data-ttu-id="9f59e-282">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="9f59e-282">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="9f59e-283">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="9f59e-283">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="9f59e-284">100</span><span class="sxs-lookup"><span data-stu-id="9f59e-284">100</span></span>  <br/> |<span data-ttu-id="9f59e-285">0,1</span><span class="sxs-lookup"><span data-stu-id="9f59e-285">1</span></span>  <br/> |<span data-ttu-id="9f59e-286">5061</span><span class="sxs-lookup"><span data-stu-id="9f59e-286">5061</span></span>  <br/> |<span data-ttu-id="9f59e-287">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="9f59e-287">sipfed.online.lync.com</span></span>  <br/> |
       
    ![Netregistry_SRV_values](../media/49292846-1598-4b8c-9940-db6e10675753.png)
  
6. <span data-ttu-id="9f59e-289">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="9f59e-289">Select **Add Record**.</span></span>
    
    ![Netregistry_SRV_values_AddRecord](../media/abc82061-939f-4757-87e4-0e8f9e43ebcb.png)
  
7. <span data-ttu-id="9f59e-291">Répétez les étapes précédentes pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="9f59e-291">Repeat the previous steps to create the other SRV record.</span></span>
    
    <span data-ttu-id="9f59e-292">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9f59e-292">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9f59e-p113">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="9f59e-p113">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  

