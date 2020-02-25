---
title: Modifier les serveurs de noms de manière à configurer Office 365 avec Amazon Web Services (AWS)
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
ms.assetid: 0ddbe33c-81ea-4c02-8db9-e71d3810c0ec
description: 'Découvrez comment configurer Office 365 pour gérer vos enregistrements DNS sur Amazon Web Services (AWS). '
ms.openlocfilehash: 08deba83738ba0e530e719cd6fd57bee423df5e0
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42242872"
---
# <a name="change-nameservers-to-set-up-office-365-with-amazon-web-services-aws"></a><span data-ttu-id="d5028-103">Modifier les serveurs de noms de manière à configurer Office 365 avec Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="d5028-103">Change nameservers to set up Office 365 with Amazon Web Services (AWS)</span></span>

 <span data-ttu-id="d5028-104">**[Consultez les Forums aux questions des domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="d5028-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="d5028-p101">Si vous voulez laisser Office 365 gérer vos enregistrements DNS Office 365 à votre place, suivez ces instructions (si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Office 365 via AWS](create-dns-records-at-aws.md)).</span><span class="sxs-lookup"><span data-stu-id="d5028-p101">Follow these instructions if you want Office 365 to manage your Office 365 DNS records for you. (If you prefer, you can [manage all your Office 365 DNS records at AWS](create-dns-records-at-aws.md).)</span></span>
  
    
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="d5028-107">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="d5028-107">Add a TXT record for verification</span></span>

<span data-ttu-id="d5028-p102">Avant d'utiliser votre domaine avec Office 365, nous devons vérifier que celui-ci vous appartient. Votre capacité à vous connecter à votre compte auprès de votre bureau d'enregistrement de domaines et à créer l'enregistrement DNS montre à Office 365 que le domaine vous appartient réellement.</span><span class="sxs-lookup"><span data-stu-id="d5028-p102">Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d5028-p103">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d5028-p103">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span> 
  
1. <span data-ttu-id="d5028-p104">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home). Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d5028-p104">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home). You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d5028-114">Sur la page **ressources** , sélectionnez **zones hébergées**.</span><span class="sxs-lookup"><span data-stu-id="d5028-114">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="d5028-115">Dans la page **zones hébergées** , dans la colonne **nom de domaine** , sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="d5028-115">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="d5028-116">Sélectionnez **créer un jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="d5028-116">Select **Create Record Set**.</span></span>
    
5. <span data-ttu-id="d5028-117">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d5028-117">In the **Create Record Set** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d5028-118">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span><span class="sxs-lookup"><span data-stu-id="d5028-118">(Choose the **Type** and **Routing Policy** values from the drop-down lists.)</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="d5028-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span><span class="sxs-lookup"><span data-stu-id="d5028-p105">The quotation marks required by the onscreen instructions are supplied automatically. You don't need to type them manually.</span></span> 
  
|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5028-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="d5028-121">**Name**</span></span> <br/> |<span data-ttu-id="d5028-122">**Type**</span><span class="sxs-lookup"><span data-stu-id="d5028-122">**Type**</span></span> <br/> |<span data-ttu-id="d5028-123">**Alias**</span><span class="sxs-lookup"><span data-stu-id="d5028-123">**Alias**</span></span> <br/> |<span data-ttu-id="d5028-124">**TTL (Seconds) (Durée de vie (secondes))**</span><span class="sxs-lookup"><span data-stu-id="d5028-124">**TTL (Seconds)**</span></span> <br/> |<span data-ttu-id="d5028-125">**Value (Valeur)**</span><span class="sxs-lookup"><span data-stu-id="d5028-125">**Value**</span></span> <br/> |<span data-ttu-id="d5028-126">**Routing Policy (Stratégie de routage)**</span><span class="sxs-lookup"><span data-stu-id="d5028-126">**Routing Policy**</span></span> <br/> |
|<span data-ttu-id="d5028-127">(Laissez ce champ vide)</span><span class="sxs-lookup"><span data-stu-id="d5028-127">(Leave this field empty)</span></span>  <br/> |<span data-ttu-id="d5028-128">TXT - Text</span><span class="sxs-lookup"><span data-stu-id="d5028-128">TXT - Text</span></span>  <br/> |<span data-ttu-id="d5028-129">Non</span><span class="sxs-lookup"><span data-stu-id="d5028-129">No</span></span>  <br/> |<span data-ttu-id="d5028-130">300</span><span class="sxs-lookup"><span data-stu-id="d5028-130">300</span></span>  <br/> |<span data-ttu-id="d5028-131">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="d5028-131">MS=ms *XXXXXXXX*</span></span> <br/> <span data-ttu-id="d5028-132">**Remarque :** Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="d5028-132">**Note:** This is an example.</span></span> <span data-ttu-id="d5028-133">Utilisez votre valeur **Adresse de destination ou de pointage** spécifique ici, à partir du tableau dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="d5028-133">Use your specific **Destination or Points to Address** value here, from the table in Office 365.</span></span> [<span data-ttu-id="d5028-134">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="d5028-134">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)  <br/>  |<span data-ttu-id="d5028-135">Simple</span><span class="sxs-lookup"><span data-stu-id="d5028-135">Simple</span></span> <br/> |
   
