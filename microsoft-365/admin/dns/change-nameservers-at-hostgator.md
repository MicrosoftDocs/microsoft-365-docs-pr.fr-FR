---
title: Modifier les serveurs de noms pour configurer Microsoft avec Hostgator
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
ms.assetid: f3bd3c62-0477-48e4-b2b5-21e329d67985
description: Découvrez comment configurer Microsoft pour gérer les enregistrements DNS de votre domaine personnalisé sur Hostgator.
ms.openlocfilehash: 09f0409ed2a5f81b450c9aae7bb3699373ce6f22
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629886"
---
# <a name="change-nameservers-to-set-up-microsoft-365-with-hostgator"></a><span data-ttu-id="d2e6d-103">Modifier les serveurs de noms pour configurer Microsoft 365 avec Hostgator</span><span class="sxs-lookup"><span data-stu-id="d2e6d-103">Change nameservers to set up Microsoft 365 with Hostgator</span></span>

 <span data-ttu-id="d2e6d-104">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-104">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span>
  
<span data-ttu-id="d2e6d-105">Suivez ces instructions si vous voulez que Microsoft gère vos enregistrements DNS pour vous.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-105">Follow these instructions if you want Microsoft to manage your DNS records for you.</span></span> <span data-ttu-id="d2e6d-106">(Si vous préférez, vous pouvez [gérer tous vos enregistrements DNS Microsoft sur Hostgator](create-dns-records-at-hostgator.md).)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-106">(If you prefer, you can [manage all your Microsoft DNS records at Hostgator](create-dns-records-at-hostgator.md).)</span></span>
  
    
## <a name="point-your-domain-to-your-hosting-account"></a><span data-ttu-id="d2e6d-107">Pointez votre domaine vers votre compte d'hébergement.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-107">Point your domain to your hosting account.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2e6d-108">Vous devez effectuer cette procédure avant d'effectuer celle décrite dans la section **Ajouter un enregistrement TXT de vérification)**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-108">You must perform this procedure before you perform the procedure in the following section, **Add a TXT record for verification**.</span></span>
  
<span data-ttu-id="d2e6d-109">Suivez ces étapes pour associer votre domaine et vos comptes d'hébergement.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-109">Follow these steps to associate your domain and hosting accounts.</span></span>
  
