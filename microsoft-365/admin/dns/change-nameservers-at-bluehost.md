---
title: Modifier les serveurs de noms pour configurer Office 365 auprès de Bluehost
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
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
description: 'Découvrez comment configurer Office 365 pour gérer vos enregistrements DNS sur Bluehost. '
ms.openlocfilehash: 081abe977b498ea0cc0a0e2da9b54b00687df530
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42352375"
---
# <a name="change-nameservers-to-set-up-office-365-with-bluehost"></a><span data-ttu-id="e3aa2-103">Modifier les serveurs de noms pour configurer Office 365 auprès de Bluehost</span><span class="sxs-lookup"><span data-stu-id="e3aa2-103">Change nameservers to set up Office 365 with Bluehost</span></span>

 <span data-ttu-id="e3aa2-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="e3aa2-p101">Si vous voulez qu'Office 365 gère vos enregistrements DNS Office 365 à votre place, suivez ces instructions (vous pouvez également [gérer tous vos enregistrements DNS Office 365 via Bluehost](create-dns-records-at-bluehost.md)).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p101">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at Bluehost](create-dns-records-at-bluehost.md).)</span></span>
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="e3aa2-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="e3aa2-107">Add a TXT record for verification</span></span>

<span data-ttu-id="e3aa2-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e3aa2-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="e3aa2-112">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-112">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="e3aa2-113">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-113">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="e3aa2-114">Dans la page **domains (domaines)**, dans la zone **domain (domaine)**, recherchez la ligne associée au domaine que vous modifiez, puis cochez la case correspondant à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-114">On the **domains** page, in the **domain** area, find the row for the domain that you're changing, and then select the check box for that domain.</span></span> 
    
    <span data-ttu-id="e3aa2-115">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="e3aa2-115">(You may have to scroll down.)</span></span> 
    
3. <span data-ttu-id="e3aa2-116">Dans la zone **domain_name** , sur la ligne **éditeur de zone DNS** , sélectionnez **gérer les enregistrements DNS**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-116">In the **domain_name** area, on the **DNS Zone Editor** row, select **Manage DNS records**.</span></span>
    
4. <span data-ttu-id="e3aa2-117">On the **DNS Zone Editor** page, in the Add DNS Record area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-117">On the **DNS Zone Editor** page, in the Add DNS Record area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="e3aa2-118">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="e3aa2-118">(Choose the **Type** value from the drop-down list.)</span></span> 
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e3aa2-119">**Host Record**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-119">**Host Record**</span></span> <br/> |<span data-ttu-id="e3aa2-120">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-120">**TTL**</span></span> <br/> |<span data-ttu-id="e3aa2-121">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-121">**Type**</span></span> <br/> |<span data-ttu-id="e3aa2-122">**TXT Value**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-122">**TXT Value**</span></span> <br/> |
|@  <br/> |<span data-ttu-id="e3aa2-123">14400</span><span class="sxs-lookup"><span data-stu-id="e3aa2-123">14400</span></span>  <br/> |<span data-ttu-id="e3aa2-124">TXT</span><span class="sxs-lookup"><span data-stu-id="e3aa2-124">TXT</span></span>  <br/> |<span data-ttu-id="e3aa2-125">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="e3aa2-125">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="e3aa2-126">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-126">**Note:** This is an example.</span></span> <span data-ttu-id="e3aa2-127">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-127">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="e3aa2-128">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="e3aa2-128">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) <br/> |

   
5. <span data-ttu-id="e3aa2-129">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-129">Select **add record**.</span></span>
    
6. <span data-ttu-id="e3aa2-130">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-130">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="e3aa2-131">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-131">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="e3aa2-132">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-132">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="e3aa2-133">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-133">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="e3aa2-134">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-134">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="e3aa2-135">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-135">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="e3aa2-136">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-136">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e3aa2-137">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-137">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="e3aa2-138">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-138">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="e3aa2-139">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-139">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="e3aa2-140">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="e3aa2-140">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="e3aa2-p107">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p107">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="e3aa2-p108">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés. Par exemple, les messages envoyés à votre domaine (tel que thomas@ *votre_domaine*  .com) arriveront dans Office 365 une fois cette modification appliquée.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p108">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="e3aa2-146">La procédure suivante montre comment supprimer tous les autres serveurs de noms indésirables de la liste, et également comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-146">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="e3aa2-147">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants : > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-147">>  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com</span></span> 
  
