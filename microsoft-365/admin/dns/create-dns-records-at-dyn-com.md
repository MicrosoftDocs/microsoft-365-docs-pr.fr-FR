---
title: Créer des enregistrements DNS Dyn.com microsoft
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
ms.assetid: 34e57a00-2a7d-469c-beec-089423f18369
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur Dyn.com pour Microsoft.
ms.openlocfilehash: d1b77d6b4f38dd3e0979f448a77b293564841f45
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657935"
---
# <a name="create-dns-records-at-dyncom-for-microsoft"></a><span data-ttu-id="309fd-103">Créer des enregistrements DNS Dyn.com microsoft</span><span class="sxs-lookup"><span data-stu-id="309fd-103">Create DNS records at Dyn.com for Microsoft</span></span>

 <span data-ttu-id="309fd-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="309fd-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="309fd-105">Si Dyn.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="309fd-105">If Dyn.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
 

  
> [!NOTE]
>  <span data-ttu-id="309fd-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="309fd-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="309fd-109">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="309fd-109">Add a TXT record for verification</span></span>
<span data-ttu-id="309fd-110"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="309fd-110"><a name="BKMK_verify"> </a></span></span>

1. <span data-ttu-id="309fd-p102">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="309fd-p102">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="309fd-114">Dans la page **Services au niveau** de la zone, sélectionnez **Dyn Standard DNS Service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="309fd-114">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="309fd-115">Dans la page **DNS** de votre domaine, sélectionnez **Préférences.**</span><span class="sxs-lookup"><span data-stu-id="309fd-115">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="309fd-116">Sélectionnez **Activer l’interface experte.**</span><span class="sxs-lookup"><span data-stu-id="309fd-116">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="309fd-117">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="309fd-117">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="309fd-118">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="309fd-118">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="309fd-119">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="309fd-119">**Host**</span></span>|<span data-ttu-id="309fd-120">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="309fd-120">**TTL**</span></span>|<span data-ttu-id="309fd-121">**Type**</span><span class="sxs-lookup"><span data-stu-id="309fd-121">**Type**</span></span>|<span data-ttu-id="309fd-122">**Données**</span><span class="sxs-lookup"><span data-stu-id="309fd-122">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="309fd-123">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="309fd-123">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="309fd-124">600</span><span class="sxs-lookup"><span data-stu-id="309fd-124">600</span></span>  <br/> |<span data-ttu-id="309fd-125">TXT</span><span class="sxs-lookup"><span data-stu-id="309fd-125">TXT</span></span>  <br/> |<span data-ttu-id="309fd-126">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="309fd-126">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="309fd-127">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="309fd-127">**Note:** This is an example.</span></span> <span data-ttu-id="309fd-128">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="309fd-128">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="309fd-129">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="309fd-129">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![Dyn-BP-Verify-1-1](../../media/b3730b15-a313-4b4c-b91e-646eebb649e8.png)
  
6. <span data-ttu-id="309fd-131">Sélectionnez **Créer un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="309fd-131">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Verify-1-2](../../media/8b63b4ee-dbd7-44a7-b1e6-c6892b02f13e.png)
  