6. <span data-ttu-id="d5028-136">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="d5028-136">Select **Create**.</span></span>
    
7. <span data-ttu-id="d5028-137">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="d5028-137">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="d5028-138">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span><span class="sxs-lookup"><span data-stu-id="d5028-138">Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.</span></span>
  
<span data-ttu-id="d5028-139">When Office 365 finds the correct TXT record, your domain is verified.</span><span class="sxs-lookup"><span data-stu-id="d5028-139">When Office 365 finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="d5028-140">Dans le centre d’administration, accédez à la page **paramètres** \> des <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">domaines</a> .</span><span class="sxs-lookup"><span data-stu-id="d5028-140">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="d5028-141">Dans la page **domaines** , sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="d5028-141">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="d5028-142">Sur la page **installation** , sélectionnez **Démarrer l’installation**.</span><span class="sxs-lookup"><span data-stu-id="d5028-142">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="d5028-143">Sur la page **vérifier le domaine** , sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="d5028-143">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d5028-144">Typically it takes about 15 minutes for DNS changes to take effect.</span><span class="sxs-lookup"><span data-stu-id="d5028-144">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="d5028-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span><span class="sxs-lookup"><span data-stu-id="d5028-145">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="d5028-146">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS dans Office 365](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="d5028-146">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records in Office 365](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="d5028-147">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="d5028-147">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="d5028-p108">Pour finaliser la configuration de votre domaine avec Office 365, vous devez modifier les enregistrements de serveur de noms auprès de votre bureau d'enregistrement de domaines afin qu'ils pointent vers les serveurs de noms principal et secondaire Office 365. Office 365 est ainsi informé qu'il doit mettre à jour les enregistrements DNS du domaine pour vous. Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d5028-p108">To complete setting up your domain with Office 365, you change your domain's NS records at your domain registrar to point to the Office 365 primary and secondary name servers. This sets up Office 365 to update the domain's DNS records for you. We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="d5028-p109">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine de façon à ce qu'ils pointent vers les serveurs de noms Office 365, tous les services actuellement associés à votre domaine sont affectés. Par exemple, les messages envoyés à votre domaine (tel que thomas@ *votre_domaine*  .com) arriveront dans Office 365 une fois cette modification appliquée.</span><span class="sxs-lookup"><span data-stu-id="d5028-p109">When you change your domain's NS records to point to the Office 365 name servers, all the services that are currently associated with your domain are affected. For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Office 365 after you make this change.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="d5028-153">La procédure suivante montre comment supprimer tous les autres serveurs de noms indésirables de la liste, et également comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="d5028-153">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="d5028-154">> lorsque vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants : > ns1.bdm.microsoftonline.com > ns2.bdm.microsoftonline.com > ns3.bdm.microsoftonline.com > ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="d5028-154">>  When you have completed the steps in this section, the only nameservers that should be listed are these four: >  ns1.bdm.microsoftonline.com >  ns2.bdm.microsoftonline.com >  ns3.bdm.microsoftonline.com >  ns4.bdm.microsoftonline.com</span></span> 
  
