---
title: Modifier les serveurs de noms pour configurer Office 365 auprès de Network Solutions
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
ms.assetid: d4ba60f3-4e1c-4180-99bd-250b8955be2a
description: 'Apprenez à configurer votre domaine personnalisé Office 365 avec des solutions réseau si vous souhaitez qu’Office 365 gère vos enregistrements DNS. '
ms.openlocfilehash: c9465da507e6b4dea35f9ead50b5bc7c14a1b38f
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42242611"
---
# <a name="change-nameservers-to-set-up-office-365-with-network-solutions"></a><span data-ttu-id="8ff1d-103">Modifier les serveurs de noms pour configurer Office 365 auprès de Network Solutions</span><span class="sxs-lookup"><span data-stu-id="8ff1d-103">Change nameservers to set up Office 365 with Network Solutions</span></span>

 <span data-ttu-id="8ff1d-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="8ff1d-p101">Si vous voulez qu'Office 365 gère vos enregistrements DNS Office 365 à votre place, suivez ces instructions (vous pouvez également [gérer tous vos enregistrements DNS Office 365 via Network Solutions](create-dns-records-at-network-solutions.md)).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p101">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at Network Solutions](create-dns-records-at-network-solutions.md).)</span></span>
  
    
## <a name="add-a-txt-record-at-network-solutions-to-verify-that-you-own-the-domain"></a><span data-ttu-id="8ff1d-107">Ajouter un enregistrement TXT auprès de Network Solutions pour vérifier que vous êtes propriétaire du domaine</span><span class="sxs-lookup"><span data-stu-id="8ff1d-107">Add a TXT record at Network Solutions to verify that you own the domain</span></span>

<span data-ttu-id="8ff1d-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8ff1d-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
<span data-ttu-id="8ff1d-112">Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 0:47)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-112">Follow the steps below or [watch the video (start at 0:47)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
1. <span data-ttu-id="8ff1d-p104">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p104">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it). You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="8ff1d-115">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="8ff1d-115">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span>
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="8ff1d-117">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-117">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="8ff1d-119">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-119">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="8ff1d-121">Sélectionnez **gérer les enregistrements DNS avancés**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-121">Select **Manage Advanced DNS Records**.</span></span>
    
    <span data-ttu-id="8ff1d-122">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="8ff1d-122">(You may have to scroll down.)</span></span>
    
    ![Sélectionnez gérer les enregistrements DNS avancés](../media/fd2956d6-eec3-47ea-b60a-266bab14f51f.png)
  
5. <span data-ttu-id="8ff1d-124">Faites défiler jusqu’à la section **texte (enregistrements TXT)** , puis sélectionnez **modifier les enregistrements TXT**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-124">Scroll down to the **Text (TXT Records)** section, and then select **Edit TXT Records**.</span></span>
    
    ![Sélectionnez modifier les enregistrements TXT](../media/240a01d6-750a-4da6-8554-641b571e4b71.png)
  
6. <span data-ttu-id="8ff1d-126">Dans les zones du nouvel enregistrement, tapez ou copiez-collez les valeurs figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-126">In the boxes for the new record, type or copy and paste the values in the following table.</span></span>
    
|<span data-ttu-id="8ff1d-127">**Host (Hôte)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-127">**Host**</span></span>|<span data-ttu-id="8ff1d-128">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-128">**TTL**</span></span>|<span data-ttu-id="8ff1d-129">**Text (Texte)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-129">**Text**</span></span>|
|:-----|:-----|:-----|
|@  <br/> <span data-ttu-id="8ff1d-130">(The system will change this value to **@ (None)** when you save the record.)</span><span class="sxs-lookup"><span data-stu-id="8ff1d-130">(The system will change this value to **@ (None)** when you save the record.)</span></span>  <br/> |<span data-ttu-id="8ff1d-131">3600</span><span class="sxs-lookup"><span data-stu-id="8ff1d-131">3600</span></span>  <br/> |<span data-ttu-id="8ff1d-132">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="8ff1d-132">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="8ff1d-133">**Remarque**: Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-133">**Note**: This is an example.</span></span> <span data-ttu-id="8ff1d-134">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-134">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span>           [<span data-ttu-id="8ff1d-135">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="8ff1d-135">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)
   
    
   ![Tapez ou collez des valeurs dans les zones du nouvel enregistrement.](../media/8a76daab-b6ff-4c82-ba68-192b24fbb934.png)
  
