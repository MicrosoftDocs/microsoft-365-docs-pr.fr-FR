---
title: Modifier les serveurs de noms de manière à configurer Office 365 avec MyDomain
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
ms.assetid: c5f6140a-4a12-401b-9bbd-7dfb0d6b0ba3
description: Découvrez comment configurer Office 365 pour gérer les enregistrements DNS de votre domaine personnalisé sur Mon_domaine.
ms.openlocfilehash: f88f0528caf2229441fd3e5364b53864b923099f
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43212044"
---
# <a name="change-nameservers-to-set-up-office-365-with-mydomain"></a><span data-ttu-id="3ed29-103">Modifier les serveurs de noms de manière à configurer Office 365 avec MyDomain</span><span class="sxs-lookup"><span data-stu-id="3ed29-103">Change nameservers to set up Office 365 with MyDomain</span></span>

 <span data-ttu-id="3ed29-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="3ed29-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="3ed29-p101">Si vous voulez laisser Office 365 gérer vos enregistrements DNS Office 365 à votre place, suivez ces instructions (si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Office 365 via MyDomain](create-dns-records-at-mydomain.md)).</span><span class="sxs-lookup"><span data-stu-id="3ed29-p101">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at MyDomain](create-dns-records-at-mydomain.md).)</span></span>
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="3ed29-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="3ed29-107">Add a TXT record for verification</span></span>

<span data-ttu-id="3ed29-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3ed29-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="3ed29-p104">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p104">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="3ed29-114">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-114">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="3ed29-115">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="3ed29-115">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="3ed29-116">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-116">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="3ed29-117">Dans la liste déroulante **Modifier**, sélectionnez **Enregistrement TXT/SPF**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-117">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
6. <span data-ttu-id="3ed29-118">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3ed29-118">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
||
|:-----|
|<span data-ttu-id="3ed29-119">**Content**</span><span class="sxs-lookup"><span data-stu-id="3ed29-119">**Content**</span></span> <br/> |
|<span data-ttu-id="3ed29-120">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="3ed29-120">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="3ed29-121">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="3ed29-121">**Note**: This is an example.</span></span> <span data-ttu-id="3ed29-122">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="3ed29-122">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="3ed29-123">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="3ed29-123">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="3ed29-124">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-124">Select **Add**.</span></span>
    
8. <span data-ttu-id="3ed29-125">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="3ed29-125">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="3ed29-126">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3ed29-126">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="3ed29-127">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="3ed29-127">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="3ed29-128">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="3ed29-128">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="3ed29-129">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="3ed29-129">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="3ed29-130">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-130">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="3ed29-131">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-131">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3ed29-132">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="3ed29-132">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="3ed29-133">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="3ed29-133">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="3ed29-134">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="3ed29-134">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="3ed29-135">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="3ed29-135">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="3ed29-p107">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p107">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="3ed29-139">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="3ed29-139">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="3ed29-140">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain.*</span><span class="sxs-lookup"><span data-stu-id="3ed29-140">For example, all email sent to your domain (like rob@ *your_domain.*</span></span> <span data-ttu-id="3ed29-141">com) commencera à Office 365 une fois cette modification apportée.</span><span class="sxs-lookup"><span data-stu-id="3ed29-141">com) will start coming to Office 365 after you make this change.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3ed29-142">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span><span class="sxs-lookup"><span data-stu-id="3ed29-142">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span></span> <br/> <span data-ttu-id="3ed29-143">When you have completed the steps in this section, the only nameservers that should be listed are these four:</span><span class="sxs-lookup"><span data-stu-id="3ed29-143">When you have completed the steps in this section, the only nameservers that should be listed are these four:</span></span>
  
1. <span data-ttu-id="3ed29-p110">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p110">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="3ed29-146">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-146">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="3ed29-147">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="3ed29-147">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="3ed29-148">Dans la ligne **vue d’ensemble** , sélectionnez serveurs de **noms**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-148">In the **Overview** row, select **Nameservers**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-1](../../media/49e91235-44b5-46d6-a82e-8f11329db3d6.png)
  
