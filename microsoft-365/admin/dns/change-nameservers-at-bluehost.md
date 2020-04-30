---
title: Modifier les serveurs de noms pour configurer Microsoft avec Bluehost
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
ms.assetid: 7712b6af-329c-43a0-af7b-c4e4c1befb0e
description: 'Découvrez comment configurer Microsoft pour gérer vos enregistrements DNS sur Bluehost. '
ms.openlocfilehash: f20c09d2c9ca107648cba843cc93d839df8c53fc
ms.sourcegitcommit: c7f11d851073ef14a69669f6c8b7e0c11e4bb7a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43939390"
---
# <a name="change-nameservers-to-set-up-microsoft-with-bluehost"></a><span data-ttu-id="fec5d-103">Modifier les serveurs de noms pour configurer Microsoft avec Bluehost</span><span class="sxs-lookup"><span data-stu-id="fec5d-103">Change nameservers to set up Microsoft with Bluehost</span></span>

 <span data-ttu-id="fec5d-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="fec5d-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="fec5d-105">Suivez ces instructions si vous voulez que Microsoft gère vos enregistrements DNS pour vous.</span><span class="sxs-lookup"><span data-stu-id="fec5d-105">Follow these instructions if you want Microsoft to manage your DNS records for you.</span></span> <span data-ttu-id="fec5d-106">(Si vous préférez, vous pouvez [gérer tous vos enregistrements DNS sur Bluehost](create-dns-records-at-bluehost.md).)</span><span class="sxs-lookup"><span data-stu-id="fec5d-106">(If you prefer, you can [manage all your DNS records at Bluehost](create-dns-records-at-bluehost.md).)</span></span>
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="fec5d-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="fec5d-107">Add a TXT record for verification</span></span>

<span data-ttu-id="fec5d-p102">Avant que vous puissiez utiliser votre domaine avec Microsoft, nous devons vérifier qu’il vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que le domaine vous appartient.</span><span class="sxs-lookup"><span data-stu-id="fec5d-p102">Before you use your domain with Microsoft, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fec5d-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="fec5d-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="fec5d-112">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="fec5d-112">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="fec5d-113">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="fec5d-113">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="fec5d-114">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="fec5d-114">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="fec5d-115">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="fec5d-115">(You may have to scroll down.)</span></span> 
    
3. <span data-ttu-id="fec5d-116">Dans la zone **domain_name** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-116">In the **domain_name** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="fec5d-117">On the **DNS Zone Editor** page, in the Add DNS Record area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="fec5d-117">On the **DNS Zone Editor** page, in the Add DNS Record area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="fec5d-118">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="fec5d-118">(Choose the **Type** value from the drop-down list.)</span></span> 
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fec5d-119">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="fec5d-119">**Host Record**</span></span> <br/> |<span data-ttu-id="fec5d-120">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="fec5d-120">**TTL**</span></span> <br/> |<span data-ttu-id="fec5d-121">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="fec5d-121">**Type**</span></span> <br/> |<span data-ttu-id="fec5d-122">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="fec5d-122">**TXT Value**</span></span> <br/> |
|@  <br/> |<span data-ttu-id="fec5d-123">14400</span><span class="sxs-lookup"><span data-stu-id="fec5d-123">14400</span></span>  <br/> |<span data-ttu-id="fec5d-124">TXT</span><span class="sxs-lookup"><span data-stu-id="fec5d-124">TXT</span></span>  <br/> |<span data-ttu-id="fec5d-125">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="fec5d-125">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="fec5d-126">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="fec5d-126">**Note:** This is an example.</span></span> <span data-ttu-id="fec5d-127">Utilisez votre valeur spécifique d’**Adresse de destination ou de pointage** ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="fec5d-127">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="fec5d-128">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="fec5d-128">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) <br/> |

   
5. <span data-ttu-id="fec5d-129">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-129">Select **add record**.</span></span>
    