1. <span data-ttu-id="d5028-155">Pour commencer, accédez à la page de vos domaines sur le site AWS en utilisant [ce lien](https://console.aws.amazon.com/route53/home).</span><span class="sxs-lookup"><span data-stu-id="d5028-155">To get started, go to your domains page at AWS by using [this link](https://console.aws.amazon.com/route53/home).</span></span> <span data-ttu-id="d5028-156">Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d5028-156">You'll be prompted to log in first.</span></span>
    
2. <span data-ttu-id="d5028-157">Sur la page **ressources** , sélectionnez **zones hébergées**.</span><span class="sxs-lookup"><span data-stu-id="d5028-157">On the **Resources** page, select **Hosted Zones**.</span></span>
    
3. <span data-ttu-id="d5028-158">Dans la page **zones hébergées** , dans la colonne **nom de domaine** , sélectionnez le nom du domaine à modifier.</span><span class="sxs-lookup"><span data-stu-id="d5028-158">On the **Hosted Zones** page, in the **Domain Name** column, select the name of the domain that you want to edit.</span></span> 
    
4. <span data-ttu-id="d5028-159">Sélectionnez le jeu d'enregistrement **Serveur de noms**.</span><span class="sxs-lookup"><span data-stu-id="d5028-159">Select the **Nameserver** record set.</span></span> 
    
    ![Select the recordset](../media/24e618e4-0a16-43a2-9886-f4f5dac79374.png)
  
5. <span data-ttu-id="d5028-161">Dans le jeu d'enregistrements **NS - Serveur de noms**, dans la zone **Valeur**, supprimez tous les serveurs de noms en les sélectionnant, puis en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="d5028-161">In the **NS - Name server** record set in the **Value** box, delete all of the nameservers by selecting them all and then pressing the **Delete** key on your keyboard.</span></span> 
    
    > [!CAUTION]
    > <span data-ttu-id="d5028-162">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span><span class="sxs-lookup"><span data-stu-id="d5028-162">Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="d5028-163">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="d5028-163">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span> 
  
    ![Select and delete all of the nameservers in the Value box](../media/ecf1e897-fa7d-4abc-b00b-bf55b8ed2139.png)
  
6. <span data-ttu-id="d5028-165">Dans la zone **TTL (secondes) :** , sélectionnez **1H** (1 heure).</span><span class="sxs-lookup"><span data-stu-id="d5028-165">In the **TTL (Seconds):** area, select **1h** (1 Hour).</span></span> 
    
    ![Sélectionner 1H pour une heure](../media/c70070e1-4bde-41a7-b271-9d22c475edf6.png)
  
7. <span data-ttu-id="d5028-167">Toujours dans le jeu d'enregistrements **NS - Serveur de noms**, dans la zone **Valeur**, tapez ou copiez-collez la valeur de la **première ligne** du tableau suivant, appuyez sur la touche **Entrée** du clavier, puis tapez ou copiez-collez la valeur de la **ligne** suivante.</span><span class="sxs-lookup"><span data-stu-id="d5028-167">Still in the **NS - Name server** record set, in the **Value** box, type or copy and paste the **First line** value from the following table, then press the **Enter** key on your keyboard and type or copy and paste the next **line** value.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="d5028-168">Chaque valeur de serveur de noms  *doit*  figurer sur sa propre ligne distincte dans la zone **Valeur**, comme dans l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d5028-168">Each nameserver value  *must*  be on its own separate line within the **Value** box, as shown in the following illustration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5028-169">**Première ligne**</span><span class="sxs-lookup"><span data-stu-id="d5028-169">**First line**</span></span> <br/> |<span data-ttu-id="d5028-170">ns1.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="d5028-170">ns1.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="d5028-171">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d5028-171">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="d5028-172">**Deuxième ligne**</span><span class="sxs-lookup"><span data-stu-id="d5028-172">**Second line**</span></span> <br/> |<span data-ttu-id="d5028-173">ns2.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="d5028-173">ns2.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="d5028-174">**This value MUST end with a period (.)**</span><span class="sxs-lookup"><span data-stu-id="d5028-174">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="d5028-175">**Troisième ligne**</span><span class="sxs-lookup"><span data-stu-id="d5028-175">**Third line**</span></span> <br/> |<span data-ttu-id="d5028-176">ns3.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="d5028-176">ns3.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="d5028-177">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="d5028-177">**This value MUST end with a period (.)**</span></span> <br/> |
|<span data-ttu-id="d5028-178">**Quatrième ligne**</span><span class="sxs-lookup"><span data-stu-id="d5028-178">**Fourth line**</span></span> <br/> |<span data-ttu-id="d5028-179">ns4.bdm.microsoftonline.com.</span><span class="sxs-lookup"><span data-stu-id="d5028-179">ns4.bdm.microsoftonline.com.</span></span>  <br/> <span data-ttu-id="d5028-180">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="d5028-180">**This value MUST end with a period (.)**</span></span> <br/> |
   
   ![Tapez ou collez la valeur de la première ligne dans la zone valeur.](../media/b63f41e0-51ef-4ab2-a4b8-ee7380e5ab35.png)
  
8. <span data-ttu-id="d5028-182">Sélectionnez **enregistrer le jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="d5028-182">Select **Save Record Set**.</span></span>
    
    ![Sélectionnez Enregistrer le jeu d’enregistrements](../media/ab3c0558-bb7c-41e4-871e-ea82f1553476.png)
  
> [!NOTE]
> <span data-ttu-id="d5028-p113">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures. Vous pourrez ensuite utiliser votre messagerie et les autres services Office 365 avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d5028-p113">Your nameserver record updates may take up to several hours to update across the Internet's DNS system. Then your Office 365 email and other services will be all set to work with your domain.</span></span> 
