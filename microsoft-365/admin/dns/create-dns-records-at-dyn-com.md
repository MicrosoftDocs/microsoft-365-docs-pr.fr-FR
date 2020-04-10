---
title: Créer des enregistrements DNS auprès de Dyn.com pour Office 365
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
ms.assetid: 34e57a00-2a7d-469c-beec-089423f18369
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur Dyn.com pour Office 365.
ms.openlocfilehash: d25d4d9712dcd2e2a171c6ad0eac70b8c01e75ab
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211774"
---
# <a name="create-dns-records-at-dyncom-for-office-365"></a><span data-ttu-id="a4fe9-103">Créer des enregistrements DNS auprès de Dyn.com pour Office 365</span><span class="sxs-lookup"><span data-stu-id="a4fe9-103">Create DNS records at Dyn.com for Office 365</span></span>

 <span data-ttu-id="a4fe9-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="a4fe9-105">Si Dyn.com est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-105">If Dyn.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
 
<span data-ttu-id="a4fe9-106">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-106">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="a4fe9-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="a4fe9-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="a4fe9-110">Add a TXT record for verification</span></span>
<span data-ttu-id="a4fe9-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="a4fe9-111"><a name="BKMK_verify"> </a></span></span>

1. <span data-ttu-id="a4fe9-p102">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p102">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="a4fe9-115">Dans la page **zone Level services** , sélectionnez **dyn standard DNS service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-115">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="a4fe9-116">Sur la page **DNS** de votre domaine, sélectionnez **Préférences**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-116">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="a4fe9-117">Sélectionnez **activer l’interface expert**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-117">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="a4fe9-118">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-118">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a4fe9-119">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-119">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a4fe9-120">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-120">**Host**</span></span>|<span data-ttu-id="a4fe9-121">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-121">**TTL**</span></span>|<span data-ttu-id="a4fe9-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-122">**Type**</span></span>|<span data-ttu-id="a4fe9-123">**Données**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-123">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a4fe9-124">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-124">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="a4fe9-125">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-125">600</span></span>  <br/> |<span data-ttu-id="a4fe9-126">TXT</span><span class="sxs-lookup"><span data-stu-id="a4fe9-126">TXT</span></span>  <br/> |<span data-ttu-id="a4fe9-127">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="a4fe9-127">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="a4fe9-128">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-128">**Note:** This is an example.</span></span> <span data-ttu-id="a4fe9-129">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-129">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="a4fe9-130">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a4fe9-130">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
       
   ![Dyn-BP-Verify-1-1](../../media/b3730b15-a313-4b4c-b91e-646eebb649e8.png)
  
6. <span data-ttu-id="a4fe9-132">Sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-132">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Verify-1-2](../../media/8b63b4ee-dbd7-44a7-b1e6-c6892b02f13e.png)
  
7. <span data-ttu-id="a4fe9-134">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-134">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="a4fe9-135">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-135">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="a4fe9-136">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-136">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="a4fe9-137">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-137">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="a4fe9-138">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-138">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="a4fe9-139">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-139">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="a4fe9-140">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-140">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="a4fe9-p104">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p104">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="a4fe9-144">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="a4fe9-144">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="a4fe9-145"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="a4fe9-145"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="a4fe9-p105">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p105">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="a4fe9-149">Dans la page **zone Level services** , sélectionnez **dyn standard DNS service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-149">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="a4fe9-150">Sur la page DNS de votre domaine, sélectionnez **Préférences**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-150">On the DNS page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="a4fe9-151">Sélectionnez **activer l’interface expert**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-151">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="a4fe9-152">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-152">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a4fe9-153">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-153">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a4fe9-154">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-154">**Host**</span></span>|<span data-ttu-id="a4fe9-155">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-155">**TTL**</span></span>|<span data-ttu-id="a4fe9-156">**Type**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-156">**Type**</span></span>|<span data-ttu-id="a4fe9-157">**Données**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-157">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a4fe9-158">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-158">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="a4fe9-159">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-159">600</span></span>  <br/> |<span data-ttu-id="a4fe9-160">MX</span><span class="sxs-lookup"><span data-stu-id="a4fe9-160">MX</span></span>  <br/> |<span data-ttu-id="a4fe9-161">10  *\<clé_de_domaine\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-161">10  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="a4fe9-162">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-162">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="a4fe9-p106">La valeur **10** représente la valeur de priorité MX. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par un espace.  </span><span class="sxs-lookup"><span data-stu-id="a4fe9-p106">The **10** is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="a4fe9-165">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-165">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="a4fe9-166">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a4fe9-166">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)      <br>    <span data-ttu-id="a4fe9-167">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-167">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |
   
    ![Dyn-BP-configure-2-1](../../media/62ac77b7-c84d-426d-9ec4-a28d6479ad04.png)
  