1. <span data-ttu-id="d2e6d-p102">Pour commencer, accédez à votre page du portail client sur le site Hostgator en utilisant [ce lien](https://portal.hostgator.com/domain/manage). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p102">To get started, go to your customer portal page at Hostgator by using [this link](https://portal.hostgator.com/domain/manage). You'll be prompted to log in.</span></span>
    
    ![Hostgator-BP-Redelegate-1-0](../../media/6749ac23-4832-4daf-8f3b-bc3b9b1b979c.png)
  
2. <span data-ttu-id="d2e6d-113">Sélectionnez l’onglet **domaines** .</span><span class="sxs-lookup"><span data-stu-id="d2e6d-113">Select the **Domains** tab.</span></span>
    
    ![Hostgator-BP-Redelegate-1-1](../../media/56d12bfd-3549-4033-90dc-077c76ca798c.png)
  
3. <span data-ttu-id="d2e6d-115">Sur la page **gérer les domaines** , dans la zone **Mes domaines** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-115">On the **Manage Domains** page, in the **My Domains** area, select the domain you want to update.</span></span>
    
    ![Hostgator-BP-Redelegate-1-2](../../media/2c2f8530-26a1-4e62-bb04-b3874bc1cf36.png)
  
4. <span data-ttu-id="d2e6d-117">Dans la page **vue d’ensemble des domaines** , dans la zone **serveurs de noms** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-117">On the **Domains Overview** page, in the **Name Servers** area, select **Change**.</span></span>
    
    ![Hostgator-BP-Redelegate-1-3](../../media/c8979d8a-ee96-4064-a8df-c5b01054cb16.png)
  
5. <span data-ttu-id="d2e6d-119">Sur la page **serveurs de noms** de votre domaine, dans la liste déroulante Sélectionner un compte d' **hébergement** , sélectionnez le compte d' **hébergement** associé à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-119">On the **Name Servers** page for your domain, in the **Select Hosting Account** drop-down list, choose the **hosting account** that is associated with your domain.</span></span>
    
    ![Hostgator-BP-Redelegate-1-4](../../media/4cf61060-1e8a-4758-9892-32059ffc90c2.png)
  
6. <span data-ttu-id="d2e6d-121">Sélectionnez **enregistrer les serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-121">Select **Save Name Servers**.</span></span>
    
    ![Hostgator-BP-Redelegate-1-9](../../media/b52a825a-6d54-49ba-87c8-52f770fdfa0c.png)
  
## <a name="add-a-txt-record-for-verification"></a><span data-ttu-id="d2e6d-123">Ajouter un enregistrement TXT à des fins de vérification</span><span class="sxs-lookup"><span data-stu-id="d2e6d-123">Add a TXT record for verification</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2e6d-124">Avant d’effectuer cette procédure, vous devez d’abord effectuer la procédure décrite dans la première section de cet article, [faire pointer votre domaine vers votre compte d’hébergement.](#point-your-domain-to-your-hosting-account).</span><span class="sxs-lookup"><span data-stu-id="d2e6d-124">Before you perform this procedure, you must first perform the procedure in the first section of this article, [Point your domain to your hosting account.](#point-your-domain-to-your-hosting-account).</span></span>
  
<span data-ttu-id="d2e6d-125">Avant d’utiliser votre domaine avec Microsoft, vous devez vous assurer que vous en êtes propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-125">Before you use your domain with Microsoft, we have to make sure that you own it.</span></span> <span data-ttu-id="d2e6d-126">Votre capacité à vous connecter à votre compte auprès de votre bureau d’enregistrement de domaines et à créer l’enregistrement DNS prouve à Microsoft que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-126">Your ability to log in to your account at your domain registrar and create the DNS record proves to Microsoft that you own the domain.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2e6d-p104">Cet enregistrement sert uniquement à vérifier que vous êtes propriétaire du domaine. Vous pouvez éventuellement le supprimer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p104">This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like.</span></span>
  
1. <span data-ttu-id="d2e6d-p105">Pour commencer, accédez à la page cPanel sur Hostgator. Avant toute chose, vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p105">To get started, go to your cPanel page at Hostgator. You'll be prompted to log in first.</span></span>
    
    <span data-ttu-id="d2e6d-p106">(Une adresse cPanel unique est affectée à chaque compte hébergé sur Hostgator. Votre adresse cPanel doit ressembler à ceci : https://YourSiteAddress:secure-port-numberéro-port-sécurisé. Le message d'inscription que vous avez reçu de Hostgator mentionne cette adresse.)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p106">(Each hosted account at Hostgator is assigned a unique cPanel address. Your cPanel address should look like this: https://YourSiteAddress:secure-port-number. The sign-up email you received from Hostgator will specify that address.)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="d2e6d-134">To have a cPanel associated with your domain, you need a hosting account with Hostgator.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-134">To have a cPanel associated with your domain, you need a hosting account with Hostgator.</span></span> <span data-ttu-id="d2e6d-135">Pour commencer, vous pouvez acheter un compte d’hébergement auprès de Hostgator ou [modifier les enregistrements de serveur de noms de votre domaine (NS)](#change-your-domains-nameserver-ns-records) de sorte qu’il pointe vers Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-135">To get started, you can either purchase a hosting account from Hostgator or [change your domain's nameserver (NS) records](#change-your-domains-nameserver-ns-records) to point to Microsoft.</span></span> 
  
2. <span data-ttu-id="d2e6d-136">Sur la page **panneau de configuration** , dans la zone **domaines** , sélectionnez **éditeur de zone DNS avancée**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-136">On the **Control Panel** page, in the **Domains** area, select **Advanced DNS Zone Editor**.</span></span>
    
    <span data-ttu-id="d2e6d-137">(You may have to scroll down.)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-137">(You may have to scroll down.)</span></span> 
    
3. <span data-ttu-id="d2e6d-138">On the **Advanced DNS Zone Editor** page, in the **Add a Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-138">On the **Advanced DNS Zone Editor** page, in the **Add a Record** area, in the boxes for the new record, type or copy and paste the values from the following table.</span></span> 
    
    <span data-ttu-id="d2e6d-139">(Choisissez la valeur **Type (Type)** dans la liste déroulante.)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-139">(Choose the **Type** value from the drop-down list.)</span></span> 
    
|||||
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d2e6d-140">**Name (Nom)**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-140">**Name**</span></span> <br/> |<span data-ttu-id="d2e6d-141">**TTL (Durée de vie)**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-141">**TTL**</span></span> <br/> |<span data-ttu-id="d2e6d-142">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-142">**Type**</span></span> <br/> |<span data-ttu-id="d2e6d-143">**TXT Data (Données TXT)**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-143">**TXT Data**</span></span> <br/> |
|<span data-ttu-id="d2e6d-p108">Utilisez votre  *nom_de_domaine*  (par exemple, fourthcoffee.com).</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p108">Use your  *domain_name*  . (for example, fourthcoffee.com.)  </span></span><br/> <span data-ttu-id="d2e6d-146">**Cette valeur DOIT se terminer par un point (.)**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-146">**This value MUST end with a period (.)**</span></span> <br/> |<span data-ttu-id="d2e6d-147">0,1</span><span class="sxs-lookup"><span data-stu-id="d2e6d-147">1</span></span>  <br/> |<span data-ttu-id="d2e6d-148">TXT</span><span class="sxs-lookup"><span data-stu-id="d2e6d-148">TXT</span></span>  <br/> |<span data-ttu-id="d2e6d-149">MS=ms *XXXXXXXX*</span><span class="sxs-lookup"><span data-stu-id="d2e6d-149">MS=ms *XXXXXXXX*</span></span>  <br/> <span data-ttu-id="d2e6d-150">**Remarque :** il s'agit d'un exemple.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-150">**Note:** This is an example.</span></span> <span data-ttu-id="d2e6d-151">Utilisez votre **adresse de destination ou de pointage** spécifique ici, à partir du tableau.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-151">Use your specific **Destination or Points to Address** value here, from the table.</span></span> [<span data-ttu-id="d2e6d-152">Comment trouver cette valeur ?</span><span class="sxs-lookup"><span data-stu-id="d2e6d-152">How do I find this?</span></span>](../get-help-with-domains/information-for-dns-records.md)     <br/>  |
   
4. <span data-ttu-id="d2e6d-153">Sélectionnez **Ajouter un enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-153">Select **Add Record**.</span></span>
    
5. <span data-ttu-id="d2e6d-154">Patientez quelques minutes, le temps que l'enregistrement que vous venez de créer soit mis à jour sur Internet.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-154">Wait a few minutes before you continue, so that the record you just created can update across the Internet.</span></span>
    
<span data-ttu-id="d2e6d-155">À présent que vous avez ajouté l’enregistrement sur le site de votre bureau d’enregistrement de domaines, vous allez retourner à Microsoft et demander une recherche pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-155">Now that you've added the record at your domain registrar's site, you'll go back to Microsoft and request a search for the record.</span></span>
  
<span data-ttu-id="d2e6d-156">Lorsque Microsoft trouve l’enregistrement TXT correct, votre domaine est vérifié.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-156">When Microsoft finds the correct TXT record, your domain is verified.</span></span>
  
1. <span data-ttu-id="d2e6d-157">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-157">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

    
2. <span data-ttu-id="d2e6d-158">Dans la page **Domaines**, sélectionnez le domaine que vous vérifiez.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-158">On the **Domains** page, select the domain that you are verifying.</span></span> 
    
3. <span data-ttu-id="d2e6d-159">Dans la page **Configuration**, sélectionnez **Démarrer la configuration**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-159">On the **Setup** page, select **Start setup**.</span></span>
    
4. <span data-ttu-id="d2e6d-160">Dans la page **Vérifier le domaine**, sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-160">On the **Verify domain** page, select **Verify**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d2e6d-161">Généralement, les modifications DNS sont appliquées dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-161">Typically it takes about 15 minutes for DNS changes to take effect.</span></span> <span data-ttu-id="d2e6d-162">Il peut toutefois arriver que la répercussion d’une modification dans le système DNS sur Internet prenne davantage de temps.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-162">However, it can occasionally take longer for a change you've made to update across the Internet's DNS system.</span></span> <span data-ttu-id="d2e6d-163">Si vous rencontrez des problèmes avec le flux de messagerie ou d’autres problèmes après avoir ajouté des enregistrements DNS, consultez [la rubrique Rechercher et corriger les problèmes après avoir ajouté votre domaine ou des enregistrements DNS](../get-help-with-domains/find-and-fix-issues.md).</span><span class="sxs-lookup"><span data-stu-id="d2e6d-163">If you're having trouble with mail flow or other issues after adding DNS records, see [Find and fix issues after adding your domain or DNS records](../get-help-with-domains/find-and-fix-issues.md).</span></span> 
  
## <a name="change-your-domains-nameserver-ns-records"></a><span data-ttu-id="d2e6d-164">Modifier les enregistrements de serveur de noms (NS) de votre domaine</span><span class="sxs-lookup"><span data-stu-id="d2e6d-164">Change your domain's nameserver (NS) records</span></span>

<span data-ttu-id="d2e6d-165">Pour terminer la configuration de votre domaine avec Microsoft, vous devez modifier les enregistrements de serveur de noms de votre domaine au niveau de votre bureau d’enregistrement de domaines afin de pointer vers les serveurs de noms principaux et secondaires Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-165">To complete setting up your domain with Microsoft, you change your domain's NS records at your domain registrar to point to the Microsoft primary and secondary name servers.</span></span> <span data-ttu-id="d2e6d-166">Cela permet à Microsoft de mettre à jour les enregistrements DNS du domaine pour vous.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-166">This sets up Microsoft to update the domain's DNS records for you.</span></span> <span data-ttu-id="d2e6d-167">Pour finaliser la configuration, nous ajouterons tous les enregistrements de façon à ce que vous puissiez utiliser la messagerie, Skype Entreprise Online et votre site web public avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-167">We'll add all records so that email, Skype for Business Online, and your public website work with your domain, and you'll be all set.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="d2e6d-168">Lorsque vous modifiez les enregistrements de serveur de noms de votre domaine pour qu’ils pointent vers les serveurs de noms Microsoft, tous les services actuellement associés à votre domaine sont affectés.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-168">When you change your domain's NS records to point to the Microsoft name servers, all the services that are currently associated with your domain are affected.</span></span> <span data-ttu-id="d2e6d-169">Par exemple, tous les messages électroniques envoyés à votre domaine (par exemple, rob@ *your_domain* . com) débuteront à Microsoft après avoir effectué cette modification.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-169">For example, all email sent to your domain (like rob@ *your_domain*  .com) will start coming to Microsoft after you make this change.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d2e6d-170">La procédure suivante montre comment supprimer tous les autres serveurs de noms indésirables de la liste, et également comment ajouter les serveurs de noms corrects s’ils ne sont pas déjà répertoriés.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-170">The following procedure will show you how to delete any other, unwanted nameservers from the list, and also how to add the correct nameservers if they are not already listed.</span></span> <span data-ttu-id="d2e6d-171">Une fois que vous avez effectué les étapes de cette section, les seuls serveurs de noms qui doivent être répertoriés sont les quatre suivants : **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**et **NS4.BDM.microsoftonline.com**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-171">When you have completed the steps in this section, the only nameservers that should be listed are these four:  **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, and **ns4.bdm.microsoftonline.com**.</span></span>
  
1. <span data-ttu-id="d2e6d-p114">Pour commencer, accédez à votre page du portail clients sur le site Hostgator en utilisant [ce lien](https://portal.hostgator.com/domain/manage). Vous serez invité à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-p114">To get started, go to your customer portal page at Hostgator by using [this link](https://portal.hostgator.com/domain/manage). You'll be prompted to log in.</span></span>
    
    ![Hostgator-BP-Redelegate-1-0](../../media/6749ac23-4832-4daf-8f3b-bc3b9b1b979c.png)
  
2. <span data-ttu-id="d2e6d-175">Sélectionnez l’onglet **domaines** .</span><span class="sxs-lookup"><span data-stu-id="d2e6d-175">Select the **Domains** tab.</span></span> 
    
    ![Hostgator-BP-Redelegate-1-1](../../media/56d12bfd-3549-4033-90dc-077c76ca798c.png)
  
3. <span data-ttu-id="d2e6d-177">Sur la page **gérer les domaines** , dans la zone **Mes domaines** , sélectionnez le domaine que vous souhaitez mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-177">On the **Manage Domains** page, in the **My Domains** area, select the domain you want to update.</span></span> 
    
    ![Hostgator-BP-Redelegate-1-2](../../media/2c2f8530-26a1-4e62-bb04-b3874bc1cf36.png)
  
4. <span data-ttu-id="d2e6d-179">Dans la page **vue d’ensemble du domaine** , dans la zone **serveurs de noms** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-179">On the **Domain Overview** page, in the **Name Servers** area, select **Change**.</span></span>
    
    ![Hostgator-BP-Redelegate-1-3](../../media/c8979d8a-ee96-4064-a8df-c5b01054cb16.png)
  
5. <span data-ttu-id="d2e6d-181">Sur la page **serveurs de noms** de votre domaine, dans la liste déroulante Sélectionner un compte d' **hébergement** , sélectionnez le compte d' **hébergement** associé à votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-181">On the **Name Servers** page for your domain, in the **Select Hosting Account** drop-down list, choose the **hosting account** that is associated with your domain.</span></span> 
    
    ![Hostgator-BP-Redelegate-1-4](../../media/4cf61060-1e8a-4758-9892-32059ffc90c2.png)
  
6. <span data-ttu-id="d2e6d-183">Sélectionnez **définir manuellement les serveurs mon nom**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-183">Select **Manually set my name servers**.</span></span>
    
    ![Hostgator-BP-Redelegate-1-5](../../media/5b73ae32-f26e-48aa-b5ad-6da20f1c491a.png)
  
7.   <span data-ttu-id="d2e6d-185">**Attention**: suivez ces étapes uniquement si vous avez des serveurs de noms existants autres que les quatre serveurs de noms corrects.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-185">**CAUTION**: Follow these steps only if you have existing nameservers other than the four correct nameservers.</span></span> <span data-ttu-id="d2e6d-186">(Autrement dit, supprimez uniquement les serveurs de noms en cours qui *ne sont pas* nommés **NS1.BDM.microsoftonline.com**, **ns2.BDM.microsoftonline.com**, **NS3.BDM.microsoftonline.com**ou **NS4.BDM.microsoftonline.com**.)</span><span class="sxs-lookup"><span data-stu-id="d2e6d-186">(That is, delete only any current nameservers that are  *not*  named **ns1.bdm.microsoftonline.com**, **ns2.bdm.microsoftonline.com**, **ns3.bdm.microsoftonline.com**, or **ns4.bdm.microsoftonline.com**.)</span></span>
  
        <span data-ttu-id="d2e6d-187">Toujours sur la page **Name Servers (Serveurs de noms)** pour votre domaine, dans la liste des serveurs de noms, supprimez les serveurs de noms individuellement dans la liste en les sélectionnant un par un et en appuyant sur la touche **Suppr** du clavier.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-187">Still on the **Name Servers** page for your domain, in the list of nameservers, delete each nameserver in the list by selecting it and then pressing the **Delete** key on your keyboard.</span></span> 
    
   ![Hostgator-BP-Redelegate-1-6](../../media/fa9820e7-28bb-4792-b16c-51e54d83feb1.png)
  
8. <span data-ttu-id="d2e6d-189">Toujours dans la liste des serveurs de noms, tapez ou copiez-collez les deux premières valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-189">Still in the list of nameservers, type or copy and paste the first two values from the following table.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="d2e6d-190">**Name server 1 (Serveur de noms 1) :**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-190">**Name Server 1:**</span></span> <br/> |<span data-ttu-id="d2e6d-191">ns1.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="d2e6d-191">ns1.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="d2e6d-192">**Name server 2 (Serveur de noms 2) :**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-192">**Name Server 2:**</span></span> <br/> |<span data-ttu-id="d2e6d-193">ns2.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="d2e6d-193">ns2.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="d2e6d-194">**Serveur de noms 3 :**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-194">**Name Server 3:**</span></span> <br/> |<span data-ttu-id="d2e6d-195">ns3.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="d2e6d-195">ns3.bdm.microsoftonline.com</span></span>  <br/> |
|<span data-ttu-id="d2e6d-196">**Serveur de noms 4 :**</span><span class="sxs-lookup"><span data-stu-id="d2e6d-196">**Name Server 4:**</span></span> <br/> |<span data-ttu-id="d2e6d-197">ns4.bdm.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="d2e6d-197">ns4.bdm.microsoftonline.com</span></span>  <br/> |
   
   ![Hostgator-BP-redelegate-1-7-1](../../media/a8c10aa7-30b0-4bc8-9596-20256d396274.png)
  
9. <span data-ttu-id="d2e6d-199">Ajoutez les autres valeurs de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-199">Add the other nameserver values.</span></span>
    
    <span data-ttu-id="d2e6d-200">Sélectionnez **(+)** ajouter, puis tapez ou copiez-collez la valeur de la ligne suivante du tableau dans la zone de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-200">Select **(+)** add, and then type or copy and paste the value from the next row of the table into the box for the record.</span></span> 
    
    <span data-ttu-id="d2e6d-201">Répétez cette procédure jusqu'à avoir créé les quatre enregistrements de serveur de noms.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-201">Repeat this process until you have created all four nameserver records.</span></span>
    
    ![Hostgator-BP-Redelegate-1-7-2](../../media/92159a39-e498-4220-9b0d-ae2e718c7fb9.png)
  
10. <span data-ttu-id="d2e6d-203">Sélectionnez **enregistrer les serveurs de noms**.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-203">Select **Save Name Servers**.</span></span>
    
    ![Hostgator-BP-Redelegate-1-8](../../media/bd6b0dfa-5d39-4805-970d-7ab153cff117.png)
  
> [!NOTE]
> <span data-ttu-id="d2e6d-205">L'application des modifications apportées à votre enregistrement de serveur de noms dans le système DNS sur Internet peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-205">Your nameserver record updates may take up to several hours to update across the Internet's DNS system.</span></span> <span data-ttu-id="d2e6d-206">Votre messagerie Microsoft et les autres services seront tous configurés pour fonctionner avec votre domaine.</span><span class="sxs-lookup"><span data-stu-id="d2e6d-206">Then your Microsoft email and other services will be all set to work with your domain.</span></span>
