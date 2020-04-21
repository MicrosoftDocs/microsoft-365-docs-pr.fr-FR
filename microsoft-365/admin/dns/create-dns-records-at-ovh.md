---
title: Créer des enregistrements DNS sur OVH pour Microsoft
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
ms.assetid: 5176feef-36dc-4d84-842f-1f2b5a21ba96
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype entreprise Online et d’autres services sur OVH pour Microsoft.
ms.openlocfilehash: 01c455f54a7ee2efc6114dba1c01170b97ea5f71
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629286"
---
# <a name="create-dns-records-at-ovh-for-microsoft"></a><span data-ttu-id="39f9a-103">Créer des enregistrements DNS sur OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-103">Create DNS records at OVH for Microsoft</span></span>

<span data-ttu-id="39f9a-104">[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md) si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="39f9a-104">[Check the Domains FAQ](../setup/domains-faq.md) if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="39f9a-105">Si OVH est votre fournisseur d’hébergement DNS, suivez la procédure décrite dans cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier électronique, Skype entreprise Online, etc.</span><span class="sxs-lookup"><span data-stu-id="39f9a-105">If OVH is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.</span></span>
  
<span data-ttu-id="39f9a-106">Voici les principaux enregistrements à ajouter.</span><span class="sxs-lookup"><span data-stu-id="39f9a-106">These are the main records to add.</span></span> 
  