6. <span data-ttu-id="fec5d-130">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="fec5d-130">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="fec5d-131">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez retourner à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="fec5d-131">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="fec5d-132">Lorsque Microsoft trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="fec5d-132">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="fec5d-133">Dans le centre d’administration Microsoft, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="fec5d-133">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="fec5d-134">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="fec5d-134">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="fec5d-135">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-135">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="fec5d-136">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-136">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="fec5d-137">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="fec5d-137">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="fec5d-138">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="fec5d-138">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="fec5d-139">Si vous rencontrez des difficultés avec le flux de courrier ou d’autres problèmes suite à l’ajout des enregistrements DNS, consultez la page [Rechercher et corriger les problèmes suite à l’ajout de votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="fec5d-139">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="fec5d-140">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="fec5d-140">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="fec5d-141">Pour terminer la configuration de votre domaine avec Microsoft, vous devez modifier les enregistrements de serveur de noms de votre domaine au niveau de votre bureau d’enregistrement de domaines afin de pointer vers les serveurs de noms principaux et secondaires.</span><span class="sxs-lookup"><span data-stu-id="fec5d-141">To complete setting up your domain with Microsoft, you change your domain's NS records at your domain registrar to point to the  primary and secondary name servers.</span></span> <span data-ttu-id="fec5d-142">Cela permet à Microsoft de mettre à jour les enregistrements DNS du domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="fec5d-142">This sets up Microsoft to update the domain's DNS records for you.</span></span> <span data-ttu-id="fec5d-143">Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="fec5d-143">We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="fec5d-144">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="fec5d-144">When you change your domain's NS records to point to the Microsoft name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="fec5d-145">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain* . com) débuteront à Microsoft après avoir effectué cette modification.</span><span class="sxs-lookup"><span data-stu-id="fec5d-145">For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Microsoft after you make this change.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="fec5d-146">La procédure suivante montre comment supprimer tous les autres serveurs de noms indésirables de la liste, et également comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="fec5d-146">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="fec5d-147">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants : > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-147">>  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com</span></span> 
  
1. <span data-ttu-id="fec5d-148">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="fec5d-148">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="fec5d-149">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="fec5d-149">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="fec5d-150">Dans la page **domaines** , dans la zone **domain_name** , activez la case à cocher pour votre domaine, puis sélectionnez **serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-150">On the **domains** page, in the **domain_name** area, select the checkbox for your domain, and then select **name servers**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-1](../../media/8f384386-197c-4272-9675-82037922dac4.png)
  
3. <span data-ttu-id="fec5d-152">Dans la zone **domain_name** , sélectionnez utiliser des serveurs de **noms personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-152">In the **domain_name** area, select **Use Custom Nameservers**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-2](../../media/9fb47d21-c4ce-4eee-af90-c9569870a329.png)
  
4. <span data-ttu-id="fec5d-154">Suivez l'une des procédures suivantes en fonction du scénario qui s'applique à votre cas dans la page qui s'affiche :</span><span class="sxs-lookup"><span data-stu-id="fec5d-154">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:</span></span>
    
  - <span data-ttu-id="fec5d-155">Si **AUCUN** serveur de noms n'est encore répertorié, [Si AUCUN serveur de noms n'est encore répertorié](#if-there-are-no-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="fec5d-155">If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).</span></span>
    
  - <span data-ttu-id="fec5d-156">Si **DES** serveurs de noms sont déjà répertoriés, [Si DES serveurs de noms sont déjà répertoriés](#if-there-are-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="fec5d-156">If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="fec5d-157">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="fec5d-157">If there are NO nameservers already listed</span></span>

1. <span data-ttu-id="fec5d-158">Dans la section **Use Custom Nameservers (Utiliser des serveurs de noms personnalisés)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fec5d-158">In the **Use Custom Nameservers** section, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fec5d-159">**Première ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-159">**First empty row**</span></span> <br/> |<span data-ttu-id="fec5d-160">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-160">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="fec5d-161">**Deuxième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-161">**Second empty row**</span></span> <br/> |<span data-ttu-id="fec5d-162">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-162">ns2.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3-1](../../media/07b13d6d-a34e-45b5-afd5-48ebd4c1344f.png)
  
2. <span data-ttu-id="fec5d-164">Sélectionnez **Ajouter une ligne**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-164">Select **Add Row**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-3-2](../../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
3. <span data-ttu-id="fec5d-166">Toujours dans la section **Use Custom Nameservers** (Utiliser des serveurs de noms personnalisés), tapez ou copiez-collez les valeurs du tableau suivant dans la première ligne vide.</span><span class="sxs-lookup"><span data-stu-id="fec5d-166">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the first row of the following table into the new empty row.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fec5d-167">**Troisième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-167">**Third empty row**</span></span> <br/> |<span data-ttu-id="fec5d-168">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-168">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="fec5d-169">**Quatrième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-169">**Fourth empty row**</span></span> <br/> |<span data-ttu-id="fec5d-170">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-170">ns4.bdm.microsoftonline.com</span></span>  <br/> |
  
4. <span data-ttu-id="fec5d-171">Pour ajouter le quatrième enregistrement de serveur de noms, sélectionnez de nouveau **Ajouter une ligne** , puis créez un enregistrement à l’aide des valeurs de la dernière ligne du tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="fec5d-171">To add the fourth Nameserver record, select **Add Row** again, and create a record using the values from the last row of the above table.</span></span> 
    
5. <span data-ttu-id="fec5d-172">Sélectionnez **enregistrer les paramètres**serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="fec5d-172">Select **save nameserver settings**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-4](../../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> <span data-ttu-id="fec5d-174">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="fec5d-174">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="fec5d-175">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="fec5d-175">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="fec5d-176">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="fec5d-176">If there ARE nameservers already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="fec5d-177">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="fec5d-177">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="fec5d-178">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="fec5d-178">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="fec5d-179">Si d'autres serveurs de noms sont répertoriés, supprimez-les individuellement en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="fec5d-179">If there are any other name servers listed, delete each of them by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Bluehost-BP-Redelegate-1-5](../../media/d1051c43-f8ff-46d7-af26-3975d3f0f621.png)
  
2. <span data-ttu-id="fec5d-181">Toujours dans la section **Use Custom Nameservers (Utiliser des serveurs de noms personnalisés)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fec5d-181">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fec5d-182">**Première ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-182">**First empty row**</span></span> <br/> |<span data-ttu-id="fec5d-183">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-183">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="fec5d-184">**Deuxième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-184">**Second empty row**</span></span> <br/> |<span data-ttu-id="fec5d-185">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-185">ns2.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3](../../media/1523debf-5eb0-4765-8e05-bcd56e375c20.png)
  
