---
title: Modifier les serveurs de noms pour configurer Microsoft auprès d’Amazon Web Services (AWS)
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
ms.assetid: 0ddbe33c-81ea-4c02-8db9-e71d3810c0ec
description: 'Découvrez comment configurer Microsoft pour gérer vos enregistrements DNS sur Amazon Web Services (AWS). '
ms.openlocfilehash: 4700557c40973ab051cced81c129197a826964ab
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49658451"
---
# <a name="change-nameservers-to-set-up-microsoft-with-amazon-web-services-aws"></a><span data-ttu-id="f42ff-103">Modifier les serveurs de noms pour configurer Microsoft auprès d’Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="f42ff-103">Change nameservers to set up Microsoft with Amazon Web Services (AWS)</span></span>

 <span data-ttu-id="f42ff-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.yml)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="f42ff-104">**[Check the Domains FAQ](../setup/domains-faq.yml)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="f42ff-105">Si vous souhaitez que Microsoft gère vos enregistrements DNS à votre place, suivez ces instructions.</span><span class="sxs-lookup"><span data-stu-id="f42ff-105">Follow these instructions if you want Microsoft to manage your DNS records for you.</span></span> <span data-ttu-id="f42ff-106">(Si vous préférez, vous pouvez gérer tous vos [enregistrements DNS Microsoft sur AWS.)](create-dns-records-at-aws.md)</span><span class="sxs-lookup"><span data-stu-id="f42ff-106">(If you prefer, you can [manage all your Microsoft DNS records at AWS](create-dns-records-at-aws.md).)</span></span>
  
    
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="f42ff-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="f42ff-107">Add a TXT record for verification</span></span>

<span data-ttu-id="f42ff-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="f42ff-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f42ff-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f42ff-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="f42ff-p104">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f42ff-p104">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f42ff-114">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="f42ff-114">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="f42ff-115">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f42ff-115">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="f42ff-116">Sélectionnez **Créer un jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="f42ff-116">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="f42ff-117">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="f42ff-117">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="f42ff-118">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span><span class="sxs-lookup"><span data-stu-id="f42ff-118">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="f42ff-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span><span class="sxs-lookup"><span data-stu-id="f42ff-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span></span> 
  
|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f42ff-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="f42ff-121">**Name**</span></span> <br/> |<span data-ttu-id="f42ff-122">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-122">**Type**</span></span> <br/> |<span data-ttu-id="f42ff-123">**Alias**</span><span class="sxs-lookup"><span data-stu-id="f42ff-123">**Alias**</span></span> <br/> |<span data-ttu-id="f42ff-124">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="f42ff-124">**TTL (Seconds)**</span></span> <br/> |<span data-ttu-id="f42ff-125">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-125">**Value**</span></span> <br/> |<span data-ttu-id="f42ff-126">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-126">**Routing Policy**</span></span> <br/> |
|<span data-ttu-id="f42ff-127">(Laissez ce champ vide)</span><span class="sxs-lookup"><span data-stu-id="f42ff-127">(Leave this field empty)</span></span>  <br/> |<span data-ttu-id="f42ff-128">TXT - Text</span><span class="sxs-lookup"><span data-stu-id="f42ff-128">TXT - Text</span></span>  <br/> |<span data-ttu-id="f42ff-129">Non</span><span class="sxs-lookup"><span data-stu-id="f42ff-129">No</span></span>  <br/> |<span data-ttu-id="f42ff-130">300</span><span class="sxs-lookup"><span data-stu-id="f42ff-130">300</span></span>  <br/> |<span data-ttu-id="f42ff-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="f42ff-131">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="f42ff-132">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="f42ff-132">**Note:** This is an example.</span></span> <span data-ttu-id="f42ff-133">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="f42ff-133">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="f42ff-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="f42ff-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  <br/>  |<span data-ttu-id="f42ff-135">Simple</span><span class="sxs-lookup"><span data-stu-id="f42ff-135">Simple</span></span> <br/> |
   
6. <span data-ttu-id="f42ff-136">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="f42ff-136">Select **Create**.</span></span>
    
7. <span data-ttu-id="f42ff-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f42ff-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="f42ff-138">Maintenant que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, revenir à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="f42ff-138">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="f42ff-139">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="f42ff-139">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="f42ff-140">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="f42ff-140">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="f42ff-141">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="f42ff-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="f42ff-142">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="f42ff-142">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="f42ff-143">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="f42ff-143">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f42ff-144">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="f42ff-144">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="f42ff-145">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="f42ff-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="f42ff-146">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="f42ff-146">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="f42ff-147">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="f42ff-147">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="f42ff-148">Pour terminer la configuration de votre domaine avec Microsoft, vous modifiez les enregistrements NS de votre domaine auprès de votre bureau d’enregistrement de domaines pour qu’ils pointent vers les serveurs de noms principaux et secondaires de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f42ff-148">To complete setting up your domain with Microsoft, you change your domain's NS records at your domain registrar to point to the Microsoft primary and secondary name servers.</span></span> <span data-ttu-id="f42ff-149">Cela permet à Microsoft de mettre à jour les enregistrements DNS du domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="f42ff-149">This sets up Microsoft to update the domain's DNS records for you.</span></span> <span data-ttu-id="f42ff-150">Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f42ff-150">We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="f42ff-151">Lorsque vous modifiez les enregistrements NS de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="f42ff-151">When you change your domain's NS records to point to the Microsoft name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="f42ff-152">Par exemple, tous les e-mails envoyés à votre domaine (comme rob@ *your_domain*  .com) commenceront à arriver à Microsoft après avoir fait cette modification.</span><span class="sxs-lookup"><span data-stu-id="f42ff-152">For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Microsoft after you make this change.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="f42ff-153">La procédure suivante vous montre comment supprimer d’autres serveurs de noms indésirables de la liste et comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="f42ff-153">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="f42ff-154">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre : > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="f42ff-154">>  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com</span></span> 
  
