---
title: Modifier les serveurs de noms pour configurer Office 365 avec 1&1 IONOS
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
ms.assetid: 31efc571-c8b9-46fb-b42d-203c2fb25289
description: Découvrez comment configurer Office 365 géré par 21Vianet pour gérer vos enregistrements DNS, quand 1&1 Internet est le fournisseur d’hébergement DNS.
ms.openlocfilehash: bda6a19ba7bfca20bc1764187f429e13900d8460
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43212364"
---
# <a name="change-nameservers-to-set-up-office-365-with-11-ionos"></a><span data-ttu-id="2b81b-103">Modifier les serveurs de noms pour configurer Office 365 avec 1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="2b81b-103">Change nameservers to set up Office 365 with 1&1 IONOS</span></span>

 <span data-ttu-id="2b81b-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="2b81b-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="2b81b-105">Suivez ces instructions si vous voulez laisser le soin à Office 365 de gérer vos enregistrements DNS Office 365 à votre place.</span><span class="sxs-lookup"><span data-stu-id="2b81b-105">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you.</span></span> <span data-ttu-id="2b81b-106">(Si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Office 365 à 1&1 Ionos](create-dns-records-at-1-1-internet.md).)</span><span class="sxs-lookup"><span data-stu-id="2b81b-106">(If you prefer, you can [manage all your Office 365 DNS records at 1&1 IONOS](create-dns-records-at-1-1-internet.md).)</span></span> 
  

    
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="2b81b-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="2b81b-107">Add a TXT record for verification</span></span>


<span data-ttu-id="2b81b-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2b81b-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="2b81b-112">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:42)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="2b81b-112">Follow the steps below or [watch the video (start at 0:42)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="2b81b-113">Pour commencer, accédez à la page de vos domaines à l’adresse 1&1 IONOS via [ce lien](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F).</span><span class="sxs-lookup"><span data-stu-id="2b81b-113">To get started, go to your domains page at 1&1 IONOS via [this link](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F).</span></span> <span data-ttu-id="2b81b-114">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="2b81b-114">You'll be prompted to log in.</span></span> 
    
2. <span data-ttu-id="2b81b-115">Sous **Mes domaines**, sélectionnez **gérer les domaines**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-115">Under **MY DOMAINS**, select **Manage domains**.</span></span>
    
3. <span data-ttu-id="2b81b-116">Sur la page **Centre de domaines** , recherchez le domaine que vous souhaitez mettre à jour ; Ensuite, sélectionnez le contrôle de **volet** ( **v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="2b81b-116">On the **Domain Center** page, find the domain that you want to update; then select the **Panel** ( **v**) control for that domain.</span></span>
    
4. <span data-ttu-id="2b81b-117">Dans la zone **paramètres du domaine** , sélectionnez Modifier les **paramètres DNS**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-117">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="2b81b-118">Dans la section **txt and SRV Records (enregistrements TXT** ), sélectionnez **Add record (ajouter un enregistrement**).</span><span class="sxs-lookup"><span data-stu-id="2b81b-118">In the **TXT and SRV Records** section, select **Add Record**.</span></span>
    
    <span data-ttu-id="2b81b-119">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="2b81b-119">(You may have to scroll down.)</span></span> 
    
6. <span data-ttu-id="2b81b-120">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="2b81b-120">In the **Add Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="2b81b-121">**Type**</span><span class="sxs-lookup"><span data-stu-id="2b81b-121">**Type**</span></span> <br/> |<span data-ttu-id="2b81b-122">**Prefix (Préfixe)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-122">**Prefix**</span></span> <br/> |<span data-ttu-id="2b81b-123">**Name Value (Valeur de nom)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-123">**Name Value**</span></span> <br/> |
|<span data-ttu-id="2b81b-124">TXT</span><span class="sxs-lookup"><span data-stu-id="2b81b-124">TXT</span></span>  <br/> |<span data-ttu-id="2b81b-125">(Leave this field empty.)</span><span class="sxs-lookup"><span data-stu-id="2b81b-125">(Leave this field empty.)</span></span>  <br/> |<span data-ttu-id="2b81b-126">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="2b81b-126">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="2b81b-127">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="2b81b-127">**Note**: This is an example.</span></span> <span data-ttu-id="2b81b-128">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="2b81b-128">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="2b81b-129">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="2b81b-129">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md) <br/> |

   
7. <span data-ttu-id="2b81b-130">Sélectionnez **Enregistrer**, puis **Enregistrer** à nouveau.</span><span class="sxs-lookup"><span data-stu-id="2b81b-130">Select **Save**, and then **Save** again.</span></span> 
    
