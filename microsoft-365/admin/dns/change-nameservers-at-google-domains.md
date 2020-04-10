---
title: Modifier les serveurs de noms de manière à configurer Office 365 avec Google Domains
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
ms.assetid: 68a08e94-26c2-4df2-9216-026b8ec907ca
description: Découvrez comment configurer Office 365 pour gérer les enregistrements DNS de votre domaine personnalisé sur Google Domains.
ms.openlocfilehash: 86dd1745fdc85c9837e5c20844427768d4c74a81
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43211930"
---
# <a name="change-nameservers-to-set-up-office-365-with-google-domains"></a><span data-ttu-id="22f60-103">Modifier les serveurs de noms de manière à configurer Office 365 avec Google Domains</span><span class="sxs-lookup"><span data-stu-id="22f60-103">Change nameservers to set up Office 365 with Google Domains</span></span>

 <span data-ttu-id="22f60-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="22f60-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="22f60-p101">Si vous voulez laisser Office 365 gérer vos enregistrements DNS Office 365 à votre place, suivez ces instructions (si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Office 365 via Google Domains](create-dns-records-at-google-domains.md)).</span><span class="sxs-lookup"><span data-stu-id="22f60-p101">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at Google Domains](create-dns-records-at-google-domains.md).)</span></span>
  
    
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="22f60-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="22f60-107">Add a TXT record for verification</span></span>

<span data-ttu-id="22f60-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="22f60-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="22f60-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="22f60-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="22f60-112">Pour commencer, accédez à la page de vos domaines sur Google Domains via [ce lien](https://domains.google.com/registrar).</span><span class="sxs-lookup"><span data-stu-id="22f60-112">To get started, go to your domains page at Google Domains via [this link](https://domains.google.com/registrar).</span></span> <span data-ttu-id="22f60-113">You'll be prompted to sign in.</span><span class="sxs-lookup"><span data-stu-id="22f60-113">You'll be prompted to sign in.</span></span> <span data-ttu-id="22f60-114">To do so:</span><span class="sxs-lookup"><span data-stu-id="22f60-114">To do so:</span></span>
    
1. <span data-ttu-id="22f60-115">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="22f60-115">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="22f60-116">Entrez vos informations d’identification de connexion et sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="22f60-116">Enter your login credentials and again select **Sign In**.</span></span>
    
2. <span data-ttu-id="22f60-117">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="22f60-117">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="22f60-118">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="22f60-118">In the **Custom resource records** section, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="22f60-119">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="22f60-119">(You may have to scroll down.)</span></span>
    
    <span data-ttu-id="22f60-120">(Choose the **Type** value from the drop-down list.)</span><span class="sxs-lookup"><span data-stu-id="22f60-120">(Choose the **Type** value from the drop-down list.)</span></span> 
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="22f60-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="22f60-121">**Name**</span></span> <br/> |<span data-ttu-id="22f60-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="22f60-122">**Type**</span></span> <br/> |<span data-ttu-id="22f60-123">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="22f60-123">**TTL**</span></span> <br/> |<span data-ttu-id="22f60-124">**Data (Données)**</span><span class="sxs-lookup"><span data-stu-id="22f60-124">**Data**</span></span> <br/> |
|@  <br/> |<span data-ttu-id="22f60-125">TXT</span><span class="sxs-lookup"><span data-stu-id="22f60-125">TXT</span></span>  <br/> |<span data-ttu-id="22f60-126">Premier</span><span class="sxs-lookup"><span data-stu-id="22f60-126">1H</span></span>  <br/> |<span data-ttu-id="22f60-127">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="22f60-127">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="22f60-128">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="22f60-128">**Note:** This is an example.</span></span> <span data-ttu-id="22f60-129">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="22f60-129">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="22f60-130">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="22f60-130">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)       <br/>  |
   
4. <span data-ttu-id="22f60-131">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="22f60-131">Select **Add**.</span></span>
    