7. <span data-ttu-id="8ff1d-137">Sélectionnez **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-137">Select **Continue**.</span></span>
    
    ![Sélectionnez continuer](../media/89e7fb38-b4d9-4949-a1bb-d0dd10b361e0.png)
  
8. <span data-ttu-id="8ff1d-139">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-139">Select **Save Changes**.</span></span>
    
    ![Sélectionnez Enregistrer les modifications.](../media/bd4d7cd0-c8a3-497a-b080-cfd5a5c60dc5.png)
  
9. <span data-ttu-id="8ff1d-141">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-141">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="8ff1d-142">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-142">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="8ff1d-143">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-143">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="8ff1d-144">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="8ff1d-144">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="8ff1d-145">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-145">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
    
  
3. <span data-ttu-id="8ff1d-146">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-146">On the **Setup** page, select **Start setup**.</span></span>
    
    
  
4. <span data-ttu-id="8ff1d-147">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-147">On the **Verify domain** page, select **Verify**.</span></span>
    
    
  
> [!NOTE]
>  <span data-ttu-id="8ff1d-p106">L'application des enregistrements DNS modifiés prend généralement 15 minutes. Il peut toutefois arriver que la répercussion d'une modification dans le système DNS sur Internet prenne davantage de temps. Si vous rencontrez des problèmes avec le flux de messages ou d'autres problèmes suite à l'ajout des enregistrements DNS, voir [Résolution des problèmes suite à la modification de votre nom de domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p106">Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="8ff1d-151">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="8ff1d-151">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="8ff1d-p107">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p107">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="8ff1d-p108">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés. Par exemple, les messages envoyés à votre domaine (tel que thomas@ *votre_domaine*  .com) arriveront dans Office 365 une fois cette modification appliquée.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p108">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change.</span></span>
  
<span data-ttu-id="8ff1d-p109">Vous êtes prêt à modifier vos enregistrements NS de sorte que Office 365 puisse configurer votre domaine ? Suivez les étapes décrites ci-dessous ou [regardez la vidéo (commencez la lecture à 2:23)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p109">Ready to change your NS records so Office 365 can set up your domain? Follow the steps below or [watch the video (start at 2:23)](https://support.office.com/article/Video-Change-nameservers-to-set-up-Office-365-with-Network-Solutions-69b092e3-c026-4d19-a7d0-16cdb2d8b261?ui=en-US&amp;rs=en-US&amp;ad=US).</span></span>
  
> [!IMPORTANT]
>  <span data-ttu-id="8ff1d-159">Une fois que vous avez effectué les étapes de cette section, les *seuls* serveurs de noms qui doivent être répertoriés sont les quatre suivants : **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**et **NS4.BDM.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-159">When you have completed the steps in this section, the  *only*  nameservers that should be listed are these four: **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, and **ns4.bdm.microsoftonline.com**.</span></span> <span data-ttu-id="8ff1d-160">La procédure suivante décrit comment supprimer tout autre serveur de noms indésirable de la liste, et y ajouter les serveurs de noms  *corrects*  qui n'y figurent pas encore.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-160">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the  *correct*  nameservers if they are not already in the list.</span></span> 
  
1. <span data-ttu-id="8ff1d-161">Pour commencer, accédez à la page de vos domaines sur Network Solutions à l'aide de [ce lien](https://www.networksolutions.com/manage-it).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-161">To get started, go to your domains page at Network Solutions by using [this link](https://www.networksolutions.com/manage-it).</span></span> <span data-ttu-id="8ff1d-162">Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-162">You'll be prompted to log in.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="8ff1d-163">Avant de cliquer sur le bouton de **connexion** , choisissez **gérer mes noms de domaine** dans la liste déroulante **se connecter à :** .</span><span class="sxs-lookup"><span data-stu-id="8ff1d-163">Before you select the **Login** button, first choose **Manage My Domain Names** in the **Log In to:** drop-down list.</span></span> 
  
    ![Sélectionnez Manage My Domain Names (Gérer mes noms de domaine) et connectez-vous à Network Solutions](../media/fda7d4a1-9445-4086-be9c-87c6983ef2aa.png)
  
2. <span data-ttu-id="8ff1d-165">Cochez la case située en regard du nom du domaine que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-165">Select the check box next to the name of the domain that you are modifying.</span></span>
    
    ![Activez la case à cocher correspondant à votre domaine](../media/2c13d2ba-4a31-44da-812c-2cc90900a183.png)
  
3. <span data-ttu-id="8ff1d-167">Sélectionnez **modifier DNS**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-167">Select **Edit DNS**.</span></span>
    
    ![Sélectionnez Modifier DNS](../media/9d7c269f-48d1-442c-9d7b-63bd384a36a9.png)
  
4. <span data-ttu-id="8ff1d-169">Sélectionnez **déplacer DNS**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-169">Select **Move DNS**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-1](../media/e57a30f3-63d5-4bcb-84c6-c8be21c261a2.png)
  
5. <span data-ttu-id="8ff1d-171">Suivez l'une des procédures suivantes en fonction du scénario qui s'applique à votre cas dans la page qui s'affiche :</span><span class="sxs-lookup"><span data-stu-id="8ff1d-171">Depending on whether or not there are already nameservers listed on the page that is displayed now, continue to one of the two following procedures:</span></span>
    
  - <span data-ttu-id="8ff1d-172">Si **AUCUN** serveur de noms n'est encore répertorié, [Si AUCUN serveur de noms n'est encore répertorié](#if-there-are-no-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-172">If there are **NO** nameservers already listed, [If there are NO nameservers already listed](#if-there-are-no-nameservers-already-listed).</span></span>
    
  - <span data-ttu-id="8ff1d-173">Si **DES** serveurs de noms sont déjà répertoriés, [Si DES serveurs de noms sont déjà répertoriés](#if-there-are-nameservers-already-listed).</span><span class="sxs-lookup"><span data-stu-id="8ff1d-173">If there **ARE** nameservers already listed, [If there ARE nameservers already listed](#if-there-are-nameservers-already-listed).</span></span>
    
### <a name="if-there-are-no-nameservers-already-listed"></a><span data-ttu-id="8ff1d-174">Si AUCUN serveur de noms n'est encore répertorié</span><span class="sxs-lookup"><span data-stu-id="8ff1d-174">If there are NO nameservers already listed</span></span>

1. <span data-ttu-id="8ff1d-175">Dans la page **domaines** , dans la section **spécifier les serveurs de noms de domaine** , sélectionnez Ajouter d' **autres serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-175">On the **Domains** page, in the **Specify Domain Name Servers** section, select **Add More Name Servers**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-1](../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
2. <span data-ttu-id="8ff1d-177">Sur la page **Domain Names (Noms de domaines)**, tapez ou copiez-collez les valeurs de serveur de noms du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-177">On the **Domain Names** page, type or copy and paste the nameserver values from the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="8ff1d-178">**Name server 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-178">**Name Server 1**</span></span> <br/> |<span data-ttu-id="8ff1d-179">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-179">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-180">**Name Server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-180">**Name Server 2**</span></span> <br/> |<span data-ttu-id="8ff1d-181">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-181">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-182">**Name Server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-182">**Name Server 2**</span></span> <br/> |<span data-ttu-id="8ff1d-183">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-183">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-184">**Name server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-184">**Name Server 2**</span></span> <br/> |<span data-ttu-id="8ff1d-185">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-185">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
    
![NetworkSolutionsBP-redelegate-1-2-2](../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
3. <span data-ttu-id="8ff1d-187">Sélectionnez **déplacer DNS**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-187">Select **Move DNS**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-3](../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
4. <span data-ttu-id="8ff1d-189">Sélectionnez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-189">Select **Save Changes**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-4](../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> <span data-ttu-id="8ff1d-p112">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p112">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
  
### <a name="if-there-are-nameservers-already-listed"></a><span data-ttu-id="8ff1d-193">Si DES serveurs de noms sont déjà répertoriés</span><span class="sxs-lookup"><span data-stu-id="8ff1d-193">If there ARE nameservers already listed</span></span>

> [!CAUTION]
> <span data-ttu-id="8ff1d-p113">Suivez ces étapes  *uniquement*  si vous avez des serveurs de noms existants autres que les quatre serveurs de noms  *corrects*  . Autrement dit, ne supprimez  *que*  les serveurs de noms  *qui ne sont pas*  nommés **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com** ou **ns4.bdm.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p113">Follow these steps  *only*  if you have existing nameservers other than the four  *correct*  nameservers. (That is, delete  *only*  any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span>
  
1. <span data-ttu-id="8ff1d-196">Si d'autres serveurs de noms sont répertoriés, supprimez-les en les sélectionnant et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-196">If there are any other nameservers listed, delete each one by selecting it and then pressing the **Delete** key on your keyboard.</span></span>
    
    ![NetworkSolutions-BP-redelegate-1-5](../media/eeb8ad22-bf4a-43a8-b97a-f09c3654d89b.png)
  
2. <span data-ttu-id="8ff1d-198">Sélectionnez **ajouter d’autres serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-198">Select **Add More Name Servers**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-1](../media/57e22ef1-ac88-4d4a-bc8e-058023255dfd.png)
  
3. <span data-ttu-id="8ff1d-200">Sur la page **Domain Names (Noms de domaines)**, tapez ou copiez-collez les valeurs de serveur de noms du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-200">On the **Domain Names** page, type or copy and paste the nameserver values from the following table.</span></span>
 
    
|||
|:-----|:-----|
|<span data-ttu-id="8ff1d-201">**Name server 1 (Serveur de noms 1)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-201">**Name Server 1**</span></span> <br/> |<span data-ttu-id="8ff1d-202">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-202">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-203">**Name Server 2 (Serveur de noms 2)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-203">**Name Server 2**</span></span> <br/> |<span data-ttu-id="8ff1d-204">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-204">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-205">**Name Server 3 (Serveur de noms 3)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-205">**Name Server 3**</span></span> <br/> |<span data-ttu-id="8ff1d-206">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-206">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="8ff1d-207">**Name Server 4 (Serveur de noms 4)**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-207">**Name Server 4**</span></span> <br/> |<span data-ttu-id="8ff1d-208">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="8ff1d-208">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
    
![NetworkSolutionsBP-redelegate-1-2-2](../media/795e8c6b-4828-4de2-b624-82f067bb2eb1.png)
  
4. <span data-ttu-id="8ff1d-210">Sélectionnez **déplacer DNS**.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-210">Select **Move DNS**.</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-3](../media/d4a0a7c2-6868-471f-bbf4-16ce2e2348de.png)
  
5. <span data-ttu-id="8ff1d-212">Sélectionnez **enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="8ff1d-212">Select **Save Changes.**</span></span>
    
    ![NetworkSolutionsBP-redelegate-1-2-4](../media/897bc864-b340-4385-abeb-f94bc7f73e5e.png)
  
> [!NOTE]
> <span data-ttu-id="8ff1d-p114">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-p114">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span>