1. <span data-ttu-id="e3aa2-148">Pour commencer, accédez à la page de vos domaines sur le site Bluehost en utilisant [ce lien](https://my.bluehost.com/cgi/dm).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-148">To get started, go to your domains page at Bluehost by using [this link](https://my.bluehost.com/cgi/dm).</span></span> <span data-ttu-id="e3aa2-149">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-149">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="e3aa2-150">Dans la page **domaines** , dans la zone **domain_name** , activez la case à cocher pour votre domaine, puis sélectionnez **serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-150">On the **domains** page, in the **domain_name** area, select the checkbox for your domain, and then select **name servers**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-1](../../media/8f384386-197c-4272-9675-82037922dac4.png)
  
3. <span data-ttu-id="e3aa2-152">Dans la zone **domain_name** , sélectionnez utiliser des serveurs de **noms personnalisés**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-152">In the **domain_name** area, select **Use Custom Nameservers**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-2](../../media/9fb47d21-c4ce-4eee-af90-c9569870a329.png)
  
4. <span data-ttu-id="e3aa2-154">Suivez l'une des procédures suivantes en fonction du scénario qui s'applique à votre cas dans la page qui s'affiche :</span><span class="sxs-lookup"><span data-stu-id="e3aa2-154">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:</span></span>
    
  - <span data-ttu-id="e3aa2-155">Si **AUCUN** serveur de noms n'est encore répertorié, [Si AUCUN serveur de noms n'est encore répertorié](#if-there-are-no-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-155">If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).</span></span>
    
  - <span data-ttu-id="e3aa2-156">Si **DES** serveurs de noms sont déjà répertoriés, [Si DES serveurs de noms sont déjà répertoriés](#if-there-are-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="e3aa2-156">If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="e3aa2-157">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="e3aa2-157">If there are NO nameservers already listed</span></span>

1. <span data-ttu-id="e3aa2-158">Dans la section **Use Custom Nameservers (Utiliser des serveurs de noms personnalisés)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-158">In the **Use Custom Nameservers** section, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e3aa2-159">**Première ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-159">**First empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-160">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-160">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="e3aa2-161">**Deuxième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-161">**Second empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-162">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-162">ns2.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3-1](../../media/07b13d6d-a34e-45b5-afd5-48ebd4c1344f.png)
  
2. <span data-ttu-id="e3aa2-164">Sélectionnez **Ajouter une ligne**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-164">Select **Add Row**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-3-2](../../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
3. <span data-ttu-id="e3aa2-166">Toujours dans la section **Use Custom Nameservers** (Utiliser des serveurs de noms personnalisés), tapez ou copiez-collez les valeurs du tableau suivant dans la première ligne vide.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-166">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the first row of the following table into the new empty row.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e3aa2-167">**Troisième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-167">**Third empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-168">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-168">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="e3aa2-169">**Quatrième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-169">**Fourth empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-170">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-170">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
    ![Bluehost-BP-Redelegate-1-3-3](../../media/480b32bb-af27-40a5-90c5-5617ed02bb41.png)
  
4. <span data-ttu-id="e3aa2-171">Pour ajouter le quatrième enregistrement de serveur de noms, sélectionnez de nouveau **Ajouter une ligne** , puis créez un enregistrement à l’aide des valeurs de la dernière ligne du tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-171">To add the fourth Nameserver record, select **Add Row** again, and create a record using the values from the last row of the above table.</span></span> 
    
5. <span data-ttu-id="e3aa2-172">Sélectionnez **enregistrer les paramètres**serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-172">Select **save nameserver settings**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-4](../../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> <span data-ttu-id="e3aa2-p111">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p111">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="e3aa2-176">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="e3aa2-176">If there ARE nameservers already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="e3aa2-177">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-177">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="e3aa2-178">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="e3aa2-178">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="e3aa2-179">Si d'autres serveurs de noms sont répertoriés, supprimez-les individuellement en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-179">If there are any other name servers listed, delete each of them by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Bluehost-BP-Redelegate-1-5](../../media/d1051c43-f8ff-46d7-af26-3975d3f0f621.png)
  
2. <span data-ttu-id="e3aa2-181">Toujours dans la section **Use Custom Nameservers (Utiliser des serveurs de noms personnalisés)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-181">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e3aa2-182">**Première ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-182">**First empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-183">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-183">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="e3aa2-184">**Deuxième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-184">**Second empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-185">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-185">ns2.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3](../../media/1523debf-5eb0-4765-8e05-bcd56e375c20.png)
  
3. <span data-ttu-id="e3aa2-187">Sélectionnez **Ajouter une ligne**.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-187">Select **Add Row**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-3-2](../../media/db34b632-1d10-44b7-aa1f-44bd27bf09e3.png)
  
4. <span data-ttu-id="e3aa2-189">Toujours dans la section **Use Custom Nameservers** (Utiliser des serveurs de noms personnalisés), tapez ou copiez-collez les valeurs du tableau suivant dans la première ligne vide.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-189">Still in the **Use Custom Nameservers** section, type or copy and paste the values from the first row of the following table into the new empty row.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="e3aa2-190">**Troisième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-190">**Third empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-191">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-191">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="e3aa2-192">**Quatrième ligne vide**</span><span class="sxs-lookup"><span data-stu-id="e3aa2-192">**Fourth empty row**</span></span> <br/> |<span data-ttu-id="e3aa2-193">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="e3aa2-193">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Bluehost-BP-redelegate-1-3-3](../../media/480b32bb-af27-40a5-90c5-5617ed02bb41.png)
  
5. <span data-ttu-id="e3aa2-195">Pour ajouter le quatrième enregistrement de serveur de noms, sélectionnez de nouveau **Ajouter une ligne** , puis créez un enregistrement à l’aide des valeurs de la dernière ligne du tableau ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-195">To add the fourth Nameserver record, select **Add Row** again, and create a record using the values from the last row of the above table.</span></span> 
    
6. <span data-ttu-id="e3aa2-196">Sélectionnez **enregistrer les paramètres**serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-196">Select **save nameserver settings**.</span></span>
    
    ![Bluehost-BP-Redelegate-1-4](../../media/b24a4cfd-924b-4b6d-ad3d-2dea148fc77f.png)
  
> [!NOTE]
> <span data-ttu-id="e3aa2-p113">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="e3aa2-p113">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