3. <span data-ttu-id="fec5d-187">Sélectionnez **Ajouter une ligne**.</span><span class="sxs-lookup"><span data-stu-id="fec5d-187">Select **Add Row**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-3-2](../../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
4. <span data-ttu-id="fec5d-189">Toujours dans la section **Use Custom Nameservers** (Utiliser des serveurs de noms personnalisés), tapez ou copiez-collez les valeurs du tableau suivant dans la première ligne vide.</span><span class="sxs-lookup"><span data-stu-id="fec5d-189">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the first row of the following table into the new empty row.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fec5d-190">**Troisième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-190">**Third empty row**</span></span> <br/> |<span data-ttu-id="fec5d-191">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-191">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="fec5d-192">**Quatrième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="fec5d-192">**Fourth empty row**</span></span> <br/> |<span data-ttu-id="fec5d-193">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="fec5d-193">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3-3](../../media/480b32bb-af27-40a5-90c5-5617ed02bb41.png)
  
5. <span data-ttu-id="fec5d-195">Pour ajouter le quatrième enregistrement de serveur de noms, sélectionnez de nouveau **Ajouter une ligne** , puis créez un enregistrement à l’aide des valeurs de la dernière ligne du tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="fec5d-195">To add the fourth Nameserver record, select **Add Row** again, and create a record using the values from the last row of the above table.</span></span> 
    
6. <span data-ttu-id="fec5d-196">Sélectionnez **enregistrer les paramètres**serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="fec5d-196">Select **save nameserver settings**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-4](../../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> <span data-ttu-id="fec5d-198">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="fec5d-198">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="fec5d-199">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="fec5d-199">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
  