1. <span data-ttu-id="f42ff-155">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home).</span><span class="sxs-lookup"><span data-stu-id="f42ff-155">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home).</span></span> <span data-ttu-id="f42ff-156">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="f42ff-156">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="f42ff-157">Dans la page **Ressources,** sélectionnez **Zones hébergées.**</span><span class="sxs-lookup"><span data-stu-id="f42ff-157">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="f42ff-158">Dans la page **Zones hébergées,** dans la colonne **Nom** de domaine, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="f42ff-158">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="f42ff-159">Sélectionnez le jeu d'enregistrement **Serveur de noms**.</span><span class="sxs-lookup"><span data-stu-id="f42ff-159">Select the **Nameserver** record set.</span></span> 
    
    ![Select the recordset](../../media/24e618e4-0a16-43a2-9886-f4f5dac79374.png)
  
5. <span data-ttu-id="f42ff-161">Dans le jeu d'enregistrements **NS - Serveur de noms**, dans la zone **Valeur**, supprimez tous les serveurs de noms en les sélectionnant, puis en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="f42ff-161">In the **NS - Name server** record set in the **Value** box, delete all of the nameservers by selecting them all and then pressing the **Delete** key on your keyboard.</span></span> 
    
    > [!CAUTION]
    > <span data-ttu-id="f42ff-162">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="f42ff-162">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="f42ff-163">(Autrement dit, supprimez uniquement les  serveurs de noms actuels qui ne sont pas nommés **ns1.bdm.microsoftonline.com,** **ns2.bdm.microsoftonline.com,** **ns3.bdm.microsoftonline.com** ou **ns4.bdm.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="f42ff-163">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
    ![Select and delete all of the nameservers in the Value box](../../media/ecf1e897-fa7d-4abc-b00b-bf55b8ed2139.png)
  
6. <span data-ttu-id="f42ff-165">Dans la **zone TTL (Secondes)** : **sélectionnez 1h** (1 heure).</span><span class="sxs-lookup"><span data-stu-id="f42ff-165">In the **TTL (Seconds):** area, select **1h** (1 Hour).</span></span> 
    
    ![Sélectionner 1H pour une heure](../../media/c70070e1-4bde-41a7-b271-9d22c475edf6.png)
  
7. <span data-ttu-id="f42ff-167">Toujours dans le jeu d'enregistrements **NS - Serveur de noms**, dans la zone **Valeur**, tapez ou copiez-collez la valeur de la **première ligne** du tableau suivant, appuyez sur la touche **Entrée** du clavier, puis tapez ou copiez-collez la valeur de la **ligne** suivante.</span><span class="sxs-lookup"><span data-stu-id="f42ff-167">Still in the **NS - Name server** record set, in the **Value** box, type or copy and paste the **First line** value from the following table, then press the **Enter** key on your keyboard and type or copy and paste the next **line** value.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="f42ff-168">Chaque valeur de serveur de noms  *doit*  figurer sur sa propre ligne distincte dans la zone **Valeur**, comme dans l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="f42ff-168">Each nameserver value  *must*  be on its own separate line within the **Value** box, as shown in the following illustration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f42ff-169">**Première ligne**</span><span class="sxs-lookup"><span data-stu-id="f42ff-169">**First line**</span></span> <br/> |<span data-ttu-id="f42ff-170">ns1.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="f42ff-170">ns1.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="f42ff-171">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-171">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="f42ff-172">**Deuxième ligne**</span><span class="sxs-lookup"><span data-stu-id="f42ff-172">**Second line**</span></span> <br/> |<span data-ttu-id="f42ff-173">ns2.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="f42ff-173">ns2.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="f42ff-174">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-174">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="f42ff-175">**Troisième ligne**</span><span class="sxs-lookup"><span data-stu-id="f42ff-175">**Third line**</span></span> <br/> |<span data-ttu-id="f42ff-176">ns3.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="f42ff-176">ns3.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="f42ff-177">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-177">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="f42ff-178">**Quatrième ligne**</span><span class="sxs-lookup"><span data-stu-id="f42ff-178">**Fourth line**</span></span> <br/> |<span data-ttu-id="f42ff-179">ns4.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="f42ff-179">ns4.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="f42ff-180">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="f42ff-180">**This value MUST end with a period (.)**</span></span> <br/> |
   
   ![Tapez ou collez la valeur de première ligne dans la zone Valeur](../../media/b63f41e0-51ef-4ab2-a4b8-ee7380e5ab35.png)
  
8. <span data-ttu-id="f42ff-182">Sélectionnez **Enregistrer le jeu d’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="f42ff-182">Select **Save Record Set**.</span></span>
    
    ![Sélectionnez Enregistrer le jeu d’enregistrement](../../media/ab3c0558-bb7c-41e4-871e-ea82f1553476.png)
  
> [!NOTE]
> <span data-ttu-id="f42ff-184">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="f42ff-184">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="f42ff-185">Ensuite, votre messagerie Microsoft et d’autres services seront tous définies pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="f42ff-185">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