6. <span data-ttu-id="a4fe9-169">Sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-169">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-2-2](../../media/e84e2cca-75e3-4584-8a98-f2f89cb71bd3.png)
  
7. <span data-ttu-id="a4fe9-171">Si d'autres enregistrements MX sont répertoriés, supprimez-les en activant la case à cocher correspondante dans la colonne **Delete (Supprimer)**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-171">If there are any other MX records, remove them by selecting the check box for each one in the **Delete** column.</span></span> 
    
    ![Dyn-BP-Configure-2-3](../../media/f24f02cc-c0b7-42cf-a2ff-4d0fc203e4de.png)
  
8. <span data-ttu-id="a4fe9-173">Sélectionnez **appliquer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-173">Select **Apply Changes**.</span></span>
    
    ![Dyn-BP-Configure-2-4](../../media/0cc23c2b-b6f2-4f58-af20-4c6506de7b43.png)
  
## <a name="add-the-six-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="a4fe9-175">Ajouter les 6 enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="a4fe9-175">Add the six CNAME records that are required for Office 365</span></span>
<span data-ttu-id="a4fe9-176"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="a4fe9-176"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="a4fe9-p108">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p108">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="a4fe9-180">Dans la page **zone Level services** , sélectionnez **dyn standard DNS service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-180">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="a4fe9-181">Sur la page **DNS** de votre domaine, sélectionnez **Préférences**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-181">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="a4fe9-182">Sélectionnez **activer l’interface expert**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-182">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="a4fe9-183">Ajoutez le premier des six enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-183">Add the first of the six CNAME records.</span></span>
    
    <span data-ttu-id="a4fe9-184">Dans la section **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-184">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    <span data-ttu-id="a4fe9-185">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-185">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a4fe9-186">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-186">**Host**</span></span>|<span data-ttu-id="a4fe9-187">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-187">**TTL**</span></span>|<span data-ttu-id="a4fe9-188">**Type**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-188">**Type**</span></span>|<span data-ttu-id="a4fe9-189">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-189">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a4fe9-190">autodiscover</span><span class="sxs-lookup"><span data-stu-id="a4fe9-190">autodiscover</span></span>  <br/> |<span data-ttu-id="a4fe9-191">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-191">600</span></span>  <br/> |<span data-ttu-id="a4fe9-192">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4fe9-192">CNAME</span></span>  <br/> |<span data-ttu-id="a4fe9-193">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-193">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="a4fe9-194">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-194">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="a4fe9-195">sip</span><span class="sxs-lookup"><span data-stu-id="a4fe9-195">sip</span></span>  <br/> |<span data-ttu-id="a4fe9-196">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-196">600</span></span>  <br/> |<span data-ttu-id="a4fe9-197">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4fe9-197">CNAME</span></span>  <br/> |<span data-ttu-id="a4fe9-198">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-198">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="a4fe9-199">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-199">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="a4fe9-200">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="a4fe9-200">lyncdiscover</span></span>  <br/> |<span data-ttu-id="a4fe9-201">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-201">600</span></span>  <br/> |<span data-ttu-id="a4fe9-202">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4fe9-202">CNAME</span></span>  <br/> |<span data-ttu-id="a4fe9-203">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-203">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="a4fe9-204">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-204">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="a4fe9-205">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="a4fe9-205">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="a4fe9-206">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-206">600</span></span>  <br/> |<span data-ttu-id="a4fe9-207">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4fe9-207">CNAME</span></span>  <br/> |<span data-ttu-id="a4fe9-208">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-208">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="a4fe9-209">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-209">**This value MUST end with a period (.)**</span></span> <br/> |
    |<span data-ttu-id="a4fe9-210">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="a4fe9-210">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="a4fe9-211">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-211">600</span></span>  <br/> |<span data-ttu-id="a4fe9-212">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4fe9-212">CNAME</span></span>  <br/> |<span data-ttu-id="a4fe9-213">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-213">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="a4fe9-214">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-214">**This value MUST end with a period (.)**</span></span> <br/> |
   
    ![Dyn-BP-configure-3-1](../../media/1fd80695-d3d7-4298-9ebe-97a69f46f1b2.png)
  
