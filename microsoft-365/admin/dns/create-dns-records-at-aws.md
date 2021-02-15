---
title: Créer des enregistrements DNS sur Amazon Web Services (AWS) pour Microsoft
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
ms.assetid: 7a2efd75-0771-4897-ba7b-082fe5bfa9da
description: Découvrez comment vérifier votre domaine et configurer les enregistrements DNS pour la messagerie, Skype Entreprise Online et d’autres services sur Amazon Web Services (AWS) pour Microsoft.
ms.openlocfilehash: bb687b8685aed79f5f768c12d652205bbbed0f59
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49657971"
---
# <a name="create-dns-records-at-amazon-web-services-aws-for-microsoft"></a><span data-ttu-id="25db4-103">Créer des enregistrements DNS sur Amazon Web Services (AWS) pour Microsoft</span><span class="sxs-lookup"><span data-stu-id="25db4-103">Create DNS records at Amazon Web Services (AWS) for Microsoft</span></span>

 <span data-ttu-id="25db4-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="25db4-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="25db4-105">Si AWS est votre fournisseur d’hébergement DNS, suivez les étapes de cet article pour vérifier votre domaine et configurer les enregistrements DNS pour le courrier, Skype Online pour les entreprises, etc.</span><span class="sxs-lookup"><span data-stu-id="25db4-105">If AWS is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype Online for Business, and so on.</span></span>
  
<span data-ttu-id="25db4-106">Une fois ces enregistrements ajoutés sur AWS, votre domaine est installé pour fonctionner avec les services Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25db4-106">After you add these records at AWS, your domain will be set up to work with Microsoft services.</span></span>
  

  
> [!NOTE]
> <span data-ttu-id="25db4-107">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="25db4-107">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="25db4-108">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="25db4-108">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="25db4-109">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="25db4-109">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="25db4-110">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="25db4-110">Add a TXT record for verification</span></span>
<span data-ttu-id="25db4-111"><a name="BKMK_verify"> </a></span><span class="sxs-lookup"><span data-stu-id="25db4-111"><a name="BKMK_verify"> </a></span></span>

