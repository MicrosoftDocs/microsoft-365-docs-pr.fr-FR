---
title: Créer des enregistrements DNS sur OVH pour Microsoft
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
ms.assetid: 5176feef-36dc-4d84-842f-1f2b5a21ba96
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur OVH pour Microsoft.
ms.openlocfilehash: 14c3796ff6686ae0d98ec32ec6ddf6afc004a3c3
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657778"
---
# <a name="create-dns-records-at-ovh-for-microsoft"></a><span data-ttu-id="e1eda-103">Créer des enregistrements DNS sur OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-103">Create DNS records at OVH for Microsoft</span></span>

<span data-ttu-id="e1eda-104">[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="e1eda-104">[Check the Domains FAQ](../setup/domains-faq.yml) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="e1eda-105">Si OVH est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="e1eda-105">If OVH is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="e1eda-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e1eda-106">These are the main records to add.</span></span> 
  
- [<span data-ttu-id="e1eda-107">Créer des enregistrements DNS sur OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-107">Create DNS records at OVH for Microsoft</span></span>](#create-dns-records-at-ovh-for-microsoft)
    
- [<span data-ttu-id="e1eda-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="e1eda-109">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-109">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="e1eda-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="e1eda-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="e1eda-111">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="e1eda-112">Une fois ces enregistrements ajoutés sur OVH, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1eda-112">After you add these records at OVH, your domain will be set up to work with Microsoft services.</span></span>

  
> [!NOTE]
>  <span data-ttu-id="e1eda-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e1eda-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="e1eda-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="e1eda-116">Add a TXT record for verification</span></span>
<span data-ttu-id="e1eda-117"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="e1eda-117"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="e1eda-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="e1eda-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1eda-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e1eda-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="e1eda-122">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="e1eda-122">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="e1eda-123">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="e1eda-123">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="e1eda-125">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1eda-125">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="e1eda-127">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-127">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="e1eda-129">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-129">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="e1eda-131">Sélectionnez **txt**</span><span class="sxs-lookup"><span data-stu-id="e1eda-131">Select **TXT**</span></span>
    
    ![OVH Select TXT Entry](../../media/3aaa9dae-0b1d-436b-a980-b67a970f31a9.png)
  
6. <span data-ttu-id="e1eda-133">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1eda-133">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="e1eda-134">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="e1eda-134">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="e1eda-135">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e1eda-135">**Record type**</span></span>|<span data-ttu-id="e1eda-136">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="e1eda-136">**Sub-domain**</span></span>|<span data-ttu-id="e1eda-137">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-137">**TTL**</span></span>|<span data-ttu-id="e1eda-138">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-138">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e1eda-139">TXT</span><span class="sxs-lookup"><span data-stu-id="e1eda-139">TXT</span></span>  <br/> |<span data-ttu-id="e1eda-140">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="e1eda-140">(leave blank)</span></span>  <br/> |<span data-ttu-id="e1eda-141">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="e1eda-141">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="e1eda-142">MS = msxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="e1eda-142">MS=msxxxxxxxx</span></span>  <br/> <span data-ttu-id="e1eda-143">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="e1eda-143">**Note:** This is an example.</span></span> <span data-ttu-id="e1eda-144">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="e1eda-144">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="e1eda-145">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="e1eda-145">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="e1eda-146">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-146">Select **Confirm**.</span></span> 
    
    ![OVH confirmer le TXT pour vérification](../../media/bde45596-9a55-4634-b5e7-16d7cde6e1b8.png)
  
8. <span data-ttu-id="e1eda-148">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="e1eda-148">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="e1eda-149">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e1eda-149">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="e1eda-150">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="e1eda-150">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="e1eda-151">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="e1eda-151">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="e1eda-152">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="e1eda-152">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="e1eda-153">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-153">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="e1eda-154">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-154">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="e1eda-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e1eda-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="e1eda-158">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-158">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="e1eda-159"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="e1eda-159"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="e1eda-160">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="e1eda-160">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="e1eda-161">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="e1eda-161">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="e1eda-163">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1eda-163">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="e1eda-165">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-165">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="e1eda-167">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-167">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="e1eda-169">Sélectionnez **MX**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-169">Select **MX**.</span></span>
    
    ![Type d’enregistrement MX OVH](../../media/29b5e54e-440a-41f2-9eb9-3de573922ddf.png)
  
6. <span data-ttu-id="e1eda-171">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1eda-171">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="e1eda-172">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="e1eda-172">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e1eda-173">Par défaut OVH utilise la notation relative pour la cible, qui ajoute le nom de domaine à la fin de l’enregistrement cible.</span><span class="sxs-lookup"><span data-stu-id="e1eda-173">By default OVH uses relative notation for the target, which adds the domain name to the end of the target record.</span></span> <span data-ttu-id="e1eda-174">Pour utiliser la notation absolue, ajoutez un point à l’enregistrement cible comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1eda-174">To use absolute notation instead, add a dot to the target record as shown in the table below.</span></span> 
  
    |<span data-ttu-id="e1eda-175">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e1eda-175">**Record type**</span></span>|<span data-ttu-id="e1eda-176">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="e1eda-176">**Sub-domain**</span></span>|<span data-ttu-id="e1eda-177">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-177">**TTL**</span></span>|<span data-ttu-id="e1eda-178">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-178">**Priority**</span></span>|<span data-ttu-id="e1eda-179">**Target**</span><span class="sxs-lookup"><span data-stu-id="e1eda-179">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e1eda-180">MX</span><span class="sxs-lookup"><span data-stu-id="e1eda-180">MX</span></span>  <br/> |<span data-ttu-id="e1eda-181">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="e1eda-181">(leave blank)</span></span>  <br/> |<span data-ttu-id="e1eda-182">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="e1eda-182">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="e1eda-183">10 </span><span class="sxs-lookup"><span data-stu-id="e1eda-183">10</span></span>  <br/> <span data-ttu-id="e1eda-184">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="e1eda-184">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |<span data-ttu-id="e1eda-185">\<domain-key\>. mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-185">\<domain-key\>.mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="e1eda-186">**Remarque :** Obtenir votre  *\<domain-key\>*  à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1eda-186">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="e1eda-187">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="e1eda-187">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  |
   
    ![Enregistrement MX OVH pour le courrier électronique](../../media/6e2f5655-93e2-4620-8f19-c452e7edf8f0.png)
  
7. <span data-ttu-id="e1eda-189">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-189">Select **Next**.</span></span>
    
    ![Enregistrement MX OVH sélectionnez suivant](../../media/4db62d07-0dc4-49f6-bd19-2b4a07fd764a.png)
  
8. <span data-ttu-id="e1eda-191">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-191">Select **Confirm**.</span></span>
    
    ![Enregistrement MX OVH sélectionnez confirmer](../../media/090bfb11-a753-4af0-8982-582a4069a169.png)
  
9. <span data-ttu-id="e1eda-193">S’il existe d’autres enregistrements MX, supprimez-les tous dans la liste de la page **zone DNS** .</span><span class="sxs-lookup"><span data-stu-id="e1eda-193">If there are any other MX records, delete them all in the list on the **DNS zone** page.</span></span> <span data-ttu-id="e1eda-194">Sélectionnez chaque enregistrement, puis, dans la colonne **actions** , sélectionnez l’icône Corbeille-peut-être **supprimée** .</span><span class="sxs-lookup"><span data-stu-id="e1eda-194">Select each record and then, in the **Actions** column, select the trash-can **Delete** icon.</span></span> 
    
    ![OVH supprimer un enregistrement MX](../../media/892b328b-7057-4828-b8c5-fe26284dc8c2.png)
  
10. <span data-ttu-id="e1eda-196">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-196">Select **Confirm**.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="e1eda-197">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-197">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="e1eda-198"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="e1eda-198"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="e1eda-199">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="e1eda-199">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="e1eda-200">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="e1eda-200">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="e1eda-202">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1eda-202">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="e1eda-204">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-204">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="e1eda-206">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-206">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="e1eda-208">Sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-208">Select **CNAME**.</span></span>
    
    ![OVH ajouter un type d’enregistrement CNAMe](../../media/33c7ac74-18d7-4ae1-9e27-1c0f9773a3c3.png)
  
6. <span data-ttu-id="e1eda-210">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="e1eda-210">Create the first CNAME record.</span></span>
    
    <span data-ttu-id="e1eda-211">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1eda-211">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="e1eda-212">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="e1eda-212">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="e1eda-213">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e1eda-213">**Record type**</span></span>|<span data-ttu-id="e1eda-214">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="e1eda-214">**Sub-domain**</span></span>|<span data-ttu-id="e1eda-215">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-215">**Target**</span></span>|<span data-ttu-id="e1eda-216">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-216">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e1eda-217">CNAME</span><span class="sxs-lookup"><span data-stu-id="e1eda-217">CNAME</span></span>  <br/> |<span data-ttu-id="e1eda-218">autodiscover</span><span class="sxs-lookup"><span data-stu-id="e1eda-218">autodiscover</span></span>  <br/> |<span data-ttu-id="e1eda-219">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-219">autodiscover.outlook.com.</span></span>  <br/> |<span data-ttu-id="e1eda-220">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="e1eda-220">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="e1eda-221">CNAME</span><span class="sxs-lookup"><span data-stu-id="e1eda-221">CNAME</span></span>  <br/> |<span data-ttu-id="e1eda-222">sip</span><span class="sxs-lookup"><span data-stu-id="e1eda-222">sip</span></span>  <br/> |<span data-ttu-id="e1eda-223">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-223">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="e1eda-224">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="e1eda-224">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="e1eda-225">CNAME</span><span class="sxs-lookup"><span data-stu-id="e1eda-225">CNAME</span></span>  <br/> |<span data-ttu-id="e1eda-226">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="e1eda-226">lyncdiscover</span></span>  <br/> |<span data-ttu-id="e1eda-227">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-227">webdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="e1eda-228">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="e1eda-228">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="e1eda-229">CNAME</span><span class="sxs-lookup"><span data-stu-id="e1eda-229">CNAME</span></span>  <br/> |<span data-ttu-id="e1eda-230">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="e1eda-230">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="e1eda-231">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="e1eda-231">enterpriseregistration.windows.net.</span></span>  <br/> |<span data-ttu-id="e1eda-232">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="e1eda-232">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="e1eda-233">CNAME</span><span class="sxs-lookup"><span data-stu-id="e1eda-233">CNAME</span></span>  <br/> |<span data-ttu-id="e1eda-234">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="e1eda-234">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="e1eda-235">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-235">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |<span data-ttu-id="e1eda-236">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="e1eda-236">3600 seconds</span></span>  <br/> |
   
    ![Enregistrement CNAMe OVH](../../media/516938b3-0b12-4736-a631-099e12e189f5.png)
  
7. <span data-ttu-id="e1eda-238">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-238">Select **Next**.</span></span>
    
    ![OVH ajouter des valeurs CNAMe et sélectionner suivant](../../media/f9481cb1-559d-4da1-9643-9cacb0d80d29.png)
  
8. <span data-ttu-id="e1eda-240">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-240">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="e1eda-241">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="e1eda-241">Repeat the previous steps to create the other five CNAME records.</span></span>
    
    <span data-ttu-id="e1eda-242">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e1eda-242">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="e1eda-243">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="e1eda-243">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="e1eda-244"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="e1eda-244"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1eda-245">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="e1eda-245">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="e1eda-246">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="e1eda-246">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="e1eda-247">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1eda-247">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="e1eda-248">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un  *seul*  enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="e1eda-248">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="e1eda-249">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="e1eda-249">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="e1eda-250">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="e1eda-250">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="e1eda-252">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1eda-252">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="e1eda-254">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-254">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="e1eda-256">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-256">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="e1eda-258">Sélectionnez **txt**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-258">Select **TXT**.</span></span>
    
6. <span data-ttu-id="e1eda-259">In the boxes for the new record, type or copy and paste the following values.</span><span class="sxs-lookup"><span data-stu-id="e1eda-259">In the boxes for the new record, type or copy and paste the following values.</span></span>
    
    |<span data-ttu-id="e1eda-260">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e1eda-260">**Record type**</span></span>|<span data-ttu-id="e1eda-261">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="e1eda-261">**Sub-domain**</span></span>|<span data-ttu-id="e1eda-262">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-262">**TTL**</span></span>|<span data-ttu-id="e1eda-263">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="e1eda-263">**TXT Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e1eda-264">TXT</span><span class="sxs-lookup"><span data-stu-id="e1eda-264">TXT</span></span>  <br/> |<span data-ttu-id="e1eda-265">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="e1eda-265">(leave blank)</span></span>  <br/> |<span data-ttu-id="e1eda-266">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="e1eda-266">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="e1eda-267">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="e1eda-267">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="e1eda-268">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="e1eda-268">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![OVH ajouter un enregistrement TXT pour SPF](../../media/f50466e9-1557-4548-8a39-e98978a5ee2e.png)
  
7. <span data-ttu-id="e1eda-270">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-270">Select **Next**.</span></span>
    
    ![OVH ajouter un enregistrement TXT pour SPF et sélectionner suivant](../../media/7937eb7c-114f-479f-a916-bcbe476d6108.png)
  
8. <span data-ttu-id="e1eda-272">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-272">Select **Confirm**.</span></span>
    
    ![OVH ajouter un enregistrement TXT pour SPF et confirmer](../../media/649eefeb-3227-49e3-98a0-1ce19c42fa54.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="e1eda-274">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="e1eda-274">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="e1eda-275"><a name="bkmk_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="e1eda-275"><a name="bkmk_srv"> </a></span></span>

1. <span data-ttu-id="e1eda-276">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="e1eda-276">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="e1eda-277">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="e1eda-277">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="e1eda-279">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="e1eda-279">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="e1eda-281">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-281">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="e1eda-283">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-283">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="e1eda-285">Sélectionnez **SRV**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-285">Select **SRV**.</span></span>
    
    ![OVH sélectionner un type d’enregistrement SRV](../../media/66bad536-a531-4a4e-b08d-c0d99f6ea1b2.png)
  
6. <span data-ttu-id="e1eda-287">Créez le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="e1eda-287">Create the first SRV record.</span></span>
    
    <span data-ttu-id="e1eda-288">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e1eda-288">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="e1eda-289">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="e1eda-289">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="e1eda-290">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="e1eda-290">**Record type**</span></span>|<span data-ttu-id="e1eda-291">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="e1eda-291">**Sub-domain**</span></span>|<span data-ttu-id="e1eda-292">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-292">**Priority**</span></span>|<span data-ttu-id="e1eda-293">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-293">**Weight**</span></span>|<span data-ttu-id="e1eda-294">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-294">**Port**</span></span>|<span data-ttu-id="e1eda-295">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e1eda-295">**TTL**</span></span>|<span data-ttu-id="e1eda-296">**Target**</span><span class="sxs-lookup"><span data-stu-id="e1eda-296">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="e1eda-297">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="e1eda-297">SRV (Service)</span></span>  <br/> |<span data-ttu-id="e1eda-298">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="e1eda-298">_sip._tls</span></span>  <br/> |<span data-ttu-id="e1eda-299">100</span><span class="sxs-lookup"><span data-stu-id="e1eda-299">100</span></span>  <br/> |<span data-ttu-id="e1eda-300">1 </span><span class="sxs-lookup"><span data-stu-id="e1eda-300">1</span></span>  <br/> |<span data-ttu-id="e1eda-301">443</span><span class="sxs-lookup"><span data-stu-id="e1eda-301">443</span></span>  <br/> |<span data-ttu-id="e1eda-302">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="e1eda-302">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="e1eda-303">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-303">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="e1eda-304">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="e1eda-304">SRV (Service)</span></span>  <br/> |<span data-ttu-id="e1eda-305">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="e1eda-305">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="e1eda-306">100</span><span class="sxs-lookup"><span data-stu-id="e1eda-306">100</span></span>  <br/> |<span data-ttu-id="e1eda-307">1 </span><span class="sxs-lookup"><span data-stu-id="e1eda-307">1</span></span>  <br/> |<span data-ttu-id="e1eda-308">5061</span><span class="sxs-lookup"><span data-stu-id="e1eda-308">5061</span></span>  <br/> |<span data-ttu-id="e1eda-309">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="e1eda-309">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="e1eda-310">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="e1eda-310">sipfed.online.lync.com.</span></span>  <br/> |
       
    ![Enregistrement SRV OVH](../../media/73956b9e-9e4f-40a5-803e-c4ead2f77fa6.png)
  
7. <span data-ttu-id="e1eda-312">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-312">Select **Next**.</span></span>
    
    ![Enregistrement SRV OVH sélectionner suivant](../../media/cb4ad7e2-a8f0-4ab1-9797-d1b51c1d2da9.png)
  
8. <span data-ttu-id="e1eda-314">Sélectionnez  **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="e1eda-314">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="e1eda-315">Répétez les étapes précédentes pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="e1eda-315">Repeat the previous steps to create the other SRV record.</span></span> <span data-ttu-id="e1eda-316">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e1eda-316">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="e1eda-p120">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e1eda-p120">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