7. <span data-ttu-id="309fd-133">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="309fd-133">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="309fd-134">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="309fd-134">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="309fd-135">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="309fd-135">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="309fd-136">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="309fd-136">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="309fd-137">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="309fd-137">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="309fd-138">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="309fd-138">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="309fd-139">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="309fd-139">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="309fd-p104">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="309fd-p104">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="309fd-143">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="309fd-143">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="309fd-144"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="309fd-144"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="309fd-p105">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="309fd-p105">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="309fd-148">Dans la page **Services de niveau** de zone, sélectionnez **Dyn Standard DNS Service** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="309fd-148">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="309fd-149">Dans la page DNS de votre domaine, sélectionnez **Préférences.**</span><span class="sxs-lookup"><span data-stu-id="309fd-149">On the DNS page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="309fd-150">Sélectionnez **Activer l’interface experte.**</span><span class="sxs-lookup"><span data-stu-id="309fd-150">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="309fd-151">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="309fd-151">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="309fd-152">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="309fd-152">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="309fd-153">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="309fd-153">**Host**</span></span>|<span data-ttu-id="309fd-154">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="309fd-154">**TTL**</span></span>|<span data-ttu-id="309fd-155">**Type**</span><span class="sxs-lookup"><span data-stu-id="309fd-155">**Type**</span></span>|<span data-ttu-id="309fd-156">**Données**</span><span class="sxs-lookup"><span data-stu-id="309fd-156">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="309fd-157">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="309fd-157">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="309fd-158">600</span><span class="sxs-lookup"><span data-stu-id="309fd-158">600</span></span>  <br/> |<span data-ttu-id="309fd-159">MX</span><span class="sxs-lookup"><span data-stu-id="309fd-159">MX</span></span>  <br/> |<span data-ttu-id="309fd-160">10  *\<domain-key\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-160">10  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="309fd-161">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-161">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="309fd-p106">La valeur **10** représente la valeur de priorité MX. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par un espace.  </span><span class="sxs-lookup"><span data-stu-id="309fd-p106">The **10** is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="309fd-164">**Remarque :** Obtenez votre  *\<domain-key\>*  compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="309fd-164">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="309fd-165">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="309fd-165">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)      <br>    <span data-ttu-id="309fd-166">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="309fd-166">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |
   
    ![Dyn-BP-Configure-2-1](../../media/62ac77b7-c84d-426d-9ec4-a28d6479ad04.png)
  
6. <span data-ttu-id="309fd-168">Sélectionnez **Créer un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="309fd-168">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-2-2](../../media/e84e2cca-75e3-4584-8a98-f2f89cb71bd3.png)
  
7. <span data-ttu-id="309fd-170">Si d'autres enregistrements MX sont répertoriés, supprimez-les en activant la case à cocher correspondante dans la colonne **Delete (Supprimer)**.</span><span class="sxs-lookup"><span data-stu-id="309fd-170">If there are any other MX records, remove them by selecting the check box for each one in the **Delete** column.</span></span> 
    
    ![Dyn-BP-Configure-2-3](../../media/f24f02cc-c0b7-42cf-a2ff-4d0fc203e4de.png)
  
