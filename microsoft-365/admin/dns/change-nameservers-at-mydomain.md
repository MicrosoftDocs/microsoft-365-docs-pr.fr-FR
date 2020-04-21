---
title: Modifier les serveurs de noms pour configurer Microsoft avec Mon_domaine
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
description: Découvrez comment configurer Microsoft pour gérer les enregistrements DNS de votre domaine personnalisé sur Mon_domaine.
ms.openlocfilehash: 8f4a72aa0ece24ed09c4d036239a2a13c196be6c
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629790"
---
# <a name="change-nameservers-to-set-up-microsoft-with-mydomain"></a><span data-ttu-id="94a6b-103">Modifier les serveurs de noms pour configurer Microsoft avec Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="94a6b-103">Change nameservers to set up Microsoft with MyDomain</span></span>

 <span data-ttu-id="94a6b-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="94a6b-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="94a6b-105">Suivez ces instructions si vous voulez que Microsoft gère vos enregistrements DNS pour vous.</span><span class="sxs-lookup"><span data-stu-id="94a6b-105">Follow these instructions if you want Microsoft to manage your DNS records for you.</span></span> <span data-ttu-id="94a6b-106">(Si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Microsoft sur mondomaine](create-dns-records-at-mydomain.md).)</span><span class="sxs-lookup"><span data-stu-id="94a6b-106">(If you prefer, you can [manage all your Microsoft DNS records at MyDomain](create-dns-records-at-mydomain.md).)</span></span>
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="94a6b-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="94a6b-107">Add a TXT record for verification</span></span>

<span data-ttu-id="94a6b-108">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="94a6b-108">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="94a6b-109">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="94a6b-109">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="94a6b-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="94a6b-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="94a6b-p104">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="94a6b-p104">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="94a6b-114">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-114">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="94a6b-115">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="94a6b-115">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="94a6b-116">Sur la ligne de la **Vue d'ensemble**, choisissez **DNS**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-116">In the **Overview** row, select **DNS**.</span></span>
    
5. <span data-ttu-id="94a6b-117">Dans la liste déroulante **Modifier**, sélectionnez **Enregistrement TXT/SPF**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-117">From the **Modify** drop-down list, choose **TXT/SPF Record**.</span></span>
    
6. <span data-ttu-id="94a6b-118">Sous **Content (Contenu)**, dans la zone du nouvel enregistrement, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94a6b-118">Under **Content**, in the box for the new record, type or copy and paste the value from the following table.</span></span>
    
||
|:-----|
|<span data-ttu-id="94a6b-119">**Content**</span><span class="sxs-lookup"><span data-stu-id="94a6b-119">**Content**</span></span> <br/> |
|<span data-ttu-id="94a6b-120">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="94a6b-120">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="94a6b-121">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="94a6b-121">**Note**: This is an example.</span></span> <span data-ttu-id="94a6b-122">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="94a6b-122">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="94a6b-123">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="94a6b-123">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)          |
   
7. <span data-ttu-id="94a6b-124">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-124">Select **Add**.</span></span>
    
8. <span data-ttu-id="94a6b-125">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="94a6b-125">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="94a6b-126">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous revenez à Microsoft 365 et demandez à Microsoft 365 de Rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="94a6b-126">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft 365 and request Microsoft 365 to look for the record.</span></span>
  
<span data-ttu-id="94a6b-127">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="94a6b-127">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="94a6b-128">Dans le centre d’administration Microsoft, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="94a6b-128">In the Microsoft admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="94a6b-129">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="94a6b-129">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="94a6b-130">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-130">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="94a6b-131">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-131">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="94a6b-132">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="94a6b-132">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="94a6b-133">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="94a6b-133">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="94a6b-134">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="94a6b-134">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="94a6b-135">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="94a6b-135">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="94a6b-136">Pour terminer la configuration de votre domaine avec Microsoft, vous devez modifier les enregistrements de serveur de noms de votre domaine au niveau de votre bureau d’enregistrement de domaines afin de pointer vers les serveurs de noms principaux et secondaires Microsoft.</span><span class="sxs-lookup"><span data-stu-id="94a6b-136">To complete setting up your domain with Microsoft, you change your domain's NS records at your domain registrar to point to the Microsoft primary and secondary name servers.</span></span> <span data-ttu-id="94a6b-137">Cela permet à Microsoft de mettre à jour les enregistrements DNS du domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="94a6b-137">This sets up Microsoft to update the domain's DNS records for you.</span></span> <span data-ttu-id="94a6b-138">Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="94a6b-138">We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="94a6b-139">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="94a6b-139">When you change your domain's NS records to point to the Microsoft name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="94a6b-140">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain.*</span><span class="sxs-lookup"><span data-stu-id="94a6b-140">For example, all email sent to your domain (like rob@ *your_domain.*</span></span> <span data-ttu-id="94a6b-141">com) démarrera à Microsoft une fois cette modification apportée.</span><span class="sxs-lookup"><span data-stu-id="94a6b-141">com) will start coming to Microsoft after you make this change.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="94a6b-142">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span><span class="sxs-lookup"><span data-stu-id="94a6b-142">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already in the list.</span></span> <br/> <span data-ttu-id="94a6b-143">When you have completed the steps in this section, the only nameservers that should be listed are these four:</span><span class="sxs-lookup"><span data-stu-id="94a6b-143">When you have completed the steps in this section, the only nameservers that should be listed are these four:</span></span>
  
