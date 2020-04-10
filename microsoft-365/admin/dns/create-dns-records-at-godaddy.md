---
title: Créer des enregistrements DNS auprès de GoDaddy pour Office 365
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
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur GoDaddy pour Office 365.
ms.custom: okr_smb
ms.openlocfilehash: eceab4659dfc01d6a731c4ed07f27bb29214e5fb
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211738"
---
# <a name="create-dns-records-at-godaddy-for-office-365"></a><span data-ttu-id="6ff20-103">Créer des enregistrements DNS auprès de GoDaddy pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ff20-103">Create DNS records at GoDaddy for Office 365</span></span>

 <span data-ttu-id="6ff20-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="6ff20-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>

<span data-ttu-id="6ff20-105">Si GoDaddy est votre fournisseur d'hébergement DNS, suivez les étapes décrites dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="6ff20-105">If GoDaddy is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>

<span data-ttu-id="6ff20-106">Une fois ces enregistrements ajoutés sur GoDaddy, votre domaine est configuré pour utiliser les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ff20-106">After you add these records at GoDaddy, your domain will be set up to work with Office 365 services.</span></span>

<span data-ttu-id="6ff20-107">Pour en savoir plus sur l'hébergement web et le DNS pour les sites web avec Office 365, voir [Utiliser un site web public avec Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span><span class="sxs-lookup"><span data-stu-id="6ff20-107">To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/choose-a-public-website-3325d50e-d131-403c-a278-7f3296fe33a9).</span></span>

> [!NOTE]
> <span data-ttu-id="6ff20-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6ff20-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="6ff20-111">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="6ff20-111">Add a TXT record for verification</span></span>
<span data-ttu-id="6ff20-112"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="6ff20-112"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="6ff20-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="6ff20-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span>

<span data-ttu-id="6ff20-117">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ff20-117">Follow the steps below.</span></span>