8. <span data-ttu-id="309fd-172">Sélectionnez **Appliquer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="309fd-172">Select **Apply Changes**.</span></span>
    
    ![Dyn-BP-Configure-2-4](../../media/0cc23c2b-b6f2-4f58-af20-4c6506de7b43.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="309fd-174">Ajouter les six enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="309fd-174">Add the six CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="309fd-175"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="309fd-175"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="309fd-p108">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="309fd-p108">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="309fd-179">Dans la page **Services au niveau** de la zone, sélectionnez **Dyn Standard DNS Service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="309fd-179">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="309fd-180">Dans la page **DNS** de votre domaine, sélectionnez **Préférences.**</span><span class="sxs-lookup"><span data-stu-id="309fd-180">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="309fd-181">Sélectionnez **Activer l’interface experte.**</span><span class="sxs-lookup"><span data-stu-id="309fd-181">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="309fd-182">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="309fd-182">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="309fd-183">Dans la section **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="309fd-183">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    <span data-ttu-id="309fd-184">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="309fd-184">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="309fd-185">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="309fd-185">**Host**</span></span>|<span data-ttu-id="309fd-186">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="309fd-186">**TTL**</span></span>|<span data-ttu-id="309fd-187">**Type**</span><span class="sxs-lookup"><span data-stu-id="309fd-187">**Type**</span></span>|<span data-ttu-id="309fd-188">**Données**</span><span class="sxs-lookup"><span data-stu-id="309fd-188">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="309fd-189">autodiscover</span><span class="sxs-lookup"><span data-stu-id="309fd-189">autodiscover</span></span>  <br/> |<span data-ttu-id="309fd-190">600</span><span class="sxs-lookup"><span data-stu-id="309fd-190">600</span></span>  <br/> |<span data-ttu-id="309fd-191">CNAME</span><span class="sxs-lookup"><span data-stu-id="309fd-191">CNAME</span></span>  <br/> |<span data-ttu-id="309fd-192">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-192">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="309fd-193">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-193">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="309fd-194">sip</span><span class="sxs-lookup"><span data-stu-id="309fd-194">sip</span></span>  <br/> |<span data-ttu-id="309fd-195">600</span><span class="sxs-lookup"><span data-stu-id="309fd-195">600</span></span>  <br/> |<span data-ttu-id="309fd-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="309fd-196">CNAME</span></span>  <br/> |<span data-ttu-id="309fd-197">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-197">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="309fd-198">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-198">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="309fd-199">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="309fd-199">lyncdiscover</span></span>  <br/> |<span data-ttu-id="309fd-200">600</span><span class="sxs-lookup"><span data-stu-id="309fd-200">600</span></span>  <br/> |<span data-ttu-id="309fd-201">CNAME</span><span class="sxs-lookup"><span data-stu-id="309fd-201">CNAME</span></span>  <br/> |<span data-ttu-id="309fd-202">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-202">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="309fd-203">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-203">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="309fd-204">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="309fd-204">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="309fd-205">600</span><span class="sxs-lookup"><span data-stu-id="309fd-205">600</span></span>  <br/> |<span data-ttu-id="309fd-206">CNAME</span><span class="sxs-lookup"><span data-stu-id="309fd-206">CNAME</span></span>  <br/> |<span data-ttu-id="309fd-207">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="309fd-207">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="309fd-208">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-208">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="309fd-209">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="309fd-209">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="309fd-210">600</span><span class="sxs-lookup"><span data-stu-id="309fd-210">600</span></span>  <br/> |<span data-ttu-id="309fd-211">CNAME</span><span class="sxs-lookup"><span data-stu-id="309fd-211">CNAME</span></span>  <br/> |<span data-ttu-id="309fd-212">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-212">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="309fd-213">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-213">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Dyn-BP-Configure-3-1](../../media/1fd80695-d3d7-4298-9ebe-97a69f46f1b2.png)
  
6. <span data-ttu-id="309fd-215">Sélectionnez **Créer un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="309fd-215">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-3-2](../../media/89551495-3fa5-44ab-96b2-855f70be0880.png)
  
7. <span data-ttu-id="309fd-217">Ajoutez les cinq enregistrements CNAME restants.</span><span class="sxs-lookup"><span data-stu-id="309fd-217">Add the remaining five CNAME records.</span></span>
    
    <span data-ttu-id="309fd-218">Dans la section Ajouter un enregistrement **DNS,** créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Créer** un enregistrement pour terminer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="309fd-218">In the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again select **Create Record** to complete that record.</span></span> 
    
    <span data-ttu-id="309fd-219">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="309fd-219">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="309fd-220">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="309fd-220">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="309fd-221"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="309fd-221"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="309fd-222">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="309fd-222">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="309fd-223">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="309fd-223">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="309fd-224">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="309fd-224">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="309fd-225">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de n’avoir qu’un seul  *enregistrement*  SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="309fd-225">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="309fd-p110">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="309fd-p110">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="309fd-229">Dans la page **Services au niveau** de la zone, sélectionnez **Dyn Standard DNS Service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="309fd-229">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="309fd-230">Dans la page **DNS** de votre domaine, sélectionnez **Préférences.**</span><span class="sxs-lookup"><span data-stu-id="309fd-230">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="309fd-231">Sélectionnez **Activer l’interface experte.**</span><span class="sxs-lookup"><span data-stu-id="309fd-231">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="309fd-232">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="309fd-232">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="309fd-233">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="309fd-233">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="309fd-234">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="309fd-234">**Host**</span></span>|<span data-ttu-id="309fd-235">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="309fd-235">**TTL**</span></span>|<span data-ttu-id="309fd-236">**Type**</span><span class="sxs-lookup"><span data-stu-id="309fd-236">**Type**</span></span>|<span data-ttu-id="309fd-237">**Données**</span><span class="sxs-lookup"><span data-stu-id="309fd-237">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="309fd-238">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="309fd-238">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="309fd-239">600</span><span class="sxs-lookup"><span data-stu-id="309fd-239">600</span></span>  <br/> |<span data-ttu-id="309fd-240">TXT</span><span class="sxs-lookup"><span data-stu-id="309fd-240">TXT</span></span>  <br/> |<span data-ttu-id="309fd-241">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="309fd-241">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="309fd-242">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="309fd-242">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Dyn-BP-Configure-4-1](../../media/f8511349-3ea2-40c3-9853-98e1a58a91b5.png)
  