8. <span data-ttu-id="2b81b-131">Dans la boîte de dialogue **modifier les paramètres DNS** , sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-131">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
9. <span data-ttu-id="2b81b-132">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="2b81b-132">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="2b81b-133">L’enregistrement étant désormais ajouté sur le site de votre bureau d’enregistrement de domaines, revenez à Office 365 et demandez à Office 365 de rechercher l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2b81b-133">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="2b81b-134">Lorsqu’Office 365 trouve l’enregistrement TXT approprié, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="2b81b-134">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="2b81b-135">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="2b81b-135">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>
    
2. <span data-ttu-id="2b81b-136">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="2b81b-136">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="2b81b-137">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-137">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="2b81b-138">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-138">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2b81b-139">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="2b81b-139">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="2b81b-140">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="2b81b-140">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="2b81b-141">Si vous rencontrez des difficultés avec le flux de courrier ou d'autres problèmes suite à l'ajout des enregistrements DNS, consultez [Rechercher et corriger les problèmes suite à l'ajout de votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="2b81b-141">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="2b81b-142">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="2b81b-142">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="2b81b-p107">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p107">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="2b81b-p108">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés. Par exemple, les messages envoyés à votre domaine (tel que thomas@ *votre_domaine*  .com) arriveront dans Office 365 une fois cette modification appliquée.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p108">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change.</span></span> 
  