- [<span data-ttu-id="39f9a-107">Créer des enregistrements DNS sur OVH pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-107">Create DNS records at OVH for Microsoft</span></span>](#create-dns-records-at-ovh-for-microsoft)
    
- [<span data-ttu-id="39f9a-108">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-108">Add an MX record so email for your domain will come to Microsoft</span></span>](#add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft)
    
- [<span data-ttu-id="39f9a-109">Ajouter les enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-109">Add the CNAME records that are required for Microsoft</span></span>](#add-the-cname-records-that-are-required-for-microsoft)
    
- [<span data-ttu-id="39f9a-110">Ajouter un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="39f9a-110">Add a TXT record for SPF to help prevent email spam</span></span>](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [<span data-ttu-id="39f9a-111">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-111">Add the two SRV records that are required for Microsoft</span></span>](#add-the-two-srv-records-that-are-required-for-microsoft)
    
<span data-ttu-id="39f9a-112">Une fois ces enregistrements ajoutés sur OVH, votre domaine est configuré pour utiliser les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39f9a-112">After you add these records at OVH, your domain will be set up to work with Microsoft services.</span></span>
  
<span data-ttu-id="39f9a-113">Pour en savoir plus sur l’hébergement Web et le DNS pour les sites Web avec Microsoft, consultez [la rubrique utiliser un site Web public avec Microsoft](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span><span class="sxs-lookup"><span data-stu-id="39f9a-113">To learn about webhosting and DNS for websites with Microsoft, see [Use a public website with Microsoft](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).</span></span>
  
> [!NOTE]
>  <span data-ttu-id="39f9a-p101">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="39f9a-p101">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="39f9a-117">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="39f9a-117">Add a TXT record for verification</span></span>
<span data-ttu-id="39f9a-118"><a name="bkmk_txt"> </a></span><span class="sxs-lookup"><span data-stu-id="39f9a-118"><a name="bkmk_txt"> </a></span></span>

<span data-ttu-id="39f9a-119">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="39f9a-119">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="39f9a-120">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="39f9a-120">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="39f9a-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="39f9a-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="39f9a-123">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="39f9a-123">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="39f9a-124">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="39f9a-124">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="39f9a-126">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="39f9a-126">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="39f9a-128">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-128">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="39f9a-130">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-130">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="39f9a-132">Sélectionnez **txt**</span><span class="sxs-lookup"><span data-stu-id="39f9a-132">Select **TXT**</span></span>
    
    ![OVH Select TXT Entry](../../media/3aaa9dae-0b1d-436b-a980-b67a970f31a9.png)
  
6. <span data-ttu-id="39f9a-134">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39f9a-134">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="39f9a-135">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="39f9a-135">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="39f9a-136">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="39f9a-136">**Record type**</span></span>|<span data-ttu-id="39f9a-137">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="39f9a-137">**Sub-domain**</span></span>|<span data-ttu-id="39f9a-138">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-138">**TTL**</span></span>|<span data-ttu-id="39f9a-139">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-139">**Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="39f9a-140">TXT</span><span class="sxs-lookup"><span data-stu-id="39f9a-140">TXT</span></span>  <br/> |<span data-ttu-id="39f9a-141">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="39f9a-141">(leave blank)</span></span>  <br/> |<span data-ttu-id="39f9a-142">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="39f9a-142">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="39f9a-143">MS = msxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="39f9a-143">MS=msxxxxxxxx</span></span>  <br/> <span data-ttu-id="39f9a-144">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="39f9a-144">**Note:** This is an example.</span></span> <span data-ttu-id="39f9a-145">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="39f9a-145">Use your specific **Destination or Points to Address** value here, from the table.</span></span>           [<span data-ttu-id="39f9a-146">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="39f9a-146">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="39f9a-147">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-147">Select **Confirm**.</span></span> 
    
    ![OVH confirmer le TXT pour vérification](../../media/bde45596-9a55-4634-b5e7-16d7cde6e1b8.png)
  
8. <span data-ttu-id="39f9a-149">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="39f9a-149">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="39f9a-150">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez revenir à Microsoft et demander l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39f9a-150">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request the record.</span></span>
  
<span data-ttu-id="39f9a-151">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="39f9a-151">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="39f9a-152">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="39f9a-152">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="39f9a-153">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="39f9a-153">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="39f9a-154">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-154">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="39f9a-155">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-155">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="39f9a-p107">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="39f9a-p107">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft"></a><span data-ttu-id="39f9a-159">Ajouter un enregistrement MX afin que les courriers électroniques pour votre domaine soient envoyés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-159">Add an MX record so email for your domain will come to Microsoft</span></span>
<span data-ttu-id="39f9a-160"><a name="bkmk_mx"> </a></span><span class="sxs-lookup"><span data-stu-id="39f9a-160"><a name="bkmk_mx"> </a></span></span>

1. <span data-ttu-id="39f9a-161">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="39f9a-161">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="39f9a-162">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="39f9a-162">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="39f9a-164">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="39f9a-164">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="39f9a-166">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-166">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="39f9a-168">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-168">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="39f9a-170">Sélectionnez **MX**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-170">Select **MX**.</span></span>
    
    ![Type d’enregistrement MX OVH](../../media/29b5e54e-440a-41f2-9eb9-3de573922ddf.png)
  
6. <span data-ttu-id="39f9a-172">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39f9a-172">In the boxes for the new record, type or copy and paste the values from the following table.</span></span> <span data-ttu-id="39f9a-173">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="39f9a-173">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="39f9a-174">Par défaut OVH utilise la notation relative pour la cible, qui ajoute le nom de domaine à la fin de l’enregistrement cible.</span><span class="sxs-lookup"><span data-stu-id="39f9a-174">By default OVH uses relative notation for the target, which adds the domain name to the end of the target record.</span></span> <span data-ttu-id="39f9a-175">Pour utiliser la notation absolue, ajoutez un point à l’enregistrement cible comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="39f9a-175">To use absolute notation instead, add a dot to the target record as shown in the table below.</span></span> 
  
    |<span data-ttu-id="39f9a-176">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="39f9a-176">**Record type**</span></span>|<span data-ttu-id="39f9a-177">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="39f9a-177">**Sub-domain**</span></span>|<span data-ttu-id="39f9a-178">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-178">**TTL**</span></span>|<span data-ttu-id="39f9a-179">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-179">**Priority**</span></span>|<span data-ttu-id="39f9a-180">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-180">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="39f9a-181">MX</span><span class="sxs-lookup"><span data-stu-id="39f9a-181">MX</span></span>  <br/> |<span data-ttu-id="39f9a-182">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="39f9a-182">(leave blank)</span></span>  <br/> |<span data-ttu-id="39f9a-183">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="39f9a-183">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="39f9a-184">10 </span><span class="sxs-lookup"><span data-stu-id="39f9a-184">10</span></span>  <br/> <span data-ttu-id="39f9a-185">Pour plus d'informations sur la priorité, voir [Qu'est-ce que la priorité MX ?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx).</span><span class="sxs-lookup"><span data-stu-id="39f9a-185">For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx)</span></span> <br/> |<span data-ttu-id="39f9a-186">\<Key\>. mail.protection.Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-186">\<domain-key\>.mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="39f9a-187">**Remarque :** Obtenir votre \* \<clé\> de domaine\* à partir de votre compte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39f9a-187">**Note:** Get your  *\<domain-key\>*  from your Microsoft account.</span></span>  [<span data-ttu-id="39f9a-188">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="39f9a-188">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  |
   
    ![Enregistrement MX OVH pour le courrier électronique](../../media/6e2f5655-93e2-4620-8f19-c452e7edf8f0.png)
  
7. <span data-ttu-id="39f9a-190">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-190">Select **Next**.</span></span>
    
    ![Enregistrement MX OVH sélectionnez suivant](../../media/4db62d07-0dc4-49f6-bd19-2b4a07fd764a.png)
  
8. <span data-ttu-id="39f9a-192">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-192">Select **Confirm**.</span></span>
    
    ![Enregistrement MX OVH sélectionnez confirmer](../../media/090bfb11-a753-4af0-8982-582a4069a169.png)
  
9. <span data-ttu-id="39f9a-194">S’il existe d’autres enregistrements MX, supprimez-les tous dans la liste de la page **zone DNS** .</span><span class="sxs-lookup"><span data-stu-id="39f9a-194">If there are any other MX records, delete them all in the list on the **DNS zone** page.</span></span> <span data-ttu-id="39f9a-195">Sélectionnez chaque enregistrement, puis, dans la colonne **actions** , sélectionnez l’icône Corbeille-peut-être **supprimée** .</span><span class="sxs-lookup"><span data-stu-id="39f9a-195">Select each record and then, in the **Actions** column, select the trash-can **Delete** icon.</span></span> 
    
    ![OVH supprimer un enregistrement MX](../../media/892b328b-7057-4828-b8c5-fe26284dc8c2.png)
  
10. <span data-ttu-id="39f9a-197">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-197">Select **Confirm**.</span></span>
    
## <a name="add-the-cname-records-that-are-required-for-microsoft"></a><span data-ttu-id="39f9a-198">Ajouter les enregistrements CNAMe requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-198">Add the CNAME records that are required for Microsoft</span></span>
<span data-ttu-id="39f9a-199"><a name="bkmk_cname"> </a></span><span class="sxs-lookup"><span data-stu-id="39f9a-199"><a name="bkmk_cname"> </a></span></span>

1. <span data-ttu-id="39f9a-200">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="39f9a-200">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="39f9a-201">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="39f9a-201">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="39f9a-203">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="39f9a-203">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="39f9a-205">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-205">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="39f9a-207">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-207">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="39f9a-209">Sélectionnez **CNAME**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-209">Select **CNAME**.</span></span>
    
    ![OVH ajouter un type d’enregistrement CNAMe](../../media/33c7ac74-18d7-4ae1-9e27-1c0f9773a3c3.png)
  
6. <span data-ttu-id="39f9a-211">Créez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="39f9a-211">Create the first CNAME record.</span></span>
    
    <span data-ttu-id="39f9a-212">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39f9a-212">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="39f9a-213">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="39f9a-213">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="39f9a-214">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="39f9a-214">**Record type**</span></span>|<span data-ttu-id="39f9a-215">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="39f9a-215">**Sub-domain**</span></span>|<span data-ttu-id="39f9a-216">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-216">**Target**</span></span>|<span data-ttu-id="39f9a-217">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-217">**TTL**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="39f9a-218">CNAME</span><span class="sxs-lookup"><span data-stu-id="39f9a-218">CNAME</span></span>  <br/> |<span data-ttu-id="39f9a-219">autodiscover</span><span class="sxs-lookup"><span data-stu-id="39f9a-219">autodiscover</span></span>  <br/> |<span data-ttu-id="39f9a-220">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-220">autodiscover.outlook.com.</span></span>  <br/> |<span data-ttu-id="39f9a-221">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="39f9a-221">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="39f9a-222">CNAME</span><span class="sxs-lookup"><span data-stu-id="39f9a-222">CNAME</span></span>  <br/> |<span data-ttu-id="39f9a-223">sip</span><span class="sxs-lookup"><span data-stu-id="39f9a-223">sip</span></span>  <br/> |<span data-ttu-id="39f9a-224">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-224">sipdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="39f9a-225">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="39f9a-225">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="39f9a-226">CNAME</span><span class="sxs-lookup"><span data-stu-id="39f9a-226">CNAME</span></span>  <br/> |<span data-ttu-id="39f9a-227">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="39f9a-227">lyncdiscover</span></span>  <br/> |<span data-ttu-id="39f9a-228">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-228">webdir.online.lync.com.</span></span>  <br/> |<span data-ttu-id="39f9a-229">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="39f9a-229">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="39f9a-230">CNAME</span><span class="sxs-lookup"><span data-stu-id="39f9a-230">CNAME</span></span>  <br/> |<span data-ttu-id="39f9a-231">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="39f9a-231">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="39f9a-232">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="39f9a-232">enterpriseregistration.windows.net.</span></span>  <br/> |<span data-ttu-id="39f9a-233">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="39f9a-233">3600 seconds</span></span>  <br/> |
    |<span data-ttu-id="39f9a-234">CNAME</span><span class="sxs-lookup"><span data-stu-id="39f9a-234">CNAME</span></span>  <br/> |<span data-ttu-id="39f9a-235">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="39f9a-235">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="39f9a-236">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-236">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> |<span data-ttu-id="39f9a-237">3600 secondes</span><span class="sxs-lookup"><span data-stu-id="39f9a-237">3600 seconds</span></span>  <br/> |
   
    ![Enregistrement CNAMe OVH](../../media/516938b3-0b12-4736-a631-099e12e189f5.png)
  
7. <span data-ttu-id="39f9a-239">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-239">Select **Next**.</span></span>
    
    ![OVH ajouter des valeurs CNAMe et sélectionner suivant](../../media/f9481cb1-559d-4da1-9643-9cacb0d80d29.png)
  
8. <span data-ttu-id="39f9a-241">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-241">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="39f9a-242">Répétez les étapes précédentes pour créer les cinq autres enregistrements CNAMe.</span><span class="sxs-lookup"><span data-stu-id="39f9a-242">Repeat the previous steps to create the other five CNAME records.</span></span>
    
    <span data-ttu-id="39f9a-243">Pour chaque enregistrement, tapez ou copiez-collez les valeurs de la ligne suivante du tableau ci-dessus dans les zones de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39f9a-243">For each record, type or copy and paste the values from the next row of the table above into the boxes for that record.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="39f9a-244">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="39f9a-244">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="39f9a-245"><a name="bkmk_spf"> </a></span><span class="sxs-lookup"><span data-stu-id="39f9a-245"><a name="bkmk_spf"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="39f9a-246">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="39f9a-246">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="39f9a-247">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="39f9a-247">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="39f9a-248">Si vous disposez déjà d’un enregistrement SPF pour votre domaine, n’en créez pas pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39f9a-248">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="39f9a-249">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de disposer d’un *seul* enregistrement SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="39f9a-249">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> 
  
1. <span data-ttu-id="39f9a-250">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="39f9a-250">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="39f9a-251">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="39f9a-251">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="39f9a-253">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="39f9a-253">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="39f9a-255">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-255">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="39f9a-257">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-257">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="39f9a-259">Sélectionnez **txt**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-259">Select **TXT**.</span></span>
    
6. <span data-ttu-id="39f9a-260">In the boxes for the new record, type or copy and paste the following values.</span><span class="sxs-lookup"><span data-stu-id="39f9a-260">In the boxes for the new record, type or copy and paste the following values.</span></span>
    
    |<span data-ttu-id="39f9a-261">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="39f9a-261">**Record type**</span></span>|<span data-ttu-id="39f9a-262">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="39f9a-262">**Sub-domain**</span></span>|<span data-ttu-id="39f9a-263">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-263">**TTL**</span></span>|<span data-ttu-id="39f9a-264">**VALEUR TXT**</span><span class="sxs-lookup"><span data-stu-id="39f9a-264">**TXT Value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="39f9a-265">TXT</span><span class="sxs-lookup"><span data-stu-id="39f9a-265">TXT</span></span>  <br/> |<span data-ttu-id="39f9a-266">(Laisser vide)</span><span class="sxs-lookup"><span data-stu-id="39f9a-266">(leave blank)</span></span>  <br/> |<span data-ttu-id="39f9a-267">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="39f9a-267">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="39f9a-268">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="39f9a-268">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="39f9a-269">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="39f9a-269">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![OVH ajouter un enregistrement TXT pour SPF](../../media/f50466e9-1557-4548-8a39-e98978a5ee2e.png)
  
7. <span data-ttu-id="39f9a-271">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-271">Select **Next**.</span></span>
    
    ![OVH ajouter un enregistrement TXT pour SPF et sélectionner suivant](../../media/7937eb7c-114f-479f-a916-bcbe476d6108.png)
  
8. <span data-ttu-id="39f9a-273">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-273">Select **Confirm**.</span></span>
    
    ![OVH ajouter un enregistrement TXT pour SPF et confirmer](../../media/649eefeb-3227-49e3-98a0-1ce19c42fa54.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft"></a><span data-ttu-id="39f9a-275">Ajouter les deux enregistrements SRV requis pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="39f9a-275">Add the two SRV records that are required for Microsoft</span></span>
<span data-ttu-id="39f9a-276"><a name="bkmk_srv"> </a></span><span class="sxs-lookup"><span data-stu-id="39f9a-276"><a name="bkmk_srv"> </a></span></span>

1. <span data-ttu-id="39f9a-277">Pour commencer, accédez à la page de vos domaines dans OVH à l’aide de [ce lien](https://www.ovh.com/manager/).</span><span class="sxs-lookup"><span data-stu-id="39f9a-277">To get started, go to your domains page in OVH by using [this link](https://www.ovh.com/manager/).</span></span> <span data-ttu-id="39f9a-278">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="39f9a-278">You'll be prompted to log in.</span></span>
    
    ![Connexion OVH](../../media/1424cc15-720d-49d1-b99b-8ba63b216238.png)
  
2. <span data-ttu-id="39f9a-280">Sous **domaines**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="39f9a-280">Under **Domains**, select the name of the domain that you want edit.</span></span>
    
    ![OVH sélectionnez le domaine](../../media/fe407909-4ea6-4b92-a3bd-dec4022b1d8d.png)
  
3. <span data-ttu-id="39f9a-282">Sélectionnez **zone DNS**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-282">Select **DNS zone**.</span></span>
    
    ![OVH sélectionner une zone DNS](../../media/45218cbe-f3f8-4804-87f9-cfcef89ea113.png)
  
4. <span data-ttu-id="39f9a-284">Sélectionnez **Ajouter une entrée**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-284">Select **Add an entry**.</span></span>
    
    ![OVH ajouter une entrée](../../media/13ded54b-9e48-4c98-8e1b-8c4a99633bc0.png)
  
5. <span data-ttu-id="39f9a-286">Sélectionnez **SRV**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-286">Select **SRV**.</span></span>
    
    ![OVH sélectionner un type d’enregistrement SRV](../../media/66bad536-a531-4a4e-b08d-c0d99f6ea1b2.png)
  
6. <span data-ttu-id="39f9a-288">Créez le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="39f9a-288">Create the first SRV record.</span></span>
    
    <span data-ttu-id="39f9a-289">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39f9a-289">In the boxes for the new record, type or copy and paste the values from the first row of the following table.</span></span> <span data-ttu-id="39f9a-290">Pour affecter une valeur de durée de vie, sélectionnez **personnalisée** dans la liste déroulante, puis tapez la valeur dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="39f9a-290">To assign a TTL value, choose **Personalized** from the drop-down list, and then type the value in the text box.</span></span> 
    
    |<span data-ttu-id="39f9a-291">**Type d'enregistrement**</span><span class="sxs-lookup"><span data-stu-id="39f9a-291">**Record type**</span></span>|<span data-ttu-id="39f9a-292">**Sous-domaine**</span><span class="sxs-lookup"><span data-stu-id="39f9a-292">**Sub-domain**</span></span>|<span data-ttu-id="39f9a-293">**Priority (Priorité)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-293">**Priority**</span></span>|<span data-ttu-id="39f9a-294">**Weight (Poids)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-294">**Weight**</span></span>|<span data-ttu-id="39f9a-295">**Port (Port)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-295">**Port**</span></span>|<span data-ttu-id="39f9a-296">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-296">**TTL**</span></span>|<span data-ttu-id="39f9a-297">**Target (Cible)**</span><span class="sxs-lookup"><span data-stu-id="39f9a-297">**Target**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="39f9a-298">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="39f9a-298">SRV (Service)</span></span>  <br/> |<span data-ttu-id="39f9a-299">_sip. _tls</span><span class="sxs-lookup"><span data-stu-id="39f9a-299">_sip._tls</span></span>  <br/> |<span data-ttu-id="39f9a-300">100</span><span class="sxs-lookup"><span data-stu-id="39f9a-300">100</span></span>  <br/> |<span data-ttu-id="39f9a-301">0,1</span><span class="sxs-lookup"><span data-stu-id="39f9a-301">1</span></span>  <br/> |<span data-ttu-id="39f9a-302">443</span><span class="sxs-lookup"><span data-stu-id="39f9a-302">443</span></span>  <br/> |<span data-ttu-id="39f9a-303">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="39f9a-303">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="39f9a-304">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-304">sipdir.online.lync.com.</span></span>  <br/> |
    |<span data-ttu-id="39f9a-305">SRV (Service)</span><span class="sxs-lookup"><span data-stu-id="39f9a-305">SRV (Service)</span></span>  <br/> |<span data-ttu-id="39f9a-306">_sipfederationtls. _tcp</span><span class="sxs-lookup"><span data-stu-id="39f9a-306">_sipfederationtls._tcp</span></span>  <br/> |<span data-ttu-id="39f9a-307">100</span><span class="sxs-lookup"><span data-stu-id="39f9a-307">100</span></span>  <br/> |<span data-ttu-id="39f9a-308">0,1</span><span class="sxs-lookup"><span data-stu-id="39f9a-308">1</span></span>  <br/> |<span data-ttu-id="39f9a-309">5061</span><span class="sxs-lookup"><span data-stu-id="39f9a-309">5061</span></span>  <br/> |<span data-ttu-id="39f9a-310">3600 (secondes)</span><span class="sxs-lookup"><span data-stu-id="39f9a-310">3600 (seconds)</span></span>  <br/> |<span data-ttu-id="39f9a-311">sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="39f9a-311">sipfed.online.lync.com.</span></span>  <br/> |
       
    ![Enregistrement SRV OVH](../../media/73956b9e-9e4f-40a5-803e-c4ead2f77fa6.png)
  
7. <span data-ttu-id="39f9a-313">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-313">Select **Next**.</span></span>
    
    ![Enregistrement SRV OVH sélectionner suivant](../../media/cb4ad7e2-a8f0-4ab1-9797-d1b51c1d2da9.png)
  
8. <span data-ttu-id="39f9a-315">Sélectionnez **confirmer**.</span><span class="sxs-lookup"><span data-stu-id="39f9a-315">Select **Confirm**.</span></span>
    
9. <span data-ttu-id="39f9a-316">Répétez les étapes précédentes pour créer l’autre enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="39f9a-316">Repeat the previous steps to create the other SRV record.</span></span> <span data-ttu-id="39f9a-317">Tapez ou copiez-collez les valeurs de la deuxième ligne du tableau ci-dessus dans les zones du deuxième enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39f9a-317">Type or copy and paste the values from the second row of the table above into the boxes for the second record.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="39f9a-p120">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="39f9a-p120">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