5. <span data-ttu-id="22f60-132">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="22f60-132">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="22f60-133">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="22f60-133">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="22f60-134">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="22f60-134">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="22f60-135">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="22f60-135">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="22f60-136">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="22f60-136">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="22f60-137">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="22f60-137">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="22f60-138">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="22f60-138">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="22f60-139">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="22f60-139">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="22f60-140">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="22f60-140">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="22f60-141">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="22f60-141">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="22f60-142">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="22f60-142">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="22f60-p107">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="22f60-p107">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="22f60-146">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="22f60-146">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="22f60-147">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain.*</span><span class="sxs-lookup"><span data-stu-id="22f60-147">For example, all email sent to your domain (like rob@ *your_domain.*</span></span>  <span data-ttu-id="22f60-148">com) commencera à Office 365 une fois cette modification apportée.</span><span class="sxs-lookup"><span data-stu-id="22f60-148">com) will start coming to Office 365 after you make this change.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="22f60-149">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span><span class="sxs-lookup"><span data-stu-id="22f60-149">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span></span> <span data-ttu-id="22f60-150">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants :</span><span class="sxs-lookup"><span data-stu-id="22f60-150">> When you have completed the steps in this section, the only nameservers that should be listed are these four:</span></span> 
  
1. <span data-ttu-id="22f60-p110">Pour commencer, accédez à la page de vos domaines sur le site Google Domains en utilisant [ce lien](https://domains.google.com/registrar). Vous êtes invité à vous connecter. Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="22f60-p110">To get started, go to your domains page at Google Domains by using [this link](https://domains.google.com/registrar). You'll be prompted to sign in. To do so:</span></span>
    
1. <span data-ttu-id="22f60-154">Sélectionnez **se connecter**.</span><span class="sxs-lookup"><span data-stu-id="22f60-154">Select **Sign In**.</span></span>
    
2. <span data-ttu-id="22f60-155">Entrez vos informations d’identification de connexion, puis sélectionnez **de nouveau connexion**.</span><span class="sxs-lookup"><span data-stu-id="22f60-155">Enter your login credentials, and then again select **Sign In**.</span></span>
    
2. <span data-ttu-id="22f60-156">Dans la page **domaines** , dans la section **domaine** , sélectionnez **configurer DNS** pour le domaine que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="22f60-156">On the **Domains** page, in the **Domain** section, select **Configure DNS** for the domain that you want to edit.</span></span> 
    
3. <span data-ttu-id="22f60-157">Dans la page **Domains** (domaines), dans la section **Name servers** (Serveurs de noms), sélectionnez **Use custom name servers** (Utiliser les serveurs de noms personnalisés).</span><span class="sxs-lookup"><span data-stu-id="22f60-157">On the **Domains** page, in the **Name servers** section, select **Use custom name servers**.</span></span>
    
    ![Google-Domains-BP-Redelegate-1-1](../../media/e264bc05-5a56-4962-bcaf-e2d999f62278.png)
  
4. <span data-ttu-id="22f60-159">Suivez l'une des procédures suivantes en fonction du scénario qui s'applique à votre cas dans la page qui s'affiche :</span><span class="sxs-lookup"><span data-stu-id="22f60-159">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:</span></span>
    
  - <span data-ttu-id="22f60-160">Si **AUCUN** serveur de noms n'est encore répertorié, [Si AUCUN serveur de noms n'est encore répertorié](#if-there-are-no-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="22f60-160">If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).</span></span>
    
  - <span data-ttu-id="22f60-161">Si **DES** serveurs de noms sont déjà répertoriés, [Si DES serveurs de noms sont déjà répertoriés](#if-there-are-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="22f60-161">If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="22f60-162">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="22f60-162">If there are NO nameservers already listed</span></span>

1. <span data-ttu-id="22f60-163">Ajoutez le premier serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="22f60-163">Add the first nameserver.</span></span>
    
    <span data-ttu-id="22f60-164">Dans la section **Name servers (Serveurs de noms)**, dans la zone **NAME SERVER (SERVEUR DE NOMS)**, tapez ou copiez-collez la première valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22f60-164">In the **Name servers** section, in the **NAME SERVER** box, type or copy and paste the first value from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="22f60-165">**Premier serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-165">**First name server**</span></span> <br/> |<span data-ttu-id="22f60-166">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-166">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-167">**Deuxième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-167">**Second name server**</span></span> <br/> |<span data-ttu-id="22f60-168">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-168">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-169">**Troisième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-169">**Third name server**</span></span> <br/> |<span data-ttu-id="22f60-170">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-170">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-171">**Quatrième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-171">**Fourth name server**</span></span> <br/> |<span data-ttu-id="22f60-172">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-172">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Google-Domains-BP-redelegate-1-2](../../media/6d14544d-7783-4ed4-b4dd-691624af7172.png)
  
2. <span data-ttu-id="22f60-174">Sélectionnez le contrôle **+ (ajouter)** pour créer une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="22f60-174">Select the **+ (add)** control to create an empty row.</span></span> 
    
    ![Google-Domains-BP-Redelegate-1-3](../../media/ea23e5fc-07e1-4ffc-b8cf-8526867b752d.png)
  
3. <span data-ttu-id="22f60-176">Ajoutez les trois autres enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="22f60-176">Add the other three Nameserver records.</span></span>
    
    <span data-ttu-id="22f60-177">Dans la section **utiliser des serveurs de noms personnalisés** , créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez le contrôle **+ (ajouter)** pour ajouter une autre ligne.</span><span class="sxs-lookup"><span data-stu-id="22f60-177">In the **Use custom name servers** section, create a record by using the values from the next row in the table, and then select the **+ (add)** control to add another row.</span></span> 
    
    <span data-ttu-id="22f60-178">Répétez cette procédure jusqu'à avoir créé les quatre enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="22f60-178">Repeat this process until you have created all four Nameserver records.</span></span>
    
4. <span data-ttu-id="22f60-179">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="22f60-179">Select **Save**.</span></span>
    
    ![Google-Domains-BP-Redelegate-1-5](../../media/cb954aa2-12ee-4e90-9b67-184cbe898bbb.png)
  
> [!NOTE]
> <span data-ttu-id="22f60-p111">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="22f60-p111">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="22f60-183">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="22f60-183">If there ARE nameservers already listed</span></span>

1. <span data-ttu-id="22f60-184">Si d’autres serveurs de noms sont répertoriés, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="22f60-184">If there are any other nameservers listed, select **Edit**.</span></span>
    
    > [!CAUTION]
    > <span data-ttu-id="22f60-185">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="22f60-185">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="22f60-186">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="22f60-186">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
    ![Google-Domains-BP-Redelegate-1-6-1](../../media/fb45d120-55ab-42c2-bdb6-19b130c3c7db.png)
  
2. <span data-ttu-id="22f60-188">Supprimez chacun d'eux en le sélectionnant, puis en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="22f60-188">Delete each one by selecting it, and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Google-Domains-BP-Redelegate-1-6-2](../../media/524e64ad-56e6-4254-8a64-e4a4c3230f89.png)
  
3. <span data-ttu-id="22f60-190">Toujours dans la section **Name servers** (Serveurs de noms), dans les lignes **NAME SERVER** (SERVEUR DE NOMS), tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22f60-190">Still in the **Name servers** section, in the **NAME SERVER** rows, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="22f60-191">**Premier serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-191">**First name server**</span></span> <br/> |<span data-ttu-id="22f60-192">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-192">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-193">**Deuxième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-193">**Second name server**</span></span> <br/> |<span data-ttu-id="22f60-194">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-194">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-195">**Troisième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-195">**Third name server**</span></span> <br/> |<span data-ttu-id="22f60-196">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-196">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="22f60-197">**Quatrième serveur de noms**</span><span class="sxs-lookup"><span data-stu-id="22f60-197">**Fourth name server**</span></span> <br/> |<span data-ttu-id="22f60-198">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="22f60-198">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Google-Domains-BP-redelegate-1-7](../../media/e008dccb-d789-4f52-8ecc-02831b7c6fb2.png)
  
4. <span data-ttu-id="22f60-200">Sélectionnez le contrôle **+ (ajouter)** pour créer une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="22f60-200">Select the **+(add)** control to create an empty row.</span></span> 
    
    ![Google-Domains-BP-Redelegate-1-8](../../media/6ce40b1e-8464-443f-a64a-825dc8764590.png)
  
5. <span data-ttu-id="22f60-202">Ajoutez les deux autres enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="22f60-202">Add the other two Nameserver records.</span></span>
    
    <span data-ttu-id="22f60-203">Dans la section **utiliser des serveurs de noms personnalisés** , créez un enregistrement en utilisant les valeurs de la ligne suivante du tableau, puis sélectionnez le contrôle **+ (ajouter)** pour ajouter une autre ligne.</span><span class="sxs-lookup"><span data-stu-id="22f60-203">In the **Use custom name servers** section, create a record by using the values from the next row in the table, and then select the **+(add)** control to add another row.</span></span> 
    
    <span data-ttu-id="22f60-204">Répétez cette procédure jusqu'à avoir créé les quatre enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="22f60-204">Repeat this process until you have created all four Nameserver records.</span></span>
    
6. <span data-ttu-id="22f60-205">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="22f60-205">Select **Save**.</span></span>
    
    ![Google-Domains-BP-Redelegate-1-5](../../media/cb954aa2-12ee-4e90-9b67-184cbe898bbb.png)
  
> [!NOTE]
> <span data-ttu-id="22f60-p113">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="22f60-p113">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