<span data-ttu-id="2b81b-p109">Vous êtes prêt à modifier vos enregistrements NS de sorte que Office 365 puisse configurer votre domaine ? Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 2:47)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="2b81b-p109">Ready to change your NS records so Office 365 can set up your domain? Follow the steps below or [watch the video (start at 2:47)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-1-1-Internet-0ef1b3b5-d27a-4004-8ca1-fbe0453a0ea3?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
> [!IMPORTANT]
>  <span data-ttu-id="2b81b-150">La procédure suivante montre comment supprimer tous les autres serveurs de noms indésirables de la liste, et également comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="2b81b-150">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="2b81b-151">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants : > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-151">>  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com</span></span> 
  
1. <span data-ttu-id="2b81b-152">Pour commencer, accédez à la page de vos domaines à l’adresse 1&1 IONOS à l’aide de [ce lien](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F).</span><span class="sxs-lookup"><span data-stu-id="2b81b-152">To get started, go to your domains page at 1&1 IONOS by using [this link](https://account.1and1.com/?redirect_url=https%3A%2F%2Fmy.1and1.com%2F).</span></span> <span data-ttu-id="2b81b-153">You'll be prompted to log in.</span><span class="sxs-lookup"><span data-stu-id="2b81b-153">You'll be prompted to log in.</span></span> 
    
2. <span data-ttu-id="2b81b-154">Sous **Mes domaines**, sélectionnez **gérer les domaines**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-154">Under **MY DOMAINS**, select **Manage domains**.</span></span>
    
3. <span data-ttu-id="2b81b-155">Sur la page **Centre de domaine** , recherchez le domaine que vous souhaitez mettre à jour, puis sélectionnez le contrôle de **volet** ( **v**) pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="2b81b-155">On the **Domain Center** page, find the domain that you want to update, and then select the **Panel** ( **v**) control for that domain.</span></span>
    
4. <span data-ttu-id="2b81b-156">Dans la zone **paramètres du domaine** , sélectionnez Modifier les **paramètres DNS**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-156">In the **Domain Settings** area, select **Edit DNS Settings**.</span></span>
    
5. <span data-ttu-id="2b81b-157">Dans la section **Name Server Settings (Paramètres du serveur de noms)**, sélectionnez **Other name servers (Autres serveurs de noms)**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-157">In the **Name Server Settings** section, select **Other name servers**.</span></span>
    
    <span data-ttu-id="2b81b-158">(Vous devrez peut-être faire défiler la page vers le bas.)</span><span class="sxs-lookup"><span data-stu-id="2b81b-158">(You may have to scroll down.)</span></span>
    
6. <span data-ttu-id="2b81b-159">Suivez l'une des procédures suivantes en fonction du scénario qui s'applique à votre cas dans la page qui s'affiche :</span><span class="sxs-lookup"><span data-stu-id="2b81b-159">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:</span></span>
    
  - <span data-ttu-id="2b81b-160">Si **AUCUN** serveur de noms n'est encore répertorié, [Si AUCUN serveur de noms n'est encore répertorié](#if-there-are-no-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="2b81b-160">If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).</span></span>
    
  - <span data-ttu-id="2b81b-161">Si **DES** serveurs de noms sont déjà répertoriés, [Si DES serveurs de noms sont déjà répertoriés](#if-there-are-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="2b81b-161">If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="2b81b-162">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="2b81b-162">If there are NO nameservers already listed</span></span>

1. <span data-ttu-id="2b81b-163">Dans la zone **Name server 1 (Serveur de noms 1)**, tapez ou copiez-collez la valeur du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b81b-163">In the **Name server 1** box, type or copy and paste the value from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="2b81b-164">**Name server 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-164">**Name server 1**</span></span> <br/> |<span data-ttu-id="2b81b-165">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-165">ns1.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Saisie d’une valeur dans la zone Nom du serveur 1](../../media/34509935-461f-427f-9796-c3cf840bd9be.png)
  
2. <span data-ttu-id="2b81b-167">Dans le menu déroulant **Additional name servers (Autres serveurs de noms)**, sélectionnez **My secondary name servers (Mes serveurs de noms secondaires)**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-167">In the **Additional name servers** drop-down list, choose **My secondary name servers**.</span></span>
    
    ![Choosing My secondary name servers in the list](../../media/7eb14856-86da-45c2-910c-c72312250a18.png)
  
3. <span data-ttu-id="2b81b-169">Dans les zones **Serveur de noms (2, 3 et 4)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b81b-169">In the **Name server 2, 3, and 4** boxes, type or copy and paste the value from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="2b81b-170">**Name server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-170">**Name server 2**</span></span> <br/> |<span data-ttu-id="2b81b-171">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-171">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="2b81b-172">**Serveur de noms 3**</span><span class="sxs-lookup"><span data-stu-id="2b81b-172">**Name server 3**</span></span> <br/> |<span data-ttu-id="2b81b-173">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-173">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="2b81b-174">**Serveur de noms 4**</span><span class="sxs-lookup"><span data-stu-id="2b81b-174">**Name server 4**</span></span> <br/> |<span data-ttu-id="2b81b-175">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-175">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
    ![Entering name server values](../../media/0f15880c-88b6-4133-8f31-62f0d98ee63f.png)
  
4. <span data-ttu-id="2b81b-176">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-176">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer dans la page Paramètres du serveur de noms.](../../media/864f7927-7127-4784-b8d2-dadfea2f9dc8.png)
  
5. <span data-ttu-id="2b81b-178">Dans la boîte de dialogue **modifier les paramètres DNS** , sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-178">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
    ![Sélection de l’option Enregistrer dans la boîte de dialogue Modifier les paramètres DNS](../../media/0558e24c-17cd-428c-9ec1-5ed46481af7c.png)
  
> [!NOTE]
> <span data-ttu-id="2b81b-p112">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p112">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="2b81b-182">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="2b81b-182">If there ARE nameservers already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="2b81b-p113">Suivez ces étapes  *uniquement*  si vous avez des serveurs de noms existants autres que les quatre serveurs de noms  *corrects*  . Autrement dit, ne supprimez  *que*  les serveurs de noms  *qui ne sont pas*  nommés **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com** ou **ns4.bdm.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p113">Follow these steps  *only*  if you have existing nameservers other than the four  *correct*  nameservers. (That is, delete  *only*  any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
1. <span data-ttu-id="2b81b-185">Si d'autres serveurs de noms sont répertoriés dans les zones **Name server (Serveur de noms)**, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="2b81b-185">If there are already nameservers listed in the **Name server** boxes, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
    ![Deleting name servers](../../media/af0a68cc-b058-4925-b3b1-52dfded003c1.png)
  
2. <span data-ttu-id="2b81b-187">Dans les zones **Serveur de noms (1, 2, 3 et 4)**, tapez ou copiez-collez les valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b81b-187">In the **Name server 1, 2, 3, and 4** boxes, type or copy and paste the values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="2b81b-188">**Name server 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-188">**Name server 1**</span></span> <br/> |<span data-ttu-id="2b81b-189">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-189">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="2b81b-190">**Name server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="2b81b-190">**Name server 2**</span></span> <br/> |<span data-ttu-id="2b81b-191">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-191">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="2b81b-192">**Serveur de noms 3**</span><span class="sxs-lookup"><span data-stu-id="2b81b-192">**Name server 3**</span></span> <br/> |<span data-ttu-id="2b81b-193">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-193">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="2b81b-194">**Serveur de noms 4**</span><span class="sxs-lookup"><span data-stu-id="2b81b-194">**Name server 4**</span></span> <br/> |<span data-ttu-id="2b81b-195">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2b81b-195">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Entrée de valeurs de serveur de noms](../../media/52826bd1-0596-4103-a728-d5d28b9610d2.png)
  
3. <span data-ttu-id="2b81b-197">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-197">Select **Save**.</span></span>
    
    ![Sélectionnez Enregistrer dans la page Paramètres du serveur de noms.](../../media/cd10e4fb-b7fa-480f-855b-a443f2705cf2.png)
  
4. <span data-ttu-id="2b81b-199">Dans la boîte de dialogue **modifier les paramètres DNS** , sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2b81b-199">In the **Edit DNS Settings** dialog box, select **Yes**.</span></span>
    
    ![Sélection de l’option Enregistrer dans la boîte de dialogue Modifier les paramètres DNS](../../media/0558e24c-17cd-428c-9ec1-5ed46481af7c.png)
  
> [!NOTE]
> <span data-ttu-id="2b81b-p114">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="2b81b-p114">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  