6. <span data-ttu-id="a4fe9-216">Sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-216">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-3-2](../../media/89551495-3fa5-44ab-96b2-855f70be0880.png)
  
7. <span data-ttu-id="a4fe9-218">Ajoutez les cinq enregistrements CNAME restants.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-218">Add the remaining five CNAME records.</span></span>
    
    <span data-ttu-id="a4fe9-219">Dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau **Create record (créer un enregistrement** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-219">In the **Add DNS Record** section, create a record by using the values from the next row in the table, and then again select **Create Record** to complete that record.</span></span> 
    
    <span data-ttu-id="a4fe9-220">Répétez cette procédure jusqu'à avoir créé les 6 enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-220">Repeat this process until you have created all six CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="a4fe9-221">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a4fe9-221">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="a4fe9-222"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="a4fe9-222"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4fe9-223">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-223">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="a4fe9-224">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-224">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="a4fe9-225">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-225">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="a4fe9-226">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-226">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>
  
1. <span data-ttu-id="a4fe9-p110">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p110">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/). You'll be prompted to login first.</span></span>
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="a4fe9-230">Dans la page **zone Level services** , sélectionnez **dyn standard DNS service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-230">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="a4fe9-231">Sur la page **DNS** de votre domaine, sélectionnez **Préférences**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-231">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="a4fe9-232">Sélectionnez **activer l’interface expert**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-232">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="a4fe9-233">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-233">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="a4fe9-234">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-234">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a4fe9-235">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-235">**Host**</span></span>|<span data-ttu-id="a4fe9-236">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-236">**TTL**</span></span>|<span data-ttu-id="a4fe9-237">**Type**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-237">**Type**</span></span>|<span data-ttu-id="a4fe9-238">**Données**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-238">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a4fe9-239">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-239">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="a4fe9-240">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-240">600</span></span>  <br/> |<span data-ttu-id="a4fe9-241">TXT</span><span class="sxs-lookup"><span data-stu-id="a4fe9-241">TXT</span></span>  <br/> |<span data-ttu-id="a4fe9-242">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="a4fe9-242">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="a4fe9-243">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-243">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Dyn-BP-configure-4-1](../../media/f8511349-3ea2-40c3-9853-98e1a58a91b5.png)
  