1. <span data-ttu-id="94a6b-p110">Pour commencer, accédez à la page de vos domaines sur le site MyDomain en utilisant [ce lien](https://www.mydomain.com/controlpanel). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="94a6b-p110">To get started, go to your domains page at MyDomain by using [this link](https://www.mydomain.com/controlpanel). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="94a6b-146">Dans la rubrique **Mes favoris**, choisissez **Domaine central**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-146">In the **My Favorites** section, select **Domain Central**.</span></span>
    
3. <span data-ttu-id="94a6b-147">Sous **Domaine**, sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="94a6b-147">Under **Domain**, select the name of the domain that you want to edit.</span></span>
    
4. <span data-ttu-id="94a6b-148">Dans la ligne **vue d’ensemble** , sélectionnez serveurs de **noms**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-148">In the **Overview** row, select **Nameservers**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-1](../../media/49e91235-44b5-46d6-a82e-8f11329db3d6.png)
  
5. <span data-ttu-id="94a6b-150">Dans la section **Update Name Servers**, sélectionnez **Use different name servers**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-150">In the **Update Name Servers** section, select **Use different name servers**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-2-1](../../media/f869fb26-54dc-4b66-8378-a78a79b582bd.png)
  
6. <span data-ttu-id="94a6b-152">Selon qu’il y a déjà ou non des serveurs de noms répertoriés dans la page qui s’affiche maintenant, passez à l’une des deux procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="94a6b-152">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures.</span></span>
    
### <a name="if-the-correct-nameservers-are-already-listed"></a><span data-ttu-id="94a6b-153">Si les serveurs de noms appropriés SONT déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="94a6b-153">If the correct nameservers ARE already listed</span></span>

- <span data-ttu-id="94a6b-154">Si les serveurs de noms corrects sont répertoriés, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="94a6b-154">If the correct nameservers are already listed, you can skip this step.</span></span>
    
    ![Mondomaine-BP-redelegate-1-2-2](../../media/601f6a46-15bd-4a92-b792-ac628ff86628.png)
  
### <a name="if-the-correct-nameservers-are-not-already-listed"></a><span data-ttu-id="94a6b-156">Si les serveurs de noms corrects ne sont PAS répertoriés</span><span class="sxs-lookup"><span data-stu-id="94a6b-156">If the correct nameservers are NOT already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="94a6b-157">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="94a6b-157">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="94a6b-158">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="94a6b-158">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="94a6b-159">Supprimez les serveurs de noms existants en sélectionnant chaque entrée du champ **Nameserver : (Serveur de noms :)**, puis en appuyant sur la touche **Suppr** de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="94a6b-159">Delete the existing nameservers by selecting each entry in the **Nameserver:** field, and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Mondomaine-BP-redelegate-1-3-1](../../media/5024cd27-a2b1-42a2-99e4-5ceb5e6eddb9.png)
  
2. <span data-ttu-id="94a6b-161">Sélectionnez **plus** deux fois pour ajouter deux nouvelles lignes de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="94a6b-161">Select **Add More** twice to add two new Nameserver rows.</span></span> 
    
    ![Mondomaine-BP-redelegate-1-3-2](../../media/19307893-2f73-4e4d-9221-a5870e09ab48.png)
  
3. <span data-ttu-id="94a6b-163">Dans les zones des enregistrements, tapez ou copiez-collez les valeurs de serveur de noms du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94a6b-163">In the boxes for the records, type or copy and paste the nameserver values from the following table.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="94a6b-164">**Nameserver 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="94a6b-164">**Nameserver 1**</span></span> <br/> |<span data-ttu-id="94a6b-165">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="94a6b-165">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="94a6b-166">**Nameserver 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="94a6b-166">**Nameserver 2**</span></span> <br/> |<span data-ttu-id="94a6b-167">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="94a6b-167">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="94a6b-168">**Nameserver 3 (Serveur de noms 3)**</span><span class="sxs-lookup"><span data-stu-id="94a6b-168">**Nameserver 3**</span></span> <br/> |<span data-ttu-id="94a6b-169">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="94a6b-169">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="94a6b-170">**Nameserver 4 (Serveur de noms 4)**</span><span class="sxs-lookup"><span data-stu-id="94a6b-170">**Nameserver 4**</span></span> <br/> |<span data-ttu-id="94a6b-171">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="94a6b-171">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Mondomaine-BP-redelegate-1-4](../../media/7427e99c-49c7-4a2e-a5bf-66fc46900cd1.png)
  
4. <span data-ttu-id="94a6b-173">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="94a6b-173">Select **Save**.</span></span>
    
    ![Mondomaine-BP-redelegate-1-5](../../media/48473816-b881-47f0-9344-74622efa3bf8.png)
  
> [!NOTE]
> <span data-ttu-id="94a6b-175">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="94a6b-175">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="94a6b-176">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="94a6b-176">Then your Microsoft email and other services will be all set to work with your domain.</span></span> 