1. <span data-ttu-id="6ff20-p104">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p104">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="6ff20-121">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="6ff20-121">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="6ff20-123">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-123">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="6ff20-125">Choisissez **TXT (Text)** (TXT (Texte)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6ff20-125">Choose **TXT (Text)** from the drop-down list.</span></span> <span data-ttu-id="6ff20-126">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ff20-126">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

    |<span data-ttu-id="6ff20-127">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-127">**Record type**</span></span> |<span data-ttu-id="6ff20-128">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="6ff20-128">**Host**</span></span>|<span data-ttu-id="6ff20-129">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="6ff20-129">**TXT Value**</span></span>|<span data-ttu-id="6ff20-130">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6ff20-130">**TTL**</span></span> |
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6ff20-131">TXT (texte)</span><span class="sxs-lookup"><span data-stu-id="6ff20-131">TXT (Text)</span></span>|@|<span data-ttu-id="6ff20-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="6ff20-132">MS=ms *XXXXXXXX*</span></span><br><span data-ttu-id="6ff20-133">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="6ff20-133">**Note**: This is an example.</span></span> <span data-ttu-id="6ff20-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ff20-134">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="6ff20-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6ff20-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)|<span data-ttu-id="6ff20-136">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-136">1 hour</span></span>  <br><span data-ttu-id="6ff20-137">(Sélectionnez une valeur dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="6ff20-137">(Select a value from the drop-down list.)</span></span>|

      ![GoDaddy-BP-Verify-1-0](../../media/dns/56526870-d6465780-651a-11e9-9cf0-d6fff71e2f62.png)

5. <span data-ttu-id="6ff20-139">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-139">Select **Save**.</span></span>

6. <span data-ttu-id="6ff20-140">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6ff20-140">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>

<span data-ttu-id="6ff20-141">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="6ff20-141">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>

<span data-ttu-id="6ff20-142">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="6ff20-142">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="6ff20-143">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="6ff20-143">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="6ff20-144">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="6ff20-144">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="6ff20-145">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-145">On the **Setup** page, select **Start setup**.</span></span>



4. <span data-ttu-id="6ff20-146">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-146">On the **Verify domain** page, select **Verify**.</span></span>



> [!NOTE]
>  <span data-ttu-id="6ff20-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6ff20-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>

## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-office-365"></a><span data-ttu-id="6ff20-150">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Office 365</span><span class="sxs-lookup"><span data-stu-id="6ff20-150">Add an MX record so email for your domain will come to Office 365</span></span>
<span data-ttu-id="6ff20-151"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="6ff20-151"><a name="BKMK_add_MX"> </a></span></span>

<span data-ttu-id="6ff20-152">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ff20-152">Follow the steps below.</span></span>

1. <span data-ttu-id="6ff20-p108">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p108">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="6ff20-156">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="6ff20-156">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="6ff20-158">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-158">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="6ff20-160">Choisissez **MX (Mail Exchanger)** (MX - Serveur de courrier) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6ff20-160">Choose **MX (Mail Exchanger)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-2-0](../../media/dns/56528642-85842e00-651d-11e9-8dd8-217f468f9a18.png)

5. <span data-ttu-id="6ff20-162">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ff20-162">In the boxes for the new record, type or copy and paste the values from the following table.</span></span>

    <span data-ttu-id="6ff20-163">(Choisissez la valeur **TTL (durée de vie** ) dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="6ff20-163">(Choose the **TTL** value from the drop-down list.)</span></span>

    |<span data-ttu-id="6ff20-164">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-164">**Record type**</span></span>|<span data-ttu-id="6ff20-165">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-165">**Host**</span></span>|<span data-ttu-id="6ff20-166">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-166">**Points to**</span></span>|<span data-ttu-id="6ff20-167">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6ff20-167">**Priority**</span></span>|<span data-ttu-id="6ff20-168">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-168">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6ff20-169">MX (Mail Exchanger) (MX - Serveur de courrier)</span><span class="sxs-lookup"><span data-stu-id="6ff20-169">MX (Mail Exchanger)</span></span>  <br/> |@  <br/> | <span data-ttu-id="6ff20-170">*\<domain-key\>*  .mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-170">*\<domain-key\>*  .mail.protection.outlook.com</span></span>  <br/> <span data-ttu-id="6ff20-171">**Remarque :** Obtenez votre \* \<clé\> de domaine\* à partir de votre compte Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ff20-171">**Note:** Get your  *\<domain-key\>*  from your Office 365 account.</span></span>           [<span data-ttu-id="6ff20-172">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="6ff20-172">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="6ff20-173">10 </span><span class="sxs-lookup"><span data-stu-id="6ff20-173">10</span></span>  <br/> <span data-ttu-id="6ff20-174">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="6ff20-174">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="6ff20-175">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-175">1 hour</span></span>  <br/> |

6. <span data-ttu-id="6ff20-176">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-176">Select **Save**.</span></span>

## <a name="add-the-cname-records-that-are-required-for-office-365"></a><span data-ttu-id="6ff20-177">Ajouter les enregistrements CNAME requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ff20-177">Add the CNAME records that are required for Office 365</span></span>
<span data-ttu-id="6ff20-178"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="6ff20-178"><a name="BKMK_add_CNAME"> </a></span></span>

<span data-ttu-id="6ff20-179">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ff20-179">Follow the steps below.</span></span>

1. <span data-ttu-id="6ff20-p110">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p110">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="6ff20-183">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="6ff20-183">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="6ff20-185">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-185">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)


4. <span data-ttu-id="6ff20-187">Choisissez **CNAME (Alias)** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6ff20-187">Choose **CNAME (Alias)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-3-0](../../media/dns/56528891-e7449800-651d-11e9-8eac-112285b8e38c.png)

5. <span data-ttu-id="6ff20-189">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="6ff20-189">Create the first CNAME record.</span></span>

    <span data-ttu-id="6ff20-190">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ff20-190">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>

    <span data-ttu-id="6ff20-191">(Choisissez la valeur **TTL (durée de vie** ) dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="6ff20-191">(Choose the **TTL** value from the drop-down list.)</span></span>

    |<span data-ttu-id="6ff20-192">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-192">**Record type**</span></span>|<span data-ttu-id="6ff20-193">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-193">**Host**</span></span>|<span data-ttu-id="6ff20-194">**Points to (Destination)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-194">**Points to**</span></span>|<span data-ttu-id="6ff20-195">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-195">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6ff20-196">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="6ff20-196">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="6ff20-197">autodiscover</span><span class="sxs-lookup"><span data-stu-id="6ff20-197">autodiscover</span></span>  <br/> |<span data-ttu-id="6ff20-198">autodiscover.outlook.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-198">autodiscover.outlook.com</span></span>  <br/> |<span data-ttu-id="6ff20-199">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-199">1 hour</span></span>  <br/> |
    |<span data-ttu-id="6ff20-200">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="6ff20-200">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="6ff20-201">sip</span><span class="sxs-lookup"><span data-stu-id="6ff20-201">sip</span></span>  <br/> |<span data-ttu-id="6ff20-202">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-202">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="6ff20-203">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-203">1 hour</span></span>  <br/> |
    |<span data-ttu-id="6ff20-204">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="6ff20-204">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="6ff20-205">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="6ff20-205">lyncdiscover</span></span>  <br/> |<span data-ttu-id="6ff20-206">webdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-206">webdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="6ff20-207">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-207">1 hour</span></span>  <br/> |
    |<span data-ttu-id="6ff20-208">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="6ff20-208">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="6ff20-209">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="6ff20-209">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="6ff20-210">enterpriseregistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="6ff20-210">enterpriseregistration.windows.net</span></span>  <br/> |<span data-ttu-id="6ff20-211">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-211">1 hour</span></span>  <br/> |
    |<span data-ttu-id="6ff20-212">CNAME (Alias)</span><span class="sxs-lookup"><span data-stu-id="6ff20-212">CNAME (Alias)</span></span>  <br/> |<span data-ttu-id="6ff20-213">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="6ff20-213">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="6ff20-214">enterpriseenrollment.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-214">enterpriseenrollment.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="6ff20-215">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-215">1 hour</span></span>  <br/> |



6. <span data-ttu-id="6ff20-216">Répétez ces étapes pour ajouter l’enregistrement CNAMe suivant jusqu’à ce que vous ayez créé les six enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="6ff20-216">Repeat these steps to add the next CNAME record until you have created all six of the CNAME records.</span></span>

## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="6ff20-217">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="6ff20-217">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="6ff20-218"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="6ff20-218"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ff20-219">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="6ff20-219">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="6ff20-220">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="6ff20-220">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="6ff20-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ff20-221">If you already have an SPF record for your domain, don't create a new one for Office 365.</span></span> <span data-ttu-id="6ff20-222">Ajoutez plutôt les valeurs Office 365 requises à l'enregistrement actuel de manière à n'avoir qu'un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="6ff20-222">Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span>

<span data-ttu-id="6ff20-223">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ff20-223">Follow the steps below.</span></span>

1. <span data-ttu-id="6ff20-p112">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p112">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="6ff20-227">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="6ff20-227">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="6ff20-229">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-229">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="6ff20-231">Choisissez **TXT (Text)** (TXT (Texte)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6ff20-231">Choose **TXT (Text)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-4-0](../../media/dns/56529449-c0d32c80-651e-11e9-90e9-895aa1c4bbf1.png)

5. <span data-ttu-id="6ff20-233">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ff20-233">In the boxes for the new record, type or copy and paste the following values.</span></span>

    <span data-ttu-id="6ff20-234">(Choisissez la valeur **TTL (durée de vie** ) dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="6ff20-234">(Choose the **TTL** value from the drop-down lists.)</span></span>

    |<span data-ttu-id="6ff20-235">**Record type (Type d'enregistrement)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-235">**Record type**</span></span>|<span data-ttu-id="6ff20-236">**Hôte**</span><span class="sxs-lookup"><span data-stu-id="6ff20-236">**Host**</span></span>|<span data-ttu-id="6ff20-237">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="6ff20-237">**TXT Value**</span></span>|<span data-ttu-id="6ff20-238">**TTL**</span><span class="sxs-lookup"><span data-stu-id="6ff20-238">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6ff20-239">TXT (texte)</span><span class="sxs-lookup"><span data-stu-id="6ff20-239">TXT (Text)</span></span>  <br/> |@  <br/> |<span data-ttu-id="6ff20-240">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="6ff20-240">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="6ff20-241">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="6ff20-241">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="6ff20-242">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-242">1 hour</span></span>  <br/> |

    ![GoDaddy-BP-configure-4-1](../../media/7c724f02-c9b3-42ab-b9c0-78959fa6ffad.png)

6. <span data-ttu-id="6ff20-244">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-244">Select **Save**.</span></span>


## <a name="add-the-two-srv-records-that-are-required-for-office-365"></a><span data-ttu-id="6ff20-245">Ajoutez les 2 enregistrements SRV requis pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ff20-245">Add the two SRV records that are required for Office 365</span></span>
<span data-ttu-id="6ff20-246"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="6ff20-246"><a name="BKMK_add_SRV"> </a></span></span>

<span data-ttu-id="6ff20-247">Suivez la procédure ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6ff20-247">Follow the steps below.</span></span>

1. <span data-ttu-id="6ff20-p113">Pour commencer, accédez à la page de vos domaines sur le site GoDaddy en utilisant [ce lien](https://account.godaddy.com/products/?go_redirect=disabled). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="6ff20-p113">To get started, go to your domains page at GoDaddy by using [this link](https://account.godaddy.com/products/?go_redirect=disabled). You'll be prompted to log in.</span></span>

    ![GoDaddy-BP-configure-1-1](../../media/d6833ec7-9904-43fd-a877-7c663e5f5c25.png)

2. <span data-ttu-id="6ff20-251">Sous **domaines**, sélectionnez DNS sous le domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="6ff20-251">Under **Domains**, select DNS under the domain that you want to edit.</span></span>

    ![GoDaddy-BP-configure-1-2](../../media/dns/56528038-94b6ac00-651c-11e9-8874-12db60cc7ea6.png)

3. <span data-ttu-id="6ff20-253">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-253">Select **Add**.</span></span>

    ![GoDaddy-BP-configure-1-4](../../media/dns/56527673-ffb3b300-651b-11e9-91c2-83dc9fe5ca30.png)

4. <span data-ttu-id="6ff20-255">Choisissez **SRV (Service)** (SRV (Service)) dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6ff20-255">Choose **SRV (Service)** from the drop-down list.</span></span>

    ![GoDaddy-BP-configure-5-0](../../media/dns/56529669-1dcee280-651f-11e9-8ba2-ecf4fc2f6dca.png)

5. <span data-ttu-id="6ff20-257">Créez le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="6ff20-257">Create the first SRV record.</span></span>

    <span data-ttu-id="6ff20-258">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ff20-258">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span>

    <span data-ttu-id="6ff20-259">(Choisissez le **type d’enregistrement** et les valeurs de **durée de vie** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="6ff20-259">(Choose the **Record type** and **TTL** values from the drop-down lists.)</span></span>

    |<span data-ttu-id="6ff20-260">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="6ff20-260">**Record type**</span></span>|<span data-ttu-id="6ff20-261">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-261">**Name**</span></span>|<span data-ttu-id="6ff20-262">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-262">**Target**</span></span>|<span data-ttu-id="6ff20-263">**Protocol (Protocole)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-263">**Protocol**</span></span>|<span data-ttu-id="6ff20-264">**Service (Service)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-264">**Service**</span></span>|<span data-ttu-id="6ff20-265">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-265">**Priority**</span></span>|<span data-ttu-id="6ff20-266">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-266">**Weight**</span></span>|<span data-ttu-id="6ff20-267">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-267">**Port**</span></span>|<span data-ttu-id="6ff20-268">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="6ff20-268">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="6ff20-269">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="6ff20-269">SRV (Service)</span></span>  <br/> |@  <br/> |<span data-ttu-id="6ff20-270">sipdir.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-270">sipdir.online.lync.com</span></span>  <br/> |<span data-ttu-id="6ff20-271">_tls</span><span class="sxs-lookup"><span data-stu-id="6ff20-271">_tls</span></span>  <br/> |<span data-ttu-id="6ff20-272">_sip</span><span class="sxs-lookup"><span data-stu-id="6ff20-272">_sip</span></span>  <br/> |<span data-ttu-id="6ff20-273">100</span><span class="sxs-lookup"><span data-stu-id="6ff20-273">100</span></span>  <br/> |<span data-ttu-id="6ff20-274">0,1</span><span class="sxs-lookup"><span data-stu-id="6ff20-274">1</span></span>  <br/> |<span data-ttu-id="6ff20-275">443</span><span class="sxs-lookup"><span data-stu-id="6ff20-275">443</span></span>  <br/> |<span data-ttu-id="6ff20-276">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-276">1 hour</span></span>  <br/> |
    |<span data-ttu-id="6ff20-277">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="6ff20-277">SRV (Service)</span></span>  <br/> |@  <br/> |<span data-ttu-id="6ff20-278">sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="6ff20-278">sipfed.online.lync.com</span></span>  <br/> |<span data-ttu-id="6ff20-279">_tcp</span><span class="sxs-lookup"><span data-stu-id="6ff20-279">_tcp</span></span>  <br/> |<span data-ttu-id="6ff20-280">_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="6ff20-280">_sipfederationtls</span></span>  <br/> |<span data-ttu-id="6ff20-281">100</span><span class="sxs-lookup"><span data-stu-id="6ff20-281">100</span></span>  <br/> |<span data-ttu-id="6ff20-282">0,1</span><span class="sxs-lookup"><span data-stu-id="6ff20-282">1</span></span>  <br/> |<span data-ttu-id="6ff20-283">5061</span><span class="sxs-lookup"><span data-stu-id="6ff20-283">5061</span></span>  <br/> |<span data-ttu-id="6ff20-284">1 heure</span><span class="sxs-lookup"><span data-stu-id="6ff20-284">1 hour</span></span>  <br/> |

    ![GoDaddy-BP-configure-5-1](../../media/a1b15ab1-eb6a-4672-90d1-7ac3e0beb223.png)


6. <span data-ttu-id="6ff20-286">Répétez l' **étape 5** pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="6ff20-286">Repeat **Step 5** to Create the other SRV record.</span></span>

7. <span data-ttu-id="6ff20-287">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6ff20-287">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ff20-p114">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="6ff20-p114">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span>