6. <span data-ttu-id="a4fe9-245">Sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-245">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-4-2](../../media/bbe04835-d3c0-4146-8123-9781bb9eca51.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="a4fe9-247">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="a4fe9-247">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="a4fe9-248"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="a4fe9-248"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="a4fe9-249">Pour commencer, accédez à la page de vos domaines sur le site Dyn.com en utilisant [ce lien](https://account.dyn.com/dns/).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-249">To get started, go to your domains page at Dyn.com by using [this link](https://account.dyn.com/dns/).</span></span> <span data-ttu-id="a4fe9-250">Vous serez invité à vous connecter d’abord.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-250">You'll be prompted to login first</span></span> 
    
    ![Dyn-BP-Configure-1-1](../../media/77597d44-9b04-43b1-8e23-d4fad238def2.png)
  
2. <span data-ttu-id="a4fe9-252">Dans la page **zone Level services** , sélectionnez **dyn standard DNS service** pour le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-252">On the **Zone Level Services** page, select **Dyn Standard DNS Service** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="a4fe9-253">Sur la page **DNS** de votre domaine, sélectionnez **Préférences**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-253">On the **DNS** page for your domain, select **Preferences**.</span></span>
    
4. <span data-ttu-id="a4fe9-254">Sélectionnez **activer l’interface expert**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-254">Select **Enable Expert Interface**.</span></span>
    
5. <span data-ttu-id="a4fe9-255">Ajoutez le premier des deux enregistrements SRV.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-255">Add the first of the two SRV records.</span></span>
    
    <span data-ttu-id="a4fe9-256">Dans la section **Add DNS Record (Ajouter un enregistrement DNS)**, dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-256">In the **Add DNS Record** section, in the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> 
    
    <span data-ttu-id="a4fe9-257">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a4fe9-257">(Choose the **Type** value from the drop-down list.)</span></span> 
    
    |<span data-ttu-id="a4fe9-258">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-258">**Host**</span></span>|<span data-ttu-id="a4fe9-259">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-259">**TTL**</span></span>|<span data-ttu-id="a4fe9-260">**Type**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-260">**Type**</span></span>|<span data-ttu-id="a4fe9-261">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-261">**Data**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a4fe9-262">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="a4fe9-262">_sip._tls</span></span>|<span data-ttu-id="a4fe9-263">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-263">600</span></span>|<span data-ttu-id="a4fe9-264">SRV</span><span class="sxs-lookup"><span data-stu-id="a4fe9-264">SRV</span></span>|<span data-ttu-id="a4fe9-265">100 1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-265">100 1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="a4fe9-266">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-266">**This value MUST end with a period (.)**</span></span><br><span data-ttu-id="a4fe9-267">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-267">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
    |<span data-ttu-id="a4fe9-268">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="a4fe9-268">_sipfederationtls._tcp</span></span>|<span data-ttu-id="a4fe9-269">600</span><span class="sxs-lookup"><span data-stu-id="a4fe9-269">600</span></span>|<span data-ttu-id="a4fe9-270">SRV</span><span class="sxs-lookup"><span data-stu-id="a4fe9-270">SRV</span></span>|<span data-ttu-id="a4fe9-271">100 1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-271">100 1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="a4fe9-272">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="a4fe9-272">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="a4fe9-273">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-273">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![Dyn-BP-configure-5-1](../../media/a6873411-f4ce-4327-9145-02d435930976.png)
  
6. <span data-ttu-id="a4fe9-275">Sélectionnez **créer un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-275">Select **Create Record**.</span></span>
    
    ![Dyn-BP-Configure-5-2](../../media/e6f33452-e527-473b-a645-b31ed70b0d43.png)
  
7. <span data-ttu-id="a4fe9-277">Ajoutez l'autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-277">Add the other SRV record.</span></span>
    
    <span data-ttu-id="a4fe9-278">Dans la section **Add DNS record (ajouter un enregistrement DNS** ), créez un enregistrement en utilisant les valeurs de la deuxième ligne du tableau, puis sélectionnez de nouveau **Create record (créer un enregistrement** ) pour valider cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a4fe9-278">In the **Add DNS Record** section, create a record by using the values from the second row in the table, and then again select **Create Record** to complete that record.</span></span> 
    
> [!NOTE]
>  <span data-ttu-id="a4fe9-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a4fe9-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
