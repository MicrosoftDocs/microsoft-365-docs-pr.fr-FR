---
title: Créer des enregistrements DNS sur GoDaddy pour Microsoft
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
ms.assetid: f40a9185-b6d5-4a80-bb31-aa3bb0cab48a
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur GoDaddy pour Microsoft.
ms.custom: okr_smb
ms.openlocfilehash: 0f71eb512b83451db8fee41b535ecc0c60d8d6bc
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939214"
---
# <a name="create-dns-records-at-godaddy-for-microsoft"></a><span data-ttu-id="a7160-103">Créer des enregistrements DNS sur GoDaddy pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7160-103">Create DNS records at GoDaddy for Microsoft</span></span>

 <span data-ttu-id="a7160-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a7160-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>

<span data-ttu-id="a7160-105">Si GoDaddy est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="a7160-105">If GoDaddy is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>

<span data-ttu-id="a7160-106">Une fois ces enregistrements ajoutés sur GoDaddy, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7160-106">After you add these records at GoDaddy, your domain will be set up to work with Microsoft services.</span></span>

> [!NOTE]
> <span data-ttu-id="a7160-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a7160-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="a7160-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="a7160-110">Add a TXT record for verification</span></span>
<span data-ttu-id="a7160-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="a7160-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="a7160-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="a7160-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="a7160-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a7160-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span>

<span data-ttu-id="a7160-116">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a7160-116">Follow the steps below.</span></span>

1. <span data-ttu-id="a7160-p104">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a7160-p104">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="a7160-120">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a7160-120">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="a7160-122">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a7160-122">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="a7160-124">Choisissez **TXT (Text)** (TXT (Texte)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7160-124">Choose **TXT (Text)** from the drop-down list.</span></span> <span data-ttu-id="a7160-125">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7160-125">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

    |<span data-ttu-id="a7160-126">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="a7160-126">**Record type**</span></span> |<span data-ttu-id="a7160-127">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="a7160-127">**Host**</span></span>|<span data-ttu-id="a7160-128">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="a7160-128">**TXT Value**</span></span>|<span data-ttu-id="a7160-129">**TTL**</span><span class="sxs-lookup"><span data-stu-id="a7160-129">**TTL**</span></span> |
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a7160-130">TXT (texte)</span><span class="sxs-lookup"><span data-stu-id="a7160-130">TXT (Text)</span></span>|@|<span data-ttu-id="a7160-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="a7160-131">MS=ms *XXXXXXXX*</span></span><br><span data-ttu-id="a7160-132">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="a7160-132">**Note**: This is an example.</span></span> <span data-ttu-id="a7160-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="a7160-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="a7160-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a7160-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="a7160-135">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-135">1 hour</span></span>  <br><span data-ttu-id="a7160-136">(Sélectionnez une valeur dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a7160-136">(Select a value from the drop-down list.)</span></span>|

      ![GoDaddy-BP-Verify-1-0](../../media/dns/56526870-d6465780-651a-11e9-9cf0-d6fff71e2f62.png)

5. <span data-ttu-id="a7160-138">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7160-138">Select **Save**.</span></span>

6. <span data-ttu-id="a7160-139">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="a7160-139">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>

<span data-ttu-id="a7160-140">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a7160-140">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>

<span data-ttu-id="a7160-141">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="a7160-141">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="a7160-142">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="a7160-142">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="a7160-143">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="a7160-143">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="a7160-144">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="a7160-144">On the **Setup** page, select **Start setup**.</span></span>



4. <span data-ttu-id="a7160-145">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="a7160-145">On the **Verify domain** page, select **Verify**.</span></span>



> [!NOTE]
>  <span data-ttu-id="a7160-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a7160-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="a7160-149">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7160-149">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="a7160-150"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="a7160-150"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="a7160-151">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a7160-151">Follow the steps below.</span></span>

1. <span data-ttu-id="a7160-p108">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a7160-p108">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="a7160-155">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a7160-155">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="a7160-157">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a7160-157">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="a7160-159">Choisissez **MX (Mail Exchanger)** (MX - Serveur de courrier) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7160-159">Choose **MX (Mail Exchanger)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-2-0](../../media/dns/56528642-85842e00-651d-11e9-8dd8-217f468f9a18.png)