6. <span data-ttu-id="309fd-244">Sélectionnez **Créer un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="309fd-244">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-4-2](../../media/bbe04835-d3c0-4146-8123-9781bb9eca51.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="309fd-246">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="309fd-246">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="309fd-247"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="309fd-247"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="309fd-248">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/).</span><span class="sxs-lookup"><span data-stu-id="309fd-248">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/).</span></span> <span data-ttu-id="309fd-249">Vous serez d’abord invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="309fd-249">You'll be prompted to login first</span></span> 
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="309fd-251">Dans la page **Services au niveau** de la zone, sélectionnez **Dyn Standard DNS Service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="309fd-251">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="309fd-252">Dans la page **DNS** de votre domaine, sélectionnez **Préférences.**</span><span class="sxs-lookup"><span data-stu-id="309fd-252">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="309fd-253">Sélectionnez **Activer l’interface experte.**</span><span class="sxs-lookup"><span data-stu-id="309fd-253">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="309fd-254">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="309fd-254">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="309fd-255">Dans la section **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="309fd-255">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    <span data-ttu-id="309fd-256">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="309fd-256">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="309fd-257">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="309fd-257">**Host**</span></span>|<span data-ttu-id="309fd-258">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="309fd-258">**TTL**</span></span>|<span data-ttu-id="309fd-259">**Type**</span><span class="sxs-lookup"><span data-stu-id="309fd-259">**Type**</span></span>|<span data-ttu-id="309fd-260">**Données**</span><span class="sxs-lookup"><span data-stu-id="309fd-260">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="309fd-261">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="309fd-261">_sip._tls</span></span>|<span data-ttu-id="309fd-262">600</span><span class="sxs-lookup"><span data-stu-id="309fd-262">600</span></span>|<span data-ttu-id="309fd-263">SRV</span><span class="sxs-lookup"><span data-stu-id="309fd-263">SRV</span></span>|<span data-ttu-id="309fd-264">100 1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-264">100 1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="309fd-265">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-265">**This value MUST end with a period (.)**</span></span><br><span data-ttu-id="309fd-266">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="309fd-266">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="309fd-267">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="309fd-267">_sipfederationtls._tcp</span></span>|<span data-ttu-id="309fd-268">600</span><span class="sxs-lookup"><span data-stu-id="309fd-268">600</span></span>|<span data-ttu-id="309fd-269">SRV</span><span class="sxs-lookup"><span data-stu-id="309fd-269">SRV</span></span>|<span data-ttu-id="309fd-270">100 1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="309fd-270">100 1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="309fd-271">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="309fd-271">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="309fd-272">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="309fd-272">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Dyn-BP-Configure-5-1](../../media/a6873411-f4ce-4327-9145-02d435930976.png)
  
6. <span data-ttu-id="309fd-274">Sélectionnez **Créer un enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="309fd-274">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-5-2](../../media/e6f33452-e527-473b-a645-b31ed70b0d43.png)
  
7. <span data-ttu-id="309fd-276">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="309fd-276">Add the other SRV record.</span></span>
    
    <span data-ttu-id="309fd-277">Dans la section Ajouter un enregistrement **DNS,** créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Créer** un enregistrement pour terminer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="309fd-277">In the **Add DNS Record** section, create a record by using the values from the second row in the table, and then again select **Create Record** to complete that record.</span></span> 
    
> [!NOTE]
>  <span data-ttu-id="309fd-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="309fd-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