5. <span data-ttu-id="3ed29-150">Dans la section **Update Name Servers**, sélectionnez **Use different name servers**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-150">In the **Update Name Servers** section, select **Use different name servers**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-2-1](../../media/f869fb26-54dc-4b66-8378-a78a79b582bd.png)
  
6. <span data-ttu-id="3ed29-152">Selon qu’il y a déjà ou non des serveurs de noms répertoriés dans la page qui s’affiche maintenant, passez à l’une des deux procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ed29-152">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures.</span></span>
    
### <a name="if-the-correct-nameservers-are-already-listed"></a><span data-ttu-id="3ed29-153">Si les serveurs de noms appropriés SONT déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="3ed29-153">If the correct nameservers ARE already listed</span></span>

- <span data-ttu-id="3ed29-154">Si les serveurs de noms corrects sont répertoriés, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="3ed29-154">If the correct nameservers are already listed, you can skip this step.</span></span>
    
    ![Mondomaine-BP-redelegate-1-2-2](../../media/601f6a46-15bd-4a92-b792-ac628ff86628.png)
  
### <a name="if-the-correct-nameservers-are-not-already-listed"></a><span data-ttu-id="3ed29-156">Si les serveurs de noms corrects ne sont PAS répertoriés</span><span class="sxs-lookup"><span data-stu-id="3ed29-156">If the correct nameservers are NOT already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="3ed29-157">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="3ed29-157">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="3ed29-158">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="3ed29-158">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="3ed29-159">Supprimez les serveurs de noms existants en sélectionnant chaque entrée du champ **Nameserver : (Serveur de noms :)**, puis en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="3ed29-159">Delete the existing nameservers by selecting each entry in the **Nameserver:** field, and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Mondomaine-BP-redelegate-1-3-1](../../media/5024cd27-a2b1-42a2-99e4-5ceb5e6eddb9.png)
  
2. <span data-ttu-id="3ed29-161">Sélectionnez **plus** deux fois pour ajouter deux nouvelles lignes de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="3ed29-161">Select **Add More** twice to add two new Nameserver rows.</span></span> 
    
    ![Mondomaine-BP-redelegate-1-3-2](../../media/19307893-2f73-4e4d-9221-a5870e09ab48.png)
  
3. <span data-ttu-id="3ed29-163">Dans les zones des enregistrements, tapez ou copiez-collez les valeurs de serveur de noms du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3ed29-163">In the boxes for the records, type or copy and paste the nameserver values from the following table.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="3ed29-164">**Nameserver 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="3ed29-164">**Nameserver 1**</span></span> <br/> |<span data-ttu-id="3ed29-165">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3ed29-165">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3ed29-166">**Nameserver 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="3ed29-166">**Nameserver 2**</span></span> <br/> |<span data-ttu-id="3ed29-167">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3ed29-167">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3ed29-168">**Nameserver 3 (Serveur de noms 3)**</span><span class="sxs-lookup"><span data-stu-id="3ed29-168">**Nameserver 3**</span></span> <br/> |<span data-ttu-id="3ed29-169">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3ed29-169">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="3ed29-170">**Nameserver 4 (Serveur de noms 4)**</span><span class="sxs-lookup"><span data-stu-id="3ed29-170">**Nameserver 4**</span></span> <br/> |<span data-ttu-id="3ed29-171">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="3ed29-171">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Mondomaine-BP-redelegate-1-4](../../media/7427e99c-49c7-4a2e-a5bf-66fc46900cd1.png)
  
4. <span data-ttu-id="3ed29-173">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3ed29-173">Select **Save**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-5](../../media/48473816-b881-47f0-9344-74622efa3bf8.png)
  
> [!NOTE]
> <span data-ttu-id="3ed29-p112">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="3ed29-p112">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
