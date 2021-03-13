---
title: Créer des enregistrements DNS auprès de OVH pour Microsoft
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
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online et les autres services sur OVH pour Microsoft.
ms.openlocfilehash: 14c3796ff6686ae0d98ec32ec6ddf6afc004a3c3
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657778"
---
# <a name="create-dns-records-at-ovh-for-microsoft"></a><span data-ttu-id="f2f8d-103">Créer des enregistrements DNS auprès de OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-103">Create DNS records at OVH for Microsoft</span></span>

<span data-ttu-id="f2f8d-104">[Consultez les FAQ des domaines](../setup/domains-faq.yml) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-104">[Check the Domains FAQ](../setup/domains-faq.yml) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f2f8d-105">Si OVH est votre fournisseur d'hébergement DNS, procédez de la manière décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-105">If OVH is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="f2f8d-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-106">These are the main records to add.</span></span> 
  
- [<span data-ttu-id="f2f8d-107">Créer des enregistrements DNS auprès de OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-107">Create DNS records at OVH for Microsoft</span></span>](#create-dns-records-at-ovh-for-microsoft)
    
- [<span data-ttu-id="f2f8d-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="f2f8d-109">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-109">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="f2f8d-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f2f8d-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="f2f8d-111">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="f2f8d-112">Une fois ces enregistrements ajoutés sur OVH, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-112">After you add these records at OVH, your domain will be set up to work with Microsoft services.</span></span>

  
> [!NOTE]
>  <span data-ttu-id="f2f8d-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f2f8d-116">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f2f8d-116">Add a TXT record for verification</span></span>
<span data-ttu-id="f2f8d-117"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="f2f8d-117"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="f2f8d-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f2f8d-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f2f8d-122">Pour commencer, accédez à la page de vos domaines sur le site d’OVH en utilisant [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-122">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="f2f8d-123">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-123">You'll be prompted to log in.</span></span>
    
    ![OVH Connexion](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="f2f8d-125">Sous **Domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-125">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH Sélectionner le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="f2f8d-127">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-127">Select **DNS zone**.</span></span>
    
    ![OVH Sélectionner la zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="f2f8d-129">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-129">Select **Add an entry**.</span></span>
    
    ![OVH Ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="f2f8d-131">Sélectionnez **TXT**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-131">Select **TXT**</span></span>
    
    ![OVH Sélectionner une entrée TXT](../../media/3aaa9dae-0b1d-436b-a980-b67a970f31a9.png)
  
6. <span data-ttu-id="f2f8d-133">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-133">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="f2f8d-134">Afin de définir une valeur TTL, choisissez **Personnalisé** depuis la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-134">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="f2f8d-135">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-135">**Record type**</span></span>|<span data-ttu-id="f2f8d-136">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-136">**Sub-domain**</span></span>|<span data-ttu-id="f2f8d-137">**TTL**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-137">**TTL**</span></span>|<span data-ttu-id="f2f8d-138">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-138">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f2f8d-139">TXT</span><span class="sxs-lookup"><span data-stu-id="f2f8d-139">TXT</span></span>  <br/> |<span data-ttu-id="f2f8d-140">(laissez vide)</span><span class="sxs-lookup"><span data-stu-id="f2f8d-140">(leave blank)</span></span>  <br/> |<span data-ttu-id="f2f8d-141">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-141">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="f2f8d-142">MS=msXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="f2f8d-142">MS=msxxxxxxxx</span></span>  <br/> <span data-ttu-id="f2f8d-143">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-143">**Note:** This is an example.</span></span> <span data-ttu-id="f2f8d-144">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-144">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="f2f8d-145">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f2f8d-145">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="f2f8d-146">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-146">Select **Confirm**.</span></span> 
    
    ![OVH Confirmer TXT pour vérification](../../media/bde45596-9a55-4634-b5e7-16d7cde6e1b8.png)
  
8. <span data-ttu-id="f2f8d-148">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-148">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f2f8d-149">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez sur Microsoft et demandez l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-149">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="f2f8d-150">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-150">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f2f8d-151">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-151">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="f2f8d-152">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-152">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="f2f8d-153">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-153">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="f2f8d-154">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-154">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="f2f8d-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="f2f8d-158">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient transférés vers Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-158">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="f2f8d-159"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="f2f8d-159"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="f2f8d-160">Pour commencer, accédez à la page de vos domaines sur le site d’OVH en utilisant [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-160">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="f2f8d-161">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-161">You'll be prompted to log in.</span></span>
    
    ![OVH Connexion](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="f2f8d-163">Sous **Domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-163">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH Sélectionner le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="f2f8d-165">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-165">Select **DNS zone**.</span></span>
    
    ![OVH Sélectionner la zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="f2f8d-167">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-167">Select **Add an entry**.</span></span>
    
    ![OVH Ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="f2f8d-169">Sélectionnez **MX**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-169">Select **MX**.</span></span>
    
    ![OVH Type d'enregistrement MX](../../media/29b5e54e-440a-41f2-9eb9-3de573922ddf.png)
  
6. <span data-ttu-id="f2f8d-171">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-171">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="f2f8d-172">Afin de définir une valeur TTL, choisissez **Personnalisé** depuis la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-172">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f2f8d-173">Par défaut, OVH utilise une notation relative pour localiser la cible. Celle-ci s’ajoute au nom de domaine à la fin de l’enregistrement cible.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-173">By default OVH uses relative notation for the target, which adds the domain name to the end of the target record.</span></span> <span data-ttu-id="f2f8d-174">Pour utiliser une notation absolue, ajoutez un point à l’enregistrement cible, ainsi que montré dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-174">To use absolute notation instead, add a dot to the target record as shown in the table below.</span></span> 
  
    |<span data-ttu-id="f2f8d-175">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-175">**Record type**</span></span>|<span data-ttu-id="f2f8d-176">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-176">**Sub-domain**</span></span>|<span data-ttu-id="f2f8d-177">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-177">**TTL**</span></span>|<span data-ttu-id="f2f8d-178">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-178">**Priority**</span></span>|<span data-ttu-id="f2f8d-179">**Cible**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-179">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f2f8d-180">MX</span><span class="sxs-lookup"><span data-stu-id="f2f8d-180">MX</span></span>  <br/> |<span data-ttu-id="f2f8d-181">(laissez vide)</span><span class="sxs-lookup"><span data-stu-id="f2f8d-181">(leave blank)</span></span>  <br/> |<span data-ttu-id="f2f8d-182">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-182">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="f2f8d-183">10</span><span class="sxs-lookup"><span data-stu-id="f2f8d-183">10</span></span>  <br/> <span data-ttu-id="f2f8d-184">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-184">For more information about priority, see [What is MX priority?](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq)</span></span> <br/> |<span data-ttu-id="f2f8d-185">\<domain-key\>.mail.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="f2f8d-185">\<domain-key\>.mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="f2f8d-186">**Remarque :** Obtenez votre *\<domain-key\>* depuis votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-186">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="f2f8d-187">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f2f8d-187">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  |
   
    ![OVH Enregistrement MX pour courrier](../../media/6e2f5655-93e2-4620-8f19-c452e7edf8f0.png)
  
7. <span data-ttu-id="f2f8d-189">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-189">Select **Next**.</span></span>
    
    ![OVH Enregistrement MX Sélectionner Suivant](../../media/4db62d07-0dc4-49f6-bd19-2b4a07fd764a.png)
  
8. <span data-ttu-id="f2f8d-191">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-191">Select **Confirm**.</span></span>
    
    ![OVH Enregistrement MX Sélectionner Confirmer](../../media/090bfb11-a753-4af0-8982-582a4069a169.png)
  
9. <span data-ttu-id="f2f8d-193">S'il existe d'autres enregistrements MX, supprimez-les dans la liste sur la page **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-193">If there are any other MX records, delete them all in the list on the **DNS zone** page.</span></span> <span data-ttu-id="f2f8d-194">Sélectionnez chaque enregistrement, puis, dans la colonne **Actions**, sélectionnez l'icône corbeille **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-194">Select each record and then, in the **Actions** column, select the trash-can **Delete** icon.</span></span> 
    
    ![OVH Supprimer un enregistrement MX](../../media/892b328b-7057-4828-b8c5-fe26284dc8c2.png)
  
10. <span data-ttu-id="f2f8d-196">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-196">Select **Confirm**.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="f2f8d-197">Ajouter les enregistrements CNAME requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-197">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="f2f8d-198"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="f2f8d-198"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="f2f8d-199">Pour commencer, accédez à la page de vos domaines sur le site d’OVH en utilisant [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-199">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="f2f8d-200">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-200">You'll be prompted to log in.</span></span>
    
    ![OVH Connexion](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="f2f8d-202">Sous **Domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-202">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH Sélectionner le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="f2f8d-204">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-204">Select **DNS zone**.</span></span>
    
    ![OVH Sélectionner la zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="f2f8d-206">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-206">Select **Add an entry**.</span></span>
    
    ![OVH Ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="f2f8d-208">Sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-208">Select **CNAME**.</span></span>
    
    ![OVH Ajouter un type d’enregistrement CNAME](../../media/33c7ac74-18d7-4ae1-9e27-1c0f9773a3c3.png)
  
6. <span data-ttu-id="f2f8d-210">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-210">Create the first CNAME record.</span></span>
    
    <span data-ttu-id="f2f8d-211">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-211">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="f2f8d-212">Afin de définir une valeur TTL, choisissez **Personnalisé** depuis la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-212">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="f2f8d-213">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-213">**Record type**</span></span>|<span data-ttu-id="f2f8d-214">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-214">**Sub-domain**</span></span>|<span data-ttu-id="f2f8d-215">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-215">**Target**</span></span>|<span data-ttu-id="f2f8d-216">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-216">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f2f8d-217">CNAME</span><span class="sxs-lookup"><span data-stu-id="f2f8d-217">CNAME</span></span>  <br/> |<span data-ttu-id="f2f8d-218">autodiscover</span><span class="sxs-lookup"><span data-stu-id="f2f8d-218">autodiscover</span></span>  <br/> |<span data-ttu-id="f2f8d-219">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-219">autodiscover.outlook.com.</span></span>  <br/> |<span data-ttu-id="f2f8d-220">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-220">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="f2f8d-221">CNAME</span><span class="sxs-lookup"><span data-stu-id="f2f8d-221">CNAME</span></span>  <br/> |<span data-ttu-id="f2f8d-222">sip</span><span class="sxs-lookup"><span data-stu-id="f2f8d-222">sip</span></span>  <br/> |<span data-ttu-id="f2f8d-223">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-223">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="f2f8d-224">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-224">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="f2f8d-225">CNAME</span><span class="sxs-lookup"><span data-stu-id="f2f8d-225">CNAME</span></span>  <br/> |<span data-ttu-id="f2f8d-226">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="f2f8d-226">lyncdiscover</span></span>  <br/> |<span data-ttu-id="f2f8d-227">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-227">webdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="f2f8d-228">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-228">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="f2f8d-229">CNAME</span><span class="sxs-lookup"><span data-stu-id="f2f8d-229">CNAME</span></span>  <br/> |<span data-ttu-id="f2f8d-230">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="f2f8d-230">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="f2f8d-231">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-231">enterpriseregistration.windows.net.</span></span>  <br/> |<span data-ttu-id="f2f8d-232">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-232">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="f2f8d-233">CNAME</span><span class="sxs-lookup"><span data-stu-id="f2f8d-233">CNAME</span></span>  <br/> |<span data-ttu-id="f2f8d-234">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="f2f8d-234">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="f2f8d-235">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-235">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |<span data-ttu-id="f2f8d-236">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-236">3600 seconds</span></span>  <br/> |
   
    ![OVH Enregistrement CNAME](../../media/516938b3-0b12-4736-a631-099e12e189f5.png)
  
7. <span data-ttu-id="f2f8d-238">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-238">Select **Next**.</span></span>
    
    ![OVH Ajouter des valeurs CNAME et sélectionner Suivant](../../media/f9481cb1-559d-4da1-9643-9cacb0d80d29.png)
  
8. <span data-ttu-id="f2f8d-240">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-240">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="f2f8d-241">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-241">Repeat the previous steps to create the other five CNAME records.</span></span>
    
    <span data-ttu-id="f2f8d-242">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones appropriées.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-242">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="f2f8d-243">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="f2f8d-243">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="f2f8d-244"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="f2f8d-244"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2f8d-245">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-245">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="f2f8d-246">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-246">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="f2f8d-247">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-247">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="f2f8d-248">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel de manière à n’avoir *qu’un seul* enregistrement SPF incluant les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-248">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="f2f8d-249">Pour commencer, accédez à la page de vos domaines sur le site d’OVH en utilisant [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-249">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="f2f8d-250">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-250">You'll be prompted to log in.</span></span>
    
    ![OVH Connexion](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="f2f8d-252">Sous **Domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-252">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH Sélectionner le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="f2f8d-254">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-254">Select **DNS zone**.</span></span>
    
    ![OVH Sélectionner la zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="f2f8d-256">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-256">Select **Add an entry**.</span></span>
    
    ![OVH Ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="f2f8d-258">Sélectionnez **TXT**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-258">Select **TXT**.</span></span>
    
6. <span data-ttu-id="f2f8d-259">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-259">In the boxes for the new record, type or copy and paste the following values.</span></span>
    
    |<span data-ttu-id="f2f8d-260">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-260">**Record type**</span></span>|<span data-ttu-id="f2f8d-261">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-261">**Sub-domain**</span></span>|<span data-ttu-id="f2f8d-262">**TTL**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-262">**TTL**</span></span>|<span data-ttu-id="f2f8d-263">**Valeur TXT**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-263">**TXT Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f2f8d-264">TXT</span><span class="sxs-lookup"><span data-stu-id="f2f8d-264">TXT</span></span>  <br/> |<span data-ttu-id="f2f8d-265">(laissez vide)</span><span class="sxs-lookup"><span data-stu-id="f2f8d-265">(leave blank)</span></span>  <br/> |<span data-ttu-id="f2f8d-266">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-266">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="f2f8d-267">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="f2f8d-267">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="f2f8d-268">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-268">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![OVH Ajouter un enregistrement TXT pour SPF](../../media/f50466e9-1557-4548-8a39-e98978a5ee2e.png)
  
7. <span data-ttu-id="f2f8d-270">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-270">Select **Next**.</span></span>
    
    ![OVH Ajouter un enregistrement TXT pour SPF et sélectionner Suivant](../../media/7937eb7c-114f-479f-a916-bcbe476d6108.png)
  
8. <span data-ttu-id="f2f8d-272">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-272">Select **Confirm**.</span></span>
    
    ![OVH Ajouter un enregistrement TXT pour SPF et sélectionner Confirmer](../../media/649eefeb-3227-49e3-98a0-1ce19c42fa54.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="f2f8d-274">Ajoutez les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2f8d-274">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="f2f8d-275"><a name="bkmk_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="f2f8d-275"><a name="bkmk_srv"> </a></span></span>

1. <span data-ttu-id="f2f8d-276">Pour commencer, accédez à la page de vos domaines sur le site d’OVH en utilisant [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-276">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="f2f8d-277">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-277">You'll be prompted to log in.</span></span>
    
    ![OVH Connexion](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="f2f8d-279">Sous **Domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-279">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH Sélectionner le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="f2f8d-281">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-281">Select **DNS zone**.</span></span>
    
    ![OVH Sélectionner la zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="f2f8d-283">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-283">Select **Add an entry**.</span></span>
    
    ![OVH Ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="f2f8d-285">Sélectionnez **SRV**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-285">Select **SRV**.</span></span>
    
    ![OVH Sélectionner le type d’enregistrement SRV](../../media/66bad536-a531-4a4e-b08d-c0d99f6ea1b2.png)
  
6. <span data-ttu-id="f2f8d-287">Créez le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-287">Create the first SRV record.</span></span>
    
    <span data-ttu-id="f2f8d-288">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-288">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="f2f8d-289">Afin de définir une valeur TTL, choisissez **Personnalisé** depuis la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-289">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="f2f8d-290">**Type d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-290">**Record type**</span></span>|<span data-ttu-id="f2f8d-291">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-291">**Sub-domain**</span></span>|<span data-ttu-id="f2f8d-292">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-292">**Priority**</span></span>|<span data-ttu-id="f2f8d-293">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-293">**Weight**</span></span>|<span data-ttu-id="f2f8d-294">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-294">**Port**</span></span>|<span data-ttu-id="f2f8d-295">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-295">**TTL**</span></span>|<span data-ttu-id="f2f8d-296">**Cible**</span><span class="sxs-lookup"><span data-stu-id="f2f8d-296">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="f2f8d-297">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="f2f8d-297">SRV (Service)</span></span>  <br/> |<span data-ttu-id="f2f8d-298">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="f2f8d-298">_sip._tls</span></span>  <br/> |<span data-ttu-id="f2f8d-299">100</span><span class="sxs-lookup"><span data-stu-id="f2f8d-299">100</span></span>  <br/> |<span data-ttu-id="f2f8d-300">1</span><span class="sxs-lookup"><span data-stu-id="f2f8d-300">1</span></span>  <br/> |<span data-ttu-id="f2f8d-301">443</span><span class="sxs-lookup"><span data-stu-id="f2f8d-301">443</span></span>  <br/> |<span data-ttu-id="f2f8d-302">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-302">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="f2f8d-303">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-303">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="f2f8d-304">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="f2f8d-304">SRV (Service)</span></span>  <br/> |<span data-ttu-id="f2f8d-305">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="f2f8d-305">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="f2f8d-306">100</span><span class="sxs-lookup"><span data-stu-id="f2f8d-306">100</span></span>  <br/> |<span data-ttu-id="f2f8d-307">1</span><span class="sxs-lookup"><span data-stu-id="f2f8d-307">1</span></span>  <br/> |<span data-ttu-id="f2f8d-308">5061</span><span class="sxs-lookup"><span data-stu-id="f2f8d-308">5061</span></span>  <br/> |<span data-ttu-id="f2f8d-309">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="f2f8d-309">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="f2f8d-310">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-310">sipfed.online.lync.com.</span></span>  <br/> |
       
    ![OVH Enregistrement SRV](../../media/73956b9e-9e4f-40a5-803e-c4ead2f77fa6.png)
  
7. <span data-ttu-id="f2f8d-312">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-312">Select **Next**.</span></span>
    
    ![OVH Enregistrement SRV Sélectionner Suivant](../../media/cb4ad7e2-a8f0-4ab1-9797-d1b51c1d2da9.png)
  
8. <span data-ttu-id="f2f8d-314">Sélectionnez **Confirmer**.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-314">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="f2f8d-315">Répétez les étapes précédentes pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-315">Repeat the previous steps to create the other SRV record.</span></span> <span data-ttu-id="f2f8d-316">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f2f8d-316">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="f2f8d-p120">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f2f8d-p120">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