5. <span data-ttu-id="a7160-161">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7160-161">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

    <span data-ttu-id="a7160-162">(Choisissez la valeur **TTL (durée de vie** ) dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a7160-162">(Choose the **TTL** value from the drop-down list.)</span></span>

    |<span data-ttu-id="a7160-163">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="a7160-163">**Record type**</span></span>|<span data-ttu-id="a7160-164">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a7160-164">**Host**</span></span>|<span data-ttu-id="a7160-165">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="a7160-165">**Points to**</span></span>|<span data-ttu-id="a7160-166">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="a7160-166">**Priority**</span></span>|<span data-ttu-id="a7160-167">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a7160-167">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a7160-168">MX (Mail Exchanger) (MX - Serveur de courrier)</span><span class="sxs-lookup"><span data-stu-id="a7160-168">MX (Mail Exchanger)</span></span>  <br/> |@  <br/> | <span data-ttu-id="a7160-169">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="a7160-169">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="a7160-170">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7160-170">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>           [<span data-ttu-id="a7160-171">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="a7160-171">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="a7160-172">10 </span><span class="sxs-lookup"><span data-stu-id="a7160-172">10</span></span>  <br/> <span data-ttu-id="a7160-173">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7160-173">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="a7160-174">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-174">1 hour</span></span>  <br/> |

6. <span data-ttu-id="a7160-175">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7160-175">Select **Save**.</span></span>

## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="a7160-176">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7160-176">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="a7160-177"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="a7160-177"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="a7160-178">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a7160-178">Follow the steps below.</span></span>

1. <span data-ttu-id="a7160-p110">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a7160-p110">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="a7160-182">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a7160-182">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="a7160-184">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a7160-184">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)


4. <span data-ttu-id="a7160-186">Choisissez **CNAME (Alias)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7160-186">Choose **CNAME (Alias)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-3-0](../../media/dns/56528891-e7449800-651d-11e9-8eac-112285b8e38c.png)

5. <span data-ttu-id="a7160-188">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="a7160-188">Create the first CNAME record.</span></span>

    <span data-ttu-id="a7160-189">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7160-189">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>

    <span data-ttu-id="a7160-190">(Choisissez la valeur **TTL (durée de vie** ) dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="a7160-190">(Choose the **TTL** value from the drop-down list.)</span></span>

    |<span data-ttu-id="a7160-191">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="a7160-191">**Record type**</span></span>|<span data-ttu-id="a7160-192">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="a7160-192">**Host**</span></span>|<span data-ttu-id="a7160-193">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="a7160-193">**Points to**</span></span>|<span data-ttu-id="a7160-194">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a7160-194">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a7160-195">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="a7160-195">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="a7160-196">autodiscover</span><span class="sxs-lookup"><span data-stu-id="a7160-196">autodiscover</span></span>  <br/> |<span data-ttu-id="a7160-197">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="a7160-197">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="a7160-198">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-198">1 hour</span></span>  <br/> |
    |<span data-ttu-id="a7160-199">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="a7160-199">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="a7160-200">sip</span><span class="sxs-lookup"><span data-stu-id="a7160-200">sip</span></span>  <br/> |<span data-ttu-id="a7160-201">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a7160-201">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="a7160-202">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-202">1 hour</span></span>  <br/> |
    |<span data-ttu-id="a7160-203">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="a7160-203">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="a7160-204">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="a7160-204">lyncdiscover</span></span>  <br/> |<span data-ttu-id="a7160-205">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a7160-205">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="a7160-206">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-206">1 hour</span></span>  <br/> |
    |<span data-ttu-id="a7160-207">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="a7160-207">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="a7160-208">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="a7160-208">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="a7160-209">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="a7160-209">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="a7160-210">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-210">1 hour</span></span>  <br/> |
    |<span data-ttu-id="a7160-211">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="a7160-211">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="a7160-212">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="a7160-212">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="a7160-213">enterpriseenrollment.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="a7160-213">enterpriseenrollment.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="a7160-214">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-214">1 hour</span></span>  <br/> |



6. <span data-ttu-id="a7160-215">Répétez ces étapes pour ajouter l’enregistrement CNAMe suivant jusqu’à ce que vous ayez créé les six enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="a7160-215">Repeat these steps to add the next CNAME record until you have created all six of the CNAME records.</span></span>

## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="a7160-216">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="a7160-216">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="a7160-217"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="a7160-217"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7160-218">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="a7160-218">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="a7160-219">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a7160-219">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="a7160-220">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7160-220">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="a7160-221">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="a7160-221">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>

<span data-ttu-id="a7160-222">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a7160-222">Follow the steps below.</span></span>

1. <span data-ttu-id="a7160-p112">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a7160-p112">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="a7160-226">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a7160-226">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="a7160-228">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a7160-228">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="a7160-230">Choisissez **TXT (Text)** (TXT (Texte)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7160-230">Choose **TXT (Text)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-4-0](../../media/dns/56529449-c0d32c80-651e-11e9-90e9-895aa1c4bbf1.png)

5. <span data-ttu-id="a7160-232">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a7160-232">In the boxes for the new record, type or copy and paste the following values.</span></span>

    <span data-ttu-id="a7160-233">(Choisissez la valeur **TTL (durée de vie** ) dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="a7160-233">(Choose the **TTL** value from the drop-down lists.)</span></span>

    |<span data-ttu-id="a7160-234">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="a7160-234">**Record type**</span></span>|<span data-ttu-id="a7160-235">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="a7160-235">**Host**</span></span>|<span data-ttu-id="a7160-236">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="a7160-236">**TXT Value**</span></span>|<span data-ttu-id="a7160-237">**TTL**</span><span class="sxs-lookup"><span data-stu-id="a7160-237">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a7160-238">TXT (texte)</span><span class="sxs-lookup"><span data-stu-id="a7160-238">TXT (Text)</span></span>  <br/> |@  <br/> |<span data-ttu-id="a7160-239">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="a7160-239">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="a7160-240">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="a7160-240">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="a7160-241">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-241">1 hour</span></span>  <br/> |

    ![GoDaddy-BP-configure-4-1](../../media/7c724f02-c9b3-42ab-b9c0-78959fa6ffad.png)

6. <span data-ttu-id="a7160-243">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7160-243">Select **Save**.</span></span>


## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="a7160-244">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="a7160-244">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="a7160-245"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="a7160-245"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="a7160-246">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a7160-246">Follow the steps below.</span></span>

1. <span data-ttu-id="a7160-p113">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="a7160-p113">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="a7160-250">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="a7160-250">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="a7160-252">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a7160-252">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="a7160-254">Choisissez **SRV (Service)** (SRV (Service)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a7160-254">Choose **SRV (Service)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-5-0](../../media/dns/56529669-1dcee280-651f-11e9-8ba2-ecf4fc2f6dca.png)

5. <span data-ttu-id="a7160-256">Créez le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a7160-256">Create the first SRV record.</span></span>

    <span data-ttu-id="a7160-257">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7160-257">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>

    <span data-ttu-id="a7160-258">(Choisissez le **type d’enregistrement** et les valeurs de **durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="a7160-258">(Choose the **Record type** and **TTL** values from the drop-down lists.)</span></span>

    |<span data-ttu-id="a7160-259">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="a7160-259">**Record type**</span></span>|<span data-ttu-id="a7160-260">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="a7160-260">**Name**</span></span>|<span data-ttu-id="a7160-261">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="a7160-261">**Target**</span></span>|<span data-ttu-id="a7160-262">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="a7160-262">**Protocol**</span></span>|<span data-ttu-id="a7160-263">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="a7160-263">**Service**</span></span>|<span data-ttu-id="a7160-264">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="a7160-264">**Priority**</span></span>|<span data-ttu-id="a7160-265">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="a7160-265">**Weight**</span></span>|<span data-ttu-id="a7160-266">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="a7160-266">**Port**</span></span>|<span data-ttu-id="a7160-267">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="a7160-267">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="a7160-268">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="a7160-268">SRV (Service)</span></span>  <br/> |@  <br/> |<span data-ttu-id="a7160-269">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a7160-269">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="a7160-270">_tls</span><span class="sxs-lookup"><span data-stu-id="a7160-270">_tls</span></span>  <br/> |<span data-ttu-id="a7160-271">_sip</span><span class="sxs-lookup"><span data-stu-id="a7160-271">_sip</span></span>  <br/> |<span data-ttu-id="a7160-272">100</span><span class="sxs-lookup"><span data-stu-id="a7160-272">100</span></span>  <br/> |<span data-ttu-id="a7160-273">0,1</span><span class="sxs-lookup"><span data-stu-id="a7160-273">1</span></span>  <br/> |<span data-ttu-id="a7160-274">443</span><span class="sxs-lookup"><span data-stu-id="a7160-274">443</span></span>  <br/> |<span data-ttu-id="a7160-275">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-275">1 hour</span></span>  <br/> |
    |<span data-ttu-id="a7160-276">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="a7160-276">SRV (Service)</span></span>  <br/> |@  <br/> |<span data-ttu-id="a7160-277">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a7160-277">sipfed.online.lync.com</span></span>  <br/> |<span data-ttu-id="a7160-278">_tcp</span><span class="sxs-lookup"><span data-stu-id="a7160-278">_tcp</span></span>  <br/> |<span data-ttu-id="a7160-279">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="a7160-279">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="a7160-280">100</span><span class="sxs-lookup"><span data-stu-id="a7160-280">100</span></span>  <br/> |<span data-ttu-id="a7160-281">0,1</span><span class="sxs-lookup"><span data-stu-id="a7160-281">1</span></span>  <br/> |<span data-ttu-id="a7160-282">5061</span><span class="sxs-lookup"><span data-stu-id="a7160-282">5061</span></span>  <br/> |<span data-ttu-id="a7160-283">1 heure</span><span class="sxs-lookup"><span data-stu-id="a7160-283">1 hour</span></span>  <br/> |

    ![GoDaddy-BP-configure-5-1](../../media/a1b15ab1-eb6a-4672-90d1-7ac3e0beb223.png)


6. <span data-ttu-id="a7160-285">Répétez l' **étape 5** pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a7160-285">Repeat **Step 5** to Create the other SRV record.</span></span>

7. <span data-ttu-id="a7160-286">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a7160-286">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="a7160-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="a7160-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>