<span data-ttu-id="25db4-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="25db4-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="25db4-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="25db4-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="25db4-p104">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="25db4-p104">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="25db4-118">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="25db4-118">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="25db4-119">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="25db4-119">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="25db4-120">Sélectionnez **Créer un jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-120">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="25db4-121">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="25db4-121">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="25db4-122">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span><span class="sxs-lookup"><span data-stu-id="25db4-122">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="25db4-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span><span class="sxs-lookup"><span data-stu-id="25db4-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span></span> 
  
    |||||||
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="25db4-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="25db4-125">**Name**</span></span> <br/> |<span data-ttu-id="25db4-126">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="25db4-126">**Type**</span></span> <br/> |<span data-ttu-id="25db4-127">**Alias**</span><span class="sxs-lookup"><span data-stu-id="25db4-127">**Alias**</span></span> <br/> |<span data-ttu-id="25db4-128">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="25db4-128">**TTL (Seconds)**</span></span> <br/> |<span data-ttu-id="25db4-129">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="25db4-129">**Value**</span></span> <br/> |<span data-ttu-id="25db4-130">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="25db4-130">**Routing Policy**</span></span> <br/> |
    |<span data-ttu-id="25db4-131">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="25db4-131">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="25db4-132">TXT - Text</span><span class="sxs-lookup"><span data-stu-id="25db4-132">TXT - Text</span></span>  <br/> |<span data-ttu-id="25db4-133">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-133">No</span></span>  <br/> |<span data-ttu-id="25db4-134">300</span><span class="sxs-lookup"><span data-stu-id="25db4-134">300</span></span>  <br/> |<span data-ttu-id="25db4-135">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="25db4-135">MS=ms *XXXXXXXX*</span></span>  <br/><span data-ttu-id="25db4-136">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="25db4-136">**Note:** This is an example.</span></span> <span data-ttu-id="25db4-137">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25db4-137">Use your specific **Destination or Points to Address** value here, from the table in Microsoft 365.</span></span> [<span data-ttu-id="25db4-138">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="25db4-138">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="25db4-139">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-139">Simple</span></span>  <br/> |
   
6. <span data-ttu-id="25db4-140">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="25db4-140">Select **Create**.</span></span>
    
7. <span data-ttu-id="25db4-141">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="25db4-141">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="25db4-142">Maintenant que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous revenir à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="25db4-142">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="25db4-143">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="25db4-143">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="25db4-144">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="25db4-144">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="25db4-145">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="25db4-145">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="25db4-146">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="25db4-146">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="25db4-147">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="25db4-147">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="25db4-148">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="25db4-148">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="25db4-149">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="25db4-149">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="25db4-150">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="25db4-150">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="add-an-mx-record-so-email-for-your-domain-will-come-to-microsoft-365"></a><span data-ttu-id="25db4-151">Ajouter un enregistrement MX afin que le courrier électronique de votre domaine soit envoyé à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="25db4-151">Add an MX record so email for your domain will come to Microsoft 365</span></span>
<span data-ttu-id="25db4-152"><a name="BKMK_add_MX"> </a></span><span class="sxs-lookup"><span data-stu-id="25db4-152"><a name="BKMK_add_MX"> </a></span></span>

1. <span data-ttu-id="25db4-p108">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="25db4-p108">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="25db4-155">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="25db4-155">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="25db4-156">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="25db4-156">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="25db4-157">Sélectionnez **Créer un jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-157">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="25db4-158">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="25db4-158">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="25db4-159">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span><span class="sxs-lookup"><span data-stu-id="25db4-159">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="25db4-160">**Name**</span><span class="sxs-lookup"><span data-stu-id="25db4-160">**Name**</span></span>|<span data-ttu-id="25db4-161">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="25db4-161">**Type**</span></span>|<span data-ttu-id="25db4-162">**Alias**</span><span class="sxs-lookup"><span data-stu-id="25db4-162">**Alias**</span></span>|<span data-ttu-id="25db4-163">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="25db4-163">**TTL (Seconds)**</span></span>|<span data-ttu-id="25db4-164">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="25db4-164">**Value**</span></span>|<span data-ttu-id="25db4-165">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="25db4-165">**Routing Policy**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="25db4-166">(Laissez ce champ vide.)</span><span class="sxs-lookup"><span data-stu-id="25db4-166">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="25db4-167">MX - Serveur de courrier</span><span class="sxs-lookup"><span data-stu-id="25db4-167">MX - Mail exchange</span></span>  <br/> |<span data-ttu-id="25db4-168">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-168">No</span></span>  <br/> |<span data-ttu-id="25db4-169">300</span><span class="sxs-lookup"><span data-stu-id="25db4-169">300</span></span>  <br/> |<span data-ttu-id="25db4-170">0  *\<domain-key\>*  .mail.protection.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-170">0  *\<domain-key\>*  .mail.protection.outlook.com.</span></span>  <br/> <span data-ttu-id="25db4-p109">La valeur 0 est la valeur de priorité Max. Ajoutez-la au début de la valeur MX, séparée du reste de la valeur par une espace.  </span><span class="sxs-lookup"><span data-stu-id="25db4-p109">The 0 is the MX priority value. Add it to the beginning of the MX value, separated from the remainder of the value by a space.  </span></span><br/> <span data-ttu-id="25db4-173">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-173">**This value MUST end with a period (.)**</span></span> <br/> <span data-ttu-id="25db4-174">**Remarque :** Obtenez votre \<*domain-key*\> compte Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25db4-174">**Note:** Get your \<*domain-key*\> from your Microsoft 365 account.</span></span> [<span data-ttu-id="25db4-175">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="25db4-175">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |<span data-ttu-id="25db4-176">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-176">Simple</span></span>  <br/> |
       
    ![AWS-BP-Configure-2-1](../../media/94a71ce7-1b3b-4b1a-9ad3-9592db133075.png)
  
6. <span data-ttu-id="25db4-178">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="25db4-178">Select **Create**.</span></span>
    
    ![AWS-BP-Configurer-2-2](../../media/1c050c72-c04f-48d5-a8e9-44cd83ddd33e.png)
  
7. <span data-ttu-id="25db4-180">S'il existe d'autres enregistrements MX, supprimez-les.</span><span class="sxs-lookup"><span data-stu-id="25db4-180">If there are any other MX records, remove them.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="25db4-181">AWS stocke les enregistrements MX en tant qu'ensemble pouvant contenir plusieurs enregistrements.</span><span class="sxs-lookup"><span data-stu-id="25db4-181">AWS stores MX records as a set that may contain multiple records.</span></span> <span data-ttu-id="25db4-182">**NE sélectionnez** **PAS Supprimer le jeu d’enregistrements,** car cela supprimera tous vos enregistrements MX, y compris celui que vous viennent d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="25db4-182">**DO NOT** select **Delete Record Set**, as this will delete all of your MX records, including the one you just added.</span></span> <span data-ttu-id="25db4-183">Suivez plutôt les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="25db4-183">Use the following instructions instead.</span></span> 
  
    <span data-ttu-id="25db4-184">Tout d’abord, sélectionnez le jeu d’enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="25db4-184">First, select the MX record set.</span></span>
    
    ![AWS-BP-Configurer-2-3](../../media/9d9388cb-e2d0-43b7-928c-e1d07e519c6f.png)
  
    <span data-ttu-id="25db4-186">Ensuite, dans la zone **Edit Record Set (Modifier le jeu d'enregistrements)**, supprimez chaque enregistrement MX obsolète en sélectionnant son entrée dans la zone **Value (Valeur)** en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="25db4-186">Next, in the **Edit Record Set** area, delete each obsolete MX record by selecting the entry in the **Value** box and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![AWS-BP-Configurer-2-4](../../media/c3b0c1bc-21ab-44cc-84b7-f504725c5540.png)
  
8. <span data-ttu-id="25db4-188">Sélectionnez **Enregistrer le jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-188">Select **Save Record Set**.</span></span>
    
    ![AWS-BP-Configurer-2-5](../../media/86f0998d-f5d4-4750-a93d-ac13b318c40b.png)
  
## <a name="add-the-five-cname-records-that-are-required-for-microsoft-365"></a><span data-ttu-id="25db4-190">Ajouter les cinq enregistrements CNAME requis pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="25db4-190">Add the five CNAME records that are required for Microsoft 365</span></span>
<span data-ttu-id="25db4-191"><a name="BKMK_add_CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="25db4-191"><a name="BKMK_add_CNAME"> </a></span></span>

1. <span data-ttu-id="25db4-p112">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="25db4-p112">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="25db4-194">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="25db4-194">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="25db4-195">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="25db4-195">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="25db4-196">Sélectionnez **Créer un jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-196">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="25db4-197">Ajoutez le premier enregistrement CNAME.</span><span class="sxs-lookup"><span data-stu-id="25db4-197">Add the first CNAME record.</span></span>
    
    <span data-ttu-id="25db4-198">Dans la zone **Create Record Set (Créer un jeu d'enregistrements)**, dans les champs du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="25db4-198">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="25db4-199">(Sélectionnez les valeurs **Type (Type)** et **Routing Policy (Stratégie de routage)** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="25db4-199">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="25db4-200">**Name**</span><span class="sxs-lookup"><span data-stu-id="25db4-200">**Name**</span></span>|<span data-ttu-id="25db4-201">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="25db4-201">**Type**</span></span>|<span data-ttu-id="25db4-202">**Alias**</span><span class="sxs-lookup"><span data-stu-id="25db4-202">**Alias**</span></span>|<span data-ttu-id="25db4-203">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="25db4-203">**TTL (Seconds)**</span></span>|<span data-ttu-id="25db4-204">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="25db4-204">**Value**</span></span>|<span data-ttu-id="25db4-205">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="25db4-205">**Routing Policy**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="25db4-206">autodiscover</span><span class="sxs-lookup"><span data-stu-id="25db4-206">autodiscover</span></span>  <br/> |<span data-ttu-id="25db4-207">CNAME - Nom canonique</span><span class="sxs-lookup"><span data-stu-id="25db4-207">CNAME - Canonical name</span></span>  <br/> |<span data-ttu-id="25db4-208">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-208">No</span></span>  <br/> |<span data-ttu-id="25db4-209">300</span><span class="sxs-lookup"><span data-stu-id="25db4-209">300</span></span>  <br/> |<span data-ttu-id="25db4-210">autodiscover.outlook.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-210">autodiscover.outlook.com.</span></span>  <br/> <span data-ttu-id="25db4-211">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-211">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="25db4-212">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-212">Simple</span></span>  <br/> |
    |<span data-ttu-id="25db4-213">sip</span><span class="sxs-lookup"><span data-stu-id="25db4-213">sip</span></span>  <br/> |<span data-ttu-id="25db4-214">CNAME - Nom canonique</span><span class="sxs-lookup"><span data-stu-id="25db4-214">CNAME - Canonical name</span></span>  <br/> |<span data-ttu-id="25db4-215">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-215">No</span></span>  <br/> |<span data-ttu-id="25db4-216">300</span><span class="sxs-lookup"><span data-stu-id="25db4-216">300</span></span>  <br/> |<span data-ttu-id="25db4-217">sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-217">sipdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="25db4-218">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-218">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="25db4-219">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-219">Simple</span></span>  <br/> |
    |<span data-ttu-id="25db4-220">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="25db4-220">lyncdiscover</span></span>  <br/> |<span data-ttu-id="25db4-221">CNAME - Nom canonique</span><span class="sxs-lookup"><span data-stu-id="25db4-221">CNAME - Canonical name</span></span>  <br/> |<span data-ttu-id="25db4-222">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-222">No</span></span>  <br/> |<span data-ttu-id="25db4-223">300</span><span class="sxs-lookup"><span data-stu-id="25db4-223">300</span></span>  <br/> |<span data-ttu-id="25db4-224">webdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-224">webdir.online.lync.com.</span></span>  <br/> <span data-ttu-id="25db4-225">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-225">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="25db4-226">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-226">Simple</span></span>  <br/> |
    |<span data-ttu-id="25db4-227">enterpriseregistration</span><span class="sxs-lookup"><span data-stu-id="25db4-227">enterpriseregistration</span></span>  <br/> |<span data-ttu-id="25db4-228">CNAME - Nom canonique</span><span class="sxs-lookup"><span data-stu-id="25db4-228">CNAME - Canonical name</span></span>  <br/> |<span data-ttu-id="25db4-229">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-229">No</span></span>  <br/> |<span data-ttu-id="25db4-230">300</span><span class="sxs-lookup"><span data-stu-id="25db4-230">300</span></span>  <br/> |<span data-ttu-id="25db4-231">enterpriseregistration.windows.net.</span><span class="sxs-lookup"><span data-stu-id="25db4-231">enterpriseregistration.windows.net.</span></span>  <br/> <span data-ttu-id="25db4-232">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-232">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="25db4-233">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-233">Simple</span></span>  <br/> |
    |<span data-ttu-id="25db4-234">enterpriseenrollment</span><span class="sxs-lookup"><span data-stu-id="25db4-234">enterpriseenrollment</span></span>  <br/> |<span data-ttu-id="25db4-235">CNAME - Nom canonique</span><span class="sxs-lookup"><span data-stu-id="25db4-235">CNAME - Canonical name</span></span>  <br/> |<span data-ttu-id="25db4-236">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-236">No</span></span>  <br/> |<span data-ttu-id="25db4-237">300</span><span class="sxs-lookup"><span data-stu-id="25db4-237">300</span></span>  <br/> |<span data-ttu-id="25db4-238">enterpriseenrollment-s.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-238">enterpriseenrollment-s.manage.microsoft.com.</span></span>  <br/> <span data-ttu-id="25db4-239">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-239">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="25db4-240">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-240">Simple</span></span>  <br/> |
   
    ![AWS-BP-Configure-3-1](../../media/895c71bd-0e3a-425e-9681-98c1c67e714b.png)
  
6. <span data-ttu-id="25db4-242">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="25db4-242">Select **Create**.</span></span>
    
    ![AWS-BP-Configurer-3-2](../../media/33964846-5282-44a4-b241-62ce02b96735.png)
  
7. <span data-ttu-id="25db4-244">Ajoutez les quatre autres enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="25db4-244">Add the other four CNAME records.</span></span>
    
    <span data-ttu-id="25db4-245">Dans la page **Zones** hébergées, sélectionnez Créer un jeu d’enregistrement, créez  un enregistrement à l’aide des valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau Créer pour terminer cet enregistrement. </span><span class="sxs-lookup"><span data-stu-id="25db4-245">In the **Hosted Zones** page, select **Create Record Set**, create a record using the values from the next row in the table, and then again select **Create** to complete that record.</span></span> 
    
    <span data-ttu-id="25db4-246">Répétez ce processus jusqu’à ce que vous avez créé les cinq enregistrements CNAME.</span><span class="sxs-lookup"><span data-stu-id="25db4-246">Repeat this process until you have created all five CNAME records.</span></span>
    
## <a name="add-a-txt-record-for-spf-to-help-prevent-email-spam"></a><span data-ttu-id="25db4-247">Ajoutez un enregistrement TXT pour SPF afin d'éviter le courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="25db4-247">Add a TXT record for SPF to help prevent email spam</span></span>
<span data-ttu-id="25db4-248"><a name="BKMK_add_TXT"> </a></span><span class="sxs-lookup"><span data-stu-id="25db4-248"><a name="BKMK_add_TXT"> </a></span></span>

> [!IMPORTANT]
> <span data-ttu-id="25db4-249">Vous ne pouvez avoir qu’un enregistrement TXT pour SPF pour un domaine.</span><span class="sxs-lookup"><span data-stu-id="25db4-249">You cannot have more than one TXT record for SPF for a domain.</span></span> <span data-ttu-id="25db4-250">Si votre domaine comporte plusieurs enregistrements SPF, vous rencontrez des erreurs au niveau de la transmission du courrier électronique ainsi que des problèmes de remise du courrier et de classification en tant que courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="25db4-250">If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues.</span></span> <span data-ttu-id="25db4-251">Si vous avez déjà un enregistrement SPF pour votre domaine, il n’est pas nécessaire d’en créer un nouveau pour Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25db4-251">If you already have an SPF record for your domain, don't create a new one for Microsoft.</span></span> <span data-ttu-id="25db4-252">Ajoutez plutôt les valeurs Microsoft requises à l’enregistrement actuel afin de n’avoir qu’un seul  *enregistrement*  SPF qui inclut les deux ensembles de valeurs.</span><span class="sxs-lookup"><span data-stu-id="25db4-252">Instead, add the required Microsoft values to the current record so that you have a  *single*  SPF record that includes both sets of values.</span></span> <span data-ttu-id="25db4-253">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="25db4-253">Need examples?</span></span> <span data-ttu-id="25db4-254">Consultez ces [Enregistrements DNS externes pour Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span><span class="sxs-lookup"><span data-stu-id="25db4-254">Check out these [External Domain Name System records for Microsoft](https://docs.microsoft.com/microsoft-365/enterprise/external-domain-name-system-records).</span></span> <span data-ttu-id="25db4-255">Pour valider votre enregistrement SPF, vous pouvez utiliser l’un de ces outils[de validation SPF.](../setup/domains-faq.yml)</span><span class="sxs-lookup"><span data-stu-id="25db4-255">To validate your SPF record, you can use one of these[SPF validation tools](../setup/domains-faq.yml).</span></span> 
  
1. <span data-ttu-id="25db4-256">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home).</span><span class="sxs-lookup"><span data-stu-id="25db4-256">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home).</span></span> <span data-ttu-id="25db4-257">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="25db4-257">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="25db4-258">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="25db4-258">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="25db4-259">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="25db4-259">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="25db4-260">Sélectionnez **le jeu d’enregistrement TXT.**</span><span class="sxs-lookup"><span data-stu-id="25db4-260">Select the **TXT** record set.</span></span> 
    
    ![AWS-BP-Configurer-4-1](../../media/0310fa66-c016-4987-80df-930f1c8f3c39.png)
  
5. <span data-ttu-id="25db4-p115">Dans la zone **Edit Record Set (Modifier le jeu d'enregistrements)**, à la fin de l'entrée active dans le champ **Value (Valeur)** pour l'enregistrement existant, appuyez sur la touche Entrée de votre clavier pour créer une ligne. Ensuite, dans cette nouvelle ligne (sous la valeur existante), tapez ou copiez-collez la valeur du tableau suivant (vous pouvez voir un exemple dans l'illustration située sous le tableau).</span><span class="sxs-lookup"><span data-stu-id="25db4-p115">In the **Edit Record Set** area, at the end of the current entry in the **Value:** box for the existing record, press Enter on your keyboard to create a new line; and then, on that new line (under the existing value), type or copy and paste the value from the following table. (You can see an example in the illustration below the table.)</span></span> 
    
    |<span data-ttu-id="25db4-264">**Valeur :**</span><span class="sxs-lookup"><span data-stu-id="25db4-264">**Value:**</span></span>|
    |:-----|
    |<span data-ttu-id="25db4-265">v=spf1 include:spf.protection.outlook.com -all</span><span class="sxs-lookup"><span data-stu-id="25db4-265">v=spf1 include:spf.protection.outlook.com -all</span></span>  <br/> <span data-ttu-id="25db4-p116">(Les guillemets requis pour les instructions à l'écran sont insérés automatiquement. Vous n'avez pas besoin de les entrer manuellement.)  </span><span class="sxs-lookup"><span data-stu-id="25db4-p116">(The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.)  </span></span><br/> <span data-ttu-id="25db4-268">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="25db4-268">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |
   
    ![AWS-BP-Configure-4-2](../../media/beb3c086-eaf8-4245-9860-18512a3ff72e.png)
  
6. <span data-ttu-id="25db4-270">Sélectionnez **Enregistrer le jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-270">Select **Save Record Set**.</span></span>
    
    ![AWS-BP-Configurer-4-3](../../media/94b9306c-bdc9-4f84-ad6f-6d12edbfde90.png)
  
## <a name="add-the-two-srv-records-that-are-required-for-microsoft-365"></a><span data-ttu-id="25db4-272">Ajouter les deux enregistrements SRV requis pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="25db4-272">Add the two SRV records that are required for Microsoft 365</span></span>
<span data-ttu-id="25db4-273"><a name="BKMK_add_SRV"> </a></span><span class="sxs-lookup"><span data-stu-id="25db4-273"><a name="BKMK_add_SRV"> </a></span></span>

1. <span data-ttu-id="25db4-p117">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="25db4-p117">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="25db4-276">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="25db4-276">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="25db4-277">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="25db4-277">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="25db4-278">Sélectionnez **Créer un jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="25db4-278">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="25db4-279">Ajouter le premier enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="25db4-279">Add the first SRV record:</span></span>
    
    <span data-ttu-id="25db4-280">Dans la zone **Create Record Set (Créer un jeu d'enregistrements)**, dans les champs du nouvel enregistrement, tapez ou copiez-collez les valeurs de la première ligne du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="25db4-280">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the first row in the following table.</span></span> 
    
    <span data-ttu-id="25db4-281">(Sélectionnez les valeurs **Type (Type)** et **Routing Policy (Stratégie de routage)** dans les listes déroulantes.)</span><span class="sxs-lookup"><span data-stu-id="25db4-281">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    |<span data-ttu-id="25db4-282">**Name**</span><span class="sxs-lookup"><span data-stu-id="25db4-282">**Name**</span></span>|<span data-ttu-id="25db4-283">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="25db4-283">**Type**</span></span>|<span data-ttu-id="25db4-284">**Alias**</span><span class="sxs-lookup"><span data-stu-id="25db4-284">**Alias**</span></span>|<span data-ttu-id="25db4-285">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="25db4-285">**TTL (Seconds)**</span></span>|<span data-ttu-id="25db4-286">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="25db4-286">**Value**</span></span>|<span data-ttu-id="25db4-287">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="25db4-287">**Routing Policy**</span></span>|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |<span data-ttu-id="25db4-288">_sip._tls</span><span class="sxs-lookup"><span data-stu-id="25db4-288">_sip._tls</span></span>|<span data-ttu-id="25db4-289">SRV - Localisation de service</span><span class="sxs-lookup"><span data-stu-id="25db4-289">SRV - Service locator</span></span>|<span data-ttu-id="25db4-290">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-290">No</span></span>|<span data-ttu-id="25db4-291">300</span><span class="sxs-lookup"><span data-stu-id="25db4-291">300</span></span>|<span data-ttu-id="25db4-292">100 1 443 sipdir.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-292">100 1 443 sipdir.online.lync.com.</span></span> <span data-ttu-id="25db4-293">**Cette valeur DOIT se terminer par un point (.)**></span><span class="sxs-lookup"><span data-stu-id="25db4-293">**This value MUST end with a period (.)**></span></span><br> <span data-ttu-id="25db4-294">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="25db4-294">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="25db4-295">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-295">Simple</span></span>|
    |<span data-ttu-id="25db4-296">_sipfederationtls._tcp</span><span class="sxs-lookup"><span data-stu-id="25db4-296">_sipfederationtls._tcp</span></span>|<span data-ttu-id="25db4-297">SRV - Localisation de service</span><span class="sxs-lookup"><span data-stu-id="25db4-297">SRV - Service locator</span></span>|<span data-ttu-id="25db4-298">Non</span><span class="sxs-lookup"><span data-stu-id="25db4-298">No</span></span>|<span data-ttu-id="25db4-299">300</span><span class="sxs-lookup"><span data-stu-id="25db4-299">300</span></span>|<span data-ttu-id="25db4-300">100 1 5061 sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="25db4-300">100 1 5061 sipfed.online.lync.com.</span></span> <span data-ttu-id="25db4-301">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="25db4-301">**This value MUST end with a period (.)**</span></span><br> <span data-ttu-id="25db4-302">**Remarque :** nous vous recommandons de copier et coller cette entrée, afin que l’espacement reste correcte.</span><span class="sxs-lookup"><span data-stu-id="25db4-302">**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.</span></span>           |<span data-ttu-id="25db4-303">Simple</span><span class="sxs-lookup"><span data-stu-id="25db4-303">Simple</span></span>|
   
    ![AWS-BP-Configure-5-1](../../media/c3f841d3-6076-428f-bb04-e71cc5f392fa.png)
  
6. <span data-ttu-id="25db4-305">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="25db4-305">Select **Create**.</span></span>
    
    ![AWS-BP-Configurer-5-2](../../media/1bf5dc58-a46b-47a5-bd69-7c2147dd4e50.png)
  
7. <span data-ttu-id="25db4-307">Pour ajouter l'autre enregistrement SRV :</span><span class="sxs-lookup"><span data-stu-id="25db4-307">To add the other SRV record:</span></span>
    
    <span data-ttu-id="25db4-308">Dans la page **Zones** hébergées, sélectionnez Créer un jeu d’enregistrement, créez  un enregistrement à l’aide des valeurs de la ligne suivante du tableau, puis sélectionnez de nouveau Créer pour terminer cet enregistrement. </span><span class="sxs-lookup"><span data-stu-id="25db4-308">In the **Hosted Zones** page, select **Create Record Set**, create a record using the values from the next row in the table, and then again select **Create** to complete that record.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="25db4-309">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="25db4-309">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="25db4-310">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="25db4-310">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="25db4-311">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="25db4-311">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
